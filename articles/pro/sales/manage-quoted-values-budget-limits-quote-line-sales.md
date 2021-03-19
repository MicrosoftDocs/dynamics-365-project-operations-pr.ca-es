---
title: Informació general de les línies d'oferta basades en projectes (bàsic)
description: En aquest tema s'ofereix informació sobre l'ús de línies d'oferta basades en projectes per al treball del projecte. (Pro)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4865c06691fba09eacf5fe6449adfaf542444520
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272961"
---
# <a name="project-based-quote-lines-overview---lite"></a><span data-ttu-id="d9f21-104">Informació general de les línies d'oferta basades en projectes (bàsic)</span><span class="sxs-lookup"><span data-stu-id="d9f21-104">Project-based quote lines overview - lite</span></span>

<span data-ttu-id="d9f21-105">_**S'aplica a:** implementació bàsica: tracte de facturació proforma_</span><span class="sxs-lookup"><span data-stu-id="d9f21-105">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d9f21-106">Les línies d'oferta basades en projectes estan dissenyades per ajudar a estimar el treball del projecte en una interacció.</span><span class="sxs-lookup"><span data-stu-id="d9f21-106">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="d9f21-107">L'estructura d'una línia d'oferta basada en projectes s'amplia per a estimacions de projecte amb els conceptes següents:</span><span class="sxs-lookup"><span data-stu-id="d9f21-107">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="d9f21-108">Mètode de facturació</span><span class="sxs-lookup"><span data-stu-id="d9f21-108">Billing Method</span></span>
- <span data-ttu-id="d9f21-109">Assignació de projectes i tasques</span><span class="sxs-lookup"><span data-stu-id="d9f21-109">Project and Task Mapping</span></span>
- <span data-ttu-id="d9f21-110">Classes de transaccions incloses</span><span class="sxs-lookup"><span data-stu-id="d9f21-110">Included Transaction classes</span></span>
- <span data-ttu-id="d9f21-111">Límit que no s’ha de superar</span><span class="sxs-lookup"><span data-stu-id="d9f21-111">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="d9f21-112">Configuració de la imputabilitat</span><span class="sxs-lookup"><span data-stu-id="d9f21-112">Chargeability setup</span></span>
- <span data-ttu-id="d9f21-113">Estimació mitjançant detalls de la línia d'oferta</span><span class="sxs-lookup"><span data-stu-id="d9f21-113">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="d9f21-114">Clients de la línia d’oferta</span><span class="sxs-lookup"><span data-stu-id="d9f21-114">Quote line Customers</span></span>

<span data-ttu-id="d9f21-115">A la taula següent es proporciona informació sobre els camps de la pestanya **General** de la línia d'oferta basada en projectes.</span><span class="sxs-lookup"><span data-stu-id="d9f21-115">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="d9f21-116">Aquests camps ajuden a configurar la base per a una estimació detallada i des de zero per al treball del projecte.</span><span class="sxs-lookup"><span data-stu-id="d9f21-116">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="d9f21-117">**Camp**</span><span class="sxs-lookup"><span data-stu-id="d9f21-117">**Field**</span></span> | <span data-ttu-id="d9f21-118">**Descripció**</span><span class="sxs-lookup"><span data-stu-id="d9f21-118">**Description**</span></span> | <span data-ttu-id="d9f21-119">**Impacte descendent**</span><span class="sxs-lookup"><span data-stu-id="d9f21-119">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="d9f21-120">Nom</span><span class="sxs-lookup"><span data-stu-id="d9f21-120">Name</span></span> | <span data-ttu-id="d9f21-121">Nom de la línia d'oferta que hauria d'ajudar-vos a identificar el component discret de l'oferta que s'està estimant.</span><span class="sxs-lookup"><span data-stu-id="d9f21-121">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="d9f21-122">Es copia a la línia de contracte del projecte que es crea des d'aquesta línia d'oferta en guanyar l'oferta.</span><span class="sxs-lookup"><span data-stu-id="d9f21-122">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d9f21-123">Mètode de facturació</span><span class="sxs-lookup"><span data-stu-id="d9f21-123">Billing Method</span></span> | <span data-ttu-id="d9f21-124">En una oferta creada a partir d'una oportunitat, aquest valor es copia des del camp corresponent a la línia d'oportunitat.</span><span class="sxs-lookup"><span data-stu-id="d9f21-124">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="d9f21-125">Aquest camp inclou els dos models de contracte principals compatibles amb el Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="d9f21-125">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="d9f21-126">- Preu fix</span><span class="sxs-lookup"><span data-stu-id="d9f21-126">- Fixed price</span></span></br><span data-ttu-id="d9f21-127">- Temps i material.</span><span class="sxs-lookup"><span data-stu-id="d9f21-127">- Time and material.</span></span>| <span data-ttu-id="d9f21-128">El valor d'aquest camp es copia a la línia de contracte del projecte que es crea des d'aquesta línia d'oferta en guanyar l'oferta.</span><span class="sxs-lookup"><span data-stu-id="d9f21-128">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d9f21-129">Project</span><span class="sxs-lookup"><span data-stu-id="d9f21-129">Project</span></span> | <span data-ttu-id="d9f21-130">Utilitzeu aquest camp opcional per identificar el projecte que s'utilitzarà per lliurar el treball en aquesta interacció.</span><span class="sxs-lookup"><span data-stu-id="d9f21-130">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="d9f21-131">Quan un projecte s'assigna a una línia d'oferta, ajuda amb la creació de tasques imputables i també amb l'aportació d'una estimació basada en projectes a la línia d'oferta com a detalls de la línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="d9f21-131">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="d9f21-132">Quan un projecte no està assignat a una línia d'oferta basada en projectes, la estimació s'ha de crear manualment creant cada detall de la línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="d9f21-132">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="d9f21-133">El valor d'aquest camp es copia a la línia de contracte del projecte que es crea des d'aquesta línia d'oferta en guanyar l'oferta.</span><span class="sxs-lookup"><span data-stu-id="d9f21-133">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="d9f21-134">Tasques incloses</span><span class="sxs-lookup"><span data-stu-id="d9f21-134">Included Tasks</span></span> | <span data-ttu-id="d9f21-135">Indica si aquesta línia d'oferta s'utilitza per a totes o algunes de les tasques del projecte seleccionat.</span><span class="sxs-lookup"><span data-stu-id="d9f21-135">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="d9f21-136">Aquest camp té els següents valors possibles:</span><span class="sxs-lookup"><span data-stu-id="d9f21-136">This field has the following possible values:</span></span></br><span data-ttu-id="d9f21-137">- Totes les tasques de projecte</span><span class="sxs-lookup"><span data-stu-id="d9f21-137">- All project tasks</span></span></br><span data-ttu-id="d9f21-138">- Només les tasques de projecte seleccionades</span><span class="sxs-lookup"><span data-stu-id="d9f21-138">- Selected project tasks only</span></span></br><span data-ttu-id="d9f21-139">Un valor en blanc en aquest camp equival a l'opció **Totes les tasques del projecte**.</span><span class="sxs-lookup"><span data-stu-id="d9f21-139">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="d9f21-140">Quan **Només les tasques de projecte seleccionades** se seleccionen a la pàgina del projecte, la pestanya **Configuració de facturació de la tasca** us permet seleccionar tasques específiques per associar-les a aquesta línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="d9f21-140">When **Selected project tasks only** is selected then on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="d9f21-141">El valor d'aquest camp es copia a la línia de contracte del projecte que es crea des d'aquesta línia d'oferta en guanyar l'oferta.</span><span class="sxs-lookup"><span data-stu-id="d9f21-141">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d9f21-142">Inclou el temps</span><span class="sxs-lookup"><span data-stu-id="d9f21-142">Include Time</span></span> | <span data-ttu-id="d9f21-143">Una marca **Sí**/**No** indica si les transaccions de temps o els costos de treball del projecte seleccionat s'inclouran a l'estimació en aquesta línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="d9f21-143">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="d9f21-144">Un valor **No** indica que les transaccions de temps o els costos de treball no s'inclouran a l'estimació en aquesta línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="d9f21-144">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="d9f21-145">Un valor **Sí** indica que les transaccions de temps o els costos de treball s'inclouran a l'estimació en aquesta línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="d9f21-145">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="d9f21-146">El valor d'aquest camp es copia a la línia de contracte del projecte que es crea des d'aquesta línia d'oferta en guanyar l'oferta.</span><span class="sxs-lookup"><span data-stu-id="d9f21-146">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d9f21-147">Inclou la despesa</span><span class="sxs-lookup"><span data-stu-id="d9f21-147">Include Expense</span></span> | <span data-ttu-id="d9f21-148">Una marca **Sí**/**No** indica si els costos de despesa del projecte seleccionat s'inclouran a l'estimació en aquesta línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="d9f21-148">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="d9f21-149">Un valor **No** indica que el cost de despesa no s'inclourà a l'estimació en aquesta línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="d9f21-149">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="d9f21-150">Un valor **Sí** indica que el cost de despesa s'inclourà a l'estimació en aquesta línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="d9f21-150">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="d9f21-151">El valor d'aquest camp es copia a la línia de contracte del projecte que es crea des d'aquesta línia d'oferta en guanyar l'oferta.</span><span class="sxs-lookup"><span data-stu-id="d9f21-151">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d9f21-152">Inclou la taxa</span><span class="sxs-lookup"><span data-stu-id="d9f21-152">Include Fee</span></span> | <span data-ttu-id="d9f21-153">Una marca **Sí**/**No** indica si les taxes del projecte seleccionat s'inclouran a l'estimació en aquesta línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="d9f21-153">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="d9f21-154">Un valor **No** indica que les taxes no s'inclouran a l'estimació en aquesta línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="d9f21-154">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="d9f21-155">Un valor **Sí** indica que les taxes s'inclouran a l'estimació en aquesta línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="d9f21-155">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="d9f21-156">El valor d'aquest camp es copia a la línia de contracte del projecte que es crea des d'aquesta línia d'oferta en guanyar l'oferta.</span><span class="sxs-lookup"><span data-stu-id="d9f21-156">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d9f21-157">Import de l’oferta</span><span class="sxs-lookup"><span data-stu-id="d9f21-157">Quoted Amount</span></span> | <span data-ttu-id="d9f21-158">Això és una quantitat que s'oferirà al client per a tot el treball previst en aquesta línia d'oferta basada en el projecte.</span><span class="sxs-lookup"><span data-stu-id="d9f21-158">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="d9f21-159">En una oferta creada a partir d'una oportunitat, aquest valor es copia des del camp **Pressupost de client** a la línia d'oportunitat.</span><span class="sxs-lookup"><span data-stu-id="d9f21-159">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="d9f21-160">Quan la línia d'oferta basada en projectes té detalls de línia, aquest camp està bloquejat per editar-lo i es resumeix de l'import dels detalls de la línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="d9f21-160">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="d9f21-161">El valor d'aquest camp es copia a la línia de contracte del projecte que es crea des d'aquesta línia d'oferta en guanyar l'oferta.</span><span class="sxs-lookup"><span data-stu-id="d9f21-161">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d9f21-162">Impost estimat</span><span class="sxs-lookup"><span data-stu-id="d9f21-162">Estimated Tax</span></span> | <span data-ttu-id="d9f21-163">Es tracta d'un camp editable per a l'usuari que afegirà l'import de l'impost previst a la línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="d9f21-163">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="d9f21-164">Quan una línia d'oferta basada en projectes té detalls de línia, aquest camp està bloquejat per editar-lo i es resumeix de l'import d'impostos dels detalls de la línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="d9f21-164">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="d9f21-165">El valor d'aquest camp es copia a la línia de contracte del projecte que es crea des d'aquesta línia d'oferta en guanyar l'oferta.</span><span class="sxs-lookup"><span data-stu-id="d9f21-165">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d9f21-166">Import de l’oferta després d’impostos</span><span class="sxs-lookup"><span data-stu-id="d9f21-166">Quoted Amount after Tax</span></span> | <span data-ttu-id="d9f21-167">Aquest camp és l'import de la línia d'oferta després de l'impost i és només de lectura.</span><span class="sxs-lookup"><span data-stu-id="d9f21-167">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="d9f21-168">L'import d'aquest camp es calcula com a *Import de l'oferta + impost*.</span><span class="sxs-lookup"><span data-stu-id="d9f21-168">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="d9f21-169">El valor d'aquest camp es copia a la línia de contracte del projecte que es crea des d'aquesta línia d'oferta en guanyar l'oferta.</span><span class="sxs-lookup"><span data-stu-id="d9f21-169">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d9f21-170">Límit que no s’ha de superar</span><span class="sxs-lookup"><span data-stu-id="d9f21-170">Not-to-exceed Limit</span></span> | <span data-ttu-id="d9f21-171">Aquest camp és editable i només està disponible a les línies d'oferta basades en el projecte que tenen un mètode de facturació **Temps i material**.</span><span class="sxs-lookup"><span data-stu-id="d9f21-171">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="d9f21-172">El valor d'aquest camp es copia a la línia de contracte del projecte que es crea des d'aquesta línia d'oferta en guanyar l'oferta.</span><span class="sxs-lookup"><span data-stu-id="d9f21-172">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d9f21-173">Pressupost del client</span><span class="sxs-lookup"><span data-stu-id="d9f21-173">Customer Budget</span></span> | <span data-ttu-id="d9f21-174">Aquest camp és editable i es copia des del camp corresponent a la línia d'oportunitat si l'oferta es va crear a partir d'una oportunitat.</span><span class="sxs-lookup"><span data-stu-id="d9f21-174">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="d9f21-175">El valor d'aquest camp es copia a la línia de contracte del projecte que es crea des d'aquesta línia d'oferta en guanyar l'oferta.</span><span class="sxs-lookup"><span data-stu-id="d9f21-175">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="d9f21-176">Regles de validació per als camps de la pestanya General de línies d'oferta basades en projectes</span><span class="sxs-lookup"><span data-stu-id="d9f21-176">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="d9f21-177">**Regla 1**: si el camp **Tasques incloses** està en blanc o si està definit com a **Totes les tasques del projecte**, s'inclou un projecte a la línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="d9f21-177">**Rule 1**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project is included in the quote line.</span></span>

<span data-ttu-id="d9f21-178">**Regla 2**: si el camp **Tasques incloses** està en blanc o si està definit com a **Totes les tasques del projecte**, un projecte i una determinada classe de transacció només es poden incloure en una línia d'oferta basada en projectes d'una oferta.</span><span class="sxs-lookup"><span data-stu-id="d9f21-178">**Rule 2**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="d9f21-179">**Regla 3**: si el camp **Tasques incloses** està definit com a **Només les tasques del projecte seleccionades**, un projecte i una determinada classe de transacció es poden incloure en diverses línies d'oferta basades en projectes d'una oferta.</span><span class="sxs-lookup"><span data-stu-id="d9f21-179">**Rule 3**: If the **Included Tasks** field is set to **Selected project tasks only**, a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="d9f21-180">**Regla 4**: si una oportunitat té diverses ofertes, pot haver-hi línies d'ofertes de diverses ofertes que facin referència al mateix projecte i que incloguin la mateixa classe de transacció.</span><span class="sxs-lookup"><span data-stu-id="d9f21-180">**Rule 4**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="d9f21-181">**Regla 5**: si les ofertes no pertanyen a la mateixa oportunitat, no poden incloure el mateix projecte i classe de transacció.</span><span class="sxs-lookup"><span data-stu-id="d9f21-181">**Rule 5**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="d9f21-182">
                    <strong>Oportunitat</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d9f21-182">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="d9f21-183">
                    <strong>Oferta</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d9f21-183">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="d9f21-184">
                    <strong>Línia d’oferta</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d9f21-184">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="d9f21-185">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d9f21-185">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="90" valign="top">
                <p><span data-ttu-id="d9f21-186">
                    <strong>Tasques incloses</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d9f21-186">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="d9f21-187">
                    <strong>Inclou el temps</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d9f21-187">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="d9f21-188">
                    <strong>Inclou la despesa</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d9f21-188">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="d9f21-189">
                    <strong>Inclou</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d9f21-189">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="d9f21-190">
                    <strong>Tarifa</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d9f21-190">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="d9f21-191">
                    <strong>Vàlid/No és vàlid</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d9f21-191">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="d9f21-192">
                    <strong>Motiu</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d9f21-192">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d9f21-193">O1</span><span class="sxs-lookup"><span data-stu-id="d9f21-193">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d9f21-194">T1</span><span class="sxs-lookup"><span data-stu-id="d9f21-194">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9f21-195">QL1</span><span class="sxs-lookup"><span data-stu-id="d9f21-195">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9f21-196">P1</span><span class="sxs-lookup"><span data-stu-id="d9f21-196">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d9f21-197">En blanc</span><span class="sxs-lookup"><span data-stu-id="d9f21-197">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d9f21-198">Sí</span><span class="sxs-lookup"><span data-stu-id="d9f21-198">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d9f21-199">Sí</span><span class="sxs-lookup"><span data-stu-id="d9f21-199">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9f21-200">Sí</span><span class="sxs-lookup"><span data-stu-id="d9f21-200">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d9f21-201">No és vàlid</span><span class="sxs-lookup"><span data-stu-id="d9f21-201">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d9f21-202">Infracció de la regla 2.</span><span class="sxs-lookup"><span data-stu-id="d9f21-202">Violation of Rule #2.</span></span> <span data-ttu-id="d9f21-203">El temps, les despeses i els impostos en el projecte P1 s'inclouen a les línies d'oferta QL1 i QL2.</span><span class="sxs-lookup"><span data-stu-id="d9f21-203">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d9f21-204">O1</span><span class="sxs-lookup"><span data-stu-id="d9f21-204">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d9f21-205">T1</span><span class="sxs-lookup"><span data-stu-id="d9f21-205">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9f21-206">QL2</span><span class="sxs-lookup"><span data-stu-id="d9f21-206">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9f21-207">P1</span><span class="sxs-lookup"><span data-stu-id="d9f21-207">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d9f21-208">En blanc</span><span class="sxs-lookup"><span data-stu-id="d9f21-208">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d9f21-209">Sí</span><span class="sxs-lookup"><span data-stu-id="d9f21-209">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d9f21-210">Sí</span><span class="sxs-lookup"><span data-stu-id="d9f21-210">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9f21-211">Sí</span><span class="sxs-lookup"><span data-stu-id="d9f21-211">Yes</span></span> </p>
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
            <td width="90" valign="top">
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
<span data-ttu-id="d9f21-212">O1</span><span class="sxs-lookup"><span data-stu-id="d9f21-212">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d9f21-213">T1</span><span class="sxs-lookup"><span data-stu-id="d9f21-213">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9f21-214">QL1</span><span class="sxs-lookup"><span data-stu-id="d9f21-214">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9f21-215">P1</span><span class="sxs-lookup"><span data-stu-id="d9f21-215">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d9f21-216">En blanc</span><span class="sxs-lookup"><span data-stu-id="d9f21-216">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d9f21-217">Sí</span><span class="sxs-lookup"><span data-stu-id="d9f21-217">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d9f21-218">No</span><span class="sxs-lookup"><span data-stu-id="d9f21-218">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9f21-219">Sí</span><span class="sxs-lookup"><span data-stu-id="d9f21-219">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d9f21-220">No és vàlid</span><span class="sxs-lookup"><span data-stu-id="d9f21-220">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d9f21-221">Infracció de la regla 2.</span><span class="sxs-lookup"><span data-stu-id="d9f21-221">Violation of Rule #2.</span></span> <span data-ttu-id="d9f21-222">El temps i els impostos en el projecte P1 s'inclouen a les línies d'oferta QL1 i QL2.</span><span class="sxs-lookup"><span data-stu-id="d9f21-222">Time and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d9f21-223">O1</span><span class="sxs-lookup"><span data-stu-id="d9f21-223">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d9f21-224">T1</span><span class="sxs-lookup"><span data-stu-id="d9f21-224">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9f21-225">QL2</span><span class="sxs-lookup"><span data-stu-id="d9f21-225">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9f21-226">P1</span><span class="sxs-lookup"><span data-stu-id="d9f21-226">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d9f21-227">En blanc</span><span class="sxs-lookup"><span data-stu-id="d9f21-227">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d9f21-228">Sí</span><span class="sxs-lookup"><span data-stu-id="d9f21-228">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d9f21-229">Sí</span><span class="sxs-lookup"><span data-stu-id="d9f21-229">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9f21-230">Sí</span><span class="sxs-lookup"><span data-stu-id="d9f21-230">Yes</span></span> </p>
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
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d9f21-231">O1</span><span class="sxs-lookup"><span data-stu-id="d9f21-231">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d9f21-232">T1</span><span class="sxs-lookup"><span data-stu-id="d9f21-232">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9f21-233">QL1</span><span class="sxs-lookup"><span data-stu-id="d9f21-233">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9f21-234">P1</span><span class="sxs-lookup"><span data-stu-id="d9f21-234">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d9f21-235">En blanc</span><span class="sxs-lookup"><span data-stu-id="d9f21-235">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d9f21-236">Sí</span><span class="sxs-lookup"><span data-stu-id="d9f21-236">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d9f21-237">No</span><span class="sxs-lookup"><span data-stu-id="d9f21-237">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9f21-238">Sí</span><span class="sxs-lookup"><span data-stu-id="d9f21-238">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d9f21-239">Vàlid</span><span class="sxs-lookup"><span data-stu-id="d9f21-239">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                  <p>
<span data-ttu-id="d9f21-240">El temps i els impostos en el projecte P1 s'inclouen a QL1.</span><span class="sxs-lookup"><span data-stu-id="d9f21-240">Time and Fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="d9f21-241">La despesa en el projecte P1 s'inclou a QL2.</span><span class="sxs-lookup"><span data-stu-id="d9f21-241">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="d9f21-242">No se superposa el que s'inclou a cada línia d'oferta i és vàlid.</span><span class="sxs-lookup"><span data-stu-id="d9f21-242">There is no overlap in what is being included on each quote line and is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d9f21-243">O1</span><span class="sxs-lookup"><span data-stu-id="d9f21-243">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d9f21-244">T1</span><span class="sxs-lookup"><span data-stu-id="d9f21-244">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9f21-245">QL2</span><span class="sxs-lookup"><span data-stu-id="d9f21-245">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9f21-246">P1</span><span class="sxs-lookup"><span data-stu-id="d9f21-246">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d9f21-247">En blanc</span><span class="sxs-lookup"><span data-stu-id="d9f21-247">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d9f21-248">No</span><span class="sxs-lookup"><span data-stu-id="d9f21-248">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d9f21-249">Sí</span><span class="sxs-lookup"><span data-stu-id="d9f21-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9f21-250">No</span><span class="sxs-lookup"><span data-stu-id="d9f21-250">No</span></span> </p>
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
            <td width="90" valign="top">
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
<span data-ttu-id="d9f21-251">O1</span><span class="sxs-lookup"><span data-stu-id="d9f21-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d9f21-252">T1</span><span class="sxs-lookup"><span data-stu-id="d9f21-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9f21-253">QL1</span><span class="sxs-lookup"><span data-stu-id="d9f21-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9f21-254">P1</span><span class="sxs-lookup"><span data-stu-id="d9f21-254">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d9f21-255">Només les tasques seleccionades</span><span class="sxs-lookup"><span data-stu-id="d9f21-255">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d9f21-256">Sí</span><span class="sxs-lookup"><span data-stu-id="d9f21-256">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d9f21-257">Sí</span><span class="sxs-lookup"><span data-stu-id="d9f21-257">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9f21-258">Sí</span><span class="sxs-lookup"><span data-stu-id="d9f21-258">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d9f21-259">No és vàlid</span><span class="sxs-lookup"><span data-stu-id="d9f21-259">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d9f21-260">Infracció de la regla 2 anterior</span><span class="sxs-lookup"><span data-stu-id="d9f21-260">Violation of Rule #2 above</span></span> </p>
                <p>
<span data-ttu-id="d9f21-261">Q1 inclou el temps, les despeses i els impostos d'un subconjunt de tasques del projecte P1.</span><span class="sxs-lookup"><span data-stu-id="d9f21-261">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="d9f21-262">QL2 inclou el temps, les despeses i els impostos per a tot el projecte P1 i se superposa amb el que s'inclou a Q1.</span><span class="sxs-lookup"><span data-stu-id="d9f21-262">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d9f21-263">O1</span><span class="sxs-lookup"><span data-stu-id="d9f21-263">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d9f21-264">T1</span><span class="sxs-lookup"><span data-stu-id="d9f21-264">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9f21-265">QL2</span><span class="sxs-lookup"><span data-stu-id="d9f21-265">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9f21-266">P1</span><span class="sxs-lookup"><span data-stu-id="d9f21-266">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d9f21-267">En blanc</span><span class="sxs-lookup"><span data-stu-id="d9f21-267">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d9f21-268">Sí</span><span class="sxs-lookup"><span data-stu-id="d9f21-268">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d9f21-269">Sí</span><span class="sxs-lookup"><span data-stu-id="d9f21-269">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9f21-270">Sí</span><span class="sxs-lookup"><span data-stu-id="d9f21-270">Yes</span></span> </p>
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
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d9f21-271">O1</span><span class="sxs-lookup"><span data-stu-id="d9f21-271">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d9f21-272">T1</span><span class="sxs-lookup"><span data-stu-id="d9f21-272">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9f21-273">QL1</span><span class="sxs-lookup"><span data-stu-id="d9f21-273">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9f21-274">P1</span><span class="sxs-lookup"><span data-stu-id="d9f21-274">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d9f21-275">Només les tasques seleccionades</span><span class="sxs-lookup"><span data-stu-id="d9f21-275">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d9f21-276">Sí</span><span class="sxs-lookup"><span data-stu-id="d9f21-276">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d9f21-277">Sí</span><span class="sxs-lookup"><span data-stu-id="d9f21-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9f21-278">Sí</span><span class="sxs-lookup"><span data-stu-id="d9f21-278">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d9f21-279">Vàlid</span><span class="sxs-lookup"><span data-stu-id="d9f21-279">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d9f21-280">Segons la regla 3 anterior,</span><span class="sxs-lookup"><span data-stu-id="d9f21-280">Per Rule #3 above,</span></span> </p>
                <p>
<span data-ttu-id="d9f21-281">Q1 inclou el temps, les despeses i els impostos d'un subconjunt de tasques del projecte P1.</span><span class="sxs-lookup"><span data-stu-id="d9f21-281">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="d9f21-282">QL2 inclou el temps, les despeses i els impostos d'un subconjunt de tasques del projecte P1.</span><span class="sxs-lookup"><span data-stu-id="d9f21-282">QL2 includes Time, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="d9f21-283">L'única validació addicional és pel que fa al subconjunt de tasques a QL1 que són diferents del subconjunt de tasques de QL2.</span><span class="sxs-lookup"><span data-stu-id="d9f21-283">The only additional validation is around the subset of tasks on QL1 which are different from the subset of tasks on QL2.</span></span> <span data-ttu-id="d9f21-284">Això assegura que no hi ha cap superposició.</span><span class="sxs-lookup"><span data-stu-id="d9f21-284">This ensures that there are no overlaps.</span></span> <span data-ttu-id="d9f21-285">Això ho fa el sistema quan s'associen les tasques.</span><span class="sxs-lookup"><span data-stu-id="d9f21-285">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d9f21-286">O1</span><span class="sxs-lookup"><span data-stu-id="d9f21-286">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d9f21-287">T1</span><span class="sxs-lookup"><span data-stu-id="d9f21-287">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9f21-288">QL2</span><span class="sxs-lookup"><span data-stu-id="d9f21-288">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9f21-289">P1</span><span class="sxs-lookup"><span data-stu-id="d9f21-289">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d9f21-290">Només les tasques seleccionades</span><span class="sxs-lookup"><span data-stu-id="d9f21-290">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d9f21-291">Sí</span><span class="sxs-lookup"><span data-stu-id="d9f21-291">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d9f21-292">Sí</span><span class="sxs-lookup"><span data-stu-id="d9f21-292">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9f21-293">Sí</span><span class="sxs-lookup"><span data-stu-id="d9f21-293">Yes</span></span> </p>
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
            <td width="90" valign="top">
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
<span data-ttu-id="d9f21-294">O1</span><span class="sxs-lookup"><span data-stu-id="d9f21-294">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d9f21-295">T1</span><span class="sxs-lookup"><span data-stu-id="d9f21-295">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9f21-296">QL1</span><span class="sxs-lookup"><span data-stu-id="d9f21-296">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9f21-297">P1</span><span class="sxs-lookup"><span data-stu-id="d9f21-297">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d9f21-298">Totes les tasques del projecte o en blanc</span><span class="sxs-lookup"><span data-stu-id="d9f21-298">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d9f21-299">Sí</span><span class="sxs-lookup"><span data-stu-id="d9f21-299">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d9f21-300">Sí</span><span class="sxs-lookup"><span data-stu-id="d9f21-300">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9f21-301">Sí</span><span class="sxs-lookup"><span data-stu-id="d9f21-301">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="d9f21-302">Vàlid</span><span class="sxs-lookup"><span data-stu-id="d9f21-302">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d9f21-303">Segons la regla 5, Q1 i Q2 són dues ofertes de la mateixa oportunitat, per la qual cosa poden estimar-se per als mateixos components d'un projecte.</span><span class="sxs-lookup"><span data-stu-id="d9f21-303">Based on Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d9f21-304">O1</span><span class="sxs-lookup"><span data-stu-id="d9f21-304">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d9f21-305">T2</span><span class="sxs-lookup"><span data-stu-id="d9f21-305">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9f21-306">QL1</span><span class="sxs-lookup"><span data-stu-id="d9f21-306">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9f21-307">P1</span><span class="sxs-lookup"><span data-stu-id="d9f21-307">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d9f21-308">Totes les tasques del projecte o en blanc</span><span class="sxs-lookup"><span data-stu-id="d9f21-308">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d9f21-309">Sí</span><span class="sxs-lookup"><span data-stu-id="d9f21-309">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d9f21-310">Sí</span><span class="sxs-lookup"><span data-stu-id="d9f21-310">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9f21-311">Sí</span><span class="sxs-lookup"><span data-stu-id="d9f21-311">Yes</span></span> </p>
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
            <td width="90" valign="top">
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
<span data-ttu-id="d9f21-312">O1</span><span class="sxs-lookup"><span data-stu-id="d9f21-312">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d9f21-313">T1</span><span class="sxs-lookup"><span data-stu-id="d9f21-313">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9f21-314">QL1</span><span class="sxs-lookup"><span data-stu-id="d9f21-314">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9f21-315">P1</span><span class="sxs-lookup"><span data-stu-id="d9f21-315">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d9f21-316">Totes les tasques del projecte o en blanc</span><span class="sxs-lookup"><span data-stu-id="d9f21-316">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d9f21-317">Sí</span><span class="sxs-lookup"><span data-stu-id="d9f21-317">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d9f21-318">Sí</span><span class="sxs-lookup"><span data-stu-id="d9f21-318">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9f21-319">Sí</span><span class="sxs-lookup"><span data-stu-id="d9f21-319">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="d9f21-320">Vàlid</span><span class="sxs-lookup"><span data-stu-id="d9f21-320">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d9f21-321">Segons la regla 4, Q1 i Q2 són dues ofertes d'oportunitats diferents, per la qual cosa no poden estimar-se per als mateixos components d'un mateix projecte.</span><span class="sxs-lookup"><span data-stu-id="d9f21-321">Based on Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d9f21-322">O2</span><span class="sxs-lookup"><span data-stu-id="d9f21-322">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d9f21-323">T1</span><span class="sxs-lookup"><span data-stu-id="d9f21-323">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9f21-324">QL1</span><span class="sxs-lookup"><span data-stu-id="d9f21-324">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9f21-325">P1</span><span class="sxs-lookup"><span data-stu-id="d9f21-325">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d9f21-326">Totes les tasques del projecte o en blanc</span><span class="sxs-lookup"><span data-stu-id="d9f21-326">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d9f21-327">Sí</span><span class="sxs-lookup"><span data-stu-id="d9f21-327">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d9f21-328">Sí</span><span class="sxs-lookup"><span data-stu-id="d9f21-328">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9f21-329">Sí</span><span class="sxs-lookup"><span data-stu-id="d9f21-329">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="d9f21-330">No és vàlid</span><span class="sxs-lookup"><span data-stu-id="d9f21-330">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]