---
title: Progrés dels projectes i consum de cost
description: En aquest tema es proporciona informació sobre com fer el seguiment del progrés del projecte i del consum de costos.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 0d742164-5469-421d-8917-63160a81f651
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8aa5814938129f30885d8161a7c86197ab013364
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749553"
---
# <a name="project-progress-and-cost-consumption"></a><span data-ttu-id="e0c03-103">Progrés dels projectes i consum de cost</span><span class="sxs-lookup"><span data-stu-id="e0c03-103">Project progress and cost consumption</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="e0c03-104">La necessitat de fer un seguiment del progrés davant d'una planificació varia segons la indústria.</span><span class="sxs-lookup"><span data-stu-id="e0c03-104">The need to track progress against a schedule varies by industry.</span></span> <span data-ttu-id="e0c03-105">Algunes indústries fan el seguiment en un nivell granular, mentre que altres indústries fan el seguiment en un nivell superior.</span><span class="sxs-lookup"><span data-stu-id="e0c03-105">Some industries track at a granular level, whereas other industries track at a higher level.</span></span> <span data-ttu-id="e0c03-106">En aquest tema es mostra la manera de planificar per tal de satisfer els requisits de la vostra organització.</span><span class="sxs-lookup"><span data-stu-id="e0c03-106">This topic shows how to schedule in order to meet your organization's requirements.</span></span>

## <a name="effort-tracking-view"></a><span data-ttu-id="e0c03-107">Vista Seguiment de l'esforç</span><span class="sxs-lookup"><span data-stu-id="e0c03-107">Effort tracking view</span></span>

<span data-ttu-id="e0c03-108">La visualització **Seguiment de l'esforç** segueix el progrés de les tasques a la planificació.</span><span class="sxs-lookup"><span data-stu-id="e0c03-108">The **Effort tracking** view tracks the progress of tasks in the schedule.</span></span> <span data-ttu-id="e0c03-109">Compara les hores d'esforç real que s'han invertit en una tasca amb les hores d'esforç planificades per a aquesta tasca.</span><span class="sxs-lookup"><span data-stu-id="e0c03-109">It compares the actual effort hours that have been spent on a task to the planned effort hours for that task.</span></span> <span data-ttu-id="e0c03-110">El PSA utilitza les següents fórmules per calcular les mètriques de seguiment:</span><span class="sxs-lookup"><span data-stu-id="e0c03-110">PSA uses the following formulas to calculate the tracking metrics:</span></span>

- <span data-ttu-id="e0c03-111">Percentatge de progrés = Esforç real invertit fins al moment ÷ Esforç planificat per a la tasca</span><span class="sxs-lookup"><span data-stu-id="e0c03-111">Progress percentage = Actual effort spent to date ÷ Planned effort for the task</span></span> 
- <span data-ttu-id="e0c03-112">Estimació per completar (ETC) = Esforç planificat - Esforç real dedicat fins al moment</span><span class="sxs-lookup"><span data-stu-id="e0c03-112">Estimate to complete (ETC) = Planned effort – Actual effort spent to date</span></span> 
- <span data-ttu-id="e0c03-113">Estimació per completar (EAC) = Esforç restant + Esforç real dedicat fins al moment</span><span class="sxs-lookup"><span data-stu-id="e0c03-113">Estimate at complete (EAC) = Remaining effort + Actual effort spent to date</span></span> 
- <span data-ttu-id="e0c03-114">Variació d'esforç previst = Esforç planificat – EAC</span><span class="sxs-lookup"><span data-stu-id="e0c03-114">Projected effort variance = Planned effort – EAC</span></span>

<span data-ttu-id="e0c03-115">El PSA mostra una projecció de la variació de l'esforç en la tasca.</span><span class="sxs-lookup"><span data-stu-id="e0c03-115">PSA shows a projection of the effort variance on the task.</span></span> <span data-ttu-id="e0c03-116">Si l'EAC és més gran que l'esforç planificat, es preveu que la tasca comporti més temps del que s'ha planejat originalment.</span><span class="sxs-lookup"><span data-stu-id="e0c03-116">If the EAC is more than the planned effort, the task is projected to take more time than was originally planned.</span></span> <span data-ttu-id="e0c03-117">Per tant, va per darrere de la planificació.</span><span class="sxs-lookup"><span data-stu-id="e0c03-117">Therefore, it's behind schedule.</span></span> <span data-ttu-id="e0c03-118">Si l'EAC és més petit que l'esforç planificat, es preveu que la tasca comporti menys temps del que s'ha planejat originalment.</span><span class="sxs-lookup"><span data-stu-id="e0c03-118">If the EAC is less than the planned effort, the task is projected to take less time than was originally planned.</span></span> <span data-ttu-id="e0c03-119">Per tant, va per davant de la planificació.</span><span class="sxs-lookup"><span data-stu-id="e0c03-119">Therefore, it's ahead of schedule.</span></span>

## <a name="re-projecting-effort"></a><span data-ttu-id="e0c03-120">Tornar a projectar l'esforç</span><span class="sxs-lookup"><span data-stu-id="e0c03-120">Re-projecting effort</span></span>

<span data-ttu-id="e0c03-121">És habitual que un administrador de projecte revisi les estimacions originals d'una tasca.</span><span class="sxs-lookup"><span data-stu-id="e0c03-121">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="e0c03-122">Les reprojeccions de projectes són la percepció de les estimacions d'un administrador de projecte, donat l'estat actual del projecte.</span><span class="sxs-lookup"><span data-stu-id="e0c03-122">Project re-projections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="e0c03-123">No obstant, no recomanem que els administradors de projectes canviïn els números de la línia de base, ja que la línia de base del projecte representa la font de veritat establerta de l'estimació de la planificació i el cost del projecte, i totes les parts interessades del projecte l'han acordat.</span><span class="sxs-lookup"><span data-stu-id="e0c03-123">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="e0c03-124">Hi ha dues maneres de fer que un administrador del projecte pugui tornar a projectar l'esforç de les tasques:</span><span class="sxs-lookup"><span data-stu-id="e0c03-124">There are two ways that a project manager can re-project effort on tasks:</span></span>

- <span data-ttu-id="e0c03-125">Substituir l'ETC per defecte amb una nova estimació de l'esforç real restant de la tasca.</span><span class="sxs-lookup"><span data-stu-id="e0c03-125">Override the default ETC with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="e0c03-126">Substituir el percentatge de progrés per defecte amb una nova estimació del progrés real de la tasca.</span><span class="sxs-lookup"><span data-stu-id="e0c03-126">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="e0c03-127">Cadascuna d'aquestes aproximacions provoca un nou càlcul de l'ETC de la tasca, l'EAC i el percentatge de progrés, i la variació de l'esforç projectat d'una tasca.</span><span class="sxs-lookup"><span data-stu-id="e0c03-127">Each of these approaches cause a recalculation of the task's ETC, EAC, and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="e0c03-128">També es torna a calcular l'EAC, l'ETC i el percentatge de progrés de les tasques de resum, i produeixen una nova projecció de la variació d'esforç.</span><span class="sxs-lookup"><span data-stu-id="e0c03-128">The EAC, ETC, and progress percentage on the summary tasks are also recalculated, and produce a new projection of effort variance.</span></span>

## <a name="re-projection-of-effort-on-summary-tasks"></a><span data-ttu-id="e0c03-129">Reprojecció de l'esforç en tasques de resum</span><span class="sxs-lookup"><span data-stu-id="e0c03-129">Re-projection of effort on summary tasks</span></span>

<span data-ttu-id="e0c03-130">Es pot tornar a projectar l'esforç en tasques de resum o contenidor.</span><span class="sxs-lookup"><span data-stu-id="e0c03-130">Effort on summary tasks or container tasks can be re-projected.</span></span> <span data-ttu-id="e0c03-131">Independentment de si l'usuari torna a fer una projecció amb l'esforç restant o el percentatge de progrés de les tasques de resum, s'inicia el següent conjunt de càlculs:</span><span class="sxs-lookup"><span data-stu-id="e0c03-131">Regardless of whether the user re-projects by using the remaining effort or the progress percentage on the summary tasks, the following set of calculations begins:</span></span>

- <span data-ttu-id="e0c03-132">El valor de l'EAC, l'ETC i el percentatge de progrés de la tasca es calculen.</span><span class="sxs-lookup"><span data-stu-id="e0c03-132">The EAC, ETC, and progress percentage on the task are calculated.</span></span>
- <span data-ttu-id="e0c03-133">El nou EAC es distribueix cap avall a les tasques secundàries en la mateixa proporció que l'EAC original era a la tasca.</span><span class="sxs-lookup"><span data-stu-id="e0c03-133">The new EAC is distributed down to the child tasks in the same proportion as the original EAC was on the task.</span></span>
- <span data-ttu-id="e0c03-134">Es calcula l'EAC nou en cadascuna de les tasques individuals fins a les tasques de node fulla.</span><span class="sxs-lookup"><span data-stu-id="e0c03-134">The new EAC on each of the individualt tasks down to the leaf node tasks is calculated.</span></span> 
- <span data-ttu-id="e0c03-135">Es torna a calcular l'ETC i el percentatge de progrés per a les tasques secundàries afectades fins als nodes fulla en funció del valor de l'EAC.</span><span class="sxs-lookup"><span data-stu-id="e0c03-135">The affected child tasks down to the leaf nodes have their ETC and progress percentage recalculated based on the EAC value.</span></span> <span data-ttu-id="e0c03-136">Això es tradueix en una nova projecció per a la variació de l'esforç de la tasca.</span><span class="sxs-lookup"><span data-stu-id="e0c03-136">This results in a new projection for the effort variance of the task.</span></span> 
- <span data-ttu-id="e0c03-137">Els EAC de les tasques de resum es tornen a calcular fins al node arrel.</span><span class="sxs-lookup"><span data-stu-id="e0c03-137">The EACs of the summary tasks all the way to the root node are recalculated.</span></span>

### <a name="cost-tracking-view"></a><span data-ttu-id="e0c03-138">Visualització de seguiment del cost</span><span class="sxs-lookup"><span data-stu-id="e0c03-138">Cost tracking view</span></span> 

<span data-ttu-id="e0c03-139">La visualització **Seguiment del cost** compara el cost real que va comportar una tasca amb el cost previst en una tasca.</span><span class="sxs-lookup"><span data-stu-id="e0c03-139">The **Cost tracking** view compares the actual cost that was spent on a task to the planned cost on a task.</span></span> 

> [!NOTE]
> <span data-ttu-id="e0c03-140">Aquesta visualització només mostra els costos de treball i no inclou els costos de les estimacions de la despesa.</span><span class="sxs-lookup"><span data-stu-id="e0c03-140">This view shows only labor costs and doesn’t include costs from the expense estimates.</span></span> 

<span data-ttu-id="e0c03-141">El PSA utilitza les següents fórmules per calcular les mètriques de seguiment:</span><span class="sxs-lookup"><span data-stu-id="e0c03-141">PSA uses the following formulas to calculate the tracking metrics:</span></span>

- <span data-ttu-id="e0c03-142">Percentatge de cost consumit = Cost real fins al moment ÷ Cost previst per a la tasca</span><span class="sxs-lookup"><span data-stu-id="e0c03-142">Percentage of cost consumed = Actual cost spent to date ÷ Planned cost for the task</span></span>
- <span data-ttu-id="e0c03-143">Cost per completar (CTC) = Cost planificat - Cost real fins al moment</span><span class="sxs-lookup"><span data-stu-id="e0c03-143">Cost to complete (CTC) = Planned cost – Actual cost spent to date</span></span>
- <span data-ttu-id="e0c03-144">EAC = CTC + Cost real fins al moment</span><span class="sxs-lookup"><span data-stu-id="e0c03-144">EAC = CTC + Actual cost spent to date</span></span>
- <span data-ttu-id="e0c03-145">Variació de costos projectats = Cost previst – EAC</span><span class="sxs-lookup"><span data-stu-id="e0c03-145">Projected cost variance = Planned cost – EAC</span></span>

<span data-ttu-id="e0c03-146">Es mostra una projecció de la variació del cost en la tasca.</span><span class="sxs-lookup"><span data-stu-id="e0c03-146">A projection of the cost variance is shown on the task.</span></span> <span data-ttu-id="e0c03-147">Si l'EAC és més gran que el cost planificat, es preveu que la tasca costi més del que s'ha planejat originalment.</span><span class="sxs-lookup"><span data-stu-id="e0c03-147">If the EAC is more than the planned cost, the task is projected to cost more than was originally planned.</span></span> <span data-ttu-id="e0c03-148">Per tant, està per sobre del pressupost.</span><span class="sxs-lookup"><span data-stu-id="e0c03-148">Therefore, it's trending over budget.</span></span> <span data-ttu-id="e0c03-149">Si l'EAC és més petit que el cost planificat, es preveu que la tasca costi menys del que s'ha planejat originalment.</span><span class="sxs-lookup"><span data-stu-id="e0c03-149">If the EAC is less than the planned cost, the task is projected to cost less than was originally planned.</span></span> <span data-ttu-id="e0c03-150">Per tant, està per sota del pressupost.</span><span class="sxs-lookup"><span data-stu-id="e0c03-150">Therefore, it's trending under budget.</span></span>

## <a name="project-managers-re-projection-of-cost"></a><span data-ttu-id="e0c03-151">Reprojecció del cost de l'administrador de projectes</span><span class="sxs-lookup"><span data-stu-id="e0c03-151">Project manager’s re-projection of cost</span></span>

<span data-ttu-id="e0c03-152">Quan es torna a projectar l'esforç, el CTC, l'EAC, el percentatge de cost consumit i la variació de costos projectats es tornen a calcular a la visualització **Seguiment del cost**.</span><span class="sxs-lookup"><span data-stu-id="e0c03-152">When effort is re-projected, the CTC, EAC, percentage of cost consumed, and projected cost variance are all recalculated in the **Cost tracking** view.</span></span>

## <a name="project-status-summary"></a><span data-ttu-id="e0c03-153">Resum de l'estat del projecte</span><span class="sxs-lookup"><span data-stu-id="e0c03-153">Project status summary</span></span>

<span data-ttu-id="e0c03-154">El seguiment de dades a les visualitzacions **Seguiment de l'esforç** i **Seguiment del cost** mostra el progrés i el consum de costos als nivells de node arrel del projecte, tasques de resum i tasques de nodes fulla.</span><span class="sxs-lookup"><span data-stu-id="e0c03-154">Tracking data in the **Effort tracking** and **Cost tracking** views shows the progress and cost consumption at the project root node, summary tasks, and leaf node tasks levels.</span></span> <span data-ttu-id="e0c03-155">La secció **Estat** de la pàgina **Entitat del projecte** mostra un resum de l'estat a nivell del projecte.</span><span class="sxs-lookup"><span data-stu-id="e0c03-155">The **Status** section on the **Project entity** page shows a summary of project-level status.</span></span>

## <a name="status-summary-fields"></a><span data-ttu-id="e0c03-156">Camps de resum d'estat</span><span class="sxs-lookup"><span data-stu-id="e0c03-156">Status summary fields</span></span>

<span data-ttu-id="e0c03-157">El camp **Estat global del projecte** és un camp editable que mostra l'estat general del projecte.</span><span class="sxs-lookup"><span data-stu-id="e0c03-157">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="e0c03-158">Utilitza una codificació de color, com ara verd, groc i vermell, per indicar un risc cada vegada major.</span><span class="sxs-lookup"><span data-stu-id="e0c03-158">It uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> <span data-ttu-id="e0c03-159">El camp **Comentaris** permet a l'administrador del projecte introduir comentaris específics sobre l'estat.</span><span class="sxs-lookup"><span data-stu-id="e0c03-159">The **Comments** field lets the project manager enter specific comments about the status.</span></span> <span data-ttu-id="e0c03-160">El camp **Estat actualitzat el** no és editable i el valor és una marca de temps que indica quan es va actualitzar l'estat per última vegada.</span><span class="sxs-lookup"><span data-stu-id="e0c03-160">The **Status updated on** field is not editable and the value is a timestamp that indicates when the status was last updated.</span></span>

<span data-ttu-id="e0c03-161">Els camps **Rendiment de la programació** i **Rendiment del cost** es defineixen a partir de la data de seguiment.</span><span class="sxs-lookup"><span data-stu-id="e0c03-161">The **Schedule performance** and **Cost performance** fields are set from the tracking date.</span></span> <span data-ttu-id="e0c03-162">Quan la variació de planificació i costos per al node arrel de la visualització **Seguiment de l'esforç** és positiva, podeu definir aquests camps com a **Per davant**.</span><span class="sxs-lookup"><span data-stu-id="e0c03-162">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, you can set these fields to **Ahead**.</span></span> <span data-ttu-id="e0c03-163">Quan la variació de planificació i costos per al node arrel és negativa, podeu definir-los com a **Per darrere**.</span><span class="sxs-lookup"><span data-stu-id="e0c03-163">When the schedule and cost variance for the root node are negative, you can set them to **Behind**.</span></span>
