---
title: Línies de factures del proveïdor per a fites
description: En aquest tema s'explica com crear línies de factures de proveïdor per a fites en una subcontracta.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 4fa11e2a4f459016b3ce141b03fe97e55c9a2759
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8590610"
---
# <a name="vendor-invoice-lines-for-milestones"></a>Línies de factures del proveïdor per a fites

[!include [banner](../../includes/dataverse-preview.md)]

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_

Una factura de proveïdor a Microsoft Dynamics 365 Project Operations pot tenir línies de factura de proveïdor per a fites definides en una línia de subcontractació. Els administradors de projectes poden utilitzar línies de factures de proveïdors per registrar els costos dels serveis que s'adquireixen com a costos basats en fites que s'incorren en serveis o productes que s'adquireixen per al projecte.

Les línies de factura del proveïdor per a fites sempre han de fer referència a una línia de subcontractació que tingui un mètode de facturació de preu fix. Quan una línia de factura de proveïdor per a fites fa referència a una línia de subcontractació, els gestors de projectes podran fer coincidir i verificar els costos subjacents de temps, despeses o materials que fan referència a aquesta línia de subcontractació contra la fita que està facturant el proveïdor.

La taula següent proporciona informació sobre els camps de les línies de factures del proveïdor per a les fites.

| Camp | Descripció | Impacte funcional |
| --- | --- | --- |
| Nom | El nom de la línia de factura del proveïdor, per ajudar-vos a identificar-la. | Aquest nom es mostrarà com la primera columna de totes les cerques que es basen en línies de factura de proveïdor. |
| Descripció | Una breu descripció dels serveis que el proveïdor està facturant a la línia de factura del proveïdor. | cap |
| Subcontracte | La subcontractació sobre la que es van encarregar originalment els serveis. | Quan se selecciona una subcontracta per a la factura del proveïdor, totes les línies de la factura del proveïdor heretaran aquesta selecció. Una factura de proveïdor no pot tenir línies de factura de proveïdor que fan referència a subcontractacions diferents. |
| Línia subcontractada | La línia de subcontractació en la que es van encarregar els serveis. La llista de línies de subcontractació que es poden seleccionar es limita a les línies de la subcontractació seleccionada. | Quan se selecciona una línia de subcontractació en una línia de factura de proveïdor per a fites, els **camps Categoria Funció** i **Transacció** i camps relacionats amb el producte són irrellevants i no estan disponibles. Els **camps Grup de quantitat** **, Unitat** i **Unitat** tampoc són rellevants per a les línies de factura de proveïdor basades en fites. |
| Data de la transacció | La data en què es registrarà el cost real de la línia de factura del proveïdor al projecte. | cap |
| Classe de la transacció | Seleccioneu **Milestone** per registrar una factura de proveïdor per a una fita completada definida en una línia de subcontractació. | cap |
| Fita | Seleccioneu la fita definida a la línia de subcontractació relacionada que es marca com **a Preparada per facturar**. | Les fites de la línia de subcontractació que tenen un estat de **Llest per facturar** es poden seleccionar en una línia de factura del proveïdor. |
| Project | El nom del projecte en què s'han utilitzat els serveis que s'estan facturant. | Aquest camp és obligatori i no es pot deixar en blanc. |
| Tasca | El nom de la tasca del projecte en què s'han utilitzat els serveis que s'estan facturant. Aquest camp només està disponible si se selecciona un projecte. La selecció d'una tasca de projecte és opcional. | Si aquest camp es deixa en blanc, el gestor del projecte pot fer coincidir la línia de factura del proveïdor amb la classe de transaccions de la línia de subcontractació relacionada que es registra en qualsevol tasca del projecte. Si la línia de factura del proveïdor no fa referència a una línia de subcontractació i aquest camp es deixa en blanc, el cost real creat per la línia de factura del proveïdor no s'enllaçarà amb cap real de vendes no facturat. En aquest cas, si es configura la facturació basada en tasques, és possible que els costos no es puguin facturar al client final. |
| Import de la fita | Introduïu el valor de la fita definida a la línia de subcontractació que està a punt per facturar. | cap |
| Impost sobre les vendes | Especifiqueu l'import de l'impost sobre les vendes. | cap |
| Import total | L'import total de la línia de factures del proveïdor, inclosos els impostos. Aquest camp es calcula com a *import* + *fita Impost sobre* les vendes. | cap |

> [!NOTE]
> Quan es crea una línia de factura de proveïdor que fa referència a una fita de la línia de subcontractació, l'estat de la fita de subcontractació s'actualitza a la **factura del proveïdor creada**. A continuació, quan es confirma aquesta factura del proveïdor, l'estat de la fita de la línia de subcontracta s'actualitza a la **factura del proveïdor confirmada**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
