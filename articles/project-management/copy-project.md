---
title: Còpia d'un projecte
description: Aquest tema proporciona informació sobre la còpia de projectes al Dynamics 365 Project Operations.
author: ruhercul
ms.date: 05/21/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: c3055ab5b8c07faa2bc9167956d283e2a66029dd
ms.sourcegitcommit: 173f2b1f4e063c440a5f78d76d456c62aadbd89e
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/24/2021
ms.locfileid: "6091242"
---
# <a name="copy-a-project"></a><span data-ttu-id="4646e-103">Còpia d'un projecte</span><span class="sxs-lookup"><span data-stu-id="4646e-103">Copy a project</span></span>

<span data-ttu-id="4646e-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_</span><span class="sxs-lookup"><span data-stu-id="4646e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="4646e-105">Amb el Dynamics 365 Project Operations, podeu crear projectes nous ràpidament seleccionant **Copia el projecte** al formulari **Projectes**.</span><span class="sxs-lookup"><span data-stu-id="4646e-105">With Dynamics 365 Project Operations, you can quickly build new projects by selecting **Copy Project** on the **Projects** form.</span></span> <span data-ttu-id="4646e-106">Per copiar un projecte, obriu el projecte que voleu copiar i seleccioneu **Copia el projecte**.</span><span class="sxs-lookup"><span data-stu-id="4646e-106">To copy a project, open the project you want to copy, and then select **Copy project**.</span></span> <span data-ttu-id="4646e-107">L'acció copiarà el següent:</span><span class="sxs-lookup"><span data-stu-id="4646e-107">The action will copy the following:</span></span>

- <span data-ttu-id="4646e-108">Les propietats del projecte</span><span class="sxs-lookup"><span data-stu-id="4646e-108">Project properties</span></span> 
- <span data-ttu-id="4646e-109">Estructura del desglossament del treball</span><span class="sxs-lookup"><span data-stu-id="4646e-109">Work breakdown structure</span></span>
- <span data-ttu-id="4646e-110">Membres de l'equip del projecte</span><span class="sxs-lookup"><span data-stu-id="4646e-110">Project team members</span></span>
- <span data-ttu-id="4646e-111">Estimacions del projecte</span><span class="sxs-lookup"><span data-stu-id="4646e-111">Project estimates</span></span>
- <span data-ttu-id="4646e-112">Estimacions de despesa del projecte</span><span class="sxs-lookup"><span data-stu-id="4646e-112">Project expense estimates</span></span>
- <span data-ttu-id="4646e-113">Estimacions de materials del projecte</span><span class="sxs-lookup"><span data-stu-id="4646e-113">Project material estimates</span></span>

## <a name="project-properties"></a><span data-ttu-id="4646e-114">Les propietats del projecte</span><span class="sxs-lookup"><span data-stu-id="4646e-114">Project properties</span></span>

<span data-ttu-id="4646e-115">Quan el projecte es copia, es copien els valors dels camps següents:</span><span class="sxs-lookup"><span data-stu-id="4646e-115">When the project is copied, the values in the following fields are copied:</span></span>

- <span data-ttu-id="4646e-116">Nom</span><span class="sxs-lookup"><span data-stu-id="4646e-116">Name</span></span>
- <span data-ttu-id="4646e-117">Descripció</span><span class="sxs-lookup"><span data-stu-id="4646e-117">Description</span></span>
- <span data-ttu-id="4646e-118">Client</span><span class="sxs-lookup"><span data-stu-id="4646e-118">Customer</span></span>
- <span data-ttu-id="4646e-119">Plantilla de calendari</span><span class="sxs-lookup"><span data-stu-id="4646e-119">Calendar Template</span></span>
- <span data-ttu-id="4646e-120">Moneda</span><span class="sxs-lookup"><span data-stu-id="4646e-120">Currency</span></span>
- <span data-ttu-id="4646e-121">Unitat de contractació</span><span class="sxs-lookup"><span data-stu-id="4646e-121">Contracting Unit</span></span>
- <span data-ttu-id="4646e-122">Administrador de projectes</span><span class="sxs-lookup"><span data-stu-id="4646e-122">Project Manager</span></span>
- <span data-ttu-id="4646e-123">Estat</span><span class="sxs-lookup"><span data-stu-id="4646e-123">Status</span></span>
- <span data-ttu-id="4646e-124">Estat general del projecte</span><span class="sxs-lookup"><span data-stu-id="4646e-124">Overall Project Status</span></span>
- <span data-ttu-id="4646e-125">Comentaris</span><span class="sxs-lookup"><span data-stu-id="4646e-125">Comments</span></span>
- <span data-ttu-id="4646e-126">Estimacions</span><span class="sxs-lookup"><span data-stu-id="4646e-126">Estimates</span></span>
- <span data-ttu-id="4646e-127">Data d'inici prevista: aquesta és la data de creació del projecte a partir de la còpia.</span><span class="sxs-lookup"><span data-stu-id="4646e-127">Estimated Start Date: This is the date that the project is created from the copy.</span></span>
- <span data-ttu-id="4646e-128">Data de finalització prevista: aquesta data s'ajusta segons la data d'inici del nou projecte que s'ha fet a partir de la còpia.</span><span class="sxs-lookup"><span data-stu-id="4646e-128">Estimated Finish Date: This date is adjusted based on the start date of the new project that was made from the copy.</span></span>
- <span data-ttu-id="4646e-129">Esforç (hores)</span><span class="sxs-lookup"><span data-stu-id="4646e-129">Effort (Hours)</span></span>
- <span data-ttu-id="4646e-130">Cost estimat de la mà d’obra</span><span class="sxs-lookup"><span data-stu-id="4646e-130">Estimated Labor Cost</span></span>
- <span data-ttu-id="4646e-131">Cost estimat de les despeses</span><span class="sxs-lookup"><span data-stu-id="4646e-131">Estimated Expense Cost</span></span>
- <span data-ttu-id="4646e-132">Cost estimat del material</span><span class="sxs-lookup"><span data-stu-id="4646e-132">Estimated Material Cost</span></span>

> [!NOTE]
> <span data-ttu-id="4646e-133">Copiar un projecte és una operació de llarga execució.</span><span class="sxs-lookup"><span data-stu-id="4646e-133">Copy project is a long running operation.</span></span> <span data-ttu-id="4646e-134">També es copien els registres de projecte, els seus atributs rellevants i moltes entitats relacionades.</span><span class="sxs-lookup"><span data-stu-id="4646e-134">Project records, their relevant attributes, and many related entities are also copied.</span></span> <span data-ttu-id="4646e-135">A causa del caràcter de llarga execució de l'operació, un cop iniciada la còpia, la pàgina del projecte de destinació queda blocada per editar-la fins que l'operació de còpia s'ha completat.</span><span class="sxs-lookup"><span data-stu-id="4646e-135">Because of the long running nature of the operation, after the copy starts, the target project page is locked for editing until the copy operation is complete.</span></span>

## <a name="work-breakdown-structure"></a><span data-ttu-id="4646e-136">Estructura del desglossament del treball</span><span class="sxs-lookup"><span data-stu-id="4646e-136">Work breakdown structure</span></span>

<span data-ttu-id="4646e-137">Quan es copia el projecte, es copia tota l'estructura del desglossament del treball carregada de recursos.</span><span class="sxs-lookup"><span data-stu-id="4646e-137">When the project is copied, the entire resource-loaded work breakdown structure is copied.</span></span> <span data-ttu-id="4646e-138">Els recursos amb nom se substitueixen per recursos genèrics.</span><span class="sxs-lookup"><span data-stu-id="4646e-138">Named resources are replaced with generic resources.</span></span> <span data-ttu-id="4646e-139">Si els recursos amb nom no tenen les mateixes hores de feina que el recurs genèric, la planificació es tornarà a calcular i les duracions de les tasques poden canviar.</span><span class="sxs-lookup"><span data-stu-id="4646e-139">If the named resources don't have the same working hours as the generic resource, the schedule will be recalculated and task durations may change.</span></span>

## <a name="project-team-members"></a><span data-ttu-id="4646e-140">Membres de l'equip del projecte</span><span class="sxs-lookup"><span data-stu-id="4646e-140">Project team members</span></span>

<span data-ttu-id="4646e-141">Quan un equip del projecte es copia des del projecte d'origen, es copien els recursos genèrics.</span><span class="sxs-lookup"><span data-stu-id="4646e-141">When a project team is copied from the source project, the generic resources are copied.</span></span> <span data-ttu-id="4646e-142">Les assignacions de recursos genèrics també es mantenen com estaven al projecte d'origen.</span><span class="sxs-lookup"><span data-stu-id="4646e-142">Generic resource assignments are also maintained as they were in the source project.</span></span> <span data-ttu-id="4646e-143">Els recursos amb nom es convertiran en membres de l'equip genèric.</span><span class="sxs-lookup"><span data-stu-id="4646e-143">Named resources will be converted to generic team members.</span></span>

## <a name="estimates"></a><span data-ttu-id="4646e-144">Estimacions</span><span class="sxs-lookup"><span data-stu-id="4646e-144">Estimates</span></span>

<span data-ttu-id="4646e-145">Quan es copia el projecte, les línies de càlcul de recursos, despeses i materials es copien del projecte d'origen.</span><span class="sxs-lookup"><span data-stu-id="4646e-145">When the project is copied, resource, expense and material estimate lines are copied from the source project.</span></span> 

<span data-ttu-id="4646e-146">Per obtenir informació sobre com accedir mitjançant programació a Copia el projecte, vegeu [Desenvolupar plantilles de projecte amb Copia el projecte](dev-copy-project.md).</span><span class="sxs-lookup"><span data-stu-id="4646e-146">For information on how to programmatically access Copy Project, see [Develop project templates with Copy Project](dev-copy-project.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
