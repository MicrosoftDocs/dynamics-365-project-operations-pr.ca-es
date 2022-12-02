---
title: Línies de factura del proveïdor per a productes
description: En aquest article s'explica com registrar les línies de factura de proveïdor per als productes i utilitzar els diferents camps per registrar les compres de productes dels proveïdors.
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

Una factura del proveïdor del Microsoft Dynamics 365 Project Operations pot tenir línies de factura del proveïdor per als productes (també anomenades materials). Els administradors de projecte poden utilitzar les línies de factura de proveïdor per a productes per registrar els costos dels productes comprats en els projectes.

Les línies de factura de proveïdor per a productes podrien o no fer referència a una línia de subcontracte per a materials. Si una línia de factura de proveïdor per a productes fa referència a un subcontracte, els administradors de projecte podran fer coincidir i verificar els productes que s'estan facturant amb la línia de factura de proveïdor amb l'ús dels productes comprats que registren i aproven els administradors del projecte.

La taula següent proporciona informació sobre els camps de les línies de factura de proveïdor per a productes.

| Camp | Descripció | Impacte funcional |
| --- | --- | --- |
| Nom | Nom de la línia de factura de proveïdor per ajudar a identificar-la. | Aquest nom es mostrarà com la primera columna de totes les consultes basades en les línies de factura de proveïdor. |
| Descripció | Descripció breu dels productes que factura el proveïdor a la línia de factura de proveïdor. | cap |
| Subcontracte | El subcontracte en què es van demanar els productes originalment. | Quan se selecciona un subcontracte per a la factura del proveïdor, totes les línies de la factura del proveïdor heretaran aquesta selecció. Una factura del proveïdor no pot tenir línies de factura del proveïdor que facin referència a diferents subcontractes. |
| Línia de subcontracte | La línia de subcontracte en què es van demanar els productes. La llista de línies de subcontracte que es poden seleccionar està limitada a les línies del subcontracte seleccionat. | Quan se selecciona una línia de subcontracte en una línia de factura de proveïdor per a productes, els valors per defecte dels camps **Projecte**, **Tasca** i **Producte** s'introdueixen des dels camps corresponents de la línia de subcontracte. Si la línia de subcontracte seleccionada té valors als camps **Projecte**, **Tasca** i **Producte**, els valors dels camps corresponents de la línia de factura de proveïdor no poden diferir d'aquests valors. |
| Data de la transacció | La data en què el valor real de cost de la línia de factura del proveïdor es registrarà al projecte. | cap|
| Classe de la transacció | Quan es facturen els productes, aquest camp s'ha de definir com a **Material**. | El valor de **Material** indica que la línia de factura del proveïdor s'utilitza per registrar l'import de la factura dels materials que s'han comprat. |
| Project | Nom del projecte on s'han utilitzat els productes que es facturen. | Aquest camp és obligatori i no es pot deixar en blanc. |
| Tasca | Nom de la tasca de projecte on s'han utilitzat els productes que es facturen. Aquest camp només està disponible si se selecciona un projecte. La selecció d'una tasca de projecte és opcional. | Si aquest camp es deixa en blanc, l'administrador del projecte pot aparellar la línia de factura de proveïdor amb el producte comprat que s'utilitza en qualsevol tasca del projecte. Si la línia de factura del proveïdor no fa referència a una línia de subcontracte i aquest camp es deixa en blanc, el valor real de cost que crea la línia de factura del proveïdor no s'enllaçarà amb cap valor real de vendes no facturades. En aquest cas, si es configura la facturació basada en tasques, els costos no es podran facturar al client final. |
| Seleccioneu el producte | Seleccioneu si el producte que s'està facturant és un producte existent del catàleg o si és un producte fora de catàleg. | El valor per defecte s'introdueix des de la línia de subcontracte quan se selecciona una línia de subcontracte. |
| Producte | Seleccioneu el producte del catàleg. Si el producte és un producte fora de catàleg, introduïu el nom del producte. | Aquest camp s'utilitza per introduir els preus de compra per defecte per als productes existents. |
| Quantitat | Introduïu la quantitat de material que factura el proveïdor en aquesta línia de factura. | cap |
| Grup d'unitats | Seleccioneu el grup d'unitats de la unitat en què s'expressa la quantitat que s'està facturant. | cap |
| Unit | El valor per defecte és la unitat base del grup d'unitats seleccionat. Podeu canviar aquest valor per pagar qualsevol unitat del grup d'unitats seleccionat. | La combinació dels valors **Producte** i **Unitat** s'utilitzarà com a valor per defecte o valor calculat per al camp **Preu unitari** de la línia de factura de proveïdor. |
| Preu unitari | El preu unitari per defecte utilitza la combinació dels valors **Producte** i **Unitat** de la llista de preus del projecte aplicable a la data de la transacció de la línia de factura de proveïdor. | cap |
| Subtotal | És un camp només de lectura que es calcula com *Quantitat* &times; *Preu unitari* si s'introdueixen valors tant en el camp **Quantitat** com en el camp **Preu unitari**. Si un o tots dos camps estan en blanc, podeu introduir un valor en aquest camp. | cap |
| Impost sobre les vendes | Especifiqueu l'import de l'impost sobre les vendes. | cap |
| Import total | Quantitat total de la línia de factura de proveïdor amb els impostos. Aquest camp es calcula com *Subtotal* + *Impost sobre les vendes*. | cap |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
