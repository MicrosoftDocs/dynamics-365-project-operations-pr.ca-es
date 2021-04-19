---
title: Informació general de les línies d'oferta de projecte
description: Aquest tema proporciona informació sobre l'ús de les línies d'oferta del projecte per al treball del projecte.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: fa48a90c275eae1b0c0dbce685ae718dd9674c88
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858011"
---
# <a name="project-quote-lines-overview"></a><span data-ttu-id="b49a2-103">Informació general de les línies d'oferta de projecte</span><span class="sxs-lookup"><span data-stu-id="b49a2-103">Project quote lines overview</span></span>

<span data-ttu-id="b49a2-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_</span><span class="sxs-lookup"><span data-stu-id="b49a2-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="b49a2-105">Les línies d'oferta basades en projectes estan dissenyades per ajudar a estimar el treball del projecte en una interacció.</span><span class="sxs-lookup"><span data-stu-id="b49a2-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="b49a2-106">L'estructura d'una línia d'oferta basada en projectes s'amplia per a estimacions de projecte amb els conceptes següents:</span><span class="sxs-lookup"><span data-stu-id="b49a2-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="b49a2-107">Mètode de facturació</span><span class="sxs-lookup"><span data-stu-id="b49a2-107">Billing Method</span></span>
- <span data-ttu-id="b49a2-108">Assignació de projectes</span><span class="sxs-lookup"><span data-stu-id="b49a2-108">Project Mapping</span></span>
- <span data-ttu-id="b49a2-109">Classes de transaccions incloses</span><span class="sxs-lookup"><span data-stu-id="b49a2-109">Included Transaction classes</span></span>
- <span data-ttu-id="b49a2-110">Límit que no s’ha de superar</span><span class="sxs-lookup"><span data-stu-id="b49a2-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="b49a2-111">Configuració de la imputabilitat</span><span class="sxs-lookup"><span data-stu-id="b49a2-111">Chargeability setup</span></span>
- <span data-ttu-id="b49a2-112">Estimació mitjançant detalls de la línia d'oferta</span><span class="sxs-lookup"><span data-stu-id="b49a2-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="b49a2-113">Clients de la línia d’oferta</span><span class="sxs-lookup"><span data-stu-id="b49a2-113">Quote line Customers</span></span>

<span data-ttu-id="b49a2-114">A la taula següent es proporciona informació sobre els camps de la pestanya **General** de la línia d'oferta basada en projectes.</span><span class="sxs-lookup"><span data-stu-id="b49a2-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="b49a2-115">Aquests camps ajuden a configurar la base per a una estimació detallada i des de zero per al treball del projecte.</span><span class="sxs-lookup"><span data-stu-id="b49a2-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="b49a2-116">**Camp**</span><span class="sxs-lookup"><span data-stu-id="b49a2-116">**Field**</span></span> | <span data-ttu-id="b49a2-117">**Descripció**</span><span class="sxs-lookup"><span data-stu-id="b49a2-117">**Description**</span></span> | <span data-ttu-id="b49a2-118">**Impacte descendent**</span><span class="sxs-lookup"><span data-stu-id="b49a2-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="b49a2-119">Nom</span><span class="sxs-lookup"><span data-stu-id="b49a2-119">Name</span></span> | <span data-ttu-id="b49a2-120">Nom de la línia d'oferta que hauria d'ajudar-vos a identificar el component discret de l'oferta que s'està estimant.</span><span class="sxs-lookup"><span data-stu-id="b49a2-120">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="b49a2-121">Es copia a la línia de contracte del projecte que es crea des d'aquesta línia d'oferta en guanyar l'oferta.</span><span class="sxs-lookup"><span data-stu-id="b49a2-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="b49a2-122">Mètode de facturació</span><span class="sxs-lookup"><span data-stu-id="b49a2-122">Billing Method</span></span> | <span data-ttu-id="b49a2-123">En una oferta creada a partir d'una oportunitat, aquest valor es copia des del camp corresponent a la línia d'oportunitat.</span><span class="sxs-lookup"><span data-stu-id="b49a2-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="b49a2-124">Aquest camp inclou els dos models de contracte principals compatibles amb el Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="b49a2-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="b49a2-125">- Preu fix</span><span class="sxs-lookup"><span data-stu-id="b49a2-125">- Fixed price</span></span></br><span data-ttu-id="b49a2-126">- Temps i material.</span><span class="sxs-lookup"><span data-stu-id="b49a2-126">- Time and material.</span></span>| <span data-ttu-id="b49a2-127">El valor d'aquest camp es copia a la línia de contracte del projecte que es crea des d'aquesta línia d'oferta en guanyar l'oferta.</span><span class="sxs-lookup"><span data-stu-id="b49a2-127">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="b49a2-128">Project</span><span class="sxs-lookup"><span data-stu-id="b49a2-128">Project</span></span> | <span data-ttu-id="b49a2-129">Utilitzeu aquest camp opcional per identificar el projecte que s'utilitzarà per lliurar el treball en aquesta interacció.</span><span class="sxs-lookup"><span data-stu-id="b49a2-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="b49a2-130">Quan un projecte s'assigna a una línia d'oferta, ajuda amb la creació de tasques imputables i també amb l'aportació d'una estimació basada en projectes a la línia d'oferta com a detalls de la línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="b49a2-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="b49a2-131">Quan un projecte no està assignat a una línia d'oferta basada en projectes, la estimació s'ha de crear manualment creant cada detall de la línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="b49a2-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="b49a2-132">El valor d'aquest camp es copia a la línia de contracte del projecte que es crea des d'aquesta línia d'oferta en guanyar l'oferta.</span><span class="sxs-lookup"><span data-stu-id="b49a2-132">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="b49a2-133">Inclou el temps</span><span class="sxs-lookup"><span data-stu-id="b49a2-133">Include Time</span></span> | <span data-ttu-id="b49a2-134">Una marca **Sí**/**No** indica si les transaccions de temps o els costos de treball del projecte seleccionat s'inclouran a l'estimació en aquesta línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="b49a2-134">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="b49a2-135">Un valor **No** indica que les transaccions de temps o els costos de treball no s'inclouran a l'estimació en aquesta línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="b49a2-135">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="b49a2-136">Un valor **Sí** indica que les transaccions de temps o els costos de treball s'inclouran a l'estimació en aquesta línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="b49a2-136">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="b49a2-137">El valor d'aquest camp es copia a la línia de contracte del projecte que es crea des d'aquesta línia d'oferta en guanyar l'oferta.</span><span class="sxs-lookup"><span data-stu-id="b49a2-137">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="b49a2-138">Inclou la despesa</span><span class="sxs-lookup"><span data-stu-id="b49a2-138">Include Expense</span></span> | <span data-ttu-id="b49a2-139">Una marca **Sí**/**No** indica si els costos de despesa del projecte seleccionat s'inclouran a l'estimació en aquesta línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="b49a2-139">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="b49a2-140">Un valor **No** indica que el cost de despesa no s'inclourà a l'estimació en aquesta línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="b49a2-140">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="b49a2-141">Un valor **Sí** indica que el cost de despesa s'inclourà a l'estimació en aquesta línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="b49a2-141">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="b49a2-142">El valor d'aquest camp es copia a la línia de contracte del projecte que es crea des d'aquesta línia d'oferta en guanyar l'oferta.</span><span class="sxs-lookup"><span data-stu-id="b49a2-142">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="b49a2-143">Inclou la taxa</span><span class="sxs-lookup"><span data-stu-id="b49a2-143">Include Fee</span></span> | <span data-ttu-id="b49a2-144">Una marca **Sí**/**No** indica si les taxes del projecte seleccionat s'inclouran a l'estimació en aquesta línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="b49a2-144">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="b49a2-145">Un valor **No** indica que les taxes no s'inclouran a l'estimació en aquesta línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="b49a2-145">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="b49a2-146">Un valor **Sí** indica que les taxes s'inclouran a l'estimació en aquesta línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="b49a2-146">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="b49a2-147">El valor d'aquest camp es copia a la línia de contracte del projecte que es crea des d'aquesta línia d'oferta en guanyar l'oferta.</span><span class="sxs-lookup"><span data-stu-id="b49a2-147">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="b49a2-148">Import de l’oferta</span><span class="sxs-lookup"><span data-stu-id="b49a2-148">Quoted Amount</span></span> | <span data-ttu-id="b49a2-149">Això és una quantitat que s'oferirà al client per a tot el treball previst en aquesta línia d'oferta basada en el projecte.</span><span class="sxs-lookup"><span data-stu-id="b49a2-149">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="b49a2-150">En una oferta creada a partir d'una oportunitat, aquest valor es copia des del camp **Pressupost de client** a la línia d'oportunitat.</span><span class="sxs-lookup"><span data-stu-id="b49a2-150">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="b49a2-151">Quan la línia d'oferta basada en projectes té detalls de línia, aquest camp està bloquejat per editar-lo i es resumeix de l'import dels detalls de la línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="b49a2-151">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="b49a2-152">El valor d'aquest camp es copia a la línia de contracte del projecte que es crea des d'aquesta línia d'oferta en guanyar l'oferta.</span><span class="sxs-lookup"><span data-stu-id="b49a2-152">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="b49a2-153">Impost estimat</span><span class="sxs-lookup"><span data-stu-id="b49a2-153">Estimated Tax</span></span> | <span data-ttu-id="b49a2-154">Es tracta d'un camp editable per a l'usuari que afegirà l'import de l'impost previst a la línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="b49a2-154">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="b49a2-155">Quan una línia d'oferta basada en projectes té detalls de línia, aquest camp està bloquejat per editar-lo i es resumeix de l'import d'impostos dels detalls de la línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="b49a2-155">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="b49a2-156">El valor d'aquest camp es copia a la línia de contracte del projecte que es crea des d'aquesta línia d'oferta en guanyar l'oferta.</span><span class="sxs-lookup"><span data-stu-id="b49a2-156">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="b49a2-157">Import de l’oferta després d’impostos</span><span class="sxs-lookup"><span data-stu-id="b49a2-157">Quoted Amount after Tax</span></span> | <span data-ttu-id="b49a2-158">Aquest camp és l'import de la línia d'oferta després de l'impost i és només de lectura.</span><span class="sxs-lookup"><span data-stu-id="b49a2-158">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="b49a2-159">L'import d'aquest camp es calcula com a *Import de l'oferta + impost*.</span><span class="sxs-lookup"><span data-stu-id="b49a2-159">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="b49a2-160">El valor d'aquest camp es copia a la línia de contracte del projecte que es crea des d'aquesta línia d'oferta en guanyar l'oferta.</span><span class="sxs-lookup"><span data-stu-id="b49a2-160">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="b49a2-161">Límit que no s’ha de superar</span><span class="sxs-lookup"><span data-stu-id="b49a2-161">Not-to-exceed Limit</span></span> | <span data-ttu-id="b49a2-162">Aquest camp és editable i només està disponible a les línies d'oferta basades en el projecte que tenen un mètode de facturació **Temps i material**.</span><span class="sxs-lookup"><span data-stu-id="b49a2-162">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="b49a2-163">El valor d'aquest camp es copia a la línia de contracte del projecte que es crea des d'aquesta línia d'oferta en guanyar l'oferta.</span><span class="sxs-lookup"><span data-stu-id="b49a2-163">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="b49a2-164">Pressupost del client</span><span class="sxs-lookup"><span data-stu-id="b49a2-164">Customer Budget</span></span> | <span data-ttu-id="b49a2-165">Aquest camp és editable i es copia des del camp corresponent a la línia d'oportunitat si l'oferta es va crear a partir d'una oportunitat.</span><span class="sxs-lookup"><span data-stu-id="b49a2-165">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="b49a2-166">El valor d'aquest camp es copia a la línia de contracte del projecte que es crea des d'aquesta línia d'oferta en guanyar l'oferta.</span><span class="sxs-lookup"><span data-stu-id="b49a2-166">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |

## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="b49a2-167">Regles de validació per als camps de la pestanya General de línies d'oferta basades en projectes</span><span class="sxs-lookup"><span data-stu-id="b49a2-167">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="b49a2-168">**Regla 1**: una determinada classe de transacció del projecte seleccionat només es pot incloure en una línia d'oferta basada en projectes d'una oferta.</span><span class="sxs-lookup"><span data-stu-id="b49a2-168">**Rule 1**: A certain transaction class on the selected project can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="b49a2-169">**Regla 2**: si una oportunitat té diverses ofertes, pot haver-hi línies d'ofertes de diverses ofertes que facin referència al mateix projecte i que incloguin la mateixa classe de transacció.</span><span class="sxs-lookup"><span data-stu-id="b49a2-169">**Rule 2**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="b49a2-170">**Regla 3**: si les ofertes no pertanyen a la mateixa oportunitat, no poden incloure el mateix projecte i classe de transacció.</span><span class="sxs-lookup"><span data-stu-id="b49a2-170">**Rule 3**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="1" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="b49a2-171">
                    <strong>Oportunitat</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b49a2-171">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="b49a2-172">
                    <strong>Oferta</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b49a2-172">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="b49a2-173">
                    <strong>Línia d’oferta</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b49a2-173">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="b49a2-174">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b49a2-174">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="b49a2-175">
                    <strong>Inclou el temps</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b49a2-175">
                    <strong>Include time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="b49a2-176">
                    <strong>Inclou la despesa</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b49a2-176">
                    <strong>Include expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="b49a2-177">
                    <strong>Inclou</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b49a2-177">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="b49a2-178">
                    <strong>Tarifa</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b49a2-178">
                    <strong>fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="b49a2-179">
                    <strong>Vàlid/No és vàlid</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b49a2-179">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="b49a2-180">
                    <strong>Motiu</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b49a2-180">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="b49a2-181">O1</span><span class="sxs-lookup"><span data-stu-id="b49a2-181">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="b49a2-182">T1</span><span class="sxs-lookup"><span data-stu-id="b49a2-182">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b49a2-183">QL1</span><span class="sxs-lookup"><span data-stu-id="b49a2-183">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b49a2-184">P1</span><span class="sxs-lookup"><span data-stu-id="b49a2-184">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="b49a2-185">Sí</span><span class="sxs-lookup"><span data-stu-id="b49a2-185">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="b49a2-186">Sí</span><span class="sxs-lookup"><span data-stu-id="b49a2-186">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b49a2-187">Sí</span><span class="sxs-lookup"><span data-stu-id="b49a2-187">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="b49a2-188">No és vàlid</span><span class="sxs-lookup"><span data-stu-id="b49a2-188">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="b49a2-189">Infracció de la regla 1.</span><span class="sxs-lookup"><span data-stu-id="b49a2-189">Violation of Rule #1.</span></span> <span data-ttu-id="b49a2-190">El temps, les despeses i els impostos en el projecte P1 s'inclouen a les línies d'oferta QL1 i QL2.</span><span class="sxs-lookup"><span data-stu-id="b49a2-190">Time, Expense, and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="b49a2-191">O1</span><span class="sxs-lookup"><span data-stu-id="b49a2-191">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="b49a2-192">T1</span><span class="sxs-lookup"><span data-stu-id="b49a2-192">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b49a2-193">QL2</span><span class="sxs-lookup"><span data-stu-id="b49a2-193">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b49a2-194">P1</span><span class="sxs-lookup"><span data-stu-id="b49a2-194">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="b49a2-195">Sí</span><span class="sxs-lookup"><span data-stu-id="b49a2-195">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="b49a2-196">Sí</span><span class="sxs-lookup"><span data-stu-id="b49a2-196">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b49a2-197">Sí</span><span class="sxs-lookup"><span data-stu-id="b49a2-197">Yes</span></span> </p>
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
<span data-ttu-id="b49a2-198">O1</span><span class="sxs-lookup"><span data-stu-id="b49a2-198">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="b49a2-199">T1</span><span class="sxs-lookup"><span data-stu-id="b49a2-199">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b49a2-200">QL1</span><span class="sxs-lookup"><span data-stu-id="b49a2-200">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b49a2-201">P1</span><span class="sxs-lookup"><span data-stu-id="b49a2-201">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="b49a2-202">Sí</span><span class="sxs-lookup"><span data-stu-id="b49a2-202">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="b49a2-203">No</span><span class="sxs-lookup"><span data-stu-id="b49a2-203">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b49a2-204">Sí</span><span class="sxs-lookup"><span data-stu-id="b49a2-204">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="b49a2-205">No és vàlid</span><span class="sxs-lookup"><span data-stu-id="b49a2-205">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="b49a2-206">Infracció de la regla 1.</span><span class="sxs-lookup"><span data-stu-id="b49a2-206">Violation of Rule #1.</span></span> <span data-ttu-id="b49a2-207">El temps i els impostos en el projecte P1 s'inclouen a les línies d'oferta QL1 i QL2.</span><span class="sxs-lookup"><span data-stu-id="b49a2-207">Time and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="b49a2-208">O1</span><span class="sxs-lookup"><span data-stu-id="b49a2-208">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="b49a2-209">T1</span><span class="sxs-lookup"><span data-stu-id="b49a2-209">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b49a2-210">QL2</span><span class="sxs-lookup"><span data-stu-id="b49a2-210">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b49a2-211">P1</span><span class="sxs-lookup"><span data-stu-id="b49a2-211">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="b49a2-212">Sí</span><span class="sxs-lookup"><span data-stu-id="b49a2-212">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="b49a2-213">Sí</span><span class="sxs-lookup"><span data-stu-id="b49a2-213">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b49a2-214">Sí</span><span class="sxs-lookup"><span data-stu-id="b49a2-214">Yes</span></span> </p>
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
<span data-ttu-id="b49a2-215">O1</span><span class="sxs-lookup"><span data-stu-id="b49a2-215">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="b49a2-216">T1</span><span class="sxs-lookup"><span data-stu-id="b49a2-216">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b49a2-217">QL1</span><span class="sxs-lookup"><span data-stu-id="b49a2-217">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b49a2-218">P1</span><span class="sxs-lookup"><span data-stu-id="b49a2-218">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="b49a2-219">Sí</span><span class="sxs-lookup"><span data-stu-id="b49a2-219">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="b49a2-220">No</span><span class="sxs-lookup"><span data-stu-id="b49a2-220">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b49a2-221">Sí</span><span class="sxs-lookup"><span data-stu-id="b49a2-221">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="b49a2-222">Vàlid</span><span class="sxs-lookup"><span data-stu-id="b49a2-222">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                 <p>
<span data-ttu-id="b49a2-223">El temps i els impostos en el projecte P1 s'inclouen a QL1.</span><span class="sxs-lookup"><span data-stu-id="b49a2-223">Time and fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="b49a2-224">La despesa en el projecte P1 s'inclou a QL2.</span><span class="sxs-lookup"><span data-stu-id="b49a2-224">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="b49a2-225">No se superposa el que s'inclou a cada línia d'oferta i per tant és vàlid.</span><span class="sxs-lookup"><span data-stu-id="b49a2-225">There is no overlap in what is being included on each quote line so it is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="b49a2-226">O1</span><span class="sxs-lookup"><span data-stu-id="b49a2-226">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="b49a2-227">T1</span><span class="sxs-lookup"><span data-stu-id="b49a2-227">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b49a2-228">QL2</span><span class="sxs-lookup"><span data-stu-id="b49a2-228">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b49a2-229">P1</span><span class="sxs-lookup"><span data-stu-id="b49a2-229">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="b49a2-230">No</span><span class="sxs-lookup"><span data-stu-id="b49a2-230">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="b49a2-231">Sí</span><span class="sxs-lookup"><span data-stu-id="b49a2-231">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b49a2-232">No</span><span class="sxs-lookup"><span data-stu-id="b49a2-232">No</span></span> </p>
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
<span data-ttu-id="b49a2-233">O1</span><span class="sxs-lookup"><span data-stu-id="b49a2-233">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="b49a2-234">T1</span><span class="sxs-lookup"><span data-stu-id="b49a2-234">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b49a2-235">QL1</span><span class="sxs-lookup"><span data-stu-id="b49a2-235">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b49a2-236">P1</span><span class="sxs-lookup"><span data-stu-id="b49a2-236">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="b49a2-237">Sí</span><span class="sxs-lookup"><span data-stu-id="b49a2-237">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="b49a2-238">Sí</span><span class="sxs-lookup"><span data-stu-id="b49a2-238">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b49a2-239">Sí</span><span class="sxs-lookup"><span data-stu-id="b49a2-239">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="b49a2-240">No és vàlid</span><span class="sxs-lookup"><span data-stu-id="b49a2-240">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="b49a2-241">Infracció de la regla 1 anterior</span><span class="sxs-lookup"><span data-stu-id="b49a2-241">Violation of Rule #1 above</span></span> </p>
                <p>
<span data-ttu-id="b49a2-242">Q1 inclou el temps, les despeses i els impostos del projecte P1 sencer.</span><span class="sxs-lookup"><span data-stu-id="b49a2-242">Q1 includes Time, Expenses, and Fees for the whole project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="b49a2-243">QL2 inclou el temps, les despeses i els impostos per a tot el projecte P1 i se superposa amb el que s'inclou a Q1.</span><span class="sxs-lookup"><span data-stu-id="b49a2-243">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="b49a2-244">O1</span><span class="sxs-lookup"><span data-stu-id="b49a2-244">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="b49a2-245">T1</span><span class="sxs-lookup"><span data-stu-id="b49a2-245">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b49a2-246">QL2</span><span class="sxs-lookup"><span data-stu-id="b49a2-246">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b49a2-247">P1</span><span class="sxs-lookup"><span data-stu-id="b49a2-247">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="b49a2-248">Sí</span><span class="sxs-lookup"><span data-stu-id="b49a2-248">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="b49a2-249">Sí</span><span class="sxs-lookup"><span data-stu-id="b49a2-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b49a2-250">Sí</span><span class="sxs-lookup"><span data-stu-id="b49a2-250">Yes</span></span> </p>
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
<span data-ttu-id="b49a2-251">O1</span><span class="sxs-lookup"><span data-stu-id="b49a2-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="b49a2-252">T1</span><span class="sxs-lookup"><span data-stu-id="b49a2-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b49a2-253">QL1</span><span class="sxs-lookup"><span data-stu-id="b49a2-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b49a2-254">P1</span><span class="sxs-lookup"><span data-stu-id="b49a2-254">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="b49a2-255">Sí</span><span class="sxs-lookup"><span data-stu-id="b49a2-255">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="b49a2-256">Sí</span><span class="sxs-lookup"><span data-stu-id="b49a2-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b49a2-257">Sí</span><span class="sxs-lookup"><span data-stu-id="b49a2-257">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="b49a2-258">Vàlid</span><span class="sxs-lookup"><span data-stu-id="b49a2-258">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="b49a2-259">Segons la regla 2, Q1 i Q2 són dues ofertes de la mateixa oportunitat, per la qual cosa poden estimar-se per als mateixos components d'un projecte.</span><span class="sxs-lookup"><span data-stu-id="b49a2-259">Based on Rule #2, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="b49a2-260">O1</span><span class="sxs-lookup"><span data-stu-id="b49a2-260">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="b49a2-261">T2</span><span class="sxs-lookup"><span data-stu-id="b49a2-261">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b49a2-262">QL1 a Q2</span><span class="sxs-lookup"><span data-stu-id="b49a2-262">QL1 on Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b49a2-263">P1</span><span class="sxs-lookup"><span data-stu-id="b49a2-263">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="b49a2-264">Sí</span><span class="sxs-lookup"><span data-stu-id="b49a2-264">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="b49a2-265">Sí</span><span class="sxs-lookup"><span data-stu-id="b49a2-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b49a2-266">Sí</span><span class="sxs-lookup"><span data-stu-id="b49a2-266">Yes</span></span> </p>
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
<span data-ttu-id="b49a2-267">O1</span><span class="sxs-lookup"><span data-stu-id="b49a2-267">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="b49a2-268">T1</span><span class="sxs-lookup"><span data-stu-id="b49a2-268">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b49a2-269">QL1</span><span class="sxs-lookup"><span data-stu-id="b49a2-269">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b49a2-270">P1</span><span class="sxs-lookup"><span data-stu-id="b49a2-270">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="b49a2-271">Sí</span><span class="sxs-lookup"><span data-stu-id="b49a2-271">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="b49a2-272">Sí</span><span class="sxs-lookup"><span data-stu-id="b49a2-272">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b49a2-273">Sí</span><span class="sxs-lookup"><span data-stu-id="b49a2-273">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="b49a2-274">Vàlid</span><span class="sxs-lookup"><span data-stu-id="b49a2-274">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="b49a2-275">Segons la regla 3, Q1 i Q2 són dues ofertes d'oportunitats diferents, per la qual cosa no poden estimar-se per als mateixos components d'un mateix projecte.</span><span class="sxs-lookup"><span data-stu-id="b49a2-275">Based on Rule #3, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="b49a2-276">O2</span><span class="sxs-lookup"><span data-stu-id="b49a2-276">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="b49a2-277">T1</span><span class="sxs-lookup"><span data-stu-id="b49a2-277">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b49a2-278">QL1</span><span class="sxs-lookup"><span data-stu-id="b49a2-278">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b49a2-279">P1</span><span class="sxs-lookup"><span data-stu-id="b49a2-279">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="b49a2-280">Sí</span><span class="sxs-lookup"><span data-stu-id="b49a2-280">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="b49a2-281">Sí</span><span class="sxs-lookup"><span data-stu-id="b49a2-281">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="b49a2-282">Sí</span><span class="sxs-lookup"><span data-stu-id="b49a2-282">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="b49a2-283">No és vàlid</span><span class="sxs-lookup"><span data-stu-id="b49a2-283">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../includes/footer-banner.md)]
