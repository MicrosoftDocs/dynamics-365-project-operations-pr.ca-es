---
title: Configuració dels recursos del projecte
description: Aquest tema proporciona informació sobre la configuració o la sol·licitud de recursos del projecte.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0bf146c3bfb2fd558c471d8a9e980834cb1b87df
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288727"
---
# <a name="set-up-project-resources"></a><span data-ttu-id="8bcad-103">Configuració dels recursos del projecte</span><span class="sxs-lookup"><span data-stu-id="8bcad-103">Set up project resources</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8bcad-104">Heu de configurar un calendari i associar-lo a un empleat o a un treballador.</span><span class="sxs-lookup"><span data-stu-id="8bcad-104">You must set up a calendar and associate it with an employee or a worker.</span></span> <span data-ttu-id="8bcad-105">El calendari s'utilitza per planificar el projecte i el temps de treball dels recursos que es reserven per al projecte.</span><span class="sxs-lookup"><span data-stu-id="8bcad-105">The calendar is used to schedule the project and the working time of the resources that are reserved for the project.</span></span> <span data-ttu-id="8bcad-106">Durant la configuració del calendari, els administradors del projecte poden fer un anivellament de recursos com a part de l'optimització de recursos.</span><span class="sxs-lookup"><span data-stu-id="8bcad-106">During calendar setup, project managers can do resource leveling as part of resource optimization.</span></span> <span data-ttu-id="8bcad-107">Segons la planificació de calendari, es poden posar restriccions als recursos.</span><span class="sxs-lookup"><span data-stu-id="8bcad-107">Based on the calendar schedule, restrictions can be put on resources.</span></span> <span data-ttu-id="8bcad-108">Podeu configurar un calendari a la pàgina **Calendaris**.</span><span class="sxs-lookup"><span data-stu-id="8bcad-108">You can set up a calendar on the **Calendars** page.</span></span>

<span data-ttu-id="8bcad-109">Quan configureu un treballador com a recurs de projecte, podeu seleccionar els treballadors que treballen a l'empresa per a la qual configureu els recursos.</span><span class="sxs-lookup"><span data-stu-id="8bcad-109">When you set up a worker as a project resource, you can select from workers who work in the company that you're setting up resources for.</span></span> <span data-ttu-id="8bcad-110">Si ho preferiu, podeu seleccionar treballadors d'altres empreses a l'organització.</span><span class="sxs-lookup"><span data-stu-id="8bcad-110">Alternatively, you can select workers from other companies in your organization.</span></span> <span data-ttu-id="8bcad-111">Aquests treballadors s'anomenen recursos entre empreses.</span><span class="sxs-lookup"><span data-stu-id="8bcad-111">These workers are known as intercompany resources.</span></span>

<span data-ttu-id="8bcad-112">En els procediments següents s'explica com es configura un treballador com a recurs de projecte a l'empresa i com es configura un recurs de projecte entre empreses.</span><span class="sxs-lookup"><span data-stu-id="8bcad-112">The following procedures explain how to set up a worker as a project resource in your company and how to set up an intercompany project resource.</span></span>

## <a name="set-up-a-worker-as-a-project-resource"></a><span data-ttu-id="8bcad-113">Configurar un treballador com a recurs de projecte</span><span class="sxs-lookup"><span data-stu-id="8bcad-113">Set up a worker as a project resource</span></span>

1. <span data-ttu-id="8bcad-114">A la pàgina **Treballadors**, a la llista **Treballadors**, seleccioneu el treballador que voleu afegir com a recurs del projecte i obriu el registre del treballador.</span><span class="sxs-lookup"><span data-stu-id="8bcad-114">On the **Workers** page, in the **Workers** list, select the worker that you're adding as a project resource, and open the worker record.</span></span>
2. <span data-ttu-id="8bcad-115">A la subfinestra d'acció, seleccioneu **Projecte** &gt; **Configuració** &gt; **Configuració del projecte**.</span><span class="sxs-lookup"><span data-stu-id="8bcad-115">On the Action Pane, select **Project** &gt; **Setup** &gt; **Project setup**.</span></span>
3. <span data-ttu-id="8bcad-116">Seleccioneu un calendari i, a continuació, tanqueu la pàgina.</span><span class="sxs-lookup"><span data-stu-id="8bcad-116">Select a calendar, and then close the page.</span></span>

<span data-ttu-id="8bcad-117">També podeu especificar projectes per defecte per a un recurs com a tipus d'assignació prèvia.</span><span class="sxs-lookup"><span data-stu-id="8bcad-117">You can also specify default projects for a resource as a type of pre-assignment.</span></span> <span data-ttu-id="8bcad-118">Les assignacions prèvies es poden utilitzar quan l'administrador de recursos o l'administrador del projecte sap en quins projectes treballarà el recurs amb antelació.</span><span class="sxs-lookup"><span data-stu-id="8bcad-118">Pre-assignments can be used when the resource manager or project manager knows which projects the resource will be working on in advance.</span></span> <span data-ttu-id="8bcad-119">Les assignacions prèvies també poden basar-se en la sol·licitud d'un patrocinador o client del projecte.</span><span class="sxs-lookup"><span data-stu-id="8bcad-119">Pre-assignments can also be based on the request of a project sponsor or customer.</span></span> <span data-ttu-id="8bcad-120">Per assignar prèviament un projecte abans, a la pàgina **Assigna els projectes**, a la pestanya **Projectes**, a la llista **Projectes restants**, seleccioneu el projecte adient.</span><span class="sxs-lookup"><span data-stu-id="8bcad-120">To pre-assign a project, on the **Assign projects** page, on the **Projects** tab, in the **Remaining projects** list, select the appropriate project.</span></span>

## <a name="set-up-an-intercompany-resource"></a><span data-ttu-id="8bcad-121">Configurar un recurs entre empreses</span><span class="sxs-lookup"><span data-stu-id="8bcad-121">Set up an intercompany resource</span></span>

<span data-ttu-id="8bcad-122">Quan configureu un treballador com a recurs entre empreses, heu d'emplenar la configuració tant de l'empresa prestadora com de l'empresa prestatària.</span><span class="sxs-lookup"><span data-stu-id="8bcad-122">When you set up a worker as an intercompany resource, you must complete the setup in both the lending company and the borrowing company.</span></span>

### <a name="in-the-lending-company"></a><span data-ttu-id="8bcad-123">A l'empresa prestadora</span><span class="sxs-lookup"><span data-stu-id="8bcad-123">In the lending company</span></span>

1. <span data-ttu-id="8bcad-124">Al Finance, comproveu que l'empresa prestadora està seleccionada i, a continuació, completeu el procediment a la secció anterior, "Configurar un treballador com a recurs del projecte".</span><span class="sxs-lookup"><span data-stu-id="8bcad-124">In Finance, verify that the lending company is selected, and then complete the procedure in the previous section, "Set up a worker as a project resource."</span></span>
2. <span data-ttu-id="8bcad-125">A la pàgina **Comptabilitat entre empreses**, seleccioneu **Nova**.</span><span class="sxs-lookup"><span data-stu-id="8bcad-125">On the **Intercompany accounting** page, select **New**.</span></span>
3. <span data-ttu-id="8bcad-126">Al camp **ID de l'entitat jurídica**, seleccioneu l'empresa prestadora.</span><span class="sxs-lookup"><span data-stu-id="8bcad-126">In the **Legal entity ID** field, select the lending company.</span></span> <span data-ttu-id="8bcad-127">Empleneu els camps restants segons calgui i seleccioneu **Desa**.</span><span class="sxs-lookup"><span data-stu-id="8bcad-127">Fill in the remaining fields as appropriate, and then select **Save**.</span></span>
4. <span data-ttu-id="8bcad-128">A la pàgina **Transferència de preus**, seleccioneu **Nova**.</span><span class="sxs-lookup"><span data-stu-id="8bcad-128">On the **Transfer price** page, select **New**.</span></span>
5. <span data-ttu-id="8bcad-129">Al camp **Entitat jurídica prestatària**, seleccioneu l'empresa adequada.</span><span class="sxs-lookup"><span data-stu-id="8bcad-129">In the **Borrowing legal entity** field, select the appropriate company.</span></span>
6. <span data-ttu-id="8bcad-130">Per prestar a l'empresa prestatària només el recurs que heu creat a l'inici d'aquesta secció, al camp **Recurs**, seleccioneu el nom del recurs que heu creat.</span><span class="sxs-lookup"><span data-stu-id="8bcad-130">To lend the borrowing company only the resource that you created at the beginning of this section, in the **Resource** field, select the name of the resource that you created.</span></span> <span data-ttu-id="8bcad-131">Per fer que tots els recursos de l'empresa prestadora estiguin disponibles per a l'empresa prestatària, deixeu el camp **Recurs** en blanc.</span><span class="sxs-lookup"><span data-stu-id="8bcad-131">To make all resources in the lending company available to the borrowing company, leave the **Resource** field blank.</span></span>
7. <span data-ttu-id="8bcad-132">A la pàgina **Paràmetres de l'administració de projectes i la comptabilitat**, a la pestanya **Entre empreses**, definiu l'opció **Habilita la planificació de recursos i els fulls d'hores entre empreses** a **Sí**.</span><span class="sxs-lookup"><span data-stu-id="8bcad-132">On the **Project management and accounting parameters** page, on the **Intercompany** tab, set the **Enable intercompany resource scheduling and timesheets** option to **Yes**.</span></span>

### <a name="in-the-borrowing-company"></a><span data-ttu-id="8bcad-133">A l'empresa prestatària</span><span class="sxs-lookup"><span data-stu-id="8bcad-133">In the borrowing company</span></span>

- <span data-ttu-id="8bcad-134">A la pàgina **Llista de recursos**, al filtre de cerca, introduïu el nom del recurs que heu creat per a l'empresa prestadora, per comprovar que el nom s'inclou a la llista de recursos de l'empresa prestatària.</span><span class="sxs-lookup"><span data-stu-id="8bcad-134">On the **Resources list** page, in the search filter, enter the name of the resource that you created for the lending company, to verify that the name is included in the resource list for the borrowing company.</span></span>

## <a name="request-project-resources"></a><span data-ttu-id="8bcad-135">Sol·licitud de recursos del projecte</span><span class="sxs-lookup"><span data-stu-id="8bcad-135">Request project resources</span></span>
<span data-ttu-id="8bcad-136">La funcionalitat per a la planificació de recursos de projectes només permet distribuir els recursos de personal a compromisos o projectes.</span><span class="sxs-lookup"><span data-stu-id="8bcad-136">The functionality for project resource scheduling only lets resource managers distribute staffed resources on engagements or projects.</span></span> <span data-ttu-id="8bcad-137">Per habilitar aquesta funcionalitat, completeu les tasques següents o verifiqueu que s'hagin completat:</span><span class="sxs-lookup"><span data-stu-id="8bcad-137">To enable this functionality, complete the following tasks, or verify that they have been completed:</span></span>

- <span data-ttu-id="8bcad-138">Configureu les seqüències de números.</span><span class="sxs-lookup"><span data-stu-id="8bcad-138">Set up number sequences.</span></span>
- <span data-ttu-id="8bcad-139">Configureu l'administració de projectes i els fluxos de treball de comptabilitat.</span><span class="sxs-lookup"><span data-stu-id="8bcad-139">Set up project management and accounting workflows.</span></span>
- <span data-ttu-id="8bcad-140">Habiliteu els fluxos de treball de sol·licitud de recursos.</span><span class="sxs-lookup"><span data-stu-id="8bcad-140">Enable resource request workflows.</span></span>

<span data-ttu-id="8bcad-141">Quan s'hagin completat les tasques anteriors, podreu completar les tasques següents segons calgui:</span><span class="sxs-lookup"><span data-stu-id="8bcad-141">After the preceding tasks have been completed, you can complete the following tasks as you require:</span></span>

- <span data-ttu-id="8bcad-142">Crear una sol·licitud de recurs des d'un recurs de personal reservat de manera flexible.</span><span class="sxs-lookup"><span data-stu-id="8bcad-142">Create a resource request from a soft-booked staffed resource.</span></span>
- <span data-ttu-id="8bcad-143">Supervisar les sol·licituds de recursos.</span><span class="sxs-lookup"><span data-stu-id="8bcad-143">Monitor resource requests.</span></span>
- <span data-ttu-id="8bcad-144">Complir les sol·licituds de recursos.</span><span class="sxs-lookup"><span data-stu-id="8bcad-144">Fulfill resource requests.</span></span>
- <span data-ttu-id="8bcad-145">Sol·licitar un recurs de personal d'una WBS.</span><span class="sxs-lookup"><span data-stu-id="8bcad-145">Request a staffed resource from a WBS.</span></span>
- <span data-ttu-id="8bcad-146">Reservar recursos en un projecte sense necessitat de tenir una sol·licitud de recurs de personal.</span><span class="sxs-lookup"><span data-stu-id="8bcad-146">Book resources to a project without having a request for a staffed resource.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]