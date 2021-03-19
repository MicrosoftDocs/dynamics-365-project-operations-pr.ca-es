---
title: Línies d'oferta basades en productes
description: En aquest tema es proporciona informació sobre les línies d'oferta basades en productes.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 8bde88f5f2d00c09129c6a9363c09f6f6ad1dd90
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5284076"
---
# <a name="product-based-quote-lines"></a><span data-ttu-id="f52a8-103">Línies d'oferta basades en productes</span><span class="sxs-lookup"><span data-stu-id="f52a8-103">Product-based quote lines</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


<span data-ttu-id="f52a8-104">Podeu crear línies d'oferta basades en productes al Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="f52a8-104">You can create product-based quote lines in Dynamics 365 Project Service Automation.</span></span> <span data-ttu-id="f52a8-105">Les línies d'oferta basades en productes poden ser línies fora del catàleg o poden ser elements del catàleg de productes.</span><span class="sxs-lookup"><span data-stu-id="f52a8-105">Product-based quote lines can be "write-in" lines, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="f52a8-106">Catàleg de productes</span><span class="sxs-lookup"><span data-stu-id="f52a8-106">Product catalog</span></span>

<span data-ttu-id="f52a8-107">Els productes d'un catàleg de productes del Dynamics 365 tenen una unitat i un grup d'unitats per defecte.</span><span class="sxs-lookup"><span data-stu-id="f52a8-107">The products in a Dynamics 365 product catalog have a default unit and unit group.</span></span> <span data-ttu-id="f52a8-108">Si diversos productes comparteixen el mateix conjunt d'atributs, podeu crear una família de productes que també tingui aquests atributs.</span><span class="sxs-lookup"><span data-stu-id="f52a8-108">If several products share the same set of attributes, you can create a product family that also has those attributes.</span></span> <span data-ttu-id="f52a8-109">Tots els productes d'una família de productes hereten el mateix conjunt d'atributs.</span><span class="sxs-lookup"><span data-stu-id="f52a8-109">All the products in one product family inherit the same set of attributes.</span></span>

<span data-ttu-id="f52a8-110">Per exemple, una empresa ven llicències de subscripció per a diversos programes.</span><span class="sxs-lookup"><span data-stu-id="f52a8-110">For example, a company sells subscription licenses for a variety of software.</span></span> <span data-ttu-id="f52a8-111">Tots els programes de subscripció tenen els dos atributs següents:</span><span class="sxs-lookup"><span data-stu-id="f52a8-111">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="f52a8-112">Nombre d'usuaris</span><span class="sxs-lookup"><span data-stu-id="f52a8-112">Number of users</span></span> 
- <span data-ttu-id="f52a8-113">Duració de la subscripció (en mesos)</span><span class="sxs-lookup"><span data-stu-id="f52a8-113">Subscription duration (in months)</span></span>

<span data-ttu-id="f52a8-114">Una bona manera de mantenir aquest tipus de catàleg és crear una família de productes que s'anomeni **Programari de subscripció** i que tingui **Nombre d'usuaris** i **Duració de la subscripció** com a atributs.</span><span class="sxs-lookup"><span data-stu-id="f52a8-114">A good way to maintain this type of catalog is to create a product family that is named **Subscription Software**, and that has **Number of users** and **Subscription duration** as attributes.</span></span> <span data-ttu-id="f52a8-115">A continuació, podeu afegir productes individuals, com ara el **Dynamics 365 Sales** o el **Dynamics 365 Field Service** a la família de productes **Programari de subscripció**.</span><span class="sxs-lookup"><span data-stu-id="f52a8-115">You can then add individual products, such as **Dynamics 365 Sales** or **Dynamics 365 Field Service** to the **Subscription Software** product family.</span></span>

## <a name="adding-product-catalog-items-to-a-project-quote"></a><span data-ttu-id="f52a8-116">Afegir elements del catàleg de productes a una oferta de projecte</span><span class="sxs-lookup"><span data-stu-id="f52a8-116">Adding product catalog items to a project quote</span></span>

<span data-ttu-id="f52a8-117">Les pàgines dels contractes d'oferta i de contractes de projecte tenen seccions per a dos tipus de línies: línies basades en el projecte i línies basades en productes.</span><span class="sxs-lookup"><span data-stu-id="f52a8-117">Project quote and project contract pages have sections for two types of lines: project-based lines and product-based lines.</span></span> <span data-ttu-id="f52a8-118">Per a les línies basades en productes, el Dynamics 365 s'utilitza per afegir elements d'un catàleg de productes a una oferta.</span><span class="sxs-lookup"><span data-stu-id="f52a8-118">For product-based lines, Dynamics 365 is used to add items from a product catalog to a quote.</span></span> <span data-ttu-id="f52a8-119">La llista desplegable de la línia d'oferta o de la línia de contracte de projecte inclou tots els productes i les unitats de la llista de preus de productes adjunta al contracte de l'oferta o del projecte.</span><span class="sxs-lookup"><span data-stu-id="f52a8-119">The drop-down list on the quote line or project contract line includes all the products and units in the product price list that is attached to the quote or project contract.</span></span> <span data-ttu-id="f52a8-120">També podeu afegir productes que no siguin part de la llista de preus de productes de l'oferta.</span><span class="sxs-lookup"><span data-stu-id="f52a8-120">You can also add products that aren't part of quote's product price list.</span></span>

<span data-ttu-id="f52a8-121">A més, podeu seleccionar productes d'altres llistes de preus o bé podeu seleccionar productes directament des del catàleg de productes.</span><span class="sxs-lookup"><span data-stu-id="f52a8-121">Additionally, you can select products from other price lists, or you can select products directly from the product catalog.</span></span> <span data-ttu-id="f52a8-122">En seleccionar productes directament des d'un catàleg de productes, la llista de preus per defecte d'aquest producte s'utilitza per obtenir el preu de venda del producte.</span><span class="sxs-lookup"><span data-stu-id="f52a8-122">When you select products directly from a product catalog, the default price list of that product is used to get the product's sales price.</span></span> <span data-ttu-id="f52a8-123">Si no es defineix una llista de preus per defecte, el preu es defineix com a 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="f52a8-123">If a default price list isn't set, the price is set to 0 (zero).</span></span>

<span data-ttu-id="f52a8-124">Si una línia d'oferta es basa en un catàleg de productes, podeu substituir el preu de venda directament a la línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="f52a8-124">If a quote line is based on a product catalog, you can override the sales price directly on the quote line.</span></span> <span data-ttu-id="f52a8-125">Heu de tenir en compte que una línia d'oferta del Dynamics 365 té un camp **Preu**.</span><span class="sxs-lookup"><span data-stu-id="f52a8-125">Note that a quote line in Dynamics 365 has a **Pricing** field.</span></span> <span data-ttu-id="f52a8-126">Hi ha dos valors disponibles:</span><span class="sxs-lookup"><span data-stu-id="f52a8-126">Two values are available:</span></span>

- <span data-ttu-id="f52a8-127">Substitueix el preu</span><span class="sxs-lookup"><span data-stu-id="f52a8-127">Override pricing</span></span>  
- <span data-ttu-id="f52a8-128">Utilitza el valor per defecte</span><span class="sxs-lookup"><span data-stu-id="f52a8-128">Use default</span></span>

<span data-ttu-id="f52a8-129">Si definiu aquest camp com a **Substitueix el preu**, el Dynamics 365 no configura cap preu per defecte.</span><span class="sxs-lookup"><span data-stu-id="f52a8-129">If you set this field to **Override pricing**, Dynamics 365 doesn't set a default price.</span></span> <span data-ttu-id="f52a8-130">Heu d'introduir un preu per al producte a la línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="f52a8-130">You must enter a price for the product on the quote line.</span></span> <span data-ttu-id="f52a8-131">Si definiu aquest camp com a **Utilitza els valors per defecte**, el Dynamics 365 utilitza el preu de vendes per defecte i bloca el camp per evitar l'edició.</span><span class="sxs-lookup"><span data-stu-id="f52a8-131">If you set this field to **Use default**, Dynamics 365 uses the default sales price and locks the field to prevent editing.</span></span>

<span data-ttu-id="f52a8-132">Després d'instal·lar el PSA, els preus de vendes per defecte s'introdueixen a les línies basades en productes en una oferta.</span><span class="sxs-lookup"><span data-stu-id="f52a8-132">After you install PSA, default sales prices are entered on the product-based lines on a quote.</span></span> <span data-ttu-id="f52a8-133">El camp **Preu** es defineix com a **Substitueix el preu** per tal que pugueu editar el preu per defecte a les línies d'oferta.</span><span class="sxs-lookup"><span data-stu-id="f52a8-133">The **Pricing** field is then set to **Override pricing** so that you can edit the default price on the quote lines.</span></span>

> ![Definir la substitució del preu](media/basic-guide-10.png)
 
## <a name="quantity-factors-for-products"></a><span data-ttu-id="f52a8-135">Factors de quantitat per a productes</span><span class="sxs-lookup"><span data-stu-id="f52a8-135">Quantity factors for products</span></span>

<span data-ttu-id="f52a8-136">El PSA utilitza factors de quantitat per admetre la venda de productes basats en subscripcions.</span><span class="sxs-lookup"><span data-stu-id="f52a8-136">PSA uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="f52a8-137">Per als productes basats en subscripcions, la quantitat de l'oferta o la línia de contracte del projecte s'expressa com el nombre de mesos d'usuari.</span><span class="sxs-lookup"><span data-stu-id="f52a8-137">For subscription-based products, the quantity on the quote or project contract line is expressed as the number of user months.</span></span>

<span data-ttu-id="f52a8-138">Normalment, el preu del programari de subscripció s'emmagatzema al catàleg com el preu per usuari i per mes.</span><span class="sxs-lookup"><span data-stu-id="f52a8-138">Usually, the price of subscription software is stored in the catalog as the price per user per month.</span></span> <span data-ttu-id="f52a8-139">Tanmateix, podeu utilitzar altres descripcions de temps en el seu lloc.</span><span class="sxs-lookup"><span data-stu-id="f52a8-139">However, you can use other time descriptions instead.</span></span> <span data-ttu-id="f52a8-140">Durant el procés de vendes, el preu de la línia d'oferta sol ser el preu per usuari per mes que ha estat negociat i descomptat per l'agent de vendes de TI.</span><span class="sxs-lookup"><span data-stu-id="f52a8-140">During the sales process, the price on the quote line is usually the per-user, per-month price that was negotiated and discounted by the IT sales agent.</span></span> <span data-ttu-id="f52a8-141">Cada operació té un nombre diferent d'usuaris i un nombre diferent de mesos de subscripció.</span><span class="sxs-lookup"><span data-stu-id="f52a8-141">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="f52a8-142">La quantitat que s'utilitza per calcular la quantitat de la línia d'oferta és un producte del nombre d'usuaris i el nombre de mesos de subscripció.</span><span class="sxs-lookup"><span data-stu-id="f52a8-142">The quantity that is used to compute the amount of the quote line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="f52a8-143">Per admetre aquest tipus de venda, el PSA ha introduït el concepte de factors de quantitat.</span><span class="sxs-lookup"><span data-stu-id="f52a8-143">To support this type of sale, PSA introduced the concept of quantity factors.</span></span> <span data-ttu-id="f52a8-144">Els factors de quantitat depenen dels atributs de producte al Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="f52a8-144">Quantity factors rely on the product attributes in Dynamics 365.</span></span> <span data-ttu-id="f52a8-145">Quan configureu propietats específiques per a un producte, el PSA us permet marcar un subconjunt d'aquestes propietats, o bé totes les propietats, com a factors de quantitat.</span><span class="sxs-lookup"><span data-stu-id="f52a8-145">When you configure specific properties for a product, PSA lets you flag a subset of those properties, or all the properties, as quantity factors.</span></span>

<span data-ttu-id="f52a8-146">El PSA valida que només les propietats numèriques o les propietats dels productes que tenen un tipus de dades numèric es marquen com a factors de quantitat.</span><span class="sxs-lookup"><span data-stu-id="f52a8-146">PSA validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="f52a8-147">Quan un producte amb factors de quantitat configurats s'afegeix a una línia d'oferta, el camp **Quantitat** de la línia d'oferta es converteix en un camp de només de lectura.</span><span class="sxs-lookup"><span data-stu-id="f52a8-147">When a product that quantity factors are configured for is added to a quote line, the **Quantity** field on the quote line becomes a read-only field.</span></span> <span data-ttu-id="f52a8-148">Després d'introduir els valors per a les propietats dels productes que són factors de quantitat, el PSA calcula la quantitat de la línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="f52a8-148">After you enter values for product properties that are quantity factors, PSA computes the quantity of the quote line.</span></span>

<span data-ttu-id="f52a8-149">Per exemple, el Dynamics 365 pot tenir les propietats següents:</span><span class="sxs-lookup"><span data-stu-id="f52a8-149">For example, Dynamics 365 might have the following properties:</span></span> 

- <span data-ttu-id="f52a8-150">**Nombre d'usuaris**: el nombre d'usuaris</span><span class="sxs-lookup"><span data-stu-id="f52a8-150">**No of users** - The number of users</span></span> 
- <span data-ttu-id="f52a8-151">**Nombre de mesos**: el nombre de mesos de subscripció</span><span class="sxs-lookup"><span data-stu-id="f52a8-151">**No of Months** - The number of subscription months</span></span>
- <span data-ttu-id="f52a8-152">**SKU de producte**</span><span class="sxs-lookup"><span data-stu-id="f52a8-152">**Product SKU**</span></span> 

<span data-ttu-id="f52a8-153">Les propietats **Nombre d'usuaris** i **Nombre de mesos** es poden marcar com a factors de quantitat per editar les propietats de la línia de productes.</span><span class="sxs-lookup"><span data-stu-id="f52a8-153">Tne **No of Users** and **No of Months** properties can be flagged as quantity factors by editing the properties of the product line.</span></span> 

> ![Marcar Nombre d'usuaris i Nombre de mesos com a factors de qualitat](media/basic-guide-11.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]