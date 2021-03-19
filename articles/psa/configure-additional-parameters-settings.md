---
title: Configurar paràmetres addicionals
description: Com configurar paràmetres addicionals al Project Service
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: bac484e29f1a0578042f350b1657a42e80b48cb4
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290752"
---
# <a name="configure-additional-parameter-settings-project-service"></a><span data-ttu-id="d07c0-103">Configurar paràmetres addicionals (Project Service)</span><span class="sxs-lookup"><span data-stu-id="d07c0-103">Configure additional parameter settings (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="d07c0-104">Un cop hàgiu configurat els elements als temes anteriors, heu de definir paràmetres addicionals per utilitzar-los per als vostres projectes.</span><span class="sxs-lookup"><span data-stu-id="d07c0-104">Once you’ve configured the items in previous topics, you need to set additional project parameters to use for your projects.</span></span> <span data-ttu-id="d07c0-105">Quan hàgiu instal·lat l'[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] per primer cop, podeu crear paràmetres per crear per primer cop tots els registres necessaris per que funcionin a l'[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="d07c0-105">When you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], you created a parameters setting to first create all the records required for [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to work.</span></span> <span data-ttu-id="d07c0-106">Ara és el moment de tornar enrere i configurar camps addicionals per a aquests paràmetres.</span><span class="sxs-lookup"><span data-stu-id="d07c0-106">Now it’s time to go back and configure additional fields for these settings.</span></span>  
  
 <span data-ttu-id="d07c0-107">Haureu d'haver configurat els paràmetres següents:</span><span class="sxs-lookup"><span data-stu-id="d07c0-107">You’ll need to have configured the following settings:</span></span>  
  
-   <span data-ttu-id="d07c0-108">Unitat organitzativa</span><span class="sxs-lookup"><span data-stu-id="d07c0-108">Organizational unit</span></span>  
  
-   <span data-ttu-id="d07c0-109">Freqüència de facturació</span><span class="sxs-lookup"><span data-stu-id="d07c0-109">Invoice frequency</span></span>  
  
-   <span data-ttu-id="d07c0-110">Plantilles d'hores de feina</span><span class="sxs-lookup"><span data-stu-id="d07c0-110">Work hours template</span></span>  
  
-   <span data-ttu-id="d07c0-111">Llista de preus</span><span class="sxs-lookup"><span data-stu-id="d07c0-111">Price list</span></span>  
 
<span data-ttu-id="d07c0-112">En aquest pas, també indicareu quin tipus d'assignació de recursos voleu:</span><span class="sxs-lookup"><span data-stu-id="d07c0-112">In this step, you’ll also indicate what type of resource allocation you want:</span></span>  
  
- <span data-ttu-id="d07c0-113">**Central**.</span><span class="sxs-lookup"><span data-stu-id="d07c0-113">**Central**.</span></span> <span data-ttu-id="d07c0-114">Només els administradors de recursos poden assignar recursos a projectes.</span><span class="sxs-lookup"><span data-stu-id="d07c0-114">Only resource managers can allocate resources to projects.</span></span>  
  
- <span data-ttu-id="d07c0-115">**Híbrida**.</span><span class="sxs-lookup"><span data-stu-id="d07c0-115">**Hybrid**.</span></span> <span data-ttu-id="d07c0-116">Els administradors de recursos, projectes i comptes poden assignar recursos a projectes.</span><span class="sxs-lookup"><span data-stu-id="d07c0-116">Resource managers, project managers, and account managers can allocate resources to projects.</span></span>  
  
 
<span data-ttu-id="d07c0-117">Per definir els paràmetres del projecte:</span><span class="sxs-lookup"><span data-stu-id="d07c0-117">To set project parameters:</span></span>  
  
1. <span data-ttu-id="d07c0-118">Aneu a **Project Service > Paràmetres**.</span><span class="sxs-lookup"><span data-stu-id="d07c0-118">Go to **Project Service > Parameters**.</span></span>  
  
2. <span data-ttu-id="d07c0-119">Feu clic als paràmetres que voleu configurar (els que vàreu crear en instal·lar per primer cop l'[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]) o feu clic a **Crea** per crear-ne de nous.</span><span class="sxs-lookup"><span data-stu-id="d07c0-119">Click the parameters setting you want to configure (the one you created when you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]), or click **New** to create a new one.</span></span>  
  
3. <span data-ttu-id="d07c0-120">A l'àrea **General**, definiu totes les opcions per als paràmetres del vostre projecte.</span><span class="sxs-lookup"><span data-stu-id="d07c0-120">In the **General** area, set all the options for your project parameters.</span></span>  
  
4. <span data-ttu-id="d07c0-121">A l'àrea **Llista de preus**, feu clic a **+** per afegir una llista de preus, seleccioneu una llista de preus a la llista desplegable **Llista de preus de paràmetres de projecte** i feu clic a **Desa**.</span><span class="sxs-lookup"><span data-stu-id="d07c0-121">In the **Price List** area, click **+** to add a price list, select a price list in the **Project Parameter Price List** drop-down list, and then click **Save**.</span></span>  
  
5. <span data-ttu-id="d07c0-122">Feu clic al botó **Desa** a la cantonada inferior dreta de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="d07c0-122">Click the **Save** button in the bottom right corner of the screen.</span></span>  

> [!NOTE]
> <span data-ttu-id="d07c0-123">El registre del paràmetre del projecte s'ha de mantenir perquè el Project Service funcioni de manera correcta.</span><span class="sxs-lookup"><span data-stu-id="d07c0-123">The project parameter record must be maintained for Project Service to function correcly.</span></span> <span data-ttu-id="d07c0-124">Aquest registre no s'ha de suprimir.</span><span class="sxs-lookup"><span data-stu-id="d07c0-124">This record should not be deleted.</span></span>

### <a name="see-also"></a><span data-ttu-id="d07c0-125">Vegeu també</span><span class="sxs-lookup"><span data-stu-id="d07c0-125">See Also</span></span>  
 [<span data-ttu-id="d07c0-126">Definir recursos</span><span class="sxs-lookup"><span data-stu-id="d07c0-126">Set up resources</span></span>](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]