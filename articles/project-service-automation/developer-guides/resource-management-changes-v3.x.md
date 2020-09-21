---
title: Canvis a l'administració de recursos (Project Service Automation 3.x)
description: En aquest tema es proporciona informació sobre els canvis en l'àrea administració de recursos.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 03/18/2019
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 25fafd22-fe94-4865-8d4d-3e6582c999d5
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
ms.openlocfilehash: e00ce5a9604e25764567a3f9d38ec85aec4245d4
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749512"
---
# <a name="resource-management-changes-project-service-automation-3x"></a><span data-ttu-id="be45a-103">Canvis a l'administració de recursos (Project Service Automation 3.x)</span><span class="sxs-lookup"><span data-stu-id="be45a-103">Resource management changes (Project Service Automation 3.x)</span></span>

<span data-ttu-id="be45a-104">A les seccions d'aquest tema es proporciona informació sobre els canvis que s'han dut a terme a l'àrea administració de recursos de la versió 3.x del Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="be45a-104">The sections of this topic provide information about the changes that have been made to the Resource management area of Dynamics 365 Project Service Automation version 3.x.</span></span>

## <a name="project-estimates"></a><span data-ttu-id="be45a-105">Estimacions del projecte</span><span class="sxs-lookup"><span data-stu-id="be45a-105">Project estimates</span></span>

<span data-ttu-id="be45a-106">En lloc de basar-se en l'entitat **msdyn\_projecttask** (**Tasca del projecte**), les estimacions de projecte es basen en l'entitat **msdyn\_resourceassignment** (**Assignació de recursos**).</span><span class="sxs-lookup"><span data-stu-id="be45a-106">Instead of being based on the **msdyn\_projecttask** entity (**Project Task**), project estimates are based on the **msdyn\_resourceassignment** entity (**Resource Assignment**).</span></span> <span data-ttu-id="be45a-107">Les assignacions de recursos s'ha convertit en l'"origen de la veritat" per a la planificació de tasques i els preus.</span><span class="sxs-lookup"><span data-stu-id="be45a-107">Resource assignments have become the "source of truth" for task scheduling and pricing.</span></span>

## <a name="line-tasks"></a><span data-ttu-id="be45a-108">Tasques de línia</span><span class="sxs-lookup"><span data-stu-id="be45a-108">Line tasks</span></span>

<span data-ttu-id="be45a-109">Al PSA 3.x, les tasques de línia són obsoletes.</span><span class="sxs-lookup"><span data-stu-id="be45a-109">In PSA 3.x, line tasks are obsolete (deprecated).</span></span> <span data-ttu-id="be45a-110">Ara, les assignacions apunten a la tasca sencera en comptes de les tasques de línia.</span><span class="sxs-lookup"><span data-stu-id="be45a-110">Assignments now point to the whole task instead of the line tasks.</span></span>

<span data-ttu-id="be45a-111">A l'exemple següent es mostra com s'assigna una tasca que s'anomena "Tasca de prova" als membres de l'equip A i B a les versions anteriors del PSA i al PSA 3.x.</span><span class="sxs-lookup"><span data-stu-id="be45a-111">The following example shows how a task that is named "Test task" is assigned to team members A and B in earlier versions of PSA and in PSA 3.x.</span></span>

- <span data-ttu-id="be45a-112">**Abans del PSA 3.x:**</span><span class="sxs-lookup"><span data-stu-id="be45a-112">**Before PSA 3.x:**</span></span>

    - <span data-ttu-id="be45a-113">Tasca de prova</span><span class="sxs-lookup"><span data-stu-id="be45a-113">Test task</span></span>

        - <span data-ttu-id="be45a-114">Tasca de prova: tasca de línia 1</span><span class="sxs-lookup"><span data-stu-id="be45a-114">Test task – Line task 1</span></span>

            - <span data-ttu-id="be45a-115">Assignació a A</span><span class="sxs-lookup"><span data-stu-id="be45a-115">Assignment to A</span></span>

        - <span data-ttu-id="be45a-116">Tasca de prova: tasca de línia 2</span><span class="sxs-lookup"><span data-stu-id="be45a-116">Test task – Line task 2</span></span>

            - <span data-ttu-id="be45a-117">Assignació a B</span><span class="sxs-lookup"><span data-stu-id="be45a-117">Assignment to B</span></span>

- <span data-ttu-id="be45a-118">**PSA 3.x:**</span><span class="sxs-lookup"><span data-stu-id="be45a-118">**PSA 3.x:**</span></span>

    - <span data-ttu-id="be45a-119">Tasca de prova</span><span class="sxs-lookup"><span data-stu-id="be45a-119">Test task</span></span>

        - <span data-ttu-id="be45a-120">Assignació a A</span><span class="sxs-lookup"><span data-stu-id="be45a-120">Assignment to A</span></span>
        - <span data-ttu-id="be45a-121">Assignació a B</span><span class="sxs-lookup"><span data-stu-id="be45a-121">Assignment to B</span></span>

## <a name="unassigned-assignment"></a><span data-ttu-id="be45a-122">Assignació no assignada</span><span class="sxs-lookup"><span data-stu-id="be45a-122">Unassigned assignment</span></span>

<span data-ttu-id="be45a-123">Al PSA 3.x, una assignació no assignada és una assignació assignada a un membre de l'equip **NUL** i a un recurs **NUL**.</span><span class="sxs-lookup"><span data-stu-id="be45a-123">In PSA 3.x, an unassigned assignment is an assignment that is assigned to a **NULL** team member and a **NULL** resource.</span></span> <span data-ttu-id="be45a-124">Les assignacions no assignades poden produir-se en alguns escenaris:</span><span class="sxs-lookup"><span data-stu-id="be45a-124">Unassigned assignments can occur in a couple of scenarios:</span></span>

- <span data-ttu-id="be45a-125">Si s'ha creat una tasca, però encara no s'ha assignat a cap membre de l'equip, sempre es crea una assignació no assignada.</span><span class="sxs-lookup"><span data-stu-id="be45a-125">If a task has been created, but it hasn't yet been assigned to any team member, an unassigned assignment is always created.</span></span> 
- <span data-ttu-id="be45a-126">Si se suprimeixen tots els assignats d'una tasca, una assignació no assignada es torna a crear per a aquesta tasca.</span><span class="sxs-lookup"><span data-stu-id="be45a-126">If all assignees on a task are removed, an unassigned assignment is re-created for that task.</span></span>

## <a name="scheduling-fields-on-the-project-task-entity"></a><span data-ttu-id="be45a-127">Planificar camps a l'entitat Tasca del projecte</span><span class="sxs-lookup"><span data-stu-id="be45a-127">Scheduling fields on the Project Task entity</span></span>

<span data-ttu-id="be45a-128">Els camps de l'entitat **msdyn\_projecttask** s'han deixat d'utilitzar o s'han mogut a l'entitat **msdyn\_resourceassignment**, o ara s'hi fa referència des de l'entitat **msdyn\_projectteam** (**Membre de l'equip del projecte**).</span><span class="sxs-lookup"><span data-stu-id="be45a-128">The fields on the **msdyn\_projecttask** entity have been deprecated or moved to the **msdyn\_resourceassignment** entity, or they are now referenced from the **msdyn\_projectteam** entity (**Project Team Member**).</span></span>

| <span data-ttu-id="be45a-129">Camp obsolet a msdyn\_projecttask (Tasca del projecte)</span><span class="sxs-lookup"><span data-stu-id="be45a-129">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="be45a-130">Camp nou a msdyn\_resourceassignment (Assignació de recursos)</span><span class="sxs-lookup"><span data-stu-id="be45a-130">New field on msdyn\_resourceassignment (Resource Assignment)</span></span> | <span data-ttu-id="be45a-131">Comentari</span><span class="sxs-lookup"><span data-stu-id="be45a-131">Comment</span></span> |
|---|---|---|
| <span data-ttu-id="be45a-132">msdyn\_assignedresources</span><span class="sxs-lookup"><span data-stu-id="be45a-132">msdyn\_assignedresources</span></span> | <span data-ttu-id="be45a-133">cap</span><span class="sxs-lookup"><span data-stu-id="be45a-133">None</span></span> | |
| <span data-ttu-id="be45a-134">msdyn\_assignedteammembers</span><span class="sxs-lookup"><span data-stu-id="be45a-134">msdyn\_assignedteammembers</span></span> | <span data-ttu-id="be45a-135">cap</span><span class="sxs-lookup"><span data-stu-id="be45a-135">None</span></span> | |
| <span data-ttu-id="be45a-136">msdyn\_numberofresources</span><span class="sxs-lookup"><span data-stu-id="be45a-136">msdyn\_numberofresources</span></span> | <span data-ttu-id="be45a-137">cap</span><span class="sxs-lookup"><span data-stu-id="be45a-137">None</span></span> | |
| <span data-ttu-id="be45a-138">msdyn\_scheduledhours</span><span class="sxs-lookup"><span data-stu-id="be45a-138">msdyn\_scheduledhours</span></span> | <span data-ttu-id="be45a-139">cap</span><span class="sxs-lookup"><span data-stu-id="be45a-139">None</span></span> | |
| <span data-ttu-id="be45a-140">msdyn\_effortcontour</span><span class="sxs-lookup"><span data-stu-id="be45a-140">msdyn\_effortcontour</span></span> | <span data-ttu-id="be45a-141">msdyn\_plannedwork</span><span class="sxs-lookup"><span data-stu-id="be45a-141">msdyn\_plannedwork</span></span> | <span data-ttu-id="be45a-142">El format de l'estructura de dades JavaScript Object Notation (JSON) que s'emmagatzema al camp ha canviat.</span><span class="sxs-lookup"><span data-stu-id="be45a-142">The format of the JavaScript Object Notation (JSON) data structure that is stored in the field has been changed.</span></span> |

## <a name="schedule-contour"></a><span data-ttu-id="be45a-143">Contorn de planificació</span><span class="sxs-lookup"><span data-stu-id="be45a-143">Schedule contour</span></span>

<span data-ttu-id="be45a-144">El contorn de la planificació s'emmagatzema al camp **Treball planificat** (**msdyn\_plannedwork**) de cada entitat **Assignació de recursos** (**msdyn\_resourceassignment**).</span><span class="sxs-lookup"><span data-stu-id="be45a-144">The schedule contour is stored in the **Planned Work** field (**msdyn\_plannedwork**) of each **Resource Assignment** entity (**msdyn\_resourceassignment**).</span></span>

### <a name="structure"></a><span data-ttu-id="be45a-145">Estructura</span><span class="sxs-lookup"><span data-stu-id="be45a-145">Structure</span></span>

<span data-ttu-id="be45a-146">La nova estructura del contorn de la planificació consta de porcions de temps flexibles que es defineixen per a cada dia de la planificació.</span><span class="sxs-lookup"><span data-stu-id="be45a-146">The new structure of the schedule contour consists of flexible time slices that are defined for each day of the schedule.</span></span> <span data-ttu-id="be45a-147">Cada porció de temps té les següents propietats:</span><span class="sxs-lookup"><span data-stu-id="be45a-147">Each time slice has the following properties:</span></span>

- <span data-ttu-id="be45a-148">**Inici**: l'inici de les hores de treball per al dia, segons el calendari del projecte.</span><span class="sxs-lookup"><span data-stu-id="be45a-148">**Start** – The start of the working hours for the day, according to the project calendar.</span></span>
- <span data-ttu-id="be45a-149">**Acabament**: l'acabament de les hores de treball per al dia, segons el calendari del projecte.</span><span class="sxs-lookup"><span data-stu-id="be45a-149">**End** – The end of the working hours for the day, according to the project calendar.</span></span>
- <span data-ttu-id="be45a-150">**Hores**: el nombre d'hores que s'assignen al dia.</span><span class="sxs-lookup"><span data-stu-id="be45a-150">**Hours** – The number of hours that are assigned on the day.</span></span>

<span data-ttu-id="be45a-151">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="be45a-151">**Example**</span></span>

<span data-ttu-id="be45a-152">Aquest exemple utilitza un calendari de projecte on la jornada laboral és de 9 a 5 hores a la zona horària UTC-8.</span><span class="sxs-lookup"><span data-stu-id="be45a-152">This example uses a project calendar where the workday is from 9 AM to 5 PM in the UTC-8 time zone.</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

### <a name="auto-scheduling-and-manual-scheduling"></a><span data-ttu-id="be45a-153">Planificació automàtica i programació manual</span><span class="sxs-lookup"><span data-stu-id="be45a-153">Auto-scheduling and manual scheduling</span></span>

<span data-ttu-id="be45a-154">Si una tasca es planifica automàticament, les hores es carreguen de forma frontal i la duració de la tasca es pot reduir.</span><span class="sxs-lookup"><span data-stu-id="be45a-154">If a task is auto-scheduled, the hours are front-loaded, and the task duration might be reduced.</span></span>

<span data-ttu-id="be45a-155">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="be45a-155">**Example**</span></span>

<span data-ttu-id="be45a-156">La tasca següent es planifica automàticament per a 18 hores durant tres dies (del 3 de desembre de 2018 al 5 de desembre de 2018).</span><span class="sxs-lookup"><span data-stu-id="be45a-156">The following task is auto-scheduled for 18 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

<span data-ttu-id="be45a-157">Si es planifica manualment una tasca, les hores es distribueixen de manera uniforme a totes les dates.</span><span class="sxs-lookup"><span data-stu-id="be45a-157">If a task is manually scheduled, the hours are evenly distributed to all the dates.</span></span>

<span data-ttu-id="be45a-158">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="be45a-158">**Example**</span></span>

<span data-ttu-id="be45a-159">La tasca següent es planifica manualment per a 18 hores durant tres dies (del 3 de desembre de 2018 al 5 de desembre de 2018).</span><span class="sxs-lookup"><span data-stu-id="be45a-159">The following task is manually scheduled for 18 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":6},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":6},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":6}]
```

### <a name="assignment-unit"></a><span data-ttu-id="be45a-160">Unitat d'assignació</span><span class="sxs-lookup"><span data-stu-id="be45a-160">Assignment unit</span></span>

<span data-ttu-id="be45a-161">La unitat d'assignació ha quedat obsoleta al PSA 3.x.</span><span class="sxs-lookup"><span data-stu-id="be45a-161">The assignment unit has been deprecated in PSA 3.x.</span></span> <span data-ttu-id="be45a-162">Les hores d'esforç de tasca ara es divideixen equitativament, per dia, entre tots els recursos assignats.</span><span class="sxs-lookup"><span data-stu-id="be45a-162">The task effort hours are now equally divided, per day, among all the assigned resources.</span></span>

<span data-ttu-id="be45a-163">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="be45a-163">**Example**</span></span>

<span data-ttu-id="be45a-164">En aquest exemple, la tasca s'assigna a dos recursos i es planifica automàticament per a 36 hores al llarg de tres dies (del 3 de desembre, 2018 al 5 de desembre de 2018).</span><span class="sxs-lookup"><span data-stu-id="be45a-164">In this example, the task is is assigned to two resources and is auto-scheduled for 36 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

- <span data-ttu-id="be45a-165">Assignació 1:</span><span class="sxs-lookup"><span data-stu-id="be45a-165">Assignment 1:</span></span>

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

- <span data-ttu-id="be45a-166">Assignació 2:</span><span class="sxs-lookup"><span data-stu-id="be45a-166">Assignment 2:</span></span>

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

## <a name="pricing-dimensions"></a><span data-ttu-id="be45a-167">Dimensions de preus</span><span class="sxs-lookup"><span data-stu-id="be45a-167">Pricing dimensions</span></span>

<span data-ttu-id="be45a-168">Al PSA 3.x, els camps de dimensió de preus específics de recursos (com ara **Funció** i **Unitat organitzativa**) s'han suprimit de l'entitat **msdyn\_projecttask**.</span><span class="sxs-lookup"><span data-stu-id="be45a-168">In PSA 3.x, resource-specific pricing dimension fields (such as **Role** and **Organizational Unit**) have been removed from the **msdyn\_projecttask** entity.</span></span> <span data-ttu-id="be45a-169">Ara, aquests camps es poden recuperar del membre de l'equip corresponent (**msdyn\_projectteam**) de l'assignació de recursos (**msdyn\_resourceassignment**) en el moment de generar estimacions del projecte.</span><span class="sxs-lookup"><span data-stu-id="be45a-169">These fields can now be retrieved from the corresponding project team member (**msdyn\_projectteam**) of the resource assignment (**msdyn\_resourceassignment**) when project estimates are generated.</span></span> <span data-ttu-id="be45a-170">S'ha afegit un nou camp, **msdyn\_organizationalunit** a l'entitat **msdyn\_projectteam**.</span><span class="sxs-lookup"><span data-stu-id="be45a-170">A new field, **msdyn\_organizationalunit**, has been added to the **msdyn\_projectteam** entity.</span></span>

| <span data-ttu-id="be45a-171">Camp obsolet a msdyn\_projecttask (Tasca del projecte)</span><span class="sxs-lookup"><span data-stu-id="be45a-171">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="be45a-172">Camp de msdyn\_projectteam (Membre de l'equip del projecte) que s'utilitza en comptes d'això</span><span class="sxs-lookup"><span data-stu-id="be45a-172">Field from msdyn\_projectteam (Project Team Member) that is used instead</span></span> |
|---|---|
| <span data-ttu-id="be45a-173">msdyn\_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="be45a-173">msdyn\_resourcecategory</span></span> | <span data-ttu-id="be45a-174">msdyn\_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="be45a-174">msdyn\_resourcecategory</span></span> |
| <span data-ttu-id="be45a-175">msdyn\_organizationalunit</span><span class="sxs-lookup"><span data-stu-id="be45a-175">msdyn\_organizationalunit</span></span> | <span data-ttu-id="be45a-176">msdyn\_organizationalunit</span><span class="sxs-lookup"><span data-stu-id="be45a-176">msdyn\_organizationalunit</span></span> |

## <a name="contours"></a><span data-ttu-id="be45a-177">Contorns</span><span class="sxs-lookup"><span data-stu-id="be45a-177">Contours</span></span>

<span data-ttu-id="be45a-178">Els camps de preus i estimació de contorn s'ha deixat d'utilitzar a l'entitat **msdyn\_projecttask**.</span><span class="sxs-lookup"><span data-stu-id="be45a-178">The pricing and estimation contour fields have been deprecated on the **msdyn\_projecttask** entity.</span></span> <span data-ttu-id="be45a-179">S'han desplaçat a l'entitat **msdyn\_resourceassignment**.</span><span class="sxs-lookup"><span data-stu-id="be45a-179">They have been moved to the **msdyn\_resourceassignment** entity.</span></span>

| <span data-ttu-id="be45a-180">Camp obsolet a msdyn\_projecttask (Tasca del projecte)</span><span class="sxs-lookup"><span data-stu-id="be45a-180">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="be45a-181">Camp nou a msdyn\_resourceassignment (Assignació de recursos)</span><span class="sxs-lookup"><span data-stu-id="be45a-181">New field on msdyn\_resourceassignment (Resource Assignment)</span></span> |
|---|---|
| <span data-ttu-id="be45a-182">msdyn\_costestimatecontour</span><span class="sxs-lookup"><span data-stu-id="be45a-182">msdyn\_costestimatecontour</span></span> | <span data-ttu-id="be45a-183">msdyn\_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="be45a-183">msdyn\_plannedcostcontour</span></span> |
| <span data-ttu-id="be45a-184">msdyn\_salesestimatecontour</span><span class="sxs-lookup"><span data-stu-id="be45a-184">msdyn\_salesestimatecontour</span></span> | <span data-ttu-id="be45a-185">msdyn\_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="be45a-185">msdyn\_plannedsalescontour</span></span> |

<span data-ttu-id="be45a-186">Els camps següents s'han desplaçat a l'entitat **msdyn\_resourceassignment**:</span><span class="sxs-lookup"><span data-stu-id="be45a-186">The following fields have been added to the **msdyn\_resourceassignment** entity:</span></span>

* <span data-ttu-id="be45a-187">msdyn\_plannedcost</span><span class="sxs-lookup"><span data-stu-id="be45a-187">msdyn\_plannedcost</span></span>
* <span data-ttu-id="be45a-188">msdyn\_plannedsales</span><span class="sxs-lookup"><span data-stu-id="be45a-188">msdyn\_plannedsales</span></span>

<span data-ttu-id="be45a-189">Els camps següents per al cost i les vendes previstos, reals i restants no es modifiquen a l'entitat **msdyn\_projecttask**:</span><span class="sxs-lookup"><span data-stu-id="be45a-189">The following fields for planned, actual, and remaining cost and sales are unchanged on the **msdyn\_projecttask** entity:</span></span>

* <span data-ttu-id="be45a-190">msdyn\_plannedcost</span><span class="sxs-lookup"><span data-stu-id="be45a-190">msdyn\_plannedcost</span></span>
* <span data-ttu-id="be45a-191">msdyn\_plannedsales</span><span class="sxs-lookup"><span data-stu-id="be45a-191">msdyn\_plannedsales</span></span>
* <span data-ttu-id="be45a-192">msdyn\_actualcost</span><span class="sxs-lookup"><span data-stu-id="be45a-192">msdyn\_actualcost</span></span>
* <span data-ttu-id="be45a-193">msdyn\_actualsales</span><span class="sxs-lookup"><span data-stu-id="be45a-193">msdyn\_actualsales</span></span>
* <span data-ttu-id="be45a-194">msdyn\_remainingcost</span><span class="sxs-lookup"><span data-stu-id="be45a-194">msdyn\_remainingcost</span></span>
* <span data-ttu-id="be45a-195">msdyn\_remainingsales</span><span class="sxs-lookup"><span data-stu-id="be45a-195">msdyn\_remainingsales</span></span>
