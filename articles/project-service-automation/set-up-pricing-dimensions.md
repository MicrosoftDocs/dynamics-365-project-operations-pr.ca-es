---
title: Configurar camps personalitzats com a dimensions de preus
description: En aquest tema, podreu obtenir informació sobre la configuració de dimensions de preus personalitzades.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/20/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: d5f59779-a6ed-4854-ab82-2810dace288f
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 8f19254acfc7f03ed7ccca95ed7e2b94cc199d3b
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749465"
---
# <a name="set-up-custom-fields-as-pricing-dimensions"></a><span data-ttu-id="3d6d1-103">Configurar camps personalitzats com a dimensions de preus</span><span class="sxs-lookup"><span data-stu-id="3d6d1-103">Set up custom fields as pricing dimensions</span></span> 

<span data-ttu-id="3d6d1-104">Abans de començar, aquest tema assumeix que heu completat els procediments dels temes [Crear camps i entitats personalitzats](create-custom-fields-entities.md) i [Afegir camps personalitzats a la configuració de preus i les entitats transaccionals](field-references.md).</span><span class="sxs-lookup"><span data-stu-id="3d6d1-104">Before you begin, this topic assumes that you have completed the procedures in the topics, [Create custom fields and entities](create-custom-fields-entities.md) and [Add custom fields to price setup and transactional entities](field-references.md).</span></span> <span data-ttu-id="3d6d1-105">Si no heu completat aquests procediments, aneu enrere per completar-los torneu a aquest tema.</span><span class="sxs-lookup"><span data-stu-id="3d6d1-105">If you haven't completed those procedures, go back and complete them and then return to this topic.</span></span> 

<span data-ttu-id="3d6d1-106">En aquest tema, podreu obtenir informació sobre la configuració de dimensions de preus personalitzades.</span><span class="sxs-lookup"><span data-stu-id="3d6d1-106">This topic provides information about setting up custom pricing dimensions.</span></span> <span data-ttu-id="3d6d1-107">A la interfície web del Project Service, a la pàgina **Paràmetres**, la pestanya **Dimensions de preus basades en el preu** mostra els registres de l'entitat de dimensions de preus.</span><span class="sxs-lookup"><span data-stu-id="3d6d1-107">In the Project Service web interface, on the **Parameters** page, the **Amount-Based Pricing Dimensions** tab shows the records in the pricing dimension entities.</span></span> <span data-ttu-id="3d6d1-108">Per defecte, la instal·lació del Project Service crea 2 files a la quadrícula en aquesta pestanya:</span><span class="sxs-lookup"><span data-stu-id="3d6d1-108">By default, Project Service installation creates 2 rows in the grid on this tab:</span></span>

- <span data-ttu-id="3d6d1-109">**msdyn_resourcecategory** (Funció)</span><span class="sxs-lookup"><span data-stu-id="3d6d1-109">**msdyn_resourcecategory** (Role)</span></span>
- <span data-ttu-id="3d6d1-110">**msdyn_OrganizationalUnit** (Unitat organitzativa)</span><span class="sxs-lookup"><span data-stu-id="3d6d1-110">**msdyn_OrganizationalUnit** (Organizational Unit)</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3d6d1-111">No suprimiu aquestes files.</span><span class="sxs-lookup"><span data-stu-id="3d6d1-111">Do not delete these rows.</span></span> <span data-ttu-id="3d6d1-112">No obstant, si no les necessiteu, podeu fer que no s'apliquin en un context específic establint **Aplicable al cost**, **Aplicable a les vendes**i **Aplicable a les compres** com a **No**.</span><span class="sxs-lookup"><span data-stu-id="3d6d1-112">However, if you do not need them, you can make them not applicable in a specific context by setting **Applicable to Cost**, **Applicable to Sales**, and **Applicable to Purchase** all to **No**.</span></span> <span data-ttu-id="3d6d1-113">La configuració d'aquests valors d'atribut com a **No** té el mateix efecte de no tenir el camp com a dimensió de preus.</span><span class="sxs-lookup"><span data-stu-id="3d6d1-113">Setting these attribute values to **No** has the same effect of not having the field as a pricing dimension.</span></span>

<span data-ttu-id="3d6d1-114">Per tal que un camp es converteixi en una dimensió de preus, ha de ser:</span><span class="sxs-lookup"><span data-stu-id="3d6d1-114">For a field to become a pricing dimension, it must be:</span></span>

- <span data-ttu-id="3d6d1-115">Creat com a camp a les entitats **Preu per funció** i **Marge comercial del preu per funció**.</span><span class="sxs-lookup"><span data-stu-id="3d6d1-115">Created as a field in the **Role Price** and **Role Price markup** entities.</span></span> <span data-ttu-id="3d6d1-116">Per obtenir més informació sobre com fer-ho, vegeu [Afegir camps personalitzats a la configuració de preus i a entitats transaccionals](field-references.md).</span><span class="sxs-lookup"><span data-stu-id="3d6d1-116">For more information on how to do this, see [Add custom fields to price setup and transactional entities](field-references.md).</span></span>
- <span data-ttu-id="3d6d1-117">Creat com una fila a la taula **Dimensió de preus**.</span><span class="sxs-lookup"><span data-stu-id="3d6d1-117">Created as a row in the **Pricing Dimension** table.</span></span> <span data-ttu-id="3d6d1-118">Per exemple, afegiu files de dimensió de preus com es mostra a la gràfica següent.</span><span class="sxs-lookup"><span data-stu-id="3d6d1-118">For example, add pricing dimension rows as shown in the following graphic.</span></span> 

![Files de dimensions de preus basades en els imports](media/Amt-based-PD.png)

<span data-ttu-id="3d6d1-120">Observeu que Hores de treball del recurs (**msdyn_resourceworkhours**) s'ha afegit com una dimensió basada en el marge comercial i s'ha afegit a la quadrícula a la pestanya **Dimensió de preus basada en el marge comercial**.</span><span class="sxs-lookup"><span data-stu-id="3d6d1-120">Notice that Resource Work hours (**msdyn_resourceworkhours**) has been added as a markup-based dimension and has been added to the grid on the **Markup Based Pricing Dimension** tab.</span></span>

![Files de dimensions de preus basades en el marge comercial](media/Markup-based-PD.png)

> [!IMPORTANT]
> <span data-ttu-id="3d6d1-122">Qualsevol canvi de les dades de dimensió de preus d'aquesta taula, existents o noves, es propaga a la lògica empresarial de preus del Project Service només després de l'actualització de la memòria cau.</span><span class="sxs-lookup"><span data-stu-id="3d6d1-122">Any change to pricing dimension data in this table, existing or new, is propagated to the Project Service pricing business logic only after the cache is refreshed.</span></span> <span data-ttu-id="3d6d1-123">El temps d'actualització de la memòria cau pot tardar fins a 10 minuts.</span><span class="sxs-lookup"><span data-stu-id="3d6d1-123">The cache refresh time may take up to 10 minutes.</span></span> <span data-ttu-id="3d6d1-124">Permeteu aquesta duració de temps per veure els canvis en la lògica de preus per defecte que han de derivar dels canvis en les dades de la dimensió de preus.</span><span class="sxs-lookup"><span data-stu-id="3d6d1-124">Allow that length of time to see the changes in price defaulting logic that must result from changes to the Pricing Dimension data.</span></span>


## <a name="attributes-of-the-pricing-dimensions-table"></a><span data-ttu-id="3d6d1-125">Atributs de la taula Dimensions de preus</span><span class="sxs-lookup"><span data-stu-id="3d6d1-125">Attributes of the Pricing Dimensions table</span></span>
<span data-ttu-id="3d6d1-126">A les seccions següents es proporciona informació sobre els diferents atributs a la taula **Dimensions de preus**.</span><span class="sxs-lookup"><span data-stu-id="3d6d1-126">The following sections provide information about the different attributes in the **Pricing Dimensions** table.</span></span>

### <a name="pricing-dimension-name"></a><span data-ttu-id="3d6d1-127">Nom de la dimensió de preus</span><span class="sxs-lookup"><span data-stu-id="3d6d1-127">Pricing Dimension Name</span></span>
<span data-ttu-id="3d6d1-128">Aquest valor hauria de ser el mateix que el nom de l'esquema del camp que s'afegeix a la taula **Preu per funció** per a les dimensions de preus personalitzades.</span><span class="sxs-lookup"><span data-stu-id="3d6d1-128">This value should be the exact same as the schema name of the field that is added to the **Role Price** table for custom pricing dimensions.</span></span> <span data-ttu-id="3d6d1-129">Per obtenir més informació sobre l'addició de camps a la taula **Preu per funció**, vegeu [Afegir camps personalitzats a la configuració de preus i a les entitats transaccionals](field-references.md).</span><span class="sxs-lookup"><span data-stu-id="3d6d1-129">For more information about adding fields to the **Role Price** table, see [Add custom fields to price setup and transactional entities](field-references.md).</span></span>

### <a name="type-of-dimension"></a><span data-ttu-id="3d6d1-130">Tipus de dimensió</span><span class="sxs-lookup"><span data-stu-id="3d6d1-130">Type of dimension</span></span>
<span data-ttu-id="3d6d1-131">Hi ha dos tipus de dimensions de preus:</span><span class="sxs-lookup"><span data-stu-id="3d6d1-131">There are two types of pricing dimensions:</span></span>
  
  - <span data-ttu-id="3d6d1-132">**Dimensions basades en l'import**: els valors de les dimensions del context d'entrada es corresponen als valors de dimensió en la línia **Preu per funció** i el preu i el cost s'obtindran directament per defecte dels valors de la taula **Preu per funció**.</span><span class="sxs-lookup"><span data-stu-id="3d6d1-132">**Amount-based dimensions**: The dimension values from the input context are matched to the dimension values on **Role Price** line and the price/cost is defaulted directly from the **Role Price** table.</span></span>
  - <span data-ttu-id="3d6d1-133">**Dimensions basades en el marge comercial**: són les dimensions en què el Project Service adoptarà el procés de 3 passos següent per obtenir el preu i el cost</span><span class="sxs-lookup"><span data-stu-id="3d6d1-133">**Markup-based dimensions**: These are dimensions where Project Service will adopt the following 3-step process to get the price/cost</span></span>
 
    1. <span data-ttu-id="3d6d1-134">El Project Service fa coincidir els valors de dimensió basats en el marge comercial des del context d'entrada a la línia Preu per funció per obtenir la tarifa base.</span><span class="sxs-lookup"><span data-stu-id="3d6d1-134">Project Service matches the non-markup-based dimension values from the input context to the Role Price line to get the base rate.</span></span>
    2. <span data-ttu-id="3d6d1-135">El Project Service fa coincidir tots els valors de dimensió basats en el marge comercial des del context d'entrada a la línia **Marge comercial del preu per funció** per obtenir el percentatge de marge comercial.</span><span class="sxs-lookup"><span data-stu-id="3d6d1-135">Project Service matches all of the dimension values from the input context to the **Role Price Markup** line to get a markup percentage.</span></span>
    3. <span data-ttu-id="3d6d1-136">El Project Service aplica el percentatge de marge comercial del segon pas a la tarifa base **obtinguda a** partir de la taula Preu per funció en el primer pas per arribar al preu/cost definitiu.</span><span class="sxs-lookup"><span data-stu-id="3d6d1-136">Project Service applies the markup percentage from the second step to the base rate obtained from the **Role Price** table in the first step to arrive at final price/cost.</span></span>
   
   <span data-ttu-id="3d6d1-137">La taula següent il·lustra el càlcul dels marges comercials de preus.</span><span class="sxs-lookup"><span data-stu-id="3d6d1-137">The following table illustrates the calculation of price markups.</span></span>
  
| <span data-ttu-id="3d6d1-138">Funció</span><span class="sxs-lookup"><span data-stu-id="3d6d1-138">Role</span></span>        | <span data-ttu-id="3d6d1-139">Unitat organitzativa</span><span class="sxs-lookup"><span data-stu-id="3d6d1-139">Org Unit</span></span>    |<span data-ttu-id="3d6d1-140">Ubicació del treball</span><span class="sxs-lookup"><span data-stu-id="3d6d1-140">Work Location</span></span>      |<span data-ttu-id="3d6d1-141">Càrrec estàndard</span><span class="sxs-lookup"><span data-stu-id="3d6d1-141">Standard Title</span></span>      |<span data-ttu-id="3d6d1-142">Hores de treball del recurs</span><span class="sxs-lookup"><span data-stu-id="3d6d1-142">Resource Work Hours</span></span>      |  <span data-ttu-id="3d6d1-143">Marge comercial</span><span class="sxs-lookup"><span data-stu-id="3d6d1-143">Mark Up</span></span>|
| ------------|-------------|-------------------|--------------------|-------------------------|--------:|
|             | <span data-ttu-id="3d6d1-144">Contoso India</span><span class="sxs-lookup"><span data-stu-id="3d6d1-144">Contoso India</span></span>|<span data-ttu-id="3d6d1-145">In situ</span><span class="sxs-lookup"><span data-stu-id="3d6d1-145">Onsite</span></span>            |                    |<span data-ttu-id="3d6d1-146">Hores extra</span><span class="sxs-lookup"><span data-stu-id="3d6d1-146">Overtime</span></span>                 |<span data-ttu-id="3d6d1-147">15</span><span class="sxs-lookup"><span data-stu-id="3d6d1-147">15</span></span>     |
|             | <span data-ttu-id="3d6d1-148">Contoso India</span><span class="sxs-lookup"><span data-stu-id="3d6d1-148">Contoso India</span></span>|<span data-ttu-id="3d6d1-149">Local</span><span class="sxs-lookup"><span data-stu-id="3d6d1-149">Local</span></span>             |                    |<span data-ttu-id="3d6d1-150">Hores extra</span><span class="sxs-lookup"><span data-stu-id="3d6d1-150">Overtime</span></span>                 |<span data-ttu-id="3d6d1-151">10</span><span class="sxs-lookup"><span data-stu-id="3d6d1-151">10</span></span>     |
|             | <span data-ttu-id="3d6d1-152">Contoso EUA</span><span class="sxs-lookup"><span data-stu-id="3d6d1-152">Contoso US</span></span>   |<span data-ttu-id="3d6d1-153">Local</span><span class="sxs-lookup"><span data-stu-id="3d6d1-153">Local</span></span>             |                    |<span data-ttu-id="3d6d1-154">Hores extra</span><span class="sxs-lookup"><span data-stu-id="3d6d1-154">Overtime</span></span>                 |<span data-ttu-id="3d6d1-155">20</span><span class="sxs-lookup"><span data-stu-id="3d6d1-155">20</span></span>     |


<span data-ttu-id="3d6d1-156">Si un recurs de Contoso India la tarifa base del qual és 100 USD treballa in situ, i registra 8 hores de temps normal i 2 hores de temps extra a l'entrada de temps, el motor de preus del Project Service utilitzarà la tarifa base de 100 per a les 8 hores per registrar 800 USD.</span><span class="sxs-lookup"><span data-stu-id="3d6d1-156">If a resource from Contoso India whose base rate is 100 USD is working onsite, and they log 8 hours of Regular time and 2 hours of overtime on the time entry, the Project Service pricing engine will use the base rate of 100 for the 8 hours to record 800 USD.</span></span> <span data-ttu-id="3d6d1-157">Per a les 2 hores extres, s'aplicarà un marge comercial del 15% a la tarifa base de 100 per obtenir un preu d'unitat de 115 USD i registrarà un cost total de 230 USD.</span><span class="sxs-lookup"><span data-stu-id="3d6d1-157">For the 2 hours overtime, a markup of 15% will be applied to the base rate of 100 to get a unit price of 115 USD and will record a total cost of 230 USD.</span></span>

### <a name="applicable-to-cost"></a><span data-ttu-id="3d6d1-158">Aplicable al cost</span><span class="sxs-lookup"><span data-stu-id="3d6d1-158">Applicable to Cost</span></span> 
<span data-ttu-id="3d6d1-159">Si està definit com a **Sí**, indica que el valor de la dimensió del context d'entrada s'ha d'utilitzar per coincidir amb **Preu per funció** i **Marge comercial del preu per funció** quan es recuperen les tarifes de costos i marge comercial.</span><span class="sxs-lookup"><span data-stu-id="3d6d1-159">If this is set to **Yes**, it indicates that the dimension value from the input context should be used to match to the **Role Price** and **Role Price Markup** when retrieving the cost and markup rates.</span></span>

### <a name="applicable-to-sales"></a><span data-ttu-id="3d6d1-160">Aplicable a les vendes</span><span class="sxs-lookup"><span data-stu-id="3d6d1-160">Applicable to Sales</span></span>
<span data-ttu-id="3d6d1-161">Si està definit com a **Sí**, indica que el valor de la dimensió del context d'entrada s'ha d'utilitzar per coincidir amb **Preu per funció** i **Marge comercial del preu per funció** quan es recuperen les tarifes de facturació i marge comercial.</span><span class="sxs-lookup"><span data-stu-id="3d6d1-161">If this is set to **Yes**, it indicates that the dimension value from the input context should be used to match to the **Role Price** and **Role Price Markup** when retrieving the bill and markup rates.</span></span>

### <a name="applicable-to-purchase"></a><span data-ttu-id="3d6d1-162">Aplicable a les compres</span><span class="sxs-lookup"><span data-stu-id="3d6d1-162">Applicable to Purchase</span></span>
<span data-ttu-id="3d6d1-163">Si està definit com a **Sí**, indica que el valor de la dimensió del context d'entrada s'ha d'utilitzar per coincidir amb **Preu per funció** i **Marge comercial del preu per funció** quan es recupera el preu de compra.</span><span class="sxs-lookup"><span data-stu-id="3d6d1-163">If this is set to **Yes**, it indicates that the dimension value from the input context should be used to match to the **Role Price** and **Role Price Markup** when retrieving the purchase price.</span></span> <span data-ttu-id="3d6d1-164">El Project Service actualment no és compatible amb escenaris de subcontractació, de manera que aquest camp no s'utilitza.</span><span class="sxs-lookup"><span data-stu-id="3d6d1-164">Currently Project Service does not support subcontracting scenarios, so this field is not used.</span></span> 

### <a name="priority"></a><span data-ttu-id="3d6d1-165">Prioritat</span><span class="sxs-lookup"><span data-stu-id="3d6d1-165">Priority</span></span>
<span data-ttu-id="3d6d1-166">Definir la prioritat de dimensions ajuda que el Project Service produeixi un preu encara que no trobi una coincidència exacta entre els valors de la dimensió d'entrada i els valors de les taules **Preu per funció** o **Marge comercial del preu per funció**.</span><span class="sxs-lookup"><span data-stu-id="3d6d1-166">Setting the dimension priority helps Project Service pricing produce a price even when it can't find an exact match between the input dimension values and the values from the **Role Price** or **Role Price Markup** tables.</span></span> <span data-ttu-id="3d6d1-167">En aquest escenari, el Project Service utilitzarà valors nuls per als valors d'una dimensió no coincidents pesant les dimensions segons la seva prioritat.</span><span class="sxs-lookup"><span data-stu-id="3d6d1-167">In this scenario, Project Service will use null values for unmatched dimension values by weighing the dimensions in order of their priority.</span></span>

- <span data-ttu-id="3d6d1-168">**Prioritat de costos**: el valor d'una prioritat de costos d'una dimensió indicarà el pes d'aquesta dimensió el fer-la coincidir amb la configuració dels preus de cost.</span><span class="sxs-lookup"><span data-stu-id="3d6d1-168">**Cost Priority**: The value of a dimension's cost priority will indicate the weight of that dimension when matching against the setup of cost prices.</span></span> <span data-ttu-id="3d6d1-169">El valor de **Prioritat de cost** ha de ser únic en totes les dimensions **Aplicable al cost**.</span><span class="sxs-lookup"><span data-stu-id="3d6d1-169">The value of **Cost Priority** must be unique across dimensions that are **Applicable to Cost**.</span></span>
- <span data-ttu-id="3d6d1-170">**Prioritat de vendes**: el valor d'una prioritat de vendes d'una dimensió indicarà el pes d'aquesta dimensió el fer-la coincidir amb la configuració dels preus de vendes o tarifes de facturació.</span><span class="sxs-lookup"><span data-stu-id="3d6d1-170">**Sales Priority**: The value of dimension's sales priority will indicate the weight of that dimension when matching against the setup of sales prices or bill rates.</span></span> <span data-ttu-id="3d6d1-171">El valor de **Prioritat de vendes** ha de ser únic en totes les dimensions **Aplicable a les vendes**.</span><span class="sxs-lookup"><span data-stu-id="3d6d1-171">The value of **Sales Priority** must be unique across dimensions that are **Applicable to Sales**.</span></span>