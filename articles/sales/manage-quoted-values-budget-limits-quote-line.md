---
title: Informació general de les línies d'oferta basades en projectes
description: En aquest tema s'ofereix informació sobre l'ús de línies d'oferta basades en projectes per al treball del projecte.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: e61a9fbf357123884397b930662d11f22bfdeaa0
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5277776"
---
# <a name="project-based-quote-lines-overview"></a><span data-ttu-id="4ab92-103">Informació general de les línies d'oferta basades en projectes</span><span class="sxs-lookup"><span data-stu-id="4ab92-103">Project-based quote lines overview</span></span>

<span data-ttu-id="4ab92-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_</span><span class="sxs-lookup"><span data-stu-id="4ab92-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="4ab92-105">Les línies d'oferta basades en projectes estan dissenyades per ajudar a estimar el treball del projecte en una interacció.</span><span class="sxs-lookup"><span data-stu-id="4ab92-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="4ab92-106">L'estructura d'una línia d'oferta basada en projectes s'amplia per a estimacions de projecte amb els conceptes següents:</span><span class="sxs-lookup"><span data-stu-id="4ab92-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="4ab92-107">Mètode de facturació</span><span class="sxs-lookup"><span data-stu-id="4ab92-107">Billing Method</span></span>
- <span data-ttu-id="4ab92-108">Assignació de projectes</span><span class="sxs-lookup"><span data-stu-id="4ab92-108">Project Mapping</span></span>
- <span data-ttu-id="4ab92-109">Classes de transaccions incloses</span><span class="sxs-lookup"><span data-stu-id="4ab92-109">Included Transaction classes</span></span>
- <span data-ttu-id="4ab92-110">Límit que no s’ha de superar</span><span class="sxs-lookup"><span data-stu-id="4ab92-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="4ab92-111">Configuració de la imputabilitat</span><span class="sxs-lookup"><span data-stu-id="4ab92-111">Chargeability setup</span></span>
- <span data-ttu-id="4ab92-112">Estimació mitjançant detalls de la línia d'oferta</span><span class="sxs-lookup"><span data-stu-id="4ab92-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="4ab92-113">Clients de la línia d’oferta</span><span class="sxs-lookup"><span data-stu-id="4ab92-113">Quote line Customers</span></span>

<span data-ttu-id="4ab92-114">A la taula següent es proporciona informació sobre els camps de la pestanya **General** de la línia d'oferta basada en projectes.</span><span class="sxs-lookup"><span data-stu-id="4ab92-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="4ab92-115">Aquests camps ajuden a configurar la base per a una estimació detallada i des de zero per al treball del projecte.</span><span class="sxs-lookup"><span data-stu-id="4ab92-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="4ab92-116">**Camp**</span><span class="sxs-lookup"><span data-stu-id="4ab92-116">**Field**</span></span> | <span data-ttu-id="4ab92-117">**Descripció**</span><span class="sxs-lookup"><span data-stu-id="4ab92-117">**Description**</span></span> | <span data-ttu-id="4ab92-118">**Impacte descendent**</span><span class="sxs-lookup"><span data-stu-id="4ab92-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="4ab92-119">Nom</span><span class="sxs-lookup"><span data-stu-id="4ab92-119">Name</span></span> | <span data-ttu-id="4ab92-120">Nom de la línia d'oferta que hauria d'ajudar-vos a identificar el component discret de l'oferta que s'està estimant.</span><span class="sxs-lookup"><span data-stu-id="4ab92-120">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="4ab92-121">Es copia a la línia de contracte del projecte que es crea des d'aquesta línia d'oferta en guanyar l'oferta.</span><span class="sxs-lookup"><span data-stu-id="4ab92-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="4ab92-122">Mètode de facturació</span><span class="sxs-lookup"><span data-stu-id="4ab92-122">Billing Method</span></span> | <span data-ttu-id="4ab92-123">En una oferta creada a partir d'una oportunitat, aquest valor es copia des del camp corresponent a la línia d'oportunitat.</span><span class="sxs-lookup"><span data-stu-id="4ab92-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="4ab92-124">Aquest camp inclou els dos models de contracte principals compatibles amb el Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="4ab92-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="4ab92-125">- Preu fix</span><span class="sxs-lookup"><span data-stu-id="4ab92-125">- Fixed price</span></span></br><span data-ttu-id="4ab92-126">- Temps i material.</span><span class="sxs-lookup"><span data-stu-id="4ab92-126">- Time and material.</span></span>| <span data-ttu-id="4ab92-127">El valor d'aquest camp es copia a la línia de contracte del projecte que es crea des d'aquesta línia d'oferta en guanyar l'oferta.</span><span class="sxs-lookup"><span data-stu-id="4ab92-127">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="4ab92-128">Project</span><span class="sxs-lookup"><span data-stu-id="4ab92-128">Project</span></span> | <span data-ttu-id="4ab92-129">Utilitzeu aquest camp opcional per identificar el projecte que s'utilitzarà per lliurar el treball en aquesta interacció.</span><span class="sxs-lookup"><span data-stu-id="4ab92-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="4ab92-130">Quan un projecte s'assigna a una línia d'oferta, ajuda amb la creació de tasques imputables i també amb l'aportació d'una estimació basada en projectes a la línia d'oferta com a detalls de la línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="4ab92-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="4ab92-131">Quan un projecte no està assignat a una línia d'oferta basada en projectes, la estimació s'ha de crear manualment creant cada detall de la línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="4ab92-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="4ab92-132">El valor d'aquest camp es copia a la línia de contracte del projecte que es crea des d'aquesta línia d'oferta en guanyar l'oferta.</span><span class="sxs-lookup"><span data-stu-id="4ab92-132">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="4ab92-133">Inclou el temps</span><span class="sxs-lookup"><span data-stu-id="4ab92-133">Include Time</span></span> | <span data-ttu-id="4ab92-134">Una marca **Sí**/**No** indica si les transaccions de temps o els costos de treball del projecte seleccionat s'inclouran a l'estimació en aquesta línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="4ab92-134">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="4ab92-135">Un valor **No** indica que les transaccions de temps o els costos de treball no s'inclouran a l'estimació en aquesta línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="4ab92-135">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="4ab92-136">Un valor **Sí** indica que les transaccions de temps o els costos de treball s'inclouran a l'estimació en aquesta línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="4ab92-136">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="4ab92-137">El valor d'aquest camp es copia a la línia de contracte del projecte que es crea des d'aquesta línia d'oferta en guanyar l'oferta.</span><span class="sxs-lookup"><span data-stu-id="4ab92-137">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="4ab92-138">Inclou la despesa</span><span class="sxs-lookup"><span data-stu-id="4ab92-138">Include Expense</span></span> | <span data-ttu-id="4ab92-139">Una marca **Sí**/**No** indica si els costos de despesa del projecte seleccionat s'inclouran a l'estimació en aquesta línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="4ab92-139">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="4ab92-140">Un valor **No** indica que el cost de despesa no s'inclourà a l'estimació en aquesta línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="4ab92-140">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="4ab92-141">Un valor **Sí** indica que el cost de despesa s'inclourà a l'estimació en aquesta línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="4ab92-141">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="4ab92-142">El valor d'aquest camp es copia a la línia de contracte del projecte que es crea des d'aquesta línia d'oferta en guanyar l'oferta.</span><span class="sxs-lookup"><span data-stu-id="4ab92-142">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="4ab92-143">Inclou la taxa</span><span class="sxs-lookup"><span data-stu-id="4ab92-143">Include Fee</span></span> | <span data-ttu-id="4ab92-144">Una marca **Sí**/**No** indica si les taxes del projecte seleccionat s'inclouran a l'estimació en aquesta línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="4ab92-144">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="4ab92-145">Un valor **No** indica que les taxes no s'inclouran a l'estimació en aquesta línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="4ab92-145">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="4ab92-146">Un valor **Sí** indica que les taxes s'inclouran a l'estimació en aquesta línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="4ab92-146">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="4ab92-147">El valor d'aquest camp es copia a la línia de contracte del projecte que es crea des d'aquesta línia d'oferta en guanyar l'oferta.</span><span class="sxs-lookup"><span data-stu-id="4ab92-147">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="4ab92-148">Import de l’oferta</span><span class="sxs-lookup"><span data-stu-id="4ab92-148">Quoted Amount</span></span> | <span data-ttu-id="4ab92-149">Això és una quantitat que s'oferirà al client per a tot el treball previst en aquesta línia d'oferta basada en el projecte.</span><span class="sxs-lookup"><span data-stu-id="4ab92-149">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="4ab92-150">En una oferta creada a partir d'una oportunitat, aquest valor es copia des del camp **Pressupost de client** a la línia d'oportunitat.</span><span class="sxs-lookup"><span data-stu-id="4ab92-150">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="4ab92-151">Quan la línia d'oferta basada en projectes té detalls de línia, aquest camp està bloquejat per editar-lo i es resumeix de l'import dels detalls de la línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="4ab92-151">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="4ab92-152">El valor d'aquest camp es copia a la línia de contracte del projecte que es crea des d'aquesta línia d'oferta en guanyar l'oferta.</span><span class="sxs-lookup"><span data-stu-id="4ab92-152">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="4ab92-153">Impost estimat</span><span class="sxs-lookup"><span data-stu-id="4ab92-153">Estimated Tax</span></span> | <span data-ttu-id="4ab92-154">Es tracta d'un camp editable per a l'usuari que afegirà l'import de l'impost previst a la línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="4ab92-154">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="4ab92-155">Quan una línia d'oferta basada en projectes té detalls de línia, aquest camp està bloquejat per editar-lo i es resumeix de l'import d'impostos dels detalls de la línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="4ab92-155">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="4ab92-156">El valor d'aquest camp es copia a la línia de contracte del projecte que es crea des d'aquesta línia d'oferta en guanyar l'oferta.</span><span class="sxs-lookup"><span data-stu-id="4ab92-156">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="4ab92-157">Import de l’oferta després d’impostos</span><span class="sxs-lookup"><span data-stu-id="4ab92-157">Quoted Amount after Tax</span></span> | <span data-ttu-id="4ab92-158">Aquest camp és l'import de la línia d'oferta després de l'impost i és només de lectura.</span><span class="sxs-lookup"><span data-stu-id="4ab92-158">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="4ab92-159">L'import d'aquest camp es calcula com a *Import de l'oferta + impost*.</span><span class="sxs-lookup"><span data-stu-id="4ab92-159">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="4ab92-160">El valor d'aquest camp es copia a la línia de contracte del projecte que es crea des d'aquesta línia d'oferta en guanyar l'oferta.</span><span class="sxs-lookup"><span data-stu-id="4ab92-160">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="4ab92-161">Límit que no s’ha de superar</span><span class="sxs-lookup"><span data-stu-id="4ab92-161">Not-to-exceed Limit</span></span> | <span data-ttu-id="4ab92-162">Aquest camp és editable i només està disponible a les línies d'oferta basades en el projecte que tenen un mètode de facturació **Temps i material**.</span><span class="sxs-lookup"><span data-stu-id="4ab92-162">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="4ab92-163">El valor d'aquest camp es copia a la línia de contracte del projecte que es crea des d'aquesta línia d'oferta en guanyar l'oferta.</span><span class="sxs-lookup"><span data-stu-id="4ab92-163">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="4ab92-164">Pressupost del client</span><span class="sxs-lookup"><span data-stu-id="4ab92-164">Customer Budget</span></span> | <span data-ttu-id="4ab92-165">Aquest camp és editable i es copia des del camp corresponent a la línia d'oportunitat si l'oferta es va crear a partir d'una oportunitat.</span><span class="sxs-lookup"><span data-stu-id="4ab92-165">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="4ab92-166">El valor d'aquest camp es copia a la línia de contracte del projecte que es crea des d'aquesta línia d'oferta en guanyar l'oferta.</span><span class="sxs-lookup"><span data-stu-id="4ab92-166">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |

## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="4ab92-167">Regles de validació per als camps de la pestanya General de línies d'oferta basades en projectes</span><span class="sxs-lookup"><span data-stu-id="4ab92-167">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="4ab92-168">**Regla 1**: una determinada classe de transacció del projecte seleccionat només es pot incloure en una línia d'oferta basada en projectes d'una oferta.</span><span class="sxs-lookup"><span data-stu-id="4ab92-168">**Rule 1**: A certain transaction class on the selected project can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="4ab92-169">**Regla 2**: si una oportunitat té diverses ofertes, pot haver-hi línies d'ofertes de diverses ofertes que facin referència al mateix projecte i que incloguin la mateixa classe de transacció.</span><span class="sxs-lookup"><span data-stu-id="4ab92-169">**Rule 2**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="4ab92-170">**Regla 3**: si les ofertes no pertanyen a la mateixa oportunitat, no poden incloure el mateix projecte i classe de transacció.</span><span class="sxs-lookup"><span data-stu-id="4ab92-170">**Rule 3**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="1" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="4ab92-171">
                    <strong>Oportunitat</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4ab92-171">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="4ab92-172">
                    <strong>Oferta</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4ab92-172">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="4ab92-173">
                    <strong>Línia d’oferta</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4ab92-173">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="4ab92-174">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4ab92-174">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="4ab92-175">
                    <strong>Inclou el temps</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4ab92-175">
                    <strong>Include time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="4ab92-176">
                    <strong>Inclou la despesa</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4ab92-176">
                    <strong>Include expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="4ab92-177">
                    <strong>Inclou</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4ab92-177">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="4ab92-178">
                    <strong>Tarifa</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4ab92-178">
                    <strong>fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="4ab92-179">
                    <strong>Vàlid/No és vàlid</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4ab92-179">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="4ab92-180">
                    <strong>Motiu</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4ab92-180">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="4ab92-181">O1</span><span class="sxs-lookup"><span data-stu-id="4ab92-181">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4ab92-182">T1</span><span class="sxs-lookup"><span data-stu-id="4ab92-182">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4ab92-183">QL1</span><span class="sxs-lookup"><span data-stu-id="4ab92-183">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4ab92-184">P1</span><span class="sxs-lookup"><span data-stu-id="4ab92-184">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4ab92-185">Sí</span><span class="sxs-lookup"><span data-stu-id="4ab92-185">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4ab92-186">Sí</span><span class="sxs-lookup"><span data-stu-id="4ab92-186">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4ab92-187">Sí</span><span class="sxs-lookup"><span data-stu-id="4ab92-187">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4ab92-188">No és vàlid</span><span class="sxs-lookup"><span data-stu-id="4ab92-188">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4ab92-189">Infracció de la regla 1.</span><span class="sxs-lookup"><span data-stu-id="4ab92-189">Violation of Rule #1.</span></span> <span data-ttu-id="4ab92-190">El temps, les despeses i els impostos en el projecte P1 s'inclouen a les línies d'oferta QL1 i QL2.</span><span class="sxs-lookup"><span data-stu-id="4ab92-190">Time, Expense, and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="4ab92-191">O1</span><span class="sxs-lookup"><span data-stu-id="4ab92-191">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4ab92-192">T1</span><span class="sxs-lookup"><span data-stu-id="4ab92-192">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4ab92-193">QL2</span><span class="sxs-lookup"><span data-stu-id="4ab92-193">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4ab92-194">P1</span><span class="sxs-lookup"><span data-stu-id="4ab92-194">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4ab92-195">Sí</span><span class="sxs-lookup"><span data-stu-id="4ab92-195">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4ab92-196">Sí</span><span class="sxs-lookup"><span data-stu-id="4ab92-196">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4ab92-197">Sí</span><span class="sxs-lookup"><span data-stu-id="4ab92-197">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="4ab92-198">O1</span><span class="sxs-lookup"><span data-stu-id="4ab92-198">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4ab92-199">T1</span><span class="sxs-lookup"><span data-stu-id="4ab92-199">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4ab92-200">QL1</span><span class="sxs-lookup"><span data-stu-id="4ab92-200">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4ab92-201">P1</span><span class="sxs-lookup"><span data-stu-id="4ab92-201">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4ab92-202">Sí</span><span class="sxs-lookup"><span data-stu-id="4ab92-202">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4ab92-203">No</span><span class="sxs-lookup"><span data-stu-id="4ab92-203">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4ab92-204">Sí</span><span class="sxs-lookup"><span data-stu-id="4ab92-204">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4ab92-205">No és vàlid</span><span class="sxs-lookup"><span data-stu-id="4ab92-205">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4ab92-206">Infracció de la regla 1.</span><span class="sxs-lookup"><span data-stu-id="4ab92-206">Violation of Rule #1.</span></span> <span data-ttu-id="4ab92-207">El temps i els impostos en el projecte P1 s'inclouen a les línies d'oferta QL1 i QL2.</span><span class="sxs-lookup"><span data-stu-id="4ab92-207">Time and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="4ab92-208">O1</span><span class="sxs-lookup"><span data-stu-id="4ab92-208">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4ab92-209">T1</span><span class="sxs-lookup"><span data-stu-id="4ab92-209">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4ab92-210">QL2</span><span class="sxs-lookup"><span data-stu-id="4ab92-210">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4ab92-211">P1</span><span class="sxs-lookup"><span data-stu-id="4ab92-211">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4ab92-212">Sí</span><span class="sxs-lookup"><span data-stu-id="4ab92-212">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4ab92-213">Sí</span><span class="sxs-lookup"><span data-stu-id="4ab92-213">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4ab92-214">Sí</span><span class="sxs-lookup"><span data-stu-id="4ab92-214">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="4ab92-215">O1</span><span class="sxs-lookup"><span data-stu-id="4ab92-215">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4ab92-216">T1</span><span class="sxs-lookup"><span data-stu-id="4ab92-216">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4ab92-217">QL1</span><span class="sxs-lookup"><span data-stu-id="4ab92-217">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4ab92-218">P1</span><span class="sxs-lookup"><span data-stu-id="4ab92-218">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4ab92-219">Sí</span><span class="sxs-lookup"><span data-stu-id="4ab92-219">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4ab92-220">No</span><span class="sxs-lookup"><span data-stu-id="4ab92-220">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4ab92-221">Sí</span><span class="sxs-lookup"><span data-stu-id="4ab92-221">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4ab92-222">Vàlid</span><span class="sxs-lookup"><span data-stu-id="4ab92-222">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                 <p>
<span data-ttu-id="4ab92-223">El temps i els impostos en el projecte P1 s'inclouen a QL1.</span><span class="sxs-lookup"><span data-stu-id="4ab92-223">Time and fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="4ab92-224">La despesa en el projecte P1 s'inclou a QL2.</span><span class="sxs-lookup"><span data-stu-id="4ab92-224">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="4ab92-225">No se superposa el que s'inclou a cada línia d'oferta i per tant és vàlid.</span><span class="sxs-lookup"><span data-stu-id="4ab92-225">There is no overlap in what is being included on each quote line so it is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="4ab92-226">O1</span><span class="sxs-lookup"><span data-stu-id="4ab92-226">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4ab92-227">T1</span><span class="sxs-lookup"><span data-stu-id="4ab92-227">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4ab92-228">QL2</span><span class="sxs-lookup"><span data-stu-id="4ab92-228">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4ab92-229">P1</span><span class="sxs-lookup"><span data-stu-id="4ab92-229">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4ab92-230">No</span><span class="sxs-lookup"><span data-stu-id="4ab92-230">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4ab92-231">Sí</span><span class="sxs-lookup"><span data-stu-id="4ab92-231">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4ab92-232">No</span><span class="sxs-lookup"><span data-stu-id="4ab92-232">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="4ab92-233">O1</span><span class="sxs-lookup"><span data-stu-id="4ab92-233">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4ab92-234">T1</span><span class="sxs-lookup"><span data-stu-id="4ab92-234">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4ab92-235">QL1</span><span class="sxs-lookup"><span data-stu-id="4ab92-235">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4ab92-236">P1</span><span class="sxs-lookup"><span data-stu-id="4ab92-236">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4ab92-237">Sí</span><span class="sxs-lookup"><span data-stu-id="4ab92-237">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4ab92-238">Sí</span><span class="sxs-lookup"><span data-stu-id="4ab92-238">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4ab92-239">Sí</span><span class="sxs-lookup"><span data-stu-id="4ab92-239">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4ab92-240">No és vàlid</span><span class="sxs-lookup"><span data-stu-id="4ab92-240">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4ab92-241">Infracció de la regla 1 anterior</span><span class="sxs-lookup"><span data-stu-id="4ab92-241">Violation of Rule #1 above</span></span> </p>
                <p>
<span data-ttu-id="4ab92-242">Q1 inclou el temps, les despeses i els impostos del projecte P1 sencer.</span><span class="sxs-lookup"><span data-stu-id="4ab92-242">Q1 includes Time, Expenses, and Fees for the whole project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="4ab92-243">QL2 inclou el temps, les despeses i els impostos per a tot el projecte P1 i se superposa amb el que s'inclou a Q1.</span><span class="sxs-lookup"><span data-stu-id="4ab92-243">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="4ab92-244">O1</span><span class="sxs-lookup"><span data-stu-id="4ab92-244">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4ab92-245">T1</span><span class="sxs-lookup"><span data-stu-id="4ab92-245">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4ab92-246">QL2</span><span class="sxs-lookup"><span data-stu-id="4ab92-246">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4ab92-247">P1</span><span class="sxs-lookup"><span data-stu-id="4ab92-247">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4ab92-248">Sí</span><span class="sxs-lookup"><span data-stu-id="4ab92-248">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4ab92-249">Sí</span><span class="sxs-lookup"><span data-stu-id="4ab92-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4ab92-250">Sí</span><span class="sxs-lookup"><span data-stu-id="4ab92-250">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="4ab92-251">O1</span><span class="sxs-lookup"><span data-stu-id="4ab92-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4ab92-252">T1</span><span class="sxs-lookup"><span data-stu-id="4ab92-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4ab92-253">QL1</span><span class="sxs-lookup"><span data-stu-id="4ab92-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4ab92-254">P1</span><span class="sxs-lookup"><span data-stu-id="4ab92-254">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4ab92-255">Sí</span><span class="sxs-lookup"><span data-stu-id="4ab92-255">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4ab92-256">Sí</span><span class="sxs-lookup"><span data-stu-id="4ab92-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4ab92-257">Sí</span><span class="sxs-lookup"><span data-stu-id="4ab92-257">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="4ab92-258">Vàlid</span><span class="sxs-lookup"><span data-stu-id="4ab92-258">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4ab92-259">Segons la regla 2, Q1 i Q2 són dues ofertes de la mateixa oportunitat, per la qual cosa poden estimar-se per als mateixos components d'un projecte.</span><span class="sxs-lookup"><span data-stu-id="4ab92-259">Based on Rule #2, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="4ab92-260">O1</span><span class="sxs-lookup"><span data-stu-id="4ab92-260">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4ab92-261">T2</span><span class="sxs-lookup"><span data-stu-id="4ab92-261">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4ab92-262">QL1 a Q2</span><span class="sxs-lookup"><span data-stu-id="4ab92-262">QL1 on Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4ab92-263">P1</span><span class="sxs-lookup"><span data-stu-id="4ab92-263">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4ab92-264">Sí</span><span class="sxs-lookup"><span data-stu-id="4ab92-264">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4ab92-265">Sí</span><span class="sxs-lookup"><span data-stu-id="4ab92-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4ab92-266">Sí</span><span class="sxs-lookup"><span data-stu-id="4ab92-266">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="4ab92-267">O1</span><span class="sxs-lookup"><span data-stu-id="4ab92-267">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4ab92-268">T1</span><span class="sxs-lookup"><span data-stu-id="4ab92-268">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4ab92-269">QL1</span><span class="sxs-lookup"><span data-stu-id="4ab92-269">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4ab92-270">P1</span><span class="sxs-lookup"><span data-stu-id="4ab92-270">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4ab92-271">Sí</span><span class="sxs-lookup"><span data-stu-id="4ab92-271">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4ab92-272">Sí</span><span class="sxs-lookup"><span data-stu-id="4ab92-272">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4ab92-273">Sí</span><span class="sxs-lookup"><span data-stu-id="4ab92-273">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="4ab92-274">Vàlid</span><span class="sxs-lookup"><span data-stu-id="4ab92-274">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4ab92-275">Segons la regla 3, Q1 i Q2 són dues ofertes d'oportunitats diferents, per la qual cosa no poden estimar-se per als mateixos components d'un mateix projecte.</span><span class="sxs-lookup"><span data-stu-id="4ab92-275">Based on Rule #3, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="4ab92-276">O2</span><span class="sxs-lookup"><span data-stu-id="4ab92-276">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4ab92-277">T1</span><span class="sxs-lookup"><span data-stu-id="4ab92-277">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4ab92-278">QL1</span><span class="sxs-lookup"><span data-stu-id="4ab92-278">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4ab92-279">P1</span><span class="sxs-lookup"><span data-stu-id="4ab92-279">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4ab92-280">Sí</span><span class="sxs-lookup"><span data-stu-id="4ab92-280">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4ab92-281">Sí</span><span class="sxs-lookup"><span data-stu-id="4ab92-281">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4ab92-282">Sí</span><span class="sxs-lookup"><span data-stu-id="4ab92-282">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="4ab92-283">No és vàlid</span><span class="sxs-lookup"><span data-stu-id="4ab92-283">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../includes/footer-banner.md)]