---
title: Guia de l'administrador de recursos
description: Una guia per a l'administrador de recursos al Project Service
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 4a3f3fa7-ae1a-4139-974b-f61cc8a8bda7
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 67b400fe3e6bb60775ee144c1d3720a311204d7d
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749570"
---
# <a name="resource-manager-guide-project-service"></a><span data-ttu-id="146be-103">Guia de l'administrador de recursos (Project Service)</span><span class="sxs-lookup"><span data-stu-id="146be-103">Resource manager guide (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="146be-104">Les capacitats de l' [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] al [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] us ajuden a trobar els recursos correctes en el moment adequat per al projecte adient i garanteixen que tots els recursos s'utilitzin de manera eficient.</span><span class="sxs-lookup"><span data-stu-id="146be-104">The [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] help you find the right resources at the right time for the right project and make sure all resources are utilized efficiently.</span></span>  
  
 <span data-ttu-id="146be-105">Implementeu els consultors de l'empresa de forma eficaç i efectiva amb l'[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="146be-105">Deploy your company’s consultants efficiently and effectively with the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span> <span data-ttu-id="146be-106">Us proporcionen les eines que necessiteu per planificar recursos d'acord amb els requisits i les planificacions dels projectes de consultoria i amb les aptituds i la disponibilitat dels consultors.</span><span class="sxs-lookup"><span data-stu-id="146be-106">These provide you with the tools you need to schedule resources based on the requirements and schedules of consulting projects and on the skills and availability of your consultants.</span></span> <span data-ttu-id="146be-107">Podeu trobar ràpidament els consultors més qualificats que estan disponibles per treballar en els projectes, i podeu veure fàcilment com podeu millorar la seva planificació durant el transcurs de cada projecte.</span><span class="sxs-lookup"><span data-stu-id="146be-107">You can quickly find the most qualified consultants who are available to work on projects, and you can easily see how to better schedule them during the course of each project.</span></span>  
  
 <span data-ttu-id="146be-108">La planificació de recursos us ajuda a:</span><span class="sxs-lookup"><span data-stu-id="146be-108">Resource scheduling helps you do the following:</span></span>  
  
- <span data-ttu-id="146be-109">Assignar de manera adient els recursos als projectes en funció de com s'ajusten les seves aptituds i nivells de competència als requisits del recurs del projecte.</span><span class="sxs-lookup"><span data-stu-id="146be-109">Match resources to projects, based on how well their skills and proficiency levels match the project resource requirements.</span></span>  
  
- <span data-ttu-id="146be-110">Fer coincidir la planificació d'un recurs amb un calendari de projecte segons la seva disponibilitat i temps lliure planificat.</span><span class="sxs-lookup"><span data-stu-id="146be-110">Match a resource’s schedule to a project calendar, based on their availability and scheduled time off.</span></span> <span data-ttu-id="146be-111">El calendari codificat amb colors us proporciona informació visual sobre la disponibilitat dels recursos.</span><span class="sxs-lookup"><span data-stu-id="146be-111">The color-coded calendar gives you visual cues about resource availability.</span></span>  
  
- <span data-ttu-id="146be-112">Revisar la capacitat de cada consultor i determinar com s'utilitza actualment aquesta capacitat.</span><span class="sxs-lookup"><span data-stu-id="146be-112">Review the capacity of each consultant and determine how that capacity is currently used.</span></span> <span data-ttu-id="146be-113">Això us pot ajudar a trobar els consultors que estan infrautilitzats o massa ocupats o determinar si estan treballant a la capacitat òptima.</span><span class="sxs-lookup"><span data-stu-id="146be-113">This can help you find where a consultant might be under- or over-utilized, or if they’re working at capacity.</span></span>  
  
- <span data-ttu-id="146be-114">Assigneu a un projecte un percentatge o un número determinat d'hores per a la capacitat del treballador.</span><span class="sxs-lookup"><span data-stu-id="146be-114">Assign a percentage or a specific number of hours for a worker’s capacity to a project.</span></span>  
  
- <span data-ttu-id="146be-115">Feu reserves de recursos de grups.</span><span class="sxs-lookup"><span data-stu-id="146be-115">Make group resource bookings.</span></span>  
  
- <span data-ttu-id="146be-116">Feu reserves flexibles o fixes de recursos i convertir les hores de reserva flexibles en hores de reserva fixes en un sol pas.</span><span class="sxs-lookup"><span data-stu-id="146be-116">Soft book or hard book resources, and convert soft-booked hours into hard-booked hours in one step.</span></span>  
  
- <span data-ttu-id="146be-117">Creeu automàticament un equip de projecte basat en recursos definits en una estructura del desglossament del treball per a un projecte.</span><span class="sxs-lookup"><span data-stu-id="146be-117">Automatically form a project team based on resources defined in a work breakdown structure for a project.</span></span>  
  
- <span data-ttu-id="146be-118">Compliu les sol·licituds dels recursos (reservar, proposar, trobar recursos de substitució).</span><span class="sxs-lookup"><span data-stu-id="146be-118">Fulfill resource requests (book, propose, find substitute resources).</span></span>  
  
- <span data-ttu-id="146be-119">Assigneu recursos segons un model central (assignacions d'administrador de recursos) o híbrid (tant l'administrador de recursos com altres administradors poden assignar).</span><span class="sxs-lookup"><span data-stu-id="146be-119">Assign resources according to a central (resource manager assigns) or hybrid model (resource manager and other managers can assign).</span></span> <span data-ttu-id="146be-120">Per obtenir més informació sobre la configuració d'un model d'administració central de recursos contra un model híbrid, consulteu [Configurar paràmetres addicionals (Project Service)](../project-service/configure-additional-parameters-settings.md).</span><span class="sxs-lookup"><span data-stu-id="146be-120">For more information about setting a central versus hybrid resource management model, see [Configure additional parameters settings (Project Service)](../project-service/configure-additional-parameters-settings.md).</span></span>  
  
  <span data-ttu-id="146be-121">Podeu administrar els recursos amb eficàcia entre projectes i assegurar-vos que els projectes tinguin el personal adient.</span><span class="sxs-lookup"><span data-stu-id="146be-121">You can manage resources efficiently across projects and ensure that projects are staffed appropriately.</span></span> <span data-ttu-id="146be-122">Heu de realitzar les tasques següents:</span><span class="sxs-lookup"><span data-stu-id="146be-122">You’ll need to perform the following tasks:</span></span>  
  
- <span data-ttu-id="146be-123">[Administrar sol·licituds de recursos](../project-service/manage-resource-requests.md).</span><span class="sxs-lookup"><span data-stu-id="146be-123">[Manage resource requests](../project-service/manage-resource-requests.md).</span></span> <span data-ttu-id="146be-124">Fer coincidir les aptituds i les competències dels vostres consultors amb els projectes adients.</span><span class="sxs-lookup"><span data-stu-id="146be-124">Match the skills and proficiencies of your consultants to the right projects.</span></span>  
  
- <span data-ttu-id="146be-125">[Visualització de la disponibilitat de recursos](../project-service/view-resource-availability.md).</span><span class="sxs-lookup"><span data-stu-id="146be-125">[View resource availability](../project-service/view-resource-availability.md).</span></span> <span data-ttu-id="146be-126">Consultar la disponibilitat dels consultors en una visualització de calendari.</span><span class="sxs-lookup"><span data-stu-id="146be-126">Check consultants’ availability in a calendar view.</span></span>  
  
- <span data-ttu-id="146be-127">[Visualització de l'ús de recursos](../project-service/view-resource-utilization.md).</span><span class="sxs-lookup"><span data-stu-id="146be-127">[View resource utilization](../project-service/view-resource-utilization.md).</span></span> <span data-ttu-id="146be-128">Veure el percentatge de temps reservat actual dels vostres consultors.</span><span class="sxs-lookup"><span data-stu-id="146be-128">See the percentage of time that your consultants are currently booked.</span></span>  
  
- <span data-ttu-id="146be-129">[Planificar recursos per a un projecte](../project-service/schedule-resources-project.md).</span><span class="sxs-lookup"><span data-stu-id="146be-129">[Schedule resources for a project](../project-service/schedule-resources-project.md).</span></span> <span data-ttu-id="146be-130">Planifiqueu consultors per a un projecte.</span><span class="sxs-lookup"><span data-stu-id="146be-130">Schedule consultants for a project.</span></span>  
  
  <span data-ttu-id="146be-131">Per obtenir més informació sobre com enviar sol·licituds de recursos per a projectes individuals, consulteu [Envia la sol·licitud de recurs](../project-service/submit-resource-requests.md).</span><span class="sxs-lookup"><span data-stu-id="146be-131">For more information about submitting resource requests for individual projects, see [Submit resource requests](../project-service/submit-resource-requests.md).</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="146be-132">Vegeu també</span><span class="sxs-lookup"><span data-stu-id="146be-132">See Also</span></span>  
 <span data-ttu-id="146be-133">[Informació general del Project Service](../project-service/overview.md) </span><span class="sxs-lookup"><span data-stu-id="146be-133">[Overview of Project Service](../project-service/overview.md) </span></span>  
 <span data-ttu-id="146be-134">[Guia de l'administrador](../project-service/admin-guide.md) </span><span class="sxs-lookup"><span data-stu-id="146be-134">[Administrator Guide](../project-service/admin-guide.md) </span></span>  
 <span data-ttu-id="146be-135">[Guia de l'administrador de comptes](../project-service/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="146be-135">[Account Manager Guiden](../project-service/account-manager-guide.md) </span></span>  
 <span data-ttu-id="146be-136">[Guia d'administrador de projectes](../project-service/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="146be-136">[Project Manager Guide](../project-service/project-manager-guide.md) </span></span>  
 [<span data-ttu-id="146be-137">Guia de temps, despeses i col·laboració</span><span class="sxs-lookup"><span data-stu-id="146be-137">Time, Expense, and Collaboration Guide</span></span>](../project-service/time-expense-collaboration-guide.md)
