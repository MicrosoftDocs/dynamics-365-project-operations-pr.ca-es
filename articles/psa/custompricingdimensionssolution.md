---
title: Crear solucions personalitzades per a les dimensions de preus
description: Aquest tema explica com crear una solució personalitzada en crear dimensions de preus personalitzades.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 3810df9b875d017a8d639b5253b96275571898f3
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144626"
---
# <a name="create-custom-solutions-for-pricing-dimensions"></a><span data-ttu-id="32b28-103">Crear solucions personalitzades per a les dimensions de preus</span><span class="sxs-lookup"><span data-stu-id="32b28-103">Create custom solutions for pricing dimensions</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

> [!IMPORTANT]
> <span data-ttu-id="32b28-104">Tots els canvis de dimensions de preus personalitzades han d'estar en una solució separada.</span><span class="sxs-lookup"><span data-stu-id="32b28-104">All custom pricing dimension changes should be in a separate solution.</span></span> <span data-ttu-id="32b28-105">Aquestes pràctiques recomanades importants proporcionen una flexibilitat futura per actualitzar o suprimir els canvis segons calgui, us ajudaran a reutilitzar el vostre treball i facilita la portabilitat d'aquests canvis en una altra instància.</span><span class="sxs-lookup"><span data-stu-id="32b28-105">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="32b28-106">Després de fer els canvis necessaris, exporteu aquesta solució com a **Solució administrada** i importeu-la a altres instàncies per tornar a utilitzar la configuració dels preus.</span><span class="sxs-lookup"><span data-stu-id="32b28-106">After you make the required changes, export this solution as a **Managed solution**, and import it into other instances to reuse your pricing setup.</span></span>

1. <span data-ttu-id="32b28-107">Seleccioneu **Configuració** > **Solucions** i, a continuació, **Nova**.</span><span class="sxs-lookup"><span data-stu-id="32b28-107">Select **Settings** > **Solutions**, and then select **New**.</span></span> 
2. <span data-ttu-id="32b28-108">Anomeneu la solució **Dimensions de preus de \<your organization name>**, introduïu la informació necessària restant i, a continuació, seleccioneu **Desa**.</span><span class="sxs-lookup"><span data-stu-id="32b28-108">Name the solution, **\<your organization name> pricing dimensions**, enter the remaining required information, and then select **Save**.</span></span>

> ![Crear una solució personalitzada per a les dimensions de preus](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="32b28-110">Afegir totes les entitats necessàries i els components relacionats a la solució de la dimensió de preus</span><span class="sxs-lookup"><span data-stu-id="32b28-110">Add all required entities and related components to the Pricing dimension solution</span></span>
<span data-ttu-id="32b28-111">Haureu d'afegir les següents entitats del Project Service a la solució de preus.</span><span class="sxs-lookup"><span data-stu-id="32b28-111">You will need to add the following Project Service entities to your pricing solution.</span></span> <span data-ttu-id="32b28-112">Completeu els passos d'aquest procediment per fer canvis importants d'esquema a la solució de preus de manera que les entitats coneguin les noves dimensions de preus.</span><span class="sxs-lookup"><span data-stu-id="32b28-112">Complete the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="32b28-113">Seleccioneu **Configuració** > **Solucions** i feu doble clic a **Dimensions de preus de \<your organization name>**.</span><span class="sxs-lookup"><span data-stu-id="32b28-113">Select **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="32b28-114">A l'Explorador de solucions, a la subfinestra de navegació esquerra, seleccioneu **Afegeix existent** > **Entitats**.</span><span class="sxs-lookup"><span data-stu-id="32b28-114">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="32b28-115">Al quadre de diàleg **Components de la solució**, seleccioneu una de les entitats següents:</span><span class="sxs-lookup"><span data-stu-id="32b28-115">In the **Solution Components** dialog box, select the following entities:</span></span>

- <span data-ttu-id="32b28-116">Real</span><span class="sxs-lookup"><span data-stu-id="32b28-116">Actual</span></span>
- <span data-ttu-id="32b28-117">Recurs que es pot reservar</span><span class="sxs-lookup"><span data-stu-id="32b28-117">Bookable Resource</span></span>
- <span data-ttu-id="32b28-118">Línia d'estimació</span><span class="sxs-lookup"><span data-stu-id="32b28-118">Estimate Line</span></span>
- <span data-ttu-id="32b28-119">Tasca del projecte</span><span class="sxs-lookup"><span data-stu-id="32b28-119">Project Task</span></span>
- <span data-ttu-id="32b28-120">Detall de la línia de factura</span><span class="sxs-lookup"><span data-stu-id="32b28-120">Invoice Line Detail</span></span>
- <span data-ttu-id="32b28-121">Línia del llibre diari</span><span class="sxs-lookup"><span data-stu-id="32b28-121">Journal Line</span></span>
- <span data-ttu-id="32b28-122">Detall de la línia de contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="32b28-122">Project Contract Line Detail</span></span>
- <span data-ttu-id="32b28-123">Membre de l'equip del projecte</span><span class="sxs-lookup"><span data-stu-id="32b28-123">Project Team Member</span></span>
- <span data-ttu-id="32b28-124">Detall de la línia d'oferta</span><span class="sxs-lookup"><span data-stu-id="32b28-124">Quote Line Detail</span></span>
- <span data-ttu-id="32b28-125">Marge comercial de preu de funció</span><span class="sxs-lookup"><span data-stu-id="32b28-125">Role Price Markup</span></span>
- <span data-ttu-id="32b28-126">Preu per funció</span><span class="sxs-lookup"><span data-stu-id="32b28-126">Role Price</span></span> 
- <span data-ttu-id="32b28-127">Entrada de temps</span><span class="sxs-lookup"><span data-stu-id="32b28-127">Time Entry</span></span> 

> ![Afegir entitats existents a la solució de dimensions de preus](media/Existing-entities-to-PD-solution.png)

> ![Selecció de components de la solució](media/Dimension-Components.png)

> [!NOTE]
> <span data-ttu-id="32b28-130">Assegureu-vos d'incloure tots els formularis i les visualitzacions de cadascuna de les entitats seleccionades.</span><span class="sxs-lookup"><span data-stu-id="32b28-130">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="32b28-131">Quan se us demani que inclogueu entitats dependents de les entitats seleccionades, seleccioneu **No**.</span><span class="sxs-lookup"><span data-stu-id="32b28-131">When prompted to include any dependent entities for the selected entities, select **No**.</span></span>

> ![No incloguis tots els components relacionats](media/Do-not-include-required.png)


