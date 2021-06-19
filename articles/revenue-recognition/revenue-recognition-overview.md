---
title: Informació general del reconeixement d'ingressos
description: En aquest tema es proporciona informació sobre el reconeixement d'ingressos a Project Operations.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: f5f962572c6ec0298d2d91d33f83e4120a498a6f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013744"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="0165c-103">Informació general del reconeixement d'ingressos</span><span class="sxs-lookup"><span data-stu-id="0165c-103">Revenue recognition overview</span></span>

<span data-ttu-id="0165c-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_</span><span class="sxs-lookup"><span data-stu-id="0165c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="0165c-105">Al Dynamics 365 Project Operations, els principis de reconeixement d'ingressos varien en funció del mètode de facturació seleccionat per a un projecte o una part del projecte.</span><span class="sxs-lookup"><span data-stu-id="0165c-105">In Dynamics 365 Project Operations, revenue recognition principles vary based on the selected billing method for a project or portion of the project.</span></span> <span data-ttu-id="0165c-106">En aquest tema es proporciona informació sobre el reconeixement d'ingressos a Project Operations.</span><span class="sxs-lookup"><span data-stu-id="0165c-106">This topic provides information about revenue recognition in Project Operations.</span></span>

## <a name="transactions-accounted-using-time-and-material-billing-method"></a><span data-ttu-id="0165c-107">Transaccions comptabilitzades amb el mètode de facturació de temps i material</span><span class="sxs-lookup"><span data-stu-id="0165c-107">Transactions accounted using time and material billing method</span></span>

- <span data-ttu-id="0165c-108">El reconeixement de costos i ingressos està connectat.</span><span class="sxs-lookup"><span data-stu-id="0165c-108">Cost and revenue recognition are connected.</span></span> <span data-ttu-id="0165c-109">El cost de la transacció i les vendes no facturades es comptabilitzen a través del [diari d'integració de Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="0165c-109">Transaction cost and unbilled sales are posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span>
- <span data-ttu-id="0165c-110">El perfil de costos i ingressos del projecte determina si les transaccions de vendes no facturades es comptabilitzen al llibre general.</span><span class="sxs-lookup"><span data-stu-id="0165c-110">Project cost and revenue profile determine if unbilled sales transactions are posted to the general ledger.</span></span> <span data-ttu-id="0165c-111">Si se selecciona **Meritar beneficis**, el sistema utilitza el **Valor de venda WIP** i els comptes de **Valor de vendes d'ingressos meritat** durant la comptabilització.</span><span class="sxs-lookup"><span data-stu-id="0165c-111">If **Accrue revenue** is selected, the system uses the **WIP sales value** and the **Accrued revenue sales value** accounts during posting.</span></span> <span data-ttu-id="0165c-112">A continuació us mostrem un exemple d'aquest mètode.</span><span class="sxs-lookup"><span data-stu-id="0165c-112">The following is an example of this method.</span></span>  

  | <span data-ttu-id="0165c-113">Tipus de transacció</span><span class="sxs-lookup"><span data-stu-id="0165c-113">Transaction type</span></span> | <span data-ttu-id="0165c-114">Dèbit/Crèdit</span><span class="sxs-lookup"><span data-stu-id="0165c-114">Debit/Credit</span></span> | <span data-ttu-id="0165c-115">Import</span><span class="sxs-lookup"><span data-stu-id="0165c-115">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="0165c-116">Valor de vendes WIP</span><span class="sxs-lookup"><span data-stu-id="0165c-116">WIP Sales value</span></span> | <span data-ttu-id="0165c-117">Dèbit</span><span class="sxs-lookup"><span data-stu-id="0165c-117">Debit</span></span> | <span data-ttu-id="0165c-118">100</span><span class="sxs-lookup"><span data-stu-id="0165c-118">100</span></span> |
  | <span data-ttu-id="0165c-119">Valor de vendes d'ingressos acumulats</span><span class="sxs-lookup"><span data-stu-id="0165c-119">Accrued revenue sales value</span></span> | <span data-ttu-id="0165c-120">Crèdit</span><span class="sxs-lookup"><span data-stu-id="0165c-120">Credit</span></span> | <span data-ttu-id="0165c-121">100</span><span class="sxs-lookup"><span data-stu-id="0165c-121">100</span></span> |

- <span data-ttu-id="0165c-122">Els ingressos es reconeixen durant la facturació.</span><span class="sxs-lookup"><span data-stu-id="0165c-122">Revenue is recognized during invoicing.</span></span> <span data-ttu-id="0165c-123">El sistema utilitza el compte **Ingressos facturats** durant la comptabilització.</span><span class="sxs-lookup"><span data-stu-id="0165c-123">The system uses the **Invoiced revenue** account during posting.</span></span> <span data-ttu-id="0165c-124">A continuació us mostrem un exemple d'aquest mètode.</span><span class="sxs-lookup"><span data-stu-id="0165c-124">The following is an example of this method.</span></span>  

  | <span data-ttu-id="0165c-125">Tipus de transacció</span><span class="sxs-lookup"><span data-stu-id="0165c-125">Transaction type</span></span> | <span data-ttu-id="0165c-126">Dèbit/Crèdit</span><span class="sxs-lookup"><span data-stu-id="0165c-126">Debit/Credit</span></span> | <span data-ttu-id="0165c-127">Import</span><span class="sxs-lookup"><span data-stu-id="0165c-127">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="0165c-128">Saldo de client</span><span class="sxs-lookup"><span data-stu-id="0165c-128">Customer balance</span></span> | <span data-ttu-id="0165c-129">Dèbit</span><span class="sxs-lookup"><span data-stu-id="0165c-129">Debit</span></span> | <span data-ttu-id="0165c-130">120</span><span class="sxs-lookup"><span data-stu-id="0165c-130">120</span></span> |
  | <span data-ttu-id="0165c-131">Impost sobre les vendes a pagar</span><span class="sxs-lookup"><span data-stu-id="0165c-131">Sales tax payable</span></span> | <span data-ttu-id="0165c-132">Crèdit</span><span class="sxs-lookup"><span data-stu-id="0165c-132">Credit</span></span> | <span data-ttu-id="0165c-133">20</span><span class="sxs-lookup"><span data-stu-id="0165c-133">20</span></span> |
  | <span data-ttu-id="0165c-134">Ingressos facturats</span><span class="sxs-lookup"><span data-stu-id="0165c-134">Invoiced Revenue</span></span> | <span data-ttu-id="0165c-135">Crèdit</span><span class="sxs-lookup"><span data-stu-id="0165c-135">Credit</span></span> | <span data-ttu-id="0165c-136">100</span><span class="sxs-lookup"><span data-stu-id="0165c-136">100</span></span> |

- <span data-ttu-id="0165c-137">Si els ingressos s'han acumulat en comptabilitzar les vendes no facturades, el sistema revertirà els ingressos meritats a facturació.</span><span class="sxs-lookup"><span data-stu-id="0165c-137">If revenue was accrued when the unbilled sales are posted, the system will reverse the accrued revenue at invoicing.</span></span>

  | <span data-ttu-id="0165c-138">Tipus de transacció</span><span class="sxs-lookup"><span data-stu-id="0165c-138">Transaction type</span></span> | <span data-ttu-id="0165c-139">Dèbit/Crèdit</span><span class="sxs-lookup"><span data-stu-id="0165c-139">Debit/Credit</span></span> | <span data-ttu-id="0165c-140">Import</span><span class="sxs-lookup"><span data-stu-id="0165c-140">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="0165c-141">Valor de vendes WIP</span><span class="sxs-lookup"><span data-stu-id="0165c-141">WIP Sales value</span></span> | <span data-ttu-id="0165c-142">Crèdit</span><span class="sxs-lookup"><span data-stu-id="0165c-142">Credit</span></span> | <span data-ttu-id="0165c-143">100</span><span class="sxs-lookup"><span data-stu-id="0165c-143">100</span></span> |
  | <span data-ttu-id="0165c-144">Valor de vendes d'ingressos acumulats</span><span class="sxs-lookup"><span data-stu-id="0165c-144">Accrued revenue sales value</span></span> | <span data-ttu-id="0165c-145">Dèbit</span><span class="sxs-lookup"><span data-stu-id="0165c-145">Debit</span></span> | <span data-ttu-id="0165c-146">100</span><span class="sxs-lookup"><span data-stu-id="0165c-146">100</span></span> |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a><span data-ttu-id="0165c-147">Transaccions comptabilitzades amb el mètode de facturació de preu fix</span><span class="sxs-lookup"><span data-stu-id="0165c-147">Transactions accounted using the fixed price billing method</span></span>

- <span data-ttu-id="0165c-148">El reconeixement de costos i ingressos està separat.</span><span class="sxs-lookup"><span data-stu-id="0165c-148">Cost and revenue recognition are separate.</span></span> <span data-ttu-id="0165c-149">El cost de la transacció es comptabilitza a través del [diari d'integració de Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="0165c-149">Transaction cost is posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="0165c-150">Les transaccions de vendes no facturades no es creen.</span><span class="sxs-lookup"><span data-stu-id="0165c-150">Unbilled sales transactions aren't created.</span></span>
- <span data-ttu-id="0165c-151">Els ingressos es poden reconèixer durant la facturació si el perfil de costos i ingressos del projecte té **Principi utilitzat per als càlculs de compleció de projectes** establert en **Sense WIP**.</span><span class="sxs-lookup"><span data-stu-id="0165c-151">Revenue can be recognized during invoicing if the project cost and revenue profile have **Principle used for project completion calculations** set to **No WIP**.</span></span> <span data-ttu-id="0165c-152">Utilitzeu només aquest mètode per a projectes senzills a curt termini.</span><span class="sxs-lookup"><span data-stu-id="0165c-152">Only use this method for short term, simple projects.</span></span>
- <span data-ttu-id="0165c-153">Els ingressos es poden reconèixer mitjançant estimacions d'ingressos de preu fix, amb el **Contracte completat** o el mètode de **Reconeixement d'ingressos de finalització en percentatge**.</span><span class="sxs-lookup"><span data-stu-id="0165c-153">Revenue can be recognized using fixed price revenue estimates, with either the **Completed contract** or **Percent completion revenue recognition** method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0165c-154">Recursos addicionals</span><span class="sxs-lookup"><span data-stu-id="0165c-154">Additional resources</span></span>
[<span data-ttu-id="0165c-155">Article Configuració de la comptabilitat per a projectes facturables</span><span class="sxs-lookup"><span data-stu-id="0165c-155">Configure accounting for billable projects article</span></span>](../project-accounting/configure-accounting-billable-projects.md)

[<span data-ttu-id="0165c-156">Projectes d'estimació d'ingressos de preu fix</span><span class="sxs-lookup"><span data-stu-id="0165c-156">Fixed price revenue estimate projects</span></span>](rev-rec-percentage-completion-method.md)

[<span data-ttu-id="0165c-157">Administració de les estimacions d'ingressos</span><span class="sxs-lookup"><span data-stu-id="0165c-157">Manage revenue estimates</span></span>](rev-rec-completed-contract-method.md)

[<span data-ttu-id="0165c-158">Mètodes de càlcul de costos per a la finalització</span><span class="sxs-lookup"><span data-stu-id="0165c-158">Cost to complete methods</span></span>](cost-complete-methods.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]