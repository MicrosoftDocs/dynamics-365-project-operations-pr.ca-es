---
title: Assignació de projectes i tasques a una línia d'oferta basada en projectes
description: En aquest tema es proporciona informació sobre com assignar projectes i tasques a una línia de tasca basada en projectes.
author: rumant
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d714304f408050babae1a6ba74268979e0b6ea4b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272736"
---
# <a name="map-projects-and-tasks-to-a-project-based-quote-line"></a><span data-ttu-id="b84ab-103">Assignació de projectes i tasques a una línia d'oferta basada en projectes</span><span class="sxs-lookup"><span data-stu-id="b84ab-103">Map projects and tasks to a project-based quote line</span></span>

<span data-ttu-id="b84ab-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_</span><span class="sxs-lookup"><span data-stu-id="b84ab-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b84ab-105">A les línies d'ofertes basades en projectes, podeu assignar les tasques específiques d'un projecte que ja està associat a una línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="b84ab-105">On project-based quote lines, you can map the specific tasks of a project that is already associated to a quote line.</span></span>

<span data-ttu-id="b84ab-106">Quan assigneu tasques a una línia d'oferta, els elements següents que heu definit a la línia d'oferta només s'aplicaran a aquestes tasques:</span><span class="sxs-lookup"><span data-stu-id="b84ab-106">When you map tasks to a quote line, the following items you defined on the quote line will only apply to those tasks:</span></span>

- <span data-ttu-id="b84ab-107">Mètode de facturació</span><span class="sxs-lookup"><span data-stu-id="b84ab-107">Billing method</span></span>
- <span data-ttu-id="b84ab-108">Opcions d'imputabilitat</span><span class="sxs-lookup"><span data-stu-id="b84ab-108">Chargeability options</span></span>
- <span data-ttu-id="b84ab-109">Límits que no s'han de superar</span><span class="sxs-lookup"><span data-stu-id="b84ab-109">Not-to-exceed limits</span></span>
- <span data-ttu-id="b84ab-110">Clients</span><span class="sxs-lookup"><span data-stu-id="b84ab-110">Customers</span></span>

<span data-ttu-id="b84ab-111">Per exemple, pot ser que tingueu un projecte en què una fase sigui de preu fix i que la resta de fases siguin de temps i materials.</span><span class="sxs-lookup"><span data-stu-id="b84ab-111">For example, you might have a project where one phase is fixed price and all the other phases are time and materials.</span></span> <span data-ttu-id="b84ab-112">En aquest cas, podeu associar la primera fase i totes les tasques secundàries a la línia d'oferta per a aquesta fase amb un mètode de facturació de preu fix.</span><span class="sxs-lookup"><span data-stu-id="b84ab-112">In this case, you can associate the first phase, and all of its child tasks, to the quote line for that phase with a fixed price billing method.</span></span> <span data-ttu-id="b84ab-113">A continuació, podeu associar totes les altres fases a la línia d'oferta basada en temps i materials.</span><span class="sxs-lookup"><span data-stu-id="b84ab-113">You can then associate all the other phases to the time and materials-based quote line.</span></span>

## <a name="associate-tasks-to-project-based-quote-lines"></a><span data-ttu-id="b84ab-114">Associar tasques a línies d’oferta basades en projectes</span><span class="sxs-lookup"><span data-stu-id="b84ab-114">Associate tasks to project-based quote lines</span></span>

<span data-ttu-id="b84ab-115">Podeu associar tasques amb línies d'oferta des de les ubicacions següents:</span><span class="sxs-lookup"><span data-stu-id="b84ab-115">You can associate tasks with quote lines from the following locations:</span></span>

- <span data-ttu-id="b84ab-116">Pàgina **Projecte** > pestanya **Facturació de tasques** (òptima)</span><span class="sxs-lookup"><span data-stu-id="b84ab-116">**Project** page > **Task billing** tab (optimal)</span></span>
- <span data-ttu-id="b84ab-117">Pàgina **Línia d'oferta** > pestanya **Tasques imputables**</span><span class="sxs-lookup"><span data-stu-id="b84ab-117">**Quote Line** page > **Chargeable tasks** tab</span></span> 

### <a name="from-the-project-page"></a><span data-ttu-id="b84ab-118">Des de la pàgina Projecte</span><span class="sxs-lookup"><span data-stu-id="b84ab-118">From the Project page</span></span>

<span data-ttu-id="b84ab-119">La pàgina **Projecte** proporciona l'experiència òptima per associar tasques a línies d'oferta.</span><span class="sxs-lookup"><span data-stu-id="b84ab-119">The **Project** page provides the optimal experience for associating tasks to quote lines.</span></span> <span data-ttu-id="b84ab-120">Podeu utilitzar aquesta pàgina per seleccionar diverses tasques i associar-les totes, a més de les tasques secundàries, a la línia d'oferta seleccionada.</span><span class="sxs-lookup"><span data-stu-id="b84ab-120">You can use this page to select multiple tasks and associate all of them, plus their child tasks, to the selected quote line.</span></span>

1. <span data-ttu-id="b84ab-121">A la pestanya **General** d'una línia d'oferta basada en projectes, verifiqueu que el camp **Projecte** s'hagi emplenat.</span><span class="sxs-lookup"><span data-stu-id="b84ab-121">On the **General** tab of a project–based quote line, verify the **Project** field is filled out.</span></span>
2. <span data-ttu-id="b84ab-122">Al camp **Tasques incloses**, seleccioneu **Només les tasques seleccionades**.</span><span class="sxs-lookup"><span data-stu-id="b84ab-122">In the **Included tasks** field, select **Selected tasks only**.</span></span>
3. <span data-ttu-id="b84ab-123">Deseu la línia d'oferta basada en projectes.</span><span class="sxs-lookup"><span data-stu-id="b84ab-123">Save the project-based quote line.</span></span> <span data-ttu-id="b84ab-124">Quan el formulari s'actualitza, la pestanya **Tasques imputables** es mostra.</span><span class="sxs-lookup"><span data-stu-id="b84ab-124">When the form refreshes, the **Chargeable tasks** tab displays.</span></span>
4. <span data-ttu-id="b84ab-125">A la pestanya **General**, seleccioneu l'enllaç per al projecte des del camp **Projecte**.</span><span class="sxs-lookup"><span data-stu-id="b84ab-125">On the **General** tab, select the link for the project from the **Project** field.</span></span>
5. <span data-ttu-id="b84ab-126">A la pàgina **Projecte**, seleccioneu la pestanya **Facturació de tasques**.</span><span class="sxs-lookup"><span data-stu-id="b84ab-126">On the **Project** page, select the **Task billing** tab.</span></span>
6. <span data-ttu-id="b84ab-127">A la segona quadrícula, que s'aplica a la configuració de facturació específica de la tasca, seleccioneu una o diverses tasques i, a continuació, seleccioneu **Associa les línies d'oferta**.</span><span class="sxs-lookup"><span data-stu-id="b84ab-127">In the second grid, which applies to task-specific billing setup, select one or more tasks and then select **Associate quote lines**.</span></span>
7. <span data-ttu-id="b84ab-128">A la pàgina de diàleg que apareix, seleccioneu una línia d'oferta que mostri les línies d'oferta basades en projectes a l'oferta.</span><span class="sxs-lookup"><span data-stu-id="b84ab-128">In the dialog page that appears, select a quote line that displays project-based quote lines on the quote.</span></span>
8. <span data-ttu-id="b84ab-129">Al camp **Tipus de facturació**, indiqueu si aquestes tasques són imputables o no.</span><span class="sxs-lookup"><span data-stu-id="b84ab-129">In the **Billing type** field, indicate if these tasks are chargeable or non-chargeable.</span></span>
9. <span data-ttu-id="b84ab-130">Marqueu la casella de selecció per indicar si l'associació ha d'incloure les tasques secundàries de les tasques seleccionades.</span><span class="sxs-lookup"><span data-stu-id="b84ab-130">Select the check box to indicate if the association should include child tasks of the selected tasks.</span></span> <span data-ttu-id="b84ab-131">Si marqueu la casella s'associaran les tasques secundàries de les tasques seleccionades a la línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="b84ab-131">Checking the box will associate the child tasks of the selected tasks to the quote line.</span></span>
10. <span data-ttu-id="b84ab-132">Trieu **D'acord** per tancar el quadre de diàleg.</span><span class="sxs-lookup"><span data-stu-id="b84ab-132">Select **OK** to close the dialog.</span></span>

### <a name="from-the-quote-line-page"></a><span data-ttu-id="b84ab-133">Des de la pàgina de la línia d'oferta</span><span class="sxs-lookup"><span data-stu-id="b84ab-133">From the Quote line page</span></span>

<span data-ttu-id="b84ab-134">Podeu associar tasques de projecte a línies d'oferta des de la pestanya **Tasques imputables** a la pàgina **Línia d'oferta**.</span><span class="sxs-lookup"><span data-stu-id="b84ab-134">You can associate project tasks to quote lines from the **Chargeable tasks** tab on **Quote line** page.</span></span>

>[!NOTE]
><span data-ttu-id="b84ab-135">El lloc òptim per associar tasques de projecte a línies d'oferta és la pestanya **Facturació de tasques** a la pàgina **Projecte**.</span><span class="sxs-lookup"><span data-stu-id="b84ab-135">The optimal place to associate project tasks to quote lines is on the **Task billing** tab on the **Project** page.</span></span> <span data-ttu-id="b84ab-136">Si associeu tasques de la pestanya **Tasques imputables** a la pàgina **Línia d'oferta**, heu d'associar cada projecte manualment.</span><span class="sxs-lookup"><span data-stu-id="b84ab-136">If you associate tasks from the **Chargeable tasks** tab on **Quote line** page, you must manually associate each project.</span></span>

1. <span data-ttu-id="b84ab-137">A la pestanya **General** d'una línia d'oferta basada en projectes, verifiqueu que hi hagi un projecte seleccionat al camp **Projecte**.</span><span class="sxs-lookup"><span data-stu-id="b84ab-137">On the **General** tab of a project–based quote line, verify that there is a project selected in the **Project** field.</span></span>
2. <span data-ttu-id="b84ab-138">Al camp **Tasques incloses**, seleccioneu **Només les tasques seleccionades**.</span><span class="sxs-lookup"><span data-stu-id="b84ab-138">In the **Included tasks** field, select **Selected tasks only**.</span></span>
3. <span data-ttu-id="b84ab-139">Deseu la línia d'oferta basada en projectes.</span><span class="sxs-lookup"><span data-stu-id="b84ab-139">Save the project-based quote line.</span></span> <span data-ttu-id="b84ab-140">Quan el formulari s'actualitza, la pestanya **Tasques imputables** es mostra.</span><span class="sxs-lookup"><span data-stu-id="b84ab-140">When the form refreshes, the **Chargeable tasks** tab displays.</span></span>
4. <span data-ttu-id="b84ab-141">A la pestanya **Tasques imputables**, seleccioneu **Afegeix una tasca de línia d'oferta**.</span><span class="sxs-lookup"><span data-stu-id="b84ab-141">On the **Chargeable tasks** tab, select **Add a quote line task**.</span></span>
5. <span data-ttu-id="b84ab-142">A la pàgina **Tasca de la línia d'oferta**, al camp **Tasques**, seleccioneu la tasca i, al camp **Tipus de facturació**, seleccioneu **Desa**.</span><span class="sxs-lookup"><span data-stu-id="b84ab-142">On the **Quote line task** page, in the **Tasks** field, select the task and in the **Billing type** field, select **Save**.</span></span> 
6. <span data-ttu-id="b84ab-143">Tanqueu la pàgina.</span><span class="sxs-lookup"><span data-stu-id="b84ab-143">Close the page.</span></span> <span data-ttu-id="b84ab-144">La tasca seleccionada s'associa ara a la línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="b84ab-144">The selected task is now associated to the quote line.</span></span>

## <a name="disassociate-tasks-from-projectbased-quote-lines"></a><span data-ttu-id="b84ab-145">Desassociar tasques de línies d’oferta basades en projectes</span><span class="sxs-lookup"><span data-stu-id="b84ab-145">Disassociate tasks from project–based quote lines</span></span>

### <a name="from-the-project-page"></a><span data-ttu-id="b84ab-146">Des de la pàgina Projecte</span><span class="sxs-lookup"><span data-stu-id="b84ab-146">From the Project page</span></span>

<span data-ttu-id="b84ab-147">Aquest mètode proporciona l'experiència més òptima per desassociar tasques de línies d'oferta.</span><span class="sxs-lookup"><span data-stu-id="b84ab-147">This method provides the most optimal experience for disassociating tasks from quote lines.</span></span> <span data-ttu-id="b84ab-148">Podeu utilitzar seleccionar diverses tasques i desassociar-les totes, a més de les tasques secundàries, de la línia d'oferta seleccionada.</span><span class="sxs-lookup"><span data-stu-id="b84ab-148">You can select multiple tasks and disassociate all of the them, plus their child tasks, from the selected quote line.</span></span>

1. <span data-ttu-id="b84ab-149">A la pestanya **General** d'una línia d'oferta basada en projectes, al camp **Projecte**, seleccioneu l'enllaç del projecte.</span><span class="sxs-lookup"><span data-stu-id="b84ab-149">On the **General** tab of a project–based quote line, in the **Project** field, select the project link.</span></span>
2. <span data-ttu-id="b84ab-150">A la pàgina **Projecte**, seleccioneu la pestanya **Facturació de tasques**.</span><span class="sxs-lookup"><span data-stu-id="b84ab-150">On the **Project** page, select the **Task billing** tab.</span></span>
3. <span data-ttu-id="b84ab-151">A la segona quadrícula, que s'aplica a la configuració de facturació específica de la tasca, seleccioneu una o diverses tasques i, a continuació, seleccioneu **Desassocia les línies d'oferta**.</span><span class="sxs-lookup"><span data-stu-id="b84ab-151">In the second grid, which applies to task-specific billing setup, select one or more tasks, and then select **Disassociate quote lines**.</span></span>
4. <span data-ttu-id="b84ab-152">A la pàgina de diàleg que apareix, seleccioneu una línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="b84ab-152">In the dialog page that appears, select a quote line.</span></span>
5. <span data-ttu-id="b84ab-153">Marqueu la casella de selecció per indicar si l'associació també s'ha de suprimir de les tasques secundàries de les tasques seleccionades.</span><span class="sxs-lookup"><span data-stu-id="b84ab-153">Select the check box to indicate whether the association should also be removed from child tasks of the selected tasks.</span></span> <span data-ttu-id="b84ab-154">Si marqueu la casella també es desassociaran les tasques secundàries de les tasques seleccionades a la línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="b84ab-154">Checking the box will also disassociate the child tasks of the selected tasks to the quote line.</span></span>
6. <span data-ttu-id="b84ab-155">Seleccioneu **D'acord**.</span><span class="sxs-lookup"><span data-stu-id="b84ab-155">Select **OK**.</span></span> <span data-ttu-id="b84ab-156">Un missatge d'advertiment us informa que, si suprimiu aquesta associació, els valors reals registrats prèviament a la tasca podrien revertir-se.</span><span class="sxs-lookup"><span data-stu-id="b84ab-156">A warning message informs you that if you remove this association, any actuals previously recorded on the task could be reversed.</span></span> 
7. <span data-ttu-id="b84ab-157">Seleccioneu **D'acord** per continuar i suprimir l'associació entre la tasca i la línia d'oferta basada en projectes.</span><span class="sxs-lookup"><span data-stu-id="b84ab-157">Select **OK** to continue and remove the association between the task and the project-based quote line.</span></span>

### <a name="from-the-quote-line-page"></a><span data-ttu-id="b84ab-158">Des de la pàgina de la línia d'oferta</span><span class="sxs-lookup"><span data-stu-id="b84ab-158">From the Quote line page</span></span>

<span data-ttu-id="b84ab-159">També podeu desassociar tasques de projecte a línies d'oferta des de la pestanya **Tasques imputables** a la pàgina **Línia d'oferta**.</span><span class="sxs-lookup"><span data-stu-id="b84ab-159">You can also disassociate project tasks to quote lines from the **Chargeable tasks** tab on **Quote line** page.</span></span>

1. <span data-ttu-id="b84ab-160">A la pestanya **Tasques imputables**, seleccioneu **Suprimeix una tasca de línia d'oferta**.</span><span class="sxs-lookup"><span data-stu-id="b84ab-160">On the **Chargeable tasks** tab, select **Delete a quote line task**.</span></span>
2. <span data-ttu-id="b84ab-161">Seleccioneu **D'acord**.</span><span class="sxs-lookup"><span data-stu-id="b84ab-161">Select **OK**.</span></span> <span data-ttu-id="b84ab-162">Un missatge d'advertiment us informa que, si suprimiu aquesta associació, els valors reals registrats prèviament a la tasca podrien revertir-se.</span><span class="sxs-lookup"><span data-stu-id="b84ab-162">A warning message informs you that if you remove this association, any actuals previously recorded on the task could be reversed.</span></span> 
3. <span data-ttu-id="b84ab-163">Seleccioneu **D'acord** per continuar i suprimir l'associació entre la tasca i la línia d'oferta basada en projectes.</span><span class="sxs-lookup"><span data-stu-id="b84ab-163">Select **OK** to continue and remove the association between the task and the project-based quote line.</span></span>

>[!NOTE]
> <span data-ttu-id="b84ab-164">Aquest procediment no suprimeix la tasca del projecte.</span><span class="sxs-lookup"><span data-stu-id="b84ab-164">This procedure doesn't delete the task from the project.</span></span> <span data-ttu-id="b84ab-165">Només elimina l'associació de la tasca de la línia d'oferta basada en projectes.</span><span class="sxs-lookup"><span data-stu-id="b84ab-165">It only removes the task association from the project-based quote line.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]