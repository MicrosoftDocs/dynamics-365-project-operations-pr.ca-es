---
title: Comandes de compra per a un projecte
description: En aquest article es descriuen els diversos mètodes que podeu utilitzar per crear comandes de compra per a un projecte. El mètode que utilitzeu depèn de la finalitat de la comanda de compra i quan es consumeixen i carregaran els articles adquirits en un projecte.
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a4975b9f9e20906fb1259e36a07d8ef3db4f4fee
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749482"
---
# <a name="purchase-orders-for-a-project"></a><span data-ttu-id="8bc1d-104">Comandes de compra per a un projecte</span><span class="sxs-lookup"><span data-stu-id="8bc1d-104">Purchase orders for a project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8bc1d-105">En aquest article es descriuen els diversos mètodes que podeu utilitzar per crear comandes de compra per a un projecte.</span><span class="sxs-lookup"><span data-stu-id="8bc1d-105">This article describes the various methods that you can use to create purchase orders for a project.</span></span> <span data-ttu-id="8bc1d-106">El mètode que utilitzeu depèn de la finalitat de la comanda de compra i quan es consumeixen i carregaran els articles adquirits en un projecte.</span><span class="sxs-lookup"><span data-stu-id="8bc1d-106">The method that you use depends on the purpose of the purchase order, and when the purchased items are consumed and charged to a project.</span></span>

### <a name="methods-for-creating-a-purchase-order"></a><span data-ttu-id="8bc1d-107">Mètodes per crear una comanda de compra</span><span class="sxs-lookup"><span data-stu-id="8bc1d-107">Methods for creating a purchase order</span></span>

<span data-ttu-id="8bc1d-108">Podeu utilitzar un dels mètodes següents per crear una comanda de compra a Administració de projectes i comptabilitat.</span><span class="sxs-lookup"><span data-stu-id="8bc1d-108">You can use one of the following methods to create a purchase order in Project management and accounting.</span></span> <span data-ttu-id="8bc1d-109">La finalitat de la comanda de compra determina quan es consumeix la comanda de compra i, per tant, quan es consumeixen i carregaran els articles en un projecte.</span><span class="sxs-lookup"><span data-stu-id="8bc1d-109">The purpose of the purchase order determines when the purchase order is consumed and, therefore, when items are charged to a project.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8bc1d-110">Mètode</span><span class="sxs-lookup"><span data-stu-id="8bc1d-110">Method</span></span></th>
<th><span data-ttu-id="8bc1d-111">Finalitat</span><span class="sxs-lookup"><span data-stu-id="8bc1d-111">Purpose</span></span></th>
<th><span data-ttu-id="8bc1d-112">Consum d'articles</span><span class="sxs-lookup"><span data-stu-id="8bc1d-112">Consumption of items</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8bc1d-113">Creeu una comanda de compra directament des d'un projecte.</span><span class="sxs-lookup"><span data-stu-id="8bc1d-113">Create a purchase order directly from a project.</span></span></td>
<td><span data-ttu-id="8bc1d-114">Utilitzeu aquest mètode per comprar articles d'un proveïdor extern per al consum en un projecte.</span><span class="sxs-lookup"><span data-stu-id="8bc1d-114">Use this method to purchase items from an external vendor for consumption on a project.</span></span> <span data-ttu-id="8bc1d-115">Podeu crear la comanda de compra de dues maneres:</span><span class="sxs-lookup"><span data-stu-id="8bc1d-115">You can create the purchase order in two ways:</span></span>
<ul>
<li><span data-ttu-id="8bc1d-116">Des del projecte en si mateix.</span><span class="sxs-lookup"><span data-stu-id="8bc1d-116">From the project itself.</span></span> <span data-ttu-id="8bc1d-117">En aquest cas, el projecte ja s'ha definit per a la comanda de compra.</span><span class="sxs-lookup"><span data-stu-id="8bc1d-117">In this case, the project is already defined for the purchase order.</span></span></li>
<li><span data-ttu-id="8bc1d-118">Navegant a la comanda de compra del projecte.</span><span class="sxs-lookup"><span data-stu-id="8bc1d-118">By navigating to the project purchase order.</span></span> <span data-ttu-id="8bc1d-119">Heu de seleccionar el proveïdor i el projecte per als quals crear la comanda de compra.</span><span class="sxs-lookup"><span data-stu-id="8bc1d-119">You must select both the vendor and the project to create the purchase order for.</span></span></li>
</ul></td>
<td><span data-ttu-id="8bc1d-120">Els articles es consumeixen en actualitzar la factura del proveïdor.</span><span class="sxs-lookup"><span data-stu-id="8bc1d-120">Items are consumed when the vendor invoice is updated.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8bc1d-121">Creeu una comanda de compra d'una comanda de vendes.</span><span class="sxs-lookup"><span data-stu-id="8bc1d-121">Create a purchase order from a sales order.</span></span></td>
<td><span data-ttu-id="8bc1d-122">Utilitzeu aquest mètode per comprar articles quan creeu una comanda de vendes d'un projecte.</span><span class="sxs-lookup"><span data-stu-id="8bc1d-122">Use this method to purchase items when you create a sales order from a project.</span></span></td>
<td><span data-ttu-id="8bc1d-123">Els articles es consumeixen quan la comanda de vendes s'ha facturat al client.</span><span class="sxs-lookup"><span data-stu-id="8bc1d-123">Items are consumed when the sales order is invoiced to the customer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8bc1d-124">Creeu una comanda de compra a partir d'un requisit d'articles.</span><span class="sxs-lookup"><span data-stu-id="8bc1d-124">Create a purchase order from an item requirement.</span></span></td>
<td><span data-ttu-id="8bc1d-125">Utilitzeu aquest mètode per comprar articles quan creeu un requisit d'articles d'un projecte.</span><span class="sxs-lookup"><span data-stu-id="8bc1d-125">Use this method to purchase items when you create an item requirement from a project.</span></span></td>
<td><span data-ttu-id="8bc1d-126">Els articles es consumeixen quan s'actualitza l'albarà de requisits d'articles.</span><span class="sxs-lookup"><span data-stu-id="8bc1d-126">Items are consumed when the item requirement packing slip is updated.</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE] 
> <span data-ttu-id="8bc1d-127">En actualitzar la factura o l'albarà del venedor, se us demanarà que actualitzeu l'albarà del requisit d'articles.</span><span class="sxs-lookup"><span data-stu-id="8bc1d-127">When you update the vendor invoice or packing slip, you're prompted to update the packing slip on the item requirement.</span></span>

<span data-ttu-id="8bc1d-128">Per obtenir més informació, vegeu [Rebre articles en una comanda de compra per a un requisit d'articles](tasks/receive-items-purchase-order-item-requirement.md).</span><span class="sxs-lookup"><span data-stu-id="8bc1d-128">For more information, see [Receive items on purchase order from item requirement](tasks/receive-items-purchase-order-item-requirement.md).</span></span>

