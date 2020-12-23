---
title: Implementació del Project Operations (bàsic)
description: 'En aquest tema es proporciona informació sobre com instal·lar la implementació bàsica del Project Operations: acord a facturació proforma.'
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: d4ef905f875ac8af7b2d70c3e64506558bdea1ed
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642171"
---
# <a name="deploy-project-operations---lite"></a><span data-ttu-id="35849-103">Implementació del Project Operations (bàsic)</span><span class="sxs-lookup"><span data-stu-id="35849-103">Deploy Project Operations - lite</span></span>

<span data-ttu-id="35849-104">_**S'aplica a:** implementació bàsica: tracte de facturació proforma_</span><span class="sxs-lookup"><span data-stu-id="35849-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="35849-105">El Project Operations admet diversos models d'implementació.</span><span class="sxs-lookup"><span data-stu-id="35849-105">Project Operations supports multiple deployment models.</span></span> <span data-ttu-id="35849-106">Per determinar el millor model d'implementació, vegeu [Tipus d'implementació](determine-deployment-type.md).</span><span class="sxs-lookup"><span data-stu-id="35849-106">To determine the best deployment model, see [Deployment types](determine-deployment-type.md).</span></span>


> [!IMPORTANT]
> <span data-ttu-id="35849-107">Aquesta implementació, la implementació bàsica: acord a facturació proforma, genera una **implementació del Project Operations només del Common Data Service**.</span><span class="sxs-lookup"><span data-stu-id="35849-107">This deployment, Lite deployment – deal to proforma invoicing, results in a **Common Data Service-only deployment of Project Operations**.</span></span>

- [<span data-ttu-id="35849-108">Instal·lar el Project Operations en un nou entorn</span><span class="sxs-lookup"><span data-stu-id="35849-108">Install Project Operations into a new CDS environment</span></span>](#new)
- [<span data-ttu-id="35849-109">Instal·lació en un entorn del CDS existent</span><span class="sxs-lookup"><span data-stu-id="35849-109">Install into an existing CDS environment</span></span>](#existing)



## <a name="install-project-operations-to-a-new-cds-environment"></a><a name="new"></a><span data-ttu-id="35849-110">Instal·lar el Project Operations en un nou entorn del CDS</span><span class="sxs-lookup"><span data-stu-id="35849-110">Install Project Operations to a new CDS environment</span></span>

1. <span data-ttu-id="35849-111">Com a [administrador global o del Power Platform](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) amb una llicència del Project Operations, creeu un entorn del CDS nou al [centre d'administració del Power Platform](https://admin.powerplatform.com).</span><span class="sxs-lookup"><span data-stu-id="35849-111">As the [Global or Power Platform Administrator](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) with a Project Operations license, create a new CDS environment in the [PowerPlatform admin center](https://admin.powerplatform.com).</span></span> <span data-ttu-id="35849-112">Assegureu-vos que **Base de dades del CDS** i **Aplicacions del Dynamics 365** estiguin habilitades.</span><span class="sxs-lookup"><span data-stu-id="35849-112">Make sure that **CDS database** and **Dynamics 365 Apps** are enabled.</span></span> <span data-ttu-id="35849-113">Per obtenir informació, vegeu [Crear i administrar entorns al centre d'administració del Power Platform](https://docs.microsoft.com/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).</span><span class="sxs-lookup"><span data-stu-id="35849-113">For more information, see [Create and manage environments in the Power Platform admin center](https://docs.microsoft.com/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).</span></span>
2. <span data-ttu-id="35849-114">Seleccioneu **Microsoft Dynamics 365 Project Operations** des de la llista d'implementació de les aplicacions del Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="35849-114">Select **Microsoft Dynamics 365 Project Operations** from the deployment list of Dynamics 365 apps.</span></span>


## <a name="install-project-operations-to-an-existing-cds-environment"></a><a name="existing"></a><span data-ttu-id="35849-115">Instal·lar el Project Operations en un entorn existent del CDS</span><span class="sxs-lookup"><span data-stu-id="35849-115">Install Project Operations to an existing CDS environment</span></span>

1. <span data-ttu-id="35849-116">Com a [administrador global o del Power Platform](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) amb una llicència del Project Operations, localitzeu l'entorn al [centre d'administració del Power Platform](https://admin.powerplatform.com) on voleu instal·lar el Project Operations.</span><span class="sxs-lookup"><span data-stu-id="35849-116">As the [Global or Power Platform Administrator](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) with a Project Operations license, locate the environment in the [PowerPlatform admin center](https://admin.powerplatform.com) where you want to install Project Operations.</span></span>
2. <span data-ttu-id="35849-117">Instal·leu **Microsoft Dynamics 365 Project Operations** des de la llista d'implementació de les aplicacions del Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="35849-117">Install **Microsoft Dynamics 365 Project Operations** from the deployment list of Dynamics 365 apps.</span></span> <span data-ttu-id="35849-118">Per obtenir més informació, vegeu [Administrar les aplicacions del Dynamics 365](https://docs.microsoft.com/power-platform/admin/manage-apps).</span><span class="sxs-lookup"><span data-stu-id="35849-118">For more information, see [Manage Dynamics 365 apps](https://docs.microsoft.com/power-platform/admin/manage-apps).</span></span>


