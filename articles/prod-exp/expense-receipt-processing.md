---
title: Processament de rebuts de despeses
description: Aquest tema proporciona informació sobre el processament del reconeixement òptic de caràcters (OCR) per als rebuts. Aquesta característica està dissenyada per millorar l'experiència de l'usuari en crear informes de despeses al Microsoft Dynamics 365 Finance.
author: stsporen
manager: AnnBe
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 64901610144f9dfe274bd4c2294ab32659743a1a
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960280"
---
# <a name="expense-receipt-processing"></a><span data-ttu-id="7a163-104">Processament de rebuts de despeses</span><span class="sxs-lookup"><span data-stu-id="7a163-104">Expense receipt processing</span></span>

<span data-ttu-id="7a163-105">L'entrada de despesa s'ha millorat mitjançant la introducció del reconeixement òptic de caràcters (OCR) per al processament de rebuts.</span><span class="sxs-lookup"><span data-stu-id="7a163-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="7a163-106">Aquesta característica està dissenyada per millorar l'experiència de l'usuari en crear informes de despeses.</span><span class="sxs-lookup"><span data-stu-id="7a163-106">This feature is designed to improve the user experience when expense reports are created.</span></span>

## <a name="key-features"></a><span data-ttu-id="7a163-107">Característiques destacades</span><span class="sxs-lookup"><span data-stu-id="7a163-107">Key features</span></span>

- <span data-ttu-id="7a163-108">El nom del comerciant, la data i la quantitat total s'extreuen dels rebuts.</span><span class="sxs-lookup"><span data-stu-id="7a163-108">The merchant name, date, and total amount are extracted from receipts.</span></span>
- <span data-ttu-id="7a163-109">La característica intenta fer coincidir els rebuts no adjunts a transaccions de despeses no adjuntes.</span><span class="sxs-lookup"><span data-stu-id="7a163-109">The feature tries to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="7a163-110">Els usuaris poden crear transaccions de despeses introduïdes manualment des dels rebuts.</span><span class="sxs-lookup"><span data-stu-id="7a163-110">Users can create manually entered expense transactions from receipts.</span></span>

## <a name="usage-examples"></a><span data-ttu-id="7a163-111">Exemples d'ús</span><span class="sxs-lookup"><span data-stu-id="7a163-111">Usage examples</span></span>

<span data-ttu-id="7a163-112">Per adjuntar automàticament els rebuts que inclouen transaccions de targetes de crèdit quan es crea un informe de despeses, feu el següent:</span><span class="sxs-lookup"><span data-stu-id="7a163-112">To automatically attach receipts that include credit card transactions when an expense report is created, do the following:</span></span>

  1. <span data-ttu-id="7a163-113">Obriu l'àrea de treball **Administració de despeses**.</span><span class="sxs-lookup"><span data-stu-id="7a163-113">Open the **Expense management** workspace.</span></span>
  2. <span data-ttu-id="7a163-114">A la pestanya **Rebuts**, verifiqueu que hi hagi rebuts no adjunts.</span><span class="sxs-lookup"><span data-stu-id="7a163-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="7a163-115">També podeu carregar els rebuts a la pestanya **Rebuts**.</span><span class="sxs-lookup"><span data-stu-id="7a163-115">You can also upload receipts on the **Receipts** tab.</span></span>
  3. <span data-ttu-id="7a163-116">A la pestanya **Despeses**, verifiqueu que hi hagi despeses no adjuntes.</span><span class="sxs-lookup"><span data-stu-id="7a163-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="7a163-117">Normalment, l'administrador de despeses importa aquestes despeses del proveïdor de la targeta de crèdit.</span><span class="sxs-lookup"><span data-stu-id="7a163-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
  4. <span data-ttu-id="7a163-118">Seleccioneu **Informe de despeses nou**.</span><span class="sxs-lookup"><span data-stu-id="7a163-118">Select **New expense report**.</span></span> <span data-ttu-id="7a163-119">Heu de tenir en compte que podeu incloure despeses i rebuts, ara també, quan creeu un informe de despeses.</span><span class="sxs-lookup"><span data-stu-id="7a163-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="7a163-120">Si afegiu despeses i rebuts, la coincidència automàtica dels rebuts amb les despeses s'activa.</span><span class="sxs-lookup"><span data-stu-id="7a163-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

<span data-ttu-id="7a163-121">Per crear una despesa o fer coincidir una despesa d'un rebut, feu el següent:</span><span class="sxs-lookup"><span data-stu-id="7a163-121">To create an expense, or match an expense from a receipt, do the following:</span></span>

  1. <span data-ttu-id="7a163-122">A l'informe de despeses, a la pestanya **Rebuts**, adjunteu un rebut seleccionant **Afegeix rebuts**.</span><span class="sxs-lookup"><span data-stu-id="7a163-122">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
  2. <span data-ttu-id="7a163-123">A la imatge carregada del rebut, observeu les opcions **Crea** i **Fes coincidir**.</span><span class="sxs-lookup"><span data-stu-id="7a163-123">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

      - <span data-ttu-id="7a163-124">Seleccioneu **Crea** per crear una transacció de despeses introduïda manualment i empleneu els valors que s'extreuen del rebut.</span><span class="sxs-lookup"><span data-stu-id="7a163-124">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
      - <span data-ttu-id="7a163-125">Si seleccioneu **Fes coincidir**, el sistema prova de fer coincidir una despesa existent amb el justificant.</span><span class="sxs-lookup"><span data-stu-id="7a163-125">If you select **Match**, the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="7a163-126">Instal·lació</span><span class="sxs-lookup"><span data-stu-id="7a163-126">Installation</span></span>

<span data-ttu-id="7a163-127">Aquesta característica funciona en combinació amb la característica **Informes de despeses reinventats** per ajudar a simplificar l'experiència de despesa.</span><span class="sxs-lookup"><span data-stu-id="7a163-127">This feature works in combination with the **Expense reports re-imagined** feature to help simplify the expense experience.</span></span> <span data-ttu-id="7a163-128">Aquesta característica només està disponible per a entorns del nivell 2 o superior, que són espai aïllat i producció.</span><span class="sxs-lookup"><span data-stu-id="7a163-128">This feature is only available for Tier 2+ environments, which are Sandbox and Production.</span></span>

<span data-ttu-id="7a163-129">Per utilitzar aquestes capacitats de despesa avançada, instal·leu el complement Servei d'administració de despeses per al Microsoft Dynamics 365 Finance i activeu les característiques a la instància.</span><span class="sxs-lookup"><span data-stu-id="7a163-129">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="7a163-130">Podeu accedir al complement des del projecte al Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="7a163-130">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="7a163-131">Inicieu la sessió al LCS i obriu l'entorn desitjat.</span><span class="sxs-lookup"><span data-stu-id="7a163-131">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="7a163-132">Aneu a **Detalls complets**.</span><span class="sxs-lookup"><span data-stu-id="7a163-132">Go to **Full details**.</span></span>
3. <span data-ttu-id="7a163-133">Seleccioneu **Mantén** o desplaceu-vos avall al FastTab **Complements de l'entorn**.</span><span class="sxs-lookup"><span data-stu-id="7a163-133">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="7a163-134">Seleccioneu **Instal·la un complement nou**.</span><span class="sxs-lookup"><span data-stu-id="7a163-134">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="7a163-135">Seleccioneu **Servei d'administració de despeses**.</span><span class="sxs-lookup"><span data-stu-id="7a163-135">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="7a163-136">Seguiu la guia d'instal·lació i accepteu els termes i les condicions.</span><span class="sxs-lookup"><span data-stu-id="7a163-136">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="7a163-137">Seleccioneu **Instal·la**.</span><span class="sxs-lookup"><span data-stu-id="7a163-137">Select **Install**.</span></span>

<span data-ttu-id="7a163-138">A l'àrea de treball **Administració de funcions**, activeu les característiques següents:</span><span class="sxs-lookup"><span data-stu-id="7a163-138">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="7a163-139">Informes de despeses reimaginats</span><span class="sxs-lookup"><span data-stu-id="7a163-139">Expense reports re-imagined</span></span>
- <span data-ttu-id="7a163-140">Coincidència automàtica i creació de despeses des del rebut</span><span class="sxs-lookup"><span data-stu-id="7a163-140">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="7a163-141">Quan activeu aquestes característiques es produeixen les següents accions:</span><span class="sxs-lookup"><span data-stu-id="7a163-141">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="7a163-142">L'àrea de treball **Administració de despeses** existent se substitueix per la nova àrea de treball.</span><span class="sxs-lookup"><span data-stu-id="7a163-142">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="7a163-143">S'afegirà un element de menú nou per a la visibilitat del camp de despeses.</span><span class="sxs-lookup"><span data-stu-id="7a163-143">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="7a163-144">Encara podeu obrir la pàgina **Informes de despeses** anterior anant a **Administració de despeses > Les meves despeses > Informes de despeses**.</span><span class="sxs-lookup"><span data-stu-id="7a163-144">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="7a163-145">Els fluxos de treball i les aprovacions encara us porten a la pàgina d'informes de despeses existent.</span><span class="sxs-lookup"><span data-stu-id="7a163-145">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="7a163-146">Els rebuts es processaran mitjançant el Microsoft Azure Cognitive Services i s'extrauran i s'afegiran les metadades.</span><span class="sxs-lookup"><span data-stu-id="7a163-146">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="7a163-147">S'ha afegit una opció que us permet crear un informe de despeses que inclogui rebuts coincidents no adjunts.</span><span class="sxs-lookup"><span data-stu-id="7a163-147">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="7a163-148">Una opció afegida als informes de despeses us permet crear una línia de despesa a partir d'un rebut o intenta fer coincidir un rebut existent amb una línia de despesa existent.</span><span class="sxs-lookup"><span data-stu-id="7a163-148">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

<span data-ttu-id="7a163-149">Per a més informació sobre els informes de despeses reinventats, vegeu [Informes de despeses reinventats](ExpenseWorkspaceNew.md).</span><span class="sxs-lookup"><span data-stu-id="7a163-149">For more information about the Expense reports re-imagined feature, see [Expense reports reimagined](ExpenseWorkspaceNew.md).</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="7a163-150">Preguntes més freqüents</span><span class="sxs-lookup"><span data-stu-id="7a163-150">Frequently asked questions</span></span>

<span data-ttu-id="7a163-151">**Microsoft utilitza les meves dades per als seus models?**</span><span class="sxs-lookup"><span data-stu-id="7a163-151">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="7a163-152">No, Microsoft ha creat un model d'aprenentatge automàtic general per al servei de processament de rebuts.</span><span class="sxs-lookup"><span data-stu-id="7a163-152">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="7a163-153">Aquest model no es basa en els rebuts que heu carregat.</span><span class="sxs-lookup"><span data-stu-id="7a163-153">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="7a163-154">**On està disponible i on es processa aquesta característica?**</span><span class="sxs-lookup"><span data-stu-id="7a163-154">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="7a163-155">Actualment, s'admeten els Estats Units.</span><span class="sxs-lookup"><span data-stu-id="7a163-155">Currently, the United States is supported.</span></span>

<span data-ttu-id="7a163-156">**On van els meus rebuts?**</span><span class="sxs-lookup"><span data-stu-id="7a163-156">**Where do my receipts go?**</span></span>

<span data-ttu-id="7a163-157">El Finance es posarà en contacte amb el Cognitive Services per extreure les dades dels camps.</span><span class="sxs-lookup"><span data-stu-id="7a163-157">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="7a163-158">El Cognitive Services conservarà una còpia del rebut fins a 24 hores mentre es produeix el processament.</span><span class="sxs-lookup"><span data-stu-id="7a163-158">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="7a163-159">Després de completar el processament, el Cognitive Services eliminarà el rebut.</span><span class="sxs-lookup"><span data-stu-id="7a163-159">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="7a163-160">Els rebuts es continuen emmagatzemant al Finance.</span><span class="sxs-lookup"><span data-stu-id="7a163-160">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="7a163-161">Per obtenir més informació, vegeu [Habilitar la comprensió de rebuts amb la funcionalitat nova del reconeixedor de formularis](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span><span class="sxs-lookup"><span data-stu-id="7a163-161">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>
