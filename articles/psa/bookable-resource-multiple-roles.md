---
title: Càlcul de les vendes i els costos del projecte quan un recurs reservable té diverses funcions en un projecte
description: En aquest tema es proporciona informació sobre la manera com es poden utilitzar les dimensions de preus per admetre els preus i costos d'un recurs amb diverses funcions en un projecte.
author: rumant
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
ms.openlocfilehash: 8ddc827a4170c5576c0a4350b51e6a119094ac50
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072264"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-mulitple-roles-on-a-project"></a><span data-ttu-id="e319e-103">Càlcul de les vendes i els costos del projecte quan un recurs reservable té diverses funcions en un projecte</span><span class="sxs-lookup"><span data-stu-id="e319e-103">Estimate project sales and costs when a bookable resource fills mulitple roles on a project</span></span> 

<span data-ttu-id="e319e-104">Les empreses basades en projectes tenen sovint la necessitat que un recurs tingui diverses funcions en un projecte.</span><span class="sxs-lookup"><span data-stu-id="e319e-104">Project-based companies often have the need for one resource to perform mulitple roles on a project.</span></span> <span data-ttu-id="e319e-105">Cadascuna d'aquestes funcions podria tenir un preu i un cost diferent, la qual cosa significa que el mateix recurs en el projecte podria rebre una estimació econòmica diferent en funció de les tarifes de facturació i cost de cadascuna de les funcions.</span><span class="sxs-lookup"><span data-stu-id="e319e-105">Each of these roles could be priced and costed differently which means the same resource's time on the project could get a different financial estimate depending on the bill and cost rates for each of the roles.</span></span> <span data-ttu-id="e319e-106">El Project Service Automation permet la configuració dels valors al registre de membres de l'equip per al recurs amb nom i permet diverses substitucions en cadascuna de les tasques a les quals s'assigna el membre de l'equip.</span><span class="sxs-lookup"><span data-stu-id="e319e-106">Project Service Automation allows the setup of the values on the team member record for the named resource and allows for different overrides on each of the tasks that the team member is assigned to.</span></span>

<span data-ttu-id="e319e-107">A l'exemple següent s'explica com la simple substitució d'aquest valor permet que un recurs tingui diverses funcions en un projecte que tingui diferents tarifes de cost i facturació.</span><span class="sxs-lookup"><span data-stu-id="e319e-107">The following example  explains how the simple override of this value allows a resource to have multiple roles on a project with different cost and bill rates.</span></span>

## <a name="create-tasks"></a><span data-ttu-id="e319e-108">Creació de tasques</span><span class="sxs-lookup"><span data-stu-id="e319e-108">Create tasks</span></span>
<span data-ttu-id="e319e-109">Creeu dues tasques de projecte de 40 hores cadascuna, la tasca A i la tasca B. Seleccioneu la tasca A com a antecessora de la tasca B.</span><span class="sxs-lookup"><span data-stu-id="e319e-109">Create two project tasks for 40 hours each, Task A and Task B. Select Task A as a predecessor to Task B.</span></span>

## <a name="set-up-role-and-organization-unit-for-a-generic-project-team-member"></a><span data-ttu-id="e319e-110">Configurar la funció i unitat organitzativa per a un membre de l'equip del projecte genèric</span><span class="sxs-lookup"><span data-stu-id="e319e-110">Set up Role and Organization Unit for a generic project team member</span></span>

1. <span data-ttu-id="e319e-111">A la pàgina **Planificació** , seleccioneu la fila **Tasca** per a la tasca A.</span><span class="sxs-lookup"><span data-stu-id="e319e-111">On the **Schedule** page, select the **Task** row for Task A.</span></span> 
2. <span data-ttu-id="e319e-112">Al camp **Recursos** , seleccioneu **Crea** a la llista desplegable.</span><span class="sxs-lookup"><span data-stu-id="e319e-112">In the **Resources** field, select **Create** in the drop-down list.</span></span>
3. <span data-ttu-id="e319e-113">A la pàgina **Creació ràpida del membre de l'equip** , especifiqueu els atributs del membre de l'equip genèric que pot dur a terme aquesta tasca.</span><span class="sxs-lookup"><span data-stu-id="e319e-113">On the **Team Member Quick Create** page, specify the attributes of the generic team member who can perform this task.</span></span>
4. <span data-ttu-id="e319e-114">Seleccioneu la funció i la unitat organitzativa adients i, a continuació, seleccioneu **Desa i tanca**.</span><span class="sxs-lookup"><span data-stu-id="e319e-114">Select the appropriate role and organizational unit, and then select **Save and Close**.</span></span> <span data-ttu-id="e319e-115">Es crea un membre genèric de l'equip i s'assigna a aquesta tasca.</span><span class="sxs-lookup"><span data-stu-id="e319e-115">A generic team member is created and assigned to this task.</span></span> 

<span data-ttu-id="e319e-116">Repetiu aquests passos per a la tasca B i assegureu-vos que la funció i la unitat organitzativa del membre de l'equip genèric creades per a la tasca B siguin diferents de la tasca A.</span><span class="sxs-lookup"><span data-stu-id="e319e-116">Repeat these steps for Task B and make sure that the role and organizational unit on the generic team member created for Task B is different than Task A.</span></span> 

## <a name="set-up-role-and-organization-unit-for-a-project-task"></a><span data-ttu-id="e319e-117">Configurar la funció i unitat organitzativa per a una tasca del projecte</span><span class="sxs-lookup"><span data-stu-id="e319e-117">Set up role and organization unit for a project task</span></span>

1. <span data-ttu-id="e319e-118">Després de crear la tasca A, seleccioneu la tasca i, a continuació, seleccioneu **Edita la tasca**.</span><span class="sxs-lookup"><span data-stu-id="e319e-118">After you create Task A, select the task, and then select **Edit task**.</span></span>
2. <span data-ttu-id="e319e-119">A la pàgina **Detalls de la tasca** , localitzeu els camps **Funció** i **Unitat organitzativa** i afegiu els valors necessaris d'un recurs que ha de dur a terme aquesta tasca.</span><span class="sxs-lookup"><span data-stu-id="e319e-119">On the **Task Details** page, find the **Role** and **Organizational Unit** fields, add the values that are required of a resource that would perform this task.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="e319e-120">Si completeu aquests escenaris amb les dades de demostració del Project Service Automation, seleccioneu **Cap de consultoria** per a la funció i **Fabrikam US** com a unitat organitzativa.</span><span class="sxs-lookup"><span data-stu-id="e319e-120">If you are completing this scenarios using Project Service Automation demo data, select **Consulting Lead** for the role, and **Fabrikam US** as the organizational unit.</span></span>

3. <span data-ttu-id="e319e-121">Seleccioneu la tasca B i, a continuació, **Edita la tasca**.</span><span class="sxs-lookup"><span data-stu-id="e319e-121">Select Task B and then select **Edit task**.</span></span>
4. <span data-ttu-id="e319e-122">A la pàgina **Detalls de la tasca** , localitzeu els camps **Funció** i **Unitat organitzativa** i afegiu els valors necessaris d'un recurs que ha de dur a terme aquesta tasca.</span><span class="sxs-lookup"><span data-stu-id="e319e-122">On the **Task Details** page, find the **Role** and **Organizational Unit** fields, add the values that are required of a resource that would perform this task.</span></span> <span data-ttu-id="e319e-123">Assegureu-vos que els valors dels camps **Funció** i **Unitat organitzativa** siguin diferents per a la tasca B i per a la tasca A.</span><span class="sxs-lookup"><span data-stu-id="e319e-123">Make sure that the values in the **Role** and **Organizational Unit** fields are different for Task B from those for Task A.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="e319e-124">Si completeu aquests escenaris amb les dades de demostració del Project Service Automation, seleccioneu **Tècnic de xarxa** per a la funció i **Fabrikam US** com a unitat organitzativa.</span><span class="sxs-lookup"><span data-stu-id="e319e-124">If you are completing this scenarios using Project Service Automation demo data, select **Network Technician** for the role, and **Fabrikam US** as the organizational unit.</span></span>

5. <span data-ttu-id="e319e-125">Deseu i tanqueu la pàgina **Detalls de la tasca**.</span><span class="sxs-lookup"><span data-stu-id="e319e-125">Save and close the **Task Details** page.</span></span> 

## <a name="team-member-and-estimates-behaviour"></a><span data-ttu-id="e319e-126">Membre de l'equip i comportament de les estimacions</span><span class="sxs-lookup"><span data-stu-id="e319e-126">Team member and estimates behaviour</span></span> 

1. <span data-ttu-id="e319e-127">A la pàgina **Detalls de la tasca** , a **Membre de l'equip** , seleccioneu els dos membres de l'equip genèrics i, a continuació, seleccioneu **Genera els requisits**.</span><span class="sxs-lookup"><span data-stu-id="e319e-127">On the **Task Details** page, on the **Team Member** , select the two generic team Members and then select **Generate Requirements**.</span></span> <span data-ttu-id="e319e-128">Això generarà els requisits de recursos.</span><span class="sxs-lookup"><span data-stu-id="e319e-128">This will generate resource requirements.</span></span> 
2. <span data-ttu-id="e319e-129">Seleccioneu la fila de membre de l'equip per al **Cap de consultoria** i, a continuació, seleccioneu **Reserva**.</span><span class="sxs-lookup"><span data-stu-id="e319e-129">Select the team member row for **Consulting Lead** and then select **Book**.</span></span> <span data-ttu-id="e319e-130">El tauler de planificació s'obre i reserva un recurs al requisit.</span><span class="sxs-lookup"><span data-stu-id="e319e-130">The schedule board opens and books a resource to that requirement.</span></span>
3. <span data-ttu-id="e319e-131">Seleccioneu la fila de membre de l'equip per al **Tècnic de xarxa** i, a continuació, seleccioneu **Reserva**.</span><span class="sxs-lookup"><span data-stu-id="e319e-131">Select the team member row for **Network Technician** and the select **Book**.</span></span> <span data-ttu-id="e319e-132">El tauler de planificació s'obre i reserva el mateix recurs al requisit.</span><span class="sxs-lookup"><span data-stu-id="e319e-132">The schedule board opens and books the same resource on that requirement.</span></span>

### <a name="team-member-grid"></a><span data-ttu-id="e319e-133">Quadrícula de membre de l'equip</span><span class="sxs-lookup"><span data-stu-id="e319e-133">Team Member grid</span></span> 
<span data-ttu-id="e319e-134">A la quadrícula **Membre de l'equip** , fixeu-vos que els dos registres de membres de l'equip genèrics s'han suprimit i s'han substituït per un recurs.</span><span class="sxs-lookup"><span data-stu-id="e319e-134">On the **Team Member** grid, notice that the two generic team member records are deleted and have been replaced one resource.</span></span> <span data-ttu-id="e319e-135">Hi ha un conjunt de valors per a aquest recurs que mostra un conjunt de valors per defecte per a **Funció** i **Unitat organitzativa**.</span><span class="sxs-lookup"><span data-stu-id="e319e-135">There is one set of values for that resource that shows a default set of values for **Role** and **Organizational Unit**.</span></span>
<span data-ttu-id="e319e-136">Quan expandiu la fila d'aquest registre de membre de l'equip, podeu veure assignacions diferents al registre de membre de l'equip per a les dues tasques.</span><span class="sxs-lookup"><span data-stu-id="e319e-136">When you expand the row of that Team Member record, you can see distinct assignments on the team member record for both of those tasks.</span></span> <span data-ttu-id="e319e-137">Cada fila d'assignació té valors específics de la tasca per a **Funció** i **Unitat organitzativa**.</span><span class="sxs-lookup"><span data-stu-id="e319e-137">Each assignment row has task specific values for **Role** and **Organizational Unit**.</span></span> 

### <a name="estimates-grid"></a><span data-ttu-id="e319e-138">Quadrícula d’estimacions</span><span class="sxs-lookup"><span data-stu-id="e319e-138">Estimates grid</span></span> 
<span data-ttu-id="e319e-139">Quan navegueu a la quadrícula **Estimacions** , us adonareu que ambdues assignacions del mateix recurs tenen un preu diferent.</span><span class="sxs-lookup"><span data-stu-id="e319e-139">When you navigate to the **Estimates** grid, you will notice that both assignments for the same resource are priced differently.</span></span>
<span data-ttu-id="e319e-140">L'assignació del recurs a la tasca A rep el preu en funció del valor de l'atribut **Funció** de **Cap de consultoria**.</span><span class="sxs-lookup"><span data-stu-id="e319e-140">The assignment for the resource on Task A is priced using the **Role** attribute value of **Consulting Lead**.</span></span> <span data-ttu-id="e319e-141">L'assignació del mateix recurs a la tasca B rep el preu en funció del valor de l'atribut **Funció** de **Tècnic de xarxa**.</span><span class="sxs-lookup"><span data-stu-id="e319e-141">The assignment for the same resource on Task B is priced using the **Role** attribute value of **Network Technician**.</span></span>





