---
title: Configurar els costos estàndard per al treball i les despeses
description: En aquest tema s'explica la manera de configurar els costos estàndard per al treball i les despeses d'un projecte.
author: KimANelson
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.assetid: fa7c024f-4b18-4d29-9fd4-9c430cd83fad
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f3e796cc03aeaa28938c56ce37d5075755248dfa
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749586"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="cb10f-103">Configurar els costos estàndard per al treball i les despeses</span><span class="sxs-lookup"><span data-stu-id="cb10f-103">Configure standard costs for labor and expenses</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cb10f-104">En aquest tema s'explica la manera de configurar els costos estàndard per al treball i les despeses d'un projecte.</span><span class="sxs-lookup"><span data-stu-id="cb10f-104">This topic explains how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="cb10f-105">Aquesta tasca utilitza el conjunt de dades d'USSI.</span><span class="sxs-lookup"><span data-stu-id="cb10f-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="cb10f-106">A la subfinestra de navegació, aneu a **Mòduls > Administració de projectes i comptabilitat > Configuració > Preus > Preu de cost (hora)**.</span><span class="sxs-lookup"><span data-stu-id="cb10f-106">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (hour)**.</span></span>
2. <span data-ttu-id="cb10f-107">Seleccioneu **Crea**.</span><span class="sxs-lookup"><span data-stu-id="cb10f-107">Select **New**.</span></span>
3. <span data-ttu-id="cb10f-108">En el camp **Data d'efectivitat**, introduïu una data.</span><span class="sxs-lookup"><span data-stu-id="cb10f-108">In the **Effective date** field, enter a date.</span></span>
4. <span data-ttu-id="cb10f-109">Al camp **Preu de cost**, introduïu un número.</span><span class="sxs-lookup"><span data-stu-id="cb10f-109">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="cb10f-110">Podeu configurar un preu de cost estàndard per a la categoria del projecte o bé podeu configurar un preu de cost per número de treballador, número de projecte, categoria, data o qualsevol combinació d'aquests valors.</span><span class="sxs-lookup"><span data-stu-id="cb10f-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="cb10f-111">El preu de cost que s'aplica és el preu de cost amb el nivell màxim de detall.</span><span class="sxs-lookup"><span data-stu-id="cb10f-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="cb10f-112">Seleccioneu **Desa**.</span><span class="sxs-lookup"><span data-stu-id="cb10f-112">Select **Save**.</span></span>
6. <span data-ttu-id="cb10f-113">A la subfinestra de navegació, aneu a **Mòduls > Administració de projectes i comptabilitat > Configuració > Preus > Preu de vendes (hora)**.</span><span class="sxs-lookup"><span data-stu-id="cb10f-113">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (hour)**.</span></span>
7. <span data-ttu-id="cb10f-114">Seleccioneu **Crea**.</span><span class="sxs-lookup"><span data-stu-id="cb10f-114">Select **New**.</span></span>
8. <span data-ttu-id="cb10f-115">En el camp **Data d'efectivitat**, introduïu una data.</span><span class="sxs-lookup"><span data-stu-id="cb10f-115">In the **Effective date** field, enter a date.</span></span>
9. <span data-ttu-id="cb10f-116">Seleccioneu una opció al camp **Vàlid durant**.</span><span class="sxs-lookup"><span data-stu-id="cb10f-116">In the **Valid for** field, select an option.</span></span>
10. <span data-ttu-id="cb10f-117">Al camp **Preu**, introduïu un número.</span><span class="sxs-lookup"><span data-stu-id="cb10f-117">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="cb10f-118">Podeu configurar un preu de venda estàndard per a transaccions per hora o per a una categoria de projecte.</span><span class="sxs-lookup"><span data-stu-id="cb10f-118">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="cb10f-119">També podeu configurar els preus de les vendes per número de treballador, número de projecte, categoria, data de la transacció o qualsevol combinació d'aquests valors.</span><span class="sxs-lookup"><span data-stu-id="cb10f-119">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="cb10f-120">El preu de vendes real, que s'aplica quan un treballador introdueix una transacció al diari Hora, és el preu de vendes amb el nivell de detall més alt.</span><span class="sxs-lookup"><span data-stu-id="cb10f-120">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="cb10f-121">Per exemple, si es configuren tant un preu de vendes general com un preu de vendes específic del treballador, el preu de vendes específic del treballador s'utilitza.</span><span class="sxs-lookup"><span data-stu-id="cb10f-121">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
11. <span data-ttu-id="cb10f-122">Seleccioneu **Desa**.</span><span class="sxs-lookup"><span data-stu-id="cb10f-122">Select **Save**.</span></span>
12. <span data-ttu-id="cb10f-123">Tanqueu la pàgina.</span><span class="sxs-lookup"><span data-stu-id="cb10f-123">Close the page.</span></span>
13. <span data-ttu-id="cb10f-124">A la subfinestra de navegació, aneu a **Mòduls > Administració de projectes i comptabilitat > Configuració > Preus > Preu de cost (despesa)**.</span><span class="sxs-lookup"><span data-stu-id="cb10f-124">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (expense)**.</span></span>
14. <span data-ttu-id="cb10f-125">Seleccioneu **Crea**.</span><span class="sxs-lookup"><span data-stu-id="cb10f-125">Select **New**.</span></span>
15. <span data-ttu-id="cb10f-126">En el camp **Data d'efectivitat**, introduïu una data.</span><span class="sxs-lookup"><span data-stu-id="cb10f-126">In the **Effective date** field, enter a date.</span></span>
16. <span data-ttu-id="cb10f-127">Al camp **Preu de cost**, introduïu un número.</span><span class="sxs-lookup"><span data-stu-id="cb10f-127">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="cb10f-128">Es poden emplenar diversos camps, però aquest és el mínim necessari per desar el registre.</span><span class="sxs-lookup"><span data-stu-id="cb10f-128">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
17. <span data-ttu-id="cb10f-129">Seleccioneu **Desa**.</span><span class="sxs-lookup"><span data-stu-id="cb10f-129">Select **Save**.</span></span>
18. <span data-ttu-id="cb10f-130">A la subfinestra de navegació, aneu a **Mòduls > Administració de projectes i comptabilitat > Configuració > Preus > Preu de vendes (despesa)**.</span><span class="sxs-lookup"><span data-stu-id="cb10f-130">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (expense)**.</span></span>
19. <span data-ttu-id="cb10f-131">Seleccioneu **Crea**.</span><span class="sxs-lookup"><span data-stu-id="cb10f-131">Select **New**.</span></span>
20. <span data-ttu-id="cb10f-132">En el camp **Data d'efectivitat**, introduïu una data.</span><span class="sxs-lookup"><span data-stu-id="cb10f-132">In the **Effective date** field, enter a date.</span></span>
21. <span data-ttu-id="cb10f-133">Seleccioneu una opció al camp **Vàlid durant**.</span><span class="sxs-lookup"><span data-stu-id="cb10f-133">In the **Valid for** field, select an option.</span></span>
22. <span data-ttu-id="cb10f-134">Al camp **Preu**, introduïu un número.</span><span class="sxs-lookup"><span data-stu-id="cb10f-134">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="cb10f-135">El preu de vendes real, que s'aplica quan un treballador introdueix transaccions en un diari de despeses, és el preu de vendes amb el nivell de detall més alt.</span><span class="sxs-lookup"><span data-stu-id="cb10f-135">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="cb10f-136">Per exemple, si es configuren tant un preu de vendes general com un d'específic del treballador, el preu de vendes específic del treballador s'utilitza.</span><span class="sxs-lookup"><span data-stu-id="cb10f-136">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
23. <span data-ttu-id="cb10f-137">Seleccioneu **Desa**.</span><span class="sxs-lookup"><span data-stu-id="cb10f-137">Select **Save**.</span></span>
