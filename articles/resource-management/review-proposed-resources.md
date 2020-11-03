---
title: Revisió dels recursos proposats
description: En aquest tema es proporciona informació sobre la manera de proposar recursos de projecte.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: ad5cbdeb5fe05e6115eb024833a8d58b626ea4c9
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072179"
---
# <a name="review-proposed-resources"></a><span data-ttu-id="2fde1-103">Revisió dels recursos proposats</span><span class="sxs-lookup"><span data-stu-id="2fde1-103">Review proposed resources</span></span>

<span data-ttu-id="2fde1-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_</span><span class="sxs-lookup"><span data-stu-id="2fde1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="2fde1-105">Els administradors de recursos poden proposar un recurs a l'administrador del projecte mitjançant una sol·licitud de recursos.</span><span class="sxs-lookup"><span data-stu-id="2fde1-105">Resource managers can propose a resource to the project manager by using a resource request.</span></span>

1. <span data-ttu-id="2fde1-106">A la graella de sol·licitud o a la sol·licitud en si mateixa, seleccioneu **Cerca recursos**.</span><span class="sxs-lookup"><span data-stu-id="2fde1-106">From the request grid or the request itself, select **Find Resources**.</span></span>
2. <span data-ttu-id="2fde1-107">A la pàgina **Auxiliar de planificació,** seleccioneu el recurs i, a continuació, a la subfinestra **Crea una reserva de recursos** , al camp **Estat de la reserva** , seleccioneu **Reserva**.</span><span class="sxs-lookup"><span data-stu-id="2fde1-107">On the **Schedule Assistant** page, select the resource, and then, in the **Create Resource Booking** pane, in the **Booking Status** field, select **Book**.</span></span>

<span data-ttu-id="2fde1-108">Es produeixen les següents actualitzacions d'estat:</span><span class="sxs-lookup"><span data-stu-id="2fde1-108">The following status updates occur:</span></span>

- <span data-ttu-id="2fde1-109">A la pàgina **Auxiliar de planificació** , els indicadors d'estat s'actualitzen per indicar que es proposa la reserva, no que es reserva de manera fixa.</span><span class="sxs-lookup"><span data-stu-id="2fde1-109">On the **Schedule Assistant** page, the status indicators are updated to indicate that the booking is proposed, not hard-booked.</span></span>
- <span data-ttu-id="2fde1-110">A la sol·licitud de recursos, l'estat canvia a **Necessita revisió**.</span><span class="sxs-lookup"><span data-stu-id="2fde1-110">On the resource request, the status is changed to **Needs Review**.</span></span>
- <span data-ttu-id="2fde1-111">A la pestanya **Equip** del projecte, el valor **Estat de la sol·licitud** de l'equip genèric es canvia a **Necessita revisió**.</span><span class="sxs-lookup"><span data-stu-id="2fde1-111">On the **Team** tab of the project, the generic team member's **Request Status** value is changed to **Needs Review**.</span></span>

<span data-ttu-id="2fde1-112">L'administrador de projectes pot acceptar o rebutjar la proposta.</span><span class="sxs-lookup"><span data-stu-id="2fde1-112">The project manager can either accept or reject the proposal.</span></span>

<span data-ttu-id="2fde1-113">Quan els administradors de recursos processen les sol·licituds de recursos, poden utilitzar qualsevol dels enfocaments següents:</span><span class="sxs-lookup"><span data-stu-id="2fde1-113">When resource managers process resource requests, they can use any of the following approaches:</span></span>

- <span data-ttu-id="2fde1-114">Proposar diversos recursos per satisfer la demanda si no hi ha cap recurs disponible per complir les hores requerides.</span><span class="sxs-lookup"><span data-stu-id="2fde1-114">Propose multiple resources to satisfy the demand if no single resource is available to fulfill the required hours.</span></span> <span data-ttu-id="2fde1-115">Les hores proposades es divideixen a continuació entre diversos recursos que poden satisfer les hores requerides.</span><span class="sxs-lookup"><span data-stu-id="2fde1-115">Proposed hours are then split among multiple resources that can satisfy the required hours.</span></span> <span data-ttu-id="2fde1-116">En aquest escenari, les hores no es poden superposar.</span><span class="sxs-lookup"><span data-stu-id="2fde1-116">In this scenario, the hours can't overlap.</span></span>
- <span data-ttu-id="2fde1-117">Proposar menys recursos dels que calguin.</span><span class="sxs-lookup"><span data-stu-id="2fde1-117">Propose fewer resources than are required.</span></span> <span data-ttu-id="2fde1-118">En aquest escenari, la capacitat proposada del recurs és inferior a les hores requerides que especifica el sol·licitant.</span><span class="sxs-lookup"><span data-stu-id="2fde1-118">In this scenario, the proposed resource capacity is less than the required hours that the requestor specified.</span></span> <span data-ttu-id="2fde1-119">Per tant, quan el sol·licitant accepta els recursos proposats, es crea un requisit de recurs no complert per capturar la resta de la demanda.</span><span class="sxs-lookup"><span data-stu-id="2fde1-119">Therefore, when the requestor accepts the proposed resources, an unfulfilled resource requirement is created to capture the remaining demand.</span></span>
- <span data-ttu-id="2fde1-120">Reservar diversos recursos per satisfer la demanda si no hi ha cap recurs disponible per completar el treball.</span><span class="sxs-lookup"><span data-stu-id="2fde1-120">Book multiple resources to satisfy the demand if no single resource is available to complete the work.</span></span>
- <span data-ttu-id="2fde1-121">Reservar menys recursos dels que calguin.</span><span class="sxs-lookup"><span data-stu-id="2fde1-121">Book fewer resources than are required.</span></span> <span data-ttu-id="2fde1-122">En aquest escenari, les hores reservades són menys que les hores requerides.</span><span class="sxs-lookup"><span data-stu-id="2fde1-122">In this scenario, the booked hours are fewer than the required hours.</span></span> <span data-ttu-id="2fde1-123">El sistema us guia per proposar recursos en comptes de reserves, de manera que el sol·licitant pugui comprovar i fer un seguiment de la demanda restant.</span><span class="sxs-lookup"><span data-stu-id="2fde1-123">The system guides you to propose resources instead of bookings, so that the requestor can verify and keep track of remaining demand.</span></span>

## <a name="billable-utilization"></a><span data-ttu-id="2fde1-124">Ús facturable</span><span class="sxs-lookup"><span data-stu-id="2fde1-124">Billable utilization</span></span>

<span data-ttu-id="2fde1-125">Els recursos poden tenir un objectiu d'ús facturable.</span><span class="sxs-lookup"><span data-stu-id="2fde1-125">Resources can have a target billable utilization.</span></span> <span data-ttu-id="2fde1-126">Aquest objectiu d'ús es defineix com un atribut de la funció per defecte d'un recurs o es defineix al registre del recurs individual que es pot reservar.</span><span class="sxs-lookup"><span data-stu-id="2fde1-126">This target utilization is either defined as an attribute on a resource's default role or set on the record of the individual bookable resource.</span></span> <span data-ttu-id="2fde1-127">Els càlculs d'ús es basen en les hores reals que els recursos han informat mitjançant les entrades de temps aprovades.</span><span class="sxs-lookup"><span data-stu-id="2fde1-127">Utilization calculations are based on the actual hours that resources have reported by using approved time entries.</span></span>

<span data-ttu-id="2fde1-128">Les següents fórmules s'utilitzen per calcular l'ús:</span><span class="sxs-lookup"><span data-stu-id="2fde1-128">The following formulas are used to calculate utilization:</span></span>

- <span data-ttu-id="2fde1-129">Ús facturable = Hores reals imputables ÷ Capacitat de recursos</span><span class="sxs-lookup"><span data-stu-id="2fde1-129">Billable utilization = Chargeable actual hours ÷ Resource capacity</span></span>
- <span data-ttu-id="2fde1-130">Ús no facturable = Temps real amb ID de tipus de facturació = No imputable, Gratuït o No disponible ÷ Capacitat de recursos</span><span class="sxs-lookup"><span data-stu-id="2fde1-130">Non-billable utilization = Actual time with billing type ID = Non-chargeable, Complementary, or Not available ÷ Resource capacity</span></span>
- <span data-ttu-id="2fde1-131">Intern = Temps real sense contracte de vendes ÷ Capacitat de recursos</span><span class="sxs-lookup"><span data-stu-id="2fde1-131">Internal = Actual time with no sales contract ÷ Resource capacity</span></span>
- <span data-ttu-id="2fde1-132">Capacitat de recursos = Hores de treball - Fora de l'oficina - Dies no hàbils</span><span class="sxs-lookup"><span data-stu-id="2fde1-132">Resource capacity = Resource work hours – Out-of-office – Non-working days</span></span>

<span data-ttu-id="2fde1-133">Podeu cercar la visualització **Ús de recursos** a la subfinestra **Recursos**.</span><span class="sxs-lookup"><span data-stu-id="2fde1-133">You can find the **Resource Utilization** view in the **Resources** pane.</span></span>

<span data-ttu-id="2fde1-134">Cada cel·la de la quadrícula representa el percentatge d'ús facturable del recurs en un període, com ara un dia, una setmana o un mes.</span><span class="sxs-lookup"><span data-stu-id="2fde1-134">Each cell in the grid represents the billable utilization percentage of the resource in a period, such as a day, week, or month.</span></span> <span data-ttu-id="2fde1-135">Les següents fórmules s'utilitzen per acolorir les cel·les:</span><span class="sxs-lookup"><span data-stu-id="2fde1-135">The following formulas are used to color the cells:</span></span>

- <span data-ttu-id="2fde1-136">**Verd:** Ús facturable \>= Objectiu d'ús de recursos</span><span class="sxs-lookup"><span data-stu-id="2fde1-136">**Green:** Billable utilization \>= Resource target utilization</span></span>
- <span data-ttu-id="2fde1-137">**Groc:** Objectiu d'ús - 20 \<= Ús facturable \< Objectiu d'ús</span><span class="sxs-lookup"><span data-stu-id="2fde1-137">**Yellow:** Target utilization – 20 \<= Billable utilization \< Target utilization</span></span>
- <span data-ttu-id="2fde1-138">**Vermell:** Ús facturable \< Objectiu d'ús - 20</span><span class="sxs-lookup"><span data-stu-id="2fde1-138">**Red:** Billable utilization \< Target utilization – 20</span></span>

<span data-ttu-id="2fde1-139">Com que la visualització **Ús de recursos** està basada en el tauler de planificació, podeu utilitzar les capacitats de filtratge del tauler de planificació per filtrar els resultats.</span><span class="sxs-lookup"><span data-stu-id="2fde1-139">Because the **Resource Utilization** view is based on the Schedule Board, you can use the filtering capabilities of the Schedule Board to filter your results.</span></span>

<span data-ttu-id="2fde1-140">La quadrícula requereix que definiu un objectiu d'ús en la funció o en el recurs individual.</span><span class="sxs-lookup"><span data-stu-id="2fde1-140">The grid requires that you set a target utilization on either the role or the individual resource.</span></span> <span data-ttu-id="2fde1-141">Per configurar-ho, aneu a **Recursos** \> **Funcions de recurs**.</span><span class="sxs-lookup"><span data-stu-id="2fde1-141">To do this setup, go to **Resources** \> **Resource roles**.</span></span>

<span data-ttu-id="2fde1-142">A més, cal assignar una funció per defecte a cadascun dels recursos que es pot reservar.</span><span class="sxs-lookup"><span data-stu-id="2fde1-142">Additionally, a default role must be assigned to each bookable resource.</span></span> <span data-ttu-id="2fde1-143">Aneu a **Recursos** \> **Recursos**.</span><span class="sxs-lookup"><span data-stu-id="2fde1-143">Go to **Resources** \> **Resources**.</span></span> <span data-ttu-id="2fde1-144">A la pestanya **Project Service** , comproveu que es defineix una funció de recurs i que el camp **Per defecte** està definit com a **Sí**.</span><span class="sxs-lookup"><span data-stu-id="2fde1-144">On the **Project Service** tab, verify that a resource role is defined, and that the **Is Default** field for it is set to **Yes**.</span></span> <span data-ttu-id="2fde1-145">Podeu afegir funcions addicionals on **Per defecte = No**.</span><span class="sxs-lookup"><span data-stu-id="2fde1-145">You can add additional roles where **Is Default = No**.</span></span> <span data-ttu-id="2fde1-146">La funció on **Per defecte = Sí** s'utilitza per avaluar l'ús del recurs en relació amb l'objectiu per a aquesta funció.</span><span class="sxs-lookup"><span data-stu-id="2fde1-146">The role where the **Is Default = Yes** is used to evaluate the resource's utilization against the target for that role.</span></span>

<span data-ttu-id="2fde1-147">A la pestanya **Project Service** també podeu definir un objectiu d'ús individual per al recurs.</span><span class="sxs-lookup"><span data-stu-id="2fde1-147">On the **Project Service** tab, you can also set an individual target utilization for the resource.</span></span> <span data-ttu-id="2fde1-148">A continuació, el càlcul d'ús utilitza l'objectiu d'ús per avaluar l'objectiu del recurs en comptes de l'objectiu de la funció per defecte del recurs.</span><span class="sxs-lookup"><span data-stu-id="2fde1-148">The utilization calculation then uses that target utilization to evaluate the resource's target instead of the target of the resource's default role.</span></span>

<span data-ttu-id="2fde1-149">L'ús es mostra per a un recurs només si aquest recurs té temps aprovat imputable durant el període que es mostra a la quadrícula.</span><span class="sxs-lookup"><span data-stu-id="2fde1-149">Utilization is shown for a resource only if that resource has approved, chargeable time during the period that is shown in the grid.</span></span>

## <a name="resource-availability"></a><span data-ttu-id="2fde1-150">Disponibilitat de recursos</span><span class="sxs-lookup"><span data-stu-id="2fde1-150">Resource availability</span></span>

<span data-ttu-id="2fde1-151">És important que els administradors de recursos puguin visualitzar la disponibilitat dels recursos i actualitzar les reserves.</span><span class="sxs-lookup"><span data-stu-id="2fde1-151">It's critical that resource managers be able to view the availability of resources and update bookings.</span></span> <span data-ttu-id="2fde1-152">En alguns casos, no hi ha cap demanda formal (sol·licitud de recurs), però un administrador de recursos ha de respondre a una demanda no planificada que entri per canals com ara el correu electrònic, una trucada telefònica o un missatge instantani.</span><span class="sxs-lookup"><span data-stu-id="2fde1-152">In some cases, there is no formal demand (resource request), but a resource manager must respond to an unplanned demand that comes through channels such as an email, phone call, or instant message.</span></span> <span data-ttu-id="2fde1-153">Els administradors de recursos utilitzen el tauler de planificació per actualitzar els recursos i les reserves.</span><span class="sxs-lookup"><span data-stu-id="2fde1-153">Resource managers use the Schedule Board to update resources and bookings.</span></span>

<span data-ttu-id="2fde1-154">Les hores de treball del recurs s'utilitzen com a base per calcular la disponibilitat d'un recurs.</span><span class="sxs-lookup"><span data-stu-id="2fde1-154">Resource work hours are used as the basis for calculating the availability of a resource.</span></span> <span data-ttu-id="2fde1-155">Les reserves de recursos consumeixen la capacitat dels recursos.</span><span class="sxs-lookup"><span data-stu-id="2fde1-155">Resource bookings consume the capacity of the resources.</span></span>

<span data-ttu-id="2fde1-156">El tauler de planificació utilitza colors i ombrejat per mostrar les reserves, la disponibilitat i l'excés de reserves, i també l'estat de les reserves.</span><span class="sxs-lookup"><span data-stu-id="2fde1-156">The Schedule Board uses colors and shading to show bookings, availability, and overbookings, and also the status of bookings.</span></span> <span data-ttu-id="2fde1-157">Un paràmetre de la configuració del tauler de planificació us permet mostrar una llegenda.</span><span class="sxs-lookup"><span data-stu-id="2fde1-157">A setting in the Schedule Board settings lets you show a legend.</span></span>

<span data-ttu-id="2fde1-158">Si una fletxa que apunta a la dreta apareix al costat d'un recurs individual que es pot reservar al tauler de planificació, el recurs es podrà expandir per mostrar els detalls del treball en què està reservat el recurs.</span><span class="sxs-lookup"><span data-stu-id="2fde1-158">If a right-pointing arrow appears next to an individual bookable resource on the Schedule Board, the resource can be expanded to show details of the work that the resource is booked on.</span></span>

<span data-ttu-id="2fde1-159">Com que el Dynamics 365 Project Operations utilitza el motor del Universal Resource Scheduling, si també teniu instal·lat el Dynamics 365 Field Service, podeu visualitzar els detalls de les reserves de recursos per a projectes, ordres de treball i altres entitats a les quals hàgiu ampliat la planificació.</span><span class="sxs-lookup"><span data-stu-id="2fde1-159">Because Dynamics 365 Project Operations uses the Universal Resource Scheduling engine, if you also have Dynamics 365 Field Service installed, you can view the details of resource bookings for projects, work orders, and any other entities that you've extended scheduling to.</span></span>

<span data-ttu-id="2fde1-160">Per visualitzar més detalls d'un recurs individual, feu-hi clic amb el botó dret per obrir la targeta de recursos.</span><span class="sxs-lookup"><span data-stu-id="2fde1-160">To view more details about an individual resource, right-click it to open the resource card.</span></span>

