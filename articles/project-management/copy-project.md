---
title: Còpia d'un projecte
description: Aquest tema proporciona informació sobre la còpia de projectes al Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 02/22/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: af1942e81691d9e13fdcbbf68599c1a8a4004582
ms.sourcegitcommit: 24528bb9c0ef8898077cb3bc672daa211c0e73aa
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 03/04/2021
ms.locfileid: "5479507"
---
# <a name="copy-a-project"></a><span data-ttu-id="41102-103">Còpia d'un projecte</span><span class="sxs-lookup"><span data-stu-id="41102-103">Copy a project</span></span>

<span data-ttu-id="41102-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_</span><span class="sxs-lookup"><span data-stu-id="41102-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="41102-105">Amb el Dynamics 365 Project Operations, podeu crear projectes nous ràpidament seleccionant **Copia el projecte** al formulari **Projectes**.</span><span class="sxs-lookup"><span data-stu-id="41102-105">With Dynamics 365 Project Operations, you can quickly build new projects by selecting **Copy Project** on the **Projects** form.</span></span> <span data-ttu-id="41102-106">Per copiar un projecte, obriu el projecte que voleu copiar i seleccioneu **Copia el projecte**.</span><span class="sxs-lookup"><span data-stu-id="41102-106">To copy a project, open the project you want to copy, and then select **Copy project**.</span></span> <span data-ttu-id="41102-107">L'acció copiarà:</span><span class="sxs-lookup"><span data-stu-id="41102-107">The action will copy:</span></span>

- <span data-ttu-id="41102-108">Propietats del projecte (La data d'inici estimada es copia del projecte d'origen)</span><span class="sxs-lookup"><span data-stu-id="41102-108">Project properties (The estimated start date is copied from the source project)</span></span>
- <span data-ttu-id="41102-109">L'estructura del desglossament del treball</span><span class="sxs-lookup"><span data-stu-id="41102-109">The Work breakdown structure</span></span>
- <span data-ttu-id="41102-110">Membres de l'equip del projecte</span><span class="sxs-lookup"><span data-stu-id="41102-110">Project team members</span></span>
- <span data-ttu-id="41102-111">Estimacions del projecte</span><span class="sxs-lookup"><span data-stu-id="41102-111">Project estimates</span></span>
- <span data-ttu-id="41102-112">Estimacions de despesa del projecte</span><span class="sxs-lookup"><span data-stu-id="41102-112">Project expense estimates</span></span>

## <a name="project-properties"></a><span data-ttu-id="41102-113">Propietats del projecte</span><span class="sxs-lookup"><span data-stu-id="41102-113">Project properties</span></span>

<span data-ttu-id="41102-114">Quan el projecte es copia, es copien els valors dels camps següents:</span><span class="sxs-lookup"><span data-stu-id="41102-114">When the project is copied, the values in the following fields are copied:</span></span>

- <span data-ttu-id="41102-115">Nom</span><span class="sxs-lookup"><span data-stu-id="41102-115">Name</span></span>
- <span data-ttu-id="41102-116">Descripció</span><span class="sxs-lookup"><span data-stu-id="41102-116">Description</span></span>
- <span data-ttu-id="41102-117">Client</span><span class="sxs-lookup"><span data-stu-id="41102-117">Customer</span></span>
- <span data-ttu-id="41102-118">Plantilla de calendari</span><span class="sxs-lookup"><span data-stu-id="41102-118">Calendar Template</span></span>
- <span data-ttu-id="41102-119">Moneda</span><span class="sxs-lookup"><span data-stu-id="41102-119">Currency</span></span>
- <span data-ttu-id="41102-120">Unitat de contractació</span><span class="sxs-lookup"><span data-stu-id="41102-120">Contracting Unit</span></span>
- <span data-ttu-id="41102-121">Administrador de projectes</span><span class="sxs-lookup"><span data-stu-id="41102-121">Project Manager</span></span>
- <span data-ttu-id="41102-122">Estat</span><span class="sxs-lookup"><span data-stu-id="41102-122">Status</span></span>
- <span data-ttu-id="41102-123">Estat general del projecte</span><span class="sxs-lookup"><span data-stu-id="41102-123">Overall Project Status</span></span>
- <span data-ttu-id="41102-124">Comentaris</span><span class="sxs-lookup"><span data-stu-id="41102-124">Comments</span></span>
- <span data-ttu-id="41102-125">Estimacions</span><span class="sxs-lookup"><span data-stu-id="41102-125">Estimates</span></span>
- <span data-ttu-id="41102-126">Data d’inici estimada</span><span class="sxs-lookup"><span data-stu-id="41102-126">Estimated Start Date</span></span>
- <span data-ttu-id="41102-127">Data de finalització</span><span class="sxs-lookup"><span data-stu-id="41102-127">Finish Date</span></span>
- <span data-ttu-id="41102-128">Esforç (hores)</span><span class="sxs-lookup"><span data-stu-id="41102-128">Effort (Hours)</span></span>
- <span data-ttu-id="41102-129">Cost estimat de la mà d’obra</span><span class="sxs-lookup"><span data-stu-id="41102-129">Estimated Labor Cost</span></span>
- <span data-ttu-id="41102-130">Cost estimat de les despeses</span><span class="sxs-lookup"><span data-stu-id="41102-130">Estimated Expense Cost</span></span>

## <a name="work-breakdown-structure"></a><span data-ttu-id="41102-131">Estructura del desglossament del treball</span><span class="sxs-lookup"><span data-stu-id="41102-131">Work breakdown structure</span></span>

<span data-ttu-id="41102-132">Quan es copia el projecte, es copia tota l'estructura del desglossament del treball carregada de recursos.</span><span class="sxs-lookup"><span data-stu-id="41102-132">When the project is copied, the entire resource-loaded work breakdown structure is copied.</span></span> <span data-ttu-id="41102-133">Els recursos amb nom se substitueixen per recursos genèrics.</span><span class="sxs-lookup"><span data-stu-id="41102-133">Named resources are replaced with generic resources.</span></span> <span data-ttu-id="41102-134">Si els recursos amb nom no tenen les mateixes hores de feina que el recurs genèric, la planificació es tornarà a calcular i les duracions de les tasques poden canviar.</span><span class="sxs-lookup"><span data-stu-id="41102-134">If the named resources don't have the same working hours as the generic resource, the schedule will be recalculated and task durations may change.</span></span>

## <a name="project-team-members"></a><span data-ttu-id="41102-135">Membres de l'equip del projecte</span><span class="sxs-lookup"><span data-stu-id="41102-135">Project team members</span></span>

<span data-ttu-id="41102-136">Quan un equip del projecte es copia des del projecte d'origen, es copien els recursos genèrics.</span><span class="sxs-lookup"><span data-stu-id="41102-136">When a project team is copied from the source project, the generic resources are copied.</span></span> <span data-ttu-id="41102-137">Les assignacions de recursos genèrics també es mantenen com estaven al projecte d'origen.</span><span class="sxs-lookup"><span data-stu-id="41102-137">Generic resource assignments are also maintained as they were in the source project.</span></span> <span data-ttu-id="41102-138">Els recursos amb nom es convertiran en membres de l'equip genèric.</span><span class="sxs-lookup"><span data-stu-id="41102-138">Named resources will be converted to generic team members.</span></span>

## <a name="estimates"></a><span data-ttu-id="41102-139">Estimacions</span><span class="sxs-lookup"><span data-stu-id="41102-139">Estimates</span></span>

<span data-ttu-id="41102-140">Quan el projecte es copia, les línies d'estimació de recursos i de despesa es copien des del projecte d'origen.</span><span class="sxs-lookup"><span data-stu-id="41102-140">When the project is copied, both resource and expense estimate lines are copied from the source project.</span></span> 

<span data-ttu-id="41102-141">Per obtenir informació sobre com accedir mitjançant programació a Copia el projecte, vegeu [Desenvolupar plantilles de projecte amb Copia el projecte](dev-copy-project.md).</span><span class="sxs-lookup"><span data-stu-id="41102-141">For information on how to programmatically access Copy Project, see [Develop project templates with Copy Project](dev-copy-project.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
