---
title: Pàgina d'inici de dimensions de preus i de costos
description: Aquest tema proporciona una visió general de les dimensions de preus.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 425d7bb8-9015-4f67-b9c9-cf3602e9afe8
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 2379d0d2e038f28a1a8df87a851e9bf7db7fe33f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749476"
---
# <a name="pricing-and-costing-dimensions-home-page"></a><span data-ttu-id="d831d-103">Pàgina d'inici de dimensions de preus i de costos</span><span class="sxs-lookup"><span data-stu-id="d831d-103">Pricing and costing dimensions home page</span></span>

<span data-ttu-id="d831d-104">Les dimensions que s'utilitzen en els recursos humans per configurar els preus i els costos es divideixen en dues categories:</span><span class="sxs-lookup"><span data-stu-id="d831d-104">The dimensions that are used in human resources to set up pricing and costs fall into two categories:</span></span>

- <span data-ttu-id="d831d-105">Persones</span><span class="sxs-lookup"><span data-stu-id="d831d-105">People</span></span>
- <span data-ttu-id="d831d-106">Feina planejada</span><span class="sxs-lookup"><span data-stu-id="d831d-106">Planned work</span></span>

<span data-ttu-id="d831d-107">A causa d'això, hi ha dos tipus de valors de dimensió de preus disponibles al Project Service Automation (PSA):</span><span class="sxs-lookup"><span data-stu-id="d831d-107">Because of this, there are two types of pricing dimension values available in Project Service Automation (PSA):</span></span> 

- <span data-ttu-id="d831d-108">**Conjunts d'opcions**: dimensions que són enumeracions fixes per a un conjunt de valors.</span><span class="sxs-lookup"><span data-stu-id="d831d-108">**Option sets** - Dimensions that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="d831d-109">**Valors basats en l'entitat**: dimensions que poden ser un conjunt variat de valors.</span><span class="sxs-lookup"><span data-stu-id="d831d-109">**Entity-based values** - Dimensions that can be a varied set of values.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="d831d-110">Dimensions de preus</span><span class="sxs-lookup"><span data-stu-id="d831d-110">Pricing dimensions</span></span>

<span data-ttu-id="d831d-111">El PSA inclou de sèrie un conjunt de dimensions de preus per defecte.</span><span class="sxs-lookup"><span data-stu-id="d831d-111">PSA ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="d831d-112">Podeu visualitzar-los anant a **Project Service** > **Paràmetres**.</span><span class="sxs-lookup"><span data-stu-id="d831d-112">You can view these by going to **Project Service** > **Parameters**.</span></span> <span data-ttu-id="d831d-113">Al registre de paràmetre, a la pestanya **Dimensions de preus basades en l'import**, comproveu que la funció **msdyn_resourcecategory** i la unitat organitzativa de recursos **msdyn_organizationalunit** tinguin els camps **Aplicable a les vendes** i **Aplicable al cost** definits com a **Sí**.</span><span class="sxs-lookup"><span data-stu-id="d831d-113">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="d831d-114">Això us permetrà configurar el preu i el cost de cada combinació de funció i unitat organitzativa.</span><span class="sxs-lookup"><span data-stu-id="d831d-114">This will allow you to set up the price and cost for each role and organizational unit combination.</span></span>

![Captura de pantalla dels paràmetres del Project Service amb "Aplicable a les vendes" ressaltat](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> <span data-ttu-id="d831d-116">Si heu estat utilitzant els camps de fàbrica de funció i unitat organitzativa com a dimensions de preus abans de la versió 3 del PSA, no hi haurà cap canvi observable.</span><span class="sxs-lookup"><span data-stu-id="d831d-116">If you have been the using out-of-the box fields of role and organizational unit as pricing dimensions prior to version 3 of PSA, there will not be any observable change.</span></span> <span data-ttu-id="d831d-117">Podeu continuar utilitzant el Project Service com de costum.</span><span class="sxs-lookup"><span data-stu-id="d831d-117">You can continue to use Project Service as usual.</span></span> 

<span data-ttu-id="d831d-118">Si heu de posar un preu o un cost als recursos mitjançant atributs addicionals, podeu crear camps, entitats i dimensions personalitzats.</span><span class="sxs-lookup"><span data-stu-id="d831d-118">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span> <span data-ttu-id="d831d-119">Per obtenir més informació, vegeu els temes següents, però fixeu-vos que heu d'emplenar els procediments en l'ordre que es detalla a continuació:</span><span class="sxs-lookup"><span data-stu-id="d831d-119">For more information, see the following topics, however note that you must complete the procedures in the order listed below:</span></span>

- [<span data-ttu-id="d831d-120">Crear camps i entitats personalitzats</span><span class="sxs-lookup"><span data-stu-id="d831d-120">Create custom fields and entities</span></span>](create-custom-fields-entities.md)
- [<span data-ttu-id="d831d-121">Afegir camps personalitzats a la configuració de preus i a entitats transaccionals</span><span class="sxs-lookup"><span data-stu-id="d831d-121">Add custom fields to price setup and transactional entities</span></span>](field-references.md)
- [<span data-ttu-id="d831d-122">Configurar camps personalitzats com a dimensions de preus</span><span class="sxs-lookup"><span data-stu-id="d831d-122">Set up custom fields as pricing dimensions</span></span>](set-up-pricing-dimensions.md)
- [<span data-ttu-id="d831d-123">Actualitzar els atributs de complement per incloure noves dimensions de preus</span><span class="sxs-lookup"><span data-stu-id="d831d-123">Update plug-in attributes to include new pricing dimensions</span></span>](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a><span data-ttu-id="d831d-124">Posar preu al temps de recursos humans</span><span class="sxs-lookup"><span data-stu-id="d831d-124">Pricing human resource time</span></span>
<span data-ttu-id="d831d-125">Com una organització posa preu al temps de recursos humans és sovint una consideració estratègica important que afecta directament la rendibilitat de l'organització.</span><span class="sxs-lookup"><span data-stu-id="d831d-125">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="d831d-126">Treballeu amb els equips de finances i els caps de pràctiques quan la vostra organització estigui a punt per identificar com vol configurar la tarifa de facturació i el cost per al temps de recursos humans.</span><span class="sxs-lookup"><span data-stu-id="d831d-126">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="d831d-127">Altres consideracions sobre el preu inclouen la reutilització de camps o entitats que no són actualment dimensions de preus però que s'apliquen com una dimensió de preus per a la vostra organització.</span><span class="sxs-lookup"><span data-stu-id="d831d-127">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="d831d-128">Els camps com ara **Categoria de transacció** (**msdyn_transactioncategory**) i **Recursos que es poden reservar** (**bookableresource**) són exemples de dimensions candidates.</span><span class="sxs-lookup"><span data-stu-id="d831d-128">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="d831d-129">També heu de tenir en compte si la dimensió de preus ha de ser una taula o un conjunt d'opcions.</span><span class="sxs-lookup"><span data-stu-id="d831d-129">You should also consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="d831d-130">Si preveieu canvis dels valors d'una dimensió que excedirà els 10 o 12 i necessiteu atributs addicionals sobre aquests valors, podeu crear una entitat en comptes d'un conjunt d'opcions.</span><span class="sxs-lookup"><span data-stu-id="d831d-130">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, you could create an entity rather than an option set.</span></span> <span data-ttu-id="d831d-131">El manteniment d'un conjunt d'opcions, com afegir o eliminar valors, requereix un administrador o un desenvolupador, mentre que la majoria d'usuaris poden afegir una fila nova a una taula.</span><span class="sxs-lookup"><span data-stu-id="d831d-131">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most users.</span></span>

<span data-ttu-id="d831d-132">A l'exemple següent es mostren les tarifes de facturació que estan configurades en funció de la funció i de la unitat organitzativa de recursos a la qual pertany el recurs.</span><span class="sxs-lookup"><span data-stu-id="d831d-132">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="d831d-133">Els percentatges de costos normalment es basen en la banda de salari de l'empleat i en la unitat organitzativa a la qual pertanyen.</span><span class="sxs-lookup"><span data-stu-id="d831d-133">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="d831d-134">En aquest exemple, les taules de tarifes de facturació i de percentatge de cost s'assemblen al següent.</span><span class="sxs-lookup"><span data-stu-id="d831d-134">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="d831d-135">**Tarifes de facturació d'exemple**</span><span class="sxs-lookup"><span data-stu-id="d831d-135">**Sample bill rates**</span></span>

| <span data-ttu-id="d831d-136">Funció</span><span class="sxs-lookup"><span data-stu-id="d831d-136">Role</span></span>        | <span data-ttu-id="d831d-137">Unitat organitzativa</span><span class="sxs-lookup"><span data-stu-id="d831d-137">Org Unit</span></span>    |<span data-ttu-id="d831d-138">Unit</span><span class="sxs-lookup"><span data-stu-id="d831d-138">Unit</span></span>      |<span data-ttu-id="d831d-139">Preu</span><span class="sxs-lookup"><span data-stu-id="d831d-139">Price</span></span>      |<span data-ttu-id="d831d-140">Moneda</span><span class="sxs-lookup"><span data-stu-id="d831d-140">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="d831d-141">Desenvolupador</span><span class="sxs-lookup"><span data-stu-id="d831d-141">Developer</span></span>   | <span data-ttu-id="d831d-142">Contoso EUA</span><span class="sxs-lookup"><span data-stu-id="d831d-142">Contoso US</span></span>  |<span data-ttu-id="d831d-143">Hour</span><span class="sxs-lookup"><span data-stu-id="d831d-143">Hour</span></span> | <span data-ttu-id="d831d-144">200</span><span class="sxs-lookup"><span data-stu-id="d831d-144">200</span></span>|<span data-ttu-id="d831d-145">USD</span><span class="sxs-lookup"><span data-stu-id="d831d-145">USD</span></span>     |
| <span data-ttu-id="d831d-146">Desenvolupador</span><span class="sxs-lookup"><span data-stu-id="d831d-146">Developer</span></span>   | <span data-ttu-id="d831d-147">Contoso India</span><span class="sxs-lookup"><span data-stu-id="d831d-147">Contoso India</span></span> |<span data-ttu-id="d831d-148">Hour</span><span class="sxs-lookup"><span data-stu-id="d831d-148">Hour</span></span>|   <span data-ttu-id="d831d-149">112</span><span class="sxs-lookup"><span data-stu-id="d831d-149">112</span></span>|<span data-ttu-id="d831d-150">USD</span><span class="sxs-lookup"><span data-stu-id="d831d-150">USD</span></span>     |


<span data-ttu-id="d831d-151">**Percentatge de costos d'exemple**</span><span class="sxs-lookup"><span data-stu-id="d831d-151">**Sample cost rates**</span></span>

| <span data-ttu-id="d831d-152">Banda de salari</span><span class="sxs-lookup"><span data-stu-id="d831d-152">Salary Band</span></span>     | <span data-ttu-id="d831d-153">Unitat organitzativa</span><span class="sxs-lookup"><span data-stu-id="d831d-153">Org Unit</span></span>    |<span data-ttu-id="d831d-154">Unit</span><span class="sxs-lookup"><span data-stu-id="d831d-154">Unit</span></span>      |<span data-ttu-id="d831d-155">Preu</span><span class="sxs-lookup"><span data-stu-id="d831d-155">Price</span></span>      |<span data-ttu-id="d831d-156">Moneda</span><span class="sxs-lookup"><span data-stu-id="d831d-156">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="d831d-157">La meva empresa_banda1</span><span class="sxs-lookup"><span data-stu-id="d831d-157">My company_Band1</span></span> | <span data-ttu-id="d831d-158">Contoso EUA</span><span class="sxs-lookup"><span data-stu-id="d831d-158">Contoso US</span></span>  |<span data-ttu-id="d831d-159">Hour</span><span class="sxs-lookup"><span data-stu-id="d831d-159">Hour</span></span> | <span data-ttu-id="d831d-160">145</span><span class="sxs-lookup"><span data-stu-id="d831d-160">145</span></span>|<span data-ttu-id="d831d-161">USD</span><span class="sxs-lookup"><span data-stu-id="d831d-161">USD</span></span>     |
| <span data-ttu-id="d831d-162">La meva empresa_banda2</span><span class="sxs-lookup"><span data-stu-id="d831d-162">My company_Band2</span></span> | <span data-ttu-id="d831d-163">Contoso India</span><span class="sxs-lookup"><span data-stu-id="d831d-163">Contoso India</span></span> |<span data-ttu-id="d831d-164">Hour</span><span class="sxs-lookup"><span data-stu-id="d831d-164">Hour</span></span>|   <span data-ttu-id="d831d-165">67</span><span class="sxs-lookup"><span data-stu-id="d831d-165">67</span></span>|<span data-ttu-id="d831d-166">USD</span><span class="sxs-lookup"><span data-stu-id="d831d-166">USD</span></span>     |
