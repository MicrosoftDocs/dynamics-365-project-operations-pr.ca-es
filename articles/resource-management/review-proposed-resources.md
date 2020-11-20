---
title: Revisió dels recursos proposats
description: En aquest tema es proporciona informació sobre la manera de proposar recursos de projecte.
author: ruhercul
manager: AnnBe
ms.date: 11/05/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: 54a0924da17eac86e2fa400540e629f6d803aa35
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401161"
---
# <a name="review-proposed-resources"></a><span data-ttu-id="0ba23-103">Revisió dels recursos proposats</span><span class="sxs-lookup"><span data-stu-id="0ba23-103">Review proposed resources</span></span>

<span data-ttu-id="0ba23-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_</span><span class="sxs-lookup"><span data-stu-id="0ba23-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="0ba23-105">Els administradors de recursos poden proposar un recurs a l'administrador del projecte mitjançant una sol·licitud de recursos.</span><span class="sxs-lookup"><span data-stu-id="0ba23-105">Resource managers can propose a resource to the project manager by using a resource request.</span></span>

1. <span data-ttu-id="0ba23-106">A la graella de sol·licitud o a la sol·licitud en si mateixa, seleccioneu **Cerca recursos**.</span><span class="sxs-lookup"><span data-stu-id="0ba23-106">From the request grid or the request itself, select **Find Resources**.</span></span>
2. <span data-ttu-id="0ba23-107">A la pàgina **Auxiliar de planificació,** seleccioneu el recurs i, a continuació, a la subfinestra **Crea una reserva de recursos**, al camp **Estat de la reserva**, seleccioneu **Reserva**.</span><span class="sxs-lookup"><span data-stu-id="0ba23-107">On the **Schedule Assistant** page, select the resource, and then, in the **Create Resource Booking** pane, in the **Booking Status** field, select **Book**.</span></span>

<span data-ttu-id="0ba23-108">Es produeixen les següents actualitzacions d'estat:</span><span class="sxs-lookup"><span data-stu-id="0ba23-108">The following status updates occur:</span></span>

- <span data-ttu-id="0ba23-109">A la pàgina **Auxiliar de planificació**, els indicadors d'estat s'actualitzen per indicar que es proposa la reserva, no que es reserva de manera fixa.</span><span class="sxs-lookup"><span data-stu-id="0ba23-109">On the **Schedule Assistant** page, the status indicators are updated to indicate that the booking is proposed, not hard-booked.</span></span>
- <span data-ttu-id="0ba23-110">A la sol·licitud de recursos, l'estat canvia a **Necessita revisió**.</span><span class="sxs-lookup"><span data-stu-id="0ba23-110">On the resource request, the status is changed to **Needs Review**.</span></span>
- <span data-ttu-id="0ba23-111">A la pestanya **Equip** del projecte, el valor **Estat de la sol·licitud** de l'equip genèric es canvia a **Necessita revisió**.</span><span class="sxs-lookup"><span data-stu-id="0ba23-111">On the **Team** tab of the project, the generic team member's **Request Status** value is changed to **Needs Review**.</span></span>

<span data-ttu-id="0ba23-112">L'administrador de projectes pot acceptar o rebutjar la proposta.</span><span class="sxs-lookup"><span data-stu-id="0ba23-112">The project manager can either accept or reject the proposal.</span></span>

<span data-ttu-id="0ba23-113">Quan els administradors de recursos processen les sol·licituds de recursos, poden utilitzar qualsevol dels enfocaments següents:</span><span class="sxs-lookup"><span data-stu-id="0ba23-113">When resource managers process resource requests, they can use any of the following approaches:</span></span>

- <span data-ttu-id="0ba23-114">Proposar diversos recursos per satisfer la demanda si no hi ha cap recurs disponible per complir les hores requerides.</span><span class="sxs-lookup"><span data-stu-id="0ba23-114">Propose multiple resources to satisfy the demand if no single resource is available to fulfill the required hours.</span></span> <span data-ttu-id="0ba23-115">Les hores proposades es divideixen a continuació entre diversos recursos que poden satisfer les hores requerides.</span><span class="sxs-lookup"><span data-stu-id="0ba23-115">Proposed hours are then split among multiple resources that can satisfy the required hours.</span></span> <span data-ttu-id="0ba23-116">En aquest escenari, les hores no es poden superposar.</span><span class="sxs-lookup"><span data-stu-id="0ba23-116">In this scenario, the hours can't overlap.</span></span>
- <span data-ttu-id="0ba23-117">Proposar menys recursos dels que calguin.</span><span class="sxs-lookup"><span data-stu-id="0ba23-117">Propose fewer resources than are required.</span></span> <span data-ttu-id="0ba23-118">En aquest escenari, la capacitat proposada del recurs és inferior a les hores requerides que especifica el sol·licitant.</span><span class="sxs-lookup"><span data-stu-id="0ba23-118">In this scenario, the proposed resource capacity is less than the required hours that the requestor specified.</span></span> <span data-ttu-id="0ba23-119">Per tant, quan el sol·licitant accepta els recursos proposats, es crea un requisit de recurs no complert per capturar la resta de la demanda.</span><span class="sxs-lookup"><span data-stu-id="0ba23-119">Therefore, when the requestor accepts the proposed resources, an unfulfilled resource requirement is created to capture the remaining demand.</span></span>
- <span data-ttu-id="0ba23-120">Reservar diversos recursos per satisfer la demanda si no hi ha cap recurs disponible per completar el treball.</span><span class="sxs-lookup"><span data-stu-id="0ba23-120">Book multiple resources to satisfy the demand if no single resource is available to complete the work.</span></span>
- <span data-ttu-id="0ba23-121">Reservar menys recursos dels que calguin.</span><span class="sxs-lookup"><span data-stu-id="0ba23-121">Book fewer resources than are required.</span></span> <span data-ttu-id="0ba23-122">En aquest escenari, les hores reservades són menys que les hores requerides.</span><span class="sxs-lookup"><span data-stu-id="0ba23-122">In this scenario, the booked hours are fewer than the required hours.</span></span> <span data-ttu-id="0ba23-123">El sistema us guia per proposar recursos en comptes de reserves, de manera que el sol·licitant pugui comprovar i fer un seguiment de la demanda restant.</span><span class="sxs-lookup"><span data-stu-id="0ba23-123">The system guides you to propose resources instead of bookings, so that the requestor can verify and keep track of remaining demand.</span></span>

## <a name="resource-availability"></a><span data-ttu-id="0ba23-124">Disponibilitat de recursos</span><span class="sxs-lookup"><span data-stu-id="0ba23-124">Resource availability</span></span>

<span data-ttu-id="0ba23-125">És important que els administradors de recursos puguin visualitzar la disponibilitat dels recursos i actualitzar les reserves.</span><span class="sxs-lookup"><span data-stu-id="0ba23-125">It's critical that resource managers be able to view the availability of resources and update bookings.</span></span> <span data-ttu-id="0ba23-126">En alguns casos, no hi ha cap demanda formal (sol·licitud de recurs), però un administrador de recursos ha de respondre a una demanda no planificada que entri per canals com ara el correu electrònic, una trucada telefònica o un missatge instantani.</span><span class="sxs-lookup"><span data-stu-id="0ba23-126">In some cases, there is no formal demand (resource request), but a resource manager must respond to an unplanned demand that comes through channels such as an email, phone call, or instant message.</span></span> <span data-ttu-id="0ba23-127">Els administradors de recursos utilitzen el tauler de planificació per actualitzar els recursos i les reserves.</span><span class="sxs-lookup"><span data-stu-id="0ba23-127">Resource managers use the Schedule Board to update resources and bookings.</span></span>

<span data-ttu-id="0ba23-128">Les hores de treball del recurs s'utilitzen com a base per calcular la disponibilitat d'un recurs.</span><span class="sxs-lookup"><span data-stu-id="0ba23-128">Resource work hours are used as the basis for calculating the availability of a resource.</span></span> <span data-ttu-id="0ba23-129">Les reserves de recursos consumeixen la capacitat dels recursos.</span><span class="sxs-lookup"><span data-stu-id="0ba23-129">Resource bookings consume the capacity of the resources.</span></span>

<span data-ttu-id="0ba23-130">El tauler de planificació utilitza colors i ombrejat per mostrar les reserves, la disponibilitat i l'excés de reserves, i també l'estat de les reserves.</span><span class="sxs-lookup"><span data-stu-id="0ba23-130">The Schedule Board uses colors and shading to show bookings, availability, and overbookings, and also the status of bookings.</span></span> <span data-ttu-id="0ba23-131">Un paràmetre de la configuració del tauler de planificació us permet mostrar una llegenda.</span><span class="sxs-lookup"><span data-stu-id="0ba23-131">A setting in the Schedule Board settings lets you show a legend.</span></span>

<span data-ttu-id="0ba23-132">Si una fletxa que apunta a la dreta apareix al costat d'un recurs individual que es pot reservar al tauler de planificació, el recurs es podrà expandir per mostrar els detalls del treball en què està reservat el recurs.</span><span class="sxs-lookup"><span data-stu-id="0ba23-132">If a right-pointing arrow appears next to an individual bookable resource on the Schedule Board, the resource can be expanded to show details of the work that the resource is booked on.</span></span>

<span data-ttu-id="0ba23-133">Com que el Dynamics 365 Project Operations utilitza el motor del Universal Resource Scheduling, si també teniu instal·lat el Dynamics 365 Field Service, podeu visualitzar els detalls de les reserves de recursos per a projectes, ordres de treball i altres entitats a les quals hàgiu ampliat la planificació.</span><span class="sxs-lookup"><span data-stu-id="0ba23-133">Because Dynamics 365 Project Operations uses the Universal Resource Scheduling engine, if you also have Dynamics 365 Field Service installed, you can view the details of resource bookings for projects, work orders, and any other entities that you've extended scheduling to.</span></span>

<span data-ttu-id="0ba23-134">Per visualitzar més detalls d'un recurs individual, feu-hi clic amb el botó dret per obrir la targeta de recursos.</span><span class="sxs-lookup"><span data-stu-id="0ba23-134">To view more details about an individual resource, right-click it to open the resource card.</span></span>

