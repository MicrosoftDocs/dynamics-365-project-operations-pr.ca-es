---
title: Confirmació d'una factura proforma
description: En aquest tema, podreu obtenir informació sobre la confirmació d'una factura proforma.
author: rumant
manager: AnnBe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b2ed241509d2643d841ce55777e6e316612f70b8
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287856"
---
# <a name="confirm-a-proforma-invoice"></a><span data-ttu-id="cadbf-103">Confirmació d'una factura proforma</span><span class="sxs-lookup"><span data-stu-id="cadbf-103">Confirm a proforma invoice</span></span>

<span data-ttu-id="cadbf-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_</span><span class="sxs-lookup"><span data-stu-id="cadbf-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="cadbf-105">Després que es confirmi una factura proforma, l'estat de la factura del projecte s'actualitza a **Confirmada**.</span><span class="sxs-lookup"><span data-stu-id="cadbf-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="cadbf-106">Quan es confirma una factura, es converteix en només de lectura.</span><span class="sxs-lookup"><span data-stu-id="cadbf-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="cadbf-107">En el futur, la factura només es pot corregir si hi ha correccions o crèdits iniciats pel client, o quan la factura es marca com a pagada.</span><span class="sxs-lookup"><span data-stu-id="cadbf-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits, or when it's marked as paid.</span></span>

<span data-ttu-id="cadbf-108">La taula següent enumera els valors reals creats pel sistema.</span><span class="sxs-lookup"><span data-stu-id="cadbf-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="cadbf-109">Aquests valors reals es creen quan es realitzen certes operacions sobre l'esborrany de la factura del projecte abans de confirmar-la.</span><span class="sxs-lookup"><span data-stu-id="cadbf-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="416" valign="top">
                <p><span data-ttu-id="cadbf-110">
                    <strong>Escenari</strong>
                </span><span class="sxs-lookup"><span data-stu-id="cadbf-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="608" valign="top">
                <p><span data-ttu-id="cadbf-111">
                    <strong>Valors reals creats en la confirmació</strong>
                </span><span class="sxs-lookup"><span data-stu-id="cadbf-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="cadbf-112">Facturar una transacció de temps sense cap modificació a l'esborrany de factura.</span><span class="sxs-lookup"><span data-stu-id="cadbf-112">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="cadbf-113">Reversió de vendes no facturades per les hores i l'import en l'aprovació de temps original.</span><span class="sxs-lookup"><span data-stu-id="cadbf-113">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="cadbf-114">Valor real de venda facturada per les hores i quantitat en l'aprovació de temps original.</span><span class="sxs-lookup"><span data-stu-id="cadbf-114">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="cadbf-115">Facturació d'una transacció de temps editada per reduir la quantitat.</span><span class="sxs-lookup"><span data-stu-id="cadbf-115">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="cadbf-116">Reversió de vendes no facturades per les hores i l'import en l'aprovació de temps original.</span><span class="sxs-lookup"><span data-stu-id="cadbf-116">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="cadbf-117">Nou valor real de venda no facturada imputable per les hores i l'import en el detall de la línia de factura editada, reversió del valor real de venda sense facturar i valor real de venda facturada equivalent.</span><span class="sxs-lookup"><span data-stu-id="cadbf-117">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="cadbf-118">Nou valor real de venda no facturada no imputable per a les hores i l'import restants després de deduir les xifres corregides en el detall de la línia de factura editada, reversió del valor real de venda sense facturar i valor real de venda facturada equivalent.</span><span class="sxs-lookup"><span data-stu-id="cadbf-118">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="cadbf-119">Facturació d'una transacció de temps editada per augmentar la quantitat.</span><span class="sxs-lookup"><span data-stu-id="cadbf-119">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="cadbf-120">Reversió de vendes no facturades per les hores i l'import en l'aprovació de temps original.</span><span class="sxs-lookup"><span data-stu-id="cadbf-120">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="cadbf-121">Nou valor real de venda no facturada imputable per les hores i l'import en el detall de la línia de factura editada, reversió del valor real de venda sense facturar i valor real de venda facturada equivalent.</span><span class="sxs-lookup"><span data-stu-id="cadbf-121">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="cadbf-122">Facturar una transacció de despeses sense cap modificació a l'esborrany de factura.</span><span class="sxs-lookup"><span data-stu-id="cadbf-122">Invoicing an expense transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="cadbf-123">Reversió de vendes sense facturar per la quantitat i quantitat en l'aprovació de despeses original.</span><span class="sxs-lookup"><span data-stu-id="cadbf-123">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="cadbf-124">Valor real de venda facturada per la quantitat i quantitat en l'aprovació de despeses original.</span><span class="sxs-lookup"><span data-stu-id="cadbf-124">A billed sales actual for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="cadbf-125">Facturació d'una transacció de despesa editada per reduir la quantitat.</span><span class="sxs-lookup"><span data-stu-id="cadbf-125">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="cadbf-126">Reversió de vendes sense facturar per la quantitat i quantitat en l'aprovació de despeses original.</span><span class="sxs-lookup"><span data-stu-id="cadbf-126">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="cadbf-127">Nou valor real de venda no facturada imputable per a la quantitat i l'import en el detall de la línia de factura editada, reversió del valor real de venda no facturada i valor real de venda facturada equivalent.</span><span class="sxs-lookup"><span data-stu-id="cadbf-127">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="cadbf-128">Nou valor real de venda no facturada no imputable per a la quantitat i l'import restants després de deduir les xifres corregides en el detall de la línia de factura editada, reversió del valor real de venda sense facturar i valor real de venda facturada equivalent.</span><span class="sxs-lookup"><span data-stu-id="cadbf-128">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent of the billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="cadbf-129">Facturació d'una transacció de despesa editada per augmentar la quantitat.</span><span class="sxs-lookup"><span data-stu-id="cadbf-129">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="cadbf-130">Reversió de vendes sense facturar per la quantitat i quantitat en l'aprovació de despeses original.</span><span class="sxs-lookup"><span data-stu-id="cadbf-130">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="cadbf-131">Nou valor real de venda no facturada imputable per a la quantitat i l'import en el detall de la línia de factura editada, reversió del valor real de venda no facturada i valor real de venda facturada equivalent.</span><span class="sxs-lookup"><span data-stu-id="cadbf-131">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the untilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="cadbf-132">Facturació d'una tarifa.</span><span class="sxs-lookup"><span data-stu-id="cadbf-132">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="cadbf-133">Reversió de vendes no facturades per a l'import de la taxa en la línia del llibre diari original.</span><span class="sxs-lookup"><span data-stu-id="cadbf-133">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="cadbf-134">Valor real de venda facturada per la quantitat i quantitat en la línia del llibre diari de taxa original.</span><span class="sxs-lookup"><span data-stu-id="cadbf-134">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="cadbf-135">Facturació d'una fita.</span><span class="sxs-lookup"><span data-stu-id="cadbf-135">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="cadbf-136">Valor real de vendes facturades per l'import de la fita a la fita original a la línia de contracte del projecte.</span><span class="sxs-lookup"><span data-stu-id="cadbf-136">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]