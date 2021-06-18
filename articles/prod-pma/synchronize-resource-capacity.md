---
title: Sincronitzar la capacitat dels recursos
description: Aquest tema proporciona informació sobre com sincronitzar la capacitat d'un recurs entre calendaris i projectes.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 8bde3c434680f0651293cbce13ecdce945c3a743
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997499"
---
# <a name="synchronize-resource-capacity"></a><span data-ttu-id="d86ec-103">Sincronitzar la capacitat dels recursos</span><span class="sxs-lookup"><span data-stu-id="d86ec-103">Synchronize resource capacity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d86ec-104">Els processos per a la sincronització de recursos ajuden a garantir que la informació del calendari i el calendari base es transfereix en la planificació de recursos del projecte.</span><span class="sxs-lookup"><span data-stu-id="d86ec-104">The processes for resource synchronization help guarantee that information for the calendar and base calendar trickles down into project resource scheduling.</span></span> <span data-ttu-id="d86ec-105">Si el calendari canvia, els processos fan les actualitzacions necessàries a la planificació de recursos del projecte.</span><span class="sxs-lookup"><span data-stu-id="d86ec-105">If the calendar is changed, the processes make the required updates to the scheduling of project resources.</span></span> <span data-ttu-id="d86ec-106">Els processos també ajuden a millorar el rendiment, ja que la informació de recursos del calendari se sincronitza amb antelació.</span><span class="sxs-lookup"><span data-stu-id="d86ec-106">The processes also help improve performance, because the calendar's resource information is synchronized in advance.</span></span> <span data-ttu-id="d86ec-107">Per tant, les actualitzacions de la informació de planificació de recursos ocorren amb més rapidesa.</span><span class="sxs-lookup"><span data-stu-id="d86ec-107">Therefore, updates to resource scheduling information occur more quickly.</span></span> <span data-ttu-id="d86ec-108">Us recomanem que planifiqueu els processos com un lot en comptes d'un en un cada vegada.</span><span class="sxs-lookup"><span data-stu-id="d86ec-108">We recommend that you schedule the processes as a batch instead of one at a time.</span></span> <span data-ttu-id="d86ec-109">Altrament, hi ha un risc que algú oblidi les dates inclusives quan la informació s'ha sincronitzat per última vegada.</span><span class="sxs-lookup"><span data-stu-id="d86ec-109">Otherwise, there is a risk that someone will forget the inclusive dates when the information was last synchronized.</span></span> <span data-ttu-id="d86ec-110">Si no es fan servir dates inclusives, poden produir-se llacunes durant la sincronització de les dates.</span><span class="sxs-lookup"><span data-stu-id="d86ec-110">If inclusive dates aren't used, gaps can occur during date synchronization.</span></span>

![Sincronització del calendari](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a><span data-ttu-id="d86ec-112">Sincronització de la consolidació de capacitat de recursos</span><span class="sxs-lookup"><span data-stu-id="d86ec-112">Synchronize resource capacity roll-ups</span></span>

<span data-ttu-id="d86ec-113">El procés de sincronització està dissenyat per sincronitzar tota la informació del calendari de recursos.</span><span class="sxs-lookup"><span data-stu-id="d86ec-113">The synchronization process is designed to synchronize all resource calendar information.</span></span> <span data-ttu-id="d86ec-114">Aquesta informació inclou informació del calendari base sobre qualsevol canvi que hi hagi a la taula de capacitat de calendari de recursos del projecte.</span><span class="sxs-lookup"><span data-stu-id="d86ec-114">This information includes base calendar information about any changes to the project's Resource calendar capacity table.</span></span> <span data-ttu-id="d86ec-115">Si s'afegeixen recursos nous al projecte, la sincronització ajuda a garantir que la informació actualitzada del calendari estigui disponible.</span><span class="sxs-lookup"><span data-stu-id="d86ec-115">If new resources are added in the project, synchronization helps guarantee that the updated calendar information is available.</span></span> <span data-ttu-id="d86ec-116">Aquesta sincronització es pot fer en qualsevol moment.</span><span class="sxs-lookup"><span data-stu-id="d86ec-116">This synchronization can be done at any time.</span></span>

<span data-ttu-id="d86ec-117">Es recomana utilitzar un lot.</span><span class="sxs-lookup"><span data-stu-id="d86ec-117">We recommend that you use a batch.</span></span> <span data-ttu-id="d86ec-118">Hi ha disponibles les opcions durant la sincronització de les reserves de capacitat.</span><span class="sxs-lookup"><span data-stu-id="d86ec-118">The options are available during synchronization of capacity reservations.</span></span>

1. <span data-ttu-id="d86ec-119">Seleccioneu **Administració de projectes i comptabilitat** &gt; **Periòdic** &gt; **Sincronització de capacitat** &gt; **Sincronitza les consolidacions de capacitat de recursos**.</span><span class="sxs-lookup"><span data-stu-id="d86ec-119">Select **Project management and accounting** &gt; **Periodic** &gt; **Capacity synchronization** &gt; **Synchronize resources capacity roll-ups**.</span></span>
2. <span data-ttu-id="d86ec-120">Definiu les opcions a la taula següent.</span><span class="sxs-lookup"><span data-stu-id="d86ec-120">Set the options in the following table.</span></span>

    | <span data-ttu-id="d86ec-121">Opció</span><span class="sxs-lookup"><span data-stu-id="d86ec-121">Option</span></span>      | <span data-ttu-id="d86ec-122">Descripció</span><span class="sxs-lookup"><span data-stu-id="d86ec-122">Description</span></span> |
    |-------------|-------------|
    | <span data-ttu-id="d86ec-123">Codi de període</span><span class="sxs-lookup"><span data-stu-id="d86ec-123">Period code</span></span> | <span data-ttu-id="d86ec-124">Opcionalment, seleccioneu el codi d'interval de dates del llibre major general per definir les dates d'inici i d'acabament per al procés de sincronització per a les consolidacions de capacitat de recursos.</span><span class="sxs-lookup"><span data-stu-id="d86ec-124">Optionally select the General ledger date interval code to set the start and end dates for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="d86ec-125">Data d'inici</span><span class="sxs-lookup"><span data-stu-id="d86ec-125">Start date</span></span>  | <span data-ttu-id="d86ec-126">Introduïu la data d'inici del procés de sincronització per a la consolidació de capacitat de recursos.</span><span class="sxs-lookup"><span data-stu-id="d86ec-126">Enter the start date for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="d86ec-127">Data de finalització</span><span class="sxs-lookup"><span data-stu-id="d86ec-127">End date</span></span>    | <span data-ttu-id="d86ec-128">Introduïu la data de finalització del procés de sincronització per a la consolidació de capacitat de recursos.</span><span class="sxs-lookup"><span data-stu-id="d86ec-128">Enter the end date for the synchronization process for resource capacity roll-ups.</span></span> |

<span data-ttu-id="d86ec-129">[![Procés de sincronització](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span><span class="sxs-lookup"><span data-stu-id="d86ec-129">[![Synchronization process](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]