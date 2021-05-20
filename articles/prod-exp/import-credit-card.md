---
title: Importació i manteniment de transaccions de targeta de crèdit
description: En aquest tema es descriu la manera d'importar i mantenir transaccions amb targetes de crèdit relacionades amb les despeses. Aquestes transaccions es poden establir de manera que s'importin automàticament segons una planificació recurrent, o es poden importar manualment quan es necessitin.
author: KimANelson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvPbsMainDataLines
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: suvaidya
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: c434356c08e8490931bd60ea5b10fe2706cb0f51
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/27/2021
ms.locfileid: "5951062"
---
# <a name="import-and-maintain-credit-card-transactions"></a><span data-ttu-id="48bcb-104">Importació i manteniment de transaccions de targeta de crèdit</span><span class="sxs-lookup"><span data-stu-id="48bcb-104">Import and maintain credit card transactions</span></span>

<span data-ttu-id="48bcb-105">Les transaccions de targetes de crèdit relacionades amb despeses es poden configurar de manera que s'importin automàticament segons una planificació periòdica.</span><span class="sxs-lookup"><span data-stu-id="48bcb-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="48bcb-106">Alternativament, les transaccions es poden importar manualment a mesura que es necessitin.</span><span class="sxs-lookup"><span data-stu-id="48bcb-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="48bcb-107">Les transaccions de targeta de crèdit s'importen a través de l'entitat Dades de transaccions de targeta de crèdit.</span><span class="sxs-lookup"><span data-stu-id="48bcb-107">The credit card transactions are imported through the Credit card transactions data entity.</span></span>

<span data-ttu-id="48bcb-108">Per a més informació sobre les entitats de dades, vegeu [Entitats de dades](/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities).</span><span class="sxs-lookup"><span data-stu-id="48bcb-108">For more information about data entities, see [Data entities](/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities).</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="48bcb-109">Importació de transaccions de targeta de crèdit</span><span class="sxs-lookup"><span data-stu-id="48bcb-109">Import credit card transactions</span></span>

1. <span data-ttu-id="48bcb-110">A la pàgina **Transaccions de targeta de crèdit**, seleccioneu **Importa transaccions**.</span><span class="sxs-lookup"><span data-stu-id="48bcb-110">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="48bcb-111">Si obriu l'administració de dades per primer cop, el sistema ha d'actualitzar la llista d'entitats de dades per poder continuar.</span><span class="sxs-lookup"><span data-stu-id="48bcb-111">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="48bcb-112">Al camp **Nom**, introduïu una descripció única de la feina d'importació.</span><span class="sxs-lookup"><span data-stu-id="48bcb-112">In the **Name** field, enter a unique description of the import job.</span></span>
3. <span data-ttu-id="48bcb-113">Al camp **Format de les dades d'origen**, seleccioneu el format del fitxer que conté les transaccions de targeta de crèdit que s'importarà.</span><span class="sxs-lookup"><span data-stu-id="48bcb-113">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="48bcb-114">Seleccioneu **Carrega** i, a continuació, cerqueu i seleccioneu el fitxer que voleu importar.</span><span class="sxs-lookup"><span data-stu-id="48bcb-114">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="48bcb-115">Després d'haver carregat el fitxer, valideu l'assignació del fitxer de transaccions de targeta de crèdit i les columnes de l'entitat Dades de transaccions de targeta de crèdit seleccionant l'enllaç **Visualitza l'assignació** a la peça.</span><span class="sxs-lookup"><span data-stu-id="48bcb-115">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the Credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="48bcb-116">Si hi ha errors d'assignació o si heu de canviar l'assignació, feu els canvis de l'assignació des de la pestanya **Visualització de l'assignació** o de la pestanya **Detalls de l'assignació**.</span><span class="sxs-lookup"><span data-stu-id="48bcb-116">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="48bcb-117">Per automatitzar les transaccions amb targeta de crèdit, seleccioneu **Crea una feina de dades periòdica**.</span><span class="sxs-lookup"><span data-stu-id="48bcb-117">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="48bcb-118">A continuació, podeu definir la periodicitat que defineix amb quina freqüència s'han d'importar les transaccions de targeta de crèdit.</span><span class="sxs-lookup"><span data-stu-id="48bcb-118">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="48bcb-119">Quan hàgiu acabat, trieu **D'acord**.</span><span class="sxs-lookup"><span data-stu-id="48bcb-119">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="48bcb-120">Per importar el fitxer seleccionat ara, seleccioneu **Importa**.</span><span class="sxs-lookup"><span data-stu-id="48bcb-120">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="48bcb-121">Si es produeixen errors durant la importació, podeu visualitzar el registre d'execució o les dades intermèdies per veure els errors que heu d'esmenar per garantir una importació correcta.</span><span class="sxs-lookup"><span data-stu-id="48bcb-121">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help guarantee a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="48bcb-122">Si heu d'importar més d'un format de fitxer, heu de crear feines d'importació independents per a cada tipus de format.</span><span class="sxs-lookup"><span data-stu-id="48bcb-122">If you must import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="48bcb-123">Reassignar les transaccions de targeta de crèdit per a empleats acomiadats</span><span class="sxs-lookup"><span data-stu-id="48bcb-123">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="48bcb-124">Després d'acomiadar un registre d'empleat, el compte dels Serveis de domini de l'Active Directory (AD DS) de l'empleat està inhabilitat.</span><span class="sxs-lookup"><span data-stu-id="48bcb-124">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="48bcb-125">No obstant això, poden haver-hi transaccions de targetes de crèdit actives que s'hagin de comptabilitzar com a despeses i reemborsar.</span><span class="sxs-lookup"><span data-stu-id="48bcb-125">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="48bcb-126">Des de la pàgina **Transaccions de targeta de crèdit**, podeu reassignar el treballador per a qualsevol transacció de targeta de crèdit en la qual s'hagi acomiadat l'empleat associat.</span><span class="sxs-lookup"><span data-stu-id="48bcb-126">From the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="48bcb-127">Seleccioneu una o més transaccions de targeta de crèdit i, a continuació, seleccioneu **Reassigna les transaccions**.</span><span class="sxs-lookup"><span data-stu-id="48bcb-127">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="48bcb-128">A continuació, podeu seleccionar un altre empleat al qual assignar les transaccions de targeta de crèdit.</span><span class="sxs-lookup"><span data-stu-id="48bcb-128">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="48bcb-129">Un cop s'hagin reassignat les transaccions de targeta de crèdit, es poden seleccionar per a un informe de despeses i pagar-se mitjançant procés habitual per al reemborsament de l'informe de despeses.</span><span class="sxs-lookup"><span data-stu-id="48bcb-129">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]