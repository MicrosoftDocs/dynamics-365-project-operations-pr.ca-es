---
title: Configurar l'administració de despeses
description: Aquest article descriu les consideracions i les decisions que heu de prendre durant el procés de planificació abans de configurar l'administració de despeses al Microsoft Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 08/29/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: db3529597c662a326730cf6a0b855ae865f0dce5
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960325"
---
# <a name="configure-expense-management"></a><span data-ttu-id="388cb-103">Configurar l'administració de despeses</span><span class="sxs-lookup"><span data-stu-id="388cb-103">Configure expense management</span></span>

<span data-ttu-id="388cb-104">Aquest tema descriu les consideracions i les decisions que heu de prendre durant el procés de planificació abans de configurar l'administració de despeses.</span><span class="sxs-lookup"><span data-stu-id="388cb-104">This topic describes the considerations and the decisions that you must make during the planning process before you configure Expense management.</span></span> <span data-ttu-id="388cb-105">A l'administració de despeses, es pot emmagatzemar informació sobre els mètodes de pagament, les sol·licituds de viatge, els informes de despeses, les normes, etc.</span><span class="sxs-lookup"><span data-stu-id="388cb-105">In Expense management, you can store information about payment methods, travel requisitions, expense reports, policies, and so on.</span></span>

<span data-ttu-id="388cb-106">Com que moltes de les decisions que preneu quan planifiqueu la vostra configuració per a l'administració de despeses es basen en la jerarquia i l'estructura financera de la vostra organització, cal que consulteu els documents de planificació per a aquestes àrees.</span><span class="sxs-lookup"><span data-stu-id="388cb-106">Because many of the decisions that you make when you plan your configuration for Expense management are based on your organization’s hierarchy and financial structure, you must refer to the planning documents for those areas.</span></span>

## <a name="intercompany-expenses"></a><span data-ttu-id="388cb-107">Despeses entre empreses</span><span class="sxs-lookup"><span data-stu-id="388cb-107">Intercompany expenses</span></span>

<span data-ttu-id="388cb-108">Quan habiliteu les despeses entre empreses, permeteu que entitats jurídiques i empleats incorrin despeses en nom d'una altra entitat jurídica, i recapteu el pagament des de l'entitat jurídica d'ocupació de la vostra organització.</span><span class="sxs-lookup"><span data-stu-id="388cb-108">When you enable intercompany expenses, you allow legal entities and employees to incur expenses on behalf of another legal entity, and collect payment from the legal entity of employment within your organization.</span></span> <span data-ttu-id="388cb-109">Per exemple, un empleat de l'entitat jurídica A completa un projecte per a l'entitat jurídica B, i el projecte incorre en despeses relacionades amb els viatges.</span><span class="sxs-lookup"><span data-stu-id="388cb-109">For example, an employee in legal entity A completes a project for legal entity B, and the project incurs travel related expenses.</span></span> <span data-ttu-id="388cb-110">Si les despeses entre empreses estan habilitades, l'empleat pot presentar un informe de despeses que comptabilitzarà la despesa a l'entitat jurídica B i la despesa s'haurà de pagar l'entitat jurídica A. Si la vostra organització no té diverses entitats legals, no cal que habiliteu les despeses entre empreses.</span><span class="sxs-lookup"><span data-stu-id="388cb-110">If intercompany expenses are enabled, the employee can then file an expense report that will post the expense to legal entity B, and the expense must then be paid by legal entity A. If your organization doesn’t have multiple legal entities, you don’t have to enable intercompany expenses.</span></span>

<span data-ttu-id="388cb-111">**Decisió:** voleu habilitar les despeses entre empreses?</span><span class="sxs-lookup"><span data-stu-id="388cb-111">**Decision:** Do you want to enable intercompany expenses?</span></span>

## <a name="financial-management"></a><span data-ttu-id="388cb-112">Administració financera</span><span class="sxs-lookup"><span data-stu-id="388cb-112">Financial management</span></span>

<span data-ttu-id="388cb-113">L'administració de despeses està estretament integrada amb l'administració financera de la vostra organització.</span><span class="sxs-lookup"><span data-stu-id="388cb-113">Expense management is tightly integrated with the financial management of your organization.</span></span> <span data-ttu-id="388cb-114">Bona part de la configuració per a l'administració de despeses es basarà en les decisions que heu pres sobre les finances de la vostra organització.</span><span class="sxs-lookup"><span data-stu-id="388cb-114">Lots of your configuration for Expense management will be based on the decisions that you’ve made about your organization’s finances.</span></span> <span data-ttu-id="388cb-115">Les següents seccions descriuen les diverses àrees que requereixen planificació i decisions, en funció de les decisions financeres de la vostra organització i les pautes del vostre equip de lideratge.</span><span class="sxs-lookup"><span data-stu-id="388cb-115">The following sections describe the various areas that require planning and decisions, based on your organization’s financial decisions and guidance from your leadership team.</span></span>

### <a name="per-diems"></a><span data-ttu-id="388cb-116">Dietes</span><span class="sxs-lookup"><span data-stu-id="388cb-116">Per diems</span></span>

<span data-ttu-id="388cb-117">Heu de definir les dietes per a empleats que proporciona la vostra organització.</span><span class="sxs-lookup"><span data-stu-id="388cb-117">You must define the employee per diems that your organization provides.</span></span> <span data-ttu-id="388cb-118">Com que les dietes s'utilitzen normalment per cobrir despeses com ara àpats, allotjament i altres despeses incidentals, es poden crear regles per a les dietes que ofereix la vostra organització.</span><span class="sxs-lookup"><span data-stu-id="388cb-118">Because per diems are typically used to cover expenses such as meals, lodging, and other incidental expenses, you can create rules for the per diem allowances that your organization offers.</span></span> <span data-ttu-id="388cb-119">Les tarifes de les dietes es poden basar en l'època de l'any, en la ubicació del viatge o tots dos.</span><span class="sxs-lookup"><span data-stu-id="388cb-119">per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="388cb-120">Quan definiu una regla de dieta, podeu especificar que un percentatge de la tarifa de la dieta es retindrà si un treballador rep àpats o serveis gratuïts.</span><span class="sxs-lookup"><span data-stu-id="388cb-120">When you define a per diem rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="388cb-121">També podeu definir nivells de dietes per establir el nombre mínim i màxim d'hores en què la tarifa de dieta es pot aplicar als viatges d'un treballador.</span><span class="sxs-lookup"><span data-stu-id="388cb-121">You can also define per diem rate tiers to set the minimum and maximum number of hours that the per diem rate can be applied to a worker’s travel.</span></span>

<span data-ttu-id="388cb-122">**Decisions:**</span><span class="sxs-lookup"><span data-stu-id="388cb-122">**Decisions:**</span></span>

- <span data-ttu-id="388cb-123">Regles predeterminades de dietes per al primer i l'últim dia:</span><span class="sxs-lookup"><span data-stu-id="388cb-123">Default per diem rules for the first and last days:</span></span>

    - <span data-ttu-id="388cb-124">Quin és el nombre mínim d'hores que un empleat pot reclamar per a un dia i rebre una dieta?</span><span class="sxs-lookup"><span data-stu-id="388cb-124">What is the minimum number of hours that an employee can claim for a day and still receive a per diem?</span></span>
    - <span data-ttu-id="388cb-125">Hi ha una reducció de l'import que s'ofereix per als àpats durant el primer dia i l'últim dia?</span><span class="sxs-lookup"><span data-stu-id="388cb-125">Is there a reduction in the amount that is offered for meals for the first day and last day?</span></span> <span data-ttu-id="388cb-126">Si hi ha una reducció, quin és el percentatge de la reducció?</span><span class="sxs-lookup"><span data-stu-id="388cb-126">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="388cb-127">Hi ha una reducció de l'import que s'ofereix per a un hotel durant el primer dia i l'últim dia?</span><span class="sxs-lookup"><span data-stu-id="388cb-127">Is there a reduction in the amount that is offered for a hotel for the first day and last day?</span></span> <span data-ttu-id="388cb-128">Si hi ha una reducció, quin és el percentatge de la reducció?</span><span class="sxs-lookup"><span data-stu-id="388cb-128">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="388cb-129">Hi ha una reducció de l'import que s'ofereix per a altres despeses incorregudes durant el primer dia i l'últim dia?</span><span class="sxs-lookup"><span data-stu-id="388cb-129">Is there a reduction in the amount that is offered for other expenses that are incurred on the first day and last day?</span></span> <span data-ttu-id="388cb-130">Si hi ha una reducció, quin és el percentatge de la reducció?</span><span class="sxs-lookup"><span data-stu-id="388cb-130">If there is a reduction, what is the percentage of the reduction?</span></span>

- <span data-ttu-id="388cb-131">Regles de dietes per defecte:</span><span class="sxs-lookup"><span data-stu-id="388cb-131">Default per diem rules:</span></span>

    - <span data-ttu-id="388cb-132">Hi ha una reducció percentual de les dietes per a cada àpat si, per exemple, l'àpat és complementari?</span><span class="sxs-lookup"><span data-stu-id="388cb-132">Is there a percentage reduction in the per diem allowance for each meal if, for example, the meal is complimentary?</span></span> <span data-ttu-id="388cb-133">Si hi ha una reducció, quin és el percentatge de reducció de cada àpat?</span><span class="sxs-lookup"><span data-stu-id="388cb-133">If there is a reduction, what is the reduction percentage for each meal?</span></span>
    - <span data-ttu-id="388cb-134">Es calcula la reducció d'àpats per dia, per viatge o per nombre d'àpats al dia?</span><span class="sxs-lookup"><span data-stu-id="388cb-134">Is the meal reduction calculated per day, per trip, or by the number of meals per day?</span></span>
    - <span data-ttu-id="388cb-135">S'han d'arrodonir els imports de les dietes de manera normal o arrodonir-los cap amunt?</span><span class="sxs-lookup"><span data-stu-id="388cb-135">Should per diem amounts be rounded in the regular manner or rounded up?</span></span>
    - <span data-ttu-id="388cb-136">Es calculen les dietes en un període de 24 hores o en un dia de calendari?</span><span class="sxs-lookup"><span data-stu-id="388cb-136">Are per diems calculated on a 24-hour period or on a calendar day?</span></span>

- <span data-ttu-id="388cb-137">Regles de dietes que es basen en la ubicació:</span><span class="sxs-lookup"><span data-stu-id="388cb-137">Per diem rules that are based on location:</span></span>

    - <span data-ttu-id="388cb-138">Les tarifes de les dietes varien segons la ubicació?</span><span class="sxs-lookup"><span data-stu-id="388cb-138">Do per diem rates vary according to location?</span></span> <span data-ttu-id="388cb-139">Quines ubicacions s'inclouen?</span><span class="sxs-lookup"><span data-stu-id="388cb-139">What locations are included?</span></span>
    - <span data-ttu-id="388cb-140">Si les tarifes de les dietes varien segons la ubicació, per a cada ubicació, quina quantitat percentual es proporciona per als següents tipus de despeses:</span><span class="sxs-lookup"><span data-stu-id="388cb-140">If per diem rates vary according to location, for each location, what percentage amount is provided for the following types of expenses:</span></span>

        - <span data-ttu-id="388cb-141">Àpats</span><span class="sxs-lookup"><span data-stu-id="388cb-141">Meals</span></span>
        - <span data-ttu-id="388cb-142">Hotels</span><span class="sxs-lookup"><span data-stu-id="388cb-142">Hotel</span></span>
        - <span data-ttu-id="388cb-143">Altres despeses</span><span class="sxs-lookup"><span data-stu-id="388cb-143">Other expenses</span></span>

### <a name="expense-management-journals-and-accounts"></a><span data-ttu-id="388cb-144">Diaris i comptes d'administració de despeses</span><span class="sxs-lookup"><span data-stu-id="388cb-144">Expense management journals and accounts</span></span>

<span data-ttu-id="388cb-145">L'administració de despeses requereix que utilitzeu diversos diaris i comptes.</span><span class="sxs-lookup"><span data-stu-id="388cb-145">Expense management requires that you use multiple journals and accounts.</span></span> <span data-ttu-id="388cb-146">Heu de decidir, per exemple, si s'utilitza el mateix compte per als avançaments d'efectiu i les disputes de targetes de crèdit.</span><span class="sxs-lookup"><span data-stu-id="388cb-146">You must decide, for example, whether the same account is used for cash advances and credit card disputes.</span></span>

<span data-ttu-id="388cb-147">**Decisions:**</span><span class="sxs-lookup"><span data-stu-id="388cb-147">**Decisions:**</span></span>

- <span data-ttu-id="388cb-148">A quin llibre diari es comptabilitzen els informes de despeses aprovats?</span><span class="sxs-lookup"><span data-stu-id="388cb-148">Which ledger journal are approved expense reports posted to?</span></span>
- <span data-ttu-id="388cb-149">Quin compte s'utilitza per als avançaments d'efectiu?</span><span class="sxs-lookup"><span data-stu-id="388cb-149">Which account is used for cash advances?</span></span>
- <span data-ttu-id="388cb-150">Cal comptabilitzar immediatament els avançaments d'efectiu?</span><span class="sxs-lookup"><span data-stu-id="388cb-150">Should cash advances be posted immediately?</span></span>

### <a name="payment-methods"></a><span data-ttu-id="388cb-151">Mètodes de pagament</span><span class="sxs-lookup"><span data-stu-id="388cb-151">Payment methods</span></span>

<span data-ttu-id="388cb-152">Quan es permet als empleats incórrer despeses en nom del seu negoci, cal definir els mètodes de pagament que poden utilitzar els empleats.</span><span class="sxs-lookup"><span data-stu-id="388cb-152">When you allow employees to incur expenses on behalf of your business, you must define the payment methods that employees are allowed to use.</span></span> <span data-ttu-id="388cb-153">Per exemple, es podria permetre als empleats utilitzar diners en efectiu o una targeta de crèdit corporativa.</span><span class="sxs-lookup"><span data-stu-id="388cb-153">For example, you might allow employees to use cash or a corporate credit card.</span></span> <span data-ttu-id="388cb-154">També es podria permetre que els empleats utilitzessin targetes de crèdit personals i després reemborsar als empleats.</span><span class="sxs-lookup"><span data-stu-id="388cb-154">You might also allow employees to use personal credit cards, and then reimburse the employees.</span></span> <span data-ttu-id="388cb-155">Heu de prendre les següents decisions per a cada mètode de pagament que permeteu.</span><span class="sxs-lookup"><span data-stu-id="388cb-155">You must make the following decisions for each payment method that you allow.</span></span>

<span data-ttu-id="388cb-156">**Decisions:**</span><span class="sxs-lookup"><span data-stu-id="388cb-156">**Decisions:**</span></span>

- <span data-ttu-id="388cb-157">Quins mètodes de pagament es permeten?</span><span class="sxs-lookup"><span data-stu-id="388cb-157">What payment methods are allowed?</span></span>
- <span data-ttu-id="388cb-158">Qui és el propietari del mètode de pagament?</span><span class="sxs-lookup"><span data-stu-id="388cb-158">Who owns the payment method expenses?</span></span>
- <span data-ttu-id="388cb-159">Hi ha un tipus de compte de desplaçament?</span><span class="sxs-lookup"><span data-stu-id="388cb-159">Is there an offset account type?</span></span> <span data-ttu-id="388cb-160">Si hi ha un tipus de compte de desplaçament, quin és?</span><span class="sxs-lookup"><span data-stu-id="388cb-160">If there is an offset account type, what is it?</span></span>
- <span data-ttu-id="388cb-161">Si hi ha un compte de desplaçament, quin és el compte?</span><span class="sxs-lookup"><span data-stu-id="388cb-161">If there is an offset account, what is the account?</span></span>
- <span data-ttu-id="388cb-162">Si el mètode de pagament és una targeta de crèdit, hauria d'utilitzar-se el mètode de pagament únicament amb transaccions importades?</span><span class="sxs-lookup"><span data-stu-id="388cb-162">If the payment method is a credit card, should the payment method be used only with imported transactions?</span></span>

### <a name="expense-categories-and-shared-categories"></a><span data-ttu-id="388cb-163">Categories de despeses i categories compartides</span><span class="sxs-lookup"><span data-stu-id="388cb-163">Expense categories and shared categories</span></span>

<span data-ttu-id="388cb-164">Quan els empleats creen un informe de despeses, cada despesa que registren s'ha d'associar amb una categoria de despesa.</span><span class="sxs-lookup"><span data-stu-id="388cb-164">When employees create an expense report, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="388cb-165">Les categories de despeses es deriven de les categories compartides que es poden compartir amb els organismes jurídics de l'organització.</span><span class="sxs-lookup"><span data-stu-id="388cb-165">Expense categories are derived from shared categories that can be shared across the legal entities in your organization.</span></span> <span data-ttu-id="388cb-166">Aquestes categories també es poden compartir a l'administració de projectes i la comptabilitat, en funció de la forma com es defineixi la vostra organització.</span><span class="sxs-lookup"><span data-stu-id="388cb-166">These categories can also be shared in Project management and accounting, depending on the way that your organization is defined.</span></span> <span data-ttu-id="388cb-167">Segons la definició de l'organització i de l'orientació de l'equip d'implementació, cal que determineu si les categories que s'utilitzen a l'administració de despeses només s'utilitzaran a l'administració de despeses o si s'han de compartir entre l'administració de projectes i la comptabilitzat i l'administració de despeses.</span><span class="sxs-lookup"><span data-stu-id="388cb-167">Based on the definition of your organization and guidance from the implementation team, determine whether the categories that are used in Expense management will be used only in Expense management, or whether they should be shared between Project management and accounting and Expense management.</span></span> <span data-ttu-id="388cb-168">Tingueu en compte que aquestes categories es poden compartir entre el projecte i la despesa i el projecte i producció, però no entre la despesa i producció.</span><span class="sxs-lookup"><span data-stu-id="388cb-168">Note that these categories can be shared between Project and Expense or Project and Production, but not between Expense and Production.</span></span> <span data-ttu-id="388cb-169">Heu de prendre les següents decisions per a cada categoria de despeses.</span><span class="sxs-lookup"><span data-stu-id="388cb-169">You must make the following decisions for each expense category.</span></span>

<span data-ttu-id="388cb-170">**Decisions:**</span><span class="sxs-lookup"><span data-stu-id="388cb-170">**Decisions:**</span></span>

- <span data-ttu-id="388cb-171">Quina és la categoria de despesa?</span><span class="sxs-lookup"><span data-stu-id="388cb-171">What is the expense category?</span></span> <span data-ttu-id="388cb-172">Alguns exemples són categories per a vols, hotels o quilometratge.</span><span class="sxs-lookup"><span data-stu-id="388cb-172">Examples include categories for flights, hotel, or mileage.</span></span>
- <span data-ttu-id="388cb-173">La categoria de despesa també pot utilitzar-se en l'administració de projectes i la comptabilitat?</span><span class="sxs-lookup"><span data-stu-id="388cb-173">Can the expense category also be used in Project management and accounting?</span></span>
- <span data-ttu-id="388cb-174">Quin és el tipus de despesa?</span><span class="sxs-lookup"><span data-stu-id="388cb-174">What is the expense type?</span></span>
- <span data-ttu-id="388cb-175">Què és el mètode de pagament per defecte per a la categoria de despesa?</span><span class="sxs-lookup"><span data-stu-id="388cb-175">What is the default payment method for the expense category?</span></span>
- <span data-ttu-id="388cb-176">Les despeses de la categoria de despesa s'hauran de desglossar?</span><span class="sxs-lookup"><span data-stu-id="388cb-176">Do expenses in the expense category have to be itemized?</span></span>
- <span data-ttu-id="388cb-177">Què és el compte per defecte principal per a la categoria de despesa?</span><span class="sxs-lookup"><span data-stu-id="388cb-177">What is the main default account for the expense category?</span></span>
- <span data-ttu-id="388cb-178">Què és el grup d'impostos de vendes de l'element per a la categoria de despeses?</span><span class="sxs-lookup"><span data-stu-id="388cb-178">What is the default item sales tax group for the expense category?</span></span>
- <span data-ttu-id="388cb-179">Es permeten mètodes de pagament addicionals per a la categoria de despeses?</span><span class="sxs-lookup"><span data-stu-id="388cb-179">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="388cb-180">Si es permeten mètodes de pagament addicionals, quins són?</span><span class="sxs-lookup"><span data-stu-id="388cb-180">If additional payment methods are allowed, what are they?</span></span>
- <span data-ttu-id="388cb-181">Hi ha subcategories en aquesta categoria de despeses?</span><span class="sxs-lookup"><span data-stu-id="388cb-181">Are there subcategories in this expense category?</span></span> <span data-ttu-id="388cb-182">Si hi ha subcategories, també heu de prendre les següents decisions:</span><span class="sxs-lookup"><span data-stu-id="388cb-182">If there are subcategories, you must also make the following decisions:</span></span>

    - <span data-ttu-id="388cb-183">S'exclou cap subcategoria de la recuperació d'impostos?</span><span class="sxs-lookup"><span data-stu-id="388cb-183">Are any of the subcategories excluded from tax recovery?</span></span>
    - <span data-ttu-id="388cb-184">Quin és el grup d'impostos de vendes de l'element de les subcategories?</span><span class="sxs-lookup"><span data-stu-id="388cb-184">What is the item sales tax group of the subcategories?</span></span>

<span data-ttu-id="388cb-185">Si la categoria de despeses també s'utilitza a l'administració de projectes i la comptabilitat, responeu les preguntes restants.</span><span class="sxs-lookup"><span data-stu-id="388cb-185">If the expense category is also used in Project management and accounting, answer the remaining questions.</span></span> <span data-ttu-id="388cb-186">En cas contrari, passeu a la següent secció.</span><span class="sxs-lookup"><span data-stu-id="388cb-186">Otherwise, move on to the next section.</span></span>

- <span data-ttu-id="388cb-187">Quins comptes de cost s'utilitzaran per a les despeses següents?</span><span class="sxs-lookup"><span data-stu-id="388cb-187">Which cost accounts will be used for the following expenses?</span></span>

    - <span data-ttu-id="388cb-188">Cost</span><span class="sxs-lookup"><span data-stu-id="388cb-188">Cost</span></span>
    - <span data-ttu-id="388cb-189">Assignació de nòmines</span><span class="sxs-lookup"><span data-stu-id="388cb-189">Payroll allocation</span></span>
    - <span data-ttu-id="388cb-190">En curs: valor de cost</span><span class="sxs-lookup"><span data-stu-id="388cb-190">WIP-cost value</span></span>
    - <span data-ttu-id="388cb-191">Cost: article</span><span class="sxs-lookup"><span data-stu-id="388cb-191">Cost-item</span></span>
    - <span data-ttu-id="388cb-192">En curs: valor de cost: article</span><span class="sxs-lookup"><span data-stu-id="388cb-192">WIP-cost value-item</span></span>
    - <span data-ttu-id="388cb-193">Pèrdua acumulada</span><span class="sxs-lookup"><span data-stu-id="388cb-193">Accrued loss</span></span>
    - <span data-ttu-id="388cb-194">En curs: pèrdua acumulada</span><span class="sxs-lookup"><span data-stu-id="388cb-194">WIP-accrued loss</span></span>

- <span data-ttu-id="388cb-195">Quins comptes d'ingressos s'utilitzaran per al següent?</span><span class="sxs-lookup"><span data-stu-id="388cb-195">Which revenue accounts will be used for the following?</span></span>

    - <span data-ttu-id="388cb-196">Ingressos facturats</span><span class="sxs-lookup"><span data-stu-id="388cb-196">Invoiced revenue</span></span>
    - <span data-ttu-id="388cb-197">Ingressos acumulats: valor de vendes</span><span class="sxs-lookup"><span data-stu-id="388cb-197">Accrued revenue-sales value</span></span>
    - <span data-ttu-id="388cb-198">En curs: valor de vendes</span><span class="sxs-lookup"><span data-stu-id="388cb-198">WIP-sales value</span></span>
    - <span data-ttu-id="388cb-199">Ingressos acumulats: producció</span><span class="sxs-lookup"><span data-stu-id="388cb-199">Accrued revenue-production</span></span>
    - <span data-ttu-id="388cb-200">En curs: producció</span><span class="sxs-lookup"><span data-stu-id="388cb-200">WIP-production</span></span>
    - <span data-ttu-id="388cb-201">Ingressos acumulats: beneficis</span><span class="sxs-lookup"><span data-stu-id="388cb-201">Accrued revenue-profit</span></span>
    - <span data-ttu-id="388cb-202">En curs: beneficis</span><span class="sxs-lookup"><span data-stu-id="388cb-202">WIP-profit</span></span>
    - <span data-ttu-id="388cb-203">Ingressos acumulats: subscripció</span><span class="sxs-lookup"><span data-stu-id="388cb-203">Accrued revenue-subscription</span></span>
    - <span data-ttu-id="388cb-204">En curs: subscripció</span><span class="sxs-lookup"><span data-stu-id="388cb-204">WIP-subscription</span></span>

### <a name="taxes"></a><span data-ttu-id="388cb-205">Impostos</span><span class="sxs-lookup"><span data-stu-id="388cb-205">Taxes</span></span>

<span data-ttu-id="388cb-206">Per als impostos relacionats amb les despeses, cal determinar què s'inclou o està habilitat als informes de despeses.</span><span class="sxs-lookup"><span data-stu-id="388cb-206">For expense-related taxes, you must determine what is included or enabled on expense reports.</span></span>

<span data-ttu-id="388cb-207">**Decisions:**</span><span class="sxs-lookup"><span data-stu-id="388cb-207">**Decisions:**</span></span>

- <span data-ttu-id="388cb-208">S'inclou l'impost sobre les vendes en els imports de les despeses?</span><span class="sxs-lookup"><span data-stu-id="388cb-208">Is sales tax included in the expense amounts?</span></span>
- <span data-ttu-id="388cb-209">S'hauria d'habilitar la recuperació de despeses a les despeses?</span><span class="sxs-lookup"><span data-stu-id="388cb-209">Should tax recovery be enabled on expenses?</span></span>

    > [!NOTE]
    > <span data-ttu-id="388cb-210">Quan vau planificar el llibre major, si vau decidir aplicar l'impost de vendes dels EUA i utilitzar regles d'impostos, no podeu habilitar la recuperació d'impostos sobre les despeses.</span><span class="sxs-lookup"><span data-stu-id="388cb-210">When you were planning the general ledger, if you decided to apply U.S. sales tax and use tax rules, you can’t enable tax recovery on expenses.</span></span> <span data-ttu-id="388cb-211">(Per aplicar l'impost de vendes dels EUA i utilitzar regles d'impostos, definiu l'opció **Aplica les regles dels impostos de vendes** a **Sí**.)</span><span class="sxs-lookup"><span data-stu-id="388cb-211">(To apply U.S. sales tax and use tax rules, set the **Apply sales tax taxations rules** option to **Yes**.)</span></span>

## <a name="policies"></a><span data-ttu-id="388cb-212">Normes</span><span class="sxs-lookup"><span data-stu-id="388cb-212">Policies</span></span>

<span data-ttu-id="388cb-213">Mitjançant la creació de normes d'informe de despeses, podeu ajudar a la vostra organització a estalviar temps i diners quan els empleats incorren despeses en el seu nom.</span><span class="sxs-lookup"><span data-stu-id="388cb-213">By creating expense report policies, you can help your organization save time and money when employees incur expenses on its behalf.</span></span> <span data-ttu-id="388cb-214">Les normes ajuden a garantir que els empleats es mantenen dins del pressupost, proporcionen tota la informació necessària i gasten diners només quan ho requereixen.</span><span class="sxs-lookup"><span data-stu-id="388cb-214">Policies help guarantee that employees stay in budget, provide all required information, and spend money only as they require it.</span></span> <span data-ttu-id="388cb-215">Heu de prendre les següents decisions per a cada norma d'informe de despeses i cada norma d'aprovació de l'informe de despeses que creeu.</span><span class="sxs-lookup"><span data-stu-id="388cb-215">You must make the following decisions for each expense report policy and each expense report approval policy that you create.</span></span>

<span data-ttu-id="388cb-216">**Decisions:**</span><span class="sxs-lookup"><span data-stu-id="388cb-216">**Decisions:**</span></span>

- <span data-ttu-id="388cb-217">Quin és el nom de la norma?</span><span class="sxs-lookup"><span data-stu-id="388cb-217">What is the name of the policy?</span></span>
- <span data-ttu-id="388cb-218">Per a què serveix la norma de despeses?</span><span class="sxs-lookup"><span data-stu-id="388cb-218">What is the expense policy for?</span></span>
- <span data-ttu-id="388cb-219">Si prèviament heu decidit permetre les despeses entre empreses, a quines empreses de la vostra organització s'aplicarà aquesta norma?</span><span class="sxs-lookup"><span data-stu-id="388cb-219">If you previously decided to enable intercompany expenses, which companies in your organization will this policy apply to?</span></span>
- <span data-ttu-id="388cb-220">Quan serà efectiva la norma?</span><span class="sxs-lookup"><span data-stu-id="388cb-220">When does the policy become effective?</span></span>
- <span data-ttu-id="388cb-221">Quan venç la norma?</span><span class="sxs-lookup"><span data-stu-id="388cb-221">When does the policy expire?</span></span>
- <span data-ttu-id="388cb-222">Quina és la regla de la norma?</span><span class="sxs-lookup"><span data-stu-id="388cb-222">What is the policy rule?</span></span>
- <span data-ttu-id="388cb-223">Quin és el resultat de la regla de la norma?</span><span class="sxs-lookup"><span data-stu-id="388cb-223">What is the outcome of the policy rule?</span></span>
