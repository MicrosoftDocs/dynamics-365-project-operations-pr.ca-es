---
title: Registrar-se a les subscripcions de versió preliminar del Project Operations per a escenaris de recursos/sense existències
description: En aquest tema es proporciona informació sobre com registrar-se i implementar el Project Operations per a escenaris de recursos/sense existències.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4d35a8bf9e8a841b45808b26ae2587c5b7d99d72
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948762"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a><span data-ttu-id="8220b-103">Registrar-se a les subscripcions de versió preliminar del Project Operations per a escenaris de recursos/sense existències</span><span class="sxs-lookup"><span data-stu-id="8220b-103">Sign up for Project Operations preview subscriptions for resource/ non-stocked scenarios</span></span>

<span data-ttu-id="8220b-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_</span><span class="sxs-lookup"><span data-stu-id="8220b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="8220b-105">En aquest tema s'explica com subscriure's a l'oferta de versió preliminar/associats i implementar l'entorn del Project Operations per a escenaris de recursos/sense existències.</span><span class="sxs-lookup"><span data-stu-id="8220b-105">This topic explains how to subscribe to the preview/partner offer and deploy Project Operations environment for resource/ non-stocked based scenarios.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="8220b-106">Requisits previs</span><span class="sxs-lookup"><span data-stu-id="8220b-106">Prerequisites</span></span>

- <span data-ttu-id="8220b-107">Rebreu un correu electrònic que us convidarà a participar a la versió preliminar.</span><span class="sxs-lookup"><span data-stu-id="8220b-107">You will receive an email inviting you to participate in the preview.</span></span> <span data-ttu-id="8220b-108">Podeu sol·licitar una versió preliminar al [lloc web del Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).</span><span class="sxs-lookup"><span data-stu-id="8220b-108">You can request a preview on the [Project Operations website](https://dynamics.microsoft.com/en-us/project-operations/overview/).</span></span>
- <span data-ttu-id="8220b-109">L'usuari que implementa la versió preliminar ha de tenir drets d'administrador global a l'inquilí de l'Azure.</span><span class="sxs-lookup"><span data-stu-id="8220b-109">The user who deploys the preview must have Azure tenant global administrator rights.</span></span>
- <span data-ttu-id="8220b-110">La implementació d'un entorn del Finance requereix una subscripció vàlida de l'Azure que es facturarà per entorn.</span><span class="sxs-lookup"><span data-stu-id="8220b-110">Deploying a Finance environment requires a valid Azure subscription that will be billed per environment.</span></span> <span data-ttu-id="8220b-111">Podeu utilitzar la subscripció existent de l'organització o utilitzar una [versió de prova de l'Azure](https://azure.microsoft.com/en-us/free/) per començar.</span><span class="sxs-lookup"><span data-stu-id="8220b-111">You can use your organizations existing subscription or use an [Azure trial](https://azure.microsoft.com/en-us/free/) to get started.</span></span> <span data-ttu-id="8220b-112">L'entorn del CDS es proporcionarà gratuïtament durant un període de 30 dies limitat.</span><span class="sxs-lookup"><span data-stu-id="8220b-112">The CDS environment will be provided free for a limited 30 day period.</span></span>

## <a name="subscribe"></a><span data-ttu-id="8220b-113">Subscripció</span><span class="sxs-lookup"><span data-stu-id="8220b-113">Subscribe</span></span>

<span data-ttu-id="8220b-114">Quan s'aprovi la [sol·licitud de versió preliminar](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u), rebreu dues ofertes de Microsoft per correu electrònic.</span><span class="sxs-lookup"><span data-stu-id="8220b-114">When your [preview request](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) is approved, you will receive two offers from Microsoft by email.</span></span> <span data-ttu-id="8220b-115">Aquestes ofertes us permeten implementar la versió preliminar del Project Operations:</span><span class="sxs-lookup"><span data-stu-id="8220b-115">These offers allow you to deploy the Project Operations Preview:</span></span>

- <span data-ttu-id="8220b-116">Dynamics 365 Project Operations: prova de versió preliminar</span><span class="sxs-lookup"><span data-stu-id="8220b-116">Dynamics 365 Project Operations – Preview Trial</span></span>
- <span data-ttu-id="8220b-117">Prova de versió preliminar del Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8220b-117">Dynamics 365 for Finance and Operations Preview Trial.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8220b-118">Només cal que una persona de l'organització, l'administrador d'inquilins, realitzi aquesta tasca.</span><span class="sxs-lookup"><span data-stu-id="8220b-118">Only one person, the tenant administrator, in an organization needs to perform this task.</span></span> <span data-ttu-id="8220b-119">Si no sou el subscriptor en aquesta versió, espereu fins que l'organització s'hagi registrat i hàgiu rebut les vostres credencials d'usuari.</span><span class="sxs-lookup"><span data-stu-id="8220b-119">If you aren't the subscriber to this release, wait until your organization has been signed up and you've received your user credentials.</span></span>

### <a name="dynamics-365-project-operations--preview-trial"></a><span data-ttu-id="8220b-120">Dynamics 365 Project Operations: prova de versió preliminar</span><span class="sxs-lookup"><span data-stu-id="8220b-120">Dynamics 365 Project Operations – Preview trial</span></span>

1. <span data-ttu-id="8220b-121">Bescanvieu la primera oferta, **Prova del Dynamics 365 Project Operations**, amb l'adreça URL proporcionada al correu electrònic de benvinguda.</span><span class="sxs-lookup"><span data-stu-id="8220b-121">Redeem the first offer, **Dynamics 365 Project Operations Trial**, with the URL provided in your welcome email.</span></span>

![Primera oferta](./media/1FirstOffer.png)

2. <span data-ttu-id="8220b-123">Verifiqueu que heu iniciat la sessió com a l'usuari que pertany a l'organització que se subscriurà el servei.</span><span class="sxs-lookup"><span data-stu-id="8220b-123">Verify that you are logged in as the user who belongs to the organization who will be subscribing to the service.</span></span>
3. <span data-ttu-id="8220b-124">Continueu amb el bescanvi de l'oferta.</span><span class="sxs-lookup"><span data-stu-id="8220b-124">Proceed with redeeming the offer.</span></span> 
4. <span data-ttu-id="8220b-125">Seleccioneu **Sí, afegeix-ho al meu compte**.</span><span class="sxs-lookup"><span data-stu-id="8220b-125">Select **Yes, add it to my account**.</span></span>

![Bescanviar l'oferta](./media/2RedeemFirstOffer.png)

![Confirmar l'oferta](./media/3ConfirmFirstOffer.png)

![Oferta bescanviada](./media/4OfferSuccessfulyRedeemed.png)

### <a name="dynamics-365-finance-preview-trial"></a><span data-ttu-id="8220b-129">Prova de versió preliminar del Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="8220b-129">Dynamics 365 Finance preview trial</span></span>

<span data-ttu-id="8220b-130">Repetiu els mateixos passos amb la segona oferta del correu electrònic de benvinguda.</span><span class="sxs-lookup"><span data-stu-id="8220b-130">Repeat the same steps with the second offer from the Welcome email.</span></span>

## <a name="assign-licenses"></a><span data-ttu-id="8220b-131">Assignar llicències</span><span class="sxs-lookup"><span data-stu-id="8220b-131">Assign Licenses</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8220b-132">Necessitareu accés d'administrador al portal de l'Office 365 de l'organització per completar els passos següents.</span><span class="sxs-lookup"><span data-stu-id="8220b-132">You will need administrative access to your organization's Office 365 Portal to complete the following steps.</span></span>

1. <span data-ttu-id="8220b-133">Aneu al [centre d'administració del Microsoft 365](https://portal.office.com/) per assignar les llicències als usuaris.</span><span class="sxs-lookup"><span data-stu-id="8220b-133">Go to [Microsoft 365 admin center](https://portal.office.com/) to assign licenses to your users.</span></span>

![Portal d'administració de l'Office](./media/5OfficeAdminPortal.png)

2. <span data-ttu-id="8220b-135">A la pàgina **Usuaris actius**, seleccioneu els usuaris als quals voleu assignar una llicència.</span><span class="sxs-lookup"><span data-stu-id="8220b-135">On the **Active users** page, select the users that you want to assign a license to.</span></span>

![Assignar llicències](./media/6AssignLicenses.png)

3. <span data-ttu-id="8220b-137">Verifiqueu que s'hagi seleccionat la llicència del Project Operations i seleccioneu **Desa els canvis**.</span><span class="sxs-lookup"><span data-stu-id="8220b-137">Verify that the Project Operations license has been selected and select **Save changes**.</span></span> 

> [!NOTE]
> <span data-ttu-id="8220b-138">L'oferta de prova del Finance no s'ha d'assignar a un usuari.</span><span class="sxs-lookup"><span data-stu-id="8220b-138">The Finance trial offer does not need to be assigned to a user.</span></span>

## <a name="start-a-new-project-in-lcs"></a><span data-ttu-id="8220b-139">Iniciar un projecte nou al LCS</span><span class="sxs-lookup"><span data-stu-id="8220b-139">Start a new project in LCS</span></span>

<span data-ttu-id="8220b-140">Creeu un projecte nou del LCS tal com es descriu al tema [Iniciar un projecte nou al LCS](create-lcs-project.md)</span><span class="sxs-lookup"><span data-stu-id="8220b-140">Create a new LCS project as described in the topic, [Start a new project in LCS](create-lcs-project.md)</span></span>

## <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="8220b-141">Addició d'una subscripció a l'Azure a un projecte del LCS</span><span class="sxs-lookup"><span data-stu-id="8220b-141">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="8220b-142">Per completar aquesta tasca, seguiu els passos del tema [Afegir una subscripció de l'Azure al projecte del LCS](resource-add-azure-subscription-lcs-project.md).</span><span class="sxs-lookup"><span data-stu-id="8220b-142">To complete this task, follow the steps in the topic, [Add an Azure subscription to LCS project](resource-add-azure-subscription-lcs-project.md).</span></span>

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="8220b-143">Implementar l'entorn de demostració del Finance amb el Project Operations per a escenaris de recursos/sense existències</span><span class="sxs-lookup"><span data-stu-id="8220b-143">Deploy Finance demo environment with Project Operations for resource/non-stocked scenarios</span></span>

<span data-ttu-id="8220b-144">Seguiu les instruccions del tema [Proveir un nou entorn](resource-provision-new-environment.md) per completar la implementació.</span><span class="sxs-lookup"><span data-stu-id="8220b-144">Follow the guidance in the topic, [Provision a new environment](resource-provision-new-environment.md) to complete the deployment.</span></span> <span data-ttu-id="8220b-145">Utilitzeu el tipus d'implementació [entorn de demostració](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) per a la versió preliminar.</span><span class="sxs-lookup"><span data-stu-id="8220b-145">Use the [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) deployment type for preview.</span></span>

## <a name="install-cds-setup-and-configuration-data"></a><span data-ttu-id="8220b-146">Configuració de la instal·lació del CDS i dades de configuració</span><span class="sxs-lookup"><span data-stu-id="8220b-146">Install CDS setup and configuration data</span></span>

<span data-ttu-id="8220b-147">Instal·leu les dades instal·lació i les dades de configuració del CDS com es descriu al tema [Configurar i aplicar les dades de configuració al Common Data Service](resource-apply-pro-setup-config-data.md).</span><span class="sxs-lookup"><span data-stu-id="8220b-147">Install CDS setup and configuration data as described in the topic, [Set up and apply configuration data in the Common Data Service](resource-apply-pro-setup-config-data.md).</span></span>

