---
title: Reserves en comparació amb assignacions
description: En aquest tema es proporciona informació sobre les diferències entre les reserves de recursos i les assignacions de recursos.
author: ruhercul
manager: Annbe
ms.date: 01/08/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 3aaf8dcbae0a5762879c2b1223eba3bdc33af1a7
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279891"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="985e0-103">Reserves en comparació amb assignacions</span><span class="sxs-lookup"><span data-stu-id="985e0-103">Bookings vs assignments</span></span>

<span data-ttu-id="985e0-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_</span><span class="sxs-lookup"><span data-stu-id="985e0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="985e0-105">Les reserves són l'assignació fixa o flexible de recursos a un projecte.</span><span class="sxs-lookup"><span data-stu-id="985e0-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="985e0-106">Les reserves fixes consumeixen la capacitat d'un recurs.</span><span class="sxs-lookup"><span data-stu-id="985e0-106">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="985e0-107">Les reserves representen conceptes organitzatius per als equips perquè puguin entendre com es dedicaran els recursos entre diversos projectes.</span><span class="sxs-lookup"><span data-stu-id="985e0-107">Bookings represent organizational concepts for teams so that they can understand how resources will be engaged across various projects.</span></span> <span data-ttu-id="985e0-108">El Dynamics 365 Project Operations considera les reserves un concepte a nivell de projecte.</span><span class="sxs-lookup"><span data-stu-id="985e0-108">Dynamics 365 Project Operations considers bookings a project-level concept.</span></span> 

<span data-ttu-id="985e0-109">A diferència de les reserves, les assignacions són el compromís de recursos a tasques de projecte a la planificació del projecte.</span><span class="sxs-lookup"><span data-stu-id="985e0-109">Unlike bookings, assignments are the commitment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="985e0-110">Els recursos poden tenir nom o ser genèrics.</span><span class="sxs-lookup"><span data-stu-id="985e0-110">The resources can be named or generic.</span></span>  <span data-ttu-id="985e0-111">Quan un requisit de recurs deriva de les assignacions de tasques del projecte, el Project Operations utilitza els contorns d'esforç de l'assignació de recursos per crear els contorns dels detalls del requisit de recursos.</span><span class="sxs-lookup"><span data-stu-id="985e0-111">When a resource requirement is derived from the project task assignments, Project Operations uses the effort contours of the resources assignment to build the contours of the resource requirement details.</span></span> <span data-ttu-id="985e0-112">No obstant això, no es manté cap refència a les assignacions de recursos.</span><span class="sxs-lookup"><span data-stu-id="985e0-112">However, a refence to the resource assignments isn't maintained.</span></span> <span data-ttu-id="985e0-113">Les actualitzacions de les reserves derivades del requisit de recursos no actualitzen cap assignació de recursos.</span><span class="sxs-lookup"><span data-stu-id="985e0-113">Updates to the bookings derived from the resource requirement don't update any resource assignments.</span></span>

<span data-ttu-id="985e0-114">Normalment, la suma de les reserves d'un recurs equivaldrà a la suma de les assignacions del recurs en una o moltes tasques.</span><span class="sxs-lookup"><span data-stu-id="985e0-114">Typically, the sum of the bookings for a resource will equal the sum of the resource's assignments across one or many tasks.</span></span> <span data-ttu-id="985e0-115">No obstant, el Project Operations no obliga a aplicar aquesta concordança.</span><span class="sxs-lookup"><span data-stu-id="985e0-115">However, Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="985e0-116">La visualització **Conciliació** mostra llocs a l'administrador del projecte on les reserves i les assignacions d'un recurs no coincideixen.</span><span class="sxs-lookup"><span data-stu-id="985e0-116">The **Reconciliation** view shows the Project manager places where a resource's bookings and assignments don't agree.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]