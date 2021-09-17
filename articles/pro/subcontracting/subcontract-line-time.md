---
title: Línies del subcontracte per al temps
description: En aquest tema s'explica com registrar línies de subcontracte per al temps i registrar la compra de temps dels proveïdors.
author: rumant
ms.date: 08/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 10ebe0fcc86b4652ac01e28108361df1f768b61d
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323854"
---
# <a name="subcontract-lines-for-time"></a>Línies del subcontracte per al temps

[!include [banner](../../includes/dataverse-preview.md)]

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_

Un subcontracte al Dynamics 365 Project Operations pot tenir una línia de subcontracte per al temps. Les línies de subcontracte per al temps permeten a un Administrador de projectes comprar temps dels recursos del proveïdor a les tasques i els requisits de recursos del projecte.

Per crear una línia de subcontracte per a temps al Project Operations, completeu els passos següents.

1. A la subfinestra de navegació, seleccioneu **Subcontractes** i obriu un subcontracte.
2. A la pestanya **Línies de subcontracte**, seleccioneu **Nou** per crear una línia de subcontracte nova.
3. A la pàgina **Creació ràpida**, al camp **Classe de transacció**, seleccioneu **Hora**.
4. Introduïu la informació als camps restants i, a continuació, seleccioneu **Desa**.

  La taula següent proporciona informació sobre els camps de la pàgina **Línia de subcontracte** i la pàgina **Creació ràpida**.

| **Camp** | **Descripció** |
| --- | --- |
| Nom | Nom de la línia de subcontracte. |
| Descripció | Descripció breu dels serveis que es compren a la línia de subcontracte. | 
| Tipus de línia | Aquest camp és un valor per defecte.  |
| Mètode de facturació | Seleccioneu el mètode de facturació. Segons el mètode de facturació de la línia de subcontracte a què es fa referència, s'ofereix una planificació de facturació basada en fites per al mètode de facturació de Preu fix. |
| Classe de la transacció | Aquest camp és un valor per defecte que indica si la línia de subcontracte s'utilitza per registrar una compra de temps del subcontractista. |
| Funció | Funció dels recursos de subcontracte el temps del qual s'està comprant. La funció assignada als recursos de subcontracte determina el cost de la compra. |
| Data sol·licitada | Data en què els recursos del subcontractista són necessaris per començar a treballar. La data sol·licitada s'utilitza per seleccionar una llista de preus a les llistes de preus del projecte adjuntades al subcontracte. El cost de la funció a la línia de subcontracte es pren per defecte d'aquesta llista de preus. |
| Final sol·licitat | Data d'acabament de l'assignació de recursos del subcontracte. Aquesta data s'utilitza per mostrar advertiments quan un Administrador de projectes està prenent d'aquesta capacitat per als requisits de recursos que es produeixen després d'aquesta data. |
| Quantitat demanada | Nombre d'hores de la funció que es compra al proveïdor. Aquest valor s'utilitza per mostrar advertiments quan un Administrador de projectes està prenent d'aquesta capacitat per als requisits de recursos. |
| Grup d’unitats | Aquest valor de camp és per defecte el grup d'unitats de Temps i no es pot canviar.  |
| Unitat | Aquest camp és per defecte la unitat base d'hores del grup d'unitats de Temps. Podeu canviar aquest valor per comprar qualsevol unitat del grup d'unitats de Temps, com ara dia o setmana. La combinació de Funció i Unitat s'utilitza per calcular el preu unitari per a la línia de subcontracte. |
| Preu per unitat | El preu unitari pren el valor per defecte de la combinació de Funció i Unitat de la llista de preus aplicable per a la data d'inici sol·licitada de la línia de subcontracte. Quan la llista de preus del projecte aplicable té el preu configurat en una unitat diferent de la unitat de la línia de subcontracte, el sistema utilitza la conversió d'unitats per calcular el preu unitari. |
| Subtotal | És un camp només de lectura que es calcula automàticament com a **Quantitat x Preu unitari** si s'introdueixen els valors de quantitat i de preu unitari. Si el camp quantitat, preu unitari o tots dos estan en blanc, podeu introduir-hi un valor. |
| Impost sobre les vendes |  Especifiqueu l'import de l'impost sobre les vendes. |
| Import total | Quantitat total de la línia de subcontracte després d'incloure-hi els impostos. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
