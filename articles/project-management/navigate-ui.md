---
title: Navegació per la interfície d'usuari
description: En aquest tema es proporciona informació sobre la funcionalitat d'administració de projectes al Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: ff624a13ec88ae64dba18715fbe9b94353b070e8
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072130"
---
# <a name="navigating-the-user-interface"></a><span data-ttu-id="a3adc-103">Navegació per la interfície d'usuari</span><span class="sxs-lookup"><span data-stu-id="a3adc-103">Navigating the user interface</span></span>

<span data-ttu-id="a3adc-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_</span><span class="sxs-lookup"><span data-stu-id="a3adc-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

## <a name="overview"></a><span data-ttu-id="a3adc-105">Informació general</span><span class="sxs-lookup"><span data-stu-id="a3adc-105">Overview</span></span>

<span data-ttu-id="a3adc-106">El formulari principal del projecte està separat en diverses pestanyes.</span><span class="sxs-lookup"><span data-stu-id="a3adc-106">The main project form is separated into several tabs.</span></span> <span data-ttu-id="a3adc-107">Cada pestanya representa un nivell de detall diferent dins del projecte.</span><span class="sxs-lookup"><span data-stu-id="a3adc-107">Each tab represents a different level of detail within the project.</span></span>

- <span data-ttu-id="a3adc-108">**Resum** : proporciona una descripció del projecte i agrega el rendiment del projecte real i planificat.</span><span class="sxs-lookup"><span data-stu-id="a3adc-108">**Summary** : Provides a description of the project and aggregates both the planned and actual project performance.</span></span>

    ![Pestanya Resum i camps](media/navigation7.png)

- <span data-ttu-id="a3adc-110">**Tasques** : proporciona els detalls quant a l'estructura del desglossament del treball representada per una visualització de quadrícula, visualització de tauler i gràfic de Gantt.</span><span class="sxs-lookup"><span data-stu-id="a3adc-110">**Tasks** : Provides the details regarding the work breakdown structure represented by a grid view, board view, and a gantt.</span></span>

    ![Pestanya Tasques i camps](media/navigation8.png)

- <span data-ttu-id="a3adc-112">**Equip** : proporciona detalls relacionats amb els participants del projecte.</span><span class="sxs-lookup"><span data-stu-id="a3adc-112">**Team** : Provides details regarding the project participants.</span></span> <span data-ttu-id="a3adc-113">L'esforç assignat de cada membre de l'equip també es resumeix en aquesta visualització.</span><span class="sxs-lookup"><span data-stu-id="a3adc-113">The assigned effort of each team member is also summarized in this view.</span></span>

    ![Pestanya Equip i camps](media/navigation9.png)

- <span data-ttu-id="a3adc-115">**Assignacions de recursos** : proporciona una visualització per hores de l'esforç per a cada recurs d'un projecte.</span><span class="sxs-lookup"><span data-stu-id="a3adc-115">**Resource assignments** : Provides a time-phased view of the effort for each resource on a project.</span></span>

    ![Pestanya Assignacions de recursos i camps](media/navigation10.png)

- <span data-ttu-id="a3adc-117">**Conciliació de recursos** : proporciona una visualització per hores de les diferències entre les assignacions de cadascun dels recursos amb nom i les seves reserves.</span><span class="sxs-lookup"><span data-stu-id="a3adc-117">**Resource reconciliation** : Provides a time-phased view of the differences between the assignments of each named resource and their bookings.</span></span>

    ![Pestanya Conciliació de recursos i camps](media/navigation11.png)

- <span data-ttu-id="a3adc-119">**Estimacions** : proporciona una visualització per hores de les estimacions de costos i vendes d'un projecte.</span><span class="sxs-lookup"><span data-stu-id="a3adc-119">**Estimates** : Provides a time-phased view of the cost and sales estimates of a project.</span></span>

    ![Pestanya Estimacions i camps](media/navigation12.png)

- <span data-ttu-id="a3adc-121">**Seguiment** : proporciona una visualització que mostra el progrés de les tasques a l'estructura del desglossament del treball per a l'esforç, el cost i les vendes.</span><span class="sxs-lookup"><span data-stu-id="a3adc-121">**Tracking** : Provides a view that shows the progress of tasks in the work breakdown structure for effort, cost, and sales.</span></span>

    ![Pestanya Seguiment i camps](media/navigation13.png)

- <span data-ttu-id="a3adc-123">**Vendes** : proporciona enllaços profunds a les ofertes i als contractes associats amb el projecte.</span><span class="sxs-lookup"><span data-stu-id="a3adc-123">**Sales** : Provides deep links to quotes and contracts associated with the project.</span></span>

- <span data-ttu-id="a3adc-124">**Estimacions de despeses** : proporciona una quadrícula que defineix les despeses del projecte basades en les categories de despeses de l'organització.</span><span class="sxs-lookup"><span data-stu-id="a3adc-124">**Expense Estimates** : Provides a grid that defines project expenses based upon organizational expense categories.</span></span>

    ![Pestanya Estimacions de despeses i camps](media/navigation14.png)

## <a name="grid-controls"></a><span data-ttu-id="a3adc-126">Controls de quadrícula</span><span class="sxs-lookup"><span data-stu-id="a3adc-126">Grid controls</span></span>

<span data-ttu-id="a3adc-127">La continuació es mostra una descripció general breu dels controls típics que trobareu a les diferents pestanyes de planificació de projectes.</span><span class="sxs-lookup"><span data-stu-id="a3adc-127">The follow is a brief overview of the typical controls found on the various project planning tabs.</span></span>

### <a name="refresh"></a><span data-ttu-id="a3adc-128">Permet fer l'actualització</span><span class="sxs-lookup"><span data-stu-id="a3adc-128">Refresh</span></span>

<span data-ttu-id="a3adc-129">**Actualitza** : recupera les dades més recents del servidor si s'han produït canvis després de carregar-se la quadrícula.</span><span class="sxs-lookup"><span data-stu-id="a3adc-129">**Refresh** : Retrieves the latest data from the server if any changes occurred after the grid was loaded.</span></span>

![Botó Actualitza](media/navigation7.png)

### <a name="group-by"></a><span data-ttu-id="a3adc-131">Agrupa per</span><span class="sxs-lookup"><span data-stu-id="a3adc-131">Group by</span></span>

<span data-ttu-id="a3adc-132">**Agrupa per** : actualitza l'agrupament de les files de la quadrícula per reflectir els recursos, les funcions o les categories en funció de les necessitats de l'usuari.</span><span class="sxs-lookup"><span data-stu-id="a3adc-132">**Group by** : Updates the grouping of the rows in the grid to reflect either resources, roles, or categories based on the user's needs.</span></span>

![Botó Agrupa per](media/navigation6.png)

### <a name="previousnext"></a><span data-ttu-id="a3adc-134">Anterior/Següent</span><span class="sxs-lookup"><span data-stu-id="a3adc-134">Previous/Next</span></span>

<span data-ttu-id="a3adc-135">**Anterior**/**Següent** : actualitza els períodes de temps visibles a les quadrícules per temps.</span><span class="sxs-lookup"><span data-stu-id="a3adc-135">**Previous**/**Next** : Update the visible time periods on the time-phased grids.</span></span>

![Botons Anterior i Següent](media/navigation2.png)

### <a name="timescale"></a><span data-ttu-id="a3adc-137">Escala de temps</span><span class="sxs-lookup"><span data-stu-id="a3adc-137">Timescale</span></span>

<span data-ttu-id="a3adc-138">**Cronograma** : canvia l'agregació de les dades per temps entre dies, setmanes, mesos i anys.</span><span class="sxs-lookup"><span data-stu-id="a3adc-138">**Timescale** : Change the aggregation of the time-phased data between days, weeks, months, and years.</span></span>

![Botó Cronograma](media/navigation3.png)

### <a name="expand"></a><span data-ttu-id="a3adc-140">Amplia</span><span class="sxs-lookup"><span data-stu-id="a3adc-140">Expand</span></span>

<span data-ttu-id="a3adc-141">**Expandeix** : representa la quadrícula visible a pantalla completa i proporciona més capacitat per veure les funcions addicionals.</span><span class="sxs-lookup"><span data-stu-id="a3adc-141">**Expand** : Render the visible grid to full screen providing more ability to see additional roles.</span></span>

![botó Expandeix](media/navigation4.png)

### <a name="time-phase-by"></a><span data-ttu-id="a3adc-143">Fase de temps per</span><span class="sxs-lookup"><span data-stu-id="a3adc-143">Time-phase by</span></span>

<span data-ttu-id="a3adc-144">**Fase de temps per** : actualitza l'agrupament de les files de la quadrícula per reflectir les estimacions de costos per a les estimacions de vendes.</span><span class="sxs-lookup"><span data-stu-id="a3adc-144">**Time-phase by** : Update the grouping of the rows in the grid to reflect cost estimates for sales estimates.</span></span> <span data-ttu-id="a3adc-145">Aquest control també s'aplica al script d'estimació i a la quadrícula de seguiment.</span><span class="sxs-lookup"><span data-stu-id="a3adc-145">This control also applies to the estimate script and the tracking grid.</span></span>

![Botó Fase de temps per](media/navigation0.png)

### <a name="add-column"></a><span data-ttu-id="a3adc-147">Afegeix una columna</span><span class="sxs-lookup"><span data-stu-id="a3adc-147">Add column</span></span>

<span data-ttu-id="a3adc-148">**Afegeix una columna** : permet a l'usuari definir les columnes visibles a la quadrícula.</span><span class="sxs-lookup"><span data-stu-id="a3adc-148">**Add column** : Allows the user to define the visible columns in the grid.</span></span> <span data-ttu-id="a3adc-149">Només es poden afegir columnes de fàbrica a les quadrícules del formulari **Planificació del projecte**.</span><span class="sxs-lookup"><span data-stu-id="a3adc-149">Only out-of-the-box columns can be added to the grids in the **Project Planning** form.</span></span>

![Botó Afegeix una columna](media/navigation5.png)
