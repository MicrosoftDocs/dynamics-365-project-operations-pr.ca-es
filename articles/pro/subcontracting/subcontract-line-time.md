---
title: Línies del subcontracte per al temps
description: En aquest tema s'explica com registrar línies de subcontracte per al temps i registrar la compra de temps dels proveïdors.
author: rumant
ms.date: 08/05/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c1adc1e88369e9f60548ed69b5950070d5f10c57
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8595670"
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

| **Camp** | **Descripció** | **Impacte funcional** |
| --- | --- | --- |
| Nom | Nom de la línia de subcontracte per ajudar a identificar-la. | Es mostrarà com la primera columna de totes les consultes basada en les línies de subcontracte. |
| Descripció | Descripció breu dels serveis que es compren a la línia de subcontracte. |Cap |
| Tipus de línia |   Aquest camp té un valor per defecte **Basat en quantitat**.| Cap |
| Mètode de facturació | Es tracta d'un conjunt d'opcions que representa els dos models de contractació principals que admet el Project Operations: **Preu fix** i **Temps i material**. | Segons el mètode de facturació seleccionat, una planificació de factura basada en fites està disponible per a les línies de subcontracte amb el mètode de facturació de preus fixos. |
| Classe de la transacció | El valor per defecte és **Temps**. | Això indica que la línia de subcontracte s'utilitza per registrar una compra de temps de subcontractista. |
| Funció | Seleccioneu la funció dels recursos de subcontracte el temps dels qual es compra. | La funció que fan els recursos de subcontracte determina el cost de la compra. |
| Data sol·licitada | Introduïu la data en què els recursos de subcontracte són necessaris per començar a treballar. | S'utilitza per seleccionar una llista de preus del projecte de les llistes de preus del projecte adjuntades al subcontracte. El cost de la funció a la línia de subcontracte prové d'aquesta llista de preus. |
| Final sol·licitat | Introduïu la data en què acaba l'assignació del recurs de subcontracte. | S'utilitzarà per mostrar advertiments quan un administrador de projecte pren de la capacitat dels requisits de recursos que es produeixen després d'aquesta data. |
| Quantitat demanada | Introduïu el nombre d'hores de la funció que s'ha adquirit al proveïdor. | S'utilitzarà per mostrar advertiments quan un administrador de projecte prengui un excés de la capacitat dels requisits de recursos. |
| Grup d’unitats | El valor per defecte és **Grup d'unitats de temps**, que no es pot canviar. | Cap|
| Unitat | El valor per defecte d'aquest camp és la unitat de base d'hores del **Grup d'unitat de temps**. Podeu canviar aquest valor per comprar qualsevol unitat del **Grup d'unitats de temps**, com ara dia o setmana. | La combinació de **Funció** i **Unitat** s'utilitzarà com a valor per defecte o es calcularà per al preu unitari de la línia de subcontracte. |
| Preu per unitat | El preu unitari per defecte utilitza la combinació de **Funció** i **Unitat** de la llista de preus del projecte aplicable a la data d'**Inici sol·licitat** de la línia de subcontracte. | Quan la llista de preus del projecte aplicable té el preu configurat en una unitat diferent de la unitat de la línia de subcontracte, el sistema utilitza la conversió d'unitats per calcular el preu unitari. |
| Subtotal |    Es tracta d'un camp només de lectura que es calcula com a Quantitat x Preu unitari, si s'introdueixen tant la quantitat com els valors de preu unitari. Si el camp quantitat, preu unitari o tots dos estan en blanc, podeu introduir-hi un valor. | Cap|
| Impost sobre les vendes |   Especifiqueu l'import de l'impost sobre les vendes. |Cap |
| Import total | Quantitat total de la línia de subcontracte amb els impostos. Aquest camp es calcula com subtotal + impost sobre les vendes.|Cap |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
