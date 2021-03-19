---
title: Planificar recursos per a un projecte
description: Com planificar recursos per a un projecte al Project Service
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: f0a234f96419bac58cd932a082010da672e7dcb5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5282636"
---
# <a name="schedule-resources-for-a-project-project-service"></a><span data-ttu-id="07f2d-103">Planificar recursos per a un projecte (Project Service)</span><span class="sxs-lookup"><span data-stu-id="07f2d-103">Schedule resources for a project (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="07f2d-104">Podeu comprovar la disponibilitat de recursos per obtenir una vista general de com estan reservats els vostres recursos, o podeu filtrar la visualització per habilitats, equip, ubicació i altres opcions.</span><span class="sxs-lookup"><span data-stu-id="07f2d-104">You can check resource availability to get an overall view of how booked your resources are, or you can filter the view by skills, team, location, and other options.</span></span>  
  
<span data-ttu-id="07f2d-105">El tauler de planificació mostra una llista de recursos i la seva disponibilitat.</span><span class="sxs-lookup"><span data-stu-id="07f2d-105">The schedule board shows list of resources and their availability.</span></span> <span data-ttu-id="07f2d-106">Seleccioneu un mode de visualització per mostrar la disponibilitat per **hores**, **dia**, **setmana** o **mes**.</span><span class="sxs-lookup"><span data-stu-id="07f2d-106">Select a view mode to show availability by **Hours**, **Day**, **Week**, or **Month**.</span></span>  
  
<span data-ttu-id="07f2d-107">Abans d'utilitzar el tauler de planificació, és important configurar-lo.</span><span class="sxs-lookup"><span data-stu-id="07f2d-107">Before you use the schedule board, it’s important to set it up.</span></span> <span data-ttu-id="07f2d-108">Per obtenir-ne més informació, consulta [Configura el tauler la planificació (Field Service o Project Service Automation)](https://docs.microsoft.com/dynamics365/field-service/configure-schedule-board).</span><span class="sxs-lookup"><span data-stu-id="07f2d-108">For more information, see [Configure the schedule board (Field Service or Project Service Automation)](https://docs.microsoft.com/dynamics365/field-service/configure-schedule-board).</span></span>
  
<span data-ttu-id="07f2d-109">Si utilitzeu una versió anterior, per veure la disponibilitat dels recursos, consulteu [Visualització de la disponibilitat de recursos](../psa/view-resource-availability.md).</span><span class="sxs-lookup"><span data-stu-id="07f2d-109">If you are using an older version, for resource availability, see [View resource availability](../psa/view-resource-availability.md).</span></span>  

> [!IMPORTANT]
>  <span data-ttu-id="07f2d-110">Per utilitzar la funcionalitat de reserva de tauler de planificació, la geocodificació i els serveis d'ubicació, cal activar els mapes.</span><span class="sxs-lookup"><span data-stu-id="07f2d-110">To use the schedule board booking functionality, geocoding, and location services, you need to turn on maps.</span></span>  
> 
> 1. <span data-ttu-id="07f2d-111">Des del menú principal, seleccioneu **Planificació de recursos** > **Administració**.</span><span class="sxs-lookup"><span data-stu-id="07f2d-111">On the main menu, select **Resource Scheduling** > **Administration**.</span></span>  
> 2. <span data-ttu-id="07f2d-112">Feu clic a **Paràmetres de planificació**.</span><span class="sxs-lookup"><span data-stu-id="07f2d-112">Click **Scheduling parameters**.</span></span>  
> 3. <span data-ttu-id="07f2d-113">Obriu un registre i desplaceu-vos fins a la secció **Resource Scheduling Optimization**.</span><span class="sxs-lookup"><span data-stu-id="07f2d-113">Open record and scroll down to the **Resource Scheduling Optimization** section.</span></span>  
> 4. <span data-ttu-id="07f2d-114">Al camp **Connecta't als mapes**, seleccioneu **Sí**.</span><span class="sxs-lookup"><span data-stu-id="07f2d-114">On the **Connect to Maps** field, choose **Yes**.</span></span>  
> 5. <span data-ttu-id="07f2d-115">Accepteu les condicions i guardeu el registre.</span><span class="sxs-lookup"><span data-stu-id="07f2d-115">Accept terms and save the record.</span></span>  
> 6. <span data-ttu-id="07f2d-116">Des del menú principal, seleccioneu **Project Service** > **Tauler de planificació**.</span><span class="sxs-lookup"><span data-stu-id="07f2d-116">On the main menu, select **Project Service** > **Schedule board**.</span></span> <span data-ttu-id="07f2d-117">A partir d'aquí, hi ha diverses maneres de planificar manualment un requisit de reserva.</span><span class="sxs-lookup"><span data-stu-id="07f2d-117">From here, there are several ways to manually schedule a booking requirement.</span></span> <span data-ttu-id="07f2d-118">Escolliu el mètode que més us convingui.</span><span class="sxs-lookup"><span data-stu-id="07f2d-118">Choose the method that works for you.</span></span>
  
## <a name="find-available-resources"></a><span data-ttu-id="07f2d-119">Cerca recursos disponibles</span><span class="sxs-lookup"><span data-stu-id="07f2d-119">Find available resources</span></span>

1.  <span data-ttu-id="07f2d-120">Des de la llista **Requisits de la reserva**, feu clic amb el botó dret a una reserva sense planificar i trieu-ne una de les següents:</span><span class="sxs-lookup"><span data-stu-id="07f2d-120">From the **Booking Requirement** list, right-click an unscheduled booking and choose one of the following:</span></span>  
  
- <span data-ttu-id="07f2d-121">Trieu **Cerca la disponibilitat: recursos actuals** per cercar un recurs disponible de la llista del tauler de planificació.</span><span class="sxs-lookup"><span data-stu-id="07f2d-121">Choose **Find availability - Current Resources** to find an available resource from the list on the schedule board.</span></span>  
- <span data-ttu-id="07f2d-122">Trieu **Cerca la disponibilitat: tots els recursos** per cercar un recurs disponible dels recursos del sistema</span><span class="sxs-lookup"><span data-stu-id="07f2d-122">Choose **Find availability - All Resources**, to find an available resource from resources in the system</span></span>  
   > [!NOTE]
   >  <span data-ttu-id="07f2d-123">Després, els filtres mostraran les opcions del requisit de la reserva seleccionat.</span><span class="sxs-lookup"><span data-stu-id="07f2d-123">When you do this, the filters will show options for the selected booking requirement.</span></span>  
  
2. <span data-ttu-id="07f2d-124">Quan vegeu una franja de temps disponible, feu clic-hi amb el botó dret al tauler de planificació i trieu **Reserva aquí**.</span><span class="sxs-lookup"><span data-stu-id="07f2d-124">When you see an available slot, right-click the time slot on the schedule board and choose **Book Here**.</span></span> <span data-ttu-id="07f2d-125">O bé, arrastreu i deixeu anar el requisit de la reserva a la franja de temps disponible.</span><span class="sxs-lookup"><span data-stu-id="07f2d-125">Or, drag and drop the booking requirement to the available time slot.</span></span>  
  

## <a name="book-a-resource-using-the-daily-view-and-find-whos-under-booked"></a><span data-ttu-id="07f2d-126">Reservar un recurs amb la visualització diària i veure qui ha realitzat reserves</span><span class="sxs-lookup"><span data-stu-id="07f2d-126">Book a resource using the daily view and find who’s under-booked</span></span>
  
1.  <span data-ttu-id="07f2d-127">Al tauler de planificació, seleccioneu **Mode de visualització** i seleccioneu **Dies**.</span><span class="sxs-lookup"><span data-stu-id="07f2d-127">On the schedule board, select **View Mode** and select **Days**.</span></span>  
  
    <span data-ttu-id="07f2d-128">Es mostrarà una vista de quadrícula amb el nombre d'hores de reserva d'un recurs per dia i els dies que està lliure.</span><span class="sxs-lookup"><span data-stu-id="07f2d-128">This shows a grid view of how many hours a resource is booked per day and which days they are free.</span></span>  
  
2.  <span data-ttu-id="07f2d-129">Feu clic al nom del recurs que voleu reservar i, a continuació, seleccioneu **Reserva**.</span><span class="sxs-lookup"><span data-stu-id="07f2d-129">Click the name of the resource you want to book, and then select **Book**.</span></span>  
  
3.  <span data-ttu-id="07f2d-130">Al quadre de diàleg **Reserves de recursos (crear)**, trieu el projecte del qual voleu reservar el recurs juntament amb el mètode de reserva i les hores d'inici i finalització.</span><span class="sxs-lookup"><span data-stu-id="07f2d-130">On the **Resource booking (create)** dialog box, choose the project that you want to book the resource for along with booking method and start and end times.</span></span>  
  
4.  <span data-ttu-id="07f2d-131">Quan hàgiu acabat, seleccioneu **Reserva**.</span><span class="sxs-lookup"><span data-stu-id="07f2d-131">When you’re done, select **Book**.</span></span>  
  
## <a name="view-to-the-schedule-board"></a><span data-ttu-id="07f2d-132">Visualitza-ho al tauler la planificació</span><span class="sxs-lookup"><span data-stu-id="07f2d-132">View to the schedule board</span></span>
  
1.  <span data-ttu-id="07f2d-133">Seleccioneu un requisit de reserva sense planificar a la part inferior de la llista.</span><span class="sxs-lookup"><span data-stu-id="07f2d-133">Select an unscheduled booking requirement from the list at the bottom.</span></span>  
  
2.  <span data-ttu-id="07f2d-134">Arrossegueu el requisit de reserves a una franja de recurs/temps disponible al tauler de planificació.</span><span class="sxs-lookup"><span data-stu-id="07f2d-134">Drag the booking requirement to an available resource/time slot on the schedule board.</span></span>  
  
3.  <span data-ttu-id="07f2d-135">Quan hàgiu acabat, seleccioneu **Reserva**.</span><span class="sxs-lookup"><span data-stu-id="07f2d-135">When you're done, select **Book**.</span></span>  
  
### <a name="additional-resources"></a><span data-ttu-id="07f2d-136">Recursos addicionals</span><span class="sxs-lookup"><span data-stu-id="07f2d-136">Additional resources</span></span>  
 [<span data-ttu-id="07f2d-137">Guia de l'administrador de recursos</span><span class="sxs-lookup"><span data-stu-id="07f2d-137">Resource manager guide</span></span>](../psa/resource-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]