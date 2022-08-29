---
title: Línies de factura del proveïdor per a productes
description: En aquest article s'explica com registrar les línies de factures dels proveïdors dels productes i s'utilitzen els diferents camps per registrar les compres de productes dels proveïdors.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: d38a447c576c095a7bbe2f5ed84342a88bf69a9b
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261546"
---
# <a name="vendor-invoice-lines-for-products"></a>Línies de factura del proveïdor per a productes

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_

Una factura de proveïdor a Microsoft Dynamics 365 Project Operations pot tenir línies de factures de proveïdors per als productes (també anomenats materials). Els gestors de projectes poden utilitzar línies de factures de proveïdors de productes per registrar els costos dels productes que s'han comprat en projectes.

Les línies de factures dels proveïdors de productes poden fer referència o no a una línia de subcontractació de materials. Si una línia de factures de proveïdors de productes fa referència a un subcontractista, els gestors de projectes podran fer coincidir i verificar els productes que estan sent facturats per la línia de factura del venedor amb l'ús de productes comprats que són registrats i aprovats pels gestors del projecte.

La taula següent proporciona informació sobre els camps de les línies de factures de proveïdors de productes.

| Camp | Descripció | Impacte funcional |
| --- | --- | --- |
| Nom | El nom de la línia de factura del venedor, per ajudar a la identificació. | Aquest nom es mostrarà com a primera columna de totes les cerques basades en línies de factures de proveïdor. |
| Descripció | Una breu descripció dels productes que està facturant el venedor a la línia de factura del proveïdor. | cap |
| Subcontracte | La subcontractació en què es van encarregar originalment els productes. | Quan se selecciona un subcontractista per a la factura del venedor, totes les línies de la factura del venedor heretaran aquesta selecció. Una factura de proveïdor no pot tenir línies de factures de proveïdors que facin referència a diferents subcontractes. |
| Línia de subcontractació | La línia de subcontractació en la qual es van encarregar els productes. La llista de línies de subcontractació que es poden seleccionar es limita a les línies de la subcontractació seleccionada. | Quan se selecciona una línia de subcontractació en una línia de factura de proveïdor per a productes, els valors predeterminats per als **camps Projecte**, **Tasca** i **Producte** s'introdueixen des dels camps corresponents de la línia de subcontractació. Si la línia de subcontractació seleccionada té valors als **camps Projecte**, **Tasca** i **Producte**, els valors dels camps corresponents de la línia de factura del proveïdor no poden diferir d'aquests valors. |
| Data de la transacció | La data en què es registrarà al projecte el cost real de la línia de factura del proveïdor. | cap|
| Classe de la transacció | Quan es facturen productes, aquest camp s'ha d'establir a **Material**. | El valor **Material** indica que la línia de factura del proveïdor s'està utilitzant per registrar l'import de la factura dels materials que es van comprar. |
| Project | El nom del projecte en què es van utilitzar els productes que s'estan facturant. | Aquest camp és obligatori i no es pot deixar en blanc. |
| Tasca | El nom de la tasca del projecte en què es van utilitzar els productes que s'estan facturant. Aquest camp només està disponible si se selecciona un projecte. La selecció d'una tasca de projecte és opcional. | Si aquest camp es deixa en blanc, el gestor de projectes pot fer coincidir la línia de factura del proveïdor amb el producte comprat que s'utilitza en qualsevol tasca del projecte. Si la línia de factures del proveïdor no fa referència a una línia de subcontractació i aquest camp es deixa en blanc, el cost real creat per la línia de factures del proveïdor no estarà vinculat a cap real de vendes no codificat. En aquest cas, si es configura la facturació basada en tasques, els costos no es podran facturar al client final. |
| Seleccioneu el producte | Seleccioneu si el producte que s'està facturant és un producte existent del catàleg o un producte escrit. | El valor per defecte s'introdueix des de la línia de subcontractació quan se selecciona una línia de subcontractació. |
| Producte | Seleccioneu el producte del catàleg. Si el producte és un producte escrit, introduïu el nom del producte. | Aquest camp s'utilitza per introduir els preus de compra predeterminats dels productes existents. |
| Quantitat | Introduïu la quantitat de material que està facturant el venedor en aquesta línia de factura. | cap |
| Grup d'unitats | Seleccioneu el grup d'unitats de la unitat en què s'expressa la quantitat que s'està facturant. | cap |
| Unit | El valor per defecte és la unitat base del grup d'unitats que se selecciona. Podeu canviar aquest valor per pagar en qualsevol unitat del grup d'unitats seleccionat. | La combinació de valors Producte i Unitat s'utilitzarà **com a valor per defecte o computat per al camp Preu** unitari de **la línia de factura del proveïdor.** **·** |
| Preu unitari | El preu unitari per defecte utilitza la combinació de valors Producte **i** **Unitat** de la llista de preus del projecte que s'aplica a la data de transacció de la línia de factura de proveïdor. | cap |
| Subtotal | Aquest camp només de lectura es calcula com a *Quantitat*&times;*Preu* unitari, si s'introdueixen valors tant al camp Quantitat **com** al **camp Preu** unitari. Si un o tots dos camps estan en blanc, podeu introduir un valor en aquest camp. | cap |
| Impost sobre les vendes | Especifiqueu l'import de l'impost sobre les vendes. | cap |
| Import total | L'import total de la línia de factures del proveïdor, inclosos els impostos. Aquest camp es calcula com a *impost sobre les vendes subtotals* + *·*. | cap |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
