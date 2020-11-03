---
title: Assignar un recurs a una tasca
description: En aquest tema es proporciona informació sobre la manera d'assignar recursos a tasques.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 9/27/2019
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
ms.openlocfilehash: 77f13d1e96b76dfea241fbf7a67d5676582f0235
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072401"
---
# <a name="assign-a-resource-to-a-task"></a><span data-ttu-id="01347-103">Assignar un recurs a una tasca</span><span class="sxs-lookup"><span data-stu-id="01347-103">Assign a resource to a task</span></span>

<span data-ttu-id="01347-104">Hi ha tres maneres d'assignar un recurs a una tasca al Microsoft Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="01347-104">There are three ways to assign a resource to a task in Microsoft Dynamics 365 Project Service Automation.</span></span>

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a><span data-ttu-id="01347-105">Reservar un recurs com a membre de l'equip i després assignar-lo a una tasca</span><span class="sxs-lookup"><span data-stu-id="01347-105">Book a resource as a team member, and then assign the resource to a task</span></span>

<span data-ttu-id="01347-106">Podeu afegir un recurs a l'equip del projecte i després assignar-lo a tasques en la planificació del projecte.</span><span class="sxs-lookup"><span data-stu-id="01347-106">You can add a resource to the project team, and then assign the resource to tasks in the project schedule.</span></span>

1. <span data-ttu-id="01347-107">A la pestanya **Membre de l'equip** , afegiu un nou membre de l'equip amb **Crea**.</span><span class="sxs-lookup"><span data-stu-id="01347-107">On the **Team Member** tab, add a new team member by selecting **New**.</span></span> 

2. <span data-ttu-id="01347-108">S'obre la subfinestra **Creació ràpida d'un membre de l'equip** , on es pot seleccionar el nom del recurs que es pot reservar i establir una funció.</span><span class="sxs-lookup"><span data-stu-id="01347-108">The **Team Member Quick Create** panel opens, where you can select the bookable resource name and set a role.</span></span> 

    <span data-ttu-id="01347-109">Seleccioneu un dels següents mètodes d'assignació per a la reserva del recurs:</span><span class="sxs-lookup"><span data-stu-id="01347-109">Select one of the following allocation methods for the resource’s booking:</span></span>

    - <span data-ttu-id="01347-110">**Capacitat total** : reserva la capacitat total del recurs per a les dates especificades des de i fins a.</span><span class="sxs-lookup"><span data-stu-id="01347-110">**Full Capacity** books the resource’s full capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="01347-111">**Capacitat percentual** : reserva el recurs per a un percentatge de capacitat del recurs per a les dates especificades des de i fins a.</span><span class="sxs-lookup"><span data-stu-id="01347-111">**Percentage Capacity** books the resource for a percentage of the resource's capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="01347-112">**Per hores distribuïdes uniformement** : reserva el recurs durant un nombre específic d'hores i les distribueix de manera uniforme per dia durant les dates d'inici i finalització especificades.</span><span class="sxs-lookup"><span data-stu-id="01347-112">**By Hours Distribute Evenly** books the resource for a specified number of hours, distributing them evenly per day over the specified from and to dates.</span></span>
    - <span data-ttu-id="01347-113">**Per hores amb la càrrega frontal** : reserva el recurs durant un nombre específic d'hores, carrega les hores per dia durant les dates especificades des de i fins a.</span><span class="sxs-lookup"><span data-stu-id="01347-113">**By Hours Front Load** books the resource for a specified number of hours, front-loading the per-day hours over the specified from and to dates.</span></span>
    - <span data-ttu-id="01347-114">**Cap** : afegeix el recurs a l'equip, però no crea cap reserva que absorbeixi la seva capacitat.</span><span class="sxs-lookup"><span data-stu-id="01347-114">**None** adds the resource to the team but doesn’t create any bookings that absorb their capacity.</span></span>

3. <span data-ttu-id="01347-115">A la quadrícula **Planificació** per a una tasca, seleccioneu la icona **Recurs** a la cel·la de recursos i, a continuació, a **Membres de l'equip** seleccioneu el membre de l'equip que acabeu d'afegir.</span><span class="sxs-lookup"><span data-stu-id="01347-115">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell, and then under **Team Members** , select the team member you just added.</span></span> 

> [!NOTE]
> <span data-ttu-id="01347-116">A les pestanyes **Membre de l'equip** i **Conciliació** , el recurs mostra les hores reservades i les assignades.</span><span class="sxs-lookup"><span data-stu-id="01347-116">On the **Team Member** and **Reconciliation** tabs, the resource shows booked and assigned hours.</span></span> <span data-ttu-id="01347-117">Aquestes hores han de ser iguals, però no són obligatòries perquè les reserves i les assignacions no estan estretament unides.</span><span class="sxs-lookup"><span data-stu-id="01347-117">The hours should be the same, but it isn't required as bookings and assignments are not tightly coupled.</span></span> <span data-ttu-id="01347-118">La pestanya **Conciliació** aporta detalls quan són diferents, com quan s'assignen a un recurs més hores de les que heu reservat.</span><span class="sxs-lookup"><span data-stu-id="01347-118">The **Reconciliation** tab gives you details when they are different, such as when you assign a resource more hours than you have booked.</span></span> <span data-ttu-id="01347-119">Si cal, podeu prendre mesures correctives ampliant les reserves del recurs o canviar-ne l'assignació.</span><span class="sxs-lookup"><span data-stu-id="01347-119">If needed, you can correct the information by extending the resource's bookings or changing the assignment.</span></span>

## <a name="create-a-generic-team-member-through-task-assignment"></a><span data-ttu-id="01347-120">Crear un membre de l'equip genèric a través de l'assignació de tasques</span><span class="sxs-lookup"><span data-stu-id="01347-120">Create a generic team member through task assignment</span></span>

<span data-ttu-id="01347-121">Quan creeu un membre d'equip genèric a través d'una assignació de tasques, heu de crear un contenidor o un recurs genèric que descrigui les característiques del recurs amb nom en el qual voleu treballar en les tasques.</span><span class="sxs-lookup"><span data-stu-id="01347-121">When you create a generic team member through task assignment, you create a placeholder or generic resource that describes the characteristics of the named resource you ultimately want to work on the tasks.</span></span> <span data-ttu-id="01347-122">A continuació, genereu un requisit (o envieu una sol·licitud amb el requisit) que s'utilitzi per buscar i reservar el recurs amb nom.</span><span class="sxs-lookup"><span data-stu-id="01347-122">You then generate a requirement (or submit a request using the requirement) that is used to search for and book the named resource.</span></span>

1. <span data-ttu-id="01347-123">A la quadrícula **Planificació** d'una tasca, seleccioneu la icona **Recurs** a la cel·la de recursos.</span><span class="sxs-lookup"><span data-stu-id="01347-123">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell.</span></span>

2. <span data-ttu-id="01347-124">Introduïu un nom que servirà per al recurs contenidor.</span><span class="sxs-lookup"><span data-stu-id="01347-124">Type a name to serve as the placeholder resource’s name.</span></span> <span data-ttu-id="01347-125">Per exemple: Administrador.</span><span class="sxs-lookup"><span data-stu-id="01347-125">For example, Program Manager.</span></span>

3. <span data-ttu-id="01347-126">Seleccioneu **Crea** i al camp **Creació ràpida del membre de l'equip de projecte** , establiu la funció per al recurs genèric.</span><span class="sxs-lookup"><span data-stu-id="01347-126">Select **Create** , and in the **Quick Create Project Team Member** field, set the role for the generic resource.</span></span>

4. <span data-ttu-id="01347-127">Podeu seguir assignant tasques a aquest recurs de contenidor si seleccioneu el recurs al **Selector de recursos** per a la tasca.</span><span class="sxs-lookup"><span data-stu-id="01347-127">You can continue to assign tasks to this placeholder resource by selecting the resource on the **Resource Selector** for the task.</span></span> <span data-ttu-id="01347-128">S'enumeren a l'apartat **Membres de l'equip**.</span><span class="sxs-lookup"><span data-stu-id="01347-128">They’re listed under **Team Members**.</span></span>

5. <span data-ttu-id="01347-129">Quan hàgiu acabat d'assignar el recurs genèric, seleccioneu-lo a la pestanya **Equip** i, a continuació, seleccioneu **Genera un requisit** per crear un requisit de recursos per al recurs genèric.</span><span class="sxs-lookup"><span data-stu-id="01347-129">When you’re done assigning the generic resource, select the generic resource on the **Team** tab, and then select **Generate Requirement** to create a resource requirement for the generic resource.</span></span>

6. <span data-ttu-id="01347-130">Seleccioneu **Reserva** per al recurs genèric.</span><span class="sxs-lookup"><span data-stu-id="01347-130">Select **Book** for the generic resource.</span></span> <span data-ttu-id="01347-131">A continuació, podeu utilitzar el Tauler de planificació per buscar i reservar un recurs real.</span><span class="sxs-lookup"><span data-stu-id="01347-131">You can then use the Schedule board to find and book a real resource.</span></span> <span data-ttu-id="01347-132">També podeu enviar el requisit de compliment per un administrador de recursos.</span><span class="sxs-lookup"><span data-stu-id="01347-132">You can also submit the requirement for fulfillment by a resource manager.</span></span>

7. <span data-ttu-id="01347-133">Quan el recurs genèric es compleix amb un recurs amb nom, el genèric s'elimina de l'equip i les assignacions de tasques s'assignen al recurs amb nom que va complir els requisits de recursos del recurs genèric.</span><span class="sxs-lookup"><span data-stu-id="01347-133">When the generic resource is fulfilled with a named resource, the generic resource is removed from the team and the task assignments for the generic resource are assigned to the named resource that fulfilled the generic resource’s resource requirement.</span></span>

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a><span data-ttu-id="01347-134">Assignar un recurs amb nom de la llista de tots els recursos que es poden reservar</span><span class="sxs-lookup"><span data-stu-id="01347-134">Assign a named resource from the list of all bookable resources</span></span>

<span data-ttu-id="01347-135">Feu servir el quadre de cerca del **Selector de recursos** per buscar tots els recursos reservables i assignar-los a una tasca.</span><span class="sxs-lookup"><span data-stu-id="01347-135">You can use the search box in the **Resource Selector** to search all bookable resources and assign them to a task.</span></span>

<span data-ttu-id="01347-136">Els recursos assignats d'aquesta manera s'afegeixen a l'equip sense cap tipus de reserves.</span><span class="sxs-lookup"><span data-stu-id="01347-136">Resources assigned this way are added to the team without any bookings.</span></span> <span data-ttu-id="01347-137">Això és similar a l'addició d'un membre de l'equip i a seleccionar Cap com a mètode d'assignació.</span><span class="sxs-lookup"><span data-stu-id="01347-137">This is similar to adding a team member and selecting None as the allocation method.</span></span> <span data-ttu-id="01347-138">El recurs es mostra a la pestanya **Equip** i a la pestanya **Conciliació** com a recursos només amb assignacions i un dèficit de reserves.</span><span class="sxs-lookup"><span data-stu-id="01347-138">The resource is displayed in the **Team** and **Reconciliation** tabs as resources with only assignments and a booking deficit.</span></span> <span data-ttu-id="01347-139">Si voleu utilitzar-ne la disponibilitat, els podeu reservar.</span><span class="sxs-lookup"><span data-stu-id="01347-139">Book them if you want to use their availability.</span></span>

1. <span data-ttu-id="01347-140">A la quadrícula **Planificació** d'una tasca, seleccioneu la icona **Recurs** a la cel·la de recursos.</span><span class="sxs-lookup"><span data-stu-id="01347-140">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell.</span></span>

2. <span data-ttu-id="01347-141">Comenceu a escriure un nom.</span><span class="sxs-lookup"><span data-stu-id="01347-141">Start typing a name.</span></span> <span data-ttu-id="01347-142">Els resultats de cerca per al nom es mostren al **Selector de recursos** a l'apartat **Altres recursos**.</span><span class="sxs-lookup"><span data-stu-id="01347-142">The search results for the name are displayed in the **Resource Selector** under **Other Resources**.</span></span>

3. <span data-ttu-id="01347-143">Seleccioneu el recurs que voleu assignar a la tasca.</span><span class="sxs-lookup"><span data-stu-id="01347-143">Select the resource that you want to assign to the task.</span></span>

