---
title: Ús de les API de planificació per realitzar operacions amb entitats de Planificació
description: En aquest tema es proporciona informació i exemples per utilitzar les API de Planificació.
author: sigitac
manager: Annbe
ms.date: 04/27/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e03f4e6c49a835206b23cade3fabe3fd26693441
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950792"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="61cbc-103">Ús de les API de planificació per realitzar operacions amb entitats de Planificació</span><span class="sxs-lookup"><span data-stu-id="61cbc-103">Use Schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="61cbc-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_</span><span class="sxs-lookup"><span data-stu-id="61cbc-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="61cbc-105">Algunes de les funcionalitats que s'indiquen en aquest tema estan disponibles com a part d'una versió preliminar.</span><span class="sxs-lookup"><span data-stu-id="61cbc-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="61cbc-106">El contingut i la funcionalitat estan subjectes a canvis.</span><span class="sxs-lookup"><span data-stu-id="61cbc-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="61cbc-107">Entitats de planificació</span><span class="sxs-lookup"><span data-stu-id="61cbc-107">Scheduling entities</span></span>

<span data-ttu-id="61cbc-108">Les API de Planificació proporcionen la capacitat de crear, actualitzar i suprimir operacions amb **Entitats de planificació**.</span><span class="sxs-lookup"><span data-stu-id="61cbc-108">Schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="61cbc-109">Aquestes entitats s'administren mitjançant el motor de Planificació del Projecte for the web.</span><span class="sxs-lookup"><span data-stu-id="61cbc-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="61cbc-110">Les operacions de creació, actualització i supressió amb **Entitats de planificació** es van restringir a les versions anteriors del Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="61cbc-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="61cbc-111">La taula següent proporciona una llista completa de les **Entitats de planificació**.</span><span class="sxs-lookup"><span data-stu-id="61cbc-111">The following table provides a full list of the **Scheduling entities**.</span></span>

| <span data-ttu-id="61cbc-112">Nom de l’entitat</span><span class="sxs-lookup"><span data-stu-id="61cbc-112">Entity name</span></span>  | <span data-ttu-id="61cbc-113">Nom lògic de l’entitat</span><span class="sxs-lookup"><span data-stu-id="61cbc-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="61cbc-114">Project</span><span class="sxs-lookup"><span data-stu-id="61cbc-114">Project</span></span> | <span data-ttu-id="61cbc-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="61cbc-115">msdyn_project</span></span> |
| <span data-ttu-id="61cbc-116">Tasca del projecte</span><span class="sxs-lookup"><span data-stu-id="61cbc-116">Project Task</span></span>  | <span data-ttu-id="61cbc-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="61cbc-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="61cbc-118">Dependència de les tasques del projecte</span><span class="sxs-lookup"><span data-stu-id="61cbc-118">Project Task Dependency</span></span>  | <span data-ttu-id="61cbc-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="61cbc-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="61cbc-120">Assignació de recursos</span><span class="sxs-lookup"><span data-stu-id="61cbc-120">Resource Assignment</span></span> | <span data-ttu-id="61cbc-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="61cbc-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="61cbc-122">Dipòsit de projecte</span><span class="sxs-lookup"><span data-stu-id="61cbc-122">Project Bucket</span></span>  | <span data-ttu-id="61cbc-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="61cbc-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="61cbc-124">Membre de l'equip del projecte</span><span class="sxs-lookup"><span data-stu-id="61cbc-124">Project Team Member</span></span> | <span data-ttu-id="61cbc-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="61cbc-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="61cbc-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="61cbc-126">OperationSet</span></span>

<span data-ttu-id="61cbc-127">OperationSet és un patró d'unitat de treball que es pot utilitzar quan diverses sol·licituds que afecten la planificació s'han de processar dins d'una transacció.</span><span class="sxs-lookup"><span data-stu-id="61cbc-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="schedule-apis"></a><span data-ttu-id="61cbc-128">API de Planificació</span><span class="sxs-lookup"><span data-stu-id="61cbc-128">Schedule APIs</span></span>

<span data-ttu-id="61cbc-129">A continuació es mostra una llista de les API de Planificació actuals.</span><span class="sxs-lookup"><span data-stu-id="61cbc-129">The following is a list of current Schedule APIs.</span></span>

- <span data-ttu-id="61cbc-130">**msdyn_CreateProjectV1**: aquesta API es pot utilitzar per crear un projecte.</span><span class="sxs-lookup"><span data-stu-id="61cbc-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="61cbc-131">El projecte i el dipòsit per defecte del projecte es creen immediatament.</span><span class="sxs-lookup"><span data-stu-id="61cbc-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="61cbc-132">**msdyn_CreateTeamMemberV1**: aquesta API es pot utilitzar per crear un membre de l'equip del projecte.</span><span class="sxs-lookup"><span data-stu-id="61cbc-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="61cbc-133">El registre del membre de l'equip es crea immediatament.</span><span class="sxs-lookup"><span data-stu-id="61cbc-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="61cbc-134">**msdyn_CreateOperationSetV1**: aquesta API es pot utilitzar per planificar diverses sol·licituds que s'han de fer dins d'una transacció.</span><span class="sxs-lookup"><span data-stu-id="61cbc-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="61cbc-135">**msdyn_PSSCreateV1**: aquesta API es pot utilitzar per crear una entitat.</span><span class="sxs-lookup"><span data-stu-id="61cbc-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="61cbc-136">L'entitat pot ser qualsevol de les entitats de Planificació que admeten l'operació de creació.</span><span class="sxs-lookup"><span data-stu-id="61cbc-136">The entity can be any of the Scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="61cbc-137">**msdyn_PSSUpdateV1**: aquesta API es pot utilitzar per actualitzar una entitat.</span><span class="sxs-lookup"><span data-stu-id="61cbc-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="61cbc-138">L'entitat pot ser qualsevol de les entitats de Planificació que admeten l'operació d'actualització.</span><span class="sxs-lookup"><span data-stu-id="61cbc-138">The entity can be any of the Scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="61cbc-139">**msdyn_PSSDeleteV1**: aquesta API es pot utilitzar per suprimir una entitat.</span><span class="sxs-lookup"><span data-stu-id="61cbc-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="61cbc-140">L'entitat pot ser qualsevol de les entitats de Planificació que admeten l'operació de supressió.</span><span class="sxs-lookup"><span data-stu-id="61cbc-140">The entity can be any of the Scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="61cbc-141">**msdyn_ExecuteOperationSetV1**: aquesta API s'utilitza per executar totes les operacions dins del conjunt d'operacions determinat.</span><span class="sxs-lookup"><span data-stu-id="61cbc-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-schedule-apis-with-operationset"></a><span data-ttu-id="61cbc-142">Ús de les API de Planificació amb OperationSet</span><span class="sxs-lookup"><span data-stu-id="61cbc-142">Using Schedule APIs with OperationSet</span></span>

<span data-ttu-id="61cbc-143">Com que els registres amb **CreateProjectV1** i **CreateTeamMemberV1** es creen immediatament, aquestes API no es poden utilitzar directament a **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="61cbc-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="61cbc-144">Tanmateix, podeu utilitzar l'API per crear els registres necessaris, crear un **OperationSet** i, a continuació, utilitzar aquests registres creats a **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="61cbc-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="61cbc-145">Operacions admeses</span><span class="sxs-lookup"><span data-stu-id="61cbc-145">Supported operations</span></span>

| <span data-ttu-id="61cbc-146">Entitat de planificació</span><span class="sxs-lookup"><span data-stu-id="61cbc-146">Scheduling entity</span></span> | <span data-ttu-id="61cbc-147">Creació</span><span class="sxs-lookup"><span data-stu-id="61cbc-147">Create</span></span> | <span data-ttu-id="61cbc-148">Actualització</span><span class="sxs-lookup"><span data-stu-id="61cbc-148">Update</span></span> | <span data-ttu-id="61cbc-149">Delete</span><span class="sxs-lookup"><span data-stu-id="61cbc-149">Delete</span></span> | <span data-ttu-id="61cbc-150">Consideracions importants</span><span class="sxs-lookup"><span data-stu-id="61cbc-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="61cbc-151">Tasca del projecte</span><span class="sxs-lookup"><span data-stu-id="61cbc-151">Project task</span></span> | <span data-ttu-id="61cbc-152">Sí</span><span class="sxs-lookup"><span data-stu-id="61cbc-152">Yes</span></span> | <span data-ttu-id="61cbc-153">Sí</span><span class="sxs-lookup"><span data-stu-id="61cbc-153">Yes</span></span> | <span data-ttu-id="61cbc-154">Sí</span><span class="sxs-lookup"><span data-stu-id="61cbc-154">Yes</span></span> | <span data-ttu-id="61cbc-155">Cap</span><span class="sxs-lookup"><span data-stu-id="61cbc-155">None</span></span> |
| <span data-ttu-id="61cbc-156">Dependència de les tasques del projecte</span><span class="sxs-lookup"><span data-stu-id="61cbc-156">Project task dependency</span></span> | <span data-ttu-id="61cbc-157">Sí</span><span class="sxs-lookup"><span data-stu-id="61cbc-157">Yes</span></span> | <span data-ttu-id="61cbc-158">Sí</span><span class="sxs-lookup"><span data-stu-id="61cbc-158">Yes</span></span> | | <span data-ttu-id="61cbc-159">Els registres de dependència de les tasques del projecte no s'actualitzen.</span><span class="sxs-lookup"><span data-stu-id="61cbc-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="61cbc-160">En lloc d'això, es pot suprimir un registre antic i crear-ne un de nou.</span><span class="sxs-lookup"><span data-stu-id="61cbc-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="61cbc-161">Assignació de recursos</span><span class="sxs-lookup"><span data-stu-id="61cbc-161">Resource assignment</span></span> | <span data-ttu-id="61cbc-162">Sí</span><span class="sxs-lookup"><span data-stu-id="61cbc-162">Yes</span></span> | <span data-ttu-id="61cbc-163">Sí</span><span class="sxs-lookup"><span data-stu-id="61cbc-163">Yes</span></span> | | <span data-ttu-id="61cbc-164">No s'admeten les operacions amb els camps següents: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** i **PlannedWork**.</span><span class="sxs-lookup"><span data-stu-id="61cbc-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="61cbc-165">Els registres d'assignació de recursos no s'actualitzen.</span><span class="sxs-lookup"><span data-stu-id="61cbc-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="61cbc-166">En lloc d'això, es pot suprimir el registre antic i crear-ne un de nou.</span><span class="sxs-lookup"><span data-stu-id="61cbc-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="61cbc-167">Dipòsit de projecte</span><span class="sxs-lookup"><span data-stu-id="61cbc-167">Project bucket</span></span> | <span data-ttu-id="61cbc-168">N/D</span><span class="sxs-lookup"><span data-stu-id="61cbc-168">N/A</span></span> | <span data-ttu-id="61cbc-169">N/D</span><span class="sxs-lookup"><span data-stu-id="61cbc-169">N/A</span></span> | <span data-ttu-id="61cbc-170">N/D</span><span class="sxs-lookup"><span data-stu-id="61cbc-170">N/A</span></span> | <span data-ttu-id="61cbc-171">El dipòsit per defecte es crea amb l'API **CreateProjectV1**.</span><span class="sxs-lookup"><span data-stu-id="61cbc-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="61cbc-172">Membre de l'equip del projecte</span><span class="sxs-lookup"><span data-stu-id="61cbc-172">Project team member</span></span> | <span data-ttu-id="61cbc-173">Sí</span><span class="sxs-lookup"><span data-stu-id="61cbc-173">Yes</span></span> | <span data-ttu-id="61cbc-174">Sí</span><span class="sxs-lookup"><span data-stu-id="61cbc-174">Yes</span></span> | <span data-ttu-id="61cbc-175">Sí</span><span class="sxs-lookup"><span data-stu-id="61cbc-175">Yes</span></span> | <span data-ttu-id="61cbc-176">Per a l'operació de creació, utilitzeu l'API **CreateTeamMemberV1**.</span><span class="sxs-lookup"><span data-stu-id="61cbc-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="61cbc-177">Project</span><span class="sxs-lookup"><span data-stu-id="61cbc-177">Project</span></span> | <span data-ttu-id="61cbc-178">Sí</span><span class="sxs-lookup"><span data-stu-id="61cbc-178">Yes</span></span> | <span data-ttu-id="61cbc-179">Sí</span><span class="sxs-lookup"><span data-stu-id="61cbc-179">Yes</span></span> | <span data-ttu-id="61cbc-180">N/D</span><span class="sxs-lookup"><span data-stu-id="61cbc-180">N/A</span></span> | <span data-ttu-id="61cbc-181">Les operacions amb els camps següents no estan admeses: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** i **Duration**.</span><span class="sxs-lookup"><span data-stu-id="61cbc-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="61cbc-182">Aquestes API es poden cridar amb objectes d'entitat que inclouen camps personalitzats.</span><span class="sxs-lookup"><span data-stu-id="61cbc-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="61cbc-183">La propietat ID és opcional.</span><span class="sxs-lookup"><span data-stu-id="61cbc-183">The ID property is optional.</span></span> <span data-ttu-id="61cbc-184">Si es proporciona, el sistema intenta utilitzar-la i llança una excepció si no es pot utilitzar.</span><span class="sxs-lookup"><span data-stu-id="61cbc-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="61cbc-185">Si no es proporciona, el sistema la generarà.</span><span class="sxs-lookup"><span data-stu-id="61cbc-185">If it isn't provided, the system will generate it.</span></span>

## <a name="restricted-fields"></a><span data-ttu-id="61cbc-186">Camps restringits</span><span class="sxs-lookup"><span data-stu-id="61cbc-186">Restricted fields</span></span>

<span data-ttu-id="61cbc-187">Les taules següents defineixen els camps restringits de **Crear** i **Editar.**</span><span class="sxs-lookup"><span data-stu-id="61cbc-187">The following tables define the fields that are restricted from **Create** and **Edit.**</span></span>

### <a name="project-task"></a><span data-ttu-id="61cbc-188">Tasca del projecte</span><span class="sxs-lookup"><span data-stu-id="61cbc-188">Project task</span></span>

| <span data-ttu-id="61cbc-189">**Nom lògic**</span><span class="sxs-lookup"><span data-stu-id="61cbc-189">**Logical name**</span></span>                       | <span data-ttu-id="61cbc-190">**Pot crear**</span><span class="sxs-lookup"><span data-stu-id="61cbc-190">**Can create**</span></span> | <span data-ttu-id="61cbc-191">**Pot editar**</span><span class="sxs-lookup"><span data-stu-id="61cbc-191">**Can edit**</span></span>     |
|----------------------------------------|----------------|------------------|
| <span data-ttu-id="61cbc-192">msdyn_actualcost</span><span class="sxs-lookup"><span data-stu-id="61cbc-192">msdyn_actualcost</span></span>                       | <span data-ttu-id="61cbc-193">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-193">no</span></span>             | <span data-ttu-id="61cbc-194">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-194">no</span></span>               |
| <span data-ttu-id="61cbc-195">msdyn_actualcost_base</span><span class="sxs-lookup"><span data-stu-id="61cbc-195">msdyn_actualcost_base</span></span>                  | <span data-ttu-id="61cbc-196">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-196">no</span></span>             | <span data-ttu-id="61cbc-197">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-197">no</span></span>               |
| <span data-ttu-id="61cbc-198">msdyn_actualend</span><span class="sxs-lookup"><span data-stu-id="61cbc-198">msdyn_actualend</span></span>                        | <span data-ttu-id="61cbc-199">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-199">no</span></span>             | <span data-ttu-id="61cbc-200">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-200">no</span></span>               |
| <span data-ttu-id="61cbc-201">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="61cbc-201">msdyn_actualsales</span></span>                      | <span data-ttu-id="61cbc-202">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-202">no</span></span>             | <span data-ttu-id="61cbc-203">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-203">no</span></span>               |
| <span data-ttu-id="61cbc-204">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="61cbc-204">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="61cbc-205">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-205">no</span></span>             | <span data-ttu-id="61cbc-206">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-206">no</span></span>               |
| <span data-ttu-id="61cbc-207">msdyn_actualstart</span><span class="sxs-lookup"><span data-stu-id="61cbc-207">msdyn_actualstart</span></span>                      | <span data-ttu-id="61cbc-208">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-208">no</span></span>             | <span data-ttu-id="61cbc-209">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-209">no</span></span>               |
| <span data-ttu-id="61cbc-210">msdyn_costatcompleteestimate</span><span class="sxs-lookup"><span data-stu-id="61cbc-210">msdyn_costatcompleteestimate</span></span>           | <span data-ttu-id="61cbc-211">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-211">no</span></span>             | <span data-ttu-id="61cbc-212">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-212">no</span></span>               |
| <span data-ttu-id="61cbc-213">msdyn_costatcompleteestimate_base</span><span class="sxs-lookup"><span data-stu-id="61cbc-213">msdyn_costatcompleteestimate_base</span></span>      | <span data-ttu-id="61cbc-214">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-214">no</span></span>             | <span data-ttu-id="61cbc-215">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-215">no</span></span>               |
| <span data-ttu-id="61cbc-216">msdyn_costconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="61cbc-216">msdyn_costconsumptionpercentage</span></span>        | <span data-ttu-id="61cbc-217">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-217">no</span></span>             | <span data-ttu-id="61cbc-218">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-218">no</span></span>               |
| <span data-ttu-id="61cbc-219">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="61cbc-219">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="61cbc-220">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-220">no</span></span>             | <span data-ttu-id="61cbc-221">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-221">no</span></span>               |
| <span data-ttu-id="61cbc-222">msdyn_effortestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="61cbc-222">msdyn_effortestimateatcomplete</span></span>         | <span data-ttu-id="61cbc-223">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-223">no</span></span>             | <span data-ttu-id="61cbc-224">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-224">no</span></span>               |
| <span data-ttu-id="61cbc-225">msdyn_iscritical</span><span class="sxs-lookup"><span data-stu-id="61cbc-225">msdyn_iscritical</span></span>                       | <span data-ttu-id="61cbc-226">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-226">no</span></span>             | <span data-ttu-id="61cbc-227">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-227">no</span></span>               |
| <span data-ttu-id="61cbc-228">msdyn_iscriticalname</span><span class="sxs-lookup"><span data-stu-id="61cbc-228">msdyn_iscriticalname</span></span>                   | <span data-ttu-id="61cbc-229">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-229">no</span></span>             | <span data-ttu-id="61cbc-230">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-230">no</span></span>               |
| <span data-ttu-id="61cbc-231">msdyn_ismanual</span><span class="sxs-lookup"><span data-stu-id="61cbc-231">msdyn_ismanual</span></span>                         | <span data-ttu-id="61cbc-232">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-232">no</span></span>             | <span data-ttu-id="61cbc-233">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-233">no</span></span>               |
| <span data-ttu-id="61cbc-234">msdyn_ismanualname</span><span class="sxs-lookup"><span data-stu-id="61cbc-234">msdyn_ismanualname</span></span>                     | <span data-ttu-id="61cbc-235">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-235">no</span></span>             | <span data-ttu-id="61cbc-236">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-236">no</span></span>               |
| <span data-ttu-id="61cbc-237">msdyn_ismilestone</span><span class="sxs-lookup"><span data-stu-id="61cbc-237">msdyn_ismilestone</span></span>                      | <span data-ttu-id="61cbc-238">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-238">no</span></span>             | <span data-ttu-id="61cbc-239">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-239">no</span></span>               |
| <span data-ttu-id="61cbc-240">msdyn_ismilestonename</span><span class="sxs-lookup"><span data-stu-id="61cbc-240">msdyn_ismilestonename</span></span>                  | <span data-ttu-id="61cbc-241">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-241">no</span></span>             | <span data-ttu-id="61cbc-242">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-242">no</span></span>               |
| <span data-ttu-id="61cbc-243">msdyn_LinkStatus</span><span class="sxs-lookup"><span data-stu-id="61cbc-243">msdyn_LinkStatus</span></span>                       | <span data-ttu-id="61cbc-244">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-244">no</span></span>             | <span data-ttu-id="61cbc-245">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-245">no</span></span>               |
| <span data-ttu-id="61cbc-246">msdyn_linkstatusname</span><span class="sxs-lookup"><span data-stu-id="61cbc-246">msdyn_linkstatusname</span></span>                   | <span data-ttu-id="61cbc-247">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-247">no</span></span>             | <span data-ttu-id="61cbc-248">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-248">no</span></span>               |
| <span data-ttu-id="61cbc-249">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="61cbc-249">msdyn_msprojectclientid</span></span>                | <span data-ttu-id="61cbc-250">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-250">no</span></span>             | <span data-ttu-id="61cbc-251">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-251">no</span></span>               |
| <span data-ttu-id="61cbc-252">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="61cbc-252">msdyn_plannedcost</span></span>                      | <span data-ttu-id="61cbc-253">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-253">no</span></span>             | <span data-ttu-id="61cbc-254">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-254">no</span></span>               |
| <span data-ttu-id="61cbc-255">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="61cbc-255">msdyn_plannedcost_base</span></span>                 | <span data-ttu-id="61cbc-256">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-256">no</span></span>             | <span data-ttu-id="61cbc-257">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-257">no</span></span>               |
| <span data-ttu-id="61cbc-258">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="61cbc-258">msdyn_plannedsales</span></span>                     | <span data-ttu-id="61cbc-259">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-259">no</span></span>             | <span data-ttu-id="61cbc-260">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-260">no</span></span>               |
| <span data-ttu-id="61cbc-261">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="61cbc-261">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="61cbc-262">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-262">no</span></span>             | <span data-ttu-id="61cbc-263">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-263">no</span></span>               |
| <span data-ttu-id="61cbc-264">msdyn_pluginprocessingdata</span><span class="sxs-lookup"><span data-stu-id="61cbc-264">msdyn_pluginprocessingdata</span></span>             | <span data-ttu-id="61cbc-265">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-265">no</span></span>             | <span data-ttu-id="61cbc-266">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-266">no</span></span>               |
| <span data-ttu-id="61cbc-267">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="61cbc-267">msdyn_progress</span></span>                         | <span data-ttu-id="61cbc-268">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-268">no</span></span>             | <span data-ttu-id="61cbc-269">no (sí per a P4W)</span><span class="sxs-lookup"><span data-stu-id="61cbc-269">no (yes for P4W)</span></span> |
| <span data-ttu-id="61cbc-270">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="61cbc-270">msdyn_remainingcost</span></span>                    | <span data-ttu-id="61cbc-271">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-271">no</span></span>             | <span data-ttu-id="61cbc-272">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-272">no</span></span>               |
| <span data-ttu-id="61cbc-273">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="61cbc-273">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="61cbc-274">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-274">no</span></span>             | <span data-ttu-id="61cbc-275">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-275">no</span></span>               |
| <span data-ttu-id="61cbc-276">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="61cbc-276">msdyn_remainingsales</span></span>                   | <span data-ttu-id="61cbc-277">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-277">no</span></span>             | <span data-ttu-id="61cbc-278">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-278">no</span></span>               |
| <span data-ttu-id="61cbc-279">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="61cbc-279">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="61cbc-280">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-280">no</span></span>             | <span data-ttu-id="61cbc-281">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-281">no</span></span>               |
| <span data-ttu-id="61cbc-282">msdyn_requestedhours</span><span class="sxs-lookup"><span data-stu-id="61cbc-282">msdyn_requestedhours</span></span>                   | <span data-ttu-id="61cbc-283">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-283">no</span></span>             | <span data-ttu-id="61cbc-284">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-284">no</span></span>               |
| <span data-ttu-id="61cbc-285">msdyn_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="61cbc-285">msdyn_resourcecategory</span></span>                 | <span data-ttu-id="61cbc-286">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-286">no</span></span>             | <span data-ttu-id="61cbc-287">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-287">no</span></span>               |
| <span data-ttu-id="61cbc-288">msdyn_resourcecategoryname</span><span class="sxs-lookup"><span data-stu-id="61cbc-288">msdyn_resourcecategoryname</span></span>             | <span data-ttu-id="61cbc-289">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-289">no</span></span>             | <span data-ttu-id="61cbc-290">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-290">no</span></span>               |
| <span data-ttu-id="61cbc-291">msdyn_resourceorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="61cbc-291">msdyn_resourceorganizationalunitid</span></span>     | <span data-ttu-id="61cbc-292">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-292">no</span></span>             | <span data-ttu-id="61cbc-293">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-293">no</span></span>               |
| <span data-ttu-id="61cbc-294">msdyn_resourceorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="61cbc-294">msdyn_resourceorganizationalunitidname</span></span> | <span data-ttu-id="61cbc-295">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-295">no</span></span>             | <span data-ttu-id="61cbc-296">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-296">no</span></span>               |
| <span data-ttu-id="61cbc-297">msdyn_salesconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="61cbc-297">msdyn_salesconsumptionpercentage</span></span>       | <span data-ttu-id="61cbc-298">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-298">no</span></span>             | <span data-ttu-id="61cbc-299">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-299">no</span></span>               |
| <span data-ttu-id="61cbc-300">msdyn_salesestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="61cbc-300">msdyn_salesestimateatcomplete</span></span>          | <span data-ttu-id="61cbc-301">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-301">no</span></span>             | <span data-ttu-id="61cbc-302">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-302">no</span></span>               |
| <span data-ttu-id="61cbc-303">msdyn_salesestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="61cbc-303">msdyn_salesestimateatcomplete_base</span></span>     | <span data-ttu-id="61cbc-304">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-304">no</span></span>             | <span data-ttu-id="61cbc-305">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-305">no</span></span>               |
| <span data-ttu-id="61cbc-306">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="61cbc-306">msdyn_salesvariance</span></span>                    | <span data-ttu-id="61cbc-307">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-307">no</span></span>             | <span data-ttu-id="61cbc-308">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-308">no</span></span>               |
| <span data-ttu-id="61cbc-309">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="61cbc-309">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="61cbc-310">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-310">no</span></span>             | <span data-ttu-id="61cbc-311">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-311">no</span></span>               |
| <span data-ttu-id="61cbc-312">msdyn_scheduleddurationminutes</span><span class="sxs-lookup"><span data-stu-id="61cbc-312">msdyn_scheduleddurationminutes</span></span>         | <span data-ttu-id="61cbc-313">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-313">no</span></span>             | <span data-ttu-id="61cbc-314">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-314">no</span></span>               |
| <span data-ttu-id="61cbc-315">msdyn_scheduledend</span><span class="sxs-lookup"><span data-stu-id="61cbc-315">msdyn_scheduledend</span></span>                     | <span data-ttu-id="61cbc-316">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-316">no</span></span>             | <span data-ttu-id="61cbc-317">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-317">no</span></span>               |
| <span data-ttu-id="61cbc-318">msdyn_scheduledstart</span><span class="sxs-lookup"><span data-stu-id="61cbc-318">msdyn_scheduledstart</span></span>                   | <span data-ttu-id="61cbc-319">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-319">no</span></span>             | <span data-ttu-id="61cbc-320">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-320">no</span></span>               |
| <span data-ttu-id="61cbc-321">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="61cbc-321">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="61cbc-322">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-322">no</span></span>             | <span data-ttu-id="61cbc-323">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-323">no</span></span>               |
| <span data-ttu-id="61cbc-324">msdyn_skipupdateestimateline</span><span class="sxs-lookup"><span data-stu-id="61cbc-324">msdyn_skipupdateestimateline</span></span>           | <span data-ttu-id="61cbc-325">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-325">no</span></span>             | <span data-ttu-id="61cbc-326">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-326">no</span></span>               |
| <span data-ttu-id="61cbc-327">msdyn_skipupdateestimatelinename</span><span class="sxs-lookup"><span data-stu-id="61cbc-327">msdyn_skipupdateestimatelinename</span></span>       | <span data-ttu-id="61cbc-328">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-328">no</span></span>             | <span data-ttu-id="61cbc-329">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-329">no</span></span>               |
| <span data-ttu-id="61cbc-330">msdyn_summary</span><span class="sxs-lookup"><span data-stu-id="61cbc-330">msdyn_summary</span></span>                          | <span data-ttu-id="61cbc-331">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-331">no</span></span>             | <span data-ttu-id="61cbc-332">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-332">no</span></span>               |
| <span data-ttu-id="61cbc-333">msdyn_varianceofcost</span><span class="sxs-lookup"><span data-stu-id="61cbc-333">msdyn_varianceofcost</span></span>                   | <span data-ttu-id="61cbc-334">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-334">no</span></span>             | <span data-ttu-id="61cbc-335">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-335">no</span></span>               |
| <span data-ttu-id="61cbc-336">msdyn_varianceofcost_base</span><span class="sxs-lookup"><span data-stu-id="61cbc-336">msdyn_varianceofcost_base</span></span>              | <span data-ttu-id="61cbc-337">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-337">no</span></span>             | <span data-ttu-id="61cbc-338">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-338">no</span></span>               |

### <a name="project-task-dependency"></a><span data-ttu-id="61cbc-339">Dependència de les tasques del projecte</span><span class="sxs-lookup"><span data-stu-id="61cbc-339">Project task dependency</span></span>

| <span data-ttu-id="61cbc-340">**Nom lògic**</span><span class="sxs-lookup"><span data-stu-id="61cbc-340">**Logical name**</span></span>              | <span data-ttu-id="61cbc-341">**Pot crear**</span><span class="sxs-lookup"><span data-stu-id="61cbc-341">**Can create**</span></span> | <span data-ttu-id="61cbc-342">**Pot editar**</span><span class="sxs-lookup"><span data-stu-id="61cbc-342">**Can edit**</span></span> |
|-------------------------------|----------------|--------------|
| <span data-ttu-id="61cbc-343">msdyn_linktype</span><span class="sxs-lookup"><span data-stu-id="61cbc-343">msdyn_linktype</span></span>                | <span data-ttu-id="61cbc-344">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-344">no</span></span>             | <span data-ttu-id="61cbc-345">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-345">no</span></span>           |
| <span data-ttu-id="61cbc-346">msdyn_linktypename</span><span class="sxs-lookup"><span data-stu-id="61cbc-346">msdyn_linktypename</span></span>            | <span data-ttu-id="61cbc-347">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-347">no</span></span>             | <span data-ttu-id="61cbc-348">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-348">no</span></span>           |
| <span data-ttu-id="61cbc-349">msdyn_predecessortask</span><span class="sxs-lookup"><span data-stu-id="61cbc-349">msdyn_predecessortask</span></span>         | <span data-ttu-id="61cbc-350">sí</span><span class="sxs-lookup"><span data-stu-id="61cbc-350">yes</span></span>            | <span data-ttu-id="61cbc-351">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-351">no</span></span>           |
| <span data-ttu-id="61cbc-352">msdyn_predecessortaskname</span><span class="sxs-lookup"><span data-stu-id="61cbc-352">msdyn_predecessortaskname</span></span>     | <span data-ttu-id="61cbc-353">sí</span><span class="sxs-lookup"><span data-stu-id="61cbc-353">yes</span></span>            | <span data-ttu-id="61cbc-354">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-354">no</span></span>           |
| <span data-ttu-id="61cbc-355">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="61cbc-355">msdyn_project</span></span>                 | <span data-ttu-id="61cbc-356">sí</span><span class="sxs-lookup"><span data-stu-id="61cbc-356">yes</span></span>            | <span data-ttu-id="61cbc-357">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-357">no</span></span>           |
| <span data-ttu-id="61cbc-358">msdyn_projectname</span><span class="sxs-lookup"><span data-stu-id="61cbc-358">msdyn_projectname</span></span>             | <span data-ttu-id="61cbc-359">sí</span><span class="sxs-lookup"><span data-stu-id="61cbc-359">yes</span></span>            | <span data-ttu-id="61cbc-360">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-360">no</span></span>           |
| <span data-ttu-id="61cbc-361">msdyn_projecttaskdependencyid</span><span class="sxs-lookup"><span data-stu-id="61cbc-361">msdyn_projecttaskdependencyid</span></span> | <span data-ttu-id="61cbc-362">sí</span><span class="sxs-lookup"><span data-stu-id="61cbc-362">yes</span></span>            | <span data-ttu-id="61cbc-363">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-363">no</span></span>           |
| <span data-ttu-id="61cbc-364">msdyn_successortask</span><span class="sxs-lookup"><span data-stu-id="61cbc-364">msdyn_successortask</span></span>           | <span data-ttu-id="61cbc-365">sí</span><span class="sxs-lookup"><span data-stu-id="61cbc-365">yes</span></span>            | <span data-ttu-id="61cbc-366">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-366">no</span></span>           |
| <span data-ttu-id="61cbc-367">msdyn_successortaskname</span><span class="sxs-lookup"><span data-stu-id="61cbc-367">msdyn_successortaskname</span></span>       | <span data-ttu-id="61cbc-368">sí</span><span class="sxs-lookup"><span data-stu-id="61cbc-368">yes</span></span>            | <span data-ttu-id="61cbc-369">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-369">no</span></span>           |

### <a name="resource-assignment"></a><span data-ttu-id="61cbc-370">Assignació de recursos</span><span class="sxs-lookup"><span data-stu-id="61cbc-370">Resource assignment</span></span>

| <span data-ttu-id="61cbc-371">**Nom lògic**</span><span class="sxs-lookup"><span data-stu-id="61cbc-371">**Logical name**</span></span>             | <span data-ttu-id="61cbc-372">**Pot crear**</span><span class="sxs-lookup"><span data-stu-id="61cbc-372">**Can create**</span></span> | <span data-ttu-id="61cbc-373">**Pot editar**</span><span class="sxs-lookup"><span data-stu-id="61cbc-373">**Can edit**</span></span> |
|------------------------------|----------------|--------------|
| <span data-ttu-id="61cbc-374">msdyn_bookableresourceid</span><span class="sxs-lookup"><span data-stu-id="61cbc-374">msdyn_bookableresourceid</span></span>     | <span data-ttu-id="61cbc-375">sí</span><span class="sxs-lookup"><span data-stu-id="61cbc-375">yes</span></span>            | <span data-ttu-id="61cbc-376">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-376">no</span></span>           |
| <span data-ttu-id="61cbc-377">msdyn_bookableresourceidname</span><span class="sxs-lookup"><span data-stu-id="61cbc-377">msdyn_bookableresourceidname</span></span> | <span data-ttu-id="61cbc-378">sí</span><span class="sxs-lookup"><span data-stu-id="61cbc-378">yes</span></span>            | <span data-ttu-id="61cbc-379">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-379">no</span></span>           |
| <span data-ttu-id="61cbc-380">msdyn_bookingstatusid</span><span class="sxs-lookup"><span data-stu-id="61cbc-380">msdyn_bookingstatusid</span></span>        | <span data-ttu-id="61cbc-381">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-381">no</span></span>             | <span data-ttu-id="61cbc-382">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-382">no</span></span>           |
| <span data-ttu-id="61cbc-383">msdyn_bookingstatusidname</span><span class="sxs-lookup"><span data-stu-id="61cbc-383">msdyn_bookingstatusidname</span></span>    | <span data-ttu-id="61cbc-384">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-384">no</span></span>             | <span data-ttu-id="61cbc-385">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-385">no</span></span>           |
| <span data-ttu-id="61cbc-386">msdyn_committype</span><span class="sxs-lookup"><span data-stu-id="61cbc-386">msdyn_committype</span></span>             | <span data-ttu-id="61cbc-387">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-387">no</span></span>             | <span data-ttu-id="61cbc-388">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-388">no</span></span>           |
| <span data-ttu-id="61cbc-389">msdyn_committypename</span><span class="sxs-lookup"><span data-stu-id="61cbc-389">msdyn_committypename</span></span>         | <span data-ttu-id="61cbc-390">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-390">no</span></span>             | <span data-ttu-id="61cbc-391">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-391">no</span></span>           |
| <span data-ttu-id="61cbc-392">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="61cbc-392">msdyn_effort</span></span>                 | <span data-ttu-id="61cbc-393">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-393">no</span></span>             | <span data-ttu-id="61cbc-394">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-394">no</span></span>           |
| <span data-ttu-id="61cbc-395">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="61cbc-395">msdyn_effortcompleted</span></span>        | <span data-ttu-id="61cbc-396">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-396">no</span></span>             | <span data-ttu-id="61cbc-397">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-397">no</span></span>           |
| <span data-ttu-id="61cbc-398">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="61cbc-398">msdyn_effortremaining</span></span>        | <span data-ttu-id="61cbc-399">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-399">no</span></span>             | <span data-ttu-id="61cbc-400">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-400">no</span></span>           |
| <span data-ttu-id="61cbc-401">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="61cbc-401">msdyn_finish</span></span>                 | <span data-ttu-id="61cbc-402">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-402">no</span></span>             | <span data-ttu-id="61cbc-403">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-403">no</span></span>           |
| <span data-ttu-id="61cbc-404">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="61cbc-404">msdyn_plannedcost</span></span>            | <span data-ttu-id="61cbc-405">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-405">no</span></span>             | <span data-ttu-id="61cbc-406">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-406">no</span></span>           |
| <span data-ttu-id="61cbc-407">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="61cbc-407">msdyn_plannedcost_base</span></span>       | <span data-ttu-id="61cbc-408">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-408">no</span></span>             | <span data-ttu-id="61cbc-409">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-409">no</span></span>           |
| <span data-ttu-id="61cbc-410">msdyn_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="61cbc-410">msdyn_plannedcostcontour</span></span>     | <span data-ttu-id="61cbc-411">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-411">no</span></span>             | <span data-ttu-id="61cbc-412">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-412">no</span></span>           |
| <span data-ttu-id="61cbc-413">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="61cbc-413">msdyn_plannedsales</span></span>           | <span data-ttu-id="61cbc-414">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-414">no</span></span>             | <span data-ttu-id="61cbc-415">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-415">no</span></span>           |
| <span data-ttu-id="61cbc-416">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="61cbc-416">msdyn_plannedsales_base</span></span>      | <span data-ttu-id="61cbc-417">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-417">no</span></span>             | <span data-ttu-id="61cbc-418">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-418">no</span></span>           |
| <span data-ttu-id="61cbc-419">msdyn_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="61cbc-419">msdyn_plannedsalescontour</span></span>    | <span data-ttu-id="61cbc-420">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-420">no</span></span>             | <span data-ttu-id="61cbc-421">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-421">no</span></span>           |
| <span data-ttu-id="61cbc-422">msdyn_plannedwork</span><span class="sxs-lookup"><span data-stu-id="61cbc-422">msdyn_plannedwork</span></span>            | <span data-ttu-id="61cbc-423">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-423">no</span></span>             | <span data-ttu-id="61cbc-424">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-424">no</span></span>           |
| <span data-ttu-id="61cbc-425">msdyn_projectid</span><span class="sxs-lookup"><span data-stu-id="61cbc-425">msdyn_projectid</span></span>              | <span data-ttu-id="61cbc-426">sí</span><span class="sxs-lookup"><span data-stu-id="61cbc-426">yes</span></span>            | <span data-ttu-id="61cbc-427">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-427">no</span></span>           |
| <span data-ttu-id="61cbc-428">msdyn_projectidname</span><span class="sxs-lookup"><span data-stu-id="61cbc-428">msdyn_projectidname</span></span>          | <span data-ttu-id="61cbc-429">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-429">no</span></span>             | <span data-ttu-id="61cbc-430">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-430">no</span></span>           |
| <span data-ttu-id="61cbc-431">msdyn_projectteamid</span><span class="sxs-lookup"><span data-stu-id="61cbc-431">msdyn_projectteamid</span></span>          | <span data-ttu-id="61cbc-432">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-432">no</span></span>             | <span data-ttu-id="61cbc-433">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-433">no</span></span>           |
| <span data-ttu-id="61cbc-434">msdyn_projectteamidname</span><span class="sxs-lookup"><span data-stu-id="61cbc-434">msdyn_projectteamidname</span></span>      | <span data-ttu-id="61cbc-435">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-435">no</span></span>             | <span data-ttu-id="61cbc-436">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-436">no</span></span>           |
| <span data-ttu-id="61cbc-437">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="61cbc-437">msdyn_start</span></span>                  | <span data-ttu-id="61cbc-438">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-438">no</span></span>             | <span data-ttu-id="61cbc-439">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-439">no</span></span>           |
| <span data-ttu-id="61cbc-440">msdyn_taskid</span><span class="sxs-lookup"><span data-stu-id="61cbc-440">msdyn_taskid</span></span>                 | <span data-ttu-id="61cbc-441">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-441">no</span></span>             | <span data-ttu-id="61cbc-442">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-442">no</span></span>           |
| <span data-ttu-id="61cbc-443">msdyn_taskidname</span><span class="sxs-lookup"><span data-stu-id="61cbc-443">msdyn_taskidname</span></span>             | <span data-ttu-id="61cbc-444">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-444">no</span></span>             | <span data-ttu-id="61cbc-445">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-445">no</span></span>           |
| <span data-ttu-id="61cbc-446">msdyn_userresourceid</span><span class="sxs-lookup"><span data-stu-id="61cbc-446">msdyn_userresourceid</span></span>         | <span data-ttu-id="61cbc-447">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-447">no</span></span>             | <span data-ttu-id="61cbc-448">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-448">no</span></span>           |

### <a name="project-team-member"></a><span data-ttu-id="61cbc-449">Membre de l'equip del projecte</span><span class="sxs-lookup"><span data-stu-id="61cbc-449">Project team member</span></span>

| <span data-ttu-id="61cbc-450">**Nom lògic**</span><span class="sxs-lookup"><span data-stu-id="61cbc-450">**Logical name**</span></span>                                 | <span data-ttu-id="61cbc-451">**Pot crear**</span><span class="sxs-lookup"><span data-stu-id="61cbc-451">**Can create**</span></span> | <span data-ttu-id="61cbc-452">**Pot editar**</span><span class="sxs-lookup"><span data-stu-id="61cbc-452">**Can edit**</span></span> |
|--------------------------------------------------|----------------|--------------|
| <span data-ttu-id="61cbc-453">msdyn_calendarid</span><span class="sxs-lookup"><span data-stu-id="61cbc-453">msdyn_calendarid</span></span>                                 | <span data-ttu-id="61cbc-454">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-454">no</span></span>             | <span data-ttu-id="61cbc-455">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-455">no</span></span>           |
| <span data-ttu-id="61cbc-456">msdyn_creategenericteammemberwithrequirementname</span><span class="sxs-lookup"><span data-stu-id="61cbc-456">msdyn_creategenericteammemberwithrequirementname</span></span> | <span data-ttu-id="61cbc-457">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-457">no</span></span>             | <span data-ttu-id="61cbc-458">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-458">no</span></span>           |
| <span data-ttu-id="61cbc-459">msdyn_deletestatus</span><span class="sxs-lookup"><span data-stu-id="61cbc-459">msdyn_deletestatus</span></span>                               | <span data-ttu-id="61cbc-460">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-460">no</span></span>             | <span data-ttu-id="61cbc-461">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-461">no</span></span>           |
| <span data-ttu-id="61cbc-462">msdyn_deletestatusname</span><span class="sxs-lookup"><span data-stu-id="61cbc-462">msdyn_deletestatusname</span></span>                           | <span data-ttu-id="61cbc-463">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-463">no</span></span>             | <span data-ttu-id="61cbc-464">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-464">no</span></span>           |
| <span data-ttu-id="61cbc-465">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="61cbc-465">msdyn_effort</span></span>                                     | <span data-ttu-id="61cbc-466">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-466">no</span></span>             | <span data-ttu-id="61cbc-467">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-467">no</span></span>           |
| <span data-ttu-id="61cbc-468">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="61cbc-468">msdyn_effortcompleted</span></span>                            | <span data-ttu-id="61cbc-469">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-469">no</span></span>             | <span data-ttu-id="61cbc-470">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-470">no</span></span>           |
| <span data-ttu-id="61cbc-471">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="61cbc-471">msdyn_effortremaining</span></span>                            | <span data-ttu-id="61cbc-472">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-472">no</span></span>             | <span data-ttu-id="61cbc-473">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-473">no</span></span>           |
| <span data-ttu-id="61cbc-474">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="61cbc-474">msdyn_finish</span></span>                                     | <span data-ttu-id="61cbc-475">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-475">no</span></span>             | <span data-ttu-id="61cbc-476">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-476">no</span></span>           |
| <span data-ttu-id="61cbc-477">msdyn_hardbookedhours</span><span class="sxs-lookup"><span data-stu-id="61cbc-477">msdyn_hardbookedhours</span></span>                            | <span data-ttu-id="61cbc-478">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-478">no</span></span>             | <span data-ttu-id="61cbc-479">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-479">no</span></span>           |
| <span data-ttu-id="61cbc-480">msdyn_hours</span><span class="sxs-lookup"><span data-stu-id="61cbc-480">msdyn_hours</span></span>                                      | <span data-ttu-id="61cbc-481">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-481">no</span></span>             | <span data-ttu-id="61cbc-482">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-482">no</span></span>           |
| <span data-ttu-id="61cbc-483">msdyn_markedfordeletiontimer</span><span class="sxs-lookup"><span data-stu-id="61cbc-483">msdyn_markedfordeletiontimer</span></span>                     | <span data-ttu-id="61cbc-484">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-484">no</span></span>             | <span data-ttu-id="61cbc-485">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-485">no</span></span>           |
| <span data-ttu-id="61cbc-486">msdyn_markedfordeletiontimestamp</span><span class="sxs-lookup"><span data-stu-id="61cbc-486">msdyn_markedfordeletiontimestamp</span></span>                 | <span data-ttu-id="61cbc-487">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-487">no</span></span>             | <span data-ttu-id="61cbc-488">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-488">no</span></span>           |
| <span data-ttu-id="61cbc-489">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="61cbc-489">msdyn_msprojectclientid</span></span>                          | <span data-ttu-id="61cbc-490">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-490">no</span></span>             | <span data-ttu-id="61cbc-491">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-491">no</span></span>           |
| <span data-ttu-id="61cbc-492">msdyn_percentage</span><span class="sxs-lookup"><span data-stu-id="61cbc-492">msdyn_percentage</span></span>                                 | <span data-ttu-id="61cbc-493">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-493">no</span></span>             | <span data-ttu-id="61cbc-494">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-494">no</span></span>           |
| <span data-ttu-id="61cbc-495">msdyn_requiredhours</span><span class="sxs-lookup"><span data-stu-id="61cbc-495">msdyn_requiredhours</span></span>                              | <span data-ttu-id="61cbc-496">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-496">no</span></span>             | <span data-ttu-id="61cbc-497">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-497">no</span></span>           |
| <span data-ttu-id="61cbc-498">msdyn_softbookedhours</span><span class="sxs-lookup"><span data-stu-id="61cbc-498">msdyn_softbookedhours</span></span>                            | <span data-ttu-id="61cbc-499">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-499">no</span></span>             | <span data-ttu-id="61cbc-500">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-500">no</span></span>           |
| <span data-ttu-id="61cbc-501">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="61cbc-501">msdyn_start</span></span>                                      | <span data-ttu-id="61cbc-502">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-502">no</span></span>             | <span data-ttu-id="61cbc-503">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-503">no</span></span>           |

### <a name="project"></a><span data-ttu-id="61cbc-504">Project</span><span class="sxs-lookup"><span data-stu-id="61cbc-504">Project</span></span>

| <span data-ttu-id="61cbc-505">**Nom lògic**</span><span class="sxs-lookup"><span data-stu-id="61cbc-505">**Logical name**</span></span>                       | <span data-ttu-id="61cbc-506">**Pot crear**</span><span class="sxs-lookup"><span data-stu-id="61cbc-506">**Can create**</span></span> | <span data-ttu-id="61cbc-507">**Pot editar**</span><span class="sxs-lookup"><span data-stu-id="61cbc-507">**Can edit**</span></span> |
|----------------------------------------|----------------|--------------|
| <span data-ttu-id="61cbc-508">msdyn_actualexpensecost</span><span class="sxs-lookup"><span data-stu-id="61cbc-508">msdyn_actualexpensecost</span></span>                | <span data-ttu-id="61cbc-509">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-509">no</span></span>             | <span data-ttu-id="61cbc-510">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-510">no</span></span>           |
| <span data-ttu-id="61cbc-511">msdyn_actualexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="61cbc-511">msdyn_actualexpensecost_base</span></span>           | <span data-ttu-id="61cbc-512">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-512">no</span></span>             | <span data-ttu-id="61cbc-513">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-513">no</span></span>           |
| <span data-ttu-id="61cbc-514">msdyn_actuallaborcost</span><span class="sxs-lookup"><span data-stu-id="61cbc-514">msdyn_actuallaborcost</span></span>                  | <span data-ttu-id="61cbc-515">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-515">no</span></span>             | <span data-ttu-id="61cbc-516">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-516">no</span></span>           |
| <span data-ttu-id="61cbc-517">msdyn_actuallaborcost_base</span><span class="sxs-lookup"><span data-stu-id="61cbc-517">msdyn_actuallaborcost_base</span></span>             | <span data-ttu-id="61cbc-518">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-518">no</span></span>             | <span data-ttu-id="61cbc-519">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-519">no</span></span>           |
| <span data-ttu-id="61cbc-520">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="61cbc-520">msdyn_actualsales</span></span>                      | <span data-ttu-id="61cbc-521">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-521">no</span></span>             | <span data-ttu-id="61cbc-522">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-522">no</span></span>           |
| <span data-ttu-id="61cbc-523">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="61cbc-523">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="61cbc-524">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-524">no</span></span>             | <span data-ttu-id="61cbc-525">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-525">no</span></span>           |
| <span data-ttu-id="61cbc-526">msdyn_contractlineproject</span><span class="sxs-lookup"><span data-stu-id="61cbc-526">msdyn_contractlineproject</span></span>              | <span data-ttu-id="61cbc-527">sí</span><span class="sxs-lookup"><span data-stu-id="61cbc-527">yes</span></span>            | <span data-ttu-id="61cbc-528">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-528">no</span></span>           |
| <span data-ttu-id="61cbc-529">msdyn_contractorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="61cbc-529">msdyn_contractorganizationalunitid</span></span>     | <span data-ttu-id="61cbc-530">sí</span><span class="sxs-lookup"><span data-stu-id="61cbc-530">yes</span></span>            | <span data-ttu-id="61cbc-531">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-531">no</span></span>           |
| <span data-ttu-id="61cbc-532">msdyn_contractorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="61cbc-532">msdyn_contractorganizationalunitidname</span></span> | <span data-ttu-id="61cbc-533">sí</span><span class="sxs-lookup"><span data-stu-id="61cbc-533">yes</span></span>            | <span data-ttu-id="61cbc-534">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-534">no</span></span>           |
| <span data-ttu-id="61cbc-535">msdyn_costconsumption</span><span class="sxs-lookup"><span data-stu-id="61cbc-535">msdyn_costconsumption</span></span>                  | <span data-ttu-id="61cbc-536">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-536">no</span></span>             | <span data-ttu-id="61cbc-537">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-537">no</span></span>           |
| <span data-ttu-id="61cbc-538">msdyn_costestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="61cbc-538">msdyn_costestimateatcomplete</span></span>           | <span data-ttu-id="61cbc-539">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-539">no</span></span>             | <span data-ttu-id="61cbc-540">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-540">no</span></span>           |
| <span data-ttu-id="61cbc-541">msdyn_costestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="61cbc-541">msdyn_costestimateatcomplete_base</span></span>      | <span data-ttu-id="61cbc-542">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-542">no</span></span>             | <span data-ttu-id="61cbc-543">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-543">no</span></span>           |
| <span data-ttu-id="61cbc-544">msdyn_costvariance</span><span class="sxs-lookup"><span data-stu-id="61cbc-544">msdyn_costvariance</span></span>                     | <span data-ttu-id="61cbc-545">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-545">no</span></span>             | <span data-ttu-id="61cbc-546">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-546">no</span></span>           |
| <span data-ttu-id="61cbc-547">msdyn_costvariance_base</span><span class="sxs-lookup"><span data-stu-id="61cbc-547">msdyn_costvariance_base</span></span>                | <span data-ttu-id="61cbc-548">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-548">no</span></span>             | <span data-ttu-id="61cbc-549">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-549">no</span></span>           |
| <span data-ttu-id="61cbc-550">msdyn_duration</span><span class="sxs-lookup"><span data-stu-id="61cbc-550">msdyn_duration</span></span>                         | <span data-ttu-id="61cbc-551">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-551">no</span></span>             | <span data-ttu-id="61cbc-552">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-552">no</span></span>           |
| <span data-ttu-id="61cbc-553">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="61cbc-553">msdyn_effort</span></span>                           | <span data-ttu-id="61cbc-554">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-554">no</span></span>             | <span data-ttu-id="61cbc-555">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-555">no</span></span>           |
| <span data-ttu-id="61cbc-556">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="61cbc-556">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="61cbc-557">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-557">no</span></span>             | <span data-ttu-id="61cbc-558">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-558">no</span></span>           |
| <span data-ttu-id="61cbc-559">msdyn_effortestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="61cbc-559">msdyn_effortestimateatcompleteeac</span></span>      | <span data-ttu-id="61cbc-560">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-560">no</span></span>             | <span data-ttu-id="61cbc-561">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-561">no</span></span>           |
| <span data-ttu-id="61cbc-562">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="61cbc-562">msdyn_effortremaining</span></span>                  | <span data-ttu-id="61cbc-563">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-563">no</span></span>             | <span data-ttu-id="61cbc-564">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-564">no</span></span>           |
| <span data-ttu-id="61cbc-565">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="61cbc-565">msdyn_finish</span></span>                           | <span data-ttu-id="61cbc-566">sí</span><span class="sxs-lookup"><span data-stu-id="61cbc-566">yes</span></span>            | <span data-ttu-id="61cbc-567">sí</span><span class="sxs-lookup"><span data-stu-id="61cbc-567">yes</span></span>          |
| <span data-ttu-id="61cbc-568">msdyn_globalrevisiontoken</span><span class="sxs-lookup"><span data-stu-id="61cbc-568">msdyn_globalrevisiontoken</span></span>              | <span data-ttu-id="61cbc-569">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-569">no</span></span>             | <span data-ttu-id="61cbc-570">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-570">no</span></span>           |
| <span data-ttu-id="61cbc-571">msdyn_islinkedtomsprojectclient</span><span class="sxs-lookup"><span data-stu-id="61cbc-571">msdyn_islinkedtomsprojectclient</span></span>        | <span data-ttu-id="61cbc-572">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-572">no</span></span>             | <span data-ttu-id="61cbc-573">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-573">no</span></span>           |
| <span data-ttu-id="61cbc-574">msdyn_islinkedtomsprojectclientname</span><span class="sxs-lookup"><span data-stu-id="61cbc-574">msdyn_islinkedtomsprojectclientname</span></span>    | <span data-ttu-id="61cbc-575">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-575">no</span></span>             | <span data-ttu-id="61cbc-576">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-576">no</span></span>           |
| <span data-ttu-id="61cbc-577">msdyn_linkeddocumenturl</span><span class="sxs-lookup"><span data-stu-id="61cbc-577">msdyn_linkeddocumenturl</span></span>                | <span data-ttu-id="61cbc-578">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-578">no</span></span>             | <span data-ttu-id="61cbc-579">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-579">no</span></span>           |
| <span data-ttu-id="61cbc-580">msdyn_msprojectdocument</span><span class="sxs-lookup"><span data-stu-id="61cbc-580">msdyn_msprojectdocument</span></span>                | <span data-ttu-id="61cbc-581">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-581">no</span></span>             | <span data-ttu-id="61cbc-582">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-582">no</span></span>           |
| <span data-ttu-id="61cbc-583">msdyn_msprojectdocumentname</span><span class="sxs-lookup"><span data-stu-id="61cbc-583">msdyn_msprojectdocumentname</span></span>            | <span data-ttu-id="61cbc-584">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-584">no</span></span>             | <span data-ttu-id="61cbc-585">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-585">no</span></span>           |
| <span data-ttu-id="61cbc-586">msdyn_plannedexpensecost</span><span class="sxs-lookup"><span data-stu-id="61cbc-586">msdyn_plannedexpensecost</span></span>               | <span data-ttu-id="61cbc-587">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-587">no</span></span>             | <span data-ttu-id="61cbc-588">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-588">no</span></span>           |
| <span data-ttu-id="61cbc-589">msdyn_plannedexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="61cbc-589">msdyn_plannedexpensecost_base</span></span>          | <span data-ttu-id="61cbc-590">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-590">no</span></span>             | <span data-ttu-id="61cbc-591">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-591">no</span></span>           |
| <span data-ttu-id="61cbc-592">msdyn_plannedlaborcost</span><span class="sxs-lookup"><span data-stu-id="61cbc-592">msdyn_plannedlaborcost</span></span>                 | <span data-ttu-id="61cbc-593">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-593">no</span></span>             | <span data-ttu-id="61cbc-594">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-594">no</span></span>           |
| <span data-ttu-id="61cbc-595">msdyn_plannedlaborcost_base</span><span class="sxs-lookup"><span data-stu-id="61cbc-595">msdyn_plannedlaborcost_base</span></span>            | <span data-ttu-id="61cbc-596">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-596">no</span></span>             | <span data-ttu-id="61cbc-597">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-597">no</span></span>           |
| <span data-ttu-id="61cbc-598">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="61cbc-598">msdyn_plannedsales</span></span>                     | <span data-ttu-id="61cbc-599">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-599">no</span></span>             | <span data-ttu-id="61cbc-600">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-600">no</span></span>           |
| <span data-ttu-id="61cbc-601">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="61cbc-601">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="61cbc-602">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-602">no</span></span>             | <span data-ttu-id="61cbc-603">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-603">no</span></span>           |
| <span data-ttu-id="61cbc-604">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="61cbc-604">msdyn_progress</span></span>                         | <span data-ttu-id="61cbc-605">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-605">no</span></span>             | <span data-ttu-id="61cbc-606">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-606">no</span></span>           |
| <span data-ttu-id="61cbc-607">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="61cbc-607">msdyn_remainingcost</span></span>                    | <span data-ttu-id="61cbc-608">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-608">no</span></span>             | <span data-ttu-id="61cbc-609">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-609">no</span></span>           |
| <span data-ttu-id="61cbc-610">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="61cbc-610">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="61cbc-611">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-611">no</span></span>             | <span data-ttu-id="61cbc-612">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-612">no</span></span>           |
| <span data-ttu-id="61cbc-613">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="61cbc-613">msdyn_remainingsales</span></span>                   | <span data-ttu-id="61cbc-614">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-614">no</span></span>             | <span data-ttu-id="61cbc-615">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-615">no</span></span>           |
| <span data-ttu-id="61cbc-616">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="61cbc-616">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="61cbc-617">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-617">no</span></span>             | <span data-ttu-id="61cbc-618">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-618">no</span></span>           |
| <span data-ttu-id="61cbc-619">msdyn_replaylogheader</span><span class="sxs-lookup"><span data-stu-id="61cbc-619">msdyn_replaylogheader</span></span>                  | <span data-ttu-id="61cbc-620">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-620">no</span></span>             | <span data-ttu-id="61cbc-621">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-621">no</span></span>           |
| <span data-ttu-id="61cbc-622">msdyn_salesconsumption</span><span class="sxs-lookup"><span data-stu-id="61cbc-622">msdyn_salesconsumption</span></span>                 | <span data-ttu-id="61cbc-623">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-623">no</span></span>             | <span data-ttu-id="61cbc-624">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-624">no</span></span>           |
| <span data-ttu-id="61cbc-625">msdyn_salesestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="61cbc-625">msdyn_salesestimateatcompleteeac</span></span>       | <span data-ttu-id="61cbc-626">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-626">no</span></span>             | <span data-ttu-id="61cbc-627">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-627">no</span></span>           |
| <span data-ttu-id="61cbc-628">msdyn_salesestimateatcompleteeac_base</span><span class="sxs-lookup"><span data-stu-id="61cbc-628">msdyn_salesestimateatcompleteeac_base</span></span>  | <span data-ttu-id="61cbc-629">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-629">no</span></span>             | <span data-ttu-id="61cbc-630">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-630">no</span></span>           |
| <span data-ttu-id="61cbc-631">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="61cbc-631">msdyn_salesvariance</span></span>                    | <span data-ttu-id="61cbc-632">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-632">no</span></span>             | <span data-ttu-id="61cbc-633">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-633">no</span></span>           |
| <span data-ttu-id="61cbc-634">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="61cbc-634">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="61cbc-635">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-635">no</span></span>             | <span data-ttu-id="61cbc-636">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-636">no</span></span>           |
| <span data-ttu-id="61cbc-637">msdyn_scheduleperformance</span><span class="sxs-lookup"><span data-stu-id="61cbc-637">msdyn_scheduleperformance</span></span>              | <span data-ttu-id="61cbc-638">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-638">no</span></span>             | <span data-ttu-id="61cbc-639">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-639">no</span></span>           |
| <span data-ttu-id="61cbc-640">msdyn_scheduleperformancename</span><span class="sxs-lookup"><span data-stu-id="61cbc-640">msdyn_scheduleperformancename</span></span>          | <span data-ttu-id="61cbc-641">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-641">no</span></span>             | <span data-ttu-id="61cbc-642">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-642">no</span></span>           |
| <span data-ttu-id="61cbc-643">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="61cbc-643">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="61cbc-644">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-644">no</span></span>             | <span data-ttu-id="61cbc-645">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-645">no</span></span>           |
| <span data-ttu-id="61cbc-646">msdyn_taskearlieststart</span><span class="sxs-lookup"><span data-stu-id="61cbc-646">msdyn_taskearlieststart</span></span>                | <span data-ttu-id="61cbc-647">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-647">no</span></span>             | <span data-ttu-id="61cbc-648">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-648">no</span></span>           |
| <span data-ttu-id="61cbc-649">msdyn_teamsize</span><span class="sxs-lookup"><span data-stu-id="61cbc-649">msdyn_teamsize</span></span>                         | <span data-ttu-id="61cbc-650">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-650">no</span></span>             | <span data-ttu-id="61cbc-651">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-651">no</span></span>           |
| <span data-ttu-id="61cbc-652">msdyn_teamsize_date</span><span class="sxs-lookup"><span data-stu-id="61cbc-652">msdyn_teamsize_date</span></span>                    | <span data-ttu-id="61cbc-653">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-653">no</span></span>             | <span data-ttu-id="61cbc-654">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-654">no</span></span>           |
| <span data-ttu-id="61cbc-655">msdyn_teamsize_state</span><span class="sxs-lookup"><span data-stu-id="61cbc-655">msdyn_teamsize_state</span></span>                   | <span data-ttu-id="61cbc-656">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-656">no</span></span>             | <span data-ttu-id="61cbc-657">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-657">no</span></span>           |
| <span data-ttu-id="61cbc-658">msdyn_totalactualcost</span><span class="sxs-lookup"><span data-stu-id="61cbc-658">msdyn_totalactualcost</span></span>                  | <span data-ttu-id="61cbc-659">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-659">no</span></span>             | <span data-ttu-id="61cbc-660">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-660">no</span></span>           |
| <span data-ttu-id="61cbc-661">msdyn_totalactualcost_base</span><span class="sxs-lookup"><span data-stu-id="61cbc-661">msdyn_totalactualcost_base</span></span>             | <span data-ttu-id="61cbc-662">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-662">no</span></span>             | <span data-ttu-id="61cbc-663">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-663">no</span></span>           |
| <span data-ttu-id="61cbc-664">msdyn_totalplannedcost</span><span class="sxs-lookup"><span data-stu-id="61cbc-664">msdyn_totalplannedcost</span></span>                 | <span data-ttu-id="61cbc-665">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-665">no</span></span>             | <span data-ttu-id="61cbc-666">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-666">no</span></span>           |
| <span data-ttu-id="61cbc-667">msdyn_totalplannedcost_base</span><span class="sxs-lookup"><span data-stu-id="61cbc-667">msdyn_totalplannedcost_base</span></span>            | <span data-ttu-id="61cbc-668">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-668">no</span></span>             | <span data-ttu-id="61cbc-669">no</span><span class="sxs-lookup"><span data-stu-id="61cbc-669">no</span></span>           |


## <a name="limitations-and-known-issues"></a><span data-ttu-id="61cbc-670">Limitacions i problemes coneguts</span><span class="sxs-lookup"><span data-stu-id="61cbc-670">Limitations and known issues</span></span>
<span data-ttu-id="61cbc-671">A continuació es mostra una llista de limitacions i problemes coneguts:</span><span class="sxs-lookup"><span data-stu-id="61cbc-671">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="61cbc-672">Només poden utilitzar les API de Planificació els **Usuaris amb llicència del Microsoft Project**.</span><span class="sxs-lookup"><span data-stu-id="61cbc-672">Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="61cbc-673">No les poden utilitzar:</span><span class="sxs-lookup"><span data-stu-id="61cbc-673">They can't be used by:</span></span>
    - <span data-ttu-id="61cbc-674">Usuaris de l'aplicació</span><span class="sxs-lookup"><span data-stu-id="61cbc-674">Application users</span></span>
    - <span data-ttu-id="61cbc-675">Usuaris del sistema</span><span class="sxs-lookup"><span data-stu-id="61cbc-675">System users</span></span>
    - <span data-ttu-id="61cbc-676">Usuaris d'integració</span><span class="sxs-lookup"><span data-stu-id="61cbc-676">Integration users</span></span>
    - <span data-ttu-id="61cbc-677">Altres usuaris que no tenen la llicència necessària</span><span class="sxs-lookup"><span data-stu-id="61cbc-677">Other users that don't have the required license</span></span>
- <span data-ttu-id="61cbc-678">Cada **OperationSet** només pot tenir un màxim de 100 operacions.</span><span class="sxs-lookup"><span data-stu-id="61cbc-678">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="61cbc-679">Cada usuari només pot tenir un màxim de 10 **OperationSets** oberts.</span><span class="sxs-lookup"><span data-stu-id="61cbc-679">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="61cbc-680">El Project Operations actualment admet un màxim de 500 tasques totals en un projecte.</span><span class="sxs-lookup"><span data-stu-id="61cbc-680">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="61cbc-681">Actualment no hi ha estats d'error i registres d'error d'**OperationSet** disponibles.</span><span class="sxs-lookup"><span data-stu-id="61cbc-681">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- <span data-ttu-id="61cbc-682">Les API de Planificació es troben a la versió preliminar pública.</span><span class="sxs-lookup"><span data-stu-id="61cbc-682">Schedule APIs are in Public preview.</span></span> <span data-ttu-id="61cbc-683">Microsoft no admet l'ús d'aquestes d'aquestes API en un entorn de producció.</span><span class="sxs-lookup"><span data-stu-id="61cbc-683">Using these APIs in a Production environment isn't supported by Microsoft.</span></span>
- [<span data-ttu-id="61cbc-684">Límits dels projectes i tasques</span><span class="sxs-lookup"><span data-stu-id="61cbc-684">Limits and boundaries on projects and tasks</span></span>](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a><span data-ttu-id="61cbc-685">Gestió d'errors</span><span class="sxs-lookup"><span data-stu-id="61cbc-685">Error handling</span></span>

   - <span data-ttu-id="61cbc-686">Per revisar els errors generats a partir dels conjunts d'operacions, aneu a **Configuració** \> **Integració de la planificació** \> **Conjunts d'operacions**.</span><span class="sxs-lookup"><span data-stu-id="61cbc-686">To review errors generated from the Operation Sets, go to **Settings** \> **Schedule Integration** \> **Operations Sets**.</span></span>
   - <span data-ttu-id="61cbc-687">Per revisar els errors generats a partir del servei de planificació del projecte, aneu a **Configuració** \> **Integració de la planificació** \> **Registres d'error de PSS**.</span><span class="sxs-lookup"><span data-stu-id="61cbc-687">To review errors generated from the Project Scheduling Service, go to **Settings** \> **Schedule Integration** \> **PSS Error Logs**.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="61cbc-688">Escenari d'exemple</span><span class="sxs-lookup"><span data-stu-id="61cbc-688">Sample scenario</span></span>

<span data-ttu-id="61cbc-689">En aquest escenari, creareu un projecte, un membre de l'equip, quatre tasques i dues assignacions de recursos.</span><span class="sxs-lookup"><span data-stu-id="61cbc-689">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="61cbc-690">A continuació, actualitzareu una tasca, actualitzareu el projecte, suprimireu una tasca, suprimireu una assignació de recursos i creareu una dependència de tasca.</span><span class="sxs-lookup"><span data-stu-id="61cbc-690">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

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

## <a name="additional-samples"></a><span data-ttu-id="61cbc-691">Exemples addicionals</span><span class="sxs-lookup"><span data-stu-id="61cbc-691">Additional samples</span></span>

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
