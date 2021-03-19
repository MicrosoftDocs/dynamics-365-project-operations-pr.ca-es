---
title: Informació general del Project Service Automation
description: En aquest tema es proporciona informació sobre la solució d'integració del Dynamics 365 Project Service Automation al Dynamics 365 Finance.
author: ruhercul
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: ruhercul
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: ruhercul
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 41d2eace497f4291022da0775cca7cda7d600df7
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271071"
---
# <a name="project-service-automation-overview"></a><span data-ttu-id="7bfe6-103">Informació general del Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="7bfe6-103">Project Service Automation overview</span></span>

[!include[banner](../includes/banner.md)]
[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="7bfe6-104">La solució d'integració del Project Service Automation al Finance utilitza la característica d'integració de dades per sincronitzar dades entre les instàncies del Dynamics 365 Finance i el Dynamics 365 Project Service Automation a través del Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="7bfe6-104">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Dynamics 365 Finance and Dynamics 365 Project Service Automation via Common Data Service.</span></span> <span data-ttu-id="7bfe6-105">Les plantilles d'integració que estan disponible amb la característica d'integració de dades permeten el flux de projectes, contractes de projecte, línies de contracte de projecte, fites de les línies de contracte del projecte, tasques del projecte, categories de transacció de despeses, estimacions d'hores i estimacions de despeses del Project Service Automation al Finance.</span><span class="sxs-lookup"><span data-stu-id="7bfe6-105">The integration templates that are available with the Data integration feature enable the flow of projects, project contracts, project contract lines, project contract line milestones, project tasks, expense transaction categories, hour estimates, and expense estimates from Project Service Automation to Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="7bfe6-106">Si utilitzeu la versió 7.3.0, heu d'instal·lar el KB 4074835.</span><span class="sxs-lookup"><span data-stu-id="7bfe6-106">If you're using version 7.3.0, you must install KB 4074835.</span></span> <span data-ttu-id="7bfe6-107">Podreu integrar projectes de preu fix.</span><span class="sxs-lookup"><span data-stu-id="7bfe6-107">You will then be able to integrate fixed price projects.</span></span>
> - <span data-ttu-id="7bfe6-108">Si utilitzeu la versió 7.3.0 i incorporeu transaccions de taxes del Project Service Automation, heu d'instal·lar el KB 4345320 per tal d'incloure aquestes taxes a la factura del projecte.</span><span class="sxs-lookup"><span data-stu-id="7bfe6-108">If you're using version 7.3.0, and you are bringing fee transactions over from Project Service Automation, you must install KB 4345320 in order to include those fees in the project invoice.</span></span>
> - <span data-ttu-id="7bfe6-109">Si utilitzeu la versió 8.0, podreu utilitzar la integració de tasques de projecte, les categories de transaccions de despeses, les estimacions d'hores, les estimacions de despeses i el bloqueig de funcionalitats.</span><span class="sxs-lookup"><span data-stu-id="7bfe6-109">If you're using version 8.0, you will be able to use project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking.</span></span>
> - <span data-ttu-id="7bfe6-110">Si esteu utilitzant la versió 8.0.1 o posterior, podreu sincronitzar els valors reals.</span><span class="sxs-lookup"><span data-stu-id="7bfe6-110">If you're using version 8.0.1 or later, you will be able to synchronize actuals.</span></span>

<span data-ttu-id="7bfe6-111">Per poder integrar el Project Service Automation i el Finance, heu de configurar els paràmetres d'integració del Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="7bfe6-111">Before you can integrate Project Service Automation Finance, you must configure the Project Service Automation integration parameters.</span></span> <span data-ttu-id="7bfe6-112">Per a més informació, vegeu [Paràmetres d'integració del Project Service Automation](PSA-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="7bfe6-112">For more information, see [Project Service Automation integration parameters](PSA-parameters.md).</span></span>

<span data-ttu-id="7bfe6-113">Aquesta solució d'integració permet la sincronització directa en els següents escenaris:</span><span class="sxs-lookup"><span data-stu-id="7bfe6-113">This integration solution enables direct synchronization in the following scenarios:</span></span>

- <span data-ttu-id="7bfe6-114">Mantenir els contractes de projecte al Project Service Automation i sincronitzar-los directament del Project Service Automation al Finance.</span><span class="sxs-lookup"><span data-stu-id="7bfe6-114">Maintain project contracts in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="7bfe6-115">Crear projectes al Project Service Automation i sincronitzar-los directament del Project Service Automation al Finance.</span><span class="sxs-lookup"><span data-stu-id="7bfe6-115">Create projects in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="7bfe6-116">Mantenir línies de contracte del projecte al Project Service Automation i sincronitzar-les directament del Project Service Automation al Finance.</span><span class="sxs-lookup"><span data-stu-id="7bfe6-116">Maintain project contract lines in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="7bfe6-117">Mantenir fites de línies de contracte del projecte al Project Service Automation i sincronitzar-les directament del Project Service Automation al Finance.</span><span class="sxs-lookup"><span data-stu-id="7bfe6-117">Maintain project contract line milestones in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="7bfe6-118">Mantenir tasques del projecte al Project Service Automation i sincronitzar-les directament del Project Service Automation al Finance.</span><span class="sxs-lookup"><span data-stu-id="7bfe6-118">Maintain project tasks in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="7bfe6-119">Mantenir categories de transacció de despeses al Finance i sincronitzar-les directament del Finance al Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="7bfe6-119">Maintain expense transaction categories in Finance, and synchronize them directly from Finance to Project Service Automation.</span></span>
- <span data-ttu-id="7bfe6-120">Crear estimacions d'hores del projecte al Project Service Automation i sincronitzar-les directament del Project Service Automation al Finance.</span><span class="sxs-lookup"><span data-stu-id="7bfe6-120">Create project hour estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="7bfe6-121">Crear estimacions de despeses del projecte al Project Service Automation i sincronitzar-les directament del Project Service Automation al Finance.</span><span class="sxs-lookup"><span data-stu-id="7bfe6-121">Create project expense estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="7bfe6-122">Crear valors reals de temps, despeses i taxes al Project Service Automation i crear transaccions de projecte al diari d'integració del Project Service Automation per tal que es puguin comptabilitzar al Finance.</span><span class="sxs-lookup"><span data-stu-id="7bfe6-122">Create project time, expense, and fee actuals in Project Service Automation, and create project transactions in the Project Service Automation integration journal so that they can be posted in Finance.</span></span>

## <a name="data-synchronization"></a><span data-ttu-id="7bfe6-123">Sincronització de les dades</span><span class="sxs-lookup"><span data-stu-id="7bfe6-123">Data synchronization</span></span>

<span data-ttu-id="7bfe6-124">A la il·lustració següent es mostren les dades que se sincronitzen com a part de la integració entre el Project Service Automation i el Finance.</span><span class="sxs-lookup"><span data-stu-id="7bfe6-124">The following illustration shows how data is synchronized as part of the integration between Project Service Automation and Finance.</span></span>

> [!NOTE]
> <span data-ttu-id="7bfe6-125">No totes les plantilles estan disponibles actualment.</span><span class="sxs-lookup"><span data-stu-id="7bfe6-125">Not all templates are currently available.</span></span> <span data-ttu-id="7bfe6-126">Les plantilles es publicaran a mesura que es completin.</span><span class="sxs-lookup"><span data-stu-id="7bfe6-126">Templates will be released as they are completed.</span></span>

<span data-ttu-id="7bfe6-127">[![Integració del Project Service Automation amb el Finance](./media/PSA-integration.png)](./media/PSA-integration.png)</span><span class="sxs-lookup"><span data-stu-id="7bfe6-127">[![Project Service Automation integration with Finance](./media/PSA-integration.png)](./media/PSA-integration.png)</span></span>

## <a name="system-requirements-for-finance"></a><span data-ttu-id="7bfe6-128">Requisits del sistema per al Finance</span><span class="sxs-lookup"><span data-stu-id="7bfe6-128">System requirements for Finance</span></span>

<span data-ttu-id="7bfe6-129">Per utilitzar la solució d'integració del Project Service Automation al Finance, heu d'instal·lar l'Enterprise Edition 7.3 amb l'actualització de la plataforma 12 o posterior.</span><span class="sxs-lookup"><span data-stu-id="7bfe6-129">To use the Project Service Automation to Finance integration solution, you must install Enterprise edition 7.3 with Platform update 12 or later.</span></span>

## <a name="system-requirements-for-project-service-automation"></a><span data-ttu-id="7bfe6-130">Requisits del sistema per al Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="7bfe6-130">System requirements for Project Service Automation</span></span>

<span data-ttu-id="7bfe6-131">Per utilitzar la solució d'integració del Project Service Automation al Finance, heu d'instal·lar els components següents:</span><span class="sxs-lookup"><span data-stu-id="7bfe6-131">To use the Project Service Automation to Finance integration solution, you must install the following components:</span></span>

- <span data-ttu-id="7bfe6-132">Dynamics 365 Project Service Automation versió 9.0.0.0 o posterior</span><span class="sxs-lookup"><span data-stu-id="7bfe6-132">Dynamics 365 Project Service Automation version 9.0.0.0 or later</span></span>
- <span data-ttu-id="7bfe6-133">Solució Donant potencial a ingressos per al Dynamics 365 Sales, versió 1.14.0.0 (v14) o posterior</span><span class="sxs-lookup"><span data-stu-id="7bfe6-133">Prospect to cash solution for Dynamics 365 Sales, version 1.14.0.0 (v14) or later</span></span>
- <span data-ttu-id="7bfe6-134">Solució Project Service Automation a Finance per al Dynamics 365 Project Service Automation, versió 1.0.0.0 o posterior</span><span class="sxs-lookup"><span data-stu-id="7bfe6-134">Project Service Automation to Finance solution for Dynamics 365 Project Service Automation version 1.0.0.0 or later</span></span>

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a><span data-ttu-id="7bfe6-135">Instal·lar la solució d'integració del Project Service Automation al Finance a la instància del Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="7bfe6-135">Install the Project Service Automation to Finance integration solution in your Project Service Automation instance</span></span>

<span data-ttu-id="7bfe6-136">Baixeu la solució d'integració del Project Service Automation al Finance des del [Centre de baixades de Microsoft](https://www.microsoft.com/download/details.aspx?id=57016) i seguiu les instruccions que s'inclouen amb la solució.</span><span class="sxs-lookup"><span data-stu-id="7bfe6-136">Download the Project Service Automation to Finance integration solution from [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=57016), and follow the instructions that are included with the solution.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]