---
title: Com assigno un recurs que es pot reservar a una tasca en l'aplicació web
description: Informació general de les maneres en què podeu assignar recursos que es poden reservar.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 27a93c41243f300cadb632c697672180e5a3817b
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146561"
---
# <a name="how-do-i-assign-a-bookable-resource-to-a-task-in-the-web-app-project-service-app-v2x"></a><span data-ttu-id="9860a-103">Com assigno un recurs reservable a una a una tasca en l'aplicació web (v2.x de l'aplicació Project Service)?</span><span class="sxs-lookup"><span data-stu-id="9860a-103">How do I assign a bookable resource to a task in the web app (Project Service app v2.x)?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="9860a-104">Hi ha dues maneres d'assignar un recurs a una tasca al Project Service.</span><span class="sxs-lookup"><span data-stu-id="9860a-104">There are two ways to assign a resource to a task in Project Service.</span></span> <span data-ttu-id="9860a-105">Podeu reservar un recurs com a membre de l'equip i després assignar-lo a una tasca.</span><span class="sxs-lookup"><span data-stu-id="9860a-105">You can book a resource as a team member and then assign it to a task.</span></span> <span data-ttu-id="9860a-106">O bé, podeu crear un membre de l'equip genèric mitjançant l'assignació de rols en tasques, generar un equip i després, complir els requisits de seguretat amb un recurs amb nom.</span><span class="sxs-lookup"><span data-stu-id="9860a-106">Or, you can create a generic team member through role assignment on tasks, generate a team, and then fulfill the backing requirements with a named resource.</span></span>

<span data-ttu-id="9860a-107">Recordeu que si voleu assignar un recurs reservable a una tasca, el membre de l'equip de recursos reservables ha de tenir suficients reserves disponibles.</span><span class="sxs-lookup"><span data-stu-id="9860a-107">Note that if you’d like to assign a bookable resource to a task, the bookable resource team member must have enough available bookings.</span></span> <span data-ttu-id="9860a-108">L'estat de la reserva ha de ser tipus de confirmació Reserva fixa i Estat confirmat.</span><span class="sxs-lookup"><span data-stu-id="9860a-108">The status of the booking must be Commit Type Hard Book and Status Committed.</span></span> <span data-ttu-id="9860a-109">Si no hi ha prou reserves per al recurs, el Project Service elimina l'assignació i mostra el missatge d'error següent:</span><span class="sxs-lookup"><span data-stu-id="9860a-109">If there aren’t enough bookings for the resource, Project Service removes the assignment and displays the following error message:</span></span>

<span data-ttu-id="9860a-110">*No es pot assignar el recurs a la tasca: els recursos següents no tenen prou hores reservades per al projecte*</span><span class="sxs-lookup"><span data-stu-id="9860a-110">*Unable to assign resource to task - Following resource(s) do not have sufficient hours booked against project*</span></span>

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a><span data-ttu-id="9860a-111">Reservar un recurs com a membre de l'equip i després assignar-lo a una tasca</span><span class="sxs-lookup"><span data-stu-id="9860a-111">Book a resource as a team member and then assign the resource to a task</span></span>

<span data-ttu-id="9860a-112">Amb aquest mètode, afegiu un recurs a l'equip del projecte i després assigneu tasques al recurs en la planificació del projecte.</span><span class="sxs-lookup"><span data-stu-id="9860a-112">With this method you add a resource to the project team and then assign tasks to the resource in the project schedule.</span></span> <span data-ttu-id="9860a-113">Aquesta és la manera de fer-ho:</span><span class="sxs-lookup"><span data-stu-id="9860a-113">Here’s how you do this:</span></span>
1.  <span data-ttu-id="9860a-114">A la quadrícula de membres de l'equip, afegiu un nou membre de l'equip amb **Crea**.</span><span class="sxs-lookup"><span data-stu-id="9860a-114">On the team member grid, add a new team member by selecting **New**.</span></span>
2.  <span data-ttu-id="9860a-115">A la pantalla Creació ràpida d'un membre de l'equip, seleccioneu el nom del recurs que es pot reservar i establiu una funció.</span><span class="sxs-lookup"><span data-stu-id="9860a-115">On the Team Member Quick Create screen, select the bookable resource name and set a role.</span></span>
3.  <span data-ttu-id="9860a-116">Seleccioneu les dates **Des de** i **Fins a**.</span><span class="sxs-lookup"><span data-stu-id="9860a-116">Select the **From** and **To** dates.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="9860a-117">![Captura de pantalla de l'addició d'un membre a l'equip](media/FAQ-Resources-to-Tasks2-1.png "Captura de pantalla de l'addició d'un membre a l'equip")</span><span class="sxs-lookup"><span data-stu-id="9860a-117">![Screenshot of adding team member](media/FAQ-Resources-to-Tasks2-1.png "Screenshot of adding team member")</span></span>
 
4.  <span data-ttu-id="9860a-118">Seleccioneu un dels següents mètodes d'assignació per reservar el recurs:</span><span class="sxs-lookup"><span data-stu-id="9860a-118">Select one of the following allocation methods for booking the resource:</span></span>
    - <span data-ttu-id="9860a-119">**Capacitat total**: reserva la capacitat total del recurs per a les dates especificades des de i fins a.</span><span class="sxs-lookup"><span data-stu-id="9860a-119">**Full Capacity** books the resource’s full capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="9860a-120">**Capacitat percentual**: reserva el recurs per a un percentatge de capacitat del recurs per a les dates especificades des de i fins a.</span><span class="sxs-lookup"><span data-stu-id="9860a-120">**Percentage Capacity** books the resource for a percentage of the resource's capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="9860a-121">**Per hores distribuïdes uniformement**: reserva el recurs durant un nombre específic d'hores i les distribueix de manera uniforme per dia durant les dates especificades des de i fins a.</span><span class="sxs-lookup"><span data-stu-id="9860a-121">**By Hours Distribute Evenly** books the resource for a specified number of hours, distributing it evenly per day over the specified from and to dates.</span></span>
    - <span data-ttu-id="9860a-122">**Per hores amb la càrrega frontal**: reserva el recurs durant un nombre específic d'hores, carrega les hores per dia durant les dates especificades des de i fins a.</span><span class="sxs-lookup"><span data-stu-id="9860a-122">**By Hours Front Load** books the resource for a specified number of hours, front-loading the per-day hours over the specified from and to dates.</span></span>

    <span data-ttu-id="9860a-123">No seleccioneu **Cap** perquè afegeix el recurs a l'equip, però no crea cap reserva que absorbeixi la capacitat del recurs.</span><span class="sxs-lookup"><span data-stu-id="9860a-123">Don’t select **None** because it adds the resource to the team but doesn’t create any bookings that absorb the resource's capacity.</span></span>
5.  <span data-ttu-id="9860a-124">Seleccioneu **Desa**.</span><span class="sxs-lookup"><span data-stu-id="9860a-124">Select **Save**.</span></span>

    <span data-ttu-id="9860a-125">Recordeu que les hores de la reserva han de ser suficients per cobrir les hores d'esforç i els intervals de dates de les tasques a les que assigneu aquest recurs.</span><span class="sxs-lookup"><span data-stu-id="9860a-125">Note that the hours of the booking must be enough to cover the effort hours and date ranges of the tasks that you assign this resource to.</span></span> <span data-ttu-id="9860a-126">Si no estan alineades, no podreu assignar el recurs a la tasca.</span><span class="sxs-lookup"><span data-stu-id="9860a-126">If they aren’t in alignment, you can’t assign the resource to the task.</span></span>

6.  <span data-ttu-id="9860a-127">En l'estructura del desglossament del treball (WBS) per a la tasca, feu clic al menú desplegable de la cel·la de recursos.</span><span class="sxs-lookup"><span data-stu-id="9860a-127">On the work breakdown structure (WBS) for the task, click the resource cell dropdown.</span></span> <span data-ttu-id="9860a-128">Aleshores:</span><span class="sxs-lookup"><span data-stu-id="9860a-128">Then:</span></span> 

    1. <span data-ttu-id="9860a-129">Seleccioneu **Afegeix**.</span><span class="sxs-lookup"><span data-stu-id="9860a-129">Select **Add**.</span></span>
    2. <span data-ttu-id="9860a-130">Seleccioneu el menú desplegable de **Recursos** i el membre de l'equip que heu afegit anteriorment.</span><span class="sxs-lookup"><span data-stu-id="9860a-130">Select the dropdown under **Resources** and select the team member you added above.</span></span>
    3. <span data-ttu-id="9860a-131">Seleccioneu **D'acord**.</span><span class="sxs-lookup"><span data-stu-id="9860a-131">Select **OK**.</span></span> <span data-ttu-id="9860a-132">El membre de l'equip ara està assignat a la tasca.</span><span class="sxs-lookup"><span data-stu-id="9860a-132">The team member is now assigned to the task.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="9860a-133">![Captura de pantalla de l'addició de recursos amb el WBS](media/FAQ-Resources-to-Tasks2-2.png "Captura de pantalla de l'addició de recursos amb el WBS")</span><span class="sxs-lookup"><span data-stu-id="9860a-133">![Screenshot of adding resources with WBS](media/FAQ-Resources-to-Tasks2-2.png "Screenshot of adding resources with WBS")</span></span>
 
<span data-ttu-id="9860a-134">A la quadrícula de membres de l'equip, veureu el total d'hores assignades del recurs a l'apartat Hores assignades.</span><span class="sxs-lookup"><span data-stu-id="9860a-134">On the team member grid, you’ll see the aggregate of the resource’s assigned hours under Assigned Hours.</span></span> <span data-ttu-id="9860a-135">Serà menor o igual que les hores reservades per al recurs.</span><span class="sxs-lookup"><span data-stu-id="9860a-135">It will be less than or equal to the booked hours for the resource.</span></span> 

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="9860a-136">![Captura de pantalla de les hores assignades per a un recurs](media/FAQ-Resources-to-Tasks2-3.png "Captura de pantalla de les hores assignades per a un recurs")</span><span class="sxs-lookup"><span data-stu-id="9860a-136">![Screenshot of assigned hours for a resource](media/FAQ-Resources-to-Tasks2-3.png "Screenshot of assigned hours for a resource")</span></span>
 
<span data-ttu-id="9860a-137">Si la tasca que està intentant assignar al recurs comença després de la data de finalització de les reserves de recursos, el recurs no apareixerà en el menú desplegable.</span><span class="sxs-lookup"><span data-stu-id="9860a-137">If the task you’re attempting to assign to the resource starts after the end date of the resources bookings, the resource won’t appear in the dropdown.</span></span>

<span data-ttu-id="9860a-138">Recordeu que podeu assignar un recurs a més hores que les hores reservades si té alguna capacitat restant sense assignar.</span><span class="sxs-lookup"><span data-stu-id="9860a-138">Note that you can assign a resource to more hours than their booked hours if the resource has some remaining unassigned capacity.</span></span> <span data-ttu-id="9860a-139">En aquest cas, el recurs només s'assignarà parcialment fins arribar a les seves reserves.</span><span class="sxs-lookup"><span data-stu-id="9860a-139">In this case the resource will only be partially assigned up to their bookings.</span></span> <span data-ttu-id="9860a-140">Podeu veure aquestes hores de tasques restants sense assignar si afegiu la columna Hores sense personal a l'estructura del desglossament del treball.</span><span class="sxs-lookup"><span data-stu-id="9860a-140">You can see these remaining unassigned task hours by adding the Unstaffed Hours column to the work breakdown structure.</span></span>

<span data-ttu-id="9860a-141">Si els recursos s'assignen a les hores reservades (les hores reservades són iguals a les hores assignades), apareixerà el següent missatge d'error quan intenteu assignar-los més tasques:</span><span class="sxs-lookup"><span data-stu-id="9860a-141">If resources are assigned to their booked hours (their booked hours equals their assigned hours), you’ll see the following error message when you attempt to assign them further tasks:</span></span>

<span data-ttu-id="9860a-142">*No es pot assignar el recurs a la tasca: els recursos següents no tenen prou hores reservades per al projecte.*</span><span class="sxs-lookup"><span data-stu-id="9860a-142">*Unable to assign resource to task - Following resource(s) do not have sufficient hours booked against project.*</span></span>

<span data-ttu-id="9860a-143">A més, el membre predeterminat de l'equip de l'administrador del projecte que s'agrega a l'equip quan es crea el projecte s'agrega sense reserves i no es pot assignar a cap tasca.</span><span class="sxs-lookup"><span data-stu-id="9860a-143">Additionally, the default project manager team member that is added to the team when you create the project is added without any bookings and can’t be assigned to any task.</span></span> <span data-ttu-id="9860a-144">No es mostraran al menú desplegable de recursos per a tasques.</span><span class="sxs-lookup"><span data-stu-id="9860a-144">They won’t show up in the resource dropdown for tasks.</span></span>

<span data-ttu-id="9860a-145">Si voleu assignar aquest recurs, heu d'eliminar-les de l'equip i després tornar a afegir-les amb un mètode d'assignació diferent a Cap.</span><span class="sxs-lookup"><span data-stu-id="9860a-145">If you want to assign this resource, you need to remove them from the team and then re-add them with an allocation method other than None.</span></span> <span data-ttu-id="9860a-146">La raó per la qual s'agreguen a l'equip quan es crea el projecte és perquè un projecte tingui almenys un aprovador de projectes per defecte.</span><span class="sxs-lookup"><span data-stu-id="9860a-146">The reason they’re added to the team when the project is created is so that a project has at least one project approver by default.</span></span>

## <a name="create-a-generic-team-member-through-role-assignment-on-tasks"></a><span data-ttu-id="9860a-147">Crear un membre de l'equip genèric a través de l'assignació de rols en les tasques</span><span class="sxs-lookup"><span data-stu-id="9860a-147">Create a generic team member through role assignment on tasks</span></span>

<span data-ttu-id="9860a-148">Aquest mètode assegura que els recursos tinguin suficients reserves per a les tasques.</span><span class="sxs-lookup"><span data-stu-id="9860a-148">This method assures that resources have enough bookings for tasks.</span></span> <span data-ttu-id="9860a-149">En primer lloc, heu de crear un contenidor o un recurs genèric que descrigui les característiques del recurs amb nom en el qual voleu treballar en les tasques mitjançant un equip després d'assignar rols a les tasques.</span><span class="sxs-lookup"><span data-stu-id="9860a-149">First, you create a placeholder or generic resource that describes the characteristics of the named resource you ultimately want to work on the tasks by generating a team after assigning roles to tasks.</span></span> <span data-ttu-id="9860a-150">Aquesta és la manera de fer-ho:</span><span class="sxs-lookup"><span data-stu-id="9860a-150">Here’s how you do this:</span></span>

1. <span data-ttu-id="9860a-151">A l'estructura del desglossament del treball, seleccioneu una tasca.</span><span class="sxs-lookup"><span data-stu-id="9860a-151">On the work breakdown structure, select a task.</span></span>
2. <span data-ttu-id="9860a-152">Seleccioneu la icona desplegable **Rol assignat** a la cel·la del recurs.</span><span class="sxs-lookup"><span data-stu-id="9860a-152">Select the **Assigned Role** dropdown icon in the resource cell.</span></span>
3. <span data-ttu-id="9860a-153">Seleccioneu la llista desplegable **Funció** i la funció per al recurs genèric.</span><span class="sxs-lookup"><span data-stu-id="9860a-153">Select the **Role** dropdown and select the role for the generic resource.</span></span>
4. <span data-ttu-id="9860a-154">Seleccioneu **D'acord**.</span><span class="sxs-lookup"><span data-stu-id="9860a-154">Select **OK**.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="9860a-155">![Captura de pantalla de l'ús del WBS per afegir un recurs](media/FAQ-Resources-to-Tasks2-4.png "Captura de pantalla de l'ús del WBS per afegir un recurs")</span><span class="sxs-lookup"><span data-stu-id="9860a-155">![Screenshot of using WBS to add resource](media/FAQ-Resources-to-Tasks2-4.png "Screenshot of using WBS to add resource")</span></span>
 
<span data-ttu-id="9860a-156">Un cop hagueu completat l'assignació de funcions a les tasques al WBS, seleccioneu **Genera un equip de projecte**.</span><span class="sxs-lookup"><span data-stu-id="9860a-156">Once you’ve completed assigning roles to the tasks in the WBS, select **Generate Project Team**.</span></span> <span data-ttu-id="9860a-157">El Project Service crea la quantitat mínima de membres genèrics de l'equip en funció dels rols, les unitats d'organització de recursos i el calendari del projecte amb les tasques assignades.</span><span class="sxs-lookup"><span data-stu-id="9860a-157">Project Service creates the minimum number of generic team members based on the roles, resourcing organization units, and project calendar by aggregating the task assignments.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="9860a-158">![Captura de pantalla de la generació d'un equip de projecte](media/FAQ-Resources-to-Tasks2-5.png "Captura de pantalla de la generació d'un equip de projecte")</span><span class="sxs-lookup"><span data-stu-id="9860a-158">![Screenshot of generating project team](media/FAQ-Resources-to-Tasks2-5.png "Screenshot of generating project team")</span></span>
 
<span data-ttu-id="9860a-159">A la quadrícula Membre de l'equip, veureu els recursos del tipus Recurs genèric amb el nom de la funció i la posició.</span><span class="sxs-lookup"><span data-stu-id="9860a-159">On the Team Member grid, you’ll see resources of the Generic Resource type with the role and position name.</span></span> <span data-ttu-id="9860a-160">Si calen dos recursos perquè una funció completi la feina, la funció Generar equip crea dos membres de l'equip i fa servir el nom de la posició per distingir-los.</span><span class="sxs-lookup"><span data-stu-id="9860a-160">If two resources are needed for a role to complete the work, the Generate Team feature creates two team members and uses position name to set them apart.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="9860a-161">![Captura de pantalla de l'addició de dos recursos genèrics](media/FAQ-Resources-to-Tasks2-6.png "Captura de pantalla de l'addició de dos recursos genèrics")</span><span class="sxs-lookup"><span data-stu-id="9860a-161">![Screenshot of adding two generic resources](media/FAQ-Resources-to-Tasks2-6.png "Screenshot of adding two generic resources")</span></span>
 
<span data-ttu-id="9860a-162">Podeu obrir el requisit del recurs de suport per al membre genèric de l'equip mitjançant l'enllaç que apareix a Requisit de recursos.</span><span class="sxs-lookup"><span data-stu-id="9860a-162">You can open the backing resource requirement for the generic team member by selecting the link under Resource Requirement.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="9860a-163">![Captura de pantalla de l'obertura d'un requisit de recurs de suport](media/FAQ-Resources-to-Tasks2-7.png "Captura de pantalla de l'obertura d'un requisit de recurs de suport")</span><span class="sxs-lookup"><span data-stu-id="9860a-163">![Screenshot of opening backing resource requirement](media/FAQ-Resources-to-Tasks2-7.png "Screenshot of opening backing resource requirement")</span></span>

<span data-ttu-id="9860a-164">Seleccioneu **Reserva** per al recurs genèric i després podeu utilitzar el tauler de programació per buscar i reservar un recurs real.</span><span class="sxs-lookup"><span data-stu-id="9860a-164">Select **Book** for the generic resource, and then you can use the schedule board to find and book a real resource.</span></span> <span data-ttu-id="9860a-165">També podeu enviar el requisit de compliment per un administrador de recursos si seleccioneu **Envia sol·licitud**.</span><span class="sxs-lookup"><span data-stu-id="9860a-165">You can also submit the requirement for fulfillment by a resource manager by selecting **Submit Request**.</span></span>

<span data-ttu-id="9860a-166">Quan el recurs genèric es compleix amb un recurs amb nom, el genèric s'elimina de l'equip i les assignacions de tasques s'assignen al recurs amb nom que va complir els requisits de recursos del recurs genèric.</span><span class="sxs-lookup"><span data-stu-id="9860a-166">When the generic resource is fulfilled with a named resource, the generic resource is removed from the team and the task assignments for the generic resource are assigned to the named resource that fulfilled the generic resource’s resource requirement.</span></span>
 

