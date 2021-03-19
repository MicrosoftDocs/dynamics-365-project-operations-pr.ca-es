---
title: Configuració de les tarifes de cost i de vendes per als productes del catàleg (bàsic)
description: Aquest tema proporciona informació sobre com configurar els costos i les tarifes de venda dels articles en un catàleg de productes.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f0941c549cc38f0938a5819e8cb6ca9912f14790
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274446"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a><span data-ttu-id="a6c19-103">Configuració de les tarifes de cost i de vendes per als productes del catàleg (bàsic)</span><span class="sxs-lookup"><span data-stu-id="a6c19-103">Set up cost and sales rates for catalog products - lite</span></span>

<span data-ttu-id="a6c19-104">_**S'aplica a:** implementació bàsica: tracte de facturació proforma_</span><span class="sxs-lookup"><span data-stu-id="a6c19-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="a6c19-105">La configuració de preus dels elements del catàleg de productes del Dynamics 365 Project Operations és la mateixa que al Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="a6c19-105">Setting up pricing for product catalog items in Dynamics 365 Project Operations is the same as in Dynamics 365 Sales.</span></span>

<span data-ttu-id="a6c19-106">Al Project Operations, els productes no es poden calcular ni utilitzar en els projectes, de manera que els preus del catàleg de productes no s'han de definir a les llistes de preus del projecte per a les ofertes i els contractes.</span><span class="sxs-lookup"><span data-stu-id="a6c19-106">In Project Operations, products can't be estimated or used on projects, so product catalog prices don't need to be set on project price lists for quotes and contracts.</span></span>

<span data-ttu-id="a6c19-107">Utilitzeu el camp **Preu del producte** d'una oferta, un contracte o un compte per configurar els preus del catàleg de productes.</span><span class="sxs-lookup"><span data-stu-id="a6c19-107">Use the **Product Price** field of a quote, contract, or account to set up product catalog prices.</span></span> <span data-ttu-id="a6c19-108">No configureu els preus del catàleg de productes a les llistes de preus del projecte.</span><span class="sxs-lookup"><span data-stu-id="a6c19-108">Don't set up product catalog prices in the project price lists.</span></span> <span data-ttu-id="a6c19-109">Les llistes de preus del projecte són exclusives del Project Operations.</span><span class="sxs-lookup"><span data-stu-id="a6c19-109">Project price lists are exclusive to Project Operations.</span></span> <span data-ttu-id="a6c19-110">La lògica empresarial específica de l'aplicació copia les llistes de preus d'una oferta a un contracte.</span><span class="sxs-lookup"><span data-stu-id="a6c19-110">Application-specific business logic copies the price lists from a quote to a contract.</span></span> <span data-ttu-id="a6c19-111">El resultat és una llista de preus de projecte específica per al contracte.</span><span class="sxs-lookup"><span data-stu-id="a6c19-111">The result is a contract-specific project price list.</span></span> <span data-ttu-id="a6c19-112">L'operació de còpia pot retardar el procés de guanyar l'oferta si la llista de preus del projecte de l'oferta es fa massa gran.</span><span class="sxs-lookup"><span data-stu-id="a6c19-112">The copy operation can delay the quote win process if the project price list on the quote gets too large.</span></span> <span data-ttu-id="a6c19-113">Les llistes de preus del producte no es copien per crear llistes de preus personalitzades en els contractes.</span><span class="sxs-lookup"><span data-stu-id="a6c19-113">Product price lists aren't copied to create custom price lists on contracts.</span></span> <span data-ttu-id="a6c19-114">Com que no hi ha cap còpia involucrada, el rendiment del procés d'oferta no està afectat.</span><span class="sxs-lookup"><span data-stu-id="a6c19-114">Because there's no copying involved, the performance of the quote process isn't affected.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]