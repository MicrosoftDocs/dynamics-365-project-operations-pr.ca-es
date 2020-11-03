---
title: Informació general dels valors reals
description: Aquest tema proporciona informació sobre els valors reals del projecte.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 9559cb2dcc38cb8058c5a9a3b97a35019fea486f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072410"
---
# <a name="actuals-overview"></a><span data-ttu-id="4eed5-103">Informació general dels valors reals</span><span class="sxs-lookup"><span data-stu-id="4eed5-103">Actuals overview</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="4eed5-104">Els valors reals són la quantitat de treball que s'ha completat en un projecte.</span><span class="sxs-lookup"><span data-stu-id="4eed5-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="4eed5-105">Els valors reals del projecte es remunten als seus documents d'origen.</span><span class="sxs-lookup"><span data-stu-id="4eed5-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="4eed5-106">Aquests documents d'origen inclouen entrades de temps, despeses i del llibre diari, i també factures.</span><span class="sxs-lookup"><span data-stu-id="4eed5-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![Com es remunten els valors reals als documents d'origen](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="4eed5-108">Enviant una entrada de temps</span><span class="sxs-lookup"><span data-stu-id="4eed5-108">Submitting a time entry</span></span>

<span data-ttu-id="4eed5-109">Al PSA, quan s'envia una entrada de temps per a un projecte assignat a una línia de contracte de temps i materials, es creen dues línies del llibre diari.</span><span class="sxs-lookup"><span data-stu-id="4eed5-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="4eed5-110">Una línia és per al cost i l'altra línia és per a les vendes no facturades.</span><span class="sxs-lookup"><span data-stu-id="4eed5-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="4eed5-111">Quan s'envia una entrada de temps per a un projecte assignat a una línia de contracte de preu fix, es crea una línia del llibre diari només per al cost.</span><span class="sxs-lookup"><span data-stu-id="4eed5-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="4eed5-112">La lògica per introduir els preus per defecte resideix a la línia del llibre diari.</span><span class="sxs-lookup"><span data-stu-id="4eed5-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="4eed5-113">Tots els valors de camp d'una entrada de temps es copien a la línia del llibre diari.</span><span class="sxs-lookup"><span data-stu-id="4eed5-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="4eed5-114">Aquests camps són la data de la transacció, la línia de contracte a la qual està assignada el projecte i el resultat de moneda a la llista de preus adequada.</span><span class="sxs-lookup"><span data-stu-id="4eed5-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="4eed5-115">Els camps que afecten els preus per defecte, **com** ara Funció i **Unitat organitzativa** , fan que s'introdueixi per defecte un preu adient a la línia del llibre diari.</span><span class="sxs-lookup"><span data-stu-id="4eed5-115">The fields that affect default prices, such as **Role** and **Org Unit** , cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="4eed5-116">Si afegiu un camp personalitzat a l'entrada de temps i voleu que el valor del camp es propagui a valors reals, creeu el camp a l'entitat Valors reals i utilitzeu assignacions de camps per copiar el camp de l'entrada de temps al valor real.</span><span class="sxs-lookup"><span data-stu-id="4eed5-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="4eed5-117">Enviar una entrada de despesa</span><span class="sxs-lookup"><span data-stu-id="4eed5-117">Submitting an expense entry</span></span>

<span data-ttu-id="4eed5-118">Al PSA, quan s'envia una entrada de despesa per a un projecte assignat a una línia de contracte de temps i materials, es creen dues línies del llibre diari.</span><span class="sxs-lookup"><span data-stu-id="4eed5-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="4eed5-119">Una línia és per al cost i l'altra línia és per a les vendes no facturades.</span><span class="sxs-lookup"><span data-stu-id="4eed5-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="4eed5-120">Quan s'envia una entrada de despesa per a un projecte assignat a una línia de contracte de preu fix, es crea una línia del llibre diari només per al cost.</span><span class="sxs-lookup"><span data-stu-id="4eed5-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="4eed5-121">La lògica per a la introducció dels preus per defecte de les despeses es basa en la categoria de despeses que s'ha seleccionat a la pàgina **Entrada de despeses**.</span><span class="sxs-lookup"><span data-stu-id="4eed5-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="4eed5-122">La data de la transacció, la línia de contracte a la qual està assignada el projecte i la moneda s'utilitzen per determinar la llista de preus adequada.</span><span class="sxs-lookup"><span data-stu-id="4eed5-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="4eed5-123">No obstant, per al preu en si mateix, l'import que l'usuari ha introduït es defineix directament a les línies del llibre diari de despesa relacionades per al cost i les vendes per defecte.</span><span class="sxs-lookup"><span data-stu-id="4eed5-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="4eed5-124">A la versió actual del PSA, l'entrada basada en categories per a preus per unitat per defecte a les entrades de despesa no està disponible.</span><span class="sxs-lookup"><span data-stu-id="4eed5-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-entry-journals-to-record-costs"></a><span data-ttu-id="4eed5-125">Utilitzar llibres diaris d'entrada per registrar costos de registre</span><span class="sxs-lookup"><span data-stu-id="4eed5-125">Using Entry journals to record costs</span></span>

<span data-ttu-id="4eed5-126">Al PSA, els llibres diaris d'entrada permeten registrar els costos o ingressos en classes de material, quota, temps, despeses o transaccions tributàries.</span><span class="sxs-lookup"><span data-stu-id="4eed5-126">In PSA, Entry journals let you record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="4eed5-127">Un llibre diari té una capçalera, línies i una acció **Confirmació**.</span><span class="sxs-lookup"><span data-stu-id="4eed5-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="4eed5-128">Aquests són alguns escenaris en què podeu utilitzar un llibre diari:</span><span class="sxs-lookup"><span data-stu-id="4eed5-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="4eed5-129">Heu de registrar els costos reals materials i les vendes d'un projecte.</span><span class="sxs-lookup"><span data-stu-id="4eed5-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="4eed5-130">Heu d'avançar els valors reals de la transacció des d'un altre sistema al PSA.</span><span class="sxs-lookup"><span data-stu-id="4eed5-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="4eed5-131">Heu de registrar les despeses que s'han produït en un altre sistema, com ara les despeses d'adquisició o subcontractacions.</span><span class="sxs-lookup"><span data-stu-id="4eed5-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4eed5-132">L'ús de diaris d'entrada per a la creació de valors reals només l'ha de fer un usuari plenament conscient de l'impacte comptable que tenen els valors reals al projecte.</span><span class="sxs-lookup"><span data-stu-id="4eed5-132">Using Entry journals to create actuals should be done only by a user who is fully aware of the accounting impact the Actuals have on the project.</span></span> <span data-ttu-id="4eed5-133">El motiu és que l'aplicació no valida el tipus de línia del llibre diari ni el preu relacionat que s'introdueix a la línia del llibre diari.</span><span class="sxs-lookup"><span data-stu-id="4eed5-133">This is because the application does not validate the journal line type, or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="4eed5-134">A causa de l'impacte d'aquest tipus de llibre diari, actueu amb extremada cura en relació amb qui té accés a la creació de llibres diaris d'entrada.</span><span class="sxs-lookup"><span data-stu-id="4eed5-134">Because of the impact of this journal type, exercise adequate caution in who is given access to create Entry journals.</span></span>     


## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="4eed5-135">Enregistrament de valors reals a partir d'esdeveniments de projecte</span><span class="sxs-lookup"><span data-stu-id="4eed5-135">Recording actuals based on project events</span></span>

<span data-ttu-id="4eed5-136">El PSA registra totes les transaccions financeres que es produeixen durant un projecte.</span><span class="sxs-lookup"><span data-stu-id="4eed5-136">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="4eed5-137">Aquestes transaccions es registren com a **valors reals**.</span><span class="sxs-lookup"><span data-stu-id="4eed5-137">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="4eed5-138">Les taules següents mostren els diferents tipus de valors reals que s'han creat, en funció de si el projecte és un projecte de temps i materials o de preu fix, si es troba a la fase de prevenda o si és un projecte intern.</span><span class="sxs-lookup"><span data-stu-id="4eed5-138">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="4eed5-139">**El recurs pertany a la mateixa unitat organitzativa que la unitat de contractació del projecte**</span><span class="sxs-lookup"><span data-stu-id="4eed5-139">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="4eed5-140">Incidència</span><span class="sxs-lookup"><span data-stu-id="4eed5-140">Event</span></span></th>
<th colspan="4"><span data-ttu-id="4eed5-141">Projecte facturable o venut</span><span class="sxs-lookup"><span data-stu-id="4eed5-141">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="4eed5-142">Projecte a la fase de prevenda</span><span class="sxs-lookup"><span data-stu-id="4eed5-142">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="4eed5-143">Projecte intern</span><span class="sxs-lookup"><span data-stu-id="4eed5-143">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="4eed5-144">Temps i materials</span><span class="sxs-lookup"><span data-stu-id="4eed5-144">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="4eed5-145">Preu fix</span><span class="sxs-lookup"><span data-stu-id="4eed5-145">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="4eed5-146">Valors reals</span><span class="sxs-lookup"><span data-stu-id="4eed5-146">Actuals</span></span></th>
<th><span data-ttu-id="4eed5-147">Moneda de transacció</span><span class="sxs-lookup"><span data-stu-id="4eed5-147">Transaction currency</span></span></th>
<th><span data-ttu-id="4eed5-148">Preu fix</span><span class="sxs-lookup"><span data-stu-id="4eed5-148">Fixed price</span></span></th>
<th><span data-ttu-id="4eed5-149">Moneda de transacció</span><span class="sxs-lookup"><span data-stu-id="4eed5-149">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4eed5-150">Es crea una entrada de temps.</span><span class="sxs-lookup"><span data-stu-id="4eed5-150">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="4eed5-151">No hi ha activitat a l'entitat Valors reals</span><span class="sxs-lookup"><span data-stu-id="4eed5-151">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4eed5-152">S'envia una entrada de temps.</span><span class="sxs-lookup"><span data-stu-id="4eed5-152">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="4eed5-153">No hi ha activitat a l'entitat Valors reals</span><span class="sxs-lookup"><span data-stu-id="4eed5-153">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="4eed5-154">El temps s'aprova, i no es produeix cap canvi o augment de les hores facturables durant l'aprovació.</span><span class="sxs-lookup"><span data-stu-id="4eed5-154">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="4eed5-155">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="4eed5-155">Cost actual</span></span></td>
<td><span data-ttu-id="4eed5-156">Moneda de la unitat de contractació</span><span class="sxs-lookup"><span data-stu-id="4eed5-156">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="4eed5-157">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="4eed5-157">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="4eed5-158">Moneda de la unitat de contractació</span><span class="sxs-lookup"><span data-stu-id="4eed5-158">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="4eed5-159">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="4eed5-159">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="4eed5-160">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="4eed5-160">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4eed5-161">Valor real de les vendes no facturades - Imputable</span><span class="sxs-lookup"><span data-stu-id="4eed5-161">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="4eed5-162">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="4eed5-162">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="4eed5-163">El temps s'aprova, i es produeix una reducció de les hores facturables durant l'aprovació.</span><span class="sxs-lookup"><span data-stu-id="4eed5-163">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="4eed5-164">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="4eed5-164">Cost actual</span></span></td>
<td><span data-ttu-id="4eed5-165">Moneda de la unitat de contractació</span><span class="sxs-lookup"><span data-stu-id="4eed5-165">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="4eed5-166">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="4eed5-166">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="4eed5-167">Moneda de la unitat de contractació</span><span class="sxs-lookup"><span data-stu-id="4eed5-167">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="4eed5-168">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="4eed5-168">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="4eed5-169">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="4eed5-169">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4eed5-170">Valor real de les vendes no facturades - Imputable per a la nova quantitat</span><span class="sxs-lookup"><span data-stu-id="4eed5-170">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="4eed5-171">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="4eed5-171">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4eed5-172">Valor real de les vendes no facturades - No imputable per la diferència</span><span class="sxs-lookup"><span data-stu-id="4eed5-172">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="4eed5-173">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="4eed5-173">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="4eed5-174">Es confirma una factura, i no es produeix cap canvi o augment de les hores facturables.</span><span class="sxs-lookup"><span data-stu-id="4eed5-174">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="4eed5-175">Reversió de vendes no facturades</span><span class="sxs-lookup"><span data-stu-id="4eed5-175">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="4eed5-176">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="4eed5-176">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="4eed5-177">Vendes facturades per fita</span><span class="sxs-lookup"><span data-stu-id="4eed5-177">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="4eed5-178">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="4eed5-178">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="4eed5-179">No aplicable</span><span class="sxs-lookup"><span data-stu-id="4eed5-179">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="4eed5-180">No aplicable</span><span class="sxs-lookup"><span data-stu-id="4eed5-180">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4eed5-181">Vendes facturades</span><span class="sxs-lookup"><span data-stu-id="4eed5-181">Billed sales</span></span></td>
<td><span data-ttu-id="4eed5-182">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="4eed5-182">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="4eed5-183">Es confirma una factura, i es produeix una disminució de les hores facturables.</span><span class="sxs-lookup"><span data-stu-id="4eed5-183">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="4eed5-184">Reversió de vendes no facturades</span><span class="sxs-lookup"><span data-stu-id="4eed5-184">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="4eed5-185">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="4eed5-185">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="4eed5-186">No aplicable</span><span class="sxs-lookup"><span data-stu-id="4eed5-186">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="4eed5-187">No aplicable</span><span class="sxs-lookup"><span data-stu-id="4eed5-187">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="4eed5-188">No aplicable</span><span class="sxs-lookup"><span data-stu-id="4eed5-188">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="4eed5-189">No aplicable</span><span class="sxs-lookup"><span data-stu-id="4eed5-189">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4eed5-190">Vendes facturades - Imputable per a la nova quantitat</span><span class="sxs-lookup"><span data-stu-id="4eed5-190">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="4eed5-191">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="4eed5-191">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4eed5-192">Vendes facturades - No imputable per la diferència</span><span class="sxs-lookup"><span data-stu-id="4eed5-192">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="4eed5-193">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="4eed5-193">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="4eed5-194">Una factura es corregeix per augmentar la quantitat imputable.</span><span class="sxs-lookup"><span data-stu-id="4eed5-194">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="4eed5-195">Vendes facturades - Reversió</span><span class="sxs-lookup"><span data-stu-id="4eed5-195">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="4eed5-196">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="4eed5-196">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="4eed5-197">Reversió de vendes facturades per fita</span><span class="sxs-lookup"><span data-stu-id="4eed5-197">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="4eed5-198">Canvi en l'estat de la fita de <strong>Facturada</strong> a <strong>Llesta per facturar</strong></span><span class="sxs-lookup"><span data-stu-id="4eed5-198">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="4eed5-199">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="4eed5-199">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="4eed5-200">No aplicable</span><span class="sxs-lookup"><span data-stu-id="4eed5-200">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="4eed5-201">No aplicable</span><span class="sxs-lookup"><span data-stu-id="4eed5-201">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4eed5-202">Vendes facturades</span><span class="sxs-lookup"><span data-stu-id="4eed5-202">Billed sales</span></span></td>
<td><span data-ttu-id="4eed5-203">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="4eed5-203">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="4eed5-204">Una factura es corregeix per reduir la quantitat imputable.</span><span class="sxs-lookup"><span data-stu-id="4eed5-204">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="4eed5-205">Vendes facturades - Reversió</span><span class="sxs-lookup"><span data-stu-id="4eed5-205">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="4eed5-206">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="4eed5-206">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4eed5-207">Vendes facturades per a la nova quantitat</span><span class="sxs-lookup"><span data-stu-id="4eed5-207">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="4eed5-208">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="4eed5-208">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4eed5-209">Vendes no facturades - Imputable per la diferència</span><span class="sxs-lookup"><span data-stu-id="4eed5-209">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="4eed5-210">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="4eed5-210">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4eed5-211">**El recurs pertany a una unitat organitzativa diferent de la unitat de contractació del projecte**</span><span class="sxs-lookup"><span data-stu-id="4eed5-211">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="4eed5-212">Incidència</span><span class="sxs-lookup"><span data-stu-id="4eed5-212">Event</span></span></th>
<th colspan="4"><span data-ttu-id="4eed5-213">Projecte facturable o venut</span><span class="sxs-lookup"><span data-stu-id="4eed5-213">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="4eed5-214">Projecte a la fase de prevenda</span><span class="sxs-lookup"><span data-stu-id="4eed5-214">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="4eed5-215">Projecte intern</span><span class="sxs-lookup"><span data-stu-id="4eed5-215">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="4eed5-216">Temps i materials</span><span class="sxs-lookup"><span data-stu-id="4eed5-216">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="4eed5-217">Preu fix</span><span class="sxs-lookup"><span data-stu-id="4eed5-217">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="4eed5-218">Valors reals</span><span class="sxs-lookup"><span data-stu-id="4eed5-218">Actuals</span></span></th>
<th><span data-ttu-id="4eed5-219">Moneda de transacció</span><span class="sxs-lookup"><span data-stu-id="4eed5-219">Transaction currency</span></span></th>
<th><span data-ttu-id="4eed5-220">Preu fix</span><span class="sxs-lookup"><span data-stu-id="4eed5-220">Fixed price</span></span></th>
<th><span data-ttu-id="4eed5-221">Moneda de transacció</span><span class="sxs-lookup"><span data-stu-id="4eed5-221">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4eed5-222">Es crea una entrada de temps.</span><span class="sxs-lookup"><span data-stu-id="4eed5-222">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="4eed5-223">No hi ha activitat a l'entitat Valors reals</span><span class="sxs-lookup"><span data-stu-id="4eed5-223">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4eed5-224">S'envia una entrada de temps.</span><span class="sxs-lookup"><span data-stu-id="4eed5-224">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="4eed5-225">No hi ha activitat a l'entitat Valors reals</span><span class="sxs-lookup"><span data-stu-id="4eed5-225">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="4eed5-226">El temps s'aprova, i no es produeix cap canvi o augment de les hores facturables durant l'aprovació.</span><span class="sxs-lookup"><span data-stu-id="4eed5-226">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="4eed5-227">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="4eed5-227">Cost actual</span></span></td>
<td><span data-ttu-id="4eed5-228">Moneda de la unitat de contractació</span><span class="sxs-lookup"><span data-stu-id="4eed5-228">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="4eed5-229">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="4eed5-229">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="4eed5-230">Moneda de la unitat de contractació</span><span class="sxs-lookup"><span data-stu-id="4eed5-230">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="4eed5-231">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="4eed5-231">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="4eed5-232">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="4eed5-232">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4eed5-233">Valor real de les vendes no facturades - Imputable</span><span class="sxs-lookup"><span data-stu-id="4eed5-233">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="4eed5-234">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="4eed5-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4eed5-235">Cost de la unitat de recursos</span><span class="sxs-lookup"><span data-stu-id="4eed5-235">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="4eed5-236">Moneda de la unitat de recursos</span><span class="sxs-lookup"><span data-stu-id="4eed5-236">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4eed5-237">Vendes interorganitzatives</span><span class="sxs-lookup"><span data-stu-id="4eed5-237">Interorganizational sales</span></span></td>
<td><span data-ttu-id="4eed5-238">Moneda de la unitat de contractació</span><span class="sxs-lookup"><span data-stu-id="4eed5-238">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="4eed5-239">El temps s'aprova, i es produeix una reducció de les hores facturables durant l'aprovació.</span><span class="sxs-lookup"><span data-stu-id="4eed5-239">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="4eed5-240">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="4eed5-240">Cost actual</span></span></td>
<td><span data-ttu-id="4eed5-241">Moneda de la unitat de contractació</span><span class="sxs-lookup"><span data-stu-id="4eed5-241">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="4eed5-242">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="4eed5-242">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="4eed5-243">Moneda de la unitat de contractació</span><span class="sxs-lookup"><span data-stu-id="4eed5-243">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="4eed5-244">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="4eed5-244">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="4eed5-245">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="4eed5-245">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4eed5-246">Cost de la unitat de recursos</span><span class="sxs-lookup"><span data-stu-id="4eed5-246">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="4eed5-247">Moneda de la unitat de recursos</span><span class="sxs-lookup"><span data-stu-id="4eed5-247">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4eed5-248">Vendes interorganitzatives</span><span class="sxs-lookup"><span data-stu-id="4eed5-248">Interorganizational sales</span></span></td>
<td><span data-ttu-id="4eed5-249">Moneda de la unitat de contractació</span><span class="sxs-lookup"><span data-stu-id="4eed5-249">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4eed5-250">Valor real de les vendes no facturades - Imputable per a la nova quantitat</span><span class="sxs-lookup"><span data-stu-id="4eed5-250">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="4eed5-251">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="4eed5-251">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4eed5-252">Valor real de les vendes no facturades - No imputable per la diferència</span><span class="sxs-lookup"><span data-stu-id="4eed5-252">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="4eed5-253">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="4eed5-253">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="4eed5-254">Es confirma una factura, i no es produeix cap canvi o augment de les hores facturables.</span><span class="sxs-lookup"><span data-stu-id="4eed5-254">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="4eed5-255">Reversió de vendes no facturades</span><span class="sxs-lookup"><span data-stu-id="4eed5-255">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="4eed5-256">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="4eed5-256">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="4eed5-257">Vendes facturades per fita</span><span class="sxs-lookup"><span data-stu-id="4eed5-257">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="4eed5-258">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="4eed5-258">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="4eed5-259">No aplicable</span><span class="sxs-lookup"><span data-stu-id="4eed5-259">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="4eed5-260">No aplicable</span><span class="sxs-lookup"><span data-stu-id="4eed5-260">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4eed5-261">Vendes facturades</span><span class="sxs-lookup"><span data-stu-id="4eed5-261">Billed sales</span></span></td>
<td><span data-ttu-id="4eed5-262">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="4eed5-262">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="4eed5-263">Es confirma una factura, i es produeix una disminució de les hores facturables.</span><span class="sxs-lookup"><span data-stu-id="4eed5-263">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="4eed5-264">Reversió de vendes no facturades</span><span class="sxs-lookup"><span data-stu-id="4eed5-264">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="4eed5-265">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="4eed5-265">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="4eed5-266">No aplicable</span><span class="sxs-lookup"><span data-stu-id="4eed5-266">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="4eed5-267">No aplicable</span><span class="sxs-lookup"><span data-stu-id="4eed5-267">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="4eed5-268">No aplicable</span><span class="sxs-lookup"><span data-stu-id="4eed5-268">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="4eed5-269">No aplicable</span><span class="sxs-lookup"><span data-stu-id="4eed5-269">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4eed5-270">Vendes facturades - Imputable per a la nova quantitat</span><span class="sxs-lookup"><span data-stu-id="4eed5-270">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="4eed5-271">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="4eed5-271">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4eed5-272">Vendes facturades - No imputable per la diferència</span><span class="sxs-lookup"><span data-stu-id="4eed5-272">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="4eed5-273">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="4eed5-273">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="4eed5-274">Una factura es corregeix per augmentar la quantitat imputable.</span><span class="sxs-lookup"><span data-stu-id="4eed5-274">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="4eed5-275">Vendes facturades - Reversió</span><span class="sxs-lookup"><span data-stu-id="4eed5-275">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="4eed5-276">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="4eed5-276">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="4eed5-277">Reversió de vendes facturades per fita</span><span class="sxs-lookup"><span data-stu-id="4eed5-277">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="4eed5-278">Canvi en l'estat de la fita de <strong>Facturada</strong> a <strong>Llesta per facturar</strong></span><span class="sxs-lookup"><span data-stu-id="4eed5-278">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="4eed5-279">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="4eed5-279">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="4eed5-280">No aplicable</span><span class="sxs-lookup"><span data-stu-id="4eed5-280">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="4eed5-281">No aplicable</span><span class="sxs-lookup"><span data-stu-id="4eed5-281">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4eed5-282">Vendes facturades</span><span class="sxs-lookup"><span data-stu-id="4eed5-282">Billed sales</span></span></td>
<td><span data-ttu-id="4eed5-283">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="4eed5-283">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="4eed5-284">Una factura es corregeix per reduir la quantitat imputable.</span><span class="sxs-lookup"><span data-stu-id="4eed5-284">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="4eed5-285">Vendes facturades - Reversió</span><span class="sxs-lookup"><span data-stu-id="4eed5-285">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="4eed5-286">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="4eed5-286">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4eed5-287">Vendes facturades per a la nova quantitat</span><span class="sxs-lookup"><span data-stu-id="4eed5-287">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="4eed5-288">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="4eed5-288">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4eed5-289">Vendes no facturades - Imputable per la diferència</span><span class="sxs-lookup"><span data-stu-id="4eed5-289">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="4eed5-290">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="4eed5-290">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
