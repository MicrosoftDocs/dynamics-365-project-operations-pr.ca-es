---
title: Enllaçar els valors reals als registres originals
description: En aquest tema s'explica com enllaçar els valors reals amb els registres originals, com ara l'entrada de temps, l'entrada de despesa o els registres d'ús de materials.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b5a70d2c2b3f98028b4e4998ed25ab73a275c66e4b8137eb573b943658a1a41e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6991744"
---
# <a name="link-actuals-to-original-records"></a>Enllaçar els valors reals als registres originals

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_


Al Dynamics 365 Project Operations, una *transacció empresarial* és un concepte abstracte que no està representat per una entitat. No obstant, alguns camps i processos comuns de les entitats estan dissenyats per utilitzar el concepte de transaccions empresarials. Les entitats següents utilitzen aquest concepte:

- Detalls de la línia d'oferta
- Detalls de la línia de contracte
- Línies d'estimació
- Línies del llibre diari
- Valors reals

D'aquestes entitats, els **Detalls de la línia d'oferta**, els **Detalls de la línia de contracte** i les **Línies d'estimació** s'assignen a la fase d'estimació del cicle de vida del projecte. Les **Línies del llibre diari** i les **Entitats de valors reals** s'assignen a la fase d'execució del cicle de vida del projecte.

El Project Operations reconeix els registres d'aquestes cinc entitats com a transaccions empresarials. L'única distinció és que els registres de les entitats que estan assignats a la fase d'estimació tenen la consideració de previsions financeres, mentre que els registres de les entitats assignades a la fase d'execució es consideren fets financers que ja s'han produït.

## <a name="concepts-that-are-unique-to-business-transactions"></a>Conceptes únics per a transaccions empresarials
Els conceptes següents són únics per al concepte de transaccions empresarials:

- Tipus de transacció
- Classe de la transacció
- Origen de la transacció
- Connexió de la transacció

### <a name="transaction-type"></a>Tipus de transacció

El tipus de transacció representa el cronometratge i el context de l'impacte financer d'un projecte. Això està representat per un conjunt d'opcions que té els valors admesos següents al Project Operations:

  - Cost
  - Contracte de projecte
  - Vendes no facturades
  - Vendes facturades
  - Vendes interorganitzatives
  - Cost de la unitat de recursos

### <a name="transaction-class"></a>Classe de la transacció

La classe de la transacció representa els diferents tipus de costos que s'han incorregut en els projectes. Això està representat per un conjunt d'opcions que té els valors admesos següents al Project Operations:

  - Temps
  - Despesa
  - Material
  - Tarifa
  - Fita
  - Impostos

El valor **Fita** s'utilitza normalment per la lògica empresarial per a la facturació a preu fix al Project Operations.

### <a name="transaction-origin"></a>Origen de la transacció

L'**Origen de la transacció** és una entitat que emmagatzema l'origen de cada transacció empresarial. Quan es posa en marxa un projecte, cada transacció comercial generarà una altra transacció comercial, la qual cosa, al seu torn, en crearà una altra. L'entitat d'origen de la transacció està dissenyada per emmagatzemar dades sobre l'origen de cada transacció per ajudar en els informes i la traçabilitat. 

### <a name="transaction-connection"></a>Connexió de la transacció

La **Connexió de la transacció** és una entitat que emmagatzema la relació entre dues transaccions empresarials similars, com ara els valors reals de vendes i costos relacionats, o les reversions de transaccions desencadenades per les activitats de facturació, com ara la confirmació o la correcció de factures.

En conjunt, **Origen de la transacció** i **Connexió de la transacció** us ajudaran a fer un seguiment de les relacions entre transaccions empresarials i accions que han tingut com a resultat una transacció empresarial concreta.

### <a name="example-how-transaction-origin-works-with-transaction-connection"></a>Exemple: com funciona Origen de la transacció amb Connexió de la transacció

A l'exemple següent es mostra el processament típic de les entrades de temps en un cicle de vida de projecte del Project Operations.

> ![Processament d'entrades de temps en un cicle de vida del Project Service.](media/basic-guide-17.png)
 
1. La presentació d'una entrada de temps fa que es creïn dues línies de llibre diari: una per al cost i una altra per a les vendes no facturades.
2. L'aprovació final de l'entrada de temps fa que es creïn dos valors reals: un per al cost i un altre per a les vendes no facturades.
3. Quan es crea una factura de projecte nova, la transacció de línia de factura es crea mitjançant les dades del valor real de vendes no facturades. 
4. Quan es confirma la factura, es creen dos valors reals nous: un valor real de reversió de vendes sense facturar i un valor real de vendes facturades.

Cadascuna d'aquestes incidències crea un registre a les entitats **Origen de la transacció** i **Connexió de la transacció**. Aquests registres nous ajuden a crear un historial de relacions entre els registres que es creen en l'entrada de temps, la línia de llibre diari, els valors reals i els detalls de la línia de factura.

A la taula següent es mostren els registres de l'entitat **Origen de la transacció** per al flux de treball.

| Esdeveniment                        | Origen                   | Tipus d'origen                       | Transacció                       | Tipus de transacció         |
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

A la taula següent es mostren els registres de l'entitat **Connexió de la transacció** per al flux de treball.

| Esdeveniment                          | Transacció 1                 | Funció de la transacció 1 | Tipus de la transacció 1           | Transacció 2                | Funció de la transacció 2 | Tipus de la transacció 2 |
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
