---
title: Línies de factures del proveïdor per a categories de despeses
description: En aquest tema s'explica com registrar les línies de factures del proveïdor per a les categories de despeses.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 209460680c9e5c2e39f98ba5c48aa18992775db1
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579524"
---
# <a name="vendor-invoice-lines-for-expense-categories"></a>Línies de factures del proveïdor per a categories de despeses

[!include [banner](../../includes/dataverse-preview.md)]

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_

Una factura de proveïdor a Microsoft Dynamics 365 Project Operations pot tenir línies de factura de proveïdor per a categories de despeses. Els administradors de projectes poden utilitzar línies de factures de proveïdors per a categories de despeses per registrar els costos dels serveis que s'adquireixen com a categories de despeses.

Les línies de factures del proveïdor per a les categories de despeses poden fer referència o no a una línia de subcontractació per a les categories de despeses. Si una línia de factura del proveïdor per a categories de despeses fa referència a una subcontracta, els administradors de projectes podran fer coincidir i verificar les despeses que està facturant la línia de factura del proveïdor contra les despeses que es registren en aquestes categories de despeses i aprovades pels gestors de projectes del projecte.

A la taula següent s'ofereix informació sobre els camps de les línies de factures del proveïdor per a les categories de despeses.

| Camp | Descripció | Impacte funcional |
| --- | --- | --- |
| Nom | El nom de la línia de factura del proveïdor, per ajudar-vos a identificar-la. | Aquest nom es mostrarà com la primera columna de totes les cerques que es basen en línies de factura de proveïdor. |
| Descripció | Una breu descripció dels serveis que el proveïdor està facturant a la línia de factura del proveïdor. | cap |
| Subcontracte | La subcontractació sobre la que es van encarregar originalment els serveis. | Quan se selecciona una subcontracta per a la factura del proveïdor, totes les línies de la factura del proveïdor heretaran aquesta selecció. Una factura de proveïdor no pot tenir línies de factura de proveïdor que fan referència a subcontractacions diferents. |
| Línia subcontractada | La línia de subcontractació en la que es van encarregar els serveis. La llista de línies de subcontractació que es poden seleccionar es limita a les línies de la subcontractació seleccionada. | Quan se selecciona una línia de subcontractació en una línia de factura de proveïdor per a les categories de despeses, els valors per defecte dels **camps de categoria** Projecte **,** Tasca **i** Transacció s'introdueixen des dels camps corresponents de la línia de subcontractació. Si la línia de subcontractació seleccionada té valors als **camps De la categoria** **Projecte**, **Projecte i** Transacció, els valors dels camps corresponents de la línia de factura del proveïdor no poden diferir d'aquests valors. |
| Data de la transacció | La data en què es registrarà el cost real de la línia de factura del proveïdor al projecte. |cap |
| Classe de la transacció | Seleccioneu **Despesa** per registrar una factura de proveïdor per a una categoria de despeses. | El valor **Despesa** indica que la línia de factura del proveïdor s'està utilitzant per registrar l'import de la factura dels serveis que s'han adquirit com a categories de despeses. |
| Project | El nom del projecte en què s'han utilitzat els serveis que s'estan facturant. | Aquest camp és obligatori i no es pot deixar en blanc. |
| Tasca | El nom de la tasca del projecte en què s'han utilitzat els serveis que s'estan facturant. Aquest camp només està disponible si se selecciona un projecte. La selecció d'una tasca de projecte és opcional. | Si aquest camp es deixa en blanc, el gestor del projecte pot fer coincidir la línia de factura del proveïdor amb les despeses que es registren en qualsevol tasca del projecte. Si la línia de factura del proveïdor no fa referència a una línia de subcontractació i aquest camp es deixa en blanc, el cost real creat per la línia de factura del proveïdor no s'enllaçarà amb cap real de vendes no facturat. En aquest cas, si es configura la facturació basada en tasques, és possible que els costos no es puguin facturar al client final. |
| Categoria de la transacció | La categoria de transacció que s'està facturant. S'ha de crear una categoria de despeses corresponent per a la categoria de transacció seleccionada. | La combinació de **la categoria** transacció i **els valors Unitat** s'utilitzarà com a valor per defecte o calculat per al **camp Preu** unitari de la línia de factura del proveïdor. |
| Quantitat | Introduïu la quantitat que el proveïdor factura a la línia de factura. |cap|
| Grup d'unitats | S'introdueix un valor per defecte en funció del grup d'unitats de la categoria de transacció seleccionada. | cap |
| Unit | El valor per defecte és la unitat base del grup d'unitats seleccionat. Podeu canviar aquest valor per comprar en qualsevol unitat del grup d'unitats. | La combinació de **la categoria** transacció i **els valors Unitat** s'utilitzarà com a valor per defecte o calculat per al **camp Preu** unitari de la línia de factura del proveïdor. |
| Preu unitari | El preu unitari per defecte utilitza la combinació de la categoria **transacció** i **els valors d'unitat** de la llista de preus del projecte que s'aplica a la data de transacció de la línia de factura del proveïdor. | Si el preu de la llista de preus del projecte aplicable està configurat en una unitat que difereix de la unitat de la línia de factura del proveïdor, el sistema utilitza la conversió unitària per calcular el preu per unitat. |
| Subtotal | Aquest camp de només lectura es calcula com a *preu* unitat de quantitat &times;*·*, si els valors s'introdueixen tant al camp Quantitat **com** al **camp Preu** unitat. Si un o ambdós camps estan en blanc, podeu introduir un valor en aquest camp.| cap |
| Impost sobre les vendes | Especifiqueu l'import de l'impost sobre les vendes. | cap |
| Import total | L'import total de la línia de factures del proveïdor, inclosos els impostos. Aquest camp es calcula com a impost sobre *vendes de subtotals* + *·*. | cap |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
