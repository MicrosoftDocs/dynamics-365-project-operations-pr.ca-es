---
title: Confirmació de factures del proveïdor del projecte
description: En aquest article s'explica com confirmar una factura de proveïdor del projecte al Microsoft Dynamics 365 Project Operations i es descriu l'impacte financer de confirmar una factura de proveïdor del projecte.
author: suvaidya
ms.date: 8/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 9739b15753aa34c51a0aa1e6dfeb7f590655ca7a
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475465"
---
# <a name="confirm-project-vendor-invoices"></a>Confirmació de factures del proveïdor del projecte

**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització

Quan el paràmetre **Cal la confirmació manual del PM** està habilitat, les factures de proveïdor creades al Microsoft Dataverse tenen l'estat **Esborrany**. Les factures de proveïdor creades d'aquesta manera s'han de revisar i confirmar manualment. Quan el paràmetre **Cal la confirmació manual del PM** està inhabilitat, les factures de proveïdor creades al Dataverse es confirmen automàticament. No cal realitzar cap més acció. 

Un cop hàgiu comprovat totes les línies d'una factura de proveïdor al Dynamics 365 Project Operations, seleccioneu **Confirma** per confirmar la factura de proveïdor.

Quan seleccioneu **Confirma** en una factura de proveïdor, es produeix el comportament següent:

1. L'estatus de la factura de proveïdor s'actualitza a **Confirmada**.
1. La factura de proveïdor confirmada i els registres relacionats passen a ser només de lectura i no es poden editar ni suprimir.
1. Si els valors reals de cost fan referència a la línia de la factura de proveïdor com a part del procés de coincidència, es revertiran tots els valors reals de cost associats amb la línia de la factura de proveïdor a la qual es fa referència.
1. Es creen valors reals de cost nous utilitzant la informació de la línia de la factura de proveïdor.
1. Ja no podeu crear diaris de correcció, processar recuperacions d'entrades de temps ni cancel·lar l'aprovació dels valors reals de temps, despesa i materials originals.
1. Al Dynamics 365 Finance, el valor de **Cost del projecte** s'actualitza amb el llibre diari d'integració del projecte i el compte d'integració de proveïment es *reverteix* quan es publica el llibre diari d'integració del projecte.

> [!NOTE]
> Si qualsevol línia d'una factura de proveïdor té un estat de verificació que no sigui **Completa**, la factura de proveïdor no es pot confirmar.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
