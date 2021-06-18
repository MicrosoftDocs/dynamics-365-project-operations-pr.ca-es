---
title: Creació de camps i entitats personalitzats com a dimensions de preus
description: En aquest tema es proporciona informació sobre com crear conjunts d'opcions o entitats personalitzades.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 41c57690fecbc3bee2a1eb5d26f8a6aa56d8bea9
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000514"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a><span data-ttu-id="8db25-103">Creació de camps i entitats personalitzats com a dimensions de preus</span><span class="sxs-lookup"><span data-stu-id="8db25-103">Create custom fields and entities as pricing dimensions</span></span>

<span data-ttu-id="8db25-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_</span><span class="sxs-lookup"><span data-stu-id="8db25-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8db25-105">Completeu els passos següents quan vulgueu crear un conjunt d'opcions o una entitat personalitzats per utilitzar-los com a dimensió de preus.</span><span class="sxs-lookup"><span data-stu-id="8db25-105">Complete the following steps when you want to create a custom option set or entity for using it as a pricing dimension.</span></span> <span data-ttu-id="8db25-106">Per obtenir més informació, vegeu [Informació general sobre les dimensions de preus](pricing-dimensions-overview.md).</span><span class="sxs-lookup"><span data-stu-id="8db25-106">For more information, see [Pricing dimensions overview](pricing-dimensions-overview.md).</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="8db25-107">Us recomanem que realitzeu tots els canvis de dimensió de preus personalitzats en una solució separada.</span><span class="sxs-lookup"><span data-stu-id="8db25-107">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="8db25-108">Aquesta pràctica important proporciona flexibilitat en el futur per actualitzar o suprimir els canvis segons calgui.</span><span class="sxs-lookup"><span data-stu-id="8db25-108">This important best practice provides flexibility in the future to update or remove changes as needed.</span></span> <span data-ttu-id="8db25-109">D'aquesta manera, també us ajudarà a reutilitzar la feina feta i facilitarà el trasllat d'aquests canvis a una altra instància Quan hagueu fet tots els canvis necessaris, exporteu aquesta solució com a **Solució administrada** i importeu-la en altres instàncies per reutilitzar la configuració de preus.</span><span class="sxs-lookup"><span data-stu-id="8db25-109">This will also help with re-use of your work and make it easier to port these changes to another instance After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="8db25-110">Crear camps personalitzats i conjunts d'opcions a la solució de preus de la dimensió</span><span class="sxs-lookup"><span data-stu-id="8db25-110">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="8db25-111">Una dimensió de preus pot ser una conjunt d'opcions o una entitat.</span><span class="sxs-lookup"><span data-stu-id="8db25-111">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="8db25-112">Tots dos s'han de crear a la solució de preus.</span><span class="sxs-lookup"><span data-stu-id="8db25-112">Both must be created in your pricing solution.</span></span> <span data-ttu-id="8db25-113">Els passos d'aquest procediment expliquen com crear dimensions basades en una entitat i dimensions basades en un conjunt d'opcions.</span><span class="sxs-lookup"><span data-stu-id="8db25-113">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="8db25-114">Dimensions basades en una entitat</span><span class="sxs-lookup"><span data-stu-id="8db25-114">Entity-based dimensions</span></span>
<span data-ttu-id="8db25-115">Per crear dimensions basades en entitat, seguiu aquests passos:</span><span class="sxs-lookup"><span data-stu-id="8db25-115">To create entity-based dimensions, follow these steps:</span></span>

1. <span data-ttu-id="8db25-116">Aneu a **Configuració** > **Solucions** i feu doble clic a **Dimensions de preus de \<your organization name>**.</span><span class="sxs-lookup"><span data-stu-id="8db25-116">Go to **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="8db25-117">A l'Explorador de solucions, a la subfinestra de navegació esquerra, seleccioneu **Entitats**.</span><span class="sxs-lookup"><span data-stu-id="8db25-117">In Solution Explorer, in the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="8db25-118">Seleccioneu **Nou** per crear una entitat nova anomenada **Càrrec estàndard**.</span><span class="sxs-lookup"><span data-stu-id="8db25-118">Select **New** to create a new entity called **Standard Title**.</span></span> 
4. <span data-ttu-id="8db25-119">Introduïu la informació requerida restant i seleccioneu **Desa**.</span><span class="sxs-lookup"><span data-stu-id="8db25-119">Enter the remaining required information, and then select **Save**.</span></span>

> ![Definició de l'entitat de càrrec estàndard](media/Standard-Title-entity-definition.png)

### <a name="option-set-based-dimensions"></a><span data-ttu-id="8db25-121">Dimensions basades en un conjunt d'opcions</span><span class="sxs-lookup"><span data-stu-id="8db25-121">Option set-based dimensions</span></span> 
<span data-ttu-id="8db25-122">Podeu crear dues dimensions basades en un conjunt d'opcions.</span><span class="sxs-lookup"><span data-stu-id="8db25-122">You can create two option set-based dimensions.</span></span> 

- <span data-ttu-id="8db25-123">Utilitzeu **Ubicació del treball dels recursos** per fer el seguiment del preu de la feina a la ubicació **Casa** i de la feina **In situ**.</span><span class="sxs-lookup"><span data-stu-id="8db25-123">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work.</span></span> 
- <span data-ttu-id="8db25-124">Utilitzeu **Hores de feina de recursos** amb valors **Normals** i **Hores extres** per aplicar un marge comercial quan s'hagi completat l'obra.</span><span class="sxs-lookup"><span data-stu-id="8db25-124">Use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when the work is complete.</span></span>

<span data-ttu-id="8db25-125">El gràfic següent proporciona una visualització de la dimensió **Ubicació del treball del recurs**.</span><span class="sxs-lookup"><span data-stu-id="8db25-125">The following graphic provides a view of the **Resource Work Location** dimension.</span></span> 

> ![Dimensió de preus basada en conjunt d'opcions anomenada Ubicació de treball del recurs](media/Option-set-PD-called-Resource-Work-Location.png)

<span data-ttu-id="8db25-127">El gràfic següent proporciona una visualització de la dimensió **Hores de treball del recurs**.</span><span class="sxs-lookup"><span data-stu-id="8db25-127">The following graphic provides a view of the **Resource Work Hours** dimension.</span></span> 

> ![Dimensió de preus basada en conjunt d'opcions anomenada Hores de treball del recurs](media/Option-set-PD-called-Resource-Work-Hours.png)

1. <span data-ttu-id="8db25-129">Aneu a **Configuració** > **Solucions** i feu doble clic a **Dimensions de preus de \<your organization name>**.</span><span class="sxs-lookup"><span data-stu-id="8db25-129">Go to **Settings** > **Solutions**, and double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="8db25-130">A l'Explorador de solucions, a la subfinestra de navegació esquerra, seleccioneu **Conjunts d'opcions**.</span><span class="sxs-lookup"><span data-stu-id="8db25-130">In Solution Explorer, in the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="8db25-131">Seleccioneu **Nou** per crear un conjunt d'opcions nou, introduïu la informació necessària restant i, a continuació, seleccioneu **Desa**.</span><span class="sxs-lookup"><span data-stu-id="8db25-131">Select **New** to create a new option set, enter the remaining required information, and then select **Save**.</span></span>

## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="8db25-132">Crear dades per a les dimensions basades en l'entitat</span><span class="sxs-lookup"><span data-stu-id="8db25-132">Create data for entity-based dimensions</span></span>

<span data-ttu-id="8db25-133">Podeu crear dades per a les dimensions basades en l'entitat manualment o mitjançant una importació del Microsoft Excel o trucades de servei.</span><span class="sxs-lookup"><span data-stu-id="8db25-133">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="8db25-134">Utilitzeu els passos d'aquest procediment per crear dos càrrecs estàndard, **Enginyer de sistemes** i **Enginyer de sistemes sènior** per la dimensió basada en l'entitat **Càrrec estàndard**.</span><span class="sxs-lookup"><span data-stu-id="8db25-134">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="8db25-135">Si les dades que voleu crear són petites, com a l'exemple següent, podeu utilitzar un formulari estàndard.</span><span class="sxs-lookup"><span data-stu-id="8db25-135">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="8db25-136">Seleccioneu **Cerca avançada**.</span><span class="sxs-lookup"><span data-stu-id="8db25-136">Select **Advanced Find**.</span></span>
2. <span data-ttu-id="8db25-137">Seleccioneu l'entitat **Càrrec estàndard** i, a continuació, seleccioneu **Resultats**.</span><span class="sxs-lookup"><span data-stu-id="8db25-137">Select the entity **Standard Title**, and then select **Results**.</span></span> <span data-ttu-id="8db25-138">Es mostraran totes les files de l'entitat **Càrrec estàndard**.</span><span class="sxs-lookup"><span data-stu-id="8db25-138">All of the rows in the **Standard Title** entity will be shown.</span></span>
3. <span data-ttu-id="8db25-139">Seleccioneu **Nou** i al camp **Nom**, introduïu "Enginyer de sistemes" i, a continuació, seleccioneu **Desa**.</span><span class="sxs-lookup"><span data-stu-id="8db25-139">Select **New**, and in the **Name** field, enter "Systems Engineer" and then select **Save**.</span></span>
4. <span data-ttu-id="8db25-140">Tanqueu la pàgina.</span><span class="sxs-lookup"><span data-stu-id="8db25-140">Close the page.</span></span> 
5. <span data-ttu-id="8db25-141">Repetiu els passos 1-3 per crear un altre càrrec estàndard per a "Enginyer de sistemes sènior".</span><span class="sxs-lookup"><span data-stu-id="8db25-141">Repeat steps 1-3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![Dades d'exemple per a l'entitat Càrrec estàndard](media/ST-data.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]