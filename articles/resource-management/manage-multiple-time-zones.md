---
title: Administració de fusos horaris
description: Quan es crea un projecte, el seu fus horari es basa en el fus horari definit a la plantilla d'hores de treball aplicada.
author: ruhercul
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 27f58f0dacc3404119a719547ad374629c740740
ms.sourcegitcommit: 396e0fea2f1598a5313cb0128eca4fe0bb5aade9
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961822"
---
# <a name="manage-time-zones"></a><span data-ttu-id="c8aa5-103">Administració de fusos horaris</span><span class="sxs-lookup"><span data-stu-id="c8aa5-103">Manage time zones</span></span>

<span data-ttu-id="c8aa5-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_</span><span class="sxs-lookup"><span data-stu-id="c8aa5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


## <a name="projects"></a><span data-ttu-id="c8aa5-105">Projectes</span><span class="sxs-lookup"><span data-stu-id="c8aa5-105">Projects</span></span>

<span data-ttu-id="c8aa5-106">Quan es crea un projecte, el fus horari es basa en el fus horari definit a la plantilla d'hores de treball aplicada.</span><span class="sxs-lookup"><span data-stu-id="c8aa5-106">When a project is created, the time zone is based on the time zone defined in the applied work hour template.</span></span> <span data-ttu-id="c8aa5-107">A **Projecte**, les dates sempre són relatives a la zona horària de l'usuari que ha iniciat la sessió a cada pestanya, tret de la pestanya de la **Tasca** . Quan visualitzeu l'estructura del desglossament del treball, les dates es mostraran sempre a la zona horària del projecte.</span><span class="sxs-lookup"><span data-stu-id="c8aa5-107">On the **Project** for, the dates are always relative to the time zone of the user that is logged in on each tab, except the **Task** tab. When you view the work breakdown structure, the dates will always be displayed in the project’s time zone.</span></span>

## <a name="tasks"></a><span data-ttu-id="c8aa5-108">Tasques</span><span class="sxs-lookup"><span data-stu-id="c8aa5-108">Tasks</span></span>

<span data-ttu-id="c8aa5-109">Quan es crea una tasca, l'hora d'inici, l'hora d'acabament i les hores/dia estan controlades per les hores de treball del projecte.</span><span class="sxs-lookup"><span data-stu-id="c8aa5-109">When a task is created, the start time, end time, and hours/day is controlled by the working hours of the project.</span></span> <span data-ttu-id="c8aa5-110">Per exemple, si es crea una tasca amb un projecte la zona horària del qual és -8 PST i té les següents hores de feina: 9:00 h a 17:00 h de dilluns a divendres, qualsevol tasca creada sense assignació respectarà l'hora d'inici i l'hora d'acabament del calendari del projecte.</span><span class="sxs-lookup"><span data-stu-id="c8aa5-110">For example, if a task is created with a project whose time zone is -8 PST and has the following working hours: 9:00 AM to 5:00 PM Monday to Friday, any task created without an assignment will respect the start time and end time of the project calendar.</span></span>

## <a name="manage-resources-with-time-zones"></a><span data-ttu-id="c8aa5-111">Administrar recursos amb fusos horaris</span><span class="sxs-lookup"><span data-stu-id="c8aa5-111">Manage resources with time zones</span></span>

<span data-ttu-id="c8aa5-112">Per obtenir resultats precisos i predictibles quan s'utilitza **Amplia la reserva**, hi ha dos prerequisits clau que s'han de complir:</span><span class="sxs-lookup"><span data-stu-id="c8aa5-112">For accurate and predictable results when using **Extend Booking**, there are two key prerequisites that must be met:</span></span>  

- <span data-ttu-id="c8aa5-113">L'usuari ha de configurar el fus horari del dispositiu perquè coincideixi amb el fus horari definit a la **configuració de personalització** del sistema.</span><span class="sxs-lookup"><span data-stu-id="c8aa5-113">The user must configure their device's time zone to match the time zone defined in the system's **Personalization Settings**.</span></span>
 
  ![Configuració de fus horari al Windows 10](media/reconcile-assignments-03.png)

  ![Configuració del fus horari a la Configuració de personalització](media/reconcile-assignments-04.png)
 
- <span data-ttu-id="c8aa5-116">El recurs reservable ha de tenir com a mínim un minut de temps de treball que se solapi amb els contorns que s'utilitzen per definir l'extensió sol·licitada.</span><span class="sxs-lookup"><span data-stu-id="c8aa5-116">The bookable resource must have at least one minute of working time that overlaps with the contours that are used to define the requested extension.</span></span> <span data-ttu-id="c8aa5-117">Per exemple, els recursos següents amb hores de feina entre les 9:00 h i les 19:00 h.</span><span class="sxs-lookup"><span data-stu-id="c8aa5-117">For example, the following resources with working hours that fall between 9:00 AM and 7:00 PM.</span></span> 

  ![Comparativa de contorns de recursos](media/reconcile-assignments-05.png)

<span data-ttu-id="c8aa5-119">La taula següent mostra:</span><span class="sxs-lookup"><span data-stu-id="c8aa5-119">The following table shows:</span></span>

- <span data-ttu-id="c8aa5-120">Una plantilla de calendari de projecte</span><span class="sxs-lookup"><span data-stu-id="c8aa5-120">A project calendar template</span></span>
- <span data-ttu-id="c8aa5-121">Recurs A: aquest recurs té el mateix calendari i es troba al mateix fus horari que el projecte.</span><span class="sxs-lookup"><span data-stu-id="c8aa5-121">Resource A: This resource has the same calendar and is in the same time zone as the project.</span></span> <span data-ttu-id="c8aa5-122">L'hora d'inici de les reserves serà les 9:00 h.</span><span class="sxs-lookup"><span data-stu-id="c8aa5-122">The start time of the bookings will be 9:00 AM.</span></span>
- <span data-ttu-id="c8aa5-123">Recurs B: aquest recurs es troba en un fus horari diferent del projecte i comença a les 7:00 h del seu fus horari.</span><span class="sxs-lookup"><span data-stu-id="c8aa5-123">Resource B: This resource is located in a different time zone than the project and starts at 7:00 AM in their time zone.</span></span> <span data-ttu-id="c8aa5-124">No obstant això, les reserves començaran a partir de 9:00 h, que és la primera hora d'inici del contorn d'assignació.</span><span class="sxs-lookup"><span data-stu-id="c8aa5-124">However, the bookings will begin at 9:00 AM as that is the earliest start time of the assignment contour.</span></span>
- <span data-ttu-id="c8aa5-125">Recursos C i D: els recursos es troben ubicats en diferents fusos horaris, diferents entre si i el projecte, i les seves reserves no comencen abans de les seves respectives hores d'inici disponibles.</span><span class="sxs-lookup"><span data-stu-id="c8aa5-125">Resources C and D: The resources are located in different time zones, both different from each other and the project, and their bookings start no earlier than their respective available start times.</span></span>

|<span data-ttu-id="c8aa5-126">Entitat</span><span class="sxs-lookup"><span data-stu-id="c8aa5-126">Entity</span></span>  |<span data-ttu-id="c8aa5-127">Calendari</span><span class="sxs-lookup"><span data-stu-id="c8aa5-127">Calendar</span></span>  |
|-|-|
|<span data-ttu-id="c8aa5-128">Plantilla de calendari de projecte</span><span class="sxs-lookup"><span data-stu-id="c8aa5-128">Project calendar template</span></span>   | ![calendari de projecte](media/reconcile-assignments-06.png) |
|<span data-ttu-id="c8aa5-130">Recurs A</span><span class="sxs-lookup"><span data-stu-id="c8aa5-130">Resource A</span></span>  | ![Calendari del recurs A](media/reconcile-assignments-06.png) |
|<span data-ttu-id="c8aa5-132">Recurs B</span><span class="sxs-lookup"><span data-stu-id="c8aa5-132">Resource B</span></span>  |  ![Calendari del recurs B](media/reconcile-assignments-07.png) |
|<span data-ttu-id="c8aa5-134">Recurs C</span><span class="sxs-lookup"><span data-stu-id="c8aa5-134">Resource C</span></span>  |  ![Calendari del recurs C](media/reconcile-assignments-08.png) |
|<span data-ttu-id="c8aa5-136">Recurs D</span><span class="sxs-lookup"><span data-stu-id="c8aa5-136">Resource D</span></span>  | ![Calendari del recurs D](media/reconcile-assignments-09.png)  |
 
<span data-ttu-id="c8aa5-138">Quan navegueu a la visualització **Conciliació**, es mostren les assignacions de recursos i les mancances de reserva associades.</span><span class="sxs-lookup"><span data-stu-id="c8aa5-138">When you navigate to the **Reconciliation** view, the resource assignments and the associated booking shortages are displayed.</span></span>

![Visualització de conciliació abans de l'ampliació](media/reconcile-assignments-10.png)

<span data-ttu-id="c8aa5-140">Un cop s'ha utilitzat la funcionalitat d'ampliació de la reserva per a cada recurs, les reserves s'amplien correctament per a cada recurs, perquè les hores de feina de cada recurs se superposen amb els contorns de la manca.</span><span class="sxs-lookup"><span data-stu-id="c8aa5-140">After the extend booking functionality has been used for each resource, bookings are successfully extended for each resource because each resource’s working hours overlapped with the contours of the shortage.</span></span>

![Visualització de conciliació després de l'ampliació de la reserva](media/reconcile-assignments-11.png) 

<span data-ttu-id="c8aa5-142">Observeu que una mirada més profunda dels detalls de les reserves mostra diferències en l'hora d'inici de les reserves.</span><span class="sxs-lookup"><span data-stu-id="c8aa5-142">Notice that a closer look at the details of the bookings shows differences in the start time of the bookings.</span></span> <span data-ttu-id="c8aa5-143">Les reserves no comencen abans de l'hora d'inici del contorn d'assignació ni abans de l'hora d'inici disponible del recurs.</span><span class="sxs-lookup"><span data-stu-id="c8aa5-143">The bookings start no earlier than the start time of the assignment contour and no earlier than the available start time of the resource.</span></span>

![Noves reserves dels recursos al tauler de planificació](media/reconcile-assignments-12.png)
