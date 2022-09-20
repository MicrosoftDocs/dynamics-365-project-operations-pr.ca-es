---
title: Confirmeu les factures dels proveïdors del projecte
description: En aquest article s'explica com confirmar una factura de proveïdor de projecte a Microsoft Dynamics 365 Project Operations i es descriu l'impacte financer de la confirmació d'una factura del proveïdor del projecte.
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
# <a name="confirm-project-vendor-invoices"></a>Confirmeu les factures dels proveïdors del projecte

**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització

Quan es requereix el **paràmetre Confirmació manual per PM està habilitat, les factures de proveïdor que es creen tenen** Microsoft Dataverse l'estat Esborrany **.** Les factures dels proveïdors que es creïn d'aquesta manera s'han de revisar i confirmar manualment. Quan es desactiva el **paràmetre Confirmació manual** per PM, es confirmen automàticament les factures dels proveïdors que es creen.Dataverse No cal fer més accions. 

Un cop hàgiu verificat totes les línies d'una factura de proveïdor, Dynamics 365 Project Operations seleccioneu **Confirma** per confirmar la factura del proveïdor.

Quan seleccioneu **Confirma** a la factura d'un proveïdor, es produeix el comportament següent:

1. L'estat de la factura del proveïdor s'actualitza a **Confirmat**.
1. La factura confirmada del proveïdor i els seus registres relacionats passen a ser només de lectura i no es poden editar ni suprimir.
1. Si algun real de cost fa referència a la línia de factura del proveïdor com a part del procés de coincidència, s'inverteixen tots els reals de costos associats a la línia de factura del proveïdor referenciada.
1. Els nous reals de costos es creen mitjançant la informació de la línia de factures del proveïdor.
1. Ja no podeu crear revistes de correcció, processar recordatoris d'entrades de temps o cancel·lar l'aprovació de temps, despeses o materials originals que s'hagin invertit.
1. En Dynamics 365 Finance, el valor del cost **del** projecte s'actualitza mitjançant el diari d'integració de projectes i el compte d'integració de compres s'inverteix *després* de publicar el diari d'integració del projecte.

> [!NOTE]
> Si alguna línia d'una factura de proveïdor té un estat de verificació que no sigui **Complet**, la factura de proveïdor no es pot confirmar.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
