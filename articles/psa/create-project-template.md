---
title: Crear una plantilla de projecte
description: Com crear una plantilla de projecte al Project Service
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
ms.openlocfilehash: e8a9b75aa0721c6e7c85c2bca8796bf9f2c6d3db
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5285111"
---
# <a name="create-a-project-template-project-service"></a><span data-ttu-id="b10ac-103">Crea una plantilla de projecte (Project Service)</span><span class="sxs-lookup"><span data-stu-id="b10ac-103">Create a project template (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="b10ac-104">Les plantilles de projecte us ajuden a estalviar temps si la vostra empresa presenta freqüentment tipus de projectes similars.</span><span class="sxs-lookup"><span data-stu-id="b10ac-104">Project templates save you time if your company regularly bids on similar types of projects.</span></span> <span data-ttu-id="b10ac-105">Ofereixen un conjunt estàndard de funcions i hores estimades per a un tipus de projecte.</span><span class="sxs-lookup"><span data-stu-id="b10ac-105">They provide a standard set of roles and estimated hours for a type of project.</span></span> <span data-ttu-id="b10ac-106">Els administradors de comptes i de projectes poden crear projectes basats en una plantilla de projecte o poden copiar la plantilla i fer-ne una de pròpia.</span><span class="sxs-lookup"><span data-stu-id="b10ac-106">Account managers and project managers can create projects based on a project template, or they can copy the template and make one of their own.</span></span>  
  
## <a name="components-of-project-template"></a><span data-ttu-id="b10ac-107">Components de la plantilla de projecte</span><span class="sxs-lookup"><span data-stu-id="b10ac-107">Components of project template</span></span>
 <span data-ttu-id="b10ac-108">Una plantilla de projecte consta de tres components:</span><span class="sxs-lookup"><span data-stu-id="b10ac-108">A project template consists of three components:</span></span>  
  
- <span data-ttu-id="b10ac-109">**Estructura del desglossament del treball**: una estructura del desglossament del treball d'una plantilla de projecte té el mateix conjunt d'elements que el projecte.</span><span class="sxs-lookup"><span data-stu-id="b10ac-109">**Work breakdown structure**: A work breakdown structure in a project template has the same set of elements as in the project.</span></span> <span data-ttu-id="b10ac-110">Podeu crear una jerarquia de tasca, associar funcions a taques, definir atributs de planificació, definir dependències i visualitzar totes les dades al gràfic de Gantt.</span><span class="sxs-lookup"><span data-stu-id="b10ac-110">You can create a task hierarchy, associate roles to task, define schedule attributes, set dependencies and view all the data in the Gantt.</span></span> <span data-ttu-id="b10ac-111">L'estructura del desglossament de treball de les plantilles de projecte també admet modes de tasca per a cada tasca.</span><span class="sxs-lookup"><span data-stu-id="b10ac-111">The work breakdown structure in project templates also support task modes for each task.</span></span> <span data-ttu-id="b10ac-112">No hi ha cap diferència entre una plantilla de projecte i un projecte quan es crea la planificació de treball.</span><span class="sxs-lookup"><span data-stu-id="b10ac-112">There is no difference between a project template and a project when creating work schedule.</span></span>  
  
- <span data-ttu-id="b10ac-113">**Estimacions de projecte**: les estimacions de projecte de les plantilles funcionen de la mateixa manera que amb els projectes, excepte la llista de preus utilitzada per definir que el cost i els preus de venda per defecte siguin sempre les llistes de preus de vendes i costos definides als paràmetres de l'[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="b10ac-113">**Project estimates**: Project estimates in templates work the same way as they do in projects, except the price lists for defaulting the cost and sales prices are always the default cost and sales price lists defined in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] parameters.</span></span> <span data-ttu-id="b10ac-114">La resta de funcions són les mateixes que al projecte.</span><span class="sxs-lookup"><span data-stu-id="b10ac-114">The rest of the functionality is the same as in a project.</span></span>  
  
- <span data-ttu-id="b10ac-115">**Formació de l'equip del projecte**: en formar un equip de projecte per a una plantilla de projecte, no podeu reservar un recurs amb nom d'una plantilla.</span><span class="sxs-lookup"><span data-stu-id="b10ac-115">**Project team formation**: When forming a project team for a project template, you can’t book a named resource in a template.</span></span> <span data-ttu-id="b10ac-116">Podeu utilitzar **Generar equip de projecte** a l'estructura del desglossament del treball per generar un conjunt de recursos genèrics.</span><span class="sxs-lookup"><span data-stu-id="b10ac-116">You can use **Generate Project Team** in the work breakdown structure to generate a set of generic resources.</span></span> <span data-ttu-id="b10ac-117">També podeu especificar les aptituds i competències necessàries per als recursos genèrics.</span><span class="sxs-lookup"><span data-stu-id="b10ac-117">You can also specify required skills and proficiencies for generic resources.</span></span> <span data-ttu-id="b10ac-118">Podeu substituir un recurs genèric per un recurs que es pot reservar a les plantilles de projecte.</span><span class="sxs-lookup"><span data-stu-id="b10ac-118">You can’t substitute a generic resource with a bookable resource in project templates.</span></span>  
  
## <a name="create-a-project-from-a-template"></a><span data-ttu-id="b10ac-119">Crear un projecte a partir d'una plantilla</span><span class="sxs-lookup"><span data-stu-id="b10ac-119">Create a project from a template</span></span>  
 <span data-ttu-id="b10ac-120">Podeu crear un projecte a partir d'una plantilla de les formes següents:</span><span class="sxs-lookup"><span data-stu-id="b10ac-120">You can create a project from a template in these following ways:</span></span>  
  
-   <span data-ttu-id="b10ac-121">En crear un projecte a partir d'una oferta, podeu triar una plantilla de projecte al formulari de creació ràpida de projectes.</span><span class="sxs-lookup"><span data-stu-id="b10ac-121">When creating a project from the quote, you can choose a project template in the project quick create form.</span></span>  
  
-   <span data-ttu-id="b10ac-122">Quan es crea un projecte fent clic a **Projecte nou**, el formulari de projecte es mostra abans de desar el registre.</span><span class="sxs-lookup"><span data-stu-id="b10ac-122">When creating a project by clicking **New Project**, the project form displays before you save the record.</span></span> <span data-ttu-id="b10ac-123">Des d'aquí, podeu fer clic al camp **Tria una plantilla** per triar-ne una de la llista de plantilles de projecte predefinides de la vostra organització.</span><span class="sxs-lookup"><span data-stu-id="b10ac-123">From here, you can click **Pick a template** field to choose from the list of pre-defined project templates in your organization.</span></span>  
  
-   <span data-ttu-id="b10ac-124">Feu clic a **Crea un projecte a partir d'una plantilla** a la pàgina **Plantilla de projecte** per crear un projecte a partir d'una plantilla.</span><span class="sxs-lookup"><span data-stu-id="b10ac-124">Click **Create project from a template** on the **Project Template** page to create a project from the template.</span></span>  
  
## <a name="copying-components-of-a-template-to-a-project"></a><span data-ttu-id="b10ac-125">Copiar components d'una plantilla a un projecte</span><span class="sxs-lookup"><span data-stu-id="b10ac-125">Copying components of a template to a project</span></span>  
 <span data-ttu-id="b10ac-126">Quan es copien components d'una plantilla a un projecte, hi ha algunes coses que cal saber.</span><span class="sxs-lookup"><span data-stu-id="b10ac-126">When you copy components of a template into a project, there are a few things you should know about.</span></span>  
  
 <span data-ttu-id="b10ac-127">**Copiar una estructura del desglossament del treball**: quan es copia una estructura del desglossament del treball d'una plantilla de projecte, si el projecte té un calendari de projecte diferent del de la plantilla, les hores de treball del calendari de projecte s'aplicaran a la planificació de tasques.</span><span class="sxs-lookup"><span data-stu-id="b10ac-127">**Copying a work breakdown structure**: When you copy the work breakdown structure from a project template, if the project has a different project calendar than the template, the work hours from the project’s calendar will be applied to the schedule of tasks.</span></span> <span data-ttu-id="b10ac-128">Això ajusta la planificació al calendari de projecte de suport.</span><span class="sxs-lookup"><span data-stu-id="b10ac-128">This adjusts the schedule to the backing project calendar.</span></span> <span data-ttu-id="b10ac-129">De la mateixa manera, la primera tasca de l'estructura del desglossament del treball utilitza la data d'inici del projecte, així la resta de la planificació de la jerarquia de la tasca s'actualitza segons la duració i les dependències especificades a l'estructura del desglossament del treball de la plantilla.</span><span class="sxs-lookup"><span data-stu-id="b10ac-129">Similarly, the first task on the work breakdown structure takes the project’s start date, so the rest of the task hierarchy schedule is updated based on the duration and dependencies specified in the template’s work breakdown structure.</span></span>  
  
 <span data-ttu-id="b10ac-130">**Copiar estimacions de projecte**: en copiar línies d'estimació del projecte, les llistes de preus s'actualitzen segons la unitat propietària del projecte per a la llista de preus de cost i el client per a la llista de preus de venda.</span><span class="sxs-lookup"><span data-stu-id="b10ac-130">**Copying project estimates**: When you copy across project estimate lines, price lists are updated based on the owning unit of the project for the cost price list and customer for the sales price list.</span></span> <span data-ttu-id="b10ac-131">El cost unitari i els preus de venda són es determinen a partir de la llista de preus dels projectes associats a l'entitat de vendes.</span><span class="sxs-lookup"><span data-stu-id="b10ac-131">The unit cost and sales prices are determined from these price lists on projects that are associated to a sales entity.</span></span>  
  
 <span data-ttu-id="b10ac-132">**Copiar un equip de projecte**: en copiar l'equip de projecte de la plantilla al projecte, es copien els recursos genèrics amb les aptituds i les competències definides a la plantilla.</span><span class="sxs-lookup"><span data-stu-id="b10ac-132">**Copying a project team**: When you copy the project team from the template to a project, the generic resources are copied across, along with the skills and proficiencies defined in the template.</span></span> <span data-ttu-id="b10ac-133">Les assignacions de recursos genèrics també es mantenen com a la plantilla de projecte.</span><span class="sxs-lookup"><span data-stu-id="b10ac-133">Generic resource assignments are also maintained as in the project template.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="b10ac-134">Vegeu també</span><span class="sxs-lookup"><span data-stu-id="b10ac-134">See Also</span></span>  
 [<span data-ttu-id="b10ac-135">Guia d'administrador de projectes</span><span class="sxs-lookup"><span data-stu-id="b10ac-135">Project Manager Guide</span></span>](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]