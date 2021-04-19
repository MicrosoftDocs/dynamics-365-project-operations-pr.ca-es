---
title: Confirmació d'una factura de projecte proforma
description: Aquest tema proporciona informació sobre la confirmació de factures de projecte proforma a Project Operations.
author: rumant
manager: Annbe
ms.date: 04/05/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 144c1b6a49951af8be0c619f41808e7617e59c92
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/07/2021
ms.locfileid: "5867074"
---
# <a name="confirm-a-proforma-project-invoice"></a><span data-ttu-id="e1100-103">Confirmació d'una factura de projecte proforma</span><span class="sxs-lookup"><span data-stu-id="e1100-103">Confirm a proforma project invoice</span></span> 

<span data-ttu-id="e1100-104">_**S'aplica a:** implementació bàsica: tracte de facturació proforma_</span><span class="sxs-lookup"><span data-stu-id="e1100-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="e1100-105">Després que es confirmi una factura proforma, l'estat de la factura del projecte s'actualitza a **Confirmada**.</span><span class="sxs-lookup"><span data-stu-id="e1100-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="e1100-106">Quan es confirma una factura, es converteix en només de lectura.</span><span class="sxs-lookup"><span data-stu-id="e1100-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="e1100-107">Més endavant, la factura només es pot corregir si hi ha correccions o abonaments iniciats pels clients.</span><span class="sxs-lookup"><span data-stu-id="e1100-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits.</span></span>

<span data-ttu-id="e1100-108">La taula següent enumera els valors reals creats pel sistema.</span><span class="sxs-lookup"><span data-stu-id="e1100-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="e1100-109">Aquests valors reals es creen quan es realitzen certes operacions sobre l'esborrany de la factura del projecte abans de confirmar-la.</span><span class="sxs-lookup"><span data-stu-id="e1100-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="e1100-110">
                    <strong>Escenari</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e1100-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="e1100-111">
                    <strong>Valors reals creats en la confirmació</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e1100-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e1100-112">Facturació d'un avançament o bestreta</span><span class="sxs-lookup"><span data-stu-id="e1100-112">Invoicing an advance or retainer</span></span> </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e1100-113">Una valor real de vendes facturades del tipus <strong>Bestreta</strong> es crea per a l'import de l'avançament o bestreta.</span><span class="sxs-lookup"><span data-stu-id="e1100-113">A billed sales actual of type, <strong>Retainer</strong> is created for the amount on the advance or retainer.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e1100-114">Valor real de venda no facturada de l'import negatiu de la bestreta o avançament que s'utilitzarà per a la conciliació.</span><span class="sxs-lookup"><span data-stu-id="e1100-114">An unbilled sales actual of a negative amount of the retainer or advance to be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e1100-115">Després de reconciliar completament una bestreta o avançament en una factura.</span><span class="sxs-lookup"><span data-stu-id="e1100-115">After fully reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e1100-116">Reversió de vendes no facturada de la bestreta o avançament creat per a la conciliació.</span><span class="sxs-lookup"><span data-stu-id="e1100-116">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="e1100-117">Aquest import és positiu perquè està destinada a cancel·lar el negatiu creat quan es va facturar la bestreta o avançament.</span><span class="sxs-lookup"><span data-stu-id="e1100-117">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e1100-118">Valor real de vendes facturades per l'import d'aquesta factura.</span><span class="sxs-lookup"><span data-stu-id="e1100-118">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="e1100-119">Després de reconciliar parcialment una bestreta o avançament en una factura.</span><span class="sxs-lookup"><span data-stu-id="e1100-119">After partially reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e1100-120">Reversió de vendes no facturada de la bestreta o avançament creat per a la conciliació.</span><span class="sxs-lookup"><span data-stu-id="e1100-120">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="e1100-121">Aquest import és positiu perquè està destinada a cancel·lar el negatiu creat quan es va facturar la bestreta o avançament.</span><span class="sxs-lookup"><span data-stu-id="e1100-121">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e1100-122">Valor real de vendes facturades per l'import d'aquesta factura.</span><span class="sxs-lookup"><span data-stu-id="e1100-122">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e1100-123">Valor real de venda no facturada negatiu de l'import de la bestreta o avançament restant que s'utilitzarà per a factures futures.</span><span class="sxs-lookup"><span data-stu-id="e1100-123">A negative unbilled sales actual of the remaining retainer or advance amount to be used for reconciliation on future invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e1100-124">Facturar una transacció de temps sense cap modificació a l'esborrany de factura.</span><span class="sxs-lookup"><span data-stu-id="e1100-124">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e1100-125">Reversió de vendes no facturades per les hores i l'import en l'aprovació de temps original.</span><span class="sxs-lookup"><span data-stu-id="e1100-125">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e1100-126">Valor real de venda facturada per les hores i quantitat en l'aprovació de temps original.</span><span class="sxs-lookup"><span data-stu-id="e1100-126">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="e1100-127">Facturació d'una transacció de temps editada per reduir la quantitat.</span><span class="sxs-lookup"><span data-stu-id="e1100-127">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e1100-128">Reversió de vendes no facturades per les hores i l'import en l'aprovació de temps original.</span><span class="sxs-lookup"><span data-stu-id="e1100-128">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e1100-129">Nou valor real de venda no facturada imputable per les hores i l'import en el detall de la línia de factura editada, reversió del valor real de venda i valor real de venda facturada equivalent.</span><span class="sxs-lookup"><span data-stu-id="e1100-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e1100-130">Nou valor real de venda no facturada no imputable per les hores i l'import restants després de deduir les xifres corregides en el detall de la línia de factura editada, reversió del valor real de venda i valor real de venda facturada equivalent.</span><span class="sxs-lookup"><span data-stu-id="e1100-130">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e1100-131">Facturació d'una transacció de temps editada per augmentar la quantitat.</span><span class="sxs-lookup"><span data-stu-id="e1100-131">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e1100-132">Reversió de vendes no facturades per les hores i l'import en l'aprovació de temps original.</span><span class="sxs-lookup"><span data-stu-id="e1100-132">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e1100-133">Nou valor real de venda no facturada imputable per les hores i l'import en el detall de la línia de factura editada, reversió del valor real de venda sense facturar i valor real de venda facturada equivalent.</span><span class="sxs-lookup"><span data-stu-id="e1100-133">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e1100-134">Facturar una transacció de despeses sense cap modificació a l'esborrany de factura.</span><span class="sxs-lookup"><span data-stu-id="e1100-134">Invoicing an expense transaction without any edits on draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e1100-135">Reversió de vendes sense facturar per la quantitat i quantitat en l'aprovació de despeses original.</span><span class="sxs-lookup"><span data-stu-id="e1100-135">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e1100-136">Valor real de venda facturada per la quantitat i quantitat en l'aprovació de despeses original</span><span class="sxs-lookup"><span data-stu-id="e1100-136">A billed sales actual for the quantity and amount on the original expense approval</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="e1100-137">Facturació d'una transacció de despesa editada per reduir la quantitat.</span><span class="sxs-lookup"><span data-stu-id="e1100-137">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e1100-138">Reversió de vendes sense facturar per la quantitat i quantitat en l'aprovació de despeses original.</span><span class="sxs-lookup"><span data-stu-id="e1100-138">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e1100-139">Nou valor real de venda no facturada imputable per a la quantitat i l'import en el detall de la línia de factura editada, reversió del valor real de venda no facturada i valor real de venda facturada equivalent.</span><span class="sxs-lookup"><span data-stu-id="e1100-139">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e1100-140">Nou valor real de venda no facturada no imputable per a la quantitat i l'import restants després de deduir les xifres corregides en el detall de la línia de factura editada, reversió del valor real de venda sense facturar i valor real de venda facturada equivalent.</span><span class="sxs-lookup"><span data-stu-id="e1100-140">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e1100-141">Facturació d'una transacció de despesa editada per augmentar la quantitat.</span><span class="sxs-lookup"><span data-stu-id="e1100-141">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e1100-142">Reversió de vendes sense facturar per la quantitat i quantitat en l'aprovació de despeses original.</span><span class="sxs-lookup"><span data-stu-id="e1100-142">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e1100-143">Nou valor real de venda no facturada imputable per a la quantitat i l'import en el detall de la línia de factura editada, reversió del valor real de venda no facturada i valor real de venda facturada equivalent.</span><span class="sxs-lookup"><span data-stu-id="e1100-143">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e1100-144">Facturar una transacció de material sense edicions a l'esborrany de la factura.</span><span class="sxs-lookup"><span data-stu-id="e1100-144">Invoicing a material transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e1100-145">Una reversió de vendes no facturades per a la quantitat i l'import a la aprovació d'ús de materials original.</span><span class="sxs-lookup"><span data-stu-id="e1100-145">An unbilled sales reversal for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e1100-146">Un valor real de vendes facturades per a la quantitat i l'import a la aprovació d'ús de materials original.</span><span class="sxs-lookup"><span data-stu-id="e1100-146">A billed sales actual for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="e1100-147">Facturació d'una transacció de materials que s'ha editat per reduir la quantitat.</span><span class="sxs-lookup"><span data-stu-id="e1100-147">Invoicing a material transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e1100-148">Una reversió de vendes no facturades per a la quantitat i l'import a la aprovació de temps original.</span><span class="sxs-lookup"><span data-stu-id="e1100-148">An unbilled sales reversal for the quantity and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e1100-149">Nou valor real de venda no facturada imputable per a la quantitat i l'import en el detall de la línia de factura editada, reversió del valor real de venda no facturada i valor real de venda facturada equivalent.</span><span class="sxs-lookup"><span data-stu-id="e1100-149">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e1100-150">Nou valor real de venda no facturada no imputable per a la quantitat i l'import restants després de deduir les xifres corregides en el detall de la línia de factura editada, reversió del valor real de venda sense facturar i valor real de venda facturada equivalent.</span><span class="sxs-lookup"><span data-stu-id="e1100-150">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e1100-151">Facturació d'una transacció de materials que s'ha editat per augmentar la quantitat.</span><span class="sxs-lookup"><span data-stu-id="e1100-151">Invoicing a material transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e1100-152">Una reversió de vendes no facturades per a la quantitat i l'import a la aprovació d'ús de materials original.</span><span class="sxs-lookup"><span data-stu-id="e1100-152">An unbilled sales reversal for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e1100-153">Nou valor real de venda no facturada imputable per a la quantitat i l'import en el detall de la línia de factura editada, reversió del valor real de venda no facturada i valor real de venda facturada equivalent.</span><span class="sxs-lookup"><span data-stu-id="e1100-153">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e1100-154">Facturació d'una tarifa.</span><span class="sxs-lookup"><span data-stu-id="e1100-154">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e1100-155">Reversió de vendes no facturades per a l'import de la taxa en la línia del llibre diari original.</span><span class="sxs-lookup"><span data-stu-id="e1100-155">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e1100-156">Valor real de venda facturada per la quantitat i quantitat en la línia del llibre diari de taxa original.</span><span class="sxs-lookup"><span data-stu-id="e1100-156">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="e1100-157">Facturació d'una fita.</span><span class="sxs-lookup"><span data-stu-id="e1100-157">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e1100-158">Valor real de vendes facturades per l'import de la fita a la fita original a la línia de contracte del projecte.</span><span class="sxs-lookup"><span data-stu-id="e1100-158">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="e1100-159">Facturar una línia de contracte basada en productes.</span><span class="sxs-lookup"><span data-stu-id="e1100-159">Invoicing a product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e1100-160">Valor real de venda facturada per a la línia de producte amb la quantitat i quantitat provinents de la línia de contracte basada en el producte.</span><span class="sxs-lookup"><span data-stu-id="e1100-160">A billed sales actual for the product line with the quantity and amount coming from the product-based contract line.</span></span>
                </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
