---
title: Creació d'una solució per a les dimensions de preus personalitzades
description: En aquest tema s'ofereix informació sobre com crear solucions per a dimensions de preus personalitzades.
author: Rumant
manager: tfehr
ms.date: 11/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3e3f688b0147974ef252a0ee00be20c4669d7165
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278406"
---
# <a name="create-a-solution-for-custom-pricing-dimensions"></a><span data-ttu-id="252af-103">Creació d'una solució per a les dimensions de preus personalitzades</span><span class="sxs-lookup"><span data-stu-id="252af-103">Create a solution for custom pricing dimensions</span></span>

 <span data-ttu-id="252af-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_</span><span class="sxs-lookup"><span data-stu-id="252af-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span> 

>[!IMPORTANT]
><span data-ttu-id="252af-105">Tots els canvis de dimensions de preus personalitzades han d'estar en una solució separada.</span><span class="sxs-lookup"><span data-stu-id="252af-105">All custom pricing dimension changes should be in a separate solution.</span></span> <span data-ttu-id="252af-106">Aquestes importants pràctiques recomanades ofereixen la flexibilitat d'actualitzar o suprimir canvis segons calgui, ajuden a reutilitzar la feina i faciliten la portabilitat dels canvis a altres instàncies.</span><span class="sxs-lookup"><span data-stu-id="252af-106">This important best practice allows the flexibility to update or remove changes as needed, helps with re-use of your work, and makes it easier to port changes to other instances.</span></span> <span data-ttu-id="252af-107">Després d'haver fet tots els canvis necessaris, exporteu la solució com a solució **Administrada** i importeu-la a altres instàncies per tornar a utilitzar-la.</span><span class="sxs-lookup"><span data-stu-id="252af-107">After you make the required changes, export this solution as a **Managed** solution, and then import into other instances for reuse.</span></span>

## <a name="create-a-solution-for-custom-pricing-dimensions"></a><span data-ttu-id="252af-108">Creació d'una solució per a les dimensions de preus personalitzades</span><span class="sxs-lookup"><span data-stu-id="252af-108">Create a solution for custom pricing dimensions</span></span>

1.  <span data-ttu-id="252af-109">Seleccioneu **Configuració** > **Solucions** i, a continuació, **Nova**.</span><span class="sxs-lookup"><span data-stu-id="252af-109">Select **Settings** > **Solutions**, and then select **New**.</span></span>
2.  <span data-ttu-id="252af-110">Anomeneu la solució, *<your organization name>: dimensions de preus*.</span><span class="sxs-lookup"><span data-stu-id="252af-110">Name the solution, *<your organization name> pricing dimensions*.</span></span>
3. <span data-ttu-id="252af-111">Introduïu la informació requerida restant i seleccioneu **Desa**.</span><span class="sxs-lookup"><span data-stu-id="252af-111">Enter the remaining required information, and then select **Save**.</span></span>

  ![Creació d'una solució de dimensió de preus personalitzada](./media/Creation-of-custom-pricing-dimension-solution.png)
 
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="252af-113">Afegir totes les entitats necessàries i els components relacionats a la solució de la dimensió de preus</span><span class="sxs-lookup"><span data-stu-id="252af-113">Add all required entities and related components to the Pricing dimension solution</span></span>

<span data-ttu-id="252af-114">Afegiu les entitats del Project Service següents a la solució de preus per fer canvis d'esquema importants a la solució de preus.</span><span class="sxs-lookup"><span data-stu-id="252af-114">Add the following Project Service entities to your pricing solution to make important schema changes in the pricing solution.</span></span> <span data-ttu-id="252af-115">Un cop completat aquest procediment, les entitats reconeixeran les noves dimensions de preus.</span><span class="sxs-lookup"><span data-stu-id="252af-115">After you have completed this procedure, the entities will recognize the new pricing dimensions.</span></span>

1.  <span data-ttu-id="252af-116">Seleccioneu **Configuració** > **Solucions** i, a continuació, feu doble clic a **Dimensions de preus de <*nom de l'organització*>**.</span><span class="sxs-lookup"><span data-stu-id="252af-116">Select **Settings** > **Solutions**, and then double-click **<*your organization name*> pricing dimensions**.</span></span>
2.  <span data-ttu-id="252af-117">A l'Explorador de solucions, a la subfinestra de navegació esquerra, seleccioneu **Afegeix existent** > **Entitats**.</span><span class="sxs-lookup"><span data-stu-id="252af-117">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3.  <span data-ttu-id="252af-118">Al quadre de diàleg **Components de la solució**, seleccioneu una de les entitats següents:</span><span class="sxs-lookup"><span data-stu-id="252af-118">In the **Solution Components** dialog box, select the following entities:</span></span>
 
   - <span data-ttu-id="252af-119">**Real**</span><span class="sxs-lookup"><span data-stu-id="252af-119">**Actual**</span></span>
   - <span data-ttu-id="252af-120">**Recurs que es pot reservar**</span><span class="sxs-lookup"><span data-stu-id="252af-120">**Bookable Resource**</span></span>
   - <span data-ttu-id="252af-121">**Línia d'estimació**</span><span class="sxs-lookup"><span data-stu-id="252af-121">**Estimate Line**</span></span>
   - <span data-ttu-id="252af-122">**Tasca del projecte**</span><span class="sxs-lookup"><span data-stu-id="252af-122">**Project Task**</span></span>
   - <span data-ttu-id="252af-123">**Detall de la línia de factura**</span><span class="sxs-lookup"><span data-stu-id="252af-123">**Invoice Line Detail**</span></span>
   - <span data-ttu-id="252af-124">**Línia del llibre diari**</span><span class="sxs-lookup"><span data-stu-id="252af-124">**Journal Line**</span></span>
   - <span data-ttu-id="252af-125">**Detall de la línia de contracte del projecte**</span><span class="sxs-lookup"><span data-stu-id="252af-125">**Project Contract Line Detail**</span></span>
   - <span data-ttu-id="252af-126">**Membre de l'equip del projecte**</span><span class="sxs-lookup"><span data-stu-id="252af-126">**Project Team Member**</span></span>
   - <span data-ttu-id="252af-127">**Detall de la línia d'oferta**</span><span class="sxs-lookup"><span data-stu-id="252af-127">**Quote Line Detail**</span></span>
   - <span data-ttu-id="252af-128">**Marge comercial de preu de funció**</span><span class="sxs-lookup"><span data-stu-id="252af-128">**Role Price Markup**</span></span>
   - <span data-ttu-id="252af-129">**Preu per funció**</span><span class="sxs-lookup"><span data-stu-id="252af-129">**Role Price**</span></span>
   - <span data-ttu-id="252af-130">**Entrada de temps**</span><span class="sxs-lookup"><span data-stu-id="252af-130">**Time Entry**</span></span>
 
   ![Afegir entitats existents a la solució de dimensió de preus personalitzada](./media/Existing-entities-to-PD-solution.png)
 
 4. <span data-ttu-id="252af-132">Per a cada entitat, reviseu els components que s'afegeixen i la llista final de recursos d'entitat per a cada entitat.</span><span class="sxs-lookup"><span data-stu-id="252af-132">For each entity, review the components being added and the final list of entity assets for each entity.</span></span> 

   >[!NOTE]
   > <span data-ttu-id="252af-133">Incloeu-hi tots els formularis i visualitzacions de cadascuna de les entitats seleccionades.</span><span class="sxs-lookup"><span data-stu-id="252af-133">Include all forms and views for each of the selected entities.</span></span>

  ![Entitats afegides](./media/solution-component-selection.png)


5.  <span data-ttu-id="252af-135">Quan se us demani que incloeu entitats dependents per a les entitats seleccionades, seleccioneu **No, no incloguis els components necessaris**.</span><span class="sxs-lookup"><span data-stu-id="252af-135">When prompted to include any dependent entities for the selected entities, select **No, do not include required components.**</span></span>

    ![Incloure entitats dependents](./media/Do-not-include-required.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]