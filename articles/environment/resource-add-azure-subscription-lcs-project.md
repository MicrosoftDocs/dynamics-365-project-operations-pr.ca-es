---
title: Addició d'una subscripció a l'Azure a un projecte del LCS
description: En aquest tema es proporciona informació sobre com connectar la subscripció de l'Azure a un projecte del LCS.
author: sigitac
manager: Annbe
ms.date: 04/12/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a80c926ba67a1620e39d8c7677a05678454e6340
ms.sourcegitcommit: 7468d668c48c1d87934aab9a034decd51e56dec6
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/13/2021
ms.locfileid: "5880526"
---
# <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="bcf43-103">Addició d'una subscripció a l'Azure a un projecte del LCS</span><span class="sxs-lookup"><span data-stu-id="bcf43-103">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="bcf43-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_</span><span class="sxs-lookup"><span data-stu-id="bcf43-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="bcf43-105">Els entorns allotjats al núvol s'han de implementar mitjançant una subscripció existent de l'Azure.</span><span class="sxs-lookup"><span data-stu-id="bcf43-105">Cloud-hosted environments must be deployed using an existing Azure subscription.</span></span> <span data-ttu-id="bcf43-106">En aquest tema s'indica com connectar la subscripció de l'Azure existent a un projecte del LCS.</span><span class="sxs-lookup"><span data-stu-id="bcf43-106">This topic explains how to connect your existing Azure subscription to an LCS project.</span></span> 

## <a name="grant-admin-consent"></a><span data-ttu-id="bcf43-107">Concedir el consentiment de l'administrador</span><span class="sxs-lookup"><span data-stu-id="bcf43-107">Grant admin consent</span></span>

1. <span data-ttu-id="bcf43-108">Al projecte del LCS, a la secció **Entorns**, seleccioneu **Configuració del Microsoft Azure**.</span><span class="sxs-lookup"><span data-stu-id="bcf43-108">In your LCS project, in the **Environments** section, select **Microsoft Azure settings**.</span></span>

![Configuració del Microsoft Azure](./media/1MicrosoftAzureSettings.png)

2. <span data-ttu-id="bcf43-110">A la pàgina **Configuració del projecte**, a la pestanya **Connectors de l'Azure**, seleccioneu **Autoritza**.</span><span class="sxs-lookup"><span data-stu-id="bcf43-110">On the **Project settings** page, on the **Azure connectors** tab, select **Authorize**.</span></span> <span data-ttu-id="bcf43-111">Això permet que els entorns s'implementin en aquest projecte.</span><span class="sxs-lookup"><span data-stu-id="bcf43-111">This allows environments to be deployed to this project.</span></span>

![Connectors de l'Azure](./media/2AzureConnectors.png)

3. <span data-ttu-id="bcf43-113">Torneu a seleccionar **Autoritza** per proporcionar el consentiment de l'administrador.</span><span class="sxs-lookup"><span data-stu-id="bcf43-113">Select **Authorize** again to provide admin consent.</span></span>

![Concedir el consentiment de l'administrador](./media/3GrantAdminConsent.png)

4. <span data-ttu-id="bcf43-115">Accepteu la sol·licitud de permisos.</span><span class="sxs-lookup"><span data-stu-id="bcf43-115">Accept the permissions request.</span></span>

![Acceptar la sol·licitud de permisos](./media/4AcceptPermissionRequest.png)

<span data-ttu-id="bcf43-117">L'autorització ja s'ha completat.</span><span class="sxs-lookup"><span data-stu-id="bcf43-117">The authorization is now complete.</span></span> 

![Autorització correcta](./media/5AuthorizationComplete.png)

## <a name="provide-dynamics-deployment-services-access-to-your-azure-subscription"></a><a name="provide"></a><span data-ttu-id="bcf43-119">Proporcionar l'accés dels serveis d'implementació del Dynamics a la subscripció de l'Azure</span><span class="sxs-lookup"><span data-stu-id="bcf43-119">Provide Dynamics Deployment Services access to your Azure subscription</span></span>

1. <span data-ttu-id="bcf43-120">Aneu a [Facturació del Microsoft Azure](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) i seleccioneu la vostra subscripció.</span><span class="sxs-lookup"><span data-stu-id="bcf43-120">Go to [Microsoft Azure billing](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) and select your subscription.</span></span> <span data-ttu-id="bcf43-121">Els serveis d'implementació del Dynamics necessiten accedir a aquesta subscripció per poder implementar entorns.</span><span class="sxs-lookup"><span data-stu-id="bcf43-121">Dynamics Deployment Services needs to access this subscription to be able to deploy environments.</span></span>

![Detalls de la subscripció de l'Azure](./media/6AzureSubscription.png)

2. <span data-ttu-id="bcf43-123">Seleccioneu **Control d'accés (IAM)** a la subfinestra de navegació i, a continuació, seleccioneu **Afegeix una assignació de funcions**.</span><span class="sxs-lookup"><span data-stu-id="bcf43-123">Select **Access control (IAM)** in the navigation pane, and then select **Add role assignment**.</span></span>
3. <span data-ttu-id="bcf43-124">Al control lliscant del costat dret, seleccioneu **Funció de col·laborador** i, a la llista proporcionada, cerqueu i seleccioneu **Serveis d'implementació del Dynamics**.</span><span class="sxs-lookup"><span data-stu-id="bcf43-124">In the slider on the right side, select **Contributor role**, and in the list provided, find and select **Dynamics Deployment Services**.</span></span> 
4. <span data-ttu-id="bcf43-125">Seleccioneu **Desa**.</span><span class="sxs-lookup"><span data-stu-id="bcf43-125">Select **Save**.</span></span>

![Accés de la subscripció](./media/7SubscriptionAccess.png)

### <a name="add-a-subscription-connector-to-an-lcs-project"></a><span data-ttu-id="bcf43-127">Afegir un connector de subscripció a un projecte del LCS</span><span class="sxs-lookup"><span data-stu-id="bcf43-127">Add a subscription connector to an LCS project</span></span>

1. <span data-ttu-id="bcf43-128">Al projecte del LCS, a la pàgina **Configuració del Microsoft Azure**, seleccioneu **Afegeix** per afegir un connector nou.</span><span class="sxs-lookup"><span data-stu-id="bcf43-128">In your LCS project, on the **Microsoft Azure settings** page, select **Add** to add a new connector.</span></span>
2. <span data-ttu-id="bcf43-129">Introduïu l'identificador de subscripció de l'Azure.</span><span class="sxs-lookup"><span data-stu-id="bcf43-129">Enter your Azure subscription ID.</span></span> <span data-ttu-id="bcf43-130">Podeu trobar l'identificador de subscripció de l'Azure al [portal de l'Azure](https://ms.portal.azure.com/), a **Configuració** a la part inferior esquerra de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="bcf43-130">You can find your Azure subscription ID in the [Azure portal](https://ms.portal.azure.com/), under  **Settings**  in the lower left of the screen.</span></span>
3. <span data-ttu-id="bcf43-131">Al camp **Configura per utilitzar l'Azure Resource Manager**, seleccioneu **Sí**.</span><span class="sxs-lookup"><span data-stu-id="bcf43-131">In the **Configure to use Azure Resource Manager** field, select **Yes**.</span></span>
4. <span data-ttu-id="bcf43-132">Assegureu-vos que el domini de l'inquilí de l'AAD de subscripció de l'Azure coincideixi amb la subscripció de l'Azure propietària del domini que esteu utilitzant i seleccioneu **Següent**.</span><span class="sxs-lookup"><span data-stu-id="bcf43-132">Make sure Azure's Subscription AAD Tenant Domain matches the domain-owning Azure subscription that you are using, and select **Next**.</span></span>
5. <span data-ttu-id="bcf43-133">A la pantalla **Configuració del Microsoft Azure**, seleccioneu **Següent** per confirmar.</span><span class="sxs-lookup"><span data-stu-id="bcf43-133">On the **Microsoft Azure Setup** screen, select **Next** to confirm.</span></span> <span data-ttu-id="bcf43-134">Si rebeu un error en aquesta pantalla, torneu a la secció [Proporcionar accés dels serveis d'implementació del Dynamics a la subscripció de l'Azure](#provide) en aquest tema i assegureu-vos que heu completat tots els passos.</span><span class="sxs-lookup"><span data-stu-id="bcf43-134">If you receive an error on this screen, return to the section [Provide Dynamics Deployment Services access to Azure subscription](#provide) in this topic and make sure you have completed all of the steps.</span></span>
6. <span data-ttu-id="bcf43-135">Baixeu el certificat d'administració de l'Azure a una carpeta local de l'ordinador.</span><span class="sxs-lookup"><span data-stu-id="bcf43-135">Download the Azure Management Certificate to a local folder on your computer.</span></span> <span data-ttu-id="bcf43-136">Demaneu a l'administrador de subscripció de l'Azure que carregui el certificat a l'Azure Management Portal seleccionant la subscripció i anant a **Configuració** > **Certificats d'administració**.</span><span class="sxs-lookup"><span data-stu-id="bcf43-136">Ask your Azure subscription administrator to upload the certificate to Azure Management Portal by selecting the subscription and going to **Settings** > **Management Certificates**.</span></span> <span data-ttu-id="bcf43-137">Aquest certificat permet que el LCS es comuniqui amb l'Azure en nom vostre.</span><span class="sxs-lookup"><span data-stu-id="bcf43-137">This certificate enables LCS to communicate with Azure on your behalf.</span></span> <span data-ttu-id="bcf43-138">Podeu ometre aquest pas si l'usuari té accés a la subscripció.</span><span class="sxs-lookup"><span data-stu-id="bcf43-138">You can skip this step if your user has access to the subscription.</span></span>
7. <span data-ttu-id="bcf43-139">Seleccioneu **Següent**.</span><span class="sxs-lookup"><span data-stu-id="bcf43-139">Select  **Next**.</span></span>
8. <span data-ttu-id="bcf43-140">Seleccioneu la regió de l'Azure per implementar i seleccioneu un centre de dades a prop del lloc on teniu pensat utilitzar aquest sistema.</span><span class="sxs-lookup"><span data-stu-id="bcf43-140">Select the Azure region to deploy in and select a data center that is close to where you plan to use this system.</span></span>
9.  <span data-ttu-id="bcf43-141">Seleccioneu **Connecta**.</span><span class="sxs-lookup"><span data-stu-id="bcf43-141">Select  **Connect**.</span></span>

<span data-ttu-id="bcf43-142">Heu connectat correctament la subscripció de l'Azure.</span><span class="sxs-lookup"><span data-stu-id="bcf43-142">You have successfully connected your Azure subscription.</span></span> <span data-ttu-id="bcf43-143">Ara podeu implementar els entorns allotjats al núvol del Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="bcf43-143">You can now deploy Dynamics 365 Finance cloud-hosted environments.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]
