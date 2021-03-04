---
title: Proposar recursos de projecte
description: Aquest tema proporciona informació sobre la proposta de recursos del projecte.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: 0a3eaa9929770c91523831d92744d5084aa28cb8
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147506"
---
# <a name="propose-project-resources"></a><span data-ttu-id="befd1-103">Proposar recursos de projecte</span><span class="sxs-lookup"><span data-stu-id="befd1-103">Propose project resources</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="befd1-104">Els administradors de recursos poden proposar un recurs a l'administrador del projecte mitjançant una sol·licitud de recursos.</span><span class="sxs-lookup"><span data-stu-id="befd1-104">Resource managers can propose a resource to the project manager by using a resource request.</span></span>

1. <span data-ttu-id="befd1-105">A la graella de sol·licitud o a la sol·licitud en si mateixa, seleccioneu **Cerca recursos**.</span><span class="sxs-lookup"><span data-stu-id="befd1-105">From the request grid or the request itself, select **Find Resources**.</span></span>
2. <span data-ttu-id="befd1-106">A la pàgina **Auxiliar de planificació,** seleccioneu el recurs i, a continuació, a la subfinestra **Crea una reserva de recursos**, al camp **Estat de la reserva**, seleccioneu **Reserva**.</span><span class="sxs-lookup"><span data-stu-id="befd1-106">On the **Schedule Assistant** page, select the resource, and then, in the **Create Resource Booking** pane, in the **Booking Status** field, select **Book**.</span></span>

    ![Recurs proposat seleccionat](media/Resource-Management-image62.png)

<span data-ttu-id="befd1-108">Es produeixen les següents actualitzacions d'estat:</span><span class="sxs-lookup"><span data-stu-id="befd1-108">The following status updates occur:</span></span>

- <span data-ttu-id="befd1-109">A la pàgina **Auxiliar de planificació**, els indicadors d'estat s'actualitzen per indicar que es proposa la reserva, no que es reserva de manera fixa.</span><span class="sxs-lookup"><span data-stu-id="befd1-109">On the **Schedule Assistant** page, the status indicators are updated to indicate that the booking is proposed, not hard-booked.</span></span>

    ![Indicadors d'estat per a la reserva de proposta a la pàgina Auxiliar de planificació](media/Resource-Management-image63.png)

- <span data-ttu-id="befd1-111">A la sol·licitud de recursos, l'estat canvia a **Necessita revisió**.</span><span class="sxs-lookup"><span data-stu-id="befd1-111">On the resource request, the status is changed to **Needs Review**.</span></span>

    ![Estat de sol·licitud de recursos canviat a Necessita revisió](media/Resource-Management-image64.png)

- <span data-ttu-id="befd1-113">A la pestanya **Equip** del projecte, el valor **Estat de la sol·licitud** de l'equip genèric es canvia a **Necessita revisió**.</span><span class="sxs-lookup"><span data-stu-id="befd1-113">On the **Team** tab of the project, the generic team member's **Request Status** value is changed to **Needs Review**.</span></span>

    ![Estat de la sol·licitud de l'equip genèric canviat a Necessita revisió a la pestanya Equip](media/Resource-Management-image48.png)

<span data-ttu-id="befd1-115">L'administrador de projectes pot acceptar o rebutjar la proposta.</span><span class="sxs-lookup"><span data-stu-id="befd1-115">The project manager can either accept or reject the proposal.</span></span>

<span data-ttu-id="befd1-116">Quan els administradors de recursos processen les sol·licituds de recursos, poden utilitzar qualsevol dels enfocaments següents:</span><span class="sxs-lookup"><span data-stu-id="befd1-116">When resource managers process resource requests, they can use any of the following approaches:</span></span>

- <span data-ttu-id="befd1-117">Proposar diversos recursos per satisfer la demanda si no hi ha cap recurs disponible per complir les hores requerides.</span><span class="sxs-lookup"><span data-stu-id="befd1-117">Propose multiple resources to satisfy the demand if no single resource is available to fulfill the required hours.</span></span> <span data-ttu-id="befd1-118">Les hores proposades es divideixen a continuació entre diversos recursos que poden satisfer les hores requerides.</span><span class="sxs-lookup"><span data-stu-id="befd1-118">Proposed hours are then split among multiple resources that can satisfy the required hours.</span></span> <span data-ttu-id="befd1-119">En aquest escenari, les hores no es poden superposar.</span><span class="sxs-lookup"><span data-stu-id="befd1-119">In this scenario, the hours can't overlap.</span></span>
- <span data-ttu-id="befd1-120">Proposar menys recursos dels que calguin.</span><span class="sxs-lookup"><span data-stu-id="befd1-120">Propose fewer resources than are required.</span></span> <span data-ttu-id="befd1-121">En aquest escenari, la capacitat proposada del recurs és inferior a les hores requerides que especifica el sol·licitant.</span><span class="sxs-lookup"><span data-stu-id="befd1-121">In this scenario, the proposed resource capacity is less than the required hours that the requestor specified.</span></span> <span data-ttu-id="befd1-122">Per tant, quan el sol·licitant accepta els recursos proposats, es crea un requisit de recurs no complert per capturar la resta de la demanda.</span><span class="sxs-lookup"><span data-stu-id="befd1-122">Therefore, when the requestor accepts the proposed resources, an unfulfilled resource requirement is created to capture the remaining demand.</span></span>
- <span data-ttu-id="befd1-123">Reservar diversos recursos per satisfer la demanda si no hi ha cap recurs disponible per completar el treball.</span><span class="sxs-lookup"><span data-stu-id="befd1-123">Book multiple resources to satisfy the demand if no single resource is available to complete the work.</span></span>
- <span data-ttu-id="befd1-124">Reservar menys recursos dels que calguin.</span><span class="sxs-lookup"><span data-stu-id="befd1-124">Book fewer resources than are required.</span></span> <span data-ttu-id="befd1-125">En aquest escenari, les hores reservades són menys que les hores requerides.</span><span class="sxs-lookup"><span data-stu-id="befd1-125">In this scenario, the booked hours are fewer than the required hours.</span></span> <span data-ttu-id="befd1-126">El sistema us guia per proposar recursos en comptes de reserves, de manera que el sol·licitant pugui comprovar i fer un seguiment de la demanda restant.</span><span class="sxs-lookup"><span data-stu-id="befd1-126">The system guides you to propose resources instead of bookings, so that the requestor can verify and keep track of remaining demand.</span></span>

## <a name="billable-utilization"></a><span data-ttu-id="befd1-127">Ús facturable</span><span class="sxs-lookup"><span data-stu-id="befd1-127">Billable utilization</span></span>

<span data-ttu-id="befd1-128">Els recursos poden tenir un objectiu d'ús facturable.</span><span class="sxs-lookup"><span data-stu-id="befd1-128">Resources can have a target billable utilization.</span></span> <span data-ttu-id="befd1-129">Aquest objectiu d'ús es defineix com un atribut de la funció per defecte d'un recurs o es defineix al registre del recurs individual que es pot reservar.</span><span class="sxs-lookup"><span data-stu-id="befd1-129">This target utilization is either defined as an attribute on a resource's default role or set on the record of the individual bookable resource.</span></span> <span data-ttu-id="befd1-130">Els càlculs d'ús es basen en les hores reals que els recursos han informat mitjançant les entrades de temps aprovades.</span><span class="sxs-lookup"><span data-stu-id="befd1-130">Utilization calculations are based on the actual hours that resources have reported by using approved time entries.</span></span>

<span data-ttu-id="befd1-131">Les següents fórmules s'utilitzen per calcular l'ús:</span><span class="sxs-lookup"><span data-stu-id="befd1-131">The following formulas are used to calculate utilization:</span></span>

- <span data-ttu-id="befd1-132">Ús facturable = Hores reals imputables ÷ Capacitat de recursos</span><span class="sxs-lookup"><span data-stu-id="befd1-132">Billable utilization = Chargeable actual hours ÷ Resource capacity</span></span>
- <span data-ttu-id="befd1-133">Ús no facturable = Temps real amb ID de tipus de facturació = No imputable, Gratuït o No disponible ÷ Capacitat de recursos</span><span class="sxs-lookup"><span data-stu-id="befd1-133">Non-billable utilization = Actual time with billing type ID = Non-chargeable, Complementary, or Not available ÷ Resource capacity</span></span>
- <span data-ttu-id="befd1-134">Intern = Temps real sense contracte de vendes ÷ Capacitat de recursos</span><span class="sxs-lookup"><span data-stu-id="befd1-134">Internal = Actual time with no sales contract ÷ Resource capacity</span></span>
- <span data-ttu-id="befd1-135">Capacitat de recursos = Hores de treball - Fora de l'oficina - Dies no hàbils</span><span class="sxs-lookup"><span data-stu-id="befd1-135">Resource capacity = Resource work hours – Out-of-office – Non-working days</span></span>

<span data-ttu-id="befd1-136">Podeu cercar la visualització **Ús de recursos** a la subfinestra **Recursos**.</span><span class="sxs-lookup"><span data-stu-id="befd1-136">You can find the **Resource Utilization** view in the **Resources** pane.</span></span>

![Visualització Ús de recursos](media/Resource-Management-image65.png)

<span data-ttu-id="befd1-138">Cada cel·la de la quadrícula representa el percentatge d'ús facturable del recurs en un període, com ara un dia, una setmana o un mes.</span><span class="sxs-lookup"><span data-stu-id="befd1-138">Each cell in the grid represents the billable utilization percentage of the resource in a period, such as a day, week, or month.</span></span> <span data-ttu-id="befd1-139">Les següents fórmules s'utilitzen per acolorir les cel·les:</span><span class="sxs-lookup"><span data-stu-id="befd1-139">The following formulas are used to color the cells:</span></span>

- <span data-ttu-id="befd1-140">**Verd:** Ús facturable \>= Objectiu d'ús de recursos</span><span class="sxs-lookup"><span data-stu-id="befd1-140">**Green:** Billable utilization \>= Resource target utilization</span></span>
- <span data-ttu-id="befd1-141">**Groc:** Objectiu d'ús - 20 \<= Ús facturable \< Objectiu d'ús</span><span class="sxs-lookup"><span data-stu-id="befd1-141">**Yellow:** Target utilization – 20 \<= Billable utilization \< Target utilization</span></span>
- <span data-ttu-id="befd1-142">**Vermell:** Ús facturable \< Objectiu d'ús - 20</span><span class="sxs-lookup"><span data-stu-id="befd1-142">**Red:** Billable utilization \< Target utilization – 20</span></span>

<span data-ttu-id="befd1-143">Com que la visualització **Ús de recursos** està basada en el tauler de planificació, podeu utilitzar les capacitats de filtratge del tauler de planificació per filtrar els resultats.</span><span class="sxs-lookup"><span data-stu-id="befd1-143">Because the **Resource Utilization** view is based on the Schedule Board, you can use the filtering capabilities of the Schedule Board to filter your results.</span></span>

<span data-ttu-id="befd1-144">La quadrícula requereix que definiu un objectiu d'ús en la funció o en el recurs individual.</span><span class="sxs-lookup"><span data-stu-id="befd1-144">The grid requires that you set a target utilization on either the role or the individual resource.</span></span> <span data-ttu-id="befd1-145">Per configurar-ho, aneu a **Recursos** \> **Funcions de recurs**.</span><span class="sxs-lookup"><span data-stu-id="befd1-145">To do this setup, go to **Resources** \> **Resource roles**.</span></span>

<span data-ttu-id="befd1-146">A més, cal assignar una funció per defecte a cadascun dels recursos que es pot reservar.</span><span class="sxs-lookup"><span data-stu-id="befd1-146">Additionally, a default role must be assigned to each bookable resource.</span></span> <span data-ttu-id="befd1-147">Aneu a **Recursos** \> **Recursos**.</span><span class="sxs-lookup"><span data-stu-id="befd1-147">Go to **Resources** \> **Resources**.</span></span> <span data-ttu-id="befd1-148">A la pestanya **Project Service**, comproveu que es defineix una funció de recurs i que el camp **Per defecte** està definit com a **Sí**.</span><span class="sxs-lookup"><span data-stu-id="befd1-148">On the **Project Service** tab, verify that a resource role is defined, and that the **Is Default** field for it is set to **Yes**.</span></span> <span data-ttu-id="befd1-149">Podeu afegir funcions addicionals on **Per defecte = No**.</span><span class="sxs-lookup"><span data-stu-id="befd1-149">You can add additional roles where **Is Default = No**.</span></span> <span data-ttu-id="befd1-150">La funció on **Per defecte = Sí** s'utilitza per avaluar l'ús del recurs en relació amb l'objectiu per a aquesta funció.</span><span class="sxs-lookup"><span data-stu-id="befd1-150">The role where the **Is Default = Yes** is used to evaluate the resource's utilization against the target for that role.</span></span>

![Conjunt de funcions per defecte](media/Resource-Management-image67.png)

<span data-ttu-id="befd1-152">A la pestanya **Project Service** també podeu definir un objectiu d'ús individual per al recurs.</span><span class="sxs-lookup"><span data-stu-id="befd1-152">On the **Project Service** tab, you can also set an individual target utilization for the resource.</span></span> <span data-ttu-id="befd1-153">A continuació, el càlcul d'ús utilitza l'objectiu d'ús per avaluar l'objectiu del recurs en comptes de l'objectiu de la funció per defecte del recurs.</span><span class="sxs-lookup"><span data-stu-id="befd1-153">The utilization calculation then uses that target utilization to evaluate the resource's target instead of the target of the resource's default role.</span></span>

<span data-ttu-id="befd1-154">L'ús es mostra per a un recurs només si aquest recurs té temps aprovat imputable durant el període que es mostra a la quadrícula.</span><span class="sxs-lookup"><span data-stu-id="befd1-154">Utilization is shown for a resource only if that resource has approved, chargeable time during the period that is shown in the grid.</span></span>

## <a name="resource-availability"></a><span data-ttu-id="befd1-155">Disponibilitat de recursos</span><span class="sxs-lookup"><span data-stu-id="befd1-155">Resource availability</span></span>

<span data-ttu-id="befd1-156">És important que els administradors de recursos puguin visualitzar la disponibilitat dels recursos i actualitzar les reserves.</span><span class="sxs-lookup"><span data-stu-id="befd1-156">It's critical that resource managers be able to view the availability of resources and update bookings.</span></span> <span data-ttu-id="befd1-157">En alguns casos, no hi ha cap demanda formal (sol·licitud de recurs), però un administrador de recursos ha de respondre a una demanda no planificada que entri per canals com ara el correu electrònic, una trucada telefònica o un missatge instantani.</span><span class="sxs-lookup"><span data-stu-id="befd1-157">In some cases, there is no formal demand (resource request), but a resource manager must respond to an unplanned demand that comes through channels such as an email, phone call, or instant message.</span></span> <span data-ttu-id="befd1-158">Els administradors de recursos utilitzen el tauler de planificació per actualitzar els recursos i les reserves.</span><span class="sxs-lookup"><span data-stu-id="befd1-158">Resource managers use the Schedule Board to update resources and bookings.</span></span>

<span data-ttu-id="befd1-159">Les hores de treball del recurs s'utilitzen com a base per calcular la disponibilitat d'un recurs.</span><span class="sxs-lookup"><span data-stu-id="befd1-159">Resource work hours are used as the basis for calculating the availability of a resource.</span></span> <span data-ttu-id="befd1-160">Les reserves de recursos consumeixen la capacitat dels recursos.</span><span class="sxs-lookup"><span data-stu-id="befd1-160">Resource bookings consume the capacity of the resources.</span></span>

![Tauler de planificació](media/Resource-Management-image68.png)

<span data-ttu-id="befd1-162">El tauler de planificació utilitza colors i ombrejat per mostrar les reserves, la disponibilitat i l'excés de reserves, i també l'estat de les reserves.</span><span class="sxs-lookup"><span data-stu-id="befd1-162">The Schedule Board uses colors and shading to show bookings, availability, and overbookings, and also the status of bookings.</span></span> <span data-ttu-id="befd1-163">Un paràmetre de la configuració del tauler de planificació us permet mostrar una llegenda.</span><span class="sxs-lookup"><span data-stu-id="befd1-163">A setting in the Schedule Board settings lets you show a legend.</span></span>

<span data-ttu-id="befd1-164">Si una fletxa que apunta a la dreta apareix al costat d'un recurs individual que es pot reservar al tauler de planificació, el recurs es podrà expandir per mostrar els detalls del treball en què està reservat el recurs.</span><span class="sxs-lookup"><span data-stu-id="befd1-164">If a right-pointing arrow appears next to an individual bookable resource on the Schedule Board, the resource can be expanded to show details of the work that the resource is booked on.</span></span>

![Recurs que es pot reservar expandit al tauler de planificació](media/Resource-Management-image69.png)

<span data-ttu-id="befd1-166">Com que el Dynamics 365 Project Service Automation utilitza el motor del Universal Resource Scheduling, si també teniu instal·lat el Dynamics 365 Field Service, podeu visualitzar els detalls de les reserves de recursos per a projectes, ordres de treball i altres entitats a les quals hàgiu ampliat la planificació.</span><span class="sxs-lookup"><span data-stu-id="befd1-166">Because Dynamics 365 Project Service Automation uses the Universal Resource Scheduling engine, if you also have Dynamics 365 Field Service installed, you can view the details of resource bookings for projects, work orders, and any other entities that you've extended scheduling to.</span></span>

![Detalls de les reserves de recursos per a projectes i ordres de treball](media/Resource-Management-image70.png)

<span data-ttu-id="befd1-168">Per visualitzar més detalls d'un recurs individual, feu-hi clic amb el botó dret per obrir la targeta de recursos.</span><span class="sxs-lookup"><span data-stu-id="befd1-168">To view more details about an individual resource, right-click it to open the resource card.</span></span>

![Targeta de recursos](media/Resource-Management-image71.png)
