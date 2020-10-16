---
title: Estimacions de recursos
description: En aquest tema es proporciona informació sobre com es calculen les estimacions de recursos al Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 2ebde2b3c5bcfb5faa02ee476065ac34b1953432
ms.sourcegitcommit: f255b2cbf290973ce62fe2c1c121bd1df15a7392
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/01/2020
ms.locfileid: "3928544"
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
