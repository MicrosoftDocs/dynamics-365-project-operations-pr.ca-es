---
title: Entrada de despesa (bàsica)
description: En aquest tema es proporciona informació sobre com treballar amb l'entrada de despesa en una implementació bàsica.
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 536c961593599df8e7e2986f92259b0e690eae8b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121071"
---
# <a name="expense-entry-lite"></a><span data-ttu-id="7b55a-103">Entrada de despesa (bàsica)</span><span class="sxs-lookup"><span data-stu-id="7b55a-103">Expense entry (lite)</span></span>

<span data-ttu-id="7b55a-104">_**S'aplica a:** implementació bàsica: tracte de facturació proforma_</span><span class="sxs-lookup"><span data-stu-id="7b55a-104">_**Applies to:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="7b55a-105">Bàsica, l'administració de despeses és la capacitat de registrar les despeses simples.</span><span class="sxs-lookup"><span data-stu-id="7b55a-105">Basic, or lite, expense management is the capability to record simple expenses.</span></span> <span data-ttu-id="7b55a-106">Podeu registrar les despeses en un projecte i, a continuació, l'aprovador del projecte les revisarà i aprovarà.</span><span class="sxs-lookup"><span data-stu-id="7b55a-106">You can record expenses against a project, and then the project approver will review and approve them.</span></span>

<span data-ttu-id="7b55a-107">Per obtenir més informació sobre les capacitats de despesa del Dynamics 365 Project Operations, vegeu [Descripció general de les despeses](expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="7b55a-107">For more information about expense capabilities in Dynamics 365 Project Operations, see [Expense overview](expense-overview.md).</span></span>

## <a name="capture-a-basic-expense"></a><span data-ttu-id="7b55a-108">Capturar una despesa bàsica</span><span class="sxs-lookup"><span data-stu-id="7b55a-108">Capture a basic expense</span></span>

<span data-ttu-id="7b55a-109">Podeu capturar les despeses per enviar-les a l'aprovador.</span><span class="sxs-lookup"><span data-stu-id="7b55a-109">You can capture your expenses so that you can submit them to the approver.</span></span>

1. <span data-ttu-id="7b55a-110">Aneu a **Despeses** i seleccioneu **Nova**.</span><span class="sxs-lookup"><span data-stu-id="7b55a-110">Go to **Expenses**, and select **New**.</span></span>
2. <span data-ttu-id="7b55a-111">A la pàgina **Despesa nova**, introduïu la informació de despesa necessària i, a continuació, seleccioneu **Desa**.</span><span class="sxs-lookup"><span data-stu-id="7b55a-111">On the **New Expense** page, enter the required expense information, and then select **Save**.</span></span>

## <a name="submit-a-basic-expense"></a><span data-ttu-id="7b55a-112">Enviar una despesa bàsica</span><span class="sxs-lookup"><span data-stu-id="7b55a-112">Submit a basic expense</span></span>

<span data-ttu-id="7b55a-113">Després d'haver acabat de capturar totes les despeses i que estigueu a punt per aprovar-les, haureu d'enviar-les.</span><span class="sxs-lookup"><span data-stu-id="7b55a-113">After you've finished capturing all your expenses, and you're ready to have them approved, you must submit them.</span></span>

1. <span data-ttu-id="7b55a-114">Aneu a **Despeses** i seleccioneu una despesa.</span><span class="sxs-lookup"><span data-stu-id="7b55a-114">Go to **Expenses**, and select an expense.</span></span> <span data-ttu-id="7b55a-115">O bé, seleccioneu totes les despeses mitjançant la casella de selecció de la capçalera.</span><span class="sxs-lookup"><span data-stu-id="7b55a-115">Or, select all the expenses by using the check box on the header.</span></span>
2. <span data-ttu-id="7b55a-116">Seleccioneu **Envia**.</span><span class="sxs-lookup"><span data-stu-id="7b55a-116">Select **Submit**.</span></span> <span data-ttu-id="7b55a-117">El sistema processa les entrades seleccionades i crea sol·licituds d'aprovació de despeses.</span><span class="sxs-lookup"><span data-stu-id="7b55a-117">The system processes the selected entries and then creates expense approval requests.</span></span>

## <a name="recall-a-basic-expense"></a><span data-ttu-id="7b55a-118">Recuperar una despesa bàsica</span><span class="sxs-lookup"><span data-stu-id="7b55a-118">Recall a basic expense</span></span>

<span data-ttu-id="7b55a-119">Quan envieu una despesa per equivocació, podeu recuperar-la.</span><span class="sxs-lookup"><span data-stu-id="7b55a-119">When you submit an expense by mistake, you can recall it.</span></span> <span data-ttu-id="7b55a-120">El temps necessari per recuperar una entrada de despesa depèn de la fase d'aprovació.</span><span class="sxs-lookup"><span data-stu-id="7b55a-120">The time that is required to recall an expense entry depends on its approval stage.</span></span>  <span data-ttu-id="7b55a-121">Si l'aprovador encara no ha aprovat l'entrada, pot ser que la recuperació es produeixi immediatament.</span><span class="sxs-lookup"><span data-stu-id="7b55a-121">If the approver hasn't yet approved the entry, the recall can occur immediately.</span></span> <span data-ttu-id="7b55a-122">No obstant, si l'entrada ja ha estat aprovada, es demana a l'aprovador que aprovi la recuperació i reverteixi les transaccions.</span><span class="sxs-lookup"><span data-stu-id="7b55a-122">However, if the entry has already been approved, the approver is asked to approve the recall and reverse the transactions.</span></span>

1. <span data-ttu-id="7b55a-123">Aneu a **Despeses** i, a continuació, a la llista de despeses, seleccioneu la despesa que voleu recuperar.</span><span class="sxs-lookup"><span data-stu-id="7b55a-123">Go to **Expenses**, and then, in the list of expenses, select the expense to recall.</span></span>
2. <span data-ttu-id="7b55a-124">Seleccioneu **Recupera**.</span><span class="sxs-lookup"><span data-stu-id="7b55a-124">Select **Recall**.</span></span> <span data-ttu-id="7b55a-125">Si l'entrada de la despesa encara no s'ha aprovat, el sistema la recupera immediatament.</span><span class="sxs-lookup"><span data-stu-id="7b55a-125">If the expense entry hasn't yet been approved, the system immediately recalls it.</span></span> <span data-ttu-id="7b55a-126">Si l'entrada de la despesa ja s'ha aprovat, una sol·licitud de recuperació es crea per notificar a l'aprovador que voleu revertir la despesa.</span><span class="sxs-lookup"><span data-stu-id="7b55a-126">If the expense entry has already been approved, a recall request is created to notify the approver that you want to reverse the expense.</span></span> <span data-ttu-id="7b55a-127">A continuació, l'aprovador confirmarà que la reversió es pot fer i es recuperarà l'entrada.</span><span class="sxs-lookup"><span data-stu-id="7b55a-127">The approver will then confirm that the reversal can be done, and the entry will be returned.</span></span>

## <a name="delete-a-basic-expense"></a><span data-ttu-id="7b55a-128">Suprimir una despesa bàsica</span><span class="sxs-lookup"><span data-stu-id="7b55a-128">Delete a basic expense</span></span>

<span data-ttu-id="7b55a-129">Les despeses que encara no s'han enviat es poden suprimir.</span><span class="sxs-lookup"><span data-stu-id="7b55a-129">Expenses that haven't yet been submitted can be deleted.</span></span> <span data-ttu-id="7b55a-130">Per suprimir una despesa que ja s'ha enviat, primer heu de recuperar-la.</span><span class="sxs-lookup"><span data-stu-id="7b55a-130">To delete an expense that has already been submitted, you must first recall it.</span></span>

## <a name="see-also"></a><span data-ttu-id="7b55a-131">Consulteu també</span><span class="sxs-lookup"><span data-stu-id="7b55a-131">See also</span></span>

- [<span data-ttu-id="7b55a-132">Informació general de les aprovacions</span><span class="sxs-lookup"><span data-stu-id="7b55a-132">Approvals overview</span></span>](../approvals/approvals-overview.md)
