---
title: Cancel·lar entrades de temps i de despeses aprovades prèviament
description: En aquest tema es proporciona informació sobre com cancel·lar una transacció de despesa i temps de projecte aprovada.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 40ac37c1070e1c4da01e96bbc4248977b2b6d284
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290842"
---
# <a name="cancel-previously-approved-time-or-expense-entries"></a><span data-ttu-id="be98b-103">Cancel·lar entrades de temps o de despeses aprovades prèviament</span><span class="sxs-lookup"><span data-stu-id="be98b-103">Cancel previously approved time or expense entries</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="be98b-104">A la versió més recent del Dynamics 365 Project Service Automation, els aprovadors poden cancel·lar les entrades de temps o de despeses que prèviament s'havien aprovat.</span><span class="sxs-lookup"><span data-stu-id="be98b-104">In the latest version of Dynamics 365 Project Service Automation, approvers can cancel time or expense entries that they previously approved.</span></span>

## <a name="cancel-a-previously-approved-time-or-expense-entry"></a><span data-ttu-id="be98b-105">Cancel·lar una entrada de temps o de despeses aprovada prèviament</span><span class="sxs-lookup"><span data-stu-id="be98b-105">Cancel a previously approved time or expense entry</span></span>

<span data-ttu-id="be98b-106">Seguiu aquests passos per cancel·lar una entrada de temps o de despesa que hàgiu aprovat prèviament.</span><span class="sxs-lookup"><span data-stu-id="be98b-106">Follow these steps to cancel a time or expense entry that you previously approved.</span></span>

1. <span data-ttu-id="be98b-107">Aneu a **Projectes** \> **El meu treball** \> **Aprovacions**.</span><span class="sxs-lookup"><span data-stu-id="be98b-107">Go to **Projects** \> **My Work** \> **Approvals**.</span></span>
2. <span data-ttu-id="be98b-108">A la pàgina de llista **Aprovacions**, canvieu la visualització a **Les meves aprovacions anteriors**.</span><span class="sxs-lookup"><span data-stu-id="be98b-108">On the **Approvals** list page, change the view to **My past approvals**.</span></span> <span data-ttu-id="be98b-109">Es mostra una llista de les entrades de temps i de despesa que heu aprovat prèviament.</span><span class="sxs-lookup"><span data-stu-id="be98b-109">A list of the time and expense entries that you previously approved is shown.</span></span>
3. <span data-ttu-id="be98b-110">Seleccioneu una o diverses entrades i, a continuació , seleccioneu **Cancel·la l'aprovació**.</span><span class="sxs-lookup"><span data-stu-id="be98b-110">Select one or more entries, and then select **Cancel approval**.</span></span> <span data-ttu-id="be98b-111">Rebeu un missatge d'advertiment.</span><span class="sxs-lookup"><span data-stu-id="be98b-111">You receive a warning message.</span></span>
4. <span data-ttu-id="be98b-112">Seleccioneu **D'acord** per cancel·lar l'aprovació.</span><span class="sxs-lookup"><span data-stu-id="be98b-112">Select **OK** to cancel the approval.</span></span>

## <a name="understand-the-impact-of-canceling-a-time-or-expense-entry-approval"></a><span data-ttu-id="be98b-113">Entendre l'impacte de cancel·lar una aprovació d'entrada de temps o de despesa</span><span class="sxs-lookup"><span data-stu-id="be98b-113">Understand the impact of canceling a time or expense entry approval</span></span>

<span data-ttu-id="be98b-114">Quan una aprovació es cancel·la, hi ha un impacte operacional i un impacte financer.</span><span class="sxs-lookup"><span data-stu-id="be98b-114">When an approval is canceled, there is both operational impact and financial impact.</span></span>

### <a name="operational-impact"></a><span data-ttu-id="be98b-115">Impacte operacional</span><span class="sxs-lookup"><span data-stu-id="be98b-115">Operational impact</span></span>

<span data-ttu-id="be98b-116">A la part de les operacions, quan es cancel·la una aprovació, l'estat del registre es restableix a **Esborrany** i l'aprovació ja no apareix a la visualització **Les meves aprovacions anteriors**.</span><span class="sxs-lookup"><span data-stu-id="be98b-116">On the operations side, when an approval is canceled, the status of the record is reset to **Draft**, and the approval no longer appears in the **My past approvals** view.</span></span> <span data-ttu-id="be98b-117">En lloc d'això, l'aprovació cancel·lada es mostra a la visualització **Entrades de temps per a l'aprovació** o **Entrades de despesa per a l'aprovació**, en funció de si era una entrada de temps o de despeses.</span><span class="sxs-lookup"><span data-stu-id="be98b-117">Instead, the canceled approval appears in either the **Time entries for approval** view or the **Expense entries for approval** view, depending on whether it was a time entry or an expense entry.</span></span> <span data-ttu-id="be98b-118">A més, l'estat de l'entrada relacionada de temps o despeses es canvia a **Enviada**, de manera que l'entrada relacionada sigui coherent amb les aprovacions que tenen un estat **Esborrany**.</span><span class="sxs-lookup"><span data-stu-id="be98b-118">Additionally, the status of the related time or expense entry is changed to **Submitted**, so that the related entry is consistent with approvals that have a status of **Draft**.</span></span>

<span data-ttu-id="be98b-119">Com a aprovador, podeu editar alguns dels camps d'una aprovació que té l'estat **Esborrany**.</span><span class="sxs-lookup"><span data-stu-id="be98b-119">As an approver, you can edit some of the fields of an approval that has a status of **Draft**.</span></span> <span data-ttu-id="be98b-120">Aquests camps inclouen **Tipus de facturació** i **Hores facturables per ales entrades de temps**.</span><span class="sxs-lookup"><span data-stu-id="be98b-120">These fields include **Billing Type** and **Billable Hours for Time Entries**.</span></span> <span data-ttu-id="be98b-121">Després de fer canvis, podeu aprovar el registre de nou.</span><span class="sxs-lookup"><span data-stu-id="be98b-121">After you make changes, you can approve the record again.</span></span> <span data-ttu-id="be98b-122">O bé, podeu rebutjar l'entrada.</span><span class="sxs-lookup"><span data-stu-id="be98b-122">Alternatively, you can reject the entry.</span></span> <span data-ttu-id="be98b-123">Si rebutgeu l'aprovació d'una entrada de temps, l'estat de l'entrada es canvia a **Retornada**.</span><span class="sxs-lookup"><span data-stu-id="be98b-123">If you reject the approval of a time entry, the status of the entry is changed to **Returned**.</span></span> <span data-ttu-id="be98b-124">Si rebutgeu l'aprovació d'una entrada de despeses, l'estat de l'entrada es canvia a **Rebutjada**.</span><span class="sxs-lookup"><span data-stu-id="be98b-124">If you reject the approval of an expense entry, the status is changed to **Rejected**.</span></span> <span data-ttu-id="be98b-125">Funcionalment, tant les entrades retornades com rebutjades es comporten igualment com una entrada que té un estat **Esborrany**.</span><span class="sxs-lookup"><span data-stu-id="be98b-125">Functionally, both returned and rejected entries behave the same as an entry that has a status of **Draft**.</span></span> <span data-ttu-id="be98b-126">Un membre de l'equip del projecte pot fer els canvis necessaris a l'entrada i després tornar-la a enviar per a la seva aprovació o suprimir l'entrada per complet.</span><span class="sxs-lookup"><span data-stu-id="be98b-126">A project team member can either make any required changes to the entry and then resubmit it for approval, or delete the entry entirely.</span></span>

### <a name="financial-impact"></a><span data-ttu-id="be98b-127">Impacte financer</span><span class="sxs-lookup"><span data-stu-id="be98b-127">Financial impact</span></span>

<span data-ttu-id="be98b-128">Un projecte també es veu afectat financerament quan es cancel·la una aprovació.</span><span class="sxs-lookup"><span data-stu-id="be98b-128">A project is also affected financially when an approval is canceled.</span></span> <span data-ttu-id="be98b-129">En primer lloc, els valors reals corresponents al cost i les vendes s'actualitzen de la següent manera:</span><span class="sxs-lookup"><span data-stu-id="be98b-129">First, the corresponding actuals for cost and sales are updated in the following manner:</span></span>

- <span data-ttu-id="be98b-130">L'estat d'ajustament es defineix com a **Ajustat**.</span><span class="sxs-lookup"><span data-stu-id="be98b-130">The adjustment status is set to **Adjusted**.</span></span>
- <span data-ttu-id="be98b-131">L'estat de facturació es defineix com a **Cancel·lat**.</span><span class="sxs-lookup"><span data-stu-id="be98b-131">The billing status is set to **Canceled**.</span></span>

<span data-ttu-id="be98b-132">A continuació, les entrades d'inversió es creen a la taula Valors reals.</span><span class="sxs-lookup"><span data-stu-id="be98b-132">Next, reversal entries are created in the Actuals table.</span></span> <span data-ttu-id="be98b-133">Per crear entrades d'inversió, el sistema copia els valors de camp dels valors reals originals.</span><span class="sxs-lookup"><span data-stu-id="be98b-133">To create reversal entries, the system copies over the field values from the original actuals.</span></span> <span data-ttu-id="be98b-134">Els únics valors que no es copien són els valors de quantitat.</span><span class="sxs-lookup"><span data-stu-id="be98b-134">The only values that aren't copied over are the quantity values.</span></span> <span data-ttu-id="be98b-135">Aquests valors s'inverteixen en el seu lloc.</span><span class="sxs-lookup"><span data-stu-id="be98b-135">These values are reversed instead.</span></span> <span data-ttu-id="be98b-136">Els valors reals invertits es creen per als valors reals **Cost** i **Vendes no facturades**.</span><span class="sxs-lookup"><span data-stu-id="be98b-136">Reversed actuals are created for both **Cost** and **Unbilled Sales** actuals.</span></span> <span data-ttu-id="be98b-137">El camp **Estat d'ajustament** dels valors reals invertits es defineix com a **No ajustable** i l'estat de facturació es defineix com a **Cancel·lat**.</span><span class="sxs-lookup"><span data-stu-id="be98b-137">The **Adjustment Status** field on the reversed actuals is set to **Unadjustable**, and the billing status is set to **Canceled**.</span></span>

<span data-ttu-id="be98b-138">Després de fer aquests canvis, l'import que s'ha registrat com a invertit en el projecte i el registre d'entrada d'ingressos del projecte ja no comptabilitzarà per a les quantitats que representin aquests valors reals.</span><span class="sxs-lookup"><span data-stu-id="be98b-138">After these changes are made, the amount that is recorded as spent on the project and the revenue backlog on the project will longer account for the amounts that these actuals represent.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]