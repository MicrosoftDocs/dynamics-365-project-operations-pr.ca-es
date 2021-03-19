---
title: Crear una llista de preus
description: Com crear una llista de preus al Project Service
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 0732ccca43e404412efae8a91873e43c28d041ca
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290302"
---
# <a name="create-a-price-list-project-service"></a><span data-ttu-id="f77d3-103">Crear una llista de preus (Project Service)</span><span class="sxs-lookup"><span data-stu-id="f77d3-103">Create a price list (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="f77d3-104">Les llistes de preus proporcionen una plantilla que els administradors de comptes poden utilitzar per a la creació d'ofertes, projectes i per establir els costos d'un projecte.</span><span class="sxs-lookup"><span data-stu-id="f77d3-104">Price lists provide a template your account managers can use for creating quotes and projects, and for establishing the costs of a project.</span></span> <span data-ttu-id="f77d3-105">Proporcionen una llista d'elements de línia de funcions i despeses i el preu que es cobrarà per a cadascuna.</span><span class="sxs-lookup"><span data-stu-id="f77d3-105">They provide a line item list of roles and expenses, and the price you will charge for each.</span></span> <span data-ttu-id="f77d3-106">Podeu crear diverses llistes de preus per mantenir estructures de preus independents per a les diferents regions on veneu els productes o diferents canals de venda.</span><span class="sxs-lookup"><span data-stu-id="f77d3-106">You can create multiple price lists so that you can maintain separate price structures for different regions you sell your products in or for different sales channels.</span></span> <span data-ttu-id="f77d3-107">És una bona idea crear com a mínim una llista de preus per a cada moneda amb la qual tingueu previst facturar els vostres clients.</span><span class="sxs-lookup"><span data-stu-id="f77d3-107">It’s a good idea to create at least one price list for every currency you plan to bill your customers in.</span></span>  
  
<span data-ttu-id="f77d3-108">Per crear previsions financeres dels treballs que es lliuraran, assegureu-vos que cada projecte tingui un cost de reserva i una llista de preus de venda.</span><span class="sxs-lookup"><span data-stu-id="f77d3-108">To create financial estimates for the work to be delivered, make sure every project has a backing cost and sales price list.</span></span> <span data-ttu-id="f77d3-109">Configureu un cost per defecte i una llista de preus de venda que s'apliquin a tots els projectes creats a la vostra organització.</span><span class="sxs-lookup"><span data-stu-id="f77d3-109">Set up a default cost and sales pricelist that applies to all projects created in your organization.</span></span>  
  
<span data-ttu-id="f77d3-110">Les llistes de preus es basen en funcions i categories de despesa i, per tant, abans de crear una llista de preus, assegureu-vos que ja heu configurat les funcions i les categories de despesa que vulgueu utilitzar mentre creeu la llista de preus.</span><span class="sxs-lookup"><span data-stu-id="f77d3-110">Price lists rely on roles and expense categories, so before you create a price list, make sure you’ve already configured the roles and expense categories you want to use while creating the price list.</span></span>  
  
1.  <span data-ttu-id="f77d3-111">Aneu a **Project Service > Llistes de preus**.</span><span class="sxs-lookup"><span data-stu-id="f77d3-111">Go to **Project Service > Price Lists**.</span></span>  
  
2.  <span data-ttu-id="f77d3-112">Feu clic a **Nou**.</span><span class="sxs-lookup"><span data-stu-id="f77d3-112">Click **New**.</span></span>  
  
3.  <span data-ttu-id="f77d3-113">A **Context**, seleccioneu si aquesta llista de preus és per a **Costos**, **Compres** o **Vendes**.</span><span class="sxs-lookup"><span data-stu-id="f77d3-113">In **Context**, select whether this price list is for **Cost**, **Purchase**, or **Sales**.</span></span>  
  
4.  <span data-ttu-id="f77d3-114">A **Nom**, introduïu un nom per a la llista de preus.</span><span class="sxs-lookup"><span data-stu-id="f77d3-114">In **Name**, enter a name for the price list.</span></span>  
  
5.  <span data-ttu-id="f77d3-115">A **Moneda**, seleccioneu la moneda que utilitzareu per a la facturació o els costos.</span><span class="sxs-lookup"><span data-stu-id="f77d3-115">In **Currency**, select the currency you’re going to use for billing or costing.</span></span>  
  
6.  <span data-ttu-id="f77d3-116">A **Unitat de temps**, especifiqueu el període de temps al qual s'aplica el preu, com ara dia o hora.</span><span class="sxs-lookup"><span data-stu-id="f77d3-116">In **Time Unit**, specify the period of time the price applies to, such as day or hour.</span></span>  
  
7.  <span data-ttu-id="f77d3-117">Empleneu la **Data d'inici**, la **Data final** i la **Descripció** segons sigui necessari.</span><span class="sxs-lookup"><span data-stu-id="f77d3-117">Fill in the **Start Date**, **End Date**, and **Description** as needed.</span></span>  
  
8.  <span data-ttu-id="f77d3-118">Feu clic a **Desa** per crear el projecte per tal que el pugueu continuar editant.</span><span class="sxs-lookup"><span data-stu-id="f77d3-118">Click **Save** to create the record so you can continue editing it.</span></span>  
  
9. <span data-ttu-id="f77d3-119">Per afegir un preu de funció a la llista de preus, feu clic a **+** a **Preus de funció**.</span><span class="sxs-lookup"><span data-stu-id="f77d3-119">To add a role price to the price list, click **+** under **Role prices**.</span></span>  
  
10. <span data-ttu-id="f77d3-120">A la subfinestra **Preu de funció**, empleneu els detalls i, a continuació, feu clic a **Desa**.</span><span class="sxs-lookup"><span data-stu-id="f77d3-120">In the **Role Price** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="f77d3-121">Continueu afegint els preus de funcions que calguin.</span><span class="sxs-lookup"><span data-stu-id="f77d3-121">Continue adding role prices as necessary.</span></span> <span data-ttu-id="f77d3-122">Quan hagueu acabat, feu clic a **Desa** a la cantonada inferior dreta de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="f77d3-122">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
11. <span data-ttu-id="f77d3-123">Per afegir un preu de categoria de despesa a la llista de preus, feu clic a **+** a **Preus de categoria**.</span><span class="sxs-lookup"><span data-stu-id="f77d3-123">To add an expense category price to the price list, click **+** under **Category prices**.</span></span>  
  
12. <span data-ttu-id="f77d3-124">A la subfinestra **Preu de categoria de transacció**, empleneu els detalls i, a continuació, feu clic a **Desa**.</span><span class="sxs-lookup"><span data-stu-id="f77d3-124">In the **Transaction Category Price** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="f77d3-125">Continueu afegint els preus de categoria que calguin.</span><span class="sxs-lookup"><span data-stu-id="f77d3-125">Continue adding category prices as necessary.</span></span> <span data-ttu-id="f77d3-126">Quan hagueu acabat, feu clic a **Desa** a la cantonada inferior dreta de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="f77d3-126">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
13. <span data-ttu-id="f77d3-127">Per afegir elements de la llista de preus a la llista de preus, feu clic a **+** a **Elements de la llista de preus**.</span><span class="sxs-lookup"><span data-stu-id="f77d3-127">To add price list items to the price list, click **+** under **Price List Items**.</span></span>  
  
14. <span data-ttu-id="f77d3-128">A la subfinestra **Element de la llista de preus**, empleneu els detalls i, a continuació, feu clic a **Desa**.</span><span class="sxs-lookup"><span data-stu-id="f77d3-128">In the **Price List Item** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="f77d3-129">Continueu afegint els elements de la llista de preus que calguin.</span><span class="sxs-lookup"><span data-stu-id="f77d3-129">Continue adding price list items as necessary.</span></span> <span data-ttu-id="f77d3-130">Quan hagueu acabat, feu clic a **Desa** a la cantonada inferior dreta de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="f77d3-130">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
15. <span data-ttu-id="f77d3-131">Per afegir relacions de zones de vendes a la llista de preus, feu clic a **+** a **Relacions de zona de vendes**.</span><span class="sxs-lookup"><span data-stu-id="f77d3-131">To add territory relationships to the price list, click **+** under **Territory Relationships**.</span></span>  
  
16. <span data-ttu-id="f77d3-132">A la finestra **Nova connexió**, empleneu els detalls i, a continuació, feu clic a **Desa**.</span><span class="sxs-lookup"><span data-stu-id="f77d3-132">In the **New Connection** window, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="f77d3-133">Continueu afegint les relacions de zona de venda que sigui necessàries.</span><span class="sxs-lookup"><span data-stu-id="f77d3-133">Continue adding territory relationships as necessary.</span></span> <span data-ttu-id="f77d3-134">Quan hagueu acabat, feu clic a **Desa** a la cantonada inferior dreta de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="f77d3-134">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="f77d3-135">Vegeu també</span><span class="sxs-lookup"><span data-stu-id="f77d3-135">See Also</span></span>  
 [<span data-ttu-id="f77d3-136">Configurar el Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="f77d3-136">Configure Project Service Automation</span></span>](../psa/configure.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]