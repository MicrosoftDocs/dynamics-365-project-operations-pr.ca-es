---
title: Informació general de les línies d'oferta basades en projectes
description: En aquest tema s'ofereix informació sobre l'ús de línies d'oferta basades en projectes per al treball del projecte.
author: rumant
manager: Annbe
ms.date: 03/30/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cfe98fc89130c93dd0a36af8583881fdcb4550c0
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858686"
---
# <a name="project-based-quote-lines-overview"></a><span data-ttu-id="40d8d-103">Informació general de les línies d'oferta basades en projectes</span><span class="sxs-lookup"><span data-stu-id="40d8d-103">Project-based quote lines overview</span></span> 

<span data-ttu-id="40d8d-104">_**S'aplica a:** Implementació bàsica: tracte de facturació proforma, Project Operations per a escenaris basats en recursos/sense cotització_</span><span class="sxs-lookup"><span data-stu-id="40d8d-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="40d8d-105">Les línies d'oferta basades en projectes estan dissenyades per ajudar a estimar el treball del projecte en una interacció.</span><span class="sxs-lookup"><span data-stu-id="40d8d-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="40d8d-106">L'estructura d'una línia d'oferta basada en projectes s'amplia per a estimacions de projecte amb els conceptes següents:</span><span class="sxs-lookup"><span data-stu-id="40d8d-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="40d8d-107">Mètode de facturació</span><span class="sxs-lookup"><span data-stu-id="40d8d-107">Billing Method</span></span>
- <span data-ttu-id="40d8d-108">Assignació de projectes i tasques</span><span class="sxs-lookup"><span data-stu-id="40d8d-108">Project and Task Mapping</span></span>
- <span data-ttu-id="40d8d-109">Classes de transaccions incloses</span><span class="sxs-lookup"><span data-stu-id="40d8d-109">Included Transaction classes</span></span>
- <span data-ttu-id="40d8d-110">Límit que no s’ha de superar</span><span class="sxs-lookup"><span data-stu-id="40d8d-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="40d8d-111">Configuració de la imputabilitat</span><span class="sxs-lookup"><span data-stu-id="40d8d-111">Chargeability setup</span></span>
- <span data-ttu-id="40d8d-112">Estimació mitjançant detalls de la línia d'oferta</span><span class="sxs-lookup"><span data-stu-id="40d8d-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="40d8d-113">Clients de la línia d’oferta</span><span class="sxs-lookup"><span data-stu-id="40d8d-113">Quote line Customers</span></span>

<span data-ttu-id="40d8d-114">A la taula següent es proporciona informació sobre els camps de la pestanya **General** de la línia d'oferta basada en projectes.</span><span class="sxs-lookup"><span data-stu-id="40d8d-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="40d8d-115">Aquests camps ajuden a configurar la base per a una estimació detallada i des de zero per al treball del projecte.</span><span class="sxs-lookup"><span data-stu-id="40d8d-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="40d8d-116">**Camp**</span><span class="sxs-lookup"><span data-stu-id="40d8d-116">**Field**</span></span> | <span data-ttu-id="40d8d-117">**Descripció**</span><span class="sxs-lookup"><span data-stu-id="40d8d-117">**Description**</span></span> | <span data-ttu-id="40d8d-118">**Impacte descendent**</span><span class="sxs-lookup"><span data-stu-id="40d8d-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="40d8d-119">Nom</span><span class="sxs-lookup"><span data-stu-id="40d8d-119">Name</span></span> | <span data-ttu-id="40d8d-120">El nom de la línia d'oferta que us ajuda a identificar el component discret de l'oferta que s'està calculant.</span><span class="sxs-lookup"><span data-stu-id="40d8d-120">The name of quote line that helps you to identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="40d8d-121">Es copia a la línia de contracte del projecte que es crea des d'aquesta línia d'oferta en guanyar l'oferta.</span><span class="sxs-lookup"><span data-stu-id="40d8d-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="40d8d-122">Mètode de facturació</span><span class="sxs-lookup"><span data-stu-id="40d8d-122">Billing Method</span></span> | <span data-ttu-id="40d8d-123">En una oferta creada a partir d'una oportunitat, aquest valor es copia des del camp corresponent a la línia d'oportunitat.</span><span class="sxs-lookup"><span data-stu-id="40d8d-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="40d8d-124">Aquest camp inclou els dos models de contracte principals compatibles amb el Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="40d8d-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="40d8d-125">- Preu fix</span><span class="sxs-lookup"><span data-stu-id="40d8d-125">- Fixed price</span></span></br><span data-ttu-id="40d8d-126">- Temps i material.</span><span class="sxs-lookup"><span data-stu-id="40d8d-126">- Time and material.</span></span>| <span data-ttu-id="40d8d-127">Aquest valor es copia a la línia de contracte del projecte que es crea a partir d'aquesta línia d'oferta quan es guanya l'oferta.</span><span class="sxs-lookup"><span data-stu-id="40d8d-127">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="40d8d-128">Project</span><span class="sxs-lookup"><span data-stu-id="40d8d-128">Project</span></span> | <span data-ttu-id="40d8d-129">Utilitzeu aquest camp opcional per identificar el projecte que s'utilitzarà per lliurar el treball en aquesta interacció.</span><span class="sxs-lookup"><span data-stu-id="40d8d-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="40d8d-130">Quan un projecte s'assigna a una línia d'oferta, ajuda amb la creació de tasques imputables i també amb l'aportació d'una estimació basada en projectes a la línia d'oferta com a detalls de la línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="40d8d-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="40d8d-131">Quan un projecte no està assignat a una línia d'oferta basada en projectes, la estimació s'ha de crear manualment creant cada detall de la línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="40d8d-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="40d8d-132">Aquest valor es copia a la línia de contracte del projecte que es crea a partir d'aquesta línia d'oferta quan es guanya l'oferta.</span><span class="sxs-lookup"><span data-stu-id="40d8d-132">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="40d8d-133">Tasques incloses</span><span class="sxs-lookup"><span data-stu-id="40d8d-133">Included Tasks</span></span> | <span data-ttu-id="40d8d-134">Indica si aquesta línia d'oferta s'utilitza per a totes o algunes de les tasques del projecte seleccionat.</span><span class="sxs-lookup"><span data-stu-id="40d8d-134">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="40d8d-135">Aquest camp té els següents valors possibles:</span><span class="sxs-lookup"><span data-stu-id="40d8d-135">This field has the following possible values:</span></span></br><span data-ttu-id="40d8d-136">- Totes les tasques de projecte</span><span class="sxs-lookup"><span data-stu-id="40d8d-136">- All project tasks</span></span></br><span data-ttu-id="40d8d-137">- Només les tasques de projecte seleccionades</span><span class="sxs-lookup"><span data-stu-id="40d8d-137">- Selected project tasks only</span></span></br><span data-ttu-id="40d8d-138">Un valor en blanc en aquest camp equival a l'opció **Totes les tasques del projecte**.</span><span class="sxs-lookup"><span data-stu-id="40d8d-138">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="40d8d-139">Quan se selecciona **Només tasques de projecte seleccionades** a la pàgina de projecte, la pestanya **Configuració de facturació de la tasca** us permet seleccionar tasques específiques per associar-les a aquesta línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="40d8d-139">When **Selected project tasks only** is selected on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="40d8d-140">Aquest valor es copia a la línia de contracte del projecte que es crea a partir d'aquesta línia d'oferta quan es guanya l'oferta.</span><span class="sxs-lookup"><span data-stu-id="40d8d-140">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="40d8d-141">Inclou el temps</span><span class="sxs-lookup"><span data-stu-id="40d8d-141">Include Time</span></span> | <span data-ttu-id="40d8d-142">Un valor **Sí**/**No** indica si les transaccions de temps o els costos laborals del projecte seleccionat s'inclouran a la previsió en aquesta línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="40d8d-142">A **Yes**/**No** value indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="40d8d-143">Un valor **No** indica que les transaccions de temps o els costos de treball no s'inclouran a l'estimació en aquesta línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="40d8d-143">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="40d8d-144">Un valor **Sí** indica que les transaccions de temps o els costos de treball s'inclouran a l'estimació en aquesta línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="40d8d-144">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="40d8d-145">Aquest valor es copia a la línia de contracte del projecte que es crea a partir d'aquesta línia d'oferta quan es guanya l'oferta.</span><span class="sxs-lookup"><span data-stu-id="40d8d-145">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="40d8d-146">Inclou la despesa</span><span class="sxs-lookup"><span data-stu-id="40d8d-146">Include Expense</span></span> | <span data-ttu-id="40d8d-147">Un valor **Sí**/**No** indica si els costos de despeses del projecte seleccionat s'inclouran a la previsió en aquesta línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="40d8d-147">A **Yes**/**No** value indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="40d8d-148">Un valor **No** indica que el cost de despesa no s'inclourà a l'estimació en aquesta línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="40d8d-148">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="40d8d-149">Un valor **Sí** indica que el cost de despesa s'inclourà a l'estimació en aquesta línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="40d8d-149">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="40d8d-150">Aquest valor es copia a la línia de contracte del projecte que es crea a partir d'aquesta línia d'oferta quan es guanya l'oferta.</span><span class="sxs-lookup"><span data-stu-id="40d8d-150">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="40d8d-151">Inclou el material</span><span class="sxs-lookup"><span data-stu-id="40d8d-151">Include Material</span></span> | <span data-ttu-id="40d8d-152">Un valor **Sí**/**No** indica si els costos de materials del projecte seleccionat s'inclouran a la previsió en aquesta línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="40d8d-152">A **Yes**/**No** value indicates if material costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="40d8d-153">Un valor **No** indica que els costos de materials no s'inclouran a la previsió en aquesta línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="40d8d-153">A **No** value indicates that the material costs will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="40d8d-154">Un valor **Sí** indica que els costos de materials s'inclouran a la previsió en aquesta línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="40d8d-154">A **Yes** value indicates that the material costs will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="40d8d-155">Aquest valor es copia a la línia de contracte del projecte que es crea a partir d'aquesta línia d'oferta quan es guanya l'oferta.</span><span class="sxs-lookup"><span data-stu-id="40d8d-155">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="40d8d-156">Inclou la taxa</span><span class="sxs-lookup"><span data-stu-id="40d8d-156">Include Fee</span></span> | <span data-ttu-id="40d8d-157">Un valor **Sí**/**No** indica si les tarifes del projecte seleccionat s'inclouran a la previsió en aquesta línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="40d8d-157">A **Yes**/**No** value indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="40d8d-158">Un valor **No** indica que les tarifes no s'inclouran a l'estimació en aquesta línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="40d8d-158">A **No** value indicates that the fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="40d8d-159">Un valor **Sí** indica que les tarifes s'inclouran a l'estimació en aquesta línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="40d8d-159">A **Yes** value indicates that the fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="40d8d-160">Aquest valor es copia a la línia de contracte del projecte que es crea a partir d'aquesta línia d'oferta quan es guanya l'oferta.</span><span class="sxs-lookup"><span data-stu-id="40d8d-160">This value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="40d8d-161">Import de l’oferta</span><span class="sxs-lookup"><span data-stu-id="40d8d-161">Quoted Amount</span></span> | <span data-ttu-id="40d8d-162">Aquest és l'import que s'oferirà al client per a tots els treballs previstos en aquesta línia d'oferta basada en projectes.</span><span class="sxs-lookup"><span data-stu-id="40d8d-162">This is the amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="40d8d-163">En una oferta creada a partir d'una oportunitat, aquest valor es copia des del camp **Pressupost de client** a la línia d'oportunitat.</span><span class="sxs-lookup"><span data-stu-id="40d8d-163">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="40d8d-164">Quan la línia d'oferta basada en projectes té detalls de línia, aquest camp està bloquejat per editar-lo i es resumeix de l'import dels detalls de la línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="40d8d-164">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="40d8d-165">Aquest valor es copia a la línia de contracte del projecte que es crea a partir d'aquesta línia d'oferta quan es guanya l'oferta.</span><span class="sxs-lookup"><span data-stu-id="40d8d-165">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="40d8d-166">Impost estimat</span><span class="sxs-lookup"><span data-stu-id="40d8d-166">Estimated Tax</span></span> | <span data-ttu-id="40d8d-167">Es tracta d'un camp editable per a l'usuari que afegirà l'import de l'impost previst a la línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="40d8d-167">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="40d8d-168">Quan una línia d'oferta basada en projectes té detalls de línia, aquest camp està bloquejat per editar-lo i es resumeix de l'import d'impostos dels detalls de la línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="40d8d-168">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="40d8d-169">Aquest valor es copia a la línia de contracte del projecte que es crea a partir d'aquesta línia d'oferta quan es guanya l'oferta.</span><span class="sxs-lookup"><span data-stu-id="40d8d-169">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="40d8d-170">Import de l’oferta després d’impostos</span><span class="sxs-lookup"><span data-stu-id="40d8d-170">Quoted Amount after Tax</span></span> | <span data-ttu-id="40d8d-171">Aquest camp és l'import de la línia d'oferta després de l'impost i és només de lectura.</span><span class="sxs-lookup"><span data-stu-id="40d8d-171">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="40d8d-172">L'import d'aquest camp es calcula com a *Import de l'oferta + impost*.</span><span class="sxs-lookup"><span data-stu-id="40d8d-172">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="40d8d-173">Aquest valor es copia a la línia de contracte del projecte que es crea a partir d'aquesta línia d'oferta quan es guanya l'oferta.</span><span class="sxs-lookup"><span data-stu-id="40d8d-173">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="40d8d-174">Límit que no s’ha de superar</span><span class="sxs-lookup"><span data-stu-id="40d8d-174">Not-to-exceed Limit</span></span> | <span data-ttu-id="40d8d-175">Aquest camp és editable i només està disponible a les línies d'oferta basades en el projecte que tenen un mètode de facturació **Temps i material**.</span><span class="sxs-lookup"><span data-stu-id="40d8d-175">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="40d8d-176">Aquest valor es copia a la línia de contracte del projecte que es crea a partir d'aquesta línia d'oferta quan es guanya l'oferta.</span><span class="sxs-lookup"><span data-stu-id="40d8d-176">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="40d8d-177">Pressupost del client</span><span class="sxs-lookup"><span data-stu-id="40d8d-177">Customer Budget</span></span> | <span data-ttu-id="40d8d-178">Aquest camp és editable i es copia des del camp corresponent a la línia d'oportunitat si l'oferta es va crear a partir d'una oportunitat.</span><span class="sxs-lookup"><span data-stu-id="40d8d-178">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="40d8d-179">Aquest valor es copia a la línia de contracte del projecte que es crea a partir d'aquesta línia d'oferta quan es guanya l'oferta.</span><span class="sxs-lookup"><span data-stu-id="40d8d-179">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="40d8d-180">Regles de validació per als camps de la pestanya General de línies d'oferta basades en projectes</span><span class="sxs-lookup"><span data-stu-id="40d8d-180">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="40d8d-181">**Regla 1**: si el camp **Tasques incloses** està en blanc o si està definit com a **Totes les tasques del projecte**, s'inclou un projecte a la línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="40d8d-181">**Rule 1**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project is included in the quote line.</span></span>

<span data-ttu-id="40d8d-182">**Regla 2**: si el camp **Tasques incloses** està en blanc o si està definit com a **Totes les tasques del projecte**, un projecte i una determinada classe de transacció només es poden incloure en una línia d'oferta basada en projectes d'una oferta.</span><span class="sxs-lookup"><span data-stu-id="40d8d-182">**Rule 2**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="40d8d-183">**Regla 3**: si el camp **Tasques incloses** està definit com a **Només les tasques del projecte seleccionades**, un projecte i una determinada classe de transacció es poden incloure en diverses línies d'oferta basades en projectes d'una oferta.</span><span class="sxs-lookup"><span data-stu-id="40d8d-183">**Rule 3**: If the **Included Tasks** field is set to **Selected project tasks only**, a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="40d8d-184">**Regla 4**: si una oportunitat té diverses ofertes, pot haver-hi línies d'ofertes de diverses ofertes que facin referència al mateix projecte i que incloguin la mateixa classe de transacció.</span><span class="sxs-lookup"><span data-stu-id="40d8d-184">**Rule 4**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="40d8d-185">**Regla 5**: si les ofertes no pertanyen a la mateixa oportunitat, no poden incloure el mateix projecte i classe de transacció.</span><span class="sxs-lookup"><span data-stu-id="40d8d-185">**Rule 5**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="59" valign="top">
                <p><span data-ttu-id="40d8d-186">
                    <strong>Oportunitat</strong>
                </span><span class="sxs-lookup"><span data-stu-id="40d8d-186">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="39" valign="top">
                <p><span data-ttu-id="40d8d-187">
                    <strong>Oferta</strong>
                </span><span class="sxs-lookup"><span data-stu-id="40d8d-187">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="40" valign="top">
                <p><span data-ttu-id="40d8d-188">
                    <strong>Línia d’oferta</strong>
                </span><span class="sxs-lookup"><span data-stu-id="40d8d-188">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="40d8d-189">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="40d8d-189">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="77" valign="top">
                <p><span data-ttu-id="40d8d-190">
                    <strong>Tasques incloses</strong>
                </span><span class="sxs-lookup"><span data-stu-id="40d8d-190">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="45" valign="top">
                <p><span data-ttu-id="40d8d-191">
                    <strong>Inclou el temps</strong>
                </span><span class="sxs-lookup"><span data-stu-id="40d8d-191">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="46" valign="top">
                <p><span data-ttu-id="40d8d-192">
                    <strong>Inclou la despesa</strong>
                </span><span class="sxs-lookup"><span data-stu-id="40d8d-192">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="43" valign="top">
                <p><span data-ttu-id="40d8d-193">
                    <strong>Inclou el material</strong>
                </span><span class="sxs-lookup"><span data-stu-id="40d8d-193">
                    <strong>Include Material</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="40d8d-194">
                    <strong>Inclou</strong>
                </span><span class="sxs-lookup"><span data-stu-id="40d8d-194">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="40d8d-195">
                    <strong>Tarifa</strong>
                </span><span class="sxs-lookup"><span data-stu-id="40d8d-195">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="49" valign="top">
                <p><span data-ttu-id="40d8d-196">
                    <strong>Vàlid/No és vàlid</strong>
                </span><span class="sxs-lookup"><span data-stu-id="40d8d-196">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="200" valign="top">
                <p><span data-ttu-id="40d8d-197">
                    <strong>Motiu</strong>
                </span><span class="sxs-lookup"><span data-stu-id="40d8d-197">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="40d8d-198">O1</span><span class="sxs-lookup"><span data-stu-id="40d8d-198">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="40d8d-199">T1</span><span class="sxs-lookup"><span data-stu-id="40d8d-199">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="40d8d-200">QL1</span><span class="sxs-lookup"><span data-stu-id="40d8d-200">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="40d8d-201">P1</span><span class="sxs-lookup"><span data-stu-id="40d8d-201">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="40d8d-202">En blanc</span><span class="sxs-lookup"><span data-stu-id="40d8d-202">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="40d8d-203">Sí</span><span class="sxs-lookup"><span data-stu-id="40d8d-203">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="40d8d-204">Sí</span><span class="sxs-lookup"><span data-stu-id="40d8d-204">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="40d8d-205">Sí</span><span class="sxs-lookup"><span data-stu-id="40d8d-205">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="40d8d-206">Sí</span><span class="sxs-lookup"><span data-stu-id="40d8d-206">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="40d8d-207">No és vàlid</span><span class="sxs-lookup"><span data-stu-id="40d8d-207">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="40d8d-208">Infracció de la regla 2.</span><span class="sxs-lookup"><span data-stu-id="40d8d-208">Violation of Rule #2.</span></span> <span data-ttu-id="40d8d-209">El temps, les despeses i les tarifes del projecte P1 s'inclouen a les línies d'oferta QL1 i QL2</span><span class="sxs-lookup"><span data-stu-id="40d8d-209">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="40d8d-210">O1</span><span class="sxs-lookup"><span data-stu-id="40d8d-210">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="40d8d-211">T1</span><span class="sxs-lookup"><span data-stu-id="40d8d-211">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="40d8d-212">QL2</span><span class="sxs-lookup"><span data-stu-id="40d8d-212">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="40d8d-213">P1</span><span class="sxs-lookup"><span data-stu-id="40d8d-213">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="40d8d-214">En blanc</span><span class="sxs-lookup"><span data-stu-id="40d8d-214">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="40d8d-215">Sí</span><span class="sxs-lookup"><span data-stu-id="40d8d-215">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="40d8d-216">Sí</span><span class="sxs-lookup"><span data-stu-id="40d8d-216">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="40d8d-217">Sí</span><span class="sxs-lookup"><span data-stu-id="40d8d-217">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="40d8d-218">Sí</span><span class="sxs-lookup"><span data-stu-id="40d8d-218">Yes</span></span> </p>
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
<span data-ttu-id="40d8d-219">O1</span><span class="sxs-lookup"><span data-stu-id="40d8d-219">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="40d8d-220">T1</span><span class="sxs-lookup"><span data-stu-id="40d8d-220">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="40d8d-221">QL1</span><span class="sxs-lookup"><span data-stu-id="40d8d-221">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="40d8d-222">P1</span><span class="sxs-lookup"><span data-stu-id="40d8d-222">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="40d8d-223">En blanc</span><span class="sxs-lookup"><span data-stu-id="40d8d-223">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="40d8d-224">Sí</span><span class="sxs-lookup"><span data-stu-id="40d8d-224">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="40d8d-225">No</span><span class="sxs-lookup"><span data-stu-id="40d8d-225">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="40d8d-226">Sí</span><span class="sxs-lookup"><span data-stu-id="40d8d-226">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="40d8d-227">Sí</span><span class="sxs-lookup"><span data-stu-id="40d8d-227">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="40d8d-228">No és vàlid</span><span class="sxs-lookup"><span data-stu-id="40d8d-228">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="40d8d-229">Infracció de la regla 2.</span><span class="sxs-lookup"><span data-stu-id="40d8d-229">Violation of Rule #2.</span></span> <span data-ttu-id="40d8d-230">El temps, el material i les tarifes del projecte P1 s'inclouen a les línies d'oferta QL1 i QL2</span><span class="sxs-lookup"><span data-stu-id="40d8d-230">Time, Material, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="40d8d-231">O1</span><span class="sxs-lookup"><span data-stu-id="40d8d-231">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="40d8d-232">T1</span><span class="sxs-lookup"><span data-stu-id="40d8d-232">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="40d8d-233">QL2</span><span class="sxs-lookup"><span data-stu-id="40d8d-233">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="40d8d-234">P1</span><span class="sxs-lookup"><span data-stu-id="40d8d-234">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="40d8d-235">En blanc</span><span class="sxs-lookup"><span data-stu-id="40d8d-235">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="40d8d-236">Sí</span><span class="sxs-lookup"><span data-stu-id="40d8d-236">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="40d8d-237">Sí</span><span class="sxs-lookup"><span data-stu-id="40d8d-237">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="40d8d-238">Sí</span><span class="sxs-lookup"><span data-stu-id="40d8d-238">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="40d8d-239">Sí</span><span class="sxs-lookup"><span data-stu-id="40d8d-239">Yes</span></span> </p>
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
<span data-ttu-id="40d8d-240">O1</span><span class="sxs-lookup"><span data-stu-id="40d8d-240">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="40d8d-241">T1</span><span class="sxs-lookup"><span data-stu-id="40d8d-241">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="40d8d-242">QL1</span><span class="sxs-lookup"><span data-stu-id="40d8d-242">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="40d8d-243">P1</span><span class="sxs-lookup"><span data-stu-id="40d8d-243">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="40d8d-244">En blanc</span><span class="sxs-lookup"><span data-stu-id="40d8d-244">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="40d8d-245">Sí</span><span class="sxs-lookup"><span data-stu-id="40d8d-245">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="40d8d-246">No</span><span class="sxs-lookup"><span data-stu-id="40d8d-246">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="40d8d-247">Sí</span><span class="sxs-lookup"><span data-stu-id="40d8d-247">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="40d8d-248">Sí</span><span class="sxs-lookup"><span data-stu-id="40d8d-248">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="40d8d-249">Vàlida</span><span class="sxs-lookup"><span data-stu-id="40d8d-249">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="40d8d-250">El temps, el material i les tarifes del projecte P1 s'inclouen a QL1</span><span class="sxs-lookup"><span data-stu-id="40d8d-250">Time, Material, and Fees on P1 project are included on QL1</span></span> <br>
<span data-ttu-id="40d8d-251">La despesa del projecte P1 s'inclou a QL2</span><span class="sxs-lookup"><span data-stu-id="40d8d-251">Expense on P1 project is included on QL2</span></span> <br>
<span data-ttu-id="40d8d-252">No se superposa el que s'inclou a cada línia d'oferta i, per tant, és vàlid.</span><span class="sxs-lookup"><span data-stu-id="40d8d-252">No overlap in what is being included on each quote line and therefore valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="40d8d-253">O1</span><span class="sxs-lookup"><span data-stu-id="40d8d-253">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="40d8d-254">T1</span><span class="sxs-lookup"><span data-stu-id="40d8d-254">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="40d8d-255">QL2</span><span class="sxs-lookup"><span data-stu-id="40d8d-255">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="40d8d-256">P1</span><span class="sxs-lookup"><span data-stu-id="40d8d-256">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="40d8d-257">En blanc</span><span class="sxs-lookup"><span data-stu-id="40d8d-257">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="40d8d-258">No</span><span class="sxs-lookup"><span data-stu-id="40d8d-258">No</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="40d8d-259">Sí</span><span class="sxs-lookup"><span data-stu-id="40d8d-259">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="40d8d-260">No</span><span class="sxs-lookup"><span data-stu-id="40d8d-260">No</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="40d8d-261">No</span><span class="sxs-lookup"><span data-stu-id="40d8d-261">No</span></span> </p>
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
<span data-ttu-id="40d8d-262">O1</span><span class="sxs-lookup"><span data-stu-id="40d8d-262">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="40d8d-263">T1</span><span class="sxs-lookup"><span data-stu-id="40d8d-263">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="40d8d-264">QL1</span><span class="sxs-lookup"><span data-stu-id="40d8d-264">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="40d8d-265">P1</span><span class="sxs-lookup"><span data-stu-id="40d8d-265">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="40d8d-266">Només les tasques seleccionades</span><span class="sxs-lookup"><span data-stu-id="40d8d-266">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="40d8d-267">Sí</span><span class="sxs-lookup"><span data-stu-id="40d8d-267">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="40d8d-268">Sí</span><span class="sxs-lookup"><span data-stu-id="40d8d-268">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="40d8d-269">Sí</span><span class="sxs-lookup"><span data-stu-id="40d8d-269">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="40d8d-270">Sí</span><span class="sxs-lookup"><span data-stu-id="40d8d-270">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="40d8d-271">No és vàlid</span><span class="sxs-lookup"><span data-stu-id="40d8d-271">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="40d8d-272">Infracció de la regla núm. 2</span><span class="sxs-lookup"><span data-stu-id="40d8d-272">Violation of Rule #2</span></span> </p>
                <p>
<span data-ttu-id="40d8d-273">El Q1 inclou temps, material, despeses i tarifes en un subconjunt de tasques al projecte P1</span><span class="sxs-lookup"><span data-stu-id="40d8d-273">Q1 includes Time, Material, Expenses and Fees on a subset of tasks on project P1</span></span> </p>
                <p>
<span data-ttu-id="40d8d-274">QL2 inclou temps, despeses i tarifes per a tot el projecte P1 i, per tant, se superposa amb el que s'inclou a Q1.</span><span class="sxs-lookup"><span data-stu-id="40d8d-274">QL2 includes Time, Expenses, and Fees for the whole project P1 and therefore overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="40d8d-275">O1</span><span class="sxs-lookup"><span data-stu-id="40d8d-275">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="40d8d-276">T1</span><span class="sxs-lookup"><span data-stu-id="40d8d-276">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="40d8d-277">QL2</span><span class="sxs-lookup"><span data-stu-id="40d8d-277">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="40d8d-278">P1</span><span class="sxs-lookup"><span data-stu-id="40d8d-278">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="40d8d-279">En blanc</span><span class="sxs-lookup"><span data-stu-id="40d8d-279">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="40d8d-280">Sí</span><span class="sxs-lookup"><span data-stu-id="40d8d-280">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="40d8d-281">Sí</span><span class="sxs-lookup"><span data-stu-id="40d8d-281">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="40d8d-282">Sí</span><span class="sxs-lookup"><span data-stu-id="40d8d-282">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="40d8d-283">Sí</span><span class="sxs-lookup"><span data-stu-id="40d8d-283">Yes</span></span> </p>
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
<span data-ttu-id="40d8d-284">O1</span><span class="sxs-lookup"><span data-stu-id="40d8d-284">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="40d8d-285">T1</span><span class="sxs-lookup"><span data-stu-id="40d8d-285">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="40d8d-286">QL1</span><span class="sxs-lookup"><span data-stu-id="40d8d-286">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="40d8d-287">P1</span><span class="sxs-lookup"><span data-stu-id="40d8d-287">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="40d8d-288">Només les tasques seleccionades</span><span class="sxs-lookup"><span data-stu-id="40d8d-288">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="40d8d-289">Sí</span><span class="sxs-lookup"><span data-stu-id="40d8d-289">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="40d8d-290">Sí</span><span class="sxs-lookup"><span data-stu-id="40d8d-290">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="40d8d-291">Sí</span><span class="sxs-lookup"><span data-stu-id="40d8d-291">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="40d8d-292">Sí</span><span class="sxs-lookup"><span data-stu-id="40d8d-292">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="40d8d-293">Vàlida</span><span class="sxs-lookup"><span data-stu-id="40d8d-293">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="40d8d-294">Segons la regla núm. 3,</span><span class="sxs-lookup"><span data-stu-id="40d8d-294">Per Rule #3,</span></span> </p>
                <p>
<span data-ttu-id="40d8d-295">El Q1 inclou temps, material, despeses i tarifes en un subconjunt de tasques al projecte P1.</span><span class="sxs-lookup"><span data-stu-id="40d8d-295">Q1 includes Time, Material, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="40d8d-296">El QL2 inclou temps, material, despeses i tarifes per a un subconjunt de tasques al projecte P1.</span><span class="sxs-lookup"><span data-stu-id="40d8d-296">QL2 includes Time, Material, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="40d8d-297">L'única validació addicional és per al subconjunt de tasques de QL1, que és diferent del subconjunt de tasques de QL2 per assegurar que no hi ha superposició.</span><span class="sxs-lookup"><span data-stu-id="40d8d-297">The only additional validation is around the subset of tasks on QL1 which is different from the subset of tasks on QL2 to ensure that there is no overlap.</span></span> <span data-ttu-id="40d8d-298">Això ho fa el sistema quan s'associen les tasques.</span><span class="sxs-lookup"><span data-stu-id="40d8d-298">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="40d8d-299">O1</span><span class="sxs-lookup"><span data-stu-id="40d8d-299">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="40d8d-300">T1</span><span class="sxs-lookup"><span data-stu-id="40d8d-300">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="40d8d-301">QL2</span><span class="sxs-lookup"><span data-stu-id="40d8d-301">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="40d8d-302">P1</span><span class="sxs-lookup"><span data-stu-id="40d8d-302">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="40d8d-303">Només les tasques seleccionades</span><span class="sxs-lookup"><span data-stu-id="40d8d-303">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="40d8d-304">Sí</span><span class="sxs-lookup"><span data-stu-id="40d8d-304">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="40d8d-305">Sí</span><span class="sxs-lookup"><span data-stu-id="40d8d-305">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="40d8d-306">Sí</span><span class="sxs-lookup"><span data-stu-id="40d8d-306">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="40d8d-307">Sí</span><span class="sxs-lookup"><span data-stu-id="40d8d-307">Yes</span></span> </p>
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
<span data-ttu-id="40d8d-308">O1</span><span class="sxs-lookup"><span data-stu-id="40d8d-308">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="40d8d-309">T1</span><span class="sxs-lookup"><span data-stu-id="40d8d-309">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="40d8d-310">QL1</span><span class="sxs-lookup"><span data-stu-id="40d8d-310">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="40d8d-311">P1</span><span class="sxs-lookup"><span data-stu-id="40d8d-311">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="40d8d-312">Totes les tasques del projecte o en blanc</span><span class="sxs-lookup"><span data-stu-id="40d8d-312">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="40d8d-313">Sí</span><span class="sxs-lookup"><span data-stu-id="40d8d-313">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="40d8d-314">Sí</span><span class="sxs-lookup"><span data-stu-id="40d8d-314">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="40d8d-315">Sí</span><span class="sxs-lookup"><span data-stu-id="40d8d-315">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="40d8d-316">Sí</span><span class="sxs-lookup"><span data-stu-id="40d8d-316">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="40d8d-317">Vàlida</span><span class="sxs-lookup"><span data-stu-id="40d8d-317">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="40d8d-318">Segons la regla núm. 5, Q1 i Q2 són dues ofertes per a la mateixa oportunitat, de manera que poden calcular ambdós els mateixos components d'un projecte.</span><span class="sxs-lookup"><span data-stu-id="40d8d-318">Per Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="40d8d-319">O1</span><span class="sxs-lookup"><span data-stu-id="40d8d-319">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="40d8d-320">T2</span><span class="sxs-lookup"><span data-stu-id="40d8d-320">Q2</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="40d8d-321">QL1</span><span class="sxs-lookup"><span data-stu-id="40d8d-321">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="40d8d-322">P1</span><span class="sxs-lookup"><span data-stu-id="40d8d-322">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="40d8d-323">Totes les tasques del projecte o en blanc</span><span class="sxs-lookup"><span data-stu-id="40d8d-323">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="40d8d-324">Sí</span><span class="sxs-lookup"><span data-stu-id="40d8d-324">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="40d8d-325">Sí</span><span class="sxs-lookup"><span data-stu-id="40d8d-325">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="40d8d-326">Sí</span><span class="sxs-lookup"><span data-stu-id="40d8d-326">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="40d8d-327">Sí</span><span class="sxs-lookup"><span data-stu-id="40d8d-327">Yes</span></span> </p>
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
<span data-ttu-id="40d8d-328">O1</span><span class="sxs-lookup"><span data-stu-id="40d8d-328">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="40d8d-329">T1</span><span class="sxs-lookup"><span data-stu-id="40d8d-329">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="40d8d-330">QL1</span><span class="sxs-lookup"><span data-stu-id="40d8d-330">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="40d8d-331">P1</span><span class="sxs-lookup"><span data-stu-id="40d8d-331">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="40d8d-332">Totes les tasques del projecte o en blanc</span><span class="sxs-lookup"><span data-stu-id="40d8d-332">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="40d8d-333">Sí</span><span class="sxs-lookup"><span data-stu-id="40d8d-333">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="40d8d-334">Sí</span><span class="sxs-lookup"><span data-stu-id="40d8d-334">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="40d8d-335">Sí</span><span class="sxs-lookup"><span data-stu-id="40d8d-335">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="40d8d-336">Sí</span><span class="sxs-lookup"><span data-stu-id="40d8d-336">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="40d8d-337">No és vàlid</span><span class="sxs-lookup"><span data-stu-id="40d8d-337">Not Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="40d8d-338">Segons la regla núm. 4, Q1 i Q2 són dues ofertes d'oportunitats diferents, de manera que no poden calcular els mateixos components del mateix projecte.</span><span class="sxs-lookup"><span data-stu-id="40d8d-338">Per Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="40d8d-339">O2</span><span class="sxs-lookup"><span data-stu-id="40d8d-339">O2</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="40d8d-340">T1</span><span class="sxs-lookup"><span data-stu-id="40d8d-340">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="40d8d-341">QL1</span><span class="sxs-lookup"><span data-stu-id="40d8d-341">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="40d8d-342">P1</span><span class="sxs-lookup"><span data-stu-id="40d8d-342">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="40d8d-343">Totes les tasques del projecte o en blanc</span><span class="sxs-lookup"><span data-stu-id="40d8d-343">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="40d8d-344">Sí</span><span class="sxs-lookup"><span data-stu-id="40d8d-344">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="40d8d-345">Sí</span><span class="sxs-lookup"><span data-stu-id="40d8d-345">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="40d8d-346">Sí</span><span class="sxs-lookup"><span data-stu-id="40d8d-346">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="40d8d-347">Sí</span><span class="sxs-lookup"><span data-stu-id="40d8d-347">Yes</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
