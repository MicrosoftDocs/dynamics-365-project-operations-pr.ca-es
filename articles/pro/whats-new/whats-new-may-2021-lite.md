---
title: 'Novetats del maig de 2021: implementació bàsica del Project Operations'
description: Aquest tema proporciona informació sobre les actualitzacions de qualitat disponibles a la versió de maig de 2021 de la implementació bàsica del Project Operations.
author: sigitac
ms.date: 05/17/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6fb1955e2adb8562ac00a90880bf8e147bf5ed6a
ms.sourcegitcommit: 18bb56676999dbde1cf880239847ee9c2b216fe4
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/18/2021
ms.locfileid: "6060421"
---
# <a name="whats-new-may-2021---project-operations-lite-deployment"></a><span data-ttu-id="cf67f-103">Novetats del maig de 2021: implementació bàsica del Project Operations</span><span class="sxs-lookup"><span data-stu-id="cf67f-103">What's new May 2021 - Project Operations lite deployment</span></span>

<span data-ttu-id="cf67f-104">_S'aplica a: implementació bàsica: tracte de facturació proforma_</span><span class="sxs-lookup"><span data-stu-id="cf67f-104">_Applies To: Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="cf67f-105">Aquest tema s'aplica als components i versions següents del Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="cf67f-105">This topic applies to the following Dynamics 365 Project Operations components and versions:</span></span>

   - <span data-ttu-id="cf67f-106">Project Operations en l'entorn del Dataverse versió 4.10.0.186.</span><span class="sxs-lookup"><span data-stu-id="cf67f-106">Project Operations on Dataverse environment version 4.10.0.186.</span></span>

## <a name="features-included-in-this-release"></a><span data-ttu-id="cf67f-107">Característiques incloses en aquesta versió</span><span class="sxs-lookup"><span data-stu-id="cf67f-107">Features included in this release</span></span>

<span data-ttu-id="cf67f-108">En aquesta versió s'inclouen les característiques següents:</span><span class="sxs-lookup"><span data-stu-id="cf67f-108">The following features are included in this release:</span></span>

- <span data-ttu-id="cf67f-109">[Modes de planificació](../../project-management/scheduling-modes.md): els administradors de projectes ara poden definir si un projecte s'ha d'administrar amb el mode de planificació de duració fixa, treball fix o unitats fixes.</span><span class="sxs-lookup"><span data-stu-id="cf67f-109">[Scheduling modes](../../project-management/scheduling-modes.md): Project managers can now define if a project should be managed using a fixed duration, fixed work, or fixed units scheduling mode.</span></span>

## <a name="quality-updates"></a><span data-ttu-id="cf67f-110">Actualitzacions de qualitat</span><span class="sxs-lookup"><span data-stu-id="cf67f-110">Quality updates</span></span>

| <span data-ttu-id="cf67f-111">**Àrea de característiques**</span><span class="sxs-lookup"><span data-stu-id="cf67f-111">**Feature area**</span></span> | <span data-ttu-id="cf67f-112">**Número de referència**</span><span class="sxs-lookup"><span data-stu-id="cf67f-112">**Reference number**</span></span> | <span data-ttu-id="cf67f-113">**Actualització de qualitat**</span><span class="sxs-lookup"><span data-stu-id="cf67f-113">**Quality update**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="cf67f-114">Facturació i preus</span><span class="sxs-lookup"><span data-stu-id="cf67f-114">Billing and pricing</span></span> | <span data-ttu-id="cf67f-115">2224568</span><span class="sxs-lookup"><span data-stu-id="cf67f-115">2224568</span></span> | <span data-ttu-id="cf67f-116">S'ha afegit lògica per permetre personalitzacions que impliquen la invocació del complement de confirmació de la factura.</span><span class="sxs-lookup"><span data-stu-id="cf67f-116">Added logic to enable customizations that involve invoking the invoice confirmation plug-in.</span></span> |
| <span data-ttu-id="cf67f-117">Facturació i preus</span><span class="sxs-lookup"><span data-stu-id="cf67f-117">Billing and pricing</span></span> | <span data-ttu-id="cf67f-118">2101098</span><span class="sxs-lookup"><span data-stu-id="cf67f-118">2101098</span></span> | <span data-ttu-id="cf67f-119">S'ha millorat la lògica dels camps per defecte a la factura proforma.</span><span class="sxs-lookup"><span data-stu-id="cf67f-119">Improved the logic of default fields to proforma invoice.</span></span> <span data-ttu-id="cf67f-120">Aquests camps inclouen, **Adreça de facturació**, **Nom de facturació** i **Termes de pagament**.</span><span class="sxs-lookup"><span data-stu-id="cf67f-120">These fields include, **Bill-to address**, **Bill to name**, and **Payment terms**.</span></span> <span data-ttu-id="cf67f-121">Ara, els camps són per defecte el registre de client de contracte del projecte corresponent.</span><span class="sxs-lookup"><span data-stu-id="cf67f-121">The fields now default from the corresponding project contract customer record.</span></span> |
| <span data-ttu-id="cf67f-122">Facturació i preus</span><span class="sxs-lookup"><span data-stu-id="cf67f-122">Billing and pricing</span></span> | <span data-ttu-id="cf67f-123">2021413</span><span class="sxs-lookup"><span data-stu-id="cf67f-123">2021413</span></span> | <span data-ttu-id="cf67f-124">S'han actualitzat els camps **Cost real** i **Vendes** de l'entitat **Tasca** per incloure els valors de vendes de les despeses no facturades i facturades en les tasques.</span><span class="sxs-lookup"><span data-stu-id="cf67f-124">Updated the **Actual cost** and **Sales** fields on the **Task** entity to include sales values from unbilled and billed expenses on tasks.</span></span> |
| <span data-ttu-id="cf67f-125">Facturació i preus</span><span class="sxs-lookup"><span data-stu-id="cf67f-125">Billing and pricing</span></span> | <span data-ttu-id="cf67f-126">2182110</span><span class="sxs-lookup"><span data-stu-id="cf67f-126">2182110</span></span> | <span data-ttu-id="cf67f-127">Quan es copia un contracte de projecte, l'identificador de línia de contracte es torna a generar al contracte del projecte de destinació per assegurar que és únic.</span><span class="sxs-lookup"><span data-stu-id="cf67f-127">When copying a project contract, the contract line ID is regenerated in the destination project contract to ensure it's unique.</span></span> |
| <span data-ttu-id="cf67f-128">Administració d'oportunitats</span><span class="sxs-lookup"><span data-stu-id="cf67f-128">Opportunity Management</span></span> | <span data-ttu-id="cf67f-129">2186741</span><span class="sxs-lookup"><span data-stu-id="cf67f-129">2186741</span></span> | <span data-ttu-id="cf67f-130">S'han afegit validacions per assegurar que el camp **Origen** i el tipus de transacció no es poden actualitzar en els detalls de la línia d'oferta existent.</span><span class="sxs-lookup"><span data-stu-id="cf67f-130">Added validations to ensure the **Origin** field and transaction type can't be updated on existing quote line details.</span></span> |
| <span data-ttu-id="cf67f-131">Administració d'oportunitats</span><span class="sxs-lookup"><span data-stu-id="cf67f-131">Opportunity Management</span></span> | <span data-ttu-id="cf67f-132">2191353</span><span class="sxs-lookup"><span data-stu-id="cf67f-132">2191353</span></span> | <span data-ttu-id="cf67f-133">La creació de fites no s'han de permetre en una línia de contracte de temps i material.</span><span class="sxs-lookup"><span data-stu-id="cf67f-133">Milestone creation must not be allowed on a time and material contract line.</span></span> |
| <span data-ttu-id="cf67f-134">Administració d'oportunitats</span><span class="sxs-lookup"><span data-stu-id="cf67f-134">Opportunity Management</span></span> | <span data-ttu-id="cf67f-135">2216956</span><span class="sxs-lookup"><span data-stu-id="cf67f-135">2216956</span></span> | <span data-ttu-id="cf67f-136">Problemes corregits amb **Actualitza els preus**.</span><span class="sxs-lookup"><span data-stu-id="cf67f-136">Fixed issues with **Update prices**.</span></span> |
| <span data-ttu-id="cf67f-137">Planificació i seguiment</span><span class="sxs-lookup"><span data-stu-id="cf67f-137">Planning and Tracking</span></span> | <span data-ttu-id="cf67f-138">2182979</span><span class="sxs-lookup"><span data-stu-id="cf67f-138">2182979</span></span> | <span data-ttu-id="cf67f-139">La funció de còpia del projecte s'ha millorat per garantir que les línies de previsió de la despesa es copien del projecte original.</span><span class="sxs-lookup"><span data-stu-id="cf67f-139">Project copy function improved to ensure that expense estimate lines are copied from the original project.</span></span> |
| <span data-ttu-id="cf67f-140">Planificació i seguiment</span><span class="sxs-lookup"><span data-stu-id="cf67f-140">Planning and Tracking</span></span> | <span data-ttu-id="cf67f-141">2184144</span><span class="sxs-lookup"><span data-stu-id="cf67f-141">2184144</span></span> | <span data-ttu-id="cf67f-142">La funció de còpia del projecte s'ha millorat per garantir que el nom de posició del recurs es copia del projecte original.</span><span class="sxs-lookup"><span data-stu-id="cf67f-142">Project copy function improved to ensure the resource position name is copied from the original project.</span></span> |
| <span data-ttu-id="cf67f-143">Planificació i seguiment</span><span class="sxs-lookup"><span data-stu-id="cf67f-143">Planning and Tracking</span></span> | <span data-ttu-id="cf67f-144">2184799</span><span class="sxs-lookup"><span data-stu-id="cf67f-144">2184799</span></span> | <span data-ttu-id="cf67f-145">S'ha millorat el control en copiar un projecte per assegurar que la data d'inici prevista no es pot canviar quan la còpia està en curs.</span><span class="sxs-lookup"><span data-stu-id="cf67f-145">Tightened the control when copying a project to ensure the estimated start date can't be changed while the copy is in progress.</span></span> |
| <span data-ttu-id="cf67f-146">Planificació i seguiment</span><span class="sxs-lookup"><span data-stu-id="cf67f-146">Planning and Tracking</span></span> | <span data-ttu-id="cf67f-147">2185134</span><span class="sxs-lookup"><span data-stu-id="cf67f-147">2185134</span></span> | <span data-ttu-id="cf67f-148">Durant la còpia d'un projecte, la data d'inici prevista per al projecte de destinació es defineix a la data d'avui.</span><span class="sxs-lookup"><span data-stu-id="cf67f-148">During the copy of a project, the destination project estimated start date is set to today's date.</span></span> |
| <span data-ttu-id="cf67f-149">Planificació i seguiment</span><span class="sxs-lookup"><span data-stu-id="cf67f-149">Planning and Tracking</span></span> | <span data-ttu-id="cf67f-150">2196373</span><span class="sxs-lookup"><span data-stu-id="cf67f-150">2196373</span></span> | <span data-ttu-id="cf67f-151">S'assegura que els registres de l'administrador del projecte i dels membres de l'equip no estan duplicats a l'equip del projecte en copiar un projecte.</span><span class="sxs-lookup"><span data-stu-id="cf67f-151">Ensure project manager and team member records are not duplicated in the project team when copying a project.</span></span> |
| <span data-ttu-id="cf67f-152">Planificació i seguiment</span><span class="sxs-lookup"><span data-stu-id="cf67f-152">Planning and Tracking</span></span> | <span data-ttu-id="cf67f-153">2211833</span><span class="sxs-lookup"><span data-stu-id="cf67f-153">2211833</span></span> | <span data-ttu-id="cf67f-154">Les assignacions de recursos es copien des de la tasca de projecte d'origen al projecte de destinació.</span><span class="sxs-lookup"><span data-stu-id="cf67f-154">Resource assignments are copied from the source project task to the destination project.</span></span> |
| <span data-ttu-id="cf67f-155">Planificació i seguiment</span><span class="sxs-lookup"><span data-stu-id="cf67f-155">Planning and Tracking</span></span> | <span data-ttu-id="cf67f-156">2186541</span><span class="sxs-lookup"><span data-stu-id="cf67f-156">2186541</span></span> | <span data-ttu-id="cf67f-157">Es solucionen problemes a la quadrícula **Estimacions** en agrupar per **recurs**.</span><span class="sxs-lookup"><span data-stu-id="cf67f-157">Fixed issues in the **Estimates** grid when grouping by **Resource**.</span></span> |
| <span data-ttu-id="cf67f-158">Planificació i seguiment</span><span class="sxs-lookup"><span data-stu-id="cf67f-158">Planning and Tracking</span></span> | <span data-ttu-id="cf67f-159">2166906</span><span class="sxs-lookup"><span data-stu-id="cf67f-159">2166906</span></span> | <span data-ttu-id="cf67f-160">La categoria de transacció d'una tasca s'ha de copiar a l'entitat **Assignació de recursos**.</span><span class="sxs-lookup"><span data-stu-id="cf67f-160">The transaction category from a task must be copied to the **Resource assignment** entity.</span></span> |
| <span data-ttu-id="cf67f-161">Administració de recursos</span><span class="sxs-lookup"><span data-stu-id="cf67f-161">Resource Management</span></span> | <span data-ttu-id="cf67f-162">2125362</span><span class="sxs-lookup"><span data-stu-id="cf67f-162">2125362</span></span> | <span data-ttu-id="cf67f-163">S'han corregit problemes a l'hora de crear un membre de l'equip genèric utilitzant un mètode basat en hores.</span><span class="sxs-lookup"><span data-stu-id="cf67f-163">Fixed issues with creating a generic team member using the hours-based allocation method.</span></span> |
| <span data-ttu-id="cf67f-164">Temps i despesa</span><span class="sxs-lookup"><span data-stu-id="cf67f-164">Time and Expense</span></span> | <span data-ttu-id="cf67f-165">2113603</span><span class="sxs-lookup"><span data-stu-id="cf67f-165">2113603</span></span> | <span data-ttu-id="cf67f-166">S'ha corregit el problema relacionat amb la personalització en suprimir atributs de la pàgina **Entrada de temps**.</span><span class="sxs-lookup"><span data-stu-id="cf67f-166">Fixed customization-related issue with removing attributes from the **Time entry** page.</span></span> <span data-ttu-id="cf67f-167">El sistema comprova si l'atribut existeix a la pàgina abans d'accedir a l'atribut mitjançant un script.</span><span class="sxs-lookup"><span data-stu-id="cf67f-167">The system checks if the attribute exists on the page before accessing the attribute by using a script.</span></span> |
| <span data-ttu-id="cf67f-168">Temps i despesa</span><span class="sxs-lookup"><span data-stu-id="cf67f-168">Time and Expense</span></span> | <span data-ttu-id="cf67f-169">2204377</span><span class="sxs-lookup"><span data-stu-id="cf67f-169">2204377</span></span> | <span data-ttu-id="cf67f-170">Els fulls d'hores copiats s'han de mostrar automàticament quan seleccioneu **Copia la setmana**.</span><span class="sxs-lookup"><span data-stu-id="cf67f-170">Copied timesheets must show automatically when you select **Copy Week**.</span></span> |
| <span data-ttu-id="cf67f-171">Temps i despesa</span><span class="sxs-lookup"><span data-stu-id="cf67f-171">Time and Expense</span></span> | <span data-ttu-id="cf67f-172">2209059</span><span class="sxs-lookup"><span data-stu-id="cf67f-172">2209059</span></span> | <span data-ttu-id="cf67f-173">El camp **Estat** es pot editar per a les entrades de temps del Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="cf67f-173">The **Status** field is editable for Dynamics 365 Field Service time entries.</span></span> |