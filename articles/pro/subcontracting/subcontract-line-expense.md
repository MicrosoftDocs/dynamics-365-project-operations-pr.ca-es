---
title: Línies de subcontracte per a categories de despeses
description: En aquest tema s'explica com registrar línies de subcontracte per a despeses i utilitzar els camps per registrar la compra de temps a proveïdors.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9e8e7bb66063dab6db1ac8da1753913aee0ef3fc
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323809"
---
#  <a name="subcontract-lines-for-expense-categories"></a>Línies de subcontracte per a categories de despeses

[!include [banner](../../includes/dataverse-preview.md)]

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_

Un subcontracte al Dynamics 365 Project Operations pot tenir una línia per a categories de despesa. Les línies de subcontracte de les categories de despesa permeten a un Administrador de projectes adquirir categories de serveis o productes als proveïdors que poden carregar a un projecte.

Per crear una línia de subcontracte per a categories de despesa al Project Operations, completeu els passos següents.

1. A la subfinestra de navegació, seleccioneu **Subcontractes** i obriu el subcontracte amb el qual voleu treballar.
2. A la pestanya **Línies de subcontracte**, seleccioneu **Nou** per crear una línia nova.
3. A la pàgina **Creació ràpida**, al camp **Classe de transacció**, seleccioneu **Despesa** i introduïu o seleccioneu qualsevol altra informació de camps obligatoris.

La taula següent proporciona informació sobre els camps de la pàgina de detalls de **Línia de subcontracte** i la pàgina **Creació ràpida**.

| **Camp** |  **Descripció** |
| ----------| ---------------- |
| Nom | Nom de la línia de subcontracte. |
| Descripció | Descripció breu de les categories de serveis o productes que es compren a la línia de subcontracte. |
| Tipus de línia | Aquest camp té un valor per defecte **Basat en quantitat**.  |
| Mètode de facturació | Mètode de facturació de la línia de subcontracte. Segons el mètode de facturació de la línia, s'ofereix una planificació de facturació basada en fites per al mètode de facturació de preu fix.  |
| Classe de la transacció | Aquest camp té un valor per defecte **Temps**. Per crear línies de subcontracte per comprar productes, definiu el camp **Classe de transacció** com a **Despesa**. Aquest valor de camp indica que la línia de subcontracte s'utilitza per registrar una compra d'una categoria de productes o serveis que s'utilitzaran en projectes. |
| Categoria de transacció | Seleccioneu la categoria de transacció. |
| Data sol·licitada | Data en què les categories de compra han d'estar disponibles del proveïdor. La data sol·licitada s'utilitza per seleccionar una llista de preus a les llistes de preus del projecte adjuntades al subcontracte. El cost de la categoria a la línia de subcontracte es pren per defecte d'aquesta llista de preus. |
| Final sol·licitat | Data en què les categories de compra ja no es necessiten. Aquesta data genera un advertiment quan un administrador de projectes associa aquesta línia de subcontracte amb estimacions de despeses específiques als projectes amb data posterior a aquesta. |
| Quantitat demanada | Quantitat de la categoria que es compra al proveïdor. Si un administrador de projectes pren de la quantitat comprada, es produirà un advertiment.  |
| Grup d’unitats | Aquest valor de camp pren el valor per defecte segons el grup d'unitats per defecte configurat per a la categoria seleccionada. |
| Unitat | Aquest valor de camp pren el valor per defecte segons la unitat per defecte configurada per a la categoria seleccionada. La combinació de categoria i unitat s'utilitza per al valor per defecte del preu unitari de la línia de subcontracte. |
| Preu per unitat | El valor del camp de preu unitari pren el valor per defecte de la combinació de la categoria i la unitat dels preus de categoria relacionats amb la llista de preus del projecte que sigui aplicable a la data sol·licitada de la línia de subcontracte.  |
| Subtotal | És un camp només de lectura que es calcula automàticament com el preu unitari per quantitat si s'introdueixen els valors de quantitat i de preu unitari. Si un o tots dos camps estan buits, podeu introduir un valor en aquest camp manualment.  |
| Impost sobre les vendes | Especifiqueu l'import de l'impost sobre les vendes.  |
| Import total | Quantitat total de la línia de subcontracte amb els impostos. Aquest camp es calcula com el subtotal + impost sobre les vendes.  |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
