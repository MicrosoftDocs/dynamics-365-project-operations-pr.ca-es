---
title: Factures de projecte de correcció
description: Aquest tema proporciona informació sobre com crear i confirmar factures de projecte de correcció a Project Operations.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: dfa5535597ee6e144259c9246b33075f3492285e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004069"
---
# <a name="corrective-project-invoices"></a><span data-ttu-id="c4507-103">Factures de projecte de correcció</span><span class="sxs-lookup"><span data-stu-id="c4507-103">Corrective project invoices</span></span>

<span data-ttu-id="c4507-104">_**S'aplica a:** implementació bàsica: tracte de facturació proforma_</span><span class="sxs-lookup"><span data-stu-id="c4507-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="c4507-105">Una factura confirmada del projecte es pot corregir per processar canvis o crèdits com s'hagin negociat amb el client i l'administrador del projecte.</span><span class="sxs-lookup"><span data-stu-id="c4507-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="c4507-106">Per fer modificacions a una factura confirmada, obriu la factura confirmada i seleccioneu **Corregeix aquesta factura**.</span><span class="sxs-lookup"><span data-stu-id="c4507-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="c4507-107">Aquesta selecció no està disponible tret que es confirmi una factura de projecte.</span><span class="sxs-lookup"><span data-stu-id="c4507-107">This selection isn't available unless a project invoice is confirmed.</span></span>

<span data-ttu-id="c4507-108">Es crea un nou esborrany de factura a partir de la factura confirmada.</span><span class="sxs-lookup"><span data-stu-id="c4507-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="c4507-109">Tots els detalls de la línia de factura de la factura confirmada anteriorment es copien al nou esborrany.</span><span class="sxs-lookup"><span data-stu-id="c4507-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="c4507-110">Els següents són alguns dels punts clau per entendre els detalls de la línia sobre la nova factura corregida:</span><span class="sxs-lookup"><span data-stu-id="c4507-110">The following are some of the key points to understand about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="c4507-111">Totes les quantitats s'actualitzen a zero.</span><span class="sxs-lookup"><span data-stu-id="c4507-111">All quantities are updated to zero.</span></span> <span data-ttu-id="c4507-112">L'aplicació assumeix que tots els elements facturats estan completament acreditats.</span><span class="sxs-lookup"><span data-stu-id="c4507-112">The application assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="c4507-113">Si cal, podeu actualitzar manualment aquestes quantitats per reflectir la quantitat que s'està facturant i no la quantitat que s'està acreditant.</span><span class="sxs-lookup"><span data-stu-id="c4507-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="c4507-114">Segons la quantitat que introduïu, l'aplicació calcula la quantitat acreditada.</span><span class="sxs-lookup"><span data-stu-id="c4507-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="c4507-115">Aquesta quantitat es reflecteix en els valor reals que es creen quan es confirma la factura corregida.</span><span class="sxs-lookup"><span data-stu-id="c4507-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="c4507-116">Si s'introdueixen canvis en l'import de l'impost, s'ha d'introduir l'import de l'impost correcte i no l'import de l'impost que s'ha acreditat.</span><span class="sxs-lookup"><span data-stu-id="c4507-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="c4507-117">Les línies de contracte basades en productes confirmades prèviament no es copien.</span><span class="sxs-lookup"><span data-stu-id="c4507-117">Previously confirmed product-based contract lines are not copied over.</span></span> <span data-ttu-id="c4507-118">No s'admet el processament de correccions en una factura de projecte basada en productes.</span><span class="sxs-lookup"><span data-stu-id="c4507-118">Processing corrections on a product-based project invoice is not supported.</span></span>
- <span data-ttu-id="c4507-119">Les correccions de fites sempre es processen com a crèdits complets.</span><span class="sxs-lookup"><span data-stu-id="c4507-119">Milestone corrections are always processed as full credits.</span></span>
- <span data-ttu-id="c4507-120">Es poden corregir els imports de bestreta o d'avançament si s'ha facturat al client un import incorrecte.</span><span class="sxs-lookup"><span data-stu-id="c4507-120">Retainer or advance amounts can be corrected if the customer was invoiced for an incorrect amount.</span></span>
- <span data-ttu-id="c4507-121">Les conciliacions de retencions i avançaments es poden corregir si s'ha utilitzat un import incorrecte per conciliar els càrrecs d'una factura confirmada prèviament.</span><span class="sxs-lookup"><span data-stu-id="c4507-121">Reconciliations of retainers and advances can be corrected if an incorrect amount was used to reconcile against the charges on a previously confirmed invoice.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c4507-122">Els detalls de la línia de factura que són correccions a altres càrrecs ja facturat tenen el camp **Correcció** establert a **Sí**.</span><span class="sxs-lookup"><span data-stu-id="c4507-122">Invoice line details that are corrections to other already invoiced charges have the field **Correction** set to **Yes**.</span></span> <span data-ttu-id="c4507-123">Les factures que han corregit els detalls de la línia de factura tenen un camp anomenat **Té correccions** que també s'estableix a **Sí**.</span><span class="sxs-lookup"><span data-stu-id="c4507-123">Invoices that have corrected invoice line details have a field called **Has corrections** that is also set to **Yes**.</span></span>

## <a name="actuals-created-when-a-corrective-invoice-is-confirmed"></a><span data-ttu-id="c4507-124">Valors reals creats quan es confirma una factura de correcció</span><span class="sxs-lookup"><span data-stu-id="c4507-124">Actuals created when a corrective invoice is confirmed</span></span>

<span data-ttu-id="c4507-125">A la taula següent es mostraran els valors reals que es creen quan es confirma una factura correctiva.</span><span class="sxs-lookup"><span data-stu-id="c4507-125">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="c4507-126">
                    <strong>Escenari</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c4507-126">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="c4507-127">
                    <strong>Valors reals creats en la confirmació</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c4507-127">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="c4507-128">Confirmeu la correcció d'un avançament o bestreta facturat.<strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="c4507-128">Confirm the correction of an invoiced advance or retainer.<strong></strong>
                </span></span></p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c4507-129">Reversió de vendes no facturada de la bestreta o avançament creat per a la conciliació.</span><span class="sxs-lookup"><span data-stu-id="c4507-129">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="c4507-130">Aquest import és positiu perquè està destinada a cancel·lar el negatiu creat quan es va facturar la bestreta o avançament.</span><span class="sxs-lookup"><span data-stu-id="c4507-130">This amount is positive because it is meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c4507-131">Es crea un valor real de reversió de vendes facturades per l'import de la bestreta o l'avançament per revertir les vendes facturades originals.</span><span class="sxs-lookup"><span data-stu-id="c4507-131">A billed sales reversal actual is created for the amount on the retainer or advance to reverse the original billed sales.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c4507-132">Es crea un nou valor real de vendes facturades per a l'import corregit en la línia de factura corregida basada en una bestreta o avançament.</span><span class="sxs-lookup"><span data-stu-id="c4507-132">A new billed sales actual is created for the corrected amount on the retainer or advance-based corrected invoice line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c4507-133">Valor real de venda no facturada de l'import negatiu de la línia de factura corregida basada en una bestreta o avançament que s'utilitzarà per a la conciliació.</span><span class="sxs-lookup"><span data-stu-id="c4507-133">An unbilled sales actual of negative amount of the retainer or advance-based corrected invoice line, which will be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="c4507-134">Confirmació de la correcció d'una bestreta o avançament conciliat prèviament.</span><span class="sxs-lookup"><span data-stu-id="c4507-134">A confirmation of the correction of a previously reconciled retainer or advance.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c4507-135">Reversió de vendes no facturada de la bestreta o avançament creat per a la conciliació.</span><span class="sxs-lookup"><span data-stu-id="c4507-135">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="c4507-136">Aquest import és positiu i està destinada a cancel·lar el negatiu creat quan es va crear la conciliació anterior.</span><span class="sxs-lookup"><span data-stu-id="c4507-136">This amount is positive and is meant to cancel out the negative that was created when the previous reconciliation occurred.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c4507-137">Valor real de reversió de vendes facturades per l'import de la factura anterior.</span><span class="sxs-lookup"><span data-stu-id="c4507-137">A billed sales reversal actual for the amount on the previous invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c4507-138">Nou valor real de vendes facturades per a l'import de bestreta corregit que s'aplica a la factura corregida.</span><span class="sxs-lookup"><span data-stu-id="c4507-138">A new billed sales actual for the corrected retainer amount that is applied on the corrected invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c4507-139">Valor real de venda no facturada amb un import negatiu de la bestreta o avançament restant corregir que s'utilitzarà per a la conciliació en factures posteriors.</span><span class="sxs-lookup"><span data-stu-id="c4507-139">An unbilled sales actual with a negative amount from the corrected leftover retainer or advance, which will be used for reconciliation on later invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c4507-140">Facturació del crèdit complet d'una transacció de temps facturada prèviament.</span><span class="sxs-lookup"><span data-stu-id="c4507-140">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c4507-141">Reversió de vendes facturades per les hores i l'import en el detall de la línia de factura original per al temps.</span><span class="sxs-lookup"><span data-stu-id="c4507-141">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c4507-142">Nou valor real de vendes no facturades per les hores i l'import en el detall de la línia de factura original per al temps.</span><span class="sxs-lookup"><span data-stu-id="c4507-142">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="c4507-143">Facturació del crèdit parcial en una transacció de temps.</span><span class="sxs-lookup"><span data-stu-id="c4507-143">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c4507-144">Reversió de vendes facturades per les hores i l'import facturat en el detall de la línia de factura original per al temps.</span><span class="sxs-lookup"><span data-stu-id="c4507-144">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c4507-145">Nou valor real de venda no facturada imputable per les hores i l'import en el detall de la línia de factura editada, reversió d'això i valor real de venda facturada equivalent.</span><span class="sxs-lookup"><span data-stu-id="c4507-145">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c4507-146">Nou valor real de venda no facturada imputable per les hores restants i import després de deduir les xifres corregides en el detall de la línia de factura.</span><span class="sxs-lookup"><span data-stu-id="c4507-146">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c4507-147">Facturació del crèdit complet d'una transacció de despeses facturada prèviament.</span><span class="sxs-lookup"><span data-stu-id="c4507-147">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c4507-148">Reversió de vendes facturades per la quantitat i l'import en el detall de la línia de factura original per a la despesa.</span><span class="sxs-lookup"><span data-stu-id="c4507-148">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c4507-149">Nou valor real de vendes sense facturar per la quantitat i l'import en el detall de la línia de factura original per a la despesa.</span><span class="sxs-lookup"><span data-stu-id="c4507-149">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="c4507-150">Facturació del crèdit parcial d'una transacció de despeses facturada prèviament.</span><span class="sxs-lookup"><span data-stu-id="c4507-150">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c4507-151">Reversió de vendes facturades per la quantitat i l'import facturat en el detall de la línia de factura original per a una despesa.</span><span class="sxs-lookup"><span data-stu-id="c4507-151">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c4507-152">Nou valor real de venda no facturada imputable per la quantitat i l'import en el detall de la línia de factura corregida, reversió d'això i valor real de venda facturada equivalent.</span><span class="sxs-lookup"><span data-stu-id="c4507-152">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c4507-153">Nou valor real de venda no facturada imputable per la quantitat restant i import després de deduir les xifres corregides en el detall de la línia de factura.</span><span class="sxs-lookup"><span data-stu-id="c4507-153">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c4507-154">Facturar el crèdit complet d'una transacció de materials prèviament facturada.</span><span class="sxs-lookup"><span data-stu-id="c4507-154">Invoicing the full credit of a previously invoiced material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c4507-155">Una reversió de vendes facturades per a la quantitat i l'import del detall de línia de factura original per a materials.</span><span class="sxs-lookup"><span data-stu-id="c4507-155">A billed sales reversal for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c4507-156">Un nou valor real de vendes no facturades per a la quantitat i l'import del detall de línia de factura original per a materials.</span><span class="sxs-lookup"><span data-stu-id="c4507-156">A new unbilled sales actual for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="c4507-157">Facturació del crèdit parcial d'una transacció de material.</span><span class="sxs-lookup"><span data-stu-id="c4507-157">Invoicing the partial credit on a material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c4507-158">Una reversió de vendes facturades per a la quantitat i l'import facturats al detall de línia de factura original per a materials.</span><span class="sxs-lookup"><span data-stu-id="c4507-158">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c4507-159">Un nou valor real de vendes no facturades que es poden cobrar per la quantitat i l'import del detall de la línia de factura editat, una reversió d'aquesta i una venda facturada equivalent real.</span><span class="sxs-lookup"><span data-stu-id="c4507-159">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c4507-160">Nou valor real de venda no facturada imputable per la quantitat restant i import després de deduir les xifres corregides en el detall de la línia de factura.</span><span class="sxs-lookup"><span data-stu-id="c4507-160">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c4507-161">Facturació del crèdit complet d'una transacció d'impostos facturada prèviament.</span><span class="sxs-lookup"><span data-stu-id="c4507-161">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c4507-162">Reversió de vendes facturades per la quantitat i l'import en el detall de la línia de factura original per a l'impost.</span><span class="sxs-lookup"><span data-stu-id="c4507-162">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c4507-163">Nou valor real de vendes sense facturar per la quantitat i l'import en el detall de la línia de factura original per a l'impost.</span><span class="sxs-lookup"><span data-stu-id="c4507-163">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c4507-164">Facturació del crèdit parcial d'una transacció d'impostos facturada prèviament.</span><span class="sxs-lookup"><span data-stu-id="c4507-164">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c4507-165">Reversió de vendes facturades per la quantitat i l'import facturat en el detall de la línia de factura original per a l'impost.</span><span class="sxs-lookup"><span data-stu-id="c4507-165">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c4507-166">Nou valor real de venda no facturada imputable per la quantitat i l'import en el detall de la línia de factura correctiva editada, reversió d'això i valor real de venda facturada equivalent.</span><span class="sxs-lookup"><span data-stu-id="c4507-166">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="c4507-167">Facturació del crèdit complet d'una fita facturada prèviament.</span><span class="sxs-lookup"><span data-stu-id="c4507-167">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c4507-168">Reversió de vendes facturades per l'import en el detall de la línia de factura original per a la fita.</span><span class="sxs-lookup"><span data-stu-id="c4507-168">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="c4507-169">L'estat de la factura de la fita s'actualitza de <b>Factura de client comptabilitzada</b> a <b>Preparat per a facturació</b>.</span><span class="sxs-lookup"><span data-stu-id="c4507-169">The invoice status of the milestone is updated from <b>Customer Invoice Posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="c4507-170">Facturació del crèdit parcial d'una fita facturada prèviament.</span><span class="sxs-lookup"><span data-stu-id="c4507-170">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c4507-171">No admesos</span><span class="sxs-lookup"><span data-stu-id="c4507-171">Unsupported</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="c4507-172">Crèdits i correccions d'una línia de contracte basada en productes facturada prèviament.</span><span class="sxs-lookup"><span data-stu-id="c4507-172">Credits and corrections of a previously invoiced product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="c4507-173">No admesos</span><span class="sxs-lookup"><span data-stu-id="c4507-173">Unsupported</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
