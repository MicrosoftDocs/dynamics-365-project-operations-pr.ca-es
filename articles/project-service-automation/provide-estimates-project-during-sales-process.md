---
title: Proporcionar estimacions de treball per a un projecte durant el procés de vendes
description: Com proporcionar estimacions de treball per a un projecte durant el procés de vendes al Project Service
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 8e6fbba8-2908-4555-9470-43c37e66efea
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8edb91010dd1227bc7947b59664d08430c219638
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749552"
---
# <a name="provide-work-estimates-for-a-project-during-the-sales-process-project-service"></a><span data-ttu-id="e451a-103">Proporcionar estimacions de treball per a un projecte durant el procés de vendes (Project Service)</span><span class="sxs-lookup"><span data-stu-id="e451a-103">Provide work estimates for a project during the sales process (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="e451a-104">Durant el procés de vendes, podeu elaborar estimacions de vendes des de zero amb línies d'oferta.</span><span class="sxs-lookup"><span data-stu-id="e451a-104">During the sales process, you can work out sales estimates from the ground up with quote lines.</span></span> <span data-ttu-id="e451a-105">Les capacitats de l'[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] al [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] proporcionen una manera més científica i determinista d'arribar amb una estimació de vendes desglossant els elements de treball i associant els atributs rellevants que contribueixen a les estimacions del projecte en l'estructura del desglossament del treball.</span><span class="sxs-lookup"><span data-stu-id="e451a-105">[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] provide a more scientific and deterministic way of coming up with sales estimates by breaking down work items and associating relevant attributes that contribute toward the estimates for the project in the work breakdown structure.</span></span>  
  
 <span data-ttu-id="e451a-106">Una vegada guanyada la venda, podeu utilitzar l'estructura del desglossament del treball associada al vostre pla de projecte i millorar-la per tal de completar amb èxit el projecte.</span><span class="sxs-lookup"><span data-stu-id="e451a-106">Once you win the sale, you can use the associated work breakdown structure in your project plan, refining it as necessary for successful completion of your project.</span></span>  
  
## <a name="link-a-project-to-a-quote-line"></a><span data-ttu-id="e451a-107">Enllaçar un projecte amb una línia d'oferta</span><span class="sxs-lookup"><span data-stu-id="e451a-107">Link a project to a quote line</span></span>  
 <span data-ttu-id="e451a-108">Quan creeu una línia d'oferta basada en un projecte, podeu crear un nou projecte a partir de la línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="e451a-108">When creating a project-based quote line, you can create a new project from the quote line.</span></span> <span data-ttu-id="e451a-109">Podeu utilitzar plantilles de projecte, que poden ser plans de projecte estàndard preconfigurats i estimacions financeres habituals a la vostra organització, o una còpia d'un pla de projecte i les estimacions d'un projecte passat.</span><span class="sxs-lookup"><span data-stu-id="e451a-109">You can then use project templates, which are either pre-configured standard project plans and financial estimates common to your organization, or a copy of a project plan and estimates from a past project.</span></span> <span data-ttu-id="e451a-110">Quan creeu un projecte, la tria d'una plantilla de projecte proporciona una base per refinar el pla de projecte, les estimacions i els requisits de les funcions.</span><span class="sxs-lookup"><span data-stu-id="e451a-110">When you create a project, choosing a project template provides a basis to refine the project plan, estimates, and role requirements.</span></span> <span data-ttu-id="e451a-111">Si el vostre projecte es crea a partir de l'oferta, el projecte s'associa automàticament a la línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="e451a-111">By creating your project from the quote, the project is automatically associated with the quote line.</span></span>  
  
## <a name="project-estimate-components"></a><span data-ttu-id="e451a-112">Components d'estimació del projecte</span><span class="sxs-lookup"><span data-stu-id="e451a-112">Project estimate components</span></span>  
 <span data-ttu-id="e451a-113">L'estructura del desglossament del treball en un projecte proporciona una manera de desglossar la feina en tasques, mantenir una jerarquia de tasques i assignar una estimació de l'esforç necessari per completar cada tasca.</span><span class="sxs-lookup"><span data-stu-id="e451a-113">The work breakdown structure in a project provides a way to break down work into tasks, maintain a hierarchy of tasks, and assign an estimate of effort required to complete each task.</span></span> <span data-ttu-id="e451a-114">També podeu associar funcions a una tasca per indicar una estimació del tipus de recurs necessari per completar una tasca i una planificació.</span><span class="sxs-lookup"><span data-stu-id="e451a-114">You can also associate roles to a task to indicate an estimate of the type of resource required to complete a task and a schedule.</span></span>  
  
 <span data-ttu-id="e451a-115">L'estructura del desglossament del treball ajuda a calcular l'esforç de treball i de planificació.</span><span class="sxs-lookup"><span data-stu-id="e451a-115">The work breakdown structure helps you determine work effort and schedule estimates.</span></span> <span data-ttu-id="e451a-116">Per defecte, el projecte utilitza llistes de preus per defecte que heu definit prèviament.</span><span class="sxs-lookup"><span data-stu-id="e451a-116">By default, the project uses default price lists that you defined earlier.</span></span> <span data-ttu-id="e451a-117">El cost i els preus de vendes definits a les llistes de preus ajuden a determinar les estimacions financeres per al desglossament de feina del projecte.</span><span class="sxs-lookup"><span data-stu-id="e451a-117">The cost and sales prices defined in the price lists help determine financial estimates for the project’s work breakdown.</span></span>  
  
 <span data-ttu-id="e451a-118">Si el vostre projecte està associat amb un pressupost, i l'oferta té una llista de preus diferent del valor per defecte, la llista de preus de l'oferta s'utilitza per a les estimacions financeres.</span><span class="sxs-lookup"><span data-stu-id="e451a-118">If your project is associated with a quote, and the quote has a different price list from the default, the quote’s price list is used for financial estimates.</span></span>  
  
## <a name="import-estimates-from-a-project-into-a-quote"></a><span data-ttu-id="e451a-119">Importar estimacions d'un projecte a una oferta</span><span class="sxs-lookup"><span data-stu-id="e451a-119">Import estimates from a project into a quote</span></span>  
 <span data-ttu-id="e451a-120">Quan ja teniu les estimacions de projecte dins del projecte, podeu importar aquestes estimacions a la línia d'oferta:</span><span class="sxs-lookup"><span data-stu-id="e451a-120">Once you have project estimates in the project, you can import these estimates into the quote line:</span></span>  
  
-   <span data-ttu-id="e451a-121">A **Detalls de la línia d'oferta**, feu clic a **Importa des d'estimacions**.</span><span class="sxs-lookup"><span data-stu-id="e451a-121">In **Quote Line Details**, click **Import from estimates**.</span></span> 

-   <span data-ttu-id="e451a-122">Seleccioneu si importareu estimacions de projecte resumides per tipus d'operació, funció o nivell de node d'estructura del desglossament del treball.</span><span class="sxs-lookup"><span data-stu-id="e451a-122">Select whether to import project estimates summarized by transaction type, role, or work breakdown structure node level.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="e451a-123">Vegeu també</span><span class="sxs-lookup"><span data-stu-id="e451a-123">See Also</span></span>  
 [<span data-ttu-id="e451a-124">Guia d'administrador de projectes</span><span class="sxs-lookup"><span data-stu-id="e451a-124">Project Manager Guide</span></span>](../project-service/project-manager-guide.md)