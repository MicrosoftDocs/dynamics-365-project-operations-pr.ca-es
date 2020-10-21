---
title: Tipus d'implementació
description: En aquest tema es proporciona informació per ajudar-vos a determinar el tipus d'implementació correcte del Project Operations per a la vostra empresa.
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: c3cf378caae4510482a8ee6771bf2e6decfe3b48
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948758"
---
# <a name="deployment-types"></a>Tipus d'implementació

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

> [!IMPORTANT]
> Després d'adquirir la llicència, comenceu aquí per determinar el millor model d'implementació del Dynamics 365 Project Operations mitjançant el [Flux d'instal·lació guiada](https://aka.ms/provisionprojectoperations).
> Després d'haver acabat el flux d'instal·lació guiada, se us dirigirà al portal d'administració correcte per completar la instal·lació. Per completar la instal·lació, vegeu els detalls de la implementació.


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a>Clients existents del Dynamics que utilitzen el Dynamics 365 Project Service Automation
El Project Operations inclou les capacitats incloses al Project Service Automation. En el futur es publicarà una ruta d'actualització per a aquests clients.

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a>Clients existents del Dynamics 365 Finance que utilitzen l'administració de projectes i la comptabilitat 

Els clients del Finance que utilitzin la funcionalitat d'administració de projectes i comptabilitat poden continuar utilitzant-la. Vegeu [Project Operations per a escenaris mantinguts en existències/d’ordre de producció](#pma).

El Project Operations admet diverses opcions de implementació per adaptar-se a les vostres necessitats. Tant si sou un client nou o existent del Dynamics 365, el Project Operations pot ajudar-vos a satisfer les vostres necessitats.

El nostre [qüestionari d'implementació](https://aka.ms/provisionprojectoperations) us ajudarà a determinar la implementació adequada. Els resultats us orienten cap a un dels tipus d'implementació següents:

- [Implementació bàsica: tracte de facturació proforma](#lite)
- [Project Operations per a escenaris de recursos/no mantinguts en existències](#integrated)
- [Project Operations per a escenaris mantinguts en existències/d’ordre de producció](#pma)

El Project Operations admet escenaris d'existències/ordre de producció i escenaris sense existències/basats en recursos en el mateix entorn mitjançant configuracions de nivell d'entitat legal. Per exemple, Contoso pot aprofitar les capacitats d'existències/ordre de producció a la seva planta de fabricació de EUA (entitat legal = Contoso Manufacturing United States) i capacitats sense existències/basades en recursos a la seva planta de servei de Contoso Robotics Arms del Regne Unit (entitat legal = Contoso Robotics United Kingdom).

## <a name="a-namelitelite-deployment---deal-to-proforma-invoicing"></a><a name="lite"><a/>Implementació bàsica: tracte de facturació proforma
La implementació bàsica inclou les capacitats següents:

- Planificació de projectes mitjançant el Microsoft Project per al web
- Preus multidimensionals
- Administració de recursos unificada
- Seguiment de temps
- Despesa bàsica
- Proposta de factura

### <a name="deployment-steps"></a>Passos d'implementació:
Determineu el millor model d'implementació del Project Operations mitjançant el [qüestionari d'implementació](https://aka.ms/provisionprojectoperations).

Per a aquesta implementació, vegeu [Inscripció a versions preliminars de subscripcions](lite-preview-subscription-sign-up.md) i [Proveïment d'un entorn nou](lite-deployment.md). 


## <a name="a-nameintegratedproject-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"><a/>Project Operations per a escenaris de recursos/no mantinguts en existències
El Project Operations per a escenaris de recursos/sense existències inclou les capacitats següents:
  
- Planificació de projectes mitjançant el Microsoft Project per al web
- Preus multidimensionals
- Administració de recursos unificada
- Seguiment de temps
- Despesa bàsica
- Despesa total
- OCR de rebuts
- Facturació completa
- Reconeixement d'ingressos

### <a name="deployment-steps"></a>Passos d'implementació:
Determineu el millor model d'implementació del Project Operations mitjançant el [qüestionari d'implementació](https://aka.ms/provisionprojectoperations).

Per a aquesta implementació, vegeu [Inscripció a versions preliminars de subscripcions](resource-sign-up-preview-subscription.md) i [Proveïment d'un entorn nou](resource-provision-new-environment.md). 


## <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a>Project Operations per a escenaris mantinguts en existències/d’ordre de producció

- Planificació del projecte mitjançant WBS
- Administració de recursos
- Seguiment de temps
- Despesa total
- OCR de rebuts
- Facturació completa
- Reconeixement d'ingressos
- Comandes de producció
- Suport de materials

### <a name="deployment-steps"></a>Passos d'implementació:
Determineu el millor model d'implementació del Project Operations mitjançant el [qüestionari d'implementació](https://aka.ms/provisionprojectoperations).

Per a aquesta implementació, vegeu [Inscripció a versions preliminars de subscripcions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) i [Proveïment d'un entorn nou](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json). 



