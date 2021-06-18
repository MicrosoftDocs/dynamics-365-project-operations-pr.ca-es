---
title: Sincronitzar categories de despeses del projecte entre el Finance and Operations i el Project Service Automation
description: Aquest tema descriu les plantilles i tasques subjacents que s'utilitzen per sincronitzar categories de despesa entre el Microsoft Dynamics 365 Finance i el Dynamics 365 Project Service Automation.
author: Yowelle
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 2816d363dbfe6ef2d98a584b214f72d9b30c49bb
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999839"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a><span data-ttu-id="dce02-103">Sincronitzar categories de despeses del projecte entre el Finance and Operations i el Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="dce02-103">Synchronize project expense categories between Finance and Operations and Project Service Automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="dce02-104">Aquest tema descriu les plantilles i tasques subjacents que s'utilitzen per sincronitzar categories de despesa entre el Dynamics 365 Finance i el Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="dce02-104">This topic describes the templates and underlying tasks that are used to synchronize project expense categories between Dynamics 365 Finance and Dynamics 365 Project Service Automation.</span></span>

> [!NOTE]
> - <span data-ttu-id="dce02-105">La integració de tasques de projecte, les categories de transaccions de despeses, les estimacions d'hores, les estimacions de despeses i el bloqueig de funcionalitats estan disponibles a la versió 8.0.</span><span class="sxs-lookup"><span data-stu-id="dce02-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="dce02-106">La integració dels valors reals del projecte està disponible a la versió 8.0.1 i posteriors.</span><span class="sxs-lookup"><span data-stu-id="dce02-106">Actuals integration is available in version 8.0.1 or later.</span></span>
> - <span data-ttu-id="dce02-107">Si utilitzeu l'Enterprise Edition 7.3.0 després d'instal·lar el KB 4132657 i el KB 4132660, podreu utilitzar les plantilles per integrar tasques de projecte, categories de transaccions de despeses, estimacions d'hores, estimacions de despeses i valors reals i configurar el bloqueig de funcionalitats.</span><span class="sxs-lookup"><span data-stu-id="dce02-107">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="dce02-108">Si heu de reiniciar la distribució comptable, us recomanem que també instal·leu el KB 4131710.</span><span class="sxs-lookup"><span data-stu-id="dce02-108">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>

## <a name="data-flow-for-project-service-automation-and-finance"></a><span data-ttu-id="dce02-109">Flux de dades per al Project Service Automation i el Finance</span><span class="sxs-lookup"><span data-stu-id="dce02-109">Data flow for Project Service Automation and Finance</span></span>

<span data-ttu-id="dce02-110">La solució d'integració del Project Service Automation i el Finance utilitza la característica d'integració de dades per sincronitzar dades entre les instàncies del Project Service Automation i el Finance.</span><span class="sxs-lookup"><span data-stu-id="dce02-110">The Project Service Automation and Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="dce02-111">Les plantilles d'integració que estan disponibles amb la característica d'integració de dades permeten el flux de dades sobre les categories de transaccions de despeses de projecte entre el Project Service Automation i el Finance.</span><span class="sxs-lookup"><span data-stu-id="dce02-111">The integration templates that are available with the Data integration feature enable the flow of data about project expense transaction categories between Finance and Project Service Automation.</span></span>

<span data-ttu-id="dce02-112">Si les categories de despeses del projecte es basen en el Finance, el flux d'integració és primer del Finance al Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="dce02-112">If the project expense categories are mastered in Finance, the integration flow is first from Finance to Project Service Automation.</span></span> <span data-ttu-id="dce02-113">Els identificadors d'integració de les categories de despesa del projecte s'actualitzen a través de la sincronització del Project Service Automation al Finance.</span><span class="sxs-lookup"><span data-stu-id="dce02-113">The integration IDs of the project expense categories are then updated through synchronization from Project Service Automation to Finance.</span></span>

<span data-ttu-id="dce02-114">Si les categories de despeses del projecte es basen en el Project Service Automation, el flux d'integració és primer del Project Service Automation al Finance.</span><span class="sxs-lookup"><span data-stu-id="dce02-114">If the project expense categories are mastered in Project Service Automation, the integration flow is first from Project Service Automation to Finance.</span></span> <span data-ttu-id="dce02-115">Les categories del projecte s'han de configurar al Finance abans de la sincronització des del Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="dce02-115">The project categories must already be configured in Finance before the synchronization from Project Service Automation.</span></span> <span data-ttu-id="dce02-116">A continuació, sincronitzeu del Finance al Project Service Automation i després del Project Service Automation al Finance una altra vegada.</span><span class="sxs-lookup"><span data-stu-id="dce02-116">Then synchronize from Finance back to Project Service Automation, and then from Project Service Automation to Finance again.</span></span> <span data-ttu-id="dce02-117">D'aquesta manera, ajudareu a garantir que les categories estan enllaçades i que no es creen duplicats.</span><span class="sxs-lookup"><span data-stu-id="dce02-117">In this way, you help guarantee that the categories are linked, and that no duplicates are created.</span></span>

> [!NOTE]
> <span data-ttu-id="dce02-118">Normalment, les categories de despeses del projecte s'agrupen al Finance.</span><span class="sxs-lookup"><span data-stu-id="dce02-118">Typically, the project expense categories are mastered in Finance.</span></span> <span data-ttu-id="dce02-119">No obstant, si no ho estan o si ja s'han creat categories de despeses al Project Service Automation, heu de sincronitzar-les abans mitjançant amb la plantilla Categories de transaccions de despeses del projecte (PSA a Fin and Ops).</span><span class="sxs-lookup"><span data-stu-id="dce02-119">However, if they aren't, or if expense categories have already been created in Project Service Automation, you must first synchronize by using the Project expense transaction categories (PSA to Fin and Ops) template.</span></span> <span data-ttu-id="dce02-120">A continuació, sincronitzeu-les mitjançant la plantilla Categories de transacció de despeses del projecte (Fin and Ops a PSA).</span><span class="sxs-lookup"><span data-stu-id="dce02-120">Then synchronize by using the Project expense transaction categories (Fin and Ops to PSA) template.</span></span> <span data-ttu-id="dce02-121">A continuació, hauríeu d'executar la sincronització del Project Service Automation al Finance una vegada més.</span><span class="sxs-lookup"><span data-stu-id="dce02-121">You should then run the synchronization from Project Service Automation to Finance one more time.</span></span>
>
> <span data-ttu-id="dce02-122">Si sincronitzeu en primer lloc des del Project Service Automation, els requisits següents s'han de complir al Finance abans d'executar la sincronització:</span><span class="sxs-lookup"><span data-stu-id="dce02-122">If you synchronize first from Project Service Automation, the following requirements must be met in Finance before the synchronization is run:</span></span>
>
> - <span data-ttu-id="dce02-123">La categoria compartida que coincideix amb la categoria de projecte que s'instal·la al Project Service Automation ha d'existir i s'ha d'habilitar per al **Projecte** i per a la **Despesa**.</span><span class="sxs-lookup"><span data-stu-id="dce02-123">The shared category that matches the project category that is set up in Project Service Automation must exist, and it must be enabled for both **Project** and **Expense**.</span></span>
> - <span data-ttu-id="dce02-124">Per a cada entitat jurídica del Finance que s'ha d'integrar, han d'existir les següents categories de projectes:</span><span class="sxs-lookup"><span data-stu-id="dce02-124">For each Finance legal entity that must be integrated with, the following project categories must exist:</span></span>
>
>     - <span data-ttu-id="dce02-125">**Categoria de projecte** existeix.</span><span class="sxs-lookup"><span data-stu-id="dce02-125">**Project category** exists.</span></span> 
>     - <span data-ttu-id="dce02-126">**Ús a la despesa** està habilitat.</span><span class="sxs-lookup"><span data-stu-id="dce02-126">**Use in Expense** is enabled.</span></span>
>     - <span data-ttu-id="dce02-127">**Actiu al diari** està habilitat.</span><span class="sxs-lookup"><span data-stu-id="dce02-127">**Active in journal** is enabled.</span></span>
>     - <span data-ttu-id="dce02-128">**Tipus de transacció** està definit com a **Despesa**.</span><span class="sxs-lookup"><span data-stu-id="dce02-128">**Transaction type** is set to **Expense**.</span></span>

<span data-ttu-id="dce02-129">A la il·lustració següent es mostren les dades que se sincronitzen entre el Project Service Automation i el Finance.</span><span class="sxs-lookup"><span data-stu-id="dce02-129">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="dce02-130">[![Flux de dades per a la integració de Project Service Automation amb el Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="dce02-130">[![Data flow for Project Service Automation integration with Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span></span>

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a><span data-ttu-id="dce02-131">Sincronització de categories de despeses del projecte del Finance al Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="dce02-131">Project expense category synchronization from Finance to Project Service Automation</span></span>

### <a name="template-and-task"></a><span data-ttu-id="dce02-132">Plantilla i tasca</span><span class="sxs-lookup"><span data-stu-id="dce02-132">Template and task</span></span>

<span data-ttu-id="dce02-133">Per accedir a la plantilla, al centre d'administració del Microsoft Power Apps, seleccioneu **Projectes** i, a continuació, a la cantonada superior dreta, seleccioneu **Nou projecte** per seleccionar les plantilles públiques.</span><span class="sxs-lookup"><span data-stu-id="dce02-133">To access the template, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="dce02-134">La plantilla i la tasca subjacent següents s'utilitzen per sincronitzar les categories de despesa del projecte del Finance al Project Service Automation:</span><span class="sxs-lookup"><span data-stu-id="dce02-134">The following template and underlying task are used to synchronize project expense categories from Finance to Project Service Automation:</span></span>

- <span data-ttu-id="dce02-135">**Nom de la plantilla en la integració de dades**: categories de transaccions de despesa del projecte (Fin and Ops a PSA)</span><span class="sxs-lookup"><span data-stu-id="dce02-135">**Name of the template in Data integration:** Project expense transaction categories (Fin and Ops to PSA)</span></span>
- <span data-ttu-id="dce02-136">**Nom de la tasca del projecte:** sincronització de categories al PSA</span><span class="sxs-lookup"><span data-stu-id="dce02-136">**Name of the task in the project:** Sync categories to PSA</span></span>

### <a name="entity-set"></a><span data-ttu-id="dce02-137">Conjunt d'entitats</span><span class="sxs-lookup"><span data-stu-id="dce02-137">Entity set</span></span>

| <span data-ttu-id="dce02-138">Finance</span><span class="sxs-lookup"><span data-stu-id="dce02-138">Finance</span></span>                           | <span data-ttu-id="dce02-139">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="dce02-139">Project Service Automation</span></span> |
|-----------------------------------|----------------------------|
| <span data-ttu-id="dce02-140">Entitat d'integració per a les categories</span><span class="sxs-lookup"><span data-stu-id="dce02-140">Integration entity for categories</span></span> | <span data-ttu-id="dce02-141">Categories de transacció</span><span class="sxs-lookup"><span data-stu-id="dce02-141">Transaction categories</span></span>     |

### <a name="entity-flow"></a><span data-ttu-id="dce02-142">Flux d'entitat</span><span class="sxs-lookup"><span data-stu-id="dce02-142">Entity flow</span></span>

<span data-ttu-id="dce02-143">Les categories de despesa del projecte estan administrades al Finance i se sincronitzen amb el Project Service Automation com a categories de transacció.</span><span class="sxs-lookup"><span data-stu-id="dce02-143">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="dce02-144">Power Query</span><span class="sxs-lookup"><span data-stu-id="dce02-144">Power Query</span></span>

<span data-ttu-id="dce02-145">Quan estigueu sincronitzant al Project Service Automation, heu d'utilitzar el Microsoft Power Query per a l'Excel per definir el tipus de facturació a la categoria de la transacció.</span><span class="sxs-lookup"><span data-stu-id="dce02-145">When you're synchronizing to Project Service Automation, you must use Microsoft Power Query for Excel to set the billing type on the transaction category.</span></span> <span data-ttu-id="dce02-146">La plantilla Categories de transaccions de despesa del projecte (Fin and Ops a PSA) proporciona una columna i una assignació per defecte.</span><span class="sxs-lookup"><span data-stu-id="dce02-146">The Project expense transaction categories (Fin and Ops to PSA) template provides a default column and mapping.</span></span> <span data-ttu-id="dce02-147">Si creeu una plantilla pròpia, heu d'afegir una columna condicional al Power Query.</span><span class="sxs-lookup"><span data-stu-id="dce02-147">If you create your own template, you must add a conditional column in Power Query.</span></span> <span data-ttu-id="dce02-148">Seguiu aquests passos.</span><span class="sxs-lookup"><span data-stu-id="dce02-148">Follow these steps.</span></span>

1. <span data-ttu-id="dce02-149">Feu clic a la fletxa per obrir l'assignació de la tasca de categories de despesa del projecte a la plantilla Categories de transaccions de despesa del projecte (Fin and Ops a PSA).</span><span class="sxs-lookup"><span data-stu-id="dce02-149">Click the arrow to open the mapping of the project expense categories task in the Project expense transaction categories (Fin and Ops to PSA) template.</span></span>
2. <span data-ttu-id="dce02-150">Feu clic a l'enllaç **Consulta i filtratge avançats** per obrir el Power Query.</span><span class="sxs-lookup"><span data-stu-id="dce02-150">Click the **Advance Query and Filtering** link to open Power Query.</span></span>
2. <span data-ttu-id="dce02-151">Seleccioneu **Afegeix una columna condicional**.</span><span class="sxs-lookup"><span data-stu-id="dce02-151">Select **Add Conditional Column**.</span></span>
3. <span data-ttu-id="dce02-152">Introduïu un nom per a la columna nova, com ara **BillingType**.</span><span class="sxs-lookup"><span data-stu-id="dce02-152">Enter a name for the new column, such as **BillingType**.</span></span>
4. <span data-ttu-id="dce02-153">Introduïu la condició següent: **if CATEGORYID not equal to null then 19235001, Otherwise null**.</span><span class="sxs-lookup"><span data-stu-id="dce02-153">Enter the following condition: **if CATEGORYID not equal to null then 19235001, Otherwise null**.</span></span>
5. <span data-ttu-id="dce02-154">A la columna , feu clic a **D'acord**.</span><span class="sxs-lookup"><span data-stu-id="dce02-154">Click **OK** on the column.</span></span>
6. <span data-ttu-id="dce02-155">Assegureu-vos d'assignar aquesta columna nova a la pàgina assignació.</span><span class="sxs-lookup"><span data-stu-id="dce02-155">Be sure to map this new column on the mapping page.</span></span>

<span data-ttu-id="dce02-156">A la il·lustració següent es mostra un exemple de l'assignació de tasques de plantilla a la integració de dades.</span><span class="sxs-lookup"><span data-stu-id="dce02-156">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="dce02-157">L'assignació mostra la informació de camp que se sincronitzarà del Finance al Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="dce02-157">The mapping shows the field information that will be synchronized from Finance to Project Service Automation.</span></span>

<span data-ttu-id="dce02-158">[![Assignació de plantilla de categoria de despesa al Project Service Automation](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="dce02-158">[![Project expense category to Project Service Automation template mapping](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span></span>

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a><span data-ttu-id="dce02-159">Sincronització de categories de despeses del projecte del Project Service Automation al Finance</span><span class="sxs-lookup"><span data-stu-id="dce02-159">Project expense category synchronization from Project Service Automation to Finance</span></span>

### <a name="template-and-task"></a><span data-ttu-id="dce02-160">Plantilla i tasca</span><span class="sxs-lookup"><span data-stu-id="dce02-160">Template and task</span></span>

<span data-ttu-id="dce02-161">La plantilla i la tasca subjacent següents s'utilitzen per sincronitzar les categories de despesa del projecte del Project Service Automation al Finance:</span><span class="sxs-lookup"><span data-stu-id="dce02-161">The following template and underlying task are used to synchronize project expense categories from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="dce02-162">**Nom de la plantilla en la integració de dades**: categories de transaccions de despesa del projecte (PSA a Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="dce02-162">**Name of the template in Data integration:** Project expense transaction categories (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="dce02-163">**Nom de la tasca del projecte:** sincronització de categories al Fin Ops</span><span class="sxs-lookup"><span data-stu-id="dce02-163">**Name of the task in the project:** Sync categories to Fin Ops</span></span>

### <a name="entity-set"></a><span data-ttu-id="dce02-164">Conjunt d'entitats</span><span class="sxs-lookup"><span data-stu-id="dce02-164">Entity set</span></span>

| <span data-ttu-id="dce02-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="dce02-165">Project Service Automation</span></span> | <span data-ttu-id="dce02-166">Finance</span><span class="sxs-lookup"><span data-stu-id="dce02-166">Finance</span></span>                           |
|----------------------------|-----------------------------------|
| <span data-ttu-id="dce02-167">Categories de transacció</span><span class="sxs-lookup"><span data-stu-id="dce02-167">Transaction categories</span></span>     | <span data-ttu-id="dce02-168">Entitat d'integració per a les categories</span><span class="sxs-lookup"><span data-stu-id="dce02-168">Integration entity for categories</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="dce02-169">Flux d'entitat</span><span class="sxs-lookup"><span data-stu-id="dce02-169">Entity flow</span></span>

<span data-ttu-id="dce02-170">Les categories de despesa del projecte estan administrades al Finance i se sincronitzen amb el Project Service Automation com a categories de transacció.</span><span class="sxs-lookup"><span data-stu-id="dce02-170">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span> <span data-ttu-id="dce02-171">L'actualització al Finance actualitza la categoria del projecte al Finance amb l'identificador d'integració del Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="dce02-171">The synchronization back to Finance updates the project category in Finance with the integration ID from Project Service Automation.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="dce02-172">Assignació de plantilles a la integració de dades</span><span class="sxs-lookup"><span data-stu-id="dce02-172">Template mapping in Data integration</span></span>

<span data-ttu-id="dce02-173">A la il·lustració següent es mostra un exemple de l'assignació de tasques de plantilla a la integració de dades.</span><span class="sxs-lookup"><span data-stu-id="dce02-173">The following illustration shows an example of the template task mapping in Data integration.</span></span>

> [!NOTE]
> <span data-ttu-id="dce02-174">L'assignació mostra la informació de camp que se sincronitzarà del Project Service Automation al Finance.</span><span class="sxs-lookup"><span data-stu-id="dce02-174">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="dce02-175">[![Assignació de plantilla del Project Service Automation al Finance](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="dce02-175">[![Project Service Automation to Finance template mapping](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]