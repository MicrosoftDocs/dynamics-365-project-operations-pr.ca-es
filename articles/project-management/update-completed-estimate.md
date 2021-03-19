---
title: Actualització de l'estimació en finalitzar
description: En aquest tema es proporciona informació sobre l'actualització de la projecció de l'esforç en un projecte.
author: ruhercul
manager: AnnBe
ms.date: 09/20/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 0e63bdb815a6f758c57d055c8c03d92e04700445
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286416"
---
# <a name="update-estimate-at-completion"></a><span data-ttu-id="a7534-103">Actualització de l'estimació en finalitzar</span><span class="sxs-lookup"><span data-stu-id="a7534-103">Update estimate at completion</span></span>

<span data-ttu-id="a7534-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_</span><span class="sxs-lookup"><span data-stu-id="a7534-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a7534-105">És habitual que un administrador de projecte revisi les estimacions originals d'una tasca.</span><span class="sxs-lookup"><span data-stu-id="a7534-105">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="a7534-106">Les reprojeccions de projectes són la percepció de les estimacions d'un administrador de projecte, donat l'estat actual del projecte.</span><span class="sxs-lookup"><span data-stu-id="a7534-106">Project reprojections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="a7534-107">No obstant, no recomanem que els administradors de projectes canviïn els números de la línia de base, ja que la línia de base del projecte representa la font de veritat establerta de l'estimació de la planificació i el cost del projecte, i totes les parts interessades del projecte l'han acordat.</span><span class="sxs-lookup"><span data-stu-id="a7534-107">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="a7534-108">Hi ha dues maneres de fer que un administrador del projecte pugui tornar a projectar l'esforç de les tasques:</span><span class="sxs-lookup"><span data-stu-id="a7534-108">There are two ways that a project manager can reproject effort on tasks:</span></span>

- <span data-ttu-id="a7534-109">Substituir l'estimació per finalitzar (ETC) per defecte amb una nova estimació de l'esforç real restant de la tasca.</span><span class="sxs-lookup"><span data-stu-id="a7534-109">Override the default estimate to complete (ETC) with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="a7534-110">Substituir el percentatge de progrés per defecte amb una nova estimació del progrés real de la tasca.</span><span class="sxs-lookup"><span data-stu-id="a7534-110">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="a7534-111">Cadascuna d'aquestes aproximacions provoca un nou càlcul de l'ETC de la tasca, l'estimació en finalitzar (EAC) i el percentatge de progrés, i la variació de l'esforç projectat d'una tasca.</span><span class="sxs-lookup"><span data-stu-id="a7534-111">Each of these approaches cause a recalculation of the task's ETC, estimate at complete (EAC), and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="a7534-112">Es torna a calcular l'EAC, l'ETC i el percentatge de progrés de les tasques de resum, i produeixen una nova projecció de la variació d'esforç.</span><span class="sxs-lookup"><span data-stu-id="a7534-112">The EAC, ETC, and progress percentage on the summary tasks are recalculated, and produce a new projection of effort variance.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]