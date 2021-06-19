---
title: Comandes de vendes de projectes per a projectes de temps i materials
description: En aquest tema s'explica com crear comandes de vendes basades en projectes per a projectes de temps i materials.
author: Yowelle
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: dec9bc700d18f71ec7c9e976b38cb8cbb41f21b5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6009649"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a><span data-ttu-id="4c753-103">Comandes de vendes de projectes per a projectes de temps i materials</span><span class="sxs-lookup"><span data-stu-id="4c753-103">Project sales orders for time and material projects</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="4c753-104">En aquest tema es descriu com crear una comanda de vendes per a un projecte.</span><span class="sxs-lookup"><span data-stu-id="4c753-104">This topic describes how to create a sales order for a project.</span></span> <span data-ttu-id="4c753-105">Les comandes de vendes només es poden crear per a projectes del tipus de **temps i materials**.</span><span class="sxs-lookup"><span data-stu-id="4c753-105">Sales orders can only be created for projects of type **time and material**.</span></span>

<span data-ttu-id="4c753-106">Si un projecte de temps i material té diverses fonts de finançament al contracte del projecte, heu d'habilitar el paràmetre **Permet les comandes de vendes per a projectes amb diverses fonts de finançament** a la pàgina **Paràmetres de l'administració de projectes i la comptabilitat**.</span><span class="sxs-lookup"><span data-stu-id="4c753-106">If a time and material project has multiple funding sources on the project contract, you must enable the **Allow sales orders for projects with multiple funding sources** parameter on the **Project management and accounting parameters** page.</span></span> 

> [!NOTE]
> - <span data-ttu-id="4c753-107">El suport per a les comandes de vendes de projectes amb diverses fonts de finançament està disponible a partir de la versió de l'aplicació 10.0.2 i versions posteriors.</span><span class="sxs-lookup"><span data-stu-id="4c753-107">Support for project sales orders with multiple funding sources is available starting with application release 10.0.2 and higher.</span></span>
> - <span data-ttu-id="4c753-108">El paràmetre per habilitar el suport per a les comandes de vendes de projectes amb diverses fonts de finançament se suprimirà a la fase de llançament d'abril de 2020, després de la qual la funcionalitat estarà sempre activada.</span><span class="sxs-lookup"><span data-stu-id="4c753-108">The parameter to enable the support for project sales orders with multiple funding sources will be removed in the April 2020 release wave, after which the functionality will always be enabled.</span></span>

<span data-ttu-id="4c753-109">Podeu crear comandes de vendes basades en projectes de dues maneres diferents:</span><span class="sxs-lookup"><span data-stu-id="4c753-109">You can create project-based sales orders in two ways:</span></span>

- <span data-ttu-id="4c753-110">Aneu al projecte en si mateix.</span><span class="sxs-lookup"><span data-stu-id="4c753-110">Go to the project itself.</span></span> <span data-ttu-id="4c753-111">A la subfinestra acció, seleccioneu **Administra > Tasques d'article > Comanda de vendes**.</span><span class="sxs-lookup"><span data-stu-id="4c753-111">On the Action Pane, select **Manage > Item tasks > Sales order**.</span></span> <span data-ttu-id="4c753-112">La informació del projecte es definirà per defecte a la comanda de vendes del projecte.</span><span class="sxs-lookup"><span data-stu-id="4c753-112">The project information will default to the sales order from the project.</span></span> <span data-ttu-id="4c753-113">Si el contracte del projecte té més d'una font de finançament, haureu de seleccionar la font de finançament per definir el client per a la comanda de vendes.</span><span class="sxs-lookup"><span data-stu-id="4c753-113">If the project contract has more than one funding source, you will need to select the funding source to set the customer for the sales order.</span></span> <span data-ttu-id="4c753-114">Si només hi ha una font de finançament per al projecte, el client es definirà automàticament.</span><span class="sxs-lookup"><span data-stu-id="4c753-114">If there is only one funding source for the project, the customer will be automatically set.</span></span>
- <span data-ttu-id="4c753-115">Aneu a la pàgina de llista **Totes les comandes de vendes** i creeu una comanda de vendes nova.</span><span class="sxs-lookup"><span data-stu-id="4c753-115">Go to the **All sales order** list page and create a new sales order.</span></span> <span data-ttu-id="4c753-116">Haureu de seleccionar el projecte per a la comanda de vendes.</span><span class="sxs-lookup"><span data-stu-id="4c753-116">You will need to select the project for the sales order.</span></span> <span data-ttu-id="4c753-117">Després de seleccionar el projecte, el client es definirà des de la font del finançament o haureu de seleccionar la font del finançament si el contracte del projecte té diverses fonts de finançament.</span><span class="sxs-lookup"><span data-stu-id="4c753-117">After the project is selected, the customer will be set from the funding source or you will need to select the funding source if the project contract has multiple funding sources.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]