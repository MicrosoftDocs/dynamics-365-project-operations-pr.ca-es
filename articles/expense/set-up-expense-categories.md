---
title: Configuració de les categories de despesa
description: En aquest tema es proporciona informació sobre la configuració de les categories de despesa i categories compartides per als informes de despeses.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 13e72e4b852fd0edac5ad35d5162e74b016bce33
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123771"
---
# <a name="set-up-expense-categories"></a><span data-ttu-id="229ff-103">Configuració de les categories de despesa</span><span class="sxs-lookup"><span data-stu-id="229ff-103">Set up expense categories</span></span>

<span data-ttu-id="229ff-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_</span><span class="sxs-lookup"><span data-stu-id="229ff-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="229ff-105">Quan els empleats creen informes de despeses, cada despesa que registren s'ha d'associar amb una categoria de despesa.</span><span class="sxs-lookup"><span data-stu-id="229ff-105">When employees create expense reports, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="229ff-106">Les categories de despeses es deriven de les categories compartides que es poden compartir amb els organismes jurídics de l'organització.</span><span class="sxs-lookup"><span data-stu-id="229ff-106">Expense categories are derived from shared categories that can be shared across the legal entities in your organization.</span></span> <span data-ttu-id="229ff-107">Segons la definició de l'organització, aquestes categories de despesa també es poden compartir en altres àrees.</span><span class="sxs-lookup"><span data-stu-id="229ff-107">Depending on how your organization is defined, these expense categories can also be shared in other areas.</span></span> <span data-ttu-id="229ff-108">Segons la definició de l'organització i de l'orientació de l'equip d'implementació, cal que determineu si les categories que s'utilitzen a l'administració de despeses només s'utilitzaran a l'administració de despeses o s'han de compartir en altres àrees.</span><span class="sxs-lookup"><span data-stu-id="229ff-108">Based on the definition of your organization and guidance from the implementation team, you must determine whether the categories that are used in Expense management will be used only in Expense management or should be shared in other areas.</span></span>

> [!NOTE]
> <span data-ttu-id="229ff-109">Aquestes categories es poden compartir entre l'administració de projectes i la comptabilitat i l'administració de despeses, o entre l'administració de projectes i la comptabilitat i la producció.</span><span class="sxs-lookup"><span data-stu-id="229ff-109">These categories can be shared between Project management and accounting and Expense management, or between Project management and accounting and Production.</span></span> <span data-ttu-id="229ff-110">No obstant, no es poden compartir entre l'administració de despeses i la producció.</span><span class="sxs-lookup"><span data-stu-id="229ff-110">However, they can't be shared between Expense management and Production.</span></span>

<span data-ttu-id="229ff-111">Per poder començar el procés de configuració, cal que prendre les següents decisions per a cada categoria de despesa:</span><span class="sxs-lookup"><span data-stu-id="229ff-111">Before you can begin the setup process, the following decisions must be made for each expense category:</span></span>

- <span data-ttu-id="229ff-112">Quina és la categoria de despesa?</span><span class="sxs-lookup"><span data-stu-id="229ff-112">What is the expense category?</span></span> <span data-ttu-id="229ff-113">Alguns exemples són categories per a vols, hotels o quilometratge.</span><span class="sxs-lookup"><span data-stu-id="229ff-113">Examples include categories for flights, hotel, or mileage.</span></span>
- <span data-ttu-id="229ff-114">La categoria de despesa també pot utilitzar-se en l'administració de projectes i la comptabilitat?</span><span class="sxs-lookup"><span data-stu-id="229ff-114">Can the expense category also be used in Project management and accounting?</span></span> <span data-ttu-id="229ff-115">Si és així, també heu de prendre les següents decisions:</span><span class="sxs-lookup"><span data-stu-id="229ff-115">If it can, you must also make the following decisions:</span></span>

    - <span data-ttu-id="229ff-116">Quins comptes de cost s'utilitzaran per a les despeses següents?</span><span class="sxs-lookup"><span data-stu-id="229ff-116">Which cost accounts will be used for the following expenses?</span></span>

        - <span data-ttu-id="229ff-117">Cost</span><span class="sxs-lookup"><span data-stu-id="229ff-117">Cost</span></span>
        - <span data-ttu-id="229ff-118">Assignació de nòmines</span><span class="sxs-lookup"><span data-stu-id="229ff-118">Payroll allocation</span></span>
        - <span data-ttu-id="229ff-119">En curs: valor de cost</span><span class="sxs-lookup"><span data-stu-id="229ff-119">WIP-cost value</span></span>
        - <span data-ttu-id="229ff-120">Cost: article</span><span class="sxs-lookup"><span data-stu-id="229ff-120">Cost-item</span></span>
        - <span data-ttu-id="229ff-121">En curs: valor de cost: article</span><span class="sxs-lookup"><span data-stu-id="229ff-121">WIP-cost value-item</span></span>
        - <span data-ttu-id="229ff-122">Pèrdua acumulada</span><span class="sxs-lookup"><span data-stu-id="229ff-122">Accrued loss</span></span>
        - <span data-ttu-id="229ff-123">En curs: pèrdua acumulada</span><span class="sxs-lookup"><span data-stu-id="229ff-123">WIP-accrued loss</span></span>

    - <span data-ttu-id="229ff-124">Quins comptes d'ingressos s'utilitzaran per a les següents fonts d'ingressos?</span><span class="sxs-lookup"><span data-stu-id="229ff-124">Which revenue accounts will be used for the following sources of revenue?</span></span>

        - <span data-ttu-id="229ff-125">Ingressos facturats</span><span class="sxs-lookup"><span data-stu-id="229ff-125">Invoiced revenue</span></span>
        - <span data-ttu-id="229ff-126">Ingressos acumulats: valor de vendes</span><span class="sxs-lookup"><span data-stu-id="229ff-126">Accrued revenue-sales value</span></span>
        - <span data-ttu-id="229ff-127">En curs: valor de vendes</span><span class="sxs-lookup"><span data-stu-id="229ff-127">WIP-sales value</span></span>
        - <span data-ttu-id="229ff-128">Ingressos acumulats: producció</span><span class="sxs-lookup"><span data-stu-id="229ff-128">Accrued revenue-production</span></span>
        - <span data-ttu-id="229ff-129">En curs: producció</span><span class="sxs-lookup"><span data-stu-id="229ff-129">WIP-production</span></span>
        - <span data-ttu-id="229ff-130">Ingressos acumulats: beneficis</span><span class="sxs-lookup"><span data-stu-id="229ff-130">Accrued revenue-profit</span></span>
        - <span data-ttu-id="229ff-131">En curs: beneficis</span><span class="sxs-lookup"><span data-stu-id="229ff-131">WIP-profit</span></span>
        - <span data-ttu-id="229ff-132">Ingressos acumulats: subscripció</span><span class="sxs-lookup"><span data-stu-id="229ff-132">Accrued revenue-subscription</span></span>
        - <span data-ttu-id="229ff-133">En curs: subscripció</span><span class="sxs-lookup"><span data-stu-id="229ff-133">WIP-subscription</span></span>

- <span data-ttu-id="229ff-134">Quin és el tipus de despesa?</span><span class="sxs-lookup"><span data-stu-id="229ff-134">What is the expense type?</span></span>
- <span data-ttu-id="229ff-135">Què és el mètode de pagament per defecte per a la categoria de despesa?</span><span class="sxs-lookup"><span data-stu-id="229ff-135">What is the default payment method for the expense category?</span></span>
- <span data-ttu-id="229ff-136">Les despeses de la categoria de despesa s'hauran de desglossar?</span><span class="sxs-lookup"><span data-stu-id="229ff-136">Do expenses in the expense category have to be itemized?</span></span>
- <span data-ttu-id="229ff-137">Què és el compte per defecte principal per a la categoria de despesa?</span><span class="sxs-lookup"><span data-stu-id="229ff-137">What is the main default account for the expense category?</span></span>
- <span data-ttu-id="229ff-138">Què és el grup d'impostos de vendes de l'element per a la categoria de despeses?</span><span class="sxs-lookup"><span data-stu-id="229ff-138">What is the default item sales tax group for the expense category?</span></span>
- <span data-ttu-id="229ff-139">Es permeten mètodes de pagament addicionals per a la categoria de despeses?</span><span class="sxs-lookup"><span data-stu-id="229ff-139">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="229ff-140">Si és així, quins són?</span><span class="sxs-lookup"><span data-stu-id="229ff-140">If so, what are they?</span></span>
- <span data-ttu-id="229ff-141">Hi ha subcategories en aquesta categoria de despeses?</span><span class="sxs-lookup"><span data-stu-id="229ff-141">Are there subcategories in this expense category?</span></span> <span data-ttu-id="229ff-142">Si hi ha subcategories, també heu de prendre les següents decisions:</span><span class="sxs-lookup"><span data-stu-id="229ff-142">If there are subcategories, you must also make the following decisions:</span></span>

    - <span data-ttu-id="229ff-143">S'exclou cap subcategoria de la recuperació d'impostos?</span><span class="sxs-lookup"><span data-stu-id="229ff-143">Are any of the subcategories excluded from tax recovery?</span></span>
    - <span data-ttu-id="229ff-144">Quin és el grup d'impostos de vendes de l'element de les subcategories?</span><span class="sxs-lookup"><span data-stu-id="229ff-144">What is the item sales tax group of the subcategories?</span></span>
