---
title: Reserves en comparació amb assignacions
description: En aquest tema es proporciona informació sobre les diferències entre les reserves de recursos i les assignacions de recursos.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fa99783e52dbcdeaf80bbfd03df0f458f86b5e99
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 09/28/2020
ms.locfileid: "3895999"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="f8222-103">Reserves en comparació amb assignacions</span><span class="sxs-lookup"><span data-stu-id="f8222-103">Bookings vs assignments</span></span>

<span data-ttu-id="f8222-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_</span><span class="sxs-lookup"><span data-stu-id="f8222-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f8222-105">Les reserves són l'assignació fixa o flexible de recursos a un projecte.</span><span class="sxs-lookup"><span data-stu-id="f8222-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="f8222-106">Les reserves fixes consumeixen la capacitat d'un recurs.</span><span class="sxs-lookup"><span data-stu-id="f8222-106">Hard bookings consume a resource's capacity.</span></span> 

<span data-ttu-id="f8222-107">Les assignacions són l'assignació de recursos a tasques de projecte a la planificació del projecte.</span><span class="sxs-lookup"><span data-stu-id="f8222-107">Assignments are the assignment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="f8222-108">Els recursos poden ser reals o genèrics.</span><span class="sxs-lookup"><span data-stu-id="f8222-108">The resources can be real or generic.</span></span> 

<span data-ttu-id="f8222-109">Idealment, per als recursos reals, les reserves i les assignacions haurien de concordar, perquè no es diferencien.</span><span class="sxs-lookup"><span data-stu-id="f8222-109">Ideally, for real resources, the bookings and assignments should agree, because they don't differ.</span></span> <span data-ttu-id="f8222-110">No obstant, el Microsoft Dynamics Project Operations no obliga a aplicar aquesta concordança.</span><span class="sxs-lookup"><span data-stu-id="f8222-110">However, Microsoft Dynamics Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="f8222-111">La visualització **Conciliació** mostra llocs a l'administrador del projecte on les reserves i les assignacions d'un recurs no coincideixen.</span><span class="sxs-lookup"><span data-stu-id="f8222-111">The **Reconciliation** view shows a project manager places where a resource's bookings and assignments don't agree.</span></span>
