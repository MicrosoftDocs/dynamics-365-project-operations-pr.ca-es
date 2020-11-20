---
title: Determinació del tipus d'implementació
description: En aquest tema es proporciona informació per ajudar-vos a determinar el tipus d'implementació correcte del Project Operations per a la vostra empresa.
author: stsporen
manager: Annbe
ms.date: 11/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: e9d3a5d8e6e1daafac72a3b4c0380b679d1869bd
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401206"
---
# <a name="determine-your-deployment-type"></a><span data-ttu-id="5f992-103">Determinació del tipus d'implementació</span><span class="sxs-lookup"><span data-stu-id="5f992-103">Determine your deployment type</span></span>

<span data-ttu-id="5f992-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_</span><span class="sxs-lookup"><span data-stu-id="5f992-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5f992-105">Després d'adquirir la llicència, comenceu aquí per determinar el millor model d'implementació del Dynamics 365 Project Operations mitjançant el [Flux d'instal·lació guiada](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="5f992-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="5f992-106">Després d'haver acabat el flux d'instal·lació guiada, se us dirigirà al portal d'administració correcte per completar la instal·lació.</span><span class="sxs-lookup"><span data-stu-id="5f992-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="5f992-107">Vegeu els detalls d'implementació per completar la instal·lació.</span><span class="sxs-lookup"><span data-stu-id="5f992-107">See the deployment details to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="5f992-108">Clients existents del Dynamics que utilitzen el Dynamics 365 Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="5f992-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="5f992-109">El Project Operations inclou les capacitats incloses al Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="5f992-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="5f992-110">Es llançarà un camí d'actualització per a aquests clients a la fase 1 de llançament de 2021.</span><span class="sxs-lookup"><span data-stu-id="5f992-110">An upgrade path will be released for these customers in the 2021 release wave 1.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="5f992-111">Clients existents del Dynamics 365 Finance que utilitzen l'administració de projectes i la comptabilitat</span><span class="sxs-lookup"><span data-stu-id="5f992-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="5f992-112">Els clients existents del Finance que utilitzen la funcionalitat d'administració de projectes i comptabilitat poden continuar utilitzant-la sense canvis.</span><span class="sxs-lookup"><span data-stu-id="5f992-112">Existing customers of Finance who use the Project management and accounting functionality can continue to use it as is.</span></span> <span data-ttu-id="5f992-113">Vegeu [Project Operations per a escenaris mantinguts en existències/d’ordre de producció](#pma).</span><span class="sxs-lookup"><span data-stu-id="5f992-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>


## <a name="deployment-types"></a><span data-ttu-id="5f992-114">Tipus d'implementació</span><span class="sxs-lookup"><span data-stu-id="5f992-114">Deployment types</span></span>
<span data-ttu-id="5f992-115">El Project Operations admet diverses opcions de implementació per adaptar-se a les vostres necessitats.</span><span class="sxs-lookup"><span data-stu-id="5f992-115">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="5f992-116">Tant si sou un client nou o existent del Dynamics 365, el Project Operations pot ajudar-vos a satisfer les vostres necessitats.</span><span class="sxs-lookup"><span data-stu-id="5f992-116">Whether you're a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="5f992-117">El nostre [qüestionari d'implementació](https://aka.ms/provisionprojectoperations) us ajudarà a determinar la implementació adequada.</span><span class="sxs-lookup"><span data-stu-id="5f992-117">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="5f992-118">Els resultats us orienten cap a un dels tipus d'implementació següents:</span><span class="sxs-lookup"><span data-stu-id="5f992-118">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="5f992-119">Implementació bàsica: tracte de facturació proforma</span><span class="sxs-lookup"><span data-stu-id="5f992-119">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="5f992-120">Project Operations per a escenaris de recursos/no mantinguts en existències</span><span class="sxs-lookup"><span data-stu-id="5f992-120">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="5f992-121">Project Operations per a escenaris mantinguts en existències/d’ordre de producció</span><span class="sxs-lookup"><span data-stu-id="5f992-121">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="5f992-122">El Project Operations admet escenaris d'existències/ordre de producció i escenaris sense existències/basats en recursos en el mateix entorn mitjançant configuracions de nivell d'entitat legal.</span><span class="sxs-lookup"><span data-stu-id="5f992-122">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="5f992-123">Per exemple, Contoso pot utilitzar les funcionalitats de comanda amb existències/producció en la seva planta de fabricació dels EUA (Entitat jurídica = Contoso Manufacturing United States).</span><span class="sxs-lookup"><span data-stu-id="5f992-123">For example, Contoso can use the stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States).</span></span> <span data-ttu-id="5f992-124">Contoso pot utilitzar les funcionalitats sense existències/basades en recursos en la seva instal·lació de servei de braços robòtics de Contoso al Regne Unit (Entitat jurídica = Contoso Robotics United Kingdom).</span><span class="sxs-lookup"><span data-stu-id="5f992-124">Contoso can use the non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a><span data-ttu-id="5f992-125">Implementació bàsica: tracte de facturació proforma</span><span class="sxs-lookup"><span data-stu-id="5f992-125">Lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="5f992-126">La implementació bàsica inclou les capacitats següents:</span><span class="sxs-lookup"><span data-stu-id="5f992-126">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="5f992-127">Procés de venda per a projectes que amplien l'experiència d'aplicació del Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="5f992-127">Sales process for projects that extends Dynamics 365 Sales application experiences</span></span>
- <span data-ttu-id="5f992-128">Planificació de projectes mitjançant el Microsoft Project per al web</span><span class="sxs-lookup"><span data-stu-id="5f992-128">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="5f992-129">Preus multidimensionals</span><span class="sxs-lookup"><span data-stu-id="5f992-129">Multi-dimensional pricing</span></span>
- <span data-ttu-id="5f992-130">Administració de recursos unificada</span><span class="sxs-lookup"><span data-stu-id="5f992-130">Unified resource management</span></span>
- <span data-ttu-id="5f992-131">Seguiment de temps</span><span class="sxs-lookup"><span data-stu-id="5f992-131">Time tracking</span></span>
- <span data-ttu-id="5f992-132">Despesa bàsica</span><span class="sxs-lookup"><span data-stu-id="5f992-132">Basic expense</span></span>
- <span data-ttu-id="5f992-133">Facturació proforma i orientada al client</span><span class="sxs-lookup"><span data-stu-id="5f992-133">Proforma and customer-facing invoicing</span></span> 

#### <a name="deployment-steps"></a><span data-ttu-id="5f992-134">Passos d'implementació</span><span class="sxs-lookup"><span data-stu-id="5f992-134">Deployment steps</span></span>
<span data-ttu-id="5f992-135">Determineu el millor model d'implementació del Project Operations mitjançant el [qüestionari d'implementació](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="5f992-135">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="5f992-136">Per a aquesta implementació, vegeu [Inscripció a versions preliminars de subscripcions](lite-preview-subscription-sign-up.md) i [Proveïment d'un entorn nou](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="5f992-136">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a><span data-ttu-id="5f992-137">Project Operations per a escenaris de recursos/no mantinguts en existències</span><span class="sxs-lookup"><span data-stu-id="5f992-137">Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="5f992-138">El Project Operations per a escenaris de recursos/sense existències inclou les capacitats següents:</span><span class="sxs-lookup"><span data-stu-id="5f992-138">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
 
- <span data-ttu-id="5f992-139">Procés de venda per a projectes que amplien l'aplicació Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="5f992-139">Sales process for projects that extends the Dynamics 365 Sales application</span></span>
- <span data-ttu-id="5f992-140">Planificació de projectes mitjançant el Microsoft Project per al web</span><span class="sxs-lookup"><span data-stu-id="5f992-140">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="5f992-141">Preus multidimensionals</span><span class="sxs-lookup"><span data-stu-id="5f992-141">Multi-dimensional pricing</span></span>
- <span data-ttu-id="5f992-142">Administració de recursos unificada</span><span class="sxs-lookup"><span data-stu-id="5f992-142">Unified resource management</span></span>
- <span data-ttu-id="5f992-143">Seguiment de temps</span><span class="sxs-lookup"><span data-stu-id="5f992-143">Time tracking</span></span>
- <span data-ttu-id="5f992-144">Despesa bàsica</span><span class="sxs-lookup"><span data-stu-id="5f992-144">Basic expense</span></span>
- <span data-ttu-id="5f992-145">Despesa total</span><span class="sxs-lookup"><span data-stu-id="5f992-145">Full expense</span></span>
- <span data-ttu-id="5f992-146">OCR de rebuts</span><span class="sxs-lookup"><span data-stu-id="5f992-146">Receipt OCR</span></span>
- <span data-ttu-id="5f992-147">Facturació proforma i orientada al client</span><span class="sxs-lookup"><span data-stu-id="5f992-147">Proforma and customer-facing invoicing</span></span> 
- <span data-ttu-id="5f992-148">Reconeixement d'ingressos per a projectes</span><span class="sxs-lookup"><span data-stu-id="5f992-148">Revenue recognition for projects</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="5f992-149">Passos d'implementació</span><span class="sxs-lookup"><span data-stu-id="5f992-149">Deployment steps</span></span>
<span data-ttu-id="5f992-150">Determineu el millor model d'implementació del Project Operations mitjançant el [qüestionari d'implementació](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="5f992-150">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="5f992-151">Per a aquesta implementació, vegeu [Inscripció a versions preliminars de subscripcions](resource-sign-up-preview-subscription.md) i [Proveïment d'un entorn nou](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="5f992-151">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="5f992-152">Project Operations per a escenaris mantinguts en existències/d’ordre de producció</span><span class="sxs-lookup"><span data-stu-id="5f992-152">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="5f992-153">Planificació del projecte mitjançant WBS</span><span class="sxs-lookup"><span data-stu-id="5f992-153">Project planning using WBS</span></span>
- <span data-ttu-id="5f992-154">Administració de recursos</span><span class="sxs-lookup"><span data-stu-id="5f992-154">Resource Management</span></span>
- <span data-ttu-id="5f992-155">Seguiment de temps</span><span class="sxs-lookup"><span data-stu-id="5f992-155">Time Tracking</span></span>
- <span data-ttu-id="5f992-156">Despesa total</span><span class="sxs-lookup"><span data-stu-id="5f992-156">Full Expense</span></span>
- <span data-ttu-id="5f992-157">OCR de rebuts</span><span class="sxs-lookup"><span data-stu-id="5f992-157">Receipt OCR</span></span>
- <span data-ttu-id="5f992-158">Facturació completa</span><span class="sxs-lookup"><span data-stu-id="5f992-158">Full Invoicing</span></span>
- <span data-ttu-id="5f992-159">Reconeixement d'ingressos</span><span class="sxs-lookup"><span data-stu-id="5f992-159">Revenue Recognition</span></span>
- <span data-ttu-id="5f992-160">Comandes de producció</span><span class="sxs-lookup"><span data-stu-id="5f992-160">Production Orders</span></span>
- <span data-ttu-id="5f992-161">Suport de materials</span><span class="sxs-lookup"><span data-stu-id="5f992-161">Materials support</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="5f992-162">Passos d'implementació</span><span class="sxs-lookup"><span data-stu-id="5f992-162">Deployment steps</span></span>
<span data-ttu-id="5f992-163">Determineu el millor model d'implementació del Project Operations mitjançant el [qüestionari d'implementació](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="5f992-163">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="5f992-164">Per a aquesta implementació, vegeu [Inscripció a versions preliminars de subscripcions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) i [Proveïment d'un entorn nou](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span><span class="sxs-lookup"><span data-stu-id="5f992-164">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 

