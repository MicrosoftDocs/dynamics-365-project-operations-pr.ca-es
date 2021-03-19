---
title: Sincronitzar tasques del projecte directament des del Project Service Automation al Finance and Operations
description: Aquest tema descriu la plantilla i tasca subjacents que s'utilitzen per sincronitzar les tasques del projecte directament des del Microsoft Dynamics 365 Project Service Automation al Dynamics 365 Finance.
author: Yowelle
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
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 7cc9ee9de576549c132e14c333a1000c22a55236
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288907"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="e1e07-103">Sincronitzar tasques del projecte directament des del Project Service Automation al Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e1e07-103">Synchronize project tasks directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="e1e07-104">Aquest tema descriu la plantilla i tasca subjacents que s'utilitzen per sincronitzar les tasques del projecte directament des del Dynamics 365 Project Service Automation al Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="e1e07-104">This topic describes the template and underlying task that are used to synchronize project tasks directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="e1e07-105">La integració de tasques de projecte, les categories de transaccions de despeses, les estimacions d'hores, les estimacions de despeses i el bloqueig de funcionalitats estan disponibles a la versió 8.0.</span><span class="sxs-lookup"><span data-stu-id="e1e07-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="e1e07-106">Si utilitzeu l'Enterprise Edition 7.3.0 després d'instal·lar el KB 4132657 i el KB 4132660, podreu utilitzar les plantilles per integrar tasques de projecte, categories de transaccions de despeses, estimacions d'hores, estimacions de despeses i valors reals i configurar el bloqueig de funcionalitats.</span><span class="sxs-lookup"><span data-stu-id="e1e07-106">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="e1e07-107">Si heu de reiniciar la distribució comptable, us recomanem que també instal·leu el KB 4131710.</span><span class="sxs-lookup"><span data-stu-id="e1e07-107">If you must reset the accounting distributions, we recommended that you also install KB 4131710.</span></span>
> - <span data-ttu-id="e1e07-108">La integració dels valors reals del projecte està disponible a la versió 8.0.1 i posteriors.</span><span class="sxs-lookup"><span data-stu-id="e1e07-108">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="e1e07-109">Flux de dades del Project Service Automation al Finance</span><span class="sxs-lookup"><span data-stu-id="e1e07-109">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="e1e07-110">La solució d'integració del Project Service Automation al Finance utilitza la característica d'integració de dades per sincronitzar dades entre les instàncies del Project Service Automation i el Finance.</span><span class="sxs-lookup"><span data-stu-id="e1e07-110">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="e1e07-111">La plantilla d'integració que està disponible amb la característica d'integració de dades permet el flux de dades sobre tasques del projecte del Project Service Automation al Finance.</span><span class="sxs-lookup"><span data-stu-id="e1e07-111">The integration template that is available with the Data integration feature enables the flow of data about project tasks from Project Service Automation to Finance.</span></span>

<span data-ttu-id="e1e07-112">A la il·lustració següent es mostren les dades que se sincronitzen entre el Project Service Automation i el Finance.</span><span class="sxs-lookup"><span data-stu-id="e1e07-112">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="e1e07-113">[![Flux de dades per a la integració de Project Service Automation amb el Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span><span class="sxs-lookup"><span data-stu-id="e1e07-113">[![Data flow for Project Service Automation integration with Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span></span>

## <a name="template-and-task"></a><span data-ttu-id="e1e07-114">Plantilla i tasca</span><span class="sxs-lookup"><span data-stu-id="e1e07-114">Template and task</span></span>

<span data-ttu-id="e1e07-115">Per accedir a la plantilla, al centre d'administració del Microsoft Power Apps, seleccioneu **Projectes** i, a continuació, a la cantonada superior dreta, seleccioneu **Nou projecte** per seleccionar les plantilles públiques.</span><span class="sxs-lookup"><span data-stu-id="e1e07-115">To access the template, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="e1e07-116">La plantilla i la tasca subjacents següents s'utilitzen per sincronitzar les plantilles del projecte del Project Service Automation al Finance:</span><span class="sxs-lookup"><span data-stu-id="e1e07-116">The following template and underlying task are used to synchronize project tasks from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="e1e07-117">**Nom de la plantilla en la integració de dades**: tasques del projecte (PSA a Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="e1e07-117">**Name of the template in Data integration:** Project tasks (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="e1e07-118">**Nom de la tasca del projecte:** tasques del projecte</span><span class="sxs-lookup"><span data-stu-id="e1e07-118">**Name of the task in the project:** Project tasks</span></span>

<span data-ttu-id="e1e07-119">Abans que es produeixi la sincronització de tasques del projecte, cal sincronitzar els contractes del projecte i els projectes.</span><span class="sxs-lookup"><span data-stu-id="e1e07-119">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="entity-set"></a><span data-ttu-id="e1e07-120">Conjunt d'entitats</span><span class="sxs-lookup"><span data-stu-id="e1e07-120">Entity set</span></span>

| <span data-ttu-id="e1e07-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="e1e07-121">Project Service Automation</span></span> | <span data-ttu-id="e1e07-122">Finance</span><span class="sxs-lookup"><span data-stu-id="e1e07-122">Finance</span></span>                             |
|----------------------------|-------------------------------------|
| <span data-ttu-id="e1e07-123">Tasques del projecte</span><span class="sxs-lookup"><span data-stu-id="e1e07-123">Project Tasks</span></span>              | <span data-ttu-id="e1e07-124">Entitat d'integració per a la tasca del projecte</span><span class="sxs-lookup"><span data-stu-id="e1e07-124">Integration entity for project task</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="e1e07-125">Flux d'entitat</span><span class="sxs-lookup"><span data-stu-id="e1e07-125">Entity flow</span></span>

<span data-ttu-id="e1e07-126">Les tasques del projecte estan administrades al Project Service Automation i se sincronitzen amb el Finance com a activitats del projecte.</span><span class="sxs-lookup"><span data-stu-id="e1e07-126">Project tasks are managed in Project Service Automation, and they are synchronized to Finance as project activities.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="e1e07-127">Requisits previs i configuració de l'assignació</span><span class="sxs-lookup"><span data-stu-id="e1e07-127">Prerequisites and mapping setup</span></span>

<span data-ttu-id="e1e07-128">Abans que es produeixi la sincronització de tasques del projecte, cal sincronitzar els contractes del projecte i els projectes.</span><span class="sxs-lookup"><span data-stu-id="e1e07-128">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="power-query"></a><span data-ttu-id="e1e07-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="e1e07-129">Power Query</span></span>

<span data-ttu-id="e1e07-130">Heu d'utilitzar el Microsoft Power Query per a l'Excel per filtrar les dades si es compleix aquesta condició:</span><span class="sxs-lookup"><span data-stu-id="e1e07-130">You must use Microsoft Power Query for Excel to filter data if this condition is met:</span></span>

- <span data-ttu-id="e1e07-131">Teniu registres específics de recurs en una tasca del projecte.</span><span class="sxs-lookup"><span data-stu-id="e1e07-131">You have resource-specific records in a project task.</span></span>

<span data-ttu-id="e1e07-132">Si heu d'utilitzar el Power Query, seguiu aquesta instrucció:</span><span class="sxs-lookup"><span data-stu-id="e1e07-132">If you must use Power Query, follow this guideline:</span></span>

- <span data-ttu-id="e1e07-133">La plantilla Tasques del projecte (PSA a Fin and Ops) té un filtre per defecte que exclou els registres específics d'un recurs d'una tasca del projecte establint el filtre a **IsLineTask** com a **False**.</span><span class="sxs-lookup"><span data-stu-id="e1e07-133">The Project tasks (PSA to Fin and Ops) template has a default filter that excludes resource-specific records from a project task by setting the filter on **IsLineTask** to **False**.</span></span> <span data-ttu-id="e1e07-134">Si creeu una plantilla pròpia, heu d'afegir aquest filtre.</span><span class="sxs-lookup"><span data-stu-id="e1e07-134">If you create your own template, you must add this filter.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="e1e07-135">Assignació de plantilles a la integració de dades</span><span class="sxs-lookup"><span data-stu-id="e1e07-135">Template mapping in Data integration</span></span>

<span data-ttu-id="e1e07-136">A la il·lustració següent es mostra un exemple de les assignacions de tasques de plantilla a la integració de dades.</span><span class="sxs-lookup"><span data-stu-id="e1e07-136">The following illustration shows an example of the template task mappings in Data integration.</span></span> <span data-ttu-id="e1e07-137">L'assignació mostra la informació de camp que se sincronitzarà del Project Service Automation al Finance.</span><span class="sxs-lookup"><span data-stu-id="e1e07-137">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="e1e07-138">[![Assignació de plantilla](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span><span class="sxs-lookup"><span data-stu-id="e1e07-138">[![Template mapping](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]