---
title: Factures proforma del projecte
description: Aquest article proporciona informació sobre la les factures proforma del projecte a Project Operations.
author: rumant
ms.date: 04/06/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 8f028ec12aa3144a2c1bf13f6f8ce90c9de48519
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8934538"
---
# <a name="proforma-project-invoices"></a>Factures proforma del projecte

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_

La facturació proforma del projecte és útil perquè proporciona als administradors de projectes un segon nivell d'aprovació abans de crear factures per a clients. El primer nivell d'aprovació es completa quan s'aproven les entrades de temps, despeses i materials que envien els membres de l'equip del projecte.

La implementació bàsica del Dynamics 365 Project Operations no està dissenyada per generar factures orientades al client. A la llista següent es mostra la raó per la qual no es poden generar factures:

- No conté informació tributària.
- No es poden convertir altres monedes a la moneda de facturació.
- Les factures no es poden formatar correctament per imprimir-les.

En lloc d'això, podeu utilitzar un sistema financer o comptable per crear factures per al client que utilitzin la informació de les propostes de factura generades.

## <a name="creating-project-invoices"></a>Crear factures de projecte

Les factures de projecte es poden crear d'una en una o en massa. Podeu crear-les manualment o es poden configurar per tal que es generin en execucions automatitzades.

### <a name="manually-create-project-invoices"></a>Crear factures de projecte manualment 

A la pàgina de llista **Contractes del projecte**, podeu crear factures de projecte per separat per a cada contracte de projecte o podeu crear factures en massa per a diversos contractes de projecte.

   - Per crear una factura per a un contracte d'un projecte específic, a la pàgina de llista **Contractes del projecte**, obriu un contracte de projecte i, a continuació, seleccioneu **Crea una factura**.

   Es genera una factura per a totes les transaccions del contracte de projecte seleccionat que tinguin un estat **Llest per facturar**. Aquestes transaccions inclouen el temps, les despeses, els materials, les fites, les línies de contracte basades en productes i altres línies del llibre diari de vendes no facturades que es puguin haver confirmat.

Per crear factures massivament:

1. A la pàgina de llista **Contractes del projecte**, seleccioneu un o diversos contractes de projecte per crear una factura i, a continuació, seleccioneu **Crea les factures del projecte**.
2. Un missatge d'advertiment us informa que pot haver-hi un retard abans que es creïn les factures. El procés també es mostra. Seleccioneu **D'acord** per tancar el quadre de missatge.

   Es genera una factura per a totes les transaccions en una línia de contracte que tinguin un estat **Llest per facturar**. Aquestes transaccions inclouen el temps, les despeses, els materials, les fites, les línies de contracte basades en productes i altres línies del llibre diari de vendes no facturades que es puguin haver confirmat.

3. Visualitzeu les factures generades anant a **Vendes** \> **Facturació** \> **Factures**. Veureu una factura per a cadascun dels contractes del projecte.

### <a name="set-up-automated-creation-of-project-invoices"></a>Configurar la creació automatitzada de factures de projecte 

Seguiu aquests passos per configurar una execució de factura automàtica.

1. Aneu a **Configuració** \> **Treballs per lots**.
2. Creeu un treball per lots i anomeneu-lo **Creació de factures del Project Operations**. El nom del treball per lots ha d'incloure el terme "Crea factures".
3. Al camp **Tipus de treball**, seleccioneu **Cap**. Per defecte, les opcions **Freqüència diària** i **Actiu** estan definides com a **Sí**.
4. Seleccioneu **Executa el flux de treball**. Al quadre de diàleg **Registre de cerca**, veureu els fluxos de treball següents:

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. Seleccioneu **ProcessRunCaller** i després trieu **Afegeix**.
6. Al quadre de diàleg següent, seleccioneu **D'acord**. Un flux de treball **Repòs** va seguit d'un flux de treball **Procés**.

    També podeu seleccionar **ProcessRunner** al pas 5. Després, quan seleccioneu **D'acord**, un flux de treball **Procés** va seguit d'un flux de treball **Repòs**.

Els fluxos de treball **ProcessRunCaller** i **ProcessRunner** creen factures. **ProcessRunCaller** crida a **ProcessRunner**. **ProcessRunner** és el flux de treball que crea les factures. Aquest flux de treball passa per totes les línies de contracte per a les quals s'han de crear factures i crea les factures. Per determinar les línies de contracte per a les quals s'han de crear factures, el flux de treball consulta les dates d'execució de la factura per a les línies de contracte. Si les línies de contracte que pertanyen a un contracte tenen la mateixa data d'execució de la factura, les transaccions es combinen en una factura que té dues línies de factura. Si no hi ha cap transacció per a la qual crear factures, no es creen factures.

Després d'haver acabat d'executar-se **ProcessRunner**, crida a **ProcessRunCaller**, proporciona l'hora d'acabament i es tanca. **ProcessRunCaller** llavors inicia un temporitzador que s'executa durant 24 hores a partir de l'hora d'acabament especificada. Al final del temporitzador, **ProcessRunCaller** es tanca.

El treball de processament per lots per crear factures és una feina recurrent. Si aquest procés per lots s'executa moltes vegades, es creen diverses instàncies del treball i poden causar errors. Per resoldre aquest problema, inicieu el procés de processament per lots només una vegada i reinicieu-lo només si s'atura l'execució.

> [!NOTE]
> La facturació per lots només s'executa per a les línies de contracte del projecte que es configuren mitjançant planificacions de factura. Una línia de contracte amb un mètode de facturació de preu fix ha de tenir les fites configurades. Una línia de contracte de projecte amb un mètode de facturació de temps i material necessitarà una configuració de planificació de facturació basada en la data. El mateix s'aplica a una línia de contracte basada en projectes.      
 
### <a name="edit-a-draft-invoice"></a>Editar un esborrany de factura

Quan creeu un esborrany de factura, totes les transaccions de vendes no facturades que es van crear quan es van aprovar les entrades de temps i de despesa s'afegeixen a la factura. Podeu fer els ajustaments següents mentre la factura es manté en una fase d'esborrany:

- Suprimir o editar els detalls de la línia de factura.
- Editar i ajustar la quantitat i el tipus de facturació.
- Afegiu directament temps, despeses, material i taxes com a transaccions a la factura. Podeu utilitzar aquesta característica si la línia de factura s'assigna a una línia de contracte que permet aquestes classes de transaccions.

Seleccioneu **Confirma** per confirmar una factura. Aquesta acció de confirmació és una acció d'un sol sentit. Quan seleccioneu **Confirma**, la factura passa a ser només de lectura i crea valors reals de vendes facturades des de cada detall de línia de factura per a cada línia de factura. Si el detall de la línia de factura fa referència a un valor real de vendes no facturades, s'inverteix el valor real de vendes no facturades. Tots els detalls de la línia de factura creats a partir d'una entrada de temps, despesa o ús de materials faran referència a una venda real no facturada. Els sistemes d'integració de llibre major general poden utilitzar aquesta reversió per invertir el treball en curs (WIP) del projecte per a la comptabilitat.

### <a name="correct-a-confirmed-invoice"></a>Correcció d'una factura confirmada

Es poden editar les factures confirmades. Quan corregiu una factura confirmada, es crea un nou esborrany de factura correctiva. Com que s'assumeix que voleu revertir totes les transaccions i quantitats de la factura original, aquesta factura de correcció inclou totes les transaccions de la factura original i totes les quantitats que hi ha són zero.

Si hi ha transaccions que no requereixen cap correcció, podeu eliminar-les de l'esborrany de factura de correcció. Si voleu revertir o retornar només una quantitat parcial, podeu editar el camp **Quantitat** al detall de la línia. Si obriu el detall de la línia de factura, podeu veure la quantitat original de la factura. A continuació, podeu editar la quantitat de la factura actual de manera que sigui inferior o superior a la quantitat original de la factura.

Quan es confirma una factura correctiva, es reverteix el valor real de vendes facturades original i es crea un nou valor real de vendes facturades. Si la quantitat s'ha reduït, la diferència provocarà que també es creï un nou valor real de venda no facturada. Per exemple, si les vendes facturades originals eren de vuit hores, i el detall de la línia de factura correctiva té una quantitat menor de sis hores, es reverteix la línia de vendes facturades originals i es creen dos nous valors reals:

- Un valor de vendes facturades durant sis hores.
- Un valor de vendes no facturades per a les dues hores restants. Aquesta transacció es pot facturar més tard o marcar-la com a no imputable, en funció de les negociacions amb el client.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
