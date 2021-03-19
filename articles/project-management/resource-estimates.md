---
title: Estimacions de recursos
description: En aquest tema es proporciona informació sobre com es calculen les estimacions de recursos al Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 98a61746f172b50bf6fa29cb0d21462cd616f417
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286506"
---
# <a name="resource-estimates"></a>Estimacions de recursos

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

Les estimacions de recursos provenen de l'esforç temporal que es defineix a l'estructura del desglossament del treball juntament amb les dimensions de preus aplicables. Normalment, el càlcul és **tarifa/h per funció x hores.** L'esforç gradual de cada recurs s'emmagatzema al registre d'assignació de recursos. El preu s'emmagatzema en una llista de preus predefinida. La conversió d'unitats s'aplica segons la llista de preus aplicable.

![Estimacions de recursos](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a>Preu de cost i moneda de cost per defecte

Els preus de cost es prenen per defecte de la unitat organitzativa.

## <a name="default-bill-rate-and-sales-currency"></a>Tarifa de facturació i moneda de vendes per defecte

Els preus de vendes s'apliquen un cop per acord. La jerarquia per als valors per defecte de la llista de preus de vendes és la següent:

1. Organització
2. Client
3. Oferta/contracte


[!INCLUDE[footer-include](../includes/footer-banner.md)]