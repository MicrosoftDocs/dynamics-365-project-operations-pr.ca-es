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
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a>Ús de les API de planificació per realitzar operacions amb entitats de Planificació

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

> [!IMPORTANT] 
> Algunes de les funcionalitats que s'indiquen en aquest tema estan disponibles com a part d'una versió preliminar. El contingut i la funcionalitat estan subjectes a canvis. 

## <a name="scheduling-entities"></a>Entitats de planificació

Les API de Planificació proporcionen la capacitat de crear, actualitzar i suprimir operacions amb **Entitats de planificació**. Aquestes entitats s'administren mitjançant el motor de Planificació del Projecte for the web. Les operacions de creació, actualització i supressió amb **Entitats de planificació** es van restringir a les versions anteriors del Dynamics 365 Project Operations.

La taula següent proporciona una llista completa de les **Entitats de planificació**.

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

## <a name="schedule-apis"></a>API de Planificació

A continuació es mostra una llista de les API de Planificació actuals.

- **msdyn_CreateProjectV1**: aquesta API es pot utilitzar per crear un projecte. El projecte i el dipòsit per defecte del projecte es creen immediatament.
- **msdyn_CreateTeamMemberV1**: aquesta API es pot utilitzar per crear un membre de l'equip del projecte. El registre del membre de l'equip es crea immediatament.
- **msdyn_CreateOperationSetV1**: aquesta API es pot utilitzar per planificar diverses sol·licituds que s'han de fer dins d'una transacció.
- **msdyn_PSSCreateV1**: aquesta API es pot utilitzar per crear una entitat. L'entitat pot ser qualsevol de les entitats de Planificació que admeten l'operació de creació.
- **msdyn_PSSUpdateV1**: aquesta API es pot utilitzar per actualitzar una entitat. L'entitat pot ser qualsevol de les entitats de Planificació que admeten l'operació d'actualització.
- **msdyn_PSSDeleteV1**: aquesta API es pot utilitzar per suprimir una entitat. L'entitat pot ser qualsevol de les entitats de Planificació que admeten l'operació de supressió.
- **msdyn_ExecuteOperationSetV1**: aquesta API s'utilitza per executar totes les operacions dins del conjunt d'operacions determinat.

## <a name="using-schedule-apis-with-operationset"></a>Ús de les API de Planificació amb OperationSet

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

## <a name="limitations-and-known-issues"></a>Limitacions i problemes coneguts
A continuació es mostra una llista de limitacions i problemes coneguts:

- Només poden utilitzar les API de Planificació els **Usuaris amb llicència del Microsoft Project**. No les poden utilitzar:
    - Usuaris de l'aplicació
    - Usuaris del sistema
    - Usuaris d'integració
    - Altres usuaris que no tenen la llicència necessària
- Cada **OperationSet** només pot tenir un màxim de 100 operacions.
- Cada usuari només pot tenir un màxim de 10 **OperationSets** oberts.
- El Project Operations actualment admet un màxim de 500 tasques totals en un projecte.
- Actualment no hi ha estats d'error i registres d'error d'**OperationSet** disponibles.
- Les API de Planificació es troben a la versió preliminar pública. Microsoft no admet l'ús d'aquestes d'aquestes API en un entorn de producció.

## <a name="sample-scenario"></a>Escenari d'exemple

En aquest escenari, creareu un projecte, un membre de l'equip, quatre tasques i dues assignacions de recursos. A continuació, actualitzareu una tasca, actualitzareu el projecte, suprimireu una tasca, suprimireu una assignació de recursos i creareu una dependència de tasca.

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

## <a name="additional-samples"></a>Exemples addicionals

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
