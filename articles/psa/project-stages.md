---
title: Tipus de fases del projecte
description: Aquest tema proporciona informació sobre les fases del projecte.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 06/19/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: aa423979a794b07a8bd27440f47a29480b74b518
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123030"
---
# <a name="project-stage-types"></a><span data-ttu-id="ac070-103">Tipus de fases del projecte</span><span class="sxs-lookup"><span data-stu-id="ac070-103">Project stage types</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="ac070-104">Les fases d'un projecte estan dissenyades per reflectir l'estat del projecte a mesura que avança.</span><span class="sxs-lookup"><span data-stu-id="ac070-104">Project stages are designed to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="ac070-105">Les personalitzacions es poden utilitzar per actualitzar els trams automàticament amb flux del procés de negoci, el Power Automate o extensions de complements.</span><span class="sxs-lookup"><span data-stu-id="ac070-105">Customizations can be used to automatically update the stages with business process flows, Power Automate, or plug-in extensions.</span></span>

<span data-ttu-id="ac070-106">Les fases següents es defineixen al BPF per defecte:</span><span class="sxs-lookup"><span data-stu-id="ac070-106">The following stages are defined in the default BPF:</span></span>

- <span data-ttu-id="ac070-107">Nova</span><span class="sxs-lookup"><span data-stu-id="ac070-107">New</span></span>
- <span data-ttu-id="ac070-108">Oferta</span><span class="sxs-lookup"><span data-stu-id="ac070-108">Quote</span></span>
- <span data-ttu-id="ac070-109">Pla</span><span class="sxs-lookup"><span data-stu-id="ac070-109">Plan</span></span>
- <span data-ttu-id="ac070-110">Lliurament</span><span class="sxs-lookup"><span data-stu-id="ac070-110">Deliver</span></span>
- <span data-ttu-id="ac070-111">Completat</span><span class="sxs-lookup"><span data-stu-id="ac070-111">Complete</span></span>
- <span data-ttu-id="ac070-112">Tanca</span><span class="sxs-lookup"><span data-stu-id="ac070-112">Close</span></span> 

## <a name="new"></a><span data-ttu-id="ac070-113">New</span><span class="sxs-lookup"><span data-stu-id="ac070-113">New</span></span>

<span data-ttu-id="ac070-114">Quan creeu un projecte, la fase del projecte es defineix a **Nou**.</span><span class="sxs-lookup"><span data-stu-id="ac070-114">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="ac070-115">Si el projecte es va crear a partir d'una plantilla, pot ser que hi hagi dades de planificació, estimació i equips.</span><span class="sxs-lookup"><span data-stu-id="ac070-115">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="ac070-116">Altrament, és només un esbós del projecte i els components restants s'han d'introduir.</span><span class="sxs-lookup"><span data-stu-id="ac070-116">Otherwise, it's just an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="ac070-117">Oferta</span><span class="sxs-lookup"><span data-stu-id="ac070-117">Quote</span></span>

<span data-ttu-id="ac070-118">Quan associeu un projecte a una oferta o creeu un projecte a partir d'una oferta, la fase de projecte es defineix com a **Oferta** i les dates d'inici i finalització previstes s'actualitzen.</span><span class="sxs-lookup"><span data-stu-id="ac070-118">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote**, and the estimated start and end dates are updated.</span></span> <span data-ttu-id="ac070-119">Quan el projecte està en la fase **Oferta**, els detalls de l'oferta es mostren a la pestanya **Vendes** de la pàgina **Entitat del projecte**.</span><span class="sxs-lookup"><span data-stu-id="ac070-119">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="ac070-120">Pla</span><span class="sxs-lookup"><span data-stu-id="ac070-120">Plan</span></span>

<span data-ttu-id="ac070-121">Quan guanyeu una oferta associada amb un projecte, i quan el projecte avança a la fase **Contracte**, la fase de projecte s'actualitza a **Pla**.</span><span class="sxs-lookup"><span data-stu-id="ac070-121">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="ac070-122">Quan el projecte està en la fase **Pla**, els detalls del contracte es mostren a la pàgina **Entitat del projecte**.</span><span class="sxs-lookup"><span data-stu-id="ac070-122">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="ac070-123">Lliurament</span><span class="sxs-lookup"><span data-stu-id="ac070-123">Deliver</span></span>

<span data-ttu-id="ac070-124">Quan s'hagi completat el pla del projecte i ja esteu a punt per iniciar el projecte, l'administrador del projecte hauria d'actualitzar la fase del projecte a **Lliurament** per mostrar que el projecte ha començat.</span><span class="sxs-lookup"><span data-stu-id="ac070-124">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="ac070-125">Completat</span><span class="sxs-lookup"><span data-stu-id="ac070-125">Complete</span></span> 

<span data-ttu-id="ac070-126">Quan s'hagi completat el treball per al projecte, l'administrador del projecte pot actualitzar la fase a **Completat**.</span><span class="sxs-lookup"><span data-stu-id="ac070-126">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="ac070-127">En actualitzar la fase de projecte a **Completat**, l'administrador del projecte indica que el treball s'ha completat al 100 per cent, però que s'ha de mantenir obert el projecte de manera que es puguin registrar les entrades de temps o de despesa pendents.</span><span class="sxs-lookup"><span data-stu-id="ac070-127">By updating the project stage to **Complete**, the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="ac070-128">Tanca</span><span class="sxs-lookup"><span data-stu-id="ac070-128">Close</span></span>

<span data-ttu-id="ac070-129">Quan s'hagin registrat totes les transaccions per al projecte, l'administrador del projecte pot actualitzar la fase a **Tancat**.</span><span class="sxs-lookup"><span data-stu-id="ac070-129">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="ac070-130">En aquest moment, no es pot registrar cap transacció i el projecte es defineix com a només de lectura.</span><span class="sxs-lookup"><span data-stu-id="ac070-130">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>
