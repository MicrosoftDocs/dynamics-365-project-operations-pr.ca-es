---
title: Creació d'una plantilla d'hores de feina
description: Aquesta tema descriu com crear una plantilla d'hores de treball al Project Service.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 105e3cb2ef7b904e96dc21013906e0b7444e3b88
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997184"
---
# <a name="create-a-work-hours-template-project-service"></a><span data-ttu-id="9696c-103">Crear una plantilla d'hores de treball (Project Service)</span><span class="sxs-lookup"><span data-stu-id="9696c-103">Create a work hours template (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="9696c-104">Per crear i administrar un projecte, heu d'aplicar una plantilla de calendari al projecte.</span><span class="sxs-lookup"><span data-stu-id="9696c-104">To create and manage a project, you must apply a calendar template to the project.</span></span> <span data-ttu-id="9696c-105">La plantilla de calendari defineix els atributs de projecte següents:</span><span class="sxs-lookup"><span data-stu-id="9696c-105">The calendar template defines the following project attributes:</span></span>

- <span data-ttu-id="9696c-106">Hores de feina, incloent-hi l'hora d'inici i d'acabament</span><span class="sxs-lookup"><span data-stu-id="9696c-106">Working hours, including start and end time</span></span>
- <span data-ttu-id="9696c-107">Dies feiners</span><span class="sxs-lookup"><span data-stu-id="9696c-107">Working days</span></span>
- <span data-ttu-id="9696c-108">Excepcions del calendari, com ara dies que no són feiners</span><span class="sxs-lookup"><span data-stu-id="9696c-108">Calendar exceptions such as non-working days</span></span>

<span data-ttu-id="9696c-109">La plantilla de calendari que s'aplica a un projecte és una còpia de la plantilla de calendari definida a la configuració de l'organització.</span><span class="sxs-lookup"><span data-stu-id="9696c-109">The calendar template that's applied to a project is a copy of the calendar template defined in your organization’s settings.</span></span>

> [!NOTE]
> <span data-ttu-id="9696c-110">Si canvieu la plantilla de calendari, els canvis no s'emplenen a les hores de feina del projecte.</span><span class="sxs-lookup"><span data-stu-id="9696c-110">If you change the calendar template, those changes don't propagate to the working hours of the project.</span></span> <span data-ttu-id="9696c-111">Per canviar les hores de feina del projecte, cal aplicar una plantilla nova.</span><span class="sxs-lookup"><span data-stu-id="9696c-111">To change the working hours of the project, a new template must be applied.</span></span>

<span data-ttu-id="9696c-112">Per crear una plantilla de calendari per a l'organització, cal tenir dos requisits clau:</span><span class="sxs-lookup"><span data-stu-id="9696c-112">To create a calendar template for your organization, there are two key requirements:</span></span>

- <span data-ttu-id="9696c-113">Definiu les hores de feina desitjades de la plantilla mitjançant un recurs que es pot reservar nou o existent.</span><span class="sxs-lookup"><span data-stu-id="9696c-113">Define the desired working hours of the template using a new or existing bookable resource.</span></span>
- <span data-ttu-id="9696c-114">Creeu una plantilla de calendari nova i associeu-la amb el recurs que es pot reservar.</span><span class="sxs-lookup"><span data-stu-id="9696c-114">Create a new calendar template and associate the template with the bookable resource.</span></span>

<span data-ttu-id="9696c-115">**Definiu les hores laborables de la plantilla**</span><span class="sxs-lookup"><span data-stu-id="9696c-115">**Define the working hours of the template**</span></span>

1. <span data-ttu-id="9696c-116">Aneu a **Recursos** \> **Recursos**.</span><span class="sxs-lookup"><span data-stu-id="9696c-116">Go to **Resources** \> **Resources**.</span></span>
2. <span data-ttu-id="9696c-117">Creeu un recurs nou al qual es fa referència a la plantilla de calendari o seleccioneu un recurs existent.</span><span class="sxs-lookup"><span data-stu-id="9696c-117">Create a new resource to reference in the calendar template, or select an existing resource.</span></span>
3. <span data-ttu-id="9696c-118">Seleccioneu la pestanya **Hores de feina** del recurs i completeu les instruccions de [Definició de les hores de feina per a un recurs](/dynamics365/field-service/set-work-hours-resource.md) per configurar les regles del calendari.</span><span class="sxs-lookup"><span data-stu-id="9696c-118">Select the **Work Hours** tab of the resource and complete the instructions in [Set work hours for a resource](/dynamics365/field-service/set-work-hours-resource.md) to configure the calendar rules.</span></span>

<span data-ttu-id="9696c-119">**Creeu una plantilla de calendari nova**</span><span class="sxs-lookup"><span data-stu-id="9696c-119">**Create a new calendar template**</span></span>

1. <span data-ttu-id="9696c-120">Aneu a **Configuració** \> **Plantilla de calendari**.</span><span class="sxs-lookup"><span data-stu-id="9696c-120">Go to **Settings** \> **Calendar Template**.</span></span>
2. <span data-ttu-id="9696c-121">Seleccioneu **Crea** i introduïu un nom, una descripció i un recurs de plantilla.</span><span class="sxs-lookup"><span data-stu-id="9696c-121">Select **New**, and enter a name, description, and template resource.</span></span>


> [!NOTE]
> <span data-ttu-id="9696c-122">Quan es fa referència a un recurs en una plantilla de calendari, s'associa una còpia del calendari del recurs amb la plantilla de calendari.</span><span class="sxs-lookup"><span data-stu-id="9696c-122">When a resource is referenced in a calendar template, a copy of the resource’s calendar is associated with the calendar template.</span></span> <span data-ttu-id="9696c-123">Si les hores laborables de la plantilla copiada canvien, els canvis no s'emplenen a la plantilla del calendari.</span><span class="sxs-lookup"><span data-stu-id="9696c-123">If the working hours of the copied template change, those changes will not propagate to the calendar template.</span></span>


### <a name="see-also"></a><span data-ttu-id="9696c-124">Vegeu també</span><span class="sxs-lookup"><span data-stu-id="9696c-124">See Also</span></span>  
 [<span data-ttu-id="9696c-125">Configuració de recursos</span><span class="sxs-lookup"><span data-stu-id="9696c-125">Set up resources</span></span>](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
