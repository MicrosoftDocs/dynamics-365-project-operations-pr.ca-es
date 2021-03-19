---
title: Actualització d'un projecte
description: En aquest tema es proporciona informació sobre l'actualització de projectes al Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 27444b072bdf7de55d6b38c30c1ea5fe66ed46ac
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286371"
---
# <a name="update-a-project"></a><span data-ttu-id="5fcfd-103">Actualització d'un projecte</span><span class="sxs-lookup"><span data-stu-id="5fcfd-103">Update a project</span></span>

<span data-ttu-id="5fcfd-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_</span><span class="sxs-lookup"><span data-stu-id="5fcfd-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="5fcfd-105">A continuació, es mostra un resum dels camps que es poden actualitzar en un projecte després d'haver-lo creat i altres implicacions aplicables a les actualitzacions.</span><span class="sxs-lookup"><span data-stu-id="5fcfd-105">Below is a summary of the fields that can be updated on a project after it has been created and any applicable implications of the updates.</span></span>

## <a name="project-detail-fields"></a><span data-ttu-id="5fcfd-106">Camps de detalls del projecte</span><span class="sxs-lookup"><span data-stu-id="5fcfd-106">Project detail fields</span></span>

- <span data-ttu-id="5fcfd-107">**Nom**: títol del projecte.</span><span class="sxs-lookup"><span data-stu-id="5fcfd-107">**Name**: The title of the project.</span></span>
- <span data-ttu-id="5fcfd-108">**Descripció**: informació general del projecte.</span><span class="sxs-lookup"><span data-stu-id="5fcfd-108">**Description**: An overview of the project.</span></span>
- <span data-ttu-id="5fcfd-109">**Client**: empresa a la qual es lliurarà el projecte.</span><span class="sxs-lookup"><span data-stu-id="5fcfd-109">**Customer**: The company the project will be delivered to.</span></span>
- <span data-ttu-id="5fcfd-110">**Plantilla de calendari**: hores de treball del projecte.</span><span class="sxs-lookup"><span data-stu-id="5fcfd-110">**Calendar template**: The working hours of the project.</span></span> <span data-ttu-id="5fcfd-111">Quan el camp canvia, es torna a calcular la planificació sencera.</span><span class="sxs-lookup"><span data-stu-id="5fcfd-111">When the field is changed, the entire schedule is recalculated.</span></span>
- <span data-ttu-id="5fcfd-112">**Moneda**: moneda per al projecte.</span><span class="sxs-lookup"><span data-stu-id="5fcfd-112">**Currency**: The currency for the project.</span></span> <span data-ttu-id="5fcfd-113">Aquest camp té com a valor per defecte la moneda definida a la unitat de contractació.</span><span class="sxs-lookup"><span data-stu-id="5fcfd-113">This field defaults based on the currency defined in the contracting unit.</span></span> <span data-ttu-id="5fcfd-114">Quan la unitat de contractació s'actualitza, el camp també s'actualitza.</span><span class="sxs-lookup"><span data-stu-id="5fcfd-114">When the contracting unit is updated, the field is also updated.</span></span>
- <span data-ttu-id="5fcfd-115">**Unitat de contractació**: unitat organitzativa que representa el grup d'empreses o la divisió que s'encarrega principalment de guanyar la venda i administrar el lliurament de treballs i serveis al client.</span><span class="sxs-lookup"><span data-stu-id="5fcfd-115">**Contracting Unit**: The organizational unit that represents the company group or division that is primarily responsible for winning the sale and managing the delivery of work and services to the customer.</span></span> 
- <span data-ttu-id="5fcfd-116">**Administrador del projecte**: membre de l'equip del projecte que té l'autoritat de revisar i aprovar les entrades de temps i les despeses.</span><span class="sxs-lookup"><span data-stu-id="5fcfd-116">**Project Manager**: The project team member who has the authority to review and approve time entries and expenses.</span></span>

## <a name="estimate-fields"></a><span data-ttu-id="5fcfd-117">Camps d'estimació</span><span class="sxs-lookup"><span data-stu-id="5fcfd-117">Estimate fields</span></span>

- <span data-ttu-id="5fcfd-118">**Data d'inici estimada**: la data en què començarà el projecte.</span><span class="sxs-lookup"><span data-stu-id="5fcfd-118">**Estimated Start Date**: The date that the project will begin.</span></span> <span data-ttu-id="5fcfd-119">Quan s'actualitzi aquest camp, qualsevol tasca del projecte es desplaçarà proporcionalment a la nova data d'inici.</span><span class="sxs-lookup"><span data-stu-id="5fcfd-119">When this field is updated, any tasks on the project will move proportionately with the start new start date.</span></span>
- <span data-ttu-id="5fcfd-120">**Data de finalització**: data en què es preveu finalitzar el projecte.</span><span class="sxs-lookup"><span data-stu-id="5fcfd-120">**Finish Date**: The date that the project is scheduled to end.</span></span>
- <span data-ttu-id="5fcfd-121">**Esforç**: esforç estimat del projecte.</span><span class="sxs-lookup"><span data-stu-id="5fcfd-121">**Effort**: The estimated effort of the project.</span></span> <span data-ttu-id="5fcfd-122">Quan s'afegeixen tasques al projecte, aquest camp ja no es pot editar.</span><span class="sxs-lookup"><span data-stu-id="5fcfd-122">When tasks are added to the project, this field is no longer editable.</span></span>
- <span data-ttu-id="5fcfd-123">**Cost de treball estimat**: cost del treball previst del projecte.</span><span class="sxs-lookup"><span data-stu-id="5fcfd-123">**Estimated Labor Cost**: The estimated labor cost of the project.</span></span> <span data-ttu-id="5fcfd-124">Quan s'afegeixen costos de treball al projecte, aquest camp ja no es pot editar.</span><span class="sxs-lookup"><span data-stu-id="5fcfd-124">When labor costs are added to the project, this field is no longer editable.</span></span>
- <span data-ttu-id="5fcfd-125">**Despeses estimades**: despeses estimades del projecte.</span><span class="sxs-lookup"><span data-stu-id="5fcfd-125">**Estimated Expenses**: The estimated expenses of the project.</span></span> <span data-ttu-id="5fcfd-126">Quan s'afegeixen despeses al projecte, aquest camp ja no es pot editar.</span><span class="sxs-lookup"><span data-stu-id="5fcfd-126">When expenses are added to the project, this field is no longer editable.</span></span>

## <a name="project-actual-fields"></a><span data-ttu-id="5fcfd-127">Camps reals del projecte</span><span class="sxs-lookup"><span data-stu-id="5fcfd-127">Project actual fields</span></span>
- <span data-ttu-id="5fcfd-128">**Inici real**: data en què es va iniciar el projecte.</span><span class="sxs-lookup"><span data-stu-id="5fcfd-128">**Actual Start**: The date that the project started.</span></span>
- <span data-ttu-id="5fcfd-129">**Finalització real**: s'actualitzarà quan es completi un projecte.</span><span class="sxs-lookup"><span data-stu-id="5fcfd-129">**Actual Finish**: To be updated when a project has been completed.</span></span>

## <a name="project-status-fields"></a><span data-ttu-id="5fcfd-130">Camps d'estat del projecte</span><span class="sxs-lookup"><span data-stu-id="5fcfd-130">Project status fields</span></span>

- <span data-ttu-id="5fcfd-131">**Estat global del projecte**: estat global del projecte proporcionat per l'administrador del projecte.</span><span class="sxs-lookup"><span data-stu-id="5fcfd-131">**Overall Project Status**: The overall project health provided by the Project manager.</span></span>
- <span data-ttu-id="5fcfd-132">**Comentaris**: text sobre l'estat actual del projecte que proporciona l'administrador del projecte.</span><span class="sxs-lookup"><span data-stu-id="5fcfd-132">**Comments**: A narrative regarding the current health of the project provided by the Project manager.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]