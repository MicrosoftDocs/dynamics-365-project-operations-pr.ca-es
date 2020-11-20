---
title: Creació d'una factura proforma manual
description: En aquest tema, podreu obtenir informació sobre la creació d'una factura proforma.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 9d3c84664f1b0701db17f0c05654e0c99bb6c640
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128045"
---
# <a name="create-a-manual-proforma-invoice"></a>Creació d'una factura proforma manual

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

La facturació proporciona als administradors de projectes un segon nivell d'aprovació abans de crear factures per a clients. El primer nivell d'aprovació es completa quan s'aproven les entrades de temps i de despesa que envien els membres de l'equip del projecte.

El Dynamics 365 Project Operations no està dissenyat per generar factures de cara al client, pels motius següents:

- No conté informació tributària.
- No pot convertir altres monedes en la moneda de facturació mitjançant tipus de canvi configurats correctament.
- No pot donar format correctament a les factures per tal de poder imprimir-les.

En lloc d'això, podeu utilitzar un sistema financer o comptable per crear factures per al client que utilitzin la informació de les propostes de factura generades.

## <a name="creating-project-invoices"></a>Crear factures de projecte

Les factures de projecte es poden crear d'una en una o en massa. Podeu crear-les manualment o es poden configurar per tal que es generin en execucions automatitzades.

### <a name="manually-create-project-invoices"></a>Crear factures de projecte manualment 

Des de la pàgina de llista **Contractes del projecte**, podeu crear factures de projecte per separat per a cada contracte de projecte o podeu crear factures en massa per a diversos contractes de projecte.

Seguiu aquest pas per crear una factura per a un contracte de projecte específic.

- A la pàgina de llista **Contractes del projecte**, obriu un contracte de projecte i, a continuació, seleccioneu **Crea una factura**.

    Es genera una factura per a totes les transaccions del contracte de projecte seleccionat que tinguin un estat **Llest per facturar**. Aquestes transaccions inclouen temps, despeses, fites i línies de contracte basades en productes.

Seguiu aquests passos per crear factures de manera massiva.

1. A la pàgina de llista **Contractes del projecte**, seleccioneu un o diversos contractes de projecte per als quals heu de crear una factura i, a continuació, seleccioneu **Crea les factures del projecte**.

    Un missatge d'advertiment us informa que pot haver-hi un retard abans que es creïn les factures. El procés també es mostra.

2. Seleccioneu **D'acord** per tancar el quadre de missatge.

    Es genera una factura per a totes les transaccions en una línia de contracte que tinguin un estat **Llest per facturar**. Aquestes transaccions inclouen temps, despeses, fites i línies de contracte basades en productes.

3. Per visualitzar les factures generades, aneu a **Vendes** \> **Facturació** \> **Factures**. Veureu una factura per a cadascun dels contractes del projecte.

### <a name="set-up-automated-creation-of-project-invoices"></a>Configurar la creació automatitzada de factures de projecte 

Seguiu aquests passos per configurar una execució de factura automàtica.

1. Aneu a **Configuració** \> **Treballs per lots**.
2. Creeu un treball per lots i anomeneu-lo **Creació de factures del Project Operations**. El nom del treball per lots ha d'incloure el terme "Crea factures".
3. Al camp **Tipus de treball**, seleccioneu **Cap**. Per defecte, les opcions **Freqüència diària** i **Actiu** estan definides com a **Sí**.
4. Seleccioneu **Executa el flux de treball**. Al quadre de diàleg **Registre de cerca**, veureu tres fluxos de treball:

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. Seleccioneu **ProcessRunCaller** i després trieu **Afegeix**.
6. Al quadre de diàleg següent, seleccioneu **D'acord**. Un flux de treball **Repòs** va seguit d'un flux de treball **Procés**.

    També podeu seleccionar **ProcessRunner** al pas 5. Després, quan seleccioneu **D'acord**, un flux de treball **Procés** va seguit d'un flux de treball **Repòs**.

Els fluxos de treball **ProcessRunCaller** i **ProcessRunner** creen factures. **ProcessRunCaller** crida a **ProcessRunner**. **ProcessRunner** és el flux de treball que en realitat crea les factures. Passa per totes les línies de contracte per a les quals s'han de crear factures i crea factures d'aquestes línies. Per determinar les línies de contracte per a les quals s'han de crear factures, el treball consulta les dates d'execució de la factura per a les línies de contracte. Si les línies de contracte que pertanyen a un contracte tenen la mateixa data d'execució de la factura, les transaccions es combinen en una factura que té dues línies de factura. Si no hi ha cap transacció per a la qual crear factures, el treball omet la creació de la factura.

Després d'haver acabat d'executar-se **ProcessRunner**, crida a **ProcessRunCaller**, proporciona l'hora d'acabament i es tanca. **ProcessRunCaller** llavors inicia un temporitzador que s'executa durant 24 hores a partir de l'hora d'acabament especificada. Al final del temporitzador, **ProcessRunCaller** es tanca.

El treball de processament per lots per crear factures és una feina recurrent. Si aquest procés per lots s'executa moltes vegades, es creen diverses instàncies del treball que causen errors. Per tant, hauríeu d'iniciar el procés de processament per lots només una vegada i reiniciar-lo només si s'atura l'execució.

> [!NOTE]
> La facturació per lots només s'executa per a les línies de contracte del projecte que es configuren mitjançant planificacions de factura. Una línia de contracte amb un mètode de facturació de preu fix ha de tenir les fites configurades. Una línia de contracte de projecte amb un mètode de facturació de temps i material necessitarà una configuració de planificació de facturació basada en la data. El mateix s'aplica a una línia de contracte basada en projectes.      
 
### <a name="edit-a-draft-invoice"></a>Editar un esborrany de factura

Quan creeu un esborrany de factura, totes les transaccions de vendes no facturades que es van crear quan es van aprovar les entrades de temps i de despesa s'afegeixen a la factura. Podeu fer els ajustaments següents mentre la factura es manté en una fase d'esborrany:

- Suprimir o editar els detalls de la línia de factura.
- Editar i ajustar la quantitat i el tipus de facturació.
- Afegir directament temps, despeses i taxes com a transaccions a la factura. Podeu utilitzar aquesta característica si la línia de factura s'assigna a una línia de contracte que permet aquestes classes de transaccions.

Seleccioneu **Confirma** per confirmar una factura. L'acció de confirmació és una acció d'un sol sentit. Quan seleccioneu **Confirma**, el sistema fa que la factura sigui només de lectura i creï valors reals de vendes facturades des de cada detall de línia de factura per a cada línia de factura. Si el detall de la línia de factura fa referència a un valor real de vendes no facturades, el sistema també reinverteix el valor real de vendes no facturades. (Qualsevol detall de línia de factura que s'hagi creat des d'una entrada de compte o de despesa farà referència a un valor real de vendes sense facturar.) Els sistemes d'integració general de llibres poden utilitzar aquest canvi per revertir el treball en curs del projecte amb finalitats comptables.

### <a name="correct-a-confirmed-invoice"></a>Correcció d'una factura confirmada

Es poden editar (corregir) les factures confirmades. Quan corregiu una factura confirmada, es crea un nou esborrany de factura correctiva. Com que s'assumeix que voleu revertir totes les transaccions i quantitats de la factura original, aquesta factura correctiva inclou totes les transaccions de la factura original i totes les quantitats que hi ha són 0 (zero).

Si alguna transacció no requereix correcció, podeu eliminar-la de l'esborrany de factura correctiva. Si voleu revertir o retornar només una quantitat parcial, podeu editar el camp **Quantitat** al detall de la línia. Si obriu el detall de la línia de factura, podeu veure la quantitat original de la factura. A continuació, podeu editar la quantitat de la factura actual de manera que sigui inferior o superior a la quantitat original de la factura.

Quan es confirma una factura correctiva, es reverteix el valor real de vendes facturades original i es crea un nou valor real de vendes facturades. Si la quantitat s'ha reduït, la diferència provocarà que també s'hagi creat un nou valor real de venda no facturada. Per exemple, si les vendes facturades originals eren de vuit hores, i el detall de la línia de factura correctiva té una quantitat menor de sis hores, es reverteix la línia de vendes facturades originals i es creen dos nous valors reals:

- Un valor de vendes facturades durant sis hores.
- Un valor de vendes no facturades per a les dues hores restants. Aquesta transacció es pot facturar més tard o marcar com a no imputable, en funció de les negociacions amb el client.
