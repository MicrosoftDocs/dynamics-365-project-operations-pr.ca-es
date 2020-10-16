---
title: Pàgina inicial de valors reals
description: En aquest tema es proporciona informació sobre com treballar amb valors reals al Microsoft Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 75ad336a995aba3505325466433a5c5e2bb3e776
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/01/2020
ms.locfileid: "3907306"
---
# <a name="actuals"></a><span data-ttu-id="d15c7-103">Valors reals</span><span class="sxs-lookup"><span data-stu-id="d15c7-103">Actuals</span></span>

<span data-ttu-id="d15c7-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_</span><span class="sxs-lookup"><span data-stu-id="d15c7-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="d15c7-105">Els valors reals són la quantitat de treball que s'ha completat en un projecte.</span><span class="sxs-lookup"><span data-stu-id="d15c7-105">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="d15c7-106">Es creen com a resultat d'entrades de temps i de despeses i entrades de diari i factures.</span><span class="sxs-lookup"><span data-stu-id="d15c7-106">They are created as a result of time and expense entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="d15c7-107">Línies del llibre diari i enviament de temps</span><span class="sxs-lookup"><span data-stu-id="d15c7-107">Journal lines and time submission</span></span>

<span data-ttu-id="d15c7-108">Per obtenir més informació sobre l'entrada de temps, vegeu [Descripció general de les entrades de temps](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="d15c7-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="d15c7-109">Temps i materials</span><span class="sxs-lookup"><span data-stu-id="d15c7-109">Time and materials</span></span>

<span data-ttu-id="d15c7-110">Quan un registre de temps que s'envia està enllaçat a un projecte que s'assigna a una línia de contracte de temps i materials, el sistema crea dues línies del llibre diari, una per al cost i l'altra per a les vendes sense facturar.</span><span class="sxs-lookup"><span data-stu-id="d15c7-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="d15c7-111">Preu fix</span><span class="sxs-lookup"><span data-stu-id="d15c7-111">Fixed price</span></span>

<span data-ttu-id="d15c7-112">Quan una entrada de temps que s'envia està enllaçada a un projecte assignat a una línia de contracte de preu fix, el sistema crea una línia del llibre diari per al cost.</span><span class="sxs-lookup"><span data-stu-id="d15c7-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="d15c7-113">Preus per defecte</span><span class="sxs-lookup"><span data-stu-id="d15c7-113">Default pricing</span></span>

<span data-ttu-id="d15c7-114">La lògica per crear els preus per defecte resideix a la línia del llibre diari.</span><span class="sxs-lookup"><span data-stu-id="d15c7-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="d15c7-115">Els valors de camp de l'entrada de temps es copien a la línia del llibre diari.</span><span class="sxs-lookup"><span data-stu-id="d15c7-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="d15c7-116">Aquests valors inclouen la data de la transacció, la línia de contracte a la qual està assignada el projecte i el resultat de moneda a la llista de preus adequada.</span><span class="sxs-lookup"><span data-stu-id="d15c7-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="d15c7-117">Els camps que afecten els preus per defecte, com ara **Funció** i **Unitat organitzativa**, s'utilitzen per determinar el preu adient a la línia del llibre diari.</span><span class="sxs-lookup"><span data-stu-id="d15c7-117">The fields that affect default pricing, such as **Role** and **Org Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="d15c7-118">Podeu afegir un camp personalitzat a l'entrada de temps.</span><span class="sxs-lookup"><span data-stu-id="d15c7-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="d15c7-119">Si voleu que el valor del camp es propagui a valors reals, creeu el camp a l'entitat Valors reals i utilitzeu assignacions de camps per copiar el camp de l'entrada de temps al valor real.</span><span class="sxs-lookup"><span data-stu-id="d15c7-119">If you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="d15c7-120">Línies del llibre diari i enviament bàsic de despeses</span><span class="sxs-lookup"><span data-stu-id="d15c7-120">Journal lines and basic expense submission</span></span>

<span data-ttu-id="d15c7-121">Per obtenir més informació sobre l'entrada de despesa, vegeu [Descripció general de les entrades de despesa](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="d15c7-121">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="d15c7-122">Temps i materials</span><span class="sxs-lookup"><span data-stu-id="d15c7-122">Time and materials</span></span>

<span data-ttu-id="d15c7-123">Quan una entrada de despesa bàsica que s'envia està enllaçat a un projecte que s'assigna a una línia de contracte de temps i materials, el sistema crea dues línies del llibre diari, una per al cost i l'altra per a les vendes sense facturar.</span><span class="sxs-lookup"><span data-stu-id="d15c7-123">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="d15c7-124">Preu fix</span><span class="sxs-lookup"><span data-stu-id="d15c7-124">Fixed price</span></span>

<span data-ttu-id="d15c7-125">Quan una entrada de despesa bàsica que s'envia està enllaçada a un projecte assignat a una línia de contracte de preu fix, el sistema crea una línia del llibre diari per al cost.</span><span class="sxs-lookup"><span data-stu-id="d15c7-125">When a basic expense entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="d15c7-126">Preus per defecte</span><span class="sxs-lookup"><span data-stu-id="d15c7-126">Default pricing</span></span>

<span data-ttu-id="d15c7-127">La lògica per a la introducció dels preus per defecte de les despeses es basa en la categoria de despeses.</span><span class="sxs-lookup"><span data-stu-id="d15c7-127">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="d15c7-128">La data de la transacció, la línia de contracte a la qual està assignada el projecte i la moneda s'utilitzen per determinar la llista de preus adequada.</span><span class="sxs-lookup"><span data-stu-id="d15c7-128">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="d15c7-129">No obstant, per defecte, l'import que s'introdueix per al preu en si mateix es defineix directament a les línies del llibre diari de despesa relacionades per al cost i les vendes.</span><span class="sxs-lookup"><span data-stu-id="d15c7-129">However, by default, the amount that is entered for the price itself is set directly on the related expense journal lines for cost and sales.</span></span>

<span data-ttu-id="d15c7-130">L'entrada basada en categories per a preus per unitat per defecte a les entrades de despesa no està disponible.</span><span class="sxs-lookup"><span data-stu-id="d15c7-130">Category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="d15c7-131">Utilitzar llibres diari per registrar costos de registre</span><span class="sxs-lookup"><span data-stu-id="d15c7-131">Use entry journals to record costs</span></span>

<span data-ttu-id="d15c7-132">Podeu utilitzar llibres diari per registrar els costos o ingressos en classes de material, quota, temps, despeses o transaccions tributàries.</span><span class="sxs-lookup"><span data-stu-id="d15c7-132">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="d15c7-133">Els diaris es poden utilitzar amb l'objectiu següent:</span><span class="sxs-lookup"><span data-stu-id="d15c7-133">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="d15c7-134">Registrar els costos reals materials i les vendes d'un projecte.</span><span class="sxs-lookup"><span data-stu-id="d15c7-134">Record the actual cost of materials and sales on a project.</span></span>
- <span data-ttu-id="d15c7-135">Moure els valors reals de la transacció des d'un altre sistema al Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="d15c7-135">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="d15c7-136">Registrar els costos que s'han produït en un altre sistema.</span><span class="sxs-lookup"><span data-stu-id="d15c7-136">Record costs that occurred in another system.</span></span> <span data-ttu-id="d15c7-137">Aquestes despeses poden incloure costos de contractació o subcontractació.</span><span class="sxs-lookup"><span data-stu-id="d15c7-137">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d15c7-138">L'aplicació no valida el tipus de línia del llibre diari ni el preu relacionat que introduïu a la línia del llibre diari.</span><span class="sxs-lookup"><span data-stu-id="d15c7-138">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="d15c7-139">Per tant, només un usuari que tingui consciència de l'impacte comptable que tenen els valors reals en el projecte hauria d'utilitzar els llibres diari per crear valors reals.</span><span class="sxs-lookup"><span data-stu-id="d15c7-139">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="d15c7-140">A causa de l'impacte d'aquest tipus de diari, heu de triar amb cura qui té accés per crear llibres diari.</span><span class="sxs-lookup"><span data-stu-id="d15c7-140">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>
## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="d15c7-141">Enregistrament de valors reals a partir d'esdeveniments de projecte</span><span class="sxs-lookup"><span data-stu-id="d15c7-141">Record actuals based on project events</span></span>

<span data-ttu-id="d15c7-142">El Project Operations registra totes les transaccions financeres que es produeixen durant un projecte.</span><span class="sxs-lookup"><span data-stu-id="d15c7-142">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="d15c7-143">Aquestes transaccions es registren com a valors reals.</span><span class="sxs-lookup"><span data-stu-id="d15c7-143">These transactions are recorded as actuals.</span></span> <span data-ttu-id="d15c7-144">Les taules següents mostren els diferents tipus de valors reals que s'han creat, en funció de si el projecte és un projecte de temps i materials o de preu fix, si es troba a la fase de prevenda o si és un projecte intern.</span><span class="sxs-lookup"><span data-stu-id="d15c7-144">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="d15c7-145">El recurs pertany a la mateixa unitat organitzativa que la unitat de contractació del projecte</span><span class="sxs-lookup"><span data-stu-id="d15c7-145">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="d15c7-146">Incidència</span><span class="sxs-lookup"><span data-stu-id="d15c7-146">Event</span></span></th>
<th colspan="4"><span data-ttu-id="d15c7-147">Projecte facturable o venut</span><span class="sxs-lookup"><span data-stu-id="d15c7-147">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="d15c7-148">Projecte a la fase de prevenda</span><span class="sxs-lookup"><span data-stu-id="d15c7-148">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="d15c7-149">Projecte intern</span><span class="sxs-lookup"><span data-stu-id="d15c7-149">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="d15c7-150">Temps i materials</span><span class="sxs-lookup"><span data-stu-id="d15c7-150">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="d15c7-151">Preu fix</span><span class="sxs-lookup"><span data-stu-id="d15c7-151">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="d15c7-152">Valors reals</span><span class="sxs-lookup"><span data-stu-id="d15c7-152">Actuals</span></span></th>
<th><span data-ttu-id="d15c7-153">Moneda de transacció</span><span class="sxs-lookup"><span data-stu-id="d15c7-153">Transaction currency</span></span></th>
<th><span data-ttu-id="d15c7-154">Preu fix</span><span class="sxs-lookup"><span data-stu-id="d15c7-154">Fixed price</span></span></th>
<th><span data-ttu-id="d15c7-155">Moneda de transacció</span><span class="sxs-lookup"><span data-stu-id="d15c7-155">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d15c7-156">Es crea una entrada de temps.</span><span class="sxs-lookup"><span data-stu-id="d15c7-156">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="d15c7-157">No hi ha activitat a l'entitat Valors reals</span><span class="sxs-lookup"><span data-stu-id="d15c7-157">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d15c7-158">S'envia una entrada de temps.</span><span class="sxs-lookup"><span data-stu-id="d15c7-158">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="d15c7-159">No hi ha activitat a l'entitat Valors reals</span><span class="sxs-lookup"><span data-stu-id="d15c7-159">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="d15c7-160">El temps s'aprova, i no es produeix cap canvi o augment de les hores facturables durant l'aprovació.</span><span class="sxs-lookup"><span data-stu-id="d15c7-160">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="d15c7-161">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="d15c7-161">Cost actual</span></span></td>
<td><span data-ttu-id="d15c7-162">Moneda de la unitat de contractació</span><span class="sxs-lookup"><span data-stu-id="d15c7-162">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="d15c7-163">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="d15c7-163">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="d15c7-164">Moneda de la unitat de contractació</span><span class="sxs-lookup"><span data-stu-id="d15c7-164">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="d15c7-165">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="d15c7-165">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="d15c7-166">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="d15c7-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d15c7-167">Valor real de les vendes no facturades - Imputable</span><span class="sxs-lookup"><span data-stu-id="d15c7-167">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="d15c7-168">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="d15c7-168">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="d15c7-169">El temps s'aprova, i es produeix una reducció de les hores facturables durant l'aprovació.</span><span class="sxs-lookup"><span data-stu-id="d15c7-169">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="d15c7-170">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="d15c7-170">Cost actual</span></span></td>
<td><span data-ttu-id="d15c7-171">Moneda de la unitat de contractació</span><span class="sxs-lookup"><span data-stu-id="d15c7-171">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="d15c7-172">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="d15c7-172">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="d15c7-173">Moneda de la unitat de contractació</span><span class="sxs-lookup"><span data-stu-id="d15c7-173">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="d15c7-174">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="d15c7-174">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="d15c7-175">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="d15c7-175">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d15c7-176">Valor real de les vendes no facturades - Imputable per a la nova quantitat</span><span class="sxs-lookup"><span data-stu-id="d15c7-176">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="d15c7-177">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="d15c7-177">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d15c7-178">Valor real de les vendes no facturades - No imputable per la diferència</span><span class="sxs-lookup"><span data-stu-id="d15c7-178">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="d15c7-179">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="d15c7-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="d15c7-180">Es confirma una factura, i no es produeix cap canvi o augment de les hores facturables.</span><span class="sxs-lookup"><span data-stu-id="d15c7-180">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="d15c7-181">Reversió de vendes no facturades</span><span class="sxs-lookup"><span data-stu-id="d15c7-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="d15c7-182">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="d15c7-182">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="d15c7-183">Vendes facturades per fita</span><span class="sxs-lookup"><span data-stu-id="d15c7-183">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="d15c7-184">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="d15c7-184">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="d15c7-185">No aplicable</span><span class="sxs-lookup"><span data-stu-id="d15c7-185">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="d15c7-186">No aplicable</span><span class="sxs-lookup"><span data-stu-id="d15c7-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d15c7-187">Vendes facturades</span><span class="sxs-lookup"><span data-stu-id="d15c7-187">Billed sales</span></span></td>
<td><span data-ttu-id="d15c7-188">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="d15c7-188">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="d15c7-189">Es confirma una factura, i es produeix una disminució de les hores facturables.</span><span class="sxs-lookup"><span data-stu-id="d15c7-189">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="d15c7-190">Reversió de vendes no facturades</span><span class="sxs-lookup"><span data-stu-id="d15c7-190">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="d15c7-191">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="d15c7-191">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="d15c7-192">No aplicable</span><span class="sxs-lookup"><span data-stu-id="d15c7-192">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="d15c7-193">No aplicable</span><span class="sxs-lookup"><span data-stu-id="d15c7-193">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="d15c7-194">No aplicable</span><span class="sxs-lookup"><span data-stu-id="d15c7-194">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="d15c7-195">No aplicable</span><span class="sxs-lookup"><span data-stu-id="d15c7-195">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d15c7-196">Vendes facturades - Imputable per a la nova quantitat</span><span class="sxs-lookup"><span data-stu-id="d15c7-196">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="d15c7-197">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="d15c7-197">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d15c7-198">Vendes facturades - No imputable per la diferència</span><span class="sxs-lookup"><span data-stu-id="d15c7-198">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="d15c7-199">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="d15c7-199">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="d15c7-200">Una factura es corregeix per augmentar la quantitat imputable.</span><span class="sxs-lookup"><span data-stu-id="d15c7-200">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="d15c7-201">Vendes facturades - Reversió</span><span class="sxs-lookup"><span data-stu-id="d15c7-201">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="d15c7-202">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="d15c7-202">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="d15c7-203">Reversió de vendes facturades per fita</span><span class="sxs-lookup"><span data-stu-id="d15c7-203">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="d15c7-204">Canvi en l'estat de la fita de <strong>Facturada</strong> a <strong>Llesta per facturar</strong></span><span class="sxs-lookup"><span data-stu-id="d15c7-204">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="d15c7-205">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="d15c7-205">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="d15c7-206">No aplicable</span><span class="sxs-lookup"><span data-stu-id="d15c7-206">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="d15c7-207">No aplicable</span><span class="sxs-lookup"><span data-stu-id="d15c7-207">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d15c7-208">Vendes facturades</span><span class="sxs-lookup"><span data-stu-id="d15c7-208">Billed sales</span></span></td>
<td><span data-ttu-id="d15c7-209">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="d15c7-209">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="d15c7-210">Una factura es corregeix per reduir la quantitat imputable.</span><span class="sxs-lookup"><span data-stu-id="d15c7-210">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="d15c7-211">Vendes facturades - Reversió</span><span class="sxs-lookup"><span data-stu-id="d15c7-211">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="d15c7-212">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="d15c7-212">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d15c7-213">Vendes facturades per a la nova quantitat</span><span class="sxs-lookup"><span data-stu-id="d15c7-213">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="d15c7-214">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="d15c7-214">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d15c7-215">Vendes no facturades - Imputable per la diferència</span><span class="sxs-lookup"><span data-stu-id="d15c7-215">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="d15c7-216">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="d15c7-216">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="d15c7-217">El recurs pertany a una unitat organitzativa diferent de la unitat de contractació del projecte</span><span class="sxs-lookup"><span data-stu-id="d15c7-217">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="d15c7-218">Incidència</span><span class="sxs-lookup"><span data-stu-id="d15c7-218">Event</span></span></th>
<th colspan="4"><span data-ttu-id="d15c7-219">Projecte facturable o venut</span><span class="sxs-lookup"><span data-stu-id="d15c7-219">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="d15c7-220">Projecte a la fase de prevenda</span><span class="sxs-lookup"><span data-stu-id="d15c7-220">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="d15c7-221">Projecte intern</span><span class="sxs-lookup"><span data-stu-id="d15c7-221">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="d15c7-222">Temps i materials</span><span class="sxs-lookup"><span data-stu-id="d15c7-222">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="d15c7-223">Preu fix</span><span class="sxs-lookup"><span data-stu-id="d15c7-223">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="d15c7-224">Valors reals</span><span class="sxs-lookup"><span data-stu-id="d15c7-224">Actuals</span></span></th>
<th><span data-ttu-id="d15c7-225">Moneda de transacció</span><span class="sxs-lookup"><span data-stu-id="d15c7-225">Transaction currency</span></span></th>
<th><span data-ttu-id="d15c7-226">Preu fix</span><span class="sxs-lookup"><span data-stu-id="d15c7-226">Fixed price</span></span></th>
<th><span data-ttu-id="d15c7-227">Moneda de transacció</span><span class="sxs-lookup"><span data-stu-id="d15c7-227">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d15c7-228">Es crea una entrada de temps.</span><span class="sxs-lookup"><span data-stu-id="d15c7-228">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="d15c7-229">No hi ha activitat a l'entitat Valors reals</span><span class="sxs-lookup"><span data-stu-id="d15c7-229">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d15c7-230">S'envia una entrada de temps.</span><span class="sxs-lookup"><span data-stu-id="d15c7-230">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="d15c7-231">No hi ha activitat a l'entitat Valors reals</span><span class="sxs-lookup"><span data-stu-id="d15c7-231">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="d15c7-232">El temps s'aprova, i no es produeix cap canvi o augment de les hores facturables durant l'aprovació.</span><span class="sxs-lookup"><span data-stu-id="d15c7-232">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="d15c7-233">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="d15c7-233">Cost actual</span></span></td>
<td><span data-ttu-id="d15c7-234">Moneda de la unitat de contractació</span><span class="sxs-lookup"><span data-stu-id="d15c7-234">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="d15c7-235">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="d15c7-235">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="d15c7-236">Moneda de la unitat de contractació</span><span class="sxs-lookup"><span data-stu-id="d15c7-236">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="d15c7-237">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="d15c7-237">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="d15c7-238">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="d15c7-238">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d15c7-239">Valor real de les vendes no facturades - Imputable</span><span class="sxs-lookup"><span data-stu-id="d15c7-239">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="d15c7-240">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="d15c7-240">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d15c7-241">Cost de la unitat de recursos</span><span class="sxs-lookup"><span data-stu-id="d15c7-241">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="d15c7-242">Moneda de la unitat de recursos</span><span class="sxs-lookup"><span data-stu-id="d15c7-242">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d15c7-243">Vendes interorganitzatives</span><span class="sxs-lookup"><span data-stu-id="d15c7-243">Interorganizational sales</span></span></td>
<td><span data-ttu-id="d15c7-244">Moneda de la unitat de contractació</span><span class="sxs-lookup"><span data-stu-id="d15c7-244">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="d15c7-245">El temps s'aprova, i es produeix una reducció de les hores facturables durant l'aprovació.</span><span class="sxs-lookup"><span data-stu-id="d15c7-245">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="d15c7-246">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="d15c7-246">Cost actual</span></span></td>
<td><span data-ttu-id="d15c7-247">Moneda de la unitat de contractació</span><span class="sxs-lookup"><span data-stu-id="d15c7-247">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="d15c7-248">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="d15c7-248">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="d15c7-249">Moneda de la unitat de contractació</span><span class="sxs-lookup"><span data-stu-id="d15c7-249">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="d15c7-250">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="d15c7-250">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="d15c7-251">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="d15c7-251">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d15c7-252">Cost de la unitat de recursos</span><span class="sxs-lookup"><span data-stu-id="d15c7-252">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="d15c7-253">Moneda de la unitat de recursos</span><span class="sxs-lookup"><span data-stu-id="d15c7-253">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d15c7-254">Vendes interorganitzatives</span><span class="sxs-lookup"><span data-stu-id="d15c7-254">Interorganizational sales</span></span></td>
<td><span data-ttu-id="d15c7-255">Moneda de la unitat de contractació</span><span class="sxs-lookup"><span data-stu-id="d15c7-255">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d15c7-256">Valor real de les vendes no facturades - Imputable per a la nova quantitat</span><span class="sxs-lookup"><span data-stu-id="d15c7-256">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="d15c7-257">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="d15c7-257">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d15c7-258">Valor real de les vendes no facturades - No imputable per la diferència</span><span class="sxs-lookup"><span data-stu-id="d15c7-258">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="d15c7-259">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="d15c7-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="d15c7-260">Es confirma una factura, i no es produeix cap canvi o augment de les hores facturables.</span><span class="sxs-lookup"><span data-stu-id="d15c7-260">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="d15c7-261">Reversió de vendes no facturades</span><span class="sxs-lookup"><span data-stu-id="d15c7-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="d15c7-262">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="d15c7-262">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="d15c7-263">Vendes facturades per fita</span><span class="sxs-lookup"><span data-stu-id="d15c7-263">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="d15c7-264">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="d15c7-264">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="d15c7-265">No aplicable</span><span class="sxs-lookup"><span data-stu-id="d15c7-265">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="d15c7-266">No aplicable</span><span class="sxs-lookup"><span data-stu-id="d15c7-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d15c7-267">Vendes facturades</span><span class="sxs-lookup"><span data-stu-id="d15c7-267">Billed sales</span></span></td>
<td><span data-ttu-id="d15c7-268">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="d15c7-268">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="d15c7-269">Es confirma una factura, i es produeix una disminució de les hores facturables.</span><span class="sxs-lookup"><span data-stu-id="d15c7-269">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="d15c7-270">Reversió de vendes no facturades</span><span class="sxs-lookup"><span data-stu-id="d15c7-270">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="d15c7-271">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="d15c7-271">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="d15c7-272">No aplicable</span><span class="sxs-lookup"><span data-stu-id="d15c7-272">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="d15c7-273">No aplicable</span><span class="sxs-lookup"><span data-stu-id="d15c7-273">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="d15c7-274">No aplicable</span><span class="sxs-lookup"><span data-stu-id="d15c7-274">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="d15c7-275">No aplicable</span><span class="sxs-lookup"><span data-stu-id="d15c7-275">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d15c7-276">Vendes facturades - Imputable per a la nova quantitat</span><span class="sxs-lookup"><span data-stu-id="d15c7-276">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="d15c7-277">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="d15c7-277">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d15c7-278">Vendes facturades - No imputable per la diferència</span><span class="sxs-lookup"><span data-stu-id="d15c7-278">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="d15c7-279">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="d15c7-279">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="d15c7-280">Una factura es corregeix per augmentar la quantitat imputable.</span><span class="sxs-lookup"><span data-stu-id="d15c7-280">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="d15c7-281">Vendes facturades - Reversió</span><span class="sxs-lookup"><span data-stu-id="d15c7-281">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="d15c7-282">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="d15c7-282">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="d15c7-283">Reversió de vendes facturades per fita</span><span class="sxs-lookup"><span data-stu-id="d15c7-283">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="d15c7-284">Canvi en l'estat de la fita de <strong>Facturada</strong> a <strong>Llesta per facturar</strong></span><span class="sxs-lookup"><span data-stu-id="d15c7-284">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="d15c7-285">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="d15c7-285">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="d15c7-286">No aplicable</span><span class="sxs-lookup"><span data-stu-id="d15c7-286">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="d15c7-287">No aplicable</span><span class="sxs-lookup"><span data-stu-id="d15c7-287">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d15c7-288">Vendes facturades</span><span class="sxs-lookup"><span data-stu-id="d15c7-288">Billed sales</span></span></td>
<td><span data-ttu-id="d15c7-289">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="d15c7-289">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="d15c7-290">Una factura es corregeix per reduir la quantitat imputable.</span><span class="sxs-lookup"><span data-stu-id="d15c7-290">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="d15c7-291">Vendes facturades - Reversió</span><span class="sxs-lookup"><span data-stu-id="d15c7-291">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="d15c7-292">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="d15c7-292">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d15c7-293">Vendes facturades per a la nova quantitat</span><span class="sxs-lookup"><span data-stu-id="d15c7-293">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="d15c7-294">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="d15c7-294">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d15c7-295">Vendes no facturades - Imputable per la diferència</span><span class="sxs-lookup"><span data-stu-id="d15c7-295">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="d15c7-296">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="d15c7-296">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
