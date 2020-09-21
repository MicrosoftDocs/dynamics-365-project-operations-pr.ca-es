---
title: Sincronitzar les estimacions del projecte directament des del Project Service Automation al Finance and Operations
description: Aquest tema descriu les plantilles i tasques subjacents que s'utilitzen per sincronitzar estimacions d'hores de projecte i estimacions de despeses de projecte directament des del Microsoft Dynamics 365 Project Service Automation al Dynamics 365 Finance.
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
ms.assetid: d688ce9a-41e3-4ebe-952e-700f8351fbe9
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: a24a967d82c2e005e61234d34da8a583b61ff7b1
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749483"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="a3ff7-103">Sincronitzar les estimacions del projecte directament des del Project Service Automation al Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a3ff7-103">Synchronize project estimates directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="a3ff7-104">Aquest tema descriu les plantilles i tasques subjacents que s'utilitzen per sincronitzar estimacions d'hores de projecte i estimacions de despeses de projecte directament des del Dynamics 365 Project Service Automation al Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="a3ff7-104">This topic describes the templates and underlying tasks that are used to synchronize project hour estimates and project expense estimates directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="a3ff7-105">La integració de tasques de projecte, les categories de transaccions de despeses, les estimacions d'hores, les estimacions de despeses i el bloqueig de funcionalitats estan disponibles a la versió 8.0.</span><span class="sxs-lookup"><span data-stu-id="a3ff7-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in version 8.0.</span></span>
> - <span data-ttu-id="a3ff7-106">La integració dels valors reals del projecte està disponible a la versió 8.0.1 i posteriors.</span><span class="sxs-lookup"><span data-stu-id="a3ff7-106">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="a3ff7-107">Flux de dades del Project Service Automation al Finance</span><span class="sxs-lookup"><span data-stu-id="a3ff7-107">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="a3ff7-108">La solució d'integració del Project Service Automation al Finance utilitza la característica d'integració de dades per sincronitzar dades entre les instàncies del Project Service Automation i el Finance.</span><span class="sxs-lookup"><span data-stu-id="a3ff7-108">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="a3ff7-109">Les plantilles d'integració que estan disponibles amb la característica d'integració de dades permeten el flux de dades sobre les estimacions d'hores de projecte i estimacions de despeses de projecte del Project Service Automation al Finance.</span><span class="sxs-lookup"><span data-stu-id="a3ff7-109">The integration templates that are available with the Data integration feature enable the flow of data about project hour estimates and project expense estimates from Project Service Automation to Finance.</span></span>

<span data-ttu-id="a3ff7-110">A la il·lustració següent es mostren les dades que se sincronitzen entre el Project Service Automation i el Finance.</span><span class="sxs-lookup"><span data-stu-id="a3ff7-110">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="a3ff7-111">[![Flux de dades per a la integració de Project Service Automation amb el Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="a3ff7-111">[![Data flow for Project Service Automation integration with Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span></span>

## <a name="project-hour-estimates"></a><span data-ttu-id="a3ff7-112">Estimacions d'hores del projecte</span><span class="sxs-lookup"><span data-stu-id="a3ff7-112">Project hour estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="a3ff7-113">Plantilla i tasques</span><span class="sxs-lookup"><span data-stu-id="a3ff7-113">Template and tasks</span></span>

<span data-ttu-id="a3ff7-114">Per accedir a les plantilles disponibles, al centre d'administració del Microsoft Power Apps, seleccioneu **Projectes** i, a continuació, a la cantonada superior dreta, seleccioneu **Nou projecte** per seleccionar les plantilles públiques.</span><span class="sxs-lookup"><span data-stu-id="a3ff7-114">To access the available templates, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="a3ff7-115">La plantilla i les tasques subjacents següents s'utilitzen per sincronitzar les estimacions d'hores del projecte del Project Service Automation al Finance:</span><span class="sxs-lookup"><span data-stu-id="a3ff7-115">The following template and underlying tasks are used to synchronize project hour estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="a3ff7-116">**Nom de la plantilla en la integració de dades**: estimacions d'hores del projecte (PSA a Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="a3ff7-116">**Name of the template in Data integration:** Project hour estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="a3ff7-117">**Nom de les tasques del projecte:**</span><span class="sxs-lookup"><span data-stu-id="a3ff7-117">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="a3ff7-118">Relacions de transacció</span><span class="sxs-lookup"><span data-stu-id="a3ff7-118">Transaction relationships</span></span>
    - <span data-ttu-id="a3ff7-119">Estimacions de despeses</span><span class="sxs-lookup"><span data-stu-id="a3ff7-119">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="a3ff7-120">Conjunt d'entitats</span><span class="sxs-lookup"><span data-stu-id="a3ff7-120">Entity set</span></span>

| <span data-ttu-id="a3ff7-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="a3ff7-121">Project Service Automation</span></span> | <span data-ttu-id="a3ff7-122">Finance</span><span class="sxs-lookup"><span data-stu-id="a3ff7-122">Finance</span></span>                                       |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="a3ff7-123">Tasques del projecte</span><span class="sxs-lookup"><span data-stu-id="a3ff7-123">Project tasks</span></span>              | <span data-ttu-id="a3ff7-124">Entitat d'integració per a estimacions d'hores del projecte</span><span class="sxs-lookup"><span data-stu-id="a3ff7-124">Integration entity for project hour estimates</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="a3ff7-125">Flux d'entitat</span><span class="sxs-lookup"><span data-stu-id="a3ff7-125">Entity flow</span></span>

<span data-ttu-id="a3ff7-126">Les estimacions d'hores del projecte estan administrades al Project Service Automation i se sincronitzen amb el Finance com a previsions d'hores del projecte.</span><span class="sxs-lookup"><span data-stu-id="a3ff7-126">Project hour estimates are managed in Project Service Automation, and they are synchronized to Finance as project hour forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="a3ff7-127">Requisits previs</span><span class="sxs-lookup"><span data-stu-id="a3ff7-127">Prerequisites</span></span>

<span data-ttu-id="a3ff7-128">Abans de la sincronització de les estimacions d'hores del projecte, cal sincronitzar els projectes, les tasques del projecte i les categories de transaccions de despeses del projecte.</span><span class="sxs-lookup"><span data-stu-id="a3ff7-128">Before synchronization of project hour estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="a3ff7-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="a3ff7-129">Power Query</span></span>

<span data-ttu-id="a3ff7-130">A la plantilla d'estimacions d'hores del projecte, heu d'utilitzar el Microsoft Power Query per a l'Excel per completar aquestes tasques:</span><span class="sxs-lookup"><span data-stu-id="a3ff7-130">In the project hour estimates template, you must use Microsoft Power Query for Excel to complete these tasks:</span></span>

- <span data-ttu-id="a3ff7-131">Definiu l'identificador del model de previsió per defecte que s'utilitzarà quan la integració creï previsions d'hores noves.</span><span class="sxs-lookup"><span data-stu-id="a3ff7-131">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="a3ff7-132">Filtreu tots els registres específics del recurs a la tasca que no es podran integrar en previsions d'hores.</span><span class="sxs-lookup"><span data-stu-id="a3ff7-132">Filter out any resource-specific records in the task that will fail the integration into hour forecasts.</span></span>
- <span data-ttu-id="a3ff7-133">Filtreu totes les files de categoria de transaccions buides.</span><span class="sxs-lookup"><span data-stu-id="a3ff7-133">Filter out any empty transaction category rows.</span></span> <span data-ttu-id="a3ff7-134">Si no completeu aquesta tasca, pot ser que es facin prediccions d'hores incorrectes.</span><span class="sxs-lookup"><span data-stu-id="a3ff7-134">Failure to complete this task might result in incorrect hour forecasts.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="a3ff7-135">Definir l'identificador del model de previsió per defecte</span><span class="sxs-lookup"><span data-stu-id="a3ff7-135">Set the default forecast model ID</span></span>

<span data-ttu-id="a3ff7-136">Per actualitzar l'identificador del model de previsió per defecte a la plantilla, feu clic a la fletxa **Assignació** per obrir l'assignació.</span><span class="sxs-lookup"><span data-stu-id="a3ff7-136">To update the default forecast model ID in the template, click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="a3ff7-137">A continuació, seleccioneu l'enllaç **Consulta i filtratge avançats**.</span><span class="sxs-lookup"><span data-stu-id="a3ff7-137">Then select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="a3ff7-138">Si utilitzeu la plantilla Estimacions d'hores del projecte (PSA a Fin and Ops) per defecte, seleccioneu la **Condició inserida** a la llista de **Passos aplicats**.</span><span class="sxs-lookup"><span data-stu-id="a3ff7-138">If you're using the default Project hour estimates (PSA to Fin and Ops) template, select the **Inserted Condition** in the list of **Applied Steps**.</span></span> <span data-ttu-id="a3ff7-139">A l'entrada de **Funció**, substituïu **O\_previsió** pel nom de l'identificador del model de previsió que s'ha d'utilitzar amb la integració.</span><span class="sxs-lookup"><span data-stu-id="a3ff7-139">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="a3ff7-140">La plantilla per defecte té un ID de model de previsió a partir de les dades de demostració.</span><span class="sxs-lookup"><span data-stu-id="a3ff7-140">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="a3ff7-141">Si esteu creant una plantilla nova, heu d'afegir aquesta columna.</span><span class="sxs-lookup"><span data-stu-id="a3ff7-141">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="a3ff7-142">Al Power Query, seleccioneu **Afegeix una columna condicional** i introduïu un nom per a la columna nova, com ara **ModelID**.</span><span class="sxs-lookup"><span data-stu-id="a3ff7-142">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="a3ff7-143">Introduïu la condició per a la columna, on, if Project task is not null, then \<introduïu l'identificador del model de previsió\>; else null.</span><span class="sxs-lookup"><span data-stu-id="a3ff7-143">Enter the condition for the column, where, if Project task is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="filter-out-resource-specific-records"></a><span data-ttu-id="a3ff7-144">Filtrar els registres específics de recurs</span><span class="sxs-lookup"><span data-stu-id="a3ff7-144">Filter out resource-specific records</span></span>

<span data-ttu-id="a3ff7-145">La plantilla Estimacions d'hores del projecte (PSA a Fin and Ops) té un filtre per defecte que elimina els registres específics d'un recurs.</span><span class="sxs-lookup"><span data-stu-id="a3ff7-145">The Project hour estimates (PSA to Fin and Ops) template has a default filter that removes any resource-specific records.</span></span> <span data-ttu-id="a3ff7-146">Si creeu una plantilla pròpia, heu d'afegir aquest filtre.</span><span class="sxs-lookup"><span data-stu-id="a3ff7-146">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="a3ff7-147">Seleccioneu l'enllaç **Consulta i filtratge avançats** per filtrar a la columna **msdyn\_islinetask** per incloure només els registres amb **False**.</span><span class="sxs-lookup"><span data-stu-id="a3ff7-147">Select the **Advanced Query and Filtering** link to filter on the **msdyn\_islinetask** column so that only **False** records are included.</span></span>

#### <a name="filter-out-empty-transaction-category-rows"></a><span data-ttu-id="a3ff7-148">Filtrar les files de categoria de transaccions buides</span><span class="sxs-lookup"><span data-stu-id="a3ff7-148">Filter out empty transaction category rows</span></span>

<span data-ttu-id="a3ff7-149">Heu d'afegir un filtre per suprimir qualsevol fila que tingui categories de transaccions buides.</span><span class="sxs-lookup"><span data-stu-id="a3ff7-149">You must add a filter to remove any rows that have empty transaction categories.</span></span> <span data-ttu-id="a3ff7-150">Aquesta tasca és necessària, independentment de si utilitzeu la plantilla per defecte o creeu la vostra pròpia plantilla.</span><span class="sxs-lookup"><span data-stu-id="a3ff7-150">This task is required, regardless of whether you're using the default template or creating your own template.</span></span> <span data-ttu-id="a3ff7-151">Aquest filtre suprimeix les files de resum de Project Service Automation que podrien fer que la previsió d'hores al Finance fos incorrecta.</span><span class="sxs-lookup"><span data-stu-id="a3ff7-151">This filter removes any summary rows from Project Service Automation that might cause the hour forecasts in Finance to be incorrect.</span></span> <span data-ttu-id="a3ff7-152">Seleccioneu l'enllaç **Consulta i filtratge avançats** per filtrar els registres nuls a la columna **msdyn\_transactioncategory\_value**.</span><span class="sxs-lookup"><span data-stu-id="a3ff7-152">Select **Advanced Query and Filtering** link to filter out null records in the **msdyn\_transactioncategory\_value** column.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="a3ff7-153">Assignació de plantilles a la integració de dades</span><span class="sxs-lookup"><span data-stu-id="a3ff7-153">Template mapping in Data integration</span></span>

<span data-ttu-id="a3ff7-154">A la il·lustració següent es mostra un exemple de l'assignació de tasques de plantilla a la integració de dades.</span><span class="sxs-lookup"><span data-stu-id="a3ff7-154">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="a3ff7-155">L'assignació mostra la informació de camp que se sincronitzarà del Project Service Automation al Finance.</span><span class="sxs-lookup"><span data-stu-id="a3ff7-155">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="a3ff7-156">[![Assignació de plantilla](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="a3ff7-156">[![Template mapping](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span></span>

## <a name="project-expense-estimates"></a><span data-ttu-id="a3ff7-157">Estimacions de despesa del projecte</span><span class="sxs-lookup"><span data-stu-id="a3ff7-157">Project expense estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="a3ff7-158">Plantilla i tasques</span><span class="sxs-lookup"><span data-stu-id="a3ff7-158">Template and tasks</span></span>

<span data-ttu-id="a3ff7-159">La plantilla i les tasques subjacents següents s'utilitzen per sincronitzar les estimacions de despesa del projecte del Project Service Automation al Finance:</span><span class="sxs-lookup"><span data-stu-id="a3ff7-159">The following template and underlying tasks are used to synchronize project expense estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="a3ff7-160">**Nom de la plantilla en la integració de dades**: estimacions de despesa del projecte (PSA a Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="a3ff7-160">**Name of the template in Data integration:** Project expense estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="a3ff7-161">**Nom de les tasques del projecte:**</span><span class="sxs-lookup"><span data-stu-id="a3ff7-161">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="a3ff7-162">Relacions de transacció</span><span class="sxs-lookup"><span data-stu-id="a3ff7-162">Transaction relationships</span></span> 
    - <span data-ttu-id="a3ff7-163">Estimacions de despeses</span><span class="sxs-lookup"><span data-stu-id="a3ff7-163">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="a3ff7-164">Conjunt d'entitats</span><span class="sxs-lookup"><span data-stu-id="a3ff7-164">Entity set</span></span>

| <span data-ttu-id="a3ff7-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="a3ff7-165">Project Service Automation</span></span> | <span data-ttu-id="a3ff7-166">Finance</span><span class="sxs-lookup"><span data-stu-id="a3ff7-166">Finance</span></span>                                                  |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="a3ff7-167">Connexions de transacció</span><span class="sxs-lookup"><span data-stu-id="a3ff7-167">Transaction Connections</span></span>    | <span data-ttu-id="a3ff7-168">Entitat d'integració per a les relacions de transaccions del projecte</span><span class="sxs-lookup"><span data-stu-id="a3ff7-168">Integration entity for project transaction relationships</span></span> |
| <span data-ttu-id="a3ff7-169">Línies d'estimació</span><span class="sxs-lookup"><span data-stu-id="a3ff7-169">Estimate Lines</span></span>             | <span data-ttu-id="a3ff7-170">Entitat d'integració per a estimacions de despesa del projecte</span><span class="sxs-lookup"><span data-stu-id="a3ff7-170">Integration entity for project expense estimates</span></span>         |

### <a name="entity-flow"></a><span data-ttu-id="a3ff7-171">Flux d'entitat</span><span class="sxs-lookup"><span data-stu-id="a3ff7-171">Entity flow</span></span>

<span data-ttu-id="a3ff7-172">Les estimacions de despesa del projecte estan administrades al Project Service Automation i se sincronitzen amb el Finance com a previsions de despesa del projecte.</span><span class="sxs-lookup"><span data-stu-id="a3ff7-172">Project expense estimates are managed in Project Service Automation, and they are synchronized to Finance as project expense forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="a3ff7-173">Requisits previs</span><span class="sxs-lookup"><span data-stu-id="a3ff7-173">Prerequisites</span></span>

<span data-ttu-id="a3ff7-174">Abans de la sincronització de les estimacions de despesa del projecte, cal sincronitzar els projectes, les tasques del projecte i les categories de transaccions de despeses del projecte.</span><span class="sxs-lookup"><span data-stu-id="a3ff7-174">Before synchronization of project expense estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="a3ff7-175">Power Query</span><span class="sxs-lookup"><span data-stu-id="a3ff7-175">Power Query</span></span>

<span data-ttu-id="a3ff7-176">A la plantilla d'estimacions de despesa del projecte, heu d'utilitzar el Power Query per completar les tasques següents:</span><span class="sxs-lookup"><span data-stu-id="a3ff7-176">In the project expense estimates template, you must use Power Query to complete the following tasks:</span></span>

- <span data-ttu-id="a3ff7-177">Filtrar per incloure només els registres de la línia d'estimació de despesa.</span><span class="sxs-lookup"><span data-stu-id="a3ff7-177">Filter to include only expense estimate line records.</span></span>
- <span data-ttu-id="a3ff7-178">Definiu l'identificador del model de previsió per defecte que s'utilitzarà quan la integració creï previsions d'hores noves.</span><span class="sxs-lookup"><span data-stu-id="a3ff7-178">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="a3ff7-179">Transformar els tipus de facturació.</span><span class="sxs-lookup"><span data-stu-id="a3ff7-179">Transform the billing types.</span></span>
- <span data-ttu-id="a3ff7-180">Transformar els tipus de transacció.</span><span class="sxs-lookup"><span data-stu-id="a3ff7-180">Transform the transaction types.</span></span>

#### <a name="filter-to-include-only-expense-estimate-lines"></a><span data-ttu-id="a3ff7-181">Filtrar per incloure només les línies d'estimació de despesa</span><span class="sxs-lookup"><span data-stu-id="a3ff7-181">Filter to include only expense estimate lines</span></span>

<span data-ttu-id="a3ff7-182">La plantilla Estimacions de despesa de projecte (PSA a Fin and Ops) té un filtre per defecte que inclou només les línies de despesa a la integració.</span><span class="sxs-lookup"><span data-stu-id="a3ff7-182">The Project expense estimates (PSA to Fin and Ops) template has a default filter that includes only expense lines in the integration.</span></span> <span data-ttu-id="a3ff7-183">Si creeu una plantilla pròpia, heu d'afegir aquest filtre.</span><span class="sxs-lookup"><span data-stu-id="a3ff7-183">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="a3ff7-184">Seleccioneu la tasca **Relacions de transacció** i, a continuació, feu clic a la fletxa **Assignació** per obrir l'assignació.</span><span class="sxs-lookup"><span data-stu-id="a3ff7-184">Select the **Transaction relationships** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="a3ff7-185">Seleccioneu l'enllaç **Consulta i filtratge avançats**.</span><span class="sxs-lookup"><span data-stu-id="a3ff7-185">Select the **Advanced Query and Filtering** link.</span></span> <span data-ttu-id="a3ff7-186">Filtreu la columna **msdyn\_transactiontype1** per tal que inclogui només **msdyn\_estimateline**.</span><span class="sxs-lookup"><span data-stu-id="a3ff7-186">Filter the **msdyn\_transactiontype1** column so that it includes only **msdyn\_estimateline**.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="a3ff7-187">Definir l'identificador del model de previsió per defecte</span><span class="sxs-lookup"><span data-stu-id="a3ff7-187">Set the default forecast model ID</span></span>

<span data-ttu-id="a3ff7-188">Per actualitzar l'identificador del model de previsió per defecte a la plantilla, seleccioneu la tasca **Estimacions de despesa** i feu clic a la fletxa **Assignació** per obrir l'assignació.</span><span class="sxs-lookup"><span data-stu-id="a3ff7-188">To update the default forecast model ID in the template, select the **Expense estimates** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="a3ff7-189">Seleccioneu l'enllaç **Consulta i filtratge avançats**.</span><span class="sxs-lookup"><span data-stu-id="a3ff7-189">Select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="a3ff7-190">Si utilitzeu la plantilla Estimacions de despesa del projecte (PSA a Fin and Ops) per defecte, al Power Query, seleccioneu la primera **Condició inserida** de la secció **Passos aplicats**.</span><span class="sxs-lookup"><span data-stu-id="a3ff7-190">If you're using the default Project expense estimates (PSA to Fin and Ops) template, in Power Query, select the first **Inserted Condition** from the **Applied Steps** section.</span></span> <span data-ttu-id="a3ff7-191">A l'entrada de **Funció**, substituïu **O\_previsió** pel nom de l'identificador del model de previsió que s'ha d'utilitzar amb la integració.</span><span class="sxs-lookup"><span data-stu-id="a3ff7-191">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="a3ff7-192">La plantilla per defecte té un ID de model de previsió a partir de les dades de demostració.</span><span class="sxs-lookup"><span data-stu-id="a3ff7-192">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="a3ff7-193">Si esteu creant una plantilla nova, heu d'afegir aquesta columna.</span><span class="sxs-lookup"><span data-stu-id="a3ff7-193">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="a3ff7-194">Al Power Query, seleccioneu **Afegeix una columna condicional** i introduïu un nom per a la columna nova, com ara **ModelID**.</span><span class="sxs-lookup"><span data-stu-id="a3ff7-194">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="a3ff7-195">Introduïu la condició per a la columna, on, if Estimate line ID is not null, then \<introduïu l'identificador del model de previsió\>; else null.</span><span class="sxs-lookup"><span data-stu-id="a3ff7-195">Enter the condition for the column, where, if Estimate line ID is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="transform-the-billing-types"></a><span data-ttu-id="a3ff7-196">Transformar els tipus de facturació</span><span class="sxs-lookup"><span data-stu-id="a3ff7-196">Transform the billing types</span></span>

<span data-ttu-id="a3ff7-197">La plantilla Estimacions de despesa del projecte (PSA a Fin and Ops) inclou una columna condicional que s'utilitza per transformar els tipus de facturació que es reben del Project Service Automation durant la integració.</span><span class="sxs-lookup"><span data-stu-id="a3ff7-197">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the billing types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="a3ff7-198">Si creeu una plantilla pròpia, heu d'afegir aquesta columna condicional.</span><span class="sxs-lookup"><span data-stu-id="a3ff7-198">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="a3ff7-199">Seleccioneu l'enllaç **Consulta i filtratge avançats** i, a continuació, seleccioneu **Afegeix una columna condicional**.</span><span class="sxs-lookup"><span data-stu-id="a3ff7-199">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="a3ff7-200">Introduïu un nom per a la columna nova, com ara **BillingType**.</span><span class="sxs-lookup"><span data-stu-id="a3ff7-200">Enter a name for the new column, such as **BillingType**.</span></span> <span data-ttu-id="a3ff7-201">Introduïu la condició següent:</span><span class="sxs-lookup"><span data-stu-id="a3ff7-201">Then enter the following condition:</span></span>

<span data-ttu-id="a3ff7-202">If **msdyn\_billingtype** = 192350000, then **NonChargeable**</span><span class="sxs-lookup"><span data-stu-id="a3ff7-202">If **msdyn\_billingtype** = 192350000, then **NonChargeable**</span></span>  
<span data-ttu-id="a3ff7-203">else if **msdyn\_billingtype** = 192350001, then **Chargeable**</span><span class="sxs-lookup"><span data-stu-id="a3ff7-203">else if **msdyn\_billingtype** = 192350001, then **Chargeable**</span></span>  
<span data-ttu-id="a3ff7-204">else if **msdyn\_billingtype** = 192350002, then **Complimentary**</span><span class="sxs-lookup"><span data-stu-id="a3ff7-204">else if **msdyn\_billingtype** = 192350002, then **Complimentary**</span></span>  
<span data-ttu-id="a3ff7-205">else **NotAvailable**</span><span class="sxs-lookup"><span data-stu-id="a3ff7-205">else **NotAvailable**</span></span>

#### <a name="transform-the-transaction-types"></a><span data-ttu-id="a3ff7-206">Transformar els tipus de transacció</span><span class="sxs-lookup"><span data-stu-id="a3ff7-206">Transform the transaction types</span></span>

<span data-ttu-id="a3ff7-207">La plantilla Estimacions de despesa del projecte (PSA a Fin and Ops) inclou una columna condicional que s'utilitza per transformar els tipus de transacció que es reben del Project Service Automation durant la integració.</span><span class="sxs-lookup"><span data-stu-id="a3ff7-207">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the transaction types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="a3ff7-208">Si creeu una plantilla pròpia, heu d'afegir aquesta columna condicional.</span><span class="sxs-lookup"><span data-stu-id="a3ff7-208">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="a3ff7-209">Seleccioneu l'enllaç **Consulta i filtratge avançats** i, a continuació, seleccioneu **Afegeix una columna condicional**.</span><span class="sxs-lookup"><span data-stu-id="a3ff7-209">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="a3ff7-210">Introduïu un nom per a la columna nova, com ara **TransactionType**.</span><span class="sxs-lookup"><span data-stu-id="a3ff7-210">Enter a name for the new column, such as **TransactionType**.</span></span> <span data-ttu-id="a3ff7-211">Introduïu la condició següent:</span><span class="sxs-lookup"><span data-stu-id="a3ff7-211">Then enter the following condition:</span></span>

<span data-ttu-id="a3ff7-212">If **msdyn\_transactiontypecode** = 192350000, then **Cost**</span><span class="sxs-lookup"><span data-stu-id="a3ff7-212">If **msdyn\_transactiontypecode** = 192350000, then **Cost**</span></span>  
<span data-ttu-id="a3ff7-213">else if **msdyn\_transactiontypecode** = 192350005, then **Sales**</span><span class="sxs-lookup"><span data-stu-id="a3ff7-213">else if **msdyn\_transactiontypecode** = 192350005, then **Sales**</span></span>  
<span data-ttu-id="a3ff7-214">else **null**</span><span class="sxs-lookup"><span data-stu-id="a3ff7-214">else **null**</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="a3ff7-215">Assignació de plantilles a la integració de dades</span><span class="sxs-lookup"><span data-stu-id="a3ff7-215">Template mapping in Data integration</span></span>

<span data-ttu-id="a3ff7-216">A les il·lustracions següents es mostren exemples de l'assignació de tasques de plantilla a la integració de dades.</span><span class="sxs-lookup"><span data-stu-id="a3ff7-216">The following illustrations show examples of the template task mappings in Data integration.</span></span> <span data-ttu-id="a3ff7-217">L'assignació mostra la informació de camp que se sincronitzarà del Project Service Automation al Finance.</span><span class="sxs-lookup"><span data-stu-id="a3ff7-217">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="a3ff7-218">[![Assignació de plantilla](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="a3ff7-218">[![Template mapping](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span></span>

<span data-ttu-id="a3ff7-219">[![Assignació de plantilla](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="a3ff7-219">[![Template mapping](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span></span>
