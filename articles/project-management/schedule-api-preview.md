---
title: Utilitzar les API de planificació de projectes per fer operacions amb entitats de planificació
description: En aquest article es proporciona informació i mostres per utilitzar les API de planificació del projecte.
author: sigitac
ms.date: 01/13/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: ada06186121d41edddaa06f747b3e1687c303928
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929202"
---
# <a name="use-project-schedule-apis-to-perform-operations-with-scheduling-entities"></a>Utilitzar les API de planificació de projectes per fer operacions amb entitats de planificació

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_



## <a name="scheduling-entities"></a>Entitats de planificació

Les API de planificació de projectes proporcionen la capacitat de crear, actualitzar i suprimir operacions amb **Entitats de planificació**. Aquestes entitats s'administren mitjançant el motor de Planificació del Projecte for the web. Les operacions de creació, actualització i supressió amb **Entitats de planificació** es van restringir a les versions anteriors del Dynamics 365 Project Operations.

A la taula següent es proporciona una llista completa de les entitats de planificació de projectes.

| Nom de l’entitat  | Nom lògic de l’entitat |
| --- | --- |
| Project | msdyn_project |
| Tasca del projecte  | msdyn_projecttask  |
| Dependència de les tasques del projecte  | msdyn_projecttaskdependency  |
| Assignació de recursos | msdyn_resourceassignment |
| Dipòsit de projecte  | msdyn_projectbucket |
| Membre de l'equip del projecte | msdyn_projectteam |

## <a name="operationset"></a>OperationSet

OperationSet és un patró d'unitat de treball que es pot utilitzar quan diverses sol·licituds que afecten la planificació s'han de processar dins d'una transacció.

## <a name="project-schedule-apis"></a>API de planificació de projectes

A continuació es mostra una llista de les API de planificació de projectes actuals.

- **msdyn_CreateProjectV1**: aquesta API es pot utilitzar per crear un projecte. El projecte i el cub del projecte per defecte es creen immediatament.
- **msdyn_CreateTeamMemberV1**: aquesta API es pot utilitzar per crear un membre de l'equip del projecte. El registre del membre de l'equip es crea immediatament.
- **msdyn_CreateOperationSetV1**: aquesta API es pot utilitzar per planificar diverses sol·licituds que s'han de fer dins d'una transacció.
- **msdyn_PSSCreateV1**: aquesta API es pot utilitzar per crear una entitat. L'entitat pot ser qualsevol de les entitats de planificació de projectes que admeten l'operació de creació.
- **msdyn_PSSUpdateV1**: aquesta API es pot utilitzar per actualitzar una entitat. L'entitat pot ser qualsevol de les entitats de planificació de projectes que admeten l'operació d'actualització.
- **msdyn_PSSDeleteV1**: aquesta API es pot utilitzar per suprimir una entitat. L'entitat pot ser qualsevol de les entitats de planificació de projectes que admeten l'operació de supressió.
- **msdyn_ExecuteOperationSetV1**: aquesta API s'utilitza per executar totes les operacions dins del conjunt d'operacions determinat.

## <a name="using-project-schedule-apis-with-operationset"></a>Utilitzar API de planificació de projectes amb OperationSet

Com que els registres amb **CreateProjectV1** i **CreateTeamMemberV1** es creen immediatament, aquestes API no es poden utilitzar directament a **OperationSet**. Tanmateix, podeu utilitzar l'API per crear els registres necessaris, crear un **OperationSet** i, a continuació, utilitzar aquests registres creats a **OperationSet**.

## <a name="supported-operations"></a>Operacions admeses

| Entitat de planificació | Creació | Update | Delete | Consideracions importants |
| --- | --- | --- | --- | --- |
Tasca del projecte | Sí | Sí | Sí | Els **camps Progrés**, **EsforçCompletat** i **EsforçRemaining** es poden editar al Project for the Web, però no es poden editar a Operacions del projecte.  |
| Dependència de les tasques del projecte | Sí |  | Sí | Els registres de dependència de les tasques del projecte no s'actualitzen. En lloc d'això, es pot suprimir un registre antic i crear un registre nou. |
| Assignació de recursos | Sí | Sí | | No s'admeten les operacions amb els camps següents: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** i **PlannedWork**. Els registres d'assignació de recursos no s'actualitzen. En lloc d'això, es pot suprimir el registre antic i es pot crear un registre nou. |
| Dipòsit de projecte | Sí | Sí | Sí | El cub per defecte es crea mitjançant l'API **CreateProjectV1**. El suport per crear i suprimir cubs de projectes s'ha afegit a la versió d'actualització 16. |
| Membre de l'equip del projecte | Sí | Sí | Sí | Per a l'operació de creació, utilitzeu l'API **CreateTeamMemberV1**. |
| Project | Sí | Sí |  | Les operacions amb els camps següents no estan admeses: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** i **Duration**. |

Aquestes API es poden cridar amb objectes d'entitat que inclouen camps personalitzats.

La propietat ID és opcional. Si es proporciona, el sistema intenta utilitzar-la i llança una excepció si no es pot utilitzar. Si no es proporciona, el sistema la generarà.

## <a name="restricted-fields"></a>Camps restringits

Les taules següents defineixen els camps restringits des de **Crea** i **Edita**.

### <a name="project-task"></a>Tasca del projecte

| Nom lògic                           | Es pot crear     | Pot editar         |
|----------------------------------------|----------------|------------------|
| msdyn_actualcost                       | No             | No               |
| msdyn_actualcost_base                  | No             | No               |
| msdyn_actualend                        | No             | No               |
| msdyn_actualsales                      | No             | No               |
| msdyn_actualsales_base                 | No             | No               |
| msdyn_actualstart                      | No             | No               |
| msdyn_costatcompleteestimate           | No             | No               |
| msdyn_costatcompleteestimate_base      | No             | No               |
| msdyn_costconsumptionpercentage        | No             | No               |
| msdyn_effortcompleted                  | No (sí al projecte)             | No (sí al projecte)               |
| msdyn_effortremaining                  | No (sí al projecte)              | No (sí al projecte)                |
| msdyn_effortestimateatcomplete         | No             | No               |
| msdyn_iscritical                       | No             | No               |
| msdyn_iscriticalname                   | No             | No               |
| msdyn_ismanual                         | No             | No               |
| msdyn_ismanualname                     | No             | No               |
| msdyn_ismilestone                      | No             | No               |
| msdyn_ismilestonename                  | No             | No               |
| msdyn_LinkStatus                       | No             | No               |
| msdyn_linkstatusname                   | No             | No               |
| msdyn_msprojectclientid                | No             | No               |
| msdyn_plannedcost                      | No             | No               |
| msdyn_plannedcost_base                 | No             | No               |
| msdyn_plannedsales                     | No             | No               |
| msdyn_plannedsales_base                | No             | No               |
| msdyn_pluginprocessingdata             | No             | No               |
| msdyn_progress                         | No (sí al projecte)             | No (sí al projecte) |
| msdyn_remainingcost                    | No             | No               |
| msdyn_remainingcost_base               | No             | No               |
| msdyn_remainingsales                   | No             | No               |
| msdyn_remainingsales_base              | No             | No               |
| msdyn_requestedhours                   | No             | No               |
| msdyn_resourcecategory                 | No             | No               |
| msdyn_resourcecategoryname             | No             | No               |
| msdyn_resourceorganizationalunitid     | No             | No               |
| msdyn_resourceorganizationalunitidname | No             | No               |
| msdyn_salesconsumptionpercentage       | No             | No               |
| msdyn_salesestimateatcomplete          | No             | No               |
| msdyn_salesestimateatcomplete_base     | No             | No               |
| msdyn_salesvariance                    | No             | No               |
| msdyn_salesvariance_base               | No             | No               |
| msdyn_scheduleddurationminutes         | No             | No               |
| msdyn_scheduledend                     | No             | No               |
| msdyn_scheduledstart                   | No             | No               |
| msdyn_schedulevariance                 | No             | No               |
| msdyn_skipupdateestimateline           | No             | No               |
| msdyn_skipupdateestimatelinename       | No             | No               |
| msdyn_summary                          | No             | No               |
| msdyn_varianceofcost                   | No             | No               |
| msdyn_varianceofcost_base              | No             | No               |

### <a name="project-task-dependency"></a>Dependència de les tasques del projecte

| Nom lògic                  | Es pot crear     | Pot editar     |
|-------------------------------|----------------|--------------|
| msdyn_linktype                | No             | No           |
| msdyn_linktypename            | No             | No           |
| msdyn_predecessortask         | Sí            | No           |
| msdyn_predecessortaskname     | Sí            | No           |
| msdyn_project                 | Sí            | No           |
| msdyn_projectname             | Sí            | No           |
| msdyn_projecttaskdependencyid | Sí            | No           |
| msdyn_successortask           | Sí            | No           |
| msdyn_successortaskname       | Sí            | No           |

### <a name="resource-assignment"></a>Assignació de recursos

| Nom lògic                 | Es pot crear     | Pot editar     |
|------------------------------|----------------|--------------|
| msdyn_bookableresourceid     | Sí            | No           |
| msdyn_bookableresourceidname | Sí            | No           |
| msdyn_bookingstatusid        | No             | No           |
| msdyn_bookingstatusidname    | No             | No           |
| msdyn_committype             | No             | No           |
| msdyn_committypename         | No             | No           |
| msdyn_effort                 | No             | No           |
| msdyn_effortcompleted        | No             | No           |
| msdyn_effortremaining        | No             | No           |
| msdyn_finish                 | No             | No           |
| msdyn_plannedcost            | No             | No           |
| msdyn_plannedcost_base       | No             | No           |
| msdyn_plannedcostcontour     | No             | No           |
| msdyn_plannedsales           | No             | No           |
| msdyn_plannedsales_base      | No             | No           |
| msdyn_plannedsalescontour    | No             | No           |
| msdyn_plannedwork            | No             | No           |
| msdyn_projectid              | Sí            | No           |
| msdyn_projectidname          | No             | No           |
| msdyn_projectteamid          | No             | No           |
| msdyn_projectteamidname      | No             | No           |
| msdyn_start                  | No             | No           |
| msdyn_taskid                 | No             | No           |
| msdyn_taskidname             | No             | No           |
| msdyn_userresourceid         | No             | No           |

### <a name="project-team-member"></a>Membre de l'equip del projecte

| Nom lògic                                     | Es pot crear     | Pot editar     |
|--------------------------------------------------|----------------|--------------|
| msdyn_calendarid                                 | No             | No           |
| msdyn_creategenericteammemberwithrequirementname | No             | No           |
| msdyn_deletestatus                               | No             | No           |
| msdyn_deletestatusname                           | No             | No           |
| msdyn_effort                                     | No             | No           |
| msdyn_effortcompleted                            | No             | No           |
| msdyn_effortremaining                            | No             | No           |
| msdyn_finish                                     | No             | No           |
| msdyn_hardbookedhours                            | No             | No           |
| msdyn_hours                                      | No             | No           |
| msdyn_markedfordeletiontimer                     | No             | No           |
| msdyn_markedfordeletiontimestamp                 | No             | No           |
| msdyn_msprojectclientid                          | No             | No           |
| msdyn_percentage                                 | No             | No           |
| msdyn_requiredhours                              | No             | No           |
| msdyn_softbookedhours                            | No             | No           |
| msdyn_start                                      | No             | No           |

### <a name="project"></a>Project

| Nom lògic                           | Es pot crear     | Pot editar     |
|----------------------------------------|----------------|--------------|
| msdyn_actualexpensecost                | No             | No           |
| msdyn_actualexpensecost_base           | No             | No           |
| msdyn_actuallaborcost                  | No             | No           |
| msdyn_actuallaborcost_base             | No             | No           |
| msdyn_actualsales                      | No             | No           |
| msdyn_actualsales_base                 | No             | No           |
| msdyn_contractlineproject              | Sí            | No           |
| msdyn_contractorganizationalunitid     | Sí            | No           |
| msdyn_contractorganizationalunitidname | Sí            | No           |
| msdyn_costconsumption                  | No             | No           |
| msdyn_costestimateatcomplete           | No             | No           |
| msdyn_costestimateatcomplete_base      | No             | No           |
| msdyn_costvariance                     | No             | No           |
| msdyn_costvariance_base                | No             | No           |
| msdyn_duration                         | No             | No           |
| msdyn_effort                           | No             | No           |
| msdyn_effortcompleted                  | No             | No           |
| msdyn_effortestimateatcompleteeac      | No             | No           |
| msdyn_effortremaining                  | No             | No           |
| msdyn_finish                           | Sí            | Sí          |
| msdyn_globalrevisiontoken              | No             | No           |
| msdyn_islinkedtomsprojectclient        | No             | No           |
| msdyn_islinkedtomsprojectclientname    | No             | No           |
| msdyn_linkeddocumenturl                | No             | No           |
| msdyn_msprojectdocument                | No             | No           |
| msdyn_msprojectdocumentname            | No             | No           |
| msdyn_plannedexpensecost               | No             | No           |
| msdyn_plannedexpensecost_base          | No             | No           |
| msdyn_plannedlaborcost                 | No             | No           |
| msdyn_plannedlaborcost_base            | No             | No           |
| msdyn_plannedsales                     | No             | No           |
| msdyn_plannedsales_base                | No             | No           |
| msdyn_progress                         | No             | No           |
| msdyn_remainingcost                    | No             | No           |
| msdyn_remainingcost_base               | No             | No           |
| msdyn_remainingsales                   | No             | No           |
| msdyn_remainingsales_base              | No             | No           |
| msdyn_replaylogheader                  | No             | No           |
| msdyn_salesconsumption                 | No             | No           |
| msdyn_salesestimateatcompleteeac       | No             | No           |
| msdyn_salesestimateatcompleteeac_base  | No             | No           |
| msdyn_salesvariance                    | No             | No           |
| msdyn_salesvariance_base               | No             | No           |
| msdyn_scheduleperformance              | No             | No           |
| msdyn_scheduleperformancename          | No             | No           |
| msdyn_schedulevariance                 | No             | No           |
| msdyn_taskearlieststart                | No             | No           |
| msdyn_teamsize                         | No             | No           |
| msdyn_teamsize_date                    | No             | No           |
| msdyn_teamsize_state                   | No             | No           |
| msdyn_totalactualcost                  | No             | No           |
| msdyn_totalactualcost_base             | No             | No           |
| msdyn_totalplannedcost                 | No             | No           |
| msdyn_totalplannedcost_base            | No             | No           |

### <a name="project-bucket"></a>Dipòsit de projecte

| Nom lògic          | Es pot crear      | Pot editar     |
|-----------------------|-----------------|--------------|
| msdyn_displayorder    | Sí             | No           |
| msdyn_name            | Sí             | Sí          |
| msdyn_project         | Sí             | No           |
| msdyn_projectbucketid | Sí             | No           |

## <a name="limitations-and-known-issues"></a>Limitacions i problemes coneguts
A continuació es mostra una llista de limitacions i problemes coneguts:

- Les API de planificació del projecte només les poden utilitzar **els usuaris amb llicència** de projecte de Microsoft. No les poden utilitzar:

    - Usuaris de l'aplicació
    - Usuaris del sistema
    - Usuaris d'integració
    - Altres usuaris que no tenen la llicència necessària

- Cada **OperationSet** només pot tenir un màxim de 100 operacions.
- Cada usuari només pot tenir un màxim de 10 **OperationSets** oberts.
- El Project Operations actualment admet un màxim de 500 tasques totals en un projecte.
- Actualment no hi ha estats d'error i registres d'error d'**OperationSet** disponibles.
- [Límits dels projectes i tasques](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a>Gestió d'errors

- Per revisar els errors generats a partir dels conjunts d'operacions, aneu a **Configuració** \> **Integració de la planificació** \> **Conjunts d'operacions**.
- Per revisar els errors generats a partir del servei de planificació de projectes, aneu a **Configuració** \> **Integració de la planificació** \> **Registres d’errors de PSS**.

## <a name="sample-scenario"></a>Escenari d'exemple

En aquest escenari, creareu un projecte, un membre de l'equip, quatre tasques i dues assignacions de recursos. A continuació, actualitzareu una tasca, actualitzareu el projecte, suprimireu una tasca, suprimireu una assignació de recursos i creareu una dependència de tasca.

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

## <a name="additional-samples"></a>Exemples addicionals

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
