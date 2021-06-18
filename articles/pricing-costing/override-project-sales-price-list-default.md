---
title: Substitució de les llistes de preus de vendes de projectes
description: Aquest tema proporciona informació sobre la creació de llistes de preus de vendes personalitzades.
author: rumant
ms.date: 10/22/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: db2ff6acaad6ab4cbcc98d3d5b06b36ed23b758f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5995069"
---
# <a name="override-project-sales-price-lists"></a><span data-ttu-id="02350-103">Substitució de les llistes de preus de vendes de projectes</span><span class="sxs-lookup"><span data-stu-id="02350-103">Override project sales price lists</span></span>

<span data-ttu-id="02350-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_</span><span class="sxs-lookup"><span data-stu-id="02350-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

## <a name="customer-specific-project-price-lists"></a><span data-ttu-id="02350-105">Llistes de preus de projecte específiques del client</span><span class="sxs-lookup"><span data-stu-id="02350-105">Customer-specific project price lists</span></span>

<span data-ttu-id="02350-106">Es poden configurar acords de preus específics de client com a llistes de preus del projecte en un registre de compte al Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="02350-106">Customer-specific price agreements can be set up as project price lists on an account record in Dynamics 365 Project Operations.</span></span>

<span data-ttu-id="02350-107">Per configurar una llista de preus de projecte específica del client, a l'àrea **Vendes**, aneu al registre del compte.</span><span class="sxs-lookup"><span data-stu-id="02350-107">To set up a customer-specific project price list, in the **Sales** area, navigate to the account record.</span></span>

1. <span data-ttu-id="02350-108">Obriu la pàgina de llista **Comptes**.</span><span class="sxs-lookup"><span data-stu-id="02350-108">Open the **Accounts** list page.</span></span>
2. <span data-ttu-id="02350-109">Localitzeu i feu doble clic en un registre de client per obrir la pàgina **Detalls del compte**.</span><span class="sxs-lookup"><span data-stu-id="02350-109">Locate and double-click a customer record to open the **Account** details page.</span></span>
3. <span data-ttu-id="02350-110">A la pestanya **Llistes de preus del projecte**, seleccioneu **+ Nova llista de preus del projecte**.</span><span class="sxs-lookup"><span data-stu-id="02350-110">On the **Project Price lists** tab, select **+ New Project Price List**.</span></span>
4. <span data-ttu-id="02350-111">A la pàgina **Nova llista de preus del projecte**, seleccioneu una llista de preus al menú desplegable.</span><span class="sxs-lookup"><span data-stu-id="02350-111">On the **New Project Price List** page, select a price list from the drop-down.</span></span> <span data-ttu-id="02350-112">Només s'inclouen les llistes de preus que tenen el context definit com a **Vendes** i la moneda de les quals coincideixi amb la moneda del compte.</span><span class="sxs-lookup"><span data-stu-id="02350-112">Only price lists that have the context set to **Sales** and whose currency matches the account currency are included.</span></span>
5. <span data-ttu-id="02350-113">Anomeneu l'associació i seleccioneu **Desa**.</span><span class="sxs-lookup"><span data-stu-id="02350-113">Name the association, and then select **Save**.</span></span> <span data-ttu-id="02350-114">Es crea una llista de preus de projecte específica del client.</span><span class="sxs-lookup"><span data-stu-id="02350-114">A customer-specific project price list is created.</span></span> <span data-ttu-id="02350-115">Aquesta llista de preus s'utilitzarà per defecte en els preus del projecte en les ofertes o contractes de projecte creats per a aquest client en què la data de creació de l'oferta o contracte de projecte estigui dins de la data d'efectivitat de la llista de preus.</span><span class="sxs-lookup"><span data-stu-id="02350-115">This price list will be used to default project prices on project quotes or contracts created for this customer where the created date of the quote or project contract falls within the date effectivity of the price list.</span></span>

## <a name="custom-pricing-on-project-quotes"></a><span data-ttu-id="02350-116">Preus personalitzats en ofertes del projecte</span><span class="sxs-lookup"><span data-stu-id="02350-116">Custom pricing on project quotes</span></span>

<span data-ttu-id="02350-117">A les ofertes del projecte, podeu tenir preus de projecte que comencin amb una llista de preus estàndard per defecte que es basi per defecte en els paràmetres del client o del projecte.</span><span class="sxs-lookup"><span data-stu-id="02350-117">On project quotes, you can have project pricing that starts with a default standard price list that defaults from the customer or from the project parameters.</span></span>

<span data-ttu-id="02350-118">Quan necessiteu preus personalitzats per al treball relacionat amb el projecte en una oferta concreta, podeu obtenir-ho de l'entitat associada de les llistes de preus del projecte.</span><span class="sxs-lookup"><span data-stu-id="02350-118">When you need custom pricing for project-related work on a particular quote, you can get that from the project price lists associated entity.</span></span>

<span data-ttu-id="02350-119">Completeu els passos següents per configurar els preus del projecte específics de l'oferta.</span><span class="sxs-lookup"><span data-stu-id="02350-119">Complete the following steps to set up quote-specific project pricing.</span></span>

1. <span data-ttu-id="02350-120">Obriu l'oferta del projecte i seleccioneu la pestanya **Llistes de preus del projecte**.</span><span class="sxs-lookup"><span data-stu-id="02350-120">Open the project quote and select the **Project Price Lists** tab.</span></span>
2. <span data-ttu-id="02350-121">A la subquadrícula, seleccioneu **Crea preus personalitzats**.</span><span class="sxs-lookup"><span data-stu-id="02350-121">In the subgrid, select **Create custom pricing**.</span></span>

<span data-ttu-id="02350-122">Totes les llistes de preus del projecte que s'adjunten a l'oferta es copien a les llistes de preus noves.</span><span class="sxs-lookup"><span data-stu-id="02350-122">All the project price lists that are attached to the quote are copied to new price lists.</span></span> <span data-ttu-id="02350-123">Els noms de les noves llistes de preus reflecteixen el nom de l'oferta amb una marca de temps de la data de creació d'aquestes llistes de preus.</span><span class="sxs-lookup"><span data-stu-id="02350-123">The names of the new price lists reflect the name of quote with a date-time stamp for when these price lists were created.</span></span>

<span data-ttu-id="02350-124">Podeu utilitzar cadascuna d'aquestes llistes de preus i fer actualitzacions dels preus laborals (preu per funció) i de despeses (preu per categoria).</span><span class="sxs-lookup"><span data-stu-id="02350-124">You can use each of those price lists and make updates to labor (role price) and expense (category price) prices.</span></span> <span data-ttu-id="02350-125">Aquests preus només seran aplicables a aquesta oferta de projecte.</span><span class="sxs-lookup"><span data-stu-id="02350-125">These prices will only be applicable to this project quote.</span></span>

## <a name="price-lists-on-a-project-contract"></a><span data-ttu-id="02350-126">Llistes de preus en un contracte de projecte</span><span class="sxs-lookup"><span data-stu-id="02350-126">Price lists on a project contract</span></span>

<span data-ttu-id="02350-127">En un contracte de projecte, els preus del projecte sempre són per defecte una llista de preus personalitzada amb el nom del contracte i la marca de temps de creació afegida al nom.</span><span class="sxs-lookup"><span data-stu-id="02350-127">On a project contract, project pricing always defaults as a custom price list with the name of contract and the created date time stamp appended to the name.</span></span> <span data-ttu-id="02350-128">Això és cert si el contracte es va crear quan es va guanyar l'oferta o si el contracte es va crear des de zero.</span><span class="sxs-lookup"><span data-stu-id="02350-128">This is true whether the contract was created when the quote was won or if the contract was created from scratch.</span></span> <span data-ttu-id="02350-129">Si cal, podeu suprimir aquesta associació a la llista de preus personalitzada i associar una llista de preus estàndard al contracte del projecte.</span><span class="sxs-lookup"><span data-stu-id="02350-129">If needed, you can remove this association to the custom price list and associate a standard price list to the project contract instead.</span></span>

<span data-ttu-id="02350-130">Quan associeu una llista de preus estàndard a les llistes de preus del projecte en una oferta o contracte, els canvis realitzats als preus de la llista de preus afectaran totes les ofertes i contractes que utilitzin la llista de preus.</span><span class="sxs-lookup"><span data-stu-id="02350-130">When you associate a standard price list to the project price lists on quote or contract, any changes made to the prices in the price list will impact all quotes and contracts that use the price list.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]