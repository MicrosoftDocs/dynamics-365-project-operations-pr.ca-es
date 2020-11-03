---
title: Determinació del tipus d'implementació
description: En aquest tema es proporciona informació per ajudar-vos a determinar el tipus d'implementació correcte del Project Operations per a la vostra empresa.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 564f2878553fe3904a7c47c7e80a3b57c763a3b2
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072216"
---
# <a name="determine-your-deployment-type"></a><span data-ttu-id="88f1a-103">Determinació del tipus d'implementació</span><span class="sxs-lookup"><span data-stu-id="88f1a-103">Determine your deployment type</span></span>

<span data-ttu-id="88f1a-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_</span><span class="sxs-lookup"><span data-stu-id="88f1a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="88f1a-105">Després d'adquirir la llicència, comenceu aquí per determinar el millor model d'implementació del Dynamics 365 Project Operations mitjançant el [Flux d'instal·lació guiada](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="88f1a-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="88f1a-106">Després d'haver acabat el flux d'instal·lació guiada, se us dirigirà al portal d'administració correcte per completar la instal·lació.</span><span class="sxs-lookup"><span data-stu-id="88f1a-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="88f1a-107">Vegeu els detalls d'implementació per completar la instal·lació.</span><span class="sxs-lookup"><span data-stu-id="88f1a-107">See the deployment details to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="88f1a-108">Clients existents del Dynamics que utilitzen el Dynamics 365 Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="88f1a-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="88f1a-109">El Project Operations inclou les capacitats incloses al Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="88f1a-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="88f1a-110">En el futur es publicarà una ruta d'actualització per a aquests clients.</span><span class="sxs-lookup"><span data-stu-id="88f1a-110">An upgrade path will be released for these customers in the future.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="88f1a-111">Clients existents del Dynamics 365 Finance que utilitzen l'administració de projectes i la comptabilitat</span><span class="sxs-lookup"><span data-stu-id="88f1a-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="88f1a-112">Els clients del Finance que utilitzin la funcionalitat d'administració de projectes i comptabilitat poden continuar utilitzant-la.</span><span class="sxs-lookup"><span data-stu-id="88f1a-112">Existing customers of Finance who use the Project management and accounting functionality can continue to use this as is.</span></span> <span data-ttu-id="88f1a-113">Vegeu [Project Operations per a escenaris mantinguts en existències/d’ordre de producció](#pma).</span><span class="sxs-lookup"><span data-stu-id="88f1a-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>


## <a name="deployment-types"></a><span data-ttu-id="88f1a-114">Tipus d'implementació</span><span class="sxs-lookup"><span data-stu-id="88f1a-114">Deployment types</span></span>
<span data-ttu-id="88f1a-115">El Project Operations admet diverses opcions de implementació per adaptar-se a les vostres necessitats.</span><span class="sxs-lookup"><span data-stu-id="88f1a-115">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="88f1a-116">Tant si sou un client nou o existent del Dynamics 365, el Project Operations pot ajudar-vos a satisfer les vostres necessitats.</span><span class="sxs-lookup"><span data-stu-id="88f1a-116">Whether you're a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="88f1a-117">El nostre [qüestionari d'implementació](https://aka.ms/provisionprojectoperations) us ajudarà a determinar la implementació adequada.</span><span class="sxs-lookup"><span data-stu-id="88f1a-117">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="88f1a-118">Els resultats us orienten cap a un dels tipus d'implementació següents:</span><span class="sxs-lookup"><span data-stu-id="88f1a-118">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="88f1a-119">Implementació bàsica: tracte de facturació proforma</span><span class="sxs-lookup"><span data-stu-id="88f1a-119">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="88f1a-120">Project Operations per a escenaris de recursos/no mantinguts en existències</span><span class="sxs-lookup"><span data-stu-id="88f1a-120">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="88f1a-121">Project Operations per a escenaris mantinguts en existències/d’ordre de producció</span><span class="sxs-lookup"><span data-stu-id="88f1a-121">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="88f1a-122">El Project Operations admet escenaris d'existències/ordre de producció i escenaris sense existències/basats en recursos en el mateix entorn mitjançant configuracions de nivell d'entitat legal.</span><span class="sxs-lookup"><span data-stu-id="88f1a-122">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="88f1a-123">Per exemple, Contoso pot utilitzar les funcionalitats de comanda amb existències/producció en la seva planta de fabricació dels EUA (Entitat jurídica = Contoso Manufacturing United States).</span><span class="sxs-lookup"><span data-stu-id="88f1a-123">For example, Contoso can use the stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States).</span></span> <span data-ttu-id="88f1a-124">Contoso pot utilitzar les funcionalitats sense existències/basades en recursos en la seva instal·lació de servei de braços robòtics de Contoso al Regne Unit (Entitat jurídica = Contoso Robotics United Kingdom).</span><span class="sxs-lookup"><span data-stu-id="88f1a-124">Contoso can use the non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a><span data-ttu-id="88f1a-125">Implementació bàsica: tracte de facturació proforma</span><span class="sxs-lookup"><span data-stu-id="88f1a-125">Lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="88f1a-126">La implementació bàsica inclou les capacitats següents:</span><span class="sxs-lookup"><span data-stu-id="88f1a-126">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="88f1a-127">Planificació de projectes mitjançant el Microsoft Project per al web</span><span class="sxs-lookup"><span data-stu-id="88f1a-127">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="88f1a-128">Preus multidimensionals</span><span class="sxs-lookup"><span data-stu-id="88f1a-128">Multi-dimensional pricing</span></span>
- <span data-ttu-id="88f1a-129">Administració de recursos unificada</span><span class="sxs-lookup"><span data-stu-id="88f1a-129">Unified Resource Management</span></span>
- <span data-ttu-id="88f1a-130">Seguiment de temps</span><span class="sxs-lookup"><span data-stu-id="88f1a-130">Time Tracking</span></span>
- <span data-ttu-id="88f1a-131">Despesa bàsica</span><span class="sxs-lookup"><span data-stu-id="88f1a-131">Basic Expense</span></span>
- <span data-ttu-id="88f1a-132">Proposta de factura</span><span class="sxs-lookup"><span data-stu-id="88f1a-132">Invoice Proposal</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="88f1a-133">Passos d'implementació</span><span class="sxs-lookup"><span data-stu-id="88f1a-133">Deployment steps</span></span>
<span data-ttu-id="88f1a-134">Determineu el millor model d'implementació del Project Operations mitjançant el [qüestionari d'implementació](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="88f1a-134">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="88f1a-135">Per a aquesta implementació, vegeu [Inscripció a versions preliminars de subscripcions](lite-preview-subscription-sign-up.md) i [Proveïment d'un entorn nou](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="88f1a-135">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a><span data-ttu-id="88f1a-136">Project Operations per a escenaris de recursos/no mantinguts en existències</span><span class="sxs-lookup"><span data-stu-id="88f1a-136">Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="88f1a-137">El Project Operations per a escenaris de recursos/sense existències inclou les capacitats següents:</span><span class="sxs-lookup"><span data-stu-id="88f1a-137">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
  
- <span data-ttu-id="88f1a-138">Planificació de projectes mitjançant el Microsoft Project per al web</span><span class="sxs-lookup"><span data-stu-id="88f1a-138">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="88f1a-139">Preus multidimensionals</span><span class="sxs-lookup"><span data-stu-id="88f1a-139">Multi-dimensional pricing</span></span>
- <span data-ttu-id="88f1a-140">Administració de recursos unificada</span><span class="sxs-lookup"><span data-stu-id="88f1a-140">Unified Resource Management</span></span>
- <span data-ttu-id="88f1a-141">Seguiment de temps</span><span class="sxs-lookup"><span data-stu-id="88f1a-141">Time Tracking</span></span>
- <span data-ttu-id="88f1a-142">Despesa bàsica</span><span class="sxs-lookup"><span data-stu-id="88f1a-142">Basic Expense</span></span>
- <span data-ttu-id="88f1a-143">Despesa total</span><span class="sxs-lookup"><span data-stu-id="88f1a-143">Full Expense</span></span>
- <span data-ttu-id="88f1a-144">OCR de rebuts</span><span class="sxs-lookup"><span data-stu-id="88f1a-144">Receipt OCR</span></span>
- <span data-ttu-id="88f1a-145">Facturació completa</span><span class="sxs-lookup"><span data-stu-id="88f1a-145">Full Invoicing</span></span>
- <span data-ttu-id="88f1a-146">Reconeixement d'ingressos</span><span class="sxs-lookup"><span data-stu-id="88f1a-146">Revenue Recognition</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="88f1a-147">Passos d'implementació</span><span class="sxs-lookup"><span data-stu-id="88f1a-147">Deployment steps</span></span>
<span data-ttu-id="88f1a-148">Determineu el millor model d'implementació del Project Operations mitjançant el [qüestionari d'implementació](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="88f1a-148">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="88f1a-149">Per a aquesta implementació, vegeu [Inscripció a versions preliminars de subscripcions](resource-sign-up-preview-subscription.md) i [Proveïment d'un entorn nou](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="88f1a-149">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="88f1a-150">Project Operations per a escenaris mantinguts en existències/d’ordre de producció</span><span class="sxs-lookup"><span data-stu-id="88f1a-150">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="88f1a-151">Planificació del projecte mitjançant WBS</span><span class="sxs-lookup"><span data-stu-id="88f1a-151">Project planning using WBS</span></span>
- <span data-ttu-id="88f1a-152">Administració de recursos</span><span class="sxs-lookup"><span data-stu-id="88f1a-152">Resource Management</span></span>
- <span data-ttu-id="88f1a-153">Seguiment de temps</span><span class="sxs-lookup"><span data-stu-id="88f1a-153">Time Tracking</span></span>
- <span data-ttu-id="88f1a-154">Despesa total</span><span class="sxs-lookup"><span data-stu-id="88f1a-154">Full Expense</span></span>
- <span data-ttu-id="88f1a-155">OCR de rebuts</span><span class="sxs-lookup"><span data-stu-id="88f1a-155">Receipt OCR</span></span>
- <span data-ttu-id="88f1a-156">Facturació completa</span><span class="sxs-lookup"><span data-stu-id="88f1a-156">Full Invoicing</span></span>
- <span data-ttu-id="88f1a-157">Reconeixement d'ingressos</span><span class="sxs-lookup"><span data-stu-id="88f1a-157">Revenue Recognition</span></span>
- <span data-ttu-id="88f1a-158">Comandes de producció</span><span class="sxs-lookup"><span data-stu-id="88f1a-158">Production Orders</span></span>
- <span data-ttu-id="88f1a-159">Suport de materials</span><span class="sxs-lookup"><span data-stu-id="88f1a-159">Materials support</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="88f1a-160">Passos d'implementació</span><span class="sxs-lookup"><span data-stu-id="88f1a-160">Deployment steps</span></span>
<span data-ttu-id="88f1a-161">Determineu el millor model d'implementació del Project Operations mitjançant el [qüestionari d'implementació](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="88f1a-161">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="88f1a-162">Per a aquesta implementació, vegeu [Inscripció a versions preliminars de subscripcions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) i [Proveïment d'un entorn nou](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span><span class="sxs-lookup"><span data-stu-id="88f1a-162">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 

