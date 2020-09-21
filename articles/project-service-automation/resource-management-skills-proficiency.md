---
title: Aptituds i models de competència
description: En aquest tema es proporciona informació sobre com utilitzar les aptituds i els models de competència.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: d55a6d72-905f-4b82-a9fe-0b6b082473a6
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: fe4c9a62cd2ec1365daa09714fa6fa19210a7770
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749571"
---
# <a name="skills-and-proficiency-models"></a><span data-ttu-id="1ce15-103">Aptituds i models de competència</span><span class="sxs-lookup"><span data-stu-id="1ce15-103">Skills and proficiency models</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="1ce15-104">Les aptituds són característiques de recursos compartides entre el Dynamics 365 Project Service Automation i el Dynamics 365 Field Service, si està present.</span><span class="sxs-lookup"><span data-stu-id="1ce15-104">Skills are resource characteristics that are shared between Dynamics 365 Project Service Automation and if present, Dynamics 365 Field Service.</span></span> 

<span data-ttu-id="1ce15-105">Per mantenir el dipòsit d'aptituds del Project Service Automation, aneu a **Recursos** \> **Aptituds de recursos**.</span><span class="sxs-lookup"><span data-stu-id="1ce15-105">To maintain the repository of skills in Project Service Automation, go to **Resources** \> **Resource Skills**.</span></span> 

> ![Aptituds de recursos](media/Resource-Management-image84.png)

## <a name="use-proficiency-models-to-rate-resources"></a><span data-ttu-id="1ce15-107">Utilitzar models de competència per puntuar recursos</span><span class="sxs-lookup"><span data-stu-id="1ce15-107">Use proficiency models to rate resources</span></span>

<span data-ttu-id="1ce15-108">Les aptituds per als recursos són valorades pels models de competència.</span><span class="sxs-lookup"><span data-stu-id="1ce15-108">Skills for resources are rated by proficiency models.</span></span> <span data-ttu-id="1ce15-109">Les puntuacions individuals es troben en un model de competència.</span><span class="sxs-lookup"><span data-stu-id="1ce15-109">The individual ratings are in a proficiency model.</span></span> 

1. <span data-ttu-id="1ce15-110">Per crear un model de competència, aneu a **Recursos** \> **Models de competència** i, a continuació, seleccioneu **Nou**.</span><span class="sxs-lookup"><span data-stu-id="1ce15-110">To create a proficiency model, go to **Resources** \> **Proficiency Models**, and then select **New**.</span></span>
2. <span data-ttu-id="1ce15-111">Al model de puntuació nou, especifiqueu el valor de puntuació mínim, el valor màxim i l'entitat que està sent puntuada.</span><span class="sxs-lookup"><span data-stu-id="1ce15-111">In the new rating model, specify the minimum rating value, the maximum rating value, and the entity that is being rated.</span></span>
3. <span data-ttu-id="1ce15-112">A la subquadrícula **Valors de puntuació**, podeu definir els valors de classificació diferents, del mínim al màxim.</span><span class="sxs-lookup"><span data-stu-id="1ce15-112">In the **Rating Values** sub-grid, you can define the different rating values, from the minimum to the maximum.</span></span>

> ![Puntuacions mínimes i màximes definides](media/Resource-Management-image85.png)

<span data-ttu-id="1ce15-114">Aquests valors de puntuació es mostren als filtres **Requisits de recursos**, **Tauler de planificació** i **Auxiliar de planificació**.</span><span class="sxs-lookup"><span data-stu-id="1ce15-114">These rating values are shown on the **Resource Requirements**, **Schedule Board**, and **Schedule Assistant** filters.</span></span>
