---
title: Administració de les estimacions d'ingressos
description: En aquest tema es proporciona informació sobre com treballar amb estimacions d'ingressos per a projectes.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 98df0301eaa8e9f8e9cd51fc5714254ae3bbc83d
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531363"
---
# <a name="manage-revenue-estimates"></a><span data-ttu-id="f53ac-103">Administració de les estimacions d'ingressos</span><span class="sxs-lookup"><span data-stu-id="f53ac-103">Manage revenue estimates</span></span>

<span data-ttu-id="f53ac-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_</span><span class="sxs-lookup"><span data-stu-id="f53ac-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="f53ac-105">Podeu crear, calcular, comptabilitzar, revertir o suprimir estimacions d'ingressos.</span><span class="sxs-lookup"><span data-stu-id="f53ac-105">You can create, calculate, post, reverse, or eliminate revenue estimates.</span></span> <span data-ttu-id="f53ac-106">Podeu fer-ho manualment o mitjançant un procés periòdic.</span><span class="sxs-lookup"><span data-stu-id="f53ac-106">You can do this either manually or by using a periodic process.</span></span> <span data-ttu-id="f53ac-107">En aquest tema es proporciona informació sobre com treballar amb estimacions d'ingressos per a projectes.</span><span class="sxs-lookup"><span data-stu-id="f53ac-107">This topic provides information about how to work with revenue estimates for projects.</span></span>

### <a name="manage-revenue-estimates-manually"></a><span data-ttu-id="f53ac-108">Administració manual d'estimacions d'ingressos</span><span class="sxs-lookup"><span data-stu-id="f53ac-108">Manage revenue estimates manually</span></span>

<span data-ttu-id="f53ac-109">Al projecte d'estimació d'ingressos de preu fix o a la pàgina **Consulta d'estimació** (**Gestió de projectes i comptabilitat** > **Informes i consultes** > **Consultes d'estimacions i informes**), seleccioneu **Estimacions**.</span><span class="sxs-lookup"><span data-stu-id="f53ac-109">On the fixed price revenue estimate project or the **Estimate inquiry** page (**Project management and accounting** > **Reports and inquiries** > **Estimates inquiries and reports**), select **Estimates**.</span></span>

### <a name="manage-revenue-estimates-using-a-periodic-process"></a><span data-ttu-id="f53ac-110">Administració d'estimacions d'ingressos mitjançant un procés periòdic</span><span class="sxs-lookup"><span data-stu-id="f53ac-110">Manage revenue estimates using a periodic process</span></span>

<span data-ttu-id="f53ac-111">Aneu a **Gestió de projectes i comptabilitat** > **Periòdic** > **Estimacions** i seleccioneu el procés corresponent.</span><span class="sxs-lookup"><span data-stu-id="f53ac-111">Go to **Project management and accounting** > **Periodic** > **Estimates** and select the corresponding process.</span></span>

## <a name="create-a-revenue-estimate"></a><span data-ttu-id="f53ac-112">Crear una estimació d'ingressos</span><span class="sxs-lookup"><span data-stu-id="f53ac-112">Create a revenue estimate</span></span>

<span data-ttu-id="f53ac-113">Per crear una estimació d'ingressos, completeu els passos següents.</span><span class="sxs-lookup"><span data-stu-id="f53ac-113">Complete the following steps to create a revenue estimate.</span></span> 

1. <span data-ttu-id="f53ac-114">Aneu a **Gestió de projectes i comptabilitat** > **Periòdic** > **Estimacions**.</span><span class="sxs-lookup"><span data-stu-id="f53ac-114">Go to **Project management and accounting** > **Periodic** > **Estimates**.</span></span>
2. <span data-ttu-id="f53ac-115">Seleccioneu **Crea**.</span><span class="sxs-lookup"><span data-stu-id="f53ac-115">Select **New**.</span></span> <span data-ttu-id="f53ac-116">A la pàgina **Creació d'estimació**, seleccioneu els paràmetres següents:</span><span class="sxs-lookup"><span data-stu-id="f53ac-116">On the **Estimate creation** page, select the following parameters:</span></span>

   - <span data-ttu-id="f53ac-117">**Codi de període**: aquest codi determina amb quina freqüència es publiquen les estimacions.</span><span class="sxs-lookup"><span data-stu-id="f53ac-117">**Period code**: This code determines how frequently estimates are posted.</span></span>
   - <span data-ttu-id="f53ac-118">**Data d'estimació**: data de processament de l'estimació.</span><span class="sxs-lookup"><span data-stu-id="f53ac-118">**Estimate date**: The date the estimate is processed.</span></span>
   - <span data-ttu-id="f53ac-119">**Contínua**: activeu aquesta casella de selecció per crear estimacions només si les estimacions s'han publicat en el període anterior, o si l'estimació és la primera estimació que s'ha creat.</span><span class="sxs-lookup"><span data-stu-id="f53ac-119">**Continuous**: Select this check box to create estimates only if estimates were posted in the previous period, or if the estimate is the first estimate that has been created.</span></span> <span data-ttu-id="f53ac-120">Si no se selecciona, es creen estimacions encara que les estimacions no s'hagin publicat en el període anterior.</span><span class="sxs-lookup"><span data-stu-id="f53ac-120">If this is not selected, estimates are created even if estimates were not posted in the previous period.</span></span>
   - <span data-ttu-id="f53ac-121">**Mètode de cost per completar**: definiu com calcular el treball restant del projecte.</span><span class="sxs-lookup"><span data-stu-id="f53ac-121">**Cost to complete method**: Define how to estimate the remaining project work.</span></span> <span data-ttu-id="f53ac-122">Per obtenir més informació, vegeu [Mètodes de cost per completar](cost-complete-methods.md).</span><span class="sxs-lookup"><span data-stu-id="f53ac-122">For more information, see [Cost to complete methods](cost-complete-methods.md).</span></span>
   - <span data-ttu-id="f53ac-123">**Mètode de compleció**: seleccioneu un mètode de compleció de les opcions següents:</span><span class="sxs-lookup"><span data-stu-id="f53ac-123">**Completion method**: Select a completion method from the following options:</span></span>
     - <span data-ttu-id="f53ac-124">**Automàtic**: el percentatge de compleció es calcula automàticament i es basa en les línies de cost incloses en el càlcul.</span><span class="sxs-lookup"><span data-stu-id="f53ac-124">**Automatic**: The completion percentage is calculated automatically and based on the cost lines included in the calculation.</span></span> <span data-ttu-id="f53ac-125">La plantilla de cost defineix les línies de cost que s'inclouen.</span><span class="sxs-lookup"><span data-stu-id="f53ac-125">The cost template defines the cost lines that are included.</span></span>
     - <span data-ttu-id="f53ac-126">**Manual**: el percentatge de compleció és igual al percentatge de compleció de l'última estimació.</span><span class="sxs-lookup"><span data-stu-id="f53ac-126">**Manual**: The completion percentage equals the completion percentage of the last estimate.</span></span> <span data-ttu-id="f53ac-127">Un cop creada l'estimació, podeu canviar el **Càlcul manual** a la pàgina **Estimacions**.</span><span class="sxs-lookup"><span data-stu-id="f53ac-127">After the estimate is created, you can change the **Manual calculation** on the **Estimates** page.</span></span>
     - <span data-ttu-id="f53ac-128">**A partir de la plantilla de cost**: una combinació dels mètodes automàtic i manual.</span><span class="sxs-lookup"><span data-stu-id="f53ac-128">**From cost template**: A combination of the automatic and manual methods.</span></span> <span data-ttu-id="f53ac-129">Aquesta opció s'estableix automàticament o manualment, depenent del valor per defecte de la plantilla de costos.</span><span class="sxs-lookup"><span data-stu-id="f53ac-129">This option is set automatically or manually, depending on the default value in the cost template.</span></span>
   - <span data-ttu-id="f53ac-130">**Model de predicció**: seleccioneu un model de predicció per a l'estimació.</span><span class="sxs-lookup"><span data-stu-id="f53ac-130">**Forecast model**: Select a forecast model for the estimate.</span></span>
   - <span data-ttu-id="f53ac-131">**Imprimir llista d'estimació**: creeu i mostreu una llista d'estimació.</span><span class="sxs-lookup"><span data-stu-id="f53ac-131">**Print estimate list**: Create and show an estimate list.</span></span> <span data-ttu-id="f53ac-132">La llista conté l'estat de la funció actual.</span><span class="sxs-lookup"><span data-stu-id="f53ac-132">The list contains the status of the current function.</span></span> <span data-ttu-id="f53ac-133">Podeu imprimir els advertiments sobre l'estimació de l'informe.</span><span class="sxs-lookup"><span data-stu-id="f53ac-133">You can print any warnings about the estimate on the report.</span></span> <span data-ttu-id="f53ac-134">Les condicions següents fan que apareguin advertiments a la llista d'estimació:</span><span class="sxs-lookup"><span data-stu-id="f53ac-134">The following conditions cause warnings to appear in the estimate list:</span></span>
     - <span data-ttu-id="f53ac-135">Un percentatge completat de més del 100 per cent.</span><span class="sxs-lookup"><span data-stu-id="f53ac-135">A completion percentage of more than 100 percent.</span></span>
     - <span data-ttu-id="f53ac-136">Un percentatge completat de menys del zero per cent.</span><span class="sxs-lookup"><span data-stu-id="f53ac-136">A completion percentage less than zero percent.</span></span>
     - <span data-ttu-id="f53ac-137">Una quantitat negativa a la columna **Per completar**.</span><span class="sxs-lookup"><span data-stu-id="f53ac-137">A negative amount in the **To complete** column.</span></span>
     - <span data-ttu-id="f53ac-138">Una estimació sense l'import del contracte corresponent.</span><span class="sxs-lookup"><span data-stu-id="f53ac-138">An estimate with no corresponding contract amount.</span></span>
     - <span data-ttu-id="f53ac-139">Una estimació sense una estimació de costos adjunta.</span><span class="sxs-lookup"><span data-stu-id="f53ac-139">An estimate with no attached cost estimate.</span></span>
   - <span data-ttu-id="f53ac-140">**Mostra Infolog**: seleccioneu aquesta opció per rebre un missatge que contingui informació sobre els projectes d'estimació que s'han processat quan s'ha executat la feina.</span><span class="sxs-lookup"><span data-stu-id="f53ac-140">**Show Infolog**: Select this option to receive a message that contains information about the estimate projects that were processed when the job was run.</span></span>


## <a name="post-wip-or-accruals"></a><span data-ttu-id="f53ac-141">Publicar WIP o meritacions</span><span class="sxs-lookup"><span data-stu-id="f53ac-141">Post WIP or accruals</span></span>

<span data-ttu-id="f53ac-142">Després de l'avaluació, les estimacions es mantenen, disminueixen o augmenten.</span><span class="sxs-lookup"><span data-stu-id="f53ac-142">After the estimates are evaluated, they are maintained, decreased, or increased.</span></span> <span data-ttu-id="f53ac-143">A continuació, podeu publicar la WIP quan treballeu amb el principi d'avaluació de **Contracte completat** o publicar les meritacions quan treballeu amb el principi d'avaluació de **Percentatge completat**.</span><span class="sxs-lookup"><span data-stu-id="f53ac-143">You can then post the WIP when you work with the **Completed contract** assessment principle, or post the accruals when you work with the **Completed percentage** assessment principle.</span></span>
  
<span data-ttu-id="f53ac-144">L'estat del període d'estimació canvia de **Creat** a **Publicat**.</span><span class="sxs-lookup"><span data-stu-id="f53ac-144">The estimate period status changes from **Created** to **Posted**.</span></span>

## <a name="reverse-wip-or-accruals"></a><span data-ttu-id="f53ac-145">Revertir WIP o meritacions</span><span class="sxs-lookup"><span data-stu-id="f53ac-145">Reverse WIP or accruals</span></span>

<span data-ttu-id="f53ac-146">Utilitzeu l'opció de revertir per abonar WIP o meritacions ja publicades i, a continuació, creeu estimacions per al període.</span><span class="sxs-lookup"><span data-stu-id="f53ac-146">Use the reverse option to credit already posted WIP or accruals, and then create estimates for the period.</span></span>

> [!NOTE]
> <span data-ttu-id="f53ac-147">Per revertir un període que es troba entre altres períodes, revertiu els períodes d'estimació necessaris i, a continuació, torneu-los a publicar.</span><span class="sxs-lookup"><span data-stu-id="f53ac-147">To reverse a period that is in between other periods, reverse the necessary estimate periods and then repost them.</span></span> <span data-ttu-id="f53ac-148">Com que tots els períodes posteriors depenen de les estimacions del període anterior, no se salta cap període.</span><span class="sxs-lookup"><span data-stu-id="f53ac-148">Because all subsequent periods depend on the estimates from the previous period, don't skip any periods.</span></span>

## <a name="eliminate-the-estimate-project-and-finish-the-project"></a><span data-ttu-id="f53ac-149">Suprimir el projecte d'estimació i acabar el projecte</span><span class="sxs-lookup"><span data-stu-id="f53ac-149">Eliminate the estimate project and finish the project</span></span>

<span data-ttu-id="f53ac-150">L'últim pas en el procés d'estimació és suprimir el projecte d'estimació i acabar el projecte de preu fix quan el percentatge d'acabament arriba al 100 per cent.</span><span class="sxs-lookup"><span data-stu-id="f53ac-150">The final step in the estimate process is to eliminate the estimate project and end the fixed price project when the percentage of completion reaches 100 percent.</span></span>

<span data-ttu-id="f53ac-151">El següent es produeix quan s'executa la supressió:</span><span class="sxs-lookup"><span data-stu-id="f53ac-151">The following occurs when you run the elimination:</span></span>

- <span data-ttu-id="f53ac-152">Per a un projecte de preu fix amb un contracte completat, els valors de WIP s'esborren dels balanços i es publiquen als comptes de pèrdues i guanys.</span><span class="sxs-lookup"><span data-stu-id="f53ac-152">For a fixed price project with a completed contract, the WIP values clear from the balance accounts and post to the profit and loss accounts.</span></span>
- <span data-ttu-id="f53ac-153">Per a un projecte de preu fix que tingui un percentatge completat, les meritacions s'eliminen dels comptes de pèrdues i guanys.</span><span class="sxs-lookup"><span data-stu-id="f53ac-153">For a fixed-price project with a completed percentage, the accruals are removed from the profit and loss accounts.</span></span>

<span data-ttu-id="f53ac-154">L'estimació canvia l'estat per **Eliminat**.</span><span class="sxs-lookup"><span data-stu-id="f53ac-154">The estimate changes the status to **Eliminated**.</span></span>

> [!NOTE]
> <span data-ttu-id="f53ac-155">En casos especials, el percentatge pot prolongar-se més enllà del 100 per cent.</span><span class="sxs-lookup"><span data-stu-id="f53ac-155">In special cases, the percentage can extend beyond 100 percent.</span></span> <span data-ttu-id="f53ac-156">Quan això passi, reduïu el percentatge completat mitjançant el **Mètode de cost per completar a zero** per arribar al 100 per cent.</span><span class="sxs-lookup"><span data-stu-id="f53ac-156">When this happens, reduce the percentage of completion by using the **Set cost to complete to zero method** to reach 100 percent.</span></span>

## <a name="reverse-elimination"></a><span data-ttu-id="f53ac-157">Revertir supressió</span><span class="sxs-lookup"><span data-stu-id="f53ac-157">Reverse elimination</span></span>

1. <span data-ttu-id="f53ac-158">Aneu a **Gestió de projectes i comptabilitat** > **Periòdic** > **Estimacions** > **Revertir supressió**.</span><span class="sxs-lookup"><span data-stu-id="f53ac-158">Go to **Project management and accounting** > **Periodic** > **Estimates** > **Reverse elimination**.</span></span> 
2. <span data-ttu-id="f53ac-159">A la subfinestra Acció, a la pestanya **Procés**, al grup **Manteniment**, seleccioneu **Estimació**.</span><span class="sxs-lookup"><span data-stu-id="f53ac-159">On the Action Pane, on the **Process** tab, in the **Maintain** group, select **Estimate**.</span></span> 
3. <span data-ttu-id="f53ac-160">Seleccioneu **Revertir supressió**.</span><span class="sxs-lookup"><span data-stu-id="f53ac-160">Select **Reverse elimination**.</span></span>

<span data-ttu-id="f53ac-161">Utilitzeu aquesta pàgina per revertir totes les supressions amb una data d'estimació especificada i amb un estat d'estimació de **Suprimit**.</span><span class="sxs-lookup"><span data-stu-id="f53ac-161">Use this page to reverse all eliminations with a specified estimate date and with an estimate status of **Eliminated**.</span></span> <span data-ttu-id="f53ac-162">L'estat de la transacció canvia després de seleccionar els camps apropiats.</span><span class="sxs-lookup"><span data-stu-id="f53ac-162">The transaction status changes after you select the appropriate fields.</span></span>

<span data-ttu-id="f53ac-163">Això també canvia automàticament l'estat del projecte per **En procés** si la fase del projecte està definida com a acabada.</span><span class="sxs-lookup"><span data-stu-id="f53ac-163">This also automatically changes the project status to **In process** if the project stage is set to finished.</span></span> <span data-ttu-id="f53ac-164">L'estat de l'estimació del període de projecte canvia a **Publicat**.</span><span class="sxs-lookup"><span data-stu-id="f53ac-164">The estimate status of the project period changes back to **Posted**.</span></span>
