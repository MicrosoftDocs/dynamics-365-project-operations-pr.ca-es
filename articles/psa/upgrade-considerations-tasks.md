---
title: Consideracions d'actualització per a l'estructura del desglossament del treball
description: En aquest tema es proporciona informació sobre l'actualització de l'estructura del desglossament del treball del Project Service Automation 2.x al 3.x.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 10/18/2019
ms.topic: article
author: ruhercul
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
ms.openlocfilehash: d31ca60b267063e9cadf544468ece501353950fa
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/27/2021
ms.locfileid: "5951332"
---
# <a name="upgrade-considerations-for-the-work-breakdown-structure"></a><span data-ttu-id="718c3-103">Consideracions d'actualització per a l'estructura del desglossament del treball</span><span class="sxs-lookup"><span data-stu-id="718c3-103">Upgrade considerations for the work breakdown structure</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="718c3-104">En aquest tema es proporciona informació sobre l'actualització de l'estructura del desglossament del treball del Project Service Automation 2.x al 3.x.</span><span class="sxs-lookup"><span data-stu-id="718c3-104">This topic provides information about upgrading the work breakdown structure from Project Service Automation 2.x to 3.x.</span></span> <span data-ttu-id="718c3-105">Aquest tema defineix l'estat saludable d'un projecte del Project Service Automation (PSA) necessari per a una actualització correcta.</span><span class="sxs-lookup"><span data-stu-id="718c3-105">This topic defines the healthy state of a project in Project Service Automation (PSA) that is required for a successful upgrade.</span></span> <span data-ttu-id="718c3-106">També hi ha informació sobre les condicions de bloqueig habituals que faran que falli l'actualització.</span><span class="sxs-lookup"><span data-stu-id="718c3-106">There is also information about the common blocking conditions that will cause upgrade to fail.</span></span> <span data-ttu-id="718c3-107">Per obtenir més informació sobre la definició de tasques de projecte i les seves funcions dins d'una planificació del projecte, vegeu [Planificacions de projecte](project-creating.md).</span><span class="sxs-lookup"><span data-stu-id="718c3-107">For more information about defining project tasks and their functions within a project schedule, see [Project schedules](project-creating.md).</span></span>

## <a name="key-entities"></a><span data-ttu-id="718c3-108">Entitats clau</span><span class="sxs-lookup"><span data-stu-id="718c3-108">Key entities</span></span>
<span data-ttu-id="718c3-109">Per a una estructura de desglossament del treball exacta que ja està carregada de recursos, són necessàries les entitats següents:</span><span class="sxs-lookup"><span data-stu-id="718c3-109">For an accurate work breakdown structure that is already loaded with resources, the following entities are required:</span></span>

- [<span data-ttu-id="718c3-110">Projecte</span><span class="sxs-lookup"><span data-stu-id="718c3-110">Project</span></span>](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project)
- [<span data-ttu-id="718c3-111">Equip del projecte</span><span class="sxs-lookup"><span data-stu-id="718c3-111">Project Team</span></span>](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam)
- [<span data-ttu-id="718c3-112">Tasca del projecte</span><span class="sxs-lookup"><span data-stu-id="718c3-112">Project Task</span></span>](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask)
- [<span data-ttu-id="718c3-113">Assignacions de recursos</span><span class="sxs-lookup"><span data-stu-id="718c3-113">Resource Assignments</span></span>](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment)
- [<span data-ttu-id="718c3-114">Dependència de les tasques del projecte</span><span class="sxs-lookup"><span data-stu-id="718c3-114">Project Task Dependency</span></span>](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency)
- [<span data-ttu-id="718c3-115">Recursos que es poden reservar</span><span class="sxs-lookup"><span data-stu-id="718c3-115">Bookable Resources</span></span>](/dynamics365/customerengagement/on-premises/developer/entities/bookableresource)

<span data-ttu-id="718c3-116">Per definir una estructura del desglossament del treball carregada de recursos, heu de completar els passos següents:</span><span class="sxs-lookup"><span data-stu-id="718c3-116">To define a resource loaded work breakdown structure, you must complete the following steps:</span></span>

1. <span data-ttu-id="718c3-117">Crear un projecte nou.</span><span class="sxs-lookup"><span data-stu-id="718c3-117">Create a new project.</span></span> <span data-ttu-id="718c3-118">Per obtenir més informació sobre com crear un projecte nou, vegeu [msdyn_project](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project).</span><span class="sxs-lookup"><span data-stu-id="718c3-118">For more information about how to create a new project, see [msdyn_project](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project).</span></span>
2. <span data-ttu-id="718c3-119">Crear una o diverses tasques.</span><span class="sxs-lookup"><span data-stu-id="718c3-119">Create one or more tasks.</span></span> <span data-ttu-id="718c3-120">Per obtenir més informació sobre com crear una tasca, vegeu [msdyn_projecttask](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask).</span><span class="sxs-lookup"><span data-stu-id="718c3-120">For more information about how to create a task, see [msdyn_projecttask](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask).</span></span>
3. <span data-ttu-id="718c3-121">Definir les dependències de la tasca.</span><span class="sxs-lookup"><span data-stu-id="718c3-121">Define the task dependencies.</span></span> <span data-ttu-id="718c3-122">Per obtenir més informació, vegeu [Dependència de la tasca del projecte](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency).</span><span class="sxs-lookup"><span data-stu-id="718c3-122">For more information, see [Project Task Dependency](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency).</span></span>
4. <span data-ttu-id="718c3-123">Assignar membres de l'equip del projecte al projecte.</span><span class="sxs-lookup"><span data-stu-id="718c3-123">Assign project team members to the project.</span></span> <span data-ttu-id="718c3-124">Per obtenir més informació, vegeu [msdyn_projectteam](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam).</span><span class="sxs-lookup"><span data-stu-id="718c3-124">For more information, see [msdyn_projectteam](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam).</span></span>
5. <span data-ttu-id="718c3-125">Assignar membres de l'equip del projecte a les tasques.</span><span class="sxs-lookup"><span data-stu-id="718c3-125">Assign project team members to the tasks.</span></span> <span data-ttu-id="718c3-126">Per obtenir més informació, vegeu [msdyn_resourceassignment](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment).</span><span class="sxs-lookup"><span data-stu-id="718c3-126">For more information, see [msdyn_resourceassignment](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment).</span></span>

## <a name="project-team-relationships"></a><span data-ttu-id="718c3-127">Relacions de l'equip del projecte</span><span class="sxs-lookup"><span data-stu-id="718c3-127">Project team relationships</span></span>

<span data-ttu-id="718c3-128">Per garantir l'actualització correcta, les relacions següents s'han de mantenir correctament:</span><span class="sxs-lookup"><span data-stu-id="718c3-128">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>
- <span data-ttu-id="718c3-129">Tots els membres de l'equip del projecte han d'estar associats amb un recurs que es pugui reservar.</span><span class="sxs-lookup"><span data-stu-id="718c3-129">All project team members must be associated with a bookable resource.</span></span>
- <span data-ttu-id="718c3-130">Tots els membres de l'equip del projecte han d'estar associats amb un recurs del mateix projecte.</span><span class="sxs-lookup"><span data-stu-id="718c3-130">All project team members must be associated with the same project.</span></span> 

## <a name="project-task-relationships"></a><span data-ttu-id="718c3-131">Relacions de les tasques del projecte</span><span class="sxs-lookup"><span data-stu-id="718c3-131">Project task relationships</span></span>
<span data-ttu-id="718c3-132">Per garantir l'actualització correcta, les relacions següents s'han de mantenir correctament:</span><span class="sxs-lookup"><span data-stu-id="718c3-132">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="718c3-133">Les tasques relacionades s'han d'associar amb el mateix projecte.</span><span class="sxs-lookup"><span data-stu-id="718c3-133">Any related tasks must be associated with the same project.</span></span>
- <span data-ttu-id="718c3-134">Cada tasca de línia ha de tenir una tasca principal.</span><span class="sxs-lookup"><span data-stu-id="718c3-134">Every line task must have a parent task.</span></span>
- <span data-ttu-id="718c3-135">Cada tasca de línia ha de tenir un projecte principal.</span><span class="sxs-lookup"><span data-stu-id="718c3-135">Every task must have a parent project.</span></span>

### <a name="valid-conditions"></a><span data-ttu-id="718c3-136">Condicions vàlides</span><span class="sxs-lookup"><span data-stu-id="718c3-136">Valid conditions</span></span>

- <span data-ttu-id="718c3-137">Totes les duracions de tasques han de ser superiors o iguals a (> =) una hora i menys de 1.800.000 minuts (1.250 dies).\*</span><span class="sxs-lookup"><span data-stu-id="718c3-137">All task durations must be greater than or equal to (>=) one hour and less than 1,800,000 minutes (1,250 days).\*</span></span>
- <span data-ttu-id="718c3-138">Totes les tasques han de tenir una data d'inici no anterior al 01/01/2000.\*</span><span class="sxs-lookup"><span data-stu-id="718c3-138">All tasks must have a start date no earlier than 2000/01/01.\*</span></span>
- <span data-ttu-id="718c3-139">Totes les tasques han de tenir una data d'inici que no sigui més enllà de 17 anys des del dia d'avui.\*</span><span class="sxs-lookup"><span data-stu-id="718c3-139">All tasks must have a start date no later than 17 years from the present day.\*</span></span>
- <span data-ttu-id="718c3-140">Totes les tasques han de tenir una data d'inici abans o igual a la seva data d'acabament.</span><span class="sxs-lookup"><span data-stu-id="718c3-140">All tasks must have a start date earlier or equal to their finish date.</span></span>
- <span data-ttu-id="718c3-141">Tots els tipus de transaccions de les classificacions (despeses, materials, impostos i temps) han de tenir valors per a **Unitat per defecte** i **Grup d'unitats**.</span><span class="sxs-lookup"><span data-stu-id="718c3-141">All transaction types on classifications (Expense, Material, Tax, and Time) must have values for **Default Unit** and **Unit Group**.</span></span>
- <span data-ttu-id="718c3-142">S'han d'evitar els formats de data amb lletres.</span><span class="sxs-lookup"><span data-stu-id="718c3-142">Date formats with letters should be avoided.</span></span>

### <a name="potential-mitigation-steps"></a><span data-ttu-id="718c3-143">Possibles passos per a la mitigació</span><span class="sxs-lookup"><span data-stu-id="718c3-143">Potential mitigation steps</span></span>
- <span data-ttu-id="718c3-144">Utilitzeu la cerca avançada per identificar tasques del projecte que no contenen cap identificador de projecte.</span><span class="sxs-lookup"><span data-stu-id="718c3-144">Use Advanced Find to identify Project tasks that do not contain a Project ID.</span></span>
- <span data-ttu-id="718c3-145">Utilitzeu la cerca avançada per identificar tasques del projecte en què la duració programada és superior a > 1.800.000.</span><span class="sxs-lookup"><span data-stu-id="718c3-145">Use Advanced Find to identify Project tasks where the scheduled duration is greater than > 1,800,000.</span></span>
- <span data-ttu-id="718c3-146">Abans de fer canvis de les dades, heu d'investigar qualsevol personalització associada amb l'entitat que potser hagi fet que les dades estiguin en mal estat.</span><span class="sxs-lookup"><span data-stu-id="718c3-146">Prior to making any data changes, you should investigate any customizations associated with the entity that may have led to getting the data into a bad state.</span></span> <span data-ttu-id="718c3-147">Aquestes personalitzacions s'han d'abordar abans de continuar amb qualsevol actualització relacionada amb les dades.</span><span class="sxs-lookup"><span data-stu-id="718c3-147">These customizations should be addressed before proceeding with any data-related updates.</span></span>
- <span data-ttu-id="718c3-148">Per a les tasques identificades que han quedat òrfenes, considereu la possibilitat de suprimir aquestes tasques si no es necessiten o si han d'estar associades amb el projecte principal correcte.</span><span class="sxs-lookup"><span data-stu-id="718c3-148">For the identified tasks that have been orphaned, consider deleting these tasks if they are not needed or if they should be associated with the correct parent project.</span></span>
- <span data-ttu-id="718c3-149">Per a qualsevol tasca en què la duració sigui superior a 1.250 dies, considereu afegir diverses tasques per representar la duració total, si és factible.</span><span class="sxs-lookup"><span data-stu-id="718c3-149">For any tasks where the duration is greater than 1,250 days, consider adding multiple tasks to represent the total duration, if feasible.</span></span>

> [!NOTE]
> <span data-ttu-id="718c3-150">Els elements que s'han assenyalat amb un asterisc (\*) tenen límits que es deuen al fet que l'administració de relacions entre proveïdors i associats (CRM) només admet 7.320 expansions de periodicitat.</span><span class="sxs-lookup"><span data-stu-id="718c3-150">Items noted with an asterisk (\*) have limits that are due to the fact that customer relationship management (CRM) supports only 7,320 recurrence expansions.</span></span> <span data-ttu-id="718c3-151">Heu d'estar per sota d'aquest límit.</span><span class="sxs-lookup"><span data-stu-id="718c3-151">You must stay below this limit.</span></span>

## <a name="resource-assignment-relationships"></a><span data-ttu-id="718c3-152">Relacions de l'assignació de recursos</span><span class="sxs-lookup"><span data-stu-id="718c3-152">Resource Assignment relationships</span></span>
<span data-ttu-id="718c3-153">Per garantir l'actualització correcta, les relacions següents s'han de mantenir correctament:</span><span class="sxs-lookup"><span data-stu-id="718c3-153">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="718c3-154">Totes les assignacions de recursos d'una estructura del desglossament del treball han d'estar relacionades amb el mateix projecte.</span><span class="sxs-lookup"><span data-stu-id="718c3-154">All Resource Assignments in a work breakdown structure must be related to the same project.</span></span>
- <span data-ttu-id="718c3-155">Totes les assignacions de recursos d'una estructura del desglossament del treball han d'estar associades als membres de l'equip del projecte del mateix projecte.</span><span class="sxs-lookup"><span data-stu-id="718c3-155">All Resource Assignments in a work breakdown structure must be associated to project team members in the same project.</span></span>

### <a name="potential-mitigation-steps"></a><span data-ttu-id="718c3-156">Possibles passos per a la mitigació</span><span class="sxs-lookup"><span data-stu-id="718c3-156">Potential mitigation steps</span></span>
- <span data-ttu-id="718c3-157">Identifiqueu totes les tasques que es troben fora de les condicions descrites anteriorment.</span><span class="sxs-lookup"><span data-stu-id="718c3-157">Identify all tasks that fall outside the conditions described above.</span></span>  
- <span data-ttu-id="718c3-158">Qualsevol assignació de recursos que ja no sigui vàlida hauria de suprimir-se.</span><span class="sxs-lookup"><span data-stu-id="718c3-158">Any Resource Assignments that are no longer valid should be deleted.</span></span>

## <a name="project-task-dependency-relationships"></a><span data-ttu-id="718c3-159">Relacions de dependència de les tasques del projecte</span><span class="sxs-lookup"><span data-stu-id="718c3-159">Project task dependency relationships</span></span>
<span data-ttu-id="718c3-160">Per garantir l'actualització correcta, les relacions següents s'han de mantenir correctament:</span><span class="sxs-lookup"><span data-stu-id="718c3-160">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="718c3-161">Totes les dependències de les tasques del projecte han d'estar relacionades amb el mateix projecte.</span><span class="sxs-lookup"><span data-stu-id="718c3-161">All project task dependencies must be related to the same project.</span></span>
- <span data-ttu-id="718c3-162">Una tasca no pot tenir la mateixa dependència a la qual es fa referència més d'una vegada.</span><span class="sxs-lookup"><span data-stu-id="718c3-162">A task can't have the same dependency referenced more than once.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]