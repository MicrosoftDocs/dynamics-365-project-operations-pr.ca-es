---
title: Reservar requisits manera flexible
description: En aquest tema es proporciona informació sobre com reservar requisits de manera flexible.
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
ms.openlocfilehash: 736d59976ad0f456a694cedbb28b516c90632fe6
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5282906"
---
# <a name="soft-book-requirements"></a><span data-ttu-id="627f6-103">Reservar requisits manera flexible</span><span class="sxs-lookup"><span data-stu-id="627f6-103">Soft-book requirements</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="627f6-104">Un requisit de recursos es pot reservar de manera fixa.</span><span class="sxs-lookup"><span data-stu-id="627f6-104">A resource requirement can be hard-booked.</span></span> <span data-ttu-id="627f6-105">Una reserva fixa crea una proposta que consumeix la capacitat d'un recurs.</span><span class="sxs-lookup"><span data-stu-id="627f6-105">A hard booking creates a proposal that consumes a resource's capacity.</span></span> <span data-ttu-id="627f6-106">La proposta s'envia novament al sol·licitant per a la seva aprovació.</span><span class="sxs-lookup"><span data-stu-id="627f6-106">The proposal is then sent back to the requester for approval.</span></span> <span data-ttu-id="627f6-107">Una reserva flexible afegeix provisionalment un recurs a un equip del projecte i té un estat diferent al Tauler de planificació, però no consumeix la capacitat del recurs.</span><span class="sxs-lookup"><span data-stu-id="627f6-107">A soft booking tentatively adds a resource to a project team and has a different status on the Schedule Board, but it doesn't consume the resource's capacity.</span></span> <span data-ttu-id="627f6-108">Per reservar un recurs de manera flexible al Tauler de planificació, definiu el camp **Estat de la reserva** a **Flexible**.</span><span class="sxs-lookup"><span data-stu-id="627f6-108">To soft-book a resource from the Schedule Board, set the **Booking Status** field to **Soft**.</span></span>

![Estat de la reserva definit com a Flexible](media/Resource-Management-image77.png)

<span data-ttu-id="627f6-110">Quan la pestanya **Equip** està a la visualització **Membres de l'equip amb nom**, el recurs hi apareix.</span><span class="sxs-lookup"><span data-stu-id="627f6-110">When the **Team** tab is in the **Named Team Members** view, the resource appears there.</span></span> <span data-ttu-id="627f6-111">Les hores reservades de manera flexible es comuniquen a la columna **Hores reservades de manera flexible**.</span><span class="sxs-lookup"><span data-stu-id="627f6-111">The soft-booked hours are reported in the **Soft Booked Hours** column.</span></span>

![Hores reservades de manera flexible a la visualització Membres de l'equip amb nom](media/Resource-Management-image78.png)

<span data-ttu-id="627f6-113">Els membres de l'equip reservats de manera flexible no poden assignar-se a tasques.</span><span class="sxs-lookup"><span data-stu-id="627f6-113">Soft-booked team members can be assigned to tasks.</span></span>

![Membre de l'equip reservat de manera flexible assignat a una tasca](media/Resource-Management-image79.png)

<span data-ttu-id="627f6-115">A la pestanya **Conciliació**, no es mostra cap reserva per a un recurs reservat de manera flexible , ja que la pestanya **Conciliació** només té en compte les reserves fixes.</span><span class="sxs-lookup"><span data-stu-id="627f6-115">On the **Reconciliation** tab, no bookings are shown for a soft-book resource, because the **Reconciliation** tab considers only hard-bookings.</span></span>

![Recurs reservat de manera flexible sense reserves a la pestanya Conciliació](media/Resource-Management-image80.png)

> [!NOTE]
> <span data-ttu-id="627f6-117">No es pot reservar un recurs de manera flexible d'un requisit generat a partir d'un membre de l'equip genèric.</span><span class="sxs-lookup"><span data-stu-id="627f6-117">You can't soft-book a resource from a requirement that was generated from a generic team member.</span></span>

<span data-ttu-id="627f6-118">Al Tauler de planificació, s'utilitza un color diferent per a les reserves flexibles d'un recurs.</span><span class="sxs-lookup"><span data-stu-id="627f6-118">On the Schedule Board, a different coloring is used for soft bookings for a resource.</span></span>

![Reserves flexibles al Tauler de planificació](media/Resource-Management-image81.png)

<span data-ttu-id="627f6-120">Per convertir una reserva flexible en una reserva fixa, al Tauler de planificació, feu clic amb el botó dret a la reserva flexible i, a continuació, seleccioneu **Canvia l'estat** \> **Reserva fixa** \> **Fixa**.</span><span class="sxs-lookup"><span data-stu-id="627f6-120">To convert a soft booking to a hard booking, on the Schedule Board, right-click the soft booking, and then select **Change Status** \> **Hard Book** \> **Hard**.</span></span>

![Canviar l'estat de la reserva a Fixa](media/Resource-Management-image82.png)

<span data-ttu-id="627f6-122">Es canvia la reserva i l'estat canvia al Tauler de planificació.</span><span class="sxs-lookup"><span data-stu-id="627f6-122">The booking is changed, and the status is changed on the Schedule Board.</span></span> <span data-ttu-id="627f6-123">Com que l'estat de la reserva ara és **Fixa**, el recurs es mostra com a reservat i la seva capacitat i disponibilitat s'ajusten.</span><span class="sxs-lookup"><span data-stu-id="627f6-123">Because the booking status is now **Hard**, the resource is shown as booked, and its capacity and availability are adjusted.</span></span>

<span data-ttu-id="627f6-124">Podeu utilitzar el mateix mètode per cancel·lar una reserva fixa o una reserva flexible al Tauler de planificació.</span><span class="sxs-lookup"><span data-stu-id="627f6-124">You can use the same method to cancel a hard booking or a soft booking from the Schedule Board.</span></span>

<span data-ttu-id="627f6-125">Per convertir un recurs reservat de manera flexible a reservat de manera fixa a la pestanya **Equip** del projecte, seleccioneu el recurs i, a continuació, seleccioneu **Confirma**.</span><span class="sxs-lookup"><span data-stu-id="627f6-125">To convert a resource that is soft-booked to hard-booked on the project's **Team** tab, select the resource, and then select **Confirm**.</span></span>

![Ordre Confirma](media/Resource-Management-image83.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]