---
title: Conciliar reserves i assignacions
description: Aquest tema proporciona informació sobre els valors reals.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 11/27/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 614352ba-dbd8-4fa5-8225-d54f9ec0e218
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 27fc7b6abb4c9a7a761059a2f392f13bc0dd14f9
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749576"
---
# <a name="reconcile-bookings-and-assignments"></a><span data-ttu-id="c147d-103">Conciliar reserves i assignacions</span><span class="sxs-lookup"><span data-stu-id="c147d-103">Reconcile bookings and assignments</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="c147d-104">Les reserves de projectes dels membres d'un equip del projecte i les assignacions de tasques de projectes estan lleugerament vinculades.</span><span class="sxs-lookup"><span data-stu-id="c147d-104">A project team member's project bookings and project task assignments are loosely coupled.</span></span> <span data-ttu-id="c147d-105">Per tant, un recurs pot tenir assignacions de tasques que no corresponen a reserves i reserves que no corresponen a assignacions de tasques.</span><span class="sxs-lookup"><span data-stu-id="c147d-105">Therefore, a resource can have task assignments that don't correspond to bookings and bookings that don't correspond to task assignments.</span></span> <span data-ttu-id="c147d-106">Idealment, les reserves i assignacions de projectes estan alineades perquè els recursos tinguin capacitat confirmada de dur a terme les assignacions de tasques.</span><span class="sxs-lookup"><span data-stu-id="c147d-106">Ideally, project bookings and assignments are aligned, so that resources have committed capacity to perform their task assignments.</span></span> <span data-ttu-id="c147d-107">Tanmateix, la realitat és que les reserves es poden produir segons la disponibilitat, i els temps de les tasques poden canviar al llarg del cicle de vida del projecte.</span><span class="sxs-lookup"><span data-stu-id="c147d-107">However, the reality is that bookings can occur based on availability, and task timings can change as the project continues through its lifecycle.</span></span> <span data-ttu-id="c147d-108">Per tant, la lleugera vinculació permet flexibilitat.</span><span class="sxs-lookup"><span data-stu-id="c147d-108">Therefore, the loose coupling allows for flexibility.</span></span>

<span data-ttu-id="c147d-109">A causa de la lleugera vinculació de les reserves de projectes i de les assignacions de tasques, s'inclou una pestanya **Conciliació** a l'entitat Projecte.</span><span class="sxs-lookup"><span data-stu-id="c147d-109">Because of the loose coupling of project bookings and task assignments, a **Reconciliation** tab is included on the Project entity.</span></span> <span data-ttu-id="c147d-110">Aquesta pestanya ajuda als administradors de projectes conciliar les reserves dels membres de l'equip i els seus treballs per a l'equip del projecte.</span><span class="sxs-lookup"><span data-stu-id="c147d-110">This tab helps project managers reconcile team members' bookings and their assignments for their project team.</span></span>

<span data-ttu-id="c147d-111">Per a cada membre de l'equip, la pestanya **Conciliació** mostra les reserves i les assignacions fins a l'assignació de tasques individuals.</span><span class="sxs-lookup"><span data-stu-id="c147d-111">For each named team member, the **Reconciliation** tab shows bookings and assignments down to the individual task assignment.</span></span> <span data-ttu-id="c147d-112">Mostra hores a les cel·les que poden representar períodes de temps de mesos a dies.</span><span class="sxs-lookup"><span data-stu-id="c147d-112">It shows hours in cells that can represent periods from months down to days.</span></span>

<span data-ttu-id="c147d-113">Al camp **Escala de temps**, podeu seleccionar **Mes**, **Setmana**o **Dia**.</span><span class="sxs-lookup"><span data-stu-id="c147d-113">In the **Timescale** field, you can select **Month**, **Week**, or **Day**.</span></span> <span data-ttu-id="c147d-114">Se selecciona **Setmana** per defecte.</span><span class="sxs-lookup"><span data-stu-id="c147d-114">By default, **Week** is selected.</span></span> <span data-ttu-id="c147d-115">No obstant, podeu canviar el valor per defecte seleccionant el botó **Configuració**.</span><span class="sxs-lookup"><span data-stu-id="c147d-115">However, you can change the default value by selecting the **Settings** button.</span></span> <span data-ttu-id="c147d-116">Quan s'obre la pestanya **Conciliació**, es mostra la data actual, però podeu utilitzar el control de calendari per avançar o retrocedir en el temps.</span><span class="sxs-lookup"><span data-stu-id="c147d-116">When the **Reconciliation** tab is opened, it shows the current date, but you can use the calendar control to move forward or backward in time.</span></span> <span data-ttu-id="c147d-117">Quan un projecte té una data d'inici que es troba en el futur, la pestanya mostra la data en què s'ha obert.</span><span class="sxs-lookup"><span data-stu-id="c147d-117">When a project has a start date that is in the future, the tab shows that date when it's opened.</span></span> <span data-ttu-id="c147d-118">El control de calendari també té opcions que us permeten desplaçar-vos a les dates d'inici i d'acabament del projecte.</span><span class="sxs-lookup"><span data-stu-id="c147d-118">The calendar control also has options that let you move to the project start and end dates.</span></span>

<span data-ttu-id="c147d-119">Podeu utilitzar els controls d'ampliació a cada recurs per mostrar els detalls de les reserves d'aquest recurs.</span><span class="sxs-lookup"><span data-stu-id="c147d-119">You can use the expander controls on each resource to show the details of that resource's bookings.</span></span> <span data-ttu-id="c147d-120">També podeu expandir les assignacions de cada recurs al nivell de tasca individual.</span><span class="sxs-lookup"><span data-stu-id="c147d-120">You can also expand each resource's assignments to the level of the individual task.</span></span>

<span data-ttu-id="c147d-121">A la part inferior de la pestanya **Conciliació** es mostra un total net global del projecte i la pestanya també inclou una columna total.</span><span class="sxs-lookup"><span data-stu-id="c147d-121">The bottom of the **Reconciliation** tab shows an overall net total for the project, and the tab also includes a total column.</span></span> <span data-ttu-id="c147d-122">Per a cada recurs, la pestanya pren la diferència entre les reserves d'un membre de l'equip al projecte i un valor consolidat de les assignacions de tasques d'aquest membre de l'equip.</span><span class="sxs-lookup"><span data-stu-id="c147d-122">For each resource, the tab takes the difference between a team member's bookings on the project and rollup of that team member's task assignments.</span></span> <span data-ttu-id="c147d-123">Idealment, la diferència hauria de ser 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="c147d-123">Ideally, the difference should be 0 (zero).</span></span> <span data-ttu-id="c147d-124">En altres paraules, no hi hauria d'haver diferències entre les reserves del recurs i les assignacions de tasques.</span><span class="sxs-lookup"><span data-stu-id="c147d-124">In other words, there should be no difference between the resource's bookings and its task assignments.</span></span> <span data-ttu-id="c147d-125">Qualsevol diferència s'indica amb color i ombrejat per indicar a dues condicions:</span><span class="sxs-lookup"><span data-stu-id="c147d-125">Any differences are indicated by color and shading to call out two conditions:</span></span>

- <span data-ttu-id="c147d-126">**Manca de reserves**: les manques de reserves es produeixen quan un recurs té més assignacions que reserves.</span><span class="sxs-lookup"><span data-stu-id="c147d-126">**Booking shortage** – Booking shortages occur when a resource has more assignments than bookings.</span></span> <span data-ttu-id="c147d-127">Com que aquesta capacitat no s'ha reservat, un administrador de projecte pot corregir aquesta situació ampliant les reserves del recurs fins a cobrir la manca.</span><span class="sxs-lookup"><span data-stu-id="c147d-127">Because this capacity hasn't been reserved, a project manager can correct this condition by extending the resource's bookings to cover the shortage.</span></span>
- <span data-ttu-id="c147d-128">**Excés de reserves**: un excés de reserves es produeix quan un recurs s'ha reservat al projecte però no s'ha assignat a tasques.</span><span class="sxs-lookup"><span data-stu-id="c147d-128">**Excess bookings** – Excess bookings occur when a resource has been booked to the project but hasn't been assigned to tasks.</span></span> <span data-ttu-id="c147d-129">Aquesta situació pot ser acceptable, per exemple, si el recurs s'ha reservat abans de l'assignació de tasques.</span><span class="sxs-lookup"><span data-stu-id="c147d-129">This condition might be acceptable if, for example, the resource has been booked before task assignment occurs.</span></span> <span data-ttu-id="c147d-130">No obstant, en altres casos, pot ser que el recurs no estigui planificat per assignar-se a tasques.</span><span class="sxs-lookup"><span data-stu-id="c147d-130">However, in other cases, the resource might not be planned to be assigned.</span></span> <span data-ttu-id="c147d-131">En aquests casos, l'administrador del projecte hauria de considerar la cancel·lació de les reserves del recurs, de manera que la capacitat pugui utilitzar-se per a un altre projecte.</span><span class="sxs-lookup"><span data-stu-id="c147d-131">In these cases, the project manager should consider canceling the resource's bookings, so that the capacity can be used for another project.</span></span>

> [!NOTE]
> <span data-ttu-id="c147d-132">La llegenda d'aquestes condicions podria estar amagada per deixar més espai per a la quadrícula.</span><span class="sxs-lookup"><span data-stu-id="c147d-132">The legend for these conditions might be hidden to leave more room for the grid.</span></span> <span data-ttu-id="c147d-133">En aquest cas, podeu fer que la llegenda sigui visible seleccionant el botó **Configuració**.</span><span class="sxs-lookup"><span data-stu-id="c147d-133">In this case, you can make the legend visible by selecting the **Settings** button.</span></span>

<span data-ttu-id="c147d-134">En alguns casos, quan el camp **Escala de temps** està definit a un nivell superior a **Dia**, les diferències es poden calcular com a 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="c147d-134">In some cases, when the **Timescale** field is set to a level that is higher than **Day**, differences might be calculated as 0 (zero).</span></span> <span data-ttu-id="c147d-135">Per exemple, al nivell de **Mes**, la diferència neta per a un recurs podria ser 0 (zero) per indicar que les tasques equivalen a les reserves.</span><span class="sxs-lookup"><span data-stu-id="c147d-135">For example, at the **Month** level, the net difference for a resource might be 0 (zero) to indicate that bookings equal assignments.</span></span> <span data-ttu-id="c147d-136">No obstant, si ho mireu al nivell de **Setmana**, podeu veure que hi ha assignacions de 0 (zero) hores i reserves de 40 hores a la primera setmana del mes, i assignacions de 40 hores i reserves de 0 (zero) hores a la segona setmana del mes.</span><span class="sxs-lookup"><span data-stu-id="c147d-136">However, if you look at the **Week** level, you might see that there are assignments of 0 (zero) hours and bookings of 40 hours in the first week of the month, and assignments of 40 hours and bookings of 0 (zero) hours in the second week of the month.</span></span> <span data-ttu-id="c147d-137">Tot i que les reserves i assignacions totals per al mes són iguals, difereixen per setmana.</span><span class="sxs-lookup"><span data-stu-id="c147d-137">Although the total bookings and assignments for the month are equal, they differ by week.</span></span>

<span data-ttu-id="c147d-138">Quan visualitzeu el temps en nivells superiors, la pestanya **Conciliació** mostra un indicador a les cel·les per informar-vos que hi ha diferències en nivells de temps inferiors.</span><span class="sxs-lookup"><span data-stu-id="c147d-138">When you view higher time levels, the **Reconciliation** tab shows a cell indicator to notify you that there are differences at lower time levels.</span></span> <span data-ttu-id="c147d-139">Per exemple, en la il·lustració següent, un indicador de cel la apareix a la cel·la per al mes d'octubre de 2018 per al recurs que s'anomena Gabriela Magrinyà.</span><span class="sxs-lookup"><span data-stu-id="c147d-139">For example, in the following illustration, a cell indicator appears in the cell for the month of October 2018 for the resource that is named Katelyn Merritt.</span></span> <span data-ttu-id="c147d-140">Per tant, podeu veure que, tot i que les reserves i assignacions del recurs són iguals quan s'agreguen a nivell de **Mes**, no coincideixen en els nivells inferiors.</span><span class="sxs-lookup"><span data-stu-id="c147d-140">Therefore, you can see that, even though the resource's bookings and assignments are equal when they are aggregated at the **Month** level, they don't match at lower levels.</span></span>

![Assignacions i reserves no coincidents](media/reconcile-assignments-01.JPG)

<span data-ttu-id="c147d-142">Feu doble clic en una cel·la per apropar-vos al nivell inferior següent i visualitzar la diferència.</span><span class="sxs-lookup"><span data-stu-id="c147d-142">Double-click a cell to zoom in to the next lower level and view the difference.</span></span> <span data-ttu-id="c147d-143">Per exemple, si feu doble clic a la diferència d'octubre de 2018 per a la Gabriela Magrinyà, baixareu fins al nivell de **Setmana**.</span><span class="sxs-lookup"><span data-stu-id="c147d-143">For example, if you double-click the October 2018 difference for Katelyn Merritt, you drill down to the **Week** level.</span></span> <span data-ttu-id="c147d-144">Llavors podeu veure que el recurs té reserves de 16 hores però cap assignació la primera quinzena d'octubre i 16 hores d'assignacions però cap reserva la tercera setmana d'octubre.</span><span class="sxs-lookup"><span data-stu-id="c147d-144">You can then see that the resource has bookings of 16 hours but no assignments in the first two weeks of October, and 16 hours of assignments but no bookings in the third week of October.</span></span>

![Assignacions i reserves no coincidents](media/reconcile-assignments-02.JPG)

<span data-ttu-id="c147d-146">Podeu fer clic amb el botó dret en una cel·la per allunyar el nivell superior següent.</span><span class="sxs-lookup"><span data-stu-id="c147d-146">You can right-click a cell to zoom out the next higher level.</span></span> <span data-ttu-id="c147d-147">També podeu desactivar l'indicador de la cel·la seleccionant el botó **Configuració**.</span><span class="sxs-lookup"><span data-stu-id="c147d-147">You can also turn off the cell indicator by selecting the **Settings** button.</span></span> 

<span data-ttu-id="c147d-148">També podeu utilitzar els botons **Anterior** i **Següent** sobre la quadrícula per desplaçar-vos per les diferències en el vostre projecte.</span><span class="sxs-lookup"><span data-stu-id="c147d-148">You can also use the **Previous** and **Next** buttons above the grid to move through any differences in your project.</span></span> <span data-ttu-id="c147d-149">Per utilitzar aquests botons, heu de seleccionar primer un recurs.</span><span class="sxs-lookup"><span data-stu-id="c147d-149">To use these buttons, you must first select a resource.</span></span> <span data-ttu-id="c147d-150">Seleccioneu **Següent** per anar a la diferència següent entre les reserves i les assignacions per a aquest recurs.</span><span class="sxs-lookup"><span data-stu-id="c147d-150">Select **Next** to go to the next difference between bookings and assignments for that resource.</span></span> <span data-ttu-id="c147d-151">Seleccioneu **Anterior** per tornar a la diferència anterior.</span><span class="sxs-lookup"><span data-stu-id="c147d-151">Select **Previous** to go to the previous difference.</span></span>

<span data-ttu-id="c147d-152">En situacions en què teniu assignacions de tasques per a un recurs però no reserves, podeu seleccionar la manca de reserves i seleccionar **Amplia la reserva**.</span><span class="sxs-lookup"><span data-stu-id="c147d-152">In situations where you have task assignments for a resource but no bookings, you can select the booking shortage and then select **Extend Booking**.</span></span> <span data-ttu-id="c147d-153">A continuació, podeu veure la reserva necessària per tal d'abordar la manca del recurs.</span><span class="sxs-lookup"><span data-stu-id="c147d-153">You can then see the booking that is required in order to address the resource's shortage.</span></span> <span data-ttu-id="c147d-154">També podeu visualitzar les reserves del recurs en el projecte actual i en altres projectes.</span><span class="sxs-lookup"><span data-stu-id="c147d-154">You can also view the resource's bookings on the current project and other projects.</span></span> <span data-ttu-id="c147d-155">Seleccioneu **D'acord** per crear la reserva del recurs sense tenir en compte la disponibilitat actual.</span><span class="sxs-lookup"><span data-stu-id="c147d-155">Select **OK** to create the booking for the resource without regard to current availability.</span></span> <span data-ttu-id="c147d-156">L'administrador de projectes o administrador de recursos poden utilitzar el tauler de planificació per administrar les situacions en què el recurs té un excés de reserves més enllà de la seva capacitat perquè s'han ampliat les reserves.</span><span class="sxs-lookup"><span data-stu-id="c147d-156">The project manager or resource manager can then use Schedule Board to manage situations where a resource has become overbooked beyond capacity because its bookings were extended.</span></span>

## <a name="managing-with-time-zones"></a><span data-ttu-id="c147d-157">Administració amb fusos horaris</span><span class="sxs-lookup"><span data-stu-id="c147d-157">Managing with time zones</span></span>
<span data-ttu-id="c147d-158">Per garantir un resultat precís i predictible quan utilitzeu Amplia la reserva, hi ha dos requisits previs clau que s'han de complir:</span><span class="sxs-lookup"><span data-stu-id="c147d-158">To ensure accurate and predictable results when using Extend Booking, there are two key prerequisites that must be met:</span></span>  

- <span data-ttu-id="c147d-159">L'usuari ha de configurar el fus horari del dispositiu perquè coincideixi amb el fus horari definit a la Configuració de personalització del sistema.</span><span class="sxs-lookup"><span data-stu-id="c147d-159">The user must configure their device's time zone to match the time zone defined in your system's Personalization Settings.</span></span>
 
  ![Configuració de fus horari al Windows 10](media/reconcile-assignments-03.png)

  ![Configuració del fus horari a la Configuració de personalització](media/reconcile-assignments-04.png)
 
- <span data-ttu-id="c147d-162">El Recurs reservable ha de tenir com a mínim un minut de temps de treball que se solapi amb els contorns que s'utilitzen per definir l'extensió sol·licitada.</span><span class="sxs-lookup"><span data-stu-id="c147d-162">The Bookable Resource must have at least one minute of working time that overlaps with the contours that are used to define the requested extension.</span></span> <span data-ttu-id="c147d-163">Per exemple, a l'exemple següent es mostra una revisió de recursos amb hores de feina que cauen entre les 9:00 h i les 19:00 h.</span><span class="sxs-lookup"><span data-stu-id="c147d-163">For instance, the following example shows review resources with working hours that fall between 9:00 AM and 7:00 PM.</span></span> 

  ![Comparativa de contorns de recursos](media/reconcile-assignments-05.png)

<span data-ttu-id="c147d-165">La taula següent mostra:</span><span class="sxs-lookup"><span data-stu-id="c147d-165">The following table shows:</span></span>

- <span data-ttu-id="c147d-166">Una plantilla de calendari de projecte.</span><span class="sxs-lookup"><span data-stu-id="c147d-166">A project calendar template.</span></span>
- <span data-ttu-id="c147d-167">Recurs A: aquest recurs té el mateix calendari i es troba al mateix fus horari que el projecte.</span><span class="sxs-lookup"><span data-stu-id="c147d-167">Resource A: This resource has the same calendar and is in the same time zone as the project.</span></span> <span data-ttu-id="c147d-168">L'hora d'inici de les reserves serà les 9:00 h.</span><span class="sxs-lookup"><span data-stu-id="c147d-168">The start time of the bookings will be 9:00 AM.</span></span>
- <span data-ttu-id="c147d-169">Recurs B: aquest recurs es troba en un fus horari diferent del projecte i, per tant, s'inicia a les 7:00 h en el seu fus horari.</span><span class="sxs-lookup"><span data-stu-id="c147d-169">Resources B: This resource is located in a different time zone than the project and therefore starts at 7:00 AM in their time zone.</span></span> <span data-ttu-id="c147d-170">No obstant això, les reserves començaran a partir de 9:00 h, que és la primera hora d'inici del contorn d'assignació.</span><span class="sxs-lookup"><span data-stu-id="c147d-170">However, the bookings will begin at 9:00 AM as that is the earliest start time of the assignment contour.</span></span>
- <span data-ttu-id="c147d-171">Recursos C i D: els recursos també es troben en fusos horaris diferents, diferents entre si i el projecte, i les seves reserves no comencen abans que les hores d'inici disponibles respectives.</span><span class="sxs-lookup"><span data-stu-id="c147d-171">Resources C and D: The resources are also located in different time zones, both different from each other and the project, and their bookings start no earlier than their respective available start times.</span></span>

|<span data-ttu-id="c147d-172">Entitat</span><span class="sxs-lookup"><span data-stu-id="c147d-172">Entity</span></span>  |<span data-ttu-id="c147d-173">Calendari</span><span class="sxs-lookup"><span data-stu-id="c147d-173">Calendar</span></span>  |
|-|-|
|<span data-ttu-id="c147d-174">Plantilla de calendari de projecte</span><span class="sxs-lookup"><span data-stu-id="c147d-174">Project calendar template</span></span>   | ![calendari de projecte](media/reconcile-assignments-06.png) |
|<span data-ttu-id="c147d-176">Recurs A</span><span class="sxs-lookup"><span data-stu-id="c147d-176">Resource A</span></span>  | ![Calendari del recurs A](media/reconcile-assignments-06.png) |
|<span data-ttu-id="c147d-178">Recurs B</span><span class="sxs-lookup"><span data-stu-id="c147d-178">Resource B</span></span>  |  ![Calendari del recurs B](media/reconcile-assignments-07.png) |
|<span data-ttu-id="c147d-180">Recurs C</span><span class="sxs-lookup"><span data-stu-id="c147d-180">Resource C</span></span>  |  ![Calendari del recurs C](media/reconcile-assignments-08.png) |
|<span data-ttu-id="c147d-182">Recurs D</span><span class="sxs-lookup"><span data-stu-id="c147d-182">Resource D</span></span>  | ![Calendari del recurs D](media/reconcile-assignments-09.png)  |
 
<span data-ttu-id="c147d-184">Quan navegueu a la visualització de conciliació, es visualitzaran les assignacions de recursos i les manques de reserva associades.</span><span class="sxs-lookup"><span data-stu-id="c147d-184">When you navigate to the reconciliation view, the resource assignments and the associated booking shortages will be displayed.</span></span>
 <span data-ttu-id="c147d-185">![Visualització de conciliació abans de l'ampliació](media/reconcile-assignments-10.png)</span><span class="sxs-lookup"><span data-stu-id="c147d-185">![Reconciliation view before extension](media/reconcile-assignments-10.png)</span></span>

<span data-ttu-id="c147d-186">Després d'executar la característica Amplia la reserva en cada recurs, les reserves s'amplien correctament per a cada recurs.</span><span class="sxs-lookup"><span data-stu-id="c147d-186">After the Extend Booking functionality has been executed on each resource, bookings are successfully extended for each resource.</span></span> <span data-ttu-id="c147d-187">Això és degut a que les hores de feina de cada recurs es solapen amb els contorns de la manca.</span><span class="sxs-lookup"><span data-stu-id="c147d-187">This is because each resource’s working hours overlapped with the contours of the shortage.</span></span>
 <span data-ttu-id="c147d-188">![Visualització de conciliació després de l'ampliació de la reserva](media/reconcile-assignments-11.png)</span><span class="sxs-lookup"><span data-stu-id="c147d-188">![Reconciliation view after booking extension](media/reconcile-assignments-11.png)</span></span> 

<span data-ttu-id="c147d-189">No obstant, una visualització més detallada de les reserves mostra diferències en l'hora d'inici de les reserves.</span><span class="sxs-lookup"><span data-stu-id="c147d-189">However, a closer look at the details of the bookings shows differences in the start time of the bookings.</span></span> <span data-ttu-id="c147d-190">Les reserves no començaran abans que l'hora d'inici del contorn d'assignació i ni abans de l'hora d'inici disponible del recurs.</span><span class="sxs-lookup"><span data-stu-id="c147d-190">The bookings will start no earlier than the start time of the assignment contour and no earlier than the available start time of the resource.</span></span>
 <span data-ttu-id="c147d-191">![Noves reserves dels recursos al tauler de planificació](media/reconcile-assignments-12.png)</span><span class="sxs-lookup"><span data-stu-id="c147d-191">![New bookings of the resources in the schedule board](media/reconcile-assignments-12.png)</span></span>