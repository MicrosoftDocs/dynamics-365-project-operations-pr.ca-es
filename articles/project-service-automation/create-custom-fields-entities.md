---
title: Crear camps i entitats personalitzats
description: En aquest tema s'explica com crear conjunts d'opcions i entitats a la vostra pròpia solució a la plataforma Power Apps.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/26/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: fb160bfd-e037-4a21-a968-3ff2e6e16481
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 7ee30e3bb6b8034ef226e2e9181195685355011f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749560"
---
# <a name="create-custom-fields-and-entities"></a><span data-ttu-id="e7087-103">Crear camps i entitats personalitzats</span><span class="sxs-lookup"><span data-stu-id="e7087-103">Create custom fields and entities</span></span> 

<span data-ttu-id="e7087-104">Completeu els passos següents en qualsevol moment que vulgueu crear un conjunt d'opcions o una entitat personalitzada a la plataforma del Power Apps.</span><span class="sxs-lookup"><span data-stu-id="e7087-104">Complete the following steps any time that you want to create a custom option set or entity on the Power Apps platform.</span></span>  
<span data-ttu-id="e7087-105">Els procediments d'aquest tema s'han d'emplenar mitjançant la interfície web del Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="e7087-105">The procedures in this topic should be completed using the web interface of Project Service Automation (PSA).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e7087-106">Us recomanem que realitzeu tots els canvis de dimensió de preus personalitzats en una solució separada.</span><span class="sxs-lookup"><span data-stu-id="e7087-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="e7087-107">Aquestes pràctiques recomanades importants proporcionen una flexibilitat futura per actualitzar o suprimir els canvis segons calgui, us ajudaran a reutilitzar el vostre treball i facilita la portabilitat d'aquests canvis en una altra instància.</span><span class="sxs-lookup"><span data-stu-id="e7087-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="e7087-108">Després d'haver fet tots els canvis necessaris, exporteu aquesta solució com a **Solució administrada** i importeu-la a altres instàncies per tornar a utilitzar la configuració dels preus.</span><span class="sxs-lookup"><span data-stu-id="e7087-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>


## <a name="create-a-custom-solution-for-pricing-dimensions"></a><span data-ttu-id="e7087-109">Crear una solució personalitzada per a les dimensions de preus</span><span class="sxs-lookup"><span data-stu-id="e7087-109">Create a custom solution for pricing dimensions</span></span>
1. <span data-ttu-id="e7087-110">Al PSA, feu clic a **Configuració** > **Solucions** i, a continuació, feu clic a **Crea** per crear una solució nova.</span><span class="sxs-lookup"><span data-stu-id="e7087-110">In PSA, click **Settings** > **Solutions**, and then click **New** to create a new solution.</span></span> 
2. <span data-ttu-id="e7087-111">Anomeneu la solució **Dimensions de preus de \<nom de l'organització>**, introduïu la informació necessària restant i, a continuació, feu clic a **Desa**.</span><span class="sxs-lookup"><span data-stu-id="e7087-111">Name the solution, **\<your organization name> pricing dimensions**, enter the remaining required information, and then click **Save**.</span></span>

> ![Crear una solució personalitzada per a les dimensions de preus](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="e7087-113">Crear camps personalitzats i conjunts d'opcions a la solució de preus de la dimensió</span><span class="sxs-lookup"><span data-stu-id="e7087-113">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="e7087-114">Una dimensió de preus pot ser una conjunt d'opcions o una entitat.</span><span class="sxs-lookup"><span data-stu-id="e7087-114">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="e7087-115">Tots dos s'han de crear a la solució de preus.</span><span class="sxs-lookup"><span data-stu-id="e7087-115">Both must be created in your pricing solution.</span></span> <span data-ttu-id="e7087-116">Els passos d'aquest procediment expliquen com crear dimensions basades en una entitat i dimensions basades en un conjunt d'opcions.</span><span class="sxs-lookup"><span data-stu-id="e7087-116">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="e7087-117">Dimensions basades en una entitat</span><span class="sxs-lookup"><span data-stu-id="e7087-117">Entity-based dimensions</span></span>

1. <span data-ttu-id="e7087-118">Al PSA, feu clic a **Configuració** > **Solucions** i, a continuació, feu doble clic a **Dimensions de preus de \<nom de l'organització>**.</span><span class="sxs-lookup"><span data-stu-id="e7087-118">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="e7087-119">A l'Explorador de solucions, a la subfinestra de navegació esquerra, seleccioneu **Entitats**.</span><span class="sxs-lookup"><span data-stu-id="e7087-119">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="e7087-120">Feu clic a **Nou** per crear una entitat nova anomenada **Càrrec estàndard**.</span><span class="sxs-lookup"><span data-stu-id="e7087-120">Click **New** to create a new entity called **Standard Title**.</span></span> <span data-ttu-id="e7087-121">Introduïu la informació requerida restant i feu clic a **Desa**.</span><span class="sxs-lookup"><span data-stu-id="e7087-121">Enter the remaining required information, and then click **Save**.</span></span>

> ![Definició de l'entitat de càrrec estàndard](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a><span data-ttu-id="e7087-123">Dimensions basades en un conjunt d'opcions</span><span class="sxs-lookup"><span data-stu-id="e7087-123">Option set-based dimensions</span></span> 
<span data-ttu-id="e7087-124">Podeu crear dues dimensions basades en un conjunt d'opcions.</span><span class="sxs-lookup"><span data-stu-id="e7087-124">You can create two option set-based dimensions.</span></span> <span data-ttu-id="e7087-125">Utilitzeu **Ubicació de treball del recurs** per fer el seguiment del treball de la ubicació **Casa** i **In situ** i utilitzeu **Hores de treball del recurs** amb els valors **Normals** i **Extres** per aplicar un marge comercial quan s'hagi completat la feina.</span><span class="sxs-lookup"><span data-stu-id="e7087-125">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="e7087-126">Al PSA, feu clic a **Configuració** > **Solucions** i, a continuació, feu doble clic a **Dimensions de preus de \<nom de l'organització>**.</span><span class="sxs-lookup"><span data-stu-id="e7087-126">In PSA, click **Settings** > **Solutions**, and then double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="e7087-127">A l'Explorador de solucions, a la subfinestra de navegació esquerra, seleccioneu **Conjunts d'opcions**.</span><span class="sxs-lookup"><span data-stu-id="e7087-127">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="e7087-128">Feu clic a **Nou** per crear un conjunt d'opcions nou, introduïu la informació necessària restant i, a continuació, feu clic a **Desa**.</span><span class="sxs-lookup"><span data-stu-id="e7087-128">Click **New** to create a new option set, enter the remaining required information, and then click **Save**.</span></span>

> ![<span data-ttu-id="e7087-129">Dimensió de preus basada en conjunt d'opcions anomenada Ubicació de treball del recurs</span><span class="sxs-lookup"><span data-stu-id="e7087-129">Option set based pricing dimension called Resource Work Location</span></span> ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![<span data-ttu-id="e7087-130">Dimensió de preus basada en conjunt d'opcions anomenada Hores de treball del recurs</span><span class="sxs-lookup"><span data-stu-id="e7087-130">Option set based pricing dimension called Resource Work Hours</span></span> ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="e7087-131">Crear dades per a les dimensions basades en l'entitat</span><span class="sxs-lookup"><span data-stu-id="e7087-131">Create data for entity-based dimensions</span></span>

<span data-ttu-id="e7087-132">Podeu crear dades per a les dimensions basades en l'entitat manualment o mitjançant una importació del Microsoft Excel o trucades de servei.</span><span class="sxs-lookup"><span data-stu-id="e7087-132">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="e7087-133">Utilitzeu els passos d'aquest procediment per crear dos càrrecs estàndard, **Enginyer de sistemes** i **Enginyer de sistemes sènior** per la dimensió basada en l'entitat **Càrrec estàndard**.</span><span class="sxs-lookup"><span data-stu-id="e7087-133">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="e7087-134">Si les dades que voleu crear són petites, com a l'exemple següent, podeu utilitzar un formulari estàndard.</span><span class="sxs-lookup"><span data-stu-id="e7087-134">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="e7087-135">Al PSA, feu clic a **Cerca avançada**.</span><span class="sxs-lookup"><span data-stu-id="e7087-135">In PSA, click **Advanced Find**.</span></span> <span data-ttu-id="e7087-136">Seleccioneu l'entitat **Càrrec estàndard** i, a continuació, feu clic a **Resultats**.</span><span class="sxs-lookup"><span data-stu-id="e7087-136">Select the entity **Standard Title** and then click **Results**.</span></span> <span data-ttu-id="e7087-137">Es mostraran totes les files de l'entitat **Càrrec estàndard**.</span><span class="sxs-lookup"><span data-stu-id="e7087-137">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="e7087-138">Feu clic a **Nou**.</span><span class="sxs-lookup"><span data-stu-id="e7087-138">Click **New**.</span></span> <span data-ttu-id="e7087-139">Al camp **Nom**, introduïu "Enginyer de sistemes" i, a continuació, feu clic a **Desa**.</span><span class="sxs-lookup"><span data-stu-id="e7087-139">In the **Name** field, enter "Systems Engineer" and then click **Save**.</span></span>
3. <span data-ttu-id="e7087-140">Tanqueu el formulari.</span><span class="sxs-lookup"><span data-stu-id="e7087-140">Close the form.</span></span> 
4. <span data-ttu-id="e7087-141">Repetiu els passos 1-3 per crear un altre càrrec estàndard per a "Enginyer de sistemes sènior".</span><span class="sxs-lookup"><span data-stu-id="e7087-141">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![<span data-ttu-id="e7087-142">Dades d'exemple per a l'entitat Càrrec estàndard</span><span class="sxs-lookup"><span data-stu-id="e7087-142">Sample Data for Standard Title entity</span></span> ](media/ST-data.png)

## <a name="add-all-required-psa-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="e7087-143">Afegiu totes les entitats del PSA necessàries i els components relacionats a la solució de la dimensió de preus</span><span class="sxs-lookup"><span data-stu-id="e7087-143">Add all required PSA entities and related components to the Pricing Dimension Solution</span></span>
<span data-ttu-id="e7087-144">Haureu d'afegir les següents entitats del Project Service a la solució de preus.</span><span class="sxs-lookup"><span data-stu-id="e7087-144">You will need to add the following Project Service entities to your pricing solution.</span></span> <span data-ttu-id="e7087-145">Utilitzeu els passos d'aquest procediment per fer canvis importants d'esquema a la solució de preus de manera que les entitats coneguin les noves dimensions de preus.</span><span class="sxs-lookup"><span data-stu-id="e7087-145">Use the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="e7087-146">Al PSA, feu clic a **Configuració** > **Solucions** i, a continuació, feu doble clic a **Dimensions de preus de \<nom de l'organització>**.</span><span class="sxs-lookup"><span data-stu-id="e7087-146">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="e7087-147">A l'Explorador de solucions, a la subfinestra de navegació esquerra, seleccioneu **Afegeix existent** > **Entitats**.</span><span class="sxs-lookup"><span data-stu-id="e7087-147">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="e7087-148">Al quadre de diàleg **Components de la solució**, seleccioneu una de les entitats següents:</span><span class="sxs-lookup"><span data-stu-id="e7087-148">In the **Solution Components** dialog box, select the following entities:</span></span>

- <span data-ttu-id="e7087-149">Real</span><span class="sxs-lookup"><span data-stu-id="e7087-149">Actual</span></span>
- <span data-ttu-id="e7087-150">Recurs que es pot reservar</span><span class="sxs-lookup"><span data-stu-id="e7087-150">Bookable Resource</span></span>
- <span data-ttu-id="e7087-151">Línia d'estimació</span><span class="sxs-lookup"><span data-stu-id="e7087-151">Estimate Line</span></span>
- <span data-ttu-id="e7087-152">Detall de la línia de factura</span><span class="sxs-lookup"><span data-stu-id="e7087-152">Invoice Line Detail</span></span>
- <span data-ttu-id="e7087-153">Línia del llibre diari</span><span class="sxs-lookup"><span data-stu-id="e7087-153">Journal Line</span></span>
- <span data-ttu-id="e7087-154">Detall de la línia de contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="e7087-154">Project Contract Line Detail</span></span>
- <span data-ttu-id="e7087-155">Membre de l'equip del projecte</span><span class="sxs-lookup"><span data-stu-id="e7087-155">Project Team Member</span></span>
- <span data-ttu-id="e7087-156">Detall de la línia d'oferta</span><span class="sxs-lookup"><span data-stu-id="e7087-156">Quote Line Detail</span></span>
- <span data-ttu-id="e7087-157">Marge comercial de preu de funció</span><span class="sxs-lookup"><span data-stu-id="e7087-157">Role Price Markup</span></span>
- <span data-ttu-id="e7087-158">Preu per funció</span><span class="sxs-lookup"><span data-stu-id="e7087-158">Role Price</span></span> 
- <span data-ttu-id="e7087-159">Entrada de temps</span><span class="sxs-lookup"><span data-stu-id="e7087-159">Time Entry</span></span> 

> ![Afegir entitats existents a la solució de dimensions de preus](media/Existing-entities-to-PD-solution.png)

> ![Selecció de components de la solució](media/Dimension-Components.png)

> [!NOTE]
> <span data-ttu-id="e7087-162">Assegureu-vos d'incloure tots els formularis i les visualitzacions de cadascuna de les entitats seleccionades.</span><span class="sxs-lookup"><span data-stu-id="e7087-162">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="e7087-163">Quan se us demani que inclogueu entitats dependents de les entitats seleccionades anteriorment ,feu clic a **No**.</span><span class="sxs-lookup"><span data-stu-id="e7087-163">When prompted to include any dependent entities for the entities selected above, click **No**.</span></span>

> ![No incloguis tots els components relacionats](media/Do-not-include-required.png)


