---
title: Facturació entre empreses
description: En aquest article es proporciona informació i exemples sobre la facturació entre empreses per als projectes.
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerInterCompany
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 94153
ms.assetid: 33e98da7-01c1-4369-923d-aa1c8326cb80
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d0385c796ca1ac02d6b8f66c04dad21bafe15ef8
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749439"
---
# <a name="intercompany-invoicing"></a><span data-ttu-id="08569-103">Facturació entre empreses</span><span class="sxs-lookup"><span data-stu-id="08569-103">Intercompany invoicing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="08569-104">En aquest article es proporciona informació i exemples sobre la facturació entre empreses per als projectes.</span><span class="sxs-lookup"><span data-stu-id="08569-104">This article provides information and examples about intercompany invoicing for projects.</span></span>

<span data-ttu-id="08569-105">La vostra organització pot tenir diverses divisions, filials i altres entitats jurídiques que es transfereixen productes i serveis entre si per als projectes.</span><span class="sxs-lookup"><span data-stu-id="08569-105">Your organization might have multiple divisions, subsidiaries, and other legal entities that transfer products and services to each other for projects.</span></span> <span data-ttu-id="08569-106">L'entitat jurídica que proporciona el servei o producte s'anomena *entitat jurídica prestadora* i l'entitat jurídica que rep el servei o producte s'anomena *entitat jurídica prestatària*.</span><span class="sxs-lookup"><span data-stu-id="08569-106">The legal entity that provides the service or product is called the *lending legal entity*, and the legal entity that receives the service or product is called the *borrowing legal entity*.</span></span> 

<span data-ttu-id="08569-107">A la il·lustració següent es mostra un escenari típic on hi ha dues entitats jurídiques, SI FR (l'entitat legal prestatària) i SI USA (l'entitat legal prestadora), que comparteixen recursos per lliurar un projecte per al client A. Per a aquest escenari, SI FR es contracta per lliurar el treball al client A.</span><span class="sxs-lookup"><span data-stu-id="08569-107">The following illustration shows a typical scenario where two legal entities, SI FR (the borrowing legal entity) and SI USA (the lending legal entity) share resources to deliver a project for customer A. For this scenario, SI FR is contracted to deliver the work to customer A.</span></span> 

<span data-ttu-id="08569-108">[![Exemple de facturació entre empreses](./media/interco.invoicing-01.jpg)](./media/interco.invoicing-01.jpg)</span><span class="sxs-lookup"><span data-stu-id="08569-108">[![Intercompany invoicing example](./media/interco.invoicing-01.jpg)](./media/interco.invoicing-01.jpg)</span></span> 

<span data-ttu-id="08569-109">L'objectiu és fer que el control de costos, el reconeixement d'ingressos, els impostos i el preu de transferència per a les transaccions de projecte entre empreses siguin més flexibles i potents.</span><span class="sxs-lookup"><span data-stu-id="08569-109">The goal is to make cost control, revenue recognition, taxes, and transfer price for intercompany project transactions more flexible and powerful.</span></span> <span data-ttu-id="08569-110">A més, es proporcionen les capacitats següents:</span><span class="sxs-lookup"><span data-stu-id="08569-110">In addition, the following capabilities are provided:</span></span>

-   <span data-ttu-id="08569-111">Crear factures de clients en un projecte d'una entitat legal prestatària mitjançant l'ús de fulls horaris, despeses i factures de proveïdors entre empreses en una entitat legal prestadora.</span><span class="sxs-lookup"><span data-stu-id="08569-111">Create customer invoices against a project in a borrowing legal entity by using intercompany timesheets, expenses, and vendor invoices in a lending legal entity.</span></span>
-   <span data-ttu-id="08569-112">Donar suport als càlculs fiscals i els costos indirectes.</span><span class="sxs-lookup"><span data-stu-id="08569-112">Support tax calculations and indirect costs.</span></span>
-   <span data-ttu-id="08569-113">Ajornar el reconeixement d'ingressos en una entitat legal prestadora i quan una entitat legal prestatària hauria de reconèixer el cost.</span><span class="sxs-lookup"><span data-stu-id="08569-113">Defer revenue recognition in a lending legal entity and when a borrowing legal entity should recognize the cost.</span></span>
-   <span data-ttu-id="08569-114">Acumular ingressos de treball en curs (WIP) a l'entitat legal prestadora.</span><span class="sxs-lookup"><span data-stu-id="08569-114">Accrue work in process (WIP) revenue in the lending legal entity.</span></span>
-   <span data-ttu-id="08569-115">Definiu els preus de transferència, que es poden basar en diversos models de preu.</span><span class="sxs-lookup"><span data-stu-id="08569-115">Set transfer prices that can be based on various pricing models.</span></span> <span data-ttu-id="08569-116">A continuació trobareu alguns exemples:</span><span class="sxs-lookup"><span data-stu-id="08569-116">Here are some examples:</span></span>
    -   <span data-ttu-id="08569-117">**Quantitat**: la quantitat que introduïu al camp **Preu** és el cost real per quantitat o unitat.</span><span class="sxs-lookup"><span data-stu-id="08569-117">**Quantity** – The amount that you enter in the **Pricing** field is the actual cost per quantity or unit.</span></span>
    -   <span data-ttu-id="08569-118">**Import dels càrrecs**: el preu i cost per transacció més la quantitat de despeses que introduïu al camp **Preu**.</span><span class="sxs-lookup"><span data-stu-id="08569-118">**Charges amount** – The price/cost per transaction plus the charges amount that you enter in the **Pricing** field.</span></span>
    -   <span data-ttu-id="08569-119">**Percentatge de càrrecs**: el preu de la transferència és el preu i el cost per transacció multiplicat pel percentatge de càrrecs que introduïu en el camp **Preus**.</span><span class="sxs-lookup"><span data-stu-id="08569-119">**Charges percentage** – The transfer price is the price/cost per transaction multiplied by the charges percentage that you enter in the **Pricing** field.</span></span>
    -   <span data-ttu-id="08569-120">**Percentatge del preu de vendes**: percentatge del preu de vendes que es transfereix a l'entitat jurídica prestadora.</span><span class="sxs-lookup"><span data-stu-id="08569-120">**Percentage of sales price** – The percentage of the sales price that is transferred to the lending legal entity.</span></span>
    -   <span data-ttu-id="08569-121">**Import per sota de preu de vendes** import que l'entitat legal prestatària reté dels preus de les vendes abans de la transferència a l'entitat legal prestadora.</span><span class="sxs-lookup"><span data-stu-id="08569-121">**Amount below sales price** – The amount that the borrowing legal entity holds back from the sales prices before transfer to the lending legal entity.</span></span>
    -   <span data-ttu-id="08569-122">**Relació de contribució**: el nombre que introduïu en el camp **Preu** és la relació de contribució, que s'expressa com a percentatge del preu de vendes.</span><span class="sxs-lookup"><span data-stu-id="08569-122">**Contribution ratio** – The number that you enter in the **Pricing** field is the contribution ratio, which is expressed as a percentage of the sales price.</span></span>

## <a name="example-1-set-up-parameters-for-intercompany-invoicing"></a><span data-ttu-id="08569-123">Exemple 1: configuració dels paràmetres per a la facturació entre empreses</span><span class="sxs-lookup"><span data-stu-id="08569-123">Example 1: Set up parameters for intercompany invoicing</span></span>
<span data-ttu-id="08569-124">En aquest exemple, USSI és una entitat legal prestadora i els seus recursos informen del temps per a l'entitat legal prestatària, FRSI, propietària del contracte amb el client final.</span><span class="sxs-lookup"><span data-stu-id="08569-124">In this example, USSI is a lending legal entity, and its resources are reporting time against the borrowing legal entity, FRSI, which owns the contract with the end customer.</span></span> <span data-ttu-id="08569-125">Les hores i despeses que els empleats d'USSI informen es poden incloure a la factura del projecte que genera FRSI.</span><span class="sxs-lookup"><span data-stu-id="08569-125">Hours and expenses that USSI employees report can be included in the project invoice that FRSI generates.</span></span> <span data-ttu-id="08569-126">A més, hi ha un tercer origen de transaccions que es poden originar a partir de l'entitat legal prestadora (USSI en aquest exemple) quan proporciona serveis de proveïdors compartits a les filials (com ara FRSI) i, a continuació, passa aquests costos en projectes dins d'aquestes filials.</span><span class="sxs-lookup"><span data-stu-id="08569-126">In addition, there is a third source of transactions that can originate from the lending legal entity (USSI in this example) when it provides shared vendors services to subsidiaries (such as FRSI) and then passes on those costs to projects within those subsidiaries.</span></span> <span data-ttu-id="08569-127">Tots els documents de factures i els càlculs d'impostos coincidents els completa Finance.</span><span class="sxs-lookup"><span data-stu-id="08569-127">All matching invoice documents and tax calculations are completed by Finance.</span></span> 

<span data-ttu-id="08569-128">Per a aquest exemple, FRSI ha de ser client a l'entitat jurídica USSI i USSI ha de ser un proveïdor de l'entitat jurídica FRSI.</span><span class="sxs-lookup"><span data-stu-id="08569-128">For this example, FRSI must be a customer in the USSI legal entity, and USSI must be a vendor in the FRSI legal entity.</span></span> <span data-ttu-id="08569-129">A continuació, podeu configurar una relació entre empreses entre les dues entitats jurídiques.</span><span class="sxs-lookup"><span data-stu-id="08569-129">You can then set up an intercompany relationship between the two legal entities.</span></span> <span data-ttu-id="08569-130">El procediment següent mostra com configurar els paràmetres per tal que ambdues entitats jurídiques puguin participar en la facturació entre empreses.</span><span class="sxs-lookup"><span data-stu-id="08569-130">The following procedure shows how to set up the parameters so that both legal entities can participate in intercompany invoicing.</span></span>

1. <span data-ttu-id="08569-131">Configurar FRSI com a client a l'entitat jurídica USSI i configurar USSI com a proveïdor a l'entitat jurídica FRSI.</span><span class="sxs-lookup"><span data-stu-id="08569-131">Set up FRSI as a customer in the USSI legal entity, and set up USSI as a vendor in the FRSI legal entity.</span></span> <span data-ttu-id="08569-132">Hi ha tres punts d'entrada per als passos necessaris per a aquesta tasca.</span><span class="sxs-lookup"><span data-stu-id="08569-132">There are three entry points for the steps that are required for this task.</span></span>

   | <span data-ttu-id="08569-133">Pas</span><span class="sxs-lookup"><span data-stu-id="08569-133">Step</span></span> |                                                       <span data-ttu-id="08569-134">Punt d'entrada</span><span class="sxs-lookup"><span data-stu-id="08569-134">Entry point</span></span>                                                        |                                                                                                                                                                                               <span data-ttu-id="08569-135">Descripció</span><span class="sxs-lookup"><span data-stu-id="08569-135">Description</span></span>                                                                                                                                                                                               |
   |------|--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |  <span data-ttu-id="08569-136">A</span><span class="sxs-lookup"><span data-stu-id="08569-136">A</span></span>   | <span data-ttu-id="08569-137">A USSI, feu clic a <strong>Compte a cobrar</strong> &gt; <strong>Clients</strong> &gt; <strong>Tots els clients</strong>.</span><span class="sxs-lookup"><span data-stu-id="08569-137">In USSI, click <strong>Accounts receivable</strong> &gt; <strong>Customers</strong> &gt; <strong>All customers</strong>.</span></span> |                                                                                                                                                                  <span data-ttu-id="08569-138">Creeu un registre de client nou per a FRSI i seleccioneu el grup de clients.</span><span class="sxs-lookup"><span data-stu-id="08569-138">Create a new customer record for FRSI, and select the customer group.</span></span>                                                                                                                                                                  |
   |  <span data-ttu-id="08569-139">N</span><span class="sxs-lookup"><span data-stu-id="08569-139">B</span></span>   |    <span data-ttu-id="08569-140">A FRSI, feu clic a <strong>Compte a pagar</strong> &gt; <strong>Proveïdors</strong> &gt; <strong>Tots els proveïdors</strong>.</span><span class="sxs-lookup"><span data-stu-id="08569-140">In FRSI, click <strong>Accounts payable</strong> &gt; <strong>Vendors</strong> &gt; <strong>All vendors</strong>.</span></span>     |                                                                                                                                                                    <span data-ttu-id="08569-141">Creeu un registre de proveïdor nou per a USSI i seleccioneu el grup de proveïdors.</span><span class="sxs-lookup"><span data-stu-id="08569-141">Create a new vendor record for USSI, and select the vendor group.</span></span>                                                                                                                                                                    |
   |  <span data-ttu-id="08569-142">C</span><span class="sxs-lookup"><span data-stu-id="08569-142">C</span></span>   |                                  <span data-ttu-id="08569-143">A FRSI, obriu el registre del proveïdor que acabeu de crear.</span><span class="sxs-lookup"><span data-stu-id="08569-143">In FRSI, open the vendor record that you just created.</span></span>                                  | <span data-ttu-id="08569-144">A la subfinestra d'acció, a la pestanya <strong>General</strong>, al grup <strong>Configura</strong>, feu clic a <strong>Entre empreses</strong>.</span><span class="sxs-lookup"><span data-stu-id="08569-144">On the Action Pane, on the <strong>General</strong> tab, in the <strong>Set up</strong> group, click <strong>Intercompany</strong>.</span></span> <span data-ttu-id="08569-145">A la pàgina <strong>Entre empreses</strong>, a la pestanya <strong>Relació comercial</strong>, definiu el control lliscant <strong>Actiu</strong> a <strong>Sí</strong>.</span><span class="sxs-lookup"><span data-stu-id="08569-145">On the <strong>Intercompany</strong> page, on the <strong>Trading relationship</strong> tab, set the <strong>Active</strong> slider to <strong>Yes</strong>.</span></span> <span data-ttu-id="08569-146">Al camp <strong>Empresa del client</strong>, seleccioneu el registre de client que heu creat en el pas A.</span><span class="sxs-lookup"><span data-stu-id="08569-146">In the <strong>Customer company</strong> field, select the customer record that you created in step A.</span></span> |


2. <span data-ttu-id="08569-147">Feu clic a **Administració de projectes i comptabilitat** &gt; **Configuració** &gt; **Paràmetres d'administració de projectes i comptabilitat** i, a continuació, feu clic a la pestanya **Entre empreses** . La manera de configurar els paràmetres depèn de si sou l'entitat jurídica prestatària o l'entitat jurídica prestadora.</span><span class="sxs-lookup"><span data-stu-id="08569-147">Click **Project management and accounting** &gt; **Setup** &gt; **Project management accounting parameters**, and then click the **Intercompany** tab. The way that you set up the parameters depends on whether you're the borrowing legal entity or the lending legal entity.</span></span>
   -   <span data-ttu-id="08569-148">Si sou l'entitat jurídica prestatària, seleccioneu la categoria de contractació que s'ha d'utilitzar per assignar les factures dels proveïdors, que es generen automàticament.</span><span class="sxs-lookup"><span data-stu-id="08569-148">If you're the borrowing legal entity, select the procurement category that should be used to match the vendor invoices, which are automatically generated.</span></span>
   -   <span data-ttu-id="08569-149">Si sou l'entitat jurídica prestadora, per a cada entitat prestatària, seleccioneu una categoria de projecte per defecte per a cada tipus de transacció.</span><span class="sxs-lookup"><span data-stu-id="08569-149">If you're the lending legal entity, for each borrowing entity, select a default project category for each transaction type.</span></span> <span data-ttu-id="08569-150">Les categories de projecte s'utilitzen per a la configuració tributària quan la categoria facturada a les transaccions entre empreses només existeix a l'entitat jurídica prestatària.</span><span class="sxs-lookup"><span data-stu-id="08569-150">Project categories are used for tax configuration when the invoiced category in intercompany transactions exists only in the borrowing legal entity.</span></span> <span data-ttu-id="08569-151">Podeu triar acumular els ingressos per a les transaccions entre empreses.</span><span class="sxs-lookup"><span data-stu-id="08569-151">You can choose to accrue revenue for intercompany transactions.</span></span> <span data-ttu-id="08569-152">Aquesta acumulació es fa quan es publiquen les transaccions i, a continuació, s'inverteix quan es comptabilitza la factura entre empreses.</span><span class="sxs-lookup"><span data-stu-id="08569-152">This accrual is done when the transactions are posted, and it's then reversed when the intercompany invoice is posted.</span></span>

3. <span data-ttu-id="08569-153">Feu clic a **Administració de projectes i comptabilitat** &gt; **Configuració** &gt; **Preus** &gt; **Preu de transferència**.</span><span class="sxs-lookup"><span data-stu-id="08569-153">Click **Project management and accounting** &gt; **Setup** &gt; **Prices** &gt; **Transfer price**.</span></span>
4. <span data-ttu-id="08569-154">Seleccioneu una moneda, un tipus de transacció i un model de preu de transferència.</span><span class="sxs-lookup"><span data-stu-id="08569-154">Select a currency, transaction type, and transfer price model.</span></span> <span data-ttu-id="08569-155">La moneda que s'utilitza a la factura és la moneda configurada al registre de client per a l'entitat jurídica prestatària a l'entitat jurídica prestadora.</span><span class="sxs-lookup"><span data-stu-id="08569-155">The currency that is used on the invoice is the currency that is configured in the customer record for the borrowing legal entity in the lending legal entity.</span></span> <span data-ttu-id="08569-156">La moneda s'utilitza per fer coincidir les entrades de la taula de preus de transferència.</span><span class="sxs-lookup"><span data-stu-id="08569-156">The currency is used to match entries in the transfer price table.</span></span>
5. <span data-ttu-id="08569-157">Feu clic a **Llibre major general** &gt; **Configuració de la comptabilització** &gt; **Comptabilitat entre empreses** i configureu una relació per a USSI i FRSI.</span><span class="sxs-lookup"><span data-stu-id="08569-157">Click **General ledger** &gt; **Posting setup** &gt; **Intercompany accounting**, and set up a relationship for USSI and FRSI.</span></span>

## <a name="example-2-create-and-post-an-intercompany-timesheet"></a><span data-ttu-id="08569-158">Exemple 2: creació i publicació d'un full d'hores entre empreses</span><span class="sxs-lookup"><span data-stu-id="08569-158">Example 2: Create and post an intercompany timesheet</span></span>
<span data-ttu-id="08569-159">USSI, l'entitat jurídica prestadora, ha de crear i comptabilitzar el full d'hores per a un projecte de FRSI, l'entitat jurídica prestatària.</span><span class="sxs-lookup"><span data-stu-id="08569-159">USSI, the lending legal entity, must create and post the timesheet for a project from FRSI, the borrowing legal entity.</span></span> <span data-ttu-id="08569-160">Hi ha dos punts d'entrada per als passos necessaris per a aquesta tasca.</span><span class="sxs-lookup"><span data-stu-id="08569-160">There are two entry points for the steps that are required for this task.</span></span>

| <span data-ttu-id="08569-161">Pas</span><span class="sxs-lookup"><span data-stu-id="08569-161">Step</span></span> | <span data-ttu-id="08569-162">Punt d'entrada</span><span class="sxs-lookup"><span data-stu-id="08569-162">Entry point</span></span>                                                                       | <span data-ttu-id="08569-163">Descripció</span><span class="sxs-lookup"><span data-stu-id="08569-163">Description</span></span>                                                                                                                                                                                       |
|------|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08569-164">A</span><span class="sxs-lookup"><span data-stu-id="08569-164">A</span></span>    | <span data-ttu-id="08569-165">**Administració de projectes i comptabilitat** &gt; **Fulls d'hores** &gt; **Tots els fulls d'hores**</span><span class="sxs-lookup"><span data-stu-id="08569-165">**Project management and accounting** &gt; **Timesheets** &gt; **All timesheets**</span></span> | <span data-ttu-id="08569-166">Creeu un full d'hores nou.</span><span class="sxs-lookup"><span data-stu-id="08569-166">Create a new timesheet.</span></span> <span data-ttu-id="08569-167">A la línia del full d'hores, al camp **Entitat jurídica**, seleccioneu **FRSI**.</span><span class="sxs-lookup"><span data-stu-id="08569-167">On the timesheet line, in the **Legal entity** field, select **FRSI**.</span></span> <span data-ttu-id="08569-168">Al camp **ID del projecte**, seleccioneu el projecte a FRSI.</span><span class="sxs-lookup"><span data-stu-id="08569-168">In the **Project ID** field, select the project in FRSI.</span></span> <span data-ttu-id="08569-169">Introduïu les hores per a cada dia de la setmana.</span><span class="sxs-lookup"><span data-stu-id="08569-169">Enter the hours for each day of the week.</span></span> |
| <span data-ttu-id="08569-170">N</span><span class="sxs-lookup"><span data-stu-id="08569-170">B</span></span>    | <span data-ttu-id="08569-171">Pàgina **Full d'hores**</span><span class="sxs-lookup"><span data-stu-id="08569-171">**Timesheet** page</span></span>                                                                | <span data-ttu-id="08569-172">Quan el flux de treball s'executi, publiqueu el full d'hores i anoteu el número del val.</span><span class="sxs-lookup"><span data-stu-id="08569-172">After the workflow runs, post the timesheet, and make a note of the voucher number.</span></span>                                                                                                               |

## <a name="example-3-create-and-post-an-intercompany-vendor-invoice"></a><span data-ttu-id="08569-173">Exemple 3: creació i publicació d'una factura a un proveïdor entre empreses</span><span class="sxs-lookup"><span data-stu-id="08569-173">Example 3: Create and post an intercompany vendor invoice</span></span>
<span data-ttu-id="08569-174">USSI, l'entitat jurídica prestadora, ha de crear i comptabilitzar la factura per a un proveïdor entre empreses per a un projecte de FRSI, l'entitat jurídica prestatària.</span><span class="sxs-lookup"><span data-stu-id="08569-174">USSI, the lending legal entity, must create and post the intercompany vendor invoice for a project from FRSI, the borrowing legal entity.</span></span> <span data-ttu-id="08569-175">Aquesta factura de proveïdor representa el treball i les despeses externalitzats que han realitzat els proveïdors pagats per USSI.</span><span class="sxs-lookup"><span data-stu-id="08569-175">This vendor invoice represents the outsourced labor and expense that were performed by vendors that are paid by USSI.</span></span> <span data-ttu-id="08569-176">Hi ha dos punts d'entrada per als passos necessaris per a aquesta tasca.</span><span class="sxs-lookup"><span data-stu-id="08569-176">There are two entry points for the steps that are required for this task.</span></span>

| <span data-ttu-id="08569-177">Pas</span><span class="sxs-lookup"><span data-stu-id="08569-177">Step</span></span> | <span data-ttu-id="08569-178">Punt d'entrada</span><span class="sxs-lookup"><span data-stu-id="08569-178">Entry point</span></span>                                                                                      | <span data-ttu-id="08569-179">Descripció</span><span class="sxs-lookup"><span data-stu-id="08569-179">Description</span></span>                                                                                                                                                                                                                                                                          |
|------|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08569-180">A</span><span class="sxs-lookup"><span data-stu-id="08569-180">A</span></span>    | <span data-ttu-id="08569-181">**Comptes a pagar** &gt; **Factures** &gt; **Factures de proveïdors obertes** &gt; **Nova factura de proveïdor**</span><span class="sxs-lookup"><span data-stu-id="08569-181">**Accounts payable** &gt; **Invoices** &gt; **Open vendor invoices** &gt; **New vendor invoice**</span></span> | <span data-ttu-id="08569-182">Creeu una factura de proveïdor nova i introduïu els serveis que s'han fet en el projecte de FRSI.</span><span class="sxs-lookup"><span data-stu-id="08569-182">Create a new vendor invoice, and enter the services that were procured on behalf of FRSI's project.</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="08569-183">N</span><span class="sxs-lookup"><span data-stu-id="08569-183">B</span></span>    | <span data-ttu-id="08569-184">La pàgina **Factura de proveïdor**</span><span class="sxs-lookup"><span data-stu-id="08569-184">The **Vendor invoice** page</span></span>                                                                      | <span data-ttu-id="08569-185">Introduïu les línies que representen els serveis externalitzats en nom de FRSI.</span><span class="sxs-lookup"><span data-stu-id="08569-185">Enter lines that represent the outsourced services on behalf of FRSI.</span></span> <span data-ttu-id="08569-186">A FastTab **Detalls de la línia**, a la pestanya **Projecte** de la línia de factura, al camp **Empresa del projecte**, introduïu **FRSI**.</span><span class="sxs-lookup"><span data-stu-id="08569-186">On the **Line details** FastTab, on the **Project** tab for the invoice line, in the **Project company** field, enter **FRSI**.</span></span> <span data-ttu-id="08569-187">Introduïu el projecte i la informació corresponent.</span><span class="sxs-lookup"><span data-stu-id="08569-187">Enter the project and corresponding information.</span></span> <span data-ttu-id="08569-188">A continuació, comptabilitzeu la factura del proveïdor.</span><span class="sxs-lookup"><span data-stu-id="08569-188">Then post the vendor invoice.</span></span> |

## <a name="example-4-create-and-post-the-intercompany-invoice"></a><span data-ttu-id="08569-189">Exemple 4: creació i publicació de la factura entre empreses</span><span class="sxs-lookup"><span data-stu-id="08569-189">Example 4: Create and post the intercompany invoice</span></span>
<span data-ttu-id="08569-190">USSI, l'entitat jurídica prestadora, ha de crear i publicar la factura entre empreses.</span><span class="sxs-lookup"><span data-stu-id="08569-190">USSI, the lending legal entity, must create and post the intercompany invoice.</span></span> <span data-ttu-id="08569-191">Hi ha dos punts d'entrada per als passos necessaris per a aquesta tasca.</span><span class="sxs-lookup"><span data-stu-id="08569-191">There are two entry points for the steps that are required for this task.</span></span>

| <span data-ttu-id="08569-192">Pas</span><span class="sxs-lookup"><span data-stu-id="08569-192">Step</span></span> | <span data-ttu-id="08569-193">Punt d'entrada</span><span class="sxs-lookup"><span data-stu-id="08569-193">Entry point</span></span>                                                                                             | <span data-ttu-id="08569-194">Descripció</span><span class="sxs-lookup"><span data-stu-id="08569-194">Description</span></span>                                                                                                                                      |
|------|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08569-195">A</span><span class="sxs-lookup"><span data-stu-id="08569-195">A</span></span>    | <span data-ttu-id="08569-196">**Administració de projectes i comptabilitat** &gt; **Factures del projecte** &gt; **Factura de client entre empreses**</span><span class="sxs-lookup"><span data-stu-id="08569-196">**Project management and accounting** &gt; **Project invoices** &gt; **Intercompany customer invoice**</span></span>  | <span data-ttu-id="08569-197">Feu clic a **Nou** per obrir la pàgina **Crea una factura entre empreses**.</span><span class="sxs-lookup"><span data-stu-id="08569-197">Click **New** to open the **Create intercompany invoice** page.</span></span>                                                                                  |
| <span data-ttu-id="08569-198">N</span><span class="sxs-lookup"><span data-stu-id="08569-198">B</span></span>    | <span data-ttu-id="08569-199">**Administració de projectes i comptabilitat** &gt; **Factures del projecte** &gt; **Factures de client entre empreses**</span><span class="sxs-lookup"><span data-stu-id="08569-199">**Project management and accounting** &gt; **Project invoices** &gt; **Intercompany customer invoices**</span></span> | <span data-ttu-id="08569-200">A la pàgina **Crea una factura entre empreses**, introduïu l'entitat jurídica, especifiqueu la transacció que s'ha d'incloure i, a continuació, feu clic a **Cerca**.</span><span class="sxs-lookup"><span data-stu-id="08569-200">On the **Create intercompany invoice** page, enter the legal entity, specify the transaction that should be included, and then click **Search**.</span></span> |
| <span data-ttu-id="08569-201">C</span><span class="sxs-lookup"><span data-stu-id="08569-201">C</span></span>    | <span data-ttu-id="08569-202">**Administració de projectes i comptabilitat** &gt; **Factures del projecte** &gt; **Factures de client entre empreses**</span><span class="sxs-lookup"><span data-stu-id="08569-202">**Project management and accounting** &gt; **Project invoices** &gt; **Intercompany customer invoices**</span></span> | <span data-ttu-id="08569-203">Seleccioneu les transaccions que voleu facturar o feu clic a **Selecciona-ho tot** per facturar totes les transaccions a la llista i, a continuació, feu clic a **D'acord**.</span><span class="sxs-lookup"><span data-stu-id="08569-203">Select the transactions to invoice, or click **Select all** to invoice all the transactions in the list, and then click **OK**.</span></span>                  |
| <span data-ttu-id="08569-204">D</span><span class="sxs-lookup"><span data-stu-id="08569-204">D</span></span>    | <span data-ttu-id="08569-205">La pàgina **Factura entre empreses**</span><span class="sxs-lookup"><span data-stu-id="08569-205">The **Intercompany invoice** page</span></span>                                                                       | <span data-ttu-id="08569-206">Es mostra la proposta de factura de client entre empreses.</span><span class="sxs-lookup"><span data-stu-id="08569-206">The intercompany customer invoice proposal is shown.</span></span>                                                                                             |
| <span data-ttu-id="08569-207">E</span><span class="sxs-lookup"><span data-stu-id="08569-207">E</span></span>    | <span data-ttu-id="08569-208">La pàgina **Factura entre empreses**</span><span class="sxs-lookup"><span data-stu-id="08569-208">The **Intercompany invoice** page</span></span>                                                                       | <span data-ttu-id="08569-209">Feu clic a **Comptabilitza**.</span><span class="sxs-lookup"><span data-stu-id="08569-209">Click **Post**.</span></span>                                                                                                                                  |

## <a name="example-5-post-the-vendor-invoice-and-invoice-the-customer"></a><span data-ttu-id="08569-210">Exemple 5: comptabilització de la factura del proveïdor i facturació al client</span><span class="sxs-lookup"><span data-stu-id="08569-210">Example 5: Post the vendor invoice and invoice the customer</span></span>
<span data-ttu-id="08569-211">Quan l'entitat jurídica prestadora, USSI, comptabilitza la factura del client entre empreses, es crea una factura de proveïdor pendent coincident a l'entitat jurídica prestatària, FRSI.</span><span class="sxs-lookup"><span data-stu-id="08569-211">When the lending legal entity, USSI, posts the intercompany customer invoice, a matching pending vendor invoice is created in the borrowing legal entity, FRSI.</span></span> <span data-ttu-id="08569-212">Un cop comptabilitzada aquesta factura del proveïdor, FRSI també factura al client del projecte les hores que ha introduït USSI.</span><span class="sxs-lookup"><span data-stu-id="08569-212">After this vendor invoice is posted, FRSI also invoices the project customer for the hours that USSI entered.</span></span> <span data-ttu-id="08569-213">Hi ha tres punts d'entrada per als passos necessaris per a aquesta tasca.</span><span class="sxs-lookup"><span data-stu-id="08569-213">There are three entry points for the steps that are required for this task.</span></span>

| <span data-ttu-id="08569-214">Pas</span><span class="sxs-lookup"><span data-stu-id="08569-214">Step</span></span> | <span data-ttu-id="08569-215">Punt d'entrada</span><span class="sxs-lookup"><span data-stu-id="08569-215">Entry point</span></span>                                                                                        | <span data-ttu-id="08569-216">Descripció</span><span class="sxs-lookup"><span data-stu-id="08569-216">Description</span></span>                                                                                                             |
|------|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08569-217">A</span><span class="sxs-lookup"><span data-stu-id="08569-217">A</span></span>    | <span data-ttu-id="08569-218">**Comptes a pagar** &gt; **Factures** &gt; **Factures de proveïdors pendents**</span><span class="sxs-lookup"><span data-stu-id="08569-218">**Accounts payable** &gt; **Invoices** &gt; **Pending vendor invoices**</span></span>                            | <span data-ttu-id="08569-219">Reviseu la factura per comprovar que s'inclouen els valors del full d'hora i, a continuació, comptabilitzeu la factura del proveïdor.</span><span class="sxs-lookup"><span data-stu-id="08569-219">Review the invoice to verify that the timesheet values are included, and then post the vendor invoice.</span></span>                  |
| <span data-ttu-id="08569-220">N</span><span class="sxs-lookup"><span data-stu-id="08569-220">B</span></span>    | <span data-ttu-id="08569-221">**Administració de projectes i comptabilitat** &gt; **Factures del projecte** &gt; **Propostes de factura del projecte**</span><span class="sxs-lookup"><span data-stu-id="08569-221">**Project management and accounting** &gt; **Project invoices** &gt; **Project invoice proposals**</span></span> | <span data-ttu-id="08569-222">Creeu una factura de projecte nova per al projecte i verifiqueu que es mostrin les transaccions d'hora que s'han comptabilitzat.</span><span class="sxs-lookup"><span data-stu-id="08569-222">Create a new project invoice for the project, and verify that the hour transactions that were posted appear.</span></span>            |
| <span data-ttu-id="08569-223">C</span><span class="sxs-lookup"><span data-stu-id="08569-223">C</span></span>    | <span data-ttu-id="08569-224">La pàgina **Factura del projecte**</span><span class="sxs-lookup"><span data-stu-id="08569-224">The **Project invoice** page</span></span>                                                                       | <span data-ttu-id="08569-225">Seleccioneu la factura del projecte i, a continuació, feu clic a **Visualitza els detalls** per revisar l'import del cost i de les vendes.</span><span class="sxs-lookup"><span data-stu-id="08569-225">Select the project invoice, and then click **View details** to review the cost and sales amount.</span></span> <span data-ttu-id="08569-226">A continuació, comptabilitzeu la factura.</span><span class="sxs-lookup"><span data-stu-id="08569-226">Then post the invoice.</span></span> |


<span data-ttu-id="08569-227">Per obtenir més informació, vegeu [Configurar la facturació del projecte entre empreses](tasks/configure-intercompany-project-invoicing.md).</span><span class="sxs-lookup"><span data-stu-id="08569-227">For more information, see [Configure intercompany project invoicing](tasks/configure-intercompany-project-invoicing.md).</span></span>

