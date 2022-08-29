---
title: Confirmació d'una factura del proveïdor del projecte
description: En aquest article s'explica com confirmar una factura de proveïdor de projecte a Microsoft Dynamics 365 Project Operations i l'impacte financer de la confirmació d'una factura del proveïdor del projecte.
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

Un cop hàgiu verificat totes les línies d'una factura de proveïdor a Microsoft Dynamics 365 Project Operations, podeu utilitzar l'acció Confirma per confirmar la factura del proveïdor.

Quan seleccioneu **Confirma** a la factura d'un proveïdor, es produeix el comportament següent:

1. L'estat de la factura del proveïdor s'actualitza a **Confirmat**.
2. La factura confirmada del proveïdor i els seus registres relacionats passen a ser només de lectura i no es poden editar ni suprimir.
3. Si algun real de cost fa referència a la línia de factura del proveïdor com a part del procés de coincidència, s'inverteixen tots els reals de costos associats a la línia de factura del proveïdor referenciada.
4. Els nous reals de costos es creen mitjançant la informació de la línia de factures del proveïdor.
5. Un cop confirmada la factura del proveïdor, ja no podeu crear diaris de correcció, recuperar el temps d'entrada del procés ni cancel·lar l'aprovació de l'hora, la despesa o els materials reals originals que es van invertir.

> [!NOTE]
> Si alguna línia d'una factura de proveïdor té un estat de verificació que no sigui **Complet**, la factura de proveïdor no es pot confirmar.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
