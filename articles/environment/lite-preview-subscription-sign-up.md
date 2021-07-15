---
title: Registre per obtenir una subscripció de versió preliminar (bàsic)
description: "En aquest tema es proporciona informació sobre com subscriure's i implementar la implementació bàsica del Project Operations: acord a facturació proforma."
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 2b5a65f5e29915c349d40400ebbf3e4923b36a67
ms.sourcegitcommit: 52b26950bb3b1596ad81aa4ff91745ee9615d1b0
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334770"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a><span data-ttu-id="fc9f7-103">Registre per obtenir una subscripció de versió preliminar (bàsica)</span><span class="sxs-lookup"><span data-stu-id="fc9f7-103">Sign up for a preview subscription - lite</span></span> 

<span data-ttu-id="fc9f7-104">En aquest tema s'explica com subscriure's a l'oferta de prova i implementar l'oferta d'implementació bàsica del Dynamics 365 Project Operations a la facturació proforma.</span><span class="sxs-lookup"><span data-stu-id="fc9f7-104">This topic explains how to subscribe to the trial offer and deploy Dynamics 365 Project Operations lite deployment - deal to proforma invoicing.</span></span>

> [!NOTE]
> <span data-ttu-id="fc9f7-105">Aquest procés canviarà en pròximes versions del Project Operations.</span><span class="sxs-lookup"><span data-stu-id="fc9f7-105">This process will change in upcoming releases of Project Operations.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="fc9f7-106">Requisits previs</span><span class="sxs-lookup"><span data-stu-id="fc9f7-106">Prerequisites</span></span>
- <span data-ttu-id="fc9f7-107">L'usuari que implementa la versió preliminar ha de tenir drets d'administrador global a l'inquilí de l'Azure.</span><span class="sxs-lookup"><span data-stu-id="fc9f7-107">The user who deploys the preview must have Azure tenant global administrator rights.</span></span> <span data-ttu-id="fc9f7-108">Podeu crear un inquilí en bescanviar la primera oferta.</span><span class="sxs-lookup"><span data-stu-id="fc9f7-108">You can create a tenant during the first offer redemption.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fc9f7-109">Només cal que una persona de l'organització, l'administrador d'inquilins, realitzi aquesta tasca.</span><span class="sxs-lookup"><span data-stu-id="fc9f7-109">Only one person, the tenant administrator, in an organization needs to perform this task.</span></span> <span data-ttu-id="fc9f7-110">Si no sou el subscriptor en aquesta versió, espereu fins que l'organització s'hagi registrat i hàgiu rebut les vostres credencials d'usuari.</span><span class="sxs-lookup"><span data-stu-id="fc9f7-110">If you aren't the subscriber to this release, wait until your organization has been signed up and you've received your user credentials.</span></span>
> 
> <span data-ttu-id="fc9f7-111">Les proves són d'un sol ús a l'inquilí.</span><span class="sxs-lookup"><span data-stu-id="fc9f7-111">Trials are single use in the tenant.</span></span> <span data-ttu-id="fc9f7-112">Una versió de prova només es pot executar una vegada.</span><span class="sxs-lookup"><span data-stu-id="fc9f7-112">You can only run a trial one time.</span></span> <span data-ttu-id="fc9f7-113">Us recomanem que creeu un inquilí nou per a la versió de prova.</span><span class="sxs-lookup"><span data-stu-id="fc9f7-113">We recommend that you create a new tenant for the purpose of the trial.</span></span>

### <a name="dynamics-365-project-operations-trial"></a><span data-ttu-id="fc9f7-114">Prova del Dynamics 365 Project Operations</span><span class="sxs-lookup"><span data-stu-id="fc9f7-114">Dynamics 365 Project Operations trial</span></span> 

<span data-ttu-id="fc9f7-115">Abans de començar, assegureu-vos que hàgiu iniciat la sessió en un navegador amb el compte laboral de l'usuari a l'inquilí on voleu la versió preliminar del Project Operations.</span><span class="sxs-lookup"><span data-stu-id="fc9f7-115">Before you begin, make sure you are logged in to a browser with the user work account in the tenant where you want the Project Operations preview.</span></span>

1. <span data-ttu-id="fc9f7-116">Aneu a [Prova del Project Operations](https://aka.ms/try-po) per bescanviar el primer codi de l'oferta, **Dynamics 365 Project Operations**.</span><span class="sxs-lookup"><span data-stu-id="fc9f7-116">Go to [Project Operations Trial](https://aka.ms/try-po) to redeem the first offer code, **Dynamics 365 Project Operations**.</span></span>
2. <span data-ttu-id="fc9f7-117">Confirmeu la comanda.</span><span class="sxs-lookup"><span data-stu-id="fc9f7-117">Confirm your order.</span></span>

  <span data-ttu-id="fc9f7-118">Veureu que l'oferta de confirmació s'ha bescanviat correctament.</span><span class="sxs-lookup"><span data-stu-id="fc9f7-118">You'll see the confirmation offer was successfully redeemed.</span></span>

## <a name="assign-licenses"></a><span data-ttu-id="fc9f7-119">Assignar llicències</span><span class="sxs-lookup"><span data-stu-id="fc9f7-119">Assign licenses</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fc9f7-120">Necessitareu accés d'administrador al portal del Microsoft 365 de l'organització per completar els passos següents.</span><span class="sxs-lookup"><span data-stu-id="fc9f7-120">You will need administrative access to your organization's Microsoft 365 Portal to complete the following steps.</span></span>


1. <span data-ttu-id="fc9f7-121">Aneu al [centre d'administració del Microsoft 365](https://portal.office.com/) per assignar les llicències als usuaris.</span><span class="sxs-lookup"><span data-stu-id="fc9f7-121">Go to [Microsoft 365 admin center](https://portal.office.com/) to assign the licenses to your users.</span></span>
2. <span data-ttu-id="fc9f7-122">A la pàgina **Usuaris actius**, seleccioneu els usuaris als quals voleu assignar una llicència.</span><span class="sxs-lookup"><span data-stu-id="fc9f7-122">On the **Active users** page, select the users that you want to assign a license to.</span></span>
3. <span data-ttu-id="fc9f7-123">Verifiqueu que la llicència del **Dynamics 365 Project Operations** estigui seleccionada.</span><span class="sxs-lookup"><span data-stu-id="fc9f7-123">Verify that the **Dynamics 365 Project Operations** license is selected.</span></span> 
4. <span data-ttu-id="fc9f7-124">Seleccioneu **Desa els canvis**.</span><span class="sxs-lookup"><span data-stu-id="fc9f7-124">Select **Save changes**.</span></span>

## <a name="create-a-new-dataverse-environment"></a><span data-ttu-id="fc9f7-125">Crear un entorn nou del Dataverse</span><span class="sxs-lookup"><span data-stu-id="fc9f7-125">Create a new Dataverse environment</span></span>

1. <span data-ttu-id="fc9f7-126">Proveïu d'un nou entorn d'implementació del Dataverse del Project Operations seguint les instruccions del tema [Model d'implementació del Dataverse](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="fc9f7-126">Provision a new Project Operations Dataverse deployment environment by following instructions in the topic, [Dataverse deployment model](lite-deployment.md).</span></span> <span data-ttu-id="fc9f7-127">Quan seleccioneu el tipus d'entorn, assegureu-vos d'utilitzar **Prova (basada en subscripció)**.</span><span class="sxs-lookup"><span data-stu-id="fc9f7-127">When you select the environment type, make sure to use **Trial (Subscription based)**.</span></span>

  ![Entorn nou](./media/19CreateEnvironment.png)

2. <span data-ttu-id="fc9f7-129">Seleccioneu l'opció **Habilita les aplicacions del Dynamics 365** i deixeu **Implementa aquestes aplicacions automàticament** en blanc.</span><span class="sxs-lookup"><span data-stu-id="fc9f7-129">Select the **Enable Dynamics 365 apps** setting, and leave **Automatically deploy these apps** blank.</span></span>  
3. <span data-ttu-id="fc9f7-130">Seleccioneu **Desa** per crear l'entorn.</span><span class="sxs-lookup"><span data-stu-id="fc9f7-130">Select **Save** to create the environment.</span></span>

  ![Afegeix base de dades](./media/20CreateEnvironment1.png)

4. <span data-ttu-id="fc9f7-132">Un cop creat l'entorn, instal·leu la solució **Microsoft Dynamics 365 Project Operations**.</span><span class="sxs-lookup"><span data-stu-id="fc9f7-132">After the environment is created, install **Microsoft Dynamics 365 Project Operations** solution.</span></span> 

![Instal·lar la solució](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a><span data-ttu-id="fc9f7-134">Instal·lar una configuració del CDS i configurar les dades de demostració</span><span class="sxs-lookup"><span data-stu-id="fc9f7-134">Install a CDS configuration and setup demo data</span></span>

<span data-ttu-id="fc9f7-135">Instal·leu la configuració del CDS i configureu les dades de demostració seguint les instruccions del tema [Aplicar la configuració de la demostració i les dades de configuració](lite-apply-demo-setup-config-data.md).</span><span class="sxs-lookup"><span data-stu-id="fc9f7-135">Install the CDS configuration and set up demo data by following instructions in the topic, [Apply demo setup and configuration data](lite-apply-demo-setup-config-data.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
