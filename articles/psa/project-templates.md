---
title: Plantilles de projecte
description: En aquest tema es proporciona informació sobre com utilitzar les plantilles de projecte per a la configuració ràpida del projecte.
author: ruhercul
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 4fd618e15524c5cef5b6da9b282f449e3dfb7973
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122994"
---
# <a name="project-templates"></a><span data-ttu-id="cd3a4-103">Plantilles de projecte</span><span class="sxs-lookup"><span data-stu-id="cd3a4-103">Project templates</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="cd3a4-104">Una plantilla de projecte és un marc predefinit que us ajuda a iniciar ràpidament i fàcilment un projecte.</span><span class="sxs-lookup"><span data-stu-id="cd3a4-104">A project template is a predefined framework that helps you quickly and easily start a project.</span></span> <span data-ttu-id="cd3a4-105">Podeu utilitzar una plantilla predefinida per crear un projecte nou amb un sol clic.</span><span class="sxs-lookup"><span data-stu-id="cd3a4-105">You can use a predefined template to create a new project with a single click.</span></span> <span data-ttu-id="cd3a4-106">Pel que fa als projectes, heu de definir els requisits previs per a les plantilles de projecte.</span><span class="sxs-lookup"><span data-stu-id="cd3a4-106">As for projects, you must define the prerequisites for project templates.</span></span> <span data-ttu-id="cd3a4-107">Heu de definir un calendari de projecte per a cada plantilla de projecte i les funcions i llistes de preus han d'estar predefinides a l'organització, de manera que els components de la plantilla tinguin dades útils.</span><span class="sxs-lookup"><span data-stu-id="cd3a4-107">You must define a project calendar for each project template, and roles and price lists must be predefined in the organization, so that the components of the template have useful data.</span></span>

<span data-ttu-id="cd3a4-108">Una plantilla de projecte consta de tres components: una planificació, estimacions de projecte i membres de l'equip del projecte.</span><span class="sxs-lookup"><span data-stu-id="cd3a4-108">A project template consists of three components: a schedule, project estimates, and project team members.</span></span>

## <a name="schedule"></a><span data-ttu-id="cd3a4-109">Planifica</span><span class="sxs-lookup"><span data-stu-id="cd3a4-109">Schedule</span></span>

<span data-ttu-id="cd3a4-110">Una planificació d'una plantilla de projecte té el mateix conjunt d'elements que una planificació d'un projecte.</span><span class="sxs-lookup"><span data-stu-id="cd3a4-110">A schedule in a project template has the same set of elements as a schedule in a project.</span></span> <span data-ttu-id="cd3a4-111">Podeu crear una jerarquia de tasques, associar funcions a taques, definir atributs de planificació i definir dependències.</span><span class="sxs-lookup"><span data-stu-id="cd3a4-111">You can create a task hierarchy, associate roles with tasks, define schedule attributes, and set dependencies.</span></span> <span data-ttu-id="cd3a4-112">Una planificació d'una plantilla de projecte també admet modes de tasca per a cada tasca.</span><span class="sxs-lookup"><span data-stu-id="cd3a4-112">A schedule in a project template also supports task modes for each task.</span></span> <span data-ttu-id="cd3a4-113">Per tant, és compatible amb el motor de planificació.</span><span class="sxs-lookup"><span data-stu-id="cd3a4-113">Therefore, it supports the scheduling engine.</span></span> <span data-ttu-id="cd3a4-114">Heu d'associar un calendari de projectes amb el projecte.</span><span class="sxs-lookup"><span data-stu-id="cd3a4-114">You must associate a project calendar with the project.</span></span> <span data-ttu-id="cd3a4-115">Quan creeu una planificació de treball, no hi ha cap diferència entre una plantilla de projecte i un projecte.</span><span class="sxs-lookup"><span data-stu-id="cd3a4-115">When you create a work schedule, there is no difference between a project template and a project.</span></span>

## <a name="project-estimates"></a><span data-ttu-id="cd3a4-116">Estimacions del projecte</span><span class="sxs-lookup"><span data-stu-id="cd3a4-116">Project estimates</span></span>

<span data-ttu-id="cd3a4-117">Les estimacions de projecte d'una plantilla de projecte funcionen de la mateixa manera que les estimacions de projecte en un projecte.</span><span class="sxs-lookup"><span data-stu-id="cd3a4-117">Project estimates in a project template work the same way as project estimates in a project.</span></span> <span data-ttu-id="cd3a4-118">No obstant, els preus dels costos i de les vendes s'agrupen en llistes de costos i vendes per defecte definides als paràmetres.</span><span class="sxs-lookup"><span data-stu-id="cd3a4-118">However, the cost and sales prices are pulled from the default cost and sales price lists that are defined in the parameters.</span></span>

## <a name="creating-a-project-from-a-template"></a><span data-ttu-id="cd3a4-119">Crear un projecte a partir d'una plantilla</span><span class="sxs-lookup"><span data-stu-id="cd3a4-119">Creating a project from a template</span></span>
 
<span data-ttu-id="cd3a4-120">Hi ha diverses maneres de crear un projecte a partir d'una plantilla de projecte:</span><span class="sxs-lookup"><span data-stu-id="cd3a4-120">There are several ways to create a project from a project template:</span></span>

- <span data-ttu-id="cd3a4-121">En crear un projecte a partir d'una oferta, podeu seleccionar una plantilla de projecte al quadre de diàleg **Creació ràpida: projecte**.</span><span class="sxs-lookup"><span data-stu-id="cd3a4-121">When you create a project from a quote, you can select a project template in the **Quick Create: Project** dialog box.</span></span>

> ![Quadre de diàleg Creació ràpida: projecte](media/project-11.png)

- <span data-ttu-id="cd3a4-123">Quan creeu un projecte seleccionant **Nou projecte**, la pàgina **Projecte** apareix abans que el registre es desi.</span><span class="sxs-lookup"><span data-stu-id="cd3a4-123">When you create a project by selecting **New Project**, the **Project** page appears before the record is saved.</span></span> <span data-ttu-id="cd3a4-124">Al camp **Selecció de plantilla**, seleccioneu una de les plantilles de projecte predefinides a l'organització.</span><span class="sxs-lookup"><span data-stu-id="cd3a4-124">In the **Pick a Template** field, select one of the predefined project templates in the organization.</span></span>
- <span data-ttu-id="cd3a4-125">Utilitzeu **Crea un projecte des d'una plantilla** a la pàgina **Entitat de plantilla**.</span><span class="sxs-lookup"><span data-stu-id="cd3a4-125">Use **Create Project from a Template** on the **Template Entity** page.</span></span>

## <a name="copying-components-of-template-to-project"></a><span data-ttu-id="cd3a4-126">Copiar components d'una plantilla a un projecte</span><span class="sxs-lookup"><span data-stu-id="cd3a4-126">Copying components of template to project</span></span>

<span data-ttu-id="cd3a4-127">Quan copieu els components d'una plantilla de projecte a un projecte, es poden produir unes quantes substitucions, en funció de la configuració del projecte.</span><span class="sxs-lookup"><span data-stu-id="cd3a4-127">When you copy the components of a project template to a project, a few overrides can occur, depending on the settings in the project.</span></span>

### <a name="copying-the-schedule"></a><span data-ttu-id="cd3a4-128">Copiar la planificació</span><span class="sxs-lookup"><span data-stu-id="cd3a4-128">Copying the schedule</span></span>

<span data-ttu-id="cd3a4-129">Quan es copia la planificació d'una plantilla de projecte, si el projecte té un calendari de projecte diferent del de la plantilla, les hores de treball del calendari de projecte s'apliquen a la planificació de tasques.</span><span class="sxs-lookup"><span data-stu-id="cd3a4-129">When you copy the schedule from a project template, if the project has a different project calendar than the template, work hours from the project's calendar are applied to the task schedule.</span></span> <span data-ttu-id="cd3a4-130">D'aquesta manera, s'ajusta la planificació al calendari del projecte de suport.</span><span class="sxs-lookup"><span data-stu-id="cd3a4-130">In this way, the schedule is adjusted to match the backing project calendar.</span></span> <span data-ttu-id="cd3a4-131">De la mateixa manera, la primera tasca de la planificació utilitza la data d'inici del projecte, i la planificació de la resta de la planificació de la jerarquia de la tasca s'actualitza segons la duració i les dependències especificades a la plantilla.</span><span class="sxs-lookup"><span data-stu-id="cd3a4-131">Similarly, the first task on the schedule takes the project's start date, and the schedule of the rest of the hierarchy is updated based on the duration and dependencies that are specified in the template.</span></span> 

### <a name="copying-project-estimates"></a><span data-ttu-id="cd3a4-132">Copiar estimacions del projecte</span><span class="sxs-lookup"><span data-stu-id="cd3a4-132">Copying project estimates</span></span> 

<span data-ttu-id="cd3a4-133">Quan copieu diverses línies d'estimació del projecte, les llistes de preus s'actualitzen.</span><span class="sxs-lookup"><span data-stu-id="cd3a4-133">When you copy across project estimate lines, the price lists are updated.</span></span> <span data-ttu-id="cd3a4-134">Per a la llista de preus de cost, aquestes actualitzacions es basen en la unitat propietària del projecte.</span><span class="sxs-lookup"><span data-stu-id="cd3a4-134">For the cost price list, these updates are based on the owning unit of the project.</span></span> <span data-ttu-id="cd3a4-135">Per a la llista de preus de vendes, es basen en el client.</span><span class="sxs-lookup"><span data-stu-id="cd3a4-135">For the sales price list, they are based on the customer.</span></span> <span data-ttu-id="cd3a4-136">Per als projectes associats a una entitat de vendes, el cost unitari i els preus de venda són es determinen a partir d'aquestes llistes de preus.</span><span class="sxs-lookup"><span data-stu-id="cd3a4-136">For projects that are associated with a sales entity, the unit cost and sales prices are determined based on these price lists.</span></span>

### <a name="copying-a-project-team"></a><span data-ttu-id="cd3a4-137">Copiar un equip de projecte</span><span class="sxs-lookup"><span data-stu-id="cd3a4-137">Copying a project team</span></span>

<span data-ttu-id="cd3a4-138">En copiar un equip de projecte de la plantilla de projecte al projecte, es copien els recursos genèrics, juntament amb les aptituds i les competències definides a la plantilla.</span><span class="sxs-lookup"><span data-stu-id="cd3a4-138">When a project team is copied from a project template to a project, the generic resources are copied, together with the skills and proficiencies that are defined in the template.</span></span> <span data-ttu-id="cd3a4-139">Les assignacions de recursos genèrics també es mantenen com estaven a la plantilla de projecte.</span><span class="sxs-lookup"><span data-stu-id="cd3a4-139">Generic resource assignments are also maintained as they were in the project template.</span></span> <span data-ttu-id="cd3a4-140">Els recursos amb nom no són compatibles amb les plantilles de projecte.</span><span class="sxs-lookup"><span data-stu-id="cd3a4-140">Named resources aren't supported in project templates.</span></span>
