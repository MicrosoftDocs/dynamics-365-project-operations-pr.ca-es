---
title: Fases del projecte
description: En aquest tema s'ofereix informació sobre les fases del projecte disponibles al Microsoft Dynamics Project Operations.
author: ruhercul
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 079c3d2d16cf802d2b9ecc779577e6e390d92ddc
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996914"
---
# <a name="project-stages"></a><span data-ttu-id="75aef-103">Fases del projecte</span><span class="sxs-lookup"><span data-stu-id="75aef-103">Project stages</span></span>

<span data-ttu-id="75aef-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_</span><span class="sxs-lookup"><span data-stu-id="75aef-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="75aef-105">Les fases d'un projecte estan dissenyades per reflectir l'estat del projecte a mesura que avança.</span><span class="sxs-lookup"><span data-stu-id="75aef-105">Project stages are designed to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="75aef-106">Les personalitzacions es poden utilitzar per actualitzar els trams automàticament amb flux del procés de negoci, el Power Automate o extensions de complements.</span><span class="sxs-lookup"><span data-stu-id="75aef-106">Customizations can be used to automatically update the stages with business process flows, Power Automate, or plug-in extensions.</span></span>

<span data-ttu-id="75aef-107">Les fases següents es defineixen al flux del procés de negoci per defecte:</span><span class="sxs-lookup"><span data-stu-id="75aef-107">The following stages are defined in the default business process flow:</span></span>

- <span data-ttu-id="75aef-108">Nova</span><span class="sxs-lookup"><span data-stu-id="75aef-108">New</span></span>
- <span data-ttu-id="75aef-109">Oferta</span><span class="sxs-lookup"><span data-stu-id="75aef-109">Quote</span></span>
- <span data-ttu-id="75aef-110">Pla</span><span class="sxs-lookup"><span data-stu-id="75aef-110">Plan</span></span>
- <span data-ttu-id="75aef-111">Lliura</span><span class="sxs-lookup"><span data-stu-id="75aef-111">Deliver</span></span>
- <span data-ttu-id="75aef-112">Complet</span><span class="sxs-lookup"><span data-stu-id="75aef-112">Complete</span></span>
- <span data-ttu-id="75aef-113">Tanca </span><span class="sxs-lookup"><span data-stu-id="75aef-113">Close</span></span> 

## <a name="new"></a><span data-ttu-id="75aef-114">Nova</span><span class="sxs-lookup"><span data-stu-id="75aef-114">New</span></span>

<span data-ttu-id="75aef-115">Quan creeu un projecte, la fase del projecte es defineix a **Nou**.</span><span class="sxs-lookup"><span data-stu-id="75aef-115">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="75aef-116">Si el projecte es va crear a partir d'una plantilla, pot ser que hi hagi dades de planificació, estimació i equips.</span><span class="sxs-lookup"><span data-stu-id="75aef-116">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="75aef-117">Altrament, és només un esbós del projecte i els components restants s'han d'introduir.</span><span class="sxs-lookup"><span data-stu-id="75aef-117">Otherwise, it's an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="75aef-118">Oferta</span><span class="sxs-lookup"><span data-stu-id="75aef-118">Quote</span></span>

<span data-ttu-id="75aef-119">Quan associeu un projecte a una oferta o creeu un projecte a partir d'una oferta, la fase de projecte es defineix com a **Oferta** i les dates d'inici i finalització previstes s'actualitzen.</span><span class="sxs-lookup"><span data-stu-id="75aef-119">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote**, and the estimated start and end dates are updated.</span></span> <span data-ttu-id="75aef-120">Quan el projecte està en la fase **Oferta**, els detalls de l'oferta es mostren a la pestanya **Vendes** de la pàgina **Entitat del projecte**.</span><span class="sxs-lookup"><span data-stu-id="75aef-120">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="75aef-121">Pla</span><span class="sxs-lookup"><span data-stu-id="75aef-121">Plan</span></span>

<span data-ttu-id="75aef-122">Quan guanyeu una oferta associada amb un projecte, i quan el projecte avança a la fase **Contracte**, la fase de projecte s'actualitza a **Pla**.</span><span class="sxs-lookup"><span data-stu-id="75aef-122">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="75aef-123">Quan el projecte està en la fase **Pla**, els detalls del contracte es mostren a la pàgina **Entitat del projecte**.</span><span class="sxs-lookup"><span data-stu-id="75aef-123">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="75aef-124">Lliurament</span><span class="sxs-lookup"><span data-stu-id="75aef-124">Deliver</span></span>

<span data-ttu-id="75aef-125">Quan s'hagi completat el pla del projecte i ja esteu a punt per iniciar el projecte, l'administrador del projecte hauria d'actualitzar la fase del projecte a **Lliurament** per mostrar que el projecte ha començat.</span><span class="sxs-lookup"><span data-stu-id="75aef-125">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="75aef-126">Completat</span><span class="sxs-lookup"><span data-stu-id="75aef-126">Complete</span></span> 

<span data-ttu-id="75aef-127">Quan s'hagi completat el treball per al projecte, l'administrador del projecte pot actualitzar la fase a **Completat**.</span><span class="sxs-lookup"><span data-stu-id="75aef-127">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="75aef-128">En actualitzar la fase de projecte a **Completat**, l'administrador del projecte indica que el treball s'ha completat al 100 per cent, però que s'ha de mantenir obert el projecte de manera que es puguin registrar les entrades de temps o de despesa pendents.</span><span class="sxs-lookup"><span data-stu-id="75aef-128">By updating the project stage to **Complete**, the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="75aef-129">Tanca</span><span class="sxs-lookup"><span data-stu-id="75aef-129">Close</span></span>

<span data-ttu-id="75aef-130">Quan s'hagin registrat totes les transaccions per al projecte, l'administrador del projecte pot actualitzar la fase a **Tancat**.</span><span class="sxs-lookup"><span data-stu-id="75aef-130">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="75aef-131">En aquest moment, no es pot registrar cap transacció i el projecte es defineix com a només de lectura.</span><span class="sxs-lookup"><span data-stu-id="75aef-131">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]