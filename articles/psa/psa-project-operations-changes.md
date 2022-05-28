---
title: Canvis de característiques de l'automatització del project service a les operacions de projectes
description: Aquest tema proporciona una visió general dels canvis de la característica de Project Service Automation a Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/03/2022
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 7e41b381d6da267f58174305f33fc229c66cd7b7
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8595394"
---
# <a name="feature-changes-from-project-service-automation-to-project-operations"></a>Canvis de característiques de l'automatització del project service a les operacions de projectes

L'actualització des de Dynamics 365 Project Service Automation Dynamics 365 Project Operations Lite es lliurarà en tres fases. Aquest tema proporciona informació sobre els principals canvis que podeu esperar veure quan s'hagi completat l'actualització.

| Actualitza el lliurament | Fase 1 <br>(gener 2022) | Fase 2 <br>(Abril 2022) | Fase 3  |
|------------------|------------------------|---------------------------|---------------------------|
| Sense dependència de l'estructura de desglossament de l'obra (WBS) per a projectes. | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| El WBS s'inclou en els límits actualment admesos de les operacions del projecte. | &nbsp; | :heavy_check_mark: | :heavy_check_mark: |
| El WBS fora dels límits compatibles actualment amb les operacions del projecte, inclòs el suport per al client d'escriptori del Projecte. | &nbsp; | &nbsp; | :heavy_check_mark: |

## <a name="project-management"></a>Administració de projectes

Els canvis més significatius en l'experiència de l'usuari seran en l'àmbit de la planificació de projectes. Project Operations adopta una nova experiència moderna per gestionar una estructura de desglossament del treball (WBS) aprofitant les capacitats de planificació proporcionades pel [Project for the Web](https://support.microsoft.com/en-us/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5).

## <a name="differences-in-the-scheduling-experience"></a>Diferències en l'experiència de planificació

La taula següent resumeix les diferències de planificació entre l'automatització de serveis del Projecte i les operacions de projectes.

|  Planificació     |   Project Operations   |   PSA   |
|-----------------|------------------------|---------|
| Plantilles de projecte: capacitat per definir i aplicar plantilles de projecte quan es crea un projecte  |  &nbsp;    | :heavy_check_mark: |
| Integració de l'estructura del desglossament del treball del projecte (WBS) amb el client d'escriptori   |    &nbsp;  | :heavy_check_mark: |
| Restriccions: no s'inicia abans, acaba com a molt tard  | :heavy_check_mark: |   &nbsp;  |
| Fites: tasques amb durada zero   | :heavy_check_mark:  |  &nbsp;  |
| Les tasques basades en recursos respectaran la disponibilitat dels recursos assignats   | :heavy_check_mark: |  &nbsp;    |
| Edició per fases horàries: edita els plans i treballa dia a dia   |   &nbsp;  | :heavy_check_mark: |
| Planificació automàtica/manual: utilitzeu el motor de planificació de projectes per planificar automàticament o manualment tasques |  &nbsp; | :heavy_check_mark:  |
| Editar projectes grans directament a la interfície d'usuari: no hi ha límit a la mida dels plans que es poden editar  | 500 límit de tasques  | :heavy_check_mark:       |
| Percentatge completat: marca el progrés de la tasca   | :heavy_check_mark:  |  &nbsp;  |
| [Modes de planificació del](../project-management/scheduling-modes.md) projecte: definiu el projecte com a unitats fixes, esforç fix o durada fixa | :heavy_check_mark: | &nbsp; |
| Cronologia: creeu i personalitzeu la visualització de cronologia per visualitzar els detalls de la planificació i comunicar-vos amb les parts interessades. | :heavy_check_mark:  | &nbsp; |
| Tasques basades en l'esforç: planificació del suport del motor per planificar una tasca com a impulsada per l'esforç  | :heavy_check_mark:  | &nbsp; |
| **Quadre de diàleg Informació** de tasques: desa els detalls de la tasca mitjançant un quadre de diàleg | :heavy_check_mark:  |  &nbsp;  |
| Arrossegar i deixar anar : diverses tasques i modificar la seva posició al WBS | :heavy_check_mark: | &nbsp;  |
| Visualitzacions persistents flexibles: defineix visualitzacions més granulars dels atributs de tasca   | :heavy_check_mark:  | &nbsp; |
| Ordena i filtra el WBS  | :heavy_check_mark:  | &nbsp; |
| Vista de taulers per al lliurament de projectes sense cascada  | :heavy_check_mark:   | &nbsp; |
| Visualització de cronologia: gràfic interactiu de Gantt utilitzat per visualitzar i editar el WBS   | :heavy_check_mark:  | &nbsp; |
| Dreceres de teclat: utilitzeu dreceres de teclat per a operacions habituals, com ara sagnar o inserir  | :heavy_check_mark:  |  &nbsp; |
| Desfer multinivell: realitzar una anàlisi d'hipòtesis per entendre completament l'impacte dels canvis invertint i tornar a aplicar tot un conjunt d'operacions | :heavy_check_mark: | &nbsp; |
| Retalla/Copia/Enganxa - Col·labora en el desenvolupament de la planificació copiant i enganxant els detalls de la planificació entre aplicacions  | :heavy_check_mark: | &nbsp; |
| Llistes de comprovació de tasques: afegiu fins a 20 elements de la llista de comprovació a una tasca   | :heavy_check_mark: | &nbsp; |

## <a name="project-planning"></a>Planificació del projecte

La **pàgina Projecte** a Project Operations té un nombre significatiu de diferències en comparació amb la **pàgina Projecte** del Project Service Automation.

Les accions següents s'han suprimit de la **pàgina Projectes** com a part de l'actualització de fase 1:

  - **Obre a l'MS Project**
  - **Crea una plantilla**
  - **Desenllaça de l'MS Project**

La **pàgina Projecte** a Operacions del projecte inclou les pestanyes noves següents.

- **Estimacions de material**
- **Configuració de facturació de la tasca**

S'ha **suprimit la pestanya Estat** i el **camp Estat** ja és a la **pestanya Resum** amb el mode de planificació del projecte.

   ![Actualitzacions de la pàgina del projecte.](media/projectform.png)

La **pestanya Planificació** s'ha canviat el nom a la **pestanya Tasca** i inclou la nova experiència de planificació de projectes amb el Project for the Web.

   ![Pestanya Tasques del projecte nova.](media/tasktab.png)

## <a name="scheduling-modes"></a>Modes de planificació

Project Operations ha introduït una nova característica, [Modes de](../project-management/scheduling-modes.md) planificació. Tots els projectes existents d'automatització de serveis del Project funcionaran per defecte a **durada** fixa a les operacions del projecte. No obstant això, el valor per defecte per a projectes nous es pot gestionar anant al **mode de planificació de paràmetres de** > **paràmetres** > **de configuració** > **·**.

   ![Configuració del paràmetre del projecte per al mode Planifica.](media/projectparameter.png)

## <a name="project-planning-limits"></a>Límits de planificació de projectes

Project Operations es basa en el Projecte per al Web per a totes les operacions de planificació de projectes. El projecte per al web gestiona l'estructura de desglossament del treball utilitzant els límits de la taula següent.

| **Camp**                                          | **Límit**             |
|----------------------------------------------------|-----------------------|
| Tasques totals màximes per a un projecte                  | 500                   |
| Durada total màxima per a un projecte               | 3.650 dies (10 anys)  |
| Recursos totals màxims per a un projecte              | 300                   |
| Enllaços totals màxims (només successor) per a un projecte | 600                   |
| Camps personalitzats totals màxims per a un projecte          | 10                    |
| Nivell de jerarquia màxim                            | 10 nivells             |
| Enllaços màxims (successor + predecessor)            | 20                    |
| Durada màxima de la tasca de fulla                      | 1250 dies             |
| Durada màxima d'una tasca de resum                 | 3.650 dies (10 anys)  |
| Recursos màxims assignats a una tasca               | 20 recursos          |
| Interval de dates admès per a una tasca                    | 1/1/2000 - 31/12/2149 |
| Elements de llista de comprovació                                    | 20                    |

## <a name="project-planning-extensibility-and-development"></a>Extensibilitat i desenvolupament de la planificació de projectes

Després d'actualitzar a Operacions del projecte, heu d'utilitzar les API de planificació de projectes per executar operacions de creació, actualització i supressió a les entitats següents:

|   Nom de l’entitat           |   Nom lògic de l’entitat       |
|-------------------------|-----------------------------|
| Project                 | msdyn_project               |
| Tasca del projecte            | msdyn_projecttask           |
| Dependència de les tasques del projecte | msdyn_projecttaskdependency |
| Assignació de recursos     | msdyn_resourceassignment    |
| Dipòsit de projecte          | msdyn_projectbucket         |
| Membre de l'equip del projecte     | msdyn_projectteam           |

Si actualment teniu personalitzacions que impliquen aquestes entitats, vegeu [Utilitzar les API de planificació del projecte per dur a terme operacions amb entitats](../project-management/schedule-api-preview.md) de planificació per obtenir orientació d'implementació.

## <a name="data-model-changes"></a>Canvis en el model de dades

Com a part de la fase d'actualització 1, hi ha canvis en el model de dades. Aquests canvis són principalment canvis de camp a les entitats existents. En la Fase 1, les entitats, **msydn_project** i **msdyn_projectteam** són una refacció de personalitzacions. 

> [!IMPORTANT]
> Aquesta secció s'actualitzarà amb entitats addicionals a mesura que es completin les futures fases d'actualització.

Els camps següents s'han substituït per camps nous.

|   Entity          |   Nom lògic antic   |   Nom lògic nou    |
|-------------------|----------------------|-----------------------|
| msdyn_project     | msdyn_actualhours    | msdyn_effortcompleted |
| msdyn_project     | msdyn_plannedhours   | msdyn_effort          |
| msdyn_project     | msdyn_remaininghours | msdyn_effortremaining |
| msdyn_project     | msdyn_scheduledend   | msdyn_finish          |
| msdyn_project     | msdyn_wbsduration    | msdyn_duration        |
| msdyn_projectteam | msdyn_assignedhours  | msdyn_effort          |
| msdyn_projectteam | msdyn_from           | msdyn_start           |
| msdyn_projectteam | msdyn_to             | msdyn_finish          |

S'han afegit els camps següents.

|   Entity          |   Nom lògic                               |   Descripció |
|-------------------|----------------------------------------------|---------------|
| msdyn_project     | msdyn_actualfeesales                         | Mostra l'agregat de vendes reals del projecte. Només s'utilitza al Project Service Automation. |
| msdyn_project     | msdyn_actualmaterialcost                     | Mostra l'agregat del cost material real del projecte. Només s'utilitza al Project Service Automation. |
| msdyn_project     | msdyn_actualmaterialsales                    | Mostra l'agregat de vendes reals de material al projecte. Només s'utilitza al Project Service Automation. |
| msdyn_project     | msdyn_businesscase                           |                |
| msdyn_project     | msdyn_contractlineproject                    | La línia de contracte associada a aquest projecte. |
| msdyn_project     | msdyn_copyprojectcorrelationid               | Aquest és un camp del sistema intern que s'utilitza per **copiar el projecte** relacionat amb l'identificador de correlació. Només s'utilitza al Project Service Automation. |
| msdyn_project     | msdyn_copyprojectsessionid                   | Aquest és un camp del sistema intern, utilitzat per **copiar el projecte** relacionat amb l'identificador de sessió. Només s'utilitza al Project Service Automation. |
| msdyn_project     | msdyn_globalrevisiontoken                    | Últim testimoni de revisió global de sincronització xRM del servei de planificació del projecte. |
| msdyn_project     | msdyn_msprojectdocument                      | El document del Microsoft Project que pertany al projecte. |
| msdyn_project     | msdyn_plannedmaterialcost                    | El cost material previst en el projecte. Només s'utilitza al Project Service Automation. |
| msdyn_project     | msdyn_plannedmaterialsales                   | L'agregat de vendes de material previstes en el projecte. Només s'utilitza al Project Service Automation. |
| msdyn_project     | msdyn_program                                | Programa amb el qual està relacionat aquest projecte. |
| msdyn_project     | msdyn_quotelineproject                       | La línia d'oferta associada a aquest projecte. |
| msdyn_project     | msdyn_replaylogheader                        | La capçalera dels registres de reproducció. |
| msdyn_project     | msdyn_schedulemode                           | El mode de planificació per defecte utilitzat per a totes les tasques del projecte.  |
| msdyn_project     | msdyn_taskearlieststart                      | La primera data d'inici de qualsevol tasca del projecte.  |
| msdyn_project     | msdyn_valuestatement                         |                |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | El membre de l'equip del projecte del que s'ha copiat aquest membre de l'equip del projecte. |
| msdyn_projectteam | msdyn_creategenericteammemberwithrequirement | Indica si s'ha de crear el requisit de recurs per a un membre genèric de l'equip acabat de crear.  |
| msdyn_projectteam | msdyn_deletestatus                           | L'estat de supressió del membre de l'equip per fer un seguiment de si hi ha una sol·licitud de supressió enviada al servei de planificació del projecte i si envia correctament una resposta dins de la finestra de temps esperada. |
| msdyn_projectteam | msdyn_effortcompleted                        | Fa un seguiment de l'esforç realitzat pel membre de l'equip en les seves tasques. |
| msdyn_projectteam | msdyn_effortremaining                        | Fa un seguiment de l'esforç que encara no ha completat el membre de l'equip en les seves tasques. |
| msdyn_projectteam | msdyn_markedfordeletiontimer                 | El període d'espera des que el membre de l'equip envia una sol·licitud de supressió al servei de planificació del projecte fins que el membre de l'equip se suprimeixi realment a Microsoft Dataverse.|
| msdyn_projectteam | msdyn_markedfordeletiontimestamp             | La marca horària a registrar quan el membre de l'equip suprimeix la sol·licitud s'envia al servei de planificació del projecte. |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | Mostra el membre de l'equip del projecte del qual s'ha copiat aquest membre de l'equip del projecte.  |

## <a name="project-templates"></a>Plantilles de projecte

Project Operations no proporciona suport per a plantilles de projecte. Tanmateix, podeu replicar gran part de la funcionalitat bàsica amb l'ús de l'API [Project Copy](../project-management/dev-copy-project.md).

## <a name="desktop-add-in-support"></a>Suport per a complements d'escriptori

El suport per al complement del Microsoft Project Desktop no estarà disponible en les 2 primeres fases de l'actualització. A la fase 3, els clients que tinguin projectes més grans que els límits admesos actualment del Project for the Web podran utilitzar el complement d'escriptori.

## <a name="editing-resource-assignment-contours"></a>S'estan editant els contorns de l'assignació de recursos

La possibilitat d'editar els contorns de l'assignació de recursos estarà disponible quan estigui disponible la fase 2 de l'actualització.

## <a name="billing-and-pricing"></a>Facturació i preus

S'han afegit les característiques noves següents a Les operacions del projecte. Aquestes característiques són de naturalesa additiva i no afecten el model de dades de Project Service Automation.

- [Enregistrament de l'ús de material en projectes i tasques del projecte](../material/material-usage-log.md)
- [Gestió de subcontractacions](../pro/subcontracting/managing-subcontracts-overview.md)
- [Avançaments i contractes de bestreta](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Estat de no superació del contracte i validacions](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- [Facturació basada en tasques](../pro/sales/mapping-projects-tasks-quote-line-sales.md)

## <a name="deprecated-components"></a>Components obsolets

Les taules següents documenten tots els camps obsolets que es mouen a l'actualització posterior de la solució de components obsolets. Per obtenir més informació i un enllaç a la solució, vegeu [Dynamics 365 Project Service Automation 3x a Project Operations 4x components](https://github.com/microsoft/Dynamics365-Project-Operations-PowerApps/tree/main/3x-4x-deprecated-solution) obsolets.

### <a name="invoicedetail"></a>invoicedetail

| Camps                                                    |
|-----------------------------------------------------------------------------------------------|
|invoicedetail.msdyn_contractline    |

### <a name="msdyn_actual"></a>msdyn_actual

| Camps                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_actual.msdyn_salescontractline                                                          |

### <a name="msdyn_characteristicreqforteammember"></a>msdyn_characteristicreqforteammember

| Camps                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_characteristicreqforteammember.msdyn_characteristic                                     |
| msdyn_characteristicreqforteammember.msdyn_characteristicreqforteammemberid                   |
| msdyn_characteristicreqforteammember.msdyn_characteristictype                                 |
| msdyn_characteristicreqforteammember.msdyn_name                                               |
| msdyn_characteristicreqforteammember.msdyn_ratingvalue                                        |
| msdyn_characteristicreqforteammember.msdyn_resourcerequirementid                              |

### <a name="msdyn_contractlineinvoiceschedule"></a>msdyn_contractlineinvoiceschedule

| Camps                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_contractlineinvoiceschedule.msdyn_contractline                                          |
| msdyn_contractlinescheduleofvalue.msdyn_contractline                                          |
 
### <a name="msdyn_dataexport"></a>msdyn_dataexport

| Camps                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_dataexport.msdyn_dataexportid                                                           |
| msdyn_dataexport.msdyn_datatoken                                                              |
| msdyn_dataexport.msdyn_entityname                                                             |
| msdyn_dataexport.msdyn_exportedrecordcount                                                    |
| msdyn_dataexport.msdyn_exportstatus                                                           |
| msdyn_dataexport.msdyn_linkedentitydata                                                       |
| msdyn_dataexport.msdyn_name                                                                   |
| msdyn_dataexport.msdyn_pagingdata                                                             |

### <a name="msdyn_fact"></a>msdyn_fact

| Camps                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_fact.msdyn_salescontractline                                                            |

### <a name="msdyn_findworkevent"></a>msdyn_findworkevent

| Camps                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_findworkevent.msdyn_bookableresource                                                    |
| msdyn_findworkevent.msdyn_findworkeventid                                                     |
| msdyn_findworkevent.msdyn_name                                                                |
| msdyn_findworkevent.msdyn_timestamp                                                           |
| msdyn_findworkevent.msdyn_type                                                                |
| valor_msdyn_findworkevent.msdyn                                                               |
| msdyn_findworkevent.msdyn_work                                                                |

### <a name="msdyn_invoicelinetransaction"></a>msdyn_invoicelinetransaction

| Camps                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_invoicelinetransaction.msdyn_invoiceline                                                |
| msdyn_invoicelinetransaction.msdyn_salescontractline                                          |

### <a name="msdyn_journalline"></a>msdyn_journalline

| Camps                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_journalline.msdyn_salescontractline                                                     |

### <a name="msdyn_opportunitylineresourcecategory"></a>msdyn_opportunitylineresourcecategory

| Camps                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylineresourcecategory.msdyn_billingtype                                       |
| msdyn_opportunitylineresourcecategory.msdyn_description                                       |
| msdyn_opportunitylineresourcecategory.msdyn_opportunitylineresourcecategoryid                 |
| msdyn_opportunitylineresourcecategory.msdyn_opportunitylinetransactionclassification          |
| msdyn_opportunitylineresourcecategory.msdyn_resourcecategory                                  |

### <a name="msdyn_opportunitylinetransaction"></a>msdyn_opportunitylinetransaction

| Camps                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransaction.msdyn_accountcustomer                                        |
| msdyn_opportunitylinetransaction.msdyn_accountingdate                                         |
| msdyn_opportunitylinetransaction.msdyn_accountvendor                                          |
| msdyn_opportunitylinetransaction.msdyn_amount                                                 |
| msdyn_opportunitylinetransaction.msdyn_amount_base                                            |
| msdyn_opportunitylinetransaction.msdyn_amountmethod                                           |
| msdyn_opportunitylinetransaction.msdyn_basisamount                                            |
| msdyn_opportunitylinetransaction.msdyn_basisamount_base                                       |
| msdyn_opportunitylinetransaction.msdyn_basisprice                                             |
| msdyn_opportunitylinetransaction.msdyn_basisprice_base                                        |
| msdyn_opportunitylinetransaction.msdyn_basisquantity                                          |
| msdyn_opportunitylinetransaction.msdyn_billingtype                                            |
| msdyn_opportunitylinetransaction.msdyn_bookableresource                                       |
| msdyn_opportunitylinetransaction.msdyn_contactcustomer                                        |
| msdyn_opportunitylinetransaction.msdyn_contactvendor                                          |
| msdyn_opportunitylinetransaction.msdyn_customertype                                           |
| msdyn_opportunitylinetransaction.msdyn_description                                            |
| msdyn_opportunitylinetransaction.msdyn_documentdate                                           |
| msdyn_opportunitylinetransaction.msdyn_enddatetime                                            |
| msdyn_opportunitylinetransaction.msdyn_exchangeratedate                                       |
| msdyn_opportunitylinetransaction.msdyn_opportunityline                                        |
| msdyn_opportunitylinetransaction.msdyn_opportunitylinetransactionid                           |
| msdyn_opportunitylinetransaction.msdyn_percentatge                                                |
| msdyn_opportunitylinetransaction.msdyn_price                                                  |
| msdyn_opportunitylinetransaction.msdyn_price_base                                             |
| msdyn_opportunitylinetransaction.msdyn_pricelist                                              |
| msdyn_opportunitylinetransaction.msdyn_product                                                |
| msdyn_opportunitylinetransaction.msdyn_projecte                                                |
| msdyn_opportunitylinetransaction.msdyn_quantity                                               |
| msdyn_opportunitylinetransaction.msdyn_resourcecategory                                       |
| msdyn_opportunitylinetransaction.msdyn_resourceorganizationalunitid                           |
| msdyn_opportunitylinetransaction.msdyn_startdatetime                                          |
| msdyn_opportunitylinetransaction.msdyn_task                                                   |
| msdyn_opportunitylinetransaction.msdyn_transactioncategory                                    |
| msdyn_opportunitylinetransaction.msdyn_transactionclassification                              |
| msdyn_opportunitylinetransaction.msdyn_transactiontypecode                                    |
| msdyn_opportunitylinetransaction.msdyn_unitat                                                   |
| msdyn_opportunitylinetransaction.msdyn_unitschedule                                           |
| msdyn_opportunitylinetransaction.msdyn_vendortype                                             |

### <a name="msdyn_opportunitylinetransactioncategory"></a>msdyn_opportunitylinetransactioncategory

| Camps                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransactioncategory.msdyn_billingtype                                    |
| msdyn_opportunitylinetransactioncategory.msdyn_description                                    |
| msdyn_opportunitylinetransactioncategory.msdyn_opportunitylinetransactioncategoryid           |
| msdyn_opportunitylinetransactioncategory.msdyn_opportunitylinetransactionclassification       |
| msdyn_opportunitylinetransactioncategory.msdyn_transactioncategory                            |

### <a name="msdyn_opportunitylinetransactionclassificatio"></a>msdyn_opportunitylinetransactionclassificatio

| Camps                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransactionclassificatio.msdyn_billingtype                               |
| msdyn_opportunitylinetransactionclassificatio.msdyn_description                               |
| msdyn_opportunitylinetransactionclassificatio.msdyn_include                                   |
| msdyn_opportunitylinetransactionclassificatio.msdyn_opportunityline                           |
| msdyn_opportunitylinetransactionclassificatio.msdyn_opportunitylinetransactionclassificatioid |
| msdyn_opportunitylinetransactionclassificatio.msdyn_transactionclassification                 |

### <a name="msdyn_orderlineresourcecategory"></a>msdyn_orderlineresourcecategory

| Camps                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlineresourcecategory.msdyn_contractline                                            |

### <a name="msdyn_orderlinetransaction"></a>msdyn_orderlinetransaction

| Camps                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlinetransaction.msdyn_salescontractline                                            |
| msdyn_orderlinetransactioncategory.msdyn_contractline                                         |

### <a name="msdyn_orderlinetransactionclassification"></a>msdyn_orderlinetransactionclassification

| Camps                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlinetransactionclassification.msdyn_contractline                                   |

### <a name="msdyn_project"></a>msdyn_project

| Camps                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_project.msdyn_actualdurationminutes                                                     |
| msdyn_project.msdyn_actualhours                                                               |
| msdyn_project.msdyn_istemplate                                                                |
| msdyn_project.msdyn_plannedhours                                                              |
| msdyn_project.msdyn_projecttemplate                                                           |
| msdyn_project.msdyn_remaininghours                                                            |
| msdyn_project.msdyn_scheduleddurationminutes                                                  |
| msdyn_project.msdyn_scheduledend                                                              |
| msdyn_project.msdyn_stagename                                                                 |
| msdyn_project.msdyn_wbsduration                                                               |


### <a name="msdyn_projecttask"></a>msdyn_projecttask

| Camps                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttask.msdyn_actualdurationminutes                                                 |
| msdyn_projecttask.msdyn_actualeffort                                                          |
| msdyn_projecttask.msdyn_aggregationdirection                                                  |
| msdyn_projecttask.msdyn_assignedresources                                                     |
| msdyn_projecttask.msdyn_assignedteammembers                                                   |
| msdyn_projecttask.msdyn_autoscheduling                                                        |
| msdyn_projecttask.msdyn_costestimatecontour                                                   |
| msdyn_projecttask.msdyn_effortcontour                                                         |
| msdyn_projecttask.msdyn_islinetask                                                            |
| msdyn_projecttask.msdyn_numberofresources                                                     |
| msdyn_projecttask.msdyn_remaininghours                                                        |
| msdyn_projecttask.msdyn_resourceutilization                                                   |
| msdyn_projecttask.msdyn_salesestimatecontour                                                  |
| msdyn_projecttask.msdyn_scheduledhours                                                        |
| msdyn_projecttask.msdyn_wbsid                                                                 |

### <a name="msdyn_projecttaskstatususer"></a>msdyn_projecttaskstatususer

| Camps                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttaskstatususer.msdyn_bookableresource                                            |
| msdyn_projecttaskstatususer.msdyn_description                                                 |
| msdyn_projecttaskstatususer.msdyn_expectedcompletiondate                                      |
| msdyn_projecttaskstatususer.msdyn_expectedhourstocomplete                                     |
| msdyn_projecttaskstatususer.msdyn_iscompleted                                                 |
| msdyn_projecttaskstatususer.msdyn_name                                                        |
| msdyn_projecttaskstatususer.msdyn_percentcomplete                                             |
| msdyn_projecttaskstatususer.msdyn_projecttaskid                                               |
| msdyn_projecttaskstatususer.msdyn_projecttaskstatusindicator                                  |
| msdyn_projecttaskstatususer.msdyn_projecttaskstatususerid                                     |

### <a name="msdyn_projectteam"></a>msdyn_projectteam

| Camps                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projectteam.msdyn_applicantcount                                                        |
| msdyn_projectteam.msdyn_sol·licitants disponibles                                                   |
| msdyn_projectteam.msdyn_assignedhours                                                         |
| msdyn_projectteam.msdyn_description                                                           |
| msdyn_projectteam.msdyn_de                                                                  |
| msdyn_projectteam.msdyn_horesrequested                                                        |
| msdyn_projectteam.msdyn_membershipstatus                                                      |
| msdyn_projectteam.msdyn_número                                                                |
| msdyn_projectteam.msdyn_to                                                                    |

### <a name="msdyn_projectteammembersignup"></a>msdyn_projectteammembersignup

| Camps                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projectteammembersignup.msdyn_bookableresource                                          |
| msdyn_projectteammembersignup.msdyn_membershipstatus                                          |
| msdyn_projectteammembersignup.msdyn_name                                                      |
| msdyn_projectteammembersignup.msdyn_projectteammembersignupid                                 |
| msdyn_projectteammembersignup.msdyn_teammembership                                            |

### <a name="msdyn_projecttransactioncategory"></a>msdyn_projecttransactioncategory

| Camps                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttransactioncategory.msdyn_billingtype                                            |
| msdyn_projecttransactioncategory.msdyn_name                                                   |
| msdyn_projecttransactioncategory.msdyn_projecte                                                |
| msdyn_projecttransactioncategory.msdyn_projecttransactioncategoryid                           |
| msdyn_projecttransactioncategory.msdyn_transactioncategory                                    |

### <a name="msdyn_quotelineinvoiceschedule"></a>msdyn_quotelineinvoiceschedule

| Camps                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_quotelineinvoiceschedule.msdyn_quoteline                                                |
| msdyn_quotelineresourcecategory.msdyn_quoteline                                               |
| msdyn_quotelinescheduleofvalue.msdyn_quoteline                                                |
| msdyn_quotelinetransaction.msdyn_quoteline                                                    |
| msdyn_quotelinetransactioncategory.msdyn_quoteline                                            |
| msdyn_quotelinetransactionclassification.msdyn_quoteline                                      |

### <a name="msdyn_resourceassignment"></a>msdyn_resourceassignment

| Camps                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_resourceassignment.msdyn_hores                                                          |
| msdyn_resourceassignment.msdyn_fromdate                                                       |
| msdyn_resourceassignment.msdyn_msprojectclientid                                              |
| msdyn_resourceassignment.msdyn_todate                                                         |
| msdyn_resourceassignmentdetail.msdyn_duration                                                 |
| msdyn_resourceassignmentdetail.msdyn_de                                                     |
| msdyn_resourceassignmentdetail.msdyn_name                                                     |
| msdyn_resourceassignmentdetail.msdyn_resourceassignmentdetailid                               |
| msdyn_resourceassignmentdetail.msdyn_resourceassignmentid                                     |

### <a name="salesorderdetail"></a>salesorderdetail

| Camps                                                    |
|-----------------------------------------------------------------------------------------------|
| salesorderdetail.msdyn_quoteline                                                              |

