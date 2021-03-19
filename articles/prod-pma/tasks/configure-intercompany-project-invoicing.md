---
title: Configurar la facturació del projecte entre empreses
description: En aquest tema es mostra com configurar la facturació d'un projecte entre dues empreses de l'organització.
author: Yowelle
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, InterCompanyTradingRelationSetupVendor, SysDataAreaSelectLookup, ProjParameters, ProjPosting, ProjTransferPrice
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9df15cb3712356a164de3507f5dbc17a9ff9a652
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288367"
---
# <a name="configure-intercompany-project-invoicing"></a><span data-ttu-id="2b0d2-103">Configurar la facturació del projecte entre empreses</span><span class="sxs-lookup"><span data-stu-id="2b0d2-103">Configure intercompany project invoicing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2b0d2-104">En aquest tema es mostra com configurar la facturació d'un projecte entre dues empreses de l'organització.</span><span class="sxs-lookup"><span data-stu-id="2b0d2-104">This topic shows how to set up project invoicing between two companies in your organization.</span></span> <span data-ttu-id="2b0d2-105">Aquesta tasca utilitza el conjunt de dades d'USSI.</span><span class="sxs-lookup"><span data-stu-id="2b0d2-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="2b0d2-106">A la subfinestra de navegació, aneu a **Mòduls > Compte a pagar > Proveïdors > Tots els proveïdors**.</span><span class="sxs-lookup"><span data-stu-id="2b0d2-106">In the navigation pane, go to **Modules > Accounts payable > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="2b0d2-107">A la llista **Tots els proveïdors**, cerqueu i seleccioneu el registre que vulgueu.</span><span class="sxs-lookup"><span data-stu-id="2b0d2-107">In the **All vendors** list, find and select the desired record.</span></span>
3. <span data-ttu-id="2b0d2-108">A la subfinestra d'acció, seleccioneu **General**.</span><span class="sxs-lookup"><span data-stu-id="2b0d2-108">On the Action Pane, select **General**.</span></span>
4. <span data-ttu-id="2b0d2-109">Seleccioneu **Entre empreses**.</span><span class="sxs-lookup"><span data-stu-id="2b0d2-109">Select **Intercompany**.</span></span>
5. <span data-ttu-id="2b0d2-110">Definiu **Actiu** a **Sí** per habilitar el comerç entre empreses.</span><span class="sxs-lookup"><span data-stu-id="2b0d2-110">Set **Active** to **Yes** to enable intercompany trading.</span></span>
6. <span data-ttu-id="2b0d2-111">Al camp **Empresa del client**, introduïu o seleccioneu un valor.</span><span class="sxs-lookup"><span data-stu-id="2b0d2-111">In the **Customer company** field, enter or select a value.</span></span>
7. <span data-ttu-id="2b0d2-112">Al camp **El meu compte**, introduïu o seleccioneu un valor.</span><span class="sxs-lookup"><span data-stu-id="2b0d2-112">In the **My account** field, enter or select a value.</span></span>
8. <span data-ttu-id="2b0d2-113">Seleccioneu **Desa**.</span><span class="sxs-lookup"><span data-stu-id="2b0d2-113">Select **Save**.</span></span>
9. <span data-ttu-id="2b0d2-114">Tanqueu les pàgines per tornar a la pàgina principal.</span><span class="sxs-lookup"><span data-stu-id="2b0d2-114">Close the pages to return to the home page.</span></span>
10. <span data-ttu-id="2b0d2-115">A la subfinestra de navegació, aneu a **Mòduls > Administració de projectes i comptabilitat > Configuració > Paràmetres de l'administració de projectes i comptabilitat**.</span><span class="sxs-lookup"><span data-stu-id="2b0d2-115">In the navigation pane, go to **Modules > Project management and accounting > Setup > Project management and accounting parameters**.</span></span>
11. <span data-ttu-id="2b0d2-116">Seleccioneu la pestanya **Entre empreses**.</span><span class="sxs-lookup"><span data-stu-id="2b0d2-116">Select the **Intercompany** tab.</span></span>
12. <span data-ttu-id="2b0d2-117">Moveu el botó lliscant fins a **Sí** per habilitar la planificació de recursos entre empreses i els fulls d'hores.</span><span class="sxs-lookup"><span data-stu-id="2b0d2-117">Move the slider to **Yes** to enable intercompany resource scheduling and timesheets.</span></span>
13. <span data-ttu-id="2b0d2-118">A la llista, marqueu la fila seleccionada.</span><span class="sxs-lookup"><span data-stu-id="2b0d2-118">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="2b0d2-119">Seleccioneu **Crea**.</span><span class="sxs-lookup"><span data-stu-id="2b0d2-119">Select **New**.</span></span>
15. <span data-ttu-id="2b0d2-120">Al camp **Entitat legal prestatària**, introduïu o seleccioneu un valor.</span><span class="sxs-lookup"><span data-stu-id="2b0d2-120">In the **Borrowing legal entity** field, enter or select a value.</span></span>
16. <span data-ttu-id="2b0d2-121">Marqueu la casella de selecció **Acumula els ingressos**.</span><span class="sxs-lookup"><span data-stu-id="2b0d2-121">Select the **Accrue revenue** check box.</span></span>
17. <span data-ttu-id="2b0d2-122">Al camp **Categoria de full d'hores per defecte**, introduïu o seleccioneu un valor.</span><span class="sxs-lookup"><span data-stu-id="2b0d2-122">In the **Default timesheet category** field, enter or select a value.</span></span>
18. <span data-ttu-id="2b0d2-123">Al camp **Categoria de despesa per defecte**, introduïu o seleccioneu un valor.</span><span class="sxs-lookup"><span data-stu-id="2b0d2-123">In the **Default expense category** field, enter or select a value.</span></span>
19. <span data-ttu-id="2b0d2-124">Seleccioneu **Desa**.</span><span class="sxs-lookup"><span data-stu-id="2b0d2-124">Select **Save**.</span></span>
20. <span data-ttu-id="2b0d2-125">Tanqueu la pàgina.</span><span class="sxs-lookup"><span data-stu-id="2b0d2-125">Close the page.</span></span>
21. <span data-ttu-id="2b0d2-126">A la subfinestra de navegació, aneu a **Mòduls > Administració de projectes i comptabilitat > Configuració > Comptabilització > Configuració de la comptabilització al llibre major**.</span><span class="sxs-lookup"><span data-stu-id="2b0d2-126">In the navigation pane, go to **Modules > Project management and accounting > Setup > Posting > Ledger posting setup**.</span></span>
22. <span data-ttu-id="2b0d2-127">Al camp **Tipus de compte del registre major**, seleccioneu una opció.</span><span class="sxs-lookup"><span data-stu-id="2b0d2-127">In the **Ledger account types** field, select an option.</span></span>
23. <span data-ttu-id="2b0d2-128">Seleccioneu **Crea**.</span><span class="sxs-lookup"><span data-stu-id="2b0d2-128">Select **New**.</span></span>
24. <span data-ttu-id="2b0d2-129">Al camp **Compte principal** de la fila nova, especifiqueu els valors que vulgueu.</span><span class="sxs-lookup"><span data-stu-id="2b0d2-129">In the **Main account** field of the new row, specify the desired values.</span></span>
25. <span data-ttu-id="2b0d2-130">Seleccioneu **Desa**.</span><span class="sxs-lookup"><span data-stu-id="2b0d2-130">Select **Save**.</span></span>
26. <span data-ttu-id="2b0d2-131">Tanqueu la pàgina.</span><span class="sxs-lookup"><span data-stu-id="2b0d2-131">Close the page.</span></span>
27. <span data-ttu-id="2b0d2-132">A la subfinestra de navegació, aneu a **Mòduls > Administració de projectes i comptabilitat > Configuració > Preus > Preu de transferència**.</span><span class="sxs-lookup"><span data-stu-id="2b0d2-132">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Transfer price**.</span></span>
28. <span data-ttu-id="2b0d2-133">Seleccioneu **Crea**.</span><span class="sxs-lookup"><span data-stu-id="2b0d2-133">Select **New**.</span></span>
29. <span data-ttu-id="2b0d2-134">En el camp **Data d'efectivitat**, introduïu una data.</span><span class="sxs-lookup"><span data-stu-id="2b0d2-134">In the **Effective date** field, enter a date.</span></span>
30. <span data-ttu-id="2b0d2-135">Al camp **Entitat legal prestatària**, introduïu o seleccioneu un valor.</span><span class="sxs-lookup"><span data-stu-id="2b0d2-135">In the **Borrowing legal entity** field, enter or select a value.</span></span>
31. <span data-ttu-id="2b0d2-136">Al camp **Model del preu de transferència**, seleccioneu una opció.</span><span class="sxs-lookup"><span data-stu-id="2b0d2-136">In the **Transfer price model** field, select an option.</span></span>
32. <span data-ttu-id="2b0d2-137">Al camp **Preu**, introduïu un número.</span><span class="sxs-lookup"><span data-stu-id="2b0d2-137">In the **Pricing** field, enter a number.</span></span>
33. <span data-ttu-id="2b0d2-138">Seleccioneu **Desa**.</span><span class="sxs-lookup"><span data-stu-id="2b0d2-138">Select **Save**.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]