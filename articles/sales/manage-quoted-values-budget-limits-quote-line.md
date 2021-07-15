---
title: Informació general de les línies d'oferta de projecte
description: Aquest tema proporciona informació sobre l'ús de les línies d'oferta del projecte per al treball del projecte.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: c585bbc55119e678a4f75f5dfe8966a436db1a34
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368059"
---
# <a name="project-quote-lines-overview"></a><span data-ttu-id="21416-103">Informació general de les línies d'oferta de projecte</span><span class="sxs-lookup"><span data-stu-id="21416-103">Project quote lines overview</span></span>

<span data-ttu-id="21416-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_</span><span class="sxs-lookup"><span data-stu-id="21416-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="21416-105">Les línies d'oferta basades en projectes estan dissenyades per ajudar a estimar el treball del projecte en una interacció.</span><span class="sxs-lookup"><span data-stu-id="21416-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="21416-106">L'estructura d'una línia d'oferta basada en projectes s'amplia per a estimacions de projecte amb els conceptes següents:</span><span class="sxs-lookup"><span data-stu-id="21416-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="21416-107">Mètode de facturació</span><span class="sxs-lookup"><span data-stu-id="21416-107">Billing Method</span></span>
- <span data-ttu-id="21416-108">Assignació de projectes</span><span class="sxs-lookup"><span data-stu-id="21416-108">Project Mapping</span></span>
- <span data-ttu-id="21416-109">Classes de transaccions incloses</span><span class="sxs-lookup"><span data-stu-id="21416-109">Included Transaction classes</span></span>
- <span data-ttu-id="21416-110">Límit que no s’ha de superar</span><span class="sxs-lookup"><span data-stu-id="21416-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="21416-111">Configuració de la imputabilitat</span><span class="sxs-lookup"><span data-stu-id="21416-111">Chargeability setup</span></span>
- <span data-ttu-id="21416-112">Estimació mitjançant detalls de la línia d'oferta</span><span class="sxs-lookup"><span data-stu-id="21416-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="21416-113">Clients de la línia d’oferta</span><span class="sxs-lookup"><span data-stu-id="21416-113">Quote line Customers</span></span>

<span data-ttu-id="21416-114">A la taula següent es proporciona informació sobre els camps de la pestanya **General** de la línia d'oferta basada en projectes.</span><span class="sxs-lookup"><span data-stu-id="21416-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="21416-115">Aquests camps ajuden a configurar la base per a una estimació detallada i des de zero per al treball del projecte.</span><span class="sxs-lookup"><span data-stu-id="21416-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="21416-116">**Camp**</span><span class="sxs-lookup"><span data-stu-id="21416-116">**Field**</span></span> | <span data-ttu-id="21416-117">**Descripció**</span><span class="sxs-lookup"><span data-stu-id="21416-117">**Description**</span></span> | <span data-ttu-id="21416-118">**Impacte descendent**</span><span class="sxs-lookup"><span data-stu-id="21416-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="21416-119">Nom</span><span class="sxs-lookup"><span data-stu-id="21416-119">Name</span></span> | <span data-ttu-id="21416-120">Nom de la línia d'oferta que hauria d'ajudar-vos a identificar el component discret de l'oferta que s'està estimant.</span><span class="sxs-lookup"><span data-stu-id="21416-120">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="21416-121">Es copia a la línia de contracte del projecte que es crea des d'aquesta línia d'oferta en guanyar l'oferta.</span><span class="sxs-lookup"><span data-stu-id="21416-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="21416-122">Mètode de facturació</span><span class="sxs-lookup"><span data-stu-id="21416-122">Billing Method</span></span> | <span data-ttu-id="21416-123">En una oferta creada a partir d'una oportunitat, aquest valor es copia des del camp corresponent a la línia d'oportunitat.</span><span class="sxs-lookup"><span data-stu-id="21416-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="21416-124">Aquest camp inclou els dos models de contracte principals compatibles amb el Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="21416-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="21416-125">- Preu fix</span><span class="sxs-lookup"><span data-stu-id="21416-125">- Fixed price</span></span></br><span data-ttu-id="21416-126">- Temps i material.</span><span class="sxs-lookup"><span data-stu-id="21416-126">- Time and material.</span></span>| <span data-ttu-id="21416-127">El valor d'aquest camp es copia a la línia de contracte del projecte que es crea des d'aquesta línia d'oferta en guanyar l'oferta.</span><span class="sxs-lookup"><span data-stu-id="21416-127">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="21416-128">Project</span><span class="sxs-lookup"><span data-stu-id="21416-128">Project</span></span> | <span data-ttu-id="21416-129">Utilitzeu aquest camp opcional per identificar el projecte que s'utilitzarà per lliurar el treball en aquesta interacció.</span><span class="sxs-lookup"><span data-stu-id="21416-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="21416-130">Quan un projecte s'assigna a una línia d'oferta, ajuda amb la creació de tasques imputables i també amb l'aportació d'una estimació basada en projectes a la línia d'oferta com a detalls de la línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="21416-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="21416-131">Quan un projecte no està assignat a una línia d'oferta basada en projectes, la estimació s'ha de crear manualment creant cada detall de la línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="21416-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="21416-132">El valor d'aquest camp es copia a la línia de contracte del projecte que es crea des d'aquesta línia d'oferta en guanyar l'oferta.</span><span class="sxs-lookup"><span data-stu-id="21416-132">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="21416-133">Inclou el temps</span><span class="sxs-lookup"><span data-stu-id="21416-133">Include Time</span></span> | <span data-ttu-id="21416-134">Una marca **Sí**/**No** indica si les transaccions de temps o els costos de treball del projecte seleccionat s'inclouran a l'estimació en aquesta línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="21416-134">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="21416-135">Un valor **No** indica que les transaccions de temps o els costos de treball no s'inclouran a l'estimació en aquesta línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="21416-135">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="21416-136">Un valor **Sí** indica que les transaccions de temps o els costos de treball s'inclouran a l'estimació en aquesta línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="21416-136">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="21416-137">El valor d'aquest camp es copia a la línia de contracte del projecte que es crea des d'aquesta línia d'oferta en guanyar l'oferta.</span><span class="sxs-lookup"><span data-stu-id="21416-137">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="21416-138">Inclou la despesa</span><span class="sxs-lookup"><span data-stu-id="21416-138">Include Expense</span></span> | <span data-ttu-id="21416-139">Una marca **Sí**/**No** indica si els costos de despesa del projecte seleccionat s'inclouran a l'estimació en aquesta línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="21416-139">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="21416-140">Un valor **No** indica que el cost de despesa no s'inclourà a l'estimació en aquesta línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="21416-140">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="21416-141">Un valor **Sí** indica que el cost de despesa s'inclourà a l'estimació en aquesta línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="21416-141">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="21416-142">El valor d'aquest camp es copia a la línia de contracte del projecte que es crea des d'aquesta línia d'oferta en guanyar l'oferta.</span><span class="sxs-lookup"><span data-stu-id="21416-142">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="21416-143">Inclou la taxa</span><span class="sxs-lookup"><span data-stu-id="21416-143">Include Fee</span></span> | <span data-ttu-id="21416-144">Una marca **Sí**/**No** indica si les taxes del projecte seleccionat s'inclouran a l'estimació en aquesta línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="21416-144">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="21416-145">Un valor **No** indica que les taxes no s'inclouran a l'estimació en aquesta línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="21416-145">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="21416-146">Un valor **Sí** indica que les taxes s'inclouran a l'estimació en aquesta línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="21416-146">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="21416-147">El valor d'aquest camp es copia a la línia de contracte del projecte que es crea des d'aquesta línia d'oferta en guanyar l'oferta.</span><span class="sxs-lookup"><span data-stu-id="21416-147">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="21416-148">Import de l’oferta</span><span class="sxs-lookup"><span data-stu-id="21416-148">Quoted Amount</span></span> | <span data-ttu-id="21416-149">Això és una quantitat que s'oferirà al client per a tot el treball previst en aquesta línia d'oferta basada en el projecte.</span><span class="sxs-lookup"><span data-stu-id="21416-149">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="21416-150">En una oferta creada a partir d'una oportunitat, aquest valor es copia des del camp **Pressupost de client** a la línia d'oportunitat.</span><span class="sxs-lookup"><span data-stu-id="21416-150">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="21416-151">Quan la línia d'oferta basada en projectes té detalls de línia, aquest camp està bloquejat per editar-lo i es resumeix de l'import dels detalls de la línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="21416-151">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="21416-152">El valor d'aquest camp es copia a la línia de contracte del projecte que es crea des d'aquesta línia d'oferta en guanyar l'oferta.</span><span class="sxs-lookup"><span data-stu-id="21416-152">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="21416-153">Impost estimat</span><span class="sxs-lookup"><span data-stu-id="21416-153">Estimated Tax</span></span> | <span data-ttu-id="21416-154">Es tracta d'un camp editable per a l'usuari que afegirà l'import de l'impost previst a la línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="21416-154">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="21416-155">Quan una línia d'oferta basada en projectes té detalls de línia, aquest camp està bloquejat per editar-lo i es resumeix de l'import d'impostos dels detalls de la línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="21416-155">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="21416-156">El valor d'aquest camp es copia a la línia de contracte del projecte que es crea des d'aquesta línia d'oferta en guanyar l'oferta.</span><span class="sxs-lookup"><span data-stu-id="21416-156">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="21416-157">Import de l’oferta després d’impostos</span><span class="sxs-lookup"><span data-stu-id="21416-157">Quoted Amount after Tax</span></span> | <span data-ttu-id="21416-158">Aquest camp és l'import de la línia d'oferta després de l'impost i és només de lectura.</span><span class="sxs-lookup"><span data-stu-id="21416-158">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="21416-159">L'import d'aquest camp es calcula com a *Import de l'oferta + impost*.</span><span class="sxs-lookup"><span data-stu-id="21416-159">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="21416-160">El valor d'aquest camp es copia a la línia de contracte del projecte que es crea des d'aquesta línia d'oferta en guanyar l'oferta.</span><span class="sxs-lookup"><span data-stu-id="21416-160">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="21416-161">Límit que no s’ha de superar</span><span class="sxs-lookup"><span data-stu-id="21416-161">Not-to-exceed Limit</span></span> | <span data-ttu-id="21416-162">Aquest camp és editable i només està disponible a les línies d'oferta basades en el projecte que tenen un mètode de facturació **Temps i material**.</span><span class="sxs-lookup"><span data-stu-id="21416-162">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="21416-163">El valor d'aquest camp es copia a la línia de contracte del projecte que es crea des d'aquesta línia d'oferta en guanyar l'oferta.</span><span class="sxs-lookup"><span data-stu-id="21416-163">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="21416-164">Pressupost del client</span><span class="sxs-lookup"><span data-stu-id="21416-164">Customer Budget</span></span> | <span data-ttu-id="21416-165">Aquest camp és editable i es copia des del camp corresponent a la línia d'oportunitat si l'oferta es va crear a partir d'una oportunitat.</span><span class="sxs-lookup"><span data-stu-id="21416-165">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="21416-166">El valor d'aquest camp es copia a la línia de contracte del projecte que es crea des d'aquesta línia d'oferta en guanyar l'oferta.</span><span class="sxs-lookup"><span data-stu-id="21416-166">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |

## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="21416-167">Regles de validació per als camps de la pestanya General de línies d'oferta basades en projectes</span><span class="sxs-lookup"><span data-stu-id="21416-167">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="21416-168">**Regla 1**: una determinada classe de transacció del projecte seleccionat només es pot incloure en una línia d'oferta basada en projectes d'una oferta.</span><span class="sxs-lookup"><span data-stu-id="21416-168">**Rule 1**: A certain transaction class on the selected project can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="21416-169">**Regla 2**: si una oportunitat té diverses ofertes, pot haver-hi línies d'ofertes de diverses ofertes que facin referència al mateix projecte i que incloguin la mateixa classe de transacció.</span><span class="sxs-lookup"><span data-stu-id="21416-169">**Rule 2**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="21416-170">**Regla 3**: si les ofertes no pertanyen a la mateixa oportunitat, no poden incloure el mateix projecte i classe de transacció.</span><span class="sxs-lookup"><span data-stu-id="21416-170">**Rule 3**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="1" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="21416-171">
                    <strong>Oportunitat</strong>
                </span><span class="sxs-lookup"><span data-stu-id="21416-171">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="21416-172">
                    <strong>Oferta</strong>
                </span><span class="sxs-lookup"><span data-stu-id="21416-172">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="21416-173">
                    <strong>Línia d’oferta</strong>
                </span><span class="sxs-lookup"><span data-stu-id="21416-173">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="21416-174">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="21416-174">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="21416-175">
                    <strong>Inclou el temps</strong>
                </span><span class="sxs-lookup"><span data-stu-id="21416-175">
                    <strong>Include time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="21416-176">
                    <strong>Inclou la despesa</strong>
                </span><span class="sxs-lookup"><span data-stu-id="21416-176">
                    <strong>Include expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="21416-177">
                    <strong>Inclou</strong>
                </span><span class="sxs-lookup"><span data-stu-id="21416-177">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="21416-178">
                    <strong>Tarifa</strong>
                </span><span class="sxs-lookup"><span data-stu-id="21416-178">
                    <strong>fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="21416-179">
                    <strong>Vàlid/No és vàlid</strong>
                </span><span class="sxs-lookup"><span data-stu-id="21416-179">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="21416-180">
                    <strong>Motiu</strong>
                </span><span class="sxs-lookup"><span data-stu-id="21416-180">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="21416-181">O1</span><span class="sxs-lookup"><span data-stu-id="21416-181">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="21416-182">T1</span><span class="sxs-lookup"><span data-stu-id="21416-182">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="21416-183">QL1</span><span class="sxs-lookup"><span data-stu-id="21416-183">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="21416-184">P1</span><span class="sxs-lookup"><span data-stu-id="21416-184">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="21416-185">Sí</span><span class="sxs-lookup"><span data-stu-id="21416-185">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="21416-186">Sí</span><span class="sxs-lookup"><span data-stu-id="21416-186">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="21416-187">Sí</span><span class="sxs-lookup"><span data-stu-id="21416-187">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="21416-188">No és vàlid</span><span class="sxs-lookup"><span data-stu-id="21416-188">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="21416-189">Infracció de la regla 1.</span><span class="sxs-lookup"><span data-stu-id="21416-189">Violation of Rule #1.</span></span> <span data-ttu-id="21416-190">El temps, les despeses i els impostos en el projecte P1 s'inclouen a les línies d'oferta QL1 i QL2.</span><span class="sxs-lookup"><span data-stu-id="21416-190">Time, Expense, and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="21416-191">O1</span><span class="sxs-lookup"><span data-stu-id="21416-191">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="21416-192">T1</span><span class="sxs-lookup"><span data-stu-id="21416-192">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="21416-193">QL2</span><span class="sxs-lookup"><span data-stu-id="21416-193">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="21416-194">P1</span><span class="sxs-lookup"><span data-stu-id="21416-194">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="21416-195">Sí</span><span class="sxs-lookup"><span data-stu-id="21416-195">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="21416-196">Sí</span><span class="sxs-lookup"><span data-stu-id="21416-196">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="21416-197">Sí</span><span class="sxs-lookup"><span data-stu-id="21416-197">Yes</span></span> </p>
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
<span data-ttu-id="21416-198">O1</span><span class="sxs-lookup"><span data-stu-id="21416-198">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="21416-199">T1</span><span class="sxs-lookup"><span data-stu-id="21416-199">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="21416-200">QL1</span><span class="sxs-lookup"><span data-stu-id="21416-200">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="21416-201">P1</span><span class="sxs-lookup"><span data-stu-id="21416-201">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="21416-202">Sí</span><span class="sxs-lookup"><span data-stu-id="21416-202">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="21416-203">No</span><span class="sxs-lookup"><span data-stu-id="21416-203">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="21416-204">Sí</span><span class="sxs-lookup"><span data-stu-id="21416-204">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="21416-205">No és vàlid</span><span class="sxs-lookup"><span data-stu-id="21416-205">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="21416-206">Infracció de la regla 1.</span><span class="sxs-lookup"><span data-stu-id="21416-206">Violation of Rule #1.</span></span> <span data-ttu-id="21416-207">El temps i els impostos en el projecte P1 s'inclouen a les línies d'oferta QL1 i QL2.</span><span class="sxs-lookup"><span data-stu-id="21416-207">Time and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="21416-208">O1</span><span class="sxs-lookup"><span data-stu-id="21416-208">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="21416-209">T1</span><span class="sxs-lookup"><span data-stu-id="21416-209">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="21416-210">QL2</span><span class="sxs-lookup"><span data-stu-id="21416-210">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="21416-211">P1</span><span class="sxs-lookup"><span data-stu-id="21416-211">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="21416-212">Sí</span><span class="sxs-lookup"><span data-stu-id="21416-212">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="21416-213">Sí</span><span class="sxs-lookup"><span data-stu-id="21416-213">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="21416-214">Sí</span><span class="sxs-lookup"><span data-stu-id="21416-214">Yes</span></span> </p>
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
<span data-ttu-id="21416-215">O1</span><span class="sxs-lookup"><span data-stu-id="21416-215">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="21416-216">T1</span><span class="sxs-lookup"><span data-stu-id="21416-216">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="21416-217">QL1</span><span class="sxs-lookup"><span data-stu-id="21416-217">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="21416-218">P1</span><span class="sxs-lookup"><span data-stu-id="21416-218">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="21416-219">Sí</span><span class="sxs-lookup"><span data-stu-id="21416-219">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="21416-220">No</span><span class="sxs-lookup"><span data-stu-id="21416-220">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="21416-221">Sí</span><span class="sxs-lookup"><span data-stu-id="21416-221">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="21416-222">Vàlid</span><span class="sxs-lookup"><span data-stu-id="21416-222">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                 <p>
<span data-ttu-id="21416-223">El temps i els impostos en el projecte P1 s'inclouen a QL1.</span><span class="sxs-lookup"><span data-stu-id="21416-223">Time and fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="21416-224">La despesa en el projecte P1 s'inclou a QL2.</span><span class="sxs-lookup"><span data-stu-id="21416-224">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="21416-225">No se superposa el que s'inclou a cada línia d'oferta i per tant és vàlid.</span><span class="sxs-lookup"><span data-stu-id="21416-225">There is no overlap in what is being included on each quote line so it is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="21416-226">O1</span><span class="sxs-lookup"><span data-stu-id="21416-226">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="21416-227">T1</span><span class="sxs-lookup"><span data-stu-id="21416-227">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="21416-228">QL2</span><span class="sxs-lookup"><span data-stu-id="21416-228">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="21416-229">P1</span><span class="sxs-lookup"><span data-stu-id="21416-229">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="21416-230">No</span><span class="sxs-lookup"><span data-stu-id="21416-230">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="21416-231">Sí</span><span class="sxs-lookup"><span data-stu-id="21416-231">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="21416-232">No</span><span class="sxs-lookup"><span data-stu-id="21416-232">No</span></span> </p>
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
<span data-ttu-id="21416-233">O1</span><span class="sxs-lookup"><span data-stu-id="21416-233">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="21416-234">T1</span><span class="sxs-lookup"><span data-stu-id="21416-234">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="21416-235">QL1</span><span class="sxs-lookup"><span data-stu-id="21416-235">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="21416-236">P1</span><span class="sxs-lookup"><span data-stu-id="21416-236">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="21416-237">Sí</span><span class="sxs-lookup"><span data-stu-id="21416-237">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="21416-238">Sí</span><span class="sxs-lookup"><span data-stu-id="21416-238">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="21416-239">Sí</span><span class="sxs-lookup"><span data-stu-id="21416-239">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="21416-240">No és vàlid</span><span class="sxs-lookup"><span data-stu-id="21416-240">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="21416-241">Infracció de la regla 1 anterior</span><span class="sxs-lookup"><span data-stu-id="21416-241">Violation of Rule #1 above</span></span> </p>
                <p>
<span data-ttu-id="21416-242">Q1 inclou el temps, les despeses i els impostos del projecte P1 sencer.</span><span class="sxs-lookup"><span data-stu-id="21416-242">Q1 includes Time, Expenses, and Fees for the whole project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="21416-243">QL2 inclou el temps, les despeses i els impostos per a tot el projecte P1 i se superposa amb el que s'inclou a Q1.</span><span class="sxs-lookup"><span data-stu-id="21416-243">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="21416-244">O1</span><span class="sxs-lookup"><span data-stu-id="21416-244">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="21416-245">T1</span><span class="sxs-lookup"><span data-stu-id="21416-245">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="21416-246">QL2</span><span class="sxs-lookup"><span data-stu-id="21416-246">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="21416-247">P1</span><span class="sxs-lookup"><span data-stu-id="21416-247">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="21416-248">Sí</span><span class="sxs-lookup"><span data-stu-id="21416-248">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="21416-249">Sí</span><span class="sxs-lookup"><span data-stu-id="21416-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="21416-250">Sí</span><span class="sxs-lookup"><span data-stu-id="21416-250">Yes</span></span> </p>
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
<span data-ttu-id="21416-251">O1</span><span class="sxs-lookup"><span data-stu-id="21416-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="21416-252">T1</span><span class="sxs-lookup"><span data-stu-id="21416-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="21416-253">QL1</span><span class="sxs-lookup"><span data-stu-id="21416-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="21416-254">P1</span><span class="sxs-lookup"><span data-stu-id="21416-254">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="21416-255">Sí</span><span class="sxs-lookup"><span data-stu-id="21416-255">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="21416-256">Sí</span><span class="sxs-lookup"><span data-stu-id="21416-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="21416-257">Sí</span><span class="sxs-lookup"><span data-stu-id="21416-257">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="21416-258">Vàlid</span><span class="sxs-lookup"><span data-stu-id="21416-258">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="21416-259">Segons la regla 2, Q1 i Q2 són dues ofertes de la mateixa oportunitat, per la qual cosa poden estimar-se per als mateixos components d'un projecte.</span><span class="sxs-lookup"><span data-stu-id="21416-259">Based on Rule #2, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="21416-260">O1</span><span class="sxs-lookup"><span data-stu-id="21416-260">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="21416-261">T2</span><span class="sxs-lookup"><span data-stu-id="21416-261">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="21416-262">QL1 a Q2</span><span class="sxs-lookup"><span data-stu-id="21416-262">QL1 on Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="21416-263">P1</span><span class="sxs-lookup"><span data-stu-id="21416-263">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="21416-264">Sí</span><span class="sxs-lookup"><span data-stu-id="21416-264">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="21416-265">Sí</span><span class="sxs-lookup"><span data-stu-id="21416-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="21416-266">Sí</span><span class="sxs-lookup"><span data-stu-id="21416-266">Yes</span></span> </p>
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
<span data-ttu-id="21416-267">O1</span><span class="sxs-lookup"><span data-stu-id="21416-267">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="21416-268">T1</span><span class="sxs-lookup"><span data-stu-id="21416-268">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="21416-269">QL1</span><span class="sxs-lookup"><span data-stu-id="21416-269">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="21416-270">P1</span><span class="sxs-lookup"><span data-stu-id="21416-270">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="21416-271">Sí</span><span class="sxs-lookup"><span data-stu-id="21416-271">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="21416-272">Sí</span><span class="sxs-lookup"><span data-stu-id="21416-272">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="21416-273">Sí</span><span class="sxs-lookup"><span data-stu-id="21416-273">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="21416-274">Vàlid</span><span class="sxs-lookup"><span data-stu-id="21416-274">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="21416-275">Segons la regla 3, Q1 i Q2 són dues ofertes d'oportunitats diferents, per la qual cosa no poden estimar-se per als mateixos components d'un mateix projecte.</span><span class="sxs-lookup"><span data-stu-id="21416-275">Based on Rule #3, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="21416-276">O2</span><span class="sxs-lookup"><span data-stu-id="21416-276">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="21416-277">T1</span><span class="sxs-lookup"><span data-stu-id="21416-277">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="21416-278">QL1</span><span class="sxs-lookup"><span data-stu-id="21416-278">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="21416-279">P1</span><span class="sxs-lookup"><span data-stu-id="21416-279">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="21416-280">Sí</span><span class="sxs-lookup"><span data-stu-id="21416-280">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="21416-281">Sí</span><span class="sxs-lookup"><span data-stu-id="21416-281">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="21416-282">Sí</span><span class="sxs-lookup"><span data-stu-id="21416-282">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="21416-283">No és vàlid</span><span class="sxs-lookup"><span data-stu-id="21416-283">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../includes/footer-banner.md)]
