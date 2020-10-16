---
title: Càlcul de costos de les línies d'oferta basades en productes
description: En aquest tema es proporciona informació sobre l'aplicació d'un preu de cost a una línia d'oferta basada en productes.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 17b377eab5bcbc1a2327cb3ff87cc75d8de40953
ms.sourcegitcommit: a0f80d024a5d3112a39781815bd31d0c05ddaf6f
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 09/30/2020
ms.locfileid: "3906078"
---
# <a name="costing-product-based-quote-lines"></a><span data-ttu-id="dbdfb-103">Càlcul de costos de les línies d'oferta basades en productes</span><span class="sxs-lookup"><span data-stu-id="dbdfb-103">Costing product-based quote lines</span></span>

<span data-ttu-id="dbdfb-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_</span><span class="sxs-lookup"><span data-stu-id="dbdfb-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="dbdfb-105">Les línies d'oferta basades en productes del Dynamics 365 Project Operations també tenen un camp **Preu de cost**.</span><span class="sxs-lookup"><span data-stu-id="dbdfb-105">Product-based quote lines in Dynamics 365 Project Operations also have a **Cost Price** field.</span></span> <span data-ttu-id="dbdfb-106">Aquest camp s'utilitza per fer el seguiment del preu de cost del producte a la línia d'oferta i per als càlculs de rendibilitat descendents.</span><span class="sxs-lookup"><span data-stu-id="dbdfb-106">This field is used to track the cost price for the product on the quote line and for downstream profitability calculations.</span></span>

<span data-ttu-id="dbdfb-107">Quan es crea una línia d'oferta basada en productes per a un producte del catàleg, el cost de la línia d'oferta basada en productes és per defecte el del camp **Cost estàndard** del catàleg de productes.</span><span class="sxs-lookup"><span data-stu-id="dbdfb-107">When a product-based quote line is created for a catalog product, the cost of the product-based quote line is defaulted from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="dbdfb-108">El camp de cost estàndard del catàleg de productes està configurat a la moneda base de l'organització.</span><span class="sxs-lookup"><span data-stu-id="dbdfb-108">The standard cost field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="dbdfb-109">El cost per unitat per defecte de la línia d'oferta basada en productes es converteix a la moneda de vendes de l'oferta.</span><span class="sxs-lookup"><span data-stu-id="dbdfb-109">The default unit cost on the product-based quote line is converted to the sales currency on the quote.</span></span>

## <a name="unit-cost-on-a-product-based-quote-line"></a><span data-ttu-id="dbdfb-110">Cost per unitat en una línia d'oferta basada en productes</span><span class="sxs-lookup"><span data-stu-id="dbdfb-110">Unit cost on a product-based quote line</span></span>

<span data-ttu-id="dbdfb-111">El propòsit de tenir un cost unitari en una línia d'oferta basada en productes és el de permetre diferents costos d'un producte per a cada venda.</span><span class="sxs-lookup"><span data-stu-id="dbdfb-111">The purpose of having a unit cost on a product-based quote line is to allow for different costs for a product for each sale.</span></span> <span data-ttu-id="dbdfb-112">Aquest no és un escenari tipic, però de vegades el cost del producte pot ser descomptat pel proveïdor en funció del client de la venda definitiva.</span><span class="sxs-lookup"><span data-stu-id="dbdfb-112">This is not a typical scenario, but sometimes the cost of the product may be discounted by the supplier depending on the customer of the final sale.</span></span>

<span data-ttu-id="dbdfb-113">Per exemple:</span><span class="sxs-lookup"><span data-stu-id="dbdfb-113">For example:</span></span>

<span data-ttu-id="dbdfb-114">Fabrikam Robotics està instal·lant braços robòtics a les línies de muntatge d'A Datum Corporation.</span><span class="sxs-lookup"><span data-stu-id="dbdfb-114">Fabrikam Robotics is installing robotic arms at A Datum Corporation's assembly lines.</span></span> <span data-ttu-id="dbdfb-115">Fabrikam ofereix serveis d'instal·lació però els braços robotitzats els fabrica Trey Robotics.</span><span class="sxs-lookup"><span data-stu-id="dbdfb-115">Fabrikam provides installation services but the robotic arms are procured from Trey robotics.</span></span> <span data-ttu-id="dbdfb-116">Si la instal·lació de braços robòtics a A Datum Corporation obre un nou sector industrial per als braços robòtics de Trey, Trey podria oferir un descompte especial per aquest contracte a Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="dbdfb-116">If the installation of robotic arms at A Datum Corporation opens a new industry vertical for Trey's robotic arms, Trey could give a special discount for this deal to Fabrikam.</span></span>

<span data-ttu-id="dbdfb-117">En aquest cas, Fabrikam crearà una línia d'oferta basada en productes per a braços robòtics i un cost especial per unitat per a aquesta oferta.</span><span class="sxs-lookup"><span data-stu-id="dbdfb-117">In this case, Fabrikam will create product-based quote line for Robotic Arms and input a special per unit cost for this quote.</span></span> <span data-ttu-id="dbdfb-118">Aquest cost és diferent del cost estàndard de braços robòtics de Trey.</span><span class="sxs-lookup"><span data-stu-id="dbdfb-118">This cost is different from the standard cost of Trey Robotic Arms.</span></span>
