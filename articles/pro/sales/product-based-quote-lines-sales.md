---
title: Informació general de les línies d'oferta basades en productes (bàsic)
description: Aquest tema proporciona informació sobre com treballar amb línies d'oferta basades en productes.
author: rumant
ms.date: 10/30/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5cc3a97194e01b14de054a93a6268c1f0c24bc25
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994439"
---
# <a name="product-based-quote-lines-overview---lite"></a><span data-ttu-id="9fa32-103">Informació general de les línies d'oferta basades en productes (bàsic)</span><span class="sxs-lookup"><span data-stu-id="9fa32-103">Product-based quote lines overview - lite</span></span>

<span data-ttu-id="9fa32-104">_**S'aplica a:** implementació bàsica: tracte de facturació proforma_</span><span class="sxs-lookup"><span data-stu-id="9fa32-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="9fa32-105">Podeu crear línies d'oferta basades en productes al Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="9fa32-105">You can create product-based quote lines in Dynamics 365 Project Operations.</span></span> <span data-ttu-id="9fa32-106">Les línies d'oferta basades en productes poden afegir-se manualment o poden ser elements del catàleg de productes.</span><span class="sxs-lookup"><span data-stu-id="9fa32-106">Product-based quote lines can be manually added, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="9fa32-107">Catàleg de productes</span><span class="sxs-lookup"><span data-stu-id="9fa32-107">Product catalog</span></span>

<span data-ttu-id="9fa32-108">Cada producte del catàleg de productes té una unitat i un grup d'unitats per defecte.</span><span class="sxs-lookup"><span data-stu-id="9fa32-108">Each product in the product catalog has a default unit and unit group.</span></span> <span data-ttu-id="9fa32-109">Si diversos productes comparteixen el mateix conjunt d'atributs, podeu crear una família de productes que comparteixi aquests atributs.</span><span class="sxs-lookup"><span data-stu-id="9fa32-109">If multiple products share the same set of attributes, you can create a product family that share those attributes.</span></span> 

<span data-ttu-id="9fa32-110">Per exemple, una empresa ven llicències de subscripció per a diversos tipus de programes.</span><span class="sxs-lookup"><span data-stu-id="9fa32-110">For example, a company sells subscription licenses for different kinds of software.</span></span> <span data-ttu-id="9fa32-111">Tots els programes de subscripció tenen els dos atributs següents:</span><span class="sxs-lookup"><span data-stu-id="9fa32-111">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="9fa32-112">Nombre d'usuaris</span><span class="sxs-lookup"><span data-stu-id="9fa32-112">Number of users</span></span>
- <span data-ttu-id="9fa32-113">Duració de la subscripció mesurada en mesos</span><span class="sxs-lookup"><span data-stu-id="9fa32-113">A subscription duration measured in months</span></span>

<span data-ttu-id="9fa32-114">Per mantenir aquest tipus de catàleg, creeu una família de productes que s'anomeni **Programari de subscripció** i afegiu el nombre d'usuaris i la duració de la subscripció com a atributs.</span><span class="sxs-lookup"><span data-stu-id="9fa32-114">To maintain this type of catalog, create a product family named **Subscription Software** and add the number of users and the subscription duration as attributes.</span></span> <span data-ttu-id="9fa32-115">A continuació, podeu afegir productes individuals a la família de productes **Programari de subscripció**.</span><span class="sxs-lookup"><span data-stu-id="9fa32-115">Next, you can add individual products to the **Subscription Software** product family.</span></span>

## <a name="add-product-catalog-items-to-a-project-quote"></a><span data-ttu-id="9fa32-116">Afegir elements del catàleg de productes a una oferta de projecte</span><span class="sxs-lookup"><span data-stu-id="9fa32-116">Add product catalog items to a project quote</span></span>

<span data-ttu-id="9fa32-117">Les pàgines **Oferta del projecte** i **Contracte del projecte** tenen seccions per a línies basades en el projecte i línies basades en productes.</span><span class="sxs-lookup"><span data-stu-id="9fa32-117">The **Project Quote** and **Project Contract** pages have sections for project-based lines and product-based lines.</span></span> <span data-ttu-id="9fa32-118">Per a les línies basades en productes, la llista desplegable de la línia d'oferta o de la línia de contracte de projecte inclou tots els productes i les unitats de la llista de preus de productes.</span><span class="sxs-lookup"><span data-stu-id="9fa32-118">For product-based lines, the drop-down list on the quote line or project contract line includes all the products and units in the product price list.</span></span> <span data-ttu-id="9fa32-119">També podeu afegir productes que no siguin part de la llista de preus de productes.</span><span class="sxs-lookup"><span data-stu-id="9fa32-119">You can also add products that aren't part of the product price list.</span></span>

<span data-ttu-id="9fa32-120">A més, podeu seleccionar productes d'altres llistes de preus o directament des del catàleg de productes.</span><span class="sxs-lookup"><span data-stu-id="9fa32-120">Additionally, you can select products from other price lists or directly from the product catalog.</span></span> <span data-ttu-id="9fa32-121">En seleccionar productes directament des d'un catàleg de productes, la llista de preus per defecte d'aquest producte s'utilitza per obtenir el preu de venda del producte.</span><span class="sxs-lookup"><span data-stu-id="9fa32-121">When you select products directly from a product catalog, the default price list of that product is used to get the product's sales price.</span></span> <span data-ttu-id="9fa32-122">Si no es defineix una llista de preus per defecte, el preu es defineix com a zero (0).</span><span class="sxs-lookup"><span data-stu-id="9fa32-122">If a default price list isn't set, the price is set to zero (0).</span></span>

<span data-ttu-id="9fa32-123">Si una línia d'oferta es basa en un catàleg de productes, podeu substituir el preu de venda directament a la línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="9fa32-123">When a quote line is based on a product catalog, you can override the sales price directly on the quote line.</span></span> <span data-ttu-id="9fa32-124">Una línia d'oferta al camp **Preus** amb dos valors disponibles:</span><span class="sxs-lookup"><span data-stu-id="9fa32-124">A quote line in **Pricing** field with two available values:</span></span>

- <span data-ttu-id="9fa32-125">**Substitueix el preu**</span><span class="sxs-lookup"><span data-stu-id="9fa32-125">**Override Pricing**</span></span>
- <span data-ttu-id="9fa32-126">**Opcions per defecte**</span><span class="sxs-lookup"><span data-stu-id="9fa32-126">**Use Default**</span></span>

<span data-ttu-id="9fa32-127">Si seleccioneu **Substitueix el preu**, el preu per defecte no està definit.</span><span class="sxs-lookup"><span data-stu-id="9fa32-127">If you select **Override Pricing**, the default price isn't set.</span></span> <span data-ttu-id="9fa32-128">En comptes d'això, heu d'introduir un preu per al producte a la línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="9fa32-128">Instead, you must enter a price for the product on the quote line.</span></span> <span data-ttu-id="9fa32-129">Si seleccioneu **Utilitza el valor per defecte**, s'utilitzarà el preu de venda per defecte i el camp no es podrà editar.</span><span class="sxs-lookup"><span data-stu-id="9fa32-129">If you select **Use Default**, the default sales price is used and the field is locked for editing.</span></span>

<span data-ttu-id="9fa32-130">Els preus de vendes per defecte s'introdueixen a les línies basades en productes en una oferta.</span><span class="sxs-lookup"><span data-stu-id="9fa32-130">Default sales prices are entered on the product-based lines of a quote.</span></span> <span data-ttu-id="9fa32-131">El camp **Preu** es defineix com a **Substitueix el preu** per tal que pugueu editar el preu per defecte a les línies d'oferta.</span><span class="sxs-lookup"><span data-stu-id="9fa32-131">The **Pricing** field is then set to **Override Pricing** so that you can edit the default price on the quote lines.</span></span> <span data-ttu-id="9fa32-132">Es tracta d'una substitució específica del Project Operations per al comportament de les línies basades en productes al Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="9fa32-132">This is a Project Operations-specific override to the product-based lines behavior in Dynamics 365 Sales.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]