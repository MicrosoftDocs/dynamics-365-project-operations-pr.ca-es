---
title: Ús de les API de planificació per realitzar operacions amb entitats de Planificació
description: En aquest tema es proporciona informació i exemples per utilitzar les API de Planificació.
author: sigitac
ms.date: 04/27/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4a032dc7bcbdf23fce3c3b2ca63c51d473bd8e26
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116785"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="87048-103">Ús de les API de planificació per realitzar operacions amb entitats de Planificació</span><span class="sxs-lookup"><span data-stu-id="87048-103">Use Schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="87048-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_</span><span class="sxs-lookup"><span data-stu-id="87048-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="87048-105">Algunes de les funcionalitats que s'indiquen en aquest tema estan disponibles com a part d'una versió preliminar.</span><span class="sxs-lookup"><span data-stu-id="87048-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="87048-106">El contingut i la funcionalitat estan subjectes a canvis.</span><span class="sxs-lookup"><span data-stu-id="87048-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="87048-107">Entitats de planificació</span><span class="sxs-lookup"><span data-stu-id="87048-107">Scheduling entities</span></span>

<span data-ttu-id="87048-108">Les API de Planificació proporcionen la capacitat de crear, actualitzar i suprimir operacions amb **Entitats de planificació**.</span><span class="sxs-lookup"><span data-stu-id="87048-108">Schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="87048-109">Aquestes entitats s'administren mitjançant el motor de Planificació del Projecte for the web.</span><span class="sxs-lookup"><span data-stu-id="87048-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="87048-110">Les operacions de creació, actualització i supressió amb **Entitats de planificació** es van restringir a les versions anteriors del Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="87048-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="87048-111">La taula següent proporciona una llista completa de les **Entitats de planificació**.</span><span class="sxs-lookup"><span data-stu-id="87048-111">The following table provides a full list of the **Scheduling entities**.</span></span>

| <span data-ttu-id="87048-112">Nom de l’entitat</span><span class="sxs-lookup"><span data-stu-id="87048-112">Entity name</span></span>  | <span data-ttu-id="87048-113">Nom lògic de l’entitat</span><span class="sxs-lookup"><span data-stu-id="87048-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="87048-114">Project</span><span class="sxs-lookup"><span data-stu-id="87048-114">Project</span></span> | <span data-ttu-id="87048-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="87048-115">msdyn_project</span></span> |
| <span data-ttu-id="87048-116">Tasca del projecte</span><span class="sxs-lookup"><span data-stu-id="87048-116">Project Task</span></span>  | <span data-ttu-id="87048-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="87048-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="87048-118">Dependència de les tasques del projecte</span><span class="sxs-lookup"><span data-stu-id="87048-118">Project Task Dependency</span></span>  | <span data-ttu-id="87048-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="87048-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="87048-120">Assignació de recursos</span><span class="sxs-lookup"><span data-stu-id="87048-120">Resource Assignment</span></span> | <span data-ttu-id="87048-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="87048-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="87048-122">Dipòsit de projecte</span><span class="sxs-lookup"><span data-stu-id="87048-122">Project Bucket</span></span>  | <span data-ttu-id="87048-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="87048-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="87048-124">Membre de l'equip del projecte</span><span class="sxs-lookup"><span data-stu-id="87048-124">Project Team Member</span></span> | <span data-ttu-id="87048-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="87048-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="87048-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="87048-126">OperationSet</span></span>

<span data-ttu-id="87048-127">OperationSet és un patró d'unitat de treball que es pot utilitzar quan diverses sol·licituds que afecten la planificació s'han de processar dins d'una transacció.</span><span class="sxs-lookup"><span data-stu-id="87048-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="schedule-apis"></a><span data-ttu-id="87048-128">API de Planificació</span><span class="sxs-lookup"><span data-stu-id="87048-128">Schedule APIs</span></span>

<span data-ttu-id="87048-129">A continuació es mostra una llista de les API de Planificació actuals.</span><span class="sxs-lookup"><span data-stu-id="87048-129">The following is a list of current Schedule APIs.</span></span>

- <span data-ttu-id="87048-130">**msdyn_CreateProjectV1**: aquesta API es pot utilitzar per crear un projecte.</span><span class="sxs-lookup"><span data-stu-id="87048-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="87048-131">El projecte i el dipòsit per defecte del projecte es creen immediatament.</span><span class="sxs-lookup"><span data-stu-id="87048-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="87048-132">**msdyn_CreateTeamMemberV1**: aquesta API es pot utilitzar per crear un membre de l'equip del projecte.</span><span class="sxs-lookup"><span data-stu-id="87048-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="87048-133">El registre del membre de l'equip es crea immediatament.</span><span class="sxs-lookup"><span data-stu-id="87048-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="87048-134">**msdyn_CreateOperationSetV1**: aquesta API es pot utilitzar per planificar diverses sol·licituds que s'han de fer dins d'una transacció.</span><span class="sxs-lookup"><span data-stu-id="87048-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="87048-135">**msdyn_PSSCreateV1**: aquesta API es pot utilitzar per crear una entitat.</span><span class="sxs-lookup"><span data-stu-id="87048-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="87048-136">L'entitat pot ser qualsevol de les entitats de Planificació que admeten l'operació de creació.</span><span class="sxs-lookup"><span data-stu-id="87048-136">The entity can be any of the Scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="87048-137">**msdyn_PSSUpdateV1**: aquesta API es pot utilitzar per actualitzar una entitat.</span><span class="sxs-lookup"><span data-stu-id="87048-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="87048-138">L'entitat pot ser qualsevol de les entitats de Planificació que admeten l'operació d'actualització.</span><span class="sxs-lookup"><span data-stu-id="87048-138">The entity can be any of the Scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="87048-139">**msdyn_PSSDeleteV1**: aquesta API es pot utilitzar per suprimir una entitat.</span><span class="sxs-lookup"><span data-stu-id="87048-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="87048-140">L'entitat pot ser qualsevol de les entitats de Planificació que admeten l'operació de supressió.</span><span class="sxs-lookup"><span data-stu-id="87048-140">The entity can be any of the Scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="87048-141">**msdyn_ExecuteOperationSetV1**: aquesta API s'utilitza per executar totes les operacions dins del conjunt d'operacions determinat.</span><span class="sxs-lookup"><span data-stu-id="87048-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-schedule-apis-with-operationset"></a><span data-ttu-id="87048-142">Ús de les API de Planificació amb OperationSet</span><span class="sxs-lookup"><span data-stu-id="87048-142">Using Schedule APIs with OperationSet</span></span>

<span data-ttu-id="87048-143">Com que els registres amb **CreateProjectV1** i **CreateTeamMemberV1** es creen immediatament, aquestes API no es poden utilitzar directament a **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="87048-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="87048-144">Tanmateix, podeu utilitzar l'API per crear els registres necessaris, crear un **OperationSet** i, a continuació, utilitzar aquests registres creats a **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="87048-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="87048-145">Operacions admeses</span><span class="sxs-lookup"><span data-stu-id="87048-145">Supported operations</span></span>

| <span data-ttu-id="87048-146">Entitat de planificació</span><span class="sxs-lookup"><span data-stu-id="87048-146">Scheduling entity</span></span> | <span data-ttu-id="87048-147">Creació</span><span class="sxs-lookup"><span data-stu-id="87048-147">Create</span></span> | <span data-ttu-id="87048-148">Actualització</span><span class="sxs-lookup"><span data-stu-id="87048-148">Update</span></span> | <span data-ttu-id="87048-149">Delete</span><span class="sxs-lookup"><span data-stu-id="87048-149">Delete</span></span> | <span data-ttu-id="87048-150">Consideracions importants</span><span class="sxs-lookup"><span data-stu-id="87048-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="87048-151">Tasca del projecte</span><span class="sxs-lookup"><span data-stu-id="87048-151">Project task</span></span> | <span data-ttu-id="87048-152">Sí</span><span class="sxs-lookup"><span data-stu-id="87048-152">Yes</span></span> | <span data-ttu-id="87048-153">Sí</span><span class="sxs-lookup"><span data-stu-id="87048-153">Yes</span></span> | <span data-ttu-id="87048-154">Sí</span><span class="sxs-lookup"><span data-stu-id="87048-154">Yes</span></span> | <span data-ttu-id="87048-155">Cap</span><span class="sxs-lookup"><span data-stu-id="87048-155">None</span></span> |
| <span data-ttu-id="87048-156">Dependència de les tasques del projecte</span><span class="sxs-lookup"><span data-stu-id="87048-156">Project task dependency</span></span> | <span data-ttu-id="87048-157">Sí</span><span class="sxs-lookup"><span data-stu-id="87048-157">Yes</span></span> | <span data-ttu-id="87048-158">Sí</span><span class="sxs-lookup"><span data-stu-id="87048-158">Yes</span></span> | | <span data-ttu-id="87048-159">Els registres de dependència de les tasques del projecte no s'actualitzen.</span><span class="sxs-lookup"><span data-stu-id="87048-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="87048-160">En lloc d'això, es pot suprimir un registre antic i crear-ne un de nou.</span><span class="sxs-lookup"><span data-stu-id="87048-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="87048-161">Assignació de recursos</span><span class="sxs-lookup"><span data-stu-id="87048-161">Resource assignment</span></span> | <span data-ttu-id="87048-162">Sí</span><span class="sxs-lookup"><span data-stu-id="87048-162">Yes</span></span> | <span data-ttu-id="87048-163">Sí</span><span class="sxs-lookup"><span data-stu-id="87048-163">Yes</span></span> | | <span data-ttu-id="87048-164">No s'admeten les operacions amb els camps següents: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** i **PlannedWork**.</span><span class="sxs-lookup"><span data-stu-id="87048-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="87048-165">Els registres d'assignació de recursos no s'actualitzen.</span><span class="sxs-lookup"><span data-stu-id="87048-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="87048-166">En lloc d'això, es pot suprimir el registre antic i crear-ne un de nou.</span><span class="sxs-lookup"><span data-stu-id="87048-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="87048-167">Dipòsit de projecte</span><span class="sxs-lookup"><span data-stu-id="87048-167">Project bucket</span></span> | <span data-ttu-id="87048-168">N/D</span><span class="sxs-lookup"><span data-stu-id="87048-168">N/A</span></span> | <span data-ttu-id="87048-169">N/D</span><span class="sxs-lookup"><span data-stu-id="87048-169">N/A</span></span> | <span data-ttu-id="87048-170">N/D</span><span class="sxs-lookup"><span data-stu-id="87048-170">N/A</span></span> | <span data-ttu-id="87048-171">El dipòsit per defecte es crea amb l'API **CreateProjectV1**.</span><span class="sxs-lookup"><span data-stu-id="87048-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="87048-172">Membre de l'equip del projecte</span><span class="sxs-lookup"><span data-stu-id="87048-172">Project team member</span></span> | <span data-ttu-id="87048-173">Sí</span><span class="sxs-lookup"><span data-stu-id="87048-173">Yes</span></span> | <span data-ttu-id="87048-174">Sí</span><span class="sxs-lookup"><span data-stu-id="87048-174">Yes</span></span> | <span data-ttu-id="87048-175">Sí</span><span class="sxs-lookup"><span data-stu-id="87048-175">Yes</span></span> | <span data-ttu-id="87048-176">Per a l'operació de creació, utilitzeu l'API **CreateTeamMemberV1**.</span><span class="sxs-lookup"><span data-stu-id="87048-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="87048-177">Project</span><span class="sxs-lookup"><span data-stu-id="87048-177">Project</span></span> | <span data-ttu-id="87048-178">Sí</span><span class="sxs-lookup"><span data-stu-id="87048-178">Yes</span></span> | <span data-ttu-id="87048-179">Sí</span><span class="sxs-lookup"><span data-stu-id="87048-179">Yes</span></span> | <span data-ttu-id="87048-180">N/D</span><span class="sxs-lookup"><span data-stu-id="87048-180">N/A</span></span> | <span data-ttu-id="87048-181">Les operacions amb els camps següents no estan admeses: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** i **Duration**.</span><span class="sxs-lookup"><span data-stu-id="87048-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="87048-182">Aquestes API es poden cridar amb objectes d'entitat que inclouen camps personalitzats.</span><span class="sxs-lookup"><span data-stu-id="87048-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="87048-183">La propietat ID és opcional.</span><span class="sxs-lookup"><span data-stu-id="87048-183">The ID property is optional.</span></span> <span data-ttu-id="87048-184">Si es proporciona, el sistema intenta utilitzar-la i llança una excepció si no es pot utilitzar.</span><span class="sxs-lookup"><span data-stu-id="87048-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="87048-185">Si no es proporciona, el sistema la generarà.</span><span class="sxs-lookup"><span data-stu-id="87048-185">If it isn't provided, the system will generate it.</span></span>

## <a name="restricted-fields"></a><span data-ttu-id="87048-186">Camps restringits</span><span class="sxs-lookup"><span data-stu-id="87048-186">Restricted fields</span></span>

<span data-ttu-id="87048-187">Les taules següents defineixen els camps restringits de **Crear** i **Editar.**</span><span class="sxs-lookup"><span data-stu-id="87048-187">The following tables define the fields that are restricted from **Create** and **Edit.**</span></span>

### <a name="project-task"></a><span data-ttu-id="87048-188">Tasca del projecte</span><span class="sxs-lookup"><span data-stu-id="87048-188">Project task</span></span>

| <span data-ttu-id="87048-189">**Nom lògic**</span><span class="sxs-lookup"><span data-stu-id="87048-189">**Logical name**</span></span>                       | <span data-ttu-id="87048-190">**Pot crear**</span><span class="sxs-lookup"><span data-stu-id="87048-190">**Can create**</span></span> | <span data-ttu-id="87048-191">**Pot editar**</span><span class="sxs-lookup"><span data-stu-id="87048-191">**Can edit**</span></span>     |
|----------------------------------------|----------------|------------------|
| <span data-ttu-id="87048-192">msdyn_actualcost</span><span class="sxs-lookup"><span data-stu-id="87048-192">msdyn_actualcost</span></span>                       | <span data-ttu-id="87048-193">no</span><span class="sxs-lookup"><span data-stu-id="87048-193">no</span></span>             | <span data-ttu-id="87048-194">no</span><span class="sxs-lookup"><span data-stu-id="87048-194">no</span></span>               |
| <span data-ttu-id="87048-195">msdyn_actualcost_base</span><span class="sxs-lookup"><span data-stu-id="87048-195">msdyn_actualcost_base</span></span>                  | <span data-ttu-id="87048-196">no</span><span class="sxs-lookup"><span data-stu-id="87048-196">no</span></span>             | <span data-ttu-id="87048-197">no</span><span class="sxs-lookup"><span data-stu-id="87048-197">no</span></span>               |
| <span data-ttu-id="87048-198">msdyn_actualend</span><span class="sxs-lookup"><span data-stu-id="87048-198">msdyn_actualend</span></span>                        | <span data-ttu-id="87048-199">no</span><span class="sxs-lookup"><span data-stu-id="87048-199">no</span></span>             | <span data-ttu-id="87048-200">no</span><span class="sxs-lookup"><span data-stu-id="87048-200">no</span></span>               |
| <span data-ttu-id="87048-201">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="87048-201">msdyn_actualsales</span></span>                      | <span data-ttu-id="87048-202">no</span><span class="sxs-lookup"><span data-stu-id="87048-202">no</span></span>             | <span data-ttu-id="87048-203">no</span><span class="sxs-lookup"><span data-stu-id="87048-203">no</span></span>               |
| <span data-ttu-id="87048-204">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="87048-204">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="87048-205">no</span><span class="sxs-lookup"><span data-stu-id="87048-205">no</span></span>             | <span data-ttu-id="87048-206">no</span><span class="sxs-lookup"><span data-stu-id="87048-206">no</span></span>               |
| <span data-ttu-id="87048-207">msdyn_actualstart</span><span class="sxs-lookup"><span data-stu-id="87048-207">msdyn_actualstart</span></span>                      | <span data-ttu-id="87048-208">no</span><span class="sxs-lookup"><span data-stu-id="87048-208">no</span></span>             | <span data-ttu-id="87048-209">no</span><span class="sxs-lookup"><span data-stu-id="87048-209">no</span></span>               |
| <span data-ttu-id="87048-210">msdyn_costatcompleteestimate</span><span class="sxs-lookup"><span data-stu-id="87048-210">msdyn_costatcompleteestimate</span></span>           | <span data-ttu-id="87048-211">no</span><span class="sxs-lookup"><span data-stu-id="87048-211">no</span></span>             | <span data-ttu-id="87048-212">no</span><span class="sxs-lookup"><span data-stu-id="87048-212">no</span></span>               |
| <span data-ttu-id="87048-213">msdyn_costatcompleteestimate_base</span><span class="sxs-lookup"><span data-stu-id="87048-213">msdyn_costatcompleteestimate_base</span></span>      | <span data-ttu-id="87048-214">no</span><span class="sxs-lookup"><span data-stu-id="87048-214">no</span></span>             | <span data-ttu-id="87048-215">no</span><span class="sxs-lookup"><span data-stu-id="87048-215">no</span></span>               |
| <span data-ttu-id="87048-216">msdyn_costconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="87048-216">msdyn_costconsumptionpercentage</span></span>        | <span data-ttu-id="87048-217">no</span><span class="sxs-lookup"><span data-stu-id="87048-217">no</span></span>             | <span data-ttu-id="87048-218">no</span><span class="sxs-lookup"><span data-stu-id="87048-218">no</span></span>               |
| <span data-ttu-id="87048-219">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="87048-219">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="87048-220">no</span><span class="sxs-lookup"><span data-stu-id="87048-220">no</span></span>             | <span data-ttu-id="87048-221">no</span><span class="sxs-lookup"><span data-stu-id="87048-221">no</span></span>               |
| <span data-ttu-id="87048-222">msdyn_effortestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="87048-222">msdyn_effortestimateatcomplete</span></span>         | <span data-ttu-id="87048-223">no</span><span class="sxs-lookup"><span data-stu-id="87048-223">no</span></span>             | <span data-ttu-id="87048-224">no</span><span class="sxs-lookup"><span data-stu-id="87048-224">no</span></span>               |
| <span data-ttu-id="87048-225">msdyn_iscritical</span><span class="sxs-lookup"><span data-stu-id="87048-225">msdyn_iscritical</span></span>                       | <span data-ttu-id="87048-226">no</span><span class="sxs-lookup"><span data-stu-id="87048-226">no</span></span>             | <span data-ttu-id="87048-227">no</span><span class="sxs-lookup"><span data-stu-id="87048-227">no</span></span>               |
| <span data-ttu-id="87048-228">msdyn_iscriticalname</span><span class="sxs-lookup"><span data-stu-id="87048-228">msdyn_iscriticalname</span></span>                   | <span data-ttu-id="87048-229">no</span><span class="sxs-lookup"><span data-stu-id="87048-229">no</span></span>             | <span data-ttu-id="87048-230">no</span><span class="sxs-lookup"><span data-stu-id="87048-230">no</span></span>               |
| <span data-ttu-id="87048-231">msdyn_ismanual</span><span class="sxs-lookup"><span data-stu-id="87048-231">msdyn_ismanual</span></span>                         | <span data-ttu-id="87048-232">no</span><span class="sxs-lookup"><span data-stu-id="87048-232">no</span></span>             | <span data-ttu-id="87048-233">no</span><span class="sxs-lookup"><span data-stu-id="87048-233">no</span></span>               |
| <span data-ttu-id="87048-234">msdyn_ismanualname</span><span class="sxs-lookup"><span data-stu-id="87048-234">msdyn_ismanualname</span></span>                     | <span data-ttu-id="87048-235">no</span><span class="sxs-lookup"><span data-stu-id="87048-235">no</span></span>             | <span data-ttu-id="87048-236">no</span><span class="sxs-lookup"><span data-stu-id="87048-236">no</span></span>               |
| <span data-ttu-id="87048-237">msdyn_ismilestone</span><span class="sxs-lookup"><span data-stu-id="87048-237">msdyn_ismilestone</span></span>                      | <span data-ttu-id="87048-238">no</span><span class="sxs-lookup"><span data-stu-id="87048-238">no</span></span>             | <span data-ttu-id="87048-239">no</span><span class="sxs-lookup"><span data-stu-id="87048-239">no</span></span>               |
| <span data-ttu-id="87048-240">msdyn_ismilestonename</span><span class="sxs-lookup"><span data-stu-id="87048-240">msdyn_ismilestonename</span></span>                  | <span data-ttu-id="87048-241">no</span><span class="sxs-lookup"><span data-stu-id="87048-241">no</span></span>             | <span data-ttu-id="87048-242">no</span><span class="sxs-lookup"><span data-stu-id="87048-242">no</span></span>               |
| <span data-ttu-id="87048-243">msdyn_LinkStatus</span><span class="sxs-lookup"><span data-stu-id="87048-243">msdyn_LinkStatus</span></span>                       | <span data-ttu-id="87048-244">no</span><span class="sxs-lookup"><span data-stu-id="87048-244">no</span></span>             | <span data-ttu-id="87048-245">no</span><span class="sxs-lookup"><span data-stu-id="87048-245">no</span></span>               |
| <span data-ttu-id="87048-246">msdyn_linkstatusname</span><span class="sxs-lookup"><span data-stu-id="87048-246">msdyn_linkstatusname</span></span>                   | <span data-ttu-id="87048-247">no</span><span class="sxs-lookup"><span data-stu-id="87048-247">no</span></span>             | <span data-ttu-id="87048-248">no</span><span class="sxs-lookup"><span data-stu-id="87048-248">no</span></span>               |
| <span data-ttu-id="87048-249">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="87048-249">msdyn_msprojectclientid</span></span>                | <span data-ttu-id="87048-250">no</span><span class="sxs-lookup"><span data-stu-id="87048-250">no</span></span>             | <span data-ttu-id="87048-251">no</span><span class="sxs-lookup"><span data-stu-id="87048-251">no</span></span>               |
| <span data-ttu-id="87048-252">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="87048-252">msdyn_plannedcost</span></span>                      | <span data-ttu-id="87048-253">no</span><span class="sxs-lookup"><span data-stu-id="87048-253">no</span></span>             | <span data-ttu-id="87048-254">no</span><span class="sxs-lookup"><span data-stu-id="87048-254">no</span></span>               |
| <span data-ttu-id="87048-255">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="87048-255">msdyn_plannedcost_base</span></span>                 | <span data-ttu-id="87048-256">no</span><span class="sxs-lookup"><span data-stu-id="87048-256">no</span></span>             | <span data-ttu-id="87048-257">no</span><span class="sxs-lookup"><span data-stu-id="87048-257">no</span></span>               |
| <span data-ttu-id="87048-258">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="87048-258">msdyn_plannedsales</span></span>                     | <span data-ttu-id="87048-259">no</span><span class="sxs-lookup"><span data-stu-id="87048-259">no</span></span>             | <span data-ttu-id="87048-260">no</span><span class="sxs-lookup"><span data-stu-id="87048-260">no</span></span>               |
| <span data-ttu-id="87048-261">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="87048-261">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="87048-262">no</span><span class="sxs-lookup"><span data-stu-id="87048-262">no</span></span>             | <span data-ttu-id="87048-263">no</span><span class="sxs-lookup"><span data-stu-id="87048-263">no</span></span>               |
| <span data-ttu-id="87048-264">msdyn_pluginprocessingdata</span><span class="sxs-lookup"><span data-stu-id="87048-264">msdyn_pluginprocessingdata</span></span>             | <span data-ttu-id="87048-265">no</span><span class="sxs-lookup"><span data-stu-id="87048-265">no</span></span>             | <span data-ttu-id="87048-266">no</span><span class="sxs-lookup"><span data-stu-id="87048-266">no</span></span>               |
| <span data-ttu-id="87048-267">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="87048-267">msdyn_progress</span></span>                         | <span data-ttu-id="87048-268">no</span><span class="sxs-lookup"><span data-stu-id="87048-268">no</span></span>             | <span data-ttu-id="87048-269">no (sí per a P4W)</span><span class="sxs-lookup"><span data-stu-id="87048-269">no (yes for P4W)</span></span> |
| <span data-ttu-id="87048-270">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="87048-270">msdyn_remainingcost</span></span>                    | <span data-ttu-id="87048-271">no</span><span class="sxs-lookup"><span data-stu-id="87048-271">no</span></span>             | <span data-ttu-id="87048-272">no</span><span class="sxs-lookup"><span data-stu-id="87048-272">no</span></span>               |
| <span data-ttu-id="87048-273">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="87048-273">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="87048-274">no</span><span class="sxs-lookup"><span data-stu-id="87048-274">no</span></span>             | <span data-ttu-id="87048-275">no</span><span class="sxs-lookup"><span data-stu-id="87048-275">no</span></span>               |
| <span data-ttu-id="87048-276">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="87048-276">msdyn_remainingsales</span></span>                   | <span data-ttu-id="87048-277">no</span><span class="sxs-lookup"><span data-stu-id="87048-277">no</span></span>             | <span data-ttu-id="87048-278">no</span><span class="sxs-lookup"><span data-stu-id="87048-278">no</span></span>               |
| <span data-ttu-id="87048-279">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="87048-279">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="87048-280">no</span><span class="sxs-lookup"><span data-stu-id="87048-280">no</span></span>             | <span data-ttu-id="87048-281">no</span><span class="sxs-lookup"><span data-stu-id="87048-281">no</span></span>               |
| <span data-ttu-id="87048-282">msdyn_requestedhours</span><span class="sxs-lookup"><span data-stu-id="87048-282">msdyn_requestedhours</span></span>                   | <span data-ttu-id="87048-283">no</span><span class="sxs-lookup"><span data-stu-id="87048-283">no</span></span>             | <span data-ttu-id="87048-284">no</span><span class="sxs-lookup"><span data-stu-id="87048-284">no</span></span>               |
| <span data-ttu-id="87048-285">msdyn_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="87048-285">msdyn_resourcecategory</span></span>                 | <span data-ttu-id="87048-286">no</span><span class="sxs-lookup"><span data-stu-id="87048-286">no</span></span>             | <span data-ttu-id="87048-287">no</span><span class="sxs-lookup"><span data-stu-id="87048-287">no</span></span>               |
| <span data-ttu-id="87048-288">msdyn_resourcecategoryname</span><span class="sxs-lookup"><span data-stu-id="87048-288">msdyn_resourcecategoryname</span></span>             | <span data-ttu-id="87048-289">no</span><span class="sxs-lookup"><span data-stu-id="87048-289">no</span></span>             | <span data-ttu-id="87048-290">no</span><span class="sxs-lookup"><span data-stu-id="87048-290">no</span></span>               |
| <span data-ttu-id="87048-291">msdyn_resourceorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="87048-291">msdyn_resourceorganizationalunitid</span></span>     | <span data-ttu-id="87048-292">no</span><span class="sxs-lookup"><span data-stu-id="87048-292">no</span></span>             | <span data-ttu-id="87048-293">no</span><span class="sxs-lookup"><span data-stu-id="87048-293">no</span></span>               |
| <span data-ttu-id="87048-294">msdyn_resourceorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="87048-294">msdyn_resourceorganizationalunitidname</span></span> | <span data-ttu-id="87048-295">no</span><span class="sxs-lookup"><span data-stu-id="87048-295">no</span></span>             | <span data-ttu-id="87048-296">no</span><span class="sxs-lookup"><span data-stu-id="87048-296">no</span></span>               |
| <span data-ttu-id="87048-297">msdyn_salesconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="87048-297">msdyn_salesconsumptionpercentage</span></span>       | <span data-ttu-id="87048-298">no</span><span class="sxs-lookup"><span data-stu-id="87048-298">no</span></span>             | <span data-ttu-id="87048-299">no</span><span class="sxs-lookup"><span data-stu-id="87048-299">no</span></span>               |
| <span data-ttu-id="87048-300">msdyn_salesestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="87048-300">msdyn_salesestimateatcomplete</span></span>          | <span data-ttu-id="87048-301">no</span><span class="sxs-lookup"><span data-stu-id="87048-301">no</span></span>             | <span data-ttu-id="87048-302">no</span><span class="sxs-lookup"><span data-stu-id="87048-302">no</span></span>               |
| <span data-ttu-id="87048-303">msdyn_salesestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="87048-303">msdyn_salesestimateatcomplete_base</span></span>     | <span data-ttu-id="87048-304">no</span><span class="sxs-lookup"><span data-stu-id="87048-304">no</span></span>             | <span data-ttu-id="87048-305">no</span><span class="sxs-lookup"><span data-stu-id="87048-305">no</span></span>               |
| <span data-ttu-id="87048-306">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="87048-306">msdyn_salesvariance</span></span>                    | <span data-ttu-id="87048-307">no</span><span class="sxs-lookup"><span data-stu-id="87048-307">no</span></span>             | <span data-ttu-id="87048-308">no</span><span class="sxs-lookup"><span data-stu-id="87048-308">no</span></span>               |
| <span data-ttu-id="87048-309">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="87048-309">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="87048-310">no</span><span class="sxs-lookup"><span data-stu-id="87048-310">no</span></span>             | <span data-ttu-id="87048-311">no</span><span class="sxs-lookup"><span data-stu-id="87048-311">no</span></span>               |
| <span data-ttu-id="87048-312">msdyn_scheduleddurationminutes</span><span class="sxs-lookup"><span data-stu-id="87048-312">msdyn_scheduleddurationminutes</span></span>         | <span data-ttu-id="87048-313">no</span><span class="sxs-lookup"><span data-stu-id="87048-313">no</span></span>             | <span data-ttu-id="87048-314">no</span><span class="sxs-lookup"><span data-stu-id="87048-314">no</span></span>               |
| <span data-ttu-id="87048-315">msdyn_scheduledend</span><span class="sxs-lookup"><span data-stu-id="87048-315">msdyn_scheduledend</span></span>                     | <span data-ttu-id="87048-316">no</span><span class="sxs-lookup"><span data-stu-id="87048-316">no</span></span>             | <span data-ttu-id="87048-317">no</span><span class="sxs-lookup"><span data-stu-id="87048-317">no</span></span>               |
| <span data-ttu-id="87048-318">msdyn_scheduledstart</span><span class="sxs-lookup"><span data-stu-id="87048-318">msdyn_scheduledstart</span></span>                   | <span data-ttu-id="87048-319">no</span><span class="sxs-lookup"><span data-stu-id="87048-319">no</span></span>             | <span data-ttu-id="87048-320">no</span><span class="sxs-lookup"><span data-stu-id="87048-320">no</span></span>               |
| <span data-ttu-id="87048-321">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="87048-321">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="87048-322">no</span><span class="sxs-lookup"><span data-stu-id="87048-322">no</span></span>             | <span data-ttu-id="87048-323">no</span><span class="sxs-lookup"><span data-stu-id="87048-323">no</span></span>               |
| <span data-ttu-id="87048-324">msdyn_skipupdateestimateline</span><span class="sxs-lookup"><span data-stu-id="87048-324">msdyn_skipupdateestimateline</span></span>           | <span data-ttu-id="87048-325">no</span><span class="sxs-lookup"><span data-stu-id="87048-325">no</span></span>             | <span data-ttu-id="87048-326">no</span><span class="sxs-lookup"><span data-stu-id="87048-326">no</span></span>               |
| <span data-ttu-id="87048-327">msdyn_skipupdateestimatelinename</span><span class="sxs-lookup"><span data-stu-id="87048-327">msdyn_skipupdateestimatelinename</span></span>       | <span data-ttu-id="87048-328">no</span><span class="sxs-lookup"><span data-stu-id="87048-328">no</span></span>             | <span data-ttu-id="87048-329">no</span><span class="sxs-lookup"><span data-stu-id="87048-329">no</span></span>               |
| <span data-ttu-id="87048-330">msdyn_summary</span><span class="sxs-lookup"><span data-stu-id="87048-330">msdyn_summary</span></span>                          | <span data-ttu-id="87048-331">no</span><span class="sxs-lookup"><span data-stu-id="87048-331">no</span></span>             | <span data-ttu-id="87048-332">no</span><span class="sxs-lookup"><span data-stu-id="87048-332">no</span></span>               |
| <span data-ttu-id="87048-333">msdyn_varianceofcost</span><span class="sxs-lookup"><span data-stu-id="87048-333">msdyn_varianceofcost</span></span>                   | <span data-ttu-id="87048-334">no</span><span class="sxs-lookup"><span data-stu-id="87048-334">no</span></span>             | <span data-ttu-id="87048-335">no</span><span class="sxs-lookup"><span data-stu-id="87048-335">no</span></span>               |
| <span data-ttu-id="87048-336">msdyn_varianceofcost_base</span><span class="sxs-lookup"><span data-stu-id="87048-336">msdyn_varianceofcost_base</span></span>              | <span data-ttu-id="87048-337">no</span><span class="sxs-lookup"><span data-stu-id="87048-337">no</span></span>             | <span data-ttu-id="87048-338">no</span><span class="sxs-lookup"><span data-stu-id="87048-338">no</span></span>               |

### <a name="project-task-dependency"></a><span data-ttu-id="87048-339">Dependència de les tasques del projecte</span><span class="sxs-lookup"><span data-stu-id="87048-339">Project task dependency</span></span>

| <span data-ttu-id="87048-340">**Nom lògic**</span><span class="sxs-lookup"><span data-stu-id="87048-340">**Logical name**</span></span>              | <span data-ttu-id="87048-341">**Pot crear**</span><span class="sxs-lookup"><span data-stu-id="87048-341">**Can create**</span></span> | <span data-ttu-id="87048-342">**Pot editar**</span><span class="sxs-lookup"><span data-stu-id="87048-342">**Can edit**</span></span> |
|-------------------------------|----------------|--------------|
| <span data-ttu-id="87048-343">msdyn_linktype</span><span class="sxs-lookup"><span data-stu-id="87048-343">msdyn_linktype</span></span>                | <span data-ttu-id="87048-344">no</span><span class="sxs-lookup"><span data-stu-id="87048-344">no</span></span>             | <span data-ttu-id="87048-345">no</span><span class="sxs-lookup"><span data-stu-id="87048-345">no</span></span>           |
| <span data-ttu-id="87048-346">msdyn_linktypename</span><span class="sxs-lookup"><span data-stu-id="87048-346">msdyn_linktypename</span></span>            | <span data-ttu-id="87048-347">no</span><span class="sxs-lookup"><span data-stu-id="87048-347">no</span></span>             | <span data-ttu-id="87048-348">no</span><span class="sxs-lookup"><span data-stu-id="87048-348">no</span></span>           |
| <span data-ttu-id="87048-349">msdyn_predecessortask</span><span class="sxs-lookup"><span data-stu-id="87048-349">msdyn_predecessortask</span></span>         | <span data-ttu-id="87048-350">sí</span><span class="sxs-lookup"><span data-stu-id="87048-350">yes</span></span>            | <span data-ttu-id="87048-351">no</span><span class="sxs-lookup"><span data-stu-id="87048-351">no</span></span>           |
| <span data-ttu-id="87048-352">msdyn_predecessortaskname</span><span class="sxs-lookup"><span data-stu-id="87048-352">msdyn_predecessortaskname</span></span>     | <span data-ttu-id="87048-353">sí</span><span class="sxs-lookup"><span data-stu-id="87048-353">yes</span></span>            | <span data-ttu-id="87048-354">no</span><span class="sxs-lookup"><span data-stu-id="87048-354">no</span></span>           |
| <span data-ttu-id="87048-355">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="87048-355">msdyn_project</span></span>                 | <span data-ttu-id="87048-356">sí</span><span class="sxs-lookup"><span data-stu-id="87048-356">yes</span></span>            | <span data-ttu-id="87048-357">no</span><span class="sxs-lookup"><span data-stu-id="87048-357">no</span></span>           |
| <span data-ttu-id="87048-358">msdyn_projectname</span><span class="sxs-lookup"><span data-stu-id="87048-358">msdyn_projectname</span></span>             | <span data-ttu-id="87048-359">sí</span><span class="sxs-lookup"><span data-stu-id="87048-359">yes</span></span>            | <span data-ttu-id="87048-360">no</span><span class="sxs-lookup"><span data-stu-id="87048-360">no</span></span>           |
| <span data-ttu-id="87048-361">msdyn_projecttaskdependencyid</span><span class="sxs-lookup"><span data-stu-id="87048-361">msdyn_projecttaskdependencyid</span></span> | <span data-ttu-id="87048-362">sí</span><span class="sxs-lookup"><span data-stu-id="87048-362">yes</span></span>            | <span data-ttu-id="87048-363">no</span><span class="sxs-lookup"><span data-stu-id="87048-363">no</span></span>           |
| <span data-ttu-id="87048-364">msdyn_successortask</span><span class="sxs-lookup"><span data-stu-id="87048-364">msdyn_successortask</span></span>           | <span data-ttu-id="87048-365">sí</span><span class="sxs-lookup"><span data-stu-id="87048-365">yes</span></span>            | <span data-ttu-id="87048-366">no</span><span class="sxs-lookup"><span data-stu-id="87048-366">no</span></span>           |
| <span data-ttu-id="87048-367">msdyn_successortaskname</span><span class="sxs-lookup"><span data-stu-id="87048-367">msdyn_successortaskname</span></span>       | <span data-ttu-id="87048-368">sí</span><span class="sxs-lookup"><span data-stu-id="87048-368">yes</span></span>            | <span data-ttu-id="87048-369">no</span><span class="sxs-lookup"><span data-stu-id="87048-369">no</span></span>           |

### <a name="resource-assignment"></a><span data-ttu-id="87048-370">Assignació de recursos</span><span class="sxs-lookup"><span data-stu-id="87048-370">Resource assignment</span></span>

| <span data-ttu-id="87048-371">**Nom lògic**</span><span class="sxs-lookup"><span data-stu-id="87048-371">**Logical name**</span></span>             | <span data-ttu-id="87048-372">**Pot crear**</span><span class="sxs-lookup"><span data-stu-id="87048-372">**Can create**</span></span> | <span data-ttu-id="87048-373">**Pot editar**</span><span class="sxs-lookup"><span data-stu-id="87048-373">**Can edit**</span></span> |
|------------------------------|----------------|--------------|
| <span data-ttu-id="87048-374">msdyn_bookableresourceid</span><span class="sxs-lookup"><span data-stu-id="87048-374">msdyn_bookableresourceid</span></span>     | <span data-ttu-id="87048-375">sí</span><span class="sxs-lookup"><span data-stu-id="87048-375">yes</span></span>            | <span data-ttu-id="87048-376">no</span><span class="sxs-lookup"><span data-stu-id="87048-376">no</span></span>           |
| <span data-ttu-id="87048-377">msdyn_bookableresourceidname</span><span class="sxs-lookup"><span data-stu-id="87048-377">msdyn_bookableresourceidname</span></span> | <span data-ttu-id="87048-378">sí</span><span class="sxs-lookup"><span data-stu-id="87048-378">yes</span></span>            | <span data-ttu-id="87048-379">no</span><span class="sxs-lookup"><span data-stu-id="87048-379">no</span></span>           |
| <span data-ttu-id="87048-380">msdyn_bookingstatusid</span><span class="sxs-lookup"><span data-stu-id="87048-380">msdyn_bookingstatusid</span></span>        | <span data-ttu-id="87048-381">no</span><span class="sxs-lookup"><span data-stu-id="87048-381">no</span></span>             | <span data-ttu-id="87048-382">no</span><span class="sxs-lookup"><span data-stu-id="87048-382">no</span></span>           |
| <span data-ttu-id="87048-383">msdyn_bookingstatusidname</span><span class="sxs-lookup"><span data-stu-id="87048-383">msdyn_bookingstatusidname</span></span>    | <span data-ttu-id="87048-384">no</span><span class="sxs-lookup"><span data-stu-id="87048-384">no</span></span>             | <span data-ttu-id="87048-385">no</span><span class="sxs-lookup"><span data-stu-id="87048-385">no</span></span>           |
| <span data-ttu-id="87048-386">msdyn_committype</span><span class="sxs-lookup"><span data-stu-id="87048-386">msdyn_committype</span></span>             | <span data-ttu-id="87048-387">no</span><span class="sxs-lookup"><span data-stu-id="87048-387">no</span></span>             | <span data-ttu-id="87048-388">no</span><span class="sxs-lookup"><span data-stu-id="87048-388">no</span></span>           |
| <span data-ttu-id="87048-389">msdyn_committypename</span><span class="sxs-lookup"><span data-stu-id="87048-389">msdyn_committypename</span></span>         | <span data-ttu-id="87048-390">no</span><span class="sxs-lookup"><span data-stu-id="87048-390">no</span></span>             | <span data-ttu-id="87048-391">no</span><span class="sxs-lookup"><span data-stu-id="87048-391">no</span></span>           |
| <span data-ttu-id="87048-392">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="87048-392">msdyn_effort</span></span>                 | <span data-ttu-id="87048-393">no</span><span class="sxs-lookup"><span data-stu-id="87048-393">no</span></span>             | <span data-ttu-id="87048-394">no</span><span class="sxs-lookup"><span data-stu-id="87048-394">no</span></span>           |
| <span data-ttu-id="87048-395">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="87048-395">msdyn_effortcompleted</span></span>        | <span data-ttu-id="87048-396">no</span><span class="sxs-lookup"><span data-stu-id="87048-396">no</span></span>             | <span data-ttu-id="87048-397">no</span><span class="sxs-lookup"><span data-stu-id="87048-397">no</span></span>           |
| <span data-ttu-id="87048-398">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="87048-398">msdyn_effortremaining</span></span>        | <span data-ttu-id="87048-399">no</span><span class="sxs-lookup"><span data-stu-id="87048-399">no</span></span>             | <span data-ttu-id="87048-400">no</span><span class="sxs-lookup"><span data-stu-id="87048-400">no</span></span>           |
| <span data-ttu-id="87048-401">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="87048-401">msdyn_finish</span></span>                 | <span data-ttu-id="87048-402">no</span><span class="sxs-lookup"><span data-stu-id="87048-402">no</span></span>             | <span data-ttu-id="87048-403">no</span><span class="sxs-lookup"><span data-stu-id="87048-403">no</span></span>           |
| <span data-ttu-id="87048-404">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="87048-404">msdyn_plannedcost</span></span>            | <span data-ttu-id="87048-405">no</span><span class="sxs-lookup"><span data-stu-id="87048-405">no</span></span>             | <span data-ttu-id="87048-406">no</span><span class="sxs-lookup"><span data-stu-id="87048-406">no</span></span>           |
| <span data-ttu-id="87048-407">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="87048-407">msdyn_plannedcost_base</span></span>       | <span data-ttu-id="87048-408">no</span><span class="sxs-lookup"><span data-stu-id="87048-408">no</span></span>             | <span data-ttu-id="87048-409">no</span><span class="sxs-lookup"><span data-stu-id="87048-409">no</span></span>           |
| <span data-ttu-id="87048-410">msdyn_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="87048-410">msdyn_plannedcostcontour</span></span>     | <span data-ttu-id="87048-411">no</span><span class="sxs-lookup"><span data-stu-id="87048-411">no</span></span>             | <span data-ttu-id="87048-412">no</span><span class="sxs-lookup"><span data-stu-id="87048-412">no</span></span>           |
| <span data-ttu-id="87048-413">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="87048-413">msdyn_plannedsales</span></span>           | <span data-ttu-id="87048-414">no</span><span class="sxs-lookup"><span data-stu-id="87048-414">no</span></span>             | <span data-ttu-id="87048-415">no</span><span class="sxs-lookup"><span data-stu-id="87048-415">no</span></span>           |
| <span data-ttu-id="87048-416">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="87048-416">msdyn_plannedsales_base</span></span>      | <span data-ttu-id="87048-417">no</span><span class="sxs-lookup"><span data-stu-id="87048-417">no</span></span>             | <span data-ttu-id="87048-418">no</span><span class="sxs-lookup"><span data-stu-id="87048-418">no</span></span>           |
| <span data-ttu-id="87048-419">msdyn_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="87048-419">msdyn_plannedsalescontour</span></span>    | <span data-ttu-id="87048-420">no</span><span class="sxs-lookup"><span data-stu-id="87048-420">no</span></span>             | <span data-ttu-id="87048-421">no</span><span class="sxs-lookup"><span data-stu-id="87048-421">no</span></span>           |
| <span data-ttu-id="87048-422">msdyn_plannedwork</span><span class="sxs-lookup"><span data-stu-id="87048-422">msdyn_plannedwork</span></span>            | <span data-ttu-id="87048-423">no</span><span class="sxs-lookup"><span data-stu-id="87048-423">no</span></span>             | <span data-ttu-id="87048-424">no</span><span class="sxs-lookup"><span data-stu-id="87048-424">no</span></span>           |
| <span data-ttu-id="87048-425">msdyn_projectid</span><span class="sxs-lookup"><span data-stu-id="87048-425">msdyn_projectid</span></span>              | <span data-ttu-id="87048-426">sí</span><span class="sxs-lookup"><span data-stu-id="87048-426">yes</span></span>            | <span data-ttu-id="87048-427">no</span><span class="sxs-lookup"><span data-stu-id="87048-427">no</span></span>           |
| <span data-ttu-id="87048-428">msdyn_projectidname</span><span class="sxs-lookup"><span data-stu-id="87048-428">msdyn_projectidname</span></span>          | <span data-ttu-id="87048-429">no</span><span class="sxs-lookup"><span data-stu-id="87048-429">no</span></span>             | <span data-ttu-id="87048-430">no</span><span class="sxs-lookup"><span data-stu-id="87048-430">no</span></span>           |
| <span data-ttu-id="87048-431">msdyn_projectteamid</span><span class="sxs-lookup"><span data-stu-id="87048-431">msdyn_projectteamid</span></span>          | <span data-ttu-id="87048-432">no</span><span class="sxs-lookup"><span data-stu-id="87048-432">no</span></span>             | <span data-ttu-id="87048-433">no</span><span class="sxs-lookup"><span data-stu-id="87048-433">no</span></span>           |
| <span data-ttu-id="87048-434">msdyn_projectteamidname</span><span class="sxs-lookup"><span data-stu-id="87048-434">msdyn_projectteamidname</span></span>      | <span data-ttu-id="87048-435">no</span><span class="sxs-lookup"><span data-stu-id="87048-435">no</span></span>             | <span data-ttu-id="87048-436">no</span><span class="sxs-lookup"><span data-stu-id="87048-436">no</span></span>           |
| <span data-ttu-id="87048-437">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="87048-437">msdyn_start</span></span>                  | <span data-ttu-id="87048-438">no</span><span class="sxs-lookup"><span data-stu-id="87048-438">no</span></span>             | <span data-ttu-id="87048-439">no</span><span class="sxs-lookup"><span data-stu-id="87048-439">no</span></span>           |
| <span data-ttu-id="87048-440">msdyn_taskid</span><span class="sxs-lookup"><span data-stu-id="87048-440">msdyn_taskid</span></span>                 | <span data-ttu-id="87048-441">no</span><span class="sxs-lookup"><span data-stu-id="87048-441">no</span></span>             | <span data-ttu-id="87048-442">no</span><span class="sxs-lookup"><span data-stu-id="87048-442">no</span></span>           |
| <span data-ttu-id="87048-443">msdyn_taskidname</span><span class="sxs-lookup"><span data-stu-id="87048-443">msdyn_taskidname</span></span>             | <span data-ttu-id="87048-444">no</span><span class="sxs-lookup"><span data-stu-id="87048-444">no</span></span>             | <span data-ttu-id="87048-445">no</span><span class="sxs-lookup"><span data-stu-id="87048-445">no</span></span>           |
| <span data-ttu-id="87048-446">msdyn_userresourceid</span><span class="sxs-lookup"><span data-stu-id="87048-446">msdyn_userresourceid</span></span>         | <span data-ttu-id="87048-447">no</span><span class="sxs-lookup"><span data-stu-id="87048-447">no</span></span>             | <span data-ttu-id="87048-448">no</span><span class="sxs-lookup"><span data-stu-id="87048-448">no</span></span>           |

### <a name="project-team-member"></a><span data-ttu-id="87048-449">Membre de l'equip del projecte</span><span class="sxs-lookup"><span data-stu-id="87048-449">Project team member</span></span>

| <span data-ttu-id="87048-450">**Nom lògic**</span><span class="sxs-lookup"><span data-stu-id="87048-450">**Logical name**</span></span>                                 | <span data-ttu-id="87048-451">**Pot crear**</span><span class="sxs-lookup"><span data-stu-id="87048-451">**Can create**</span></span> | <span data-ttu-id="87048-452">**Pot editar**</span><span class="sxs-lookup"><span data-stu-id="87048-452">**Can edit**</span></span> |
|--------------------------------------------------|----------------|--------------|
| <span data-ttu-id="87048-453">msdyn_calendarid</span><span class="sxs-lookup"><span data-stu-id="87048-453">msdyn_calendarid</span></span>                                 | <span data-ttu-id="87048-454">no</span><span class="sxs-lookup"><span data-stu-id="87048-454">no</span></span>             | <span data-ttu-id="87048-455">no</span><span class="sxs-lookup"><span data-stu-id="87048-455">no</span></span>           |
| <span data-ttu-id="87048-456">msdyn_creategenericteammemberwithrequirementname</span><span class="sxs-lookup"><span data-stu-id="87048-456">msdyn_creategenericteammemberwithrequirementname</span></span> | <span data-ttu-id="87048-457">no</span><span class="sxs-lookup"><span data-stu-id="87048-457">no</span></span>             | <span data-ttu-id="87048-458">no</span><span class="sxs-lookup"><span data-stu-id="87048-458">no</span></span>           |
| <span data-ttu-id="87048-459">msdyn_deletestatus</span><span class="sxs-lookup"><span data-stu-id="87048-459">msdyn_deletestatus</span></span>                               | <span data-ttu-id="87048-460">no</span><span class="sxs-lookup"><span data-stu-id="87048-460">no</span></span>             | <span data-ttu-id="87048-461">no</span><span class="sxs-lookup"><span data-stu-id="87048-461">no</span></span>           |
| <span data-ttu-id="87048-462">msdyn_deletestatusname</span><span class="sxs-lookup"><span data-stu-id="87048-462">msdyn_deletestatusname</span></span>                           | <span data-ttu-id="87048-463">no</span><span class="sxs-lookup"><span data-stu-id="87048-463">no</span></span>             | <span data-ttu-id="87048-464">no</span><span class="sxs-lookup"><span data-stu-id="87048-464">no</span></span>           |
| <span data-ttu-id="87048-465">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="87048-465">msdyn_effort</span></span>                                     | <span data-ttu-id="87048-466">no</span><span class="sxs-lookup"><span data-stu-id="87048-466">no</span></span>             | <span data-ttu-id="87048-467">no</span><span class="sxs-lookup"><span data-stu-id="87048-467">no</span></span>           |
| <span data-ttu-id="87048-468">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="87048-468">msdyn_effortcompleted</span></span>                            | <span data-ttu-id="87048-469">no</span><span class="sxs-lookup"><span data-stu-id="87048-469">no</span></span>             | <span data-ttu-id="87048-470">no</span><span class="sxs-lookup"><span data-stu-id="87048-470">no</span></span>           |
| <span data-ttu-id="87048-471">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="87048-471">msdyn_effortremaining</span></span>                            | <span data-ttu-id="87048-472">no</span><span class="sxs-lookup"><span data-stu-id="87048-472">no</span></span>             | <span data-ttu-id="87048-473">no</span><span class="sxs-lookup"><span data-stu-id="87048-473">no</span></span>           |
| <span data-ttu-id="87048-474">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="87048-474">msdyn_finish</span></span>                                     | <span data-ttu-id="87048-475">no</span><span class="sxs-lookup"><span data-stu-id="87048-475">no</span></span>             | <span data-ttu-id="87048-476">no</span><span class="sxs-lookup"><span data-stu-id="87048-476">no</span></span>           |
| <span data-ttu-id="87048-477">msdyn_hardbookedhours</span><span class="sxs-lookup"><span data-stu-id="87048-477">msdyn_hardbookedhours</span></span>                            | <span data-ttu-id="87048-478">no</span><span class="sxs-lookup"><span data-stu-id="87048-478">no</span></span>             | <span data-ttu-id="87048-479">no</span><span class="sxs-lookup"><span data-stu-id="87048-479">no</span></span>           |
| <span data-ttu-id="87048-480">msdyn_hours</span><span class="sxs-lookup"><span data-stu-id="87048-480">msdyn_hours</span></span>                                      | <span data-ttu-id="87048-481">no</span><span class="sxs-lookup"><span data-stu-id="87048-481">no</span></span>             | <span data-ttu-id="87048-482">no</span><span class="sxs-lookup"><span data-stu-id="87048-482">no</span></span>           |
| <span data-ttu-id="87048-483">msdyn_markedfordeletiontimer</span><span class="sxs-lookup"><span data-stu-id="87048-483">msdyn_markedfordeletiontimer</span></span>                     | <span data-ttu-id="87048-484">no</span><span class="sxs-lookup"><span data-stu-id="87048-484">no</span></span>             | <span data-ttu-id="87048-485">no</span><span class="sxs-lookup"><span data-stu-id="87048-485">no</span></span>           |
| <span data-ttu-id="87048-486">msdyn_markedfordeletiontimestamp</span><span class="sxs-lookup"><span data-stu-id="87048-486">msdyn_markedfordeletiontimestamp</span></span>                 | <span data-ttu-id="87048-487">no</span><span class="sxs-lookup"><span data-stu-id="87048-487">no</span></span>             | <span data-ttu-id="87048-488">no</span><span class="sxs-lookup"><span data-stu-id="87048-488">no</span></span>           |
| <span data-ttu-id="87048-489">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="87048-489">msdyn_msprojectclientid</span></span>                          | <span data-ttu-id="87048-490">no</span><span class="sxs-lookup"><span data-stu-id="87048-490">no</span></span>             | <span data-ttu-id="87048-491">no</span><span class="sxs-lookup"><span data-stu-id="87048-491">no</span></span>           |
| <span data-ttu-id="87048-492">msdyn_percentage</span><span class="sxs-lookup"><span data-stu-id="87048-492">msdyn_percentage</span></span>                                 | <span data-ttu-id="87048-493">no</span><span class="sxs-lookup"><span data-stu-id="87048-493">no</span></span>             | <span data-ttu-id="87048-494">no</span><span class="sxs-lookup"><span data-stu-id="87048-494">no</span></span>           |
| <span data-ttu-id="87048-495">msdyn_requiredhours</span><span class="sxs-lookup"><span data-stu-id="87048-495">msdyn_requiredhours</span></span>                              | <span data-ttu-id="87048-496">no</span><span class="sxs-lookup"><span data-stu-id="87048-496">no</span></span>             | <span data-ttu-id="87048-497">no</span><span class="sxs-lookup"><span data-stu-id="87048-497">no</span></span>           |
| <span data-ttu-id="87048-498">msdyn_softbookedhours</span><span class="sxs-lookup"><span data-stu-id="87048-498">msdyn_softbookedhours</span></span>                            | <span data-ttu-id="87048-499">no</span><span class="sxs-lookup"><span data-stu-id="87048-499">no</span></span>             | <span data-ttu-id="87048-500">no</span><span class="sxs-lookup"><span data-stu-id="87048-500">no</span></span>           |
| <span data-ttu-id="87048-501">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="87048-501">msdyn_start</span></span>                                      | <span data-ttu-id="87048-502">no</span><span class="sxs-lookup"><span data-stu-id="87048-502">no</span></span>             | <span data-ttu-id="87048-503">no</span><span class="sxs-lookup"><span data-stu-id="87048-503">no</span></span>           |

### <a name="project"></a><span data-ttu-id="87048-504">Project</span><span class="sxs-lookup"><span data-stu-id="87048-504">Project</span></span>

| <span data-ttu-id="87048-505">**Nom lògic**</span><span class="sxs-lookup"><span data-stu-id="87048-505">**Logical name**</span></span>                       | <span data-ttu-id="87048-506">**Pot crear**</span><span class="sxs-lookup"><span data-stu-id="87048-506">**Can create**</span></span> | <span data-ttu-id="87048-507">**Pot editar**</span><span class="sxs-lookup"><span data-stu-id="87048-507">**Can edit**</span></span> |
|----------------------------------------|----------------|--------------|
| <span data-ttu-id="87048-508">msdyn_actualexpensecost</span><span class="sxs-lookup"><span data-stu-id="87048-508">msdyn_actualexpensecost</span></span>                | <span data-ttu-id="87048-509">no</span><span class="sxs-lookup"><span data-stu-id="87048-509">no</span></span>             | <span data-ttu-id="87048-510">no</span><span class="sxs-lookup"><span data-stu-id="87048-510">no</span></span>           |
| <span data-ttu-id="87048-511">msdyn_actualexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="87048-511">msdyn_actualexpensecost_base</span></span>           | <span data-ttu-id="87048-512">no</span><span class="sxs-lookup"><span data-stu-id="87048-512">no</span></span>             | <span data-ttu-id="87048-513">no</span><span class="sxs-lookup"><span data-stu-id="87048-513">no</span></span>           |
| <span data-ttu-id="87048-514">msdyn_actuallaborcost</span><span class="sxs-lookup"><span data-stu-id="87048-514">msdyn_actuallaborcost</span></span>                  | <span data-ttu-id="87048-515">no</span><span class="sxs-lookup"><span data-stu-id="87048-515">no</span></span>             | <span data-ttu-id="87048-516">no</span><span class="sxs-lookup"><span data-stu-id="87048-516">no</span></span>           |
| <span data-ttu-id="87048-517">msdyn_actuallaborcost_base</span><span class="sxs-lookup"><span data-stu-id="87048-517">msdyn_actuallaborcost_base</span></span>             | <span data-ttu-id="87048-518">no</span><span class="sxs-lookup"><span data-stu-id="87048-518">no</span></span>             | <span data-ttu-id="87048-519">no</span><span class="sxs-lookup"><span data-stu-id="87048-519">no</span></span>           |
| <span data-ttu-id="87048-520">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="87048-520">msdyn_actualsales</span></span>                      | <span data-ttu-id="87048-521">no</span><span class="sxs-lookup"><span data-stu-id="87048-521">no</span></span>             | <span data-ttu-id="87048-522">no</span><span class="sxs-lookup"><span data-stu-id="87048-522">no</span></span>           |
| <span data-ttu-id="87048-523">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="87048-523">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="87048-524">no</span><span class="sxs-lookup"><span data-stu-id="87048-524">no</span></span>             | <span data-ttu-id="87048-525">no</span><span class="sxs-lookup"><span data-stu-id="87048-525">no</span></span>           |
| <span data-ttu-id="87048-526">msdyn_contractlineproject</span><span class="sxs-lookup"><span data-stu-id="87048-526">msdyn_contractlineproject</span></span>              | <span data-ttu-id="87048-527">sí</span><span class="sxs-lookup"><span data-stu-id="87048-527">yes</span></span>            | <span data-ttu-id="87048-528">no</span><span class="sxs-lookup"><span data-stu-id="87048-528">no</span></span>           |
| <span data-ttu-id="87048-529">msdyn_contractorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="87048-529">msdyn_contractorganizationalunitid</span></span>     | <span data-ttu-id="87048-530">sí</span><span class="sxs-lookup"><span data-stu-id="87048-530">yes</span></span>            | <span data-ttu-id="87048-531">no</span><span class="sxs-lookup"><span data-stu-id="87048-531">no</span></span>           |
| <span data-ttu-id="87048-532">msdyn_contractorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="87048-532">msdyn_contractorganizationalunitidname</span></span> | <span data-ttu-id="87048-533">sí</span><span class="sxs-lookup"><span data-stu-id="87048-533">yes</span></span>            | <span data-ttu-id="87048-534">no</span><span class="sxs-lookup"><span data-stu-id="87048-534">no</span></span>           |
| <span data-ttu-id="87048-535">msdyn_costconsumption</span><span class="sxs-lookup"><span data-stu-id="87048-535">msdyn_costconsumption</span></span>                  | <span data-ttu-id="87048-536">no</span><span class="sxs-lookup"><span data-stu-id="87048-536">no</span></span>             | <span data-ttu-id="87048-537">no</span><span class="sxs-lookup"><span data-stu-id="87048-537">no</span></span>           |
| <span data-ttu-id="87048-538">msdyn_costestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="87048-538">msdyn_costestimateatcomplete</span></span>           | <span data-ttu-id="87048-539">no</span><span class="sxs-lookup"><span data-stu-id="87048-539">no</span></span>             | <span data-ttu-id="87048-540">no</span><span class="sxs-lookup"><span data-stu-id="87048-540">no</span></span>           |
| <span data-ttu-id="87048-541">msdyn_costestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="87048-541">msdyn_costestimateatcomplete_base</span></span>      | <span data-ttu-id="87048-542">no</span><span class="sxs-lookup"><span data-stu-id="87048-542">no</span></span>             | <span data-ttu-id="87048-543">no</span><span class="sxs-lookup"><span data-stu-id="87048-543">no</span></span>           |
| <span data-ttu-id="87048-544">msdyn_costvariance</span><span class="sxs-lookup"><span data-stu-id="87048-544">msdyn_costvariance</span></span>                     | <span data-ttu-id="87048-545">no</span><span class="sxs-lookup"><span data-stu-id="87048-545">no</span></span>             | <span data-ttu-id="87048-546">no</span><span class="sxs-lookup"><span data-stu-id="87048-546">no</span></span>           |
| <span data-ttu-id="87048-547">msdyn_costvariance_base</span><span class="sxs-lookup"><span data-stu-id="87048-547">msdyn_costvariance_base</span></span>                | <span data-ttu-id="87048-548">no</span><span class="sxs-lookup"><span data-stu-id="87048-548">no</span></span>             | <span data-ttu-id="87048-549">no</span><span class="sxs-lookup"><span data-stu-id="87048-549">no</span></span>           |
| <span data-ttu-id="87048-550">msdyn_duration</span><span class="sxs-lookup"><span data-stu-id="87048-550">msdyn_duration</span></span>                         | <span data-ttu-id="87048-551">no</span><span class="sxs-lookup"><span data-stu-id="87048-551">no</span></span>             | <span data-ttu-id="87048-552">no</span><span class="sxs-lookup"><span data-stu-id="87048-552">no</span></span>           |
| <span data-ttu-id="87048-553">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="87048-553">msdyn_effort</span></span>                           | <span data-ttu-id="87048-554">no</span><span class="sxs-lookup"><span data-stu-id="87048-554">no</span></span>             | <span data-ttu-id="87048-555">no</span><span class="sxs-lookup"><span data-stu-id="87048-555">no</span></span>           |
| <span data-ttu-id="87048-556">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="87048-556">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="87048-557">no</span><span class="sxs-lookup"><span data-stu-id="87048-557">no</span></span>             | <span data-ttu-id="87048-558">no</span><span class="sxs-lookup"><span data-stu-id="87048-558">no</span></span>           |
| <span data-ttu-id="87048-559">msdyn_effortestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="87048-559">msdyn_effortestimateatcompleteeac</span></span>      | <span data-ttu-id="87048-560">no</span><span class="sxs-lookup"><span data-stu-id="87048-560">no</span></span>             | <span data-ttu-id="87048-561">no</span><span class="sxs-lookup"><span data-stu-id="87048-561">no</span></span>           |
| <span data-ttu-id="87048-562">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="87048-562">msdyn_effortremaining</span></span>                  | <span data-ttu-id="87048-563">no</span><span class="sxs-lookup"><span data-stu-id="87048-563">no</span></span>             | <span data-ttu-id="87048-564">no</span><span class="sxs-lookup"><span data-stu-id="87048-564">no</span></span>           |
| <span data-ttu-id="87048-565">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="87048-565">msdyn_finish</span></span>                           | <span data-ttu-id="87048-566">sí</span><span class="sxs-lookup"><span data-stu-id="87048-566">yes</span></span>            | <span data-ttu-id="87048-567">sí</span><span class="sxs-lookup"><span data-stu-id="87048-567">yes</span></span>          |
| <span data-ttu-id="87048-568">msdyn_globalrevisiontoken</span><span class="sxs-lookup"><span data-stu-id="87048-568">msdyn_globalrevisiontoken</span></span>              | <span data-ttu-id="87048-569">no</span><span class="sxs-lookup"><span data-stu-id="87048-569">no</span></span>             | <span data-ttu-id="87048-570">no</span><span class="sxs-lookup"><span data-stu-id="87048-570">no</span></span>           |
| <span data-ttu-id="87048-571">msdyn_islinkedtomsprojectclient</span><span class="sxs-lookup"><span data-stu-id="87048-571">msdyn_islinkedtomsprojectclient</span></span>        | <span data-ttu-id="87048-572">no</span><span class="sxs-lookup"><span data-stu-id="87048-572">no</span></span>             | <span data-ttu-id="87048-573">no</span><span class="sxs-lookup"><span data-stu-id="87048-573">no</span></span>           |
| <span data-ttu-id="87048-574">msdyn_islinkedtomsprojectclientname</span><span class="sxs-lookup"><span data-stu-id="87048-574">msdyn_islinkedtomsprojectclientname</span></span>    | <span data-ttu-id="87048-575">no</span><span class="sxs-lookup"><span data-stu-id="87048-575">no</span></span>             | <span data-ttu-id="87048-576">no</span><span class="sxs-lookup"><span data-stu-id="87048-576">no</span></span>           |
| <span data-ttu-id="87048-577">msdyn_linkeddocumenturl</span><span class="sxs-lookup"><span data-stu-id="87048-577">msdyn_linkeddocumenturl</span></span>                | <span data-ttu-id="87048-578">no</span><span class="sxs-lookup"><span data-stu-id="87048-578">no</span></span>             | <span data-ttu-id="87048-579">no</span><span class="sxs-lookup"><span data-stu-id="87048-579">no</span></span>           |
| <span data-ttu-id="87048-580">msdyn_msprojectdocument</span><span class="sxs-lookup"><span data-stu-id="87048-580">msdyn_msprojectdocument</span></span>                | <span data-ttu-id="87048-581">no</span><span class="sxs-lookup"><span data-stu-id="87048-581">no</span></span>             | <span data-ttu-id="87048-582">no</span><span class="sxs-lookup"><span data-stu-id="87048-582">no</span></span>           |
| <span data-ttu-id="87048-583">msdyn_msprojectdocumentname</span><span class="sxs-lookup"><span data-stu-id="87048-583">msdyn_msprojectdocumentname</span></span>            | <span data-ttu-id="87048-584">no</span><span class="sxs-lookup"><span data-stu-id="87048-584">no</span></span>             | <span data-ttu-id="87048-585">no</span><span class="sxs-lookup"><span data-stu-id="87048-585">no</span></span>           |
| <span data-ttu-id="87048-586">msdyn_plannedexpensecost</span><span class="sxs-lookup"><span data-stu-id="87048-586">msdyn_plannedexpensecost</span></span>               | <span data-ttu-id="87048-587">no</span><span class="sxs-lookup"><span data-stu-id="87048-587">no</span></span>             | <span data-ttu-id="87048-588">no</span><span class="sxs-lookup"><span data-stu-id="87048-588">no</span></span>           |
| <span data-ttu-id="87048-589">msdyn_plannedexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="87048-589">msdyn_plannedexpensecost_base</span></span>          | <span data-ttu-id="87048-590">no</span><span class="sxs-lookup"><span data-stu-id="87048-590">no</span></span>             | <span data-ttu-id="87048-591">no</span><span class="sxs-lookup"><span data-stu-id="87048-591">no</span></span>           |
| <span data-ttu-id="87048-592">msdyn_plannedlaborcost</span><span class="sxs-lookup"><span data-stu-id="87048-592">msdyn_plannedlaborcost</span></span>                 | <span data-ttu-id="87048-593">no</span><span class="sxs-lookup"><span data-stu-id="87048-593">no</span></span>             | <span data-ttu-id="87048-594">no</span><span class="sxs-lookup"><span data-stu-id="87048-594">no</span></span>           |
| <span data-ttu-id="87048-595">msdyn_plannedlaborcost_base</span><span class="sxs-lookup"><span data-stu-id="87048-595">msdyn_plannedlaborcost_base</span></span>            | <span data-ttu-id="87048-596">no</span><span class="sxs-lookup"><span data-stu-id="87048-596">no</span></span>             | <span data-ttu-id="87048-597">no</span><span class="sxs-lookup"><span data-stu-id="87048-597">no</span></span>           |
| <span data-ttu-id="87048-598">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="87048-598">msdyn_plannedsales</span></span>                     | <span data-ttu-id="87048-599">no</span><span class="sxs-lookup"><span data-stu-id="87048-599">no</span></span>             | <span data-ttu-id="87048-600">no</span><span class="sxs-lookup"><span data-stu-id="87048-600">no</span></span>           |
| <span data-ttu-id="87048-601">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="87048-601">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="87048-602">no</span><span class="sxs-lookup"><span data-stu-id="87048-602">no</span></span>             | <span data-ttu-id="87048-603">no</span><span class="sxs-lookup"><span data-stu-id="87048-603">no</span></span>           |
| <span data-ttu-id="87048-604">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="87048-604">msdyn_progress</span></span>                         | <span data-ttu-id="87048-605">no</span><span class="sxs-lookup"><span data-stu-id="87048-605">no</span></span>             | <span data-ttu-id="87048-606">no</span><span class="sxs-lookup"><span data-stu-id="87048-606">no</span></span>           |
| <span data-ttu-id="87048-607">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="87048-607">msdyn_remainingcost</span></span>                    | <span data-ttu-id="87048-608">no</span><span class="sxs-lookup"><span data-stu-id="87048-608">no</span></span>             | <span data-ttu-id="87048-609">no</span><span class="sxs-lookup"><span data-stu-id="87048-609">no</span></span>           |
| <span data-ttu-id="87048-610">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="87048-610">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="87048-611">no</span><span class="sxs-lookup"><span data-stu-id="87048-611">no</span></span>             | <span data-ttu-id="87048-612">no</span><span class="sxs-lookup"><span data-stu-id="87048-612">no</span></span>           |
| <span data-ttu-id="87048-613">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="87048-613">msdyn_remainingsales</span></span>                   | <span data-ttu-id="87048-614">no</span><span class="sxs-lookup"><span data-stu-id="87048-614">no</span></span>             | <span data-ttu-id="87048-615">no</span><span class="sxs-lookup"><span data-stu-id="87048-615">no</span></span>           |
| <span data-ttu-id="87048-616">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="87048-616">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="87048-617">no</span><span class="sxs-lookup"><span data-stu-id="87048-617">no</span></span>             | <span data-ttu-id="87048-618">no</span><span class="sxs-lookup"><span data-stu-id="87048-618">no</span></span>           |
| <span data-ttu-id="87048-619">msdyn_replaylogheader</span><span class="sxs-lookup"><span data-stu-id="87048-619">msdyn_replaylogheader</span></span>                  | <span data-ttu-id="87048-620">no</span><span class="sxs-lookup"><span data-stu-id="87048-620">no</span></span>             | <span data-ttu-id="87048-621">no</span><span class="sxs-lookup"><span data-stu-id="87048-621">no</span></span>           |
| <span data-ttu-id="87048-622">msdyn_salesconsumption</span><span class="sxs-lookup"><span data-stu-id="87048-622">msdyn_salesconsumption</span></span>                 | <span data-ttu-id="87048-623">no</span><span class="sxs-lookup"><span data-stu-id="87048-623">no</span></span>             | <span data-ttu-id="87048-624">no</span><span class="sxs-lookup"><span data-stu-id="87048-624">no</span></span>           |
| <span data-ttu-id="87048-625">msdyn_salesestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="87048-625">msdyn_salesestimateatcompleteeac</span></span>       | <span data-ttu-id="87048-626">no</span><span class="sxs-lookup"><span data-stu-id="87048-626">no</span></span>             | <span data-ttu-id="87048-627">no</span><span class="sxs-lookup"><span data-stu-id="87048-627">no</span></span>           |
| <span data-ttu-id="87048-628">msdyn_salesestimateatcompleteeac_base</span><span class="sxs-lookup"><span data-stu-id="87048-628">msdyn_salesestimateatcompleteeac_base</span></span>  | <span data-ttu-id="87048-629">no</span><span class="sxs-lookup"><span data-stu-id="87048-629">no</span></span>             | <span data-ttu-id="87048-630">no</span><span class="sxs-lookup"><span data-stu-id="87048-630">no</span></span>           |
| <span data-ttu-id="87048-631">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="87048-631">msdyn_salesvariance</span></span>                    | <span data-ttu-id="87048-632">no</span><span class="sxs-lookup"><span data-stu-id="87048-632">no</span></span>             | <span data-ttu-id="87048-633">no</span><span class="sxs-lookup"><span data-stu-id="87048-633">no</span></span>           |
| <span data-ttu-id="87048-634">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="87048-634">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="87048-635">no</span><span class="sxs-lookup"><span data-stu-id="87048-635">no</span></span>             | <span data-ttu-id="87048-636">no</span><span class="sxs-lookup"><span data-stu-id="87048-636">no</span></span>           |
| <span data-ttu-id="87048-637">msdyn_scheduleperformance</span><span class="sxs-lookup"><span data-stu-id="87048-637">msdyn_scheduleperformance</span></span>              | <span data-ttu-id="87048-638">no</span><span class="sxs-lookup"><span data-stu-id="87048-638">no</span></span>             | <span data-ttu-id="87048-639">no</span><span class="sxs-lookup"><span data-stu-id="87048-639">no</span></span>           |
| <span data-ttu-id="87048-640">msdyn_scheduleperformancename</span><span class="sxs-lookup"><span data-stu-id="87048-640">msdyn_scheduleperformancename</span></span>          | <span data-ttu-id="87048-641">no</span><span class="sxs-lookup"><span data-stu-id="87048-641">no</span></span>             | <span data-ttu-id="87048-642">no</span><span class="sxs-lookup"><span data-stu-id="87048-642">no</span></span>           |
| <span data-ttu-id="87048-643">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="87048-643">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="87048-644">no</span><span class="sxs-lookup"><span data-stu-id="87048-644">no</span></span>             | <span data-ttu-id="87048-645">no</span><span class="sxs-lookup"><span data-stu-id="87048-645">no</span></span>           |
| <span data-ttu-id="87048-646">msdyn_taskearlieststart</span><span class="sxs-lookup"><span data-stu-id="87048-646">msdyn_taskearlieststart</span></span>                | <span data-ttu-id="87048-647">no</span><span class="sxs-lookup"><span data-stu-id="87048-647">no</span></span>             | <span data-ttu-id="87048-648">no</span><span class="sxs-lookup"><span data-stu-id="87048-648">no</span></span>           |
| <span data-ttu-id="87048-649">msdyn_teamsize</span><span class="sxs-lookup"><span data-stu-id="87048-649">msdyn_teamsize</span></span>                         | <span data-ttu-id="87048-650">no</span><span class="sxs-lookup"><span data-stu-id="87048-650">no</span></span>             | <span data-ttu-id="87048-651">no</span><span class="sxs-lookup"><span data-stu-id="87048-651">no</span></span>           |
| <span data-ttu-id="87048-652">msdyn_teamsize_date</span><span class="sxs-lookup"><span data-stu-id="87048-652">msdyn_teamsize_date</span></span>                    | <span data-ttu-id="87048-653">no</span><span class="sxs-lookup"><span data-stu-id="87048-653">no</span></span>             | <span data-ttu-id="87048-654">no</span><span class="sxs-lookup"><span data-stu-id="87048-654">no</span></span>           |
| <span data-ttu-id="87048-655">msdyn_teamsize_state</span><span class="sxs-lookup"><span data-stu-id="87048-655">msdyn_teamsize_state</span></span>                   | <span data-ttu-id="87048-656">no</span><span class="sxs-lookup"><span data-stu-id="87048-656">no</span></span>             | <span data-ttu-id="87048-657">no</span><span class="sxs-lookup"><span data-stu-id="87048-657">no</span></span>           |
| <span data-ttu-id="87048-658">msdyn_totalactualcost</span><span class="sxs-lookup"><span data-stu-id="87048-658">msdyn_totalactualcost</span></span>                  | <span data-ttu-id="87048-659">no</span><span class="sxs-lookup"><span data-stu-id="87048-659">no</span></span>             | <span data-ttu-id="87048-660">no</span><span class="sxs-lookup"><span data-stu-id="87048-660">no</span></span>           |
| <span data-ttu-id="87048-661">msdyn_totalactualcost_base</span><span class="sxs-lookup"><span data-stu-id="87048-661">msdyn_totalactualcost_base</span></span>             | <span data-ttu-id="87048-662">no</span><span class="sxs-lookup"><span data-stu-id="87048-662">no</span></span>             | <span data-ttu-id="87048-663">no</span><span class="sxs-lookup"><span data-stu-id="87048-663">no</span></span>           |
| <span data-ttu-id="87048-664">msdyn_totalplannedcost</span><span class="sxs-lookup"><span data-stu-id="87048-664">msdyn_totalplannedcost</span></span>                 | <span data-ttu-id="87048-665">no</span><span class="sxs-lookup"><span data-stu-id="87048-665">no</span></span>             | <span data-ttu-id="87048-666">no</span><span class="sxs-lookup"><span data-stu-id="87048-666">no</span></span>           |
| <span data-ttu-id="87048-667">msdyn_totalplannedcost_base</span><span class="sxs-lookup"><span data-stu-id="87048-667">msdyn_totalplannedcost_base</span></span>            | <span data-ttu-id="87048-668">no</span><span class="sxs-lookup"><span data-stu-id="87048-668">no</span></span>             | <span data-ttu-id="87048-669">no</span><span class="sxs-lookup"><span data-stu-id="87048-669">no</span></span>           |


## <a name="limitations-and-known-issues"></a><span data-ttu-id="87048-670">Limitacions i problemes coneguts</span><span class="sxs-lookup"><span data-stu-id="87048-670">Limitations and known issues</span></span>
<span data-ttu-id="87048-671">A continuació es mostra una llista de limitacions i problemes coneguts:</span><span class="sxs-lookup"><span data-stu-id="87048-671">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="87048-672">Només poden utilitzar les API de Planificació els **Usuaris amb llicència del Microsoft Project**.</span><span class="sxs-lookup"><span data-stu-id="87048-672">Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="87048-673">No les poden utilitzar:</span><span class="sxs-lookup"><span data-stu-id="87048-673">They can't be used by:</span></span>
    - <span data-ttu-id="87048-674">Usuaris de l'aplicació</span><span class="sxs-lookup"><span data-stu-id="87048-674">Application users</span></span>
    - <span data-ttu-id="87048-675">Usuaris del sistema</span><span class="sxs-lookup"><span data-stu-id="87048-675">System users</span></span>
    - <span data-ttu-id="87048-676">Usuaris d'integració</span><span class="sxs-lookup"><span data-stu-id="87048-676">Integration users</span></span>
    - <span data-ttu-id="87048-677">Altres usuaris que no tenen la llicència necessària</span><span class="sxs-lookup"><span data-stu-id="87048-677">Other users that don't have the required license</span></span>
- <span data-ttu-id="87048-678">Cada **OperationSet** només pot tenir un màxim de 100 operacions.</span><span class="sxs-lookup"><span data-stu-id="87048-678">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="87048-679">Cada usuari només pot tenir un màxim de 10 **OperationSets** oberts.</span><span class="sxs-lookup"><span data-stu-id="87048-679">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="87048-680">El Project Operations actualment admet un màxim de 500 tasques totals en un projecte.</span><span class="sxs-lookup"><span data-stu-id="87048-680">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="87048-681">Actualment no hi ha estats d'error i registres d'error d'**OperationSet** disponibles.</span><span class="sxs-lookup"><span data-stu-id="87048-681">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- [<span data-ttu-id="87048-682">Límits dels projectes i tasques</span><span class="sxs-lookup"><span data-stu-id="87048-682">Limits and boundaries on projects and tasks</span></span>](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a><span data-ttu-id="87048-683">Gestió d'errors</span><span class="sxs-lookup"><span data-stu-id="87048-683">Error handling</span></span>

   - <span data-ttu-id="87048-684">Per revisar els errors generats a partir dels conjunts d'operacions, aneu a **Configuració** \> **Integració de la planificació** \> **Conjunts d'operacions**.</span><span class="sxs-lookup"><span data-stu-id="87048-684">To review errors generated from the Operation Sets, go to **Settings** \> **Schedule Integration** \> **Operations Sets**.</span></span>
   - <span data-ttu-id="87048-685">Per revisar els errors generats a partir del servei de planificació del projecte, aneu a **Configuració** \> **Integració de la planificació** \> **Registres d'error de PSS**.</span><span class="sxs-lookup"><span data-stu-id="87048-685">To review errors generated from the Project Scheduling Service, go to **Settings** \> **Schedule Integration** \> **PSS Error Logs**.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="87048-686">Escenari d'exemple</span><span class="sxs-lookup"><span data-stu-id="87048-686">Sample scenario</span></span>

<span data-ttu-id="87048-687">En aquest escenari, creareu un projecte, un membre de l'equip, quatre tasques i dues assignacions de recursos.</span><span class="sxs-lookup"><span data-stu-id="87048-687">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="87048-688">A continuació, actualitzareu una tasca, actualitzareu el projecte, suprimireu una tasca, suprimireu una assignació de recursos i creareu una dependència de tasca.</span><span class="sxs-lookup"><span data-stu-id="87048-688">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

```csharp
Entity project = CreateProject();
project.Id = CallCreateProjectAction(project);
var projectReference = project.ToEntityReference();

var teamMember = new Entity("msdyn_projectteam", Guid.NewGuid());
teamMember["msdyn_name"] = $"TM {DateTime.Now.ToShortTimeString()}";
teamMember["msdyn_project"] = projectReference;
var createTeamMemberResponse = CallCreateTeamMemberAction(teamMember);

var description = $"My demo {DateTime.Now.ToShortTimeString()}";
var operationSetId = CallCreateOperationSetAction(project.Id, description);

var task1 = GetTask("1WW", projectReference);
var task2 = GetTask("2XX", projectReference, task1.ToEntityReference());
var task3 = GetTask("3YY", projectReference);
var task4 = GetTask("4ZZ", projectReference);

var assignment1 = GetResourceAssignment("R1", teamMember, task2, project);
var assignment2 = GetResourceAssignment("R2", teamMember, task3, project);

var task1Response = CallPssCreateAction(task1, operationSetId);
var task2Response = CallPssCreateAction(task2, operationSetId);
var task3Response = CallPssCreateAction(task3, operationSetId);
var task4Response = CallPssCreateAction(task4, operationSetId);

var assignment1Response = CallPssCreateAction(assignment1, operationSetId);
var assignment2Response = CallPssCreateAction(assignment2, operationSetId);

task2["msdyn_subject"] = "Updated Task";
var task2UpdateResponse = CallPssUpdateAction(task2, operationSetId);

project["msdyn_subject"] = $"Proj update {DateTime.Now.ToShortTimeString()}";
var projectUpdateResponse = CallPssUpdateAction(project, operationSetId);

var task4DeleteResponse = CallPssDeleteAction(task4.Id.ToString(), task4.LogicalName, operationSetId);

var assignment2DeleteResponse = CallPssDeleteAction(assignment2.Id.ToString(), assignment2.LogicalName, operationSetId);

var dependency1 = GetTaskDependency(project, task2, task3);
var dependency1Response = CallPssCreateAction(dependency1, operationSetId);

CallExecuteOperationSetAction(operationSetId);
Console.WriteLine("Done....");
```

## <a name="additional-samples"></a><span data-ttu-id="87048-689">Exemples addicionals</span><span class="sxs-lookup"><span data-stu-id="87048-689">Additional samples</span></span>

```csharp
#region Call actions --- Sample code ----

/// <summary>
/// Calls the action to create an operationSet
/// </summary>
/// <param name="projectId">project id for the operations to be included in this operationSet</param>
/// <param name="description">description of this operationSet</param>
/// <returns>operationSet id</returns>
private string CallCreateOperationSetAction(Guid projectId, string description)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_CreateOperationSetV1");
    operationSetRequest["ProjectId"] = projectId.ToString();
    operationSetRequest["Description"] = description;
    OrganizationResponse response = organizationService.Execute(operationSetRequest);
    return response["OperationSetId"].ToString();
}

/// <summary>
/// Calls the action to create an entity, only Task and Resource Assignment for now
/// </summary>
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>

private OperationSetResponse CallPssCreateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssCreateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task for now
/// </summary>
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssUpdateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssUpdateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task and Resource Assignment for now
/// </summary>
/// <param name="recordId">Id of the record to be deleted</param>
/// <param name="entityLogicalName">Entity logical name of the record</param>
/// <param name="operationSetId">OperationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssDeleteAction(string recordId, string entityLogicalName, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssDeleteV1");
    operationSetRequest["RecordId"] = recordId;
    operationSetRequest["EntityLogicalName"] = entityLogicalName;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to execute requests in an operationSet
/// </summary>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallExecuteOperationSetAction(string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_ExecuteOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// This can be used to abandon an operationSet that is no longer needed
/// </summary>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
protected OperationSetResponse CallAbandonOperationSetAction(Guid operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_AbandonOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId.ToString();
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}


/// <summary>
/// Calls the action to create a new project
/// </summary>
/// <param name="project">Project</param>
/// <returns>project Id</returns>
private Guid CallCreateProjectAction(Entity project)
{
    OrganizationRequest createProjectRequest = new OrganizationRequest("msdyn_CreateProjectV1");
    createProjectRequest["Project"] = project;
    OrganizationResponse response = organizationService.Execute(createProjectRequest);
    var projectId = Guid.Parse((string)response["ProjectId"]);
    return projectId;
}

/// <summary>
/// Calls the action to create a new project team member
/// </summary>
/// <param name="teamMember">Project team member</param>
/// <returns>project team member Id</returns>
private string CallCreateTeamMemberAction(Entity teamMember)
{
    OrganizationRequest request = new OrganizationRequest("msdyn_CreateTeamMemberV1");
    request["TeamMember"] = teamMember;
    OrganizationResponse response = organizationService.Execute(request);
    return (string)response["TeamMemberId"];
}

private OperationSetResponse GetOperationSetResponseFromOrgResponse(OrganizationResponse orgResponse)
{
    return JsonConvert.DeserializeObject<OperationSetResponse>((string)orgResponse.Results["OperationSetResponse"]);
}

private EntityCollection GetDefaultBucket(EntityReference projectReference)
{
    var columnsToFetch = new ColumnSet("msdyn_project", "msdyn_name");
    var getDefaultBucket = new QueryExpression("msdyn_projectbucket")
    {
        ColumnSet = columnsToFetch,
        Criteria =
        {
            Conditions =
            {
                new ConditionExpression("msdyn_project", ConditionOperator.Equal, projectReference.Id),
                new ConditionExpression("msdyn_name", ConditionOperator.Equal, "Bucket 1")
            }
        }
    };

    return organizationService.RetrieveMultiple(getDefaultBucket);
}

private Entity GetBucket(EntityReference projectReference)
{
    var bucketCollection = GetDefaultBucket(projectReference);
    if (bucketCollection.Entities.Count > 0)
    {
        return bucketCollection[0].ToEntity<Entity>();
    }

    throw new Exception($"Please open project with id {projectReference.Id} in the Dynamics UI and navigate to the Tasks tab");
}

private Entity CreateProject()
{
    var project = new Entity("msdyn_project", Guid.NewGuid());
    project["msdyn_subject"] = $"Proj {DateTime.Now.ToShortTimeString()}";

    return project;
}



private Entity GetTask(string name, EntityReference projectReference, EntityReference parentReference = null)
{
    var task = new Entity("msdyn_projecttask", Guid.NewGuid());
    task["msdyn_project"] = projectReference;
    task["msdyn_subject"] = name;
    task["msdyn_effort"] = 4d;
    task["msdyn_scheduledstart"] = DateTime.Today;
    task["msdyn_scheduledend"] = DateTime.Today.AddDays(5);
    task["msdyn_progress"] = 0.34m;
    task["msdyn_start"] = DateTime.Now.AddDays(1);
    task["msdyn_projectbucket"] = GetBucket(projectReference).ToEntityReference();
    task["msdyn_LinkStatus"] = new OptionSetValue(192350000);

    //Custom field handling
    /*
    task["new_custom1"] = "Just my test";
    task["new_age"] = 98;
    task["new_amount"] = 591.34m;
    task["new_isready"] = new OptionSetValue(100000000);
    */

    if (parentReference == null)
    {
        task["msdyn_outlinelevel"] = 1;
    }
    else
    {
        task["msdyn_parenttask"] = parentReference;
    }

    return task;
}

private Entity GetResourceAssignment(string name, Entity teamMember, Entity task, Entity project)
{
    var assignment = new Entity("msdyn_resourceassignment", Guid.NewGuid());
    assignment["msdyn_projectteamid"] = teamMember.ToEntityReference();
    assignment["msdyn_taskid"] = task.ToEntityReference();
    assignment["msdyn_projectid"] = project.ToEntityReference();
    assignment["msdyn_name"] = name;
    assignment["msdyn_start"] = DateTime.Now;
    assignment["msdyn_finish"] = DateTime.Now;

    return assignment;
}

protected Entity GetTaskDependency(Entity project, Entity predecessor, Entity successor)
{
    var taskDependency = new Entity("msdyn_projecttaskdependency", Guid.NewGuid());
    taskDependency["msdyn_project"] = project.ToEntityReference();
    taskDependency["msdyn_predecessortask"] = predecessor.ToEntityReference();
    taskDependency["msdyn_successortask"] = successor.ToEntityReference();
    taskDependency["msdyn_linktype"] = new OptionSetValue(192350000);

    return taskDependency;
}

#endregion


#region OperationSetResponse DataContract --- Sample code ----

[DataContract]
public class OperationSetResponse
{
[DataMember(Name = "operationSetId")]
public Guid OperationSetId { get; set; }

[DataMember(Name = "operationSetDetailId")]
public Guid OperationSetDetailId { get; set; }

[DataMember(Name = "operationType")]
public string OperationType { get; set; }

[DataMember(Name = "recordId")]
public string RecordId { get; set; }

[DataMember(Name = "correlationId")]
public string CorrelationId { get; set; }
}

#endregion
```
