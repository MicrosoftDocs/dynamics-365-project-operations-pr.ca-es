---
title: Línies de factures del proveïdor per a productes
description: En aquest tema s'explica com registrar les línies de factures dels proveïdors dels productes i utilitzar els diferents camps per registrar les compres de productes dels proveïdors.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: af078cd4392f8353b509db2dc48dc5237b8ee275
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8599166"
---
# <a name="vendor-invoice-lines-for-products"></a>Línies de factures del proveïdor per a productes

[!include [banner](../../includes/dataverse-preview.md)]

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_

Una factura de proveïdor a Microsoft Dynamics 365 Project Operations pot tenir línies de factura de proveïdors per a productes (també anomenats materials). Els gestors de projectes poden utilitzar línies de factures de proveïdors per als productes per registrar els costos dels productes que s'han comprat en projectes.

Les línies de factura del proveïdor dels productes poden o no fer referència a una línia de subcontractació de materials. Si una línia de factura del proveïdor per a productes fa referència a una subcontracta, els gestors de projectes podran coincidir i verificar els productes que la línia de factura del proveïdor factura contra l'ús de productes comprats que són registrats i aprovats pels gestors de projectes.

La taula següent proporciona informació sobre els camps de les línies de factures dels proveïdors dels productes.

| Camp | Descripció | Impacte funcional |
| --- | --- | --- |
| Nom | El nom de la línia de factura del proveïdor, per ajudar-vos a identificar-la. | Aquest nom es mostrarà com la primera columna de totes les cerques que es basen en línies de factura de proveïdor. |
| Descripció | Una breu descripció dels productes que el proveïdor factura a la línia de factura del proveïdor. | cap |
| Subcontracte | La subcontractació en la que es van demanar originalment els productes. | Quan se selecciona una subcontracta per a la factura del proveïdor, totes les línies de la factura del proveïdor heretaran aquesta selecció. Una factura de proveïdor no pot tenir línies de factura de proveïdor que fan referència a subcontractacions diferents. |
| Línia subcontractada | La línia de subcontractació en la que es van demanar els productes. La llista de línies de subcontractació que es poden seleccionar es limita a les línies de la subcontractació seleccionada. | Quan se selecciona una línia de subcontractació en una línia de factura de proveïdor per als productes, els valors per defecte dels **camps Projecte**, **Tasca** i **Producte** s'introdueixen des dels camps corresponents de la línia de subcontractació. Si la línia de subcontractació seleccionada té valors als **camps Projecte**, **Tasca** i **Producte**, els valors dels camps corresponents de la línia de factura del proveïdor no poden diferir d'aquests valors. |
| Data de la transacció | La data en què es registrarà el cost real de la línia de factura del proveïdor al projecte. | cap|
| Classe de la transacció | Quan es facturen productes, aquest camp s'ha d'establir a **Material**. | El valor **Material** indica que la línia de factura del proveïdor s'està utilitzant per registrar l'import de la factura dels materials que s'han comprat. |
| Project | El nom del projecte en què s'han utilitzat els productes que s'estan facturant. | Aquest camp és obligatori i no es pot deixar en blanc. |
| Tasca | El nom de la tasca del projecte en què s'han utilitzat els productes que s'estan facturant. Aquest camp només està disponible si se selecciona un projecte. La selecció d'una tasca de projecte és opcional. | Si aquest camp es deixa en blanc, el gestor del projecte pot fer coincidir la línia de factura del proveïdor amb el producte comprat que s'utilitza en qualsevol tasca del projecte. Si la línia de factura del proveïdor no fa referència a una línia de subcontractació i aquest camp es deixa en blanc, el cost real creat per la línia de factura del proveïdor no s'enllaçarà amb cap real de vendes no facturat. En aquest cas, si es configura la facturació basada en tasques, els costos no es podran facturar al client final. |
| Seleccioneu el producte | Seleccioneu si el producte que s'està facturant és un producte existent del catàleg o d'un producte d'escriptura. | El valor per defecte s'introdueix des de la línia de subcontractació quan se selecciona una línia de subcontractació. |
| Producte | Seleccioneu el producte del catàleg. Si el producte és un producte d'escriptura, introduïu el nom del producte. | Aquest camp s'utilitza per introduir els preus de compra predeterminats dels productes existents. |
| Quantitat | Introduïu la quantitat de material que el proveïdor està facturant en aquesta línia de factura. | cap |
| Grup d'unitats | Seleccioneu el grup d'unitats de la unitat en què s'expressa la quantitat que s'està facturant. | cap |
| Unit | El valor per defecte és la unitat base del grup d'unitats seleccionat. Podeu canviar aquest valor per pagar en qualsevol unitat del grup d'unitats seleccionat. | La combinació dels **valors Producte** i **Unitat** s'utilitzarà com a valor per defecte o calculat per al **camp Preu** unitari de la línia de factura del proveïdor. |
| Preu unitari | El preu unitari per defecte utilitza la combinació de valors Producte **i** **Unitat** de la llista de preus del projecte que s'aplica a la data de transacció de la línia de factura del proveïdor. | cap |
| Subtotal | Aquest camp de només lectura es calcula com a *preu* unitat de quantitat &times;*·*, si els valors s'introdueixen tant al camp Quantitat **com** al **camp Preu** unitat. Si un o ambdós camps estan en blanc, podeu introduir un valor en aquest camp. | cap |
| Impost sobre les vendes | Especifiqueu l'import de l'impost sobre les vendes. | cap |
| Import total | L'import total de la línia de factures del proveïdor, inclosos els impostos. Aquest camp es calcula com a impost sobre *vendes de subtotals* + *·*. | cap |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
