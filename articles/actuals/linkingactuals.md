---
title: 'Orígens de les transaccions: enllaça els reals amb la seva font'
description: Aquest tema explica com el concepte d'orígens de transacció s'utilitza per enllaçar els reals als registres d'origen originals, com ara l'entrada de temps, l'entrada de despeses o els registres d'ús de material.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 908f78f7d58ec4b18f37d03b6fa7c4e2295491fa
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584814"
---
# <a name="transaction-origins---link-actuals-to-their-source"></a>Orígens de les transaccions: enllaça els reals amb la seva font

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

Els registres d'origen de la transacció es creen per enllaçar els reals a la seva font, com ara entrades de temps, entrades de despeses, registres d'ús de material i factures del projecte.

A l'exemple següent es mostra el processament típic de les entrades de temps en un cicle de vida de projecte del Project Operations.

> ![Temps de processament sencers en operacions de projectes.](media/basic-guide-17.png)
 
1. L'enviament d'una entrada de temps fa que es creï dues línies de diari: una per al cost i una altra per a les vendes no blanques.
2. L'aprovació definitiva de l'entrada de temps fa que es creï dos reals: un per al cost i un altre per a les vendes nobilades.
3. Quan l'usuari crea una factura de projecte, la transacció de línia de factura es crea mitjançant les dades del valor real de vendes no facturades.
4. Quan es confirma la factura, es creen dos valors reals nous: una reversió de vendes sense facturar i un valor real de vendes facturades.

Cada esdeveniment d'aquest flux de treball de processament activa la creació de registres a l'entitat Origen de la transacció per ajudar a crear un rastre de les relacions entre aquests registres que es creen a través dels detalls de l'entrada de temps, la línia de diari, la línia real i la línia de factura.

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


La il·lustració següent mostra els enllaços que es creen entre els reals i les seves fonts en diversos esdeveniments utilitzant l'exemple de les entrades de temps a les operacions del projecte.

> ![Com s'enllacen els reals amb els registres d'origen de les operacions del projecte.](media/TransactionOrigins.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
