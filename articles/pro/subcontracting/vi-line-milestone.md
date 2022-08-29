---
title: Línies de factura del proveïdor per a fites
description: En aquest article s'explica com crear línies de factures de proveïdors per a fites en un subcontractat.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f066c2ac7377a989a92a9ae2e9a732d3c979a0db
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 08/11/2022
ms.locfileid: "9260983"
---
# <a name="vendor-invoice-lines-for-milestones"></a>Línies de factura del proveïdor per a fites

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_

Una factura de proveïdor a Microsoft Dynamics 365 Project Operations pot tenir línies de factures de proveïdors per a fites definides en una línia de subcontractació. Els gestors de projectes poden utilitzar línies de factures de proveïdors per a fites per registrar els costos dels serveis que s'obtenen com a costos basats en fites que s'incorren en serveis o productes que s'adquireixen per al projecte.

Les línies de factura del venedor per fites han de fer sempre referència a una línia de subcontractació que tingui un mètode de facturació de preu fix. Quan una línia de factures de proveïdors per fites faci referència a una línia de subcontractació, els gestors de projectes podran igualar i verificar els costos subjacents de temps, despeses o materials que facin referència a aquesta línia de subcontractació amb la fita que està facturant el venedor.

La taula següent proporciona informació sobre els camps de les línies de factures de proveïdors per a fites.

| Camp | Descripció | Impacte funcional |
| --- | --- | --- |
| Nom | El nom de la línia de factura del venedor, per ajudar a la identificació. | Aquest nom es mostrarà com a primera columna de totes les cerques basades en línies de factures de proveïdor. |
| Descripció | Una breu descripció dels serveis que està facturant el venedor a la línia de factura del proveïdor. | cap |
| Subcontracte | La subcontractació en què es van encarregar originalment els serveis. | Quan se selecciona un subcontractista per a la factura del venedor, totes les línies de la factura del venedor heretaran aquesta selecció. Una factura de proveïdor no pot tenir línies de factures de proveïdors que facin referència a diferents subcontractes. |
| Línia de subcontractació | La línia de subcontractació en la qual es van encarregar els serveis. La llista de línies de subcontractació que es poden seleccionar es limita a les línies de la subcontractació seleccionada. | Quan se selecciona una línia de subcontractació en una línia de factures de proveïdor per a fites, els **camps Rol** i **transacció** i camps relacionats amb el producte són irrellevants i no estan disponibles. Els **camps Quantitat**, **Unitat** i **Grup** d'unitats tampoc no són rellevants per a les línies de factures de proveïdors basades en fites. |
| Data de la transacció | La data en què es registrarà al projecte el cost real de la línia de factura del proveïdor. | cap |
| Classe de la transacció | Seleccioneu **Milestone** per registrar una factura del proveïdor per a una fita completada que s'ha definit en una línia de subcontractació. | cap |
| Fita | Seleccioneu la fita que es defineix a la línia de subcontractació relacionada que es marca com **a Ready to Invoice**. | Les fites de línies de subcontractació que tinguin un estat de **Ready to invoice** es poden seleccionar en una línia de factures del proveïdor. |
| Project | El nom del projecte en què es van utilitzar els serveis que s'estan facturant. | Aquest camp és obligatori i no es pot deixar en blanc. |
| Tasca | El nom de la tasca del projecte en què es van utilitzar els serveis que s'estan facturant. Aquest camp només està disponible si se selecciona un projecte. La selecció d'una tasca de projecte és opcional. | Si aquest camp es deixa en blanc, el gestor del projecte pot fer coincidir la línia de factura del proveïdor amb la classe de transaccions de la línia de subcontractació relacionada que es registra en qualsevol tasca del projecte. Si la línia de factures del proveïdor no fa referència a una línia de subcontractació i aquest camp es deixa en blanc, el cost real creat per la línia de factures del proveïdor no estarà vinculat a cap real de vendes no codificat. En aquest cas, si es configura la facturació basada en tasques, és possible que els costos no es puguin facturar al client final. |
| Import de la fita | Introduïu el valor de la fita que es defineix a la línia de subcontractació que està llesta per ser facturada. | cap |
| Impost sobre les vendes | Especifiqueu l'import de l'impost sobre les vendes. | cap |
| Import total | L'import total de la línia de factures del proveïdor, inclosos els impostos. Aquest camp es calcula com a *Import* + *de la fita Impost sobre* les vendes. | cap |

> [!NOTE]
> Quan es crea una línia de factura del proveïdor que fa referència a una fita de línia de subcontractació, s'actualitza l'estat de la fita de la subcontractació a **la factura del proveïdor creada**. A continuació, quan es confirma aquesta factura del proveïdor, l'estat de la fita de la línia de subcontractació s'actualitza a **la factura del proveïdor confirmada**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
