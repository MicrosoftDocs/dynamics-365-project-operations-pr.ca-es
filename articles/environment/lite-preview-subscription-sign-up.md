---
title: Registre per obtenir una subscripció de versió preliminar (bàsic)
description: "En aquest tema es proporciona informació sobre com subscriure's i implementar la implementació bàsica del Project Operations: acord a facturació proforma."
author: sigitac
ms.date: 10/07/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4de51277e5a08690cc16497e3916f40498b39fb8
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997409"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a><span data-ttu-id="d1a3d-103">Registre per obtenir una subscripció de versió preliminar (bàsic)</span><span class="sxs-lookup"><span data-stu-id="d1a3d-103">Sign up for a preview subscription - lite</span></span> 

<span data-ttu-id="d1a3d-104">En aquest tema s'explica com subscriure's a l'oferta de socis de visualització prèvia i implementar la implementació bàsica del Dynamics 365 Project Operations: tracte de facturació proforma.</span><span class="sxs-lookup"><span data-stu-id="d1a3d-104">This topic explains how to subscribe to the preview partner offer and deploy Dynamics 365 Project Operations lite deployment - deal to proforma invoicing.</span></span>

> [!NOTE]
> <span data-ttu-id="d1a3d-105">Aquest procés canviarà en pròximes versions del Project Operations.</span><span class="sxs-lookup"><span data-stu-id="d1a3d-105">This process will change in upcoming releases of Project Operations.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="d1a3d-106">Requisits previs</span><span class="sxs-lookup"><span data-stu-id="d1a3d-106">Prerequisites</span></span>

- <span data-ttu-id="d1a3d-107">Rebreu un correu electrònic que us convidarà a participar a la versió preliminar.</span><span class="sxs-lookup"><span data-stu-id="d1a3d-107">You'll receive an email inviting you to participate in the preview.</span></span> <span data-ttu-id="d1a3d-108">Podeu sol·licitar una versió preliminar al [lloc web del Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).</span><span class="sxs-lookup"><span data-stu-id="d1a3d-108">You can request a preview on the [Project Operations website](https://dynamics.microsoft.com/en-us/project-operations/overview/).</span></span>
- <span data-ttu-id="d1a3d-109">L'usuari que implementa la versió preliminar ha de tenir drets d'administrador global a l'inquilí de l'Azure.</span><span class="sxs-lookup"><span data-stu-id="d1a3d-109">The user who deploys the preview must have Azure tenant global administrator rights.</span></span>
- <span data-ttu-id="d1a3d-110">Reviseu tots els termes i condicions.</span><span class="sxs-lookup"><span data-stu-id="d1a3d-110">Review all terms and conditions.</span></span>

## <a name="subscribe"></a><span data-ttu-id="d1a3d-111">Subscripció</span><span class="sxs-lookup"><span data-stu-id="d1a3d-111">Subscribe</span></span>

<span data-ttu-id="d1a3d-112">Quan rebeu una aprovació de [sol·licitud de versió preliminar](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u), rebreu dues ofertes de Microsoft per correu electrònic.</span><span class="sxs-lookup"><span data-stu-id="d1a3d-112">When you receive a [preview request](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) approval, you'll receive two offers from Microsoft by email.</span></span> <span data-ttu-id="d1a3d-113">Aquestes ofertes us permeten implementar la versió preliminar del Project Operations:</span><span class="sxs-lookup"><span data-stu-id="d1a3d-113">These offers allow you to deploy the Project Operations Preview:</span></span>

- <span data-ttu-id="d1a3d-114">Prova de versió preliminar del Dynamics 365 Project Operations (CRM)</span><span class="sxs-lookup"><span data-stu-id="d1a3d-114">Dynamics 365 Project Operations (CRM) - Preview Trial</span></span>
- <span data-ttu-id="d1a3d-115">Office 365 Project Operations: prova de versió preliminar</span><span class="sxs-lookup"><span data-stu-id="d1a3d-115">Office 365 Project Operations - Preview Trial</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d1a3d-116">Només cal que una persona de l'organització, l'administrador d'inquilins, realitzi aquesta tasca.</span><span class="sxs-lookup"><span data-stu-id="d1a3d-116">Only one person, the tenant administrator, in an organization needs to perform this task.</span></span> <span data-ttu-id="d1a3d-117">Si no sou el subscriptor en aquesta versió, espereu fins que l'organització s'hagi registrat i hàgiu rebut les vostres credencials d'usuari.</span><span class="sxs-lookup"><span data-stu-id="d1a3d-117">If you aren't the subscriber to this release, wait until your organization has been signed up and you've received your user credentials.</span></span>

### <a name="dynamics-365-project-operations-crm---preview-trial"></a><span data-ttu-id="d1a3d-118">Prova de versió preliminar del Dynamics 365 Project Operations (CRM)</span><span class="sxs-lookup"><span data-stu-id="d1a3d-118">Dynamics 365 Project Operations (CRM) - Preview Trial</span></span> 

<span data-ttu-id="d1a3d-119">Abans de començar, assegureu-vos que hàgiu iniciat la sessió en un navegador amb el compte laboral de l'usuari a l'inquilí on voleu la versió preliminar del Project Operations.</span><span class="sxs-lookup"><span data-stu-id="d1a3d-119">Before you begin, make sure you are logged in to a browser with the user work account in the tenant where you want the Project Operations preview.</span></span>

1. <span data-ttu-id="d1a3d-120">Redimiu el primer codi d'oferta, prova de versió preliminar del **Dynamics 365 Project Operations (CRM)** enganxant-lo a l'URL del navegador.</span><span class="sxs-lookup"><span data-stu-id="d1a3d-120">Redeem the first offer code, **Dynamics 365 Project Operations (CRM) - Preview Trial** by pasting it into the browser URL.</span></span>

![Bescanviar l'oferta](./media/16RedeemFirstOfferNew.png)

2. <span data-ttu-id="d1a3d-122">Confirmeu la comanda.</span><span class="sxs-lookup"><span data-stu-id="d1a3d-122">Confirm your order.</span></span>
<span data-ttu-id="d1a3d-123">![Confirmeu la comanda](./media/17ConfirmOrderNew.png)</span><span class="sxs-lookup"><span data-stu-id="d1a3d-123">![Confirm the order](./media/17ConfirmOrderNew.png)</span></span>

<span data-ttu-id="d1a3d-124">Veureu que l'oferta de confirmació s'ha bescanviat correctament.</span><span class="sxs-lookup"><span data-stu-id="d1a3d-124">You'll see confirmation offer was successfully redeemed.</span></span>

![Confirmació](./media/18OrderConfirmationNew.png)

### <a name="office-365-project-operations---preview-trial"></a><span data-ttu-id="d1a3d-126">Office 365 Project Operations: prova de versió preliminar</span><span class="sxs-lookup"><span data-stu-id="d1a3d-126">Office 365 Project Operations - Preview Trial</span></span>

<span data-ttu-id="d1a3d-127">Repetiu els mateixos passos que amb el primer codi d'oferta.</span><span class="sxs-lookup"><span data-stu-id="d1a3d-127">Repeat the same steps as with the first offer code.</span></span> <span data-ttu-id="d1a3d-128">Assegureu-vos d'afegir el segon codi d'oferta amb el mateix compte d'usuari utilitzat amb el primer codi d'oferta.</span><span class="sxs-lookup"><span data-stu-id="d1a3d-128">Make sure to add the second offer code using the same user account that was used with the first offer code.</span></span>

## <a name="assign-licenses"></a><span data-ttu-id="d1a3d-129">Assignar llicències</span><span class="sxs-lookup"><span data-stu-id="d1a3d-129">Assign licenses</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d1a3d-130">Necessitareu accés d'administrador al portal del Microsoft 365 de l'organització per completar els passos següents.</span><span class="sxs-lookup"><span data-stu-id="d1a3d-130">You will need administrative access to your organization's Microsoft 365 Portal to complete the following steps.</span></span>


1. <span data-ttu-id="d1a3d-131">Aneu al [centre d'administració del Microsoft 365](https://portal.office.com/) per assignar les llicències als usuaris.</span><span class="sxs-lookup"><span data-stu-id="d1a3d-131">Go to [Microsoft 365 admin center](https://portal.office.com/) to assign the licenses to your users.</span></span>

![Pàgina principal del centre d'administració](./media/14AdminPortal.png)

2. <span data-ttu-id="d1a3d-133">A la pàgina **Usuaris actius**, seleccioneu els usuaris als quals voleu assignar una llicència.</span><span class="sxs-lookup"><span data-stu-id="d1a3d-133">On the **Active users** page, select the users that you want to assign a license to.</span></span>

![Assignar llicències](./media/15AssignLicenses.png)

3. <span data-ttu-id="d1a3d-135">Verifiqueu que les llicències de **Versió preliminar del Dynamics 365 Project Operations (CRM)** i la **Versió preliminar de l'Office 365** estiguin seleccionades.</span><span class="sxs-lookup"><span data-stu-id="d1a3d-135">Verify that the **Dynamics 365 Project Operations (CRM) Preview** and **Office 365 Project Operations - Preview** licenses are selected.</span></span> 
4. <span data-ttu-id="d1a3d-136">Seleccioneu **Desa els canvis**.</span><span class="sxs-lookup"><span data-stu-id="d1a3d-136">Select **Save changes**.</span></span>

## <a name="create-a-new-cds-environment"></a><span data-ttu-id="d1a3d-137">Crear un entorn nou del CDS</span><span class="sxs-lookup"><span data-stu-id="d1a3d-137">Create a new CDS environment</span></span>

1. <span data-ttu-id="d1a3d-138">Proveïu d'un nou entorn d'implementació del CDS del Project Operations seguint les instruccions del tema [Model d'implementació del CDS](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="d1a3d-138">Provision a new Project Operations CDS deployment environment by following instructions in the topic, [CDS deployment model](lite-deployment.md).</span></span> <span data-ttu-id="d1a3d-139">Quan seleccioneu el tipus d'entorn, assegureu-vos d'utilitzar **Prova (basada en subscripció)**.</span><span class="sxs-lookup"><span data-stu-id="d1a3d-139">When you select the environment type, make sure to use **Trial (Subscription based)**.</span></span>
<span data-ttu-id="d1a3d-140">![Entorn nou](./media/19CreateEnvironment.png)</span><span class="sxs-lookup"><span data-stu-id="d1a3d-140">![New environment](./media/19CreateEnvironment.png)</span></span>

2. <span data-ttu-id="d1a3d-141">Seleccioneu l'opció **Habilita les aplicacions del Dynamics 365** i deixeu **Implementa aquestes aplicacions automàticament** en blanc.</span><span class="sxs-lookup"><span data-stu-id="d1a3d-141">Select the **Enable Dynamics 365 apps** setting, and leave **Automatically deploy these apps** blank.</span></span>  
3. <span data-ttu-id="d1a3d-142">Seleccioneu **Desa** per crear l'entorn.</span><span class="sxs-lookup"><span data-stu-id="d1a3d-142">Select **Save** to create the environment.</span></span>

![Afegeix base de dades](./media/20CreateEnvironment1.png)

4. <span data-ttu-id="d1a3d-144">Un cop creat l'entorn, instal·leu la solució **Microsoft Dynamics 365 Project Operations**.</span><span class="sxs-lookup"><span data-stu-id="d1a3d-144">After the environment is created, install **Microsoft Dynamics 365 Project Operations** solution.</span></span> 

![Instal·lar la solució](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a><span data-ttu-id="d1a3d-146">Instal·lar una configuració del CDS i configurar les dades de demostració</span><span class="sxs-lookup"><span data-stu-id="d1a3d-146">Install a CDS configuration and setup demo data</span></span>

<span data-ttu-id="d1a3d-147">Instal·leu la configuració del CDS i configureu les dades de demostració seguint les instruccions del tema [Aplicar la configuració de la demostració i les dades de configuració](lite-apply-demo-setup-config-data.md).</span><span class="sxs-lookup"><span data-stu-id="d1a3d-147">Install the CDS configuration and set up demo data by following instructions in the topic, [Apply demo setup and configuration data](lite-apply-demo-setup-config-data.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]