---
title: Valors reals
description: En aquest tema es proporciona informació sobre com treballar amb valors reals al Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 78c7a9486d0338adfd7770447f21d17509e654f7
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996599"
---
# <a name="actuals"></a><span data-ttu-id="33325-103">Valors reals</span><span class="sxs-lookup"><span data-stu-id="33325-103">Actuals</span></span> 

<span data-ttu-id="33325-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_</span><span class="sxs-lookup"><span data-stu-id="33325-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="33325-105">Els valors reals representen el progrés financer revisat i aprovat i la planificació en un projecte.</span><span class="sxs-lookup"><span data-stu-id="33325-105">Actuals represent the reviewed and approved financial and schedule progress on a project.</span></span> <span data-ttu-id="33325-106">Es creen com a resultat de l'aprovació del temps, la despesa, les entrades d'ús de materials i les entrades i factures al llibre diari.</span><span class="sxs-lookup"><span data-stu-id="33325-106">They are created as a result of approval of time, expense, material usage entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="33325-107">Línies del llibre diari i enviament de temps</span><span class="sxs-lookup"><span data-stu-id="33325-107">Journal lines and time submission</span></span>

<span data-ttu-id="33325-108">Per obtenir més informació sobre l'entrada de temps, vegeu [Descripció general de les entrades de temps](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="33325-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="33325-109">Temps i materials</span><span class="sxs-lookup"><span data-stu-id="33325-109">Time and materials</span></span>

<span data-ttu-id="33325-110">Quan un registre de temps que s'envia està enllaçat a un projecte que s'assigna a una línia de contracte de temps i materials, el sistema crea dues línies del llibre diari, una per al cost i l'altra per a les vendes sense facturar.</span><span class="sxs-lookup"><span data-stu-id="33325-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="33325-111">Preu fix</span><span class="sxs-lookup"><span data-stu-id="33325-111">Fixed price</span></span>

<span data-ttu-id="33325-112">Quan una entrada de temps que s'envia està enllaçada a un projecte assignat a una línia de contracte de preu fix, el sistema crea una línia del llibre diari per al cost.</span><span class="sxs-lookup"><span data-stu-id="33325-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="33325-113">Preus per defecte</span><span class="sxs-lookup"><span data-stu-id="33325-113">Default pricing</span></span>

<span data-ttu-id="33325-114">La lògica per crear els preus per defecte resideix a la línia del llibre diari.</span><span class="sxs-lookup"><span data-stu-id="33325-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="33325-115">Els valors de camp de l'entrada de temps es copien a la línia del llibre diari.</span><span class="sxs-lookup"><span data-stu-id="33325-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="33325-116">Aquests valors inclouen la data de la transacció, la línia de contracte a la qual està assignada el projecte i el resultat de moneda a la llista de preus adequada.</span><span class="sxs-lookup"><span data-stu-id="33325-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="33325-117">Els camps que afecten els preus per defecte, com ara **Funció** i **Unitat de recursos** s'utilitzen per determinar un preu adient a la línia del llibre diari.</span><span class="sxs-lookup"><span data-stu-id="33325-117">The fields that affect default pricing, such as **Role** and **Resourcing Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="33325-118">Podeu afegir un camp personalitzat a l'entrada de temps.</span><span class="sxs-lookup"><span data-stu-id="33325-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="33325-119">Si voleu que el valor de camp es propagui als valors reals, creeu el camp a les taules **Valors reals** i **Línia del llibre diari**.</span><span class="sxs-lookup"><span data-stu-id="33325-119">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="33325-120">Utilitzeu el codi personalitzat per propagar el valor del camp seleccionat des d'Entrada de temps a Valors reals a través de la línia del llibre diari mitjançant orígens de transaccions.</span><span class="sxs-lookup"><span data-stu-id="33325-120">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="33325-121">Per obtenir més informació sobre els orígens i les connexions de les transaccions, vegeu [Enllaçar valors reals amb registres originals](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="33325-121">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="33325-122">Línies del llibre diari i enviament bàsic de despeses</span><span class="sxs-lookup"><span data-stu-id="33325-122">Journal lines and basic expense submission</span></span>

<span data-ttu-id="33325-123">Per obtenir més informació sobre l'entrada de despesa, vegeu [Descripció general de les entrades de despesa](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="33325-123">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="33325-124">Temps i materials</span><span class="sxs-lookup"><span data-stu-id="33325-124">Time and materials</span></span>

<span data-ttu-id="33325-125">Quan una entrada de despesa bàsica que s'envia està enllaçat a un projecte que s'assigna a una línia de contracte de temps i materials, el sistema crea dues línies del llibre diari, una per al cost i l'altra per a les vendes sense facturar.</span><span class="sxs-lookup"><span data-stu-id="33325-125">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="33325-126">Preu fix</span><span class="sxs-lookup"><span data-stu-id="33325-126">Fixed price</span></span>

<span data-ttu-id="33325-127">Quan una entrada de despesa bàsica presentada està a enllaçada a un projecte assignat a una línia de contracte de preu fix, el sistema crea una línia del llibre diari per al cost.</span><span class="sxs-lookup"><span data-stu-id="33325-127">When a submitted basic expense entry is linked to a project that's mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="33325-128">Preus per defecte</span><span class="sxs-lookup"><span data-stu-id="33325-128">Default pricing</span></span>

<span data-ttu-id="33325-129">La lògica per a la introducció dels preus per defecte de les despeses es basa en la categoria de despeses.</span><span class="sxs-lookup"><span data-stu-id="33325-129">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="33325-130">La data de la transacció, la línia de contracte a la qual està assignada el projecte i la moneda s'utilitzen per determinar la llista de preus adequada.</span><span class="sxs-lookup"><span data-stu-id="33325-130">The transaction date, the contract line that the project is mapped to, and the currency, are all used to determine the appropriate price list.</span></span> <span data-ttu-id="33325-131">Els camps que afecten els preus per defecte, com ara **Categoria de transacció** i **Unitat** s'utilitzen per determinar un preu adient a la línia del llibre diari.</span><span class="sxs-lookup"><span data-stu-id="33325-131">The fields that affect default pricing, such as **Transaction Category** and **Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="33325-132">Tanmateix, només funciona quan el mètode de preus de la llista de preus és **Preu per unitat**.</span><span class="sxs-lookup"><span data-stu-id="33325-132">However, this only works when the pricing method in the price list is **Price per unit**.</span></span> <span data-ttu-id="33325-133">Si el mètode de càlcul de preus és **A partir del cost** o **Marcador sobre el cost**, el preu que s'ha introduït en crear l'entrada de despesa s'utilitza per al cost i el preu de la línia al llibre diari segons el mètode de càlcul de preus.</span><span class="sxs-lookup"><span data-stu-id="33325-133">If pricing method is **At cost** or **Markup over cost**, the price entered when the expense entry is created is used for cost and the price on the sales journal line is calculated based on the pricing method.</span></span> 

<span data-ttu-id="33325-134">Podeu afegir un camp personalitzat a l'entrada de despesa.</span><span class="sxs-lookup"><span data-stu-id="33325-134">You can add a custom field on the expense entry.</span></span> <span data-ttu-id="33325-135">Si voleu que el valor de camp es propagui als valors reals, creeu el camp a les taules **Valors reals** i **Línia del llibre diari**.</span><span class="sxs-lookup"><span data-stu-id="33325-135">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="33325-136">Utilitzeu el codi personalitzat per propagar el valor del camp seleccionat des d'Entrada de temps a Valors reals a través de la línia del llibre diari mitjançant orígens de transaccions.</span><span class="sxs-lookup"><span data-stu-id="33325-136">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="33325-137">Per obtenir més informació sobre els orígens i les connexions de les transaccions, vegeu [Enllaçar valors reals amb registres originals](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="33325-137">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="journal-lines-and-material-usage-log-submission"></a><span data-ttu-id="33325-138">Enviament de línies del llibre diari i de registre d'ús de materials</span><span class="sxs-lookup"><span data-stu-id="33325-138">Journal lines and material usage log submission</span></span>

<span data-ttu-id="33325-139">Per obtenir més informació sobre l'entrada de despeses, vegeu [Registre d'ús de materials](../material/material-usage-log.md).</span><span class="sxs-lookup"><span data-stu-id="33325-139">For more information about expense entry, see [Material Usage Log](../material/material-usage-log.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="33325-140">Temps i materials</span><span class="sxs-lookup"><span data-stu-id="33325-140">Time and materials</span></span>

<span data-ttu-id="33325-141">Quan una entrada de registre d'ús de materials enviada s'enllaça amb un projecte que està assignat a una línia de contracte de temps i materials, el sistema crea dues línies del llibre diari, una per al cost i una altra per a les vendes no facturades.</span><span class="sxs-lookup"><span data-stu-id="33325-141">When a submitted material usage log entry is linked to a project that is mapped to a time and materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="33325-142">Preu fix</span><span class="sxs-lookup"><span data-stu-id="33325-142">Fixed price</span></span>

<span data-ttu-id="33325-143">Quan una entrada de registre d'ús de materials presentada està enllaçada a un projecte assignat a una línia de contracte de preu fix, el sistema crea una línia del llibre diari per al cost.</span><span class="sxs-lookup"><span data-stu-id="33325-143">When a submitted material usage log entry is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="33325-144">Preus per defecte</span><span class="sxs-lookup"><span data-stu-id="33325-144">Default pricing</span></span>

<span data-ttu-id="33325-145">La lògica per introduir preus per defecte per al material es basa en la combinació de productes i unitats.</span><span class="sxs-lookup"><span data-stu-id="33325-145">The logic for entering default prices for material is based on the product and unit combination.</span></span> <span data-ttu-id="33325-146">La data de la transacció, la línia de contracte a la qual està assignada el projecte i la moneda s'utilitzen per determinar la llista de preus adequada.</span><span class="sxs-lookup"><span data-stu-id="33325-146">The transaction date, the contract line that the project is mapped to, and the currency, are all used to determine the appropriate price list.</span></span> <span data-ttu-id="33325-147">Els camps que afecten els preus per defecte, com ara **Identificador del producte** i **Unitat**, s'utilitzen per determinar un preu adient a la línia del llibre diari.</span><span class="sxs-lookup"><span data-stu-id="33325-147">The fields that affect default pricing, such as **Product ID** and **Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="33325-148">Però això només funciona per als productes del catàleg.</span><span class="sxs-lookup"><span data-stu-id="33325-148">However, this only works for catalog products.</span></span> <span data-ttu-id="33325-149">Per als productes fora de catàleg, el preu que introduït en crear l'entrada del registre d'ús de materials s'utilitza per al cost i el preu de venda a les línies del llibre diari,</span><span class="sxs-lookup"><span data-stu-id="33325-149">For write-in products, the price entered when the material usage log entry is created is used for cost and sales price on the journal lines.</span></span> 

<span data-ttu-id="33325-150">Podeu afegir un camp personalitzat a l'entrada **Registre d'ús de materials**.</span><span class="sxs-lookup"><span data-stu-id="33325-150">You can add a custom field on the **Material Usage Log** entry.</span></span> <span data-ttu-id="33325-151">Si voleu que el valor de camp es propagui als valors reals, creeu el camp a les taules **Valors reals** i **Línia del llibre diari**.</span><span class="sxs-lookup"><span data-stu-id="33325-151">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="33325-152">Utilitzeu el codi personalitzat per propagar el valor del camp seleccionat des d'Entrada de temps a Valors reals a través de la línia del llibre diari mitjançant orígens de transaccions.</span><span class="sxs-lookup"><span data-stu-id="33325-152">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="33325-153">Per obtenir més informació sobre els orígens i les connexions de les transaccions, vegeu [Enllaçar valors reals amb registres originals](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="33325-153">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="33325-154">Utilitzar llibres diari per registrar costos de registre</span><span class="sxs-lookup"><span data-stu-id="33325-154">Use entry journals to record costs</span></span>

<span data-ttu-id="33325-155">Podeu utilitzar llibres diari per registrar els costos o ingressos en classes de material, quota, temps, despeses o transaccions tributàries.</span><span class="sxs-lookup"><span data-stu-id="33325-155">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="33325-156">Els diaris es poden utilitzar amb l'objectiu següent:</span><span class="sxs-lookup"><span data-stu-id="33325-156">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="33325-157">Avanceu els valors reals de la transacció des d'un altre sistema al Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="33325-157">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="33325-158">Registrar els costos que s'han produït en un altre sistema.</span><span class="sxs-lookup"><span data-stu-id="33325-158">Record costs that occurred in another system.</span></span> <span data-ttu-id="33325-159">Aquestes despeses poden incloure costos de contractació o subcontractació.</span><span class="sxs-lookup"><span data-stu-id="33325-159">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="33325-160">L'aplicació no valida el tipus de línia del llibre diari ni el preu relacionat que introduïu a la línia del llibre diari.</span><span class="sxs-lookup"><span data-stu-id="33325-160">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="33325-161">Per tant, només un usuari que tingui consciència de l'impacte comptable que tenen els valors reals en el projecte hauria d'utilitzar els llibres diari per crear valors reals.</span><span class="sxs-lookup"><span data-stu-id="33325-161">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="33325-162">A causa de l'impacte d'aquest tipus de diari, heu de triar amb cura qui té accés per crear llibres diari.</span><span class="sxs-lookup"><span data-stu-id="33325-162">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>

## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="33325-163">Enregistrament de valors reals a partir d'esdeveniments de projecte</span><span class="sxs-lookup"><span data-stu-id="33325-163">Record actuals based on project events</span></span>

<span data-ttu-id="33325-164">El Project Operations registra totes les transaccions financeres que es produeixen durant un projecte.</span><span class="sxs-lookup"><span data-stu-id="33325-164">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="33325-165">Aquestes transaccions es registren com a valors reals.</span><span class="sxs-lookup"><span data-stu-id="33325-165">These transactions are recorded as actuals.</span></span> <span data-ttu-id="33325-166">Les taules següents mostren els diferents tipus de valors reals que s'han creat, en funció de si el projecte és un projecte de temps i materials o de preu fix, si es troba a la fase de prevenda o si és un projecte intern.</span><span class="sxs-lookup"><span data-stu-id="33325-166">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="33325-167">El recurs pertany a la mateixa unitat organitzativa que la unitat de contractació del projecte</span><span class="sxs-lookup"><span data-stu-id="33325-167">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="33325-168">Incidència</span><span class="sxs-lookup"><span data-stu-id="33325-168">Event</span></span></th>
<th colspan="4"><span data-ttu-id="33325-169">Projecte facturable o venut</span><span class="sxs-lookup"><span data-stu-id="33325-169">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="33325-170">Projecte a la fase de prevenda</span><span class="sxs-lookup"><span data-stu-id="33325-170">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="33325-171">Projecte intern</span><span class="sxs-lookup"><span data-stu-id="33325-171">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="33325-172">Temps i materials</span><span class="sxs-lookup"><span data-stu-id="33325-172">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="33325-173">Preu fix</span><span class="sxs-lookup"><span data-stu-id="33325-173">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="33325-174">Valors reals</span><span class="sxs-lookup"><span data-stu-id="33325-174">Actuals</span></span></th>
<th><span data-ttu-id="33325-175">Moneda de transacció</span><span class="sxs-lookup"><span data-stu-id="33325-175">Transaction currency</span></span></th>
<th><span data-ttu-id="33325-176">Preu fix</span><span class="sxs-lookup"><span data-stu-id="33325-176">Fixed price</span></span></th>
<th><span data-ttu-id="33325-177">Moneda de transacció</span><span class="sxs-lookup"><span data-stu-id="33325-177">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="33325-178">Es crea una entrada de temps.</span><span class="sxs-lookup"><span data-stu-id="33325-178">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="33325-179">No hi ha activitat a l'entitat Valors reals</span><span class="sxs-lookup"><span data-stu-id="33325-179">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33325-180">S'envia una entrada de temps.</span><span class="sxs-lookup"><span data-stu-id="33325-180">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="33325-181">No hi ha activitat a l'entitat Valors reals</span><span class="sxs-lookup"><span data-stu-id="33325-181">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="33325-182">El temps s'aprova, i no es produeix cap canvi o augment de les hores facturables durant l'aprovació.</span><span class="sxs-lookup"><span data-stu-id="33325-182">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="33325-183">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="33325-183">Cost actual</span></span></td>
<td><span data-ttu-id="33325-184">Moneda de la unitat de contractació</span><span class="sxs-lookup"><span data-stu-id="33325-184">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="33325-185">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="33325-185">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="33325-186">Moneda de la unitat de contractació</span><span class="sxs-lookup"><span data-stu-id="33325-186">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="33325-187">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="33325-187">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="33325-188">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="33325-188">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33325-189">Valor real de les vendes no facturades - Imputable</span><span class="sxs-lookup"><span data-stu-id="33325-189">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="33325-190">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="33325-190">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="33325-191">El temps s'aprova, i es produeix una reducció de les hores facturables durant l'aprovació.</span><span class="sxs-lookup"><span data-stu-id="33325-191">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="33325-192">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="33325-192">Cost actual</span></span></td>
<td><span data-ttu-id="33325-193">Moneda de la unitat de contractació</span><span class="sxs-lookup"><span data-stu-id="33325-193">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="33325-194">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="33325-194">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="33325-195">Moneda de la unitat de contractació</span><span class="sxs-lookup"><span data-stu-id="33325-195">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="33325-196">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="33325-196">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="33325-197">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="33325-197">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33325-198">Valor real de les vendes no facturades - Imputable per a la nova quantitat</span><span class="sxs-lookup"><span data-stu-id="33325-198">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="33325-199">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="33325-199">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33325-200">Valor real de les vendes no facturades - No imputable per la diferència</span><span class="sxs-lookup"><span data-stu-id="33325-200">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="33325-201">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="33325-201">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="33325-202">Es confirma una factura, i no es produeix cap canvi o augment de les hores facturables.</span><span class="sxs-lookup"><span data-stu-id="33325-202">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="33325-203">Reversió de vendes no facturades</span><span class="sxs-lookup"><span data-stu-id="33325-203">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="33325-204">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="33325-204">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="33325-205">Vendes facturades per fita</span><span class="sxs-lookup"><span data-stu-id="33325-205">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="33325-206">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="33325-206">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="33325-207">No aplicable</span><span class="sxs-lookup"><span data-stu-id="33325-207">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="33325-208">No aplicable</span><span class="sxs-lookup"><span data-stu-id="33325-208">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33325-209">Vendes facturades</span><span class="sxs-lookup"><span data-stu-id="33325-209">Billed sales</span></span></td>
<td><span data-ttu-id="33325-210">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="33325-210">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="33325-211">Es confirma una factura, i es produeix una disminució de les hores facturables.</span><span class="sxs-lookup"><span data-stu-id="33325-211">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="33325-212">Reversió de vendes no facturades</span><span class="sxs-lookup"><span data-stu-id="33325-212">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="33325-213">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="33325-213">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="33325-214">No aplicable</span><span class="sxs-lookup"><span data-stu-id="33325-214">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="33325-215">No aplicable</span><span class="sxs-lookup"><span data-stu-id="33325-215">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="33325-216">No aplicable</span><span class="sxs-lookup"><span data-stu-id="33325-216">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="33325-217">No aplicable</span><span class="sxs-lookup"><span data-stu-id="33325-217">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33325-218">Vendes facturades - Imputable per a la nova quantitat</span><span class="sxs-lookup"><span data-stu-id="33325-218">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="33325-219">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="33325-219">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33325-220">Vendes facturades - No imputable per la diferència</span><span class="sxs-lookup"><span data-stu-id="33325-220">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="33325-221">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="33325-221">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="33325-222">Una factura es corregeix per augmentar la quantitat imputable.</span><span class="sxs-lookup"><span data-stu-id="33325-222">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="33325-223">Vendes facturades - Reversió</span><span class="sxs-lookup"><span data-stu-id="33325-223">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="33325-224">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="33325-224">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="33325-225">Reversió de vendes facturades per fita</span><span class="sxs-lookup"><span data-stu-id="33325-225">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="33325-226">Canvi en l'estat de la fita de <strong>Facturada</strong> a <strong>Llesta per facturar</strong></span><span class="sxs-lookup"><span data-stu-id="33325-226">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="33325-227">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="33325-227">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="33325-228">No aplicable</span><span class="sxs-lookup"><span data-stu-id="33325-228">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="33325-229">No aplicable</span><span class="sxs-lookup"><span data-stu-id="33325-229">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33325-230">Vendes facturades</span><span class="sxs-lookup"><span data-stu-id="33325-230">Billed sales</span></span></td>
<td><span data-ttu-id="33325-231">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="33325-231">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="33325-232">Una factura es corregeix per reduir la quantitat imputable.</span><span class="sxs-lookup"><span data-stu-id="33325-232">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="33325-233">Vendes facturades - Reversió</span><span class="sxs-lookup"><span data-stu-id="33325-233">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="33325-234">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="33325-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33325-235">Vendes facturades per a la nova quantitat</span><span class="sxs-lookup"><span data-stu-id="33325-235">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="33325-236">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="33325-236">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33325-237">Vendes no facturades - Imputable per la diferència</span><span class="sxs-lookup"><span data-stu-id="33325-237">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="33325-238">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="33325-238">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="33325-239">El recurs pertany a una unitat organitzativa diferent de la unitat de contractació del projecte</span><span class="sxs-lookup"><span data-stu-id="33325-239">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="33325-240">Incidència</span><span class="sxs-lookup"><span data-stu-id="33325-240">Event</span></span></th>
<th colspan="4"><span data-ttu-id="33325-241">Projecte facturable o venut</span><span class="sxs-lookup"><span data-stu-id="33325-241">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="33325-242">Projecte a la fase de prevenda</span><span class="sxs-lookup"><span data-stu-id="33325-242">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="33325-243">Projecte intern</span><span class="sxs-lookup"><span data-stu-id="33325-243">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="33325-244">Temps i materials</span><span class="sxs-lookup"><span data-stu-id="33325-244">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="33325-245">Preu fix</span><span class="sxs-lookup"><span data-stu-id="33325-245">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="33325-246">Valors reals</span><span class="sxs-lookup"><span data-stu-id="33325-246">Actuals</span></span></th>
<th><span data-ttu-id="33325-247">Moneda de transacció</span><span class="sxs-lookup"><span data-stu-id="33325-247">Transaction currency</span></span></th>
<th><span data-ttu-id="33325-248">Preu fix</span><span class="sxs-lookup"><span data-stu-id="33325-248">Fixed price</span></span></th>
<th><span data-ttu-id="33325-249">Moneda de transacció</span><span class="sxs-lookup"><span data-stu-id="33325-249">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="33325-250">Es crea una entrada de temps.</span><span class="sxs-lookup"><span data-stu-id="33325-250">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="33325-251">No hi ha activitat a l'entitat Valors reals</span><span class="sxs-lookup"><span data-stu-id="33325-251">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33325-252">S'envia una entrada de temps.</span><span class="sxs-lookup"><span data-stu-id="33325-252">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="33325-253">No hi ha activitat a l'entitat Valors reals</span><span class="sxs-lookup"><span data-stu-id="33325-253">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="33325-254">El temps s'aprova, i no es produeix cap canvi o augment de les hores facturables durant l'aprovació.</span><span class="sxs-lookup"><span data-stu-id="33325-254">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="33325-255">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="33325-255">Cost actual</span></span></td>
<td><span data-ttu-id="33325-256">Moneda de la unitat de contractació</span><span class="sxs-lookup"><span data-stu-id="33325-256">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="33325-257">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="33325-257">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="33325-258">Moneda de la unitat de contractació</span><span class="sxs-lookup"><span data-stu-id="33325-258">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="33325-259">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="33325-259">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="33325-260">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="33325-260">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33325-261">Valor real de les vendes no facturades - Imputable</span><span class="sxs-lookup"><span data-stu-id="33325-261">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="33325-262">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="33325-262">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33325-263">Cost de la unitat de recursos</span><span class="sxs-lookup"><span data-stu-id="33325-263">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="33325-264">Moneda de la unitat de recursos</span><span class="sxs-lookup"><span data-stu-id="33325-264">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33325-265">Vendes interorganitzatives</span><span class="sxs-lookup"><span data-stu-id="33325-265">Interorganizational sales</span></span></td>
<td><span data-ttu-id="33325-266">Moneda de la unitat de contractació</span><span class="sxs-lookup"><span data-stu-id="33325-266">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="33325-267">El temps s'aprova, i es produeix una reducció de les hores facturables durant l'aprovació.</span><span class="sxs-lookup"><span data-stu-id="33325-267">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="33325-268">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="33325-268">Cost actual</span></span></td>
<td><span data-ttu-id="33325-269">Moneda de la unitat de contractació</span><span class="sxs-lookup"><span data-stu-id="33325-269">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="33325-270">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="33325-270">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="33325-271">Moneda de la unitat de contractació</span><span class="sxs-lookup"><span data-stu-id="33325-271">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="33325-272">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="33325-272">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="33325-273">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="33325-273">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33325-274">Cost de la unitat de recursos</span><span class="sxs-lookup"><span data-stu-id="33325-274">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="33325-275">Moneda de la unitat de recursos</span><span class="sxs-lookup"><span data-stu-id="33325-275">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33325-276">Vendes interorganitzatives</span><span class="sxs-lookup"><span data-stu-id="33325-276">Interorganizational sales</span></span></td>
<td><span data-ttu-id="33325-277">Moneda de la unitat de contractació</span><span class="sxs-lookup"><span data-stu-id="33325-277">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33325-278">Valor real de les vendes no facturades - Imputable per a la nova quantitat</span><span class="sxs-lookup"><span data-stu-id="33325-278">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="33325-279">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="33325-279">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33325-280">Valor real de les vendes no facturades - No imputable per la diferència</span><span class="sxs-lookup"><span data-stu-id="33325-280">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="33325-281">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="33325-281">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="33325-282">Es confirma una factura, i no es produeix cap canvi o augment de les hores facturables.</span><span class="sxs-lookup"><span data-stu-id="33325-282">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="33325-283">Reversió de vendes no facturades</span><span class="sxs-lookup"><span data-stu-id="33325-283">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="33325-284">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="33325-284">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="33325-285">Vendes facturades per fita</span><span class="sxs-lookup"><span data-stu-id="33325-285">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="33325-286">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="33325-286">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="33325-287">No aplicable</span><span class="sxs-lookup"><span data-stu-id="33325-287">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="33325-288">No aplicable</span><span class="sxs-lookup"><span data-stu-id="33325-288">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33325-289">Vendes facturades</span><span class="sxs-lookup"><span data-stu-id="33325-289">Billed sales</span></span></td>
<td><span data-ttu-id="33325-290">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="33325-290">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="33325-291">Es confirma una factura, i es produeix una disminució de les hores facturables.</span><span class="sxs-lookup"><span data-stu-id="33325-291">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="33325-292">Reversió de vendes no facturades</span><span class="sxs-lookup"><span data-stu-id="33325-292">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="33325-293">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="33325-293">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="33325-294">No aplicable</span><span class="sxs-lookup"><span data-stu-id="33325-294">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="33325-295">No aplicable</span><span class="sxs-lookup"><span data-stu-id="33325-295">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="33325-296">No aplicable</span><span class="sxs-lookup"><span data-stu-id="33325-296">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="33325-297">No aplicable</span><span class="sxs-lookup"><span data-stu-id="33325-297">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33325-298">Vendes facturades - Imputable per a la nova quantitat</span><span class="sxs-lookup"><span data-stu-id="33325-298">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="33325-299">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="33325-299">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33325-300">Vendes facturades - No imputable per la diferència</span><span class="sxs-lookup"><span data-stu-id="33325-300">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="33325-301">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="33325-301">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="33325-302">Una factura es corregeix per augmentar la quantitat imputable.</span><span class="sxs-lookup"><span data-stu-id="33325-302">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="33325-303">Vendes facturades - Reversió</span><span class="sxs-lookup"><span data-stu-id="33325-303">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="33325-304">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="33325-304">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="33325-305">Reversió de vendes facturades per fita</span><span class="sxs-lookup"><span data-stu-id="33325-305">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="33325-306">Canvi en l'estat de la fita de <strong>Facturada</strong> a <strong>Llesta per facturar</strong></span><span class="sxs-lookup"><span data-stu-id="33325-306">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="33325-307">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="33325-307">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="33325-308">No aplicable</span><span class="sxs-lookup"><span data-stu-id="33325-308">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="33325-309">No aplicable</span><span class="sxs-lookup"><span data-stu-id="33325-309">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33325-310">Vendes facturades</span><span class="sxs-lookup"><span data-stu-id="33325-310">Billed sales</span></span></td>
<td><span data-ttu-id="33325-311">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="33325-311">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="33325-312">Una factura es corregeix per reduir la quantitat imputable.</span><span class="sxs-lookup"><span data-stu-id="33325-312">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="33325-313">Vendes facturades - Reversió</span><span class="sxs-lookup"><span data-stu-id="33325-313">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="33325-314">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="33325-314">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33325-315">Vendes facturades per a la nova quantitat</span><span class="sxs-lookup"><span data-stu-id="33325-315">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="33325-316">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="33325-316">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33325-317">Vendes no facturades - Imputable per la diferència</span><span class="sxs-lookup"><span data-stu-id="33325-317">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="33325-318">Moneda del contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="33325-318">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
