---
title: Informació general de les dimensions de preus
description: En aquest tema es proporciona informació sobre les dimensions de preus al Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: ec2e350e0e4c28ea1c9540d70c83fdf0a75dc408
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128451"
---
# <a name="pricing-dimensions-overview"></a><span data-ttu-id="2e309-103">Informació general de les dimensions de preus</span><span class="sxs-lookup"><span data-stu-id="2e309-103">Pricing dimensions overview</span></span>

<span data-ttu-id="2e309-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_</span><span class="sxs-lookup"><span data-stu-id="2e309-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="2e309-105">Les dimensions que s'utilitzen en els recursos humans per configurar els preus i els costos es divideixen en dues categories:</span><span class="sxs-lookup"><span data-stu-id="2e309-105">The dimensions that are used in human resources to set up pricing and costs fall into two categories:</span></span>

- <span data-ttu-id="2e309-106">Persones</span><span class="sxs-lookup"><span data-stu-id="2e309-106">People</span></span>
- <span data-ttu-id="2e309-107">Feina planejada</span><span class="sxs-lookup"><span data-stu-id="2e309-107">Planned work</span></span>

<span data-ttu-id="2e309-108">A causa d'això, hi ha dos tipus de valors de dimensió de preus disponibles:</span><span class="sxs-lookup"><span data-stu-id="2e309-108">Because of this, there are two types of pricing dimension values available:</span></span>

- <span data-ttu-id="2e309-109">**Conjunts d'opcions**: dimensions que són enumeracions fixes per a un conjunt de valors.</span><span class="sxs-lookup"><span data-stu-id="2e309-109">**Option sets**: Dimensions that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="2e309-110">**Valors basats en l'entitat**: dimensions que poden ser un conjunt variat de valors.</span><span class="sxs-lookup"><span data-stu-id="2e309-110">**Entity-based values**: Dimensions that can be a varied set of values.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="2e309-111">Dimensions de preus</span><span class="sxs-lookup"><span data-stu-id="2e309-111">Pricing dimensions</span></span>

<span data-ttu-id="2e309-112">El Dynamics 365 Project Operations inclou un conjunt per defecte de dimensions de preus.</span><span class="sxs-lookup"><span data-stu-id="2e309-112">Dynamics 365 Project Operations ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="2e309-113">Podeu visualitzar aquestes dimensions de preus anant a **Project Operations** > **Paràmetres**.</span><span class="sxs-lookup"><span data-stu-id="2e309-113">You can view these pricing dimensions by going to **Project Operations** > **Parameters**.</span></span> <span data-ttu-id="2e309-114">Al registre de paràmetre, a la pestanya **Dimensions de preus basades en l'import**, comproveu que la funció **msdyn_resourcecategory** i la unitat organitzativa de recursos **msdyn_organizationalunit** tinguin els camps **Aplicable a les vendes** i **Aplicable al cost** definits com a **Sí**.</span><span class="sxs-lookup"><span data-stu-id="2e309-114">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="2e309-115">Amb aquests camps habilitats, podeu configurar el preu i el cost de cada combinació de funció i unitat organitzativa.</span><span class="sxs-lookup"><span data-stu-id="2e309-115">With these fields enabled, you can set up the price and cost for each role and organizational unit combination.</span></span>

<span data-ttu-id="2e309-116">Si heu de posar un preu o un cost als recursos mitjançant atributs addicionals, podeu crear camps, entitats i dimensions personalitzats.</span><span class="sxs-lookup"><span data-stu-id="2e309-116">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span>

## <a name="pricing-human-resource-time"></a><span data-ttu-id="2e309-117">Posar preu al temps de recursos humans</span><span class="sxs-lookup"><span data-stu-id="2e309-117">Pricing human resource time</span></span>
<span data-ttu-id="2e309-118">Com una organització posa preu al temps de recursos humans és sovint una consideració estratègica important que afecta directament la rendibilitat de l'organització.</span><span class="sxs-lookup"><span data-stu-id="2e309-118">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="2e309-119">Treballeu amb els equips de finances i els caps de pràctiques quan la vostra organització estigui a punt per identificar com vol configurar la tarifa de facturació i el cost per al temps de recursos humans.</span><span class="sxs-lookup"><span data-stu-id="2e309-119">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="2e309-120">Altres consideracions sobre el preu inclouen la reutilització de camps o entitats que no són actualment dimensions de preus però que s'apliquen com una dimensió de preus per a la vostra organització.</span><span class="sxs-lookup"><span data-stu-id="2e309-120">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="2e309-121">Els camps com ara **Categoria de transacció** (**msdyn_transactioncategory**) i **Recursos que es poden reservar** (**bookableresource**) són exemples de dimensions candidates.</span><span class="sxs-lookup"><span data-stu-id="2e309-121">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="2e309-122">Tingueu en compte si la dimensió de preus ha de ser una taula o un conjunt d'opcions.</span><span class="sxs-lookup"><span data-stu-id="2e309-122">Consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="2e309-123">Si preveieu canvis dels valors d'una dimensió que excedirà els 10 o 12 i necessiteu atributs addicionals sobre aquests valors, podeu crear una entitat en comptes d'un conjunt d'opcions.</span><span class="sxs-lookup"><span data-stu-id="2e309-123">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, you could create an entity rather than an option set.</span></span> <span data-ttu-id="2e309-124">El manteniment d'un conjunt d'opcions, com afegir o eliminar valors, requereix un administrador o un desenvolupador, mentre que la majoria d'usuaris poden afegir una fila nova a una taula.</span><span class="sxs-lookup"><span data-stu-id="2e309-124">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most users.</span></span>

<span data-ttu-id="2e309-125">A l'exemple següent es mostren les tarifes de facturació que estan configurades en funció de la funció i de la unitat organitzativa de recursos a la qual pertany el recurs.</span><span class="sxs-lookup"><span data-stu-id="2e309-125">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="2e309-126">Els percentatges de costos normalment es basen en la banda de salari de l'empleat i en la unitat organitzativa a la qual pertanyen.</span><span class="sxs-lookup"><span data-stu-id="2e309-126">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="2e309-127">En aquest exemple, les taules de tarifes de facturació i de percentatge de cost s'assemblen al següent.</span><span class="sxs-lookup"><span data-stu-id="2e309-127">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="2e309-128">**Tarifes de facturació d'exemple**</span><span class="sxs-lookup"><span data-stu-id="2e309-128">**Sample bill rates**</span></span>

| <span data-ttu-id="2e309-129">Funció</span><span class="sxs-lookup"><span data-stu-id="2e309-129">Role</span></span>        | <span data-ttu-id="2e309-130">Unitat organitzativa</span><span class="sxs-lookup"><span data-stu-id="2e309-130">Org Unit</span></span>    |<span data-ttu-id="2e309-131">Unit</span><span class="sxs-lookup"><span data-stu-id="2e309-131">Unit</span></span>      |<span data-ttu-id="2e309-132">Preu</span><span class="sxs-lookup"><span data-stu-id="2e309-132">Price</span></span>      |<span data-ttu-id="2e309-133">Moneda</span><span class="sxs-lookup"><span data-stu-id="2e309-133">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="2e309-134">Desenvolupador</span><span class="sxs-lookup"><span data-stu-id="2e309-134">Developer</span></span>   | <span data-ttu-id="2e309-135">Contoso EUA</span><span class="sxs-lookup"><span data-stu-id="2e309-135">Contoso US</span></span>  |<span data-ttu-id="2e309-136">Hour</span><span class="sxs-lookup"><span data-stu-id="2e309-136">Hour</span></span> | <span data-ttu-id="2e309-137">200</span><span class="sxs-lookup"><span data-stu-id="2e309-137">200</span></span>|<span data-ttu-id="2e309-138">USD</span><span class="sxs-lookup"><span data-stu-id="2e309-138">USD</span></span>     |
| <span data-ttu-id="2e309-139">Desenvolupador</span><span class="sxs-lookup"><span data-stu-id="2e309-139">Developer</span></span>   | <span data-ttu-id="2e309-140">Contoso India</span><span class="sxs-lookup"><span data-stu-id="2e309-140">Contoso India</span></span> |<span data-ttu-id="2e309-141">Hour</span><span class="sxs-lookup"><span data-stu-id="2e309-141">Hour</span></span>|   <span data-ttu-id="2e309-142">112</span><span class="sxs-lookup"><span data-stu-id="2e309-142">112</span></span>|<span data-ttu-id="2e309-143">USD</span><span class="sxs-lookup"><span data-stu-id="2e309-143">USD</span></span>     |


<span data-ttu-id="2e309-144">**Percentatge de costos d'exemple**</span><span class="sxs-lookup"><span data-stu-id="2e309-144">**Sample cost rates**</span></span>

| <span data-ttu-id="2e309-145">Banda de salari</span><span class="sxs-lookup"><span data-stu-id="2e309-145">Salary Band</span></span>     | <span data-ttu-id="2e309-146">Unitat organitzativa</span><span class="sxs-lookup"><span data-stu-id="2e309-146">Org Unit</span></span>    |<span data-ttu-id="2e309-147">Unit</span><span class="sxs-lookup"><span data-stu-id="2e309-147">Unit</span></span>      |<span data-ttu-id="2e309-148">Preu</span><span class="sxs-lookup"><span data-stu-id="2e309-148">Price</span></span>      |<span data-ttu-id="2e309-149">Moneda</span><span class="sxs-lookup"><span data-stu-id="2e309-149">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="2e309-150">La meva empresa_banda1</span><span class="sxs-lookup"><span data-stu-id="2e309-150">My company_Band1</span></span> | <span data-ttu-id="2e309-151">Contoso EUA</span><span class="sxs-lookup"><span data-stu-id="2e309-151">Contoso US</span></span>  |<span data-ttu-id="2e309-152">Hour</span><span class="sxs-lookup"><span data-stu-id="2e309-152">Hour</span></span> | <span data-ttu-id="2e309-153">145</span><span class="sxs-lookup"><span data-stu-id="2e309-153">145</span></span>|<span data-ttu-id="2e309-154">USD</span><span class="sxs-lookup"><span data-stu-id="2e309-154">USD</span></span>     |
| <span data-ttu-id="2e309-155">La meva empresa_banda2</span><span class="sxs-lookup"><span data-stu-id="2e309-155">My company_Band2</span></span> | <span data-ttu-id="2e309-156">Contoso India</span><span class="sxs-lookup"><span data-stu-id="2e309-156">Contoso India</span></span> |<span data-ttu-id="2e309-157">Hour</span><span class="sxs-lookup"><span data-stu-id="2e309-157">Hour</span></span>|   <span data-ttu-id="2e309-158">67</span><span class="sxs-lookup"><span data-stu-id="2e309-158">67</span></span>|<span data-ttu-id="2e309-159">USD</span><span class="sxs-lookup"><span data-stu-id="2e309-159">USD</span></span>     |
