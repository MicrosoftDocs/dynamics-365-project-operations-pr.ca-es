---
title: Valors reals
description: Aquest tema proporciona informació sobre els valors reals del projecte.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 44c6e85f-5b21-4e24-999c-15a2f065d977
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8291e0eb8531e8e9690368675f333c44b6e92e48
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749557"
---
# <a name="actuals"></a><span data-ttu-id="90cbd-103">Valors reals</span><span class="sxs-lookup"><span data-stu-id="90cbd-103">Actuals</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="90cbd-104">Els valors reals són la quantitat de treball que s'ha completat en un projecte.</span><span class="sxs-lookup"><span data-stu-id="90cbd-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="90cbd-105">Els valors reals del projecte es remunten als seus documents d'origen.</span><span class="sxs-lookup"><span data-stu-id="90cbd-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="90cbd-106">Aquests documents d'origen inclouen entrades de temps, despeses i del llibre diari, i també factures.</span><span class="sxs-lookup"><span data-stu-id="90cbd-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![Com es remunten els valors reals als documents d'origen](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="90cbd-108">Enviant una entrada de temps</span><span class="sxs-lookup"><span data-stu-id="90cbd-108">Submitting a time entry</span></span>

<span data-ttu-id="90cbd-109">Al PSA, quan s'envia una entrada de temps per a un projecte assignat a una línia de contracte de temps i materials, es creen dues línies del llibre diari.</span><span class="sxs-lookup"><span data-stu-id="90cbd-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="90cbd-110">Una línia és per al cost i l'altra línia és per a les vendes no facturades.</span><span class="sxs-lookup"><span data-stu-id="90cbd-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="90cbd-111">Quan s'envia una entrada de temps per a un projecte assignat a una línia de contracte de preu fix, es crea una línia del llibre diari només per al cost.</span><span class="sxs-lookup"><span data-stu-id="90cbd-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="90cbd-112">La lògica per introduir els preus per defecte resideix a la línia del llibre diari.</span><span class="sxs-lookup"><span data-stu-id="90cbd-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="90cbd-113">Tots els valors de camp d'una entrada de temps es copien a la línia del llibre diari.</span><span class="sxs-lookup"><span data-stu-id="90cbd-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="90cbd-114">Aquests camps són la data de la transacció, la línia de contracte a la qual està assignada el projecte i el resultat de moneda a la llista de preus adequada.</span><span class="sxs-lookup"><span data-stu-id="90cbd-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="90cbd-115">Els camps que afecten els preus per defecte, **com** ara Funció i **Unitat organitzativa**, fan que s'introdueixi per defecte un preu adient a la línia del llibre diari.</span><span class="sxs-lookup"><span data-stu-id="90cbd-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="90cbd-116">Si afegiu un camp personalitzat a l'entrada de temps i voleu que el valor del camp es propagui a valors reals, creeu el camp a l'entitat Valors reals i utilitzeu assignacions de camps per copiar el camp de l'entrada de temps al valor real.</span><span class="sxs-lookup"><span data-stu-id="90cbd-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="90cbd-117">Enviar una entrada de despesa</span><span class="sxs-lookup"><span data-stu-id="90cbd-117">Submitting an expense entry</span></span>

<span data-ttu-id="90cbd-118">Al PSA, quan s'envia una entrada de despesa per a un projecte assignat a una línia de contracte de temps i materials, es creen dues línies del llibre diari.</span><span class="sxs-lookup"><span data-stu-id="90cbd-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="90cbd-119">Una línia és per al cost i l'altra línia és per a les vendes no facturades.</span><span class="sxs-lookup"><span data-stu-id="90cbd-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="90cbd-120">Quan s'envia una entrada de despesa per a un projecte assignat a una línia de contracte de preu fix, es crea una línia del llibre diari només per al cost.</span><span class="sxs-lookup"><span data-stu-id="90cbd-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="90cbd-121">La lògica per a la introducció dels preus per defecte de les despeses es basa en la categoria de despeses que s'ha seleccionat a la pàgina **Entrada de despeses**.</span><span class="sxs-lookup"><span data-stu-id="90cbd-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="90cbd-122">La data de la transacció, la línia de contracte a la qual està assignada el projecte i la moneda s'utilitzen per determinar la llista de preus adequada.</span><span class="sxs-lookup"><span data-stu-id="90cbd-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="90cbd-123">No obstant, per al preu en si mateix, l'import que l'usuari ha introduït es defineix directament a les línies del llibre diari de despesa relacionades per al cost i les vendes per defecte.</span><span class="sxs-lookup"><span data-stu-id="90cbd-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="90cbd-124">A la versió actual del PSA, l'entrada basada en categories per a preus per unitat per defecte a les entrades de despesa no està disponible.</span><span class="sxs-lookup"><span data-stu-id="90cbd-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-journals-to-record-costs"></a><span data-ttu-id="90cbd-125">Utilitzar llibres diari per registrar costos de registre</span><span class="sxs-lookup"><span data-stu-id="90cbd-125">Using journals to record costs</span></span>

<span data-ttu-id="90cbd-126">Al PSA, els llibres diari permeten registrar costos o ingressos en classes de material, quota, temps, despeses o transaccions tributàries.</span><span class="sxs-lookup"><span data-stu-id="90cbd-126">In PSA, journals let you record cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="90cbd-127">Un llibre diari té una capçalera, línies i una acció **Confirmació**.</span><span class="sxs-lookup"><span data-stu-id="90cbd-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="90cbd-128">Aquests són alguns escenaris en què podeu utilitzar un llibre diari:</span><span class="sxs-lookup"><span data-stu-id="90cbd-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="90cbd-129">Heu de registrar els costos reals materials i les vendes d'un projecte.</span><span class="sxs-lookup"><span data-stu-id="90cbd-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="90cbd-130">Heu d'avançar els valors reals de la transacció des d'un altre sistema al PSA.</span><span class="sxs-lookup"><span data-stu-id="90cbd-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="90cbd-131">Heu de registrar les despeses que s'han produït en un altre sistema, com ara les despeses d'adquisició o subcontractacions.</span><span class="sxs-lookup"><span data-stu-id="90cbd-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="90cbd-132">Enregistrament de valors reals a partir d'esdeveniments de projecte</span><span class="sxs-lookup"><span data-stu-id="90cbd-132">Recording actuals based on project events</span></span>

<span data-ttu-id="90cbd-133">El PSA registra totes les transaccions financeres que es produeixen durant un projecte.</span><span class="sxs-lookup"><span data-stu-id="90cbd-133">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="90cbd-134">Aquestes transaccions es registren com a **valors reals**.</span><span class="sxs-lookup"><span data-stu-id="90cbd-134">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="90cbd-135">Les taules següents mostren els diferents tipus de valors reals que s'han creat, en funció de si el projecte és un projecte de temps i materials o de preu fix, si es troba a la fase de prevenda o si és un projecte intern.</span><span class="sxs-lookup"><span data-stu-id="90cbd-135">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="90cbd-136">**El recurs pertany a la mateixa unitat organitzativa que la unitat de contractació del projecte**</span><span class="sxs-lookup"><span data-stu-id="90cbd-136">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="90cbd-137">Incidència</span><span class="sxs-lookup"><span data-stu-id="90cbd-137">Event</span></span></th>
<th colspan="4"><span data-ttu-id="90cbd-138">Projecte facturable o venut</span><span class="sxs-lookup"><span data-stu-id="90cbd-138">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="90cbd-139">Projecte a la fase de prevenda</span><span class="sxs-lookup"><span data-stu-id="90cbd-139">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="90cbd-140">Projecte intern</span><span class="sxs-lookup"><span data-stu-id="90cbd-140">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="90cbd-141">Temps i materials</span><span class="sxs-lookup"><span data-stu-id="90cbd-141">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="90cbd-142">Preu fix</span><span class="sxs-lookup"><span data-stu-id="90cbd-142">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="90cbd-143">Valors reals</span><span class="sxs-lookup"><span data-stu-id="90cbd-143">Actuals</span></span></th>
<th><span data-ttu-id="90cbd-144">Moneda de transacció</span><span class="sxs-lookup"><span data-stu-id="90cbd-144">Transaction currency</span></span></th>
<th><span data-ttu-id="90cbd-145">Preu fix</span><span class="sxs-lookup"><span data-stu-id="90cbd-145">Fixed price</span></span></th>
<th><span data-ttu-id="90cbd-146">Moneda de transacció</span><span class="sxs-lookup"><span data-stu-id="90cbd-146">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="90cbd-147">Es crea una entrada de temps.</span><span class="sxs-lookup"><span data-stu-id="90cbd-147">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="90cbd-148">No hi ha activitat a l'entitat Valors reals</span><span class="sxs-lookup"><span data-stu-id="90cbd-148">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90cbd-149">S'envia una entrada de temps.</span><span class="sxs-lookup"><span data-stu-id="90cbd-149">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="90cbd-150">No hi ha activitat a l'entitat Valors reals</span><span class="sxs-lookup"><span data-stu-id="90cbd-150">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="90cbd-151">El temps s'aprova, i no es produeix cap canvi o augment de les hores facturables durant l'aprovació.</span><span class="sxs-lookup"><span data-stu-id="90cbd-151">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="90cbd-152">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="90cbd-152">Cost actual</span></span></td>
<td><span data-ttu-id="90cbd-153">Moneda de la unitat de contractació</span><span class="sxs-lookup"><span data-stu-id="90cbd-153">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="90cbd-154">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="90cbd-154">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="90cbd-155">Moneda de la unitat de contractació</span><span class="sxs-lookup"><span data-stu-id="90cbd-155">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="90cbd-156">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="90cbd-156">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="90cbd-157">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="90cbd-157">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90cbd-158">Valor real de les vendes no facturades - Imputable</span><span class="sxs-lookup"><span data-stu-id="90cbd-158">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="90cbd-159">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="90cbd-159">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="90cbd-160">El temps s'aprova, i es produeix una reducció de les hores facturables durant l'aprovació.</span><span class="sxs-lookup"><span data-stu-id="90cbd-160">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="90cbd-161">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="90cbd-161">Cost actual</span></span></td>
<td><span data-ttu-id="90cbd-162">Moneda de la unitat de contractació</span><span class="sxs-lookup"><span data-stu-id="90cbd-162">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="90cbd-163">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="90cbd-163">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="90cbd-164">Moneda de la unitat de contractació</span><span class="sxs-lookup"><span data-stu-id="90cbd-164">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="90cbd-165">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="90cbd-165">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="90cbd-166">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="90cbd-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90cbd-167">Valor real de les vendes no facturades - Imputable per a la nova quantitat</span><span class="sxs-lookup"><span data-stu-id="90cbd-167">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="90cbd-168">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="90cbd-168">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90cbd-169">Valor real de les vendes no facturades - No imputable per la diferència</span><span class="sxs-lookup"><span data-stu-id="90cbd-169">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="90cbd-170">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="90cbd-170">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="90cbd-171">Es confirma una factura, i no es produeix cap canvi o augment de les hores facturables.</span><span class="sxs-lookup"><span data-stu-id="90cbd-171">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="90cbd-172">Reversió de vendes no facturades</span><span class="sxs-lookup"><span data-stu-id="90cbd-172">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="90cbd-173">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="90cbd-173">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="90cbd-174">Vendes facturades per fita</span><span class="sxs-lookup"><span data-stu-id="90cbd-174">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="90cbd-175">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="90cbd-175">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="90cbd-176">No aplicable</span><span class="sxs-lookup"><span data-stu-id="90cbd-176">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="90cbd-177">No aplicable</span><span class="sxs-lookup"><span data-stu-id="90cbd-177">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90cbd-178">Vendes facturades</span><span class="sxs-lookup"><span data-stu-id="90cbd-178">Billed sales</span></span></td>
<td><span data-ttu-id="90cbd-179">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="90cbd-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="90cbd-180">Es confirma una factura, i es produeix una disminució de les hores facturables.</span><span class="sxs-lookup"><span data-stu-id="90cbd-180">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="90cbd-181">Reversió de vendes no facturades</span><span class="sxs-lookup"><span data-stu-id="90cbd-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="90cbd-182">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="90cbd-182">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="90cbd-183">No aplicable</span><span class="sxs-lookup"><span data-stu-id="90cbd-183">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="90cbd-184">No aplicable</span><span class="sxs-lookup"><span data-stu-id="90cbd-184">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="90cbd-185">No aplicable</span><span class="sxs-lookup"><span data-stu-id="90cbd-185">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="90cbd-186">No aplicable</span><span class="sxs-lookup"><span data-stu-id="90cbd-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90cbd-187">Vendes facturades - Imputable per a la nova quantitat</span><span class="sxs-lookup"><span data-stu-id="90cbd-187">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="90cbd-188">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="90cbd-188">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90cbd-189">Vendes facturades - No imputable per la diferència</span><span class="sxs-lookup"><span data-stu-id="90cbd-189">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="90cbd-190">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="90cbd-190">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="90cbd-191">Una factura es corregeix per augmentar la quantitat imputable.</span><span class="sxs-lookup"><span data-stu-id="90cbd-191">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="90cbd-192">Vendes facturades - Reversió</span><span class="sxs-lookup"><span data-stu-id="90cbd-192">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="90cbd-193">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="90cbd-193">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="90cbd-194">Reversió de vendes facturades per fita</span><span class="sxs-lookup"><span data-stu-id="90cbd-194">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="90cbd-195">Canvi en l'estat de la fita de <strong>Facturada</strong> a <strong>Llesta per facturar</strong></span><span class="sxs-lookup"><span data-stu-id="90cbd-195">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="90cbd-196">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="90cbd-196">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="90cbd-197">No aplicable</span><span class="sxs-lookup"><span data-stu-id="90cbd-197">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="90cbd-198">No aplicable</span><span class="sxs-lookup"><span data-stu-id="90cbd-198">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90cbd-199">Vendes facturades</span><span class="sxs-lookup"><span data-stu-id="90cbd-199">Billed sales</span></span></td>
<td><span data-ttu-id="90cbd-200">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="90cbd-200">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="90cbd-201">Una factura es corregeix per reduir la quantitat imputable.</span><span class="sxs-lookup"><span data-stu-id="90cbd-201">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="90cbd-202">Vendes facturades - Reversió</span><span class="sxs-lookup"><span data-stu-id="90cbd-202">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="90cbd-203">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="90cbd-203">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90cbd-204">Vendes facturades per a la nova quantitat</span><span class="sxs-lookup"><span data-stu-id="90cbd-204">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="90cbd-205">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="90cbd-205">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90cbd-206">Vendes no facturades - Imputable per la diferència</span><span class="sxs-lookup"><span data-stu-id="90cbd-206">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="90cbd-207">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="90cbd-207">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="90cbd-208">**El recurs pertany a una unitat organitzativa diferent de la unitat de contractació del projecte**</span><span class="sxs-lookup"><span data-stu-id="90cbd-208">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="90cbd-209">Incidència</span><span class="sxs-lookup"><span data-stu-id="90cbd-209">Event</span></span></th>
<th colspan="4"><span data-ttu-id="90cbd-210">Projecte facturable o venut</span><span class="sxs-lookup"><span data-stu-id="90cbd-210">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="90cbd-211">Projecte a la fase de prevenda</span><span class="sxs-lookup"><span data-stu-id="90cbd-211">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="90cbd-212">Projecte intern</span><span class="sxs-lookup"><span data-stu-id="90cbd-212">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="90cbd-213">Temps i materials</span><span class="sxs-lookup"><span data-stu-id="90cbd-213">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="90cbd-214">Preu fix</span><span class="sxs-lookup"><span data-stu-id="90cbd-214">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="90cbd-215">Valors reals</span><span class="sxs-lookup"><span data-stu-id="90cbd-215">Actuals</span></span></th>
<th><span data-ttu-id="90cbd-216">Moneda de transacció</span><span class="sxs-lookup"><span data-stu-id="90cbd-216">Transaction currency</span></span></th>
<th><span data-ttu-id="90cbd-217">Preu fix</span><span class="sxs-lookup"><span data-stu-id="90cbd-217">Fixed price</span></span></th>
<th><span data-ttu-id="90cbd-218">Moneda de transacció</span><span class="sxs-lookup"><span data-stu-id="90cbd-218">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="90cbd-219">Es crea una entrada de temps.</span><span class="sxs-lookup"><span data-stu-id="90cbd-219">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="90cbd-220">No hi ha activitat a l'entitat Valors reals</span><span class="sxs-lookup"><span data-stu-id="90cbd-220">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90cbd-221">S'envia una entrada de temps.</span><span class="sxs-lookup"><span data-stu-id="90cbd-221">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="90cbd-222">No hi ha activitat a l'entitat Valors reals</span><span class="sxs-lookup"><span data-stu-id="90cbd-222">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="90cbd-223">El temps s'aprova, i no es produeix cap canvi o augment de les hores facturables durant l'aprovació.</span><span class="sxs-lookup"><span data-stu-id="90cbd-223">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="90cbd-224">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="90cbd-224">Cost actual</span></span></td>
<td><span data-ttu-id="90cbd-225">Moneda de la unitat de contractació</span><span class="sxs-lookup"><span data-stu-id="90cbd-225">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="90cbd-226">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="90cbd-226">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="90cbd-227">Moneda de la unitat de contractació</span><span class="sxs-lookup"><span data-stu-id="90cbd-227">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="90cbd-228">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="90cbd-228">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="90cbd-229">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="90cbd-229">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90cbd-230">Valor real de les vendes no facturades - Imputable</span><span class="sxs-lookup"><span data-stu-id="90cbd-230">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="90cbd-231">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="90cbd-231">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90cbd-232">Cost de la unitat de recursos</span><span class="sxs-lookup"><span data-stu-id="90cbd-232">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="90cbd-233">Moneda de la unitat de recursos</span><span class="sxs-lookup"><span data-stu-id="90cbd-233">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90cbd-234">Vendes interorganitzatives</span><span class="sxs-lookup"><span data-stu-id="90cbd-234">Interorganizational sales</span></span></td>
<td><span data-ttu-id="90cbd-235">Moneda de la unitat de contractació</span><span class="sxs-lookup"><span data-stu-id="90cbd-235">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="90cbd-236">El temps s'aprova, i es produeix una reducció de les hores facturables durant l'aprovació.</span><span class="sxs-lookup"><span data-stu-id="90cbd-236">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="90cbd-237">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="90cbd-237">Cost actual</span></span></td>
<td><span data-ttu-id="90cbd-238">Moneda de la unitat de contractació</span><span class="sxs-lookup"><span data-stu-id="90cbd-238">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="90cbd-239">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="90cbd-239">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="90cbd-240">Moneda de la unitat de contractació</span><span class="sxs-lookup"><span data-stu-id="90cbd-240">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="90cbd-241">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="90cbd-241">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="90cbd-242">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="90cbd-242">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90cbd-243">Cost de la unitat de recursos</span><span class="sxs-lookup"><span data-stu-id="90cbd-243">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="90cbd-244">Moneda de la unitat de recursos</span><span class="sxs-lookup"><span data-stu-id="90cbd-244">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90cbd-245">Vendes interorganitzatives</span><span class="sxs-lookup"><span data-stu-id="90cbd-245">Interorganizational sales</span></span></td>
<td><span data-ttu-id="90cbd-246">Moneda de la unitat de contractació</span><span class="sxs-lookup"><span data-stu-id="90cbd-246">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90cbd-247">Valor real de les vendes no facturades - Imputable per a la nova quantitat</span><span class="sxs-lookup"><span data-stu-id="90cbd-247">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="90cbd-248">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="90cbd-248">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90cbd-249">Valor real de les vendes no facturades - No imputable per la diferència</span><span class="sxs-lookup"><span data-stu-id="90cbd-249">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="90cbd-250">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="90cbd-250">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="90cbd-251">Es confirma una factura, i no es produeix cap canvi o augment de les hores facturables.</span><span class="sxs-lookup"><span data-stu-id="90cbd-251">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="90cbd-252">Reversió de vendes no facturades</span><span class="sxs-lookup"><span data-stu-id="90cbd-252">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="90cbd-253">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="90cbd-253">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="90cbd-254">Vendes facturades per fita</span><span class="sxs-lookup"><span data-stu-id="90cbd-254">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="90cbd-255">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="90cbd-255">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="90cbd-256">No aplicable</span><span class="sxs-lookup"><span data-stu-id="90cbd-256">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="90cbd-257">No aplicable</span><span class="sxs-lookup"><span data-stu-id="90cbd-257">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90cbd-258">Vendes facturades</span><span class="sxs-lookup"><span data-stu-id="90cbd-258">Billed sales</span></span></td>
<td><span data-ttu-id="90cbd-259">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="90cbd-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="90cbd-260">Es confirma una factura, i es produeix una disminució de les hores facturables.</span><span class="sxs-lookup"><span data-stu-id="90cbd-260">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="90cbd-261">Reversió de vendes no facturades</span><span class="sxs-lookup"><span data-stu-id="90cbd-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="90cbd-262">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="90cbd-262">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="90cbd-263">No aplicable</span><span class="sxs-lookup"><span data-stu-id="90cbd-263">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="90cbd-264">No aplicable</span><span class="sxs-lookup"><span data-stu-id="90cbd-264">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="90cbd-265">No aplicable</span><span class="sxs-lookup"><span data-stu-id="90cbd-265">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="90cbd-266">No aplicable</span><span class="sxs-lookup"><span data-stu-id="90cbd-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90cbd-267">Vendes facturades - Imputable per a la nova quantitat</span><span class="sxs-lookup"><span data-stu-id="90cbd-267">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="90cbd-268">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="90cbd-268">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90cbd-269">Vendes facturades - No imputable per la diferència</span><span class="sxs-lookup"><span data-stu-id="90cbd-269">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="90cbd-270">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="90cbd-270">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="90cbd-271">Una factura es corregeix per augmentar la quantitat imputable.</span><span class="sxs-lookup"><span data-stu-id="90cbd-271">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="90cbd-272">Vendes facturades - Reversió</span><span class="sxs-lookup"><span data-stu-id="90cbd-272">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="90cbd-273">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="90cbd-273">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="90cbd-274">Reversió de vendes facturades per fita</span><span class="sxs-lookup"><span data-stu-id="90cbd-274">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="90cbd-275">Canvi en l'estat de la fita de <strong>Facturada</strong> a <strong>Llesta per facturar</strong></span><span class="sxs-lookup"><span data-stu-id="90cbd-275">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="90cbd-276">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="90cbd-276">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="90cbd-277">No aplicable</span><span class="sxs-lookup"><span data-stu-id="90cbd-277">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="90cbd-278">No aplicable</span><span class="sxs-lookup"><span data-stu-id="90cbd-278">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90cbd-279">Vendes facturades</span><span class="sxs-lookup"><span data-stu-id="90cbd-279">Billed sales</span></span></td>
<td><span data-ttu-id="90cbd-280">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="90cbd-280">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="90cbd-281">Una factura es corregeix per reduir la quantitat imputable.</span><span class="sxs-lookup"><span data-stu-id="90cbd-281">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="90cbd-282">Vendes facturades - Reversió</span><span class="sxs-lookup"><span data-stu-id="90cbd-282">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="90cbd-283">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="90cbd-283">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90cbd-284">Vendes facturades per a la nova quantitat</span><span class="sxs-lookup"><span data-stu-id="90cbd-284">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="90cbd-285">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="90cbd-285">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90cbd-286">Vendes no facturades - Imputable per la diferència</span><span class="sxs-lookup"><span data-stu-id="90cbd-286">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="90cbd-287">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="90cbd-287">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
