---
title: Definició dels calendaris del projecte
description: En aquest tema es proporciona informació sobre com aplicar una plantilla de calendari a un projecte per fer el seguiment de la planificació del projecte.
author: ruhercul
manager: AnnBe
ms.date: 02/05/2021
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
ms.openlocfilehash: 1d5642d7a2246dc878b2bc4f504f138b71d29a69
ms.sourcegitcommit: c45ceda833b30ad39861f5bcd3ba1bbfff11fe7a
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/04/2021
ms.locfileid: "5981288"
---
# <a name="define-project-calendars"></a><span data-ttu-id="384fb-103">Definició dels calendaris del projecte</span><span class="sxs-lookup"><span data-stu-id="384fb-103">Define project calendars</span></span>

<span data-ttu-id="384fb-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_</span><span class="sxs-lookup"><span data-stu-id="384fb-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="384fb-105">Per crear i administrar un projecte, heu d'aplicar una plantilla de calendari al projecte.</span><span class="sxs-lookup"><span data-stu-id="384fb-105">To create and manage a project, you must apply a calendar template to the project.</span></span> <span data-ttu-id="384fb-106">La plantilla de calendari defineix els atributs de projecte següents:</span><span class="sxs-lookup"><span data-stu-id="384fb-106">The calendar template defines the following project attributes:</span></span>

- <span data-ttu-id="384fb-107">Hores de feina, incloent-hi l'hora d'inici i d'acabament</span><span class="sxs-lookup"><span data-stu-id="384fb-107">Working hours, including start and end time</span></span>
- <span data-ttu-id="384fb-108">Dies feiners</span><span class="sxs-lookup"><span data-stu-id="384fb-108">Working days</span></span>
- <span data-ttu-id="384fb-109">Excepcions del calendari, com ara dies que no són feiners</span><span class="sxs-lookup"><span data-stu-id="384fb-109">Calendar exceptions such as non-working days</span></span>

<span data-ttu-id="384fb-110">La plantilla de calendari que s'aplica a un projecte és una còpia de la plantilla de calendari definida a la configuració de l'organització.</span><span class="sxs-lookup"><span data-stu-id="384fb-110">The calendar template that's applied to a project is a copy of the calendar template defined in your organization’s settings.</span></span>

> [!NOTE]
> <span data-ttu-id="384fb-111">Si canvieu la plantilla de calendari, els canvis no s'emplenen a les hores de feina del projecte.</span><span class="sxs-lookup"><span data-stu-id="384fb-111">If you change the calendar template, those changes don't propagate to the working hours of the project.</span></span> <span data-ttu-id="384fb-112">Per canviar les hores de feina del projecte, cal aplicar una plantilla nova.</span><span class="sxs-lookup"><span data-stu-id="384fb-112">To change the working hours of the project, a new template must be applied.</span></span>

<span data-ttu-id="384fb-113">Per crear una plantilla de calendari per a l'organització, cal tenir dos requisits clau:</span><span class="sxs-lookup"><span data-stu-id="384fb-113">To create a calendar template for your organization, there are two key requirements:</span></span>

- <span data-ttu-id="384fb-114">Definiu les hores de feina desitjades de la plantilla mitjançant un recurs que es pot reservar nou o existent.</span><span class="sxs-lookup"><span data-stu-id="384fb-114">Define the desired working hours of the template using a new or existing bookable resource.</span></span>
- <span data-ttu-id="384fb-115">Creeu una plantilla de calendari nova i associeu-la amb el recurs que es pot reservar.</span><span class="sxs-lookup"><span data-stu-id="384fb-115">Create a new calendar template and associate the template with the bookable resource.</span></span>

<span data-ttu-id="384fb-116">**Definiu les hores laborables de la plantilla**</span><span class="sxs-lookup"><span data-stu-id="384fb-116">**Define the working hours of the template**</span></span>

1. <span data-ttu-id="384fb-117">Aneu a **Recursos** \> **Recursos**.</span><span class="sxs-lookup"><span data-stu-id="384fb-117">Go to **Resources** \> **Resources**.</span></span>
2. <span data-ttu-id="384fb-118">Creeu un recurs nou al qual es fa referència a la plantilla de calendari o seleccioneu un recurs existent.</span><span class="sxs-lookup"><span data-stu-id="384fb-118">Create a new resource to reference in the calendar template, or select an existing resource.</span></span>
3. <span data-ttu-id="384fb-119">Seleccioneu la pestanya **Hores de feina** del recurs i completeu les instruccions de [Definició de les hores de feina per a un recurs](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource) per configurar les regles del calendari.</span><span class="sxs-lookup"><span data-stu-id="384fb-119">Select the **Work Hours** tab of the resource and complete the instructions in [Set work hours for a resource](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource) to configure the calendar rules.</span></span>

<span data-ttu-id="384fb-120">**Creeu una plantilla de calendari nova**</span><span class="sxs-lookup"><span data-stu-id="384fb-120">**Create a new calendar template**</span></span>

1. <span data-ttu-id="384fb-121">Aneu a **Configuració** \> **Plantilla de calendari**.</span><span class="sxs-lookup"><span data-stu-id="384fb-121">Go to **Settings** \> **Calendar Template**.</span></span>
2. <span data-ttu-id="384fb-122">Seleccioneu **Crea** i introduïu un nom, una descripció i un recurs de plantilla.</span><span class="sxs-lookup"><span data-stu-id="384fb-122">Select **New**, and enter a name, description, and template resource.</span></span>

> [!NOTE]
> <span data-ttu-id="384fb-123">Quan es fa referència a un recurs en una plantilla de calendari, s'associa una còpia del calendari del recurs amb la plantilla de calendari.</span><span class="sxs-lookup"><span data-stu-id="384fb-123">When a resource is referenced in a calendar template, a copy of the resource’s calendar is associated with the calendar template.</span></span> <span data-ttu-id="384fb-124">Si les hores laborables de la plantilla copiada canvien, els canvis no s'emplenen a la plantilla del calendari.</span><span class="sxs-lookup"><span data-stu-id="384fb-124">If the working hours of the copied template change, those changes will not propagate to the calendar template.</span></span>

<span data-ttu-id="384fb-125">Ara podeu associar la plantilla de treball amb una plantilla de calendari de projectes.</span><span class="sxs-lookup"><span data-stu-id="384fb-125">You can now associate the work template with a project calendar template.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]

