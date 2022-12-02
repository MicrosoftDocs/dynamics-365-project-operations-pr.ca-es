---
title: Confirmació d'una factura del proveïdor del projecte
description: En aquest article s'explica com confirmar una factura de proveïdor del projecte al Microsoft Dynamics 365 Project Operations i l'impacte financer de confirmar una factura de proveïdor del projecte.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 4dafbe64e0727957068d68f510202a12871b62aa
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261499"
---
# <a name="confirm-a-project-vendor-invoice"></a>Confirmació d'una factura del proveïdor del projecte

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_

Un cop hàgiu comprovat totes les línies d'una factura de proveïdor al Microsoft Dynamics 365 Project Operations, podeu utilitzar l'acció Confirma per confirmar la factura de proveïdor.

Quan seleccioneu **Confirma** en una factura de proveïdor, es produeix el comportament següent:

1. L'estat de la factura de proveïdor s'actualitza a **Confirmada**.
2. La factura de proveïdor confirmada i els registres relacionats passen a ser només de lectura i no es poden editar ni suprimir.
3. Si els valors reals de cost fan referència a la línia de la factura de proveïdor com a part del procés de coincidència, es revertiran tots els valors reals de cost associats amb la línia de la factura de proveïdor a la qual es fa referència.
4. Es creen valors reals de cost nous utilitzant la informació de la línia de la factura de proveïdor.
5. Quan la factura de proveïdor es confirma, ja no podeu crear diaris de correcció, processar recuperacions d'entrades de temps ni cancel·lar l'aprovació dels valors reals de temps, despesa i materials originals que s'ha revertit.

> [!NOTE]
> Si qualsevol línia d'una factura de proveïdor té un estat de verificació que no sigui **Completa**, la factura de proveïdor no es pot confirmar.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
