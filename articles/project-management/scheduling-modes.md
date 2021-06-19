---
title: Modes de planificació
description: Aquest tema proporciona informació sobre els modes de planificació.
author: ruhercul
ms.date: 05/28/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 508ff1df8f7e31066712fab6f8871dfdb107a43b
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116695"
---
# <a name="scheduling-modes"></a><span data-ttu-id="52869-103">Modes de planificació</span><span class="sxs-lookup"><span data-stu-id="52869-103">Scheduling modes</span></span>

<span data-ttu-id="52869-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_</span><span class="sxs-lookup"><span data-stu-id="52869-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="52869-105">El Dynamics 365 Project Operations permet a les organitzacions definir com administren els canvis en variables clau de les tasques dins de l'estructura del desglossament del treball.</span><span class="sxs-lookup"><span data-stu-id="52869-105">Dynamics 365 Project Operations provides the ability for organizations to define how they manage changes to key variables in tasks within the work breakdown structure.</span></span> <span data-ttu-id="52869-106">Segons les necessitats específiques de l'organització, els administradors de projectes poden fer canvis en el mode de planificació en crear un projecte.</span><span class="sxs-lookup"><span data-stu-id="52869-106">Based on the specific needs of the organization, Project Managers can make changes to the scheduling mode when a project is created.</span></span>

<span data-ttu-id="52869-107">Hi ha tres modes de planificació disponibles al Project Operations:</span><span class="sxs-lookup"><span data-stu-id="52869-107">There are three scheduling modes available in Project Operations:</span></span>

  - <span data-ttu-id="52869-108">Duració fixa (és el mode per defecte)</span><span class="sxs-lookup"><span data-stu-id="52869-108">Fixed duration (this is the default mode)</span></span>
  - <span data-ttu-id="52869-109">Esforç fix (*Treball*)</span><span class="sxs-lookup"><span data-stu-id="52869-109">Fixed effort (*Work*)</span></span>
  - <span data-ttu-id="52869-110">Unitats fixes</span><span class="sxs-lookup"><span data-stu-id="52869-110">Fixed units</span></span>

<span data-ttu-id="52869-111">Els valors afectats per la definició d'un mode de planificació específic estan determinats per la fórmula següent:</span><span class="sxs-lookup"><span data-stu-id="52869-111">The values impacted by the definition of a specific scheduling mode are determined by the following formula:</span></span>

  <span data-ttu-id="52869-112">Esforç = Duració x Unitats</span><span class="sxs-lookup"><span data-stu-id="52869-112">Effort  = Duration x Units</span></span>

<span data-ttu-id="52869-113">Quan definiu el mode de planificació d'un projecte, esteu configurant un d'aquests valors, que després no es pot canviar.</span><span class="sxs-lookup"><span data-stu-id="52869-113">When you define a project’s scheduling mode, you are setting one of these values, which then can't be changed.</span></span> <span data-ttu-id="52869-114">Mantenir aquest valor com una constant dona prioritat sobre aquest valor, que notifica al sistema que no el canviï quan canviïn els altres dos valors.</span><span class="sxs-lookup"><span data-stu-id="52869-114">Holding this value as a constant places a priority on that value, which notifies the system not to change it when the other two values change.</span></span> <span data-ttu-id="52869-115">A la taula següent es proporciona informació sobre els impactes de la selecció d'un mode específic.</span><span class="sxs-lookup"><span data-stu-id="52869-115">The following table provides information about the impacts of selecting a specific mode.</span></span>

| <span data-ttu-id="52869-116">**En aquesta tasca**</span><span class="sxs-lookup"><span data-stu-id="52869-116">**In this task**</span></span>             | <span data-ttu-id="52869-117">**Si reviseu unitats**</span><span class="sxs-lookup"><span data-stu-id="52869-117">**If you revise units**</span></span>   | <span data-ttu-id="52869-118">**Si reviseu la duració**</span><span class="sxs-lookup"><span data-stu-id="52869-118">**If you revise duration**</span></span> | <span data-ttu-id="52869-119">**Si reviseu l'esforç**</span><span class="sxs-lookup"><span data-stu-id="52869-119">**If you revise effort**</span></span>  |
|----------------------|---------------------------|----------------------------|---------------------------|
| <span data-ttu-id="52869-120">Tasca d'unitats fixes</span><span class="sxs-lookup"><span data-stu-id="52869-120">Fixed units task</span></span>     | <span data-ttu-id="52869-121">La duració es torna a calcular.</span><span class="sxs-lookup"><span data-stu-id="52869-121">Duration is recalculated.</span></span> | <span data-ttu-id="52869-122">L'esforç es torna a calcular.</span><span class="sxs-lookup"><span data-stu-id="52869-122">Effort is recalculated.</span></span>    | <span data-ttu-id="52869-123">La duració es torna a calcular.</span><span class="sxs-lookup"><span data-stu-id="52869-123">Duration is recalculated.</span></span> |
| <span data-ttu-id="52869-124">Tasca d'esforç fix</span><span class="sxs-lookup"><span data-stu-id="52869-124">Fixed effort task</span></span>    | <span data-ttu-id="52869-125">La duració es torna a calcular.</span><span class="sxs-lookup"><span data-stu-id="52869-125">Duration is recalculated.</span></span> | <span data-ttu-id="52869-126">Les unitats es tornen a calcular.</span><span class="sxs-lookup"><span data-stu-id="52869-126">Units are recalculated.</span></span>    | <span data-ttu-id="52869-127">La duració es torna a calcular.</span><span class="sxs-lookup"><span data-stu-id="52869-127">Duration is recalculated.</span></span> |
| <span data-ttu-id="52869-128">Tasca de duració fixa</span><span class="sxs-lookup"><span data-stu-id="52869-128">Fixed duration task</span></span>  | <span data-ttu-id="52869-129">L'esforç es torna a calcular.</span><span class="sxs-lookup"><span data-stu-id="52869-129">Effort is recalculated.</span></span>   | <span data-ttu-id="52869-130">L'esforç es torna a calcular.</span><span class="sxs-lookup"><span data-stu-id="52869-130">Effort is recalculated.</span></span>    | <span data-ttu-id="52869-131">Les unitats es tornen a calcular.</span><span class="sxs-lookup"><span data-stu-id="52869-131">Units are recalculated.</span></span>   |

<span data-ttu-id="52869-132">Per obtenir més informació sobre les implicacions d'un mode determinat, vegeu [Canviar el tipus de tasca per obtenir una planificació més precisa](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72).</span><span class="sxs-lookup"><span data-stu-id="52869-132">For more information about the implications of a given mode, see [Change the task type for more accurate scheduling](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72).</span></span> <span data-ttu-id="52869-133">En el tema, el terme **Feina** s'utilitza en lloc d'**Esforç**.</span><span class="sxs-lookup"><span data-stu-id="52869-133">In the topic, the term **Work** is used instead of **Effort**.</span></span>

## <a name="change-the-organizations-scheduling-mode"></a><span data-ttu-id="52869-134">Canviar el mode de planificació de l'organització</span><span class="sxs-lookup"><span data-stu-id="52869-134">Change the organization’s scheduling mode</span></span>

<span data-ttu-id="52869-135">Completeu els passos següents per definir el mode de planificació d'una organització.</span><span class="sxs-lookup"><span data-stu-id="52869-135">Complete the following steps to define the scheduling mode of an organization.</span></span>

1. <span data-ttu-id="52869-136">Aneu a **Configuració** \> **General** \> **Paràmetres** i, a continuació, seleccioneu el paràmetre de projecte.</span><span class="sxs-lookup"><span data-stu-id="52869-136">Go to **Settings** \> **General** \> **Parameters**, and then select the project parameter.</span></span> 
2. <span data-ttu-id="52869-137">A la pàgina **Paràmetres del projecte**, seleccioneu el mode de planificació per defecte de l'organització i, a continuació, permeteu que l'administrador de projectes substitueixi la configuració en crear un projecte nou.</span><span class="sxs-lookup"><span data-stu-id="52869-137">On the **Project Parameters** page, select the default scheduling mode for the organization, and then define ability for the Project manager to override the setting when creating a new project.</span></span>

## <a name="change-the-scheduling-mode-setting-on-a-project"></a><span data-ttu-id="52869-138">Canviar la configuració del mode de planificació d'un projecte</span><span class="sxs-lookup"><span data-stu-id="52869-138">Change the scheduling mode setting on a project</span></span>

<span data-ttu-id="52869-139">Si una organització permet a l'administrador del projecte substituir el mode de planificació per defecte, l'administrador del projecte pot fer que canviï quan creï un projecte nou.</span><span class="sxs-lookup"><span data-stu-id="52869-139">If an organization allows the Project manager to override the default scheduling mode, the Project manager can make that change when they create a new project.</span></span> <span data-ttu-id="52869-140">Tanmateix, quan el projecte s'ha desat, el mode de planificació no es pot canviar.</span><span class="sxs-lookup"><span data-stu-id="52869-140">However, after the project has been saved, the scheduling mode can't be changed.</span></span>

## <a name="copied-projects"></a><span data-ttu-id="52869-141">Projecte copiats</span><span class="sxs-lookup"><span data-stu-id="52869-141">Copied projects</span></span>

<span data-ttu-id="52869-142">Com que un projecte es crea quan s'adopta l'acció de projecte de còpia, l'administrador del projecte no pot definir el mode de planificació.</span><span class="sxs-lookup"><span data-stu-id="52869-142">Because a project is created when the copy project action is taken, the Project manager can't set the scheduling mode.</span></span> <span data-ttu-id="52869-143">El projecte de destinació sempre serà per defecte el mode definit en el nivell de l'organització.</span><span class="sxs-lookup"><span data-stu-id="52869-143">The destination project will always default to the mode defined at the organizational level.</span></span>

## <a name="copied-tasks"></a><span data-ttu-id="52869-144">Tasques copiades</span><span class="sxs-lookup"><span data-stu-id="52869-144">Copied tasks</span></span>

<span data-ttu-id="52869-145">Quan es copia una tasca d'un projecte a un altre, la tasca hereta el mode de planificació del projecte de destinació.</span><span class="sxs-lookup"><span data-stu-id="52869-145">When a task is copied from one project to another, the task inherits the scheduling mode of the destination project.</span></span>
