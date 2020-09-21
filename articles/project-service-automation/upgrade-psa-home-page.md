---
title: Pàgina d'inici de les actualitzacions
description: Aquest tema mostra on es troba informació important sobre les característiques noves i canviades al Dynamics 365 Project Service Automation, i el procés per actualitzar a la versió més recent.
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 05/30/2019
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 for Project Service 3.x
author: rumant
ms.assetid: c92d0849-e40c-4a56-9719-34030fbf5991
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 55f544636f39fc4faae06fdd512f859800bb7b44
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749530"
---
# <a name="upgrade-home-page"></a><span data-ttu-id="b31eb-103">Pàgina d'inici de les actualitzacions</span><span class="sxs-lookup"><span data-stu-id="b31eb-103">Upgrade home page</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="upgrade-from-psa-version-2x-or-1x-to-version-3x"></a><span data-ttu-id="b31eb-104">Actualització de la versió de PSA 2.x o 1.x a la versió 3.x</span><span class="sxs-lookup"><span data-stu-id="b31eb-104">Upgrade from PSA version 2.x or 1.x to version 3.x</span></span>

### <a name="new-instances"></a><span data-ttu-id="b31eb-105">Noves instàncies</span><span class="sxs-lookup"><span data-stu-id="b31eb-105">New instances</span></span>

<span data-ttu-id="b31eb-106">A partir del 17 de maig de 2019, en seleccionar el Project Service Automation durant el proveïment d'una instància nova, la versió 3.x s'instal·la per defecte.</span><span class="sxs-lookup"><span data-stu-id="b31eb-106">As of May 17, 2019, when Project Service Automation is selected during the provisioning of a new instance, version 3.x is installed by default.</span></span>

### <a name="existing-instances"></a><span data-ttu-id="b31eb-107">Instàncies existents</span><span class="sxs-lookup"><span data-stu-id="b31eb-107">Existing instances</span></span>

<span data-ttu-id="b31eb-108">Anteriorment, els clients que tenien una instància de la versió 2.x del PSA i necessitaven actualitzar a la versió 3.x, que és la versió basada en la interfície de client unificada (UCI) del PSA, havien de contactar amb el servei tècnic de Microsoft i proporcionar els detalls de la seva instància, de manera que el servei tècnic pogués habilitar l'actualització a la versió 3.x.</span><span class="sxs-lookup"><span data-stu-id="b31eb-108">Previously, customers who have an instance of PSA version 2.x and needed to upgrade to version 3.x, which is the Unified client interface-based (UCI) version of PSA , had to contact Microsoft Support and provide the details of thier instance so that support could enable the instance for upgrade to version 3.x.</span></span> <span data-ttu-id="b31eb-109">A partir de l'1 de març del 2020, els clients que tinguin una instància de la versió 2.x del PSA i que necessitin actualitzar-la a la versió 3.x, podran actualitzar les seves instàncies directament des del portal d'administració sense haver de contactar amb el servei tècnic de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b31eb-109">As of March 1st, 2020, customers who have an instance of PSA version 2.x and need to upgrade to version 3.x, will able to upgrade their instances directly from the Admin portal without having to contact Microsoft Support.</span></span>  

> [!NOTE]
> <span data-ttu-id="b31eb-110">La versió 3.x del PSA inclou canvis significatius.</span><span class="sxs-lookup"><span data-stu-id="b31eb-110">PSA version 3.x includes significant changes.</span></span> <span data-ttu-id="b31eb-111">S'ha construït sobre el marc de la interfície unificada per ajudar a proporcionar una experiència d'usuari millorada.</span><span class="sxs-lookup"><span data-stu-id="b31eb-111">It has been built on the Unified Interface framework to help provide an improved user experience.</span></span> <span data-ttu-id="b31eb-112">L'aplicació redissenyada ofereix una interfície d'usuari (IU) coherent i homogènia, i segueix els principis de disseny responsiu per a una òptima visualització en qualsevol mida de pantalla o dispositiu.</span><span class="sxs-lookup"><span data-stu-id="b31eb-112">The redesigned app delivers a consistent, uniform user interface (UI), and it follows responsive design principles for optimal viewing on any screen size or device.</span></span> <span data-ttu-id="b31eb-113">Hi ha hagut altres canvis a l'aplicació.</span><span class="sxs-lookup"><span data-stu-id="b31eb-113">There have been other changes throughout the application.</span></span> <span data-ttu-id="b31eb-114">Algunes de les àrees que s'ha canviat inclouen els preus, la reserva i l'assignació de recursos, el temps, les despeses i les aprovacions.</span><span class="sxs-lookup"><span data-stu-id="b31eb-114">Some of the areas that have been changed include pricing, booking and assigning resources, time, expenses, and approvals.</span></span>

<span data-ttu-id="b31eb-115">Abans de començar el procés d'actualització, us recomanem que completeu les tasques següents:</span><span class="sxs-lookup"><span data-stu-id="b31eb-115">Before you begin the upgrade process, we recommend that you complete the following tasks:</span></span>

- <span data-ttu-id="b31eb-116">Verifiqueu si tant el Dynamics 365 Field Service com el Project Service Automation estan instal·lats a la instància identificada.</span><span class="sxs-lookup"><span data-stu-id="b31eb-116">Verify whether both Dynamics 365 Field Service and Project Service Automation are installed on the identified instance.</span></span> <span data-ttu-id="b31eb-117">Si totes dues solucions estan instal·lades, heu de planificar l'actualització de tots dos abans de reprendre l'ús periòdic de la instància.</span><span class="sxs-lookup"><span data-stu-id="b31eb-117">If both solutions are installed, you should plan to upgrade both before you resume regular use of the instance.</span></span>
- <span data-ttu-id="b31eb-118">Reviseu amb atenció els temes següents.</span><span class="sxs-lookup"><span data-stu-id="b31eb-118">Carefully review the following topics.</span></span> <span data-ttu-id="b31eb-119">La conscienciació i la comprensió dels canvis entre versions us ajudaran en el procés d'actualització.</span><span class="sxs-lookup"><span data-stu-id="b31eb-119">Awareness and understanding of the changes between versions will help you with the upgrade process.</span></span> <span data-ttu-id="b31eb-120">Aquests temes proporcionen informació sobre els canvis més importants del PSA, així com les consideracions i recomanacions per planificar l'actualització a la versió 3.x.</span><span class="sxs-lookup"><span data-stu-id="b31eb-120">These topics provide information about the major changes in PSA, together with considerations and recommendations for planning your upgrade to version 3.x.</span></span>

    - [<span data-ttu-id="b31eb-121">Novetats o canvis al Project Service Automation versió 3</span><span class="sxs-lookup"><span data-stu-id="b31eb-121">What's new or changed in Project Service Automation version 3</span></span>](whats-new-changed-v3.md)
    - [<span data-ttu-id="b31eb-122">Consideracions d'actualització - Project Service Automation 2.x o 1.x a la versió 3.x</span><span class="sxs-lookup"><span data-stu-id="b31eb-122">Upgrade considerations - Project Service Automation version 2.x or 1.x to version 3</span></span>](upgrade-v3.md)

- <span data-ttu-id="b31eb-123">Actualitzeu la instància d'espai aïllat per avaluar els canvis en la implementació abans d'actualitzar la instància de producció.</span><span class="sxs-lookup"><span data-stu-id="b31eb-123">Upgrade your sandbox instance to evaluate the changes in your implementation before you upgrade your production instance.</span></span>

<span data-ttu-id="b31eb-124">Després d'haver revisat els temes que s'han esmentat abans i que estigueu preparat per actualitzar a la versió 3.x o la versió basada en UCI, envieu una sol·licitud al suport tècnic de Microsoft per fer que l'actualització estigui disponible des del Centre d'administració.</span><span class="sxs-lookup"><span data-stu-id="b31eb-124">After you've reviewed the topics that were mentioned earlier and are ready to upgrade to PSA version 3.x or the UCI-based version, submit a request to Microsoft support to make the upgrade available from Admin center.</span></span> <span data-ttu-id="b31eb-125">A la vostra sol·licitud, proporcioneu els detalls de la instància.</span><span class="sxs-lookup"><span data-stu-id="b31eb-125">In your request, provide the details of your instance.</span></span>

## <a name="older-versions-of-psa-psa-version-2x-in-a-newly-created-instance"></a><span data-ttu-id="b31eb-126">Versions anteriors del PSA (versió PSA 2.x) en una instància creada recentment</span><span class="sxs-lookup"><span data-stu-id="b31eb-126">Older versions of PSA (PSA version 2.x) in a newly created instance</span></span>

<span data-ttu-id="b31eb-127">A partir del 17 de maig de 2019, totes les instàncies noves tindran l'UCI com a client per defecte.</span><span class="sxs-lookup"><span data-stu-id="b31eb-127">As of May 17, 2019, all new instances will have UCI as the default client.</span></span> <span data-ttu-id="b31eb-128">En coherència amb aquest canvi, la versió 3.x de PSA i la versió 8.x del Field Service seran subministrades per defecte, perquè aquestes versions estan dissenyades per treballar amb el client UCI.</span><span class="sxs-lookup"><span data-stu-id="b31eb-128">For alignment with this change, PSA version 3.x and Field Service version 8.x will be provisioned by default, because these versions are designed to work with the UCI client.</span></span>

<span data-ttu-id="b31eb-129">A partir del dia 1 de març de 2020, els clients del Dynamics PSA ja no podran crear nous entorns amb versions anteriors del PSA, per exemple, la versió 2.x o el PSA.</span><span class="sxs-lookup"><span data-stu-id="b31eb-129">Starting March 1st 2020, customers of Dynamics PSA will no longer be able to create a new environments with older versions of PSA, for example PSA version 2.x or lower.</span></span> <span data-ttu-id="b31eb-130">Qualsevol entorn nou només serà per obtenir la versió 3.x del PSA.</span><span class="sxs-lookup"><span data-stu-id="b31eb-130">Any new environment will be to get only version 3.x of PSA.</span></span>

> [!NOTE]
> <span data-ttu-id="b31eb-131">Per obtenir la millor experiència en utilitzar versions anteriors de les aplicacions del Field Service i el PSA, aneu a la pàgina **Configuració del sistema** i per al camp **Utilitza només la nova interfície unificada (recomanat)** seleccioneu **No**, perquè aquestes versions no estan dissenyades perquè es carreguin correctament a l'UCI.</span><span class="sxs-lookup"><span data-stu-id="b31eb-131">For the best experience when you use older versions of the Field Service and PSA applications, go to the **System settings** page and for the field, **Use the new Unified Interface only (recommended)** field, select **No** as these versions aren't designed to be correctly loaded in UCI.</span></span> <span data-ttu-id="b31eb-132">Després d'haver desactivat l'UCI, podeu obrir i executar aquestes versions de Field Service i el PSA mitjançant el client web antic.</span><span class="sxs-lookup"><span data-stu-id="b31eb-132">After you have turned off UCI, you can open and run these versions of Field Service and PSA by using the old web client.</span></span> <span data-ttu-id="b31eb-133">Per obtenir instruccions sobre com desactivar el client de l'UCI, vegeu [Habilitar només la interfície unificada](../admin/enable-unified-interface-only.md).</span><span class="sxs-lookup"><span data-stu-id="b31eb-133">For instructions about how to turn off the UCI client, see [Enable unified interface only](../admin/enable-unified-interface-only.md).</span></span>