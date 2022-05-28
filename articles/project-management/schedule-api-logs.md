---
title: Registres de planificació de projectes
description: Aquest tema proporciona informació i mostres que us ajudaran a utilitzar els registres de planificació de projectes per fer un seguiment dels errors relacionats amb les API del Servei de planificació de projectes i de planificació de projectes.
author: ruhercul
ms.date: 11/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 1a58a588d3e2fb92f1b4a4ed0f6f69d0a63908db
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8589506"
---
# <a name="project-scheduling-logs"></a>Registres de planificació de projectes

_**Aplica a:** Operacions de projecte per a escenaris basats en recursos/ no emmagatzemats, implementació de Lite: acord a la facturació_ proforma, _Projecte per al web_

Microsoft Dynamics 365 Project Operations utilitza [el Project for the Web](https://support.microsoft.com/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5) com a principal motor de planificació. En lloc d'utilitzar les interfícies de programació d'aplicacions web estàndard Microsoft Dataverse (API), Project Operations utilitza les noves API de planificació de projectes per crear, actualitzar i suprimir tasques de projecte, assignacions de recursos, dependències de tasques, cubells de projectes i membres de l'equip de projecte. Tanmateix, quan les operacions de creació, actualització o supressió s'executen per programació en entitats de l'estructura de desglossament del treball (WBS), es poden produir errors. Per fer un seguiment d'aquests errors i de l'historial d'operacions, s'han implementat dos nous registres administratius: **El conjunt** d'operacions i **el servei de planificació de projectes (PSS).** Per accedir a aquests registres, aneu a **Configuració** \> **de la integració de la planificació.**

La il·lustració següent mostra el model de dades dels registres de planificació de projectes.

![Model de dades per als registres de planificació de projectes.](media/LOGDATAMODEL.jpg)

## <a name="operation-set-log"></a>Registre del conjunt d'operacions

El registre Conjunt d'operacions fa un seguiment de l'execució d'un conjunt d'operacions que s'utilitza per executar una o diverses operacions de creació, actualització o supressió en un lot de projectes, tasques de projecte, assignacions de recursos, dependències de tasques, cubells de projecte o membres de l'equip del projecte. El **camp Operació en estat** mostra l'estat general del conjunt d'operacions. Els detalls de la càrrega útil del conjunt d'operacions es capturen als registres de detalls del conjunt d'operacions relacionats.

### <a name="operation-set"></a>Conjunt d'operacions

A la taula següent es mostren els camps relacionats amb l'entitat **Conjunt** d'operacions.

| Nom de l'esquema            | Descripció                                                                                                  | DisplayName            |
|-----------------------|--------------------------------------------------------------------------------------------------------------|------------------------|
| msdyn_completedon     | La data/hora en què s'ha completat o ha fallat el conjunt d'operacions.                                                | CompletedOn            |
| msdyn_correlationid   | El **valor de correlacióId** de la sol·licitud.                                                                  | Id. de correlació          |
| msdyn_description     | La descripció del conjunt d'operacions.                                                                        | Descripció            |
| msdyn_executedon      | La data i l'hora en què s'ha executat el registre.                                                                       | Data d’execució            |
| msdyn_operationsetId  | L'identificador únic de les instàncies d'entitat.                                                                   | OperationSet           |
| msdyn_Project         | El projecte que està relacionat amb el conjunt d'operacions.                                                            | Project                |
| msdyn_projectid       | El **valor del projecteId** de la sol·licitud.                                                                      | ProjectId (obsolet) |
| msdyn_projectName     | No aplicable.                                                                                              | No aplicable         |
| msdyn_PSSErrorLog     | L'identificador únic del registre d'errors del servei de planificació de projectes associat amb el conjunt d'operacions. | Registre d’errors de PSS          |
| msdyn_PSSErrorLogName | No aplicable.                                                                                              | No aplicable         |
| msdyn_status          | L'estat del conjunt d'operacions.                                                                             | Estat d'execució                 |
| msdyn_statusName      | No aplicable.                                                                                              | No aplicable         |
| msdyn_useraadid       | L'identificador Azure Active Directory d'objecte (Azure AD) de l'usuari al qual pertany la sol·licitud.                     | UserAADID              |

### <a name="operation-set-detail"></a>Detall del conjunt d'operacions

A la taula següent es mostren els camps relacionats amb l'entitat Detall **del** conjunt d'operacions.

| Nom de l'esquema                 | Descripció                                                                                 | DisplayName           |
|----------------------------|---------------------------------------------------------------------------------------------|-----------------------|
| msdyn_cdspayload           | Els camps serialitzats Dataverse de la sol·licitud.                                            | CdsPayload            |
| msdyn_entityname           | El nom de l'entitat de la sol·licitud.                                                     | EntityName            |
| msdyn_httpverb             | El mètode de sol·licitud.                                                                         | Verb HTTP (obsolet) |
| msdyn_httpverbName         | No aplicable.                                                                             | No aplicable        |
| msdyn_operationset         | L'identificador únic del conjunt d'operacions al qual pertany el registre.                      | OperationSet          |
| msdyn_operationsetdetailId | L'identificador únic de les instàncies d'entitat.                                                  | Detall d’OperationSet   |
| msdyn_operationsetName     | No aplicable.                                                                             | No aplicable        |
| msdyn_operationtype        | El tipus d'operació de l'operació estableix el detall.                                             | OperationType         |
| msdyn_operationtypeName    | No aplicable.                                                                             | No aplicable        |
| msdyn_psspayload           | Els camps del servei de planificació de projectes serialitzats per a la sol·licitud.                           | PssPayload            |
| msdyn_recordid             | L'identificador del registre de sol·licitud.                                                       | ID de registre             |
| msdyn_requestnumber        | Un número generat automàticament que identifica la comanda en què s'han rebut les sol·licituds. | Número de sol·licitud        |

## <a name="project-scheduling-service-error-logs"></a>Registres d'errors del servei de planificació de projectes

L'error del servei de planificació de projectes registra errors de captura que es produeixen quan el Servei de planificació de projectes prova una **operació de desament** o **obertura**. Hi ha tres escenaris admesos on es generen aquests registres:

- Les accions iniciades per l'usuari fallen críticament (per exemple, no es pot crear una tasca a causa dels privilegis que falten).
- El Servei de planificació de projectes no pot crear, actualitzar, suprimir ni dur a terme cap altra operació en cascada en cascada en una entitat.
- L'usuari experimenta errors quan un registre no s'obre (per exemple, quan s'obre un projecte o s'actualitza la informació d'un membre de l'equip).

### <a name="project-scheduling-service-log"></a>Registre del servei de planificació de projectes

La taula següent mostra els camps que s'inclouen al registre del servei de planificació de projectes.

| Nom de l'esquema          | Descripció                                                                    | DisplayName    |
|---------------------|--------------------------------------------------------------------------------|----------------|
| msdyn_CallStack     | Pila de trucades de l'excepció.                                               | Pila de trucades     |
| msdyn_correlationid | L'identificador de correlació de l'error.                                               | Id. de correlació  |
| msdyn_errorcode     | Un camp que s'utilitza per emmagatzemar el codi d'error Dataverse o el codi d'error HTTP. | Codi d’error     |
| msdyn_HelpLink      | Un enllaç a la documentació de l'ajuda pública.                                       | Enllaç d'ajuda      |
| msdyn_log           | El registre del servei de planificació de projectes.                                   | Registre            |
| msdyn_project       | El projecte associat amb el registre d'errors.                             | Project        |
| msdyn_projectName   | El nom del projecte si es mantindrà la càrrega útil del conjunt d'operacions. | No aplicable |
| msdyn_psserrorlogId | L'identificador únic de les instàncies d'entitat.                                     | Registre d’errors de PSS  |
| msdyn_SessionId     | L'identificador de la sessió del projecte.                                                        | Id. de sessió     |

## <a name="error-log-cleanup"></a>Neteja del registre d'errors

Per defecte, tant els registres d'errors del servei de planificació de projectes com el registre del conjunt d'operacions es poden netejar cada 90 dies. Se suprimiran els registres que tindran més de 90 dies. Tanmateix, canviant el valor del camp msdyn_StateOperationSetAge **de** la pàgina Paràmetres **del** projecte, els administradors poden ajustar l'interval de neteja perquè sigui entre 1 i 120 dies. Hi ha disponibles diversos mètodes per canviar aquest valor:

- Personalitzeu l'entitat **Paràmetre del** projecte creant una pàgina personalitzada i afegint el camp Edat del **conjunt d'operacions** obsolet.
- Utilitzeu el codi de client que utilitzi el kit de [desenvolupament de programari WebApi (SDK).](/powerapps/developer/model-driven-apps/clientapi/reference/xrm-webapi/updaterecord)"
- Utilitzeu el codi de l'SDK del servei que utilitza el mètode de l'SDK **updateRecord** de l'Xrm (referència de l'API client) a les aplicacions basades en models. Power Apps inclou una descripció i paràmetres admesos per al **mètode updateRecord**.

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
