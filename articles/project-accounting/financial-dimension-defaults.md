---
title: Valors per defecte de la dimensió financera
description: Aquest tema proporciona informació sobre com configurar els valors predeterminats de les dimensions financeres.
author: sigitac
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 0a76447bb1a81a7157fccc0cd58eddd1eb5995de
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950117"
---
# <a name="financial-dimension-defaults"></a><span data-ttu-id="b5f84-103">Valors per defecte de la dimensió financera</span><span class="sxs-lookup"><span data-stu-id="b5f84-103">Financial dimension defaults</span></span>

<span data-ttu-id="b5f84-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_</span><span class="sxs-lookup"><span data-stu-id="b5f84-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="b5f84-105">El Dynamics 365 Project Operations utilitza el marc de [dimensions financeres](/dynamics365/finance/general-ledger/financial-dimensions) del Dynamics 365 Finance per proporcionar informació addicional sobre les transaccions del subdiari del projecte i el diari general.</span><span class="sxs-lookup"><span data-stu-id="b5f84-105">Dynamics 365 Project Operations uses the [Financial dimensions](/dynamics365/finance/general-ledger/financial-dimensions) framework in Dynamics 365 Finance to provide additional insights on project subledger and general ledger transactions.</span></span>

<span data-ttu-id="b5f84-106">Les dimensions financeres predeterminades es poden establir en un client, font de finançament de projectes, fita, línia de contracte de projecte o projecte.</span><span class="sxs-lookup"><span data-stu-id="b5f84-106">Default financial dimensions can be set on a customer, project funding source, milestone, project contract line, or project.</span></span>

## <a name="define-default-financial-dimensions-for-a-customer"></a><span data-ttu-id="b5f84-107">Definir dimensions financeres per defecte per a un client</span><span class="sxs-lookup"><span data-stu-id="b5f84-107">Define default financial dimensions for a customer</span></span>

<span data-ttu-id="b5f84-108">Els valors per defecte de la dimensió del client s'especifiquen al Finance.</span><span class="sxs-lookup"><span data-stu-id="b5f84-108">Customer dimension defaults are specified in Finance.</span></span> <span data-ttu-id="b5f84-109">Completeu els passos següents per definir valors per defecte de dimensió.</span><span class="sxs-lookup"><span data-stu-id="b5f84-109">Complete the following steps to set dimension defaults.</span></span>

1. <span data-ttu-id="b5f84-110">Aneu a **Comptes a cobrar** > **Clients** > **Tots els clients**.</span><span class="sxs-lookup"><span data-stu-id="b5f84-110">Go to **Accounts receivable** > **Customers** > **All customers**.</span></span>
2. <span data-ttu-id="b5f84-111">A la pàgina **Clients**, a la pestanya **Dimensions financeres**, definiu els valors de la dimensió financera per a un client concret.</span><span class="sxs-lookup"><span data-stu-id="b5f84-111">On the **Customers** page, on the **Financial dimensions** tab, set the financial dimension values for specific customer.</span></span>

## <a name="define-default-financial-dimensions-for-project-contracts"></a><span data-ttu-id="b5f84-112">Definir dimensions financeres per defecte per a contractes de projecte</span><span class="sxs-lookup"><span data-stu-id="b5f84-112">Define default financial dimensions for project contracts</span></span>

<span data-ttu-id="b5f84-113">Els contractes de projecte es creen i es mantenen al Common Data Service (CDS).</span><span class="sxs-lookup"><span data-stu-id="b5f84-113">Project contracts are created and maintained in Common Data Service (CDS).</span></span> <span data-ttu-id="b5f84-114">Els atributs de comptabilitat dels contractes de projecte es fixen en el mòdul **Administració de projectes i comptabilitat** del Finance.</span><span class="sxs-lookup"><span data-stu-id="b5f84-114">Accounting attributes for project contracts are set in the **Project management and accounting** module in Finance.</span></span>

### <a name="set-financial-dimensions-for-a-project-funding-source"></a><span data-ttu-id="b5f84-115">Definir dimensions financeres per a una font de finançament del projecte</span><span class="sxs-lookup"><span data-stu-id="b5f84-115">Set financial dimensions for a project funding source</span></span>

1. <span data-ttu-id="b5f84-116">Aneu a **Administració de projectes i comptabilitat** > **Projectes** > **Contractes de projecte**.</span><span class="sxs-lookup"><span data-stu-id="b5f84-116">Go to **Project management and accounting** > **Projects** > **Project contracts**.</span></span>
2. <span data-ttu-id="b5f84-117">Seleccioneu el registre que voleu actualitzar i, a la pestanya **Contracte del projecte**, seleccioneu **Mostra la comptabilitat per defecte**.</span><span class="sxs-lookup"><span data-stu-id="b5f84-117">Select the record you want to update, and on the **Project contract** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="b5f84-118">Expandiu **Informació relacionada** i seleccioneu la pestanya **Fonts de finançament**.</span><span class="sxs-lookup"><span data-stu-id="b5f84-118">Expand **Related information** and select the **Funding sources** tab.</span></span>
4. <span data-ttu-id="b5f84-119">Definiu els valors per defecte de la dimensió financera.</span><span class="sxs-lookup"><span data-stu-id="b5f84-119">Set the financial dimension defaults.</span></span> <span data-ttu-id="b5f84-120">Tingueu en compte que les dimensions financeres provenen per defecte del compte de client.</span><span class="sxs-lookup"><span data-stu-id="b5f84-120">Notice that the financial dimensions default from the customer account.</span></span>

### <a name="set-financial-dimensions-for-a-project-contract-line"></a><span data-ttu-id="b5f84-121">Definir dimensions financeres per a una línia de contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="b5f84-121">Set financial dimensions for a project contract line</span></span>

1. <span data-ttu-id="b5f84-122">Aneu a **Administració de projectes i comptabilitat** > **Projectes** > **Contractes de projecte**.</span><span class="sxs-lookup"><span data-stu-id="b5f84-122">Go to **Project management and accounting** > **Projects** > **Project contracts**.</span></span>
2. <span data-ttu-id="b5f84-123">Seleccioneu el registre que voleu actualitzar i, a la pestanya **Contracte del projecte**, seleccioneu **Mostra la comptabilitat per defecte**.</span><span class="sxs-lookup"><span data-stu-id="b5f84-123">Select the record you want to update and on the **Project contract** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="b5f84-124">Expandiu **Informació relacionada** i seleccioneu la pestanya **Línies de contracte**.</span><span class="sxs-lookup"><span data-stu-id="b5f84-124">Expand **Related information** and select the **Contract lines** tab.</span></span>
4. <span data-ttu-id="b5f84-125">Definiu els valors per defecte de la dimensió financera.</span><span class="sxs-lookup"><span data-stu-id="b5f84-125">Set the financial dimension defaults.</span></span> <span data-ttu-id="b5f84-126">Els valors per defecte de la dimensió financera són aplicables i només es poden utilitzar amb línies de contracte de preu fix (fita).</span><span class="sxs-lookup"><span data-stu-id="b5f84-126">The financial dimension defaults are applicable and can be used only with Fixed price (milestone) contract lines.</span></span>

<span data-ttu-id="b5f84-127">Aquests valors per defecte s'utilitzen en les transaccions i línies de factura relacionades amb el projecte.</span><span class="sxs-lookup"><span data-stu-id="b5f84-127">These defaults are used on related project on-account transactions and invoice lines.</span></span>

## <a name="define-default-financial-dimensions-for-projects"></a><span data-ttu-id="b5f84-128">Definir dimensions financeres per defecte per a projectes</span><span class="sxs-lookup"><span data-stu-id="b5f84-128">Define default financial dimensions for projects</span></span>

<span data-ttu-id="b5f84-129">Els projectes es creen i es mantenen al CDS.</span><span class="sxs-lookup"><span data-stu-id="b5f84-129">Projects are created and maintained in CDS.</span></span> <span data-ttu-id="b5f84-130">Els atributs de comptabilitat dels projectes es fixen en el mòdul **Administració de projectes i comptabilitat** del Finance.</span><span class="sxs-lookup"><span data-stu-id="b5f84-130">Accounting attributes for projects are set in the **Project management and accounting** module in Finance.</span></span>

1. <span data-ttu-id="b5f84-131">Aneu a **Administració de projectes i comptabilitat** > **Projectes** > **Tots els projectes**.</span><span class="sxs-lookup"><span data-stu-id="b5f84-131">Go to **Project management and accounting** > **Projects** > **All projects**.</span></span>
2. <span data-ttu-id="b5f84-132">Seleccioneu el registre que voleu actualitzar i, a la pestanya **Projecte**, seleccioneu **Mostra la comptabilitat per defecte**.</span><span class="sxs-lookup"><span data-stu-id="b5f84-132">Select the record that you want to update and on the **Project** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="b5f84-133">Expandiu **Informació relacionada** i seleccioneu la pestanya **Configuració**.</span><span class="sxs-lookup"><span data-stu-id="b5f84-133">Expand **Related information** and select the **Setup** tab.</span></span>
4. <span data-ttu-id="b5f84-134">Definiu els valors per defecte de la dimensió financera.</span><span class="sxs-lookup"><span data-stu-id="b5f84-134">Set the financial dimension defaults.</span></span> <span data-ttu-id="b5f84-135">Tingueu en compte que les dimensions financeres provenen per defecte del compte de client.</span><span class="sxs-lookup"><span data-stu-id="b5f84-135">Notice that financial dimensions default from the customer account.</span></span> <span data-ttu-id="b5f84-136">Si el projecte està associat a una línia de contracte amb diversos clients del contracte del projecte, el client principal s'utilitza per obtenir les dimensions financeres per defecte.</span><span class="sxs-lookup"><span data-stu-id="b5f84-136">If the project is associated with a contract line with multiple project contract customers, the primary customer is used to default financial dimensions.</span></span>

<span data-ttu-id="b5f84-137">Les dimensions financeres per defecte del projecte s'utilitzen per definir els valors per defecte de la línia de diari per a les transaccions de temps, despeses i càrrecs al **Diari d'integració del Project Operations** i a les línies de factura del projecte relacionades.</span><span class="sxs-lookup"><span data-stu-id="b5f84-137">Project default financial dimensions are used to set journal line defaults for time, expense, and fee transactions in the **Project Operations Integration Journal** and on related project invoice lines.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]