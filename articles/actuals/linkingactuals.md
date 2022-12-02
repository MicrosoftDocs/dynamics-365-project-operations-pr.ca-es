---
title: 'Orígens de les transaccions: enllaçar els valors reals amb els seus orígens'
description: En aquest article s'explica com s'utilitza el concepte d'orígens de transacció per enllaçar els valors reals amb els registres originals, com ara registres d'entrada de temps, d'entrada de despesa o d'ús de materials.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f1beff392ddd449a930d38016ca6083fea97953b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921290"
---
# <a name="transaction-origins---link-actuals-to-their-source"></a>Orígens de les transaccions: enllaçar els valors reals amb els seus orígens

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

Els registres d'origen de les transaccions es creen per enllaçar els valors reals amb els seus orígens, com ara entrades de temps, entrades de despesa, registres d'ús de materials i factures de projecte.

A l'exemple següent es mostra el processament típic de les entrades de temps en un cicle de vida de projecte del Project Operations.

> ![Entrades de temps de processament al Project Operations.](media/basic-guide-17.png)
 
1. L'enviament d'una entrada de temps provoca la creació de dues línies de llibre diari: una per a cost i una per a vendes no facturades.
2. L'aprovació final de l'entrada de temps provoca la creació de dos valors reals: un per a cost i un per a vendes no facturades.
3. Quan l'usuari crea una factura de projecte, la transacció de línia de factura es crea mitjançant les dades del valor real de vendes no facturades.
4. Quan es confirma la factura, es creen dos valors reals nous: una reversió de vendes sense facturar i un valor real de vendes facturades.

Cada incidència d'aquest flux de treball de processament activa la creació de registres a l'entitat Origen de la transacció per ajudar-vos a construir un seguiment de relacions entre aquests registres creats a l'entrada de temps, la línia del llibre diari, el valor real i els detalls de línia de factura.

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


A la il·lustració següent es mostren els enllaços que es creen entre els valors reals i els seus orígens en diverses incidències fent servir l'exemple d'entrades de temps del Project Operations.

> ![Com s'enllacen els valors reals als registres d'origen al Project Operations.](media/TransactionOrigins.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
