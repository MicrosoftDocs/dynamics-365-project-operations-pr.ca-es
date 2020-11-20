---
title: Valors reals
description: En aquest tema es proporciona informació sobre com treballar amb valors reals al Microsoft Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 13c429763fa805fae5324e4dcf1bf7669e842281
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4126291"
---
# <a name="actuals"></a><span data-ttu-id="64064-103">Valors reals</span><span class="sxs-lookup"><span data-stu-id="64064-103">Actuals</span></span> 

<span data-ttu-id="64064-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_</span><span class="sxs-lookup"><span data-stu-id="64064-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="64064-105">Els valors reals són la quantitat de treball que s'ha completat en un projecte.</span><span class="sxs-lookup"><span data-stu-id="64064-105">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="64064-106">Es creen com a resultat d'entrades de temps i de despeses i entrades de diari i factures.</span><span class="sxs-lookup"><span data-stu-id="64064-106">They are created as a result of time and expense entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="64064-107">Línies del llibre diari i enviament de temps</span><span class="sxs-lookup"><span data-stu-id="64064-107">Journal lines and time submission</span></span>

<span data-ttu-id="64064-108">Per obtenir més informació sobre l'entrada de temps, vegeu [Descripció general de les entrades de temps](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="64064-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="64064-109">Temps i materials</span><span class="sxs-lookup"><span data-stu-id="64064-109">Time and materials</span></span>

<span data-ttu-id="64064-110">Quan un registre de temps que s'envia està enllaçat a un projecte que s'assigna a una línia de contracte de temps i materials, el sistema crea dues línies del llibre diari, una per al cost i l'altra per a les vendes sense facturar.</span><span class="sxs-lookup"><span data-stu-id="64064-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="64064-111">Preu fix</span><span class="sxs-lookup"><span data-stu-id="64064-111">Fixed price</span></span>

<span data-ttu-id="64064-112">Quan una entrada de temps que s'envia està enllaçada a un projecte assignat a una línia de contracte de preu fix, el sistema crea una línia del llibre diari per al cost.</span><span class="sxs-lookup"><span data-stu-id="64064-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="64064-113">Preus per defecte</span><span class="sxs-lookup"><span data-stu-id="64064-113">Default pricing</span></span>

<span data-ttu-id="64064-114">La lògica per crear els preus per defecte resideix a la línia del llibre diari.</span><span class="sxs-lookup"><span data-stu-id="64064-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="64064-115">Els valors de camp de l'entrada de temps es copien a la línia del llibre diari.</span><span class="sxs-lookup"><span data-stu-id="64064-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="64064-116">Aquests valors inclouen la data de la transacció, la línia de contracte a la qual està assignada el projecte i el resultat de moneda a la llista de preus adequada.</span><span class="sxs-lookup"><span data-stu-id="64064-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="64064-117">Els camps que afecten els preus per defecte, com ara **Funció** i **Unitat organitzativa**, s'utilitzen per determinar el preu adient a la línia del llibre diari.</span><span class="sxs-lookup"><span data-stu-id="64064-117">The fields that affect default pricing, such as **Role** and **Org Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="64064-118">Podeu afegir un camp personalitzat a l'entrada de temps.</span><span class="sxs-lookup"><span data-stu-id="64064-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="64064-119">Si voleu que el valor del camp es propagui a valors reals, creeu el camp a l'entitat Valors reals i utilitzeu assignacions de camps per copiar el camp de l'entrada de temps al valor real.</span><span class="sxs-lookup"><span data-stu-id="64064-119">If you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="64064-120">Línies del llibre diari i enviament bàsic de despeses</span><span class="sxs-lookup"><span data-stu-id="64064-120">Journal lines and basic expense submission</span></span>

<span data-ttu-id="64064-121">Per obtenir més informació sobre l'entrada de despesa, vegeu [Descripció general de les entrades de despesa](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="64064-121">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="64064-122">Temps i materials</span><span class="sxs-lookup"><span data-stu-id="64064-122">Time and materials</span></span>

<span data-ttu-id="64064-123">Quan una entrada de despesa bàsica que s'envia està enllaçat a un projecte que s'assigna a una línia de contracte de temps i materials, el sistema crea dues línies del llibre diari, una per al cost i l'altra per a les vendes sense facturar.</span><span class="sxs-lookup"><span data-stu-id="64064-123">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="64064-124">Preu fix</span><span class="sxs-lookup"><span data-stu-id="64064-124">Fixed price</span></span>

<span data-ttu-id="64064-125">Quan una entrada de despesa bàsica que s'envia està enllaçada a un projecte assignat a una línia de contracte de preu fix, el sistema crea una línia del llibre diari per al cost.</span><span class="sxs-lookup"><span data-stu-id="64064-125">When a basic expense entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="64064-126">Preus per defecte</span><span class="sxs-lookup"><span data-stu-id="64064-126">Default pricing</span></span>

<span data-ttu-id="64064-127">La lògica per a la introducció dels preus per defecte de les despeses es basa en la categoria de despeses.</span><span class="sxs-lookup"><span data-stu-id="64064-127">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="64064-128">La data de la transacció, la línia de contracte a la qual està assignada el projecte i la moneda s'utilitzen per determinar la llista de preus adequada.</span><span class="sxs-lookup"><span data-stu-id="64064-128">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="64064-129">No obstant, per defecte, l'import que s'introdueix per al preu en si mateix es defineix directament a les línies del llibre diari de despesa relacionades per al cost i les vendes.</span><span class="sxs-lookup"><span data-stu-id="64064-129">However, by default, the amount that is entered for the price itself is set directly on the related expense journal lines for cost and sales.</span></span>

<span data-ttu-id="64064-130">L'entrada basada en categories per a preus per unitat per defecte a les entrades de despesa no està disponible.</span><span class="sxs-lookup"><span data-stu-id="64064-130">Category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="64064-131">Utilitzar llibres diari per registrar costos de registre</span><span class="sxs-lookup"><span data-stu-id="64064-131">Use entry journals to record costs</span></span>

<span data-ttu-id="64064-132">Podeu utilitzar llibres diari per registrar els costos o ingressos en classes de material, quota, temps, despeses o transaccions tributàries.</span><span class="sxs-lookup"><span data-stu-id="64064-132">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="64064-133">Els diaris es poden utilitzar amb l'objectiu següent:</span><span class="sxs-lookup"><span data-stu-id="64064-133">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="64064-134">Registrar els costos reals materials i les vendes d'un projecte.</span><span class="sxs-lookup"><span data-stu-id="64064-134">Record the actual cost of materials and sales on a project.</span></span>
- <span data-ttu-id="64064-135">Moure els valors reals de la transacció des d'un altre sistema al Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="64064-135">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="64064-136">Registrar els costos que s'han produït en un altre sistema.</span><span class="sxs-lookup"><span data-stu-id="64064-136">Record costs that occurred in another system.</span></span> <span data-ttu-id="64064-137">Aquestes despeses poden incloure costos de contractació o subcontractació.</span><span class="sxs-lookup"><span data-stu-id="64064-137">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="64064-138">L'aplicació no valida el tipus de línia del llibre diari ni el preu relacionat que introduïu a la línia del llibre diari.</span><span class="sxs-lookup"><span data-stu-id="64064-138">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="64064-139">Per tant, només un usuari que tingui consciència de l'impacte comptable que tenen els valors reals en el projecte hauria d'utilitzar els llibres diari per crear valors reals.</span><span class="sxs-lookup"><span data-stu-id="64064-139">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="64064-140">A causa de l'impacte d'aquest tipus de diari, heu de triar amb cura qui té accés per crear llibres diari.</span><span class="sxs-lookup"><span data-stu-id="64064-140">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>
## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="64064-141">Enregistrament de valors reals a partir d'esdeveniments de projecte</span><span class="sxs-lookup"><span data-stu-id="64064-141">Record actuals based on project events</span></span>

<span data-ttu-id="64064-142">El Project Operations registra totes les transaccions financeres que es produeixen durant un projecte.</span><span class="sxs-lookup"><span data-stu-id="64064-142">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="64064-143">Aquestes transaccions es registren com a valors reals.</span><span class="sxs-lookup"><span data-stu-id="64064-143">These transactions are recorded as actuals.</span></span> <span data-ttu-id="64064-144">Les taules següents mostren els diferents tipus de valors reals que s'han creat, en funció de si el projecte és un projecte de temps i materials o de preu fix, si es troba a la fase de prevenda o si és un projecte intern.</span><span class="sxs-lookup"><span data-stu-id="64064-144">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="64064-145">El recurs pertany a la mateixa unitat organitzativa que la unitat de contractació del projecte</span><span class="sxs-lookup"><span data-stu-id="64064-145">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="64064-146">Incidència</span><span class="sxs-lookup"><span data-stu-id="64064-146">Event</span></span></th>
<th colspan="4"><span data-ttu-id="64064-147">Projecte facturable o venut</span><span class="sxs-lookup"><span data-stu-id="64064-147">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="64064-148">Projecte a la fase de prevenda</span><span class="sxs-lookup"><span data-stu-id="64064-148">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="64064-149">Projecte intern</span><span class="sxs-lookup"><span data-stu-id="64064-149">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="64064-150">Temps i materials</span><span class="sxs-lookup"><span data-stu-id="64064-150">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="64064-151">Preu fix</span><span class="sxs-lookup"><span data-stu-id="64064-151">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="64064-152">Valors reals</span><span class="sxs-lookup"><span data-stu-id="64064-152">Actuals</span></span></th>
<th><span data-ttu-id="64064-153">Moneda de transacció</span><span class="sxs-lookup"><span data-stu-id="64064-153">Transaction currency</span></span></th>
<th><span data-ttu-id="64064-154">Preu fix</span><span class="sxs-lookup"><span data-stu-id="64064-154">Fixed price</span></span></th>
<th><span data-ttu-id="64064-155">Moneda de transacció</span><span class="sxs-lookup"><span data-stu-id="64064-155">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="64064-156">Es crea una entrada de temps.</span><span class="sxs-lookup"><span data-stu-id="64064-156">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="64064-157">No hi ha activitat a l'entitat Valors reals</span><span class="sxs-lookup"><span data-stu-id="64064-157">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64064-158">S'envia una entrada de temps.</span><span class="sxs-lookup"><span data-stu-id="64064-158">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="64064-159">No hi ha activitat a l'entitat Valors reals</span><span class="sxs-lookup"><span data-stu-id="64064-159">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="64064-160">El temps s'aprova, i no es produeix cap canvi o augment de les hores facturables durant l'aprovació.</span><span class="sxs-lookup"><span data-stu-id="64064-160">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="64064-161">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="64064-161">Cost actual</span></span></td>
<td><span data-ttu-id="64064-162">Moneda de la unitat de contractació</span><span class="sxs-lookup"><span data-stu-id="64064-162">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="64064-163">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="64064-163">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="64064-164">Moneda de la unitat de contractació</span><span class="sxs-lookup"><span data-stu-id="64064-164">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="64064-165">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="64064-165">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="64064-166">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="64064-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64064-167">Valor real de les vendes no facturades - Imputable</span><span class="sxs-lookup"><span data-stu-id="64064-167">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="64064-168">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="64064-168">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="64064-169">El temps s'aprova, i es produeix una reducció de les hores facturables durant l'aprovació.</span><span class="sxs-lookup"><span data-stu-id="64064-169">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="64064-170">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="64064-170">Cost actual</span></span></td>
<td><span data-ttu-id="64064-171">Moneda de la unitat de contractació</span><span class="sxs-lookup"><span data-stu-id="64064-171">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="64064-172">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="64064-172">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="64064-173">Moneda de la unitat de contractació</span><span class="sxs-lookup"><span data-stu-id="64064-173">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="64064-174">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="64064-174">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="64064-175">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="64064-175">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64064-176">Valor real de les vendes no facturades - Imputable per a la nova quantitat</span><span class="sxs-lookup"><span data-stu-id="64064-176">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="64064-177">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="64064-177">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64064-178">Valor real de les vendes no facturades - No imputable per la diferència</span><span class="sxs-lookup"><span data-stu-id="64064-178">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="64064-179">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="64064-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="64064-180">Es confirma una factura, i no es produeix cap canvi o augment de les hores facturables.</span><span class="sxs-lookup"><span data-stu-id="64064-180">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="64064-181">Reversió de vendes no facturades</span><span class="sxs-lookup"><span data-stu-id="64064-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="64064-182">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="64064-182">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="64064-183">Vendes facturades per fita</span><span class="sxs-lookup"><span data-stu-id="64064-183">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="64064-184">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="64064-184">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="64064-185">No aplicable</span><span class="sxs-lookup"><span data-stu-id="64064-185">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="64064-186">No aplicable</span><span class="sxs-lookup"><span data-stu-id="64064-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64064-187">Vendes facturades</span><span class="sxs-lookup"><span data-stu-id="64064-187">Billed sales</span></span></td>
<td><span data-ttu-id="64064-188">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="64064-188">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="64064-189">Es confirma una factura, i es produeix una disminució de les hores facturables.</span><span class="sxs-lookup"><span data-stu-id="64064-189">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="64064-190">Reversió de vendes no facturades</span><span class="sxs-lookup"><span data-stu-id="64064-190">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="64064-191">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="64064-191">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="64064-192">No aplicable</span><span class="sxs-lookup"><span data-stu-id="64064-192">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="64064-193">No aplicable</span><span class="sxs-lookup"><span data-stu-id="64064-193">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="64064-194">No aplicable</span><span class="sxs-lookup"><span data-stu-id="64064-194">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="64064-195">No aplicable</span><span class="sxs-lookup"><span data-stu-id="64064-195">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64064-196">Vendes facturades - Imputable per a la nova quantitat</span><span class="sxs-lookup"><span data-stu-id="64064-196">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="64064-197">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="64064-197">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64064-198">Vendes facturades - No imputable per la diferència</span><span class="sxs-lookup"><span data-stu-id="64064-198">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="64064-199">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="64064-199">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="64064-200">Una factura es corregeix per augmentar la quantitat imputable.</span><span class="sxs-lookup"><span data-stu-id="64064-200">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="64064-201">Vendes facturades - Reversió</span><span class="sxs-lookup"><span data-stu-id="64064-201">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="64064-202">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="64064-202">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="64064-203">Reversió de vendes facturades per fita</span><span class="sxs-lookup"><span data-stu-id="64064-203">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="64064-204">Canvi en l'estat de la fita de <strong>Facturada</strong> a <strong>Llesta per facturar</strong></span><span class="sxs-lookup"><span data-stu-id="64064-204">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="64064-205">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="64064-205">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="64064-206">No aplicable</span><span class="sxs-lookup"><span data-stu-id="64064-206">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="64064-207">No aplicable</span><span class="sxs-lookup"><span data-stu-id="64064-207">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64064-208">Vendes facturades</span><span class="sxs-lookup"><span data-stu-id="64064-208">Billed sales</span></span></td>
<td><span data-ttu-id="64064-209">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="64064-209">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="64064-210">Una factura es corregeix per reduir la quantitat imputable.</span><span class="sxs-lookup"><span data-stu-id="64064-210">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="64064-211">Vendes facturades - Reversió</span><span class="sxs-lookup"><span data-stu-id="64064-211">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="64064-212">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="64064-212">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64064-213">Vendes facturades per a la nova quantitat</span><span class="sxs-lookup"><span data-stu-id="64064-213">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="64064-214">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="64064-214">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64064-215">Vendes no facturades - Imputable per la diferència</span><span class="sxs-lookup"><span data-stu-id="64064-215">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="64064-216">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="64064-216">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="64064-217">El recurs pertany a una unitat organitzativa diferent de la unitat de contractació del projecte</span><span class="sxs-lookup"><span data-stu-id="64064-217">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="64064-218">Incidència</span><span class="sxs-lookup"><span data-stu-id="64064-218">Event</span></span></th>
<th colspan="4"><span data-ttu-id="64064-219">Projecte facturable o venut</span><span class="sxs-lookup"><span data-stu-id="64064-219">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="64064-220">Projecte a la fase de prevenda</span><span class="sxs-lookup"><span data-stu-id="64064-220">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="64064-221">Projecte intern</span><span class="sxs-lookup"><span data-stu-id="64064-221">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="64064-222">Temps i materials</span><span class="sxs-lookup"><span data-stu-id="64064-222">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="64064-223">Preu fix</span><span class="sxs-lookup"><span data-stu-id="64064-223">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="64064-224">Valors reals</span><span class="sxs-lookup"><span data-stu-id="64064-224">Actuals</span></span></th>
<th><span data-ttu-id="64064-225">Moneda de transacció</span><span class="sxs-lookup"><span data-stu-id="64064-225">Transaction currency</span></span></th>
<th><span data-ttu-id="64064-226">Preu fix</span><span class="sxs-lookup"><span data-stu-id="64064-226">Fixed price</span></span></th>
<th><span data-ttu-id="64064-227">Moneda de transacció</span><span class="sxs-lookup"><span data-stu-id="64064-227">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="64064-228">Es crea una entrada de temps.</span><span class="sxs-lookup"><span data-stu-id="64064-228">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="64064-229">No hi ha activitat a l'entitat Valors reals</span><span class="sxs-lookup"><span data-stu-id="64064-229">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64064-230">S'envia una entrada de temps.</span><span class="sxs-lookup"><span data-stu-id="64064-230">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="64064-231">No hi ha activitat a l'entitat Valors reals</span><span class="sxs-lookup"><span data-stu-id="64064-231">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="64064-232">El temps s'aprova, i no es produeix cap canvi o augment de les hores facturables durant l'aprovació.</span><span class="sxs-lookup"><span data-stu-id="64064-232">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="64064-233">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="64064-233">Cost actual</span></span></td>
<td><span data-ttu-id="64064-234">Moneda de la unitat de contractació</span><span class="sxs-lookup"><span data-stu-id="64064-234">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="64064-235">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="64064-235">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="64064-236">Moneda de la unitat de contractació</span><span class="sxs-lookup"><span data-stu-id="64064-236">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="64064-237">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="64064-237">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="64064-238">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="64064-238">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64064-239">Valor real de les vendes no facturades - Imputable</span><span class="sxs-lookup"><span data-stu-id="64064-239">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="64064-240">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="64064-240">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64064-241">Cost de la unitat de recursos</span><span class="sxs-lookup"><span data-stu-id="64064-241">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="64064-242">Moneda de la unitat de recursos</span><span class="sxs-lookup"><span data-stu-id="64064-242">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64064-243">Vendes interorganitzatives</span><span class="sxs-lookup"><span data-stu-id="64064-243">Interorganizational sales</span></span></td>
<td><span data-ttu-id="64064-244">Moneda de la unitat de contractació</span><span class="sxs-lookup"><span data-stu-id="64064-244">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="64064-245">El temps s'aprova, i es produeix una reducció de les hores facturables durant l'aprovació.</span><span class="sxs-lookup"><span data-stu-id="64064-245">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="64064-246">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="64064-246">Cost actual</span></span></td>
<td><span data-ttu-id="64064-247">Moneda de la unitat de contractació</span><span class="sxs-lookup"><span data-stu-id="64064-247">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="64064-248">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="64064-248">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="64064-249">Moneda de la unitat de contractació</span><span class="sxs-lookup"><span data-stu-id="64064-249">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="64064-250">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="64064-250">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="64064-251">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="64064-251">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64064-252">Cost de la unitat de recursos</span><span class="sxs-lookup"><span data-stu-id="64064-252">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="64064-253">Moneda de la unitat de recursos</span><span class="sxs-lookup"><span data-stu-id="64064-253">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64064-254">Vendes interorganitzatives</span><span class="sxs-lookup"><span data-stu-id="64064-254">Interorganizational sales</span></span></td>
<td><span data-ttu-id="64064-255">Moneda de la unitat de contractació</span><span class="sxs-lookup"><span data-stu-id="64064-255">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64064-256">Valor real de les vendes no facturades - Imputable per a la nova quantitat</span><span class="sxs-lookup"><span data-stu-id="64064-256">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="64064-257">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="64064-257">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64064-258">Valor real de les vendes no facturades - No imputable per la diferència</span><span class="sxs-lookup"><span data-stu-id="64064-258">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="64064-259">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="64064-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="64064-260">Es confirma una factura, i no es produeix cap canvi o augment de les hores facturables.</span><span class="sxs-lookup"><span data-stu-id="64064-260">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="64064-261">Reversió de vendes no facturades</span><span class="sxs-lookup"><span data-stu-id="64064-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="64064-262">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="64064-262">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="64064-263">Vendes facturades per fita</span><span class="sxs-lookup"><span data-stu-id="64064-263">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="64064-264">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="64064-264">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="64064-265">No aplicable</span><span class="sxs-lookup"><span data-stu-id="64064-265">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="64064-266">No aplicable</span><span class="sxs-lookup"><span data-stu-id="64064-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64064-267">Vendes facturades</span><span class="sxs-lookup"><span data-stu-id="64064-267">Billed sales</span></span></td>
<td><span data-ttu-id="64064-268">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="64064-268">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="64064-269">Es confirma una factura, i es produeix una disminució de les hores facturables.</span><span class="sxs-lookup"><span data-stu-id="64064-269">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="64064-270">Reversió de vendes no facturades</span><span class="sxs-lookup"><span data-stu-id="64064-270">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="64064-271">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="64064-271">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="64064-272">No aplicable</span><span class="sxs-lookup"><span data-stu-id="64064-272">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="64064-273">No aplicable</span><span class="sxs-lookup"><span data-stu-id="64064-273">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="64064-274">No aplicable</span><span class="sxs-lookup"><span data-stu-id="64064-274">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="64064-275">No aplicable</span><span class="sxs-lookup"><span data-stu-id="64064-275">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64064-276">Vendes facturades - Imputable per a la nova quantitat</span><span class="sxs-lookup"><span data-stu-id="64064-276">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="64064-277">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="64064-277">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64064-278">Vendes facturades - No imputable per la diferència</span><span class="sxs-lookup"><span data-stu-id="64064-278">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="64064-279">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="64064-279">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="64064-280">Una factura es corregeix per augmentar la quantitat imputable.</span><span class="sxs-lookup"><span data-stu-id="64064-280">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="64064-281">Vendes facturades - Reversió</span><span class="sxs-lookup"><span data-stu-id="64064-281">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="64064-282">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="64064-282">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="64064-283">Reversió de vendes facturades per fita</span><span class="sxs-lookup"><span data-stu-id="64064-283">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="64064-284">Canvi en l'estat de la fita de <strong>Facturada</strong> a <strong>Llesta per facturar</strong></span><span class="sxs-lookup"><span data-stu-id="64064-284">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="64064-285">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="64064-285">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="64064-286">No aplicable</span><span class="sxs-lookup"><span data-stu-id="64064-286">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="64064-287">No aplicable</span><span class="sxs-lookup"><span data-stu-id="64064-287">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64064-288">Vendes facturades</span><span class="sxs-lookup"><span data-stu-id="64064-288">Billed sales</span></span></td>
<td><span data-ttu-id="64064-289">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="64064-289">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="64064-290">Una factura es corregeix per reduir la quantitat imputable.</span><span class="sxs-lookup"><span data-stu-id="64064-290">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="64064-291">Vendes facturades - Reversió</span><span class="sxs-lookup"><span data-stu-id="64064-291">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="64064-292">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="64064-292">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64064-293">Vendes facturades per a la nova quantitat</span><span class="sxs-lookup"><span data-stu-id="64064-293">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="64064-294">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="64064-294">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="64064-295">Vendes no facturades - Imputable per la diferència</span><span class="sxs-lookup"><span data-stu-id="64064-295">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="64064-296">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="64064-296">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
