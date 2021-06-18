---
title: Contractes del projecte
description: En aquest tema es proporcionen exemples dels contractes del projecte que podeu crear per a diversos tipus de projectes i fonts de finançament, i com podeu administrar els contractes i facturar els clients del projecte.
author: Yowelle
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a794ec38ac07c1418f9e95b741941a83492bb3d5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999749"
---
# <a name="project-contracts"></a><span data-ttu-id="8fea3-103">Contractes del projecte</span><span class="sxs-lookup"><span data-stu-id="8fea3-103">Project contracts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8fea3-104">En aquest article es proporcionen exemples dels contractes del projecte que podeu crear per a diversos tipus de projectes i fonts de finançament, i com podeu administrar els contractes i facturar els clients del projecte.</span><span class="sxs-lookup"><span data-stu-id="8fea3-104">This article provides examples of the project contracts that you can create for various types of projects and funding sources, and how you can manage contracts and invoice project customers.</span></span>

<span data-ttu-id="8fea3-105">El tipus de projecte que es crea per a un contracte de projecte determina el mètode que s'utilitza per facturar els clients del projecte.</span><span class="sxs-lookup"><span data-stu-id="8fea3-105">The type of project that you create for a project contract determines the method that is used to invoice project customers.</span></span> <span data-ttu-id="8fea3-106">Podeu canviar un contracte de projecte i el projecte relacionat, però no podeu canviar el tipus de projecte.</span><span class="sxs-lookup"><span data-stu-id="8fea3-106">You can change a project contract and the related project, but you can't change the project type.</span></span> 

<span data-ttu-id="8fea3-107">En utilitzar un contracte de projecte, podeu facturar un o més projectes al mateix temps.</span><span class="sxs-lookup"><span data-stu-id="8fea3-107">By using a project contract, you can invoice one or more projects at the same time.</span></span> <span data-ttu-id="8fea3-108">El contracte de projecte també us ajuda a garantir un procediment de facturació coherent per a cada subprojecte en una estructura de projecte.</span><span class="sxs-lookup"><span data-stu-id="8fea3-108">The project contract also helps guarantee a consistent invoicing procedure for every subproject in a project structure.</span></span> 

<span data-ttu-id="8fea3-109">Cada projecte que s'ha de facturar ha d'estar associat amb un contracte de projecte.</span><span class="sxs-lookup"><span data-stu-id="8fea3-109">Every project that will be invoiced must be associated with a project contract.</span></span> <span data-ttu-id="8fea3-110">La configuració d'un contracte de projecte s'aplica a tots els projectes i subprojectes associats amb el contracte del projecte.</span><span class="sxs-lookup"><span data-stu-id="8fea3-110">The settings for a project contract apply to all projects and subprojects that are associated with that project contract.</span></span> 

<span data-ttu-id="8fea3-111">Un contracte de projecte pot especificar una o diverses fonts de finançament.</span><span class="sxs-lookup"><span data-stu-id="8fea3-111">A project contract can specify one or more sources of funding.</span></span> <span data-ttu-id="8fea3-112">Per tant, podeu dividir la facturació entre diversos finançadors, configurar límits de finançament per tal que les fonts de finançament no es facturin en més d'una quantitat especificada i configurar regles de finançament per a la càrrega de despeses.</span><span class="sxs-lookup"><span data-stu-id="8fea3-112">Therefore, you can split the billing among multiple funders, set up funding limits so that funding sources are not billed more than a specified amount, and configure funding rules for charging expenditures.</span></span>

## <a name="funding-for-project-contracts"></a><span data-ttu-id="8fea3-113">Finançament per a contractes de projectes</span><span class="sxs-lookup"><span data-stu-id="8fea3-113">Funding for project contracts</span></span>
<span data-ttu-id="8fea3-114">Alguns contractes de projecte especifiquen que diverses parts comparteixen la responsabilitat de finançar els costos del projecte.</span><span class="sxs-lookup"><span data-stu-id="8fea3-114">Some project contracts specify that multiple parties share the responsibility for funding the project costs.</span></span> <span data-ttu-id="8fea3-115">A continuació trobareu alguns exemples:</span><span class="sxs-lookup"><span data-stu-id="8fea3-115">Here are some examples:</span></span>

-   <span data-ttu-id="8fea3-116">Un client gran que té diverses divisions sol·licita que el finançament d'un projecte es divideixi.</span><span class="sxs-lookup"><span data-stu-id="8fea3-116">A large customer that has multiple divisions requests that funding of a project be split by division.</span></span>
-   <span data-ttu-id="8fea3-117">La vostra empresa comparteix els costos d'un projecte gran amb una organització externa.</span><span class="sxs-lookup"><span data-stu-id="8fea3-117">Your company shares the costs of a large project with an external organization.</span></span>
-   <span data-ttu-id="8fea3-118">Un projecte de carretera està cofinançat per dos municipis.</span><span class="sxs-lookup"><span data-stu-id="8fea3-118">A  road project is co-funded by two municipalities.</span></span>
-   <span data-ttu-id="8fea3-119">Un projecte de pont està finançat per una subvenció governamental i una corporació privada.</span><span class="sxs-lookup"><span data-stu-id="8fea3-119">A bridge project is funded by a government grant and a private corporation.</span></span>

<span data-ttu-id="8fea3-120">Al Dynamics 365 Finance, podeu dividir la facturació d'una única transacció o d'un projecte sencer entre diversos clients, subvencions o organitzacions.</span><span class="sxs-lookup"><span data-stu-id="8fea3-120">In Dynamics 365 Finance, you can split the billing for a single transaction or an entire project among multiple customers, grants, or organizations.</span></span> 

<span data-ttu-id="8fea3-121">En projectes que tinguin diversos finançadors, totes les parts que contribueixin al finançament d'un projecte de finançament avançat s'anomenen fonts de finançament.</span><span class="sxs-lookup"><span data-stu-id="8fea3-121">In projects that have multiple funders, all parties that contribute to the funding of an advanced funding project are called funding sources.</span></span> <span data-ttu-id="8fea3-122">Després que un client, una organització o una subvenció es defineixi com a font de finançament, es pot assignar a una o diverses regles de finançament.</span><span class="sxs-lookup"><span data-stu-id="8fea3-122">After a customer, organization, or grant is defined as a funding source, it can be assigned to one or more funding rules.</span></span> <span data-ttu-id="8fea3-123">Les regles de finançament contenen els criteris que determinen la manera com es destinen els càrrecs a les diverses fonts de finançament d'un projecte.</span><span class="sxs-lookup"><span data-stu-id="8fea3-123">Funding rules contain the criteria that determines how charges are allocated to the various funding sources for a project.</span></span> 

<span data-ttu-id="8fea3-124">Com que els articles en estoc, com els que apareixen a les requisicions de compra i les comandes de compra, no es poden dividir, l'import del cost no es pot dividir entre diverses fonts de finançament a l'hora de la distribució.</span><span class="sxs-lookup"><span data-stu-id="8fea3-124">Because stocked items, such as those that appear on purchase requisitions and purchase orders, can't be split, the cost amount can't be split among multiple funding sources at the time of distribution.</span></span> <span data-ttu-id="8fea3-125">Per tant, el valor de la font de finançament segueix sent 0 (zero) fins que es comptabilitzi l'inventari.</span><span class="sxs-lookup"><span data-stu-id="8fea3-125">Therefore, the funding source value remains 0 (zero) until the inventory issue is posted.</span></span> <span data-ttu-id="8fea3-126">Quan es comptabilitzi l'inventari, l'import de la despesa es distribueix segons les regles de distribució del compte per al projecte.</span><span class="sxs-lookup"><span data-stu-id="8fea3-126">When the inventory issue is posted, the cost amount is distributed according to the account distribution rules for the project.</span></span>

<span data-ttu-id="8fea3-127">A continuació, us indiquem alguns passos que podeu dur a terme per fer més fàcil la divisió de la facturació entre diverses fonts de finançament:</span><span class="sxs-lookup"><span data-stu-id="8fea3-127">Here are some steps that you can take to make it easier to split the billing among multiple funding sources:</span></span>

-   <span data-ttu-id="8fea3-128">Especifiqueu que totes les transaccions que s'introdueixen per a un projecte utilitzin la mateixa moneda de vendes en el contracte del projecte.</span><span class="sxs-lookup"><span data-stu-id="8fea3-128">Specify that all transactions that are entered for a project use the same sales currency as the project contract.</span></span>
-   <span data-ttu-id="8fea3-129">Configureu els límits de finançament, de manera que no es facturi cap font de finançament més d'un import especificat en un projecte.</span><span class="sxs-lookup"><span data-stu-id="8fea3-129">Set up funding limits, so that a funding source isn't invoiced more than a specified amount toward a project.</span></span>
-   <span data-ttu-id="8fea3-130">Configureu les regles de finançament i els límits de finançament de cada treballador, article, categoria, grup de categories i tipus de transacció (o per a tots els tipus de transaccions).</span><span class="sxs-lookup"><span data-stu-id="8fea3-130">Configure funding rules and funding limits for each worker, item, category, category group, and transaction type (or for all transaction types).</span></span>
-   <span data-ttu-id="8fea3-131">Seleccioneu dates d'inici i d'acabament opcionals per definir el període en què cada regla de finançament és vàlida.</span><span class="sxs-lookup"><span data-stu-id="8fea3-131">Select optional start and end dates to define the period when each funding rule is valid.</span></span>
-   <span data-ttu-id="8fea3-132">Especifiqueu el percentatge del qual és responsable cada font de finançament.</span><span class="sxs-lookup"><span data-stu-id="8fea3-132">Specify the percentage that each funding source is responsible for.</span></span>
-   <span data-ttu-id="8fea3-133">Especifiqueu quina font de finançament s'encarrega de les diferències d'arrodoniment causades pels càlculs d'assignació de finançament.</span><span class="sxs-lookup"><span data-stu-id="8fea3-133">Specify which funding source is responsible for rounding differences that are caused by funding allocation calculations.</span></span>
-   <span data-ttu-id="8fea3-134">Configureu regles que determinin com els costos de projecte es facturen a clients externs i es carreguen a organitzacions internes.</span><span class="sxs-lookup"><span data-stu-id="8fea3-134">Set up rules that determine how project costs are invoiced to external customers and charged to internal organizations.</span></span>
-   <span data-ttu-id="8fea3-135">Registreu les transaccions en un compte de finançament de retenció fins que es pugui obtenir finançament addicional o fins que decidiu suportar les despeses internament.</span><span class="sxs-lookup"><span data-stu-id="8fea3-135">Record transactions in an on-hold funding account until additional funding can be obtained, or until you decide to bear the costs internally.</span></span>

<span data-ttu-id="8fea3-136">Per determinar quin grup d'impostos s'ha d'associar amb una transacció, se cerca una assignació de grup d'impostos al projecte.</span><span class="sxs-lookup"><span data-stu-id="8fea3-136">To determine which tax group to associate with a transaction, the project is searched for a tax group assignment.</span></span> <span data-ttu-id="8fea3-137">Si no s'ha fet cap assignació de grup d'impostos en el mateix nivell de projecte, se cerca en el contracte del projecte.</span><span class="sxs-lookup"><span data-stu-id="8fea3-137">If no tax group assignment has been made at the project level, the project contract is searched.</span></span>

### <a name="example-multiple-funding-sources-simple"></a><span data-ttu-id="8fea3-138">Exemple: diverses fonts de finançament (simple)</span><span class="sxs-lookup"><span data-stu-id="8fea3-138">Example: Multiple funding sources (simple)</span></span>

<span data-ttu-id="8fea3-139">A la taula següent es proporcionen escenaris per administrar l'assignació de finançament entre diverses fonts de finançament.</span><span class="sxs-lookup"><span data-stu-id="8fea3-139">The following table provides scenarios for managing funding allocation among multiple funding sources.</span></span> <span data-ttu-id="8fea3-140">Aquests escenaris es basen en els següents supòsits:</span><span class="sxs-lookup"><span data-stu-id="8fea3-140">These scenarios are based on the following assumptions:</span></span>

-   <span data-ttu-id="8fea3-141">La configuració de prioritat s'ha traduït a l'assignació de fons abans que s'apliquin altres criteris de regla de finançament.</span><span class="sxs-lookup"><span data-stu-id="8fea3-141">Priority settings are factored into the allocation of funds before other funding rule criteria are applied.</span></span>
-   <span data-ttu-id="8fea3-142">No s'ha especificat cap interval de dates per definir el període quan la regla de finançament és vàlida.</span><span class="sxs-lookup"><span data-stu-id="8fea3-142">No date range has been specified to define the period d when the funding rule is valid.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8fea3-143"><strong>Escenari</strong></span><span class="sxs-lookup"><span data-stu-id="8fea3-143"><strong>Scenario</strong></span></span></td>
<td><span data-ttu-id="8fea3-144"><strong>Font de finançament</strong></span><span class="sxs-lookup"><span data-stu-id="8fea3-144"><strong>Funding source</strong></span></span></td>
<td><span data-ttu-id="8fea3-145"><strong>Percentatge d'assignació</strong></span><span class="sxs-lookup"><span data-stu-id="8fea3-145"><strong>Allocation percentage</strong></span></span></td>
<td><span data-ttu-id="8fea3-146"><strong>Prioritat d'assignació</strong></span><span class="sxs-lookup"><span data-stu-id="8fea3-146"><strong>Allocation priority</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8fea3-147">Voleu assignar costos a una font de finançament fins que s'esgotin els seus recursos, assignar costos a una segona font de finançament fins que s'esgotin els seus diners i, finalment, assignar els costos restants a una tercera font de finançament.</span><span class="sxs-lookup"><span data-stu-id="8fea3-147">You want to allocate costs to one funding source until its funds are exhausted, allocate costs to a second funding source until its funds are exhausted, and finally allocate the remaining costs to a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="8fea3-148">Font de finançament 1</span><span class="sxs-lookup"><span data-stu-id="8fea3-148">Funding　source　1</span></span></li>
<li><span data-ttu-id="8fea3-149">Font de finançament 2</span><span class="sxs-lookup"><span data-stu-id="8fea3-149">Funding　source　2</span></span></li>
<li><span data-ttu-id="8fea3-150">Font de finançament 3</span><span class="sxs-lookup"><span data-stu-id="8fea3-150">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="8fea3-151">100 %</span><span class="sxs-lookup"><span data-stu-id="8fea3-151">100%</span></span></li>
<li><span data-ttu-id="8fea3-152">100 %</span><span class="sxs-lookup"><span data-stu-id="8fea3-152">100%</span></span></li>
<li><span data-ttu-id="8fea3-153">100 %</span><span class="sxs-lookup"><span data-stu-id="8fea3-153">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="8fea3-154">1</span><span class="sxs-lookup"><span data-stu-id="8fea3-154">1</span></span></li>
<li><span data-ttu-id="8fea3-155">2</span><span class="sxs-lookup"><span data-stu-id="8fea3-155">2</span></span></li>
<li><span data-ttu-id="8fea3-156">3</span><span class="sxs-lookup"><span data-stu-id="8fea3-156">3</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8fea3-157">Voleu assignar el 75 per cent dels costos a una font de finançament i el 25 per cent a una segona font de finançament.</span><span class="sxs-lookup"><span data-stu-id="8fea3-157">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="8fea3-158">Quan alguna d'aquestes fonts de finançament s'esgoti, voleu pagar els costos restants amb una tercera font de finançament.</span><span class="sxs-lookup"><span data-stu-id="8fea3-158">When either of those funding sources is exhausted, you want to pay the remaining costs from a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="8fea3-159">Font de finançament 1</span><span class="sxs-lookup"><span data-stu-id="8fea3-159">Funding　source　1</span></span></li>
<li><span data-ttu-id="8fea3-160">Font de finançament 2</span><span class="sxs-lookup"><span data-stu-id="8fea3-160">Funding　source　2</span></span></li>
<li><span data-ttu-id="8fea3-161">Font de finançament 3</span><span class="sxs-lookup"><span data-stu-id="8fea3-161">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="8fea3-162">75 %</span><span class="sxs-lookup"><span data-stu-id="8fea3-162">75%</span></span></li>
<li><span data-ttu-id="8fea3-163">25 %</span><span class="sxs-lookup"><span data-stu-id="8fea3-163">25%</span></span></li>
<li><span data-ttu-id="8fea3-164">100 %</span><span class="sxs-lookup"><span data-stu-id="8fea3-164">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="8fea3-165">1</span><span class="sxs-lookup"><span data-stu-id="8fea3-165">1</span></span></li>
<li><span data-ttu-id="8fea3-166">1</span><span class="sxs-lookup"><span data-stu-id="8fea3-166">1</span></span></li>
<li><span data-ttu-id="8fea3-167">2</span><span class="sxs-lookup"><span data-stu-id="8fea3-167">2</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8fea3-168">Voleu assignar el 75 per cent dels costos a una font de finançament i el 25 per cent a una segona font de finançament.</span><span class="sxs-lookup"><span data-stu-id="8fea3-168">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="8fea3-169">Quan alguna d'aquestes fonts de finançament s'esgoti, voleu dividir els costos restants entre una tercera font de finançament i una quarta.</span><span class="sxs-lookup"><span data-stu-id="8fea3-169">When either of those funding sources is exhausted, you want to split the remaining costs between a third funding source and a fourth funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="8fea3-170">Font de finançament 1</span><span class="sxs-lookup"><span data-stu-id="8fea3-170">Funding　source　1</span></span></li>
<li><span data-ttu-id="8fea3-171">Font de finançament 2</span><span class="sxs-lookup"><span data-stu-id="8fea3-171">Funding　source　2</span></span></li>
<li><span data-ttu-id="8fea3-172">Font de finançament 3</span><span class="sxs-lookup"><span data-stu-id="8fea3-172">Funding　source　3</span></span></li>
<li><span data-ttu-id="8fea3-173">Font de finançament 4</span><span class="sxs-lookup"><span data-stu-id="8fea3-173">Funding　source　4</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="8fea3-174">75 %</span><span class="sxs-lookup"><span data-stu-id="8fea3-174">75%</span></span></li>
<li><span data-ttu-id="8fea3-175">25 %</span><span class="sxs-lookup"><span data-stu-id="8fea3-175">25%</span></span></li>
<li><span data-ttu-id="8fea3-176">50 %</span><span class="sxs-lookup"><span data-stu-id="8fea3-176">50%</span></span></li>
<li><span data-ttu-id="8fea3-177">50 %</span><span class="sxs-lookup"><span data-stu-id="8fea3-177">50%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="8fea3-178">1</span><span class="sxs-lookup"><span data-stu-id="8fea3-178">1</span></span></li>
<li><span data-ttu-id="8fea3-179">1</span><span class="sxs-lookup"><span data-stu-id="8fea3-179">1</span></span></li>
<li><span data-ttu-id="8fea3-180">2</span><span class="sxs-lookup"><span data-stu-id="8fea3-180">2</span></span></li>
<li><span data-ttu-id="8fea3-181">2</span><span class="sxs-lookup"><span data-stu-id="8fea3-181">2</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8fea3-182">Voleu assignar el primer 25 per cent dels costos a una font de finançament i la resta a una segona font de finançament.</span><span class="sxs-lookup"><span data-stu-id="8fea3-182">You want to allocate the first 25 percent of costs to one funding source and the rest to a second funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="8fea3-183">Font de finançament 1</span><span class="sxs-lookup"><span data-stu-id="8fea3-183">Funding　source　1</span></span></li>
<li><span data-ttu-id="8fea3-184">Font de finançament 2</span><span class="sxs-lookup"><span data-stu-id="8fea3-184">Funding　source　2</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="8fea3-185">25 %</span><span class="sxs-lookup"><span data-stu-id="8fea3-185">25%</span></span></li>
<li><span data-ttu-id="8fea3-186">100 %</span><span class="sxs-lookup"><span data-stu-id="8fea3-186">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="8fea3-187">1</span><span class="sxs-lookup"><span data-stu-id="8fea3-187">1</span></span></li>
<li><span data-ttu-id="8fea3-188">2</span><span class="sxs-lookup"><span data-stu-id="8fea3-188">2</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a><span data-ttu-id="8fea3-189">Exemple: diverses fonts de finançament (complex)</span><span class="sxs-lookup"><span data-stu-id="8fea3-189">Example: Multiple funding sources (complex)</span></span>

<span data-ttu-id="8fea3-190">Teniu tres fonts de finançament que voleu utilitzar en l'ordre següent:</span><span class="sxs-lookup"><span data-stu-id="8fea3-190">You have three funding sources that you want to use in the following order:</span></span>

1.  <span data-ttu-id="8fea3-191">Utilitzar la font de finançament 2 i la font de finançament 3 per igual fins que la font de finançament 2 estigui esgotada.</span><span class="sxs-lookup"><span data-stu-id="8fea3-191">Use funding source 2 and funding source 3 equally until funding source 2 is exhausted.</span></span>
2.  <span data-ttu-id="8fea3-192">Continuar utilitzant la font de finançament 3 fins que s'esgoti.</span><span class="sxs-lookup"><span data-stu-id="8fea3-192">Continue to use funding source 3 until it is exhausted.</span></span>
3.  <span data-ttu-id="8fea3-193">Utilitzar la font de finançament 1 després que s'esgoti la font de finançament 3.</span><span class="sxs-lookup"><span data-stu-id="8fea3-193">Use funding source 1 after funding source 3 is exhausted.</span></span>

<span data-ttu-id="8fea3-194">Per aconseguir aquest objectiu, heu de fer el següent:</span><span class="sxs-lookup"><span data-stu-id="8fea3-194">To accomplish this goal, you must do the following:</span></span>

-   <span data-ttu-id="8fea3-195">Configureu els límits de finançament per a la font de finançament 2 i la font de finançament 3, per a les seves quantitats respectives.</span><span class="sxs-lookup"><span data-stu-id="8fea3-195">Set up funding limits for funding source 2 and funding source 3, for their respective amounts.</span></span>
-   <span data-ttu-id="8fea3-196">Creeu les regles de finançament següents:</span><span class="sxs-lookup"><span data-stu-id="8fea3-196">Create the following funding rules:</span></span>
    -   <span data-ttu-id="8fea3-197">Regla 1 (prioritat 1): assigneu un 50 per cent de les transaccions a la font de finançament 2 i un 50 per cent a la font de finançament 3.</span><span class="sxs-lookup"><span data-stu-id="8fea3-197">Rule 1 (Priority 1): Allocate 50 percent of transactions to funding source 2 and 50 percent to funding source 3.</span></span>
    -   <span data-ttu-id="8fea3-198">Regla 2 (prioritat 2): assigneu un 100 per cent de les transaccions a la font de finançament 3.</span><span class="sxs-lookup"><span data-stu-id="8fea3-198">Rule 2 (Priority 2): Allocate 100 percent of transactions to funding source 3.</span></span>
    -   <span data-ttu-id="8fea3-199">Regla 3 (prioritat 3): assigneu un 100 per cent de les transaccions a la font de finançament 1.</span><span class="sxs-lookup"><span data-stu-id="8fea3-199">Rule 3 (Priority 3): Allocate 100 percent of transactions to funding source 1.</span></span>

<span data-ttu-id="8fea3-200">Aquesta configuració funciona perquè les transaccions es comproven amb les regles i els límits per determinar si s'apliquen a la transacció.</span><span class="sxs-lookup"><span data-stu-id="8fea3-200">This setup works because transactions are checked against rules and limits to determine whether any of them apply to the transaction.</span></span> <span data-ttu-id="8fea3-201">Si no s'aplica cap norma o límit específic a la transacció, la regla Totes les transaccions s'aplicarà.</span><span class="sxs-lookup"><span data-stu-id="8fea3-201">If no specific rules or limits apply to the transaction, the All transactions rule applies.</span></span> <span data-ttu-id="8fea3-202">La regla Totes les transaccions coincideix amb totes les transaccions.</span><span class="sxs-lookup"><span data-stu-id="8fea3-202">The All transactions rule matches all transactions.</span></span> 

<span data-ttu-id="8fea3-203">Si es troba una regla que coincideix amb una transacció, primer s'aplica el percentatge que s'ha assignat en aquesta regla, però només quan es comproven les coincidències amb qualsevol límit que s'hagi configurat.</span><span class="sxs-lookup"><span data-stu-id="8fea3-203">If a rule is found that matches a transaction, the percentage that has been allocated in that rule is applied first, but only after the matches are checked against any limits that have been set up.</span></span> <span data-ttu-id="8fea3-204">Si s'ha complert un límit i s'han esgotat els fons de la font de finançament, la regla de finançament associada amb el límit de finançament s'ignora i el programa comprova la següent regla que s'aplica.</span><span class="sxs-lookup"><span data-stu-id="8fea3-204">If a limit has been met, and a funding source’s funds are exhausted, the funding rule that is associated with the funding limit is disregarded, and the program checks for the next rule that applies.</span></span> 

<span data-ttu-id="8fea3-205">En alguns casos, només es pot assignar una part d'una transacció en virtut d'una regla.</span><span class="sxs-lookup"><span data-stu-id="8fea3-205">In some cases, only part of a transaction can be allocated under a rule.</span></span> <span data-ttu-id="8fea3-206">Això podria passar perquè el límit s'ha assolit quan s'ha assignat la transacció.</span><span class="sxs-lookup"><span data-stu-id="8fea3-206">This might happen because a limit is reached when the transaction is allocated.</span></span> <span data-ttu-id="8fea3-207">En aquest cas, només s'assigna un import determinat segons aquesta regla, com ara el 50 per cent a cada font de finançament.</span><span class="sxs-lookup"><span data-stu-id="8fea3-207">In this case, only a certain amount is allocated according to that rule, such as 50 percent to each funding source.</span></span> <span data-ttu-id="8fea3-208">Aquest és el cas de la regla 1, que es descriu abans en aquesta secció.</span><span class="sxs-lookup"><span data-stu-id="8fea3-208">This is the case in rule 1, which is described earlier in this section.</span></span> <span data-ttu-id="8fea3-209">La resta s'assigna d'acord amb la regla següent a la seqüència.</span><span class="sxs-lookup"><span data-stu-id="8fea3-209">The remainder is allocated according to the next rule in the sequence.</span></span> 

<span data-ttu-id="8fea3-210">A la taula següent s'examina més detalladament aquest escenari.</span><span class="sxs-lookup"><span data-stu-id="8fea3-210">The following table examines this scenario in more detail.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8fea3-211"><strong>Focus</strong></span><span class="sxs-lookup"><span data-stu-id="8fea3-211"><strong>Focus</strong></span></span></td>
<td><span data-ttu-id="8fea3-212"><strong>Detalls</strong></span><span class="sxs-lookup"><span data-stu-id="8fea3-212"><strong>Details</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8fea3-213">Regles de finançament</span><span class="sxs-lookup"><span data-stu-id="8fea3-213">Funding rules</span></span></td>
<td><ul>
<li><span data-ttu-id="8fea3-214">Regla 1 (prioritat 1): totes les transaccions.</span><span class="sxs-lookup"><span data-stu-id="8fea3-214">Rule 1 (Priority 1): All transactions.</span></span> <span data-ttu-id="8fea3-215">Assigna la font de finançament 2 al 50 % i la font de finançament 3 al 50 %.</span><span class="sxs-lookup"><span data-stu-id="8fea3-215">Allocate funding source 2 at 50% and funding source 3 at 50%.</span></span></li>
<li><span data-ttu-id="8fea3-216">Regla 2 (prioritat 2): totes les transaccions.</span><span class="sxs-lookup"><span data-stu-id="8fea3-216">Rule 2 (Priority 2): All transactions.</span></span> <span data-ttu-id="8fea3-217">Assigna la font de finançament 3 al 100 %.</span><span class="sxs-lookup"><span data-stu-id="8fea3-217">Allocate funding source 3 at 100%.</span></span></li>
<li><span data-ttu-id="8fea3-218">Regla 3 (prioritat 2): totes les transaccions.</span><span class="sxs-lookup"><span data-stu-id="8fea3-218">Rule 3 (Priority 2): All transactions.</span></span> <span data-ttu-id="8fea3-219">Assigna la font de finançament 1 al 100 %.</span><span class="sxs-lookup"><span data-stu-id="8fea3-219">Allocate funding source 1 at 100%.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8fea3-220">Límits de finançament</span><span class="sxs-lookup"><span data-stu-id="8fea3-220">Funding limits</span></span></td>
<td><ul>
<li><span data-ttu-id="8fea3-221">Límit de la font de finançament 1 = 10.000,00</span><span class="sxs-lookup"><span data-stu-id="8fea3-221">Funding source 1 limit = 10,000.00</span></span></li>
<li><span data-ttu-id="8fea3-222">Límit de la font de finançament 2 = 500,00</span><span class="sxs-lookup"><span data-stu-id="8fea3-222">Funding source 2 limit = 500.00</span></span></li>
<li><span data-ttu-id="8fea3-223">Límit de la font de finançament 3 = 750,00</span><span class="sxs-lookup"><span data-stu-id="8fea3-223">Funding source 3 limit = 750.00</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8fea3-224">Transacció 1</span><span class="sxs-lookup"><span data-stu-id="8fea3-224">Transaction 1</span></span></td>
<td><span data-ttu-id="8fea3-225"><strong>Import de la transacció:</strong> 100,00<strong>Finançament:</strong> la transacció es paga només segons la regla 1, perquè l'operació s'abona íntegrament després que s'apliqui la regla 1.</span><span class="sxs-lookup"><span data-stu-id="8fea3-225"><strong>Transaction amount:</strong> 100.00<strong>Funding:</strong> The transaction is paid according to rule 1 only, because the transaction is fully paid after rule 1 is applied.</span></span> <span data-ttu-id="8fea3-226">La transacció es finança equitativament entre la font de finançament 2 i la font de finançament 3.</span><span class="sxs-lookup"><span data-stu-id="8fea3-226">The transaction is funded equally between funding source 2 and funding source 3.</span></span>
<ul>
<li><span data-ttu-id="8fea3-227">Font de finançament 2: 50,00</span><span class="sxs-lookup"><span data-stu-id="8fea3-227">Funding source 2: 50.00</span></span></li>
<li><span data-ttu-id="8fea3-228">Font de finançament 3: 50,00</span><span class="sxs-lookup"><span data-stu-id="8fea3-228">Funding source 3: 50.00</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8fea3-229">Transacció 2</span><span class="sxs-lookup"><span data-stu-id="8fea3-229">Transaction 2</span></span></td>
<td><span data-ttu-id="8fea3-230"><strong>Import de la transacció:</strong> 5.000,00<strong>Finançament:</strong> la transacció es paga segons les tres regles.</span><span class="sxs-lookup"><span data-stu-id="8fea3-230"><strong>Transaction amount:</strong> 5,000.00<strong>Funding:</strong> The transaction is paid according to all three rules.</span></span> <span data-ttu-id="8fea3-231"><strong>Regla 1</strong>
</span><span class="sxs-lookup"><span data-stu-id="8fea3-231"><strong>Rule 1</strong>
</span></span><ul>
<li><span data-ttu-id="8fea3-232">Font de finançament 2: 450,00</span><span class="sxs-lookup"><span data-stu-id="8fea3-232">Funding source 2: 450.00</span></span></li>
<li><span data-ttu-id="8fea3-233">Font de finançament 3: 450,00</span><span class="sxs-lookup"><span data-stu-id="8fea3-233">Funding source 3: 450.00</span></span></li>
</ul><span data-ttu-id="8fea3-234">
<strong>Regla 2</strong>
</span><span class="sxs-lookup"><span data-stu-id="8fea3-234">
<strong>Rule 2</strong>
</span></span><ul>
<li><span data-ttu-id="8fea3-235">Font de finançament 3: 250,00 (= 750,00 - 50,00 - 450,00)</span><span class="sxs-lookup"><span data-stu-id="8fea3-235">Funding source 3: 250.00 (= 750.00 – 50.00 – 450.00)</span></span></li>
</ul><span data-ttu-id="8fea3-236">
<strong>Regla 3</strong>
</span><span class="sxs-lookup"><span data-stu-id="8fea3-236">
<strong>Rule 3</strong>
</span></span><ul>
<li><span data-ttu-id="8fea3-237">Font de finançament 1: 3.850,00 (= 5.000,00 - 450,00 - 450,00 - 250,00)</span><span class="sxs-lookup"><span data-stu-id="8fea3-237">Funding source 1: 3,850.00 (= 5,000.00 – 450.00 – 450.00 – 250.00)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8fea3-238">Total de fons que es distribueixen per a cada font de finançament</span><span class="sxs-lookup"><span data-stu-id="8fea3-238">Total funds that are distributed for each funding source</span></span></td>
<td><ul>
<li><span data-ttu-id="8fea3-239">Font de finançament 1: 3.850,00</span><span class="sxs-lookup"><span data-stu-id="8fea3-239">Funding source 1: 3,850.00</span></span></li>
<li><span data-ttu-id="8fea3-240">Font de finançament 2: 500,00</span><span class="sxs-lookup"><span data-stu-id="8fea3-240">Funding source 2: 500.00</span></span></li>
<li><span data-ttu-id="8fea3-241">Font de finançament 3: 750,00</span><span class="sxs-lookup"><span data-stu-id="8fea3-241">Funding source 3: 750.00</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a><span data-ttu-id="8fea3-242">Regles de facturació</span><span class="sxs-lookup"><span data-stu-id="8fea3-242">Billing rules</span></span>
<span data-ttu-id="8fea3-243">Quan negocieu un contracte de projecte amb un client, heu de definir com i quan podeu facturar el client per treballar en un projecte.</span><span class="sxs-lookup"><span data-stu-id="8fea3-243">When you negotiate a project contract with a customer, you define how and when you can invoice the customer for work on a project.</span></span> <span data-ttu-id="8fea3-244">Després de configurar el contracte del projecte i el projecte, podeu configurar les regles de facturació del projecte.</span><span class="sxs-lookup"><span data-stu-id="8fea3-244">After you set up the project contract and the project, you can set up billing rules for the project.</span></span> <span data-ttu-id="8fea3-245">Les regles de facturació es basen en les condicions del projecte que s'especifiquen al contracte del projecte.</span><span class="sxs-lookup"><span data-stu-id="8fea3-245">Billing rules are based on the project terms that are specified in the project contract.</span></span> <span data-ttu-id="8fea3-246">Les regles de facturació que creeu depenen de les condicions del contracte del projecte i del tipus de projecte, com ara temps i material o de preu fix, que associeu amb la regla de facturació.</span><span class="sxs-lookup"><span data-stu-id="8fea3-246">The billing rules that you can create depend on the terms of the project contract and the project type, such as Time and material or Fixed-price, that you associate with the billing rule.</span></span> <span data-ttu-id="8fea3-247">Podeu crear més d'una regla de facturació per a un contracte de projecte.</span><span class="sxs-lookup"><span data-stu-id="8fea3-247">You can create more than one billing rule for a project contract.</span></span> <span data-ttu-id="8fea3-248">També podeu assignar una regla de facturació a diversos projectes associats amb el mateix contracte de projecte i tenir termes de facturació similars.</span><span class="sxs-lookup"><span data-stu-id="8fea3-248">You can also assign a billing rule to multiple projects that are associated with the same project contract and have similar billing terms.</span></span> 

<span data-ttu-id="8fea3-249">Podeu configurar els tipus següents de regles de facturació:</span><span class="sxs-lookup"><span data-stu-id="8fea3-249">You can set up the following types of billing rules:</span></span>

-   <span data-ttu-id="8fea3-250">**Unitat de lliurament**: factureu un client quan completeu una unitat de lliurament.</span><span class="sxs-lookup"><span data-stu-id="8fea3-250">**Unit of delivery** – Invoice a customer when you complete a unit of delivery.</span></span> <span data-ttu-id="8fea3-251">Definiu les unitats de lliurament al contracte.</span><span class="sxs-lookup"><span data-stu-id="8fea3-251">You define the units of delivery in the contract.</span></span>
-   <span data-ttu-id="8fea3-252">**Progrés**: factureu un client quan completeu un percentatge especificat del projecte.</span><span class="sxs-lookup"><span data-stu-id="8fea3-252">**Progress** – Invoice a customer when you complete a specified percentage of the project.</span></span> <span data-ttu-id="8fea3-253">Podeu configurar una regla de facturació per calcular automàticament el percentatge de treball completat, o podeu calcular manualment el percentatge de treball completat i l'import per facturar al client.</span><span class="sxs-lookup"><span data-stu-id="8fea3-253">You can set up a billing rule to automatically calculate the percentage of work completed, or you can manually calculate the percentage of work completed and the amount to invoice the customer.</span></span>
-   <span data-ttu-id="8fea3-254">**Fita**: factureu un client l'import total d'un fita de projecte quan s'assoleixi la fita.</span><span class="sxs-lookup"><span data-stu-id="8fea3-254">**Milestone** – Invoice a customer for the full amount of a project milestone when the milestone is reached.</span></span>
-   <span data-ttu-id="8fea3-255">**Taxa**: factureu un client pels vostres serveis, a més d'una taxa d'administració, que sol ser un percentatge del cost dels serveis.</span><span class="sxs-lookup"><span data-stu-id="8fea3-255">**Fee** – Invoice a customer for your services plus a management fee, which is typically a percentage of the cost of services.</span></span>
-   <span data-ttu-id="8fea3-256">**Temps i material**: factureu un client pel valor del temps i els materials que s'utilitzen en un projecte.</span><span class="sxs-lookup"><span data-stu-id="8fea3-256">**Time and material** – Invoice a customer for the value of time and materials that are used on a project.</span></span>

<span data-ttu-id="8fea3-257">Per a tots els tipus de regles de facturació, podeu especificar un percentatge de retenció que es dedueix de les factures del client fins que un projecte arribi a una fase consensuada.</span><span class="sxs-lookup"><span data-stu-id="8fea3-257">For all types of billing rules, you can specify a retention percentage that is deducted from customer invoices until a project reaches an agreed-upon stage.</span></span> <span data-ttu-id="8fea3-258">El percentatge de retenció de pagament s'especifica al contracte del projecte.</span><span class="sxs-lookup"><span data-stu-id="8fea3-258">The payment retention percentage is specified in the project contract.</span></span> <span data-ttu-id="8fea3-259">L'import es calcula i es resta en funció del valor total de les línies d'una factura de client.</span><span class="sxs-lookup"><span data-stu-id="8fea3-259">The amount is calculated based on, and subtracted from, the total value of the lines in a customer invoice.</span></span> 

<span data-ttu-id="8fea3-260">Per a les regles de facturació **Temps i de materials** i **Progrés**, podeu assignar categories imputables.</span><span class="sxs-lookup"><span data-stu-id="8fea3-260">For **Time and material** and **Progress** billing rules, you can assign chargeable categories.</span></span> <span data-ttu-id="8fea3-261">Les categories imputables indiquen les transaccions que s'han d'incloure a les factures de client.</span><span class="sxs-lookup"><span data-stu-id="8fea3-261">Chargeable categories indicate the transactions that should be included in customer invoices.</span></span> 

<span data-ttu-id="8fea3-262">Quan estigueu a punt per facturar el client, l'import de la factura del projecte es calcula segons les regles de facturació i es genera una proposta de factura de projecte.</span><span class="sxs-lookup"><span data-stu-id="8fea3-262">When you are ready to invoice the customer, the amount to invoice for the project is calculated based on the billing rules, and a project invoice proposal is generated.</span></span> 

<span data-ttu-id="8fea3-263">A les seccions següents s'ofereixen exemples que mostren la configuració i l'administració de les regles de facturació d'un projecte.</span><span class="sxs-lookup"><span data-stu-id="8fea3-263">The following sections provide examples that show how to set up and manage billing rules for a project.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a><span data-ttu-id="8fea3-264">Exemple: crear una regla de facturació basada en el nombre d'unitats entregades</span><span class="sxs-lookup"><span data-stu-id="8fea3-264">Example: Create a billing rule that is based on the number of units delivered</span></span>

<span data-ttu-id="8fea3-265">La vostra organització entra en un acord per proporcionar un total de cinc sessions formatives als empleats d'un client amb un cost de 10.000 USD per sessió formativa.</span><span class="sxs-lookup"><span data-stu-id="8fea3-265">Your organization enters into an agreement to provide a total of five training sessions to a customer’s employees at a cost of 10,000 per training session.</span></span> <span data-ttu-id="8fea3-266">Factureu al client després de cada sessió formativa.</span><span class="sxs-lookup"><span data-stu-id="8fea3-266">You invoice the customer after each training session.</span></span> 

<span data-ttu-id="8fea3-267">Quan configureu les regles de facturació per al contracte, s'utilitzen els valors següents:</span><span class="sxs-lookup"><span data-stu-id="8fea3-267">When you set up the billing rules for the contract, you use the following values:</span></span>

-   <span data-ttu-id="8fea3-268">La unitat de lliurament és una sessió formativa.</span><span class="sxs-lookup"><span data-stu-id="8fea3-268">The unit of delivery is one training session.</span></span>
-   <span data-ttu-id="8fea3-269">El preu unitari és de 10.000 per sessió formativa.</span><span class="sxs-lookup"><span data-stu-id="8fea3-269">The unit price is 10,000 per training session.</span></span>
-   <span data-ttu-id="8fea3-270">El nombre total d'unitats és de cinc sessions formatives.</span><span class="sxs-lookup"><span data-stu-id="8fea3-270">The total number of units is five training sessions.</span></span>

<span data-ttu-id="8fea3-271">Quan hàgiu completat una sessió formativa, podeu crear una factura de 10.000, per a la primera unitat que s'ha lliurat i enviar la factura al client.</span><span class="sxs-lookup"><span data-stu-id="8fea3-271">When you have completed one training session, you can create an invoice for 10,000, for the first unit that was delivered, and send the invoice to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a><span data-ttu-id="8fea3-272">Exemple: crear una regla de facturació basada en un percentatge especificat de finalització del projecte (càlcul manual)</span><span class="sxs-lookup"><span data-stu-id="8fea3-272">Example: Create a billing rule that is based on a specified percentage of project completion (manual calculation)</span></span>

<span data-ttu-id="8fea3-273">La vostra organització, una firma de consultoria de programari, entra en un acord amb un client per desenvolupar part d'un producte que el client està desenvolupant.</span><span class="sxs-lookup"><span data-stu-id="8fea3-273">Your organization, a software consulting firm, enters into an agreement with a customer to develop part of a product that the customer is developing.</span></span> <span data-ttu-id="8fea3-274">L'organització accepta el lliurament del codi de programari durant un període de sis mesos.</span><span class="sxs-lookup"><span data-stu-id="8fea3-274">Your organization agrees to deliver the software code over a period of six months.</span></span> <span data-ttu-id="8fea3-275">El client es compromet a pagar a la vostra organització un total de 100.000 pel treball.</span><span class="sxs-lookup"><span data-stu-id="8fea3-275">The customer agrees to pay your organization a total of 100,000 for the work.</span></span> <span data-ttu-id="8fea3-276">Creeu una regla de facturació per facturar al client en funció del percentatge de treball que s'hagi completat al projecte, tal com s'especifica al contracte.</span><span class="sxs-lookup"><span data-stu-id="8fea3-276">You create a billing rule to invoice the customer based on the percentage of work that is completed on the project, as specified in the contract.</span></span>

-   <span data-ttu-id="8fea3-277">Al final del primer mes, us trobeu amb el client per determinar el percentatge de feina completada.</span><span class="sxs-lookup"><span data-stu-id="8fea3-277">At the end of the first month, you meet with the customer to determine the percentage of work completed.</span></span> <span data-ttu-id="8fea3-278">Després de revisar el projecte amb el client, decidiu que el projecte s'ha completat un 15 per cent.</span><span class="sxs-lookup"><span data-stu-id="8fea3-278">After you and the customer review the project, you decide that the project is 15 percent completed.</span></span>
-   <span data-ttu-id="8fea3-279">Es crea una factura per a 15.000 (15 per cent de 100.000) i s'envia al client.</span><span class="sxs-lookup"><span data-stu-id="8fea3-279">You create an invoice for 15,000 (15 percent of 100,000) and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a><span data-ttu-id="8fea3-280">Exemple: crear una regla de facturació basada en un percentatge especificat de finalització del projecte (càlcul automàtic)</span><span class="sxs-lookup"><span data-stu-id="8fea3-280">Example: Create a billing rule that is based on a specified percentage of project completion (automatic calculation)</span></span>

<span data-ttu-id="8fea3-281">La vostra organització, una firma de desenvolupament de programari, accepta desenvolupar un paquet de comptabilitat de nòmines d'un client per 30.000.</span><span class="sxs-lookup"><span data-stu-id="8fea3-281">Your organization, a software development firm, agrees to develop a payroll accounting package for a customer for 30,000.</span></span> <span data-ttu-id="8fea3-282">El client es compromet a pagar a la vostra organització en funció del percentatge de feina completada.</span><span class="sxs-lookup"><span data-stu-id="8fea3-282">The customer agrees to pay your organization based on the percentage of work completed.</span></span> <span data-ttu-id="8fea3-283">Estimeu que els costos del projecte són 20.000.</span><span class="sxs-lookup"><span data-stu-id="8fea3-283">You estimate that the project costs are 20,000.</span></span> <span data-ttu-id="8fea3-284">El contracte del projecte especifica les categories de treball que utilitzeu en el procés de facturació.</span><span class="sxs-lookup"><span data-stu-id="8fea3-284">The project contract specifies the categories of work that you use in the billing process.</span></span> <span data-ttu-id="8fea3-285">Configureu regles de facturació que calculen automàticament els imports de la factura per al percentatge de treball que s'ha completat per a cada categoria.</span><span class="sxs-lookup"><span data-stu-id="8fea3-285">You set up billing rules that automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="8fea3-286">Configureu un pressupost per a cada categoria:</span><span class="sxs-lookup"><span data-stu-id="8fea3-286">You set up a budget for each category:</span></span>

-   <span data-ttu-id="8fea3-287">**Desenvolupament**: cost de 15.000 i ingressos de 20.000</span><span class="sxs-lookup"><span data-stu-id="8fea3-287">**Development** – Cost of 15,000 and revenue of 20,000</span></span>
-   <span data-ttu-id="8fea3-288">**Instal·lació**: cost de 5.000 i ingressos de 10.000</span><span class="sxs-lookup"><span data-stu-id="8fea3-288">**Installation** – Cost of 5,000 and revenue of 10,000</span></span>

<span data-ttu-id="8fea3-289">Quan creeu una factura del client per primer cop, l'import de la factura es calcula automàticament segons la informació següent:</span><span class="sxs-lookup"><span data-stu-id="8fea3-289">When you create a customer invoice for the first time, the invoice amount is automatically calculated based on the following information:</span></span>

-   <span data-ttu-id="8fea3-290">Després d'un mes, el treballador del projecte envia un full d'hores per al projecte.</span><span class="sxs-lookup"><span data-stu-id="8fea3-290">After a month, the worker on the project submits a timesheet for the project.</span></span> <span data-ttu-id="8fea3-291">El cost de les hores del treballador és de 5.000 per al desenvolupament i 1.000 per a la instal·lació.</span><span class="sxs-lookup"><span data-stu-id="8fea3-291">The cost of the worker’s hours is 5,000 for development and 1,000 for installation.</span></span> <span data-ttu-id="8fea3-292">El treball de desenvolupament està completat en un 33 per cent (5.000 cost real/15.000 cost pressupostat), i el treball d'instal lació està completat en un 20 per cent (1.000 cost real/5.000 cost pressupostat).</span><span class="sxs-lookup"><span data-stu-id="8fea3-292">The development work is 33 percent completed (5,000 actual cost/15,000 budget cost), and the installation work is 20 percent completed (1,000 actual cost/5,000 budget cost).</span></span>
-   <span data-ttu-id="8fea3-293">El import de la factura de 8.667 es calcula automàticament (33 per cent de 20.000 + 20 per cent de 10.000).</span><span class="sxs-lookup"><span data-stu-id="8fea3-293">The invoice amount of 8,667 is automatically calculated (33 percent of 20,000 + 20 percent of 10,000).</span></span>
-   <span data-ttu-id="8fea3-294">Es crea una factura per 8.667 i s'envia al client.</span><span class="sxs-lookup"><span data-stu-id="8fea3-294">You create an invoice for 8,667 and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a><span data-ttu-id="8fea3-295">Exemple: crear una regla de facturació basada en les fites acordades</span><span class="sxs-lookup"><span data-stu-id="8fea3-295">Example: Create a billing rule that is based on agreed-upon milestones</span></span>

<span data-ttu-id="8fea3-296">La vostra organització, una consultora de gestió, accepta dur a terme una investigació de mercat per a un producte de consum que el client té previst vendre.</span><span class="sxs-lookup"><span data-stu-id="8fea3-296">Your organization, a management consulting firm, agrees to conduct market research for a consumer product that the customer plans to sell.</span></span> <span data-ttu-id="8fea3-297">El client es compromet a utilitzar els vostres serveis durant un període de tres mesos, començant pel març, i es compromet a pagar 50.000 a la vostra seva organització.</span><span class="sxs-lookup"><span data-stu-id="8fea3-297">The customer agrees to use your services for a period of three months, starting in March, and agrees to pay your organization 50,000.</span></span> <span data-ttu-id="8fea3-298">El projecte té tres fites:</span><span class="sxs-lookup"><span data-stu-id="8fea3-298">The project has three milestones:</span></span>

-   <span data-ttu-id="8fea3-299">Fita 1: recopilar dades dels consumidors, 31 de març</span><span class="sxs-lookup"><span data-stu-id="8fea3-299">Milestone 1: Collect consumer data – March 31</span></span>
-   <span data-ttu-id="8fea3-300">Fita 2: analitzar les dades dels consumidors, 30 d'abril</span><span class="sxs-lookup"><span data-stu-id="8fea3-300">Milestone 2: Analyze consumer data – April 30</span></span>
-   <span data-ttu-id="8fea3-301">Fita 3: presentar una proposta de viabilitat del producte, 31 de maig</span><span class="sxs-lookup"><span data-stu-id="8fea3-301">Milestone 3: Present a product viability proposal – May 31</span></span>

<span data-ttu-id="8fea3-302">El client es compromet a pagar a la vostra organització 10.000 per la primera fita, 20.000 per la segona fita i 20.000 per la tercera fita.</span><span class="sxs-lookup"><span data-stu-id="8fea3-302">The customer agrees to pay your organization 10,000 for the first milestone, 20,000 for the second milestone, and 20,000 for the third milestone.</span></span> 

<span data-ttu-id="8fea3-303">Quan configureu el contracte del projecte, accepteu que factureu al client segons la fita que s'hagi completat.</span><span class="sxs-lookup"><span data-stu-id="8fea3-303">When you set up the project contract, you agree to bill the customer based on the milestone that has been completed.</span></span> <span data-ttu-id="8fea3-304">La configuració de la regla de facturació inclou els passos següents:</span><span class="sxs-lookup"><span data-stu-id="8fea3-304">The billing rule setup includes the following steps:</span></span>

-   <span data-ttu-id="8fea3-305">Definir les fites del projecte.</span><span class="sxs-lookup"><span data-stu-id="8fea3-305">Define the project milestones.</span></span>
-   <span data-ttu-id="8fea3-306">Definir l'import per facturar al client quan s'hagi completat cada fita.</span><span class="sxs-lookup"><span data-stu-id="8fea3-306">Define the amount to invoice the customer when each milestone is completed.</span></span>

<span data-ttu-id="8fea3-307">Quan la primera fita es completa el 31 de març, es marca la fita com a completada i, a continuació, es crea una factura per 10.000 i s'envia al client.</span><span class="sxs-lookup"><span data-stu-id="8fea3-307">When the first milestone is completed on March 31, you mark the milestone as completed, and then create an invoice for 10,000 and send it to the customer.</span></span> <span data-ttu-id="8fea3-308">No podeu crear una factura per a una fita fins que no hàgiu marcat la fita com a completada.</span><span class="sxs-lookup"><span data-stu-id="8fea3-308">You can’t create an invoice for a milestone until you have marked the milestone as completed.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a><span data-ttu-id="8fea3-309">Exemple: crear una regla de facturació basada en els serveis més una taxa d'administració</span><span class="sxs-lookup"><span data-stu-id="8fea3-309">Example: Create a billing rule that is based on services plus a management fee</span></span>

<span data-ttu-id="8fea3-310">La vostra organització, una consultora de gestió, accepta dur a terme una investigació de mercat per avaluar la viabilitat d'un producte que el client, una empresa minorista, està desenvolupant.</span><span class="sxs-lookup"><span data-stu-id="8fea3-310">Your organization, a management consulting firm, agrees to conduct market research to evaluate the viability of a product that the customer, a retail company, is developing.</span></span> <span data-ttu-id="8fea3-311">Els termes de l'acord especifiquen que proporcioneu els serveis dels tres principals consultors d'administració, els quals dirigeixen la recerca segons temps i materials.</span><span class="sxs-lookup"><span data-stu-id="8fea3-311">The terms of the agreement specify that you will provide the services of your top three management consultants, who will conduct the research on a time-and-materials basis.</span></span> <span data-ttu-id="8fea3-312">El client acorda pagar 100 per hora, a més d'una taxa d'administració del 10 per cent per a les hores de consultoria que es carregaran en el projecte.</span><span class="sxs-lookup"><span data-stu-id="8fea3-312">The customer agrees to pay 100 per hour, plus a 10 percent management fee for the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="8fea3-313">Quan configureu el contracte del projecte, creeu una regla de facturació per afegir una taxa d'administració del 10 per cent a les hores de consultoria que es carregaran al projecte.</span><span class="sxs-lookup"><span data-stu-id="8fea3-313">When you set up the project contract, create a billing rule to add a 10 percent management fee to the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="8fea3-314">Quan creeu una factura per al client, es factura al client un 10 per cent de taxa d'administració i el cost de les hores de consultoria.</span><span class="sxs-lookup"><span data-stu-id="8fea3-314">When you create an invoice for the customer, the customer is billed a 10 percent management fee plus the cost of the consulting hours.</span></span> <span data-ttu-id="8fea3-315">Per exemple, si els tres consultors han treballat un total de 200 hores en el projecte, es crea una factura de 22.000 segons el càlcul següent:</span><span class="sxs-lookup"><span data-stu-id="8fea3-315">For example, if the three consultants worked a total of 200 hours on the project, an invoice for 22,000 is created based on the following calculation:</span></span>

-   <span data-ttu-id="8fea3-316">200 hores a 100 per hora = 20.000</span><span class="sxs-lookup"><span data-stu-id="8fea3-316">200 hours at 100 per hour = 20,000</span></span>
-   <span data-ttu-id="8fea3-317">Taxa d'administració del 10 per cent = 2.000</span><span class="sxs-lookup"><span data-stu-id="8fea3-317">10 percent management fee = 2,000</span></span>
-   <span data-ttu-id="8fea3-318">Import total de la factura = 22.000</span><span class="sxs-lookup"><span data-stu-id="8fea3-318">Total invoice amount = 22,000</span></span>

<span data-ttu-id="8fea3-319">Si les taxes estan imposades a un client i seleccioneu un grup d'impostos de vendes al contracte del projecte, el grup d'impostos de vendes s'introdueix automàticament en una regla de facturació per a les taxes.</span><span class="sxs-lookup"><span data-stu-id="8fea3-319">If fees are taxable to a customer, and you select a sales tax group in the project contract, the sales tax group is automatically entered in a billing rule for fees.</span></span>

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a><span data-ttu-id="8fea3-320">Exemple: crear una regla de facturació per al valor del temps i els materials</span><span class="sxs-lookup"><span data-stu-id="8fea3-320">Example: Create a billing rule for the value of time and materials</span></span>

<span data-ttu-id="8fea3-321">La vostra organització, una consultora de programari, accepta proporcionar cinc consultors tècnics per treballar en un projecte de desenvolupament de programari per a un client durant els pròxims sis mesos.</span><span class="sxs-lookup"><span data-stu-id="8fea3-321">Your organization, a software consulting firm, agrees to provide five technical consultants to work on a software development project for a customer for the next six months.</span></span> <span data-ttu-id="8fea3-322">El client es compromet a pagar 150 per cada hora de consultoria, a més del cost dels subministraments de l'oficina.</span><span class="sxs-lookup"><span data-stu-id="8fea3-322">The customer agrees to pay 150 for each consulting hour, plus the cost of office supplies.</span></span> <span data-ttu-id="8fea3-323">La vostra organització envia una factura al client al final de cada mes.</span><span class="sxs-lookup"><span data-stu-id="8fea3-323">Your organization sends an invoice to the customer at the end of each month.</span></span> 

<span data-ttu-id="8fea3-324">Quan configureu el contracte del projecte, accepteu facturar al client cada mes pel temps i els materials del projecte.</span><span class="sxs-lookup"><span data-stu-id="8fea3-324">When you set up the project contract, you agree to bill the customer each month for time and materials on the project.</span></span> <span data-ttu-id="8fea3-325">Creeu una regla de facturació que inclou la següent informació:</span><span class="sxs-lookup"><span data-stu-id="8fea3-325">You create a billing rule that includes the following information:</span></span>

-   <span data-ttu-id="8fea3-326">El període del contracte és de sis mesos.</span><span class="sxs-lookup"><span data-stu-id="8fea3-326">The contract period is six months.</span></span>
-   <span data-ttu-id="8fea3-327">El temps de consulta es calcula a una relació de 150 per hora.</span><span class="sxs-lookup"><span data-stu-id="8fea3-327">Consulting time is calculated at a rate of 150 per hour.</span></span>
-   <span data-ttu-id="8fea3-328">Els subministraments d'oficina es facturen a un cost i el cost total del projecte no pot superar els 10.000.</span><span class="sxs-lookup"><span data-stu-id="8fea3-328">Office supplies are invoiced at cost, and the total cost for the project must not exceed 10,000.</span></span>
-   <span data-ttu-id="8fea3-329">Creeu una factura del client al final de cada mes natural durant el projecte.</span><span class="sxs-lookup"><span data-stu-id="8fea3-329">You create a customer invoice at the end of each calendar month during the project.</span></span>

<span data-ttu-id="8fea3-330">Durant el primer mes, es registren un total de 800 hores pels consultors del projecte.</span><span class="sxs-lookup"><span data-stu-id="8fea3-330">During the first month, a total of 800 hours are recorded by the consultants on the project.</span></span> <span data-ttu-id="8fea3-331">El cost dels subministraments d'oficina que es carrega en el projecte és de 2.000.</span><span class="sxs-lookup"><span data-stu-id="8fea3-331">The cost of office supplies that are charged to the project is 2,000.</span></span> <span data-ttu-id="8fea3-332">Per tant, al final del mes, es crea una factura de 122.000, que es calcula com a 800 hores a 150 per hora, més 2.000 per subministraments d'oficina.</span><span class="sxs-lookup"><span data-stu-id="8fea3-332">Therefore, at the end of the month, you create an invoice for 122,000, which is calculated as 800 hours at 150 per hour, plus 2,000 for office supplies.</span></span>





[!INCLUDE[footer-include](../includes/footer-banner.md)]