---
title: Cancel·lació d'una factura del proveïdor del projecte
description: En aquest article s'explica com cancel·lar una factura de proveïdor de projectes a Microsoft Dynamics 365 Project Operations i l'impacte financer de cancel·lar una factura del proveïdor del projecte.
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

Un cop confirmada una factura de proveïdor, no es pot editar ni suprimir. Si s'ha produït un error en una factura de proveïdor que s'ha confirmat, podeu utilitzar l'acció Cancel·la per revertir l'impacte de la factura de proveïdor i crear una factura de proveïdor nova.

Quan seleccioneu **Cancel·la** a la factura de proveïdor, es produeix el comportament següent:

1. L'estat de la factura del venedor s'actualitza a **Cancel·lada**.
2. La factura cancel·lada del proveïdor i els seus registres relacionats passen a ser només de lectura i no es poden editar ni suprimir.
3. S'inverteixen els reals de costos que es van crear a partir de les línies de factura del proveïdor com a part de la confirmació de la factura del proveïdor.
4. Si els reals de costos estaven vinculats a les línies de factura del proveïdor com a part del procés de coincidència, la confirmació original de la factura del proveïdor les revertia. Durant la cancel·lació de factures del proveïdor, es tornen a crear aquests costos reals. Els orígens apunten a les entrades de temps, despeses o ús de material.
5. Després de cancel·lar la factura del proveïdor, podeu tornar a crear diaris de correcció, processar recordatoris d'entrada de temps i cancel·lar l'aprovació de l'hora, la despesa o els reals materials originals.

> [!NOTE]
> Només es poden cancel·lar les factures confirmades dels proveïdors del projecte. Les factures de proveïdors d'altres estats no es poden cancel·lar.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
