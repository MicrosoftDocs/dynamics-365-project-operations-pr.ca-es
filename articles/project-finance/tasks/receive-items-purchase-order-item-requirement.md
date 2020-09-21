---
title: Rebre articles en una comanda de compra d'un requisit d'article
description: Aquest tema explica com rebre articles en una comanda de compra d'un requisit d'article.
author: KimANelson
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.assetid: c61e3a5e-da3d-4f4c-87fa-03dea19f6936
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c5ed287aa24aff647ef1dc625f9e9f5f086ee662
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749430"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a><span data-ttu-id="6c28d-103">Rebre articles en una comanda de compra d'un requisit d'article</span><span class="sxs-lookup"><span data-stu-id="6c28d-103">Receive items on purchase order from item requirement</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6c28d-104">Aquest tema explica com rebre articles en una comanda de compra d'un requisit d'article.</span><span class="sxs-lookup"><span data-stu-id="6c28d-104">This topic explains how to receive items on a purchase order from an item requirement.</span></span>

<span data-ttu-id="6c28d-105">Mitjançant l'ús d'un requisit d'article en comptes d'una transacció d'articles, podeu planificar l'entrega just abans d'utilitzar l'article, crear una comanda de compra, incloure l'article a l'estructura de l'acord de comerç i incloure el requisit d'article a la planificació de la producció.</span><span class="sxs-lookup"><span data-stu-id="6c28d-105">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span> 

<span data-ttu-id="6c28d-106">Aquesta tasca utilitza el conjunt de dades d'USSI.</span><span class="sxs-lookup"><span data-stu-id="6c28d-106">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="6c28d-107">A la subfinestra de navegació, aneu a **Mòduls > Administració de projectes i comptabilitat > Projectes > Tots els projectes**.</span><span class="sxs-lookup"><span data-stu-id="6c28d-107">In the navigation pane, go to **Modules > Project management and accounting > Projects > All projects**.</span></span>
2. <span data-ttu-id="6c28d-108">A la llista, seleccioneu l'enllaç de la fila desitjada.</span><span class="sxs-lookup"><span data-stu-id="6c28d-108">In the list, select the link in the desired row.</span></span>
3. <span data-ttu-id="6c28d-109">A la subfinestra d'acció, seleccioneu **Planificació**.</span><span class="sxs-lookup"><span data-stu-id="6c28d-109">On the Action Pane, select **Plan**.</span></span>
4. <span data-ttu-id="6c28d-110">Seleccioneu **Requisits d'article**.</span><span class="sxs-lookup"><span data-stu-id="6c28d-110">Select **Item requirements**.</span></span>
5. <span data-ttu-id="6c28d-111">Seleccioneu **Crea**.</span><span class="sxs-lookup"><span data-stu-id="6c28d-111">Select **New**.</span></span>
6. <span data-ttu-id="6c28d-112">A la fila nova, introduïu o seleccioneu un valor al camp **Número d'article**.</span><span class="sxs-lookup"><span data-stu-id="6c28d-112">In the new row, enter or select a value in the **Item number** field.</span></span>
7. <span data-ttu-id="6c28d-113">Al camp **Quantitat**, introduïu un número.</span><span class="sxs-lookup"><span data-stu-id="6c28d-113">In the **Quantity** field, enter a number.</span></span>
8. <span data-ttu-id="6c28d-114">Seleccioneu **Desa**.</span><span class="sxs-lookup"><span data-stu-id="6c28d-114">Select **Save**.</span></span>
9. <span data-ttu-id="6c28d-115">A la subfinestra d'acció, seleccioneu **Administra**.</span><span class="sxs-lookup"><span data-stu-id="6c28d-115">On the Action Pane, select **Manage**.</span></span>
10. <span data-ttu-id="6c28d-116">Seleccioneu **Funcions**.</span><span class="sxs-lookup"><span data-stu-id="6c28d-116">Select **Functions**.</span></span>
11. <span data-ttu-id="6c28d-117">Seleccioneu **Crea una comanda de compra**.</span><span class="sxs-lookup"><span data-stu-id="6c28d-117">Select **Create purchase order**.</span></span>
12. <span data-ttu-id="6c28d-118">Marqueu la casella de selecció **Inclou-ho tot**.</span><span class="sxs-lookup"><span data-stu-id="6c28d-118">Select the **Include all** check box.</span></span>
13. <span data-ttu-id="6c28d-119">Al camp **Compte del proveïdor**, introduïu o seleccioneu un valor.</span><span class="sxs-lookup"><span data-stu-id="6c28d-119">In the **Vendor account** field, enter or select a value.</span></span>
14. <span data-ttu-id="6c28d-120">Seleccioneu **D'acord**.</span><span class="sxs-lookup"><span data-stu-id="6c28d-120">Select **OK**.</span></span>
15. <span data-ttu-id="6c28d-121">A la subfinestra de navegació, aneu a **Mòduls > Compte a pagar > Comandes de compra > Totes les comandes de compra**.</span><span class="sxs-lookup"><span data-stu-id="6c28d-121">In the navigation pane, go to **Modules > Accounts payable > Purchase orders > All purchase orders**.</span></span>
16. <span data-ttu-id="6c28d-122">A la llista, seleccioneu l'enllaç de la fila desitjada.</span><span class="sxs-lookup"><span data-stu-id="6c28d-122">In the list, select the link in the desired row.</span></span>
17. <span data-ttu-id="6c28d-123">A la subfinestra d'acció, seleccioneu **Compra**.</span><span class="sxs-lookup"><span data-stu-id="6c28d-123">On the Action Pane, select **Purchase**.</span></span>
18. <span data-ttu-id="6c28d-124">Seleccioneu **Confirma**.</span><span class="sxs-lookup"><span data-stu-id="6c28d-124">Select **Confirm**.</span></span>
19. <span data-ttu-id="6c28d-125">A la subfinestra d'acció, seleccioneu **Rep**.</span><span class="sxs-lookup"><span data-stu-id="6c28d-125">On the Action Pane, select **Receive**.</span></span>
20. <span data-ttu-id="6c28d-126">Seleccioneu **Rebut del producte**.</span><span class="sxs-lookup"><span data-stu-id="6c28d-126">Select **Product receipt**.</span></span>
21. <span data-ttu-id="6c28d-127">Al camp **Rebut de producte**, escriviu un valor.</span><span class="sxs-lookup"><span data-stu-id="6c28d-127">In the **Product receipt** field, type a value.</span></span>
22. <span data-ttu-id="6c28d-128">Seleccioneu **D'acord**.</span><span class="sxs-lookup"><span data-stu-id="6c28d-128">Select **OK**.</span></span>

