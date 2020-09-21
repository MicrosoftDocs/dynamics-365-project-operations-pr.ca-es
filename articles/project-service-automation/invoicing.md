---
title: Facturació al Project Service Automation
description: Aquest tema proporciona informació sobre la facturació.
author: rumant
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 03/11/2019
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365  Project Service Automation 2.x and 3.x
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 8d95f17aba0a4cab65a6f020aade5e19568de3be
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749419"
---
# <a name="invoicing-in-project-service-automation"></a>Facturació al Project Service Automation

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

La facturació al Dynamics 365 Project Service Automation és útil perquè proporciona als administradors de projectes un segon nivell d'aprovació abans de crear factures per a clients. El primer nivell d'aprovació es completa quan s'aproven les entrades de temps i de despesa que envien els membres de l'equip del projecte.

El PSA no està dissenyat per generar factures de cara al client, pels motius següents:

- No conté informació tributària.
- No pot convertir altres monedes en la moneda de facturació mitjançant tipus de canvi configurats correctament.
- No pot donar format correctament a les factures per tal de poder imprimir-les.

En lloc d'això, podeu utilitzar un sistema financer o comptable per crear factures per al client que utilitzin la informació de les propostes de factura generades al PSA.

## <a name="creating-project-invoices-in-psa"></a>Crea factures de projecte al PSA

Les factures de projecte es poden crear d'una en una o en massa. Podeu crear-les manualment o es poden configurar per tal que es generin en execucions automatitzades.

### <a name="manually-create-project-invoices-in-psa"></a>Crear factures de projecte manualment al PSA

Des de la pàgina de llista **Contractes del projecte**, podeu crear factures de projecte per separat per a cada contracte de projecte o podeu crear factures en massa per a diversos contractes de projecte.

Seguiu aquest pas per crear una factura per a un contracte de projecte específic.

- A la pàgina de llista **Contractes del projecte**, obriu un contracte de projecte i, a continuació, seleccioneu **Crea una factura**.

    ![Crear factures de projecte per a un contracte específic de projecte](media/CreateProjectInvoicesOneByOne.png)

    Es genera una factura per a totes les transaccions del contracte de projecte seleccionat que tinguin un estat **Llest per facturar**. Aquestes transaccions inclouen temps, despeses, fites i línies de contracte basades en productes.

Seguiu aquests passos per crear factures de manera massiva.

1. A la pàgina de llista **Contractes del projecte**, seleccioneu un o diversos contractes de projecte per als quals heu de crear una factura i, a continuació, seleccioneu **Crea les factures del projecte**.

    ![Crear factures de projecte en massa](media/CreateProjectInvoicesBulk.png)

    Un missatge d'advertiment us informa que pot haver-hi un retard abans que es creïn les factures. El procés també es mostra.

2. Seleccioneu **D'acord** per tancar el quadre de missatge.

    Es genera una factura per a totes les transaccions en una línia de contracte que tinguin un estat **Llest per facturar**. Aquestes transaccions inclouen temps, despeses, fites i línies de contracte basades en productes.

3. Per visualitzar les factures generades, aneu a **Vendes** \> **Facturació** \> **Factures**. Veureu una factura per a cadascun dels contractes del projecte.

### <a name="set-up-automated-creation-of-project-invoices-in-psa"></a>Configurar la creació automatitzada de factures de projecte al PSA

Seguiu aquests passos per configurar una factura automàtica que s'executi al PSA.

1. Aneu a **Project Service** \> **Configuració** \> **Treballs per lots**.
2. Creeu un treball per lots i anomeneu-lo **Crea factures del PSA**. El nom del treball per lots ha d'incloure el terme "Crea factures".
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
 
### <a name="edit-a-draft-psa-invoice"></a>Editar un esborrany de factura del PSA

Quan creeu un esborrany de factura, totes les transaccions de vendes no facturades que es van crear quan es van aprovar les entrades de temps i de despesa s'afegeixen a la factura. Podeu fer els ajustaments següents mentre la factura es manté en una fase d'esborrany:

- Suprimir o editar els detalls de la línia de factura.
- Editar i ajustar la quantitat i el tipus de facturació.
- Afegir directament temps, despeses i taxes com a transaccions a la factura. Podeu utilitzar aquesta característica si la línia de factura s'assigna a una línia de contracte que permet aquestes classes de transaccions.

Seleccioneu **Confirma** per confirmar una factura. L'acció de confirmació és una acció d'un sol sentit. Quan seleccioneu **Confirma**, el sistema fa que la factura sigui només de lectura i creï valors reals de vendes facturades des de cada detall de línia de factura per a cada línia de factura. Si el detall de la línia de factura fa referència a un valor real de vendes no facturades, el sistema també reinverteix el valor real de vendes no facturades. (Qualsevol detall de línia de factura que s'hagi creat des d'una entrada de compte o de despesa farà referència a un valor real de vendes sense facturar.) Els sistemes d'integració general de llibres poden utilitzar aquest canvi per revertir el treball en curs del projecte amb finalitats comptables.

### <a name="correct-a-confirmed-psa-invoice"></a>Correcció d'una factura confirmada al PSA

Es poden editar (corregir) les factures del PSA confirmades. Quan corregiu una factura confirmada, es crea un nou esborrany de factura correctiva. Com que s'assumeix que voleu revertir totes les transaccions i quantitats de la factura original, aquesta factura correctiva inclou totes les transaccions de la factura original i totes les quantitats que hi ha són 0 (zero).

Si alguna transacció no requereix correcció, podeu eliminar-la de l'esborrany de factura correctiva. Si voleu revertir o retornar només una quantitat parcial, podeu editar el camp **Quantitat** al detall de la línia. Si obriu el detall de la línia de factura, podeu veure la quantitat original de la factura. A continuació, podeu editar la quantitat de la factura actual de manera que sigui inferior o superior a la quantitat original de la factura.

Quan es confirma una factura correctiva, es reverteix el valor real de vendes facturades original i es crea un nou valor real de vendes facturades. Si la quantitat s'ha reduït, la diferència provocarà que també s'hagi creat un nou valor real de venda no facturada. Per exemple, si les vendes facturades originals va ser de vuit hores, i el detall de la línia de factura correctiva té una quantitat menor de sis hores, el PSA reverteix la línia de vendes facturades originals i crea dos nous valors reals:

- Un valor de vendes facturades durant sis hores.
- Un valor de vendes no facturades per a les dues hores restants. Aquesta transacció es pot facturar més tard o marcar com a no imputable, en funció de les negociacions amb el client.
