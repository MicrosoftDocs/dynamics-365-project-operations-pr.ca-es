---
title: Canvis de característiques del Project Service Automation al Project Operations
description: En aquest article es proporciona informació general sobre els canvis en les característiques del Project Service Automation al Dynamics 365 Project Operations.
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
ms.openlocfilehash: a9c69fc4296d30763f3994a4955e64ab258ceb4f
ms.sourcegitcommit: 675e9f3615e701c5f998de3a5ea3e25df11ae107
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 09/09/2022
ms.locfileid: "9459914"
---
# <a name="feature-changes-from-project-service-automation-to-project-operations"></a>Canvis de característiques del Project Service Automation al Project Operations

L'actualització del Dynamics 365 Project Service Automation al Dynamics 365 Project Operations Lite es farà en tres fases. En aquest article es proporciona informació sobre els canvis principals que podeu esperar veure quan s'hagi completat l'actualització.

| Actualització del lliurament | Fase 1 <br>(Gener de 2022) | Fase 2 <br>(Novembre de 2022) | Fase 3  |
|------------------|------------------------|---------------------------|---------------------------|
| Cap dependència en l'estructura del desglossament del treball (WBS) per als projectes. | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| La WBS s'inclou en els límits admesos actualment del Project Operations. | &nbsp; | :heavy_check_mark: | :heavy_check_mark: |
| La WBS fora dels límits admesos actualment del Project Operations, incloent-hi la compatibilitat amb el Project Desktop Client. | &nbsp; | &nbsp; | :heavy_check_mark: |

## <a name="project-management"></a>Administració de projectes

Els canvis més importants en l'experiència de l'usuari seran en l'àrea de planificació de projectes. El Project Operations adopta una nova experiència moderna per administrar una estructura del desglossament del treball (WBS) amb les capacitats de planificació proporcionades pel [Project for the Web](https://support.microsoft.com/en-us/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5).

## <a name="differences-in-the-scheduling-experience"></a>Diferències en l'experiència de planificació

A la taula següent es resumeixen les diferències de planificació entre el Project Service Automation i el Project Operations.

|  Planificació     |   Project Operations   |   PSA   |
|-----------------|------------------------|---------|
| Plantilles de projecte: capacitat per definir i aplicar plantilles de projecte quan es crea un projecte  |  &nbsp;    | :heavy_check_mark: |
| Integració de l'estructura del desglossament del treball (WBS) del projecte amb el client d'escriptori   |    &nbsp;  | :heavy_check_mark: |
| Restriccions: no comencis abans de, no acabis més tard de  | :heavy_check_mark: |   &nbsp;  |
| Fites: tasques amb durada zero   | :heavy_check_mark:  |  &nbsp;  |
| Les tasques generades per recursos respecten la disponibilitat dels recursos assignats   | :heavy_check_mark: |  &nbsp;    |
| Edició per temps: editar plans i treballar dia a dia   |   &nbsp;  | :heavy_check_mark: |
| Planificació automàtica/manual: utilitzeu el motor de planificació del projecte per planificar automàticament o manualment tasques |  &nbsp; | :heavy_check_mark:  |
| Editar projectes grans directament a la interfície d'usuari: no hi ha cap límit pel que fa a la mida dels plans que es poden editar  | Límit de 500 tasques  | :heavy_check_mark:       |
| Percentatge completat: marca el progrés de la tasca   | :heavy_check_mark:  |  &nbsp;  |
| [Modes de planificació del projecte](../project-management/scheduling-modes.md): defineix el projecte com a unitats fixes, esforç fix o durada fixa | :heavy_check_mark: | &nbsp; |
| Cronologia: creeu i personalitzeu la visualització de la cronologia per visualitzar els detalls de la planificació i comunicar-vos amb les parts interessades. | :heavy_check_mark:  | &nbsp; |
| Tasques basades en l'esforç: planificar el suport del motor per planificar una tasca com a basada en l'esforç  | :heavy_check_mark:  | &nbsp; |
| **Quadre de diàleg d'informació de la tasca**: deseu els detalls de la tasca mitjançant un quadre de diàleg | :heavy_check_mark:  |  &nbsp;  |
| Arrossegar i deixar anar: selecció de múltiples tasques i modificació de la seva posició a la WBS | :heavy_check_mark: | &nbsp;  |
| Visualitzacions persistents flexibles: definició de visualitzacions més granulars dels atributs de tasca   | :heavy_check_mark:  | &nbsp; |
| Ordenar i filtrar la WBS  | :heavy_check_mark:  | &nbsp; |
| Visualització de taulers per a la realització del projecte no en cascada  | :heavy_check_mark:   | &nbsp; |
| Visualització de la cronologia: gràfic de Gantt interactiu utilitzat per visualitzar i editar la WBS   | :heavy_check_mark:  | &nbsp; |
| Dreceres de teclat: utilitzeu les dreceres de teclat per a les operacions habituals, com ara sagnar o inserir  | :heavy_check_mark:  |  &nbsp; |
| Desfer diversos nivells: feu una anàlisi what-if si voleu comprendre completament l'impacte dels canvis revertint i tornar a aplicar un conjunt d'operacions sencer | :heavy_check_mark: | &nbsp; |
| Retalla/copia/enganxa: col·laboreu en el desenvolupament de planificacions copiant i enganxant detalls de la planificació entre aplicacions  | :heavy_check_mark: | &nbsp; |
| Llistes de verificació de tasques: afegiu fins a 20 elements de la llista de verificació a una tasca   | :heavy_check_mark: | &nbsp; |

## <a name="project-planning"></a>Planificació del projecte

La pàgina **Projecte** al Project Operations té un nombre considerable de diferències en comparació amb la pàgina **Projecte** del Project Service Automation.

Les accions següents s'han eliminat de la pàgina **Projectes** com a part de l'actualització de la Fase 1:

  - **Obre a l'MS Project**
  - **Crea una plantilla**
  - **Desenllaça de l'MS Project**

La pàgina **Projecte** del Project Operations inclou les següents pestanyes noves.

- **Estimacions de material**
- **Configuració de facturació de la tasca**

S'ha eliminat la pestanya **Estat** i el camp **Estat** es troba ara a la pestanya **Resum** amb el mode de planificació del projecte.

   ![Actualitzacions a la pàgina Projecte.](media/projectform.png)

La pestanya **Planificació** ha canviat de nom per la pestanya **Tasca** i inclou la nova experiència de planificació de projectes amb el Project for the Web.

   ![Pestanya Noves tasques del projecte.](media/tasktab.png)

## <a name="scheduling-modes"></a>Modes de planificació

El Project Operations ha introduït una nova característica: els [Modes de planificació](../project-management/scheduling-modes.md). Tots els projectes existents del Project Service Automation prendran per defecte la **Durada fixa** al Project Operations. Tanmateix, el valor per defecte dels projectes nous es pot administrar anant a **Configuració** > **Paràmetres** > **Paràmetre** > **Mode de planificació**.

   ![Configuració de paràmetres de projecte per al mode de planificació.](media/projectparameter.png)

## <a name="project-planning-limits"></a>Límits de planificació del projecte

El Project Operations es basa en Project for the Web per a totes les operacions de planificació de projectes. Project for the Web administra l'estructura del desglossament del treball mitjançant els límits de la taula següent.

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

Després d'actualitzar al Project Operations, heu d'utilitzar les API de Planificació de projectes per executar les operacions de creació, actualització i supressió a les entitats següents:

|   Nom de l’entitat           |   Nom lògic de l’entitat       |
|-------------------------|-----------------------------|
| Project                 | msdyn_project               |
| Tasca del projecte            | msdyn_projecttask           |
| Dependència de les tasques del projecte | msdyn_projecttaskdependency |
| Assignació de recursos     | msdyn_resourceassignment    |
| Dipòsit de projecte          | msdyn_projectbucket         |
| Membre de l'equip del projecte     | msdyn_projectteam           |

Si actualment teniu personalitzacions que impliquen aquestes entitats, vegeu [Utilitzar les API de planificació de projectes per realitzar operacions amb les entitats de Planificació](../project-management/schedule-api-preview.md) per a orientació en la implementació.

## <a name="data-model-changes"></a>Canvis en e model de dades

Com a part de l'actualització de la Fase 1, s'han fet canvis en el model de dades. Aquests canvis són principalment canvis en els camps d'entitats existents. A la Fase 1, les entitats **msydn_project** i **msdyn_projectteam** són una refactorització de personalitzacions. 

> [!IMPORTANT]
> Aquesta secció s'actualitzarà amb entitats addicionals a mesura que es completin les fases d'actualització futures.

Els camps següents s'han substituït per camps nous.

|   Entity          |   Nom lògic anterior   |   Nom lògic nou    |
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
| msdyn_project     | msdyn_actualfeesales                         | Mostra l'agregació de les vendes reals de la tarifa del projecte. Per utilitzar-se només al Project Service Automation. |
| msdyn_project     | msdyn_actualmaterialcost                     | Mostra l'agregació del cost real de materials del projecte. Per utilitzar-se només al Project Service Automation. |
| msdyn_project     | msdyn_actualmaterialsales                    | Mostra l'agregació de les vendes reals de material del projecte. Per utilitzar-se només al Project Service Automation. |
| msdyn_project     | msdyn_businesscase                           |                |
| msdyn_project     | msdyn_contractlineproject                    | La línia de contracte associada a aquest projecte. |
| msdyn_project     | msdyn_copyprojectcorrelationid               | Aquest camp és intern del sistema i s'utilitza per a **Copia el projecte** en relació amb Identificador de correlació. Per utilitzar-se només al Project Service Automation. |
| msdyn_project     | msdyn_copyprojectsessionid                   | Aquest camp és intern del sistema i s'utilitza per a **Copia el projecte** en relació amb Identificador de sessió. Per utilitzar-se només al Project Service Automation. |
| msdyn_project     | msdyn_globalrevisiontoken                    | Testimoni de revisió global de l'xRM de l'última sincronització des del servei de planificació del projecte. |
| msdyn_project     | msdyn_msprojectdocument                      | El document del Microsoft Project que pertany al projecte. |
| msdyn_project     | msdyn_plannedmaterialcost                    | L'agregació del cost de materials previst del projecte. Per utilitzar-se només al Project Service Automation. |
| msdyn_project     | msdyn_plannedmaterialsales                   | L'agregació de les vendes de materials previstes del projecte. Per utilitzar-se només al Project Service Automation. |
| msdyn_project     | msdyn_program                                | Programa amb el qual està relacionat aquest projecte. |
| msdyn_project     | msdyn_quotelineproject                       | La línia d'oferta associada a aquest projecte. |
| msdyn_project     | msdyn_replaylogheader                        | La capçalera per als registres de reproducció. |
| msdyn_project     | msdyn_schedulemode                           | El mode de planificació per defecte utilitzat per a totes les tasques del projecte.  |
| msdyn_project     | msdyn_taskearlieststart                      | La primera data d'inici de qualsevol tasca del projecte.  |
| msdyn_project     | msdyn_valuestatement                         |                |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | El membre de l'equip del projecte del qual s'ha copiat aquest membre de l'equip del projecte. |
| msdyn_projectteam | msdyn_creategenericteammemberwithrequirement | Indica si es crearan els requisits de recursos per a un membre de l'equip genèric de nova creació.  |
| msdyn_projectteam | msdyn_deletestatus                           | Estat de supressió del membre de l'equip per fer el seguiment de si una sol·licitud de supressió s'ha enviat al Project Scheduling Service i si reenvia satisfactòriament una resposta dins del temps previst. |
| msdyn_projectteam | msdyn_effortcompleted                        | Fa el seguiment de l'esforç realitzat pel membre de l'equip a les seves assignacions. |
| msdyn_projectteam | msdyn_effortremaining                        | Fa el seguiment de l'esforç que ha de completar del membre de l'equip a les seves assignacions. |
| msdyn_projectteam | msdyn_markedfordeletiontimer                 | Període d'espera des del moment en què el membre de l'equip envia una sol·licitud de supressió al servei de planificació del projecte fins que el membre de l'equip se suprimeix realment al Microsoft Dataverse.|
| msdyn_projectteam | msdyn_markedfordeletiontimestamp             | Data i hora de registre quan s'envia la sol·licitud de supressió del membre de l'equip al servei de planificació del projecte. |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | Mostra el membre de l'equip del projecte del qual s'ha copiat aquest membre de l'equip del projecte.  |

## <a name="project-templates"></a>Plantilles de projecte

El Project Operations no proporciona suport per a les plantilles de projecte. Tanmateix, podeu replicar gran part de la funcionalitat principal amb l'ús de l'[API de còpia del projecte](../project-management/dev-copy-project.md).

## <a name="desktop-add-in-support"></a>Compatibilitat amb el complement d'escriptori

La compatibilitat amb el complement del Microsoft Project Desktop no estarà disponible a les primeres 2 fases de l'actualització. A la Fase 3, els clients que tenen projectes d'una mida superior als límits admesos actualment al Project for the Web podran utilitzar el complement d'escriptori.

## <a name="editing-resource-assignment-contours"></a>Edició dels contorns de l'assignació de recursos

La capacitat d'editar els contorns de l'assignació de recursos estarà disponible quan s'estiguin assoliments 2 de l'actualització.

## <a name="billing-and-pricing"></a>Facturació i preus

S'han afegit les característiques noves següents al Project Operations. Aquestes característiques són additives i no afecten el model de dades del Project Service Automation.

- [Registre de l'ús de materials en projectes i tasques de projectes](../material/material-usage-log.md)
- [Administració de subcontractes](../pro/subcontracting/managing-subcontracts-overview.md)
- [Avançaments i contractes de bestreta](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Estat que no s'ha de superar del contracte i validacions](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- [Facturació basada en tasques](../pro/sales/mapping-projects-tasks-quote-line-sales.md)

## <a name="deprecated-components"></a>Components obsolets

A les taules següents es documenten tots els camps obsolets que s'han desplaçat a l'actualització posterior a la solució de components obsoleta. Per obtenir més informació i un enllaç a la solució, vegeu [Components obsolets entre Dynamics 365 Project Service Automation 3x i Project Operations 4x](https://github.com/microsoft/Dynamics365-Project-Operations-PowerApps/tree/main/3x-4x-deprecated-solution).

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
| msdyn_findworkevent.msdyn_value                                                               |
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
| msdyn_opportunitylinetransaction.msdyn_percent                                                |
| msdyn_opportunitylinetransaction.msdyn_price                                                  |
| msdyn_opportunitylinetransaction.msdyn_price_base                                             |
| msdyn_opportunitylinetransaction.msdyn_pricelist                                              |
| msdyn_opportunitylinetransaction.msdyn_product                                                |
| msdyn_opportunitylinetransaction.msdyn_project                                                |
| msdyn_opportunitylinetransaction.msdyn_quantity                                               |
| msdyn_opportunitylinetransaction.msdyn_resourcecategory                                       |
| msdyn_opportunitylinetransaction.msdyn_resourceorganizationalunitid                           |
| msdyn_opportunitylinetransaction.msdyn_startdatetime                                          |
| msdyn_opportunitylinetransaction.msdyn_task                                                   |
| msdyn_opportunitylinetransaction.msdyn_transactioncategory                                    |
| msdyn_opportunitylinetransaction.msdyn_transactionclassification                              |
| msdyn_opportunitylinetransaction.msdyn_transactiontypecode                                    |
| msdyn_opportunitylinetransaction.msdyn_unit                                                   |
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
| msdyn_projectteam.msdyn_applicantsavailable                                                   |
| msdyn_projectteam.msdyn_assignedhours                                                         |
| msdyn_projectteam.msdyn_description                                                           |
| msdyn_projectteam.msdyn_from                                                                  |
| msdyn_projectteam.msdyn_hoursrequested                                                        |
| msdyn_projectteam.msdyn_membershipstatus                                                      |
| msdyn_projectteam.msdyn_number                                                                |
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
| msdyn_projecttransactioncategory.msdyn_project                                                |
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
| msdyn_resourceassignment.msdyn_hours                                                          |
| msdyn_resourceassignment.msdyn_fromdate                                                       |
| msdyn_resourceassignment.msdyn_msprojectclientid                                              |
| msdyn_resourceassignment.msdyn_todate                                                         |
| msdyn_resourceassignmentdetail.msdyn_duration                                                 |
| msdyn_resourceassignmentdetail.msdyn_from                                                     |
| msdyn_resourceassignmentdetail.msdyn_name                                                     |
| msdyn_resourceassignmentdetail.msdyn_resourceassignmentdetailid                               |
| msdyn_resourceassignmentdetail.msdyn_resourceassignmentid                                     |

### <a name="salesorderdetail"></a>salesorderdetail

| Camps                                                    |
|-----------------------------------------------------------------------------------------------|
| salesorderdetail.msdyn_quoteline                                                              |

