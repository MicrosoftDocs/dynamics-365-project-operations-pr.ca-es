---
title: Configuració dels components imputables d'una línia d'oferta
description: Aquest tema proporciona informació sobre la configuració de components imputables i no imputables en una línia d'oferta basada en el projecte.
author: rumant
manager: Annbe
ms.date: 03/30/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1a9e1851bd8c5a4070df2774c945d1f3eabaaa8a
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858281"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a><span data-ttu-id="ea37d-103">Configuració dels components imputables d'una línia d'oferta</span><span class="sxs-lookup"><span data-stu-id="ea37d-103">Configure the chargeable components of a quote line</span></span> 

<span data-ttu-id="ea37d-104">_**S'aplica a:** Implementació bàsica: tracte de facturació proforma, Project Operations per a escenaris basats en recursos/sense cotització_</span><span class="sxs-lookup"><span data-stu-id="ea37d-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="ea37d-105">Una línia d'oferta basada en projectes té el concepte de components *inclosos* i components *imputables*.</span><span class="sxs-lookup"><span data-stu-id="ea37d-105">A project-based quote line has the concept of *included* components and *chargeable* components.</span></span>

<span data-ttu-id="ea37d-106">Els components inclosos estan subjectes a:</span><span class="sxs-lookup"><span data-stu-id="ea37d-106">Included components are subject to:</span></span>

  - <span data-ttu-id="ea37d-107">Mètode de facturació i desglossament del client</span><span class="sxs-lookup"><span data-stu-id="ea37d-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="ea37d-108">Límits que no s'han de superar</span><span class="sxs-lookup"><span data-stu-id="ea37d-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="ea37d-109">Paràmetres de freqüència de facturació definits a la línia d'oferta basada en projectes</span><span class="sxs-lookup"><span data-stu-id="ea37d-109">Invoice frequency settings defined on the project-based quote line</span></span>

<span data-ttu-id="ea37d-110">Un subconjunt dels components inclosos es pot marcar com a imputable mitjançant el camp **Tipus de facturació**.</span><span class="sxs-lookup"><span data-stu-id="ea37d-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="ea37d-111">El camp **Tipus de facturació** és un conjunt d'opcions que permet els següents valors en el context d'una línia d'oferta:</span><span class="sxs-lookup"><span data-stu-id="ea37d-111">The **Billing Type** field is an option-set that allows the following values in the context of a quote line:</span></span>

  - <span data-ttu-id="ea37d-112">Imputable</span><span class="sxs-lookup"><span data-stu-id="ea37d-112">Chargeable</span></span>
  - <span data-ttu-id="ea37d-113">No imputable</span><span class="sxs-lookup"><span data-stu-id="ea37d-113">Non-chargeable</span></span>

<span data-ttu-id="ea37d-114">Els components imputables es poden definir en tasques, rols i categories de transacció.</span><span class="sxs-lookup"><span data-stu-id="ea37d-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="ea37d-115">La imputabilitat es defineix en les tasques d'una línia d'oferta i s'aplica a totes les classes de transacció incloses a la línia.</span><span class="sxs-lookup"><span data-stu-id="ea37d-115">Chargeability is defined on the tasks for a quote line and applies to all transaction classes included on that line.</span></span> <span data-ttu-id="ea37d-116">Si el camp **Inclou les tasques** és buit o s'ha establert a **Tot el projecte**, la pestanya **Tasques imputables** no està disponible.</span><span class="sxs-lookup"><span data-stu-id="ea37d-116">If the **Include Tasks** field is set to **Entire project** or left blank, the **Chargeable Tasks** tab isn't available.</span></span>

<span data-ttu-id="ea37d-117">La imputabilitat definida a les funcions d'una línia d'oferta i només s'aplica a la classe de transacció **Temps**.</span><span class="sxs-lookup"><span data-stu-id="ea37d-117">Chargeability is defined on roles for a quote line and only applies to the **Time** transaction class.</span></span> <span data-ttu-id="ea37d-118">Si el camp **Inclou el temps** d'una línia d'oferta de projecte s'ha establert a **No**, la pestanya **Funcions imputables** no està disponible.</span><span class="sxs-lookup"><span data-stu-id="ea37d-118">If the field, **Include Time** is set to **No** on a project quote line, the **Chargeable Roles** tab isn't available.</span></span>

<span data-ttu-id="ea37d-119">La imputabilitat definida a les categories de transacció d'una línia d'oferta i només s'aplica a la classe de transacció **Despesa**.</span><span class="sxs-lookup"><span data-stu-id="ea37d-119">Chargeability is defined on transaction categories for a  quote line and only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="ea37d-120">Si el camp **Inclou les despeses** d'una línia d'oferta de projecte s'ha establert a **No**, la pestanya **Categories imputables** no està disponible.</span><span class="sxs-lookup"><span data-stu-id="ea37d-120">If the field, **Include Expenses** is set to **No** on a project quote line, the **Chargeable Categories** tab isn't available.</span></span>

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="ea37d-121">Actualitzar una tasca de projecte com a imputable o no imputable</span><span class="sxs-lookup"><span data-stu-id="ea37d-121">Update a project task to be chargeable or non-chargeable</span></span>

<span data-ttu-id="ea37d-122">Una tasca de projecte pot ser imputable o no imputable en el context d'una línia d'oferta basada en projectes específica, cosa que fa possible la configuració següent.</span><span class="sxs-lookup"><span data-stu-id="ea37d-122">A project task can be chargeable or non-chargeable in the context of a specific project-based quote line, which makes the following setup possible.</span></span>

<span data-ttu-id="ea37d-123">Si una línia d'oferta basada en projectes inclou **Temps** i la tasca **T1**, la tasca s'associa a la línia d'oferta com a imputable.</span><span class="sxs-lookup"><span data-stu-id="ea37d-123">If a project-based quote line includes **Time** and the task **T1**, the task is associated to the quote line as chargeable.</span></span> <span data-ttu-id="ea37d-124">Si hi ha una segona línia d'oferta que inclou **Despeses**, es pot associar la tasca **T1** a la línia d'oferta com a no imputable.</span><span class="sxs-lookup"><span data-stu-id="ea37d-124">If there is a second quote line that includes **Expenses**, you can associate the **T1** task on the quote line as non-chargeable.</span></span> <span data-ttu-id="ea37d-125">El resultat és que tot el temps que es registra en la tasca és imputable i totes les despeses registrades a la tasca no són imputables.</span><span class="sxs-lookup"><span data-stu-id="ea37d-125">The result is that all time recorded on the task is chargeable and all expenses recorded on the task are non-chargeable.</span></span>

<span data-ttu-id="ea37d-126">El tipus de facturació d'una tasca es pot configurar a la pestanya **Tasques imputables** de la línia de d'oferta basada en projectes actualitzant el camp **Tipus de facturació** a la subquadrícula **Tasques de la línia d'oferta**.</span><span class="sxs-lookup"><span data-stu-id="ea37d-126">A task's billing type can be configured on the **Chargeable Tasks** tab of a project-based quote line by updating the **Billing Type** field on the **Quote Line Tasks** subgrid.</span></span> <span data-ttu-id="ea37d-127">Alternativament, podeu actualitzar el tipus de facturació per a una tasca de projecte al camp **Tipus de facturació** a la subquadrícula de configuració de la facturació de la tasca d'un projecte que mostra les línies de contracte associades a una tasca.</span><span class="sxs-lookup"><span data-stu-id="ea37d-127">Alternatively, you can update the billing type for a project task in the **Billing Type** field on the subgrid on the task billing setup of a project that shows the quote lines associated to a task.</span></span>

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="ea37d-128">Actualitzar una funció com a imputable o no imputable</span><span class="sxs-lookup"><span data-stu-id="ea37d-128">Update a role to be chargeable or non-chargeable</span></span>

<span data-ttu-id="ea37d-129">Una funció pot ser imputable o no imputable en el context d'una línia d'oferta basada en projectes específica.</span><span class="sxs-lookup"><span data-stu-id="ea37d-129">A role can be chargeable or non-chargeable in the context of a specific project-based quote line.</span></span>

<span data-ttu-id="ea37d-130">El tipus de facturació d'una funció es pot configurar a la pestanya **Funcions imputables** de la línia de d'oferta actualitzant el camp **Tipus de facturació** a la subquadrícula **Funcions imputables**.</span><span class="sxs-lookup"><span data-stu-id="ea37d-130">A role's billing type can be configured on the **Chargeable Roles** tab of a quote line by updating the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="ea37d-131">Actualitzar una categoria de transacció com a imputable o no imputable</span><span class="sxs-lookup"><span data-stu-id="ea37d-131">Update a transaction category to be chargeable or non-chargeable</span></span>

<span data-ttu-id="ea37d-132">Una categoria de transacció pot ser imputable o no imputable en una línia d'oferta específica.</span><span class="sxs-lookup"><span data-stu-id="ea37d-132">A transaction category can be chargeable or non-chargeable on a specific quote line.</span></span>

<span data-ttu-id="ea37d-133">El tipus de facturació d'una transacció es pot configurar a la pestanya **Categories imputables** de la línia de d'oferta actualitzant el camp **Tipus de facturació** a la subquadrícula **Categories imputables**.</span><span class="sxs-lookup"><span data-stu-id="ea37d-133">A transaction's billing type can be configured on the **Chargeable Categories** tab of a quote line by updating the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="ea37d-134">Resoldre la imputabilitat</span><span class="sxs-lookup"><span data-stu-id="ea37d-134">Resolve chargeability</span></span>
<span data-ttu-id="ea37d-135">Una estimació o un valor real creats per al temps només es consideraran imputables si:</span><span class="sxs-lookup"><span data-stu-id="ea37d-135">An estimate or actual created for time will only be considered chargeable if:</span></span>

   - <span data-ttu-id="ea37d-136">El **Temps** s'inclou a la línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="ea37d-136">**Time** is included on the quote line.</span></span>
   - <span data-ttu-id="ea37d-137">La **Funció** està configurada com a imputable a la línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="ea37d-137">**Role** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="ea37d-138">**Tasques incloses** està establert com a **Tasques seleccionades** a la línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="ea37d-138">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span> 

<span data-ttu-id="ea37d-139">Si aquestes tres coses són certes, la **Tasca** també es configura com a imputable.</span><span class="sxs-lookup"><span data-stu-id="ea37d-139">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="ea37d-140">Una estimació o un valor real creats per a despeses només es consideraran imputables si:</span><span class="sxs-lookup"><span data-stu-id="ea37d-140">An estimate or actual created for expense is only considered chargeable if:</span></span> 

   - <span data-ttu-id="ea37d-141">La **Despesa** s'inclou a la línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="ea37d-141">**Expense** is included on the quote line.</span></span>
   - <span data-ttu-id="ea37d-142">**Categoria de transacció** està configurat com a imputable a la línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="ea37d-142">**Transaction category** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="ea37d-143">**Tasques incloses** està establert com a **Tasques seleccionades** a la línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="ea37d-143">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="ea37d-144">Si aquestes tres coses són certes, la **Tasca** també es configura com a imputable.</span><span class="sxs-lookup"><span data-stu-id="ea37d-144">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="ea37d-145">Una estimació o un valor real creats per al material només es consideraran imputables si:</span><span class="sxs-lookup"><span data-stu-id="ea37d-145">An estimate or actual created for material will only be considered chargeable if:</span></span>

   - <span data-ttu-id="ea37d-146">**Materials** s'inclou a la línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="ea37d-146">**Materials** is included on the quote line.</span></span>
   - <span data-ttu-id="ea37d-147">**Tasques incloses** està establert com a **Tasques seleccionades** a la línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="ea37d-147">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="ea37d-148">Si aquestes dues coses són certes, la **Tasca** també s'hauria de configurar com a imputable.</span><span class="sxs-lookup"><span data-stu-id="ea37d-148">If these two things are true, the **Task** should also be configured as chargeable.</span></span> 


<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="ea37d-149">
                    <strong>Inclou el temps</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea37d-149">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="ea37d-150">
                    <strong>Inclou les despeses</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea37d-150">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="ea37d-151">
                    <strong>Inclou materials</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea37d-151">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="ea37d-152">
                    <strong>Tasques incloses</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea37d-152">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="ea37d-153">
                    <strong>Funció</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea37d-153">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="ea37d-154">
                    <strong>Categoria</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea37d-154">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="ea37d-155">
                    <strong>Tasca</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea37d-155">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="ea37d-156">
                    <strong>Impacte de la imputabilitat</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea37d-156">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ea37d-157">Sí</span><span class="sxs-lookup"><span data-stu-id="ea37d-157">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="ea37d-158">Sí</span><span class="sxs-lookup"><span data-stu-id="ea37d-158">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="ea37d-159">Sí</span><span class="sxs-lookup"><span data-stu-id="ea37d-159">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="ea37d-160">Tot el projecte</span><span class="sxs-lookup"><span data-stu-id="ea37d-160">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ea37d-161">Imputable</span><span class="sxs-lookup"><span data-stu-id="ea37d-161">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ea37d-162">Imputable</span><span class="sxs-lookup"><span data-stu-id="ea37d-162">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ea37d-163">No es pot definir</span><span class="sxs-lookup"><span data-stu-id="ea37d-163">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="ea37d-164">Facturació en un valor real de temps: Imputable</span><span class="sxs-lookup"><span data-stu-id="ea37d-164">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="ea37d-165">Tipus de facturació en un valor real de despesa: Imputable</span><span class="sxs-lookup"><span data-stu-id="ea37d-165">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="ea37d-166">Tipus de facturació del material real: imputable</span><span class="sxs-lookup"><span data-stu-id="ea37d-166">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ea37d-167">Sí</span><span class="sxs-lookup"><span data-stu-id="ea37d-167">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="ea37d-168">Sí</span><span class="sxs-lookup"><span data-stu-id="ea37d-168">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="ea37d-169">Sí</span><span class="sxs-lookup"><span data-stu-id="ea37d-169">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="ea37d-170">Només les tasques seleccionades</span><span class="sxs-lookup"><span data-stu-id="ea37d-170">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ea37d-171">Imputable</span><span class="sxs-lookup"><span data-stu-id="ea37d-171">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ea37d-172">Imputable</span><span class="sxs-lookup"><span data-stu-id="ea37d-172">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ea37d-173">Imputable</span><span class="sxs-lookup"><span data-stu-id="ea37d-173">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="ea37d-174">Facturació en un valor real de temps: Imputable</span><span class="sxs-lookup"><span data-stu-id="ea37d-174">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="ea37d-175">Tipus de facturació en un valor real de despesa: Imputable</span><span class="sxs-lookup"><span data-stu-id="ea37d-175">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="ea37d-176">Tipus de facturació del material real: imputable</span><span class="sxs-lookup"><span data-stu-id="ea37d-176">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ea37d-177">Sí</span><span class="sxs-lookup"><span data-stu-id="ea37d-177">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="ea37d-178">Sí</span><span class="sxs-lookup"><span data-stu-id="ea37d-178">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="ea37d-179">Sí</span><span class="sxs-lookup"><span data-stu-id="ea37d-179">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="ea37d-180">Només les tasques seleccionades</span><span class="sxs-lookup"><span data-stu-id="ea37d-180">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="ea37d-181">
                    <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea37d-181">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ea37d-182">Imputable</span><span class="sxs-lookup"><span data-stu-id="ea37d-182">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ea37d-183">Imputable</span><span class="sxs-lookup"><span data-stu-id="ea37d-183">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="ea37d-184">Facturació en un valor real de temps: <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea37d-184">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="ea37d-185">Tipus de facturació en un valor real de despesa: Imputable</span><span class="sxs-lookup"><span data-stu-id="ea37d-185">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="ea37d-186">Tipus de facturació del material real: imputable</span><span class="sxs-lookup"><span data-stu-id="ea37d-186">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ea37d-187">Sí</span><span class="sxs-lookup"><span data-stu-id="ea37d-187">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="ea37d-188">Sí</span><span class="sxs-lookup"><span data-stu-id="ea37d-188">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="ea37d-189">Sí</span><span class="sxs-lookup"><span data-stu-id="ea37d-189">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="ea37d-190">Només les tasques seleccionades</span><span class="sxs-lookup"><span data-stu-id="ea37d-190">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ea37d-191">Imputable</span><span class="sxs-lookup"><span data-stu-id="ea37d-191">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ea37d-192">Imputable</span><span class="sxs-lookup"><span data-stu-id="ea37d-192">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="ea37d-193">
                    <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea37d-193">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="ea37d-194">Facturació en un valor real de temps: <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea37d-194">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="ea37d-195">Tipus de facturació en un valor real de despesa: <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea37d-195">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="ea37d-196">Tipus de facturació en un valor real de material: <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea37d-196">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ea37d-197">Sí</span><span class="sxs-lookup"><span data-stu-id="ea37d-197">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="ea37d-198">Sí</span><span class="sxs-lookup"><span data-stu-id="ea37d-198">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="ea37d-199">Sí</span><span class="sxs-lookup"><span data-stu-id="ea37d-199">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="ea37d-200">Només les tasques seleccionades</span><span class="sxs-lookup"><span data-stu-id="ea37d-200">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="ea37d-201">
                    <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea37d-201">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ea37d-202">Imputable</span><span class="sxs-lookup"><span data-stu-id="ea37d-202">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="ea37d-203">
                    <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea37d-203">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="ea37d-204">Facturació en un valor real de temps: <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea37d-204">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="ea37d-205">Tipus de facturació en un valor real de despesa: <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea37d-205">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="ea37d-206">Tipus de facturació en un valor real de material: <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea37d-206">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ea37d-207">Sí</span><span class="sxs-lookup"><span data-stu-id="ea37d-207">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="ea37d-208">Sí</span><span class="sxs-lookup"><span data-stu-id="ea37d-208">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="ea37d-209">Sí</span><span class="sxs-lookup"><span data-stu-id="ea37d-209">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="ea37d-210">Només les tasques seleccionades</span><span class="sxs-lookup"><span data-stu-id="ea37d-210">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="ea37d-211">
                    <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea37d-211">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="ea37d-212">
                    <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea37d-212">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ea37d-213">Imputable</span><span class="sxs-lookup"><span data-stu-id="ea37d-213">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="ea37d-214">Facturació en un valor real de temps: <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea37d-214">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="ea37d-215">Tipus de facturació en un valor real de despesa: <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea37d-215">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="ea37d-216">Tipus de facturació del material real: imputable</span><span class="sxs-lookup"><span data-stu-id="ea37d-216">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="ea37d-217">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea37d-217">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="ea37d-218">Sí</span><span class="sxs-lookup"><span data-stu-id="ea37d-218">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="ea37d-219">Sí</span><span class="sxs-lookup"><span data-stu-id="ea37d-219">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="ea37d-220">Tot el projecte</span><span class="sxs-lookup"><span data-stu-id="ea37d-220">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ea37d-221">No es pot definir</span><span class="sxs-lookup"><span data-stu-id="ea37d-221">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="ea37d-222">
                    <strong>Imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea37d-222">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ea37d-223">No es pot definir</span><span class="sxs-lookup"><span data-stu-id="ea37d-223">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="ea37d-224">Facturació en un valor real de temps: <strong>No disponible</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea37d-224">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="ea37d-225">Tipus de facturació en un valor real de despesa: Imputable</span><span class="sxs-lookup"><span data-stu-id="ea37d-225">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="ea37d-226">Tipus de facturació del material real: imputable</span><span class="sxs-lookup"><span data-stu-id="ea37d-226">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="ea37d-227">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea37d-227">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="ea37d-228">Sí</span><span class="sxs-lookup"><span data-stu-id="ea37d-228">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="ea37d-229">Sí</span><span class="sxs-lookup"><span data-stu-id="ea37d-229">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="ea37d-230">Tot el projecte</span><span class="sxs-lookup"><span data-stu-id="ea37d-230">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ea37d-231">No es pot definir</span><span class="sxs-lookup"><span data-stu-id="ea37d-231">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="ea37d-232">
                    <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea37d-232">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ea37d-233">No es pot definir</span><span class="sxs-lookup"><span data-stu-id="ea37d-233">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="ea37d-234">Facturació en un valor real de temps: <strong>No disponible</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea37d-234">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="ea37d-235">Tipus de facturació en un valor real de despesa: <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea37d-235">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="ea37d-236">Tipus de facturació del material real: imputable</span><span class="sxs-lookup"><span data-stu-id="ea37d-236">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ea37d-237">Sí</span><span class="sxs-lookup"><span data-stu-id="ea37d-237">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="ea37d-238">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea37d-238">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="ea37d-239">Sí</span><span class="sxs-lookup"><span data-stu-id="ea37d-239">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="ea37d-240">Tot el projecte</span><span class="sxs-lookup"><span data-stu-id="ea37d-240">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ea37d-241">Imputable</span><span class="sxs-lookup"><span data-stu-id="ea37d-241">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ea37d-242">No es pot definir</span><span class="sxs-lookup"><span data-stu-id="ea37d-242">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ea37d-243">No es pot definir</span><span class="sxs-lookup"><span data-stu-id="ea37d-243">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="ea37d-244">Facturació en un valor real de temps: Imputable</span><span class="sxs-lookup"><span data-stu-id="ea37d-244">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="ea37d-245">Tipus de facturació en un valor real de despesa: <strong>No disponible</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea37d-245">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="ea37d-246">Tipus de facturació del material real: imputable</span><span class="sxs-lookup"><span data-stu-id="ea37d-246">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ea37d-247">Sí</span><span class="sxs-lookup"><span data-stu-id="ea37d-247">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="ea37d-248">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea37d-248">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="ea37d-249">Sí</span><span class="sxs-lookup"><span data-stu-id="ea37d-249">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="ea37d-250">Tot el projecte</span><span class="sxs-lookup"><span data-stu-id="ea37d-250">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="ea37d-251">
                    <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea37d-251">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ea37d-252">No es pot definir</span><span class="sxs-lookup"><span data-stu-id="ea37d-252">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ea37d-253">No es pot definir</span><span class="sxs-lookup"><span data-stu-id="ea37d-253">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="ea37d-254">Facturació en un valor real de temps: <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea37d-254">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="ea37d-255">Tipus de facturació en un valor real de despesa: <strong>No disponible</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea37d-255">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="ea37d-256">Tipus de facturació del material real: imputable</span><span class="sxs-lookup"><span data-stu-id="ea37d-256">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ea37d-257">Sí</span><span class="sxs-lookup"><span data-stu-id="ea37d-257">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="ea37d-258">Sí</span><span class="sxs-lookup"><span data-stu-id="ea37d-258">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="ea37d-259">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea37d-259">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="ea37d-260">Tot el projecte</span><span class="sxs-lookup"><span data-stu-id="ea37d-260">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ea37d-261">Imputable</span><span class="sxs-lookup"><span data-stu-id="ea37d-261">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ea37d-262">Imputable</span><span class="sxs-lookup"><span data-stu-id="ea37d-262">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ea37d-263">No es pot definir</span><span class="sxs-lookup"><span data-stu-id="ea37d-263">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="ea37d-264">Facturació en un valor real de temps: Imputable</span><span class="sxs-lookup"><span data-stu-id="ea37d-264">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="ea37d-265">Tipus de facturació en un valor real de despesa: Imputable</span><span class="sxs-lookup"><span data-stu-id="ea37d-265">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="ea37d-266">Tipus de facturació en un valor real de material: <strong>No disponible</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea37d-266">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="ea37d-267">Sí</span><span class="sxs-lookup"><span data-stu-id="ea37d-267">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="ea37d-268">Sí</span><span class="sxs-lookup"><span data-stu-id="ea37d-268">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="ea37d-269">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea37d-269">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="ea37d-270">Tot el projecte</span><span class="sxs-lookup"><span data-stu-id="ea37d-270">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="ea37d-271">
                    <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea37d-271">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="ea37d-272">
                    <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea37d-272">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="ea37d-273">No es pot definir</span><span class="sxs-lookup"><span data-stu-id="ea37d-273">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="ea37d-274">Facturació en un valor real de temps: <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea37d-274">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="ea37d-275">Tipus de facturació en un valor real de despesa: <strong>No imputable</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea37d-275">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="ea37d-276">Tipus de facturació en un valor real de material: <strong>No disponible</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ea37d-276">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
