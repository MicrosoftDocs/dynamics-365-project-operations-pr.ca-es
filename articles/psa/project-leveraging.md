---
title: Estimacions de vendes i projectes
description: En aquest tema es proporciona informació sobre com aprofitar la planificació i les estimacions del procés de venda.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: eafe60362003198a223026526f56261de414bb4a
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072230"
---
# <a name="sales-estimates-and-projects"></a><span data-ttu-id="a8783-103">Estimacions de vendes i projectes</span><span class="sxs-lookup"><span data-stu-id="a8783-103">Sales estimates and projects</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="a8783-104">Durant el procés de vendes, podeu crear estimacions de vendes mitjançant la vinculació d'un projecte a una oferta de vendes.</span><span class="sxs-lookup"><span data-stu-id="a8783-104">During the sales process, you can create sales estimates by linking a project to a sales quote.</span></span> <span data-ttu-id="a8783-105">D'aquesta manera, pot produir-se una estimació determinista durant el procés de vendes, per aprofitar les capacitats de planificació i estimació del projecte.</span><span class="sxs-lookup"><span data-stu-id="a8783-105">In this way, deterministic estimation can occur during the sales process, to take advantage of project scheduling and estimation capabilities.</span></span> <span data-ttu-id="a8783-106">Si la venda prospera, la planificació que s'utilitza per a propòsits d'estimació de vendes es pot utilitzar com a base per a un major refinament del pla del projecte.</span><span class="sxs-lookup"><span data-stu-id="a8783-106">If the sale goes through, the schedule that was used for sales estimation purposes can be used as the basis for further refinement of the project plan.</span></span>

## <a name="linking-a-project-to-a-quote-line"></a><span data-ttu-id="a8783-107">Enllaçar un projecte amb una línia d'oferta</span><span class="sxs-lookup"><span data-stu-id="a8783-107">Linking a project to a quote line</span></span>

<span data-ttu-id="a8783-108">Quan creeu una línia d'oferta basada en projectes, podeu crear un projecte nou o associar-ne un d'existent a la pàgina **Línia d'oferta**.</span><span class="sxs-lookup"><span data-stu-id="a8783-108">When you create a project-based quote line, you can create a new project or associate an existing project pn the **Quote Line** page.</span></span> 

> ![Formulari de línia d'oferta](media/project-8.png)
 
<span data-ttu-id="a8783-110">Quan creeu un projecte nou a partir dels detalls de la línia d'oferta, podeu treure partit de les plantilles del projecte.</span><span class="sxs-lookup"><span data-stu-id="a8783-110">When you create a new project from the quote line details, you can take advantage of project templates.</span></span> <span data-ttu-id="a8783-111">Les plantilles de projecte són projectes model que representen plans de projecte estàndard i estimacions financeres que són típiques d'una organització.</span><span class="sxs-lookup"><span data-stu-id="a8783-111">Project templates are model projects that represent standard project plans and financial estimates that are typical in an organization.</span></span> <span data-ttu-id="a8783-112">També poden representar exemplars de plans de projecte i estimacions de projectes anteriors.</span><span class="sxs-lookup"><span data-stu-id="a8783-112">They can also represent copies of project plans and estimates from past projects.</span></span>

> ![Detalls de la línia d'oferta](media/project-9.png)
  
<span data-ttu-id="a8783-114">Quan creeu el projecte a partir de l'oferta, el projecte s'associa automàticament a la línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="a8783-114">When you create the project from the quote, the project is automatically associated with the quote line.</span></span>

## <a name="components-of-estimates-in-a-project"></a><span data-ttu-id="a8783-115">Components de les estimacions d'un projecte</span><span class="sxs-lookup"><span data-stu-id="a8783-115">Components of estimates in a project</span></span>

<span data-ttu-id="a8783-116">Una planificació us permet dividir el treball en tasques, mantenir una jerarquia de tasques, determinar quins recursos han de completar una tasca i assignar una estimació de l'esforç necessari per completar una tasca.</span><span class="sxs-lookup"><span data-stu-id="a8783-116">A schedule lets you divide work into tasks, maintain a hierarchy of tasks, determine what resources are required to complete a task, and assign an estimate of the effort that is required to complete a task.</span></span>

<span data-ttu-id="a8783-117">Podeu definir l'esforç de treball i les estimacions de planificació mitjançant els camps de la pestanya **Planificació** de la pàgina **Projecte**.</span><span class="sxs-lookup"><span data-stu-id="a8783-117">You can define the work effort and schedule estimates by using the fields on the **Schedule** tab of the **Project** page.</span></span> <span data-ttu-id="a8783-118">Com que una llista de preus està associada amb el projecte, les estimacions financeres es calculen mitjançant l'ús de les tarifes de costos i vendes definides a la llista de tarifes.</span><span class="sxs-lookup"><span data-stu-id="a8783-118">Because a price list is associated with the project, financial estimates are calculated by using cost and sales prices that are defined in the price list.</span></span>

## <a name="importing-estimates-from-a-project-into-a-quote"></a><span data-ttu-id="a8783-119">Importar estimacions d'un projecte a una oferta</span><span class="sxs-lookup"><span data-stu-id="a8783-119">Importing estimates from a project into a quote</span></span>

<span data-ttu-id="a8783-120">Després de definir estimacions de projecte, podeu importar-les a la línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="a8783-120">After you define project estimates, you can import them into the quote line.</span></span> <span data-ttu-id="a8783-121">A la pàgina **Detalls de la línia d'oferta** , seleccioneu **Importa a partir d'estimacions** a la franja per resumir les estimacions de projecte pel tipus de transacció, la funció o el nivell de tasca.</span><span class="sxs-lookup"><span data-stu-id="a8783-121">On the **Quote Line Details** page, select **Import from estimates** on the ribbon to summarize project estimates by transaction type, role, or task level.</span></span>
