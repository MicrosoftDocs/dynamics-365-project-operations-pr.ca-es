---
title: Transaccions empresarials
description: En aquest tema es proporciona informació les transaccions empresarials.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 33c27acc6747c94d76892f41031adc46150da0e0
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6011539"
---
# <a name="business-transactions"></a>Transaccions empresarials

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Al Dynamics 365 Project Service Automation, la *transacció empresarial* és un concepte abstracte que no està representat per cap entitat. No obstant, alguns camps i processos comuns de les entitats estan dissenyats per utilitzar el concepte de transaccions empresarials. Les entitats següents utilitzen aquesta abstracció:

- Detalls de la línia d'oferta
- Detalls de la línia de contracte
- Línies d'estimació
- Línies del llibre diari
- Valors reals

D'aquestes entitats, els detalls de la línia d'oferta, els detalls de la línia de contracte i les línies d'estimació s'assignen a la fase d'estimació del cicle de vida del projecte. Les entitats Línies del llibre diari i Valors reals s'assignen a la fase d'execució del cicle de vida del projecte.

El PSA tracta els registres d'aquestes cinc entitats com a transaccions empresarials. L'única distinció és que els registres d'entitats que estan assignats a la fase d'estimació tenen la consideració de previsions financeres, mentre que els registres de les entitats assignades a la fase d'execució es consideren fets financers que ja s'han produït.

Per obtenir més informació, vegeu [Estimacions](estimates.md) i [Valors reals](actuals.md).

## <a name="concepts-that-are-unique-to-business-transactions"></a>Conceptes únics per a transaccions empresarials
Els conceptes següents són únics per al concepte de transaccions empresarials:

- Tipus de transacció
- Classe de la transacció
- Origen de la transacció
- Connexió de la transacció

### <a name="transaction-type"></a>Tipus de transacció

El tipus de transacció representa el cronometratge i el context de l'impacte financer d'un projecte. Està representat per un conjunt d'opcions que té els valors admesos següents al PSA:
- Cost
- Contracte de projecte
- Vendes no facturades
- Vendes facturades
- Vendes interorganitzatives
- Cost de la unitat de recursos

### <a name="transaction-class"></a>Classe de la transacció

La classe de la transacció representa els diferents tipus de costos que s'han incorregut en els projectes. Està representat per un conjunt d'opcions que té els valors admesos següents al PSA:

- Time
- Despesa
- Material
- Tarifa
- Fita
- Impost

El valor **Fita** s'utilitza normalment per la lògica empresarial per a la facturació a preu fix al PSA.

### <a name="transaction-origin"></a>Origen de la transacció

L'origen de les transaccions és una entitat que emmagatzema l'origen de cada transacció empresarial. A mesura que s'inicia l'execució d'un projecte, cada transacció empresarial donarà lloc a una altra transacció empresarial que, al seu torn, en crearà una altra i així successivament. L'entitat d'origen de les transaccions es va dissenyar per emmagatzemar dades sobre els orígens de cada transacció per ajudar a informar i fer-ne la traçabilitat. 

### <a name="transaction-connection"></a>Connexió de la transacció

La connexió de la transacció és una entitat que emmagatzema la relació entre dues transaccions empresarials similars, com ara els valors reals de vendes i costos relacionats, o les reversions de transaccions desencadenades per les activitats de facturació, com ara la confirmació o la correcció de factures.

En conjunt, Origen de la transacció i Connexió de la transacció us ajudaran a fer un seguiment de les relacions entre transaccions empresarials i accions que han tingut com a resultat la creació d'una transacció empresarial concreta.

### <a name="example-how-transaction-origin-works-with-transaction-connection"></a>Exemple: com funciona Origen de la transacció amb Connexió de la transacció

A l'exemple següent es mostra el processament típic de les entrades de temps en un cicle de vida de projecte del PSA.

> ![Processament d'entrades de temps en un cicle de vida del Project Service](media/basic-guide-17.png)
 
1. La presentació d'una entrada de temps provoca la creació de dues línies de llibre diari: una per a un cost i una per a les vendes no facturades.
2. L'aprovació final de la entrada de temps provoca la creació de dos valors reals: un per a un cost i un per a les vendes no facturades.
3. Quan l'usuari crea una factura de projecte, la transacció de línia de factura es crea mitjançant les dades del valor real de vendes no facturades. 
4. Quan es confirma la factura, es creen dos valors reals nous: una reversió de vendes sense facturar i un valor real de vendes facturades.

Cadascun d'aquests esdeveniments activa la creació de registres a les entitats Origen de la transacció i Connexió de la transacció per ajudar-vos a construir un seguiment de relacions entre aquests registres creats a l'entrada de l'hora, la línia del llibre diari, els valors reals i els detalls de línia de factura.

A la taula següent es mostren els registres de l'entitat Origen de la transacció per al flux de treball anterior.

| Incidència                        | Origen                   | Tipus d'origen                       | Transacció                       | Tipus de transacció         |
|------------------------------|--------------------------|-----------------------------------|-----------------------------------|--------------------------|
| Enviament d'entrada de temps        | GUID de registre d'entrada de temps   | Entrada de temps                        | GUID de registre de línia del llibre diari (cost)   | Línia del llibre diari             |
| GUID de registre d'entrada de temps       | Entrada de temps               | GUID de registre de línia del llibre diari (vendes)  | Línia del llibre diari                      |                          |
| Aprovació de temps                | GUID de registre de línia del llibre diari | Línia del llibre diari                      | GUID del registre de vendes no facturades        | Real                   |
| GUID de registre d'entrada de temps       | Entrada de temps               | GUID del registre de vendes no facturades        | Real                            |                          |
| GUID de registre de línia del llibre diari     | Línia del llibre diari             | GUID de registre de valor real de cost           | Real                            |                          |
| GUID de registre d'entrada de temps       | Entrada de temps               | GUID de registre de valor real de cost           | Real                            |                          |
| Creació de la factura             | GUID de registre d'entrada de temps   | Entrada de temps                        | GUID de transacció de la línia de factura     | Transacció de la línia de factura |
| GUID de registre de línia del llibre diari     | Línia del llibre diari             | GUID de transacció de la línia de factura     | Transacció de la línia de factura          |                          |
| Confirmació de la factura         | GUID de línia de factura        | Línia de factura                      | GUID del registre de vendes facturades          | Real                   |
| GUID de la factura                 | Factura                  | GUID del registre de vendes facturades          | Real                            |                          |
| GUID del detall de la línia de factura     | Detall de la línia de factura      | GUID del registre de vendes facturades          | Real                            |                          |
| GUID de registre d'entrada de temps       | Entrada de temps               | GUID del registre de vendes facturades          | Real                            |                          |
| GUID de registre de línia del llibre diari     | Línia del llibre diari             | GUID del registre de vendes facturades          | Real                            |                          |
| GUID de registre d'entrada de temps       | Entrada de temps               | GUID de la reversió de vendes no facturades      | Real                            |                          |
| GUID de registre de línia del llibre diari     | Línia del llibre diari             | GUID de la reversió de vendes no facturades      | Real                            |                          |
| Correcció d'esborrany de factura     | GUID de descripció de línia de factura antic             | Transacció de la línia de factura          | GUID de descripció de línia de factura de correcció               | Transacció de la línia de factura |
| GUID de línia de factura antic                  | Línia de factura             | GUID de descripció de línia de factura de correcció               | Transacció de la línia de factura          |                          |
| GUID de factura antic             | Factura                  | GUID de descripció de línia de factura de correcció               | Transacció de la línia de factura          |                          |
| GUID de registre d'entrada de temps       | Entrada de temps               | GUID de descripció de línia de factura de correcció               | Transacció de la línia de factura          |                          |
| GUID de registre de línia del llibre diari     | Línia del llibre diari             | GUID de descripció de línia de factura de correcció               | Transacció de la línia de factura          |                          |
| Correcció de factura confirmada | GUID de descripció de línia de factura antic             | Transacció de la línia de factura          | GUID de valor real de vendes facturades invertides | Real                   |
| GUID de línia de factura antic                  | Línia de factura             | GUID de valor real de vendes facturades invertides | Real                            |                          |
| GUID de factura antic             | Factura                  | GUID de valor real de vendes facturades invertides | Real                            |                          |
| GUID de registre d'entrada de temps       | Entrada de temps               | GUID de valor real de vendes facturades invertides | Real                            |                          |
| GUID de registre de línia del llibre diari     | Línia del llibre diari             | GUID de valor real de vendes facturades invertides | Real                            |                          |
| GUID de descripció de línia de factura antic                 | Transacció de la línia de factura | GUID del valor real de vendes no facturades nou    | Real                            |                          |
| GUID de línia de factura antic                  | Línia de factura             | GUID del valor real de vendes no facturades nou    | Real                            |                          |
| GUID de factura antic             | Factura                  | GUID del valor real de vendes no facturades nou    | Real                            |                          |
| GUID de registre d'entrada de temps       | Entrada de temps               | GUID del valor real de vendes no facturades nou    | Real                            |                          |
| GUID de registre de línia del llibre diari     | Línia del llibre diari             | GUID del valor real de vendes no facturades nou    | Real                            |                          |
| GUID de descripció de línia de factura de correcció          | Transacció de la línia de factura | GUID del valor real de vendes no facturades nou    | Real                            |                          |
| GUID de línia de factura de correcció           | Línia de factura             | GUID del valor real de vendes no facturades nou    | Real                            |                          |
| GUID de la factura de correcció      | Factura                  | GUID del valor real de vendes no facturades nou    | Real                            |                          |

A la taula següent es mostren els registres de l'entitat Connexió de la transacció per al flux de treball anterior.

| Incidència                          | Transacció 1                 | Funció de la transacció 1 | Tipus de la transacció 1           | Transacció 2                | Funció de la transacció 2 | Tipus de la transacció 2 |
|--------------------------------|-------------------------------|--------------------|------------------------------|------------------------------|--------------------|--------------------|
| Enviament d'entrada de temps          | GUID de línia del llibre diari (Vendes)     | Vendes no facturades     | msdyn_journalline            | GUID de de línia del llibre diari (cost)     | Cost               | msdyn_journalline  |
| Aprovació de temps                  | GUID de valor real no facturat (vendes)  | Vendes no facturades     | msdyn_actual                 | GUID del valor real del cost (cost)       | Cost               | msdyn_actual       |
| Creació de la factura               | GUID del detall de la línia de factura      | Vendes facturades       | msdyn_invoicelinetransaction | GUID de valor real de vendes no facturades   | Vendes no facturades     | msdyn_actual       |
| Confirmació de la factura           | GUID del valor real de reversió         | Reversió          | msdyn_actual                 | GUID de vendes no facturades original | Original           | msdyn_actual       |
| GUID de vendes facturades              | Vendes facturades                  | msdyn_actual       | GUID de valor real de vendes no facturades   | Vendes no facturades               | msdyn_actual       |                    |
| Correcció d'esborrany de factura       | GUID de transacció de la línia de factura | Reemplaçament          | msdyn_invoicelinetransaction | GUID de vendes facturades            | Original           | msdyn_actual       |
| Correcció de confirmació de factura     | GUID de la reversió de vendes facturades    | Reversió          | msdyn_actual                 | GUID de vendes facturades            | Original           | msdyn_actual       |
| GUID del valor real de vendes no facturades nou | Reemplaçament                     | msdyn_actual       | GUID de vendes facturades            | Original                     | msdyn_actual       |                    |


[!INCLUDE[footer-include](../includes/footer-banner.md)]