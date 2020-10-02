---
title: Creació de camps i entitats personalitzats com a dimensions de preus
description: En aquest tema es proporciona informació sobre com crear conjunts d'opcions o entitats personalitzades.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: 2000f7e710267560fe2bd52b0e33024617d108ea
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898249"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a><span data-ttu-id="66d62-103">Creació de camps i entitats personalitzats com a dimensions de preus</span><span class="sxs-lookup"><span data-stu-id="66d62-103">Create custom fields and entities as pricing dimensions</span></span>

<span data-ttu-id="66d62-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_</span><span class="sxs-lookup"><span data-stu-id="66d62-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="66d62-105">Completeu els passos següents en qualsevol moment que vulgueu crear un conjunt d'opcions o una entitat personalitzada.</span><span class="sxs-lookup"><span data-stu-id="66d62-105">Complete the following steps any time that you want to create a custom option set or entity.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="66d62-106">Us recomanem que realitzeu tots els canvis de dimensió de preus personalitzats en una solució separada.</span><span class="sxs-lookup"><span data-stu-id="66d62-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="66d62-107">Aquestes pràctiques recomanades importants proporcionen una flexibilitat futura per actualitzar o suprimir els canvis segons calgui, us ajudaran a reutilitzar el vostre treball i facilita la portabilitat d'aquests canvis en una altra instància.</span><span class="sxs-lookup"><span data-stu-id="66d62-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="66d62-108">Després d'haver fet tots els canvis necessaris, exporteu aquesta solució com a **Solució administrada** i importeu-la a altres instàncies per tornar a utilitzar la configuració dels preus.</span><span class="sxs-lookup"><span data-stu-id="66d62-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>


## <a name="create-a-custom-solution-for-pricing-dimensions"></a><span data-ttu-id="66d62-109">Crear una solució personalitzada per a les dimensions de preus</span><span class="sxs-lookup"><span data-stu-id="66d62-109">Create a custom solution for pricing dimensions</span></span>
1. <span data-ttu-id="66d62-110">Aneu a **Configuració** > **Solucions** i, a continuació, seleccioneu **Crea** per crear una solució nova.</span><span class="sxs-lookup"><span data-stu-id="66d62-110">Go to **Settings** > **Solutions**, and then select **New** to create a new solution.</span></span> 
2. <span data-ttu-id="66d62-111">Anomeneu la solució **Dimensions de preus de \<your organization name>**, introduïu la informació necessària restant i, a continuació, seleccioneu **Desa**.</span><span class="sxs-lookup"><span data-stu-id="66d62-111">Name the solution, **\<your organization name> pricing dimensions**, enter the remaining required information, and then select **Save**.</span></span>
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="66d62-112">Crear camps personalitzats i conjunts d'opcions a la solució de preus de la dimensió</span><span class="sxs-lookup"><span data-stu-id="66d62-112">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="66d62-113">Una dimensió de preus pot ser una conjunt d'opcions o una entitat.</span><span class="sxs-lookup"><span data-stu-id="66d62-113">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="66d62-114">Tots dos s'han de crear a la solució de preus.</span><span class="sxs-lookup"><span data-stu-id="66d62-114">Both must be created in your pricing solution.</span></span> <span data-ttu-id="66d62-115">Els passos d'aquest procediment expliquen com crear dimensions basades en una entitat i dimensions basades en un conjunt d'opcions.</span><span class="sxs-lookup"><span data-stu-id="66d62-115">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="66d62-116">Dimensions basades en una entitat</span><span class="sxs-lookup"><span data-stu-id="66d62-116">Entity-based dimensions</span></span>

1. <span data-ttu-id="66d62-117">Aneu a **Configuració** > **Solucions** i feu doble clic a **Dimensions de preus de \<your organization name>**.</span><span class="sxs-lookup"><span data-stu-id="66d62-117">Go to **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="66d62-118">A l'Explorador de solucions, a la subfinestra de navegació esquerra, seleccioneu **Entitats**.</span><span class="sxs-lookup"><span data-stu-id="66d62-118">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="66d62-119">Seleccioneu **Nou** per crear una entitat nova anomenada **Càrrec estàndard**.</span><span class="sxs-lookup"><span data-stu-id="66d62-119">Select **New** to create a new entity called **Standard Title**.</span></span> 
4. <span data-ttu-id="66d62-120">Introduïu la informació requerida restant i seleccioneu **Desa**.</span><span class="sxs-lookup"><span data-stu-id="66d62-120">Enter the remaining required information, and then select **Save**.</span></span>


### <a name="option-set-based-dimensions"></a><span data-ttu-id="66d62-121">Dimensions basades en un conjunt d'opcions</span><span class="sxs-lookup"><span data-stu-id="66d62-121">Option set-based dimensions</span></span> 
<span data-ttu-id="66d62-122">Podeu crear dues dimensions basades en un conjunt d'opcions.</span><span class="sxs-lookup"><span data-stu-id="66d62-122">You can create two option set-based dimensions.</span></span> <span data-ttu-id="66d62-123">Utilitzeu **Ubicació de treball del recurs** per fer el seguiment del treball de la ubicació **Casa** i **In situ** i utilitzeu **Hores de treball del recurs** amb els valors **Normals** i **Extres** per aplicar un marge comercial quan s'hagi completat la feina.</span><span class="sxs-lookup"><span data-stu-id="66d62-123">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="66d62-124">Aneu a **Configuració** > **Solucions** i feu doble clic a **Dimensions de preus de \<your organization name>**.</span><span class="sxs-lookup"><span data-stu-id="66d62-124">Go to **Settings** > **Solutions**, and double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="66d62-125">A l'Explorador de solucions, a la subfinestra de navegació esquerra, seleccioneu **Conjunts d'opcions**.</span><span class="sxs-lookup"><span data-stu-id="66d62-125">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="66d62-126">Seleccioneu **Nou** per crear un conjunt d'opcions nou, introduïu la informació necessària restant i, a continuació, seleccioneu **Desa**.</span><span class="sxs-lookup"><span data-stu-id="66d62-126">Select **New** to create a new option set, enter the remaining required information, and then select **Save**.</span></span>

## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="66d62-127">Crear dades per a les dimensions basades en l'entitat</span><span class="sxs-lookup"><span data-stu-id="66d62-127">Create data for entity-based dimensions</span></span>

<span data-ttu-id="66d62-128">Podeu crear dades per a les dimensions basades en l'entitat manualment o mitjançant una importació del Microsoft Excel o trucades de servei.</span><span class="sxs-lookup"><span data-stu-id="66d62-128">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="66d62-129">Utilitzeu els passos d'aquest procediment per crear dos càrrecs estàndard, **Enginyer de sistemes** i **Enginyer de sistemes sènior** per la dimensió basada en l'entitat **Càrrec estàndard**.</span><span class="sxs-lookup"><span data-stu-id="66d62-129">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="66d62-130">Si les dades que voleu crear són petites, com a l'exemple següent, podeu utilitzar un formulari estàndard.</span><span class="sxs-lookup"><span data-stu-id="66d62-130">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="66d62-131">Seleccioneu **Cerca avançada**, seleccioneu l'entitat **Càrrec estàndard** i, a continuació, seleccioneu **Resultats**.</span><span class="sxs-lookup"><span data-stu-id="66d62-131">Select **Advanced Find**, select the entity **Standard Title**, and then select **Results**.</span></span> <span data-ttu-id="66d62-132">Es mostraran totes les files de l'entitat **Càrrec estàndard**.</span><span class="sxs-lookup"><span data-stu-id="66d62-132">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="66d62-133">Seleccioneu **Nou** i al camp **Nom**, introduïu "Enginyer de sistemes" i, a continuació, seleccioneu **Desa**.</span><span class="sxs-lookup"><span data-stu-id="66d62-133">Select **New**, and in the **Name** field, enter "Systems Engineer" and then select **Save**.</span></span>
3. <span data-ttu-id="66d62-134">Tanca el formulari.</span><span class="sxs-lookup"><span data-stu-id="66d62-134">Close the form.</span></span> 
4. <span data-ttu-id="66d62-135">Repetiu els passos 1-3 per crear un altre càrrec estàndard per a "Enginyer de sistemes sènior".</span><span class="sxs-lookup"><span data-stu-id="66d62-135">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="66d62-136">Afegiu totes les entitats necessàries i els components relacionats a la solució de la dimensió de preus</span><span class="sxs-lookup"><span data-stu-id="66d62-136">Add all required entities and related components to the Pricing Dimension Solution</span></span>
<span data-ttu-id="66d62-137">Haureu d'afegir les següents entitats a la solució de preus.</span><span class="sxs-lookup"><span data-stu-id="66d62-137">You will need to add the following entities to your pricing solution.</span></span> <span data-ttu-id="66d62-138">Utilitzeu els passos d'aquest procediment per fer canvis importants d'esquema a la solució de preus de manera que les entitats coneguin les noves dimensions de preus.</span><span class="sxs-lookup"><span data-stu-id="66d62-138">Use the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="66d62-139">Seleccioneu **Configuració** > **Solucions** i feu doble clic a **Dimensions de preus de \<your organization name>**.</span><span class="sxs-lookup"><span data-stu-id="66d62-139">Select **Settings** > **Solutions**, and double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="66d62-140">A l'Explorador de solucions, a la subfinestra de navegació esquerra, seleccioneu **Afegeix existent** > **Entitats**.</span><span class="sxs-lookup"><span data-stu-id="66d62-140">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="66d62-141">Al quadre de diàleg **Components de la solució**, seleccioneu una de les entitats següents:</span><span class="sxs-lookup"><span data-stu-id="66d62-141">In the **Solution Components** dialog box, select the following entities:</span></span>

  - <span data-ttu-id="66d62-142">Real</span><span class="sxs-lookup"><span data-stu-id="66d62-142">Actual</span></span>
  - <span data-ttu-id="66d62-143">Recurs que es pot reservar</span><span class="sxs-lookup"><span data-stu-id="66d62-143">Bookable Resource</span></span>
  - <span data-ttu-id="66d62-144">Línia d'estimació</span><span class="sxs-lookup"><span data-stu-id="66d62-144">Estimate Line</span></span>
  - <span data-ttu-id="66d62-145">Detall de la línia de factura</span><span class="sxs-lookup"><span data-stu-id="66d62-145">Invoice Line Detail</span></span>
  - <span data-ttu-id="66d62-146">Línia del llibre diari</span><span class="sxs-lookup"><span data-stu-id="66d62-146">Journal Line</span></span>
  - <span data-ttu-id="66d62-147">Detall de la línia de contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="66d62-147">Project Contract Line Detail</span></span>
  - <span data-ttu-id="66d62-148">Membre de l'equip del projecte</span><span class="sxs-lookup"><span data-stu-id="66d62-148">Project Team Member</span></span>
  - <span data-ttu-id="66d62-149">Detall de la línia d’oferta</span><span class="sxs-lookup"><span data-stu-id="66d62-149">Quote Line Detail</span></span>
  - <span data-ttu-id="66d62-150">Marge comercial de preu de funció</span><span class="sxs-lookup"><span data-stu-id="66d62-150">Role Price Markup</span></span>
  - <span data-ttu-id="66d62-151">Preu per funció</span><span class="sxs-lookup"><span data-stu-id="66d62-151">Role Price</span></span> 
  - <span data-ttu-id="66d62-152">Entrada de temps</span><span class="sxs-lookup"><span data-stu-id="66d62-152">Time Entry</span></span> 


> [!NOTE]
> <span data-ttu-id="66d62-153">Assegureu-vos d'incloure tots els formularis i les visualitzacions de cadascuna de les entitats seleccionades.</span><span class="sxs-lookup"><span data-stu-id="66d62-153">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="66d62-154">Quan se us demani que inclogueu entitats dependents de les entitats seleccionades anteriorment, seleccioneu **No**.</span><span class="sxs-lookup"><span data-stu-id="66d62-154">When prompted to include any dependent entities for the entities selected above, select **No**.</span></span>

