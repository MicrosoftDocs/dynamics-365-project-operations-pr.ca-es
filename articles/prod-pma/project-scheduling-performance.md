---
title: Rendiment de planificació dels recursos del projecte
description: Aquest tema proporciona informació sobre com millorar el rendiment de la planificació dels recursos per a un gran nombre de projectes.
author: Yowelle
manager: AnnBe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: c3f219ce0635545976a6a4639233f166e18468af
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072195"
---
# <a name="project-resource-scheduling-performance"></a><span data-ttu-id="77db6-103">Rendiment de planificació dels recursos del projecte</span><span class="sxs-lookup"><span data-stu-id="77db6-103">Project resource scheduling performance</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


<span data-ttu-id="77db6-104">Els problemes de rendiment relacionats amb la planificació de recursos poden ocórrer quan el nombre de projectes arriba als milers.</span><span class="sxs-lookup"><span data-stu-id="77db6-104">Performance issues related to resource scheduling can occur when the number of projects reaches into the thousands.</span></span> <span data-ttu-id="77db6-105">Per millorar el rendiment de la planificació de recursos, hi ha una característica disponible que permet als usuaris reduir el temps que es tarda a iniciar el formulari de disponibilitat de recursos.</span><span class="sxs-lookup"><span data-stu-id="77db6-105">To improve resource scheduling performance, a feature is available that allows users to reduce the time that it takes to launch the resource availability form.</span></span> <span data-ttu-id="77db6-106">Específicament, això elimina el procés de sincronització d'informes de capacitat de recursos i utilitza la taula **ResProjectResource** per accelerar la cerca de recursos.</span><span class="sxs-lookup"><span data-stu-id="77db6-106">Specifically, this removes the resource capacity roll-up synchronization process and uses the **ResProjectResource** table to speed up the resource lookup.</span></span> <span data-ttu-id="77db6-107">Tingueu en compte que la taula **ResRollup** ja no s'utilitzarà.</span><span class="sxs-lookup"><span data-stu-id="77db6-107">Note that the **ResRollup** table will no longer be used.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="77db6-108">Si hi ha una dependència del procés de sincronització d'informes de capacitat de recursos o de la taula **ResProjectResource** , no utilitzeu aquesta funció.</span><span class="sxs-lookup"><span data-stu-id="77db6-108">If there is a dependency on either the resource capacity roll-up synchronization process or the **ResProjectResource** table, do not use this feature.</span></span>

## <a name="enable-resource-scheduling-performance-enhancement"></a><span data-ttu-id="77db6-109">Habilitar la millora del rendiment de la planificació de recursos</span><span class="sxs-lookup"><span data-stu-id="77db6-109">Enable resource scheduling performance enhancement</span></span>
<span data-ttu-id="77db6-110">Per permetre la millora del rendiment de la planificació de recursos, completeu els passos següents.</span><span class="sxs-lookup"><span data-stu-id="77db6-110">To enable resource scheduling performance enhancement, complete the following steps.</span></span>

1. <span data-ttu-id="77db6-111">Aneu a **Administració de característiques** > **Tot** i, a la llista de característiques, cerqueu **Habilita la característica de millora de la planificació de recursos del projecte**.</span><span class="sxs-lookup"><span data-stu-id="77db6-111">Go to **Feature management** > **All** , and in the feature list, locate **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="77db6-112">Seleccioneu **Habilita ara**.</span><span class="sxs-lookup"><span data-stu-id="77db6-112">Select **Enable now**.</span></span>

> [!NOTE]
> <span data-ttu-id="77db6-113">Si no podeu trobar la característica a la llista, seleccioneu **Comprova si hi ha actualitzacions** per actualitzar la llista.</span><span class="sxs-lookup"><span data-stu-id="77db6-113">If you can't find the feature in the list, select **Check for updates** to refresh the list.</span></span>

3. <span data-ttu-id="77db6-114">Actualitzeu el vostre navegador i aneu a **Administració de projectes i comptabilitat** > **Periòdic** > **Recursos del projecte** > **Sincronitza la capacitat dels calendaris de recursos entre totes les empreses**.</span><span class="sxs-lookup"><span data-stu-id="77db6-114">Refresh your browser, and then go to **Project management and accounting** > **Periodic** > **Project resources** > **Synchronize resource calendars capacity across all companies**.</span></span>
4. <span data-ttu-id="77db6-115">Establiu **Suprimeix els registres de capacitat existents** a **Sí** per suprimir dades anteriors.</span><span class="sxs-lookup"><span data-stu-id="77db6-115">Set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="77db6-116">Si voleu generar dades incrementals, definiu-ho a **No**.</span><span class="sxs-lookup"><span data-stu-id="77db6-116">If you want generate incremental data, set it to **No**.</span></span>
5. <span data-ttu-id="77db6-117">En el camp **Codi de període** , seleccioneu el període en què s'han de generar les dades.</span><span class="sxs-lookup"><span data-stu-id="77db6-117">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="77db6-118">Si seleccioneu un codi de període, no cal definir una data d'inici i finalització.</span><span class="sxs-lookup"><span data-stu-id="77db6-118">If you select a period code, a start and end date do not need to be defined.</span></span>
6. <span data-ttu-id="77db6-119">Si deixeu el camp **Codi de període** en blanc, seleccioneu dates específiques d'inici i finalització per generar les dades.</span><span class="sxs-lookup"><span data-stu-id="77db6-119">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
7. <span data-ttu-id="77db6-120">Seleccioneu **D'acord**.</span><span class="sxs-lookup"><span data-stu-id="77db6-120">Select **OK**.</span></span>

 > [!NOTE]
 > <span data-ttu-id="77db6-121">Això distribuirà les dades generals a la taula **ResCalendarCapacity** entre totes les empreses del vostre entorn, de manera que el treball per lots només s'ha d'executar en una entitat jurídica.</span><span class="sxs-lookup"><span data-stu-id="77db6-121">This will distribute general data to the **ResCalendarCapacity** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="77db6-122">Les dades d'aquest treball per lots són necessàries per calcular la capacitat dels recursos a través del calendari associat.</span><span class="sxs-lookup"><span data-stu-id="77db6-122">The data in this batch job is needed to calculate resource capacity through the associated calendar.</span></span>

8. <span data-ttu-id="77db6-123">Aneu a **Administració de projectes i comptabilitat** > **Periòdic** > **Recursos del projecte** > **Emplena els recursos del projecte entre totes les empreses** i seleccioneu **D'acord**.</span><span class="sxs-lookup"><span data-stu-id="77db6-123">Go to **Project management and accounting** > **Periodic** > **Project resources** > **Populate project resources across all companies** and then select **OK**.</span></span> <span data-ttu-id="77db6-124">Aquest és l'script d'actualització de dades per a dades generals a les taules **ResProjectResourceResource** , **ResCalendarDateTimeRange** i **ResEffectiveDateTimeRange**.</span><span class="sxs-lookup"><span data-stu-id="77db6-124">This is the data upgrade script for general data in the **ResProjectResource** , **ResCalendarDateTimeRange** , and **ResEffectiveDateTimeRange** tables.</span></span> <span data-ttu-id="77db6-125">Els valors per al camp **PSAPRojSchedRole.RootActivity** també s'actualitzen.</span><span class="sxs-lookup"><span data-stu-id="77db6-125">Values for the **PSAPRojSchedRole.RootActivity** field are also updated.</span></span> <span data-ttu-id="77db6-126">Si això no s'executa, rebreu un avís quan intenteu executar operacions de planificació de recursos.</span><span class="sxs-lookup"><span data-stu-id="77db6-126">If this is not run, you will receive a warning when you try to execute resource scheduling operations.</span></span>
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a><span data-ttu-id="77db6-127">Desactivar la millora del rendiment de la planificació de recursos</span><span class="sxs-lookup"><span data-stu-id="77db6-127">Turn off resource scheduling performance enhancement</span></span>

1. <span data-ttu-id="77db6-128">Aneu a **Administració de característiques** > **Tot** i cerqueu **Habilita la característica de millora de la planificació de recursos del projecte**.</span><span class="sxs-lookup"><span data-stu-id="77db6-128">Go to **Feature management** > **All**  and search for **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="77db6-129">Seleccioneu la característica i seleccioneu el botó **Inhabilita**.</span><span class="sxs-lookup"><span data-stu-id="77db6-129">Select the feature, and then select the **Disable** button.</span></span>
3. <span data-ttu-id="77db6-130">Actualitzeu el navegador.</span><span class="sxs-lookup"><span data-stu-id="77db6-130">Refresh your browser.</span></span>
4. <span data-ttu-id="77db6-131">Aneu a **Administració de projectes i comptabilitat** > **Periòdic** > **Sincronització de capacitat** > **Sincronitza les consolidacions de capacitat de recursos**.</span><span class="sxs-lookup"><span data-stu-id="77db6-131">Go to **Project management and accounting** > **Periodic** > **Capacity synchronization** > **Synchronize resource capacity roll-ups**.</span></span>
5. <span data-ttu-id="77db6-132">A la pàgina **Sincronització d'informes de capacitat** , establiu **Suprimeix els registres de capacitat existents** a **Sí** per suprimir dades anteriors.</span><span class="sxs-lookup"><span data-stu-id="77db6-132">On the **Capacity roll-up synchronization** page, set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="77db6-133">Si voleu generar dades incrementals, definiu-ho a **No**.</span><span class="sxs-lookup"><span data-stu-id="77db6-133">If you want to generate incremental data, set it to **No**.</span></span>
6. <span data-ttu-id="77db6-134">En el camp **Codi de període** , seleccioneu el període en què s'han de generar les dades.</span><span class="sxs-lookup"><span data-stu-id="77db6-134">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="77db6-135">Si seleccioneu un codi de període, no cal definir una data d'inici i finalització.</span><span class="sxs-lookup"><span data-stu-id="77db6-135">If you select a period code, a start and end date do not need to be defined.</span></span>
7. <span data-ttu-id="77db6-136">Si deixeu el camp **Codi de període** en blanc, seleccioneu dates específiques d'inici i finalització per generar les dades.</span><span class="sxs-lookup"><span data-stu-id="77db6-136">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
8. <span data-ttu-id="77db6-137">Seleccioneu **D'acord**.</span><span class="sxs-lookup"><span data-stu-id="77db6-137">Select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="77db6-138">Això distribuirà les dades generals a la taula **ResRollup** entre totes les empreses del vostre entorn, de manera que el treball per lots només s'ha d'executar en una entitat jurídica.</span><span class="sxs-lookup"><span data-stu-id="77db6-138">This will distribute general data to the **ResRollup** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="77db6-139">Aquest treball per lots és necessari per a totes les visualitzacions de **Disponibilitat de recursos**.</span><span class="sxs-lookup"><span data-stu-id="77db6-139">This batch job is needed for all **Resource Availability** views.</span></span> <span data-ttu-id="77db6-140">Si aquest treball per lots no s'executa, les dades de **ResRollup** es generaran sobre la marxa, cosa que pot tardar temps.</span><span class="sxs-lookup"><span data-stu-id="77db6-140">If this batch job is not run, the **ResRollup** data will be generated on the fly, which can take time.</span></span>
