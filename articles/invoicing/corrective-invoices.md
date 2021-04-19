---
title: Creació de factures basades en projecte de correcció
description: Aquest tema proporciona informació sobre les factures de correcció a Project Operations.
author: rumant
manager: Annbe
ms.date: 03/29/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 32772d64b3fc77f0af9618edff40e3b295593454
ms.sourcegitcommit: 504c09365bf404c1f1aa9b5034c1e1e5bc9d0d54
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 03/31/2021
ms.locfileid: "5788834"
---
# <a name="create-corrective-project-based-invoices"></a><span data-ttu-id="48623-103">Creació de factures basades en projecte de correcció</span><span class="sxs-lookup"><span data-stu-id="48623-103">Create corrective project-based invoices</span></span> 

<span data-ttu-id="48623-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_</span><span class="sxs-lookup"><span data-stu-id="48623-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="48623-105">Una factura confirmada del projecte es pot corregir per processar canvis o crèdits com s'hagin negociat amb el client i l'administrador del projecte.</span><span class="sxs-lookup"><span data-stu-id="48623-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="48623-106">Per fer modificacions a una factura confirmada, obriu la factura confirmada i seleccioneu **Corregeix aquesta factura**.</span><span class="sxs-lookup"><span data-stu-id="48623-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="48623-107">Aquesta selecció no està disponible tret que es confirmi una factura de projecte.</span><span class="sxs-lookup"><span data-stu-id="48623-107">This selection isn't available unless a project invoice is confirmed.</span></span>

<span data-ttu-id="48623-108">Es crea un nou esborrany de factura a partir de la factura confirmada.</span><span class="sxs-lookup"><span data-stu-id="48623-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="48623-109">Tots els detalls de la línia de factura de la factura confirmada anteriorment es copien al nou esborrany.</span><span class="sxs-lookup"><span data-stu-id="48623-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="48623-110">Els següents són alguns aspectes clau per ajudar-vos a entendre millor els detalls de la línia sobre la nova factura de correcció:</span><span class="sxs-lookup"><span data-stu-id="48623-110">The following are some key points to help you understand more about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="48623-111">Totes les quantitats s'actualitzen a zero.</span><span class="sxs-lookup"><span data-stu-id="48623-111">All quantities are updated to zero.</span></span> <span data-ttu-id="48623-112">Se suposa que tots els elements facturats s'abonen totalment.</span><span class="sxs-lookup"><span data-stu-id="48623-112">This assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="48623-113">Si cal, podeu actualitzar manualment aquestes quantitats per reflectir la quantitat que s'està facturant i no la quantitat que s'està acreditant.</span><span class="sxs-lookup"><span data-stu-id="48623-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="48623-114">Segons la quantitat que introduïu, l'aplicació calcula la quantitat acreditada.</span><span class="sxs-lookup"><span data-stu-id="48623-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="48623-115">Aquesta quantitat es reflecteix en els valor reals que es creen quan es confirma la factura corregida.</span><span class="sxs-lookup"><span data-stu-id="48623-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="48623-116">Si s'introdueixen canvis en l'import de l'impost, s'ha d'introduir l'import de l'impost correcte i no l'import de l'impost que s'ha acreditat.</span><span class="sxs-lookup"><span data-stu-id="48623-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="48623-117">Les correccions de fites sempre es processen com a crèdits complets.</span><span class="sxs-lookup"><span data-stu-id="48623-117">Milestone corrections are always processed as full credits.</span></span>
- <span data-ttu-id="48623-118">Es poden corregir els imports de bestreta o d'avançament si s'ha facturat al client un import incorrecte.</span><span class="sxs-lookup"><span data-stu-id="48623-118">Retainer or advance amounts can be corrected if the customer was invoiced for an incorrect amount.</span></span>
- <span data-ttu-id="48623-119">Les conciliacions de retencions i avançaments es poden corregir si s'ha utilitzat un import incorrecte per conciliar els càrrecs d'una factura confirmada prèviament.</span><span class="sxs-lookup"><span data-stu-id="48623-119">Reconciliations of retainers and advances can be corrected if an incorrect amount was used to reconcile against the charges on a previously confirmed invoice.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="48623-120">Els detalls de la línia de factura que són correccions a altres càrrecs ja facturats tenen el camp **Correcció** definit com a **Sí**.</span><span class="sxs-lookup"><span data-stu-id="48623-120">Invoice line details that are corrections to other already invoiced charges have the **Correction** field set to **Yes**.</span></span> <span data-ttu-id="48623-121">Les factures que han corregit els detalls de la línia de factura tenen un camp anomenat **Té correccions** que també s'estableix a **Sí**.</span><span class="sxs-lookup"><span data-stu-id="48623-121">Invoices that have corrected invoice line details have a field called **Has corrections** that is also set to **Yes**.</span></span>

## <a name="actuals-created-on-confirmation-of-a-corrective-invoice"></a><span data-ttu-id="48623-122">Valors reals creats a la confirmació d'una factura correctiva</span><span class="sxs-lookup"><span data-stu-id="48623-122">Actuals created on confirmation of a corrective invoice</span></span>

<span data-ttu-id="48623-123">A la taula següent es mostraran els valors reals que es creen quan es confirma una factura correctiva.</span><span class="sxs-lookup"><span data-stu-id="48623-123">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="48623-124">
                    <strong>Escenari</strong>
                </span><span class="sxs-lookup"><span data-stu-id="48623-124">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="48623-125">
                    <strong>Valors reals creats en la confirmació</strong>
                </span><span class="sxs-lookup"><span data-stu-id="48623-125">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="48623-126">Confirmeu la correcció d'un avançament o bestreta facturat.<strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="48623-126">Confirm the correction of an invoiced advance or retainer.<strong></strong>
                </span></span></p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="48623-127">Reversió de vendes no facturada de la bestreta o avançament creat per a la conciliació.</span><span class="sxs-lookup"><span data-stu-id="48623-127">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="48623-128">Aquest import és positiu perquè està destinada a cancel·lar el negatiu creat quan es va facturar la bestreta o avançament.</span><span class="sxs-lookup"><span data-stu-id="48623-128">This amount is positive because it is meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="48623-129">Es crea un valor real de reversió de vendes facturades per l'import de la bestreta o l'avançament per revertir les vendes facturades originals.</span><span class="sxs-lookup"><span data-stu-id="48623-129">A billed sales reversal actual is created for the amount on the retainer or advance to reverse the original billed sales.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="48623-130">Es crea un nou valor real de vendes facturades per a l'import corregit en la línia de factura corregida basada en una bestreta o avançament.</span><span class="sxs-lookup"><span data-stu-id="48623-130">A new billed sales actual is created for the corrected amount on the retainer or advance-based corrected invoice line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="48623-131">Valor real de venda no facturada de l'import negatiu de la línia de factura corregida basada en una bestreta o avançament que s'utilitzarà per a la conciliació.</span><span class="sxs-lookup"><span data-stu-id="48623-131">An unbilled sales actual of negative amount of the retainer or advance-based corrected invoice line, which will be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="48623-132">Confirmació de la correcció d'una bestreta o avançament conciliat prèviament.</span><span class="sxs-lookup"><span data-stu-id="48623-132">A confirmation of the correction of a previously reconciled retainer or advance.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="48623-133">Reversió de vendes no facturada de la bestreta o avançament creat per a la conciliació.</span><span class="sxs-lookup"><span data-stu-id="48623-133">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="48623-134">Aquest import és positiu i està destinada a cancel·lar el negatiu creat quan es va crear la conciliació anterior.</span><span class="sxs-lookup"><span data-stu-id="48623-134">This amount is positive and is meant to cancel out the negative that was created when the previous reconciliation occurred.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="48623-135">Valor real de reversió de vendes facturades per l'import de la factura anterior.</span><span class="sxs-lookup"><span data-stu-id="48623-135">A billed sales reversal actual for the amount on the previous invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="48623-136">Nou valor real de vendes facturades per a l'import de bestreta corregit que s'aplica a la factura corregida.</span><span class="sxs-lookup"><span data-stu-id="48623-136">A new billed sales actual for the corrected retainer amount that is applied on the corrected invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="48623-137">Valor real de venda no facturada amb un import negatiu de la bestreta o avançament restant corregir que s'utilitzarà per a la conciliació en factures posteriors.</span><span class="sxs-lookup"><span data-stu-id="48623-137">An unbilled sales actual with a negative amount from the corrected leftover retainer or advance, which will be used for reconciliation on later invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="48623-138">Facturació del crèdit complet d'una transacció de temps facturada prèviament.</span><span class="sxs-lookup"><span data-stu-id="48623-138">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="48623-139">Reversió de vendes facturades per les hores i l'import en el detall de la línia de factura original per al temps.</span><span class="sxs-lookup"><span data-stu-id="48623-139">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="48623-140">Nou valor real de vendes no facturades per les hores i l'import en el detall de la línia de factura original per al temps.</span><span class="sxs-lookup"><span data-stu-id="48623-140">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="48623-141">Facturació del crèdit parcial en una transacció de temps.</span><span class="sxs-lookup"><span data-stu-id="48623-141">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="48623-142">Reversió de vendes facturades per les hores i l'import facturat en el detall de la línia de factura original per al temps.</span><span class="sxs-lookup"><span data-stu-id="48623-142">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="48623-143">Nou valor real de venda no facturada imputable per les hores i l'import en el detall de la línia de factura editada, reversió d'això i valor real de venda facturada equivalent.</span><span class="sxs-lookup"><span data-stu-id="48623-143">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="48623-144">Nou valor real de venda no facturada imputable per les hores restants i import després de deduir les xifres corregides en el detall de la línia de factura.</span><span class="sxs-lookup"><span data-stu-id="48623-144">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="48623-145">Facturació del crèdit complet d'una transacció de despeses facturada prèviament.</span><span class="sxs-lookup"><span data-stu-id="48623-145">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="48623-146">Reversió de vendes facturades per la quantitat i l'import en el detall de la línia de factura original per a la despesa.</span><span class="sxs-lookup"><span data-stu-id="48623-146">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="48623-147">Nou valor real de vendes sense facturar per la quantitat i l'import en el detall de la línia de factura original per a la despesa.</span><span class="sxs-lookup"><span data-stu-id="48623-147">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="48623-148">Facturació del crèdit parcial d'una transacció de despeses facturada prèviament.</span><span class="sxs-lookup"><span data-stu-id="48623-148">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="48623-149">Reversió de vendes facturades per la quantitat i l'import facturat en el detall de la línia de factura original per a una despesa.</span><span class="sxs-lookup"><span data-stu-id="48623-149">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="48623-150">Nou valor real de venda no facturada imputable per la quantitat i l'import en el detall de la línia de factura corregida, reversió d'això i valor real de venda facturada equivalent.</span><span class="sxs-lookup"><span data-stu-id="48623-150">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="48623-151">Nou valor real de venda no facturada imputable per la quantitat restant i import després de deduir les xifres corregides en el detall de la línia de factura.</span><span class="sxs-lookup"><span data-stu-id="48623-151">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="48623-152">Facturació del crèdit complet d'una transacció d'impostos facturada prèviament.</span><span class="sxs-lookup"><span data-stu-id="48623-152">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="48623-153">Reversió de vendes facturades per la quantitat i l'import en el detall de la línia de factura original per a l'impost.</span><span class="sxs-lookup"><span data-stu-id="48623-153">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="48623-154">Nou valor real de vendes sense facturar per la quantitat i l'import en el detall de la línia de factura original per a l'impost.</span><span class="sxs-lookup"><span data-stu-id="48623-154">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="48623-155">Facturació del crèdit parcial d'una transacció d'impostos facturada prèviament.</span><span class="sxs-lookup"><span data-stu-id="48623-155">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="48623-156">Reversió de vendes facturades per la quantitat i l'import facturat en el detall de la línia de factura original per a l'impost.</span><span class="sxs-lookup"><span data-stu-id="48623-156">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="48623-157">Nou valor real de venda no facturada imputable per la quantitat i l'import en el detall de la línia de factura correctiva editada, reversió d'això i valor real de venda facturada equivalent.</span><span class="sxs-lookup"><span data-stu-id="48623-157">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="48623-158">Facturació del crèdit complet d'una fita facturada prèviament.</span><span class="sxs-lookup"><span data-stu-id="48623-158">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="48623-159">Reversió de vendes facturades per l'import en el detall de la línia de factura original per a la fita.</span><span class="sxs-lookup"><span data-stu-id="48623-159">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="48623-160">L'estat de la factura a la fita s'actualitza des de <b>Factura del client publicada</b> a <b>Preparat per a la factura</b>.</span><span class="sxs-lookup"><span data-stu-id="48623-160">The invoice status on the milestone is updated from <b>Customer invoice posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="48623-161">Facturació del crèdit parcial d'una fita facturada prèviament.</span><span class="sxs-lookup"><span data-stu-id="48623-161">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="48623-162">No admesos</span><span class="sxs-lookup"><span data-stu-id="48623-162">Unsupported</span></span> </p>
            </td>
        </tr>        
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
