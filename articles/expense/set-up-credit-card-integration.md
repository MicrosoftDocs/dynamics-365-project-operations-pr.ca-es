---
title: Configuració de la integració amb targeta de crèdit
description: En aquest tema s'explica com treballar amb transaccions amb targetes de crèdit relacionades amb despeses.
author: suvaidya
manager: AnnBe
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 72ff98f5985af4362cde3c9914e0d20247f1f09a
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866671"
---
# <a name="set-up-credit-card-integration"></a><span data-ttu-id="1f02f-103">Configuració de la integració amb targeta de crèdit</span><span class="sxs-lookup"><span data-stu-id="1f02f-103">Set up credit card integration</span></span>

<span data-ttu-id="1f02f-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_</span><span class="sxs-lookup"><span data-stu-id="1f02f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="1f02f-105">Les transaccions de targetes de crèdit relacionades amb despeses es poden configurar de manera que s'importin automàticament segons una planificació periòdica.</span><span class="sxs-lookup"><span data-stu-id="1f02f-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="1f02f-106">Alternativament, les transaccions es poden importar manualment a mesura que es necessitin.</span><span class="sxs-lookup"><span data-stu-id="1f02f-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="1f02f-107">Les transaccions de targeta de crèdit s'importen a través de l'entitat de dades de transaccions de targeta de crèdit.</span><span class="sxs-lookup"><span data-stu-id="1f02f-107">The credit card transactions are imported through the credit card transactions data entity.</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="1f02f-108">Importació de transaccions de targeta de crèdit</span><span class="sxs-lookup"><span data-stu-id="1f02f-108">Import credit card transactions</span></span>

<span data-ttu-id="1f02f-109">Per importar transaccions de targeta de crèdit, seguiu aquests passos:</span><span class="sxs-lookup"><span data-stu-id="1f02f-109">To import credit card transactions, follow these steps:</span></span>

1. <span data-ttu-id="1f02f-110">A la pàgina **Transaccions de targeta de crèdit**, seleccioneu **Importa transaccions**.</span><span class="sxs-lookup"><span data-stu-id="1f02f-110">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="1f02f-111">Si obriu l'administració de dades per primer cop, el sistema ha d'actualitzar la llista d'entitats de dades per poder continuar.</span><span class="sxs-lookup"><span data-stu-id="1f02f-111">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="1f02f-112">Al camp **Nom**, introduïu una descripció única de la feina d'importació.</span><span class="sxs-lookup"><span data-stu-id="1f02f-112">In the **Name** field, enter a unique description for the import job.</span></span>
3. <span data-ttu-id="1f02f-113">Al camp **Format de les dades d'origen**, seleccioneu el format del fitxer que conté les transaccions de targeta de crèdit que s'importarà.</span><span class="sxs-lookup"><span data-stu-id="1f02f-113">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="1f02f-114">Seleccioneu **Carrega** i, a continuació, cerqueu i seleccioneu el fitxer que voleu importar.</span><span class="sxs-lookup"><span data-stu-id="1f02f-114">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="1f02f-115">Després d'haver carregat el fitxer, valideu l'assignació del fitxer de transaccions de targeta de crèdit i les columnes de l'entitat Dades de transaccions de targeta de crèdit seleccionant l'enllaç **Visualitza l'assignació** a la peça.</span><span class="sxs-lookup"><span data-stu-id="1f02f-115">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="1f02f-116">Si hi ha errors d'assignació o si heu de canviar l'assignació, feu els canvis de l'assignació des de la pestanya **Visualització de l'assignació** o de la pestanya **Detalls de l'assignació**.</span><span class="sxs-lookup"><span data-stu-id="1f02f-116">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="1f02f-117">Per automatitzar les transaccions amb targeta de crèdit, seleccioneu **Crea una feina de dades periòdica**.</span><span class="sxs-lookup"><span data-stu-id="1f02f-117">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="1f02f-118">A continuació, podeu definir la periodicitat que defineix amb quina freqüència s'han d'importar les transaccions de targeta de crèdit.</span><span class="sxs-lookup"><span data-stu-id="1f02f-118">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="1f02f-119">Quan hàgiu acabat, trieu **D'acord**.</span><span class="sxs-lookup"><span data-stu-id="1f02f-119">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="1f02f-120">Per importar el fitxer seleccionat ara, seleccioneu **Importa**.</span><span class="sxs-lookup"><span data-stu-id="1f02f-120">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="1f02f-121">Si s'han produït errors durant la importació, podeu visualitzar el registre d'execució o les dades intermèdies per veure els errors que heu de corregir per assegurar-vos que s'importa correctament.</span><span class="sxs-lookup"><span data-stu-id="1f02f-121">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help ensure a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="1f02f-122">Si heu d'importar més d'un format de fitxer, heu de crear feines d'importació independents per a cada tipus de format.</span><span class="sxs-lookup"><span data-stu-id="1f02f-122">If you need to import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="1f02f-123">Reassignar les transaccions de targeta de crèdit per a empleats acomiadats</span><span class="sxs-lookup"><span data-stu-id="1f02f-123">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="1f02f-124">Després d'acomiadar un registre d'empleat, el compte dels Serveis de domini de l'Active Directory (AD DS) de l'empleat està inhabilitat.</span><span class="sxs-lookup"><span data-stu-id="1f02f-124">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="1f02f-125">No obstant això, poden haver-hi transaccions de targetes de crèdit actives que s'hagin de comptabilitzar com a despeses i reemborsar.</span><span class="sxs-lookup"><span data-stu-id="1f02f-125">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="1f02f-126">A la pàgina **Transaccions de targeta de crèdit**, podeu reassignar l'empleat per a qualsevol transacció de targeta de crèdit en què l'empleat associat hagi estat acomiadat.</span><span class="sxs-lookup"><span data-stu-id="1f02f-126">On the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="1f02f-127">Seleccioneu una o més transaccions de targeta de crèdit i, a continuació, seleccioneu **Reassigna les transaccions**.</span><span class="sxs-lookup"><span data-stu-id="1f02f-127">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="1f02f-128">A continuació, podeu seleccionar un altre empleat al qual assignar les transaccions de targeta de crèdit.</span><span class="sxs-lookup"><span data-stu-id="1f02f-128">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="1f02f-129">Un cop s'hagin reassignat les transaccions de targeta de crèdit, es poden seleccionar per a un informe de despeses i pagar-se mitjançant procés habitual per al reemborsament de l'informe de despeses.</span><span class="sxs-lookup"><span data-stu-id="1f02f-129">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>

## <a name="delete-credit-card-transactions"></a><span data-ttu-id="1f02f-130">Suprimir transaccions de targeta de crèdit</span><span class="sxs-lookup"><span data-stu-id="1f02f-130">Delete credit card transactions</span></span> 

<span data-ttu-id="1f02f-131">De vegades, després d'importar transaccions de targeta de crèdit, és possible que calgui suprimir determinades transaccions.</span><span class="sxs-lookup"><span data-stu-id="1f02f-131">Sometimes, after credit card transactions are imported, certain transactions may need to be deleted.</span></span> <span data-ttu-id="1f02f-132">Això podria ser perquè les transaccions són duplicades o perquè les dades no són precises.</span><span class="sxs-lookup"><span data-stu-id="1f02f-132">This could be because the transactions are duplicates or because the data might isn't accurate.</span></span> <span data-ttu-id="1f02f-133">Els administradors poden utilitzar la característica **Suprimeix transaccions de targeta de crèdit** per seleccionar i suprimir transaccions de targeta de crèdit que no estan **adjuntades** a un informe de despeses.</span><span class="sxs-lookup"><span data-stu-id="1f02f-133">Admins can use the **"Delete credit card transactions"** feature to select and delete credit card transactions that are **not attached** to an expense report.</span></span> 

1. <span data-ttu-id="1f02f-134">Aneu a **Tasques periòdiques** > **Suprimeix transaccions de targeta de crèdit**.</span><span class="sxs-lookup"><span data-stu-id="1f02f-134">Go to **Periodic tasks** > **Delete credit card transactions**.</span></span>
2. <span data-ttu-id="1f02f-135">Seleccioneu **Filtra** i proporcioneu informació per identificar els registres que voleu incloure.</span><span class="sxs-lookup"><span data-stu-id="1f02f-135">Select **Filter** and provide information to identify the records to include.</span></span>
3. <span data-ttu-id="1f02f-136">Seleccioneu **D'acord** per suprimir els registres.</span><span class="sxs-lookup"><span data-stu-id="1f02f-136">Select **OK** to delete the records.</span></span> 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
