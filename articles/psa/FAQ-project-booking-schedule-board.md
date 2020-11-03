---
title: Crear una reserva de projecte des del tauler de planificació
description: En aquest tema es proporciona informació sobre com crear una reserva de projecte des del tauler de planificació.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
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
ms.openlocfilehash: 57fbc71681015fca73cdda4bc7d392f6be4289f3
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072229"
---
# <a name="create-a-project-booking-from-the-schedule-board"></a><span data-ttu-id="fd9a5-103">Crear una reserva de projecte des del tauler de planificació</span><span class="sxs-lookup"><span data-stu-id="fd9a5-103">Create a project booking from the Schedule board</span></span>

<span data-ttu-id="fd9a5-104">Podeu reservar un recurs en un projecte directament a la pestanya **Equip** del projecte o generant un requisit de recursos d'una assignació del membre de l'equip genèric i complint després amb el requisit generat amb un membre de l'equip del projecte.</span><span class="sxs-lookup"><span data-stu-id="fd9a5-104">You can book a resource onto a project directly from the **Team** tab of the project or by generating a resource requirement from a generic team member assignment and then fulfilling the generated requirement with a project team member.</span></span>

<span data-ttu-id="fd9a5-105">També podeu reservar un recurs en un projecte directament des del Tauler de planificació.</span><span class="sxs-lookup"><span data-stu-id="fd9a5-105">You can also book a resource onto a project directly from the Schedule board.</span></span> <span data-ttu-id="fd9a5-106">Hi ha dues maneres de fer-ho:</span><span class="sxs-lookup"><span data-stu-id="fd9a5-106">There are three ways to do this:</span></span>

- <span data-ttu-id="fd9a5-107">: **Reserva a partir d'un requisit de recurs generat:** podeu generar un requisit de recurs després de crear un recurs genèric i assignar tasques dins d'un projecte.</span><span class="sxs-lookup"><span data-stu-id="fd9a5-107">**Book from a generated resource requirement:** You can generate a resource requirement after you create a generic resource and assign tasks within a project.</span></span>

- <span data-ttu-id="fd9a5-108">**Reserva des del requisit principal:** els requisits principals es mostren al tauler de planificació de la pestanya **Projecte**.</span><span class="sxs-lookup"><span data-stu-id="fd9a5-108">**Book from the primary requirement:** The primary requirements show up on the Schedule board on the **Project** tab.</span></span> 

- <span data-ttu-id="fd9a5-109">**Reserva des d'un requisit de recurs nou:** podeu crear un requisit de recursos des de zero i associar-lo amb un projecte.</span><span class="sxs-lookup"><span data-stu-id="fd9a5-109">**Book from a new resource requirement:** You can create a resource requirement from scratch and associate it with a project.</span></span> <span data-ttu-id="fd9a5-110">Al Tauler de planificació, el requisit de recursos apareix a la pestanya **Obre els requisits**.</span><span class="sxs-lookup"><span data-stu-id="fd9a5-110">On the Schedule board, the resource requirement shows up on the **Open Requirements** tab.</span></span>

## <a name="book-from-a-generated-resource-requirement"></a><span data-ttu-id="fd9a5-111">Reservar a partir d'un requisit de recursos generat</span><span class="sxs-lookup"><span data-stu-id="fd9a5-111">Book from a generated resource requirement</span></span>

<span data-ttu-id="fd9a5-112">Podeu crear un recurs genèric i assignar-li una o diverses tasques dins d'un projecte.</span><span class="sxs-lookup"><span data-stu-id="fd9a5-112">You can create a generic resource and assign it one or more tasks within a project.</span></span> <span data-ttu-id="fd9a5-113">A continuació podeu generar un requisit de recursos des del membre de l'equip genèric.</span><span class="sxs-lookup"><span data-stu-id="fd9a5-113">Then you can generate a resource requirement from the generic team member.</span></span> 

1.  <span data-ttu-id="fd9a5-114">Al Tauler de planificació, aquest recurs apareixerà a la pestanya **Obre els requisits**. És possible que hàgiu d'utilitzar filtres de columna a la quadrícula si teniu molts requisits oberts.</span><span class="sxs-lookup"><span data-stu-id="fd9a5-114">On the Schedule board, this resource will show up on the **Open Requirements** tab. You might need to use column filters on the grid if you have many open requirements.</span></span> 

    <span data-ttu-id="fd9a5-115">![Pestanya Requisits oberts al Tauler de planificació](media/FAQ-Project-Booking-Schedule-Board-1.png "Captura de pantalla de la taula de reserves i assignacions")</span><span class="sxs-lookup"><span data-stu-id="fd9a5-115">![Open Requirements tab on the Schedule board](media/FAQ-Project-Booking-Schedule-Board-1.png "Screenshot of bookings and assignments table")</span></span>

2. <span data-ttu-id="fd9a5-116">Seleccioneu el requisit.</span><span class="sxs-lookup"><span data-stu-id="fd9a5-116">Select the requirement.</span></span> <span data-ttu-id="fd9a5-117">La pestanya **Cerca la disponibilitat** apareixerà a la part superior de la fila seleccionada.</span><span class="sxs-lookup"><span data-stu-id="fd9a5-117">The **Find Availability** tab will appear at the top of the selected row.</span></span>
 
3. <span data-ttu-id="fd9a5-118">En seleccionar la pestanya s'obre el mode Auxiliar de programació del Tauler de planificació i filtra els recursos disponibles que compleixen amb els requisits de recursos.</span><span class="sxs-lookup"><span data-stu-id="fd9a5-118">When you select the tab, the Schedule Assistant mode of the Schedule board opens and then filters the available resources that meet the resource requirement.</span></span> <span data-ttu-id="fd9a5-119">Tot seguit, podeu reservar un recurs.</span><span class="sxs-lookup"><span data-stu-id="fd9a5-119">After that, you can book a resource.</span></span>

4. <span data-ttu-id="fd9a5-120">També podeu arrossegar i deixar anar la fila seleccionada des de la part inferior del Tauler de planificació a una cel·la de recurs a la quadrícula anterior.</span><span class="sxs-lookup"><span data-stu-id="fd9a5-120">You can also drag and drop the selected row from the bottom of the Schedule board to a resource cell in the grid above.</span></span> <span data-ttu-id="fd9a5-121">Quan el deixeu anar, s'obre la subfinestra **Crea la reserva de recursos** a la dreta.</span><span class="sxs-lookup"><span data-stu-id="fd9a5-121">When you drop it, it opens the **Create Resource Booking** panel on the right.</span></span>

    <span data-ttu-id="fd9a5-122">Si seleccioneu **Reserva** es reserva el recurs a l'equip del projecte.</span><span class="sxs-lookup"><span data-stu-id="fd9a5-122">Selecting **Book** books the resource onto the project team.</span></span>

![Subfinestra Crea la reserva de recursos](media/FAQ-Project-Booking-Schedule-Board-6.png "")
 

## <a name="book-from-the-primary-requirement"></a><span data-ttu-id="fd9a5-124">Reservar des del requisit principal</span><span class="sxs-lookup"><span data-stu-id="fd9a5-124">Book from the Primary Requirement</span></span>

<span data-ttu-id="fd9a5-125">La creació d'un projecte al Project Service crea automàticament un requisit de recurs denominat Requisit principal.</span><span class="sxs-lookup"><span data-stu-id="fd9a5-125">Creating a project in Project Service automatically creates a resource requirement called the Primary Requirement.</span></span> <span data-ttu-id="fd9a5-126">És un requisit buit que s'utilitza per reservar ràpidament un recurs amb el Tauler de planificació sense generar un requisit ni crear-ne un des de zero.</span><span class="sxs-lookup"><span data-stu-id="fd9a5-126">This is an empty requirement that is used to quickly book a resource with the Schedule board without generating a requirement or creating one from scratch.</span></span> <span data-ttu-id="fd9a5-127">Atès que el requisit està buit, haureu d'especificar les dates, així com el mètode d'assignació i les hores, si és necessari.</span><span class="sxs-lookup"><span data-stu-id="fd9a5-127">Because the requirement is empty, you’ll need to specify dates as well as the allocation method and hours, if applicable.</span></span> 

1. <span data-ttu-id="fd9a5-128">Per reservar un recurs amb el Requisit principal, al tauler de planificació, seleccioneu la pestanya **Projecte**. Si teniu molts projectes, és possible que hagueu d'utilitzar el filtre de columna a la columna **Projecte**.</span><span class="sxs-lookup"><span data-stu-id="fd9a5-128">To book a resource with the Primary Requirement, on the Schedule board, select the **Project** tab. You might need to use the column filter on the **Project** column if you have many projects.</span></span>

   <span data-ttu-id="fd9a5-129">![Filtres de columna al Tauler de planificació](media/FAQ-Project-Booking-Schedule-Board-2.png "Captura de pantalla de la taula de reserves i assignacions")</span><span class="sxs-lookup"><span data-stu-id="fd9a5-129">![Column filters on the Schedule board](media/FAQ-Project-Booking-Schedule-Board-2.png "Screenshot of bookings and assignments table")</span></span>

2. <span data-ttu-id="fd9a5-130">Seleccioneu el requisit que té el nom del projecte que busqueu i té una durada de zero (0).</span><span class="sxs-lookup"><span data-stu-id="fd9a5-130">Select the requirement that only has the project name as its name and has a duration of zero (0).</span></span>

3. <span data-ttu-id="fd9a5-131">Seleccioneu la pestanya **Cerca la disponibilitat** que apareix a la fila.</span><span class="sxs-lookup"><span data-stu-id="fd9a5-131">Select the **Find Availability** tab that appears on the row.</span></span> <span data-ttu-id="fd9a5-132">Aquesta acció posa el tauler de planificació en el mode Assistent de planificació i mostra els recursos disponibles que es poden reservar en el projecte.</span><span class="sxs-lookup"><span data-stu-id="fd9a5-132">This puts the Schedule board in Schedule Assistant mode and shows the available resources that can be booked onto the project.</span></span>

4. <span data-ttu-id="fd9a5-133">Com que un **Requisit principal** és un requisit buit amb una durada de zero (0), haureu d'establir la duració en la subfinestra **Crea la reserva de recursos** en seleccionar i reservar un recurs.</span><span class="sxs-lookup"><span data-stu-id="fd9a5-133">Because a **Primary Requirement** is an empty requirement with zero (0) duration, you’ll need to set the duration on the **Create Resource Booking** panel when selecting and booking a resource.</span></span>

5. <span data-ttu-id="fd9a5-134">També podeu seleccionar el **Requisit principal del projecte** a la part inferior del tauler de planificació i arrossegar-lo i deixar-lo anar en un recurs per reservar-lo.</span><span class="sxs-lookup"><span data-stu-id="fd9a5-134">You can also select the **Project Primary Requirement** at the bottom of the Schedule board and drag and drop it on a resource to book it.</span></span>
 
    <span data-ttu-id="fd9a5-135">Com que un **Requisit principal** és un requisit buit amb una durada de zero (0), haureu d'establir la duració en la subfinestra **Crea la reserva de recursos** en seleccionar i reservar un recurs.</span><span class="sxs-lookup"><span data-stu-id="fd9a5-135">Because the **Primary Requirement** is an empty requirement that has zero (0) duration, you’ll need to set the duration on the **Create Resource Booking** panel when you select and book a resource.</span></span>
 
    <span data-ttu-id="fd9a5-136">Quan reserveu un recurs mitjançant el **Requisit principal** al tauler de planificació, l'afegiu a l'equip del projecte sense cap assignació.</span><span class="sxs-lookup"><span data-stu-id="fd9a5-136">When you book a resource through the **Primary Requirement** on the Schedule board, you add it to the project team without any assignments.</span></span>
 
## <a name="book-from-a-new-resource-requirement"></a><span data-ttu-id="fd9a5-137">Reservar a partir d'un requisit de recursos nou</span><span class="sxs-lookup"><span data-stu-id="fd9a5-137">Book from a new resource requirement</span></span>
<span data-ttu-id="fd9a5-138">Completeu els passos següents per fer la reserva des d'un requisit de recurs nou.</span><span class="sxs-lookup"><span data-stu-id="fd9a5-138">Complete the following steps to book from a new resource requirement.</span></span> 

1. <span data-ttu-id="fd9a5-139">Aneu a **Requisits de recursos** i seleccioneu **Crea** per crear un requisit de recursos nou.</span><span class="sxs-lookup"><span data-stu-id="fd9a5-139">Go to **Resource Requirements** , and then select **New** to create a new resource requirement.</span></span>

2. <span data-ttu-id="fd9a5-140">A la pestanya **Projecte** , seleccioneu un projecte per associar el requisit al projecte.</span><span class="sxs-lookup"><span data-stu-id="fd9a5-140">On the **Project** tab, select a project to associate the requirement to the project.</span></span>
 
    <span data-ttu-id="fd9a5-141">Al tauler de planificació, aquest requisit acabat de crear es mostra com a **Requisit obert** que podeu complir.</span><span class="sxs-lookup"><span data-stu-id="fd9a5-141">On the Schedule board, this new requirement shows as an **Open Requirement** that you can fulfill.</span></span>

3. <span data-ttu-id="fd9a5-142">Reserveu el recurs per afegir-lo a l'equip del projecte.</span><span class="sxs-lookup"><span data-stu-id="fd9a5-142">Book the resource to add it to the project team.</span></span>

4. <span data-ttu-id="fd9a5-143">Ara que el recurs està reservat, heu d'assignar tasques manualment.</span><span class="sxs-lookup"><span data-stu-id="fd9a5-143">Now that the resource is booked, you must assign tasks manually.</span></span>

