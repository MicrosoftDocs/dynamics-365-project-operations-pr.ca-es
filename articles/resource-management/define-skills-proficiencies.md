---
title: Definició d'aptituds i competències
description: En aquest tema es proporciona informació sobre com configurar models de competència per puntuar recursos.
author: ruhercul
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 982f64677b74f2195eacc287fc07b80c34f7acc0
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6015319"
---
# <a name="define-skills-and-proficiencies"></a><span data-ttu-id="f5161-103">Definició d'aptituds i competències</span><span class="sxs-lookup"><span data-stu-id="f5161-103">Define skills and proficiencies</span></span>

<span data-ttu-id="f5161-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_</span><span class="sxs-lookup"><span data-stu-id="f5161-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f5161-105">Les aptituds són característiques de recursos compartides entre el Dynamics 365 Project Operations i el Dynamics 365 Field Service, si està present.</span><span class="sxs-lookup"><span data-stu-id="f5161-105">Skills are resource characteristics that are shared between Dynamics 365 Project Operations and if present, Dynamics 365 Field Service.</span></span> 

- <span data-ttu-id="f5161-106">Per mantenir el dipòsit d'aptituds del Project Operations, aneu a **Recursos** \> **Aptituds de recursos**.</span><span class="sxs-lookup"><span data-stu-id="f5161-106">To maintain the repository of skills in Project Operations, go to **Resources** \> **Resource Skills**.</span></span> 

## <a name="use-proficiency-models-to-rate-resources"></a><span data-ttu-id="f5161-107">Utilitzar models de competència per puntuar recursos</span><span class="sxs-lookup"><span data-stu-id="f5161-107">Use proficiency models to rate resources</span></span>

<span data-ttu-id="f5161-108">Les aptituds per als recursos són valorades pels models de competència.</span><span class="sxs-lookup"><span data-stu-id="f5161-108">Skills for resources are rated by proficiency models.</span></span> <span data-ttu-id="f5161-109">Les puntuacions individuals es troben en un model de competència.</span><span class="sxs-lookup"><span data-stu-id="f5161-109">The individual ratings are in a proficiency model.</span></span> 

1. <span data-ttu-id="f5161-110">Per crear un model de competència, aneu a **Recursos** \> **Models de competència** i, a continuació, seleccioneu **Nou**.</span><span class="sxs-lookup"><span data-stu-id="f5161-110">To create a proficiency model, go to **Resources** \> **Proficiency Models**, and then select **New**.</span></span>
2. <span data-ttu-id="f5161-111">Al model de puntuació nou, especifiqueu el valor de puntuació mínim, el valor màxim i l'entitat que està sent puntuada.</span><span class="sxs-lookup"><span data-stu-id="f5161-111">In the new rating model, specify the minimum rating value, the maximum rating value, and the entity that is being rated.</span></span>
3. <span data-ttu-id="f5161-112">A la subquadrícula **Valors de classificació**, podeu definir els valors de classificació diferents, del mínim al màxim.</span><span class="sxs-lookup"><span data-stu-id="f5161-112">In the **Rating Values** subgrid, you can define the different rating values, from the minimum to the maximum.</span></span>


<span data-ttu-id="f5161-113">Aquests valors de puntuació es mostren als filtres **Requisits de recursos**, **Tauler de planificació** i **Auxiliar de planificació**.</span><span class="sxs-lookup"><span data-stu-id="f5161-113">These rating values are shown on the **Resource Requirements**, **Schedule Board**, and **Schedule Assistant** filters.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]