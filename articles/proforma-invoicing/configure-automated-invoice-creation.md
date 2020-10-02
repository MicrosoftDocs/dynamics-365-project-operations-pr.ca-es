---
title: Configuració de la creació de factures automàtica
description: En aquest tema es proporciona informació sobre com configurar el sistema per generar factures de manera automàtica.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: 764fd4568619e4f5676ee3cbf7fce14ffb069548
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898114"
---
# <a name="configure-automated-invoice-creation"></a><span data-ttu-id="35bd0-103">Configuració de la creació de factures automàtica</span><span class="sxs-lookup"><span data-stu-id="35bd0-103">Configure automated invoice creation</span></span>

<span data-ttu-id="35bd0-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_</span><span class="sxs-lookup"><span data-stu-id="35bd0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="35bd0-105">Seguiu aquests passos per configurar una execució de factura automàtica al Project Operations.</span><span class="sxs-lookup"><span data-stu-id="35bd0-105">Complete the following steps to configure an automated invoice run in Project operations.</span></span>

1. <span data-ttu-id="35bd0-106">Aneu a **Configuració** \> **Treballs per lots**.</span><span class="sxs-lookup"><span data-stu-id="35bd0-106">Go to **Settings** \> **Batch jobs**.</span></span>
2. <span data-ttu-id="35bd0-107">Creeu un treball per lots i anomeneu-lo **Creació de factures del Project Operations**.</span><span class="sxs-lookup"><span data-stu-id="35bd0-107">Create a batch job, and name it **Project operations create invoices**.</span></span> <span data-ttu-id="35bd0-108">El nom del treball per lots ha d'incloure el terme "Creació de factures".</span><span class="sxs-lookup"><span data-stu-id="35bd0-108">The name of the batch job must include the term "create invoices."</span></span>
3. <span data-ttu-id="35bd0-109">Al camp **Tipus de treball**, seleccioneu **Cap**.</span><span class="sxs-lookup"><span data-stu-id="35bd0-109">In the **Job type** field, select **None**.</span></span> <span data-ttu-id="35bd0-110">Per defecte, les opcions **Freqüència diària** i **Actiu** estan definides com a **Sí**.</span><span class="sxs-lookup"><span data-stu-id="35bd0-110">By default, the **Frequency Daily** and **Is Active** options are set to **Yes**.</span></span>
4. <span data-ttu-id="35bd0-111">Seleccioneu **Executa el flux de treball**.</span><span class="sxs-lookup"><span data-stu-id="35bd0-111">Select **Run Workflow**.</span></span> <span data-ttu-id="35bd0-112">Al quadre de diàleg **Registre de cerca**, veureu tres fluxos de treball:</span><span class="sxs-lookup"><span data-stu-id="35bd0-112">In the **Look Up Record** dialog box, you will see three workflows:</span></span>

    - <span data-ttu-id="35bd0-113">ProcessRunCaller</span><span class="sxs-lookup"><span data-stu-id="35bd0-113">ProcessRunCaller</span></span>
    - <span data-ttu-id="35bd0-114">ProcessRunner</span><span class="sxs-lookup"><span data-stu-id="35bd0-114">ProcessRunner</span></span>
    - <span data-ttu-id="35bd0-115">UpdateRoleUtilization</span><span class="sxs-lookup"><span data-stu-id="35bd0-115">UpdateRoleUtilization</span></span>

5. <span data-ttu-id="35bd0-116">Seleccioneu **ProcessRunCaller** i després trieu **Afegeix**.</span><span class="sxs-lookup"><span data-stu-id="35bd0-116">Select **ProcessRunCaller**, and then select **Add**.</span></span>
6. <span data-ttu-id="35bd0-117">Al quadre de diàleg següent, seleccioneu **D'acord**.</span><span class="sxs-lookup"><span data-stu-id="35bd0-117">In the next dialog box, select **OK**.</span></span> <span data-ttu-id="35bd0-118">Un flux de treball **Repòs** va seguit d'un flux de treball **Procés**.</span><span class="sxs-lookup"><span data-stu-id="35bd0-118">A **Sleep** workflow is followed by a **Process** workflow.</span></span>

    <span data-ttu-id="35bd0-119">També podeu seleccionar **ProcessRunner** al pas 5.</span><span class="sxs-lookup"><span data-stu-id="35bd0-119">You can also select **ProcessRunner** in step 5.</span></span> <span data-ttu-id="35bd0-120">Després, quan seleccioneu **D'acord**, un flux de treball **Procés** va seguit d'un flux de treball **Repòs**.</span><span class="sxs-lookup"><span data-stu-id="35bd0-120">Then, when you select **OK**, a **Process** workflow is followed by a **Sleep** workflow.</span></span>

<span data-ttu-id="35bd0-121">Els fluxos de treball **ProcessRunCaller** i **ProcessRunner** creen factures.</span><span class="sxs-lookup"><span data-stu-id="35bd0-121">The **ProcessRunCaller** and **ProcessRunner** workflows create invoices.</span></span> <span data-ttu-id="35bd0-122">**ProcessRunCaller** crida a **ProcessRunner**.</span><span class="sxs-lookup"><span data-stu-id="35bd0-122">**ProcessRunCaller** calls **ProcessRunner**.</span></span> <span data-ttu-id="35bd0-123">**ProcessRunner** és el flux de treball que en realitat crea les factures.</span><span class="sxs-lookup"><span data-stu-id="35bd0-123">**ProcessRunner** is the workflow that actually creates the invoices.</span></span> <span data-ttu-id="35bd0-124">Passa per totes les línies de contracte per a les quals s'han de crear factures i crea factures d'aquestes línies.</span><span class="sxs-lookup"><span data-stu-id="35bd0-124">It goes through all the contract lines that invoices must be created for, and it creates invoices for those lines.</span></span> <span data-ttu-id="35bd0-125">Per determinar les línies de contracte per a les quals s'han de crear factures, el treball consulta les dates d'execució de la factura per a les línies de contracte.</span><span class="sxs-lookup"><span data-stu-id="35bd0-125">To determine the contract lines that invoices must be created for, the job looks at invoice run dates for the contract lines.</span></span> <span data-ttu-id="35bd0-126">Si les línies de contracte que pertanyen a un contracte tenen la mateixa data d'execució de la factura, les transaccions es combinen en una factura que té dues línies de factura.</span><span class="sxs-lookup"><span data-stu-id="35bd0-126">If contract lines that belong to one contract have the same invoice run date, the transactions are combined into one invoice that has two invoice lines.</span></span> <span data-ttu-id="35bd0-127">Si no hi ha cap transacció per a la qual crear factures, el treball omet la creació de la factura.</span><span class="sxs-lookup"><span data-stu-id="35bd0-127">If there are no transactions to create invoices for, the job skips invoice creation.</span></span>

<span data-ttu-id="35bd0-128">Després d'haver acabat d'executar-se **ProcessRunner**, crida a **ProcessRunCaller**, proporciona l'hora d'acabament i es tanca.</span><span class="sxs-lookup"><span data-stu-id="35bd0-128">After **ProcessRunner** has finished running, it calls **ProcessRunCaller**, provides the end time, and is closed.</span></span> <span data-ttu-id="35bd0-129">**ProcessRunCaller** llavors inicia un temporitzador que s'executa durant 24 hores a partir de l'hora d'acabament especificada.</span><span class="sxs-lookup"><span data-stu-id="35bd0-129">**ProcessRunCaller** then starts a timer that runs for 24 hours from the specified end time.</span></span> <span data-ttu-id="35bd0-130">Al final del temporitzador, **ProcessRunCaller** es tanca.</span><span class="sxs-lookup"><span data-stu-id="35bd0-130">At the end of the timer, **ProcessRunCaller** is closed.</span></span>

<span data-ttu-id="35bd0-131">El treball de processament per lots per crear factures és una feina recurrent.</span><span class="sxs-lookup"><span data-stu-id="35bd0-131">The batch process job for creating invoices is a recurrent job.</span></span> <span data-ttu-id="35bd0-132">Si aquest procés per lots s'executa moltes vegades, es creen diverses instàncies del treball que causen errors.</span><span class="sxs-lookup"><span data-stu-id="35bd0-132">If this batch process is run many times, multiple instances of the job are created and cause errors.</span></span> <span data-ttu-id="35bd0-133">Per tant, hauríeu d'iniciar el procés de processament per lots només una vegada i reiniciar-lo només si s'atura l'execució.</span><span class="sxs-lookup"><span data-stu-id="35bd0-133">Therefore, you should start the batch process only one time, and you should restart it only if it stops running.</span></span>

> [!NOTE]
> <span data-ttu-id="35bd0-134">La facturació per lots només s'executa per a les línies de contracte del projecte que es configuren mitjançant planificacions de factura.</span><span class="sxs-lookup"><span data-stu-id="35bd0-134">Batch invoicing only runs for project contract lines that are configured by invoice schedules.</span></span> <span data-ttu-id="35bd0-135">Una línia de contracte amb un mètode de facturació de preu fix ha de tenir les fites configurades.</span><span class="sxs-lookup"><span data-stu-id="35bd0-135">A contract line with a fixed price billing method must have milestones configured.</span></span> <span data-ttu-id="35bd0-136">Una línia de contracte de projecte amb un mètode de facturació de temps i material necessitarà una configuració de planificació de facturació basada en la data.</span><span class="sxs-lookup"><span data-stu-id="35bd0-136">A project contract line with a time and material billing method will need a date-based invoice schedule set up.</span></span> <span data-ttu-id="35bd0-137">El mateix s'aplica a una línia de contracte basada en projectes.</span><span class="sxs-lookup"><span data-stu-id="35bd0-137">The same applies to a project-based contract line.</span></span>     
