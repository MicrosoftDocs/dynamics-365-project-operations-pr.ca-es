---
title: Línies de factura del proveïdor per a categories de despeses
description: En aquest article s'explica com registrar les línies de factures dels proveïdors per a les categories de despeses.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 2c3cd2fab87af1cbfccd81e543f2cea0278978f6
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261663"
---
# <a name="vendor-invoice-lines-for-expense-categories"></a>Línies de factura del proveïdor per a categories de despeses

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_

Una factura de proveïdor a Microsoft Dynamics 365 Project Operations pot tenir línies de factures de proveïdor per a categories de despeses. Els gestors de projectes poden utilitzar línies de factures de proveïdors per a categories de despeses per registrar els costos dels serveis que s'obtenen com a categories de despeses.

Les línies de factures dels proveïdors per a categories de despeses poden fer referència o no a una línia de subcontractació per a categories de despeses. Si una línia de factures de proveïdors per categories de despeses fa referència a un subcontractista, els gestors de projectes podran igualar i verificar les despeses que estiguin sent facturades per la línia de factures del proveïdor contra les despeses que es registrin en aquestes categories de despeses i aprovades pels gestors del projecte.

La taula següent proporciona informació sobre els camps de les línies de factures de proveïdors per a les categories de despeses.

| Camp | Descripció | Impacte funcional |
| --- | --- | --- |
| Nom | El nom de la línia de factura del venedor, per ajudar a la identificació. | Aquest nom es mostrarà com a primera columna de totes les cerques basades en línies de factures de proveïdor. |
| Descripció | Una breu descripció dels serveis que està facturant el venedor a la línia de factura del proveïdor. | cap |
| Subcontracte | La subcontractació en què es van encarregar originalment els serveis. | Quan se selecciona un subcontractista per a la factura del venedor, totes les línies de la factura del venedor heretaran aquesta selecció. Una factura de proveïdor no pot tenir línies de factures de proveïdors que facin referència a diferents subcontractes. |
| Línia de subcontractació | La línia de subcontractació en la qual es van encarregar els serveis. La llista de línies de subcontractació que es poden seleccionar es limita a les línies de la subcontractació seleccionada. | Quan se selecciona una línia de subcontractació en una línia de factures de proveïdor per a les categories de despeses, els valors predeterminats per als **camps de categoria** Projecte **,** Tasca **i** Transacció s'introdueixen des dels camps corresponents de la línia de subcontractació. Si la línia de subcontractació seleccionada té valors als **camps Projecte**, **Tasca** del projecte i **Transacció**, els valors dels camps corresponents de la línia de factura del proveïdor no poden diferir d'aquests valors. |
| Data de la transacció | La data en què es registrarà al projecte el cost real de la línia de factura del proveïdor. |cap |
| Classe de la transacció | Seleccioneu **Despesa** per registrar una factura de proveïdor per a una categoria de despesa. | El valor **Despesa** indica que la línia de factura del proveïdor s'està utilitzant per registrar l'import de la factura dels serveis que es van contractar com a categories de despesa. |
| Project | El nom del projecte en què es van utilitzar els serveis que s'estan facturant. | Aquest camp és obligatori i no es pot deixar en blanc. |
| Tasca | El nom de la tasca del projecte en què es van utilitzar els serveis que s'estan facturant. Aquest camp només està disponible si se selecciona un projecte. La selecció d'una tasca de projecte és opcional. | Si aquest camp es deixa en blanc, el gestor de projectes pot fer coincidir la línia de factures del proveïdor amb les despeses registrades en qualsevol tasca del projecte. Si la línia de factures del proveïdor no fa referència a una línia de subcontractació i aquest camp es deixa en blanc, el cost real creat per la línia de factures del proveïdor no estarà vinculat a cap real de vendes no codificat. En aquest cas, si es configura la facturació basada en tasques, és possible que els costos no es puguin facturar al client final. |
| Categoria de la transacció | La categoria de transacció que s'està facturant. S'ha de crear una categoria de despesa corresponent per a la categoria de transacció seleccionada. | La combinació de categoria **de** transacció i **valors unitaris** s'utilitzarà com a valor per defecte o calculat per al camp Preu **unitari de** la línia de factura del proveïdor. |
| Quantitat | Introduïu la quantitat que està facturant el venedor a la línia de factura. |cap|
| Grup d'unitats | S'introdueix un valor per defecte en funció del grup d'unitats de la categoria de transacció seleccionada. | cap |
| Unit | El valor per defecte és la unitat base del grup d'unitats que se selecciona. Podeu canviar aquest valor per comprar-lo en qualsevol unitat del grup d'unitats. | La combinació de categoria **de** transacció i **valors unitaris** s'utilitzarà com a valor per defecte o calculat per al camp Preu **unitari de** la línia de factura del proveïdor. |
| Preu unitari | El preu unitari per defecte utilitza la combinació de la categoria **de** transacció i **els** valors unitaris de la llista de preus del projecte que s'aplica a la data de transacció de la línia de factura del proveïdor. | Si el preu de la llista de preus del projecte aplicable està configurat en una unitat diferent de la unitat de la línia de factura de proveïdor, el sistema utilitza la conversió unitària per calcular el preu per unitat. |
| Subtotal | Aquest camp només de lectura es calcula com a *Quantitat*&times;*Preu* unitari, si s'introdueixen valors tant al camp Quantitat **com** al **camp Preu** unitari. Si un o tots dos camps estan en blanc, podeu introduir un valor en aquest camp.| cap |
| Impost sobre les vendes | Especifiqueu l'import de l'impost sobre les vendes. | cap |
| Import total | L'import total de la línia de factures del proveïdor, inclosos els impostos. Aquest camp es calcula com a *impost sobre les vendes subtotals* + *·*. | cap |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
