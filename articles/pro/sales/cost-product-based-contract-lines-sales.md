---
title: Càlcul de costos de línies de contracte basades en productes (bàsic)
description: Aquest tema proporciona informació sobre la creació
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 001b0b54abcdd5fcd1eca7f3271cc78392f68860
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273681"
---
# <a name="cost-product-based-contract-lines---lite"></a><span data-ttu-id="3fccf-103">Càlcul de costos de línies de contracte basades en productes (bàsic)</span><span class="sxs-lookup"><span data-stu-id="3fccf-103">Cost product-based contract lines - lite</span></span>

<span data-ttu-id="3fccf-104">_**S'aplica a:** implementació bàsica: tracte de facturació proforma_</span><span class="sxs-lookup"><span data-stu-id="3fccf-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="3fccf-105">Les línies de contracte basades en productes al Dynamics 365 Project Operations inclouen el camp **Preu de cost**, que emmagatzema el preu de cost del producte per als càlculs de rendibilitat posteriors.</span><span class="sxs-lookup"><span data-stu-id="3fccf-105">Product-based contract lines in Dynamics 365 Project Operations include the **Cost Price** field, which stores the cost price of the product for downstream profitability calculations.</span></span>

<span data-ttu-id="3fccf-106">Quan es crea una línia de contracte basada en productes per a un producte del catàleg, el cost de la línia ve per defecte del camp **Cost estàndard** del catàleg de productes.</span><span class="sxs-lookup"><span data-stu-id="3fccf-106">When a product-based contract line is created for a catalog product, the cost of the line defaults from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="3fccf-107">El camp **Cost estàndard** del catàleg de productes està configurat a la moneda base de l'organització.</span><span class="sxs-lookup"><span data-stu-id="3fccf-107">The **Standard Cost** field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="3fccf-108">Quan el cost unitari per defecte és el de la línia de contracte, es converteix a la moneda de venda del contracte.</span><span class="sxs-lookup"><span data-stu-id="3fccf-108">When the unit cost defaults on the contract line, it's converted into the sales currency on the contract.</span></span>

## <a name="unit-cost-on-a-product-based-contract-line"></a><span data-ttu-id="3fccf-109">Cost per unitat en una línia de contracte basada en productes</span><span class="sxs-lookup"><span data-stu-id="3fccf-109">Unit cost on a product-based contract line</span></span>

<span data-ttu-id="3fccf-110">Tenir un cost unitari en una línia de contracte basada en el producte permet diferents costos de producte per a cada venda d'una unitat.</span><span class="sxs-lookup"><span data-stu-id="3fccf-110">Having a unit cost on a product-based contract line allows for different product costs for each sale of a unit.</span></span> <span data-ttu-id="3fccf-111">Encara que no sempre és necessari, hi ha algunes situacions en les quals el proveïdor pot descomptar el cost del producte per al client.</span><span class="sxs-lookup"><span data-stu-id="3fccf-111">While not always necessary, there are certain scenarios where the cost of the product may be discounted for the customer by the supplier.</span></span> <span data-ttu-id="3fccf-112">Tingueu en compte aquesta hipotètica situació:</span><span class="sxs-lookup"><span data-stu-id="3fccf-112">Consider the following scenario:</span></span>

<span data-ttu-id="3fccf-113">Fabrikam Robotics està instal·lant braços robòtics a les línies de muntatge d'Adatum Corporation.</span><span class="sxs-lookup"><span data-stu-id="3fccf-113">Fabrikam Robotics is installing robotic arms at Adatum Corporation's assembly lines.</span></span> <span data-ttu-id="3fccf-114">Fabrikam proporciona serveis d'instal·lació, però els braços robòtics són de Trey Research.</span><span class="sxs-lookup"><span data-stu-id="3fccf-114">Fabrikam provides installation services but the robotic arms are from Trey Research.</span></span> <span data-ttu-id="3fccf-115">Si la instal·lació de braços robòtics a Adatum Corporation obre un nou sector industrial per a Trey Research, podria oferir un descompte especial per aquest contracte a Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="3fccf-115">If the installation of robotic arms at Adatum Corporation opens a new industry vertical for Trey Research, they could offer a special discount for this deal to Fabrikam.</span></span> <span data-ttu-id="3fccf-116">En aquest cas, Fabrikam crea una línia de contracte basada en productes per a braços robòtics.</span><span class="sxs-lookup"><span data-stu-id="3fccf-116">In this case, Fabrikam creates a product-based contract line for Robotic Arms.</span></span> <span data-ttu-id="3fccf-117">S'introdueix un cost per unitat per a aquest contracte.</span><span class="sxs-lookup"><span data-stu-id="3fccf-117">A per unit cost is entered for this contract.</span></span> <span data-ttu-id="3fccf-118">El cost és diferent del cost dels braços robòtics de Trey Research.</span><span class="sxs-lookup"><span data-stu-id="3fccf-118">The cost is different from the cost of robotic arms from Trey Research.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]