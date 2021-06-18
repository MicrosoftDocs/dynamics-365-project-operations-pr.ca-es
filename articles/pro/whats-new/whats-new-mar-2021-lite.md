---
title: Novetats del març del 2021 - Implementació bàsica del Project Operations
description: Aquest tema proporciona informació sobre les actualitzacions de qualitat disponibles en el llançament de març de 2021 de la implementació bàsica del Project Operations.
author: sigitac
ms.date: 03/03/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: efddb96b2cb428b9dc0488c32eb5670d01322bcb
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993854"
---
# <a name="whats-new-march-2021---project-operations-lite-deployment"></a><span data-ttu-id="999f9-103">Novetats del març del 2021 - Implementació bàsica del Project Operations</span><span class="sxs-lookup"><span data-stu-id="999f9-103">What's new March 2021 - Project Operations lite deployment</span></span>

<span data-ttu-id="999f9-104">_S'aplica a: implementació bàsica: tracte de facturació proforma_</span><span class="sxs-lookup"><span data-stu-id="999f9-104">_Applies To: Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="999f9-105">Aquest tema s'aplica als components i versions següents del Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="999f9-105">This topic applies to the following Dynamics 365 Project Operations components and versions:</span></span>

- <span data-ttu-id="999f9-106">Project Operations en entorn del Dataverse versió 4.8.0.91</span><span class="sxs-lookup"><span data-stu-id="999f9-106">Project Operations on Dataverse environment version 4.8.0.91</span></span> 

## <a name="quality-updates"></a><span data-ttu-id="999f9-107">Actualitzacions de qualitat</span><span class="sxs-lookup"><span data-stu-id="999f9-107">Quality updates</span></span>

| <span data-ttu-id="999f9-108">**Àrea de característiques**</span><span class="sxs-lookup"><span data-stu-id="999f9-108">**Feature area**</span></span> | <span data-ttu-id="999f9-109">**Número de referència**</span><span class="sxs-lookup"><span data-stu-id="999f9-109">**Reference number**</span></span> | <span data-ttu-id="999f9-110">**Actualització de qualitat**</span><span class="sxs-lookup"><span data-stu-id="999f9-110">**Quality update**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="999f9-111">Facturació i preus</span><span class="sxs-lookup"><span data-stu-id="999f9-111">Billing and pricing</span></span> | <span data-ttu-id="999f9-112">2133873</span><span class="sxs-lookup"><span data-stu-id="999f9-112">2133873</span></span> | <span data-ttu-id="999f9-113">S'ha corregit la visualització del símbol de moneda de **Preu de venda per unitat** a la quadrícula **Estimacions de despeses**.</span><span class="sxs-lookup"><span data-stu-id="999f9-113">Fixed the display of **Unit Sales Price** currency symbol in the **Expense Estimates** grid.</span></span> |
| <span data-ttu-id="999f9-114">Facturació i preus</span><span class="sxs-lookup"><span data-stu-id="999f9-114">Billing and pricing</span></span> | <span data-ttu-id="999f9-115">2174616</span><span class="sxs-lookup"><span data-stu-id="999f9-115">2174616</span></span> | <span data-ttu-id="999f9-116">Quan es guanya una oferta, es fa referència a la llista de preus personalitzada del contracte als detalls de la línia de contracte que es copien de l'oferta.</span><span class="sxs-lookup"><span data-stu-id="999f9-116">When a quote is won, the contract custom pricelist is referenced on contract line details that are copied from the quote.</span></span> |
| <span data-ttu-id="999f9-117">Administració d'oportunitats</span><span class="sxs-lookup"><span data-stu-id="999f9-117">Opportunity Management</span></span> | <span data-ttu-id="999f9-118">2167475</span><span class="sxs-lookup"><span data-stu-id="999f9-118">2167475</span></span> | <span data-ttu-id="999f9-119">Import de l'impost fix a la factura de correcció que s'ha originat d'una entrada real no facturada.</span><span class="sxs-lookup"><span data-stu-id="999f9-119">Fixed tax amount in the correction invoice that originated an unbilled actual entry.</span></span> |
| <span data-ttu-id="999f9-120">Administració d'oportunitats</span><span class="sxs-lookup"><span data-stu-id="999f9-120">Opportunity Management</span></span> | <span data-ttu-id="999f9-121">2176285</span><span class="sxs-lookup"><span data-stu-id="999f9-121">2176285</span></span> | <span data-ttu-id="999f9-122">L'import de l'impost no s'ha de copiar dels detalls del contracte de vendes/línia d'oferta als detalls del contracte de cost/línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="999f9-122">Tax amount must not be copied from sales contract/quote line details to cost contract/quote line details.</span></span> |
| <span data-ttu-id="999f9-123">Administració d'oportunitats</span><span class="sxs-lookup"><span data-stu-id="999f9-123">Opportunity Management</span></span> | <span data-ttu-id="999f9-124">2188079</span><span class="sxs-lookup"><span data-stu-id="999f9-124">2188079</span></span> | <span data-ttu-id="999f9-125">No s'ha de crear una regla de facturació dividida per als contractes que no estiguin basats en treball.</span><span class="sxs-lookup"><span data-stu-id="999f9-125">Split billing rule must not be created for contracts that are not work-based.</span></span> |
| <span data-ttu-id="999f9-126">Planificació i seguiment</span><span class="sxs-lookup"><span data-stu-id="999f9-126">Planning and Tracking</span></span> | <span data-ttu-id="999f9-127">2138853</span><span class="sxs-lookup"><span data-stu-id="999f9-127">2138853</span></span> | <span data-ttu-id="999f9-128">La funció de còpia del projecte s'actualitza per garantir que les línies d'estimació de despeses que fan referència a tasques es copien al projecte de destinació.</span><span class="sxs-lookup"><span data-stu-id="999f9-128">Project copy function updated to ensure expense estimate lines that reference tasks are copied to the destination project.</span></span> |
| <span data-ttu-id="999f9-129">Planificació i seguiment</span><span class="sxs-lookup"><span data-stu-id="999f9-129">Planning and Tracking</span></span> | <span data-ttu-id="999f9-130">2173259</span><span class="sxs-lookup"><span data-stu-id="999f9-130">2173259</span></span> | <span data-ttu-id="999f9-131">Funció de còpia del projecte actualitzada per assegurar-se que no mostra el missatge d'error **S'està copiant l'estructura de desglossament del treball (WBS)** en certs escenaris.</span><span class="sxs-lookup"><span data-stu-id="999f9-131">Project copy function updated to ensure it doesn't display the **Copying WBS** error message in certain scenarios.</span></span> |
| <span data-ttu-id="999f9-132">Temps i despesa</span><span class="sxs-lookup"><span data-stu-id="999f9-132">Time and Expense</span></span> | <span data-ttu-id="999f9-133">2148910</span><span class="sxs-lookup"><span data-stu-id="999f9-133">2148910</span></span> | <span data-ttu-id="999f9-134">S'ha corregit el problema de visualització a la pàgina **Edita l'entrada** a la quadrícula **Entrada de temps**.</span><span class="sxs-lookup"><span data-stu-id="999f9-134">Fixed display issue with the **Edit Entry** page in the **Time Entry** grid.</span></span> |
| <span data-ttu-id="999f9-135">Temps i despesa</span><span class="sxs-lookup"><span data-stu-id="999f9-135">Time and Expense</span></span> | <span data-ttu-id="999f9-136">2159798</span><span class="sxs-lookup"><span data-stu-id="999f9-136">2159798</span></span> | <span data-ttu-id="999f9-137">Controls ajustats per garantir que les entrades de despeses aprovades no es poden editar.</span><span class="sxs-lookup"><span data-stu-id="999f9-137">Tightened controls to ensure approved expense entries can't be edited.</span></span> |


