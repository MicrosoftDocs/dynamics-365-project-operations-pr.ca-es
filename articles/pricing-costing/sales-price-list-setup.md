---
title: Configuració de la llista de preus de vendes
description: En aquest tema es proporciona informació sobre les llistes de preus de vendes per als preus del projecte.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 1d2c797b72666123eb0a18d2d0c1df9fe3d207f7
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072267"
---
# <a name="sales-price-list-setup"></a><span data-ttu-id="63c7b-103">Configuració de la llista de preus de vendes</span><span class="sxs-lookup"><span data-stu-id="63c7b-103">Sales price list setup</span></span>

<span data-ttu-id="63c7b-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_</span><span class="sxs-lookup"><span data-stu-id="63c7b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="63c7b-105">Per a les ofertes i els contractes del projecte, una llista de preus de projecte té un patró de substitució de preu diferent que una llista de preus de producte.</span><span class="sxs-lookup"><span data-stu-id="63c7b-105">For project quotes and contracts, a project price list has a different price override pattern than a product price list.</span></span> <span data-ttu-id="63c7b-106">En una línia d'oferta basada en un catàleg de productes, podeu substituir el preu a les funcions i a les categories directament a la línia d'oferta, perquè cada línia d'oferta apunta a exactament un element del catàleg.</span><span class="sxs-lookup"><span data-stu-id="63c7b-106">On a product catalog–based quote line, you can override the price to roles and categories directly on the quote line, because each quote line points to exactly one catalog item.</span></span> <span data-ttu-id="63c7b-107">Tanmateix, en una línia d'oferta basada en projectes, no podeu substituir el preu a les funcions i a les categories directament a la línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="63c7b-107">However, on a project-based quote line, you can't override the price to roles and categories directly on the quote line.</span></span> <span data-ttu-id="63c7b-108">Podeu utilitzar la llista de preus del projecte per treballar amb els dos patrons de substitució diferents.</span><span class="sxs-lookup"><span data-stu-id="63c7b-108">You can use the project price list to work with the two distinct override patterns.</span></span>

> [!NOTE]
> <span data-ttu-id="63c7b-109">Es recomana que tingueu una llista de preus separada per als recursos del projecte i per als elements del catàleg, a causa de les diferències de comportament entre les dues en substituir els preus.</span><span class="sxs-lookup"><span data-stu-id="63c7b-109">We recommend that you have a separate price list for your project resources and your catalog items, because of the behavior differences between the two when you override pricing.</span></span>

<span data-ttu-id="63c7b-110">Cadascuna de les entitats següents pot tenir una o diverses llistes de preus associades per a preus del projecte:</span><span class="sxs-lookup"><span data-stu-id="63c7b-110">Each of the following entities can have one or more associated sales price lists for project pricing:</span></span>

- <span data-ttu-id="63c7b-111">Client (compte)</span><span class="sxs-lookup"><span data-stu-id="63c7b-111">Customer (account)</span></span> 
- <span data-ttu-id="63c7b-112">Oportunitat</span><span class="sxs-lookup"><span data-stu-id="63c7b-112">Opportunity</span></span> 
- <span data-ttu-id="63c7b-113">Oferta</span><span class="sxs-lookup"><span data-stu-id="63c7b-113">Quote</span></span> 
- <span data-ttu-id="63c7b-114">Contracte de projecte</span><span class="sxs-lookup"><span data-stu-id="63c7b-114">Project Contract</span></span>

<span data-ttu-id="63c7b-115">L'associació d'aquestes entitats amb una llista de preus s'indica a les llistes de preus del projecte.</span><span class="sxs-lookup"><span data-stu-id="63c7b-115">The association of these entities with a price list is indicated by the project price lists.</span></span> <span data-ttu-id="63c7b-116">Podeu associar una o diverses llistes de preus amb les entitats de vendes Client, Oportunitat, Oferta i Contracte del projecte.</span><span class="sxs-lookup"><span data-stu-id="63c7b-116">You can associate one or more price lists with the Customer, Opportunity, Quote, and Project Contract sales entities.</span></span>

<span data-ttu-id="63c7b-117">Una llista de preus de projecte per defecte no s'introdueix automàticament en un registre de client.</span><span class="sxs-lookup"><span data-stu-id="63c7b-117">A default project price list isn't automatically entered on a customer record.</span></span> <span data-ttu-id="63c7b-118">No obstant, podeu adjuntar manualment una llista de preus de projecte al registre de client.</span><span class="sxs-lookup"><span data-stu-id="63c7b-118">However, you can manually attach a project price list to the customer record.</span></span> <span data-ttu-id="63c7b-119">De totes maneres, heu d'adjuntar manualment una llista de preus de projecte només quan tingueu un acord de preus personalitzat amb el client.</span><span class="sxs-lookup"><span data-stu-id="63c7b-119">Nevertheless, you should manually attach a project price list only when you have a custom pricing agreement with the customer.</span></span> 

<span data-ttu-id="63c7b-120">Quan una llista de preus de projecte s'adjunta a una entitat de vendes, es valida la següent informació:</span><span class="sxs-lookup"><span data-stu-id="63c7b-120">When a project price list is attached to a sales entity, the following information is validated:</span></span>

- <span data-ttu-id="63c7b-121">La llista de preus té un context de **Vendes**.</span><span class="sxs-lookup"><span data-stu-id="63c7b-121">The price list has a context of **Sales**.</span></span> 
- <span data-ttu-id="63c7b-122">La moneda de la llista de preus coincideix amb la moneda del client.</span><span class="sxs-lookup"><span data-stu-id="63c7b-122">The price list currency matches the customer currency.</span></span> 

<span data-ttu-id="63c7b-123">En un contracte de projecte, s'utilitza el següent ordre de precedència per definir automàticament les llistes de preus relacionades amb el projecte:</span><span class="sxs-lookup"><span data-stu-id="63c7b-123">On a project contract, the following order of precedence is used to automatically set related project price lists:</span></span>

1. <span data-ttu-id="63c7b-124">Oferta</span><span class="sxs-lookup"><span data-stu-id="63c7b-124">Quote</span></span>
2. <span data-ttu-id="63c7b-125">Oportunitat</span><span class="sxs-lookup"><span data-stu-id="63c7b-125">Opportunity</span></span>
3. <span data-ttu-id="63c7b-126">Client</span><span class="sxs-lookup"><span data-stu-id="63c7b-126">Customer</span></span> 
4. <span data-ttu-id="63c7b-127">Configuració global</span><span class="sxs-lookup"><span data-stu-id="63c7b-127">Global settings</span></span> 

<span data-ttu-id="63c7b-128">Quan una llista de preus de projecte s'introdueix per defecte, el sistema valida que la moneda coincideix amb la moneda del client i que les llistes de preus per defecte que s'han introduït tenen un context de **Vendes**.</span><span class="sxs-lookup"><span data-stu-id="63c7b-128">When a project price list is entered by default, the system validates that the currency matches the customer’s currency, and that the default price lists that have been entered have a context of **Sales**.</span></span>

<span data-ttu-id="63c7b-129">Podeu associar diverses llistes de preus amb les entitats Client, Oportunitat, Oferta i Contracte del projecte.</span><span class="sxs-lookup"><span data-stu-id="63c7b-129">You can associate multiple project price lists with the Customer, Opportunity, Quote, and Project Contract entities.</span></span> <span data-ttu-id="63c7b-130">Aquesta capacitat admet els preus per defecte específics d'una data per a un contracte de projecte de llarg termini, on podeu necessitar més d'una llista de preus per explicar les actualitzacions dels preus que es produeixen a causa de la inflació.</span><span class="sxs-lookup"><span data-stu-id="63c7b-130">This capability supports date-specific default prices for a long-running project contract, where you might require more than one price list to account for price updates that occur because of inflation.</span></span> <span data-ttu-id="63c7b-131">No obstant, si les llistes de preus que s'associen amb l'entitat Client, Oportunitat, Oferta o Contracte del projecte tenen una data d'efectivitat que se solapa, els preus per defecte podrien ser incorrectes.</span><span class="sxs-lookup"><span data-stu-id="63c7b-131">However, if the price lists that you associate with the Customer, Opportunity, Quote, or Project Contract entity have overlapping date effectivity, the default prices might be incorrect.</span></span> <span data-ttu-id="63c7b-132">Per tant, heu d'assegurar-vos que les llistes de preus de projecte que tenen una data d'efectivitat que se solapa no estan associades amb aquestes entitats.</span><span class="sxs-lookup"><span data-stu-id="63c7b-132">Therefore, you should make sure that project price lists that have overlapping date effectivity aren't associated with those entities.</span></span>
