---
title: Registrar-se a les subscripcions de versió preliminar del Project Operations per a escenaris de recursos/sense existències
description: En aquest tema es proporciona informació sobre com registrar-se i implementar el Project Operations per a escenaris de recursos/sense existències.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: da93fcf23ee3f255812842e31cb22b5d39daa963
ms.sourcegitcommit: 52b26950bb3b1596ad81aa4ff91745ee9615d1b0
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334815"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a><span data-ttu-id="95c8b-103">Registrar-se a les subscripcions de versió preliminar del Project Operations per a escenaris de recursos/sense existències</span><span class="sxs-lookup"><span data-stu-id="95c8b-103">Sign up for Project Operations preview subscriptions for resource/ non-stocked scenarios</span></span>

<span data-ttu-id="95c8b-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_</span><span class="sxs-lookup"><span data-stu-id="95c8b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="95c8b-105">En aquest tema s'explica com subscriure's a l'oferta de prova i implementar l'entorn del Project Operations per als escenaris basats en recursos/no mantinguts en existències.</span><span class="sxs-lookup"><span data-stu-id="95c8b-105">This topic explains how to subscribe to the trial offer and deploy Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="95c8b-106">Requisits previs</span><span class="sxs-lookup"><span data-stu-id="95c8b-106">Prerequisites</span></span>
- <span data-ttu-id="95c8b-107">L'usuari que implementa la versió preliminar ha de tenir drets d'administrador global a l'inquilí de l'Azure.</span><span class="sxs-lookup"><span data-stu-id="95c8b-107">The user who deploys the preview must have Azure tenant global administrator rights.</span></span> <span data-ttu-id="95c8b-108">Podeu crear un inquilí en bescanviar la primera oferta.</span><span class="sxs-lookup"><span data-stu-id="95c8b-108">You can create a tenant during the first offer redemption.</span></span> 
- <span data-ttu-id="95c8b-109">La implementació d'un entorn del Finance requereix una subscripció vàlida de l'Azure que es facturarà per entorn.</span><span class="sxs-lookup"><span data-stu-id="95c8b-109">Deploying a Finance environment requires a valid Azure subscription that will be billed per environment.</span></span> <span data-ttu-id="95c8b-110">Podeu utilitzar la subscripció existent de l'organització o utilitzar una [versió de prova de l'Azure](https://azure.microsoft.com/en-us/free/) per començar.</span><span class="sxs-lookup"><span data-stu-id="95c8b-110">You can use your organizations existing subscription or use an [Azure trial](https://azure.microsoft.com/en-us/free/) to get started.</span></span> <span data-ttu-id="95c8b-111">L'entorn del CDS es proporcionarà gratuïtament durant un període de 30 dies limitat.</span><span class="sxs-lookup"><span data-stu-id="95c8b-111">The CDS environment will be provided free for a limited 30 day period.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="95c8b-112">Només cal que una persona de l'organització, l'administrador d'inquilins, realitzi aquesta tasca.</span><span class="sxs-lookup"><span data-stu-id="95c8b-112">Only one person, the tenant administrator, in an organization needs to perform this task.</span></span> <span data-ttu-id="95c8b-113">Si no sou el subscriptor en aquesta versió, espereu fins que l'organització s'hagi registrat i hàgiu rebut les vostres credencials d'usuari.</span><span class="sxs-lookup"><span data-stu-id="95c8b-113">If you aren't the subscriber to this release, wait until your organization has been signed up and you've received your user credentials.</span></span>
> 
> <span data-ttu-id="95c8b-114">Les proves són d'un sol ús a l'inquilí.</span><span class="sxs-lookup"><span data-stu-id="95c8b-114">Trials are single use in the tenant.</span></span> <span data-ttu-id="95c8b-115">Una versió de prova només es pot executar una vegada.</span><span class="sxs-lookup"><span data-stu-id="95c8b-115">You can only run a trial one time.</span></span> <span data-ttu-id="95c8b-116">Us recomanem que creeu un inquilí nou per a la versió de prova.</span><span class="sxs-lookup"><span data-stu-id="95c8b-116">We recommend that you create a new tenant for the purpose of the trial.</span></span>


### <a name="dynamics-365-project-operations-ce---preview-trial"></a><span data-ttu-id="95c8b-117">Dynamics 365 Project Operations (CE): prova de versió preliminar</span><span class="sxs-lookup"><span data-stu-id="95c8b-117">Dynamics 365 Project Operations (CE) - Preview Trial</span></span> 

<span data-ttu-id="95c8b-118">Abans de començar, assegureu-vos que hàgiu iniciat la sessió en un navegador amb el compte laboral de l'usuari a l'inquilí on voleu la versió preliminar del Project Operations.</span><span class="sxs-lookup"><span data-stu-id="95c8b-118">Before you begin, make sure you are logged in to a browser with the user work account in the tenant where you want the Project Operations preview.</span></span>

1. <span data-ttu-id="95c8b-119">Bescanvieu el primer codi de l'oferta, **Dynamics 365 Project Operations**, aquí [Prova del Project Operations](https://aka.ms/try-po).</span><span class="sxs-lookup"><span data-stu-id="95c8b-119">Redeem the first offer code, **Dynamics 365 Project Operations** here [Project Operations Trial](https://aka.ms/try-po).</span></span>
2. <span data-ttu-id="95c8b-120">Confirmeu la comanda.</span><span class="sxs-lookup"><span data-stu-id="95c8b-120">Confirm your order.</span></span>

  <span data-ttu-id="95c8b-121">Veureu que l'oferta de confirmació s'ha bescanviat correctament.</span><span class="sxs-lookup"><span data-stu-id="95c8b-121">You will see confirmation offer was successfully redeemed.</span></span>

### <a name="dynamics-365-finance-preview-trial"></a><span data-ttu-id="95c8b-122">Prova de versió preliminar del Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="95c8b-122">Dynamics 365 Finance preview trial</span></span>

<span data-ttu-id="95c8b-123">Aneu a [Prova de versió preliminar del Dynamics 365 for Finance](https://aka.ms/trypoche) i repetiu els passos de la secció anterior amb l'oferta Registrar-se per obtenir un entorn allotjat al núvol.</span><span class="sxs-lookup"><span data-stu-id="95c8b-123">Go to [Dynamics 365 for Finance Preview Trial](https://aka.ms/trypoche) and repeat the steps from the previous section with the offer, Sign up for the Cloud Hosted Environment.</span></span>  

## <a name="assign-licenses"></a><span data-ttu-id="95c8b-124">Assignar llicències</span><span class="sxs-lookup"><span data-stu-id="95c8b-124">Assign licenses</span></span>

> [!IMPORTANT]
> <span data-ttu-id="95c8b-125">Necessitareu accés d'administrador al portal del Microsoft 365 de l'organització per completar els passos següents.</span><span class="sxs-lookup"><span data-stu-id="95c8b-125">You will need administrative access to your organization's Microsoft 365 Portal to complete the following steps.</span></span>

1. <span data-ttu-id="95c8b-126">Aneu al [centre d'administració del Microsoft 365](https://portal.office.com/) per assignar les llicències als usuaris.</span><span class="sxs-lookup"><span data-stu-id="95c8b-126">Go to [Microsoft 365 admin center](https://portal.office.com/) to assign the licenses to your users.</span></span>

2. <span data-ttu-id="95c8b-127">A la pàgina **Usuaris actius**, seleccioneu els usuaris als quals voleu assignar una llicència.</span><span class="sxs-lookup"><span data-stu-id="95c8b-127">On the **Active users** page, select the users that you want to assign a license to.</span></span>

3. <span data-ttu-id="95c8b-128">Verifiqueu que la llicència del **Dynamics 365 Project Operations** estigui seleccionat i seleccioneu **Desa els canvis**.</span><span class="sxs-lookup"><span data-stu-id="95c8b-128">Verify that the **Dynamics 365 Project Operations** license has been selected and select **Save changes**.</span></span>

> [!NOTE]
> <span data-ttu-id="95c8b-129">L'oferta de prova del Finance no s'ha d'assignar a un usuari.</span><span class="sxs-lookup"><span data-stu-id="95c8b-129">The Finance trial offer does not need to be assigned to a user.</span></span>

## <a name="start-a-new-project-in-lcs"></a><span data-ttu-id="95c8b-130">Iniciar un projecte nou al LCS</span><span class="sxs-lookup"><span data-stu-id="95c8b-130">Start a new project in LCS</span></span>

<span data-ttu-id="95c8b-131">Creeu un projecte nou del LCS tal com es descriu al tema [Iniciar un projecte nou al LCS](create-lcs-project.md)</span><span class="sxs-lookup"><span data-stu-id="95c8b-131">Create a new LCS project as described in the topic, [Start a new project in LCS](create-lcs-project.md)</span></span>

## <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="95c8b-132">Addició d'una subscripció a l'Azure a un projecte del LCS</span><span class="sxs-lookup"><span data-stu-id="95c8b-132">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="95c8b-133">Per completar aquesta tasca, seguiu els passos del tema [Afegir una subscripció de l'Azure al projecte del LCS](resource-add-azure-subscription-lcs-project.md).</span><span class="sxs-lookup"><span data-stu-id="95c8b-133">To complete this task, follow the steps in the topic, [Add an Azure subscription to LCS project](resource-add-azure-subscription-lcs-project.md).</span></span>

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="95c8b-134">Implementar l'entorn de demostració del Finance amb el Project Operations per a escenaris de recursos/sense existències</span><span class="sxs-lookup"><span data-stu-id="95c8b-134">Deploy Finance demo environment with Project Operations for resource/non-stocked scenarios</span></span>

<span data-ttu-id="95c8b-135">Seguiu les instruccions del tema [Proveir un nou entorn](resource-provision-new-environment.md) per completar la implementació.</span><span class="sxs-lookup"><span data-stu-id="95c8b-135">Follow the guidance in the topic, [Provision a new environment](resource-provision-new-environment.md) to complete the deployment.</span></span> <span data-ttu-id="95c8b-136">Utilitzeu el tipus d'implementació [entorn de demostració](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) per a la versió preliminar.</span><span class="sxs-lookup"><span data-stu-id="95c8b-136">Use the [demo environment](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) deployment type for preview.</span></span> 

## <a name="install-cds-setup-and-configuration-data"></a><span data-ttu-id="95c8b-137">Configuració de la instal·lació del CDS i dades de configuració</span><span class="sxs-lookup"><span data-stu-id="95c8b-137">Install CDS setup and configuration data</span></span>

<span data-ttu-id="95c8b-138">Instal·leu les dades instal·lació i les dades de configuració del CDS com es descriu al tema [Configurar i aplicar les dades de configuració al Common Data Service](resource-apply-pro-setup-config-data.md).</span><span class="sxs-lookup"><span data-stu-id="95c8b-138">Install CDS setup and configuration data as described in the topic, [Set up and apply configuration data in the Common Data Service](resource-apply-pro-setup-config-data.md).</span></span>
<span data-ttu-id="95c8b-139">Completeu aquest pas només quan s'implementi l'entorn de demostració del Finance i les dades de demostració estiguin a punt.</span><span class="sxs-lookup"><span data-stu-id="95c8b-139">Complete this step only after Finance demo environment is deployed and demo data is ready.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
