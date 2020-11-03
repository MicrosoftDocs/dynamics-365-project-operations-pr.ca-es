---
title: Configuració de categories del projecte
description: Aquest tema proporciona informació sobre la configuració de categories de projectes.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 84033182ce047d230724409eef9bc6afcaefd2b4
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072108"
---
# <a name="configure-project-categories"></a><span data-ttu-id="60977-103">Configuració de categories del projecte</span><span class="sxs-lookup"><span data-stu-id="60977-103">Configure project categories</span></span>

<span data-ttu-id="60977-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_</span><span class="sxs-lookup"><span data-stu-id="60977-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="60977-105">El Project Operations ofereix capacitats robustes per categoritzar ingressos i despeses als projectes.</span><span class="sxs-lookup"><span data-stu-id="60977-105">Project Operations offers robust capabilities for categorizing revenue and expenses on projects.</span></span> <span data-ttu-id="60977-106">Les categories proporcionen la capacitat d'informar i analitzar les transaccions de projectes i impulsar la comptabilització al llibre major.</span><span class="sxs-lookup"><span data-stu-id="60977-106">Categories provide the ability to report on and analyze project transactions, and drive posting to the general ledger.</span></span>

<span data-ttu-id="60977-107">El diagrama següent il·lustra la correlació entre categories de transaccions, categories compartides i categories de projectes.</span><span class="sxs-lookup"><span data-stu-id="60977-107">The following diagram illustrates the correlation between transaction categories, shared categories, and project categories.</span></span> 

<span data-ttu-id="60977-108">Les categories de transacció són l'agrupament bàsic per a transaccions de projectes.</span><span class="sxs-lookup"><span data-stu-id="60977-108">Transaction categories are the basic grouping for project transactions.</span></span> <span data-ttu-id="60977-109">Dins d'aquest agrupament, hi ha un conjunt de categories compartides que es poden compartir entre aplicacions i mòduls.</span><span class="sxs-lookup"><span data-stu-id="60977-109">Within that grouping, there is a set of shared categories that can be shared across applications and modules.</span></span> <span data-ttu-id="60977-110">De manera més específica, les categories de projectes són el nivell de categoria més granular.</span><span class="sxs-lookup"><span data-stu-id="60977-110">Getting even further into specifics, project categories are the most granular level of categories.</span></span> <span data-ttu-id="60977-111">Les categories de projecte són especifiques per a l'entitat legal, el mòdul i l'aplicació.</span><span class="sxs-lookup"><span data-stu-id="60977-111">Project categories are specific to legal entity, module, and application.</span></span>

![Correlació entre categories de transaccions, categories compartides i categories de projectes](media/project-categories.png)

## <a name="transaction-categories"></a><span data-ttu-id="60977-113">Categories de transacció</span><span class="sxs-lookup"><span data-stu-id="60977-113">Transaction categories</span></span>

<span data-ttu-id="60977-114">Les categories de transacció representen l'agrupament bàsic per a transaccions de projectes i no són específiques de l'empresa ni del tipus de transacció.</span><span class="sxs-lookup"><span data-stu-id="60977-114">Transaction categories represent the basic grouping for project transactions and are not company or transaction type-specific.</span></span> <span data-ttu-id="60977-115">Per exemple, Contoso Robotics utilitza categories de disseny, viatges, instal·lació i transacció de servei per agrupar les transaccions de projectes.</span><span class="sxs-lookup"><span data-stu-id="60977-115">For example, Contoso Robotics uses Design, Travel, Installation, and Service Transaction categories to group Project transactions.</span></span>

<span data-ttu-id="60977-116">Les categories de transaccions es defineixen al mòdul Project Operations.</span><span class="sxs-lookup"><span data-stu-id="60977-116">Transaction categories are defined in the Project Operations module.</span></span> 
1. <span data-ttu-id="60977-117">Aneu a **Configuració** \> **Categories de transaccions** per obrir el formulari.</span><span class="sxs-lookup"><span data-stu-id="60977-117">Go to **Settings** \> **Transaction Categories** to open the form.</span></span> 
2. <span data-ttu-id="60977-118">Creeu una categoria de transacció nova seleccionant **Nou** o seleccionant **Importa des de l'Excel**.</span><span class="sxs-lookup"><span data-stu-id="60977-118">Create a new transaction category either by selecting **New** or by selecting **Import from Excel**.</span></span>

## <a name="shared-categories"></a><span data-ttu-id="60977-119">Categories compartides</span><span class="sxs-lookup"><span data-stu-id="60977-119">Shared categories</span></span>

<span data-ttu-id="60977-120">El Dynamics 365 utilitza el concepte de categories compartides per categoritzar les despeses d'aplicacions diferents, com ara el Dynamics 365 Finance, el Dynamics 365 Supply Chain i el Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="60977-120">Dynamics 365 uses the Shared categories concept to categorize expenses in different applications, such as Dynamics 365 Finance, Dynamics 365 Supply Chain, and Dynamics 365 Project Operations.</span></span> <span data-ttu-id="60977-121">Per a cada categoria de transacció creada, el Project Operations crea automàticament quatre categories compartides relacionades: hores, despeses, càrrecs i article.</span><span class="sxs-lookup"><span data-stu-id="60977-121">For each Transaction category created, Project Operations automatically creates four related Shared categories: Hours, Expense, Fees, and Item.</span></span> <span data-ttu-id="60977-122">Podeu revisar i ajustar les categories compartides anant a **Administració de projectes i comptabilitat** \> **Configuració** \> **Categories** \> **Categories compartides**.</span><span class="sxs-lookup"><span data-stu-id="60977-122">You can review and adjust the shared categories by going to **Project management and accounting** \> **Setup** \> **Categories** \> **Shared Categories**.</span></span>

## <a name="project-categories"></a><span data-ttu-id="60977-123">Categories del projecte</span><span class="sxs-lookup"><span data-stu-id="60977-123">Project categories</span></span>

<span data-ttu-id="60977-124">Les categories de projecte representen el nivell de configuració més granular i s'han de configurar per separat i per a cada empresa; ho ha de fer un comptable de projecte.</span><span class="sxs-lookup"><span data-stu-id="60977-124">Project categories represent most granular level of category configuration and must be configured separately, and for each company, by a Project accountant.</span></span>

1. <span data-ttu-id="60977-125">Aneu a **Administració de projectes i comptabilitat** \> **Configuració** \> **Categories** \> **Categories del projecte**.</span><span class="sxs-lookup"><span data-stu-id="60977-125">Go to **Project Management and Accounting** \> **Setup** \> **Categories** \> **Project categories**.</span></span>
2. <span data-ttu-id="60977-126">Seleccioneu **Crea**.</span><span class="sxs-lookup"><span data-stu-id="60977-126">Select **New**.</span></span>
3. <span data-ttu-id="60977-127">Seleccioneu l' **identificador de categoria** de la categoria compartida que heu creat a la secció anterior.</span><span class="sxs-lookup"><span data-stu-id="60977-127">Select the **Category ID** of the Shared category you created in the previous section.</span></span> <span data-ttu-id="60977-128">El Project Operations només permet utilitzar les categories compartides que estan associades amb categories de transaccions.</span><span class="sxs-lookup"><span data-stu-id="60977-128">Project Operations allows using only those shared categories that are associated with transaction categories.</span></span>
4. <span data-ttu-id="60977-129">Seleccioneu un grup de categories.</span><span class="sxs-lookup"><span data-stu-id="60977-129">Select a category group.</span></span>

## <a name="category-groups"></a><span data-ttu-id="60977-130">Grups de categories</span><span class="sxs-lookup"><span data-stu-id="60977-130">Category groups</span></span>

<span data-ttu-id="60977-131">Els grups de categories s'utilitzen per compartir propietats, principalment perfils de comptabilització, entre categories de projectes relacionats.</span><span class="sxs-lookup"><span data-stu-id="60977-131">Category groups are used to share properties, primarily posting profiles, between related Project categories.</span></span> <span data-ttu-id="60977-132">Hi ha d'haver com a mínim un grup de categoria per a cada tipus de transacció i s'assigna a cada categoria de projecte un grup.</span><span class="sxs-lookup"><span data-stu-id="60977-132">There must be at least one category group for each transaction type and each project category is assigned a group.</span></span>

<span data-ttu-id="60977-133">Les especificacions de comptabilització del Project Operations es defineixen per les regles del perfil de cost i ingrés del projecte, categories de projectes i grups de categories.</span><span class="sxs-lookup"><span data-stu-id="60977-133">The posting specifications in Project Operations are defined by the project cost and revenue profile rules, project categories, and category groups.</span></span> <span data-ttu-id="60977-134">Podeu configurar els grups de categories anant a **Administració de projectes i comptabilitat** \> **Configuració** \> **Categories** \> **Grups de categories**.</span><span class="sxs-lookup"><span data-stu-id="60977-134">You can set up category groups by going to **Project management and accounting** \> **Setup** \> **Categories** \> **Category groups**.</span></span>
