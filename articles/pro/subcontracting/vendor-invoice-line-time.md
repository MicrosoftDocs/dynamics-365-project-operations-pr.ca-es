---
title: Línies de factura del proveïdor per al temps
description: En aquest article s'explica com registrar les línies de factures del proveïdor pels costos de temps que els subcontractistes posen.
author: rumant
ms.date: 03/15/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 0b81d2884580e9054457906627c1f9101f435524
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927523"
---
# <a name="vendor-invoice-lines-for-time"></a>Línies de factura del proveïdor per al temps

[!include [banner](../../includes/dataverse-preview.md)]

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_

Una factura de proveïdor de Microsoft Dynamics 365 Project Operations pot tenir línies de factura de proveïdor durant el temps. Els administradors de projectes poden utilitzar línies de factures de proveïdors durant el temps per registrar els costos del temps de subcontractació en projectes.

Les línies de factura del proveïdor durant el temps poden o no fer referència a una línia de subcontractació durant el temps. Si una línia de factura del proveïdor per a les referències de temps d'una subcontracta, els administradors de projectes podran coincidir i verificar l'hora que factura la línia de factura del proveïdor contra el temps que els subcontractistes registren i l'aprova els gestors del projecte del projecte.

La taula següent proporciona informació sobre els camps de les línies de factura del proveïdor durant el temps.

| Camp | Descripció | Impacte funcional |
| --- | --- | --- |
| Nom | El nom de la línia de factura del proveïdor, per ajudar-vos a identificar-la. | Aquest nom es mostrarà com la primera columna de totes les cerques que es basen en línies de factura de proveïdor. |
| Descripció | Una breu descripció dels serveis que el proveïdor està facturant a la línia de factura del proveïdor. | cap |
| Subcontracte | La subcontractació sobre la que es van encarregar originalment els serveis. | Quan se selecciona una subcontracta per a la factura del proveïdor, totes les línies de la factura del proveïdor heretaran aquesta selecció. Una factura de proveïdor no pot tenir línies de factura de proveïdor que fan referència a subcontractacions diferents. |
| Línia subcontractada | La línia de subcontractació en la que es van encarregar els serveis. La llista de línies de subcontractació que es poden seleccionar es limita a les línies de la subcontractació seleccionada. | Quan se selecciona una línia de subcontractació en una línia de factura de proveïdor durant el temps, els valors per defecte dels **camps De projecte**, **Funció** i **recurs** que es poden reservar s'introdueixen des dels camps corresponents de la línia de subcontractació. Si la línia de subcontractació seleccionada té valors als **camps Projecte**, **Funció** i **Reservable**, els valors dels camps corresponents de la línia de factura del proveïdor no poden diferir d'aquests valors. |
| Data de la transacció | La data en què es registrarà el cost real de la línia de factura del proveïdor al projecte. | cap |
| Classe de la transacció | El valor per defecte és **Temps**. | El valor **Temps** indica que la línia de factura del proveïdor s'està utilitzant per registrar l'import de la factura del temps del subcontractista. |
| Project | El nom del projecte en què s'han utilitzat els serveis que s'estan facturant. | Aquest camp és obligatori i no es pot deixar en blanc. |
| Tasca | El nom de la tasca del projecte en què s'han utilitzat els serveis que s'estan facturant. Aquest camp només està disponible si se selecciona un projecte. La selecció d'una tasca de projecte és opcional. | Si aquest camp es deixa en blanc, el gestor del projecte pot fer coincidir la línia de factura del proveïdor amb el temps que enregistren els recursos del subcontractista en qualsevol tasca del projecte. Si la línia de factura del proveïdor no fa referència a una línia de subcontractació i aquest camp es deixa en blanc, el cost real creat per la línia de factura del proveïdor no s'enllaçarà amb cap real de vendes no facturat. En aquest cas, si es configura la facturació basada en tasques, és possible que els costos no es puguin facturar al client final. |
| Funció | El paper dels recursos de subcontractació el temps dels quals s'està facturant. | En aquest camp s'especifica la funció que realitzen els recursos de subcontractació l'hora dels quals es factura a la factura del proveïdor. |
| Recurs que es pot reservar | El nom del subcontractista el temps del qual s'està facturant. La selecció d'un recurs que es pot reservar és opcional. | Si aquest camp es deixa en blanc, el gestor del projecte pot fer coincidir la línia de factura del proveïdor amb el temps que enregistra qualsevol recurs que pertany al proveïdor a la línia de factura del proveïdor. |
| Quantitat | Introduïu el nombre d'hores de temps que el proveïdor factura a la línia de factura. |cap |
| Grup d'unitats | El valor per defecte és **el grup** d'unitats temps i no es pot canviar. | cap |
| Unit | El valor per defecte és la unitat base d'hores del grup d'unitats de temps. Podeu canviar aquest valor per comprar en qualsevol unitat del grup d'unitats de temps, com ara el dia o la setmana. | La combinació dels **valors Funció** i **Unitat** s'utilitzarà com a valor per defecte o calculat per al **camp Preu** unitari de la línia de factura del proveïdor. |
| Preu unitari | El preu unitari per defecte utilitza la combinació de valors de **funció** i **unitat** de la llista de preus del projecte que s'aplica a la data de transacció de la línia de factura del proveïdor. | Si el preu de la llista de preus del projecte aplicable està configurat en una unitat que difereix de la unitat de la línia de factura del proveïdor, el sistema utilitza la conversió unitària per calcular el preu per unitat. |
| Subtotal | Aquest camp de només lectura es calcula com a *preu* unitat de quantitat &times;*·*, si els valors s'introdueixen tant al camp Quantitat **com** al **camp Preu** unitat. Si un o ambdós camps estan en blanc, podeu introduir un valor en aquest camp. | cap |
| Impost sobre les vendes | Especifiqueu l'import de l'impost sobre les vendes. | cap |
| Import total | L'import total de la línia de factures del proveïdor, inclosos els impostos. Aquest camp es calcula com a impost sobre *vendes de subtotals* + *·*. | cap |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
