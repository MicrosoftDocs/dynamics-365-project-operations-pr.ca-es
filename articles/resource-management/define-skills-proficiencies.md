---
title: Definició d'aptituds i competències
description: En aquest tema es proporciona informació sobre com configurar models de competència per puntuar recursos.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
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
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 8738a4743554704ef76807c81fdefcd74e668e1b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4124761"
---
# <a name="define-skills-and-proficiencies"></a><span data-ttu-id="dd3d0-103">Definició d'aptituds i competències</span><span class="sxs-lookup"><span data-stu-id="dd3d0-103">Define skills and proficiencies</span></span>

<span data-ttu-id="dd3d0-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_</span><span class="sxs-lookup"><span data-stu-id="dd3d0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="dd3d0-105">Les aptituds són característiques de recursos compartides entre el Dynamics 365 Project Operations i el Dynamics 365 Field Service, si està present.</span><span class="sxs-lookup"><span data-stu-id="dd3d0-105">Skills are resource characteristics that are shared between Dynamics 365 Project Operations and if present, Dynamics 365 Field Service.</span></span> 

- <span data-ttu-id="dd3d0-106">Per mantenir el dipòsit d'aptituds del Project Operations, aneu a **Recursos** \> **Aptituds de recursos**.</span><span class="sxs-lookup"><span data-stu-id="dd3d0-106">To maintain the repository of skills in Project Operations, go to **Resources** \> **Resource Skills**.</span></span> 

## <a name="use-proficiency-models-to-rate-resources"></a><span data-ttu-id="dd3d0-107">Utilitzar models de competència per puntuar recursos</span><span class="sxs-lookup"><span data-stu-id="dd3d0-107">Use proficiency models to rate resources</span></span>

<span data-ttu-id="dd3d0-108">Les aptituds per als recursos són valorades pels models de competència.</span><span class="sxs-lookup"><span data-stu-id="dd3d0-108">Skills for resources are rated by proficiency models.</span></span> <span data-ttu-id="dd3d0-109">Les puntuacions individuals es troben en un model de competència.</span><span class="sxs-lookup"><span data-stu-id="dd3d0-109">The individual ratings are in a proficiency model.</span></span> 

1. <span data-ttu-id="dd3d0-110">Per crear un model de competència, aneu a **Recursos** \> **Models de competència** i, a continuació, seleccioneu **Nou**.</span><span class="sxs-lookup"><span data-stu-id="dd3d0-110">To create a proficiency model, go to **Resources** \> **Proficiency Models**, and then select **New**.</span></span>
2. <span data-ttu-id="dd3d0-111">Al model de puntuació nou, especifiqueu el valor de puntuació mínim, el valor màxim i l'entitat que està sent puntuada.</span><span class="sxs-lookup"><span data-stu-id="dd3d0-111">In the new rating model, specify the minimum rating value, the maximum rating value, and the entity that is being rated.</span></span>
3. <span data-ttu-id="dd3d0-112">A la subquadrícula **Valors de classificació**, podeu definir els valors de classificació diferents, del mínim al màxim.</span><span class="sxs-lookup"><span data-stu-id="dd3d0-112">In the **Rating Values** subgrid, you can define the different rating values, from the minimum to the maximum.</span></span>


<span data-ttu-id="dd3d0-113">Aquests valors de puntuació es mostren als filtres **Requisits de recursos**, **Tauler de planificació** i **Auxiliar de planificació**.</span><span class="sxs-lookup"><span data-stu-id="dd3d0-113">These rating values are shown on the **Resource Requirements**, **Schedule Board**, and **Schedule Assistant** filters.</span></span>
