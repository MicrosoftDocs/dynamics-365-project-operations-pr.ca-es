---
title: Ús de les API de planificació per realitzar operacions amb entitats de Planificació
description: En aquest tema es proporciona informació i exemples per utilitzar les API de Planificació.
author: sigitac
manager: Annbe
ms.date: 04/07/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a50a2c6220bb49de8146d0758019827e120e0526
ms.sourcegitcommit: 8ff9fe396db6dec581c21cd6bb9acc2691c815b0
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/07/2021
ms.locfileid: "5868117"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="f3753-103">Ús de les API de planificació per realitzar operacions amb entitats de Planificació</span><span class="sxs-lookup"><span data-stu-id="f3753-103">Use Schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="f3753-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_</span><span class="sxs-lookup"><span data-stu-id="f3753-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="f3753-105">Algunes de les funcionalitats que s'indiquen en aquest tema estan disponibles com a part d'una versió preliminar.</span><span class="sxs-lookup"><span data-stu-id="f3753-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="f3753-106">El contingut i la funcionalitat estan subjectes a canvis.</span><span class="sxs-lookup"><span data-stu-id="f3753-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="f3753-107">Entitats de planificació</span><span class="sxs-lookup"><span data-stu-id="f3753-107">Scheduling entities</span></span>

<span data-ttu-id="f3753-108">Les API de Planificació proporcionen la capacitat de crear, actualitzar i suprimir operacions amb **Entitats de planificació**.</span><span class="sxs-lookup"><span data-stu-id="f3753-108">Schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="f3753-109">Aquestes entitats s'administren mitjançant el motor de Planificació del Projecte for the web.</span><span class="sxs-lookup"><span data-stu-id="f3753-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="f3753-110">Les operacions de creació, actualització i supressió amb **Entitats de planificació** es van restringir a les versions anteriors del Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="f3753-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="f3753-111">La taula següent proporciona una llista completa de les **Entitats de planificació**.</span><span class="sxs-lookup"><span data-stu-id="f3753-111">The following table provides a full list of the **Scheduling entities**.</span></span>

| <span data-ttu-id="f3753-112">Nom de l’entitat</span><span class="sxs-lookup"><span data-stu-id="f3753-112">Entity name</span></span>  | <span data-ttu-id="f3753-113">Nom lògic de l’entitat</span><span class="sxs-lookup"><span data-stu-id="f3753-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="f3753-114">Project</span><span class="sxs-lookup"><span data-stu-id="f3753-114">Project</span></span> | <span data-ttu-id="f3753-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="f3753-115">msdyn_project</span></span> |
| <span data-ttu-id="f3753-116">Tasca del projecte</span><span class="sxs-lookup"><span data-stu-id="f3753-116">Project Task</span></span>  | <span data-ttu-id="f3753-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="f3753-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="f3753-118">Dependència de les tasques del projecte</span><span class="sxs-lookup"><span data-stu-id="f3753-118">Project Task Dependency</span></span>  | <span data-ttu-id="f3753-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="f3753-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="f3753-120">Assignació de recursos</span><span class="sxs-lookup"><span data-stu-id="f3753-120">Resource Assignment</span></span> | <span data-ttu-id="f3753-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="f3753-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="f3753-122">Dipòsit de projecte</span><span class="sxs-lookup"><span data-stu-id="f3753-122">Project Bucket</span></span>  | <span data-ttu-id="f3753-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="f3753-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="f3753-124">Membre de l'equip del projecte</span><span class="sxs-lookup"><span data-stu-id="f3753-124">Project Team Member</span></span> | <span data-ttu-id="f3753-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="f3753-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="f3753-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="f3753-126">OperationSet</span></span>

<span data-ttu-id="f3753-127">OperationSet és un patró d'unitat de treball que es pot utilitzar quan diverses sol·licituds que afecten la planificació s'han de processar dins d'una transacció.</span><span class="sxs-lookup"><span data-stu-id="f3753-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="schedule-apis"></a><span data-ttu-id="f3753-128">API de Planificació</span><span class="sxs-lookup"><span data-stu-id="f3753-128">Schedule APIs</span></span>

<span data-ttu-id="f3753-129">A continuació es mostra una llista de les API de Planificació actuals.</span><span class="sxs-lookup"><span data-stu-id="f3753-129">The following is a list of current Schedule APIs.</span></span>

- <span data-ttu-id="f3753-130">**msdyn_CreateProjectV1**: aquesta API es pot utilitzar per crear un projecte.</span><span class="sxs-lookup"><span data-stu-id="f3753-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="f3753-131">El projecte i el dipòsit per defecte del projecte es creen immediatament.</span><span class="sxs-lookup"><span data-stu-id="f3753-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="f3753-132">**msdyn_CreateTeamMemberV1**: aquesta API es pot utilitzar per crear un membre de l'equip del projecte.</span><span class="sxs-lookup"><span data-stu-id="f3753-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="f3753-133">El registre del membre de l'equip es crea immediatament.</span><span class="sxs-lookup"><span data-stu-id="f3753-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="f3753-134">**msdyn_CreateOperationSetV1**: aquesta API es pot utilitzar per planificar diverses sol·licituds que s'han de fer dins d'una transacció.</span><span class="sxs-lookup"><span data-stu-id="f3753-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="f3753-135">**msdyn_PSSCreateV1**: aquesta API es pot utilitzar per crear una entitat.</span><span class="sxs-lookup"><span data-stu-id="f3753-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="f3753-136">L'entitat pot ser qualsevol de les entitats de Planificació que admeten l'operació de creació.</span><span class="sxs-lookup"><span data-stu-id="f3753-136">The entity can be any of the Scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="f3753-137">**msdyn_PSSUpdateV1**: aquesta API es pot utilitzar per actualitzar una entitat.</span><span class="sxs-lookup"><span data-stu-id="f3753-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="f3753-138">L'entitat pot ser qualsevol de les entitats de Planificació que admeten l'operació d'actualització.</span><span class="sxs-lookup"><span data-stu-id="f3753-138">The entity can be any of the Scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="f3753-139">**msdyn_PSSDeleteV1**: aquesta API es pot utilitzar per suprimir una entitat.</span><span class="sxs-lookup"><span data-stu-id="f3753-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="f3753-140">L'entitat pot ser qualsevol de les entitats de Planificació que admeten l'operació de supressió.</span><span class="sxs-lookup"><span data-stu-id="f3753-140">The entity can be any of the Scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="f3753-141">**msdyn_ExecuteOperationSetV1**: aquesta API s'utilitza per executar totes les operacions dins del conjunt d'operacions determinat.</span><span class="sxs-lookup"><span data-stu-id="f3753-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-schedule-apis-with-operationset"></a><span data-ttu-id="f3753-142">Ús de les API de Planificació amb OperationSet</span><span class="sxs-lookup"><span data-stu-id="f3753-142">Using Schedule APIs with OperationSet</span></span>

<span data-ttu-id="f3753-143">Com que els registres amb **CreateProjectV1** i **CreateTeamMemberV1** es creen immediatament, aquestes API no es poden utilitzar directament a **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="f3753-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="f3753-144">Tanmateix, podeu utilitzar l'API per crear els registres necessaris, crear un **OperationSet** i, a continuació, utilitzar aquests registres creats a **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="f3753-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="f3753-145">Operacions admeses</span><span class="sxs-lookup"><span data-stu-id="f3753-145">Supported operations</span></span>

| <span data-ttu-id="f3753-146">Entitat de planificació</span><span class="sxs-lookup"><span data-stu-id="f3753-146">Scheduling entity</span></span> | <span data-ttu-id="f3753-147">Creació</span><span class="sxs-lookup"><span data-stu-id="f3753-147">Create</span></span> | <span data-ttu-id="f3753-148">Actualització</span><span class="sxs-lookup"><span data-stu-id="f3753-148">Update</span></span> | <span data-ttu-id="f3753-149">Delete</span><span class="sxs-lookup"><span data-stu-id="f3753-149">Delete</span></span> | <span data-ttu-id="f3753-150">Consideracions importants</span><span class="sxs-lookup"><span data-stu-id="f3753-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="f3753-151">Tasca del projecte</span><span class="sxs-lookup"><span data-stu-id="f3753-151">Project task</span></span> | <span data-ttu-id="f3753-152">Sí</span><span class="sxs-lookup"><span data-stu-id="f3753-152">Yes</span></span> | <span data-ttu-id="f3753-153">Sí</span><span class="sxs-lookup"><span data-stu-id="f3753-153">Yes</span></span> | <span data-ttu-id="f3753-154">Sí</span><span class="sxs-lookup"><span data-stu-id="f3753-154">Yes</span></span> | <span data-ttu-id="f3753-155">Cap</span><span class="sxs-lookup"><span data-stu-id="f3753-155">None</span></span> |
| <span data-ttu-id="f3753-156">Dependència de les tasques del projecte</span><span class="sxs-lookup"><span data-stu-id="f3753-156">Project task dependency</span></span> | <span data-ttu-id="f3753-157">Sí</span><span class="sxs-lookup"><span data-stu-id="f3753-157">Yes</span></span> | <span data-ttu-id="f3753-158">Sí</span><span class="sxs-lookup"><span data-stu-id="f3753-158">Yes</span></span> | | <span data-ttu-id="f3753-159">Els registres de dependència de les tasques del projecte no s'actualitzen.</span><span class="sxs-lookup"><span data-stu-id="f3753-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="f3753-160">En lloc d'això, es pot suprimir un registre antic i crear-ne un de nou.</span><span class="sxs-lookup"><span data-stu-id="f3753-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="f3753-161">Assignació de recursos</span><span class="sxs-lookup"><span data-stu-id="f3753-161">Resource assignment</span></span> | <span data-ttu-id="f3753-162">Sí</span><span class="sxs-lookup"><span data-stu-id="f3753-162">Yes</span></span> | <span data-ttu-id="f3753-163">Sí</span><span class="sxs-lookup"><span data-stu-id="f3753-163">Yes</span></span> | | <span data-ttu-id="f3753-164">No s'admeten les operacions amb els camps següents: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** i **PlannedWork**.</span><span class="sxs-lookup"><span data-stu-id="f3753-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="f3753-165">Els registres d'assignació de recursos no s'actualitzen.</span><span class="sxs-lookup"><span data-stu-id="f3753-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="f3753-166">En lloc d'això, es pot suprimir el registre antic i crear-ne un de nou.</span><span class="sxs-lookup"><span data-stu-id="f3753-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="f3753-167">Dipòsit de projecte</span><span class="sxs-lookup"><span data-stu-id="f3753-167">Project bucket</span></span> | <span data-ttu-id="f3753-168">N/D</span><span class="sxs-lookup"><span data-stu-id="f3753-168">N/A</span></span> | <span data-ttu-id="f3753-169">N/D</span><span class="sxs-lookup"><span data-stu-id="f3753-169">N/A</span></span> | <span data-ttu-id="f3753-170">N/D</span><span class="sxs-lookup"><span data-stu-id="f3753-170">N/A</span></span> | <span data-ttu-id="f3753-171">El dipòsit per defecte es crea amb l'API **CreateProjectV1**.</span><span class="sxs-lookup"><span data-stu-id="f3753-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="f3753-172">Membre de l'equip del projecte</span><span class="sxs-lookup"><span data-stu-id="f3753-172">Project team member</span></span> | <span data-ttu-id="f3753-173">Sí</span><span class="sxs-lookup"><span data-stu-id="f3753-173">Yes</span></span> | <span data-ttu-id="f3753-174">Sí</span><span class="sxs-lookup"><span data-stu-id="f3753-174">Yes</span></span> | <span data-ttu-id="f3753-175">Sí</span><span class="sxs-lookup"><span data-stu-id="f3753-175">Yes</span></span> | <span data-ttu-id="f3753-176">Per a l'operació de creació, utilitzeu l'API **CreateTeamMemberV1**.</span><span class="sxs-lookup"><span data-stu-id="f3753-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="f3753-177">Project</span><span class="sxs-lookup"><span data-stu-id="f3753-177">Project</span></span> | <span data-ttu-id="f3753-178">Sí</span><span class="sxs-lookup"><span data-stu-id="f3753-178">Yes</span></span> | <span data-ttu-id="f3753-179">Sí</span><span class="sxs-lookup"><span data-stu-id="f3753-179">Yes</span></span> | <span data-ttu-id="f3753-180">N/D</span><span class="sxs-lookup"><span data-stu-id="f3753-180">N/A</span></span> | <span data-ttu-id="f3753-181">Les operacions amb els camps següents no estan admeses: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** i **Duration**.</span><span class="sxs-lookup"><span data-stu-id="f3753-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="f3753-182">Aquestes API es poden cridar amb objectes d'entitat que inclouen camps personalitzats.</span><span class="sxs-lookup"><span data-stu-id="f3753-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="f3753-183">La propietat ID és opcional.</span><span class="sxs-lookup"><span data-stu-id="f3753-183">The ID property is optional.</span></span> <span data-ttu-id="f3753-184">Si es proporciona, el sistema intenta utilitzar-la i llança una excepció si no es pot utilitzar.</span><span class="sxs-lookup"><span data-stu-id="f3753-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="f3753-185">Si no es proporciona, el sistema la generarà.</span><span class="sxs-lookup"><span data-stu-id="f3753-185">If it isn't provided, the system will generate it.</span></span>

## <a name="limitations-and-known-issues"></a><span data-ttu-id="f3753-186">Limitacions i problemes coneguts</span><span class="sxs-lookup"><span data-stu-id="f3753-186">Limitations and known issues</span></span>
<span data-ttu-id="f3753-187">A continuació es mostra una llista de limitacions i problemes coneguts:</span><span class="sxs-lookup"><span data-stu-id="f3753-187">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="f3753-188">Només poden utilitzar les API de Planificació els **Usuaris amb llicència del Microsoft Project**.</span><span class="sxs-lookup"><span data-stu-id="f3753-188">Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="f3753-189">No les poden utilitzar:</span><span class="sxs-lookup"><span data-stu-id="f3753-189">They can't be used by:</span></span>
    - <span data-ttu-id="f3753-190">Usuaris de l'aplicació</span><span class="sxs-lookup"><span data-stu-id="f3753-190">Application users</span></span>
    - <span data-ttu-id="f3753-191">Usuaris del sistema</span><span class="sxs-lookup"><span data-stu-id="f3753-191">System users</span></span>
    - <span data-ttu-id="f3753-192">Usuaris d'integració</span><span class="sxs-lookup"><span data-stu-id="f3753-192">Integration users</span></span>
    - <span data-ttu-id="f3753-193">Altres usuaris que no tenen la llicència necessària</span><span class="sxs-lookup"><span data-stu-id="f3753-193">Other users that don't have the required license</span></span>
- <span data-ttu-id="f3753-194">Cada **OperationSet** només pot tenir un màxim de 100 operacions.</span><span class="sxs-lookup"><span data-stu-id="f3753-194">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="f3753-195">Cada usuari només pot tenir un màxim de 10 **OperationSets** oberts.</span><span class="sxs-lookup"><span data-stu-id="f3753-195">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="f3753-196">El Project Operations actualment admet un màxim de 500 tasques totals en un projecte.</span><span class="sxs-lookup"><span data-stu-id="f3753-196">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="f3753-197">Actualment no hi ha estats d'error i registres d'error d'**OperationSet** disponibles.</span><span class="sxs-lookup"><span data-stu-id="f3753-197">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- <span data-ttu-id="f3753-198">Les API de Planificació es troben a la versió preliminar pública.</span><span class="sxs-lookup"><span data-stu-id="f3753-198">Schedule APIs are in Public preview.</span></span> <span data-ttu-id="f3753-199">Microsoft no admet l'ús d'aquestes d'aquestes API en un entorn de producció.</span><span class="sxs-lookup"><span data-stu-id="f3753-199">Using these APIs in a Production environment isn't supported by Microsoft.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="f3753-200">Escenari d'exemple</span><span class="sxs-lookup"><span data-stu-id="f3753-200">Sample scenario</span></span>

<span data-ttu-id="f3753-201">En aquest escenari, creareu un projecte, un membre de l'equip, quatre tasques i dues assignacions de recursos.</span><span class="sxs-lookup"><span data-stu-id="f3753-201">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="f3753-202">A continuació, actualitzareu una tasca, actualitzareu el projecte, suprimireu una tasca, suprimireu una assignació de recursos i creareu una dependència de tasca.</span><span class="sxs-lookup"><span data-stu-id="f3753-202">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

```C#
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
var task4 = GetTask("4ZZ";, projectReference);

var assignment1 = GetResourceAssignment("R1", teamMember, task2, project);
var assignment2 = GetResourceAssignment"R2", teamMember, task3, project);

var task1Response = CallPssCreateAction(task1, operationSetId);
var task2Response = CallPssCreateAction(task2, operationSetId);
var task3Response = CallPssCreateAction(task3, operationSetId);
var task4Response = CallPssCreateAction(task4, operationSetId);

varassignment1Response = CallPssCreateAction(assignment1, operationSetId);
varassignment2Response = CallPssCreateAction(assignment2, operationSetId);

task2["msdyn_subject"] = "Updated Task";
var task2UpdateResponse = CallPssUpdateAction(task2, operationSetId);

project["msdyn_subject"] = $"Proj update {DateTime.Now.ToShortTimeString()}";
var projectUpdateResponse = CallPssUpdateAction(project, operationSetId);

var task4DeleteResponse = CallPssDeleteAction(task4.Id.ToString(), task4.LogicalName, operationSetId);

varassignment2DeleteResponse = CallPssDeleteAction(assignment2.Id.ToString(), assignment2.LogicalName, operationSetId);

var dependency1 = GetTaskDependency(project, task2, task3);
var dependency1Response = CallPssCreateAction(dependency1, operationSetId);

CallExecuteOperationSetAction(operationSetId);
Console.WriteLine("Done....");
```

## <a name="additional-samples"></a><span data-ttu-id="f3753-203">Exemples addicionals</span><span class="sxs-lookup"><span data-stu-id="f3753-203">Additional samples</span></span>

```C#
#region Call actions 

///<summary>
/// Calls the action to create an operationSet
/// </summary>
/// <paramname="projectId">project id for the operations to be included in this operationSet>/param>
/// <paramname="description">description of this operationSet</param>
/// <returns>operationSet id</returns>
privatestring CallCreateOperationSetAction(Guid projectId, string description)
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
/// <paramname="entity">Task or Resource Assignment</param>
/// <paramname="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssCreateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssCreateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary<
/// Calls the action to update an entity, only Task for now
/// </summary>
/// <paramname="entity">Task or Resource Assignment</param>
/// <paramname="operationSetId">operationSet Id</param>
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
/// <summary>
/// <paramname="recordId">Id of the record to be deleted</param>
/// <paramname="entityLogicalName">Entity logical name of the record</param>
/// <paramname="operationSetId">OperationSet Id</param>
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
/// <summary>
/// <paramname="operationSetId">operationSet id</param>
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
/// <paramname="operationSetId">operationSet id</param>
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
/// <paramname="project">Project</param>
/// <returns>project Id</returns>
private Guid CallCreateProjectAction(Entity project)
{
    OrganizationRequest createProjectRequest = new OrganizationRequest("msdyn_CreateProjectV1";
    createProjectRequest["Project"] = project;
    OrganizationResponse response = organizationService.Execute(createProjectRequest);
    var projectId = Guid.Parse((string)response["ProjectId"]);

    return projectId;
}

/// <summary>
/// Calls the action to create a new project team member
/// </summary>
/// <paramname="teamMember">Project team member</param>
/// <returns>project team member Id</returns>
privatestring CallCreateTeamMemberAction(Entity teamMember)
{
    OrganizationRequest request = new OrganizationRequest("msdyn_CreateTeamMemberV1");
    request["TeamMember"] = teamMember;
    OrganizationResponse response = organizationService.Execute(request);
    return (string)response["TeamMemberId"];
}

private OperationSetResponse GetOperationSetResponseFromOrgResponse(OrganizationResponse orgResponse)
{
    return JsonConvert.DeserializeObject><OperationSetResponse>
    ((string)orgResponse.Results["OperationSetResponse";]);
}

private EntityCollection GetDefaultBucket(EntityReference projectReference)
{
    var columnsToFetch = new ColumnSet(";msdyn_project", "msdyn_name");
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
    task["msdyn_effort";] = 4d;
    task["msdyn_scheduledstart"] = DateTime.Today;
    task["msdyn_scheduledend"] = DateTime.Today.AddDays(5);
    task["msdyn_progress"] = 0.34m;
    task["msdyn_start"] = DateTime.Now.AddDays(1);
    task["msdyn_projectbucket"] = GetBucket(projectReference).ToEntityReference();
    task["msdyn_LinkStatus"] = new OptionSetValue(192350000);

    //Custom field handling
    /*
        task["new_custom1"] = "Just my test";
        task[";new_age"] = 98;
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
publicclassOperationSetResponse
{
    [DataMember(Name = "operationSetId")]
    public Guid OperationSetId { get; set; }

    [DataMember(Name = "operationSetDetailId")]
    public Guid OperationSetDetailId { get; set; }

    [DataMember(Name = "operationType")]
    publicstring OperationType { get; set; }

    [DataMember(Name = "recordId")]
    publicstring RecordId { get; set; }

    [DataMember(Name = "correlationId")]
    publicstring CorrelationId { get; set; }
}

#endregion
```
