---
title: Comandes de vendes de projectes per a projectes de temps i materials
description: En aquest tema s'explica com crear comandes de vendes basades en projectes per a projectes de temps i materials.
author: KimANelson
manager: AnnBe
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: 05ab0cf6-318c-42de-ba56-3e662283497e
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 446c73e9491b1892847caf7e843c802292107ef9
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749449"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a><span data-ttu-id="f066a-103">Comandes de vendes de projectes per a projectes de temps i materials</span><span class="sxs-lookup"><span data-stu-id="f066a-103">Project sales orders for time and material projects</span></span>

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

<span data-ttu-id="f066a-104">En aquest tema es descriu com crear una comanda de vendes per a un projecte.</span><span class="sxs-lookup"><span data-stu-id="f066a-104">This topic describes how to create a sales order for a project.</span></span> <span data-ttu-id="f066a-105">Les comandes de vendes només es poden crear per a projectes del tipus de **temps i materials**.</span><span class="sxs-lookup"><span data-stu-id="f066a-105">Sales orders can only be created for projects of type **time and material**.</span></span>

<span data-ttu-id="f066a-106">Si un projecte de temps i material té diverses fonts de finançament al contracte del projecte, heu d'habilitar el paràmetre **Permet les comandes de vendes per a projectes amb diverses fonts de finançament** a la pàgina **Paràmetres de l'administració de projectes i la comptabilitat**.</span><span class="sxs-lookup"><span data-stu-id="f066a-106">If a time and material project has multiple funding sources on the project contract, you must enable the **Allow sales orders for projects with multiple funding sources** parameter on the **Project management and accounting parameters** page.</span></span> 

> [!NOTE]
> - <span data-ttu-id="f066a-107">El suport per a les comandes de vendes de projectes amb diverses fonts de finançament està disponible a partir de la versió de l'aplicació 10.0.2 i versions posteriors.</span><span class="sxs-lookup"><span data-stu-id="f066a-107">Support for project sales orders with multiple funding sources is available starting with application release 10.0.2 and higher.</span></span>
> - <span data-ttu-id="f066a-108">El paràmetre per habilitar el suport per a les comandes de vendes de projectes amb diverses fonts de finançament se suprimirà a la fase de llançament d'abril de 2020, després de la qual la funcionalitat estarà sempre activada.</span><span class="sxs-lookup"><span data-stu-id="f066a-108">The parameter to enable the support for project sales orders with multiple funding sources will be removed in the April 2020 release wave, after which the functionality will always be enabled.</span></span>

<span data-ttu-id="f066a-109">Podeu crear comandes de vendes basades en projectes de dues maneres diferents:</span><span class="sxs-lookup"><span data-stu-id="f066a-109">You can create project-based sales orders in two ways:</span></span>

- <span data-ttu-id="f066a-110">Aneu al projecte en si mateix.</span><span class="sxs-lookup"><span data-stu-id="f066a-110">Go to the project itself.</span></span> <span data-ttu-id="f066a-111">A la subfinestra acció, seleccioneu **Administra > Tasques d'article > Comanda de vendes**.</span><span class="sxs-lookup"><span data-stu-id="f066a-111">On the Action Pane, select **Manage > Item tasks > Sales order**.</span></span> <span data-ttu-id="f066a-112">La informació del projecte es definirà per defecte a la comanda de vendes del projecte.</span><span class="sxs-lookup"><span data-stu-id="f066a-112">The project information will default to the sales order from the project.</span></span> <span data-ttu-id="f066a-113">Si el contracte del projecte té més d'una font de finançament, haureu de seleccionar la font de finançament per definir el client per a la comanda de vendes.</span><span class="sxs-lookup"><span data-stu-id="f066a-113">If the project contract has more than one funding source, you will need to select the funding source to set the customer for the sales order.</span></span> <span data-ttu-id="f066a-114">Si només hi ha una font de finançament per al projecte, el client es definirà automàticament.</span><span class="sxs-lookup"><span data-stu-id="f066a-114">If there is only one funding source for the project, the customer will be automatically set.</span></span>
- <span data-ttu-id="f066a-115">Aneu a la pàgina de llista **Totes les comandes de vendes** i creeu una comanda de vendes nova.</span><span class="sxs-lookup"><span data-stu-id="f066a-115">Go to the **All sales order** list page and create a new sales order.</span></span> <span data-ttu-id="f066a-116">Haureu de seleccionar el projecte per a la comanda de vendes.</span><span class="sxs-lookup"><span data-stu-id="f066a-116">You will need to select the project for the sales order.</span></span> <span data-ttu-id="f066a-117">Després de seleccionar el projecte, el client es definirà des de la font del finançament o haureu de seleccionar la font del finançament si el contracte del projecte té diverses fonts de finançament.</span><span class="sxs-lookup"><span data-stu-id="f066a-117">After the project is selected, the customer will be set from the funding source or you will need to select the funding source if the project contract has multiple funding sources.</span></span>

