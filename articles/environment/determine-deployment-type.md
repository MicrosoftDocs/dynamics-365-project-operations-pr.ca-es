---
title: Determinació del tipus d'implementació
description: En aquest tema es proporciona informació per ajudar-vos a determinar el tipus d'implementació correcte del Project Operations per a la vostra empresa.
author: stsporen
ms.date: 03/15/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: ad700a84edd6c39609bc5b4f09ca74af3059a0dd
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997094"
---
# <a name="determine-your-deployment-type"></a><span data-ttu-id="8cf47-103">Determinació del tipus d'implementació</span><span class="sxs-lookup"><span data-stu-id="8cf47-103">Determine your deployment type</span></span>

<span data-ttu-id="8cf47-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_</span><span class="sxs-lookup"><span data-stu-id="8cf47-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8cf47-105">Després d'adquirir la llicència, comenceu aquí per determinar el millor model d'implementació del Dynamics 365 Project Operations utilitzant el [Flux d'instal·lació guiada](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="8cf47-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="8cf47-106">Després d'haver acabat el flux d'instal·lació guiada, se us dirigirà al portal d'administració correcte per completar la instal·lació.</span><span class="sxs-lookup"><span data-stu-id="8cf47-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="8cf47-107">Vegeu els detalls d'implementació per completar la instal·lació.</span><span class="sxs-lookup"><span data-stu-id="8cf47-107">See the deployment details to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="8cf47-108">Clients existents del Dynamics que utilitzen el Dynamics 365 Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="8cf47-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="8cf47-109">El Project Operations inclou les capacitats incloses al Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="8cf47-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="8cf47-110">Es llançarà un camí d'actualització per a aquests clients a la fase 1 de llançament de 2021.</span><span class="sxs-lookup"><span data-stu-id="8cf47-110">An upgrade path will be released for these customers in the 2021 release wave 1.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="8cf47-111">Clients existents del Dynamics 365 Finance que utilitzen l'administració de projectes i la comptabilitat</span><span class="sxs-lookup"><span data-stu-id="8cf47-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="8cf47-112">Els clients existents del Finance que utilitzen la funcionalitat d'administració de projectes i comptabilitat poden continuar utilitzant-la sense canvis.</span><span class="sxs-lookup"><span data-stu-id="8cf47-112">Existing customers of Finance who use the Project management and accounting functionality can continue to use it as is.</span></span> <span data-ttu-id="8cf47-113">Vegeu [Project Operations per a escenaris mantinguts en existències/d’ordre de producció](#pma).</span><span class="sxs-lookup"><span data-stu-id="8cf47-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>


## <a name="deployment-regions"></a><span data-ttu-id="8cf47-114">Regions d'implementació</span><span class="sxs-lookup"><span data-stu-id="8cf47-114">Deployment regions</span></span>
<span data-ttu-id="8cf47-115">Per determinar quines regions admeten la implementació del Project Operations, vegeu [Disponibilitat geogràfica per a l'informe del Dynamics 365 i de Power Platform](https://dynamics.microsoft.com/en-us/geographic-availability/).</span><span class="sxs-lookup"><span data-stu-id="8cf47-115">To determine which regions support Project Operations deployment, see [Geographical availability for Dynamics 365 and Power Platform report](https://dynamics.microsoft.com/en-us/geographic-availability/).</span></span> <span data-ttu-id="8cf47-116">Seleccioneu **Visualitza l'informe** i expandiu **Dynamics 365 > Aplicacions d'operacions > Dynamics 365 Project Operations** per veure les regions admeses.</span><span class="sxs-lookup"><span data-stu-id="8cf47-116">Select **View Report**, and expand **Dynamics 365 > Operations Apps > Dynamics 365 Project Operations** to view the supported regions.</span></span>

## <a name="deployment-types"></a><span data-ttu-id="8cf47-117">Tipus d'implementació</span><span class="sxs-lookup"><span data-stu-id="8cf47-117">Deployment types</span></span>
<span data-ttu-id="8cf47-118">El Project Operations admet diverses opcions de implementació per adaptar-se a les vostres necessitats.</span><span class="sxs-lookup"><span data-stu-id="8cf47-118">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="8cf47-119">Tant si sou un client nou o existent del Dynamics 365, el Project Operations pot ajudar-vos a satisfer les vostres necessitats.</span><span class="sxs-lookup"><span data-stu-id="8cf47-119">Whether you're a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="8cf47-120">El nostre [qüestionari d'implementació](https://aka.ms/provisionprojectoperations) us ajudarà a determinar la implementació adequada.</span><span class="sxs-lookup"><span data-stu-id="8cf47-120">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="8cf47-121">Els resultats us orienten cap a un dels tipus d'implementació següents:</span><span class="sxs-lookup"><span data-stu-id="8cf47-121">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="8cf47-122">Implementació bàsica: tracte de facturació proforma</span><span class="sxs-lookup"><span data-stu-id="8cf47-122">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="8cf47-123">Project Operations per a escenaris de recursos/no mantinguts en existències</span><span class="sxs-lookup"><span data-stu-id="8cf47-123">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="8cf47-124">Project Operations per a escenaris mantinguts en existències/d’ordre de producció</span><span class="sxs-lookup"><span data-stu-id="8cf47-124">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="8cf47-125">El Project Operations admet escenaris d'existències/ordre de producció i escenaris sense existències/basats en recursos en el mateix entorn mitjançant configuracions de nivell d'entitat legal.</span><span class="sxs-lookup"><span data-stu-id="8cf47-125">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="8cf47-126">Per exemple, Contoso pot utilitzar les capacitats d'ordre de producció o emmagatzematge a la seva instal·lació de fabricació dels EUA (Entitat legal = Fabricació de Contoso als Estats Units).</span><span class="sxs-lookup"><span data-stu-id="8cf47-126">For example, Contoso can use the stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States).</span></span> <span data-ttu-id="8cf47-127">Contoso pot utilitzar les capacitats sense existències/basades en recursos en la seva instal·lació de serveis de Contoso Robotics Arms al Regne Unit (Entitat legal = Contoso Robotics Regne Unit).</span><span class="sxs-lookup"><span data-stu-id="8cf47-127">Contoso can use the non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a><span data-ttu-id="8cf47-128">Implementació bàsica: tracte de facturació proforma</span><span class="sxs-lookup"><span data-stu-id="8cf47-128">Lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="8cf47-129">La implementació bàsica inclou les capacitats següents:</span><span class="sxs-lookup"><span data-stu-id="8cf47-129">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="8cf47-130">Procés de venda per a projectes que amplien l'experiència d'aplicació del Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="8cf47-130">Sales process for projects that extends Dynamics 365 Sales application experiences</span></span>
- <span data-ttu-id="8cf47-131">Planificació de projectes mitjançant el Microsoft Project per al web</span><span class="sxs-lookup"><span data-stu-id="8cf47-131">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="8cf47-132">Preus multidimensionals</span><span class="sxs-lookup"><span data-stu-id="8cf47-132">Multi-dimensional pricing</span></span>
- <span data-ttu-id="8cf47-133">Administració de recursos unificada</span><span class="sxs-lookup"><span data-stu-id="8cf47-133">Unified resource management</span></span>
- <span data-ttu-id="8cf47-134">Seguiment de temps</span><span class="sxs-lookup"><span data-stu-id="8cf47-134">Time tracking</span></span>
- <span data-ttu-id="8cf47-135">Despesa bàsica</span><span class="sxs-lookup"><span data-stu-id="8cf47-135">Basic expense</span></span>
- <span data-ttu-id="8cf47-136">Facturació proforma per a la revisió i edició de l'Administrador de projectes</span><span class="sxs-lookup"><span data-stu-id="8cf47-136">Proforma invoicing for Project manager's review and edits</span></span> 

#### <a name="deployment-steps"></a><span data-ttu-id="8cf47-137">Passos d'implementació</span><span class="sxs-lookup"><span data-stu-id="8cf47-137">Deployment steps</span></span>
<span data-ttu-id="8cf47-138">Determineu el millor model d'implementació del Project Operations mitjançant el [qüestionari d'implementació](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="8cf47-138">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="8cf47-139">Per a aquesta implementació, vegeu [Inscripció a versions preliminars de subscripcions](lite-preview-subscription-sign-up.md) i [Proveïment d'un entorn nou](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="8cf47-139">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a><span data-ttu-id="8cf47-140">Project Operations per a escenaris de recursos/no mantinguts en existències</span><span class="sxs-lookup"><span data-stu-id="8cf47-140">Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="8cf47-141">El Project Operations per a escenaris de recursos/sense existències inclou les capacitats següents:</span><span class="sxs-lookup"><span data-stu-id="8cf47-141">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
 
- <span data-ttu-id="8cf47-142">Procés de venda per a projectes que amplien l'aplicació Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="8cf47-142">Sales process for projects that extends the Dynamics 365 Sales application</span></span>
- <span data-ttu-id="8cf47-143">Planificació de projectes mitjançant el Microsoft Project per al web</span><span class="sxs-lookup"><span data-stu-id="8cf47-143">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="8cf47-144">Preus multidimensionals</span><span class="sxs-lookup"><span data-stu-id="8cf47-144">Multi-dimensional pricing</span></span>
- <span data-ttu-id="8cf47-145">Administració de recursos unificada</span><span class="sxs-lookup"><span data-stu-id="8cf47-145">Unified resource management</span></span>
- <span data-ttu-id="8cf47-146">Seguiment de temps</span><span class="sxs-lookup"><span data-stu-id="8cf47-146">Time tracking</span></span>
- <span data-ttu-id="8cf47-147">Despesa bàsica</span><span class="sxs-lookup"><span data-stu-id="8cf47-147">Basic expense</span></span>
- <span data-ttu-id="8cf47-148">Despesa total</span><span class="sxs-lookup"><span data-stu-id="8cf47-148">Full expense</span></span>
- <span data-ttu-id="8cf47-149">OCR de rebuts</span><span class="sxs-lookup"><span data-stu-id="8cf47-149">Receipt OCR</span></span>
- <span data-ttu-id="8cf47-150">Facturació proforma i orientada al client</span><span class="sxs-lookup"><span data-stu-id="8cf47-150">Proforma and customer-facing invoicing</span></span> 
- <span data-ttu-id="8cf47-151">Reconeixement d'ingressos per a projectes</span><span class="sxs-lookup"><span data-stu-id="8cf47-151">Revenue recognition for projects</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="8cf47-152">Passos d'implementació</span><span class="sxs-lookup"><span data-stu-id="8cf47-152">Deployment steps</span></span>
<span data-ttu-id="8cf47-153">Determineu el millor model d'implementació del Project Operations mitjançant el [qüestionari d'implementació](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="8cf47-153">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="8cf47-154">Per a aquesta implementació, vegeu [Inscripció a versions preliminars de subscripcions](resource-sign-up-preview-subscription.md) i [Proveïment d'un entorn nou](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="8cf47-154">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="8cf47-155">Project Operations per a escenaris mantinguts en existències/d’ordre de producció</span><span class="sxs-lookup"><span data-stu-id="8cf47-155">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="8cf47-156">Planificació del projecte mitjançant WBS</span><span class="sxs-lookup"><span data-stu-id="8cf47-156">Project planning using WBS</span></span>
- <span data-ttu-id="8cf47-157">Administració de recursos</span><span class="sxs-lookup"><span data-stu-id="8cf47-157">Resource management</span></span>
- <span data-ttu-id="8cf47-158">Seguiment de temps</span><span class="sxs-lookup"><span data-stu-id="8cf47-158">Time tracking</span></span>
- <span data-ttu-id="8cf47-159">Despesa total</span><span class="sxs-lookup"><span data-stu-id="8cf47-159">Full expense</span></span>
- <span data-ttu-id="8cf47-160">OCR de rebuts</span><span class="sxs-lookup"><span data-stu-id="8cf47-160">Receipt OCR</span></span>
- <span data-ttu-id="8cf47-161">Facturació completa</span><span class="sxs-lookup"><span data-stu-id="8cf47-161">Full invoicing</span></span>
- <span data-ttu-id="8cf47-162">Reconeixement d'ingressos</span><span class="sxs-lookup"><span data-stu-id="8cf47-162">Revenue recognition</span></span>
- <span data-ttu-id="8cf47-163">Comandes de producció</span><span class="sxs-lookup"><span data-stu-id="8cf47-163">Production orders</span></span>
- <span data-ttu-id="8cf47-164">Suport de materials amb existències amb inventari</span><span class="sxs-lookup"><span data-stu-id="8cf47-164">Stocked materials support with inventory</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="8cf47-165">Passos d'implementació</span><span class="sxs-lookup"><span data-stu-id="8cf47-165">Deployment steps</span></span>
<span data-ttu-id="8cf47-166">Determineu el millor model d'implementació del Project Operations mitjançant el [qüestionari d'implementació](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="8cf47-166">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="8cf47-167">Per a aquesta implementació, vegeu [Inscripció a versions preliminars de subscripcions](/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=%2fdynamics365%2ffinance%2ftoc.json) i [Proveïment d'un entorn nou](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=%2fdynamics365%2ffinance%2ftoc.json).</span><span class="sxs-lookup"><span data-stu-id="8cf47-167">For this deployment, see [Sign-up for preview subscriptions](/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=%2fdynamics365%2ffinance%2ftoc.json) and [Provision new environment](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=%2fdynamics365%2ffinance%2ftoc.json).</span></span> 



[!INCLUDE[footer-include](../includes/footer-banner.md)]