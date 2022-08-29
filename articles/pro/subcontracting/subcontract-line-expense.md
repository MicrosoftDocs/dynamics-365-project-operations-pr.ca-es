---
title: Línies de subcontracte per a categories de despeses
description: En aquest article s'explica com registrar les línies de subcontractació per a despeses i utilitzar els camps per registrar la compra de temps als proveïdors.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7166642abc2187a53f7019639df6f0d7124f4765
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261828"
---
#  <a name="subcontract-lines-for-expense-categories"></a>Línies de subcontracte per a categories de despeses

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_

Un subcontracte al Dynamics 365 Project Operations pot tenir una línia per a categories de despesa. Les línies de subcontracte de les categories de despesa permeten a un Administrador de projectes adquirir categories de serveis o productes als proveïdors que poden carregar a un projecte.

Per crear una línia de subcontracte per a categories de despesa al Project Operations, completeu els passos següents.

1. A la subfinestra de navegació, seleccioneu **Subcontractes** i obriu el subcontracte amb el qual voleu treballar.
2. A la pestanya **Línies de subcontracte**, seleccioneu **Nou** per crear una línia nova.
3. A la pàgina **Creació ràpida**, al camp **Classe de transacció**, seleccioneu **Despesa** i introduïu o seleccioneu qualsevol altra informació de camps obligatoris.

La taula següent proporciona informació sobre els camps de la pàgina de detalls de **Línia de subcontracte** i la pàgina **Creació ràpida**.

| **Camp** | **Descripció** | **Impacte funcional** |
| --- | --- | --- |
| Nom | Nom de la línia de subcontracte per ajudar a identificar-la. | Es mostrarà com la primera columna de totes les consultes basada en les línies de subcontracte. |
| Descripció | Descripció breu de les categories de despeses que s'adquireixen a la línia de subcontracte. | Cap |
|Tipus de línia | Aquest camp té un valor per defecte de **Basat en quantitat**. |Cap |
| Mètode de facturació | Es tracta d'un conjunt d'opcions que representa els dos models de contractació principals que admet el Project Operations: **Preu fix** i **Temps i material**. | Una planificació de factura basada en fites està disponible per a les línies de subcontracte si se selecciona el mètode de facturació de preus fixos. |
| Classe de la transacció | Aquest camp té un valor per defecte de **Temps**. Per crear línies de subcontracte per comprar productes, definiu el camp **Classe de transacció** com a **Despesa**.  | Això indica que la línia de subcontracte s'utilitza per registrar la compra d'una categoria de despeses que s'utilitzaran en els projectes. |
| Categoria de transacció | Mostra una llista de les categories de transaccions actives al sistema. |Cap |
| Data sol·licitada | Introduïu la data en què les categories de compra han d'estar disponibles al proveïdor. | S'utilitza l'inici sol·licitat per seleccionar una llista de preus del projecte de les llistes de preus del projecte adjuntades al subcontracte. El cost de la categoria a la línia de subcontracte prové d'aquesta llista de preus. |
| Final sol·licitat | Introduïu la data en què ja no es necessitarien les categories de compra. | S'utilitzarà per mostrar advertiments quan un administrador de projecte associa aquesta línia de subcontracte a estimacions de despeses específiques del projecte que són necessàries a partir d'aquesta data. |
| Quantitat demanada | Quantitat de la categoria que es compra al proveïdor. | S'utilitzarà per mostrar advertiments quan un administrador de projecte prengui un excés d'aquesta quantitat.|
| Grup d’unitats | El valor per defecte es basa en el grup d'unitats per defecte configurat per a la categoria seleccionada. |Cap |
| Unitat | El valor per defecte es basa en la unitat per defecte configurada per a la categoria seleccionada.  | La combinació de **Categoria** i **Unitat** s'utilitzarà com a valor per defecte o es calcularà per al preu unitari de la línia de subcontracte.  |
| Preu per unitat | El valor per defecte utilitza la combinació de **Categoria** i **Unitat** dels preus de categoria relacionats amb la llista de preus del projecte, que és aplicable a l'Inici sol·licitat de la línia de subcontracte. |Cap |
| Subtotal | Es tracta d'un camp només de lectura que es calcula com a Quantitat x Preu unitari, si s'introdueixen tant la quantitat com els valors de preu unitari. Si un o tots dos camps estan en blanc, podeu introduir un valor en aquest camp. |Cap |
| Impost sobre les vendes | Especifiqueu l'import de l'impost sobre les vendes. |Cap |
| Import total | Quantitat total de la línia de subcontracte amb els impostos. Aquest camp es calcula com subtotal + impost sobre les vendes. |Cap |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
