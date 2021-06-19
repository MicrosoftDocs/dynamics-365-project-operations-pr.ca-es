---
title: Informació general sobre l'ajudant de planificació
description: En aquest tema es proporciona informació sobre com treballar amb l'ajudant de planificació per reservar recursos.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 4d58f5f45ca54691b6e736dee5aab7b273a8e042
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014104"
---
# <a name="schedule-assistant-overview"></a><span data-ttu-id="058e8-103">Informació general sobre l'ajudant de planificació</span><span class="sxs-lookup"><span data-stu-id="058e8-103">Schedule assistant overview</span></span>

<span data-ttu-id="058e8-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_</span><span class="sxs-lookup"><span data-stu-id="058e8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="058e8-105">L'auxiliar de planificació s'utilitza per reservar recursos en funció dels requisits definits per l'administrador del projecte.</span><span class="sxs-lookup"><span data-stu-id="058e8-105">The Schedule assistant is used to book resources based on requirements defined by the Project manager.</span></span> <span data-ttu-id="058e8-106">L'auxiliar de planificació es basa en els paràmetres proporcionats al requisit de recurs per cercar el recurs.</span><span class="sxs-lookup"><span data-stu-id="058e8-106">The schedule assistant relies on the parameters provided in the resource requirement to find the resource.</span></span> <span data-ttu-id="058e8-107">L'auxiliar de planificació recomana recursos que coincideixen amb els requisits pertinents, com ara franges temporals o coneixements necessaris.</span><span class="sxs-lookup"><span data-stu-id="058e8-107">The Schedule assistant recommends resources that match relevant requirements, like time windows or skills needed.</span></span>

<span data-ttu-id="058e8-108">Un cop identificats els recursos adients, l'administrador de recursos o del projecte poden reservar el recurs al treball.</span><span class="sxs-lookup"><span data-stu-id="058e8-108">After suitable resources are identified, the Resource or Project manager can book the resource to the work.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="058e8-109">Requisits previs</span><span class="sxs-lookup"><span data-stu-id="058e8-109">Prerequisites</span></span>

<span data-ttu-id="058e8-110">L'auxiliar de planificació forma part de la solució Universal Resource Scheduling.</span><span class="sxs-lookup"><span data-stu-id="058e8-110">The Schedule assistant is a part of the Universal Resource Scheduling solution.</span></span> <span data-ttu-id="058e8-111">Aquesta solució s'inclou i s'instal·la amb el Dynamics 365 Project Operations, el Dynamics 365 Field Service i el Dynamics 365 Customer Service.</span><span class="sxs-lookup"><span data-stu-id="058e8-111">This solution is included and installed with Dynamics 365 Project Operations, Dynamics 365 Field Service, and Dynamics 365 Customer Service.</span></span>

## <a name="matching-requirements-and-resources"></a><span data-ttu-id="058e8-112">Assignació de requisits i recursos</span><span class="sxs-lookup"><span data-stu-id="058e8-112">Matching requirements and resources</span></span>

<span data-ttu-id="058e8-113">Un requisit de recurs generat es basa en detalls com:</span><span class="sxs-lookup"><span data-stu-id="058e8-113">A generated resource requirement is based on details such as:</span></span>

-   <span data-ttu-id="058e8-114">Característiques</span><span class="sxs-lookup"><span data-stu-id="058e8-114">Characteristics</span></span>
-   <span data-ttu-id="058e8-115">Funcions</span><span class="sxs-lookup"><span data-stu-id="058e8-115">Roles</span></span>
-   <span data-ttu-id="058e8-116">Unitats de negoci</span><span class="sxs-lookup"><span data-stu-id="058e8-116">Business units</span></span>
-   <span data-ttu-id="058e8-117">Preferències de recursos</span><span class="sxs-lookup"><span data-stu-id="058e8-117">Resource preferences</span></span>
-   <span data-ttu-id="058e8-118">Contorns d'esforç</span><span class="sxs-lookup"><span data-stu-id="058e8-118">Effort contours</span></span>
-   <span data-ttu-id="058e8-119">Fus horari</span><span class="sxs-lookup"><span data-stu-id="058e8-119">Time zone</span></span>

<span data-ttu-id="058e8-120">L'auxiliar de planificació utilitza aquests detalls per filtrar els recursos.</span><span class="sxs-lookup"><span data-stu-id="058e8-120">The Schedule assistant uses these details to filter resources.</span></span>

## <a name="launch-the-schedule-assistant"></a><span data-ttu-id="058e8-121">Iniciar l'auxiliar de planificació</span><span class="sxs-lookup"><span data-stu-id="058e8-121">Launch the Schedule assistant</span></span>

<span data-ttu-id="058e8-122">Hi ha dues maneres d'iniciar l'auxiliar de planificació.</span><span class="sxs-lookup"><span data-stu-id="058e8-122">There are two ways in which the schedule assistant is launched.</span></span> <span data-ttu-id="058e8-123">Si utilitzeu el mode híbrid, a la quadrícula de membres de l'equip podeu seleccionar qualsevol membre de l'equip amb un requisit de recurs no complert i, a continuació, seleccionar **Reserva**.</span><span class="sxs-lookup"><span data-stu-id="058e8-123">If you're using the hybrid mode, in the team member grid you can select any team member with an unfulfilled resource requirement, and then select **Book**.</span></span> <span data-ttu-id="058e8-124">Si utilitzeu el mode central, l'administrador de recursos cerca i selecciona el recurs.</span><span class="sxs-lookup"><span data-stu-id="058e8-124">If you're using the central mode, the Resource manager finds and selects the resource.</span></span>

## <a name="schedule-assistant-filters"></a><span data-ttu-id="058e8-125">Filtres de l'Auxiliar de planificació</span><span class="sxs-lookup"><span data-stu-id="058e8-125">Schedule assistant filters</span></span>

<span data-ttu-id="058e8-126">Després d'executar l'auxiliar de planificació, els detalls del requisit del recurs es mostren com a valors filtrats a la subfinestra esquerra.</span><span class="sxs-lookup"><span data-stu-id="058e8-126">After the Schedule assistant runs, the details from the resource requirement are displayed as filtered values in the left pane.</span></span> <span data-ttu-id="058e8-127">L'administrador de recursos o l'administrador de projectes poden afinar els resultats ajustant els filtres per complir les necessitats de planificació.</span><span class="sxs-lookup"><span data-stu-id="058e8-127">The Resource manager or the Project manager can fine-tune results by adjusting filters to meet the scheduling needs.</span></span>

<span data-ttu-id="058e8-128">A la subfinestra de filtratge es mostren les opcions relacionades amb el treball, incloent-hi:</span><span class="sxs-lookup"><span data-stu-id="058e8-128">The filter pane shows work-related options, including:</span></span>

-   <span data-ttu-id="058e8-129">Inici i acabament del treball</span><span class="sxs-lookup"><span data-stu-id="058e8-129">Work start and end</span></span>
-   <span data-ttu-id="058e8-130">Característiques</span><span class="sxs-lookup"><span data-stu-id="058e8-130">Characteristics</span></span>
-   <span data-ttu-id="058e8-131">Funcions</span><span class="sxs-lookup"><span data-stu-id="058e8-131">Roles</span></span>
-   <span data-ttu-id="058e8-132">Unitats organitzatives</span><span class="sxs-lookup"><span data-stu-id="058e8-132">Organizational units</span></span>
-   <span data-ttu-id="058e8-133">Empresa de dotació de recursos</span><span class="sxs-lookup"><span data-stu-id="058e8-133">Resourcing company</span></span>
-   <span data-ttu-id="058e8-134">Tipus de recursos</span><span class="sxs-lookup"><span data-stu-id="058e8-134">Resource types</span></span>
-   <span data-ttu-id="058e8-135">Recursos preferits</span><span class="sxs-lookup"><span data-stu-id="058e8-135">Preferred resources</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]