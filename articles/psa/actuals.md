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
ms.openlocfilehash: c4a3424bed704243dfb5524fa541c3fcc0899e57
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5285606"
---
# <a name="actuals-overview"></a><span data-ttu-id="5f8b4-103">Informació general dels valors reals</span><span class="sxs-lookup"><span data-stu-id="5f8b4-103">Actuals overview</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="5f8b4-104">Els valors reals són la quantitat de treball que s'ha completat en un projecte.</span><span class="sxs-lookup"><span data-stu-id="5f8b4-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="5f8b4-105">Els valors reals del projecte es remunten als seus documents d'origen.</span><span class="sxs-lookup"><span data-stu-id="5f8b4-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="5f8b4-106">Aquests documents d'origen inclouen entrades de temps, despeses i del llibre diari, i també factures.</span><span class="sxs-lookup"><span data-stu-id="5f8b4-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![Com es remunten els valors reals als documents d'origen](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="5f8b4-108">Enviant una entrada de temps</span><span class="sxs-lookup"><span data-stu-id="5f8b4-108">Submitting a time entry</span></span>

<span data-ttu-id="5f8b4-109">Al PSA, quan s'envia una entrada de temps per a un projecte assignat a una línia de contracte de temps i materials, es creen dues línies del llibre diari.</span><span class="sxs-lookup"><span data-stu-id="5f8b4-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="5f8b4-110">Una línia és per al cost i l'altra línia és per a les vendes no facturades.</span><span class="sxs-lookup"><span data-stu-id="5f8b4-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="5f8b4-111">Quan s'envia una entrada de temps per a un projecte assignat a una línia de contracte de preu fix, es crea una línia del llibre diari només per al cost.</span><span class="sxs-lookup"><span data-stu-id="5f8b4-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="5f8b4-112">La lògica per introduir els preus per defecte resideix a la línia del llibre diari.</span><span class="sxs-lookup"><span data-stu-id="5f8b4-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="5f8b4-113">Tots els valors de camp d'una entrada de temps es copien a la línia del llibre diari.</span><span class="sxs-lookup"><span data-stu-id="5f8b4-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="5f8b4-114">Aquests camps són la data de la transacció, la línia de contracte a la qual està assignada el projecte i el resultat de moneda a la llista de preus adequada.</span><span class="sxs-lookup"><span data-stu-id="5f8b4-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="5f8b4-115">Els camps que afecten els preus per defecte, **com** ara Funció i **Unitat organitzativa**, fan que s'introdueixi per defecte un preu adient a la línia del llibre diari.</span><span class="sxs-lookup"><span data-stu-id="5f8b4-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="5f8b4-116">Si afegiu un camp personalitzat a l'entrada de temps i voleu que el valor del camp es propagui a valors reals, creeu el camp a l'entitat Valors reals i utilitzeu assignacions de camps per copiar el camp de l'entrada de temps al valor real.</span><span class="sxs-lookup"><span data-stu-id="5f8b4-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="5f8b4-117">Enviar una entrada de despesa</span><span class="sxs-lookup"><span data-stu-id="5f8b4-117">Submitting an expense entry</span></span>

<span data-ttu-id="5f8b4-118">Al PSA, quan s'envia una entrada de despesa per a un projecte assignat a una línia de contracte de temps i materials, es creen dues línies del llibre diari.</span><span class="sxs-lookup"><span data-stu-id="5f8b4-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="5f8b4-119">Una línia és per al cost i l'altra línia és per a les vendes no facturades.</span><span class="sxs-lookup"><span data-stu-id="5f8b4-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="5f8b4-120">Quan s'envia una entrada de despesa per a un projecte assignat a una línia de contracte de preu fix, es crea una línia del llibre diari només per al cost.</span><span class="sxs-lookup"><span data-stu-id="5f8b4-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="5f8b4-121">La lògica per a la introducció dels preus per defecte de les despeses es basa en la categoria de despeses que s'ha seleccionat a la pàgina **Entrada de despeses**.</span><span class="sxs-lookup"><span data-stu-id="5f8b4-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="5f8b4-122">La data de la transacció, la línia de contracte a la qual està assignada el projecte i la moneda s'utilitzen per determinar la llista de preus adequada.</span><span class="sxs-lookup"><span data-stu-id="5f8b4-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="5f8b4-123">No obstant, per al preu en si mateix, l'import que l'usuari ha introduït es defineix directament a les línies del llibre diari de despesa relacionades per al cost i les vendes per defecte.</span><span class="sxs-lookup"><span data-stu-id="5f8b4-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="5f8b4-124">A la versió actual del PSA, l'entrada basada en categories per a preus per unitat per defecte a les entrades de despesa no està disponible.</span><span class="sxs-lookup"><span data-stu-id="5f8b4-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-entry-journals-to-record-costs"></a><span data-ttu-id="5f8b4-125">Utilitzar llibres diaris d'entrada per registrar costos de registre</span><span class="sxs-lookup"><span data-stu-id="5f8b4-125">Using Entry journals to record costs</span></span>

<span data-ttu-id="5f8b4-126">Al PSA, els llibres diaris d'entrada permeten registrar els costos o ingressos en classes de material, quota, temps, despeses o transaccions tributàries.</span><span class="sxs-lookup"><span data-stu-id="5f8b4-126">In PSA, Entry journals let you record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="5f8b4-127">Un llibre diari té una capçalera, línies i una acció **Confirmació**.</span><span class="sxs-lookup"><span data-stu-id="5f8b4-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="5f8b4-128">Aquests són alguns escenaris en què podeu utilitzar un llibre diari:</span><span class="sxs-lookup"><span data-stu-id="5f8b4-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="5f8b4-129">Heu de registrar els costos reals materials i les vendes d'un projecte.</span><span class="sxs-lookup"><span data-stu-id="5f8b4-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="5f8b4-130">Heu d'avançar els valors reals de la transacció des d'un altre sistema al PSA.</span><span class="sxs-lookup"><span data-stu-id="5f8b4-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="5f8b4-131">Heu de registrar les despeses que s'han produït en un altre sistema, com ara les despeses d'adquisició o subcontractacions.</span><span class="sxs-lookup"><span data-stu-id="5f8b4-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5f8b4-132">L'ús de diaris d'entrada per a la creació de valors reals només l'ha de fer un usuari plenament conscient de l'impacte comptable que tenen els valors reals al projecte.</span><span class="sxs-lookup"><span data-stu-id="5f8b4-132">Using Entry journals to create actuals should be done only by a user who is fully aware of the accounting impact the Actuals have on the project.</span></span> <span data-ttu-id="5f8b4-133">El motiu és que l'aplicació no valida el tipus de línia del llibre diari ni el preu relacionat que s'introdueix a la línia del llibre diari.</span><span class="sxs-lookup"><span data-stu-id="5f8b4-133">This is because the application does not validate the journal line type, or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="5f8b4-134">A causa de l'impacte d'aquest tipus de llibre diari, actueu amb extremada cura en relació amb qui té accés a la creació de llibres diaris d'entrada.</span><span class="sxs-lookup"><span data-stu-id="5f8b4-134">Because of the impact of this journal type, exercise adequate caution in who is given access to create Entry journals.</span></span>     


## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="5f8b4-135">Enregistrament de valors reals a partir d'esdeveniments de projecte</span><span class="sxs-lookup"><span data-stu-id="5f8b4-135">Recording actuals based on project events</span></span>

<span data-ttu-id="5f8b4-136">El PSA registra totes les transaccions financeres que es produeixen durant un projecte.</span><span class="sxs-lookup"><span data-stu-id="5f8b4-136">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="5f8b4-137">Aquestes transaccions es registren com a **valors reals**.</span><span class="sxs-lookup"><span data-stu-id="5f8b4-137">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="5f8b4-138">Les taules següents mostren els diferents tipus de valors reals que s'han creat, en funció de si el projecte és un projecte de temps i materials o de preu fix, si es troba a la fase de prevenda o si és un projecte intern.</span><span class="sxs-lookup"><span data-stu-id="5f8b4-138">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="5f8b4-139">**El recurs pertany a la mateixa unitat organitzativa que la unitat de contractació del projecte**</span><span class="sxs-lookup"><span data-stu-id="5f8b4-139">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="5f8b4-140">Incidència</span><span class="sxs-lookup"><span data-stu-id="5f8b4-140">Event</span></span></th>
<th colspan="4"><span data-ttu-id="5f8b4-141">Projecte facturable o venut</span><span class="sxs-lookup"><span data-stu-id="5f8b4-141">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="5f8b4-142">Projecte a la fase de prevenda</span><span class="sxs-lookup"><span data-stu-id="5f8b4-142">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="5f8b4-143">Projecte intern</span><span class="sxs-lookup"><span data-stu-id="5f8b4-143">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="5f8b4-144">Temps i materials</span><span class="sxs-lookup"><span data-stu-id="5f8b4-144">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="5f8b4-145">Preu fix</span><span class="sxs-lookup"><span data-stu-id="5f8b4-145">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="5f8b4-146">Valors reals</span><span class="sxs-lookup"><span data-stu-id="5f8b4-146">Actuals</span></span></th>
<th><span data-ttu-id="5f8b4-147">Moneda de transacció</span><span class="sxs-lookup"><span data-stu-id="5f8b4-147">Transaction currency</span></span></th>
<th><span data-ttu-id="5f8b4-148">Preu fix</span><span class="sxs-lookup"><span data-stu-id="5f8b4-148">Fixed price</span></span></th>
<th><span data-ttu-id="5f8b4-149">Moneda de transacció</span><span class="sxs-lookup"><span data-stu-id="5f8b4-149">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5f8b4-150">Es crea una entrada de temps.</span><span class="sxs-lookup"><span data-stu-id="5f8b4-150">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="5f8b4-151">No hi ha activitat a l'entitat Valors reals</span><span class="sxs-lookup"><span data-stu-id="5f8b4-151">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f8b4-152">S'envia una entrada de temps.</span><span class="sxs-lookup"><span data-stu-id="5f8b4-152">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="5f8b4-153">No hi ha activitat a l'entitat Valors reals</span><span class="sxs-lookup"><span data-stu-id="5f8b4-153">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="5f8b4-154">El temps s'aprova, i no es produeix cap canvi o augment de les hores facturables durant l'aprovació.</span><span class="sxs-lookup"><span data-stu-id="5f8b4-154">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="5f8b4-155">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="5f8b4-155">Cost actual</span></span></td>
<td><span data-ttu-id="5f8b4-156">Moneda de la unitat de contractació</span><span class="sxs-lookup"><span data-stu-id="5f8b4-156">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="5f8b4-157">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="5f8b4-157">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="5f8b4-158">Moneda de la unitat de contractació</span><span class="sxs-lookup"><span data-stu-id="5f8b4-158">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="5f8b4-159">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="5f8b4-159">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="5f8b4-160">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="5f8b4-160">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f8b4-161">Valor real de les vendes no facturades - Imputable</span><span class="sxs-lookup"><span data-stu-id="5f8b4-161">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="5f8b4-162">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="5f8b4-162">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="5f8b4-163">El temps s'aprova, i es produeix una reducció de les hores facturables durant l'aprovació.</span><span class="sxs-lookup"><span data-stu-id="5f8b4-163">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="5f8b4-164">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="5f8b4-164">Cost actual</span></span></td>
<td><span data-ttu-id="5f8b4-165">Moneda de la unitat de contractació</span><span class="sxs-lookup"><span data-stu-id="5f8b4-165">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="5f8b4-166">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="5f8b4-166">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="5f8b4-167">Moneda de la unitat de contractació</span><span class="sxs-lookup"><span data-stu-id="5f8b4-167">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="5f8b4-168">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="5f8b4-168">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="5f8b4-169">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="5f8b4-169">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f8b4-170">Valor real de les vendes no facturades - Imputable per a la nova quantitat</span><span class="sxs-lookup"><span data-stu-id="5f8b4-170">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="5f8b4-171">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="5f8b4-171">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f8b4-172">Valor real de les vendes no facturades - No imputable per la diferència</span><span class="sxs-lookup"><span data-stu-id="5f8b4-172">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="5f8b4-173">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="5f8b4-173">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="5f8b4-174">Es confirma una factura, i no es produeix cap canvi o augment de les hores facturables.</span><span class="sxs-lookup"><span data-stu-id="5f8b4-174">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="5f8b4-175">Reversió de vendes no facturades</span><span class="sxs-lookup"><span data-stu-id="5f8b4-175">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="5f8b4-176">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="5f8b4-176">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="5f8b4-177">Vendes facturades per fita</span><span class="sxs-lookup"><span data-stu-id="5f8b4-177">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="5f8b4-178">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="5f8b4-178">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="5f8b4-179">No aplicable</span><span class="sxs-lookup"><span data-stu-id="5f8b4-179">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="5f8b4-180">No aplicable</span><span class="sxs-lookup"><span data-stu-id="5f8b4-180">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f8b4-181">Vendes facturades</span><span class="sxs-lookup"><span data-stu-id="5f8b4-181">Billed sales</span></span></td>
<td><span data-ttu-id="5f8b4-182">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="5f8b4-182">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="5f8b4-183">Es confirma una factura, i es produeix una disminució de les hores facturables.</span><span class="sxs-lookup"><span data-stu-id="5f8b4-183">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="5f8b4-184">Reversió de vendes no facturades</span><span class="sxs-lookup"><span data-stu-id="5f8b4-184">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="5f8b4-185">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="5f8b4-185">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="5f8b4-186">No aplicable</span><span class="sxs-lookup"><span data-stu-id="5f8b4-186">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="5f8b4-187">No aplicable</span><span class="sxs-lookup"><span data-stu-id="5f8b4-187">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="5f8b4-188">No aplicable</span><span class="sxs-lookup"><span data-stu-id="5f8b4-188">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="5f8b4-189">No aplicable</span><span class="sxs-lookup"><span data-stu-id="5f8b4-189">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f8b4-190">Vendes facturades - Imputable per a la nova quantitat</span><span class="sxs-lookup"><span data-stu-id="5f8b4-190">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="5f8b4-191">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="5f8b4-191">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f8b4-192">Vendes facturades - No imputable per la diferència</span><span class="sxs-lookup"><span data-stu-id="5f8b4-192">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="5f8b4-193">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="5f8b4-193">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="5f8b4-194">Una factura es corregeix per augmentar la quantitat imputable.</span><span class="sxs-lookup"><span data-stu-id="5f8b4-194">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="5f8b4-195">Vendes facturades - Reversió</span><span class="sxs-lookup"><span data-stu-id="5f8b4-195">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="5f8b4-196">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="5f8b4-196">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="5f8b4-197">Reversió de vendes facturades per fita</span><span class="sxs-lookup"><span data-stu-id="5f8b4-197">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="5f8b4-198">Canvi en l'estat de la fita de <strong>Facturada</strong> a <strong>Llesta per facturar</strong></span><span class="sxs-lookup"><span data-stu-id="5f8b4-198">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="5f8b4-199">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="5f8b4-199">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="5f8b4-200">No aplicable</span><span class="sxs-lookup"><span data-stu-id="5f8b4-200">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="5f8b4-201">No aplicable</span><span class="sxs-lookup"><span data-stu-id="5f8b4-201">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f8b4-202">Vendes facturades</span><span class="sxs-lookup"><span data-stu-id="5f8b4-202">Billed sales</span></span></td>
<td><span data-ttu-id="5f8b4-203">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="5f8b4-203">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="5f8b4-204">Una factura es corregeix per reduir la quantitat imputable.</span><span class="sxs-lookup"><span data-stu-id="5f8b4-204">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="5f8b4-205">Vendes facturades - Reversió</span><span class="sxs-lookup"><span data-stu-id="5f8b4-205">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="5f8b4-206">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="5f8b4-206">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f8b4-207">Vendes facturades per a la nova quantitat</span><span class="sxs-lookup"><span data-stu-id="5f8b4-207">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="5f8b4-208">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="5f8b4-208">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f8b4-209">Vendes no facturades - Imputable per la diferència</span><span class="sxs-lookup"><span data-stu-id="5f8b4-209">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="5f8b4-210">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="5f8b4-210">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5f8b4-211">**El recurs pertany a una unitat organitzativa diferent de la unitat de contractació del projecte**</span><span class="sxs-lookup"><span data-stu-id="5f8b4-211">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="5f8b4-212">Incidència</span><span class="sxs-lookup"><span data-stu-id="5f8b4-212">Event</span></span></th>
<th colspan="4"><span data-ttu-id="5f8b4-213">Projecte facturable o venut</span><span class="sxs-lookup"><span data-stu-id="5f8b4-213">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="5f8b4-214">Projecte a la fase de prevenda</span><span class="sxs-lookup"><span data-stu-id="5f8b4-214">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="5f8b4-215">Projecte intern</span><span class="sxs-lookup"><span data-stu-id="5f8b4-215">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="5f8b4-216">Temps i materials</span><span class="sxs-lookup"><span data-stu-id="5f8b4-216">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="5f8b4-217">Preu fix</span><span class="sxs-lookup"><span data-stu-id="5f8b4-217">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="5f8b4-218">Valors reals</span><span class="sxs-lookup"><span data-stu-id="5f8b4-218">Actuals</span></span></th>
<th><span data-ttu-id="5f8b4-219">Moneda de transacció</span><span class="sxs-lookup"><span data-stu-id="5f8b4-219">Transaction currency</span></span></th>
<th><span data-ttu-id="5f8b4-220">Preu fix</span><span class="sxs-lookup"><span data-stu-id="5f8b4-220">Fixed price</span></span></th>
<th><span data-ttu-id="5f8b4-221">Moneda de transacció</span><span class="sxs-lookup"><span data-stu-id="5f8b4-221">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5f8b4-222">Es crea una entrada de temps.</span><span class="sxs-lookup"><span data-stu-id="5f8b4-222">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="5f8b4-223">No hi ha activitat a l'entitat Valors reals</span><span class="sxs-lookup"><span data-stu-id="5f8b4-223">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f8b4-224">S'envia una entrada de temps.</span><span class="sxs-lookup"><span data-stu-id="5f8b4-224">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="5f8b4-225">No hi ha activitat a l'entitat Valors reals</span><span class="sxs-lookup"><span data-stu-id="5f8b4-225">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="5f8b4-226">El temps s'aprova, i no es produeix cap canvi o augment de les hores facturables durant l'aprovació.</span><span class="sxs-lookup"><span data-stu-id="5f8b4-226">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="5f8b4-227">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="5f8b4-227">Cost actual</span></span></td>
<td><span data-ttu-id="5f8b4-228">Moneda de la unitat de contractació</span><span class="sxs-lookup"><span data-stu-id="5f8b4-228">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="5f8b4-229">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="5f8b4-229">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="5f8b4-230">Moneda de la unitat de contractació</span><span class="sxs-lookup"><span data-stu-id="5f8b4-230">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="5f8b4-231">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="5f8b4-231">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="5f8b4-232">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="5f8b4-232">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f8b4-233">Valor real de les vendes no facturades - Imputable</span><span class="sxs-lookup"><span data-stu-id="5f8b4-233">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="5f8b4-234">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="5f8b4-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f8b4-235">Cost de la unitat de recursos</span><span class="sxs-lookup"><span data-stu-id="5f8b4-235">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="5f8b4-236">Moneda de la unitat de recursos</span><span class="sxs-lookup"><span data-stu-id="5f8b4-236">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f8b4-237">Vendes interorganitzatives</span><span class="sxs-lookup"><span data-stu-id="5f8b4-237">Interorganizational sales</span></span></td>
<td><span data-ttu-id="5f8b4-238">Moneda de la unitat de contractació</span><span class="sxs-lookup"><span data-stu-id="5f8b4-238">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="5f8b4-239">El temps s'aprova, i es produeix una reducció de les hores facturables durant l'aprovació.</span><span class="sxs-lookup"><span data-stu-id="5f8b4-239">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="5f8b4-240">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="5f8b4-240">Cost actual</span></span></td>
<td><span data-ttu-id="5f8b4-241">Moneda de la unitat de contractació</span><span class="sxs-lookup"><span data-stu-id="5f8b4-241">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="5f8b4-242">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="5f8b4-242">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="5f8b4-243">Moneda de la unitat de contractació</span><span class="sxs-lookup"><span data-stu-id="5f8b4-243">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="5f8b4-244">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="5f8b4-244">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="5f8b4-245">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="5f8b4-245">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f8b4-246">Cost de la unitat de recursos</span><span class="sxs-lookup"><span data-stu-id="5f8b4-246">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="5f8b4-247">Moneda de la unitat de recursos</span><span class="sxs-lookup"><span data-stu-id="5f8b4-247">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f8b4-248">Vendes interorganitzatives</span><span class="sxs-lookup"><span data-stu-id="5f8b4-248">Interorganizational sales</span></span></td>
<td><span data-ttu-id="5f8b4-249">Moneda de la unitat de contractació</span><span class="sxs-lookup"><span data-stu-id="5f8b4-249">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f8b4-250">Valor real de les vendes no facturades - Imputable per a la nova quantitat</span><span class="sxs-lookup"><span data-stu-id="5f8b4-250">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="5f8b4-251">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="5f8b4-251">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f8b4-252">Valor real de les vendes no facturades - No imputable per la diferència</span><span class="sxs-lookup"><span data-stu-id="5f8b4-252">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="5f8b4-253">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="5f8b4-253">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="5f8b4-254">Es confirma una factura, i no es produeix cap canvi o augment de les hores facturables.</span><span class="sxs-lookup"><span data-stu-id="5f8b4-254">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="5f8b4-255">Reversió de vendes no facturades</span><span class="sxs-lookup"><span data-stu-id="5f8b4-255">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="5f8b4-256">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="5f8b4-256">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="5f8b4-257">Vendes facturades per fita</span><span class="sxs-lookup"><span data-stu-id="5f8b4-257">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="5f8b4-258">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="5f8b4-258">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="5f8b4-259">No aplicable</span><span class="sxs-lookup"><span data-stu-id="5f8b4-259">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="5f8b4-260">No aplicable</span><span class="sxs-lookup"><span data-stu-id="5f8b4-260">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f8b4-261">Vendes facturades</span><span class="sxs-lookup"><span data-stu-id="5f8b4-261">Billed sales</span></span></td>
<td><span data-ttu-id="5f8b4-262">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="5f8b4-262">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="5f8b4-263">Es confirma una factura, i es produeix una disminució de les hores facturables.</span><span class="sxs-lookup"><span data-stu-id="5f8b4-263">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="5f8b4-264">Reversió de vendes no facturades</span><span class="sxs-lookup"><span data-stu-id="5f8b4-264">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="5f8b4-265">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="5f8b4-265">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="5f8b4-266">No aplicable</span><span class="sxs-lookup"><span data-stu-id="5f8b4-266">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="5f8b4-267">No aplicable</span><span class="sxs-lookup"><span data-stu-id="5f8b4-267">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="5f8b4-268">No aplicable</span><span class="sxs-lookup"><span data-stu-id="5f8b4-268">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="5f8b4-269">No aplicable</span><span class="sxs-lookup"><span data-stu-id="5f8b4-269">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f8b4-270">Vendes facturades - Imputable per a la nova quantitat</span><span class="sxs-lookup"><span data-stu-id="5f8b4-270">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="5f8b4-271">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="5f8b4-271">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f8b4-272">Vendes facturades - No imputable per la diferència</span><span class="sxs-lookup"><span data-stu-id="5f8b4-272">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="5f8b4-273">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="5f8b4-273">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="5f8b4-274">Una factura es corregeix per augmentar la quantitat imputable.</span><span class="sxs-lookup"><span data-stu-id="5f8b4-274">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="5f8b4-275">Vendes facturades - Reversió</span><span class="sxs-lookup"><span data-stu-id="5f8b4-275">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="5f8b4-276">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="5f8b4-276">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="5f8b4-277">Reversió de vendes facturades per fita</span><span class="sxs-lookup"><span data-stu-id="5f8b4-277">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="5f8b4-278">Canvi en l'estat de la fita de <strong>Facturada</strong> a <strong>Llesta per facturar</strong></span><span class="sxs-lookup"><span data-stu-id="5f8b4-278">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="5f8b4-279">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="5f8b4-279">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="5f8b4-280">No aplicable</span><span class="sxs-lookup"><span data-stu-id="5f8b4-280">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="5f8b4-281">No aplicable</span><span class="sxs-lookup"><span data-stu-id="5f8b4-281">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f8b4-282">Vendes facturades</span><span class="sxs-lookup"><span data-stu-id="5f8b4-282">Billed sales</span></span></td>
<td><span data-ttu-id="5f8b4-283">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="5f8b4-283">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="5f8b4-284">Una factura es corregeix per reduir la quantitat imputable.</span><span class="sxs-lookup"><span data-stu-id="5f8b4-284">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="5f8b4-285">Vendes facturades - Reversió</span><span class="sxs-lookup"><span data-stu-id="5f8b4-285">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="5f8b4-286">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="5f8b4-286">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f8b4-287">Vendes facturades per a la nova quantitat</span><span class="sxs-lookup"><span data-stu-id="5f8b4-287">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="5f8b4-288">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="5f8b4-288">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f8b4-289">Vendes no facturades - Imputable per la diferència</span><span class="sxs-lookup"><span data-stu-id="5f8b4-289">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="5f8b4-290">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="5f8b4-290">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]