---
title: Cancel·lació d'una factura del proveïdor del projecte
description: En aquest article s'explica com cancel·lar una factura de proveïdor del projecte al Microsoft Dynamics 365 Project Operations i l'impacte financer de cancel·lar una factura de proveïdor del projecte.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 79d00a91f9ab2d66eab2f80349d6f1fba1934f94
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261078"
---
# <a name="cancel-a-project-vendor-invoice"></a>Cancel·lació d'una factura del proveïdor del projecte

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_

Un cop ha estat confirmada, una factura de proveïdor no es pot editar ni suprimir. Si s'ha produït un error en una factura de proveïdor que s'ha confirmat, podeu utilitzar l'acció Cancel·la per invertir l'impacte de la factura de proveïdor i crear una nova factura de proveïdor.

Quan seleccioneu **Cancel· la** en una factura de proveïdor, es produeix el comportament següent:

1. L'estat de la factura de proveïdor s'actualitza a **Cancel·lada**.
2. La factura de proveïdor cancel·lada i els registres relacionats passen a ser només de lectura i no es poden editar ni suprimir.
3. Els valors reals de cost creats a partir de les línies de factura de proveïdor com a part de la confirmació de la factura de proveïdor es reverteixen.
4. Si els valors reals de cost s'han enllaçat amb les línies de factura de proveïdor com a part del procés de coincidència, la confirmació de la factura de proveïdor original es reverteix. Durant la cancel·lació de la factura de proveïdor, els valors reals de cost es tornen a crear. Els orígens apunten a les entrades de temps, despesa o ús de materials.
5. Quan la factura del proveïdor es cancel·la, poden tornar a crear diaris de correcció, processar recuperacions d'entrades de temps i cancel·lar l'aprovació dels valors reals de temps, despesa i materials originals.

> [!NOTE]
> Només es poden cancel·lar les factures de proveïdor del projecte confirmades. Les factures de proveïdor amb altres estats no es poden cancel·lar.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
