---
title: Determinació del tipus d'implementació
description: En aquest tema es proporciona informació per ajudar-vos a determinar el tipus d'implementació correcte del Project Operations per a la vostra empresa.
author: stsporen
ms.date: 03/15/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 4be8e69c5b6ff1ed65e9484a9b427bb428f7ff3e6dc597c615d5586da52867ef
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994624"
---
# <a name="determine-your-deployment-type"></a>Determinació del tipus d'implementació

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

> [!IMPORTANT]
> Després d'adquirir la llicència, comenceu aquí per determinar el millor model d'implementació del Dynamics 365 Project Operations utilitzant el [Flux d'instal·lació guiada](https://aka.ms/provisionprojectoperations).
> Després d'haver acabat el flux d'instal·lació guiada, se us dirigirà al portal d'administració correcte per completar la instal·lació. Vegeu els detalls d'implementació per completar la instal·lació.


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a>Clients existents del Dynamics que utilitzen el Dynamics 365 Project Service Automation
El Project Operations inclou les capacitats incloses al Project Service Automation. Es llançarà un camí d'actualització per a aquests clients a la fase 1 de llançament de 2021.

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a>Clients existents del Dynamics 365 Finance que utilitzen l'administració de projectes i la comptabilitat 

Els clients existents del Finance que utilitzen la funcionalitat d'administració de projectes i comptabilitat poden continuar utilitzant-la sense canvis. Vegeu [Project Operations per a escenaris mantinguts en existències/d’ordre de producció](#pma).


## <a name="deployment-regions"></a>Regions d'implementació
Per determinar quines regions admeten la implementació del Project Operations, vegeu [Disponibilitat geogràfica per a l'informe del Dynamics 365 i de Power Platform](https://dynamics.microsoft.com/en-us/geographic-availability/). Seleccioneu **Visualitza l'informe** i expandiu **Dynamics 365 > Aplicacions d'operacions > Dynamics 365 Project Operations** per veure les regions admeses.

## <a name="deployment-types"></a>Tipus d'implementació
El Project Operations admet diverses opcions de implementació per adaptar-se a les vostres necessitats. Tant si sou un client nou o existent del Dynamics 365, el Project Operations pot ajudar-vos a satisfer les vostres necessitats.

El nostre [qüestionari d'implementació](https://aka.ms/provisionprojectoperations) us ajudarà a determinar la implementació adequada. Els resultats us orienten cap a un dels tipus d'implementació següents:

- [Implementació bàsica: tracte de facturació proforma](#lite)
- [Project Operations per a escenaris de recursos/no mantinguts en existències](#integrated)
- [Project Operations per a escenaris mantinguts en existències/d’ordre de producció](#pma)

El Project Operations admet escenaris d'existències/ordre de producció i escenaris sense existències/basats en recursos en el mateix entorn mitjançant configuracions de nivell d'entitat legal. Per exemple, Contoso pot utilitzar les capacitats d'ordre de producció o emmagatzematge a la seva instal·lació de fabricació dels EUA (Entitat legal = Fabricació de Contoso als Estats Units). Contoso pot utilitzar les capacitats sense existències/basades en recursos en la seva instal·lació de serveis de Contoso Robotics Arms al Regne Unit (Entitat legal = Contoso Robotics Regne Unit).

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a>Implementació bàsica: tracte de facturació proforma

La implementació bàsica inclou les capacitats següents:

- Procés de venda per a projectes que amplien l'experiència d'aplicació del Dynamics 365 Sales
- Planificació de projectes mitjançant el Microsoft Project per al web
- Preus multidimensionals
- Administració de recursos unificada
- Seguiment de temps
- Despesa bàsica
- Facturació proforma per a la revisió i edició de l'Administrador de projectes 

#### <a name="deployment-steps"></a>Passos d'implementació
Determineu el millor model d'implementació del Project Operations mitjançant el [qüestionari d'implementació](https://aka.ms/provisionprojectoperations).

Per a aquesta implementació, vegeu [Inscripció a versions preliminars de subscripcions](lite-preview-subscription-sign-up.md) i [Proveïment d'un entorn nou](lite-deployment.md). 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a>Project Operations per a escenaris de recursos/no mantinguts en existències
El Project Operations per a escenaris de recursos/sense existències inclou les capacitats següents:
 
- Procés de venda per a projectes que amplien l'aplicació Dynamics 365 Sales
- Planificació de projectes mitjançant el Microsoft Project per al web
- Preus multidimensionals
- Administració de recursos unificada
- Seguiment de temps
- Despesa bàsica
- Despesa total
- OCR de rebuts
- Facturació proforma i orientada al client 
- Reconeixement d'ingressos per a projectes

#### <a name="deployment-steps"></a>Passos d'implementació
Determineu el millor model d'implementació del Project Operations mitjançant el [qüestionari d'implementació](https://aka.ms/provisionprojectoperations).

Per a aquesta implementació, vegeu [Inscripció a versions preliminars de subscripcions](resource-sign-up-preview-subscription.md) i [Proveïment d'un entorn nou](resource-provision-new-environment.md). 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a>Project Operations per a escenaris mantinguts en existències/d’ordre de producció

- Planificació del projecte mitjançant WBS
- Administració de recursos
- Seguiment de temps
- Despesa total
- OCR de rebuts
- Facturació completa
- Reconeixement d'ingressos
- Comandes de producció
- Suport de materials amb existències amb inventari

#### <a name="deployment-steps"></a>Passos d'implementació
Determineu el millor model d'implementació del Project Operations mitjançant el [qüestionari d'implementació](https://aka.ms/provisionprojectoperations).

Per a aquesta implementació, vegeu [Inscripció a versions preliminars de subscripcions](/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=%2fdynamics365%2ffinance%2ftoc.json) i [Proveïment d'un entorn nou](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=%2fdynamics365%2ffinance%2ftoc.json). 



[!INCLUDE[footer-include](../includes/footer-banner.md)]