---
title: Creació d'una plantilla d'hores de feina
description: Aquesta tema descriu com crear una plantilla d'hores de treball al Project Service.
author: ruhercul
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 525f601ad6fee902cb6d5c128b596cc2d33f30c4
ms.sourcegitcommit: c45ceda833b30ad39861f5bcd3ba1bbfff11fe7a
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/04/2021
ms.locfileid: "5981243"
---
# <a name="create-a-work-hours-template-project-service"></a><span data-ttu-id="42085-103">Crear una plantilla d'hores de treball (Project Service)</span><span class="sxs-lookup"><span data-stu-id="42085-103">Create a work hours template (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="42085-104">Per crear i administrar un projecte, heu d'aplicar una plantilla de calendari al projecte.</span><span class="sxs-lookup"><span data-stu-id="42085-104">To create and manage a project, you must apply a calendar template to the project.</span></span> <span data-ttu-id="42085-105">La plantilla de calendari defineix els atributs de projecte següents:</span><span class="sxs-lookup"><span data-stu-id="42085-105">The calendar template defines the following project attributes:</span></span>

- <span data-ttu-id="42085-106">Hores de feina, incloent-hi l'hora d'inici i d'acabament</span><span class="sxs-lookup"><span data-stu-id="42085-106">Working hours, including start and end time</span></span>
- <span data-ttu-id="42085-107">Dies feiners</span><span class="sxs-lookup"><span data-stu-id="42085-107">Working days</span></span>
- <span data-ttu-id="42085-108">Excepcions del calendari, com ara dies que no són feiners</span><span class="sxs-lookup"><span data-stu-id="42085-108">Calendar exceptions such as non-working days</span></span>

<span data-ttu-id="42085-109">La plantilla de calendari que s'aplica a un projecte és una còpia de la plantilla de calendari definida a la configuració de l'organització.</span><span class="sxs-lookup"><span data-stu-id="42085-109">The calendar template that's applied to a project is a copy of the calendar template defined in your organization’s settings.</span></span>

> [!NOTE]
> <span data-ttu-id="42085-110">Si canvieu la plantilla de calendari, els canvis no s'emplenen a les hores de feina del projecte.</span><span class="sxs-lookup"><span data-stu-id="42085-110">If you change the calendar template, those changes don't propagate to the working hours of the project.</span></span> <span data-ttu-id="42085-111">Per canviar les hores de feina del projecte, cal aplicar una plantilla nova.</span><span class="sxs-lookup"><span data-stu-id="42085-111">To change the working hours of the project, a new template must be applied.</span></span>

<span data-ttu-id="42085-112">Per crear una plantilla de calendari per a l'organització, cal tenir dos requisits clau:</span><span class="sxs-lookup"><span data-stu-id="42085-112">To create a calendar template for your organization, there are two key requirements:</span></span>

- <span data-ttu-id="42085-113">Definiu les hores de feina desitjades de la plantilla mitjançant un recurs que es pot reservar nou o existent.</span><span class="sxs-lookup"><span data-stu-id="42085-113">Define the desired working hours of the template using a new or existing bookable resource.</span></span>
- <span data-ttu-id="42085-114">Creeu una plantilla de calendari nova i associeu-la amb el recurs que es pot reservar.</span><span class="sxs-lookup"><span data-stu-id="42085-114">Create a new calendar template and associate the template with the bookable resource.</span></span>

<span data-ttu-id="42085-115">**Definiu les hores laborables de la plantilla**</span><span class="sxs-lookup"><span data-stu-id="42085-115">**Define the working hours of the template**</span></span>

1. <span data-ttu-id="42085-116">Aneu a **Recursos** \> **Recursos**.</span><span class="sxs-lookup"><span data-stu-id="42085-116">Go to **Resources** \> **Resources**.</span></span>
2. <span data-ttu-id="42085-117">Creeu un recurs nou al qual es fa referència a la plantilla de calendari o seleccioneu un recurs existent.</span><span class="sxs-lookup"><span data-stu-id="42085-117">Create a new resource to reference in the calendar template, or select an existing resource.</span></span>
3. <span data-ttu-id="42085-118">Seleccioneu la pestanya **Hores de feina** del recurs i completeu les instruccions de [Definició de les hores de feina per a un recurs](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource) per configurar les regles del calendari.</span><span class="sxs-lookup"><span data-stu-id="42085-118">Select the **Work Hours** tab of the resource and complete the instructions in [Set work hours for a resource](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource) to configure the calendar rules.</span></span>

<span data-ttu-id="42085-119">**Creeu una plantilla de calendari nova**</span><span class="sxs-lookup"><span data-stu-id="42085-119">**Create a new calendar template**</span></span>

1. <span data-ttu-id="42085-120">Aneu a **Configuració** \> **Plantilla de calendari**.</span><span class="sxs-lookup"><span data-stu-id="42085-120">Go to **Settings** \> **Calendar Template**.</span></span>
2. <span data-ttu-id="42085-121">Seleccioneu **Crea** i introduïu un nom, una descripció i un recurs de plantilla.</span><span class="sxs-lookup"><span data-stu-id="42085-121">Select **New**, and enter a name, description, and template resource.</span></span>


> [!NOTE]
> <span data-ttu-id="42085-122">Quan es fa referència a un recurs en una plantilla de calendari, s'associa una còpia del calendari del recurs amb la plantilla de calendari.</span><span class="sxs-lookup"><span data-stu-id="42085-122">When a resource is referenced in a calendar template, a copy of the resource’s calendar is associated with the calendar template.</span></span> <span data-ttu-id="42085-123">Si les hores laborables de la plantilla copiada canvien, els canvis no s'emplenen a la plantilla del calendari.</span><span class="sxs-lookup"><span data-stu-id="42085-123">If the working hours of the copied template change, those changes will not propagate to the calendar template.</span></span>


### <a name="see-also"></a><span data-ttu-id="42085-124">Vegeu també</span><span class="sxs-lookup"><span data-stu-id="42085-124">See Also</span></span>  
 [<span data-ttu-id="42085-125">Configuració de recursos</span><span class="sxs-lookup"><span data-stu-id="42085-125">Set up resources</span></span>](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
