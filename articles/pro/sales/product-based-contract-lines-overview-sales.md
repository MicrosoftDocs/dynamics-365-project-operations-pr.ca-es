---
title: Informació general de les línies de contracte basades en productes (bàsic)
description: En aquest tema es proporciona informació sobre les línies de contracte basades en productes.
author: rumant
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6e9ef33cc9c79f828e85733f4f5a199bce842700
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272646"
---
# <a name="product-based-contract-lines-overview---lite"></a><span data-ttu-id="f7adb-103">Informació general de les línies de contracte basades en productes (bàsic)</span><span class="sxs-lookup"><span data-stu-id="f7adb-103">Product-based contract lines overview - lite</span></span>

<span data-ttu-id="f7adb-104">_**S'aplica a:** implementació bàsica: tracte de facturació proforma_</span><span class="sxs-lookup"><span data-stu-id="f7adb-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f7adb-105">Podeu crear línies de contracte basades en productes al Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="f7adb-105">You can create product-based contract lines in Dynamics 365 Project Operations.</span></span> <span data-ttu-id="f7adb-106">Les línies de contracte basades en productes es poden crear manualment o poden ser articles del catàleg de productes.</span><span class="sxs-lookup"><span data-stu-id="f7adb-106">Product-based contract lines can be manually created lines, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="f7adb-107">Catàleg de productes</span><span class="sxs-lookup"><span data-stu-id="f7adb-107">Product catalog</span></span>

<span data-ttu-id="f7adb-108">Els productes del catàleg de productes tenen una unitat i un grup d'unitats per defecte.</span><span class="sxs-lookup"><span data-stu-id="f7adb-108">The products in the product catalog have a default unit and unit group.</span></span> <span data-ttu-id="f7adb-109">Si diversos productes comparteixen el mateix conjunt d'atributs, podeu crear una família de productes que també tingui aquests atributs.</span><span class="sxs-lookup"><span data-stu-id="f7adb-109">If several products share the same set of attributes, you can create a product family that also has those attributes.</span></span> <span data-ttu-id="f7adb-110">Tots els productes d'una família de productes hereten el mateix conjunt d'atributs.</span><span class="sxs-lookup"><span data-stu-id="f7adb-110">All the products in one product family inherit the same set of attributes.</span></span>

<span data-ttu-id="f7adb-111">Per exemple, una empresa ven llicències de subscripció per a diversos tipus de programes.</span><span class="sxs-lookup"><span data-stu-id="f7adb-111">For example, a company sells subscription licenses for different kinds of software.</span></span> <span data-ttu-id="f7adb-112">Tots els programes de subscripció tenen els dos atributs següents:</span><span class="sxs-lookup"><span data-stu-id="f7adb-112">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="f7adb-113">Nombre d'usuaris</span><span class="sxs-lookup"><span data-stu-id="f7adb-113">Number of users</span></span>
- <span data-ttu-id="f7adb-114">Duració de la subscripció (en mesos)</span><span class="sxs-lookup"><span data-stu-id="f7adb-114">Subscription duration (in months)</span></span>

<span data-ttu-id="f7adb-115">Per mantenir aquest tipus de catàleg, creeu una família de productes que s'anomeni **Programari de subscripció**.</span><span class="sxs-lookup"><span data-stu-id="f7adb-115">To maintain this type of catalog, create a product family that is named **Subscription Software**.</span></span> <span data-ttu-id="f7adb-116">Afegiu els atributs **Nombre d'usuaris** i **Duració de la subscripció** a la família de productes.</span><span class="sxs-lookup"><span data-stu-id="f7adb-116">Add the attributes, **Number of users** and **Subscription duration** to the product family.</span></span> <span data-ttu-id="f7adb-117">A continuació, afegiu productes individuals a la família de productes **Programari de subscripció**.</span><span class="sxs-lookup"><span data-stu-id="f7adb-117">Then, add individual products to the **Subscription Software** product family.</span></span>

## <a name="add-product-catalog-items-to-a-project-contract"></a><span data-ttu-id="f7adb-118">Afegir elements del catàleg de productes a un contracte de projecte</span><span class="sxs-lookup"><span data-stu-id="f7adb-118">Add product catalog items to a project Contract</span></span>

<span data-ttu-id="f7adb-119">Els contractes de projectes tenen seccions per a dos tipus de línies, basades en projectes i basades en productes.</span><span class="sxs-lookup"><span data-stu-id="f7adb-119">Project contracts have sections for two types of lines, project-based and product-based.</span></span> <span data-ttu-id="f7adb-120">Les línies basades en productes inclouen tots els productes i unitats de la llista de preus de producte del contracte.</span><span class="sxs-lookup"><span data-stu-id="f7adb-120">Product-based lines include all of the products and units in the product price list on the contract.</span></span> <span data-ttu-id="f7adb-121">Es poden afegir productes que no formen part de la llista de preus de productes del contracte.</span><span class="sxs-lookup"><span data-stu-id="f7adb-121">Products that aren't part of contract's product price list can be added.</span></span>

<span data-ttu-id="f7adb-122">Podeu seleccionar productes d'altres llistes de preus o directament del catàleg de productes.</span><span class="sxs-lookup"><span data-stu-id="f7adb-122">You can select products from other price lists, or directly from the product catalog.</span></span> <span data-ttu-id="f7adb-123">En seleccionar productes directament des d'un catàleg de productes, la llista de preus per defecte d'aquest producte s'utilitza per obtenir el preu de venda del producte.</span><span class="sxs-lookup"><span data-stu-id="f7adb-123">When you select products directly from a product catalog, the default price list of that product is used for the product's sales price.</span></span> <span data-ttu-id="f7adb-124">Si no es defineix una llista de preus per defecte, el preu es defineix com a 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="f7adb-124">If a default price list isn't set, the price is set to 0 (zero).</span></span>

<span data-ttu-id="f7adb-125">Si una línia de contracte es basa en un catàleg de productes, podeu substituir el preu de venda directament a la línia de contracte.</span><span class="sxs-lookup"><span data-stu-id="f7adb-125">If a contract line is based on a product catalog, you can override the sales price directly on the line.</span></span> <span data-ttu-id="f7adb-126">Una línia de contracte té el camp **Preu** amb els dos valors:</span><span class="sxs-lookup"><span data-stu-id="f7adb-126">A contract line has the **Pricing** field with the two values:</span></span>

- <span data-ttu-id="f7adb-127">**Substitueix el preu**</span><span class="sxs-lookup"><span data-stu-id="f7adb-127">**Override pricing**</span></span>
- <span data-ttu-id="f7adb-128">**Utilitza el valor per defecte**</span><span class="sxs-lookup"><span data-stu-id="f7adb-128">**Use default**</span></span>

<span data-ttu-id="f7adb-129">Si establiu el camp **Preu** a **Substitueix el preu**, el preu per defecte no està establert.</span><span class="sxs-lookup"><span data-stu-id="f7adb-129">If you set the **Pricing** field to **Override pricing**, the default price isn't set.</span></span> <span data-ttu-id="f7adb-130">Introduïu un preu per al producte en la línia de contracte.</span><span class="sxs-lookup"><span data-stu-id="f7adb-130">Enter a price for the product on the contract line.</span></span> <span data-ttu-id="f7adb-131">Si establiu el camp a **Utilitza el valor per defecte**, el preu de venda per defecte s'utilitza i el camp no es pot editar.</span><span class="sxs-lookup"><span data-stu-id="f7adb-131">If you set the field to **Use default**, the default sales price is used and the field can't be edited.</span></span>

<span data-ttu-id="f7adb-132">Després d'instal·lar el Project Operations, els preus de vendes per defecte s'introdueixen a les línies basades en productes en un contracte.</span><span class="sxs-lookup"><span data-stu-id="f7adb-132">After you install Project Operations, default sales prices are entered on the product-based lines on a contract.</span></span> <span data-ttu-id="f7adb-133">El camp **Preu** es defineix com a **Substitueix el preu** per tal que pugueu editar el preu per defecte a les línies de contracte.</span><span class="sxs-lookup"><span data-stu-id="f7adb-133">The **Pricing** field is set to **Override pricing** so that you can edit the default price on the contract lines.</span></span> <span data-ttu-id="f7adb-134">Aquesta és una substitució específica del Project Operations per al comportament de línies basades en productes al Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="f7adb-134">This is a Project Operations-specific override to product-based lines behavior in Dynamics 365 Sales.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]