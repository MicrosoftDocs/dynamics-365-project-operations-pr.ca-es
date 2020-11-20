---
title: Configuració de les tarifes de cost i de vendes per als productes del catàleg (bàsic)
description: Aquest tema proporciona informació sobre com configurar els costos i les tarifes de venda dels articles en un catàleg de productes.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 135b182af73bdab7a3520589431332ad059ec497
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176689"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a><span data-ttu-id="5a49c-103">Configuració de les tarifes de cost i de vendes per als productes del catàleg (bàsic)</span><span class="sxs-lookup"><span data-stu-id="5a49c-103">Set up cost and sales rates for catalog products - lite</span></span>

<span data-ttu-id="5a49c-104">_**S'aplica a:** implementació bàsica: tracte de facturació proforma_</span><span class="sxs-lookup"><span data-stu-id="5a49c-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="5a49c-105">La configuració de preus per als articles del catàleg de productes al Dynamics 365 Project Operations és la mateixa que al Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="5a49c-105">Setting up pricing for product catalog items in Dynamics 365 Project Operations is the same as in Dynamics 365 Sales.</span></span>

<span data-ttu-id="5a49c-106">Com que els productes no es poden estimar o utilitzar en projectes del Project Operations no hi ha necessitat d'establir preus de catàleg de producte en llistes de preus de projecte per a les ofertes i els contractes.</span><span class="sxs-lookup"><span data-stu-id="5a49c-106">Because products can't be estimated or used on projects in Project Operations, there is no need to set product catalog prices on project price lists for quotes and contracts.</span></span>

<span data-ttu-id="5a49c-107">Els preus del catàleg de productes s'han d'establir en el camp **Preu de producte** d'una oferta, contracte o compte.</span><span class="sxs-lookup"><span data-stu-id="5a49c-107">Product catalog prices should be set up in the **Product Price** field of a quote, contract, or account.</span></span> <span data-ttu-id="5a49c-108">No configureu els preus del catàleg de productes a les llistes de preus del projecte per a aquestes entitats.</span><span class="sxs-lookup"><span data-stu-id="5a49c-108">Don't set up product catalog prices in the project price lists for these entities.</span></span> <span data-ttu-id="5a49c-109">Les llistes de preus del projecte són exclusives del Project Operations.</span><span class="sxs-lookup"><span data-stu-id="5a49c-109">Project price lists are exclusive to Project Operations.</span></span> <span data-ttu-id="5a49c-110">Hi ha una lògica empresarial específica de l'aplicació que copia les llistes de preus d'una oferta a un contracte.</span><span class="sxs-lookup"><span data-stu-id="5a49c-110">There is application-specific business logic that copies the price lists from a quote to a contract.</span></span> <span data-ttu-id="5a49c-111">El resultat és una llista de preus de projecte específica per al contracte.</span><span class="sxs-lookup"><span data-stu-id="5a49c-111">The result is a contract-specific project price list.</span></span> <span data-ttu-id="5a49c-112">L'operació de còpia pot retardar el procés de guanyar l'oferta si la llista de preus del projecte de l'oferta es fa massa gran.</span><span class="sxs-lookup"><span data-stu-id="5a49c-112">The copy operation can delay the quote win process if the project price list on the quote gets too large.</span></span> <span data-ttu-id="5a49c-113">Les llistes de preus del producte no es copien per crear llistes de preus personalitzades en els contractes.</span><span class="sxs-lookup"><span data-stu-id="5a49c-113">Product price lists aren't copied to create custom price lists on contracts.</span></span> <span data-ttu-id="5a49c-114">Això vol dir que les llistes de preus del producte no afecten el rendiment del procés de guanyar les ofertes.</span><span class="sxs-lookup"><span data-stu-id="5a49c-114">This means that product price lists don't impact the performance of the quote win process.</span></span>
