---
title: Registrar-se a les subscripcions de versió preliminar del Project Operations per a escenaris de recursos/sense existències
description: En aquest tema es proporciona informació sobre com registrar-se i implementar el Project Operations per a escenaris de recursos/sense existències.
author: sigitac
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7a03f021b1ae0a87dfc947976b8a16c8246e1684
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072098"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a><span data-ttu-id="7e849-103">Registrar-se a les subscripcions de versió preliminar del Project Operations per a escenaris de recursos/sense existències</span><span class="sxs-lookup"><span data-stu-id="7e849-103">Sign up for Project Operations preview subscriptions for resource/ non-stocked scenarios</span></span>

<span data-ttu-id="7e849-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_</span><span class="sxs-lookup"><span data-stu-id="7e849-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="7e849-105">En aquest tema s'explica com subscriure's a l'oferta de versió preliminar/associats i implementar l'entorn del Project Operations per a escenaris de recursos/sense existències.</span><span class="sxs-lookup"><span data-stu-id="7e849-105">This topic explains how to subscribe to the preview/partner offer and deploy Project Operations environment for resource/ non-stocked based scenarios.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="7e849-106">Requisits previs</span><span class="sxs-lookup"><span data-stu-id="7e849-106">Prerequisites</span></span>

- <span data-ttu-id="7e849-107">Rebreu un correu electrònic que us convidarà a participar a la versió preliminar.</span><span class="sxs-lookup"><span data-stu-id="7e849-107">You will receive an email inviting you to participate in the preview.</span></span> <span data-ttu-id="7e849-108">Podeu sol·licitar una versió preliminar al [lloc web del Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).</span><span class="sxs-lookup"><span data-stu-id="7e849-108">You can request a preview on the [Project Operations website](https://dynamics.microsoft.com/en-us/project-operations/overview/).</span></span>
- <span data-ttu-id="7e849-109">L'usuari que implementa la versió preliminar ha de tenir drets d'administrador global a l'inquilí de l'Azure.</span><span class="sxs-lookup"><span data-stu-id="7e849-109">The user who deploys the preview must have Azure tenant global administrator rights.</span></span>
- <span data-ttu-id="7e849-110">La implementació d'un entorn del Finance requereix una subscripció vàlida de l'Azure que es facturarà per entorn.</span><span class="sxs-lookup"><span data-stu-id="7e849-110">Deploying a Finance environment requires a valid Azure subscription that will be billed per environment.</span></span> <span data-ttu-id="7e849-111">Podeu utilitzar la subscripció existent de l'organització o utilitzar una [versió de prova de l'Azure](https://azure.microsoft.com/en-us/free/) per començar.</span><span class="sxs-lookup"><span data-stu-id="7e849-111">You can use your organizations existing subscription or use an [Azure trial](https://azure.microsoft.com/en-us/free/) to get started.</span></span> <span data-ttu-id="7e849-112">L'entorn del CDS es proporcionarà gratuïtament durant un període de 30 dies limitat.</span><span class="sxs-lookup"><span data-stu-id="7e849-112">The CDS environment will be provided free for a limited 30 day period.</span></span>

## <a name="subscribe"></a><span data-ttu-id="7e849-113">Subscripció</span><span class="sxs-lookup"><span data-stu-id="7e849-113">Subscribe</span></span>

<span data-ttu-id="7e849-114">Quan s'aprovi la [sol·licitud de versió preliminar](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u), rebreu tres ofertes de Microsoft per correu electrònic.</span><span class="sxs-lookup"><span data-stu-id="7e849-114">When your [preview request](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) is approved, you will receive three offers from Microsoft by email.</span></span> <span data-ttu-id="7e849-115">Aquestes ofertes us permeten implementar la versió preliminar del Project Operations:</span><span class="sxs-lookup"><span data-stu-id="7e849-115">These offers allow you to deploy the Project Operations Preview:</span></span>

- <span data-ttu-id="7e849-116">Dynamics 365 Project Operations (CRM): prova de versió preliminar</span><span class="sxs-lookup"><span data-stu-id="7e849-116">Dynamics 365 Project Operations (CRM) - Preview Trial</span></span>
- <span data-ttu-id="7e849-117">Office 365 Project Operations: prova de versió preliminar</span><span class="sxs-lookup"><span data-stu-id="7e849-117">Office 365 Project Operations - Preview Trial</span></span>
- <span data-ttu-id="7e849-118">Dynamics 365 Finance: prova de versió preliminar</span><span class="sxs-lookup"><span data-stu-id="7e849-118">Dynamics 365 Finance - Preview Trial</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7e849-119">Només cal que una persona de l'organització, l'administrador d'inquilins, realitzi aquesta tasca.</span><span class="sxs-lookup"><span data-stu-id="7e849-119">Only one person, the tenant administrator, in an organization needs to perform this task.</span></span> <span data-ttu-id="7e849-120">Si no sou el subscriptor en aquesta versió, espereu fins que l'organització s'hagi registrat i hàgiu rebut les vostres credencials d'usuari.</span><span class="sxs-lookup"><span data-stu-id="7e849-120">If you aren't the subscriber to this release, wait until your organization has been signed up and you've received your user credentials.</span></span>

### <a name="dynamics-365-project-operations-crm---preview-trial"></a><span data-ttu-id="7e849-121">Dynamics 365 Project Operations (CRM): prova de versió preliminar</span><span class="sxs-lookup"><span data-stu-id="7e849-121">Dynamics 365 Project Operations (CRM) - Preview Trial</span></span> 

<span data-ttu-id="7e849-122">Abans de començar, assegureu-vos que hàgiu iniciat la sessió en un navegador amb el compte laboral de l'usuari a l'inquilí on voleu la versió preliminar del Project Operations.</span><span class="sxs-lookup"><span data-stu-id="7e849-122">Before you begin, make sure you are logged in to a browser with the user work account in the tenant where you want the Project Operations preview.</span></span>

1. <span data-ttu-id="7e849-123">Bescanvieu el primer codi d'oferta, **Dynamics 365 Project Operations (CRM): prova de versió preliminar** enganxant-lo a l'URL del navegador.</span><span class="sxs-lookup"><span data-stu-id="7e849-123">Redeem the first offer code, **Dynamics 365 Project Operations (CRM) - Preview Trial** by pasting it into the browser URL.</span></span>

![Bescanviar l'oferta](./media/16RedeemFirstOfferNew.png)

2. <span data-ttu-id="7e849-125">Confirmeu la comanda.</span><span class="sxs-lookup"><span data-stu-id="7e849-125">Confirm your order.</span></span>

![Confirmeu la comanda](./media/17ConfirmOrderNew.png)

<span data-ttu-id="7e849-127">Veureu que l'oferta de confirmació s'ha bescanviat correctament.</span><span class="sxs-lookup"><span data-stu-id="7e849-127">You will see confirmation offer was successfully redeemed.</span></span>

![Confirmació](./media/18OrderConfirmationNew.png)

### <a name="office-365-project-operations---preview-trial"></a><span data-ttu-id="7e849-129">Office 365 Project Operations: prova de versió preliminar</span><span class="sxs-lookup"><span data-stu-id="7e849-129">Office 365 Project Operations - Preview Trial</span></span>

<span data-ttu-id="7e849-130">Repetiu els mateixos passos que amb el primer codi d'oferta.</span><span class="sxs-lookup"><span data-stu-id="7e849-130">Repeat the same steps as with the first offer code.</span></span> <span data-ttu-id="7e849-131">Assegureu-vos d'afegir el segon codi d'oferta amb el mateix compte d'usuari utilitzat amb el primer codi d'oferta.</span><span class="sxs-lookup"><span data-stu-id="7e849-131">Make sure to add the second offer code using the same user account that was used with the first offer code.</span></span>

### <a name="dynamics-365-finance-preview-trial"></a><span data-ttu-id="7e849-132">Prova de versió preliminar del Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="7e849-132">Dynamics 365 Finance preview trial</span></span>

<span data-ttu-id="7e849-133">Repetiu els mateixos passos amb l'última oferta del correu electrònic de benvinguda.</span><span class="sxs-lookup"><span data-stu-id="7e849-133">Repeat the same steps with the last offer from the Welcome email.</span></span>

## <a name="assign-licenses"></a><span data-ttu-id="7e849-134">Assignar llicències</span><span class="sxs-lookup"><span data-stu-id="7e849-134">Assign licenses</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7e849-135">Necessitareu accés d'administrador al portal del Microsoft 365 de l'organització per completar els passos següents.</span><span class="sxs-lookup"><span data-stu-id="7e849-135">You will need administrative access to your organization's Microsoft 365 Portal to complete the following steps.</span></span>

1. <span data-ttu-id="7e849-136">Aneu al [centre d'administració del Microsoft 365](https://portal.office.com/) per assignar les llicències als usuaris.</span><span class="sxs-lookup"><span data-stu-id="7e849-136">Go to [Microsoft 365 admin center](https://portal.office.com/) to assign the licenses to your users.</span></span>

![Pàgina principal del centre d'administració](./media/14AdminPortal.png)

2. <span data-ttu-id="7e849-138">A la pàgina **Usuaris actius** , seleccioneu els usuaris als quals voleu assignar una llicència.</span><span class="sxs-lookup"><span data-stu-id="7e849-138">On the **Active users** page, select the users that you want to assign a license to.</span></span>

![Assignar llicències](./media/15AssignLicenses.png)

3. <span data-ttu-id="7e849-140">Verifiqueu que s'hagi seleccionat la llicència **Versió preliminar del Dynamics 365 Project Operations (CRM)** i **Office 365 Project Operations: versió preliminar** i trieu **Desa els canvis**.</span><span class="sxs-lookup"><span data-stu-id="7e849-140">Verify that the **Dynamics 365 Project Operations (CRM) Preview** and **Office 365 Project Operations - Preview** license have been selected and select **Save changes**.</span></span>

> [!NOTE]
> <span data-ttu-id="7e849-141">L'oferta de prova del Finance no s'ha d'assignar a un usuari.</span><span class="sxs-lookup"><span data-stu-id="7e849-141">The Finance trial offer does not need to be assigned to a user.</span></span>

## <a name="start-a-new-project-in-lcs"></a><span data-ttu-id="7e849-142">Iniciar un projecte nou al LCS</span><span class="sxs-lookup"><span data-stu-id="7e849-142">Start a new project in LCS</span></span>

<span data-ttu-id="7e849-143">Creeu un projecte nou del LCS tal com es descriu al tema [Iniciar un projecte nou al LCS](create-lcs-project.md)</span><span class="sxs-lookup"><span data-stu-id="7e849-143">Create a new LCS project as described in the topic, [Start a new project in LCS](create-lcs-project.md)</span></span>

## <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="7e849-144">Addició d'una subscripció a l'Azure a un projecte del LCS</span><span class="sxs-lookup"><span data-stu-id="7e849-144">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="7e849-145">Per completar aquesta tasca, seguiu els passos del tema [Afegir una subscripció de l'Azure al projecte del LCS](resource-add-azure-subscription-lcs-project.md).</span><span class="sxs-lookup"><span data-stu-id="7e849-145">To complete this task, follow the steps in the topic, [Add an Azure subscription to LCS project](resource-add-azure-subscription-lcs-project.md).</span></span>

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="7e849-146">Implementar l'entorn de demostració del Finance amb el Project Operations per a escenaris de recursos/sense existències</span><span class="sxs-lookup"><span data-stu-id="7e849-146">Deploy Finance demo environment with Project Operations for resource/non-stocked scenarios</span></span>

<span data-ttu-id="7e849-147">Seguiu les instruccions del tema [Proveir un nou entorn](resource-provision-new-environment.md) per completar la implementació.</span><span class="sxs-lookup"><span data-stu-id="7e849-147">Follow the guidance in the topic, [Provision a new environment](resource-provision-new-environment.md) to complete the deployment.</span></span> <span data-ttu-id="7e849-148">Utilitzeu el tipus d'implementació [entorn de demostració](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) per a la versió preliminar.</span><span class="sxs-lookup"><span data-stu-id="7e849-148">Use the [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) deployment type for preview.</span></span> 

## <a name="install-cds-setup-and-configuration-data"></a><span data-ttu-id="7e849-149">Configuració de la instal·lació del CDS i dades de configuració</span><span class="sxs-lookup"><span data-stu-id="7e849-149">Install CDS setup and configuration data</span></span>

<span data-ttu-id="7e849-150">Instal·leu les dades instal·lació i les dades de configuració del CDS com es descriu al tema [Configurar i aplicar les dades de configuració al Common Data Service](resource-apply-pro-setup-config-data.md).</span><span class="sxs-lookup"><span data-stu-id="7e849-150">Install CDS setup and configuration data as described in the topic, [Set up and apply configuration data in the Common Data Service](resource-apply-pro-setup-config-data.md).</span></span>
<span data-ttu-id="7e849-151">Completeu aquest pas només després que s'hagi implementat l'entorn de demostració del Finance i que les dades de demostració del FO estiguin a punt.</span><span class="sxs-lookup"><span data-stu-id="7e849-151">Complete this step only after Finance demo environment is deployed and demo data in FO is ready.</span></span>
