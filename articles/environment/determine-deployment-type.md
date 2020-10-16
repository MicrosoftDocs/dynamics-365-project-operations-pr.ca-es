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
# <a name="deployment-types"></a><span data-ttu-id="59ab1-103">Tipus d'implementació</span><span class="sxs-lookup"><span data-stu-id="59ab1-103">Deployment types</span></span>

<span data-ttu-id="59ab1-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_</span><span class="sxs-lookup"><span data-stu-id="59ab1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="59ab1-105">Després d'adquirir la llicència, comenceu aquí per determinar el millor model d'implementació del Dynamics 365 Project Operations mitjançant el [Flux d'instal·lació guiada](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="59ab1-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="59ab1-106">Després d'haver acabat el flux d'instal·lació guiada, se us dirigirà al portal d'administració correcte per completar la instal·lació.</span><span class="sxs-lookup"><span data-stu-id="59ab1-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="59ab1-107">Per completar la instal·lació, vegeu els detalls de la implementació.</span><span class="sxs-lookup"><span data-stu-id="59ab1-107">See the deployment details below to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="59ab1-108">Clients existents del Dynamics que utilitzen el Dynamics 365 Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="59ab1-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="59ab1-109">El Project Operations inclou les capacitats incloses al Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="59ab1-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="59ab1-110">En el futur es publicarà una ruta d'actualització per a aquests clients.</span><span class="sxs-lookup"><span data-stu-id="59ab1-110">An upgrade path will be released for these customers in the future.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="59ab1-111">Clients existents del Dynamics 365 Finance que utilitzen l'administració de projectes i la comptabilitat</span><span class="sxs-lookup"><span data-stu-id="59ab1-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="59ab1-112">Els clients del Finance que utilitzin la funcionalitat d'administració de projectes i comptabilitat poden continuar utilitzant-la.</span><span class="sxs-lookup"><span data-stu-id="59ab1-112">Existing customers of Finance who use the Project management and accounting functionality can continue use this as is.</span></span> <span data-ttu-id="59ab1-113">Vegeu [Project Operations per a escenaris mantinguts en existències/d’ordre de producció](#pma).</span><span class="sxs-lookup"><span data-stu-id="59ab1-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>

<span data-ttu-id="59ab1-114">El Project Operations admet diverses opcions de implementació per adaptar-se a les vostres necessitats.</span><span class="sxs-lookup"><span data-stu-id="59ab1-114">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="59ab1-115">Tant si sou un client nou o existent del Dynamics 365, el Project Operations pot ajudar-vos a satisfer les vostres necessitats.</span><span class="sxs-lookup"><span data-stu-id="59ab1-115">Whether you are a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="59ab1-116">El nostre [qüestionari d'implementació](https://aka.ms/provisionprojectoperations) us ajudarà a determinar la implementació adequada.</span><span class="sxs-lookup"><span data-stu-id="59ab1-116">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="59ab1-117">Els resultats us orienten cap a un dels tipus d'implementació següents:</span><span class="sxs-lookup"><span data-stu-id="59ab1-117">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="59ab1-118">Implementació bàsica: tracte de facturació proforma</span><span class="sxs-lookup"><span data-stu-id="59ab1-118">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="59ab1-119">Project Operations per a escenaris de recursos/no mantinguts en existències</span><span class="sxs-lookup"><span data-stu-id="59ab1-119">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="59ab1-120">Project Operations per a escenaris mantinguts en existències/d’ordre de producció</span><span class="sxs-lookup"><span data-stu-id="59ab1-120">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="59ab1-121">El Project Operations admet escenaris d'existències/ordre de producció i escenaris sense existències/basats en recursos en el mateix entorn mitjançant configuracions de nivell d'entitat legal.</span><span class="sxs-lookup"><span data-stu-id="59ab1-121">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="59ab1-122">Per exemple, Contoso pot aprofitar les capacitats d'existències/ordre de producció a la seva planta de fabricació de EUA (entitat legal = Contoso Manufacturing United States) i capacitats sense existències/basades en recursos a la seva planta de servei de Contoso Robotics Arms del Regne Unit (entitat legal = Contoso Robotics United Kingdom).</span><span class="sxs-lookup"><span data-stu-id="59ab1-122">For example, Contoso can leverage stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States) and non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

## <a name="a-namelitelite-deployment---deal-to-proforma-invoicing"></a><span data-ttu-id="59ab1-123"><a name="lite"><a/>Implementació bàsica: tracte de facturació proforma</span><span class="sxs-lookup"><span data-stu-id="59ab1-123"><a name="lite"><a/>Lite deployment - deal to proforma invoicing</span></span>
<span data-ttu-id="59ab1-124">La implementació bàsica inclou les capacitats següents:</span><span class="sxs-lookup"><span data-stu-id="59ab1-124">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="59ab1-125">Planificació de projectes mitjançant el Microsoft Project per al web</span><span class="sxs-lookup"><span data-stu-id="59ab1-125">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="59ab1-126">Preus multidimensionals</span><span class="sxs-lookup"><span data-stu-id="59ab1-126">Multi-dimensional pricing</span></span>
- <span data-ttu-id="59ab1-127">Administració de recursos unificada</span><span class="sxs-lookup"><span data-stu-id="59ab1-127">Unified Resource Management</span></span>
- <span data-ttu-id="59ab1-128">Seguiment de temps</span><span class="sxs-lookup"><span data-stu-id="59ab1-128">Time Tracking</span></span>
- <span data-ttu-id="59ab1-129">Despesa bàsica</span><span class="sxs-lookup"><span data-stu-id="59ab1-129">Basic Expense</span></span>
- <span data-ttu-id="59ab1-130">Proposta de factura</span><span class="sxs-lookup"><span data-stu-id="59ab1-130">Invoice Proposal</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="59ab1-131">Passos d'implementació:</span><span class="sxs-lookup"><span data-stu-id="59ab1-131">Deployment steps:</span></span>
<span data-ttu-id="59ab1-132">Determineu el millor model d'implementació del Project Operations mitjançant el [qüestionari d'implementació](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="59ab1-132">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="59ab1-133">Per a aquesta implementació, vegeu [Inscripció a versions preliminars de subscripcions](lite-preview-subscription-sign-up.md) i [Proveïment d'un entorn nou](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="59ab1-133">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


## <a name="a-nameintegratedproject-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="59ab1-134"><a name="integrated"><a/>Project Operations per a escenaris de recursos/no mantinguts en existències</span><span class="sxs-lookup"><span data-stu-id="59ab1-134"><a name="integrated"><a/>Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="59ab1-135">El Project Operations per a escenaris de recursos/sense existències inclou les capacitats següents:</span><span class="sxs-lookup"><span data-stu-id="59ab1-135">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
  
- <span data-ttu-id="59ab1-136">Planificació de projectes mitjançant el Microsoft Project per al web</span><span class="sxs-lookup"><span data-stu-id="59ab1-136">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="59ab1-137">Preus multidimensionals</span><span class="sxs-lookup"><span data-stu-id="59ab1-137">Multi-dimensional pricing</span></span>
- <span data-ttu-id="59ab1-138">Administració de recursos unificada</span><span class="sxs-lookup"><span data-stu-id="59ab1-138">Unified Resource Management</span></span>
- <span data-ttu-id="59ab1-139">Seguiment de temps</span><span class="sxs-lookup"><span data-stu-id="59ab1-139">Time Tracking</span></span>
- <span data-ttu-id="59ab1-140">Despesa bàsica</span><span class="sxs-lookup"><span data-stu-id="59ab1-140">Basic Expense</span></span>
- <span data-ttu-id="59ab1-141">Despesa total</span><span class="sxs-lookup"><span data-stu-id="59ab1-141">Full Expense</span></span>
- <span data-ttu-id="59ab1-142">OCR de rebuts</span><span class="sxs-lookup"><span data-stu-id="59ab1-142">Receipt OCR</span></span>
- <span data-ttu-id="59ab1-143">Facturació completa</span><span class="sxs-lookup"><span data-stu-id="59ab1-143">Full Invoicing</span></span>
- <span data-ttu-id="59ab1-144">Reconeixement d'ingressos</span><span class="sxs-lookup"><span data-stu-id="59ab1-144">Revenue Recognition</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="59ab1-145">Passos d'implementació:</span><span class="sxs-lookup"><span data-stu-id="59ab1-145">Deployment steps:</span></span>
<span data-ttu-id="59ab1-146">Determineu el millor model d'implementació del Project Operations mitjançant el [qüestionari d'implementació](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="59ab1-146">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="59ab1-147">Per a aquesta implementació, vegeu [Inscripció a versions preliminars de subscripcions](resource-sign-up-preview-subscription.md) i [Proveïment d'un entorn nou](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="59ab1-147">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


## <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="59ab1-148">Project Operations per a escenaris mantinguts en existències/d’ordre de producció</span><span class="sxs-lookup"><span data-stu-id="59ab1-148">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="59ab1-149">Planificació del projecte mitjançant WBS</span><span class="sxs-lookup"><span data-stu-id="59ab1-149">Project planning using WBS</span></span>
- <span data-ttu-id="59ab1-150">Administració de recursos</span><span class="sxs-lookup"><span data-stu-id="59ab1-150">Resource Management</span></span>
- <span data-ttu-id="59ab1-151">Seguiment de temps</span><span class="sxs-lookup"><span data-stu-id="59ab1-151">Time Tracking</span></span>
- <span data-ttu-id="59ab1-152">Despesa total</span><span class="sxs-lookup"><span data-stu-id="59ab1-152">Full Expense</span></span>
- <span data-ttu-id="59ab1-153">OCR de rebuts</span><span class="sxs-lookup"><span data-stu-id="59ab1-153">Receipt OCR</span></span>
- <span data-ttu-id="59ab1-154">Facturació completa</span><span class="sxs-lookup"><span data-stu-id="59ab1-154">Full Invoicing</span></span>
- <span data-ttu-id="59ab1-155">Reconeixement d'ingressos</span><span class="sxs-lookup"><span data-stu-id="59ab1-155">Revenue Recognition</span></span>
- <span data-ttu-id="59ab1-156">Comandes de producció</span><span class="sxs-lookup"><span data-stu-id="59ab1-156">Production Orders</span></span>
- <span data-ttu-id="59ab1-157">Suport de materials</span><span class="sxs-lookup"><span data-stu-id="59ab1-157">Materials support</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="59ab1-158">Passos d'implementació:</span><span class="sxs-lookup"><span data-stu-id="59ab1-158">Deployment steps:</span></span>
<span data-ttu-id="59ab1-159">Determineu el millor model d'implementació del Project Operations mitjançant el [qüestionari d'implementació](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="59ab1-159">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="59ab1-160">Per a aquesta implementació, vegeu [Inscripció a versions preliminars de subscripcions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) i [Proveïment d'un entorn nou](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span><span class="sxs-lookup"><span data-stu-id="59ab1-160">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 



