---
title: Versions d'assignació de doble escriptura del Project Operations
description: En aquest article es proporciona la llista de mapes de doble escriptura necessaris per a Dynamics 365 Project Operations.
author: sigitac
ms.date: 04/22/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: ee0b6a1722405e6a50c42db6bd2a25b872c6118c
ms.sourcegitcommit: 51745acac29dfacba43a4003d86baff4d6ca2fb8
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/14/2022
ms.locfileid: "8959605"
---
# <a name="project-operations-dual-write-map-versions"></a>Versions d'assignació de doble escriptura del Project Operations

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

Per utilitzar el Dynamics 365 Project Operations per a escenaris de recursos/sense existències, cal que un conjunt d'assignacions de doble escriptura s'executin a l'entorn. 

## <a name="prerequisite-maps-dual-write-orchestration-solution"></a>Assignacions dels requisits previs: solució d’orquestració d’escriptura doble

Les assignacions següents són els requisits previs necessaris per a la solució del Project Operations. Assegureu-vos d'executar les assignacions enumerades a la taula següent i qualssevol assignacions de taula relacionades al vostre entorn.

| Assignació de taules | Sincronització inicial |
| --- | --- |
| Llibre major (msdyn_ledgers) | Requereix la sincronització inicial per a l'assignació de taules i tots els requisits previs. El màster per a la sincronització inicial són les aplicacions de finances i operacions. |
| Entitats jurídiques (cdm_companies) | No és obligatori. El sistema emplena aquesta entitat automàticament quan s'enllacen entorns amb doble escriptura. |
| Clients V3 (comptes) | No és necessari per al proveïment. |
| Proveïdors V2 (msdyn_vendors) | No és necessari per al proveïment. |

1. A la llista d'assignacions, seleccioneu l'assignació Llibre major **(msdyn\_ledgers)** amb tots els requisits previs i activeu la casella de selecció **Sincronització inicial**. Al camp Mestre per a la **sincronització** inicial, seleccioneu **Aplicacions** de finances i operacions tant per al mapa del llibre major com per a tots els mapes de llocs de prerequisits. Seleccioneu **Executa**.

![Sincronització de l'assignació de llibres majors.](media/DW6.png)

2. Seguiu els mateixos passos per a totes les assignacions de taula restants enumerades a la taula anterior. No activeu la casella de selecció **Sincronització inicial** en executar aquestes assignacions.

## <a name="project-operations-dual-write-maps"></a>Assignacions de doble ecriptura del Project Operations

Les assignacions següents són necessàries per a una solució del Project Operations. Les versions d'un mapa amb doble escriptura es mostren a partir de l'actualització del maig del 2021 del Project Operations, la versió 4.10.0.186.

| Assignació d'entitats | Versió més recent | Sincronització inicial | Versió Dynamics 365 Finance necessària |
| --- | --- | --- | --- |
| Entitat d'integració per a les relacions de transaccions del projecte (msdyn\_transactionconnections) | 1.0.0.0 | No és necessari per al proveïment. ||
| Capçaleres de contracte del projecte (comandes de vendes) | 1.0.0.1 | No és necessari per al proveïment. ||
| Línies de contracte del projecte (salesorderdetails) | 1.0.0.0 | No és necessari per al proveïment. ||
| Origen del fons del projecte (msdyn_projectcontractsplitbillingrules) | 1.0.0.2 | No és necessari per al proveïment. ||
| Taula d'integració del Project Operations per a estimacions de materials (msdyn\_estimatelines) | 1.0.0.0 | No és necessari per al proveïment. ||
| Propostes de factura del projecte V2 (factures) | 1.0.0.3 | No és necessari per al proveïment. ||
| Valors reals d'integració del Project Operations (msdyn_actuals) | 1.0.0.14 | No és necessari per al proveïment. ||
| Fites de línia de contracte d'integració al Project Operations (msdyn_contractlinescheduleofvalues) | 1.0.0.4 | No és necessari per al proveïment. ||
| Entitat d'integració del Project Operations per a estimacions de despeses (msdyn_estimatelines) | 1.0.0.2 | No és necessari per al proveïment. ||
| Entitat d'integració del Project Operations per a l'estimació d'hores (msdyn_resourceassignments) | 1.0.0.5 | No és necessari per al proveïment. ||
| Entitat d'exportació de categories de despeses del projecte d'integració del Project Operations (msdyn_expensecategories) | 1.0.0.1 | No és necessari per al proveïment. ||
| Entitat d'exportació de despeses del projecte d'integració del Project Operations (msdyn_expenses) | 1.0.0.3 | No és necessari per al proveïment. ||
| Entitat d'exportació de factura del proveïdor del projecte de la integració del Project Operations (msdyn_projectvendorinvoices) | 1.0.0.1 | No és necessari per al proveïment. |10.0.26 o posterior|
| Entitat d'exportació de la línia de factura del proveïdor del projecte de la integració del Project Operations (msdyn_projectvendorinvoicelines) | 1.0.0.4 | No és necessari per al proveïment. | 10.0.26 o posterior |
| Funcions de recurs del projecte per a totes les empreses (bookableresourcecategories) | 1.0.0.1 | Requereix una sincronització inicial perquè l'assignació de taules sincronitzi les funcions de recurs de l'administrador de projectes i del membre de l'equip que s'han emplenat a l'entorn del Dataverse del Dynamics 365 el proveïment. El Dataverse és l'origen principal de la sincronització inicial. ||
| Tasques del projecte (msdyn_projecttasks) | 1.0.0.4 | No és necessari per al proveïment. ||
| Categories de transacció del projecte (msdyn_transactioncategories) | 1.0.0.0 | No és necessari per al proveïment. ||
| Projectes V2 (msdyn_projects) | 1.0.0.2 | No és necessari per al proveïment. ||

Completeu els passos següents per executar les assignacions enumerades.

1. Habiliteu les funcions de recurs de projecte per a l'assignació de taules de **totes les empreses (bookableresourcecategories)**, ja que aquesta assignació necessita la sincronització inicial. Al camp **Patró per a la sincronització inicial**, seleccioneu **Common data service**. 

 ![Sincronització d'assignació de taules de funció de recurs.](media/6ResourceInitialSync.jpg)

 Espereu fins que l'estat de l'assignació sigui **S'està executant** abans de passar al pas següent.

2. Seleccioneu totes les assignacions necessàries restants. Les podeu filtrar per la llista d'assignacions d'escriptura doble utilitzant la paraula clau **Projecte** a la cerca de la part superior dreta. Podeu seleccionar totes les assignacions i, a continuació, executar-les. Per obtenir més informació, vegeu [Administrar diverses assignacions de taules](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/multiple-entity-maps). Assegureu-vos d'habilitar i executar assignacions d'entitats relacionades.

### <a name="project-operations-dual-write-map-versions"></a>Versions d'assignació de doble escriptura del Project Operations

Executeu sempre la versió més recent de l'assignació al vostre entorn. Pot ser que algunes característiques i capacitats no funcionin correctament si hi ha alguna de les condicions següents:

- Una assignació no està activada.
- L'última versió de l'assignació no està activada. 
- Les assignacions de taules relacionades no estan activades.

Podeu visualitzar la versió activa de l'assignació a la columna **Versió** de la pàgina **Escriptura doble**. Per activar una versió nova de l'assignació, seleccioneu **Versions de l'assignació de la taula**, seleccioneu la versió més recent i després deseu la versió seleccionada. Si heu personalitzat una assignació de taules llesta per al seu ús, necessitareu tornar a aplicar els canvis. Per a més informació, vegeu [Administració del cicle de vida de les aplicacions](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).
