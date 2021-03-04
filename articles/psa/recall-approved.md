---
title: Recuperar entrades de temps o de despeses aprovades
description: En aquest tema es proporciona informació sobre com recuperar una transacció de despesa i temps de projecte aprovada anteriorment.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom: ''
ms.author: rumant
ms.date: 03/08/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: f9bb25ac9ef7b400063c5f958311e475de6f6506
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147821"
---
# <a name="recall-approved-time-or-expense-entries"></a><span data-ttu-id="f7303-103">Recuperar entrades de temps o de despeses aprovades</span><span class="sxs-lookup"><span data-stu-id="f7303-103">Recall approved time or expense entries</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="f7303-104">Un membre d'un equip del projecte o una altra persona que presenti una entrada de temps o de despesa, pot recuperar l'entrada de temps o despesa després d'haver estat aprovada.</span><span class="sxs-lookup"><span data-stu-id="f7303-104">A project team member or an other person who submits a time or expense entry can recall that time or expense entry after it has been approved.</span></span> <span data-ttu-id="f7303-105">El procés de recuperació d'una entrada de temps o de despesa té dos passos:</span><span class="sxs-lookup"><span data-stu-id="f7303-105">The process for recalling an approved time or expense entry has two steps:</span></span>

1. <span data-ttu-id="f7303-106">Un remitent sol·licita una recuperació.</span><span class="sxs-lookup"><span data-stu-id="f7303-106">A submitter requests a recall.</span></span>
2. <span data-ttu-id="f7303-107">Un aprovador aprova la recuperació.</span><span class="sxs-lookup"><span data-stu-id="f7303-107">An approver approves the recall.</span></span>

## <a name="request-a-recall"></a><span data-ttu-id="f7303-108">Sol·licitar una recuperació</span><span class="sxs-lookup"><span data-stu-id="f7303-108">Request a recall</span></span>

<span data-ttu-id="f7303-109">Seguiu aquests passos per sol·licitar la recuperació d'una entrada de temps o de despesa aprovada.</span><span class="sxs-lookup"><span data-stu-id="f7303-109">Follow these steps to request a recall of an approved time or expense entry.</span></span>

1. <span data-ttu-id="f7303-110">Per a les entrades de temps, aneu a **Projectes** \> **El meu treball** \> **Entrada de temps**.</span><span class="sxs-lookup"><span data-stu-id="f7303-110">For time entries, go to **Projects** \> **My Work** \> **Time Entry**.</span></span>

    <span data-ttu-id="f7303-111">-o bé-</span><span class="sxs-lookup"><span data-stu-id="f7303-111">–or–</span></span>

    <span data-ttu-id="f7303-112">Per a les entrades de despeses, aneu a **Projectes** \> **El meu treball** \> **Despeses**.</span><span class="sxs-lookup"><span data-stu-id="f7303-112">For expense entries, go to **Projects** \> **My Work** \> **Expenses**.</span></span>

2. <span data-ttu-id="f7303-113">Per a entrades de temps, seleccioneu totes les entrades de temps per a una combinació específica d'un projecte i una tasca.</span><span class="sxs-lookup"><span data-stu-id="f7303-113">For time entries, select all the time entries for a specific combination of a project and a task.</span></span> <span data-ttu-id="f7303-114">De manera alternativa, a la quadrícula, seleccioneu les cel·les individuals per al temps d'una data concreta per a un projecte concret.</span><span class="sxs-lookup"><span data-stu-id="f7303-114">Alternatively, in the grid, select the individual cells for time on a specific date for a specific project.</span></span>

    <span data-ttu-id="f7303-115">-o bé-</span><span class="sxs-lookup"><span data-stu-id="f7303-115">–or–</span></span>

    <span data-ttu-id="f7303-116">Per a les entrades de despeses, seleccioneu la fila de l'entrada de la despesa que voleu recuperar.</span><span class="sxs-lookup"><span data-stu-id="f7303-116">For expense entries, select the row for the expense entry to recall.</span></span>

3. <span data-ttu-id="f7303-117">Seleccioneu **Recupera**.</span><span class="sxs-lookup"><span data-stu-id="f7303-117">Select **Recall**.</span></span> <span data-ttu-id="f7303-118">Apareix un quadre de diàleg de confirmació.</span><span class="sxs-lookup"><span data-stu-id="f7303-118">A confirmation dialog box appears.</span></span> <span data-ttu-id="f7303-119">Si les entrades de temps i de despeses seleccionades ja estaven aprovades, se us demanarà que introduïu un motiu per a la recuperació.</span><span class="sxs-lookup"><span data-stu-id="f7303-119">If the selected time and expense entries were already approved, you're prompted to enter a reason for the recall.</span></span>
4. <span data-ttu-id="f7303-120">Introduïu un motiu per a la recuperació i, a continuació, seleccioneu **D'acord** per confirmar l'operació.</span><span class="sxs-lookup"><span data-stu-id="f7303-120">Enter a reason for the recall, and then select **OK** to confirm the operation.</span></span> <span data-ttu-id="f7303-121">El sistema envia a la persona que ha aprovat les entrades una sol·licitud per aprovar la recuperació.</span><span class="sxs-lookup"><span data-stu-id="f7303-121">The system sends the person who approved the entries a request to approve the recall.</span></span>

> [!NOTE]
> <span data-ttu-id="f7303-122">Tot i que les entrades de temps i de despeses aprovades es poden recuperar, si un temps o una despesa aprovada ja s'ha facturat al client, no es pot crear una sol·licitud de recuperació.</span><span class="sxs-lookup"><span data-stu-id="f7303-122">Although approved time and expense entries can be recalled, if an approved time or expense has already been invoiced to the customer, a recall request can't be created.</span></span> <span data-ttu-id="f7303-123">Un usuari que provi de crear una sol·licitud de recuperació rebrà un missatge que indica que el temps o la despesa no es poden recuperar perquè ja s'han facturat.</span><span class="sxs-lookup"><span data-stu-id="f7303-123">A user who tries to create a recall request will receive a message that states that the time or expense can't be recalled because it was already invoiced.</span></span>

## <a name="approve-or-reject-a-recall-request"></a><span data-ttu-id="f7303-124">Aprovar o rebutjar una sol·licitud de recuperació</span><span class="sxs-lookup"><span data-stu-id="f7303-124">Approve or reject a recall request</span></span>

<span data-ttu-id="f7303-125">Seguiu aquests passos per aprovar o rebutjar una sol·licitud de recuperació.</span><span class="sxs-lookup"><span data-stu-id="f7303-125">Follow these steps to approve or reject a recall request.</span></span>

1. <span data-ttu-id="f7303-126">Aneu a **Projectes** \> **El meu treball** \> **Aprovacions**.</span><span class="sxs-lookup"><span data-stu-id="f7303-126">Go to **Projects** \> **My Work** \> **Approvals**.</span></span>
2. <span data-ttu-id="f7303-127">A la pàgina de llista **Aprovacions**, canvieu la visualització a **Sol·licituds de recuperació pendents d'aprovació**.</span><span class="sxs-lookup"><span data-stu-id="f7303-127">On the **Approvals** list page, change the view to **Recall requests for approval**.</span></span> <span data-ttu-id="f7303-128">Es mostra una llista de sol·licituds de recuperació enviades.</span><span class="sxs-lookup"><span data-stu-id="f7303-128">A list of submitted recall requests is shown.</span></span>
3. <span data-ttu-id="f7303-129">Seleccioneu una o diverses entrades i, a continuació , seleccioneu **Aprova** o **Rebutja**.</span><span class="sxs-lookup"><span data-stu-id="f7303-129">Select one or more entries, and then select either **Approve** or **Reject**.</span></span>
4. <span data-ttu-id="f7303-130">Si heu seleccionat **Aprova**, rebreu un missatge d'advertiment que explica l'impacte de l'aprovació.</span><span class="sxs-lookup"><span data-stu-id="f7303-130">If you selected **Approve**, you receive a warning message that explains the impact of the approval.</span></span> <span data-ttu-id="f7303-131">Seleccioneu **D'acord** per confirmar l'operació.</span><span class="sxs-lookup"><span data-stu-id="f7303-131">Select **OK** to confirm the operation.</span></span> <span data-ttu-id="f7303-132">La sol·licitud de recuperació s'ha aprovat.</span><span class="sxs-lookup"><span data-stu-id="f7303-132">The recall request is approved.</span></span>

    <span data-ttu-id="f7303-133">-o bé-</span><span class="sxs-lookup"><span data-stu-id="f7303-133">–or–</span></span>

    <span data-ttu-id="f7303-134">Si heu seleccionat **Rebutja**, la sol·licitud de recuperació es rebutja.</span><span class="sxs-lookup"><span data-stu-id="f7303-134">If you selected **Reject**, the recall request is rejected.</span></span>

> [!NOTE]
> <span data-ttu-id="f7303-135">Com quan es demana una recuperació, quan s'aprova una recuperació, el sistema comprova si hi ha activitats de facturació a les entrades de temps o de despeses.</span><span class="sxs-lookup"><span data-stu-id="f7303-135">As when a recall is requested, when a recall is approved, the system checks for any invoicing activity on the time or expense entries.</span></span> <span data-ttu-id="f7303-136">Si una entrada ja s'ha facturat o si està en un esborrany de factura, l'aprovador rebrà un missatge d'error que indica que el temps o la despesa no es poden aprovar per a la recuperació, perquè ja s'han facturat.</span><span class="sxs-lookup"><span data-stu-id="f7303-136">If an entry was already invoiced, or if it's on a draft invoice, the approver will receive an error message that states that the time or expense can't be approved for recall, because it was already invoiced.</span></span>

## <a name="impact-of-a-recall-request"></a><span data-ttu-id="f7303-137">Impacte d'una sol·licitud de recuperació</span><span class="sxs-lookup"><span data-stu-id="f7303-137">Impact of a recall request</span></span>

<span data-ttu-id="f7303-138">Quan una aprovació es recupera, hi ha un impacte operacional i un impacte financer.</span><span class="sxs-lookup"><span data-stu-id="f7303-138">When an approval is recalled, there is both operational impact and financial impact.</span></span>

### <a name="operational-impact"></a><span data-ttu-id="f7303-139">Impacte operacional</span><span class="sxs-lookup"><span data-stu-id="f7303-139">Operational impact</span></span>

<span data-ttu-id="f7303-140">Si una sol·licitud de recuperació d'aprova, el registre d'aprovació es marca com a **Rebutjat**.</span><span class="sxs-lookup"><span data-stu-id="f7303-140">If a recall request is approved, the approval record is marked as **Rejected**.</span></span> <span data-ttu-id="f7303-141">L'estat de l'entrada es canvia a **Retornada** o **Rebutjada** en funció de si es tracta d'una entrada de temps o d'una entrada de despesa.</span><span class="sxs-lookup"><span data-stu-id="f7303-141">The status of the entry is changed to either **Returned** or **Rejected**, depending on whether it's a time entry or an expense entry.</span></span>

<span data-ttu-id="f7303-142">El membre del grup de projectes pot visualitzar les entrades, editar i tornar a enviar les entrades o suprimir les entrades del tot.</span><span class="sxs-lookup"><span data-stu-id="f7303-142">The project team member can view entries, edit and then resubmit entries, or delete entries entirely.</span></span>

<span data-ttu-id="f7303-143">Si es rebutja una sol·licitud de recuperació, l'estat de l'entrada continua sent **Aprovada** i l'entrada no es pot editar pel membre de l'equip del projecte o l'aprovador del projecte.</span><span class="sxs-lookup"><span data-stu-id="f7303-143">If a recall request is rejected, the status of the entry remains **Approved**, and the entry can't be edited by the project team member or the approver for the project.</span></span>

### <a name="financial-impact"></a><span data-ttu-id="f7303-144">Impacte financer</span><span class="sxs-lookup"><span data-stu-id="f7303-144">Financial impact</span></span>

<span data-ttu-id="f7303-145">Si s'aprova una sol·licitud de recuperació, els valors reals corresponents al cost i les vendes s'actualitzen de la següent manera:</span><span class="sxs-lookup"><span data-stu-id="f7303-145">If a recall request is approved, the corresponding actuals for cost and sales are updated in the following manner:</span></span>

- <span data-ttu-id="f7303-146">El camp **Estat d'ajustament** s'actualitza com a **Ajustat**.</span><span class="sxs-lookup"><span data-stu-id="f7303-146">The **Adjustment Status** field is updated to **Adjusted**.</span></span>
- <span data-ttu-id="f7303-147">El camp **Estat de facturació** s'actualitza com a **Cancel·lat**.</span><span class="sxs-lookup"><span data-stu-id="f7303-147">The **Billing Status** field is updated to **Canceled**.</span></span>

<span data-ttu-id="f7303-148">A continuació, les entrades d'inversió es creen a la taula Valors reals.</span><span class="sxs-lookup"><span data-stu-id="f7303-148">Next, reversal entries are created in the Actuals table.</span></span> <span data-ttu-id="f7303-149">Per crear entrades d'inversió, el sistema copia els valors de camp dels valors reals originals.</span><span class="sxs-lookup"><span data-stu-id="f7303-149">To create reversal entries, the system copies over the field values from the original actuals.</span></span> <span data-ttu-id="f7303-150">Els únics valors que no es copien són els valors de quantitat.</span><span class="sxs-lookup"><span data-stu-id="f7303-150">The only values that aren't copied over are the quantity values.</span></span> <span data-ttu-id="f7303-151">Aquests valors s'inverteixen en el seu lloc.</span><span class="sxs-lookup"><span data-stu-id="f7303-151">These values are reversed instead.</span></span> <span data-ttu-id="f7303-152">Els valors reals invertits es creen per als valors reals **Cost** i **Vendes no facturades**.</span><span class="sxs-lookup"><span data-stu-id="f7303-152">Reversed actuals are created for both **Cost** and **Unbilled Sales** actuals.</span></span> <span data-ttu-id="f7303-153">El camp **Estat d'ajustament** dels valors reals invertits es defineix com a **No ajustable** i el camp **Estat de facturació** es defineix com a **Cancel·lat**.</span><span class="sxs-lookup"><span data-stu-id="f7303-153">The **Adjustment Status** field on the reversed actuals is set to **Unadjustable**, and the **Billing status** field is set to **Canceled**.</span></span> <span data-ttu-id="f7303-154">A causa d'aquests canvis, la despesa i el registre d'entrada d'ingressos registrats al projecte ja no comptabilitzaran a les quantitats que representin aquests valors reals.</span><span class="sxs-lookup"><span data-stu-id="f7303-154">Because of these changes, the recorded spending and the revenue backlog on the project will no longer account for the amounts that these actuals represent.</span></span>

<span data-ttu-id="f7303-155">Si es rebutja una sol·licitud de recuperació, no hi ha cap impacte financer en el projecte.</span><span class="sxs-lookup"><span data-stu-id="f7303-155">If a recall request is rejected, there is no financial impact on the project.</span></span>

## <a name="changes-to-time-entry-records"></a><span data-ttu-id="f7303-156">Canvis en els registres d'entrada de temps</span><span class="sxs-lookup"><span data-stu-id="f7303-156">Changes to time entry records</span></span>

<span data-ttu-id="f7303-157">A la il·lustració següent es mostren els canvis que es produeixen per a les entrades de temps aprovades quan es recuperen.</span><span class="sxs-lookup"><span data-stu-id="f7303-157">The following illustration shows the changes that occur for approved time entries when they are recalled.</span></span>

![Transicions d'estat de l'entrada de temps](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-entry-records"></a><span data-ttu-id="f7303-159">Canvis en els registres d'entrada de despeses</span><span class="sxs-lookup"><span data-stu-id="f7303-159">Changes to expense entry records</span></span>

<span data-ttu-id="f7303-160">A la il·lustració següent es mostren els canvis que es produeixen per a les entrades de despeses aprovades quan es recuperen.</span><span class="sxs-lookup"><span data-stu-id="f7303-160">The following illustration shows the changes that occur for approved expense entries when they are recalled.</span></span>

![Transicions d'estat de l'entrada de despeses](media/ExpenseEntryStateTransitions.png)
