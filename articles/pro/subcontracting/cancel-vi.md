---
title: Cancel·lar una factura del proveïdor del projecte
description: En aquest tema s'explica com cancel·lar una factura del proveïdor del projecte a Microsoft Dynamics 365 Project Operations i l'impacte financer de cancel·lar una factura del proveïdor del projecte.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 87f6bdca30c5779e3d70922e75609ff4cdfca167
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580628"
---
# <a name="cancel-a-project-vendor-invoice"></a>Cancel·lar una factura del proveïdor del projecte

[!include [banner](../../includes/dataverse-preview.md)]

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_

Després de confirmar una factura de proveïdor, no es pot editar ni suprimir. Si s'ha produït un error en una factura de proveïdor que s'ha confirmat, podeu utilitzar l'acció Cancel·la per invertir l'impacte de la factura del proveïdor i crear una factura de proveïdor nova.

Quan seleccioneu **Cancel·la** en una factura de proveïdor, es produeix el comportament següent:

1. L'estat de la factura del proveïdor s'actualitza a Cancel·lat **·**.
2. La factura del proveïdor cancel·lada i els registres relacionats es converteixen en només de lectura i no es poden editar ni suprimir.
3. S'inverteixen tots els reals de cost que s'han creat en funció de les línies de factura del proveïdor com a part de la confirmació de la factura del proveïdor.
4. Si els reals de cost estaven enllaçats a les línies de factura del proveïdor com a part del procés de coincidència, la confirmació original de la factura del proveïdor les va invertir. Durant la cancel·lació de la factura del proveïdor, aquests costos reals es tornen a crear. Els orígens apunten al temps, la despesa o les entrades d'ús de material.
5. Després de cancel·lar la factura del proveïdor, podeu tornar a crear revistes de correcció, processar les retirades d'entrada de temps i cancel·lar l'aprovació de l'hora original, la despesa o els elements reals materials.

> [!NOTE]
> Només es poden cancel·lar les factures confirmades del proveïdor del projecte. Les factures del proveïdor d'altres estats no es poden cancel·lar.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
