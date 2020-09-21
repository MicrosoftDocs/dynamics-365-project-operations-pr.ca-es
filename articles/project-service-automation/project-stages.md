---
title: Fases del projecte
description: Aquest tema proporciona informació sobre les fases del projecte.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 983c25a0-ed21-4151-a109-b385a88285fa
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 70aa057e127df7ba925e84f5d056a06a4cc8833e
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749469"
---
# <a name="project-stages"></a><span data-ttu-id="c6b47-103">Fases del projecte</span><span class="sxs-lookup"><span data-stu-id="c6b47-103">Project stages</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="c6b47-104">Les fases del projecte s'actualitzen per reflectir l'estat del projecte a mesura que avança.</span><span class="sxs-lookup"><span data-stu-id="c6b47-104">Project stages are updated to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="c6b47-105">El flux del procés de negoci per defecte actualitza automàticament algunes fases del projecte i altres s'actualitzen manualment per part de l'administrador de projecte.</span><span class="sxs-lookup"><span data-stu-id="c6b47-105">The default business process flow automatically updates some stages of the project while others are manually updated by the project manager.</span></span> 

<span data-ttu-id="c6b47-106">Les fases següents es defineixen al BPF per defecte:</span><span class="sxs-lookup"><span data-stu-id="c6b47-106">The following stages are defined in the default BPF:</span></span>

- <span data-ttu-id="c6b47-107">New</span><span class="sxs-lookup"><span data-stu-id="c6b47-107">New</span></span>
- <span data-ttu-id="c6b47-108">Oferta</span><span class="sxs-lookup"><span data-stu-id="c6b47-108">Quote</span></span>
- <span data-ttu-id="c6b47-109">Pla</span><span class="sxs-lookup"><span data-stu-id="c6b47-109">Plan</span></span>
- <span data-ttu-id="c6b47-110">Lliurament</span><span class="sxs-lookup"><span data-stu-id="c6b47-110">Deliver</span></span>
- <span data-ttu-id="c6b47-111">Completat</span><span class="sxs-lookup"><span data-stu-id="c6b47-111">Complete</span></span>
- <span data-ttu-id="c6b47-112">Tanca</span><span class="sxs-lookup"><span data-stu-id="c6b47-112">Close</span></span> 

## <a name="new"></a><span data-ttu-id="c6b47-113">New</span><span class="sxs-lookup"><span data-stu-id="c6b47-113">New</span></span>

<span data-ttu-id="c6b47-114">Quan creeu un projecte, la fase del projecte es defineix a **Nou**.</span><span class="sxs-lookup"><span data-stu-id="c6b47-114">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="c6b47-115">Si el projecte es va crear a partir d'una plantilla, pot ser que hi hagi dades de planificació, estimació i equips.</span><span class="sxs-lookup"><span data-stu-id="c6b47-115">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="c6b47-116">Altrament, és només un esbós del projecte i els components restants s'han d'introduir.</span><span class="sxs-lookup"><span data-stu-id="c6b47-116">Otherwise, it's just an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="c6b47-117">Oferta</span><span class="sxs-lookup"><span data-stu-id="c6b47-117">Quote</span></span>

<span data-ttu-id="c6b47-118">Quan associeu un projecte a una oferta o creeu un projecte a partir d'una oferta, la fase de projecte es defineix com a **Oferta** i les dates d'inici i finalització previstes s'actualitzen.</span><span class="sxs-lookup"><span data-stu-id="c6b47-118">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote**, and the estimated start and end dates are updated.</span></span> <span data-ttu-id="c6b47-119">Quan el projecte està en la fase **Oferta**, els detalls de l'oferta es mostren a la pestanya **Vendes** de la pàgina **Entitat del projecte**.</span><span class="sxs-lookup"><span data-stu-id="c6b47-119">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="c6b47-120">Pla</span><span class="sxs-lookup"><span data-stu-id="c6b47-120">Plan</span></span>

<span data-ttu-id="c6b47-121">Quan guanyeu una oferta associada amb un projecte, i quan el projecte avança a la fase **Contracte**, la fase de projecte s'actualitza a **Pla**.</span><span class="sxs-lookup"><span data-stu-id="c6b47-121">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="c6b47-122">Quan el projecte està en la fase **Pla**, els detalls del contracte es mostren a la pàgina **Entitat del projecte**.</span><span class="sxs-lookup"><span data-stu-id="c6b47-122">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="c6b47-123">Lliurament</span><span class="sxs-lookup"><span data-stu-id="c6b47-123">Deliver</span></span>

<span data-ttu-id="c6b47-124">Quan s'hagi completat el pla del projecte i ja esteu a punt per iniciar el projecte, l'administrador del projecte hauria d'actualitzar la fase del projecte a **Lliurament** per mostrar que el projecte ha començat.</span><span class="sxs-lookup"><span data-stu-id="c6b47-124">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="c6b47-125">Completat</span><span class="sxs-lookup"><span data-stu-id="c6b47-125">Complete</span></span> 

<span data-ttu-id="c6b47-126">Quan s'hagi completat el treball per al projecte, l'administrador del projecte pot actualitzar la fase a **Completat**.</span><span class="sxs-lookup"><span data-stu-id="c6b47-126">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="c6b47-127">En actualitzar la fase de projecte a **Completat**, l'administrador del projecte indica que el treball s'ha completat al 100 per cent, però que s'ha de mantenir obert el projecte de manera que es puguin registrar les entrades de temps o de despesa pendents.</span><span class="sxs-lookup"><span data-stu-id="c6b47-127">By updating the project stage to **Complete**, the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="c6b47-128">Tanca</span><span class="sxs-lookup"><span data-stu-id="c6b47-128">Close</span></span>

<span data-ttu-id="c6b47-129">Quan s'hagin registrat totes les transaccions per al projecte, l'administrador del projecte pot actualitzar la fase a **Tancat**.</span><span class="sxs-lookup"><span data-stu-id="c6b47-129">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="c6b47-130">En aquest moment, no es pot registrar cap transacció i el projecte es defineix com a només de lectura.</span><span class="sxs-lookup"><span data-stu-id="c6b47-130">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>
