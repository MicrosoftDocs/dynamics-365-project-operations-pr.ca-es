---
title: Informació general de les línies de contracte basades en projectes
description: Aquest tema proporciona informació sobre com treballar amb línies de contracte basades en projectes.
author: rumant
manager: Annbe
ms.date: 10/28/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 824fdd54d7b513b49afd1a6d76d3387df81418e2
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858146"
---
# <a name="project-based-contract-lines-overview"></a><span data-ttu-id="2fe6a-103">Informació general de les línies de contracte basades en projectes</span><span class="sxs-lookup"><span data-stu-id="2fe6a-103">Project-based contract lines overview</span></span>

<span data-ttu-id="2fe6a-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_</span><span class="sxs-lookup"><span data-stu-id="2fe6a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="2fe6a-105">Les línies de contracte basades en projectes al Dynamics 365 Project Operations estan dissenyades per contenir l'estimació i els acords de facturació per a components específics del treball del projecte en una interacció.</span><span class="sxs-lookup"><span data-stu-id="2fe6a-105">Project-based contract lines in Dynamics 365 Project Operations are designed to hold the estimate and billing agreements for specific components of project work on an engagement.</span></span> <span data-ttu-id="2fe6a-106">L'estructura d'una línia de contracte basada en projectes s'amplia per a les estimacions del projecte i els escenaris de facturació amb els següents conceptes:</span><span class="sxs-lookup"><span data-stu-id="2fe6a-106">The structure of a project–based contract line is extended for project estimates and billing scenarios with the following concepts:</span></span>

- <span data-ttu-id="2fe6a-107">Mètode de facturació</span><span class="sxs-lookup"><span data-stu-id="2fe6a-107">Billing method</span></span>
- <span data-ttu-id="2fe6a-108">Assignació de projectes i tasques</span><span class="sxs-lookup"><span data-stu-id="2fe6a-108">Project and task mapping</span></span>
- <span data-ttu-id="2fe6a-109">Classes de transaccions incloses</span><span class="sxs-lookup"><span data-stu-id="2fe6a-109">Included transaction classes</span></span>
- <span data-ttu-id="2fe6a-110">Límit que no s’ha de superar</span><span class="sxs-lookup"><span data-stu-id="2fe6a-110">Not-to-exceed limit</span></span>
- <span data-ttu-id="2fe6a-111">Configuració de la imputabilitat</span><span class="sxs-lookup"><span data-stu-id="2fe6a-111">Chargeability setup</span></span>
- <span data-ttu-id="2fe6a-112">Estimacions amb detalls de línia de contracte</span><span class="sxs-lookup"><span data-stu-id="2fe6a-112">Estimates using contract line details</span></span>
- <span data-ttu-id="2fe6a-113">Clients de línia de contracte</span><span class="sxs-lookup"><span data-stu-id="2fe6a-113">Contract line customers</span></span>

<span data-ttu-id="2fe6a-114">A la taula següent s'inclouen els camps de la pestanya **General** de les línies de contracte basades en projectes que ajuden a configurar la base per a ajustaments detallats, d'estimacions des de zero i facturació per al treball basat en el projecte.</span><span class="sxs-lookup"><span data-stu-id="2fe6a-114">The following table includes the fields on the **General** tab of project–based contract lines that help set up the basis for a detailed, ground–up estimate and billing arrangements for project–based work.</span></span>

| <span data-ttu-id="2fe6a-115">Camp</span><span class="sxs-lookup"><span data-stu-id="2fe6a-115">Field</span></span> | <span data-ttu-id="2fe6a-116">Descripció</span><span class="sxs-lookup"><span data-stu-id="2fe6a-116">Description</span></span> | <span data-ttu-id="2fe6a-117">Impacte descendent</span><span class="sxs-lookup"><span data-stu-id="2fe6a-117">Downstream impact</span></span> |
| --- | --- | --- |
| <span data-ttu-id="2fe6a-118">**Nom**</span><span class="sxs-lookup"><span data-stu-id="2fe6a-118">**Name**</span></span> | <span data-ttu-id="2fe6a-119">Nom de la línia de contracte.</span><span class="sxs-lookup"><span data-stu-id="2fe6a-119">Name of the contract line.</span></span> <span data-ttu-id="2fe6a-120">Això identifica el component discret del contracte que s'estima.</span><span class="sxs-lookup"><span data-stu-id="2fe6a-120">This identifies the discrete component of the contract that is being estimated.</span></span> <span data-ttu-id="2fe6a-121">Per a un contracte de projecte creat a partir d'una oferta, aquest valor es copia d'un valor corresponent de la línia d'oferta basada en el projecte.</span><span class="sxs-lookup"><span data-stu-id="2fe6a-121">For a project contract created from a quote, this value is copied from a corresponding value of the project-based quote line.</span></span> | <span data-ttu-id="2fe6a-122">Nom que es copia a la línia de factura del projecte que es crea a partir d'aquesta línia de contracte quan es crea la factura.</span><span class="sxs-lookup"><span data-stu-id="2fe6a-122">The name copied over to the project invoice line that is created from this contract line when the invoice is created.</span></span> |
| <span data-ttu-id="2fe6a-123">**Mètode de facturació**</span><span class="sxs-lookup"><span data-stu-id="2fe6a-123">**Billing Method**</span></span> | <span data-ttu-id="2fe6a-124">En un contracte de projecte creat a partir d'una oferta, aquest valor es copia del camp corresponent de la línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="2fe6a-124">On a project contract created from a quote, this value is copied from the corresponding field on the quote line.</span></span> <span data-ttu-id="2fe6a-125">Aquest és un conjunt d'opcions que representa els dos principals models de contractació admesos pel Project Operations:</span><span class="sxs-lookup"><span data-stu-id="2fe6a-125">This is an option set that represents the two main contracting models supported by Project Operations:</span></span></br><span data-ttu-id="2fe6a-126">- **Preu fix**</span><span class="sxs-lookup"><span data-stu-id="2fe6a-126">- **Fixed Price**</span></span></br><span data-ttu-id="2fe6a-127">- **Temps i material**</span><span class="sxs-lookup"><span data-stu-id="2fe6a-127">- **Time and Material**</span></span> | <span data-ttu-id="2fe6a-128">En funció del mètode de facturació de la línia de contracte a la qual es fa referència, es processarà la transacció de valors reals.</span><span class="sxs-lookup"><span data-stu-id="2fe6a-128">Based on the billing method of the referenced contract line, the actual transaction will be processed.</span></span> <span data-ttu-id="2fe6a-129">Si la línia de contracte a la qual fa referència el valor real té un mètode de facturació de temps i material, es creen registres de cost i de valor real de vendes no facturades.</span><span class="sxs-lookup"><span data-stu-id="2fe6a-129">If the contract line referenced by the actual has a time and material billing method, cost and unbilled sales actual records are created.</span></span> <span data-ttu-id="2fe6a-130">Si la línia de contracte a la qual fa referència el valor real té un mètode de facturació de preu fix, només es crea un valor real de cost.</span><span class="sxs-lookup"><span data-stu-id="2fe6a-130">If the contract line referenced by the actual has a fixed price billing method, only a cost actual is created.</span></span> |
| <span data-ttu-id="2fe6a-131">**Project**</span><span class="sxs-lookup"><span data-stu-id="2fe6a-131">**Project**</span></span> | <span data-ttu-id="2fe6a-132">Utilitzeu aquest camp per identificar el projecte que s'utilitzarà per lliurar el treball en aquesta interacció.</span><span class="sxs-lookup"><span data-stu-id="2fe6a-132">Use this field to identify the project that will be used to deliver the work on this engagement.</span></span> | <span data-ttu-id="2fe6a-133">Aquest valor s'utilitzarà conjuntament amb **Tasques incloses** i **Classes de transaccions incloses** per resoldre la referència de línia de contracte en un registre de línia real o de previsió.</span><span class="sxs-lookup"><span data-stu-id="2fe6a-133">This value will be used in conjunction with **Included Tasks** and **Included Transaction Classes** to resolve the contract line reference on an actual or estimate line record.</span></span> |
| <span data-ttu-id="2fe6a-134">**Tasques incloses**</span><span class="sxs-lookup"><span data-stu-id="2fe6a-134">**Included Tasks**</span></span> | <span data-ttu-id="2fe6a-135">Indica si aquesta línia de contracte inclou totes les tasques del projecte per al projecte seleccionat o només un subconjunt de les tasques.</span><span class="sxs-lookup"><span data-stu-id="2fe6a-135">Indicates if this contract line includes all project tasks for the selected project or only a subset of the tasks.</span></span> <span data-ttu-id="2fe6a-136">És un conjunt d'opcions que té els següents valors possibles:</span><span class="sxs-lookup"><span data-stu-id="2fe6a-136">This is an option set that has the following possible values:</span></span></br><span data-ttu-id="2fe6a-137">- **Totes les tasques de projecte**</span><span class="sxs-lookup"><span data-stu-id="2fe6a-137">- **All Project Tasks**</span></span></br><span data-ttu-id="2fe6a-138">- **Només les tasques de projecte seleccionades**.</span><span class="sxs-lookup"><span data-stu-id="2fe6a-138">- **Selected Project Tasks Only**.</span></span> <span data-ttu-id="2fe6a-139">Un valor en blanc en aquest camp és igual a seleccionar **Totes les tasques del projecte**.</span><span class="sxs-lookup"><span data-stu-id="2fe6a-139">A blank value in this field is equal to selecting **All Project Tasks**.</span></span> | <span data-ttu-id="2fe6a-140">Si se selecciona **Només les tasques seleccionades**, podeu seleccionar tasques específiques i associar-les a aquesta línia de contracte a la pestanya **Configuració de la facturació de tasques** de la pàgina **Projecte**.</span><span class="sxs-lookup"><span data-stu-id="2fe6a-140">If **Selected Tasks Only** is selected, you can select specific tasks and associate them to this contract line on the **Task Billing Setup** tab on the **Project** page.</span></span> <span data-ttu-id="2fe6a-141">El valor s'utilitzarà conjuntament amb **Projecte** i **Classes de transacció incloses** per resoldre la referència de la línia de contracte en un registre de línia real o estimat.</span><span class="sxs-lookup"><span data-stu-id="2fe6a-141">The value will be used in conjunction with **Project** and **Included Transaction** classes to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="2fe6a-142">**Inclou el temps**</span><span class="sxs-lookup"><span data-stu-id="2fe6a-142">**Include Time**</span></span> | <span data-ttu-id="2fe6a-143">Un valor **Sí**/**No** indica si les transaccions de temps o els costos laborals del projecte seleccionat s'inclouran en aquesta línia de contracte.</span><span class="sxs-lookup"><span data-stu-id="2fe6a-143">A **Yes**/**No** value indicates if time transactions or labor costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="2fe6a-144">Un valor **No** indica que les transaccions de temps o els costos laborals no s'inclouran en aquesta línia de contracte.</span><span class="sxs-lookup"><span data-stu-id="2fe6a-144">A **No** value indicates that the time transactions or labor cost will not be included on this contract line.</span></span> <span data-ttu-id="2fe6a-145">Un valor **Sí** indica que s'inclouran.</span><span class="sxs-lookup"><span data-stu-id="2fe6a-145">A **Yes** value indicates that they will.</span></span> | <span data-ttu-id="2fe6a-146">Aquest valor s'utilitza conjuntament amb el projecte per resoldre la referència de línia de contracte en un registre real o de línia de previsió.</span><span class="sxs-lookup"><span data-stu-id="2fe6a-146">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="2fe6a-147">**Inclou la despesa**</span><span class="sxs-lookup"><span data-stu-id="2fe6a-147">**Include Expense**</span></span> | <span data-ttu-id="2fe6a-148">Un valor **Sí**/**No** indica si els costos de despeses del projecte seleccionat s'inclouran a la previsió en aquesta línia de contracte.</span><span class="sxs-lookup"><span data-stu-id="2fe6a-148">A **Yes**/**No** value indicates if expense costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="2fe6a-149">Un valor **No** indica que el cost de despesa no s'inclourà en aquesta línia de contracte.</span><span class="sxs-lookup"><span data-stu-id="2fe6a-149">A **No** value indicates that the expense cost will not be included on this contract line.</span></span> <span data-ttu-id="2fe6a-150">Un valor **Sí** indica que s'inclourà.</span><span class="sxs-lookup"><span data-stu-id="2fe6a-150">A **Yes** value indicates that it will.</span></span> | <span data-ttu-id="2fe6a-151">Aquest valor s'utilitza conjuntament amb el projecte per resoldre la referència de línia de contracte en un registre real o de línia de previsió.</span><span class="sxs-lookup"><span data-stu-id="2fe6a-151">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="2fe6a-152">**Inclou els materials**</span><span class="sxs-lookup"><span data-stu-id="2fe6a-152">**Include Materials**</span></span> | <span data-ttu-id="2fe6a-153">Un valor **Sí**/**No** indica si els costos de materials del projecte seleccionat s'inclouran a la previsió en aquesta línia de contracte.</span><span class="sxs-lookup"><span data-stu-id="2fe6a-153">A **Yes**/**No** value indicates if material costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="2fe6a-154">Un valor **No** indica que els costos de materials no s'inclouran en aquesta línia del contracte.</span><span class="sxs-lookup"><span data-stu-id="2fe6a-154">A **No** value indicates that the material costs will not be included on this contract line.</span></span> <span data-ttu-id="2fe6a-155">Un valor **Sí** indica que s'inclourà.</span><span class="sxs-lookup"><span data-stu-id="2fe6a-155">A **Yes** value indicates that it will.</span></span> | <span data-ttu-id="2fe6a-156">Aquest valor s'utilitza conjuntament amb el projecte per resoldre la referència de línia de contracte en un registre real o de línia de previsió.</span><span class="sxs-lookup"><span data-stu-id="2fe6a-156">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="2fe6a-157">**Inclou la taxa**</span><span class="sxs-lookup"><span data-stu-id="2fe6a-157">**Include Fee**</span></span> | <span data-ttu-id="2fe6a-158">Un valor **Sí**/**No** indica si les tarifes del projecte seleccionat s'inclouran a la previsió en aquesta línia de contracte.</span><span class="sxs-lookup"><span data-stu-id="2fe6a-158">A **Yes**/**No** value indicates if fees on the selected project will be included on this contract line.</span></span> <span data-ttu-id="2fe6a-159">Un valor **No** indica que els càrrecs no s'inclouran en aquesta línia de contracte.</span><span class="sxs-lookup"><span data-stu-id="2fe6a-159">A **No** value indicates that the fees will not be included on this contract line.</span></span> <span data-ttu-id="2fe6a-160">Un valor **Sí** indica que s'inclouran.</span><span class="sxs-lookup"><span data-stu-id="2fe6a-160">A **Yes** value indicates that they will.</span></span> | <span data-ttu-id="2fe6a-161">Aquest valor s'utilitza conjuntament amb el projecte per resoldre la referència de línia de contracte en un registre real o de línia de previsió.</span><span class="sxs-lookup"><span data-stu-id="2fe6a-161">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="2fe6a-162">**Import contractat**</span><span class="sxs-lookup"><span data-stu-id="2fe6a-162">**Contracted Amount**</span></span> | <span data-ttu-id="2fe6a-163">En una línia de contracte de preu fix, aquest import és el valor acordat que es facturarà al client per a tots els components de treball associats amb aquesta línia de contracte.</span><span class="sxs-lookup"><span data-stu-id="2fe6a-163">On a fixed price contract line, this amount is the agreed-on value that will be invoiced to the customer for all the work components associated to this contract line.</span></span> <span data-ttu-id="2fe6a-164">En una línia de contracte de temps i material, aquest import és un valor estimat del que es facturarà al client per a tots els components de treball associats a aquesta línia de contracte.</span><span class="sxs-lookup"><span data-stu-id="2fe6a-164">On a time and material contract line, this amount is an estimated value of what will be invoiced to the customer for all the work components associated to this contract line.</span></span> <span data-ttu-id="2fe6a-165">En un contracte de projecte creat a partir d'una oferta, aquest valor es copia del camp corresponent de la línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="2fe6a-165">On a project contract that is created from a quote, this value is copied from the corresponding field on the quote line.</span></span> <span data-ttu-id="2fe6a-166">Quan una línia de contracte basada en un projecte té detalls de la línia, aquest camp no es pot editar i es resumeix a partir de l'import dels detalls de la línia de contracte.</span><span class="sxs-lookup"><span data-stu-id="2fe6a-166">When a project–based contract line has line details, this field is locked for editing and is summarized from the amount on the contract line details.</span></span> | <span data-ttu-id="2fe6a-167">Quan la línia de contracte té detalls de la línia, aquest valor es pot modificar canviant els imports als detalls de la línia.</span><span class="sxs-lookup"><span data-stu-id="2fe6a-167">When the contract line has line details, this value can be modified by changing the amounts on the line details.</span></span> <span data-ttu-id="2fe6a-168">En una línia de contracte de preu fix, aquest valor s'utilitza per generar l'import abans de l'impost a les fites de facturació periòdiques.</span><span class="sxs-lookup"><span data-stu-id="2fe6a-168">On a fixed price contract line, this value is used to generate the amount before tax on periodic billing milestones.</span></span> |
| <span data-ttu-id="2fe6a-169">**Impost estimat**</span><span class="sxs-lookup"><span data-stu-id="2fe6a-169">**Estimated Tax**</span></span> | <span data-ttu-id="2fe6a-170">L'usuari pot editar aquest camp per introduir l'import d'impostos estimat en la línia de contracte.</span><span class="sxs-lookup"><span data-stu-id="2fe6a-170">The user can edit this field to input the estimated tax amount on the contract line.</span></span> <span data-ttu-id="2fe6a-171">Quan una línia de contracte basada en un projecte té detalls de la línia, aquest camp no es pot editar i es resumeix a partir de l'import d'impostos dels detalls de la línia de contracte.</span><span class="sxs-lookup"><span data-stu-id="2fe6a-171">When a project–based contract line has line details, this field is locked for editing and is summarized from the tax amount on the contract line details.</span></span> | <span data-ttu-id="2fe6a-172">Quan la línia de contracte té detalls de la línia, aquest valor es pot modificar canviant els imports d'impostos als detalls de la línia.</span><span class="sxs-lookup"><span data-stu-id="2fe6a-172">When the contract line has line details, this value can be modified by changing the tax amounts on the line details.</span></span> <span data-ttu-id="2fe6a-173">En una línia de contracte de preu fix, aquest valor s'utilitza per generar l'impost a les fites de facturació periòdiques.</span><span class="sxs-lookup"><span data-stu-id="2fe6a-173">On a fixed price contract line, this value is used to generate the tax on periodic billing milestones.</span></span> |
| <span data-ttu-id="2fe6a-174">**Import contractat després d’impostos**</span><span class="sxs-lookup"><span data-stu-id="2fe6a-174">**Contracted Amount after Tax**</span></span> | <span data-ttu-id="2fe6a-175">Import de la línia de contracte després de l'impost.</span><span class="sxs-lookup"><span data-stu-id="2fe6a-175">The contract line amount after tax.</span></span> <span data-ttu-id="2fe6a-176">Aquest camp és de només lectura i es calcula com a **Import contractat + Impostos**.</span><span class="sxs-lookup"><span data-stu-id="2fe6a-176">This field is read only and is calculated as **Contracted Amount + Tax**.</span></span> | <span data-ttu-id="2fe6a-177">En una línia de contracte de preu fix, aquest valor s'utilitza per generar fites de facturació periòdiques.</span><span class="sxs-lookup"><span data-stu-id="2fe6a-177">On a fixed price contract line, this value is used to generate periodic billing milestones.</span></span> |
| <span data-ttu-id="2fe6a-178">**Límit que no s’ha de superar**</span><span class="sxs-lookup"><span data-stu-id="2fe6a-178">**Not-to-Exceed Limit**</span></span> | <span data-ttu-id="2fe6a-179">L'usuari pot editar aquest camp i només està disponible en línies de contracte basades en projectes que tenen el mètode de facturació definit en temps i material.</span><span class="sxs-lookup"><span data-stu-id="2fe6a-179">The user can edit this field and it is only available on project-based contract lines that have the billing method set as time and material.</span></span> | <span data-ttu-id="2fe6a-180">L'usuari pot editar aquest camp.</span><span class="sxs-lookup"><span data-stu-id="2fe6a-180">The user can edit this field.</span></span> <span data-ttu-id="2fe6a-181">Quan un valor real de temps i material fa referència a aquesta línia de contracte per temps i material, l'import del valor real s'avalua amb el límit que no es pot superar de la línia de contracte.</span><span class="sxs-lookup"><span data-stu-id="2fe6a-181">When an actual for time and material references this contract line for time and material, the amount on the actual is evaluated against the not-to-exceed limit on the contract line.</span></span> <span data-ttu-id="2fe6a-182">Aquesta avaluació es completa un cop comptabilitzats els imports ja gastats i compromesos.</span><span class="sxs-lookup"><span data-stu-id="2fe6a-182">This evaluation is completed after  the already spent and committed amounts are accounted for.</span></span> |
| <span data-ttu-id="2fe6a-183">**Pressupost del client**</span><span class="sxs-lookup"><span data-stu-id="2fe6a-183">**Customer Budget**</span></span> | <span data-ttu-id="2fe6a-184">Aquest camp és editable i es copia del camp corresponent de la línia d'oferta si el contracte s'ha creat a partir d'una oferta.</span><span class="sxs-lookup"><span data-stu-id="2fe6a-184">This field is editable and is copied from the corresponding field on the quote line if the contract was created from a quote.</span></span> | <span data-ttu-id="2fe6a-185">Aquest camp només s'utilitza per a informació i no té cap importància descendent.</span><span class="sxs-lookup"><span data-stu-id="2fe6a-185">This field is only used for information and does not have any downstream significance.</span></span> |

## <a name="validation-rules-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a><span data-ttu-id="2fe6a-186">Regles de validació per a les opcions a la pestanya General de línies de contracte basades en projectes</span><span class="sxs-lookup"><span data-stu-id="2fe6a-186">Validation rules for the options on the General tab of project-based contract lines</span></span>

<span data-ttu-id="2fe6a-187">Regla 1: si el camp **Tasques incloses** està en blanc o està definit en **Totes les tasques del projecte**, totes les tasques del projecte s'inclouen a la línia de contracte.</span><span class="sxs-lookup"><span data-stu-id="2fe6a-187">Rule 1: If the **Included Tasks** field is blank or set to **All Project Tasks**, all tasks of the project are included on the contract line.</span></span>

<span data-ttu-id="2fe6a-188">Regla 2: quan el camp **Tasques incloses** estigui en blanc o definit explícitament en **Totes les tasques del projecte**, un projecte i una determinada classe de transacció només es poden incloure en una línia de contracte basada en projectes d'un contracte.</span><span class="sxs-lookup"><span data-stu-id="2fe6a-188">Rule 2: When the **Included Tasks** field is blank or explicitly set to **All Project Tasks**, a project and a certain transaction class can only be included on one project-based contract line of a contract.</span></span>

<span data-ttu-id="2fe6a-189">Regla 3: quan el camp **Tasques incloses** estigui definit en **Només les tasques del projecte seleccionades**, un projecte i una determinada classe de transacció només es poden incloure en diverses línies de contracte basades en projectes d'un contracte.</span><span class="sxs-lookup"><span data-stu-id="2fe6a-189">Rule 3: When the **Included Tasks** field is set to **Selected Project Tasks Only**, a project and a certain transaction class can be included on multiple project-based contract lines of a contract.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="43" valign="top">
                <p><span data-ttu-id="2fe6a-190">
                    <strong>Contracte</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2fe6a-190">
                    <strong>Contract</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="2fe6a-191">
                    <strong>Línia de contracte</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2fe6a-191">
                    <strong>Contract line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="2fe6a-192">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2fe6a-192">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="67" valign="top">
                <p><span data-ttu-id="2fe6a-193">
                    <strong>Tasques incloses</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2fe6a-193">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="2fe6a-194">
                    <strong>Inclou el temps</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2fe6a-194">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="2fe6a-195">
                    <strong>Inclou la despesa</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2fe6a-195">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="2fe6a-196">
                    <strong>Inclou els materials</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2fe6a-196">
                    <strong>Include Materials</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="2fe6a-197">
                    <strong>Inclou</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2fe6a-197">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="2fe6a-198">
                    <strong>Tarifa</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2fe6a-198">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="53" valign="top">
                <p><span data-ttu-id="2fe6a-199">
                    <strong>Vàlid/No és vàlid</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2fe6a-199">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="250" valign="top">
                <p><span data-ttu-id="2fe6a-200">
                    <strong>Motiu</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2fe6a-200">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="2fe6a-201">C1</span><span class="sxs-lookup"><span data-stu-id="2fe6a-201">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="2fe6a-202">CL1</span><span class="sxs-lookup"><span data-stu-id="2fe6a-202">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2fe6a-203">P1</span><span class="sxs-lookup"><span data-stu-id="2fe6a-203">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="2fe6a-204">En blanc</span><span class="sxs-lookup"><span data-stu-id="2fe6a-204">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2fe6a-205">Sí</span><span class="sxs-lookup"><span data-stu-id="2fe6a-205">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2fe6a-206">Sí</span><span class="sxs-lookup"><span data-stu-id="2fe6a-206">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2fe6a-207">Sí</span><span class="sxs-lookup"><span data-stu-id="2fe6a-207">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2fe6a-208">Sí</span><span class="sxs-lookup"><span data-stu-id="2fe6a-208">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2fe6a-209">No és vàlid</span><span class="sxs-lookup"><span data-stu-id="2fe6a-209">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2fe6a-210">Infracció de la regla 2.</span><span class="sxs-lookup"><span data-stu-id="2fe6a-210">Violation of Rule #2.</span></span> <span data-ttu-id="2fe6a-211">El temps, les despeses, els materials i les tarifes del projecte P1 s'inclouen a les línies de contracte CL1 i CL2.</span><span class="sxs-lookup"><span data-stu-id="2fe6a-211">Time, Expense, Materials, and Fees on P1 project are included on both Contract lines CL1 and CL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="2fe6a-212">C1</span><span class="sxs-lookup"><span data-stu-id="2fe6a-212">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="2fe6a-213">CL2</span><span class="sxs-lookup"><span data-stu-id="2fe6a-213">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2fe6a-214">P1</span><span class="sxs-lookup"><span data-stu-id="2fe6a-214">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="2fe6a-215">En blanc</span><span class="sxs-lookup"><span data-stu-id="2fe6a-215">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2fe6a-216">Sí</span><span class="sxs-lookup"><span data-stu-id="2fe6a-216">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2fe6a-217">Sí</span><span class="sxs-lookup"><span data-stu-id="2fe6a-217">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2fe6a-218">Sí</span><span class="sxs-lookup"><span data-stu-id="2fe6a-218">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2fe6a-219">Sí</span><span class="sxs-lookup"><span data-stu-id="2fe6a-219">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="2fe6a-220">C1</span><span class="sxs-lookup"><span data-stu-id="2fe6a-220">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="2fe6a-221">CL1</span><span class="sxs-lookup"><span data-stu-id="2fe6a-221">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2fe6a-222">P1</span><span class="sxs-lookup"><span data-stu-id="2fe6a-222">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="2fe6a-223">En blanc</span><span class="sxs-lookup"><span data-stu-id="2fe6a-223">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2fe6a-224">Sí</span><span class="sxs-lookup"><span data-stu-id="2fe6a-224">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2fe6a-225">No</span><span class="sxs-lookup"><span data-stu-id="2fe6a-225">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2fe6a-226">Sí</span><span class="sxs-lookup"><span data-stu-id="2fe6a-226">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2fe6a-227">Sí</span><span class="sxs-lookup"><span data-stu-id="2fe6a-227">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2fe6a-228">No és vàlid</span><span class="sxs-lookup"><span data-stu-id="2fe6a-228">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2fe6a-229">Infracció de la regla 2.</span><span class="sxs-lookup"><span data-stu-id="2fe6a-229">Violation of Rule #2.</span></span> <span data-ttu-id="2fe6a-230">El temps, els materials i les tarifes del projecte P1 s'inclouen a les línies de contracte CL1 i CL2.</span><span class="sxs-lookup"><span data-stu-id="2fe6a-230">Time, Materials, and Fees on P1 project are included on both Contract lines CL1 and CL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="2fe6a-231">C1</span><span class="sxs-lookup"><span data-stu-id="2fe6a-231">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="2fe6a-232">CL2</span><span class="sxs-lookup"><span data-stu-id="2fe6a-232">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2fe6a-233">P1</span><span class="sxs-lookup"><span data-stu-id="2fe6a-233">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="2fe6a-234">En blanc</span><span class="sxs-lookup"><span data-stu-id="2fe6a-234">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2fe6a-235">Sí</span><span class="sxs-lookup"><span data-stu-id="2fe6a-235">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2fe6a-236">Sí</span><span class="sxs-lookup"><span data-stu-id="2fe6a-236">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2fe6a-237">Sí</span><span class="sxs-lookup"><span data-stu-id="2fe6a-237">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2fe6a-238">Sí</span><span class="sxs-lookup"><span data-stu-id="2fe6a-238">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="2fe6a-239">C1</span><span class="sxs-lookup"><span data-stu-id="2fe6a-239">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="2fe6a-240">CL1</span><span class="sxs-lookup"><span data-stu-id="2fe6a-240">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2fe6a-241">P1</span><span class="sxs-lookup"><span data-stu-id="2fe6a-241">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="2fe6a-242">En blanc</span><span class="sxs-lookup"><span data-stu-id="2fe6a-242">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2fe6a-243">Sí</span><span class="sxs-lookup"><span data-stu-id="2fe6a-243">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2fe6a-244">No</span><span class="sxs-lookup"><span data-stu-id="2fe6a-244">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2fe6a-245">Sí</span><span class="sxs-lookup"><span data-stu-id="2fe6a-245">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2fe6a-246">Sí</span><span class="sxs-lookup"><span data-stu-id="2fe6a-246">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2fe6a-247">Vàlida</span><span class="sxs-lookup"><span data-stu-id="2fe6a-247">Valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2fe6a-248">El temps, els materials i les tarifes del projecte P1 s'inclouen a CL1.</span><span class="sxs-lookup"><span data-stu-id="2fe6a-248">Time, Materials, and Fees on P1 project are included on CL1.</span></span>
                </p>
                <ul>
                    <li>
<span data-ttu-id="2fe6a-249">La despesa en el projecte P1 s'inclou a CL2.</span><span class="sxs-lookup"><span data-stu-id="2fe6a-249">Expense on P1 project is included on CL2.</span></span>
                    </li>
                </ul>
                <p>
<span data-ttu-id="2fe6a-250">No se superposa el que s'inclou a cada línia de contracte i, per tant, és vàlid.</span><span class="sxs-lookup"><span data-stu-id="2fe6a-250">No overlap in what is being included on each Contract line and therefore valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="2fe6a-251">C1</span><span class="sxs-lookup"><span data-stu-id="2fe6a-251">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="2fe6a-252">CL2</span><span class="sxs-lookup"><span data-stu-id="2fe6a-252">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2fe6a-253">P1</span><span class="sxs-lookup"><span data-stu-id="2fe6a-253">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="2fe6a-254">En blanc</span><span class="sxs-lookup"><span data-stu-id="2fe6a-254">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2fe6a-255">No</span><span class="sxs-lookup"><span data-stu-id="2fe6a-255">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2fe6a-256">Sí</span><span class="sxs-lookup"><span data-stu-id="2fe6a-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2fe6a-257">No</span><span class="sxs-lookup"><span data-stu-id="2fe6a-257">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2fe6a-258">No</span><span class="sxs-lookup"><span data-stu-id="2fe6a-258">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="2fe6a-259">C1</span><span class="sxs-lookup"><span data-stu-id="2fe6a-259">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="2fe6a-260">CL1</span><span class="sxs-lookup"><span data-stu-id="2fe6a-260">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2fe6a-261">P1</span><span class="sxs-lookup"><span data-stu-id="2fe6a-261">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="2fe6a-262">Només les tasques seleccionades</span><span class="sxs-lookup"><span data-stu-id="2fe6a-262">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2fe6a-263">Sí</span><span class="sxs-lookup"><span data-stu-id="2fe6a-263">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2fe6a-264">Sí</span><span class="sxs-lookup"><span data-stu-id="2fe6a-264">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2fe6a-265">Sí</span><span class="sxs-lookup"><span data-stu-id="2fe6a-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2fe6a-266">Sí</span><span class="sxs-lookup"><span data-stu-id="2fe6a-266">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2fe6a-267">No és vàlid</span><span class="sxs-lookup"><span data-stu-id="2fe6a-267">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2fe6a-268">Infracció de la regla núm. 2</span><span class="sxs-lookup"><span data-stu-id="2fe6a-268">Violation of Rule #2</span></span> </p>
                <p>
<span data-ttu-id="2fe6a-269">El C1 inclou temps, materials, despeses i tarifes en un subconjunt de tasques al projecte P1.</span><span class="sxs-lookup"><span data-stu-id="2fe6a-269">C1 includes Time, Materials, Expenses and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="2fe6a-270">CL2 inclou temps, materials, despeses i tarifes per a tot el projecte P1 i, per tant, se superposa amb el que s'inclou a C1.</span><span class="sxs-lookup"><span data-stu-id="2fe6a-270">CL2 includes Time, Materials, Expenses and Fees for the whole project P1 and therefore overlaps with what is included on C1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="2fe6a-271">C1</span><span class="sxs-lookup"><span data-stu-id="2fe6a-271">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="2fe6a-272">CL2</span><span class="sxs-lookup"><span data-stu-id="2fe6a-272">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2fe6a-273">P1</span><span class="sxs-lookup"><span data-stu-id="2fe6a-273">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="2fe6a-274">En blanc</span><span class="sxs-lookup"><span data-stu-id="2fe6a-274">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2fe6a-275">Sí</span><span class="sxs-lookup"><span data-stu-id="2fe6a-275">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2fe6a-276">Sí</span><span class="sxs-lookup"><span data-stu-id="2fe6a-276">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2fe6a-277">Sí</span><span class="sxs-lookup"><span data-stu-id="2fe6a-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2fe6a-278">Sí</span><span class="sxs-lookup"><span data-stu-id="2fe6a-278">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="2fe6a-279">C1</span><span class="sxs-lookup"><span data-stu-id="2fe6a-279">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="2fe6a-280">CL1</span><span class="sxs-lookup"><span data-stu-id="2fe6a-280">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2fe6a-281">P1</span><span class="sxs-lookup"><span data-stu-id="2fe6a-281">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="2fe6a-282">Només les tasques seleccionades</span><span class="sxs-lookup"><span data-stu-id="2fe6a-282">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2fe6a-283">Sí</span><span class="sxs-lookup"><span data-stu-id="2fe6a-283">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2fe6a-284">Sí</span><span class="sxs-lookup"><span data-stu-id="2fe6a-284">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2fe6a-285">Sí</span><span class="sxs-lookup"><span data-stu-id="2fe6a-285">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2fe6a-286">Sí</span><span class="sxs-lookup"><span data-stu-id="2fe6a-286">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2fe6a-287">Vàlida</span><span class="sxs-lookup"><span data-stu-id="2fe6a-287">Valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2fe6a-288">Segons la regla 3</span><span class="sxs-lookup"><span data-stu-id="2fe6a-288">Per Rule #3</span></span> </p>
                <p>
<span data-ttu-id="2fe6a-289">El C1 inclou temps, despeses, materials i tarifes en un subconjunt de tasques al projecte P1.</span><span class="sxs-lookup"><span data-stu-id="2fe6a-289">C1 includes Time, Expenses, Materials, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="2fe6a-290">El CL2 inclou temps, despeses, materials i tarifes per a un subconjunt de tasques al projecte P1.</span><span class="sxs-lookup"><span data-stu-id="2fe6a-290">CL2 includes Time, Expenses, Materials, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="2fe6a-291">L'única validació addicional és per al subconjunt de tasques de CL1, que és diferent del subconjunt de tasques de CL2 per assegurar que no hi ha superposicions.</span><span class="sxs-lookup"><span data-stu-id="2fe6a-291">The only additional validation is around the subset of tasks on CL1 is different from the subset of tasks on CL2 to ensure that there are no overlaps there.</span></span> <span data-ttu-id="2fe6a-292">Això ho fa el sistema quan s'associen les tasques.</span><span class="sxs-lookup"><span data-stu-id="2fe6a-292">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="2fe6a-293">C1</span><span class="sxs-lookup"><span data-stu-id="2fe6a-293">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="2fe6a-294">CL2</span><span class="sxs-lookup"><span data-stu-id="2fe6a-294">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2fe6a-295">P1</span><span class="sxs-lookup"><span data-stu-id="2fe6a-295">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="2fe6a-296">Només les tasques seleccionades</span><span class="sxs-lookup"><span data-stu-id="2fe6a-296">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2fe6a-297">Sí</span><span class="sxs-lookup"><span data-stu-id="2fe6a-297">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2fe6a-298">Sí</span><span class="sxs-lookup"><span data-stu-id="2fe6a-298">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2fe6a-299">Sí</span><span class="sxs-lookup"><span data-stu-id="2fe6a-299">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2fe6a-300">Sí</span><span class="sxs-lookup"><span data-stu-id="2fe6a-300">Yes</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
