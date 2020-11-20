---
title: Reservar recursos que es poden reservar a un equip de projecte i assignar tasques
description: En aquest tema es proporciona informació sobre la reserva de recursos amb nom a equips de projecte i assignar-los a tasques.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
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
ms.openlocfilehash: 0300c494a3294b26e2de6bbfa1dd50a76bb72651
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130161"
---
# <a name="book-named-bookable-resources-to-a-project-team-and-assign-tasks"></a><span data-ttu-id="da2e5-103">Reservar recursos que es poden reservar a un equip de projecte i assignar tasques</span><span class="sxs-lookup"><span data-stu-id="da2e5-103">Book named bookable resources to a project team and assign tasks</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="da2e5-104">Podeu afegir un recurs amb nom a l'equip del projecte reservant-lo directament a l'equip.</span><span class="sxs-lookup"><span data-stu-id="da2e5-104">You can  add a named resource to your project team by booking them directly onto the team.</span></span> <span data-ttu-id="da2e5-105">Per fer-ho, feu els passos següents:</span><span class="sxs-lookup"><span data-stu-id="da2e5-105">To do this, complete the following steps.</span></span>

1. <span data-ttu-id="da2e5-106">Al Project Service Automation, aneu a **Projectes** i, a continuació, seleccioneu el projecte obert al qual voleu reservar.</span><span class="sxs-lookup"><span data-stu-id="da2e5-106">In  Project Service Automation, go to **Projects**, and select the open the project that you are booking for.</span></span>
2. <span data-ttu-id="da2e5-107">A la pàgina **Projecte**, a la pestanya **Equip**, feu clic a **Crea**.</span><span class="sxs-lookup"><span data-stu-id="da2e5-107">On the **Project** page, on the **Team** tab, click **New**.</span></span> 

![Afegir un membre de l'equip des de la pestanya Equip](media/RM-how-to-1.png)

3. <span data-ttu-id="da2e5-109">Al quadre de diàleg **Creació ràpida de membre de l'equip**, seleccioneu el recurs que es pot reservar.</span><span class="sxs-lookup"><span data-stu-id="da2e5-109">In the **Quick Create Project Team Member** dialog box, select the bookable resource.</span></span> <span data-ttu-id="da2e5-110">El camp **Funció** s'emplenarà amb la funció per defecte del recurs si en té assignada una.</span><span class="sxs-lookup"><span data-stu-id="da2e5-110">The **Role** field will populate with the resource's default role if they have one assigned.</span></span> <span data-ttu-id="da2e5-111">Podeu canviar la funció si cal.</span><span class="sxs-lookup"><span data-stu-id="da2e5-111">You can change the role if needed.</span></span> 
4. <span data-ttu-id="da2e5-112">Seleccioneu les dates d'origen i finalització en què es necessitaran els recursos i seleccioneu el mètode d'assignació de la capacitat del recurs.</span><span class="sxs-lookup"><span data-stu-id="da2e5-112">Select the from and to dates that the resource will be needed and select the allocation method of the resource's capacity.</span></span> 
5. <span data-ttu-id="da2e5-113">Si voleu que el membre de l'equip sigui un aprovador de projecte, seleccioneu **Sí** al camp **Aprovador de projectes**.</span><span class="sxs-lookup"><span data-stu-id="da2e5-113">If you want the team member to be a project approver, select **Yes** in the **Project Approver** field.</span></span> <span data-ttu-id="da2e5-114">Això significarà que el membre de l'equip pot aprovar les entrades de despesa i de despeses enviades per a aquest projecte.</span><span class="sxs-lookup"><span data-stu-id="da2e5-114">This will mean that the team member can approve submitted time and expense entries for this project.</span></span> 
6. <span data-ttu-id="da2e5-115">Feu clic a **Desa**.</span><span class="sxs-lookup"><span data-stu-id="da2e5-115">Click **Save**.</span></span>

![Afegir un membre de l'equip al formulari de creació ràpida](media/RM-how-to-2.png)


<span data-ttu-id="da2e5-117">Ara podeu assignar el recurs reservat a les tasques del projecte.</span><span class="sxs-lookup"><span data-stu-id="da2e5-117">You can now assign the booked resource to tasks on the project.</span></span> <span data-ttu-id="da2e5-118">A la pàgina **Projecte**, feu clic a la pestanya **Planificació** per assignar tasques al recurs nou.</span><span class="sxs-lookup"><span data-stu-id="da2e5-118">On the **Project** page, click the **Schedule** tab to assign tasks to the new resource.</span></span> <span data-ttu-id="da2e5-119">El selector de recursos que s'inicia des del camp **Recursos** de la quadrícula de tasques mostrarà els membres de l'equip que podeu seleccionar.</span><span class="sxs-lookup"><span data-stu-id="da2e5-119">The resource picker that is launched from the **Resources** field in the task grid will show the team members that you can select.</span></span>

![Assignar un membre d'un equip a una tasca de la pestanya Planificació](media/RM-how-to-3.png)

<span data-ttu-id="da2e5-121">A la versió 3 del Project Service Automation (PSA), les reserves de recursos i les assignacions de tasques no estan vinculades estretament.</span><span class="sxs-lookup"><span data-stu-id="da2e5-121">In version 3 for Project Service Automation (PSA), resource bookings and task assignments are not tightly coupled.</span></span> <span data-ttu-id="da2e5-122">Això vol dir que quan utilitzeu el selector de recursos de la planificació, podeu assignar tasques als membres de l'equip durant més hores de les cobertes per les reserves en el projecte.</span><span class="sxs-lookup"><span data-stu-id="da2e5-122">This means that when you use the resource picker in the schedule, you can assign tasks to team members for more hours than their bookings cover on the project.</span></span>
<span data-ttu-id="da2e5-123">Podeu veure les diferències entre les reserves dels membres de l'equip i les assignacions a la pestanya **Equip** o a la pestanya **Conciliació de recursos**. També podeu conciliar les diferències entre reserves i assignacions per als recursos en un nivell més detallat.</span><span class="sxs-lookup"><span data-stu-id="da2e5-123">You can see the differences between team member bookings and assignments on the **Team** tab or on the **Resource Reconciliation** tab. You can also reconcile the differences between bookings and assignments for resources at a more detailed level.</span></span>

![Pestanya Conciliació de recursos](media/RM-how-to-4.png)

<span data-ttu-id="da2e5-125">També podeu utilitzar el selector de recursos a la pestanya **Planificació** per cercar i seleccionar altres recursos que encara no formen part de l'equip del projecte.</span><span class="sxs-lookup"><span data-stu-id="da2e5-125">You can also use the resource picker on the **Schedule** tab to search for and select bookable resources that are not already part of the project team.</span></span> <span data-ttu-id="da2e5-126">Es mostren al selector de recursos com a **Altres recursos**.</span><span class="sxs-lookup"><span data-stu-id="da2e5-126">These are shown in the resource picker as **Other Resources**.</span></span>

![Assignar un recurs no membre de l'equip a una tasca](media/RM-how-to-5.png)

<span data-ttu-id="da2e5-128">En fer-ho, el recurs s'afegeix a l'equip del projecte i se l'assigna a la tasca, però no es genera cap reserva.</span><span class="sxs-lookup"><span data-stu-id="da2e5-128">When you do this, the resource is added to the project team and assigned to the task, but no bookings are generated.</span></span>

![Membre de l'equip amb assignacions i sense reserves](media/RM-how-to-6.png)

<span data-ttu-id="da2e5-130">Podeu utilitzar la capacitat d'ampliació de la reserva de la pestanya **Conciliació** o el **Tauler de planificació** per reservar la capacitat del recurs al projecte.</span><span class="sxs-lookup"><span data-stu-id="da2e5-130">You can use the **Reconciliation** tab’s extend booking capability or the **Schedule Board** to book the resource’s capacity to the project.</span></span>

![Ampliar les reserves d'un membre de l'equip a la pestanya Conciliació de recursos](media/RM-how-to-7.png)

<span data-ttu-id="da2e5-132">Després d'haver reservat un membre de l'equip al vostre projecte, podeu utilitzar el manteniment de les reserves o utilitzar el Tauler de planificació directament per administrar les seves reserves.</span><span class="sxs-lookup"><span data-stu-id="da2e5-132">After a team member is booked on your project, you can use maintain bookings or use the Schedule Board directly to manage their bookings.</span></span>
