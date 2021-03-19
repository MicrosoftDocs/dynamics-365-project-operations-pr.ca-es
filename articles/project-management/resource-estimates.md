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
# <a name="resource-estimates"></a><span data-ttu-id="8d9da-103">Estimacions de recursos</span><span class="sxs-lookup"><span data-stu-id="8d9da-103">Resource estimates</span></span>

<span data-ttu-id="8d9da-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_</span><span class="sxs-lookup"><span data-stu-id="8d9da-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8d9da-105">Les estimacions de recursos provenen de l'esforç temporal que es defineix a l'estructura del desglossament del treball juntament amb les dimensions de preus aplicables.</span><span class="sxs-lookup"><span data-stu-id="8d9da-105">Resource estimates come from time-phased effort that is defined in the work breakdown structure along with applicable pricing dimensions.</span></span> <span data-ttu-id="8d9da-106">Normalment, el càlcul és **tarifa/h per funció x hores.**</span><span class="sxs-lookup"><span data-stu-id="8d9da-106">Typically, the calculation is **rate/hr for each role x hours.**</span></span> <span data-ttu-id="8d9da-107">L'esforç gradual de cada recurs s'emmagatzema al registre d'assignació de recursos.</span><span class="sxs-lookup"><span data-stu-id="8d9da-107">The time-phased effort for each resource is stored in the resource assignment record.</span></span> <span data-ttu-id="8d9da-108">El preu s'emmagatzema en una llista de preus predefinida.</span><span class="sxs-lookup"><span data-stu-id="8d9da-108">The pricing is stored in a pre-defined price list.</span></span> <span data-ttu-id="8d9da-109">La conversió d'unitats s'aplica segons la llista de preus aplicable.</span><span class="sxs-lookup"><span data-stu-id="8d9da-109">Unit conversion is applied based on the applicable price list.</span></span>

![Estimacions de recursos](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a><span data-ttu-id="8d9da-111">Preu de cost i moneda de cost per defecte</span><span class="sxs-lookup"><span data-stu-id="8d9da-111">Default cost price and cost currency</span></span>

<span data-ttu-id="8d9da-112">Els preus de cost es prenen per defecte de la unitat organitzativa.</span><span class="sxs-lookup"><span data-stu-id="8d9da-112">Cost prices are defaulted from the Organizational Unit.</span></span>

## <a name="default-bill-rate-and-sales-currency"></a><span data-ttu-id="8d9da-113">Tarifa de facturació i moneda de vendes per defecte</span><span class="sxs-lookup"><span data-stu-id="8d9da-113">Default bill rate and sales currency</span></span>

<span data-ttu-id="8d9da-114">Els preus de vendes s'apliquen un cop per acord.</span><span class="sxs-lookup"><span data-stu-id="8d9da-114">Sales prices are applied once per deal.</span></span> <span data-ttu-id="8d9da-115">La jerarquia per als valors per defecte de la llista de preus de vendes és la següent:</span><span class="sxs-lookup"><span data-stu-id="8d9da-115">The hierarchy for sale price list defaulting is as follows:</span></span>

1. <span data-ttu-id="8d9da-116">Organització</span><span class="sxs-lookup"><span data-stu-id="8d9da-116">Organization</span></span>
2. <span data-ttu-id="8d9da-117">Client</span><span class="sxs-lookup"><span data-stu-id="8d9da-117">Customer</span></span>
3. <span data-ttu-id="8d9da-118">Oferta/contracte</span><span class="sxs-lookup"><span data-stu-id="8d9da-118">Quote/contract</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]