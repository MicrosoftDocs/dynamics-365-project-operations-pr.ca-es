---
title: Reserves en comparació amb assignacions
description: En aquest tema es proporciona informació sobre les diferències entre les reserves de recursos i les assignacions de recursos.
author: ruhercul
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 8fe6937dfdfe137f28917c16da1d7dc6155284ae
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130206"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="dbb7c-103">Reserves en comparació amb assignacions</span><span class="sxs-lookup"><span data-stu-id="dbb7c-103">Bookings vs assignments</span></span>

<span data-ttu-id="dbb7c-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_</span><span class="sxs-lookup"><span data-stu-id="dbb7c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="dbb7c-105">Les reserves són l'assignació fixa o flexible de recursos a un projecte.</span><span class="sxs-lookup"><span data-stu-id="dbb7c-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="dbb7c-106">Les reserves fixes consumeixen la capacitat d'un recurs.</span><span class="sxs-lookup"><span data-stu-id="dbb7c-106">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="dbb7c-107">Les reserves representen conceptes organitzatius per als equips perquè puguin entendre com es dedicaran els recursos entre diversos projectes.</span><span class="sxs-lookup"><span data-stu-id="dbb7c-107">Bookings represent organizational concepts for teams so that they can understand how resources will be engaged across various projects.</span></span> <span data-ttu-id="dbb7c-108">El Dynamics 365 Project Operations considera les reserves un concepte a nivell de projecte.</span><span class="sxs-lookup"><span data-stu-id="dbb7c-108">Dynamics 365 Project Operations considers bookings a project-level concept.</span></span> 

<span data-ttu-id="dbb7c-109">A diferència de les reserves, les assignacions són el compromís de recursos a tasques de projecte a la planificació del projecte.</span><span class="sxs-lookup"><span data-stu-id="dbb7c-109">Unlike bookings, assignments are the commitment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="dbb7c-110">Els recursos poden tenir nom o ser genèrics.</span><span class="sxs-lookup"><span data-stu-id="dbb7c-110">The resources can be named or generic.</span></span> 

<span data-ttu-id="dbb7c-111">Normalment, la suma de les reserves d'un recurs equivaldrà a la suma de les assignacions del recurs en una o moltes tasques.</span><span class="sxs-lookup"><span data-stu-id="dbb7c-111">Typically, the sum of the bookings for a resource will equal the sum of the resource's assignments across one or many tasks.</span></span> <span data-ttu-id="dbb7c-112">No obstant, el Project Operations no obliga a aplicar aquesta concordança.</span><span class="sxs-lookup"><span data-stu-id="dbb7c-112">However, Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="dbb7c-113">La visualització **Conciliació** mostra llocs a l'administrador del projecte on les reserves i les assignacions d'un recurs no coincideixen.</span><span class="sxs-lookup"><span data-stu-id="dbb7c-113">The **Reconciliation** view shows the Project manager places where a resource's bookings and assignments don't agree.</span></span>
