---
title: Registres de planificació de projectes
description: Aquest article proporciona informació i exemples que us ajudaran a utilitzar els registres de Planificació del projecte per fer un seguiment dels errors relacionats amb el Servei de planificació de projectes i les API de planificació de projectes.
author: ruhercul
ms.date: 11/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: c57419642e90e4def01f2cd2474c9e82dc162b86
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923683"
---
# <a name="project-scheduling-logs"></a>Registres de planificació de projectes

_**S'aplica a**: Project Operations per a escenaris basats en recursos/no mantinguts en existències, implementació bàsica: tracte de facturació proforma_, _Project for the Web_

El Microsoft Dynamics 365 Project Operations utilitza [Project for the Web](https://support.microsoft.com/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5) com a principal motor de planificació. En comptes d'utilitzar les interfícies de programació d'aplicacions web (API) estàndard del Microsoft Dataverse, el Project Operations utilitza les noves API de planificació del projecte per crear, actualitzar i suprimir tasques de projecte, assignacions de recursos, dependències de tasques, dipòsits de tasques i membres dels equips de projecte. No obstant, quan les operacions de creació, actualització o supressió s'executen mitjançant programació a les entitats de l'estructura del desglossament del treball (WBS), es podrien produir errors. Per fer un seguiment d'aquests errors i de l'historial de les operacions, s'han implementat dos nous registres administratius: **Conjunt d'operacions** i **Servei de planificació de projectes (PSS)**. Per accedir a aquests registres, aneu a **Configuració** \> **Integració de la planificació**.

A la il·lustració següent es mostra el model de dades per als registres de Planificació de projectes.

![Mode de dades per als registres de Planificació de projectes.](media/LOGDATAMODEL.jpg)

## <a name="operation-set-log"></a>Registre del conjunt d'operacions

El registre del conjunt d'operacions fa un seguiment de l'execució d'un conjunt d'operacions que s'utilitza per executar una o moltes operacions de creació, actualització o supressió en un lot de projectes, tasques de projectes, assignacions de recursos, dependències de tasques, dipòsits de projectes o membres de l'equip del projecte. El camp **Operació en estat** mostra l'estat global del conjunt d'operacions. Els detalls de la càrrega del conjunt d'operacions es capturen als registres de detalls del conjunt d'operacions relacionats.

### <a name="operation-set"></a>Conjunt d'operacions

La taula següent mostra els camps que estan relacionats amb l'entitat **Conjunt d'operacions**.

| Nom de l'esquema            | Descripció                                                                                                  | DisplayName            |
|-----------------------|--------------------------------------------------------------------------------------------------------------|------------------------|
| msdyn_completedon     | Data i hora en què el conjunt d'operacions s'ha completat o ha fallat.                                                | CompletedOn            |
| msdyn_correlationid   | Valor **correlationId** del registre de la sol·licitud.                                                                  | Id. de correlació          |
| msdyn_description     | Descripció del conjunt d'operacions.                                                                        | Descripció            |
| msdyn_executedon      | Data i hora d'execució del registre.                                                                       | Data d’execució            |
| msdyn_operationsetId  | Identificador únic de les instàncies d'entitat.                                                                   | OperationSet           |
| msdyn_Project         | Projecte relacionat amb el conjunt d'operacions.                                                            | Project                |
| msdyn_projectid       | Valor **projectId** del registre de la sol·licitud.                                                                      | ProjectId (obsolet) |
| msdyn_projectName     | No aplicable.                                                                                              | No aplicable         |
| msdyn_PSSErrorLog     | Identificador únic del registre d'errors del Servei de planificació del projecte que està associat amb el conjunt d'operacions. | Registre d’errors de PSS          |
| msdyn_PSSErrorLogName | No aplicable.                                                                                              | No aplicable         |
| msdyn_status          | Estat del conjunt d'operacions.                                                                             | Estat d'execució                 |
| msdyn_statusName      | No aplicable.                                                                                              | No aplicable         |
| msdyn_useraadid       | ID d'objecte de l'Azure Active Directory (Azure AD) de l'usuari al qual pertany la sol·licitud.                     | UserAADID              |

### <a name="operation-set-detail"></a>Detall del conjunt d'operacions

La taula següent mostra els camps que estan relacionats amb l'entitat **Detall del conjunt d'operacions**.

| Nom de l'esquema                 | Descripció                                                                                 | DisplayName           |
|----------------------------|---------------------------------------------------------------------------------------------|-----------------------|
| msdyn_cdspayload           | Camps del Dataverse serialitzats per a la sol·licitud.                                            | CdsPayload            |
| msdyn_entityname           | El nom de l'entitat per a la sol·licitud.                                                     | EntityName            |
| msdyn_httpverb             | El mètode de sol·licitud.                                                                         | Verb HTTP (obsolet) |
| msdyn_httpverbName         | No aplicable.                                                                             | No aplicable        |
| msdyn_operationset         | Identificador únic del conjunt d'operacions al qual pertany el registre.                      | OperationSet          |
| msdyn_operationsetdetailId | Identificador únic de les instàncies d'entitat.                                                  | Detall d’OperationSet   |
| msdyn_operationsetName     | No aplicable.                                                                             | No aplicable        |
| msdyn_operationtype        | Tipus d'operació del detall del conjunt d'operacions.                                             | OperationType         |
| msdyn_operationtypeName    | No aplicable.                                                                             | No aplicable        |
| msdyn_psspayload           | Els camps de Servei de planificació de projectes serialitzats de la sol·licitud.                           | PssPayload            |
| msdyn_recordid             | Identificador del registre de la sol·licitud.                                                       | ID de registre             |
| msdyn_requestnumber        | Número generat automàticament que identifica la comanda en la qual es van rebre les sol·licituds. | Número de sol·licitud        |

## <a name="project-scheduling-service-error-logs"></a>Registres del Servei de planificació de projectes

Els registres d'error del Servei de planificació de projectes capturen els errors que es produeixen quan el Servei de planificació de projectes intenta fer una operació **Desa** o **Obre**. Hi ha tres escenaris admesos en què es generen aquests registres:

- Les accions iniciades per l'usuari fallen críticament (per exemple, una assignació no es pot crear a causa de la falta de privilegis).
- El Servei de planificació de projectes no pot crear, actualitzar, suprimir ni dur a terme cap altra operació en cascada de manera programàtica en una entitat.
- L'usuari experimenta errors quan un registre no s'obre (per exemple, quan s'obre un projecte o s'actualitza la informació d'un membre de l'equip).

### <a name="project-scheduling-service-log"></a>Registre del Servei de planificació de projectes

La taula següent mostra els camps que s'inclouen en el registre del Servei de planificació del projecte.

| Nom de l'esquema          | Descripció                                                                    | DisplayName    |
|---------------------|--------------------------------------------------------------------------------|----------------|
| msdyn_CallStack     | Pila de trucades de l'excepció.                                               | Pila de trucades     |
| msdyn_correlationid | ID de correlació de l'error.                                               | Id. de correlació  |
| msdyn_errorcode     | Camp utilitzat per emmagatzemar el codi d'error del Dataverse o el codi d'error HTTP. | Codi d’error     |
| msdyn_HelpLink      | Enllaç a la documentació d'ajuda pública.                                       | Enllaç d'ajuda      |
| msdyn_log           | El registre del Servei de planificació del projecte.                                   | Registre            |
| msdyn_project       | El projecte que està associat amb el registre d'errors.                             | Project        |
| msdyn_projectName   | El nom del projecte si es manté la càrrega del conjunt d'operacions. | No aplicable |
| msdyn_psserrorlogId | Identificador únic de les instàncies d'entitat.                                     | Registre d’errors de PSS  |
| msdyn_SessionId     | ID de sessió del projecte.                                                        | Id. de sessió     |

## <a name="error-log-cleanup"></a>Neteja del registre d'errors

Per defecte, tots dos registres d'error del Servei de planificació del projecte i el registre de conjunt d'operacions es poden netejar cada 90 dies. Els registres que tenen més de 90 dies se suprimeixen. Tanmateix, si canvieu el valor del camp **msdyn_StateOperationSetAge** de la pàgina **Paràmetres del projecte**, els administradors poden ajustar l'interval de neteja per tal que es trobi entre 1 i 120 dies. Hi ha diversos mètodes per canviar aquest valor:

- Personalitzeu l'entitat **Paràmetre del projecte** creant una pàgina personalitzada i afegint el camp **Antiguitat de conjunt d'operacions obsolet**.
- Utilitzeu el codi de client que utilitza el [kit de desenvolupament de programari (SDK) de WebApi](/powerapps/developer/model-driven-apps/clientapi/reference/xrm-webapi/updaterecord).
- Utilitzeu el codi SDK del servei que utilitza el mètode **updateRecord** de l'SDK Xrm (referència a API de client) a les aplicacions basades en models. El Power Apps inclou una descripció i els paràmetres compatibles per al mètode **updateRecord**.

    ```C#
    Xrm.WebApi.retrieveMultipleRecords('msdyn_projectparameter').then(function (response) {
        parameter = response.entities[0];
        var staleOperationValue = prompt("All records older than (x) days will be deleted, please enter X between 1 to 90 days", 1)
        var newData = {};
        newData.msdyn_projectparameterid = parameter.msdyn_projectparameterid;
        newData.msdyn_staleoperationsetage = parseInt(staleOperationValue);
        Xrm.WebApi.updateRecord("msdyn_projectparameter", parameter.msdyn_projectparameterid, newData).then(
            function success(result) {
                console.log("Project Parameter: Stale Operation Expiry is set to: " + newData.msdyn_staleoperationsetage);
                // perform operations on record update
                Xrm.WebApi.retrieveMultipleRecords('msdyn_projectparameter')
                .then(function (response2) { console.log("Confirmed Project Parameter: Stale Operation Expiry is set to: " + response2.entities[0].msdyn_staleoperationsetage) });
            },
            function (error) {
                console.log("Failed to Update Project Ednpoint with error: " + error.message);
            // handle error conditions
            }
        );
    });
    ```
