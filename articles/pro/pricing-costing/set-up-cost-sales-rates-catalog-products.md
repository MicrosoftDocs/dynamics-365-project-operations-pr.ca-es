---
title: Configuració de les tarifes de cost i de vendes per als productes del catàleg (bàsic)
description: Aquest tema proporciona informació sobre com configurar els costos i les tarifes de venda dels articles en un catàleg de productes.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4995859696c844e99593139f63dffbf86a52f2f0
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004299"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a><span data-ttu-id="30311-103">Configuració de les tarifes de cost i de vendes per als productes del catàleg (bàsic)</span><span class="sxs-lookup"><span data-stu-id="30311-103">Set up cost and sales rates for catalog products - lite</span></span>

<span data-ttu-id="30311-104">_**S'aplica a:** implementació bàsica: tracte de facturació proforma_</span><span class="sxs-lookup"><span data-stu-id="30311-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="30311-105">La configuració de preus dels elements del catàleg de productes del Dynamics 365 Project Operations és la mateixa que al Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="30311-105">Setting up pricing for product catalog items in Dynamics 365 Project Operations is the same as in Dynamics 365 Sales.</span></span>

<span data-ttu-id="30311-106">Al Project Operations, els productes no es poden calcular ni utilitzar en els projectes, de manera que els preus del catàleg de productes no s'han de definir a les llistes de preus del projecte per a les ofertes i els contractes.</span><span class="sxs-lookup"><span data-stu-id="30311-106">In Project Operations, products can't be estimated or used on projects, so product catalog prices don't need to be set on project price lists for quotes and contracts.</span></span>

<span data-ttu-id="30311-107">Utilitzeu el camp **Preu del producte** d'una oferta, un contracte o un compte per configurar els preus del catàleg de productes.</span><span class="sxs-lookup"><span data-stu-id="30311-107">Use the **Product Price** field of a quote, contract, or account to set up product catalog prices.</span></span> <span data-ttu-id="30311-108">No configureu els preus del catàleg de productes a les llistes de preus del projecte.</span><span class="sxs-lookup"><span data-stu-id="30311-108">Don't set up product catalog prices in the project price lists.</span></span> <span data-ttu-id="30311-109">Les llistes de preus del projecte són exclusives del Project Operations.</span><span class="sxs-lookup"><span data-stu-id="30311-109">Project price lists are exclusive to Project Operations.</span></span> <span data-ttu-id="30311-110">La lògica empresarial específica de l'aplicació copia les llistes de preus d'una oferta a un contracte.</span><span class="sxs-lookup"><span data-stu-id="30311-110">Application-specific business logic copies the price lists from a quote to a contract.</span></span> <span data-ttu-id="30311-111">El resultat és una llista de preus de projecte específica per al contracte.</span><span class="sxs-lookup"><span data-stu-id="30311-111">The result is a contract-specific project price list.</span></span> <span data-ttu-id="30311-112">L'operació de còpia pot retardar el procés de guanyar l'oferta si la llista de preus del projecte de l'oferta es fa massa gran.</span><span class="sxs-lookup"><span data-stu-id="30311-112">The copy operation can delay the quote win process if the project price list on the quote gets too large.</span></span> <span data-ttu-id="30311-113">Les llistes de preus del producte no es copien per crear llistes de preus personalitzades en els contractes.</span><span class="sxs-lookup"><span data-stu-id="30311-113">Product price lists aren't copied to create custom price lists on contracts.</span></span> <span data-ttu-id="30311-114">Com que no hi ha cap còpia involucrada, el rendiment del procés d'oferta no està afectat.</span><span class="sxs-lookup"><span data-stu-id="30311-114">Because there's no copying involved, the performance of the quote process isn't affected.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]