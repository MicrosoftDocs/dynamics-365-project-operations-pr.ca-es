---
title: Utilitzar les API de planificació de projectes per fer operacions amb entitats de planificació
description: En aquest tema es proporciona informació i exemples per utilitzar les API de planificació de projectes.
author: sigitac
ms.date: 06/22/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4915261c08a3271a919e04084e92a14b297c1b35
ms.sourcegitcommit: 2f16c2bc7c8350676a6a380c61fffa9958db6a0b
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/22/2021
ms.locfileid: "6293215"
---
# <a name="use-project-schedule-apis-to-perform-operations-with-scheduling-entities"></a>Utilitzar les API de planificació de projectes per fer operacions amb entitats de planificació

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

> [!IMPORTANT] 
> Algunes de les funcionalitats que s'indiquen en aquest tema estan disponibles com a part d'una versió preliminar. El contingut i la funcionalitat estan subjectes a canvis. 

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

- **msdyn_CreateProjectV1**: aquesta API es pot utilitzar per crear un projecte. El projecte i el dipòsit per defecte del projecte es creen immediatament.
- **msdyn_CreateTeamMemberV1**: aquesta API es pot utilitzar per crear un membre de l'equip del projecte. El registre del membre de l'equip es crea immediatament.
- **msdyn_CreateOperationSetV1**: aquesta API es pot utilitzar per planificar diverses sol·licituds que s'han de fer dins d'una transacció.
- **msdyn_PSSCreateV1**: aquesta API es pot utilitzar per crear una entitat. L'entitat pot ser qualsevol de les entitats de planificació de projectes que admeten l'operació de creació.
- **msdyn_PSSUpdateV1**: aquesta API es pot utilitzar per actualitzar una entitat. L'entitat pot ser qualsevol de les entitats de planificació de projectes que admeten l'operació d'actualització.
- **msdyn_PSSDeleteV1**: aquesta API es pot utilitzar per suprimir una entitat. L'entitat pot ser qualsevol de les entitats de planificació de projectes que admeten l'operació de supressió.
- **msdyn_ExecuteOperationSetV1**: aquesta API s'utilitza per executar totes les operacions dins del conjunt d'operacions determinat.

## <a name="using-project-schedule-apis-with-operationset"></a>Utilitzar API de planificació de projectes amb OperationSet

Com que els registres amb **CreateProjectV1** i **CreateTeamMemberV1** es creen immediatament, aquestes API no es poden utilitzar directament a **OperationSet**. Tanmateix, podeu utilitzar l'API per crear els registres necessaris, crear un **OperationSet** i, a continuació, utilitzar aquests registres creats a **OperationSet**.

## <a name="supported-operations"></a>Operacions admeses

| Entitat de planificació | Creació | Actualització | Delete | Consideracions importants |
| --- | --- | --- | --- | --- |
Tasca del projecte | Sí | Sí | Sí | Cap |
| Dependència de les tasques del projecte | Sí | Sí | | Els registres de dependència de les tasques del projecte no s'actualitzen. En lloc d'això, es pot suprimir un registre antic i crear-ne un de nou. |
| Assignació de recursos | Sí | Sí | | No s'admeten les operacions amb els camps següents: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** i **PlannedWork**. Els registres d'assignació de recursos no s'actualitzen. En lloc d'això, es pot suprimir el registre antic i crear-ne un de nou. |
| Dipòsit de projecte | N/D | N/D | N/D | El dipòsit per defecte es crea amb l'API **CreateProjectV1**. |
| Membre de l'equip del projecte | Sí | Sí | Sí | Per a l'operació de creació, utilitzeu l'API **CreateTeamMemberV1**. |
| Project | Sí | Sí | N/D | Les operacions amb els camps següents no estan admeses: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** i **Duration**. |

Aquestes API es poden cridar amb objectes d'entitat que inclouen camps personalitzats.

La propietat ID és opcional. Si es proporciona, el sistema intenta utilitzar-la i llança una excepció si no es pot utilitzar. Si no es proporciona, el sistema la generarà.

## <a name="restricted-fields"></a>Camps restringits

Les taules següents defineixen els camps restringits de **Crear** i **Editar.**

### <a name="project-task"></a>Tasca del projecte

| **Nom lògic**                       | **Pot crear** | **Pot editar**     |
|----------------------------------------|----------------|------------------|
| msdyn_actualcost                       | no             | no               |
| msdyn_actualcost_base                  | no             | no               |
| msdyn_actualend                        | no             | no               |
| msdyn_actualsales                      | no             | no               |
| msdyn_actualsales_base                 | no             | no               |
| msdyn_actualstart                      | no             | no               |
| msdyn_costatcompleteestimate           | no             | no               |
| msdyn_costatcompleteestimate_base      | no             | no               |
| msdyn_costconsumptionpercentage        | no             | no               |
| msdyn_effortcompleted                  | no             | no               |
| msdyn_effortestimateatcomplete         | no             | no               |
| msdyn_iscritical                       | no             | no               |
| msdyn_iscriticalname                   | no             | no               |
| msdyn_ismanual                         | no             | no               |
| msdyn_ismanualname                     | no             | no               |
| msdyn_ismilestone                      | no             | no               |
| msdyn_ismilestonename                  | no             | no               |
| msdyn_LinkStatus                       | no             | no               |
| msdyn_linkstatusname                   | no             | no               |
| msdyn_msprojectclientid                | no             | no               |
| msdyn_plannedcost                      | no             | no               |
| msdyn_plannedcost_base                 | no             | no               |
| msdyn_plannedsales                     | no             | no               |
| msdyn_plannedsales_base                | no             | no               |
| msdyn_pluginprocessingdata             | no             | no               |
| msdyn_progress                         | no             | no (sí per a P4W) |
| msdyn_remainingcost                    | no             | no               |
| msdyn_remainingcost_base               | no             | no               |
| msdyn_remainingsales                   | no             | no               |
| msdyn_remainingsales_base              | no             | no               |
| msdyn_requestedhours                   | no             | no               |
| msdyn_resourcecategory                 | no             | no               |
| msdyn_resourcecategoryname             | no             | no               |
| msdyn_resourceorganizationalunitid     | no             | no               |
| msdyn_resourceorganizationalunitidname | no             | no               |
| msdyn_salesconsumptionpercentage       | no             | no               |
| msdyn_salesestimateatcomplete          | no             | no               |
| msdyn_salesestimateatcomplete_base     | no             | no               |
| msdyn_salesvariance                    | no             | no               |
| msdyn_salesvariance_base               | no             | no               |
| msdyn_scheduleddurationminutes         | no             | no               |
| msdyn_scheduledend                     | no             | no               |
| msdyn_scheduledstart                   | no             | no               |
| msdyn_schedulevariance                 | no             | no               |
| msdyn_skipupdateestimateline           | no             | no               |
| msdyn_skipupdateestimatelinename       | no             | no               |
| msdyn_summary                          | no             | no               |
| msdyn_varianceofcost                   | no             | no               |
| msdyn_varianceofcost_base              | no             | no               |

### <a name="project-task-dependency"></a>Dependència de les tasques del projecte

| **Nom lògic**              | **Pot crear** | **Pot editar** |
|-------------------------------|----------------|--------------|
| msdyn_linktype                | no             | no           |
| msdyn_linktypename            | no             | no           |
| msdyn_predecessortask         | sí            | no           |
| msdyn_predecessortaskname     | sí            | no           |
| msdyn_project                 | sí            | no           |
| msdyn_projectname             | sí            | no           |
| msdyn_projecttaskdependencyid | sí            | no           |
| msdyn_successortask           | sí            | no           |
| msdyn_successortaskname       | sí            | no           |

### <a name="resource-assignment"></a>Assignació de recursos

| **Nom lògic**             | **Pot crear** | **Pot editar** |
|------------------------------|----------------|--------------|
| msdyn_bookableresourceid     | sí            | no           |
| msdyn_bookableresourceidname | sí            | no           |
| msdyn_bookingstatusid        | no             | no           |
| msdyn_bookingstatusidname    | no             | no           |
| msdyn_committype             | no             | no           |
| msdyn_committypename         | no             | no           |
| msdyn_effort                 | no             | no           |
| msdyn_effortcompleted        | no             | no           |
| msdyn_effortremaining        | no             | no           |
| msdyn_finish                 | no             | no           |
| msdyn_plannedcost            | no             | no           |
| msdyn_plannedcost_base       | no             | no           |
| msdyn_plannedcostcontour     | no             | no           |
| msdyn_plannedsales           | no             | no           |
| msdyn_plannedsales_base      | no             | no           |
| msdyn_plannedsalescontour    | no             | no           |
| msdyn_plannedwork            | no             | no           |
| msdyn_projectid              | sí            | no           |
| msdyn_projectidname          | no             | no           |
| msdyn_projectteamid          | no             | no           |
| msdyn_projectteamidname      | no             | no           |
| msdyn_start                  | no             | no           |
| msdyn_taskid                 | no             | no           |
| msdyn_taskidname             | no             | no           |
| msdyn_userresourceid         | no             | no           |

### <a name="project-team-member"></a>Membre de l'equip del projecte

| **Nom lògic**                                 | **Pot crear** | **Pot editar** |
|--------------------------------------------------|----------------|--------------|
| msdyn_calendarid                                 | no             | no           |
| msdyn_creategenericteammemberwithrequirementname | no             | no           |
| msdyn_deletestatus                               | no             | no           |
| msdyn_deletestatusname                           | no             | no           |
| msdyn_effort                                     | no             | no           |
| msdyn_effortcompleted                            | no             | no           |
| msdyn_effortremaining                            | no             | no           |
| msdyn_finish                                     | no             | no           |
| msdyn_hardbookedhours                            | no             | no           |
| msdyn_hours                                      | no             | no           |
| msdyn_markedfordeletiontimer                     | no             | no           |
| msdyn_markedfordeletiontimestamp                 | no             | no           |
| msdyn_msprojectclientid                          | no             | no           |
| msdyn_percentage                                 | no             | no           |
| msdyn_requiredhours                              | no             | no           |
| msdyn_softbookedhours                            | no             | no           |
| msdyn_start                                      | no             | no           |

### <a name="project"></a>Project

| **Nom lògic**                       | **Pot crear** | **Pot editar** |
|----------------------------------------|----------------|--------------|
| msdyn_actualexpensecost                | no             | no           |
| msdyn_actualexpensecost_base           | no             | no           |
| msdyn_actuallaborcost                  | no             | no           |
| msdyn_actuallaborcost_base             | no             | no           |
| msdyn_actualsales                      | no             | no           |
| msdyn_actualsales_base                 | no             | no           |
| msdyn_contractlineproject              | sí            | no           |
| msdyn_contractorganizationalunitid     | sí            | no           |
| msdyn_contractorganizationalunitidname | sí            | no           |
| msdyn_costconsumption                  | no             | no           |
| msdyn_costestimateatcomplete           | no             | no           |
| msdyn_costestimateatcomplete_base      | no             | no           |
| msdyn_costvariance                     | no             | no           |
| msdyn_costvariance_base                | no             | no           |
| msdyn_duration                         | no             | no           |
| msdyn_effort                           | no             | no           |
| msdyn_effortcompleted                  | no             | no           |
| msdyn_effortestimateatcompleteeac      | no             | no           |
| msdyn_effortremaining                  | no             | no           |
| msdyn_finish                           | sí            | sí          |
| msdyn_globalrevisiontoken              | no             | no           |
| msdyn_islinkedtomsprojectclient        | no             | no           |
| msdyn_islinkedtomsprojectclientname    | no             | no           |
| msdyn_linkeddocumenturl                | no             | no           |
| msdyn_msprojectdocument                | no             | no           |
| msdyn_msprojectdocumentname            | no             | no           |
| msdyn_plannedexpensecost               | no             | no           |
| msdyn_plannedexpensecost_base          | no             | no           |
| msdyn_plannedlaborcost                 | no             | no           |
| msdyn_plannedlaborcost_base            | no             | no           |
| msdyn_plannedsales                     | no             | no           |
| msdyn_plannedsales_base                | no             | no           |
| msdyn_progress                         | no             | no           |
| msdyn_remainingcost                    | no             | no           |
| msdyn_remainingcost_base               | no             | no           |
| msdyn_remainingsales                   | no             | no           |
| msdyn_remainingsales_base              | no             | no           |
| msdyn_replaylogheader                  | no             | no           |
| msdyn_salesconsumption                 | no             | no           |
| msdyn_salesestimateatcompleteeac       | no             | no           |
| msdyn_salesestimateatcompleteeac_base  | no             | no           |
| msdyn_salesvariance                    | no             | no           |
| msdyn_salesvariance_base               | no             | no           |
| msdyn_scheduleperformance              | no             | no           |
| msdyn_scheduleperformancename          | no             | no           |
| msdyn_schedulevariance                 | no             | no           |
| msdyn_taskearlieststart                | no             | no           |
| msdyn_teamsize                         | no             | no           |
| msdyn_teamsize_date                    | no             | no           |
| msdyn_teamsize_state                   | no             | no           |
| msdyn_totalactualcost                  | no             | no           |
| msdyn_totalactualcost_base             | no             | no           |
| msdyn_totalplannedcost                 | no             | no           |
| msdyn_totalplannedcost_base            | no             | no           |


## <a name="limitations-and-known-issues"></a>Limitacions i problemes coneguts
A continuació es mostra una llista de limitacions i problemes coneguts:

- Només els **Usuaris amb llicència del Microsoft Project** poden utilitzar les API de planificació de projectes. No les poden utilitzar:
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
