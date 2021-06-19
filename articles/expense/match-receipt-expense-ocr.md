---
title: Captura d'un rebut amb l'OCR
description: Aquest tema proporciona informació sobre el processament del reconeixement òptic de caràcters (OCR) per als rebuts.
author: suvaidya
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3c7fa8a805acbf7c75edd49c4c49aa159493f525
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001999"
---
# <a name="capture-a-receipt-using-ocr"></a><span data-ttu-id="1c722-103">Captura d'un rebut amb l'OCR</span><span class="sxs-lookup"><span data-stu-id="1c722-103">Capture a receipt using OCR</span></span>

<span data-ttu-id="1c722-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_</span><span class="sxs-lookup"><span data-stu-id="1c722-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="1c722-105">L'entrada de despesa s'ha millorat mitjançant la introducció del reconeixement òptic de caràcters (OCR) per al processament de rebuts.</span><span class="sxs-lookup"><span data-stu-id="1c722-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="1c722-106">Aquesta funcionalitat està dissenyada per millorar l'experiència de l'usuari en crear informes de despeses.</span><span class="sxs-lookup"><span data-stu-id="1c722-106">This functionality is designed to improve the user experience when creating expense reports.</span></span>

## <a name="key-features"></a><span data-ttu-id="1c722-107">Característiques destacades</span><span class="sxs-lookup"><span data-stu-id="1c722-107">Key features</span></span>

- <span data-ttu-id="1c722-108">El sistema extreu el nom del comerciant, la data i l'import total dels rebuts.</span><span class="sxs-lookup"><span data-stu-id="1c722-108">The system extracts the merchant name, date, and total amount from receipts.</span></span>
- <span data-ttu-id="1c722-109">El sistema tractarà de fer coincidir els rebuts no adjunts a transaccions de despeses no adjuntes.</span><span class="sxs-lookup"><span data-stu-id="1c722-109">The system will try to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="1c722-110">Podeu crear transaccions de despeses introduïdes manualment des dels rebuts.</span><span class="sxs-lookup"><span data-stu-id="1c722-110">You can create manually entered expense transactions from receipts.</span></span>

## <a name="attach-receipts-to-an-expense-report"></a><span data-ttu-id="1c722-111">Adjuntar rebuts a un informe de despeses</span><span class="sxs-lookup"><span data-stu-id="1c722-111">Attach receipts to an expense report</span></span>

<span data-ttu-id="1c722-112">Per adjuntar automàticament els rebuts que inclouen transaccions de targetes de crèdit quan es crea un informe de despeses, seguiu aquests passos.</span><span class="sxs-lookup"><span data-stu-id="1c722-112">To automatically attach receipts that include credit card transactions when an expense report is created, complete the following steps.</span></span>

  1. <span data-ttu-id="1c722-113">Obriu l'àrea de treball **Administració de despeses**.</span><span class="sxs-lookup"><span data-stu-id="1c722-113">Open the **Expense management** workspace.</span></span>
  2. <span data-ttu-id="1c722-114">A la pestanya **Rebuts**, verifiqueu que hi hagi rebuts no adjunts.</span><span class="sxs-lookup"><span data-stu-id="1c722-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="1c722-115">També podeu carregar els rebuts a la pestanya **Rebuts**.</span><span class="sxs-lookup"><span data-stu-id="1c722-115">You can also upload receipts on the **Receipts** tab.</span></span>
  3. <span data-ttu-id="1c722-116">A la pestanya **Despeses**, verifiqueu que hi hagi despeses no adjuntes.</span><span class="sxs-lookup"><span data-stu-id="1c722-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="1c722-117">Normalment, l'administrador de despeses importa aquestes despeses del proveïdor de la targeta de crèdit.</span><span class="sxs-lookup"><span data-stu-id="1c722-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
  4. <span data-ttu-id="1c722-118">Seleccioneu **Informe de despeses nou**.</span><span class="sxs-lookup"><span data-stu-id="1c722-118">Select **New expense report**.</span></span> <span data-ttu-id="1c722-119">Heu de tenir en compte que podeu incloure despeses i rebuts, ara també, quan creeu un informe de despeses.</span><span class="sxs-lookup"><span data-stu-id="1c722-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="1c722-120">Si afegiu despeses i rebuts, la coincidència automàtica dels rebuts amb les despeses s'activa.</span><span class="sxs-lookup"><span data-stu-id="1c722-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

## <a name="create-or-match-receipts-to-an-expense-report"></a><span data-ttu-id="1c722-121">Crear o fer coincidir rebuts amb un informe de despeses</span><span class="sxs-lookup"><span data-stu-id="1c722-121">Create or match receipts to an expense report</span></span>
<span data-ttu-id="1c722-122">Per crear una despesa o fer coincidir una despesa d'un rebut, seguiu els passos següents.</span><span class="sxs-lookup"><span data-stu-id="1c722-122">To create an expense, or match an expense from a receipt, complete the following steps.</span></span>

  1. <span data-ttu-id="1c722-123">A l'informe de despeses, a la pestanya **Rebuts**, adjunteu un rebut seleccionant **Afegeix rebuts**.</span><span class="sxs-lookup"><span data-stu-id="1c722-123">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
  2. <span data-ttu-id="1c722-124">A la imatge carregada del rebut, observeu les opcions **Crea** i **Fes coincidir**.</span><span class="sxs-lookup"><span data-stu-id="1c722-124">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

      - <span data-ttu-id="1c722-125">Seleccioneu **Crea** per crear una transacció de despeses introduïda manualment i empleneu els valors que s'extreuen del rebut.</span><span class="sxs-lookup"><span data-stu-id="1c722-125">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
      - <span data-ttu-id="1c722-126">Si seleccioneu **Fes coincidir**, el sistema prova de fer coincidir una despesa existent amb el justificant.</span><span class="sxs-lookup"><span data-stu-id="1c722-126">If you select **Match**, the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="1c722-127">Instal·lació</span><span class="sxs-lookup"><span data-stu-id="1c722-127">Installation</span></span>

<span data-ttu-id="1c722-128">Per utilitzar aquestes capacitats de despesa avançada, instal·leu el complement Servei d'administració de despeses per al Microsoft Dynamics 365 Finance i activeu les característiques a la instància.</span><span class="sxs-lookup"><span data-stu-id="1c722-128">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="1c722-129">Podeu accedir al complement des del projecte al Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="1c722-129">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="1c722-130">Inicieu la sessió al LCS i obriu l'entorn desitjat.</span><span class="sxs-lookup"><span data-stu-id="1c722-130">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="1c722-131">Aneu a **Detalls complets**.</span><span class="sxs-lookup"><span data-stu-id="1c722-131">Go to **Full details**.</span></span>
3. <span data-ttu-id="1c722-132">Seleccioneu **Mantén** o desplaceu-vos avall al FastTab **Complements de l'entorn**.</span><span class="sxs-lookup"><span data-stu-id="1c722-132">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="1c722-133">Seleccioneu **Instal·la un complement nou**.</span><span class="sxs-lookup"><span data-stu-id="1c722-133">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="1c722-134">Seleccioneu **Servei d'administració de despeses**.</span><span class="sxs-lookup"><span data-stu-id="1c722-134">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="1c722-135">Seguiu la guia d'instal·lació i accepteu els termes i les condicions.</span><span class="sxs-lookup"><span data-stu-id="1c722-135">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="1c722-136">Seleccioneu **Instal·la**.</span><span class="sxs-lookup"><span data-stu-id="1c722-136">Select **Install**.</span></span>

<span data-ttu-id="1c722-137">A l'àrea de treball **Administració de funcions**, activeu les característiques següents:</span><span class="sxs-lookup"><span data-stu-id="1c722-137">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="1c722-138">Informes de despeses reimaginats</span><span class="sxs-lookup"><span data-stu-id="1c722-138">Expense reports re-imagined</span></span>
- <span data-ttu-id="1c722-139">Coincidència automàtica i creació de despeses des del rebut</span><span class="sxs-lookup"><span data-stu-id="1c722-139">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="1c722-140">Quan activeu aquestes característiques es produeixen les següents accions:</span><span class="sxs-lookup"><span data-stu-id="1c722-140">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="1c722-141">L'àrea de treball **Administració de despeses** existent se substitueix per la nova àrea de treball.</span><span class="sxs-lookup"><span data-stu-id="1c722-141">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="1c722-142">S'afegirà un element de menú nou per a la visibilitat del camp de despeses.</span><span class="sxs-lookup"><span data-stu-id="1c722-142">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="1c722-143">Encara podeu obrir la pàgina **Informes de despeses** anterior anant a **Administració de despeses > Les meves despeses > Informes de despeses**.</span><span class="sxs-lookup"><span data-stu-id="1c722-143">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="1c722-144">Els fluxos de treball i les aprovacions encara us porten a la pàgina d'informes de despeses existent.</span><span class="sxs-lookup"><span data-stu-id="1c722-144">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="1c722-145">Els rebuts es processaran mitjançant el Microsoft Azure Cognitive Services i s'extrauran i s'afegiran les metadades.</span><span class="sxs-lookup"><span data-stu-id="1c722-145">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="1c722-146">S'ha afegit una opció que us permet crear un informe de despeses que inclogui rebuts coincidents no adjunts.</span><span class="sxs-lookup"><span data-stu-id="1c722-146">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="1c722-147">Una opció afegida als informes de despeses us permet crear una línia de despesa a partir d'un rebut o intenta fer coincidir un rebut existent amb una línia de despesa existent.</span><span class="sxs-lookup"><span data-stu-id="1c722-147">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="1c722-148">Preguntes més freqüents</span><span class="sxs-lookup"><span data-stu-id="1c722-148">Frequently asked questions</span></span>

<span data-ttu-id="1c722-149">**Microsoft utilitza les meves dades per als seus models?**</span><span class="sxs-lookup"><span data-stu-id="1c722-149">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="1c722-150">No, Microsoft ha creat un model d'aprenentatge automàtic general per al servei de processament de rebuts.</span><span class="sxs-lookup"><span data-stu-id="1c722-150">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="1c722-151">Aquest model no es basa en els rebuts que heu carregat.</span><span class="sxs-lookup"><span data-stu-id="1c722-151">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="1c722-152">**On està disponible i on es processa aquesta característica?**</span><span class="sxs-lookup"><span data-stu-id="1c722-152">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="1c722-153">Actualment, s'admeten els Estats Units.</span><span class="sxs-lookup"><span data-stu-id="1c722-153">Currently, the United States is supported.</span></span>

<span data-ttu-id="1c722-154">**On van els meus rebuts?**</span><span class="sxs-lookup"><span data-stu-id="1c722-154">**Where do my receipts go?**</span></span>

<span data-ttu-id="1c722-155">El Finance es posarà en contacte amb el Cognitive Services per extreure les dades dels camps.</span><span class="sxs-lookup"><span data-stu-id="1c722-155">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="1c722-156">El Cognitive Services conservarà una còpia del rebut fins a 24 hores mentre es produeix el processament.</span><span class="sxs-lookup"><span data-stu-id="1c722-156">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="1c722-157">Després de completar el processament, el Cognitive Services eliminarà el rebut.</span><span class="sxs-lookup"><span data-stu-id="1c722-157">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="1c722-158">Els rebuts es continuen emmagatzemant al Finance.</span><span class="sxs-lookup"><span data-stu-id="1c722-158">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="1c722-159">Per obtenir més informació, vegeu [Habilitar la comprensió de rebuts amb la funcionalitat nova del reconeixedor de formularis](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span><span class="sxs-lookup"><span data-stu-id="1c722-159">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
