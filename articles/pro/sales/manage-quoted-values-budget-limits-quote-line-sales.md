---
title: Informació general de les línies d'oferta basades en projectes
description: En aquest tema s'ofereix informació sobre l'ús de línies d'oferta basades en projectes per al treball del projecte.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 32337b05f09ef7c5b84fdff9870744d6367e2693
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994844"
---
# <a name="project-based-quote-lines-overview"></a><span data-ttu-id="d7ee6-103">Informació general de les línies d'oferta basades en projectes</span><span class="sxs-lookup"><span data-stu-id="d7ee6-103">Project-based quote lines overview</span></span> 

<span data-ttu-id="d7ee6-104">_**S'aplica a:** Implementació bàsica: tracte de facturació proforma, Project Operations per a escenaris basats en recursos/sense cotització_</span><span class="sxs-lookup"><span data-stu-id="d7ee6-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="d7ee6-105">Les línies d'oferta basades en projectes estan dissenyades per ajudar a estimar el treball del projecte en una interacció.</span><span class="sxs-lookup"><span data-stu-id="d7ee6-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="d7ee6-106">L'estructura d'una línia d'oferta basada en projectes s'amplia per a estimacions de projecte amb els conceptes següents:</span><span class="sxs-lookup"><span data-stu-id="d7ee6-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="d7ee6-107">Mètode de facturació</span><span class="sxs-lookup"><span data-stu-id="d7ee6-107">Billing Method</span></span>
- <span data-ttu-id="d7ee6-108">Assignació de projectes i tasques</span><span class="sxs-lookup"><span data-stu-id="d7ee6-108">Project and Task Mapping</span></span>
- <span data-ttu-id="d7ee6-109">Classes de transaccions incloses</span><span class="sxs-lookup"><span data-stu-id="d7ee6-109">Included Transaction classes</span></span>
- <span data-ttu-id="d7ee6-110">Límit que no s’ha de superar</span><span class="sxs-lookup"><span data-stu-id="d7ee6-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="d7ee6-111">Configuració de la imputabilitat</span><span class="sxs-lookup"><span data-stu-id="d7ee6-111">Chargeability setup</span></span>
- <span data-ttu-id="d7ee6-112">Estimació mitjançant detalls de la línia d'oferta</span><span class="sxs-lookup"><span data-stu-id="d7ee6-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="d7ee6-113">Clients de la línia d’oferta</span><span class="sxs-lookup"><span data-stu-id="d7ee6-113">Quote line Customers</span></span>

<span data-ttu-id="d7ee6-114">A la taula següent es proporciona informació sobre els camps de la pestanya **General** de la línia d'oferta basada en projectes.</span><span class="sxs-lookup"><span data-stu-id="d7ee6-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="d7ee6-115">Aquests camps ajuden a configurar la base per a una estimació detallada i des de zero per al treball del projecte.</span><span class="sxs-lookup"><span data-stu-id="d7ee6-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="d7ee6-116">**Camp**</span><span class="sxs-lookup"><span data-stu-id="d7ee6-116">**Field**</span></span> | <span data-ttu-id="d7ee6-117">**Descripció**</span><span class="sxs-lookup"><span data-stu-id="d7ee6-117">**Description**</span></span> | <span data-ttu-id="d7ee6-118">**Impacte descendent**</span><span class="sxs-lookup"><span data-stu-id="d7ee6-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="d7ee6-119">Nom</span><span class="sxs-lookup"><span data-stu-id="d7ee6-119">Name</span></span> | <span data-ttu-id="d7ee6-120">El nom de la línia d'oferta que us ajuda a identificar el component discret de l'oferta que s'està calculant.</span><span class="sxs-lookup"><span data-stu-id="d7ee6-120">The name of quote line that helps you to identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="d7ee6-121">Es copia a la línia de contracte del projecte que es crea des d'aquesta línia d'oferta en guanyar l'oferta.</span><span class="sxs-lookup"><span data-stu-id="d7ee6-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d7ee6-122">Mètode de facturació</span><span class="sxs-lookup"><span data-stu-id="d7ee6-122">Billing Method</span></span> | <span data-ttu-id="d7ee6-123">En una oferta creada a partir d'una oportunitat, aquest valor es copia des del camp corresponent a la línia d'oportunitat.</span><span class="sxs-lookup"><span data-stu-id="d7ee6-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="d7ee6-124">Aquest camp inclou els dos models de contracte principals compatibles amb el Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="d7ee6-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="d7ee6-125">- Preu fix</span><span class="sxs-lookup"><span data-stu-id="d7ee6-125">- Fixed price</span></span></br><span data-ttu-id="d7ee6-126">- Temps i material.</span><span class="sxs-lookup"><span data-stu-id="d7ee6-126">- Time and material.</span></span>| <span data-ttu-id="d7ee6-127">Aquest valor es copia a la línia de contracte del projecte que es crea a partir d'aquesta línia d'oferta quan es guanya l'oferta.</span><span class="sxs-lookup"><span data-stu-id="d7ee6-127">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d7ee6-128">Project</span><span class="sxs-lookup"><span data-stu-id="d7ee6-128">Project</span></span> | <span data-ttu-id="d7ee6-129">Utilitzeu aquest camp opcional per identificar el projecte que s'utilitzarà per lliurar el treball en aquesta interacció.</span><span class="sxs-lookup"><span data-stu-id="d7ee6-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="d7ee6-130">Quan un projecte s'assigna a una línia d'oferta, ajuda amb la creació de tasques imputables i també amb l'aportació d'una estimació basada en projectes a la línia d'oferta com a detalls de la línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="d7ee6-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="d7ee6-131">Quan un projecte no està assignat a una línia d'oferta basada en projectes, la estimació s'ha de crear manualment creant cada detall de la línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="d7ee6-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="d7ee6-132">Aquest valor es copia a la línia de contracte del projecte que es crea a partir d'aquesta línia d'oferta quan es guanya l'oferta.</span><span class="sxs-lookup"><span data-stu-id="d7ee6-132">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="d7ee6-133">Tasques incloses</span><span class="sxs-lookup"><span data-stu-id="d7ee6-133">Included Tasks</span></span> | <span data-ttu-id="d7ee6-134">Indica si aquesta línia d'oferta s'utilitza per a totes o algunes de les tasques del projecte seleccionat.</span><span class="sxs-lookup"><span data-stu-id="d7ee6-134">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="d7ee6-135">Aquest camp té els següents valors possibles:</span><span class="sxs-lookup"><span data-stu-id="d7ee6-135">This field has the following possible values:</span></span></br><span data-ttu-id="d7ee6-136">- Totes les tasques de projecte</span><span class="sxs-lookup"><span data-stu-id="d7ee6-136">- All project tasks</span></span></br><span data-ttu-id="d7ee6-137">- Només les tasques de projecte seleccionades</span><span class="sxs-lookup"><span data-stu-id="d7ee6-137">- Selected project tasks only</span></span></br><span data-ttu-id="d7ee6-138">Un valor en blanc en aquest camp equival a l'opció **Totes les tasques del projecte**.</span><span class="sxs-lookup"><span data-stu-id="d7ee6-138">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="d7ee6-139">Quan se selecciona **Només tasques de projecte seleccionades** a la pàgina de projecte, la pestanya **Configuració de facturació de la tasca** us permet seleccionar tasques específiques per associar-les a aquesta línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="d7ee6-139">When **Selected project tasks only** is selected on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="d7ee6-140">Aquest valor es copia a la línia de contracte del projecte que es crea a partir d'aquesta línia d'oferta quan es guanya l'oferta.</span><span class="sxs-lookup"><span data-stu-id="d7ee6-140">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d7ee6-141">Inclou el temps</span><span class="sxs-lookup"><span data-stu-id="d7ee6-141">Include Time</span></span> | <span data-ttu-id="d7ee6-142">Un valor **Sí**/**No** indica si les transaccions de temps o els costos laborals del projecte seleccionat s'inclouran a la previsió en aquesta línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="d7ee6-142">A **Yes**/**No** value indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="d7ee6-143">Un valor **No** indica que les transaccions de temps o els costos de treball no s'inclouran a l'estimació en aquesta línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="d7ee6-143">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="d7ee6-144">Un valor **Sí** indica que les transaccions de temps o els costos de treball s'inclouran a l'estimació en aquesta línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="d7ee6-144">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="d7ee6-145">Aquest valor es copia a la línia de contracte del projecte que es crea a partir d'aquesta línia d'oferta quan es guanya l'oferta.</span><span class="sxs-lookup"><span data-stu-id="d7ee6-145">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d7ee6-146">Inclou la despesa</span><span class="sxs-lookup"><span data-stu-id="d7ee6-146">Include Expense</span></span> | <span data-ttu-id="d7ee6-147">Un valor **Sí**/**No** indica si els costos de despeses del projecte seleccionat s'inclouran a la previsió en aquesta línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="d7ee6-147">A **Yes**/**No** value indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="d7ee6-148">Un valor **No** indica que el cost de despesa no s'inclourà a l'estimació en aquesta línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="d7ee6-148">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="d7ee6-149">Un valor **Sí** indica que el cost de despesa s'inclourà a l'estimació en aquesta línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="d7ee6-149">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="d7ee6-150">Aquest valor es copia a la línia de contracte del projecte que es crea a partir d'aquesta línia d'oferta quan es guanya l'oferta.</span><span class="sxs-lookup"><span data-stu-id="d7ee6-150">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d7ee6-151">Inclou el material</span><span class="sxs-lookup"><span data-stu-id="d7ee6-151">Include Material</span></span> | <span data-ttu-id="d7ee6-152">Un valor **Sí**/**No** indica si els costos de materials del projecte seleccionat s'inclouran a la previsió en aquesta línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="d7ee6-152">A **Yes**/**No** value indicates if material costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="d7ee6-153">Un valor **No** indica que els costos de materials no s'inclouran a la previsió en aquesta línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="d7ee6-153">A **No** value indicates that the material costs will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="d7ee6-154">Un valor **Sí** indica que els costos de materials s'inclouran a la previsió en aquesta línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="d7ee6-154">A **Yes** value indicates that the material costs will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="d7ee6-155">Aquest valor es copia a la línia de contracte del projecte que es crea a partir d'aquesta línia d'oferta quan es guanya l'oferta.</span><span class="sxs-lookup"><span data-stu-id="d7ee6-155">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d7ee6-156">Inclou la taxa</span><span class="sxs-lookup"><span data-stu-id="d7ee6-156">Include Fee</span></span> | <span data-ttu-id="d7ee6-157">Un valor **Sí**/**No** indica si les tarifes del projecte seleccionat s'inclouran a la previsió en aquesta línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="d7ee6-157">A **Yes**/**No** value indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="d7ee6-158">Un valor **No** indica que les tarifes no s'inclouran a l'estimació en aquesta línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="d7ee6-158">A **No** value indicates that the fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="d7ee6-159">Un valor **Sí** indica que les tarifes s'inclouran a l'estimació en aquesta línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="d7ee6-159">A **Yes** value indicates that the fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="d7ee6-160">Aquest valor es copia a la línia de contracte del projecte que es crea a partir d'aquesta línia d'oferta quan es guanya l'oferta.</span><span class="sxs-lookup"><span data-stu-id="d7ee6-160">This value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d7ee6-161">Import de l’oferta</span><span class="sxs-lookup"><span data-stu-id="d7ee6-161">Quoted Amount</span></span> | <span data-ttu-id="d7ee6-162">Aquest és l'import que s'oferirà al client per a tots els treballs previstos en aquesta línia d'oferta basada en projectes.</span><span class="sxs-lookup"><span data-stu-id="d7ee6-162">This is the amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="d7ee6-163">En una oferta creada a partir d'una oportunitat, aquest valor es copia des del camp **Pressupost de client** a la línia d'oportunitat.</span><span class="sxs-lookup"><span data-stu-id="d7ee6-163">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="d7ee6-164">Quan la línia d'oferta basada en projectes té detalls de línia, aquest camp està bloquejat per editar-lo i es resumeix de l'import dels detalls de la línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="d7ee6-164">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="d7ee6-165">Aquest valor es copia a la línia de contracte del projecte que es crea a partir d'aquesta línia d'oferta quan es guanya l'oferta.</span><span class="sxs-lookup"><span data-stu-id="d7ee6-165">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d7ee6-166">Impost estimat</span><span class="sxs-lookup"><span data-stu-id="d7ee6-166">Estimated Tax</span></span> | <span data-ttu-id="d7ee6-167">Es tracta d'un camp editable per a l'usuari que afegirà l'import de l'impost previst a la línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="d7ee6-167">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="d7ee6-168">Quan una línia d'oferta basada en projectes té detalls de línia, aquest camp està bloquejat per editar-lo i es resumeix de l'import d'impostos dels detalls de la línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="d7ee6-168">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="d7ee6-169">Aquest valor es copia a la línia de contracte del projecte que es crea a partir d'aquesta línia d'oferta quan es guanya l'oferta.</span><span class="sxs-lookup"><span data-stu-id="d7ee6-169">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d7ee6-170">Import de l’oferta després d’impostos</span><span class="sxs-lookup"><span data-stu-id="d7ee6-170">Quoted Amount after Tax</span></span> | <span data-ttu-id="d7ee6-171">Aquest camp és l'import de la línia d'oferta després de l'impost i és només de lectura.</span><span class="sxs-lookup"><span data-stu-id="d7ee6-171">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="d7ee6-172">L'import d'aquest camp es calcula com a *Import de l'oferta + impost*.</span><span class="sxs-lookup"><span data-stu-id="d7ee6-172">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="d7ee6-173">Aquest valor es copia a la línia de contracte del projecte que es crea a partir d'aquesta línia d'oferta quan es guanya l'oferta.</span><span class="sxs-lookup"><span data-stu-id="d7ee6-173">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d7ee6-174">Límit que no s’ha de superar</span><span class="sxs-lookup"><span data-stu-id="d7ee6-174">Not-to-exceed Limit</span></span> | <span data-ttu-id="d7ee6-175">Aquest camp és editable i només està disponible a les línies d'oferta basades en el projecte que tenen un mètode de facturació **Temps i material**.</span><span class="sxs-lookup"><span data-stu-id="d7ee6-175">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="d7ee6-176">Aquest valor es copia a la línia de contracte del projecte que es crea a partir d'aquesta línia d'oferta quan es guanya l'oferta.</span><span class="sxs-lookup"><span data-stu-id="d7ee6-176">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d7ee6-177">Pressupost del client</span><span class="sxs-lookup"><span data-stu-id="d7ee6-177">Customer Budget</span></span> | <span data-ttu-id="d7ee6-178">Aquest camp és editable i es copia des del camp corresponent a la línia d'oportunitat si l'oferta es va crear a partir d'una oportunitat.</span><span class="sxs-lookup"><span data-stu-id="d7ee6-178">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="d7ee6-179">Aquest valor es copia a la línia de contracte del projecte que es crea a partir d'aquesta línia d'oferta quan es guanya l'oferta.</span><span class="sxs-lookup"><span data-stu-id="d7ee6-179">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="d7ee6-180">Regles de validació per als camps de la pestanya General de línies d'oferta basades en projectes</span><span class="sxs-lookup"><span data-stu-id="d7ee6-180">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="d7ee6-181">**Regla 1**: si el camp **Tasques incloses** està en blanc o si està definit com a **Totes les tasques del projecte**, s'inclou un projecte a la línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="d7ee6-181">**Rule 1**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project is included in the quote line.</span></span>

<span data-ttu-id="d7ee6-182">**Regla 2**: si el camp **Tasques incloses** està en blanc o si està definit com a **Totes les tasques del projecte**, un projecte i una determinada classe de transacció només es poden incloure en una línia d'oferta basada en projectes d'una oferta.</span><span class="sxs-lookup"><span data-stu-id="d7ee6-182">**Rule 2**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="d7ee6-183">**Regla 3**: si el camp **Tasques incloses** està definit com a **Només les tasques del projecte seleccionades**, un projecte i una determinada classe de transacció es poden incloure en diverses línies d'oferta basades en projectes d'una oferta.</span><span class="sxs-lookup"><span data-stu-id="d7ee6-183">**Rule 3**: If the **Included Tasks** field is set to **Selected project tasks only**, a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="d7ee6-184">**Regla 4**: si una oportunitat té diverses ofertes, pot haver-hi línies d'ofertes de diverses ofertes que facin referència al mateix projecte i que incloguin la mateixa classe de transacció.</span><span class="sxs-lookup"><span data-stu-id="d7ee6-184">**Rule 4**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="d7ee6-185">**Regla 5**: si les ofertes no pertanyen a la mateixa oportunitat, no poden incloure el mateix projecte i classe de transacció.</span><span class="sxs-lookup"><span data-stu-id="d7ee6-185">**Rule 5**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="59" valign="top">
                <p><span data-ttu-id="d7ee6-186">
                    <strong>Oportunitat</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d7ee6-186">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="39" valign="top">
                <p><span data-ttu-id="d7ee6-187">
                    <strong>Oferta</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d7ee6-187">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="40" valign="top">
                <p><span data-ttu-id="d7ee6-188">
                    <strong>Línia d’oferta</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d7ee6-188">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="d7ee6-189">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d7ee6-189">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="77" valign="top">
                <p><span data-ttu-id="d7ee6-190">
                    <strong>Tasques incloses</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d7ee6-190">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="45" valign="top">
                <p><span data-ttu-id="d7ee6-191">
                    <strong>Inclou el temps</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d7ee6-191">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="46" valign="top">
                <p><span data-ttu-id="d7ee6-192">
                    <strong>Inclou la despesa</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d7ee6-192">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="43" valign="top">
                <p><span data-ttu-id="d7ee6-193">
                    <strong>Inclou el material</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d7ee6-193">
                    <strong>Include Material</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="d7ee6-194">
                    <strong>Inclou</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d7ee6-194">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="d7ee6-195">
                    <strong>Tarifa</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d7ee6-195">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="49" valign="top">
                <p><span data-ttu-id="d7ee6-196">
                    <strong>Vàlid/No és vàlid</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d7ee6-196">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="200" valign="top">
                <p><span data-ttu-id="d7ee6-197">
                    <strong>Motiu</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d7ee6-197">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="d7ee6-198">O1</span><span class="sxs-lookup"><span data-stu-id="d7ee6-198">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="d7ee6-199">T1</span><span class="sxs-lookup"><span data-stu-id="d7ee6-199">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="d7ee6-200">QL1</span><span class="sxs-lookup"><span data-stu-id="d7ee6-200">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d7ee6-201">P1</span><span class="sxs-lookup"><span data-stu-id="d7ee6-201">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="d7ee6-202">En blanc</span><span class="sxs-lookup"><span data-stu-id="d7ee6-202">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="d7ee6-203">Sí</span><span class="sxs-lookup"><span data-stu-id="d7ee6-203">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="d7ee6-204">Sí</span><span class="sxs-lookup"><span data-stu-id="d7ee6-204">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="d7ee6-205">Sí</span><span class="sxs-lookup"><span data-stu-id="d7ee6-205">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d7ee6-206">Sí</span><span class="sxs-lookup"><span data-stu-id="d7ee6-206">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d7ee6-207">No és vàlid</span><span class="sxs-lookup"><span data-stu-id="d7ee6-207">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d7ee6-208">Infracció de la regla 2.</span><span class="sxs-lookup"><span data-stu-id="d7ee6-208">Violation of Rule #2.</span></span> <span data-ttu-id="d7ee6-209">El temps, les despeses i les tarifes del projecte P1 s'inclouen a les línies d'oferta QL1 i QL2</span><span class="sxs-lookup"><span data-stu-id="d7ee6-209">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="d7ee6-210">O1</span><span class="sxs-lookup"><span data-stu-id="d7ee6-210">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="d7ee6-211">T1</span><span class="sxs-lookup"><span data-stu-id="d7ee6-211">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="d7ee6-212">QL2</span><span class="sxs-lookup"><span data-stu-id="d7ee6-212">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d7ee6-213">P1</span><span class="sxs-lookup"><span data-stu-id="d7ee6-213">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="d7ee6-214">En blanc</span><span class="sxs-lookup"><span data-stu-id="d7ee6-214">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="d7ee6-215">Sí</span><span class="sxs-lookup"><span data-stu-id="d7ee6-215">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="d7ee6-216">Sí</span><span class="sxs-lookup"><span data-stu-id="d7ee6-216">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="d7ee6-217">Sí</span><span class="sxs-lookup"><span data-stu-id="d7ee6-217">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d7ee6-218">Sí</span><span class="sxs-lookup"><span data-stu-id="d7ee6-218">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="d7ee6-219">O1</span><span class="sxs-lookup"><span data-stu-id="d7ee6-219">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="d7ee6-220">T1</span><span class="sxs-lookup"><span data-stu-id="d7ee6-220">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="d7ee6-221">QL1</span><span class="sxs-lookup"><span data-stu-id="d7ee6-221">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d7ee6-222">P1</span><span class="sxs-lookup"><span data-stu-id="d7ee6-222">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="d7ee6-223">En blanc</span><span class="sxs-lookup"><span data-stu-id="d7ee6-223">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="d7ee6-224">Sí</span><span class="sxs-lookup"><span data-stu-id="d7ee6-224">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="d7ee6-225">No</span><span class="sxs-lookup"><span data-stu-id="d7ee6-225">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="d7ee6-226">Sí</span><span class="sxs-lookup"><span data-stu-id="d7ee6-226">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d7ee6-227">Sí</span><span class="sxs-lookup"><span data-stu-id="d7ee6-227">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d7ee6-228">No és vàlid</span><span class="sxs-lookup"><span data-stu-id="d7ee6-228">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d7ee6-229">Infracció de la regla 2.</span><span class="sxs-lookup"><span data-stu-id="d7ee6-229">Violation of Rule #2.</span></span> <span data-ttu-id="d7ee6-230">El temps, el material i les tarifes del projecte P1 s'inclouen a les línies d'oferta QL1 i QL2</span><span class="sxs-lookup"><span data-stu-id="d7ee6-230">Time, Material, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="d7ee6-231">O1</span><span class="sxs-lookup"><span data-stu-id="d7ee6-231">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="d7ee6-232">T1</span><span class="sxs-lookup"><span data-stu-id="d7ee6-232">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="d7ee6-233">QL2</span><span class="sxs-lookup"><span data-stu-id="d7ee6-233">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d7ee6-234">P1</span><span class="sxs-lookup"><span data-stu-id="d7ee6-234">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="d7ee6-235">En blanc</span><span class="sxs-lookup"><span data-stu-id="d7ee6-235">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="d7ee6-236">Sí</span><span class="sxs-lookup"><span data-stu-id="d7ee6-236">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="d7ee6-237">Sí</span><span class="sxs-lookup"><span data-stu-id="d7ee6-237">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="d7ee6-238">Sí</span><span class="sxs-lookup"><span data-stu-id="d7ee6-238">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d7ee6-239">Sí</span><span class="sxs-lookup"><span data-stu-id="d7ee6-239">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="d7ee6-240">O1</span><span class="sxs-lookup"><span data-stu-id="d7ee6-240">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="d7ee6-241">T1</span><span class="sxs-lookup"><span data-stu-id="d7ee6-241">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="d7ee6-242">QL1</span><span class="sxs-lookup"><span data-stu-id="d7ee6-242">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d7ee6-243">P1</span><span class="sxs-lookup"><span data-stu-id="d7ee6-243">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="d7ee6-244">En blanc</span><span class="sxs-lookup"><span data-stu-id="d7ee6-244">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="d7ee6-245">Sí</span><span class="sxs-lookup"><span data-stu-id="d7ee6-245">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="d7ee6-246">No</span><span class="sxs-lookup"><span data-stu-id="d7ee6-246">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="d7ee6-247">Sí</span><span class="sxs-lookup"><span data-stu-id="d7ee6-247">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d7ee6-248">Sí</span><span class="sxs-lookup"><span data-stu-id="d7ee6-248">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d7ee6-249">Vàlida</span><span class="sxs-lookup"><span data-stu-id="d7ee6-249">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d7ee6-250">El temps, el material i les tarifes del projecte P1 s'inclouen a QL1</span><span class="sxs-lookup"><span data-stu-id="d7ee6-250">Time, Material, and Fees on P1 project are included on QL1</span></span> <br>
<span data-ttu-id="d7ee6-251">La despesa del projecte P1 s'inclou a QL2</span><span class="sxs-lookup"><span data-stu-id="d7ee6-251">Expense on P1 project is included on QL2</span></span> <br>
<span data-ttu-id="d7ee6-252">No se superposa el que s'inclou a cada línia d'oferta i, per tant, és vàlid.</span><span class="sxs-lookup"><span data-stu-id="d7ee6-252">No overlap in what is being included on each quote line and therefore valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="d7ee6-253">O1</span><span class="sxs-lookup"><span data-stu-id="d7ee6-253">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="d7ee6-254">T1</span><span class="sxs-lookup"><span data-stu-id="d7ee6-254">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="d7ee6-255">QL2</span><span class="sxs-lookup"><span data-stu-id="d7ee6-255">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d7ee6-256">P1</span><span class="sxs-lookup"><span data-stu-id="d7ee6-256">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="d7ee6-257">En blanc</span><span class="sxs-lookup"><span data-stu-id="d7ee6-257">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="d7ee6-258">No</span><span class="sxs-lookup"><span data-stu-id="d7ee6-258">No</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="d7ee6-259">Sí</span><span class="sxs-lookup"><span data-stu-id="d7ee6-259">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="d7ee6-260">No</span><span class="sxs-lookup"><span data-stu-id="d7ee6-260">No</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d7ee6-261">No</span><span class="sxs-lookup"><span data-stu-id="d7ee6-261">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="d7ee6-262">O1</span><span class="sxs-lookup"><span data-stu-id="d7ee6-262">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="d7ee6-263">T1</span><span class="sxs-lookup"><span data-stu-id="d7ee6-263">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="d7ee6-264">QL1</span><span class="sxs-lookup"><span data-stu-id="d7ee6-264">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d7ee6-265">P1</span><span class="sxs-lookup"><span data-stu-id="d7ee6-265">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="d7ee6-266">Només les tasques seleccionades</span><span class="sxs-lookup"><span data-stu-id="d7ee6-266">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="d7ee6-267">Sí</span><span class="sxs-lookup"><span data-stu-id="d7ee6-267">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="d7ee6-268">Sí</span><span class="sxs-lookup"><span data-stu-id="d7ee6-268">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="d7ee6-269">Sí</span><span class="sxs-lookup"><span data-stu-id="d7ee6-269">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d7ee6-270">Sí</span><span class="sxs-lookup"><span data-stu-id="d7ee6-270">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d7ee6-271">No és vàlid</span><span class="sxs-lookup"><span data-stu-id="d7ee6-271">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d7ee6-272">Infracció de la regla núm. 2</span><span class="sxs-lookup"><span data-stu-id="d7ee6-272">Violation of Rule #2</span></span> </p>
                <p>
<span data-ttu-id="d7ee6-273">El Q1 inclou temps, material, despeses i tarifes en un subconjunt de tasques al projecte P1</span><span class="sxs-lookup"><span data-stu-id="d7ee6-273">Q1 includes Time, Material, Expenses and Fees on a subset of tasks on project P1</span></span> </p>
                <p>
<span data-ttu-id="d7ee6-274">QL2 inclou temps, despeses i tarifes per a tot el projecte P1 i, per tant, se superposa amb el que s'inclou a Q1.</span><span class="sxs-lookup"><span data-stu-id="d7ee6-274">QL2 includes Time, Expenses, and Fees for the whole project P1 and therefore overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="d7ee6-275">O1</span><span class="sxs-lookup"><span data-stu-id="d7ee6-275">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="d7ee6-276">T1</span><span class="sxs-lookup"><span data-stu-id="d7ee6-276">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="d7ee6-277">QL2</span><span class="sxs-lookup"><span data-stu-id="d7ee6-277">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d7ee6-278">P1</span><span class="sxs-lookup"><span data-stu-id="d7ee6-278">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="d7ee6-279">En blanc</span><span class="sxs-lookup"><span data-stu-id="d7ee6-279">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="d7ee6-280">Sí</span><span class="sxs-lookup"><span data-stu-id="d7ee6-280">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="d7ee6-281">Sí</span><span class="sxs-lookup"><span data-stu-id="d7ee6-281">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="d7ee6-282">Sí</span><span class="sxs-lookup"><span data-stu-id="d7ee6-282">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d7ee6-283">Sí</span><span class="sxs-lookup"><span data-stu-id="d7ee6-283">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="d7ee6-284">O1</span><span class="sxs-lookup"><span data-stu-id="d7ee6-284">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="d7ee6-285">T1</span><span class="sxs-lookup"><span data-stu-id="d7ee6-285">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="d7ee6-286">QL1</span><span class="sxs-lookup"><span data-stu-id="d7ee6-286">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d7ee6-287">P1</span><span class="sxs-lookup"><span data-stu-id="d7ee6-287">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="d7ee6-288">Només les tasques seleccionades</span><span class="sxs-lookup"><span data-stu-id="d7ee6-288">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="d7ee6-289">Sí</span><span class="sxs-lookup"><span data-stu-id="d7ee6-289">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="d7ee6-290">Sí</span><span class="sxs-lookup"><span data-stu-id="d7ee6-290">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="d7ee6-291">Sí</span><span class="sxs-lookup"><span data-stu-id="d7ee6-291">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d7ee6-292">Sí</span><span class="sxs-lookup"><span data-stu-id="d7ee6-292">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d7ee6-293">Vàlida</span><span class="sxs-lookup"><span data-stu-id="d7ee6-293">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d7ee6-294">Segons la regla núm. 3,</span><span class="sxs-lookup"><span data-stu-id="d7ee6-294">Per Rule #3,</span></span> </p>
                <p>
<span data-ttu-id="d7ee6-295">El Q1 inclou temps, material, despeses i tarifes en un subconjunt de tasques al projecte P1.</span><span class="sxs-lookup"><span data-stu-id="d7ee6-295">Q1 includes Time, Material, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="d7ee6-296">El QL2 inclou temps, material, despeses i tarifes per a un subconjunt de tasques al projecte P1.</span><span class="sxs-lookup"><span data-stu-id="d7ee6-296">QL2 includes Time, Material, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="d7ee6-297">L'única validació addicional és per al subconjunt de tasques de QL1, que és diferent del subconjunt de tasques de QL2 per assegurar que no hi ha superposició.</span><span class="sxs-lookup"><span data-stu-id="d7ee6-297">The only additional validation is around the subset of tasks on QL1 which is different from the subset of tasks on QL2 to ensure that there is no overlap.</span></span> <span data-ttu-id="d7ee6-298">Això ho fa el sistema quan s'associen les tasques.</span><span class="sxs-lookup"><span data-stu-id="d7ee6-298">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="d7ee6-299">O1</span><span class="sxs-lookup"><span data-stu-id="d7ee6-299">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="d7ee6-300">T1</span><span class="sxs-lookup"><span data-stu-id="d7ee6-300">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="d7ee6-301">QL2</span><span class="sxs-lookup"><span data-stu-id="d7ee6-301">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d7ee6-302">P1</span><span class="sxs-lookup"><span data-stu-id="d7ee6-302">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="d7ee6-303">Només les tasques seleccionades</span><span class="sxs-lookup"><span data-stu-id="d7ee6-303">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="d7ee6-304">Sí</span><span class="sxs-lookup"><span data-stu-id="d7ee6-304">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="d7ee6-305">Sí</span><span class="sxs-lookup"><span data-stu-id="d7ee6-305">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="d7ee6-306">Sí</span><span class="sxs-lookup"><span data-stu-id="d7ee6-306">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d7ee6-307">Sí</span><span class="sxs-lookup"><span data-stu-id="d7ee6-307">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="d7ee6-308">O1</span><span class="sxs-lookup"><span data-stu-id="d7ee6-308">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="d7ee6-309">T1</span><span class="sxs-lookup"><span data-stu-id="d7ee6-309">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="d7ee6-310">QL1</span><span class="sxs-lookup"><span data-stu-id="d7ee6-310">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d7ee6-311">P1</span><span class="sxs-lookup"><span data-stu-id="d7ee6-311">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="d7ee6-312">Totes les tasques del projecte o en blanc</span><span class="sxs-lookup"><span data-stu-id="d7ee6-312">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="d7ee6-313">Sí</span><span class="sxs-lookup"><span data-stu-id="d7ee6-313">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="d7ee6-314">Sí</span><span class="sxs-lookup"><span data-stu-id="d7ee6-314">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="d7ee6-315">Sí</span><span class="sxs-lookup"><span data-stu-id="d7ee6-315">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d7ee6-316">Sí</span><span class="sxs-lookup"><span data-stu-id="d7ee6-316">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d7ee6-317">Vàlida</span><span class="sxs-lookup"><span data-stu-id="d7ee6-317">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d7ee6-318">Segons la regla núm. 5, Q1 i Q2 són dues ofertes per a la mateixa oportunitat, de manera que poden calcular ambdós els mateixos components d'un projecte.</span><span class="sxs-lookup"><span data-stu-id="d7ee6-318">Per Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="d7ee6-319">O1</span><span class="sxs-lookup"><span data-stu-id="d7ee6-319">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="d7ee6-320">T2</span><span class="sxs-lookup"><span data-stu-id="d7ee6-320">Q2</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="d7ee6-321">QL1</span><span class="sxs-lookup"><span data-stu-id="d7ee6-321">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d7ee6-322">P1</span><span class="sxs-lookup"><span data-stu-id="d7ee6-322">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="d7ee6-323">Totes les tasques del projecte o en blanc</span><span class="sxs-lookup"><span data-stu-id="d7ee6-323">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="d7ee6-324">Sí</span><span class="sxs-lookup"><span data-stu-id="d7ee6-324">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="d7ee6-325">Sí</span><span class="sxs-lookup"><span data-stu-id="d7ee6-325">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="d7ee6-326">Sí</span><span class="sxs-lookup"><span data-stu-id="d7ee6-326">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d7ee6-327">Sí</span><span class="sxs-lookup"><span data-stu-id="d7ee6-327">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="d7ee6-328">O1</span><span class="sxs-lookup"><span data-stu-id="d7ee6-328">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="d7ee6-329">T1</span><span class="sxs-lookup"><span data-stu-id="d7ee6-329">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="d7ee6-330">QL1</span><span class="sxs-lookup"><span data-stu-id="d7ee6-330">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d7ee6-331">P1</span><span class="sxs-lookup"><span data-stu-id="d7ee6-331">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="d7ee6-332">Totes les tasques del projecte o en blanc</span><span class="sxs-lookup"><span data-stu-id="d7ee6-332">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="d7ee6-333">Sí</span><span class="sxs-lookup"><span data-stu-id="d7ee6-333">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="d7ee6-334">Sí</span><span class="sxs-lookup"><span data-stu-id="d7ee6-334">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="d7ee6-335">Sí</span><span class="sxs-lookup"><span data-stu-id="d7ee6-335">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d7ee6-336">Sí</span><span class="sxs-lookup"><span data-stu-id="d7ee6-336">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d7ee6-337">No és vàlid</span><span class="sxs-lookup"><span data-stu-id="d7ee6-337">Not Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d7ee6-338">Segons la regla núm. 4, Q1 i Q2 són dues ofertes d'oportunitats diferents, de manera que no poden calcular els mateixos components del mateix projecte.</span><span class="sxs-lookup"><span data-stu-id="d7ee6-338">Per Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="d7ee6-339">O2</span><span class="sxs-lookup"><span data-stu-id="d7ee6-339">O2</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="d7ee6-340">T1</span><span class="sxs-lookup"><span data-stu-id="d7ee6-340">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="d7ee6-341">QL1</span><span class="sxs-lookup"><span data-stu-id="d7ee6-341">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d7ee6-342">P1</span><span class="sxs-lookup"><span data-stu-id="d7ee6-342">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="d7ee6-343">Totes les tasques del projecte o en blanc</span><span class="sxs-lookup"><span data-stu-id="d7ee6-343">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="d7ee6-344">Sí</span><span class="sxs-lookup"><span data-stu-id="d7ee6-344">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="d7ee6-345">Sí</span><span class="sxs-lookup"><span data-stu-id="d7ee6-345">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="d7ee6-346">Sí</span><span class="sxs-lookup"><span data-stu-id="d7ee6-346">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d7ee6-347">Sí</span><span class="sxs-lookup"><span data-stu-id="d7ee6-347">Yes</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
