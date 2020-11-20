---
title: Informació general dels valors reals
description: Aquest tema proporciona informació sobre els valors reals del projecte.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 08/03/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: cf9e36c99790b77f0ed6490f49b4ebeb043bcdf6
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4129756"
---
# <a name="actuals-overview"></a><span data-ttu-id="6c3d3-103">Informació general dels valors reals</span><span class="sxs-lookup"><span data-stu-id="6c3d3-103">Actuals overview</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="6c3d3-104">Els valors reals són la quantitat de treball que s'ha completat en un projecte.</span><span class="sxs-lookup"><span data-stu-id="6c3d3-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="6c3d3-105">Els valors reals del projecte es remunten als seus documents d'origen.</span><span class="sxs-lookup"><span data-stu-id="6c3d3-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="6c3d3-106">Aquests documents d'origen inclouen entrades de temps, despeses i del llibre diari, i també factures.</span><span class="sxs-lookup"><span data-stu-id="6c3d3-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![Com es remunten els valors reals als documents d'origen](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="6c3d3-108">Enviant una entrada de temps</span><span class="sxs-lookup"><span data-stu-id="6c3d3-108">Submitting a time entry</span></span>

<span data-ttu-id="6c3d3-109">Al PSA, quan s'envia una entrada de temps per a un projecte assignat a una línia de contracte de temps i materials, es creen dues línies del llibre diari.</span><span class="sxs-lookup"><span data-stu-id="6c3d3-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="6c3d3-110">Una línia és per al cost i l'altra línia és per a les vendes no facturades.</span><span class="sxs-lookup"><span data-stu-id="6c3d3-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="6c3d3-111">Quan s'envia una entrada de temps per a un projecte assignat a una línia de contracte de preu fix, es crea una línia del llibre diari només per al cost.</span><span class="sxs-lookup"><span data-stu-id="6c3d3-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="6c3d3-112">La lògica per introduir els preus per defecte resideix a la línia del llibre diari.</span><span class="sxs-lookup"><span data-stu-id="6c3d3-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="6c3d3-113">Tots els valors de camp d'una entrada de temps es copien a la línia del llibre diari.</span><span class="sxs-lookup"><span data-stu-id="6c3d3-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="6c3d3-114">Aquests camps són la data de la transacció, la línia de contracte a la qual està assignada el projecte i el resultat de moneda a la llista de preus adequada.</span><span class="sxs-lookup"><span data-stu-id="6c3d3-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="6c3d3-115">Els camps que afecten els preus per defecte, **com** ara Funció i **Unitat organitzativa**, fan que s'introdueixi per defecte un preu adient a la línia del llibre diari.</span><span class="sxs-lookup"><span data-stu-id="6c3d3-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="6c3d3-116">Si afegiu un camp personalitzat a l'entrada de temps i voleu que el valor del camp es propagui a valors reals, creeu el camp a l'entitat Valors reals i utilitzeu assignacions de camps per copiar el camp de l'entrada de temps al valor real.</span><span class="sxs-lookup"><span data-stu-id="6c3d3-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="6c3d3-117">Enviar una entrada de despesa</span><span class="sxs-lookup"><span data-stu-id="6c3d3-117">Submitting an expense entry</span></span>

<span data-ttu-id="6c3d3-118">Al PSA, quan s'envia una entrada de despesa per a un projecte assignat a una línia de contracte de temps i materials, es creen dues línies del llibre diari.</span><span class="sxs-lookup"><span data-stu-id="6c3d3-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="6c3d3-119">Una línia és per al cost i l'altra línia és per a les vendes no facturades.</span><span class="sxs-lookup"><span data-stu-id="6c3d3-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="6c3d3-120">Quan s'envia una entrada de despesa per a un projecte assignat a una línia de contracte de preu fix, es crea una línia del llibre diari només per al cost.</span><span class="sxs-lookup"><span data-stu-id="6c3d3-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="6c3d3-121">La lògica per a la introducció dels preus per defecte de les despeses es basa en la categoria de despeses que s'ha seleccionat a la pàgina **Entrada de despeses**.</span><span class="sxs-lookup"><span data-stu-id="6c3d3-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="6c3d3-122">La data de la transacció, la línia de contracte a la qual està assignada el projecte i la moneda s'utilitzen per determinar la llista de preus adequada.</span><span class="sxs-lookup"><span data-stu-id="6c3d3-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="6c3d3-123">No obstant, per al preu en si mateix, l'import que l'usuari ha introduït es defineix directament a les línies del llibre diari de despesa relacionades per al cost i les vendes per defecte.</span><span class="sxs-lookup"><span data-stu-id="6c3d3-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="6c3d3-124">A la versió actual del PSA, l'entrada basada en categories per a preus per unitat per defecte a les entrades de despesa no està disponible.</span><span class="sxs-lookup"><span data-stu-id="6c3d3-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-entry-journals-to-record-costs"></a><span data-ttu-id="6c3d3-125">Utilitzar llibres diaris d'entrada per registrar costos de registre</span><span class="sxs-lookup"><span data-stu-id="6c3d3-125">Using Entry journals to record costs</span></span>

<span data-ttu-id="6c3d3-126">Al PSA, els llibres diaris d'entrada permeten registrar els costos o ingressos en classes de material, quota, temps, despeses o transaccions tributàries.</span><span class="sxs-lookup"><span data-stu-id="6c3d3-126">In PSA, Entry journals let you record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="6c3d3-127">Un llibre diari té una capçalera, línies i una acció **Confirmació**.</span><span class="sxs-lookup"><span data-stu-id="6c3d3-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="6c3d3-128">Aquests són alguns escenaris en què podeu utilitzar un llibre diari:</span><span class="sxs-lookup"><span data-stu-id="6c3d3-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="6c3d3-129">Heu de registrar els costos reals materials i les vendes d'un projecte.</span><span class="sxs-lookup"><span data-stu-id="6c3d3-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="6c3d3-130">Heu d'avançar els valors reals de la transacció des d'un altre sistema al PSA.</span><span class="sxs-lookup"><span data-stu-id="6c3d3-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="6c3d3-131">Heu de registrar les despeses que s'han produït en un altre sistema, com ara les despeses d'adquisició o subcontractacions.</span><span class="sxs-lookup"><span data-stu-id="6c3d3-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6c3d3-132">L'ús de diaris d'entrada per a la creació de valors reals només l'ha de fer un usuari plenament conscient de l'impacte comptable que tenen els valors reals al projecte.</span><span class="sxs-lookup"><span data-stu-id="6c3d3-132">Using Entry journals to create actuals should be done only by a user who is fully aware of the accounting impact the Actuals have on the project.</span></span> <span data-ttu-id="6c3d3-133">El motiu és que l'aplicació no valida el tipus de línia del llibre diari ni el preu relacionat que s'introdueix a la línia del llibre diari.</span><span class="sxs-lookup"><span data-stu-id="6c3d3-133">This is because the application does not validate the journal line type, or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="6c3d3-134">A causa de l'impacte d'aquest tipus de llibre diari, actueu amb extremada cura en relació amb qui té accés a la creació de llibres diaris d'entrada.</span><span class="sxs-lookup"><span data-stu-id="6c3d3-134">Because of the impact of this journal type, exercise adequate caution in who is given access to create Entry journals.</span></span>     


## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="6c3d3-135">Enregistrament de valors reals a partir d'esdeveniments de projecte</span><span class="sxs-lookup"><span data-stu-id="6c3d3-135">Recording actuals based on project events</span></span>

<span data-ttu-id="6c3d3-136">El PSA registra totes les transaccions financeres que es produeixen durant un projecte.</span><span class="sxs-lookup"><span data-stu-id="6c3d3-136">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="6c3d3-137">Aquestes transaccions es registren com a **valors reals**.</span><span class="sxs-lookup"><span data-stu-id="6c3d3-137">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="6c3d3-138">Les taules següents mostren els diferents tipus de valors reals que s'han creat, en funció de si el projecte és un projecte de temps i materials o de preu fix, si es troba a la fase de prevenda o si és un projecte intern.</span><span class="sxs-lookup"><span data-stu-id="6c3d3-138">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="6c3d3-139">**El recurs pertany a la mateixa unitat organitzativa que la unitat de contractació del projecte**</span><span class="sxs-lookup"><span data-stu-id="6c3d3-139">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="6c3d3-140">Incidència</span><span class="sxs-lookup"><span data-stu-id="6c3d3-140">Event</span></span></th>
<th colspan="4"><span data-ttu-id="6c3d3-141">Projecte facturable o venut</span><span class="sxs-lookup"><span data-stu-id="6c3d3-141">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="6c3d3-142">Projecte a la fase de prevenda</span><span class="sxs-lookup"><span data-stu-id="6c3d3-142">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="6c3d3-143">Projecte intern</span><span class="sxs-lookup"><span data-stu-id="6c3d3-143">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="6c3d3-144">Temps i materials</span><span class="sxs-lookup"><span data-stu-id="6c3d3-144">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="6c3d3-145">Preu fix</span><span class="sxs-lookup"><span data-stu-id="6c3d3-145">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="6c3d3-146">Valors reals</span><span class="sxs-lookup"><span data-stu-id="6c3d3-146">Actuals</span></span></th>
<th><span data-ttu-id="6c3d3-147">Moneda de transacció</span><span class="sxs-lookup"><span data-stu-id="6c3d3-147">Transaction currency</span></span></th>
<th><span data-ttu-id="6c3d3-148">Preu fix</span><span class="sxs-lookup"><span data-stu-id="6c3d3-148">Fixed price</span></span></th>
<th><span data-ttu-id="6c3d3-149">Moneda de transacció</span><span class="sxs-lookup"><span data-stu-id="6c3d3-149">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6c3d3-150">Es crea una entrada de temps.</span><span class="sxs-lookup"><span data-stu-id="6c3d3-150">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="6c3d3-151">No hi ha activitat a l'entitat Valors reals</span><span class="sxs-lookup"><span data-stu-id="6c3d3-151">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c3d3-152">S'envia una entrada de temps.</span><span class="sxs-lookup"><span data-stu-id="6c3d3-152">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="6c3d3-153">No hi ha activitat a l'entitat Valors reals</span><span class="sxs-lookup"><span data-stu-id="6c3d3-153">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="6c3d3-154">El temps s'aprova, i no es produeix cap canvi o augment de les hores facturables durant l'aprovació.</span><span class="sxs-lookup"><span data-stu-id="6c3d3-154">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="6c3d3-155">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="6c3d3-155">Cost actual</span></span></td>
<td><span data-ttu-id="6c3d3-156">Moneda de la unitat de contractació</span><span class="sxs-lookup"><span data-stu-id="6c3d3-156">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="6c3d3-157">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="6c3d3-157">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="6c3d3-158">Moneda de la unitat de contractació</span><span class="sxs-lookup"><span data-stu-id="6c3d3-158">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="6c3d3-159">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="6c3d3-159">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="6c3d3-160">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="6c3d3-160">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c3d3-161">Valor real de les vendes no facturades - Imputable</span><span class="sxs-lookup"><span data-stu-id="6c3d3-161">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="6c3d3-162">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="6c3d3-162">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="6c3d3-163">El temps s'aprova, i es produeix una reducció de les hores facturables durant l'aprovació.</span><span class="sxs-lookup"><span data-stu-id="6c3d3-163">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="6c3d3-164">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="6c3d3-164">Cost actual</span></span></td>
<td><span data-ttu-id="6c3d3-165">Moneda de la unitat de contractació</span><span class="sxs-lookup"><span data-stu-id="6c3d3-165">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="6c3d3-166">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="6c3d3-166">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="6c3d3-167">Moneda de la unitat de contractació</span><span class="sxs-lookup"><span data-stu-id="6c3d3-167">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="6c3d3-168">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="6c3d3-168">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="6c3d3-169">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="6c3d3-169">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c3d3-170">Valor real de les vendes no facturades - Imputable per a la nova quantitat</span><span class="sxs-lookup"><span data-stu-id="6c3d3-170">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="6c3d3-171">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="6c3d3-171">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c3d3-172">Valor real de les vendes no facturades - No imputable per la diferència</span><span class="sxs-lookup"><span data-stu-id="6c3d3-172">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="6c3d3-173">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="6c3d3-173">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="6c3d3-174">Es confirma una factura, i no es produeix cap canvi o augment de les hores facturables.</span><span class="sxs-lookup"><span data-stu-id="6c3d3-174">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="6c3d3-175">Reversió de vendes no facturades</span><span class="sxs-lookup"><span data-stu-id="6c3d3-175">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="6c3d3-176">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="6c3d3-176">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="6c3d3-177">Vendes facturades per fita</span><span class="sxs-lookup"><span data-stu-id="6c3d3-177">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="6c3d3-178">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="6c3d3-178">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="6c3d3-179">No aplicable</span><span class="sxs-lookup"><span data-stu-id="6c3d3-179">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="6c3d3-180">No aplicable</span><span class="sxs-lookup"><span data-stu-id="6c3d3-180">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c3d3-181">Vendes facturades</span><span class="sxs-lookup"><span data-stu-id="6c3d3-181">Billed sales</span></span></td>
<td><span data-ttu-id="6c3d3-182">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="6c3d3-182">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="6c3d3-183">Es confirma una factura, i es produeix una disminució de les hores facturables.</span><span class="sxs-lookup"><span data-stu-id="6c3d3-183">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="6c3d3-184">Reversió de vendes no facturades</span><span class="sxs-lookup"><span data-stu-id="6c3d3-184">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="6c3d3-185">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="6c3d3-185">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="6c3d3-186">No aplicable</span><span class="sxs-lookup"><span data-stu-id="6c3d3-186">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="6c3d3-187">No aplicable</span><span class="sxs-lookup"><span data-stu-id="6c3d3-187">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="6c3d3-188">No aplicable</span><span class="sxs-lookup"><span data-stu-id="6c3d3-188">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="6c3d3-189">No aplicable</span><span class="sxs-lookup"><span data-stu-id="6c3d3-189">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c3d3-190">Vendes facturades - Imputable per a la nova quantitat</span><span class="sxs-lookup"><span data-stu-id="6c3d3-190">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="6c3d3-191">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="6c3d3-191">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c3d3-192">Vendes facturades - No imputable per la diferència</span><span class="sxs-lookup"><span data-stu-id="6c3d3-192">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="6c3d3-193">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="6c3d3-193">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="6c3d3-194">Una factura es corregeix per augmentar la quantitat imputable.</span><span class="sxs-lookup"><span data-stu-id="6c3d3-194">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="6c3d3-195">Vendes facturades - Reversió</span><span class="sxs-lookup"><span data-stu-id="6c3d3-195">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="6c3d3-196">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="6c3d3-196">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="6c3d3-197">Reversió de vendes facturades per fita</span><span class="sxs-lookup"><span data-stu-id="6c3d3-197">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="6c3d3-198">Canvi en l'estat de la fita de <strong>Facturada</strong> a <strong>Llesta per facturar</strong></span><span class="sxs-lookup"><span data-stu-id="6c3d3-198">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="6c3d3-199">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="6c3d3-199">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="6c3d3-200">No aplicable</span><span class="sxs-lookup"><span data-stu-id="6c3d3-200">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="6c3d3-201">No aplicable</span><span class="sxs-lookup"><span data-stu-id="6c3d3-201">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c3d3-202">Vendes facturades</span><span class="sxs-lookup"><span data-stu-id="6c3d3-202">Billed sales</span></span></td>
<td><span data-ttu-id="6c3d3-203">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="6c3d3-203">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="6c3d3-204">Una factura es corregeix per reduir la quantitat imputable.</span><span class="sxs-lookup"><span data-stu-id="6c3d3-204">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="6c3d3-205">Vendes facturades - Reversió</span><span class="sxs-lookup"><span data-stu-id="6c3d3-205">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="6c3d3-206">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="6c3d3-206">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c3d3-207">Vendes facturades per a la nova quantitat</span><span class="sxs-lookup"><span data-stu-id="6c3d3-207">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="6c3d3-208">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="6c3d3-208">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c3d3-209">Vendes no facturades - Imputable per la diferència</span><span class="sxs-lookup"><span data-stu-id="6c3d3-209">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="6c3d3-210">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="6c3d3-210">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6c3d3-211">**El recurs pertany a una unitat organitzativa diferent de la unitat de contractació del projecte**</span><span class="sxs-lookup"><span data-stu-id="6c3d3-211">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="6c3d3-212">Incidència</span><span class="sxs-lookup"><span data-stu-id="6c3d3-212">Event</span></span></th>
<th colspan="4"><span data-ttu-id="6c3d3-213">Projecte facturable o venut</span><span class="sxs-lookup"><span data-stu-id="6c3d3-213">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="6c3d3-214">Projecte a la fase de prevenda</span><span class="sxs-lookup"><span data-stu-id="6c3d3-214">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="6c3d3-215">Projecte intern</span><span class="sxs-lookup"><span data-stu-id="6c3d3-215">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="6c3d3-216">Temps i materials</span><span class="sxs-lookup"><span data-stu-id="6c3d3-216">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="6c3d3-217">Preu fix</span><span class="sxs-lookup"><span data-stu-id="6c3d3-217">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="6c3d3-218">Valors reals</span><span class="sxs-lookup"><span data-stu-id="6c3d3-218">Actuals</span></span></th>
<th><span data-ttu-id="6c3d3-219">Moneda de transacció</span><span class="sxs-lookup"><span data-stu-id="6c3d3-219">Transaction currency</span></span></th>
<th><span data-ttu-id="6c3d3-220">Preu fix</span><span class="sxs-lookup"><span data-stu-id="6c3d3-220">Fixed price</span></span></th>
<th><span data-ttu-id="6c3d3-221">Moneda de transacció</span><span class="sxs-lookup"><span data-stu-id="6c3d3-221">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6c3d3-222">Es crea una entrada de temps.</span><span class="sxs-lookup"><span data-stu-id="6c3d3-222">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="6c3d3-223">No hi ha activitat a l'entitat Valors reals</span><span class="sxs-lookup"><span data-stu-id="6c3d3-223">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c3d3-224">S'envia una entrada de temps.</span><span class="sxs-lookup"><span data-stu-id="6c3d3-224">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="6c3d3-225">No hi ha activitat a l'entitat Valors reals</span><span class="sxs-lookup"><span data-stu-id="6c3d3-225">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="6c3d3-226">El temps s'aprova, i no es produeix cap canvi o augment de les hores facturables durant l'aprovació.</span><span class="sxs-lookup"><span data-stu-id="6c3d3-226">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="6c3d3-227">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="6c3d3-227">Cost actual</span></span></td>
<td><span data-ttu-id="6c3d3-228">Moneda de la unitat de contractació</span><span class="sxs-lookup"><span data-stu-id="6c3d3-228">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="6c3d3-229">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="6c3d3-229">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="6c3d3-230">Moneda de la unitat de contractació</span><span class="sxs-lookup"><span data-stu-id="6c3d3-230">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="6c3d3-231">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="6c3d3-231">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="6c3d3-232">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="6c3d3-232">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c3d3-233">Valor real de les vendes no facturades - Imputable</span><span class="sxs-lookup"><span data-stu-id="6c3d3-233">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="6c3d3-234">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="6c3d3-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c3d3-235">Cost de la unitat de recursos</span><span class="sxs-lookup"><span data-stu-id="6c3d3-235">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="6c3d3-236">Moneda de la unitat de recursos</span><span class="sxs-lookup"><span data-stu-id="6c3d3-236">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c3d3-237">Vendes interorganitzatives</span><span class="sxs-lookup"><span data-stu-id="6c3d3-237">Interorganizational sales</span></span></td>
<td><span data-ttu-id="6c3d3-238">Moneda de la unitat de contractació</span><span class="sxs-lookup"><span data-stu-id="6c3d3-238">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="6c3d3-239">El temps s'aprova, i es produeix una reducció de les hores facturables durant l'aprovació.</span><span class="sxs-lookup"><span data-stu-id="6c3d3-239">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="6c3d3-240">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="6c3d3-240">Cost actual</span></span></td>
<td><span data-ttu-id="6c3d3-241">Moneda de la unitat de contractació</span><span class="sxs-lookup"><span data-stu-id="6c3d3-241">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="6c3d3-242">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="6c3d3-242">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="6c3d3-243">Moneda de la unitat de contractació</span><span class="sxs-lookup"><span data-stu-id="6c3d3-243">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="6c3d3-244">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="6c3d3-244">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="6c3d3-245">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="6c3d3-245">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c3d3-246">Cost de la unitat de recursos</span><span class="sxs-lookup"><span data-stu-id="6c3d3-246">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="6c3d3-247">Moneda de la unitat de recursos</span><span class="sxs-lookup"><span data-stu-id="6c3d3-247">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c3d3-248">Vendes interorganitzatives</span><span class="sxs-lookup"><span data-stu-id="6c3d3-248">Interorganizational sales</span></span></td>
<td><span data-ttu-id="6c3d3-249">Moneda de la unitat de contractació</span><span class="sxs-lookup"><span data-stu-id="6c3d3-249">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c3d3-250">Valor real de les vendes no facturades - Imputable per a la nova quantitat</span><span class="sxs-lookup"><span data-stu-id="6c3d3-250">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="6c3d3-251">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="6c3d3-251">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c3d3-252">Valor real de les vendes no facturades - No imputable per la diferència</span><span class="sxs-lookup"><span data-stu-id="6c3d3-252">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="6c3d3-253">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="6c3d3-253">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="6c3d3-254">Es confirma una factura, i no es produeix cap canvi o augment de les hores facturables.</span><span class="sxs-lookup"><span data-stu-id="6c3d3-254">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="6c3d3-255">Reversió de vendes no facturades</span><span class="sxs-lookup"><span data-stu-id="6c3d3-255">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="6c3d3-256">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="6c3d3-256">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="6c3d3-257">Vendes facturades per fita</span><span class="sxs-lookup"><span data-stu-id="6c3d3-257">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="6c3d3-258">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="6c3d3-258">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="6c3d3-259">No aplicable</span><span class="sxs-lookup"><span data-stu-id="6c3d3-259">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="6c3d3-260">No aplicable</span><span class="sxs-lookup"><span data-stu-id="6c3d3-260">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c3d3-261">Vendes facturades</span><span class="sxs-lookup"><span data-stu-id="6c3d3-261">Billed sales</span></span></td>
<td><span data-ttu-id="6c3d3-262">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="6c3d3-262">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="6c3d3-263">Es confirma una factura, i es produeix una disminució de les hores facturables.</span><span class="sxs-lookup"><span data-stu-id="6c3d3-263">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="6c3d3-264">Reversió de vendes no facturades</span><span class="sxs-lookup"><span data-stu-id="6c3d3-264">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="6c3d3-265">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="6c3d3-265">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="6c3d3-266">No aplicable</span><span class="sxs-lookup"><span data-stu-id="6c3d3-266">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="6c3d3-267">No aplicable</span><span class="sxs-lookup"><span data-stu-id="6c3d3-267">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="6c3d3-268">No aplicable</span><span class="sxs-lookup"><span data-stu-id="6c3d3-268">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="6c3d3-269">No aplicable</span><span class="sxs-lookup"><span data-stu-id="6c3d3-269">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c3d3-270">Vendes facturades - Imputable per a la nova quantitat</span><span class="sxs-lookup"><span data-stu-id="6c3d3-270">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="6c3d3-271">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="6c3d3-271">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c3d3-272">Vendes facturades - No imputable per la diferència</span><span class="sxs-lookup"><span data-stu-id="6c3d3-272">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="6c3d3-273">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="6c3d3-273">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="6c3d3-274">Una factura es corregeix per augmentar la quantitat imputable.</span><span class="sxs-lookup"><span data-stu-id="6c3d3-274">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="6c3d3-275">Vendes facturades - Reversió</span><span class="sxs-lookup"><span data-stu-id="6c3d3-275">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="6c3d3-276">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="6c3d3-276">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="6c3d3-277">Reversió de vendes facturades per fita</span><span class="sxs-lookup"><span data-stu-id="6c3d3-277">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="6c3d3-278">Canvi en l'estat de la fita de <strong>Facturada</strong> a <strong>Llesta per facturar</strong></span><span class="sxs-lookup"><span data-stu-id="6c3d3-278">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="6c3d3-279">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="6c3d3-279">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="6c3d3-280">No aplicable</span><span class="sxs-lookup"><span data-stu-id="6c3d3-280">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="6c3d3-281">No aplicable</span><span class="sxs-lookup"><span data-stu-id="6c3d3-281">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c3d3-282">Vendes facturades</span><span class="sxs-lookup"><span data-stu-id="6c3d3-282">Billed sales</span></span></td>
<td><span data-ttu-id="6c3d3-283">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="6c3d3-283">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="6c3d3-284">Una factura es corregeix per reduir la quantitat imputable.</span><span class="sxs-lookup"><span data-stu-id="6c3d3-284">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="6c3d3-285">Vendes facturades - Reversió</span><span class="sxs-lookup"><span data-stu-id="6c3d3-285">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="6c3d3-286">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="6c3d3-286">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c3d3-287">Vendes facturades per a la nova quantitat</span><span class="sxs-lookup"><span data-stu-id="6c3d3-287">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="6c3d3-288">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="6c3d3-288">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c3d3-289">Vendes no facturades - Imputable per la diferència</span><span class="sxs-lookup"><span data-stu-id="6c3d3-289">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="6c3d3-290">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="6c3d3-290">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
