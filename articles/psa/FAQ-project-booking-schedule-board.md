---
title: Crear una reserva de projecte des del tauler de planificació
description: En aquest tema es proporciona informació sobre com crear una reserva de projecte des del tauler de planificació.
author: ruhercul
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
ms.openlocfilehash: d33786a5d0a2485a06d174eb7afcbaaa2f337cf6
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5992954"
---
# <a name="create-a-project-booking-from-the-schedule-board"></a><span data-ttu-id="9842e-103">Crear una reserva de projecte des del tauler de planificació</span><span class="sxs-lookup"><span data-stu-id="9842e-103">Create a project booking from the Schedule board</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="9842e-104">Podeu reservar un recurs en un projecte directament a la pestanya **Equip** del projecte o generant un requisit de recursos d'una assignació del membre de l'equip genèric i complint després amb el requisit generat amb un membre de l'equip del projecte.</span><span class="sxs-lookup"><span data-stu-id="9842e-104">You can book a resource onto a project directly from the **Team** tab of the project or by generating a resource requirement from a generic team member assignment and then fulfilling the generated requirement with a project team member.</span></span>

<span data-ttu-id="9842e-105">També podeu reservar un recurs en un projecte directament des del Tauler de planificació.</span><span class="sxs-lookup"><span data-stu-id="9842e-105">You can also book a resource onto a project directly from the Schedule board.</span></span> <span data-ttu-id="9842e-106">Hi ha dues maneres de fer-ho:</span><span class="sxs-lookup"><span data-stu-id="9842e-106">There are three ways to do this:</span></span>

- <span data-ttu-id="9842e-107">:**Reserva a partir d'un requisit de recurs generat:** podeu generar un requisit de recurs després de crear un recurs genèric i assignar tasques dins d'un projecte.</span><span class="sxs-lookup"><span data-stu-id="9842e-107">**Book from a generated resource requirement:** You can generate a resource requirement after you create a generic resource and assign tasks within a project.</span></span>

- <span data-ttu-id="9842e-108">**Reserva des del requisit principal:** els requisits principals es mostren al tauler de planificació de la pestanya **Projecte**.</span><span class="sxs-lookup"><span data-stu-id="9842e-108">**Book from the primary requirement:** The primary requirements show up on the Schedule board on the **Project** tab.</span></span> 

- <span data-ttu-id="9842e-109">**Reserva des d'un requisit de recurs nou:** podeu crear un requisit de recursos des de zero i associar-lo amb un projecte.</span><span class="sxs-lookup"><span data-stu-id="9842e-109">**Book from a new resource requirement:** You can create a resource requirement from scratch and associate it with a project.</span></span> <span data-ttu-id="9842e-110">Al Tauler de planificació, el requisit de recursos apareix a la pestanya **Obre els requisits**.</span><span class="sxs-lookup"><span data-stu-id="9842e-110">On the Schedule board, the resource requirement shows up on the **Open Requirements** tab.</span></span>

## <a name="book-from-a-generated-resource-requirement"></a><span data-ttu-id="9842e-111">Reservar a partir d'un requisit de recursos generat</span><span class="sxs-lookup"><span data-stu-id="9842e-111">Book from a generated resource requirement</span></span>

<span data-ttu-id="9842e-112">Podeu crear un recurs genèric i assignar-li una o diverses tasques dins d'un projecte.</span><span class="sxs-lookup"><span data-stu-id="9842e-112">You can create a generic resource and assign it one or more tasks within a project.</span></span> <span data-ttu-id="9842e-113">A continuació podeu generar un requisit de recursos des del membre de l'equip genèric.</span><span class="sxs-lookup"><span data-stu-id="9842e-113">Then you can generate a resource requirement from the generic team member.</span></span> 

1.  <span data-ttu-id="9842e-114">Al Tauler de planificació, aquest recurs apareixerà a la pestanya **Obre els requisits**. És possible que hàgiu d'utilitzar filtres de columna a la quadrícula si teniu molts requisits oberts.</span><span class="sxs-lookup"><span data-stu-id="9842e-114">On the Schedule board, this resource will show up on the **Open Requirements** tab. You might need to use column filters on the grid if you have many open requirements.</span></span> 

    <span data-ttu-id="9842e-115">![Pestanya Requisits oberts al Tauler de planificació](media/FAQ-Project-Booking-Schedule-Board-1.png "Captura de pantalla de la taula de reserves i assignacions")</span><span class="sxs-lookup"><span data-stu-id="9842e-115">![Open Requirements tab on the Schedule board](media/FAQ-Project-Booking-Schedule-Board-1.png "Screenshot of bookings and assignments table")</span></span>

2. <span data-ttu-id="9842e-116">Seleccioneu el requisit.</span><span class="sxs-lookup"><span data-stu-id="9842e-116">Select the requirement.</span></span> <span data-ttu-id="9842e-117">La pestanya **Cerca la disponibilitat** apareixerà a la part superior de la fila seleccionada.</span><span class="sxs-lookup"><span data-stu-id="9842e-117">The **Find Availability** tab will appear at the top of the selected row.</span></span>
 
3. <span data-ttu-id="9842e-118">En seleccionar la pestanya s'obre el mode Auxiliar de programació del Tauler de planificació i filtra els recursos disponibles que compleixen amb els requisits de recursos.</span><span class="sxs-lookup"><span data-stu-id="9842e-118">When you select the tab, the Schedule Assistant mode of the Schedule board opens and then filters the available resources that meet the resource requirement.</span></span> <span data-ttu-id="9842e-119">Tot seguit, podeu reservar un recurs.</span><span class="sxs-lookup"><span data-stu-id="9842e-119">After that, you can book a resource.</span></span>

4. <span data-ttu-id="9842e-120">També podeu arrossegar i deixar anar la fila seleccionada des de la part inferior del Tauler de planificació a una cel·la de recurs a la quadrícula anterior.</span><span class="sxs-lookup"><span data-stu-id="9842e-120">You can also drag and drop the selected row from the bottom of the Schedule board to a resource cell in the grid above.</span></span> <span data-ttu-id="9842e-121">Quan el deixeu anar, s'obre la subfinestra **Crea la reserva de recursos** a la dreta.</span><span class="sxs-lookup"><span data-stu-id="9842e-121">When you drop it, it opens the **Create Resource Booking** panel on the right.</span></span>

    <span data-ttu-id="9842e-122">Si seleccioneu **Reserva** es reserva el recurs a l'equip del projecte.</span><span class="sxs-lookup"><span data-stu-id="9842e-122">Selecting **Book** books the resource onto the project team.</span></span>

![Subfinestra Crea la reserva de recursos](media/FAQ-Project-Booking-Schedule-Board-6.png "")
 

## <a name="book-from-the-primary-requirement"></a><span data-ttu-id="9842e-124">Reservar des del requisit principal</span><span class="sxs-lookup"><span data-stu-id="9842e-124">Book from the Primary Requirement</span></span>

<span data-ttu-id="9842e-125">La creació d'un projecte al Project Service crea automàticament un requisit de recurs denominat Requisit principal.</span><span class="sxs-lookup"><span data-stu-id="9842e-125">Creating a project in Project Service automatically creates a resource requirement called the Primary Requirement.</span></span> <span data-ttu-id="9842e-126">És un requisit buit que s'utilitza per reservar ràpidament un recurs amb el Tauler de planificació sense generar un requisit ni crear-ne un des de zero.</span><span class="sxs-lookup"><span data-stu-id="9842e-126">This is an empty requirement that is used to quickly book a resource with the Schedule board without generating a requirement or creating one from scratch.</span></span> <span data-ttu-id="9842e-127">Atès que el requisit està buit, haureu d'especificar les dates, així com el mètode d'assignació i les hores, si és necessari.</span><span class="sxs-lookup"><span data-stu-id="9842e-127">Because the requirement is empty, you’ll need to specify dates as well as the allocation method and hours, if applicable.</span></span> 

1. <span data-ttu-id="9842e-128">Per reservar un recurs amb el Requisit principal, al tauler de planificació, seleccioneu la pestanya **Projecte**. Si teniu molts projectes, és possible que hagueu d'utilitzar el filtre de columna a la columna **Projecte**.</span><span class="sxs-lookup"><span data-stu-id="9842e-128">To book a resource with the Primary Requirement, on the Schedule board, select the **Project** tab. You might need to use the column filter on the **Project** column if you have many projects.</span></span>

   <span data-ttu-id="9842e-129">![Filtres de columna al Tauler de planificació](media/FAQ-Project-Booking-Schedule-Board-2.png "Captura de pantalla de la taula de reserves i assignacions")</span><span class="sxs-lookup"><span data-stu-id="9842e-129">![Column filters on the Schedule board](media/FAQ-Project-Booking-Schedule-Board-2.png "Screenshot of bookings and assignments table")</span></span>

2. <span data-ttu-id="9842e-130">Seleccioneu el requisit que té el nom del projecte que busqueu i té una durada de zero (0).</span><span class="sxs-lookup"><span data-stu-id="9842e-130">Select the requirement that only has the project name as its name and has a duration of zero (0).</span></span>

3. <span data-ttu-id="9842e-131">Seleccioneu la pestanya **Cerca la disponibilitat** que apareix a la fila.</span><span class="sxs-lookup"><span data-stu-id="9842e-131">Select the **Find Availability** tab that appears on the row.</span></span> <span data-ttu-id="9842e-132">Aquesta acció posa el tauler de planificació en el mode Assistent de planificació i mostra els recursos disponibles que es poden reservar en el projecte.</span><span class="sxs-lookup"><span data-stu-id="9842e-132">This puts the Schedule board in Schedule Assistant mode and shows the available resources that can be booked onto the project.</span></span>

4. <span data-ttu-id="9842e-133">Com que un **Requisit principal** és un requisit buit amb una durada de zero (0), haureu d'establir la duració en la subfinestra **Crea la reserva de recursos** en seleccionar i reservar un recurs.</span><span class="sxs-lookup"><span data-stu-id="9842e-133">Because a **Primary Requirement** is an empty requirement with zero (0) duration, you’ll need to set the duration on the **Create Resource Booking** panel when selecting and booking a resource.</span></span>

5. <span data-ttu-id="9842e-134">També podeu seleccionar el **Requisit principal del projecte** a la part inferior del tauler de planificació i arrossegar-lo i deixar-lo anar en un recurs per reservar-lo.</span><span class="sxs-lookup"><span data-stu-id="9842e-134">You can also select the **Project Primary Requirement** at the bottom of the Schedule board and drag and drop it on a resource to book it.</span></span>
 
    <span data-ttu-id="9842e-135">Com que un **Requisit principal** és un requisit buit amb una durada de zero (0), haureu d'establir la duració en la subfinestra **Crea la reserva de recursos** en seleccionar i reservar un recurs.</span><span class="sxs-lookup"><span data-stu-id="9842e-135">Because the **Primary Requirement** is an empty requirement that has zero (0) duration, you’ll need to set the duration on the **Create Resource Booking** panel when you select and book a resource.</span></span>
 
    <span data-ttu-id="9842e-136">Quan reserveu un recurs mitjançant el **Requisit principal** al tauler de planificació, l'afegiu a l'equip del projecte sense cap assignació.</span><span class="sxs-lookup"><span data-stu-id="9842e-136">When you book a resource through the **Primary Requirement** on the Schedule board, you add it to the project team without any assignments.</span></span>
 
## <a name="book-from-a-new-resource-requirement"></a><span data-ttu-id="9842e-137">Reservar a partir d'un requisit de recursos nou</span><span class="sxs-lookup"><span data-stu-id="9842e-137">Book from a new resource requirement</span></span>
<span data-ttu-id="9842e-138">Completeu els passos següents per fer la reserva des d'un requisit de recurs nou.</span><span class="sxs-lookup"><span data-stu-id="9842e-138">Complete the following steps to book from a new resource requirement.</span></span> 

1. <span data-ttu-id="9842e-139">Aneu a **Requisits de recursos** i seleccioneu **Crea** per crear un requisit de recursos nou.</span><span class="sxs-lookup"><span data-stu-id="9842e-139">Go to **Resource Requirements**, and then select **New** to create a new resource requirement.</span></span>

2. <span data-ttu-id="9842e-140">A la pestanya **Projecte**, seleccioneu un projecte per associar el requisit al projecte.</span><span class="sxs-lookup"><span data-stu-id="9842e-140">On the **Project** tab, select a project to associate the requirement to the project.</span></span>
 
    <span data-ttu-id="9842e-141">Al tauler de planificació, aquest requisit acabat de crear es mostra com a **Requisit obert** que podeu complir.</span><span class="sxs-lookup"><span data-stu-id="9842e-141">On the Schedule board, this new requirement shows as an **Open Requirement** that you can fulfill.</span></span>

3. <span data-ttu-id="9842e-142">Reserveu el recurs per afegir-lo a l'equip del projecte.</span><span class="sxs-lookup"><span data-stu-id="9842e-142">Book the resource to add it to the project team.</span></span>

4. <span data-ttu-id="9842e-143">Ara que el recurs està reservat, heu d'assignar tasques manualment.</span><span class="sxs-lookup"><span data-stu-id="9842e-143">Now that the resource is booked, you must assign tasks manually.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]