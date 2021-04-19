---
title: Configuració dels components facturables d'una línia de contracte basada en projectes
description: Aquest tema proporciona informació sobre com afegir components imputables a les línies de contracte al Project Operations.
author: rumant
manager: Annbe
ms.date: 10/08/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ddada2cb412ba7370fb0a750325a84772937d8d0
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858461"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a><span data-ttu-id="d65cc-103">Configuració dels components facturables d'una línia de contracte basada en projectes</span><span class="sxs-lookup"><span data-stu-id="d65cc-103">Configure chargeable components of a project-based contract line</span></span>

<span data-ttu-id="d65cc-104">_**S'aplica a:** Implementació bàsica: tracte de facturació proforma, Project Operations per a escenaris basats en recursos/sense cotització_</span><span class="sxs-lookup"><span data-stu-id="d65cc-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="d65cc-105">Una línia de contracte basada en projectes té components *inclosos* i components *imputables*.</span><span class="sxs-lookup"><span data-stu-id="d65cc-105">A project-based contract line has *included* components and *chargeable* components.</span></span>

<span data-ttu-id="d65cc-106">Els components inclosos són els que estan subjectes a:</span><span class="sxs-lookup"><span data-stu-id="d65cc-106">Included components are components that are subject to:</span></span>

  - <span data-ttu-id="d65cc-107">Mètode de facturació i desglossament del client</span><span class="sxs-lookup"><span data-stu-id="d65cc-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="d65cc-108">Límits que no s'han de superar</span><span class="sxs-lookup"><span data-stu-id="d65cc-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="d65cc-109">Paràmetres de freqüència de facturació definits a la línia de contracte basada en projectes</span><span class="sxs-lookup"><span data-stu-id="d65cc-109">Invoice frequency settings defined on the project-based contract line</span></span>

<span data-ttu-id="d65cc-110">Un subconjunt dels components inclosos es pot marcar com a imputable mitjançant el camp **Tipus de facturació**.</span><span class="sxs-lookup"><span data-stu-id="d65cc-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="d65cc-111">El camp **Tipus de facturació** és un conjunt d'opcions que permet els següents valors en el context d'una línia de contracte:</span><span class="sxs-lookup"><span data-stu-id="d65cc-111">The **Billing Type** field is an option-set that allows the following values in the context of a contract line:</span></span>

  - <span data-ttu-id="d65cc-112">Imputable</span><span class="sxs-lookup"><span data-stu-id="d65cc-112">Chargeable</span></span>
  - <span data-ttu-id="d65cc-113">No imputable</span><span class="sxs-lookup"><span data-stu-id="d65cc-113">Non-chargeable</span></span>

<span data-ttu-id="d65cc-114">Els components imputables es poden definir en tasques, rols i categories de transacció.</span><span class="sxs-lookup"><span data-stu-id="d65cc-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="d65cc-115">La imputabilitat es defineix en les tasques d'una línia de contracte de projecte i s'aplica a totes les classes de transacció incloses a la línia.</span><span class="sxs-lookup"><span data-stu-id="d65cc-115">Chargeability is defined on tasks for a project contract line and applies to all transaction classes included on the line.</span></span> <span data-ttu-id="d65cc-116">Si el camp **Inclou les tasques** d'una línia de contracte és buit o s'ha establert a **Tot el projecte**, la pestanya **Tasques imputables** no estarà disponible.</span><span class="sxs-lookup"><span data-stu-id="d65cc-116">If the **Include Tasks** field on a contract line is blank or set to **Entire project**, the **Chargeable tasks** tab will not be available.</span></span>

<span data-ttu-id="d65cc-117">La imputabilitat definida a les funcions d'una línia de contracte de projecte només s'aplica a la classe de transacció **Temps**.</span><span class="sxs-lookup"><span data-stu-id="d65cc-117">Chargeability defined on roles for a project contract line only applies to the **Time** transaction class.</span></span> <span data-ttu-id="d65cc-118">Si el camp **Inclou el temps** d'una línia de contracte és buit o s'ha establert a **No**, la pestanya **Funcions imputables** no estarà disponible.</span><span class="sxs-lookup"><span data-stu-id="d65cc-118">If the **Include Time** field on a contract line is set to **No**, the **Chargeable roles** tab will not be available.</span></span>

<span data-ttu-id="d65cc-119">La imputabilitat definida a les categories de transacció d'una línia de contracte de projecte només s'aplica a la classe de transacció **Despesa**.</span><span class="sxs-lookup"><span data-stu-id="d65cc-119">Chargeability defined on transaction categories for a project contract line only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="d65cc-120">Si el camp **Inclou les despeses** s'ha establert a **No**, la pestanya **Categories imputables** no estarà disponible.</span><span class="sxs-lookup"><span data-stu-id="d65cc-120">If the **Include Expenses** field is set to **No**, the **Chargeable Categories** tab will not be available.</span></span>

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a><span data-ttu-id="d65cc-121">Actualitzar una tasca de projecte com a imputable o no imputable</span><span class="sxs-lookup"><span data-stu-id="d65cc-121">Update a project task as chargeable or non-chargeable</span></span>

<span data-ttu-id="d65cc-122">Una tasca de projecte pot ser imputable o no imputable en una línia de contracte específica, cosa que fa possible la configuració següent:</span><span class="sxs-lookup"><span data-stu-id="d65cc-122">A project task can be chargeable or non-chargeable on a specific contract line, which makes the following setup possible:</span></span>

<span data-ttu-id="d65cc-123">Si una línia de contracte basada en el projecte inclou **Temps** i una tasca determinada, **T1** s'hi associa com a imputable.</span><span class="sxs-lookup"><span data-stu-id="d65cc-123">If a project-based contract line includes **Time** and a certain task, **T1** is associated to it as chargeable.</span></span> <span data-ttu-id="d65cc-124">Si hi ha una segona línia de contracte que inclou **Despesa**, es pot associar la tasca T1 a la línia de contracte com a no imputable.</span><span class="sxs-lookup"><span data-stu-id="d65cc-124">If there is a second contract line that includes **Expense**, you can associate the T1 task on the contract line as non-chargeable.</span></span> <span data-ttu-id="d65cc-125">El resultat és que tot el temps que es registra en la tasca és imputable i totes les despeses no són imputables.</span><span class="sxs-lookup"><span data-stu-id="d65cc-125">The result is that all of the time recorded on the task is chargeable and all expenses are non-chargeable.</span></span>

<span data-ttu-id="d65cc-126">El tipus de facturació d'una tasca es pot configurar a la pestanya **Tasques imputables** de la línia de contracte actualitzant el camp **Tipus de facturació** a la subquadrícula de tasques de la línia de contracte.</span><span class="sxs-lookup"><span data-stu-id="d65cc-126">A task's billing type can be configured on the **Chargeable Tasks** tab of the contract line by updating the **Billing Type** field on the contract line tasks subgrid.</span></span> <span data-ttu-id="d65cc-127">Alternativament, podeu actualitzar el camp **Tipus de facturació** a la subquadrícula de la Configuració de facturació de la tasca d'un projecte que mostra les línies de contracte associades a una tasca.</span><span class="sxs-lookup"><span data-stu-id="d65cc-127">Alternatively, you can update the **Billing Type** field on the subgrid of the task Billing setup of a project that shows the contract lines associated to a task.</span></span>

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a><span data-ttu-id="d65cc-128">Actualitzar una funció com a imputable o no imputable</span><span class="sxs-lookup"><span data-stu-id="d65cc-128">Update a role as chargeable or non-chargeable</span></span>

<span data-ttu-id="d65cc-129">Una funció pot ser imputable o no imputable en una línia de contracte específica.</span><span class="sxs-lookup"><span data-stu-id="d65cc-129">A role can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="d65cc-130">El tipus de facturació d'una funció es pot configurar a la pestanya **Funcions imputables** d'una línia de contracte.</span><span class="sxs-lookup"><span data-stu-id="d65cc-130">A role's billing type can be configured on the **Chargeable Roles** tab of a contract line.</span></span> <span data-ttu-id="d65cc-131">Per fer-ho, actualitzeu el camp **Tipus de facturació** de la subquadrícula **Funcions imputables**.</span><span class="sxs-lookup"><span data-stu-id="d65cc-131">To do this, update the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a><span data-ttu-id="d65cc-132">Actualitzar una categoria de transacció com a imputable o no imputable</span><span class="sxs-lookup"><span data-stu-id="d65cc-132">Update a transaction category as chargeable or non-chargeable</span></span>

<span data-ttu-id="d65cc-133">Una categoria de transacció pot ser imputable o no imputable en una línia de contracte específica.</span><span class="sxs-lookup"><span data-stu-id="d65cc-133">A transaction category can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="d65cc-134">El tipus de facturació d'una transacció es pot configurar a la pestanya **Categories imputables** d'una línia de contracte basada en projectes.</span><span class="sxs-lookup"><span data-stu-id="d65cc-134">A transaction's billing type can be configured on the **Chargeable Categories** tab of a project-based contract line.</span></span> <span data-ttu-id="d65cc-135">Per fer-ho, actualitzeu el camp **Tipus de facturació** de la subquadrícula **Categories imputables**.</span><span class="sxs-lookup"><span data-stu-id="d65cc-135">To do this, update the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="d65cc-136">Resoldre la imputabilitat</span><span class="sxs-lookup"><span data-stu-id="d65cc-136">Resolve chargeability</span></span>

<span data-ttu-id="d65cc-137">Una estimació o un valor real creat per a temps només es consideraran imputables si:</span><span class="sxs-lookup"><span data-stu-id="d65cc-137">An estimate or actual created for time is only considered chargeable if:</span></span>

   - <span data-ttu-id="d65cc-138">El **Temps** s'inclou a la línia de contracte.</span><span class="sxs-lookup"><span data-stu-id="d65cc-138">**Time** is included on the contract line.</span></span>
   - <span data-ttu-id="d65cc-139">La **Funció** està configurada com a imputable a la línia de contracte.</span><span class="sxs-lookup"><span data-stu-id="d65cc-139">**Role** is configured as chargeable on the contract line.</span></span>
   - <span data-ttu-id="d65cc-140">**Tasques incloses** està establert com a **Tasques seleccionades** a la línia de contracte.</span><span class="sxs-lookup"><span data-stu-id="d65cc-140">**Included Tasks** is set to **Selected tasks** on the contract line.</span></span>
 
 <span data-ttu-id="d65cc-141">Si aquestes tres coses són certes, la tasca es configura com a imputable.</span><span class="sxs-lookup"><span data-stu-id="d65cc-141">If these three things are true, the task is configured as chargeable.</span></span> 

<span data-ttu-id="d65cc-142">Una estimació o un valor real creats per a despeses només es consideraran imputables si:</span><span class="sxs-lookup"><span data-stu-id="d65cc-142">An estimate or actual created for expense is only considered chargeable if:</span></span>

   - <span data-ttu-id="d65cc-143">La **Despesa** s'inclou a la línia de contracte.</span><span class="sxs-lookup"><span data-stu-id="d65cc-143">**Expense** is included on the contract line</span></span>
   - <span data-ttu-id="d65cc-144">**Categoria de transacció** està configurat com a imputable a la línia de contracte.</span><span class="sxs-lookup"><span data-stu-id="d65cc-144">**Transaction category** is configured as chargeable on the contract line</span></span>
   - <span data-ttu-id="d65cc-145">**Tasques incloses** està establert com a **Tasca seleccionada** a la línia de contracte</span><span class="sxs-lookup"><span data-stu-id="d65cc-145">**Included Tasks** is set to **Selected task** on the contract line</span></span>
  
 <span data-ttu-id="d65cc-146">Si aquestes tres coses són certes, la **Tasca** es configura com a imputable.</span><span class="sxs-lookup"><span data-stu-id="d65cc-146">If these three things are true, the **Task** is configured as chargeable.</span></span> 

<span data-ttu-id="d65cc-147">Una estimació o un valor real creats per a materials només es consideraran imputables si:</span><span class="sxs-lookup"><span data-stu-id="d65cc-147">An estimate or actual created for material is only considered chargeable if:</span></span>

   - <span data-ttu-id="d65cc-148">**Materials** s'inclou a la línia de contracte</span><span class="sxs-lookup"><span data-stu-id="d65cc-148">**Materials** is included on the contract line</span></span>
   - <span data-ttu-id="d65cc-149">**Tasques incloses** està establert com a **Tasques seleccionades** a la línia de contracte</span><span class="sxs-lookup"><span data-stu-id="d65cc-149">**Included Tasks** is set to **Selected tasks** on the contract line</span></span>

<span data-ttu-id="d65cc-150">Si aquestes dues coses són certes, la **Tasca** es configura com a imputable.</span><span class="sxs-lookup"><span data-stu-id="d65cc-150">If these two things are true, the **Task** is configured as chargeable.</span></span> 

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="d65cc-151">
                    <strong>Inclou el temps</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d65cc-151">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="d65cc-152">
                    <strong>Inclou les despeses</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="d65cc-152">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="d65cc-153">
                    <strong>Inclou materials</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="d65cc-153">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="d65cc-154">
                    <strong>Tasques incloses</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="d65cc-154">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="d65cc-155">
                    <strong>Funció</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="d65cc-155">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="d65cc-156">
                    <strong>Categoria</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="d65cc-156">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="d65cc-157">
                    <strong>Tasca</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="d65cc-157">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="d65cc-158">
                    <strong>Impacte de la imputabilitat</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d65cc-158">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d65cc-159">Sí</span><span class="sxs-lookup"><span data-stu-id="d65cc-159">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="d65cc-160">Sí</span><span class="sxs-lookup"><span data-stu-id="d65cc-160">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="d65cc-161">Sí</span><span class="sxs-lookup"><span data-stu-id="d65cc-161">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="d65cc-162">Tot el projecte</span><span class="sxs-lookup"><span data-stu-id="d65cc-162">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d65cc-163">Imputable</span><span class="sxs-lookup"><span data-stu-id="d65cc-163">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d65cc-164">Imputable</span><span class="sxs-lookup"><span data-stu-id="d65cc-164">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d65cc-165">No es pot establir</span><span class="sxs-lookup"><span data-stu-id="d65cc-165">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="d65cc-166">Facturació en un valor real de temps: <strong>Imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d65cc-166">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="d65cc-167">Tipus de facturació en un valor real de despesa: <strong>Imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d65cc-167">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="d65cc-168">Tipus de facturació del material real: <strong>Imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d65cc-168">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d65cc-169">Sí</span><span class="sxs-lookup"><span data-stu-id="d65cc-169">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="d65cc-170">Sí</span><span class="sxs-lookup"><span data-stu-id="d65cc-170">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="d65cc-171">Sí</span><span class="sxs-lookup"><span data-stu-id="d65cc-171">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="d65cc-172">Només les tasques seleccionades</span><span class="sxs-lookup"><span data-stu-id="d65cc-172">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d65cc-173">Imputable</span><span class="sxs-lookup"><span data-stu-id="d65cc-173">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d65cc-174">Imputable</span><span class="sxs-lookup"><span data-stu-id="d65cc-174">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d65cc-175">Imputable</span><span class="sxs-lookup"><span data-stu-id="d65cc-175">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="d65cc-176">Facturació en un valor real de temps: <strong>Imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d65cc-176">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="d65cc-177">Tipus de facturació en un valor real de despesa: <strong>Imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d65cc-177">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="d65cc-178">Tipus de facturació del material real: <strong>Imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d65cc-178">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d65cc-179">Sí</span><span class="sxs-lookup"><span data-stu-id="d65cc-179">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="d65cc-180">Sí</span><span class="sxs-lookup"><span data-stu-id="d65cc-180">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="d65cc-181">Sí</span><span class="sxs-lookup"><span data-stu-id="d65cc-181">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="d65cc-182">Només les tasques seleccionades</span><span class="sxs-lookup"><span data-stu-id="d65cc-182">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="d65cc-183">
                    <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d65cc-183">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d65cc-184">Imputable</span><span class="sxs-lookup"><span data-stu-id="d65cc-184">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d65cc-185">Imputable</span><span class="sxs-lookup"><span data-stu-id="d65cc-185">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="d65cc-186">Facturació en un valor real de temps: <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d65cc-186">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="d65cc-187">Tipus de facturació en un valor real de despesa: Imputable</span><span class="sxs-lookup"><span data-stu-id="d65cc-187">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="d65cc-188">Tipus de facturació del material real: imputable</span><span class="sxs-lookup"><span data-stu-id="d65cc-188">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d65cc-189">Sí</span><span class="sxs-lookup"><span data-stu-id="d65cc-189">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="d65cc-190">Sí</span><span class="sxs-lookup"><span data-stu-id="d65cc-190">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="d65cc-191">Sí</span><span class="sxs-lookup"><span data-stu-id="d65cc-191">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="d65cc-192">Només les tasques seleccionades</span><span class="sxs-lookup"><span data-stu-id="d65cc-192">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d65cc-193">Imputable</span><span class="sxs-lookup"><span data-stu-id="d65cc-193">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d65cc-194">Imputable</span><span class="sxs-lookup"><span data-stu-id="d65cc-194">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="d65cc-195">
                    <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d65cc-195">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="d65cc-196">Facturació en un valor real de temps: <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d65cc-196">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="d65cc-197">Tipus de facturació en un valor real de despesa: <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d65cc-197">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="d65cc-198">Tipus de facturació en un valor real de material: <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d65cc-198">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d65cc-199">Sí</span><span class="sxs-lookup"><span data-stu-id="d65cc-199">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="d65cc-200">Sí</span><span class="sxs-lookup"><span data-stu-id="d65cc-200">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="d65cc-201">Sí</span><span class="sxs-lookup"><span data-stu-id="d65cc-201">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="d65cc-202">Només les tasques seleccionades</span><span class="sxs-lookup"><span data-stu-id="d65cc-202">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="d65cc-203">
                    <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d65cc-203">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d65cc-204">Imputable</span><span class="sxs-lookup"><span data-stu-id="d65cc-204">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="d65cc-205">
                    <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d65cc-205">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="d65cc-206">Facturació en un valor real de temps: <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d65cc-206">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="d65cc-207">Tipus de facturació en un valor real de despesa: <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d65cc-207">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="d65cc-208">Tipus de facturació en un valor real de material: <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d65cc-208">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d65cc-209">Sí</span><span class="sxs-lookup"><span data-stu-id="d65cc-209">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="d65cc-210">Sí</span><span class="sxs-lookup"><span data-stu-id="d65cc-210">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="d65cc-211">Sí</span><span class="sxs-lookup"><span data-stu-id="d65cc-211">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="d65cc-212">Només les tasques seleccionades</span><span class="sxs-lookup"><span data-stu-id="d65cc-212">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="d65cc-213">
                    <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d65cc-213">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="d65cc-214">
                    <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d65cc-214">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d65cc-215">Imputable</span><span class="sxs-lookup"><span data-stu-id="d65cc-215">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="d65cc-216">Facturació en un valor real de temps: <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d65cc-216">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="d65cc-217">Tipus de facturació en un valor real de despesa: <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d65cc-217">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="d65cc-218">Tipus de facturació del material real: imputable</span><span class="sxs-lookup"><span data-stu-id="d65cc-218">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="d65cc-219">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d65cc-219">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="d65cc-220">Sí</span><span class="sxs-lookup"><span data-stu-id="d65cc-220">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="d65cc-221">Sí</span><span class="sxs-lookup"><span data-stu-id="d65cc-221">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="d65cc-222">Tot el projecte</span><span class="sxs-lookup"><span data-stu-id="d65cc-222">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d65cc-223">No es pot establir</span><span class="sxs-lookup"><span data-stu-id="d65cc-223">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="d65cc-224">
                    <strong>Imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d65cc-224">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d65cc-225">No es pot establir</span><span class="sxs-lookup"><span data-stu-id="d65cc-225">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="d65cc-226">Facturació en un valor real de temps: <strong>No disponible</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d65cc-226">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="d65cc-227">Tipus de facturació en un valor real de despesa: Imputable</span><span class="sxs-lookup"><span data-stu-id="d65cc-227">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="d65cc-228">Tipus de facturació del material real: imputable</span><span class="sxs-lookup"><span data-stu-id="d65cc-228">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="d65cc-229">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d65cc-229">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="d65cc-230">Sí</span><span class="sxs-lookup"><span data-stu-id="d65cc-230">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="d65cc-231">Sí</span><span class="sxs-lookup"><span data-stu-id="d65cc-231">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="d65cc-232">Tot el projecte</span><span class="sxs-lookup"><span data-stu-id="d65cc-232">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d65cc-233">No es pot establir</span><span class="sxs-lookup"><span data-stu-id="d65cc-233">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="d65cc-234">
                    <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d65cc-234">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d65cc-235">No es pot establir</span><span class="sxs-lookup"><span data-stu-id="d65cc-235">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="d65cc-236">Facturació en un valor real de temps: <strong>No disponible</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d65cc-236">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="d65cc-237">Tipus de facturació en un valor real de despesa: <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d65cc-237">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="d65cc-238">Tipus de facturació del material real: imputable</span><span class="sxs-lookup"><span data-stu-id="d65cc-238">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d65cc-239">Sí</span><span class="sxs-lookup"><span data-stu-id="d65cc-239">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="d65cc-240">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d65cc-240">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="d65cc-241">Sí</span><span class="sxs-lookup"><span data-stu-id="d65cc-241">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="d65cc-242">Tot el projecte</span><span class="sxs-lookup"><span data-stu-id="d65cc-242">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d65cc-243">Imputable</span><span class="sxs-lookup"><span data-stu-id="d65cc-243">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d65cc-244">No es pot establir</span><span class="sxs-lookup"><span data-stu-id="d65cc-244">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d65cc-245">No es pot establir</span><span class="sxs-lookup"><span data-stu-id="d65cc-245">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="d65cc-246">Facturació en un valor real de temps: Imputable</span><span class="sxs-lookup"><span data-stu-id="d65cc-246">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="d65cc-247">Tipus de facturació en un valor real de despesa: <strong>No disponible</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d65cc-247">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="d65cc-248">Tipus de facturació del material real: imputable</span><span class="sxs-lookup"><span data-stu-id="d65cc-248">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d65cc-249">Sí</span><span class="sxs-lookup"><span data-stu-id="d65cc-249">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="d65cc-250">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d65cc-250">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="d65cc-251">Sí</span><span class="sxs-lookup"><span data-stu-id="d65cc-251">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="d65cc-252">Tot el projecte</span><span class="sxs-lookup"><span data-stu-id="d65cc-252">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="d65cc-253">
                    <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d65cc-253">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d65cc-254">No es pot establir</span><span class="sxs-lookup"><span data-stu-id="d65cc-254">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d65cc-255">No es pot establir</span><span class="sxs-lookup"><span data-stu-id="d65cc-255">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="d65cc-256">Facturació en un valor real de temps: <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d65cc-256">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="d65cc-257">Tipus de facturació en un valor real de despesa: <strong>No disponible</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d65cc-257">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="d65cc-258">Tipus de facturació del material real: imputable</span><span class="sxs-lookup"><span data-stu-id="d65cc-258">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d65cc-259">Sí</span><span class="sxs-lookup"><span data-stu-id="d65cc-259">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="d65cc-260">Sí</span><span class="sxs-lookup"><span data-stu-id="d65cc-260">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="d65cc-261">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d65cc-261">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="d65cc-262">Tot el projecte</span><span class="sxs-lookup"><span data-stu-id="d65cc-262">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d65cc-263">Imputable</span><span class="sxs-lookup"><span data-stu-id="d65cc-263">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d65cc-264">Imputable</span><span class="sxs-lookup"><span data-stu-id="d65cc-264">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d65cc-265">No es pot establir</span><span class="sxs-lookup"><span data-stu-id="d65cc-265">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="d65cc-266">Facturació en un valor real de temps: Imputable</span><span class="sxs-lookup"><span data-stu-id="d65cc-266">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="d65cc-267">Tipus de facturació en un valor real de despesa: Imputable</span><span class="sxs-lookup"><span data-stu-id="d65cc-267">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="d65cc-268">Tipus de facturació en un valor real de material: <strong>No disponible</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d65cc-268">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d65cc-269">Sí</span><span class="sxs-lookup"><span data-stu-id="d65cc-269">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="d65cc-270">Sí</span><span class="sxs-lookup"><span data-stu-id="d65cc-270">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="d65cc-271">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d65cc-271">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="d65cc-272">Tot el projecte</span><span class="sxs-lookup"><span data-stu-id="d65cc-272">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="d65cc-273">
                    <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d65cc-273">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="d65cc-274">
                    <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d65cc-274">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d65cc-275">No es pot establir</span><span class="sxs-lookup"><span data-stu-id="d65cc-275">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="d65cc-276">Facturació en un valor real de temps: <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d65cc-276">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="d65cc-277">Tipus de facturació en un valor real de despesa: <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d65cc-277">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="d65cc-278">Tipus de facturació en un valor real de material: <strong>No disponible</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d65cc-278">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
