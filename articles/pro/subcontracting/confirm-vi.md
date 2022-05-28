---
title: Confirmar una factura del proveïdor del projecte
description: En aquest tema s'explica com confirmar una factura de proveïdor de projectes a Microsoft Dynamics 365 Project Operations i l'impacte financer de confirmar una factura de proveïdor de projectes.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c248b3baec6d3f14a020e4fa93f3dad50c65b263
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8595716"
---
# <a name="confirm-a-project-vendor-invoice"></a>Confirmar una factura del proveïdor del projecte

[!include [banner](../../includes/dataverse-preview.md)]

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_

Un cop hàgiu verificat totes les línies d'una factura de proveïdor a Microsoft Dynamics 365 Project Operations, podeu utilitzar l'acció Confirma per confirmar la factura del proveïdor.

Quan seleccioneu **Confirma** en una factura de proveïdor, es produeix el comportament següent:

1. L'estat de la factura del proveïdor s'actualitza a **Confirmat**.
2. La factura de proveïdor confirmada i els registres relacionats es converteixen en només de lectura i no es poden editar ni suprimir.
3. Si els reals de cost fan referència a la línia de factura del proveïdor com a part del procés de coincidència, s'inverteixen tots els reals de cost associats a la línia de factura del proveïdor referenciat.
4. Els reals de costos nous es creen mitjançant la informació de la línia de factura del proveïdor.
5. Després de confirmar la factura del proveïdor, ja no podeu crear revistes de correcció, processar les retirades d'entrada de temps o cancel·lar l'aprovació de l'hora original, la despesa o els elements reals materials que s'han invertit.

> [!NOTE]
> Si alguna línia d'una factura de proveïdor té un estat de verificació que no sigui **Completa**, la factura del proveïdor no es pot confirmar.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
