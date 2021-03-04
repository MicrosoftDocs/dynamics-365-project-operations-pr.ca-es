---
title: Flux de treball d'administració de despeses
description: Aquest tema explica com podeu utilitzar el sistema de flux de treball al Microsoft Dynamics 365 Finance per configurar un procés de revisió per als informes de despeses a l'administració de despeses.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bbee90450749c89f643d96e4d41a387c45e9abc5
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960550"
---
# <a name="expense-management-workflow"></a><span data-ttu-id="982c8-103">Flux de treball d'administració de despeses</span><span class="sxs-lookup"><span data-stu-id="982c8-103">Expense management workflow</span></span>

<span data-ttu-id="982c8-104">Podeu utilitzar el sistema de flux de treball per configurar un procés de revisió per als informes de despeses a l'administració de despeses.</span><span class="sxs-lookup"><span data-stu-id="982c8-104">You can use the workflow system to set up a review process for expense reports in Expense management.</span></span> <span data-ttu-id="982c8-105">Podeu configurar un flux de treball que utilitzi els següents criteris per determinar qui aprova els informes de despeses:</span><span class="sxs-lookup"><span data-stu-id="982c8-105">You can set up a workflow that uses the following criteria to determine who approves expense reports:</span></span>

- <span data-ttu-id="982c8-106">Jerarquia d'informes d'empleats i límits d'aprovació predefinits</span><span class="sxs-lookup"><span data-stu-id="982c8-106">The employee reporting hierarchy and predefined approval limits</span></span>
- <span data-ttu-id="982c8-107">Aprovació de diversos nivells que admet aprovadors intermedis i un aprovador final</span><span class="sxs-lookup"><span data-stu-id="982c8-107">Multi-level approval that supports interim approvers and a final approver</span></span>
- <span data-ttu-id="982c8-108">Dimensions financeres i responsabilitat del projecte</span><span class="sxs-lookup"><span data-stu-id="982c8-108">Financial dimensions and project responsibility</span></span>
- <span data-ttu-id="982c8-109">Assignació a usuaris específics o grups d'usuaris</span><span class="sxs-lookup"><span data-stu-id="982c8-109">Assignment to specific users or user groups</span></span>

<span data-ttu-id="982c8-110">Es poden crear aprovacions de flux de treball per a informes de despeses, peticions de viatges, avançaments d'efectiu i recuperació de l'impost sobre el valor afegit (IVA).</span><span class="sxs-lookup"><span data-stu-id="982c8-110">Workflow approvals can be created for expense reports, travel requisitions, cash advances, and value-added tax (VAT) recovery.</span></span>

<span data-ttu-id="982c8-111">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="982c8-111">**Example**</span></span>

<span data-ttu-id="982c8-112">El següent procés és un exemple del flux de treball d'administració de despeses per a un informe de despeses.</span><span class="sxs-lookup"><span data-stu-id="982c8-112">The following process is an example of the expense management workflow for an expense report.</span></span>

1. <span data-ttu-id="982c8-113">Un empleat crea i desa un informe de despeses.</span><span class="sxs-lookup"><span data-stu-id="982c8-113">An employee creates and saves an expense report.</span></span>
2. <span data-ttu-id="982c8-114">L'empleat envia l'informe de despeses per a la seva aprovació.</span><span class="sxs-lookup"><span data-stu-id="982c8-114">The employee submits the expense report for approval.</span></span> <span data-ttu-id="982c8-115">L'aprovador s'identifica en funció de les regles que es van definir quan es va configurar el flux de treball.</span><span class="sxs-lookup"><span data-stu-id="982c8-115">The approver is identified based on the rules that were defined when the workflow was set up.</span></span>
3. <span data-ttu-id="982c8-116">L'aprovador rep una notificació que un informe de despeses està a punt per a la seva aprovació.</span><span class="sxs-lookup"><span data-stu-id="982c8-116">The approver receives a notification that an expense report is ready for approval.</span></span> <span data-ttu-id="982c8-117">L'aprovador revisa l'informe de despeses i verifica que es compleixin les següents condicions:</span><span class="sxs-lookup"><span data-stu-id="982c8-117">The approver reviews the expense report and verifies that the following conditions are met:</span></span>

    - <span data-ttu-id="982c8-118">Les despeses no infringeixen cap norma de despeses.</span><span class="sxs-lookup"><span data-stu-id="982c8-118">The expenses don't violate any expense policies.</span></span> <span data-ttu-id="982c8-119">Si una despesa infringeix una norma, l'aprovador verifica que l'informe de despeses inclou una justificació empresarial vàlida.</span><span class="sxs-lookup"><span data-stu-id="982c8-119">If an expense violates a policy, the approver verifies that the expense report includes a valid business justification.</span></span>
    - <span data-ttu-id="982c8-120">A l'informe de despeses s'adjunten rebuts electrònics.</span><span class="sxs-lookup"><span data-stu-id="982c8-120">Electronic receipts are attached to the expense report.</span></span>

4. <span data-ttu-id="982c8-121">L'aprovador aprova l'informe de despeses.</span><span class="sxs-lookup"><span data-stu-id="982c8-121">The approver approves the expense report.</span></span>
5. <span data-ttu-id="982c8-122">L'informe de despeses s'assigna al coordinador de comptes a pagar per a la comptabilització.</span><span class="sxs-lookup"><span data-stu-id="982c8-122">The expense report is assigned to the Accounts payable coordinator for posting.</span></span>
6. <span data-ttu-id="982c8-123">Es produeix un dels passos següents, depenent de si la comptabilització automàtica està configurada:</span><span class="sxs-lookup"><span data-stu-id="982c8-123">One of the following steps occurs, depending on whether automatic posting is configured:</span></span>

    - <span data-ttu-id="982c8-124">Si la comptabilització automàtica està configurada, l'informe de despeses es processa per al pagament i l'estat de l'informe de despeses s'actualitza.</span><span class="sxs-lookup"><span data-stu-id="982c8-124">If automatic posting is configured, the expense report is processed for payment, and the status of the expense report is updated.</span></span>
    - <span data-ttu-id="982c8-125">Si no està configurada la comptabilització automàtica, el coordinador de comptes a pagar verifica que tots els rebuts originals s'han enviat i que els rebuts s'alineen amb les despeses de l'informe de despeses.</span><span class="sxs-lookup"><span data-stu-id="982c8-125">If automatic posting isn't configured, the Accounts payable coordinator verifies that all original receipts have been submitted, and that the receipts are aligned with the expenses on the expense report.</span></span> <span data-ttu-id="982c8-126">Tots els codis d'impostos que s'introdueixen en l'informe de despeses també s'han de verificar com a correctes.</span><span class="sxs-lookup"><span data-stu-id="982c8-126">All tax codes that are entered on the expense report must also be verified as correct.</span></span>

<span data-ttu-id="982c8-127">Després de verificar aquests requisits, es comptabilitza l'informe de despeses.</span><span class="sxs-lookup"><span data-stu-id="982c8-127">After these requirements are verified, the expense report is posted.</span></span>

<span data-ttu-id="982c8-128">Després que es comptabilitzi l'informe de despeses, s'autoritza el pagament de l'informe de despeses i es reemborsa a l'empleat.</span><span class="sxs-lookup"><span data-stu-id="982c8-128">After the expense report is posted, payment is authorized for the expense report, and the employee is reimbursed.</span></span>
