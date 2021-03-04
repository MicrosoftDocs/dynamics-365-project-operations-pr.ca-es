---
title: Configurar el Project Service Automation
description: Passos per configurar el Project Service
author: ruhercul
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
ms.openlocfilehash: ec5381f91b1fe5198bd93ac8d6015b1fea38738d
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146921"
---
# <a name="configure-project-service"></a><span data-ttu-id="90137-103">Configurar el Project Service</span><span class="sxs-lookup"><span data-stu-id="90137-103">Configure Project Service</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="90137-104">Abans d'utilitzar les capacitats de l'[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] al [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] per administrar els vostres comptes, projectes i recursos, heu de completar alguns passos de configuració per assegurar-vos que la solució de l'[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] coincideixi amb les necessitats de la vostra organització.</span><span class="sxs-lookup"><span data-stu-id="90137-104">Before you can use the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] automation capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] to manage your accounts, projects, and resources, you need to complete a few configuration steps to ensure the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] solution matches your organization’s needs.</span></span> <span data-ttu-id="90137-105">Aquests passos inclouen:</span><span class="sxs-lookup"><span data-stu-id="90137-105">These steps include:</span></span>  
  
-   <span data-ttu-id="90137-106">[Establir unitats de temps](../psa/set-up-time-units.md).</span><span class="sxs-lookup"><span data-stu-id="90137-106">[Set up time units](../psa/set-up-time-units.md).</span></span> <span data-ttu-id="90137-107">Configureu les unitats de temps al catàleg de productes que utilitzareu com a base per planificar i facturar els projectes.</span><span class="sxs-lookup"><span data-stu-id="90137-107">Configure the time units in the product catalog that you’ll use as a base for scheduling and billing your projects.</span></span>  
  
-   <span data-ttu-id="90137-108">[Configurar les monedes i el tipus de canvi](../psa/set-up-currencies-exchange-rates.md).</span><span class="sxs-lookup"><span data-stu-id="90137-108">[Set up currencies and exchange rates](../psa/set-up-currencies-exchange-rates.md).</span></span> <span data-ttu-id="90137-109">Configureu les monedes que utilitzareu per als vostres projectes.</span><span class="sxs-lookup"><span data-stu-id="90137-109">Set up the currencies to use for your projects.</span></span>  
  
-   <span data-ttu-id="90137-110">[Crear unitats organitzatives](../psa/create-organizational-units.md).</span><span class="sxs-lookup"><span data-stu-id="90137-110">[Create organizational units](../psa/create-organizational-units.md).</span></span> <span data-ttu-id="90137-111">Configureu els grups que la vostra empresa utilitza per dividir el negoci, ja sigui per geografia, funció de negoci o alguna altra divisió lògica.</span><span class="sxs-lookup"><span data-stu-id="90137-111">Set up the groups that your company uses to divide its business, whether by geography, business function, or other logical division.</span></span>  
  
-   <span data-ttu-id="90137-112">[Definir freqüències de facturació](../psa/set-up-invoice-frequencies.md).</span><span class="sxs-lookup"><span data-stu-id="90137-112">[Set up invoice frequencies](../psa/set-up-invoice-frequencies.md).</span></span> <span data-ttu-id="90137-113">Configureu els períodes de temps que voleu utilitzar per a la facturació dels clients.</span><span class="sxs-lookup"><span data-stu-id="90137-113">Set up time periods that you want to use for billing your clients.</span></span>  
  
-   <span data-ttu-id="90137-114">[Configurar categories de transacció](../psa/configure-transaction-categories.md).</span><span class="sxs-lookup"><span data-stu-id="90137-114">[Configure transaction categories](../psa/configure-transaction-categories.md).</span></span> <span data-ttu-id="90137-115">Configureu categories de transacció a les quals el consultors poden carregar les despeses facturables i no facturables.</span><span class="sxs-lookup"><span data-stu-id="90137-115">Set up transaction categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="90137-116">[Configurar categories de despesa](../psa/configure-expense-categories.md).</span><span class="sxs-lookup"><span data-stu-id="90137-116">[Configure expense categories](../psa/configure-expense-categories.md).</span></span> <span data-ttu-id="90137-117">Configureu categories a les quals el consultors poden carregar les despeses facturables i no facturables.</span><span class="sxs-lookup"><span data-stu-id="90137-117">Set up the categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="90137-118">[Crear elements de catàleg de productes](../psa/create-product-catalog-items.md).</span><span class="sxs-lookup"><span data-stu-id="90137-118">[Create product catalog items](../psa/create-product-catalog-items.md).</span></span> <span data-ttu-id="90137-119">Afegiu els productes que veneu, com ara les llicències de programari, al catàleg de productes.</span><span class="sxs-lookup"><span data-stu-id="90137-119">Add the products you sell, such as software licenses, to the product catalog.</span></span>  
  
-   <span data-ttu-id="90137-120">[Crear una llista de preus](../psa/create-price-list.md).</span><span class="sxs-lookup"><span data-stu-id="90137-120">[Create a price list](../psa/create-price-list.md).</span></span> <span data-ttu-id="90137-121">Configureu llistes de preus diferents segons la quantitat que voleu cobrar als vostres clients per a cada funció que el seu projecte requereix.</span><span class="sxs-lookup"><span data-stu-id="90137-121">Configure different price lists, depending on how much you want to charge your clients for each role their project requires.</span></span>  
  
-   <span data-ttu-id="90137-122">[Definir recursos](../psa/set-up-resources.md).</span><span class="sxs-lookup"><span data-stu-id="90137-122">[Set up resources](../psa/set-up-resources.md).</span></span> <span data-ttu-id="90137-123">Afegiu les habilitats, les competències, les funcions de recurs i altra informació sobre els recursos que necessitareu per als projectes.</span><span class="sxs-lookup"><span data-stu-id="90137-123">Add the skills, proficiencies, resource roles, and other resource information that you’ll need for your projects.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="90137-124">Vegeu també</span><span class="sxs-lookup"><span data-stu-id="90137-124">See Also</span></span>  
 <span data-ttu-id="90137-125">[Informació general del Project Service Automation](../psa/overview.md) </span><span class="sxs-lookup"><span data-stu-id="90137-125">[Overview of Project Service Automation](../psa/overview.md) </span></span>  
 <span data-ttu-id="90137-126">[Configurar el Project Service Automation](../psa/configure.md) </span><span class="sxs-lookup"><span data-stu-id="90137-126">[Configure Project Service Automation](../psa/configure.md) </span></span>  
 <span data-ttu-id="90137-127">[Guia de l'administrador de comptes](../psa/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="90137-127">[Account Manager Guide](../psa/account-manager-guide.md) </span></span>  
 <span data-ttu-id="90137-128">[Guia d'administrador de projectes](../psa/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="90137-128">[Project Manager Guide](../psa/project-manager-guide.md) </span></span>  
 <span data-ttu-id="90137-129">[Guia de l'administrador de recursos](../psa/resource-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="90137-129">[Resource Manager Guide](../psa/resource-manager-guide.md) </span></span>  
 [<span data-ttu-id="90137-130">Guia de temps, despeses i col·laboració</span><span class="sxs-lookup"><span data-stu-id="90137-130">Time, Expense, and Collaboration Guid</span></span>](../psa/time-expense-collaboration-guide.md)
