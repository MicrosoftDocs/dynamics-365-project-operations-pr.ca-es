---
title: Informació general sobre els modes d'administració de recursos
description: En aquest tema es proporciona informació sobre la funcionalitat d'administració de recursos al Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 4a8e605109e48b50da68abeee989f8ac8d3d659c
ms.sourcegitcommit: cf79185c8c84c55fbae55f9cfc1b17840e072b49
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930079"
---
# <a name="resource-management-modes-overview"></a><span data-ttu-id="217de-103">Informació general sobre els modes d'administració de recursos</span><span class="sxs-lookup"><span data-stu-id="217de-103">Resource management modes overview</span></span>

<span data-ttu-id="217de-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_</span><span class="sxs-lookup"><span data-stu-id="217de-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="217de-105">El Dynamics 365 Project Operations admet dos modes per executar el flux de reserva global.</span><span class="sxs-lookup"><span data-stu-id="217de-105">Dynamics 365 Project Operations supports two modes in order for you to execute the overall booking flow.</span></span> <span data-ttu-id="217de-106">El mode d'administració es defineix com un paràmetre de projecte i es pot modificar si el vostre negoci necessita canvis.</span><span class="sxs-lookup"><span data-stu-id="217de-106">The mode of management is defined as a project parameter and can be modified if your business needs change.</span></span>    

## <a name="central-mode"></a><span data-ttu-id="217de-107">Mode central</span><span class="sxs-lookup"><span data-stu-id="217de-107">Central mode</span></span>
<span data-ttu-id="217de-108">Per a les organitzacions que centralitzin l'assignació de recursos a projectes, el mode central proporciona una manera d'assegurar-se que els administradors de projectes puguin definir requisits de recursos al nivell de projecte.</span><span class="sxs-lookup"><span data-stu-id="217de-108">For organizations who centralize the allocation for resources to projects, the Central mode provides a way to ensure Project managers can define resource requirements at the project level.</span></span> <span data-ttu-id="217de-109">El compliment dels requisits de recursos es delega en un administrador de recursos.</span><span class="sxs-lookup"><span data-stu-id="217de-109">Fulfillment of the resource requirements is delegated to a Resource manager.</span></span> <span data-ttu-id="217de-110">Els administradors de projectes poden acceptar o rebutjar els recursos que proposar l'administrador de recursos.</span><span class="sxs-lookup"><span data-stu-id="217de-110">Project managers can accept or reject resources that are proposed by the Resource manager.</span></span>

![Mode central](./media/resource-management-central.png)

<span data-ttu-id="217de-112">Per administrar els recursos amb el mode central, vegeu:</span><span class="sxs-lookup"><span data-stu-id="217de-112">To manage resources with the Central mode, see:</span></span>

- [<span data-ttu-id="217de-113">Assignació de recursos genèrics que es poden reservar a una tasca i generació de requisits de recursos</span><span class="sxs-lookup"><span data-stu-id="217de-113">Assign generic bookable resources to a task and generate resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="217de-114">Reserva de recursos amb nom a partir dels requisits de recursos</span><span class="sxs-lookup"><span data-stu-id="217de-114">Book named resources from resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
- [<span data-ttu-id="217de-115">Enviament d'una sol·licitud de recurs</span><span class="sxs-lookup"><span data-stu-id="217de-115">Submit a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/submit-resource-request)
- [<span data-ttu-id="217de-116">Complir una sol·licitud de recursos</span><span class="sxs-lookup"><span data-stu-id="217de-116">Fulfill a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/resource-management-fulfill-requests)
- [<span data-ttu-id="217de-117">Acceptar o rebutjar un recurs del projecte proposat des d'una sol·licitud de recurs</span><span class="sxs-lookup"><span data-stu-id="217de-117">Accept or reject a proposed project resource from a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a><span data-ttu-id="217de-118">Mode híbrid</span><span class="sxs-lookup"><span data-stu-id="217de-118">Hybrid mode</span></span>
<span data-ttu-id="217de-119">Per a les organitzacions que requereixin flexibilitat en l'assignació de recursos, el mode híbrid permet que tant els administradors de projectes com els administradors de recursos puguin reservar recursos.</span><span class="sxs-lookup"><span data-stu-id="217de-119">For organizations who require flexibility in the allocation of resources, the hybrid mode enables both Project managers and Resource managers the ability to book resources.</span></span>

![Mode híbrid](./media/resource-management-hybrid.png)

<span data-ttu-id="217de-121">A més del procés del mode central admès, vegeu els temes següents per administrar tots els altres fluxos de reserva admesos en el mode híbrid:</span><span class="sxs-lookup"><span data-stu-id="217de-121">In addition to the supported Central mode process, see the following topics to manage all other supported booking flows in the Hybrid mode:</span></span>

<span data-ttu-id="217de-122">Reservar un recurs directament a un projecte:</span><span class="sxs-lookup"><span data-stu-id="217de-122">Book a resource directly to a project:</span></span>
- [<span data-ttu-id="217de-123">Reservar recursos que es poden reservar a un equip de projecte i assignar tasques</span><span class="sxs-lookup"><span data-stu-id="217de-123">Book named bookable resources to a project team and assign tasks</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-named-bookable-resource)

<span data-ttu-id="217de-124">Reservar un recurs des d'un requisit de recursos:</span><span class="sxs-lookup"><span data-stu-id="217de-124">Book a resource from a resource requirement:</span></span>
- [<span data-ttu-id="217de-125">Assignació de recursos genèrics que es poden reservar a una tasca i generació de requisits de recursos</span><span class="sxs-lookup"><span data-stu-id="217de-125">Assign generic bookable resources to a task and generate resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="217de-126">Reserva de recursos amb nom a partir dels requisits de recursos</span><span class="sxs-lookup"><span data-stu-id="217de-126">Book named resources from resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
