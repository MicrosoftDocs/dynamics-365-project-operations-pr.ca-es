---
title: Utilitzar les API de planificació de projectes per fer operacions amb entitats de planificació
description: En aquest article es proporciona informació i exemples per utilitzar les API de planificació de projectes.
author: sigitac
ms.date: 01/13/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 159d395efff98f2af780e5ed1e5ab3d6483cba89
ms.sourcegitcommit: b1c26ea57be721c5b0b1a33f2de0380ad102648f
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 09/20/2022
ms.locfileid: "9541112"
---
# <a name="use-project-schedule-apis-to-perform-operations-with-scheduling-entities"></a>Utilitzar les API de planificació de projectes per fer operacions amb entitats de planificació

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_


**Entitats de planificació**

Les API de planificació de projectes proporcionen la capacitat de crear, actualitzar i suprimir operacions amb **Entitats de planificació**. Aquestes entitats s'administren mitjançant el motor de Planificació del Projecte for the web. Les operacions de creació, actualització i supressió amb **Entitats de planificació** es van restringir a les versions anteriors del Dynamics 365 Project Operations.

A la taula següent es proporciona una llista completa de les entitats de planificació de projectes.

| **Nom de l'entitat**         | **Nom lògic de l’entitat**     |
|-------------------------|-----------------------------|
| Project                 | msdyn_project               |
| Tasca del projecte            | msdyn_projecttask           |
| Dependència de les tasques del projecte | msdyn_projecttaskdependency |
| Assignació de recursos     | msdyn_resourceassignment    |
| Dipòsit de projecte          | msdyn_projectbucket         |
| Membre de l'equip del projecte     | msdyn_projectteam           |
| Llistes de comprovació del projecte      | msdyn_projectchecklist      |
| Etiqueta del projecte           | msdyn_projectlabel          |
| Tasca de projecte que s'ha d'etiqueta   | msdyn_projecttasktolabel    |
| Esprint del projecte          | msdyn_projectsprint         |

**OperationSet**

OperationSet és un patró d'unitat de treball que es pot utilitzar quan diverses sol·licituds que afecten la planificació s'han de processar dins d'una transacció.

**API de planificació de projectes**

A continuació es mostra una llista de les API de planificació de projectes actuals.

| **API**                                 | Descripció                                                                                                                       |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| **msdyn_CreateProjectV1**               | Aquesta API s'utilitza per crear un projecte. El projecte i el dipòsit per defecte del projecte es creen immediatament.                         |
| **msdyn_CreateTeamMemberV1**            | Aquesta API s'utilitza per crear un membre de l'equip del projecte. El registre del membre de l'equip es crea immediatament.                                  |
| **msdyn_CreateOperationSetV1**          | Aquesta API s'utilitza per planificar diverses sol·licituds que s'han de fer dins d'una transacció.                                        |
| **msdyn_PssCreateV1**                   | Aquesta API s'utilitza per crear una entitat. L'entitat pot ser qualsevol de les entitats de planificació de projectes que admeten l'operació de creació. |
| **msdyn_PssUpdateV1**                   | Aquesta API s'utilitza per actualitzar una entitat. L'entitat pot ser qualsevol de les entitats de planificació de projectes que admeten l'operació d'actualització  |
| **msdyn_PssDeleteV1**                   | Aquesta API s'utilitza per suprimir una entitat. L'entitat pot ser qualsevol de les entitats de planificació de projectes que admeten l'operació de supressió. |
| **msdyn_ExecuteOperationSetV1**         | Aquesta API s'utilitza per executar totes les operacions dins del conjunt d'operacions determinat.                                                 |
| **msdyn_PssUpdateResourceAssignmentV1** | Aquesta API s'utilitza per actualitzar un contorn de treball planificat d'una assignació de recursos.                                                        |



**Utilitzar API de planificació de projectes amb OperationSet**

Com que els registres amb **CreateProjectV1** i **CreateTeamMemberV1** es creen immediatament, aquestes API no es poden utilitzar directament a **OperationSet**. Tanmateix, podeu utilitzar l'API per crear els registres necessaris, crear un **OperationSet** i, a continuació, utilitzar aquests registres creats a **OperationSet**.

**Operacions admeses**

| **Entitat de planificació**   | **Creació** | **Actualització** | **Delete** | **Consideracions importants**                                                                                                                                                                                                                                                                                                                            |
|-------------------------|------------|------------|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tasca del projecte            | Sí        | Sí        | Sí        | Els camps **Progrés**, **EffortCompleted** i **EffortRemaining** es poden editar a Project for the Web, però no es poden editar al Project Operations.                                                                                                                                                                                             |
| Dependència de les tasques del projecte | Sí        | No         | Sí        | Els registres de dependència de les tasques del projecte no s'actualitzen. En lloc d'això, es pot suprimir un registre antic i crear-ne un de nou.                                                                                                                                                                                                                                 |
| Assignació de recursos     | Sí        | Sí\*      | Sí        | No s'admeten les operacions amb els camps següents: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** i **PlannedWork**. Els registres d'assignació de recursos no s'actualitzen. En lloc d'això, es pot suprimir el registre antic i crear-ne un de nou. S'ha proporcionat una API diferent per actualitzar els contorns d'Assignació de recursos. |
| Dipòsit de projecte          | Sí        | Sí        | Sí        | El dipòsit per defecte es crea amb l'API **CreateProjectV1**. La compatibilitat per crear i suprimir dipòsits de projectes s'ha afegit a la versió 16 d'actualització.                                                                                                                                                                                                   |
| Membre de l'equip del projecte     | Sí        | Sí        | Sí        | Per a l'operació de creació, utilitzeu l'API **CreateTeamMemberV1**.                                                                                                                                                                                                                                                                                           |
| Project                 | Sí        | Sí        |            | Les operacions amb els camps següents no estan admeses: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** i **Duration**.                                                                                       |
| Llistes de comprovació del projecte      | Sí        | Sí        | Sí        |                                                                                                                                                                                                                                                                                                                                                         |
| Etiqueta del projecte           | No         | Sí        | No         | Els noms de les etiquetes es poden canviar. Aquesta característica només està disponible a Project for the Web                                                                                                                                                                                                                                                                      |
| Tasca de projecte que s'ha d'etiqueta   | Sí        | No         | Sí        | Aquesta característica només està disponible a Project for the Web                                                                                                                                                                                                                                                                                                  |
| Esprint del projecte          | Sí        | Sí        | Sí        | El camp **Inici** ha de tenir una data anterior al camp **Acabament**. Els esprints del mateix projecte no es poden superposar entre si. Aquesta característica només està disponible a Project for the Web                                                                                                                                                                    |




La propietat ID és opcional. Si es proporciona, el sistema intenta utilitzar-la i llança una excepció si no es pot utilitzar. Si no es proporciona, el sistema la generarà.

**Limitacions i problemes coneguts**

A continuació es mostra una llista de limitacions i problemes coneguts:

-   Només els **Usuaris amb llicència del Microsoft Project** poden utilitzar les API de planificació de projectes. No les poden utilitzar:
    -   Usuaris de l'aplicació
    -   Usuaris del sistema
    -   Usuaris d'integració
    -   Altres usuaris que no tenen la llicència necessària
-   Cada **OperationSet** només pot tenir un màxim de 100 operacions.
-   Cada usuari només pot tenir un màxim de 10 **OperationSets** oberts.
-   El Project Operations actualment admet un màxim de 500 tasques totals en un projecte.
-   Cada operació Actualitza el contorn d'assignació de recursos es compta com una única operació.
-   Cada llista de contorns actualitzats pot contenir un màxim de 100 porcions de temps.
-   Actualment no hi ha estats d'error i registres d'error d'**OperationSet** disponibles.
-   Hi ha un màxim de 400 esprints per projecte.
-   [Límits dels projectes i les tasques](/project-for-the-web/project-for-the-web-limits-and-boundaries).
-   Actualment, les etiquetes només estan disponibles a Project for the Web.

**Gestió d'errors**

-   Per revisar els errors generats a partir dels conjunts d'operacions, aneu a **Configuració** \> **Integració de la planificació** \> **Conjunts d'operacions**.
-   Per revisar els errors generats a partir del servei de planificació de projectes, aneu a **Configuració** \> **Integració de la planificació** \> **Registres d’errors de PSS**.

**Edició dels contorns de l'assignació de recursos**

A diferència de la resta d'API de planificació de projectes que actualitzen una entitat, l'API de contorn d'assignació de recursos només és responsable de les actualitzacions d'un sol camp, msdyn_plannedwork, en una única entitat, msydn_resourceassignment.

El mode de planificació proporcionat és:

-   **unitats fixes**
-   el calendari del projecte és de 9 a 5 hores, dilluns, dimarts, dijous, divendres (NO ES TREBALLA ELS DIMECRES)
-   i el calendari de recursos és 9-1p PST de dilluns a divendres

Aquesta assignació és per a una setmana, quatre hores al dia. Això es deu a que el calendari del recurs és de 9 a 1 PST, o quatre hores al dia.

| &nbsp;     | Tasca | Data d’inici | Data d’acabament  | Quantitat | 13/6/2022 | 14/6/2022 | 15/6/2022 | 16/6/2022 | 17/6/2022 |
|------------|------|------------|-----------|----------|-----------|-----------|-----------|-----------|-----------|
| 9-1 treballador |  T1  | 13/6/2022  | 17/6/2022 | 20       | 4         | 4         | 4         | 4         | 4         |

Per exemple, si voleu que el treballador només treballi tres hores cada dia aquesta setmana i tingui una hora per a altres tasques.

#### <a name="updatedcontours-sample-payload"></a>Càrrega d'exemple UpdatedContours:

```json
[{

"minutes":900.0,

"start":"2022-06-13T00:00:00-07:00",

"end":"2022-06-18T00:00:00-07:00"

}]
```

Aquesta és l'assignació després d'executar l'API de planificació de contorn d'actualització.

| &nbsp;     | Tasca | Data d’inici | Data d’acabament  | Quantitat | 13/6/2022 | 14/6/2022 | 15/6/2022 | 16/6/2022 | 17/6/2022 |
|------------|------|------------|-----------|----------|-----------|-----------|-----------|-----------|-----------|
| 9-1 treballador | T1   | 13/6/2022  | 17/6/2022 | 15       | 3         | 3         | 3         | 3         | 3         |


**Escenari d'exemple**

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

**Exemples addicionals

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
