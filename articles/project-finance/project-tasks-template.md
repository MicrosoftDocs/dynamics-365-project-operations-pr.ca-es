---
title: Sincronitzar tasques del projecte directament des del Project Service Automation al Finance and Operations
description: Aquest tema descriu la plantilla i tasca subjacents que s'utilitzen per sincronitzar les tasques del projecte directament des del Microsoft Dynamics 365 Project Service Automation al Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: d7f32327-33c4-43ab-b799-786210e93277
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 66a255346727c7ee4fbbf2920d2ef437ded03308
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749559"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="ce94f-103">Sincronitzar tasques del projecte directament des del Project Service Automation al Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ce94f-103">Synchronize project tasks directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="ce94f-104">Aquest tema descriu la plantilla i tasca subjacents que s'utilitzen per sincronitzar les tasques del projecte directament des del Dynamics 365 Project Service Automation al Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="ce94f-104">This topic describes the template and underlying task that are used to synchronize project tasks directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="ce94f-105">La integració de tasques de projecte, les categories de transaccions de despeses, les estimacions d'hores, les estimacions de despeses i el bloqueig de funcionalitats estan disponibles a la versió 8.0.</span><span class="sxs-lookup"><span data-stu-id="ce94f-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="ce94f-106">Si utilitzeu l'Enterprise Edition 7.3.0 després d'instal·lar el KB 4132657 i el KB 4132660, podreu utilitzar les plantilles per integrar tasques de projecte, categories de transaccions de despeses, estimacions d'hores, estimacions de despeses i valors reals i configurar el bloqueig de funcionalitats.</span><span class="sxs-lookup"><span data-stu-id="ce94f-106">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="ce94f-107">Si heu de reiniciar la distribució comptable, us recomanem que també instal·leu el KB 4131710.</span><span class="sxs-lookup"><span data-stu-id="ce94f-107">If you must reset the accounting distributions, we recommended that you also install KB 4131710.</span></span>
> - <span data-ttu-id="ce94f-108">La integració dels valors reals del projecte està disponible a la versió 8.0.1 i posteriors.</span><span class="sxs-lookup"><span data-stu-id="ce94f-108">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="ce94f-109">Flux de dades del Project Service Automation al Finance</span><span class="sxs-lookup"><span data-stu-id="ce94f-109">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="ce94f-110">La solució d'integració del Project Service Automation al Finance utilitza la característica d'integració de dades per sincronitzar dades entre les instàncies del Project Service Automation i el Finance.</span><span class="sxs-lookup"><span data-stu-id="ce94f-110">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="ce94f-111">La plantilla d'integració que està disponible amb la característica d'integració de dades permet el flux de dades sobre tasques del projecte del Project Service Automation al Finance.</span><span class="sxs-lookup"><span data-stu-id="ce94f-111">The integration template that is available with the Data integration feature enables the flow of data about project tasks from Project Service Automation to Finance.</span></span>

<span data-ttu-id="ce94f-112">A la il·lustració següent es mostren les dades que se sincronitzen entre el Project Service Automation i el Finance.</span><span class="sxs-lookup"><span data-stu-id="ce94f-112">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="ce94f-113">[![Flux de dades per a la integració de Project Service Automation amb el Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span><span class="sxs-lookup"><span data-stu-id="ce94f-113">[![Data flow for Project Service Automation integration with Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span></span>

## <a name="template-and-task"></a><span data-ttu-id="ce94f-114">Plantilla i tasca</span><span class="sxs-lookup"><span data-stu-id="ce94f-114">Template and task</span></span>

<span data-ttu-id="ce94f-115">Per accedir a la plantilla, al centre d'administració del Microsoft Power Apps, seleccioneu **Projectes** i, a continuació, a la cantonada superior dreta, seleccioneu **Nou projecte** per seleccionar les plantilles públiques.</span><span class="sxs-lookup"><span data-stu-id="ce94f-115">To access the template, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="ce94f-116">La plantilla i la tasca subjacents següents s'utilitzen per sincronitzar les plantilles del projecte del Project Service Automation al Finance:</span><span class="sxs-lookup"><span data-stu-id="ce94f-116">The following template and underlying task are used to synchronize project tasks from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="ce94f-117">**Nom de la plantilla en la integració de dades**: tasques del projecte (PSA a Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="ce94f-117">**Name of the template in Data integration:** Project tasks (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="ce94f-118">**Nom de la tasca del projecte:** tasques del projecte</span><span class="sxs-lookup"><span data-stu-id="ce94f-118">**Name of the task in the project:** Project tasks</span></span>

<span data-ttu-id="ce94f-119">Abans que es produeixi la sincronització de tasques del projecte, cal sincronitzar els contractes del projecte i els projectes.</span><span class="sxs-lookup"><span data-stu-id="ce94f-119">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="entity-set"></a><span data-ttu-id="ce94f-120">Conjunt d'entitats</span><span class="sxs-lookup"><span data-stu-id="ce94f-120">Entity set</span></span>

| <span data-ttu-id="ce94f-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="ce94f-121">Project Service Automation</span></span> | <span data-ttu-id="ce94f-122">Finance</span><span class="sxs-lookup"><span data-stu-id="ce94f-122">Finance</span></span>                             |
|----------------------------|-------------------------------------|
| <span data-ttu-id="ce94f-123">Tasques del projecte</span><span class="sxs-lookup"><span data-stu-id="ce94f-123">Project Tasks</span></span>              | <span data-ttu-id="ce94f-124">Entitat d'integració per a la tasca del projecte</span><span class="sxs-lookup"><span data-stu-id="ce94f-124">Integration entity for project task</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="ce94f-125">Flux d'entitat</span><span class="sxs-lookup"><span data-stu-id="ce94f-125">Entity flow</span></span>

<span data-ttu-id="ce94f-126">Les tasques del projecte estan administrades al Project Service Automation i se sincronitzen amb el Finance com a activitats del projecte.</span><span class="sxs-lookup"><span data-stu-id="ce94f-126">Project tasks are managed in Project Service Automation, and they are synchronized to Finance as project activities.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="ce94f-127">Requisits previs i configuració de l'assignació</span><span class="sxs-lookup"><span data-stu-id="ce94f-127">Prerequisites and mapping setup</span></span>

<span data-ttu-id="ce94f-128">Abans que es produeixi la sincronització de tasques del projecte, cal sincronitzar els contractes del projecte i els projectes.</span><span class="sxs-lookup"><span data-stu-id="ce94f-128">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="power-query"></a><span data-ttu-id="ce94f-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="ce94f-129">Power Query</span></span>

<span data-ttu-id="ce94f-130">Heu d'utilitzar el Microsoft Power Query per a l'Excel per filtrar les dades si es compleix aquesta condició:</span><span class="sxs-lookup"><span data-stu-id="ce94f-130">You must use Microsoft Power Query for Excel to filter data if this condition is met:</span></span>

- <span data-ttu-id="ce94f-131">Teniu registres específics de recurs en una tasca del projecte.</span><span class="sxs-lookup"><span data-stu-id="ce94f-131">You have resource-specific records in a project task.</span></span>

<span data-ttu-id="ce94f-132">Si heu d'utilitzar el Power Query, seguiu aquesta instrucció:</span><span class="sxs-lookup"><span data-stu-id="ce94f-132">If you must use Power Query, follow this guideline:</span></span>

- <span data-ttu-id="ce94f-133">La plantilla Tasques del projecte (PSA a Fin and Ops) té un filtre per defecte que exclou els registres específics d'un recurs d'una tasca del projecte establint el filtre a **IsLineTask** com a **False**.</span><span class="sxs-lookup"><span data-stu-id="ce94f-133">The Project tasks (PSA to Fin and Ops) template has a default filter that excludes resource-specific records from a project task by setting the filter on **IsLineTask** to **False**.</span></span> <span data-ttu-id="ce94f-134">Si creeu una plantilla pròpia, heu d'afegir aquest filtre.</span><span class="sxs-lookup"><span data-stu-id="ce94f-134">If you create your own template, you must add this filter.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="ce94f-135">Assignació de plantilles a la integració de dades</span><span class="sxs-lookup"><span data-stu-id="ce94f-135">Template mapping in Data integration</span></span>

<span data-ttu-id="ce94f-136">A la il·lustració següent es mostra un exemple de les assignacions de tasques de plantilla a la integració de dades.</span><span class="sxs-lookup"><span data-stu-id="ce94f-136">The following illustration shows an example of the template task mappings in Data integration.</span></span> <span data-ttu-id="ce94f-137">L'assignació mostra la informació de camp que se sincronitzarà del Project Service Automation al Finance.</span><span class="sxs-lookup"><span data-stu-id="ce94f-137">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="ce94f-138">[![Assignació de plantilla](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span><span class="sxs-lookup"><span data-stu-id="ce94f-138">[![Template mapping](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span></span>
