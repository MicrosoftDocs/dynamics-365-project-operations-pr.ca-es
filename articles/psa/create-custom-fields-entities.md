---
title: Crear camps i entitats personalitzats
description: En aquest tema s'explica com crear conjunts d'opcions i entitats a la vostra pròpia solució a la plataforma Power Apps.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 442ff9cf2206bec307cea7ff30b9266502d8f77b
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072281"
---
# <a name="create-custom-fields-and-entities"></a><span data-ttu-id="9383e-103">Crear camps i entitats personalitzats</span><span class="sxs-lookup"><span data-stu-id="9383e-103">Create custom fields and entities</span></span> 

<span data-ttu-id="9383e-104">Completeu els passos següents en qualsevol moment que vulgueu crear un conjunt d'opcions o una entitat personalitzada a la plataforma del Power Apps.</span><span class="sxs-lookup"><span data-stu-id="9383e-104">Complete the following steps any time that you want to create a custom option set or entity on the Power Apps platform.</span></span>  
<span data-ttu-id="9383e-105">Els procediments d'aquest tema s'han d'emplenar mitjançant la interfície web del Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="9383e-105">The procedures in this topic should be completed using the web interface of Project Service Automation (PSA).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9383e-106">Us recomanem que realitzeu tots els canvis de dimensió de preus personalitzats en una solució separada.</span><span class="sxs-lookup"><span data-stu-id="9383e-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="9383e-107">Aquestes pràctiques recomanades importants proporcionen una flexibilitat futura per actualitzar o suprimir els canvis segons calgui, us ajudaran a reutilitzar el vostre treball i facilita la portabilitat d'aquests canvis en una altra instància.</span><span class="sxs-lookup"><span data-stu-id="9383e-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="9383e-108">Després d'haver fet tots els canvis necessaris, exporteu aquesta solució com a **Solució administrada** i importeu-la a altres instàncies per tornar a utilitzar la configuració dels preus.</span><span class="sxs-lookup"><span data-stu-id="9383e-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="9383e-109">Crear camps personalitzats i conjunts d'opcions a la solució de preus de la dimensió</span><span class="sxs-lookup"><span data-stu-id="9383e-109">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="9383e-110">Una dimensió de preus pot ser una conjunt d'opcions o una entitat.</span><span class="sxs-lookup"><span data-stu-id="9383e-110">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="9383e-111">Tots dos s'han de crear a la solució de preus.</span><span class="sxs-lookup"><span data-stu-id="9383e-111">Both must be created in your pricing solution.</span></span> <span data-ttu-id="9383e-112">Els passos d'aquest procediment expliquen com crear dimensions basades en una entitat i dimensions basades en un conjunt d'opcions.</span><span class="sxs-lookup"><span data-stu-id="9383e-112">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="9383e-113">Dimensions basades en una entitat</span><span class="sxs-lookup"><span data-stu-id="9383e-113">Entity-based dimensions</span></span>

1. <span data-ttu-id="9383e-114">Al PSA, feu clic a **Configuració** > **Solucions** i feu doble clic a **Dimensions de preus de \<your organization name>**.</span><span class="sxs-lookup"><span data-stu-id="9383e-114">In PSA, click **Settings** > **Solutions** , and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="9383e-115">A l'Explorador de solucions, a la subfinestra de navegació esquerra, seleccioneu **Entitats**.</span><span class="sxs-lookup"><span data-stu-id="9383e-115">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="9383e-116">Feu clic a **Nou** per crear una entitat nova anomenada **Càrrec estàndard**.</span><span class="sxs-lookup"><span data-stu-id="9383e-116">Click **New** to create a new entity called **Standard Title**.</span></span> <span data-ttu-id="9383e-117">Introduïu la informació requerida restant i feu clic a **Desa**.</span><span class="sxs-lookup"><span data-stu-id="9383e-117">Enter the remaining required information, and then click **Save**.</span></span>

> ![Definició de l'entitat de càrrec estàndard](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a><span data-ttu-id="9383e-119">Dimensions basades en un conjunt d'opcions</span><span class="sxs-lookup"><span data-stu-id="9383e-119">Option set-based dimensions</span></span> 
<span data-ttu-id="9383e-120">Podeu crear dues dimensions basades en un conjunt d'opcions.</span><span class="sxs-lookup"><span data-stu-id="9383e-120">You can create two option set-based dimensions.</span></span> <span data-ttu-id="9383e-121">Utilitzeu **Ubicació de treball del recurs** per fer el seguiment del treball de la ubicació **Casa** i **In situ** i utilitzeu **Hores de treball del recurs** amb els valors **Normals** i **Extres** per aplicar un marge comercial quan s'hagi completat la feina.</span><span class="sxs-lookup"><span data-stu-id="9383e-121">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="9383e-122">Al PSA, feu clic a **Configuració** > **Solucions** i feu doble clic a **Dimensions de preus de \<your organization name>**.</span><span class="sxs-lookup"><span data-stu-id="9383e-122">In PSA, click **Settings** > **Solutions** , and then double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="9383e-123">A l'Explorador de solucions, a la subfinestra de navegació esquerra, seleccioneu **Conjunts d'opcions**.</span><span class="sxs-lookup"><span data-stu-id="9383e-123">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="9383e-124">Feu clic a **Nou** per crear un conjunt d'opcions nou, introduïu la informació necessària restant i, a continuació, feu clic a **Desa**.</span><span class="sxs-lookup"><span data-stu-id="9383e-124">Click **New** to create a new option set, enter the remaining required information, and then click **Save**.</span></span>

> ![<span data-ttu-id="9383e-125">Dimensió de preus basada en conjunt d'opcions anomenada Ubicació de treball del recurs</span><span class="sxs-lookup"><span data-stu-id="9383e-125">Option set based pricing dimension called Resource Work Location</span></span> ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![<span data-ttu-id="9383e-126">Dimensió de preus basada en conjunt d'opcions anomenada Hores de treball del recurs</span><span class="sxs-lookup"><span data-stu-id="9383e-126">Option set based pricing dimension called Resource Work Hours</span></span> ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="9383e-127">Crear dades per a les dimensions basades en l'entitat</span><span class="sxs-lookup"><span data-stu-id="9383e-127">Create data for entity-based dimensions</span></span>

<span data-ttu-id="9383e-128">Podeu crear dades per a les dimensions basades en l'entitat manualment o mitjançant una importació del Microsoft Excel o trucades de servei.</span><span class="sxs-lookup"><span data-stu-id="9383e-128">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="9383e-129">Utilitzeu els passos d'aquest procediment per crear dos càrrecs estàndard, **Enginyer de sistemes** i **Enginyer de sistemes sènior** per la dimensió basada en l'entitat **Càrrec estàndard**.</span><span class="sxs-lookup"><span data-stu-id="9383e-129">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="9383e-130">Si les dades que voleu crear són petites, com a l'exemple següent, podeu utilitzar un formulari estàndard.</span><span class="sxs-lookup"><span data-stu-id="9383e-130">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="9383e-131">Al PSA, feu clic a **Cerca avançada**.</span><span class="sxs-lookup"><span data-stu-id="9383e-131">In PSA, click **Advanced Find**.</span></span> <span data-ttu-id="9383e-132">Seleccioneu l'entitat **Càrrec estàndard** i, a continuació, feu clic a **Resultats**.</span><span class="sxs-lookup"><span data-stu-id="9383e-132">Select the entity **Standard Title** and then click **Results**.</span></span> <span data-ttu-id="9383e-133">Es mostraran totes les files de l'entitat **Càrrec estàndard**.</span><span class="sxs-lookup"><span data-stu-id="9383e-133">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="9383e-134">Feu clic a **Nou**.</span><span class="sxs-lookup"><span data-stu-id="9383e-134">Click **New**.</span></span> <span data-ttu-id="9383e-135">Al camp **Nom** , introduïu "Enginyer de sistemes" i, a continuació, feu clic a **Desa**.</span><span class="sxs-lookup"><span data-stu-id="9383e-135">In the **Name** field, enter "Systems Engineer" and then click **Save**.</span></span>
3. <span data-ttu-id="9383e-136">Tanqueu el formulari.</span><span class="sxs-lookup"><span data-stu-id="9383e-136">Close the form.</span></span> 
4. <span data-ttu-id="9383e-137">Repetiu els passos 1-3 per crear un altre càrrec estàndard per a "Enginyer de sistemes sènior".</span><span class="sxs-lookup"><span data-stu-id="9383e-137">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![<span data-ttu-id="9383e-138">Dades d'exemple per a l'entitat Càrrec estàndard</span><span class="sxs-lookup"><span data-stu-id="9383e-138">Sample Data for Standard Title entity</span></span> ](media/ST-data.png)


