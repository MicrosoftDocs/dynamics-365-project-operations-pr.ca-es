---
title: Factures basades en projecte de correcció
description: Aquest tema proporciona informació sobre com crear i confirmar factures basades en projecte correctives a Project Operations.
author: rumant
manager: Annbe
ms.date: 03/29/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: fc96bb40f5207efc381986d46a3e37dfc1dc111c
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/07/2021
ms.locfileid: "5867029"
---
# <a name="corrective-project-based-invoices"></a><span data-ttu-id="94f3c-103">Factures basades en projecte de correcció</span><span class="sxs-lookup"><span data-stu-id="94f3c-103">Corrective project-based invoices</span></span>

<span data-ttu-id="94f3c-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_</span><span class="sxs-lookup"><span data-stu-id="94f3c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="94f3c-105">Una factura confirmada del projecte es pot corregir per processar canvis o crèdits com s'hagin negociat amb el client i l'administrador del projecte.</span><span class="sxs-lookup"><span data-stu-id="94f3c-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="94f3c-106">Per fer modificacions a una factura confirmada, obriu la factura confirmada i seleccioneu **Corregeix aquesta factura**.</span><span class="sxs-lookup"><span data-stu-id="94f3c-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="94f3c-107">Aquesta selecció no està disponible tret que es confirmi una factura de projecte o si la factura basada en projecte té avançaments o bestretes o retencions o conciliacions d'avançaments o bestretes.</span><span class="sxs-lookup"><span data-stu-id="94f3c-107">This selection isn't available unless a project invoice is confirmed or the project-based invoice has advances or retainers or reconciliations of advances or retainers.</span></span>

<span data-ttu-id="94f3c-108">Es crea un nou esborrany de factura a partir de la factura confirmada.</span><span class="sxs-lookup"><span data-stu-id="94f3c-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="94f3c-109">Tots els detalls de la línia de factura de la factura confirmada anteriorment es copien al nou esborrany.</span><span class="sxs-lookup"><span data-stu-id="94f3c-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="94f3c-110">Els següents són alguns dels punts clau per entendre els detalls de la línia sobre la nova factura corregida:</span><span class="sxs-lookup"><span data-stu-id="94f3c-110">The following are some of the key points to understand about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="94f3c-111">Totes les quantitats s'actualitzen a zero.</span><span class="sxs-lookup"><span data-stu-id="94f3c-111">All quantities are updated to zero.</span></span> <span data-ttu-id="94f3c-112">El Dynamics 365 Project Operations assumeix que tots els elements facturats s'abonen totalment.</span><span class="sxs-lookup"><span data-stu-id="94f3c-112">Dynamics 365 Project Operations assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="94f3c-113">Si cal, podeu actualitzar manualment aquestes quantitats per reflectir la quantitat que s'està facturant i no la quantitat que s'està acreditant.</span><span class="sxs-lookup"><span data-stu-id="94f3c-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="94f3c-114">Segons la quantitat que introduïu, l'aplicació calcula la quantitat acreditada.</span><span class="sxs-lookup"><span data-stu-id="94f3c-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="94f3c-115">Aquesta quantitat es reflecteix en els valor reals que es creen quan es confirma la factura corregida.</span><span class="sxs-lookup"><span data-stu-id="94f3c-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="94f3c-116">Si s'introdueixen canvis en l'import de l'impost, s'ha d'introduir l'import de l'impost correcte i no l'import de l'impost que s'ha acreditat.</span><span class="sxs-lookup"><span data-stu-id="94f3c-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="94f3c-117">Les correccions de fites sempre es processen com a crèdits complets.</span><span class="sxs-lookup"><span data-stu-id="94f3c-117">Milestone corrections are always processed as full credits.</span></span>


> [!IMPORTANT]
> <span data-ttu-id="94f3c-118">Per als detalls de la línia de factura que són correccions a altres càrrecs ja facturats, el camp **Correcció** es defineix com a **Sí**.</span><span class="sxs-lookup"><span data-stu-id="94f3c-118">For invoice line details that are corrections to other already invoiced charges, the **Correction** field is set to **Yes**.</span></span> <span data-ttu-id="94f3c-119">Per a les factures que tenen detalls de línia de factura de correcció, el camp **Té correccions** es defineix com a **Sí**.</span><span class="sxs-lookup"><span data-stu-id="94f3c-119">For invoices that have corrected invoice line details, the **Has corrections** field is set to **Yes**.</span></span>

## <a name="actuals-created-when-a-corrective-invoice-is-confirmed"></a><span data-ttu-id="94f3c-120">Valors reals creats quan es confirma una factura de correcció</span><span class="sxs-lookup"><span data-stu-id="94f3c-120">Actuals created when a corrective invoice is confirmed</span></span>

<span data-ttu-id="94f3c-121">A la taula següent es mostraran els valors reals que es creen quan es confirma una factura correctiva.</span><span class="sxs-lookup"><span data-stu-id="94f3c-121">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="94f3c-122">
                    <strong>Escenari</strong>
                </span><span class="sxs-lookup"><span data-stu-id="94f3c-122">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="94f3c-123">
                    <strong>Valors reals creats en la confirmació</strong>
                </span><span class="sxs-lookup"><span data-stu-id="94f3c-123">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="94f3c-124">Facturació del crèdit complet d'una transacció de temps facturada prèviament.</span><span class="sxs-lookup"><span data-stu-id="94f3c-124">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="94f3c-125">Reversió de vendes facturades per les hores i l'import en el detall de la línia de factura original per al temps.</span><span class="sxs-lookup"><span data-stu-id="94f3c-125">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="94f3c-126">Nou valor real de vendes no facturades per les hores i l'import en el detall de la línia de factura original per al temps.</span><span class="sxs-lookup"><span data-stu-id="94f3c-126">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="94f3c-127">Facturació del crèdit parcial en una transacció de temps.</span><span class="sxs-lookup"><span data-stu-id="94f3c-127">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="94f3c-128">Reversió de vendes facturades per les hores i l'import facturat en el detall de la línia de factura original per al temps.</span><span class="sxs-lookup"><span data-stu-id="94f3c-128">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="94f3c-129">Nou valor real de venda no facturada imputable per les hores i l'import en el detall de la línia de factura editada, reversió d'això i valor real de venda facturada equivalent.</span><span class="sxs-lookup"><span data-stu-id="94f3c-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="94f3c-130">Nou valor real de venda no facturada imputable per les hores restants i import després de deduir les xifres corregides en el detall de la línia de factura.</span><span class="sxs-lookup"><span data-stu-id="94f3c-130">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="94f3c-131">Facturació del crèdit complet d'una transacció de despeses facturada prèviament.</span><span class="sxs-lookup"><span data-stu-id="94f3c-131">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="94f3c-132">Reversió de vendes facturades per la quantitat i l'import en el detall de la línia de factura original per a la despesa.</span><span class="sxs-lookup"><span data-stu-id="94f3c-132">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="94f3c-133">Nou valor real de vendes sense facturar per la quantitat i l'import en el detall de la línia de factura original per a la despesa.</span><span class="sxs-lookup"><span data-stu-id="94f3c-133">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="94f3c-134">Facturació del crèdit parcial d'una transacció de despeses facturada prèviament.</span><span class="sxs-lookup"><span data-stu-id="94f3c-134">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="94f3c-135">Reversió de vendes facturades per la quantitat i l'import facturat en el detall de la línia de factura original per a una despesa.</span><span class="sxs-lookup"><span data-stu-id="94f3c-135">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="94f3c-136">Nou valor real de venda no facturada imputable per la quantitat i l'import en el detall de la línia de factura corregida, reversió d'això i valor real de venda facturada equivalent.</span><span class="sxs-lookup"><span data-stu-id="94f3c-136">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="94f3c-137">Nou valor real de venda no facturada imputable per la quantitat restant i import després de deduir les xifres corregides en el detall de la línia de factura.</span><span class="sxs-lookup"><span data-stu-id="94f3c-137">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
                <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="94f3c-138">Facturar el crèdit complet d'una transacció de materials prèviament facturada.</span><span class="sxs-lookup"><span data-stu-id="94f3c-138">Invoicing the full credit of a previously invoiced material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="94f3c-139">Una reversió de vendes facturades per a la quantitat i l'import del detall de línia de factura original per a materials.</span><span class="sxs-lookup"><span data-stu-id="94f3c-139">A billed sales reversal for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="94f3c-140">Un nou valor real de vendes no facturades per a la quantitat i l'import del detall de línia de factura original per a materials.</span><span class="sxs-lookup"><span data-stu-id="94f3c-140">A new unbilled sales actual for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="94f3c-141">Facturació del crèdit parcial d'una transacció de material.</span><span class="sxs-lookup"><span data-stu-id="94f3c-141">Invoicing the partial credit on a material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="94f3c-142">Una reversió de vendes facturades per a la quantitat i l'import facturats al detall de línia de factura original per a materials.</span><span class="sxs-lookup"><span data-stu-id="94f3c-142">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="94f3c-143">Un nou valor real de vendes no facturades que es poden cobrar per la quantitat i l'import del detall de la línia de factura editat, una reversió d'aquesta i una venda facturada equivalent real.</span><span class="sxs-lookup"><span data-stu-id="94f3c-143">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="94f3c-144">Nou valor real de venda no facturada imputable per la quantitat restant i import després de deduir les xifres corregides en el detall de la línia de factura.</span><span class="sxs-lookup"><span data-stu-id="94f3c-144">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="94f3c-145">Facturació del crèdit complet d'una transacció d'impostos facturada prèviament.</span><span class="sxs-lookup"><span data-stu-id="94f3c-145">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="94f3c-146">Reversió de vendes facturades per la quantitat i l'import en el detall de la línia de factura original per a l'impost.</span><span class="sxs-lookup"><span data-stu-id="94f3c-146">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="94f3c-147">Nou valor real de vendes sense facturar per la quantitat i l'import en el detall de la línia de factura original per a l'impost.</span><span class="sxs-lookup"><span data-stu-id="94f3c-147">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="94f3c-148">Facturació del crèdit parcial d'una transacció d'impostos facturada prèviament.</span><span class="sxs-lookup"><span data-stu-id="94f3c-148">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="94f3c-149">Reversió de vendes facturades per la quantitat i l'import facturat en el detall de la línia de factura original per a l'impost.</span><span class="sxs-lookup"><span data-stu-id="94f3c-149">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="94f3c-150">Nou valor real de venda no facturada imputable per la quantitat i l'import en el detall de la línia de factura correctiva editada, reversió d'això i valor real de venda facturada equivalent.</span><span class="sxs-lookup"><span data-stu-id="94f3c-150">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="94f3c-151">Facturació del crèdit complet d'una fita facturada prèviament.</span><span class="sxs-lookup"><span data-stu-id="94f3c-151">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="94f3c-152">Reversió de vendes facturades per l'import en el detall de la línia de factura original per a la fita.</span><span class="sxs-lookup"><span data-stu-id="94f3c-152">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="94f3c-153">L'estat de la factura de la fita s'actualitza de <b>Factura de client comptabilitzada</b> a <b>Preparat per a facturació</b>.</span><span class="sxs-lookup"><span data-stu-id="94f3c-153">The invoice status of the milestone is updated from <b>Customer Invoice Posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="94f3c-154">Facturació del crèdit parcial d'una fita facturada prèviament.</span><span class="sxs-lookup"><span data-stu-id="94f3c-154">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="94f3c-155">No s'admet aquest escenari.</span><span class="sxs-lookup"><span data-stu-id="94f3c-155">This scenario isn't supported.</span></span>
                </p>
            </td>
        </tr>       
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
