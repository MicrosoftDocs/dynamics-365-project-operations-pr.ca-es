---
title: PMF de l'administració de recursos
description: Aquest tema proporciona respostes a les preguntes més freqüents sobre l'administració de recursos.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 395aa57d73e5d4a0c9c827c79bf4e7ef229c3981
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072423"
---
# <a name="resource-management-faq"></a><span data-ttu-id="933e6-103">PMF de l'administració de recursos</span><span class="sxs-lookup"><span data-stu-id="933e6-103">Resource management FAQ</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

## <a name="what-is-the-difference-between-a-team-member-and-a-resource-requirement"></a><span data-ttu-id="933e6-104">Quina diferència hi ha entre un membre de l'equip i un requisit de recursos?</span><span class="sxs-lookup"><span data-stu-id="933e6-104">What is the difference between a team member and a resource requirement?</span></span>

<span data-ttu-id="933e6-105">Un membre de l'equip del projecte es pot assignar a tasques, reservar o tenir un excés de reserva, i definir-lo com a aprovador.</span><span class="sxs-lookup"><span data-stu-id="933e6-105">A project team member can be assigned to tasks, booked or overbooked, and set as an approver.</span></span> <span data-ttu-id="933e6-106">Un requisit de recurs pot existir sense membres de l'equip d'un projecte, com un esborrany de la demanda.</span><span class="sxs-lookup"><span data-stu-id="933e6-106">A resource requirement can exist without a project team member, as a draft note of demand.</span></span> 

## <a name="what-is-the-difference-between-proposed-and-soft-booked-hours"></a><span data-ttu-id="933e6-107">Quina diferència hi ha entre les hores proposades i les reservades de manera flexible?</span><span class="sxs-lookup"><span data-stu-id="933e6-107">What is the difference between proposed and soft-booked hours?</span></span>

<span data-ttu-id="933e6-108">Les hores proposades i les hores reservades de manera flexible tenen una visibilitat diferent.</span><span class="sxs-lookup"><span data-stu-id="933e6-108">Proposed hours and soft-booked hours differ in visibility.</span></span> <span data-ttu-id="933e6-109">Les hores proposades només són visibles pels administradors de recursos i per l'administrador de projectes que han iniciat la demanda mitjançant una sol·licitud de recurs.</span><span class="sxs-lookup"><span data-stu-id="933e6-109">Proposed hours are visible only to resource managers and the project manager who initiated the demand by using a resource request.</span></span> <span data-ttu-id="933e6-110">Les hores reservades de manera flexible són visibles per qualsevol persona que tingui accés al Tauler de planificació.</span><span class="sxs-lookup"><span data-stu-id="933e6-110">Soft-booked hours are visible to anyone who has access to the Schedule Board.</span></span>

## <a name="how-can-i-see-the-soft-booked-hours-for-resources-on-a-team"></a><span data-ttu-id="933e6-111">Com puc veure les hores reservades de manera flexible per als recursos d'un equip?</span><span class="sxs-lookup"><span data-stu-id="933e6-111">How can I see the soft-booked hours for resources on a team?</span></span>

<span data-ttu-id="933e6-112">Les reserves flexibles es poden fer quan reserveu un requisit de recurs.</span><span class="sxs-lookup"><span data-stu-id="933e6-112">Soft bookings can made when you book a resource requirement.</span></span> <span data-ttu-id="933e6-113">Els recursos que s'han reservat de manera flexible en un equip del projecte apareixen com a membres de l'equip que tenen hores reservades de manera flexible.</span><span class="sxs-lookup"><span data-stu-id="933e6-113">Resources that are soft-booked on a project team appear as team members who have soft-booked hours.</span></span> <span data-ttu-id="933e6-114">També apareixen al Tauler de planificació.</span><span class="sxs-lookup"><span data-stu-id="933e6-114">They also appear on the Schedule Board.</span></span>

## <a name="how-do-i-change-the-required-hours-and-the-start-and-end-dates-for-a-resource-generic-or-named-that-i-booked"></a><span data-ttu-id="933e6-115">Com puc canviar les hores requerides i les dates d'inici i d'acabament per a un recurs (genèric o amb nom) que he reservat?</span><span class="sxs-lookup"><span data-stu-id="933e6-115">How do I change the required hours, and the start and end dates, for a resource (generic or named) that I booked?</span></span>

<span data-ttu-id="933e6-116">Després de reservar els recursos, seleccioneu **Mantén les reserves** per fer els canvis necessaris.</span><span class="sxs-lookup"><span data-stu-id="933e6-116">After resources are booked, select **Maintain Bookings** to make any changes that are required.</span></span>

## <a name="what-resources-types-does-project-service-automation-support"></a><span data-ttu-id="933e6-117">Quins tipus de recursos admet el Project Service Automation?</span><span class="sxs-lookup"><span data-stu-id="933e6-117">What resources types does Project Service Automation support?</span></span>

<span data-ttu-id="933e6-118">**Usuari** i **Contacte** són els únics tipus de recurs admesos al Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="933e6-118">**User** and **Contact** are the only resource types that are supported in Dynamics 365 Project Service Automation.</span></span> <span data-ttu-id="933e6-119">Tot i que podeu crear altres tipus de recursos (per exemple, **Equipament** i **Grup** ), no s'admet cap cas d'ús d'extrem a extrem.</span><span class="sxs-lookup"><span data-stu-id="933e6-119">Although you can create other types of resources (for example, **Equipment** and **Group** ), no end-to-end use case is supported for them.</span></span>

## <a name="what-is-the-difference-between-an-assignment-and-a-booking"></a><span data-ttu-id="933e6-120">Quina diferència hi ha entre una assignació i una reserva?</span><span class="sxs-lookup"><span data-stu-id="933e6-120">What is the difference between an assignment and a booking?</span></span>

<span data-ttu-id="933e6-121">Les assignacions són l'assignació de recursos a tasques de projecte a la planificació del projecte.</span><span class="sxs-lookup"><span data-stu-id="933e6-121">Assignments are the assignment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="933e6-122">Els recursos poden ser recursos reals o genèrics.</span><span class="sxs-lookup"><span data-stu-id="933e6-122">The resources can be either real or generic resources.</span></span> <span data-ttu-id="933e6-123">Les reserves són l'assignació fixa o flexible de recursos a un projecte.</span><span class="sxs-lookup"><span data-stu-id="933e6-123">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="933e6-124">Les reserves fixes consumeixen la capacitat d'un recurs.</span><span class="sxs-lookup"><span data-stu-id="933e6-124">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="933e6-125">Idealment, per als recursos reals, les reserves i les assignacions haurien de concordar, perquè no es diferencien.</span><span class="sxs-lookup"><span data-stu-id="933e6-125">Ideally, for real resources, the bookings and assignments should agree, because they don't differ.</span></span> <span data-ttu-id="933e6-126">No obstant, el PSA no obliga a aplicar aquesta concordança.</span><span class="sxs-lookup"><span data-stu-id="933e6-126">However, PSA doesn't enforce this agreement.</span></span> <span data-ttu-id="933e6-127">La visualització Conciliació mostra llocs a l'administrador del projecte on les reserves i les assignacions d'un recurs no coincideixen.</span><span class="sxs-lookup"><span data-stu-id="933e6-127">The Reconciliation view shows a project manager places where a resource's bookings and assignments don't agree.</span></span>
