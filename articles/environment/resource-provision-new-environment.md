---
title: Proveïment d'un entorn nou
description: En aquest tema s'ofereix informació sobre com proveir un entorn nou del Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 45700371c50e3b5a840df45fc24fa8a5b4584b61
ms.sourcegitcommit: 87b7a8d793c19c50f3765b8d788cde24a6a0ca24
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949350"
---
# <a name="provision-a-new-environment"></a><span data-ttu-id="167a0-103">Proveïment d'un entorn nou</span><span class="sxs-lookup"><span data-stu-id="167a0-103">Provision a new environment</span></span>

<span data-ttu-id="167a0-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_</span><span class="sxs-lookup"><span data-stu-id="167a0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="167a0-105">En aquest tema es proporciona informació sobre com es proveeix un nou entorn del Dynamics 365 Project Operations per a escenaris basats en recursos/sense existències.</span><span class="sxs-lookup"><span data-stu-id="167a0-105">This topic provides information about how to provision a new Dynamics 365 Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a><span data-ttu-id="167a0-106">Habilitar el proveïment automatitzat del Project Operations en un projecte del LCS</span><span class="sxs-lookup"><span data-stu-id="167a0-106">Enable Project Operations automated provisioning in an LCS project</span></span>

<span data-ttu-id="167a0-107">Seguiu aquests passos per habilitar el flux de proveïment automatitzat del Project Operations per al projecte del LCS.</span><span class="sxs-lookup"><span data-stu-id="167a0-107">Use following steps to enable the Project Operations automated provisioning flow for your LCS project.</span></span>

1. <span data-ttu-id="167a0-108">Aneu a [LCS](https://lcs.dynamics.com/v2) i seleccioneu la peça **Administració de característiques de versió preliminar**.</span><span class="sxs-lookup"><span data-stu-id="167a0-108">Go to [LCS](https://lcs.dynamics.com/v2) and select the **Preview Feature management** tile.</span></span>
2. <span data-ttu-id="167a0-109">A la llista **Característiques de versió preliminar**, seleccioneu **Project Operations** i **Característica de versió preliminar habilitada** per habilitar el Project Operations.</span><span class="sxs-lookup"><span data-stu-id="167a0-109">In the **Preview feature** list, select **Project Operations** and the select **Preview feature enabled** to enable Project Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="167a0-110">Aquest pas només es fa una vegada per projecte del LCS.</span><span class="sxs-lookup"><span data-stu-id="167a0-110">This step is performed only one time per LCS project.</span></span>

## <a name="provision-a-project-operations-environment"></a><span data-ttu-id="167a0-111">Proveïment d'un entorn del Project Operations</span><span class="sxs-lookup"><span data-stu-id="167a0-111">Provision a Project Operations environment</span></span>

1. <span data-ttu-id="167a0-112">Obriu una nova implementació d'un [entorn de demostració](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) o [entorn de producció](https://docs.microsoft.com/edynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) del Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="167a0-112">Open a new Dynamics 365 Finance [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) or [sandbox/ production environment](https://docs.microsoft.com/edynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) deployment.</span></span> 
2. <span data-ttu-id="167a0-113">Seguiu els passos de l'auxiliar **Proveïment de l'entorn**.</span><span class="sxs-lookup"><span data-stu-id="167a0-113">Walk through the **Environment provisioning** wizard.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="167a0-114">Assegureu-vos que la versió de l'aplicació seleccionada sigui 10.0.13 o superior.</span><span class="sxs-lookup"><span data-stu-id="167a0-114">Make sure selected application version is 10.0.13 or higher.</span></span>

3. <span data-ttu-id="167a0-115">Per proveir el Project Operations, a **Configuració avançada**, seleccioneu **Common Data Service**.</span><span class="sxs-lookup"><span data-stu-id="167a0-115">To provision Project Operations, under **Advance settings**, select **Common Data Service**.</span></span> 
4. <span data-ttu-id="167a0-116">Habiliteu la **Configuració del Common Data Service** seleccionant **Sí** i, a continuació, introduïu informació als camps obligatoris:</span><span class="sxs-lookup"><span data-stu-id="167a0-116">Enable the **Common Data Service Setting** by selecting **Yes** and then enter information in the required fields:</span></span>

  - <span data-ttu-id="167a0-117">Nom</span><span class="sxs-lookup"><span data-stu-id="167a0-117">Name</span></span>
  - <span data-ttu-id="167a0-118">Regió</span><span class="sxs-lookup"><span data-stu-id="167a0-118">Region</span></span>
  - <span data-ttu-id="167a0-119">Language</span><span class="sxs-lookup"><span data-stu-id="167a0-119">Language</span></span>
  - <span data-ttu-id="167a0-120">Moneda</span><span class="sxs-lookup"><span data-stu-id="167a0-120">Currency</span></span>
 
5. <span data-ttu-id="167a0-121">Al camp **Plantilla del Common Data Service**, seleccioneu **Project Operations**</span><span class="sxs-lookup"><span data-stu-id="167a0-121">In the **Common Data Service Template** field, select **Project Operations**</span></span> 

6. <span data-ttu-id="167a0-122">Seleccioneu el tipus d'entorn per a la implementació.</span><span class="sxs-lookup"><span data-stu-id="167a0-122">Select the environment type for your deployment.</span></span> <span data-ttu-id="167a0-123">Una prova basada en subscripció us permetrà implementar un entorn del CDS durant 30 dies.</span><span class="sxs-lookup"><span data-stu-id="167a0-123">A subscription-based trial will let you deploy a CDS environment for 30 days.</span></span> 

![Configuració de la implementació](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> <span data-ttu-id="167a0-125">Seleccioneu **Accepto** per reconèixer les condicions del servei i, a continuació, seleccioneu **Fet** per tornar a la configuració de la implementació.</span><span class="sxs-lookup"><span data-stu-id="167a0-125">Select **Agree** to acknowledge the terms of service and then select **Done** to return to the deployment settings.</span></span>

![Consentiment de la implementació](./media/2DeploymentConsent.png)

7. <span data-ttu-id="167a0-127">Completeu els camps obligatoris restants a l'auxiliar i confirmeu la implementació.</span><span class="sxs-lookup"><span data-stu-id="167a0-127">Complete the remaining required fields in the wizard and confirm the deployment.</span></span> <span data-ttu-id="167a0-128">El temps de proveïment de l'entorn varia segons el tipus d'entorn.</span><span class="sxs-lookup"><span data-stu-id="167a0-128">Environment provisioning time varies based on the environment type.</span></span> <span data-ttu-id="167a0-129">El proveïment pot tardar fins a sis hores.</span><span class="sxs-lookup"><span data-stu-id="167a0-129">Provisioning might take up to six hours.</span></span>

  <span data-ttu-id="167a0-130">Quan la implementació es completi correctament, l'entorn es mostrarà com a **Implementat**.</span><span class="sxs-lookup"><span data-stu-id="167a0-130">After the deployment completes successfully, the environment will show as **Deployed**.</span></span>

8. <span data-ttu-id="167a0-131">Per confirmar que l'entorn s'ha implementat correctament, seleccioneu **Inicia la sessió** i inicieu la sessió a l'entorn per confirmar-ho.</span><span class="sxs-lookup"><span data-stu-id="167a0-131">To confirm the environment has deployed successfully, select **Login** and log on to the environment to confirm.</span></span>

![Detalls de l'entorn del ](./media/3EnvironmentDetails.png)

## <a name="apply-project-operations-finance-demo-data-optional-step"></a><span data-ttu-id="167a0-133">Aplicar les dades de demostració del Project Operations Finance (pas opcional)</span><span class="sxs-lookup"><span data-stu-id="167a0-133">Apply Project Operations Finance demo data (optional step)</span></span>

<span data-ttu-id="167a0-134">Apliqueu les dades de demostració del Project Operations Finance a l'entorn allotjat al núvol de la versió del servei 10.0.13 com es descriu en [aquest article](resource-apply-finance-demo-data.md).</span><span class="sxs-lookup"><span data-stu-id="167a0-134">Apply Project Operations Finance demo data to 10.0.13 service release Cloud Hosted Environment as described in [this article](resource-apply-finance-demo-data.md).</span></span>

## <a name="apply-updates-to-the-finance-environment"></a><span data-ttu-id="167a0-135">Aplicar les actualitzacions a l'entorn del Finance</span><span class="sxs-lookup"><span data-stu-id="167a0-135">Apply updates to the Finance environment</span></span>

<span data-ttu-id="167a0-136">El Project Operations requereix un entorn del Finance amb la versió de l'aplicació **10.0.13 (10.0.569.20009)** o superior.</span><span class="sxs-lookup"><span data-stu-id="167a0-136">Project Operations requires a Finance environment with application version **10.0.13 (10.0.569.20009)** or higher.</span></span>

<span data-ttu-id="167a0-137">Pot ser que hàgiu d'aplicar actualitzacions de qualitat al vostre entorn del Finance per rebre aquesta versió.</span><span class="sxs-lookup"><span data-stu-id="167a0-137">You might need to apply quality updates to your Finance environment to receive this version.</span></span>

1. <span data-ttu-id="167a0-138">Al LCS, a la pàgina **Detalls de l'entorn**, a la secció **Actualitzacions disponibles**, seleccioneu **Visualitza l'actualització**.</span><span class="sxs-lookup"><span data-stu-id="167a0-138">In LCS, on the **Environment details** page, in the **Available Updates** section, select **View Update**.</span></span>

![Visualitzar les actualitzacions](./media/5ViewUpdates.png)

2. <span data-ttu-id="167a0-140">A la pàgina **Actualitzacions binàries**, seleccioneu **Desa el paquet.**</span><span class="sxs-lookup"><span data-stu-id="167a0-140">On the **Binary updates** page, select **Save package.**</span></span>

![Desar el paquet](./media/6SavePackage.png)

3. <span data-ttu-id="167a0-142">Feu clic a **Selecciona-ho tot** i seleccioneu **Desa el paquet**.</span><span class="sxs-lookup"><span data-stu-id="167a0-142">Click **Select all** and then select **Save package**.</span></span>

![Revisar i desar les actualitzacions](./media/7ReviewAndSaveUpdates.png)

4. <span data-ttu-id="167a0-144">Introduïu un nom i una descripció del paquet i, a continuació, seleccioneu **Desa**.</span><span class="sxs-lookup"><span data-stu-id="167a0-144">Enter a name and a description of the package, and then select **Save**.</span></span> <span data-ttu-id="167a0-145">En funció de la connexió a Internet, pot ser que aquest procés tardi una estona.</span><span class="sxs-lookup"><span data-stu-id="167a0-145">Depending on the internet connection, this process might take some time.</span></span>

![Carregar el paquet a la biblioteca d'actius](./media/8UploadPackageToAssetsLibrary.png)

5. <span data-ttu-id="167a0-147">Un cop desat el paquet, seleccioneu **Fer** i deseu aquest paquet a la biblioteca d'actius del projecte del LCS.</span><span class="sxs-lookup"><span data-stu-id="167a0-147">After the package is saved, select **Done** and save this package to the Assets library in your LCS project.</span></span>

<span data-ttu-id="167a0-148">El desament i la validació del paquet poden tardar uns 15 minuts.</span><span class="sxs-lookup"><span data-stu-id="167a0-148">Saving and validating the package might take ~15 minutes.</span></span>

6. <span data-ttu-id="167a0-149">Per aplicar l'actualització, aneu a la pàgina **Detalls de l'entorn** del LCS i seleccioneu **Mantén** > **Aplica les actualitzacions**.</span><span class="sxs-lookup"><span data-stu-id="167a0-149">To apply the update, navigate to the **Environment details** page in LCS and select **Maintain** > **Apply updates**.</span></span>

![Mantenir els entorns](./media/9MaintainEnvironment.png)

7. <span data-ttu-id="167a0-151">A la llista actualitzacions, seleccioneu el paquet que heu creat i seleccioneu **Aplica**.</span><span class="sxs-lookup"><span data-stu-id="167a0-151">In the updates list select the package you created, and select **Apply**.</span></span>

![Aplicar les actualitzacions](./media/10ApplyUpdates.png)

<span data-ttu-id="167a0-153">El procés de servei de l'entorn tardarà una estona.</span><span class="sxs-lookup"><span data-stu-id="167a0-153">Environment servicing will take some time.</span></span> <span data-ttu-id="167a0-154">Després d'haver acabat, l'entorn tornarà a un estat implementat.</span><span class="sxs-lookup"><span data-stu-id="167a0-154">After it is complete, the environment will return to a deployed state.</span></span>

![Entorn implementat](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a><span data-ttu-id="167a0-156">Establir una connexió d'escriptura doble</span><span class="sxs-lookup"><span data-stu-id="167a0-156">Establish a Dual Write connection</span></span> 

1. <span data-ttu-id="167a0-157">Al projecte del LCS, aneu a la pàgina **Detalls de l'entorn**.</span><span class="sxs-lookup"><span data-stu-id="167a0-157">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="167a0-158">A **Informació de l'entorn del Common Data Service**, seleccioneu **Enllaça amb el CDS per a aplicacions**.</span><span class="sxs-lookup"><span data-stu-id="167a0-158">Under **Common Data Service Environment Information**, select **Link to CDS for Apps**.</span></span>
3. <span data-ttu-id="167a0-159">Després d'haver acabat l'enllaç, torneu a seleccionar **Enllaça amb el CDS per a aplicacions**.</span><span class="sxs-lookup"><span data-stu-id="167a0-159">After the link is complete, select **Link to CDS for Apps** again.</span></span> <span data-ttu-id="167a0-160">Se us redirigirà a l'escriptura doble al Finance.</span><span class="sxs-lookup"><span data-stu-id="167a0-160">You will be redirected to Dual Write in Finance.</span></span>

![Enllaça amb el CDS](./media/12LinktoCDS.png)

4. <span data-ttu-id="167a0-162">Seleccioneu **Aplica la solució** per accedir a les entitats que s'assignaran a la integració.</span><span class="sxs-lookup"><span data-stu-id="167a0-162">Select **Apply Solution** to access the entities that will be mapped in the integration.</span></span>

![Aplicar les solucions](./media/13ApplySolutions.png)

5. <span data-ttu-id="167a0-164">Seleccioneu les dues solucions, **Assignació d'entitats d'escriptura doble del Dynamics 365 Finance and Operations** i **Assignacions d'entitats d'escriptura doble del Dynamics 365 Project Operations** i, a continuació, seleccioneu **Aplica**.</span><span class="sxs-lookup"><span data-stu-id="167a0-164">Select both solutions, **Dynamics 365 Finance and Operations Dual Write Entity Map** and **Dynamics 365 Project Operations Dual Write Entity Maps**, and then select **Apply**.</span></span>

![Confirmar les solucions](./media/14ConfirmSolutions.png)

<span data-ttu-id="167a0-166">Després de l'aplicació de les solucions, les entitats d'escriptura doble s'apliquen a l'entorn.</span><span class="sxs-lookup"><span data-stu-id="167a0-166">After the solutions are applied, the Dual Write entities are applied to the environment.</span></span>

![Aplicar les solucions](./media/15ApplyingSolutions.png)

<span data-ttu-id="167a0-168">Després d'aplicar les entitats, totes les assignacions disponibles apareixen a la llista de l'entorn.</span><span class="sxs-lookup"><span data-stu-id="167a0-168">After the entities are applied, all available mappings are listed in the environment.</span></span>

![Assignacions d'escriptura doble](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a><span data-ttu-id="167a0-170">Actualitzar les entitats de dades després de l'actualització</span><span class="sxs-lookup"><span data-stu-id="167a0-170">Refresh the data entities after the update</span></span>

1. <span data-ttu-id="167a0-171">Al Finance, aneu a l'àrea de treball **Administració de dades**.</span><span class="sxs-lookup"><span data-stu-id="167a0-171">In Finance, go to the **Data management** workspace.</span></span>

![Espai de treball d'administració de dades](./media/16DataManagement.png)

2. <span data-ttu-id="167a0-173">Seleccioneu la peça **Paràmetres del marc**.</span><span class="sxs-lookup"><span data-stu-id="167a0-173">Select the **Framework parameters** tile.</span></span>

![Paràmetres del marc](./media/17FrameworkParameters.png)

3. <span data-ttu-id="167a0-175">A la pàgina **Configuració de l'entitat**, seleccioneu **Actualitza la llista d'entitats**.</span><span class="sxs-lookup"><span data-stu-id="167a0-175">On the **Entity settings** page, select **Refresh Entity list**.</span></span>

![Actualitzar la llista d'entitats](./media/18RefreshEntityList.png)

<span data-ttu-id="167a0-177">L'actualització tardarà uns 20 minuts.</span><span class="sxs-lookup"><span data-stu-id="167a0-177">The refresh is going to take approximately 20 minutes.</span></span> <span data-ttu-id="167a0-178">Rebreu una alerta quan s'hagi completat.</span><span class="sxs-lookup"><span data-stu-id="167a0-178">You will receive an alert when it is complete.</span></span>

![Confirmació d'actualització](./media/19RefreshConfirmation.png)

## <a name="run-project-operations-dual-write-maps"></a><span data-ttu-id="167a0-180">Executar assignacions d'escriptura doble del Project Operations</span><span class="sxs-lookup"><span data-stu-id="167a0-180">Run Project Operations Dual Write maps</span></span>

1. <span data-ttu-id="167a0-181">Al projecte del LCS, aneu a la pàgina **Detalls de l'entorn**.</span><span class="sxs-lookup"><span data-stu-id="167a0-181">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="167a0-182">A **Informació de l'entorn del Common Data Service**, seleccioneu **Enllaça amb el CDS per a aplicacions.**</span><span class="sxs-lookup"><span data-stu-id="167a0-182">Under **Common Data Service Environment Information**, select **Link to CDS for Apps.**</span></span> <span data-ttu-id="167a0-183">Després de seleccionar l'enllaç, se us redirigirà a la llista d'entitats de les assignacions.</span><span class="sxs-lookup"><span data-stu-id="167a0-183">After you select the link, you will be redirected to the list of entities in the mappings.</span></span>
3. <span data-ttu-id="167a0-184">Inicieu les assignacions com es descriu a la taula següent.</span><span class="sxs-lookup"><span data-stu-id="167a0-184">Start the maps as described in the following table.</span></span> <span data-ttu-id="167a0-185">Assegureu-vos de seguir la seqüència que s'indica a la llista.</span><span class="sxs-lookup"><span data-stu-id="167a0-185">Make sure to follow the sequence as listed.</span></span>

| <span data-ttu-id="167a0-186">**Assignació d'entitats**</span><span class="sxs-lookup"><span data-stu-id="167a0-186">**Entity Map**</span></span> | <span data-ttu-id="167a0-187">**Actualitzar l'entitat**</span><span class="sxs-lookup"><span data-stu-id="167a0-187">**Refresh entity**</span></span> | <span data-ttu-id="167a0-188">**Sincronització inicial**</span><span class="sxs-lookup"><span data-stu-id="167a0-188">**Initial sync**</span></span> | <span data-ttu-id="167a0-189">**Mestre per a la sincronització inicial**</span><span class="sxs-lookup"><span data-stu-id="167a0-189">**Master for initial sync**</span></span> | <span data-ttu-id="167a0-190">**Requisits previs de l'execució**</span><span class="sxs-lookup"><span data-stu-id="167a0-190">**Run prerequisites**</span></span> | <span data-ttu-id="167a0-191">**Sincronització inicial dels requisits previs**</span><span class="sxs-lookup"><span data-stu-id="167a0-191">**Prerequisites initial sync**</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="167a0-192">**Funcions de recurs del projecte per a totes les empreses (bookableresourcecategories)**</span><span class="sxs-lookup"><span data-stu-id="167a0-192">**Project Resource Roles for All Companies (bookableresourcecategories)**</span></span> | <span data-ttu-id="167a0-193">No</span><span class="sxs-lookup"><span data-stu-id="167a0-193">No</span></span> | <span data-ttu-id="167a0-194">Sí</span><span class="sxs-lookup"><span data-stu-id="167a0-194">Yes</span></span> | <span data-ttu-id="167a0-195">Common Data Service</span><span class="sxs-lookup"><span data-stu-id="167a0-195">Common Data Service</span></span> | <span data-ttu-id="167a0-196">No</span><span class="sxs-lookup"><span data-stu-id="167a0-196">No</span></span> | <span data-ttu-id="167a0-197">N/D</span><span class="sxs-lookup"><span data-stu-id="167a0-197">N\A</span></span> |
| <span data-ttu-id="167a0-198">**Entitats jurídiques (cdm\_companies)**</span><span class="sxs-lookup"><span data-stu-id="167a0-198">**Legal entities (cdm\_companies)**</span></span> | <span data-ttu-id="167a0-199">No</span><span class="sxs-lookup"><span data-stu-id="167a0-199">No</span></span> | <span data-ttu-id="167a0-200">Sí</span><span class="sxs-lookup"><span data-stu-id="167a0-200">Yes</span></span> | <span data-ttu-id="167a0-201">Aplicacions del Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="167a0-201">Finance and Operations apps</span></span> | <span data-ttu-id="167a0-202">No</span><span class="sxs-lookup"><span data-stu-id="167a0-202">No</span></span> | <span data-ttu-id="167a0-203">N/D</span><span class="sxs-lookup"><span data-stu-id="167a0-203">N\A</span></span> |
| <span data-ttu-id="167a0-204">**Valors reals d'integració del Project Operations (msdyn\_actuals)**</span><span class="sxs-lookup"><span data-stu-id="167a0-204">**Project Operations integration actuals (msdyn\_actuals)**</span></span> | <span data-ttu-id="167a0-205">No</span><span class="sxs-lookup"><span data-stu-id="167a0-205">No</span></span> | <span data-ttu-id="167a0-206">No</span><span class="sxs-lookup"><span data-stu-id="167a0-206">No</span></span> | <span data-ttu-id="167a0-207">N/D</span><span class="sxs-lookup"><span data-stu-id="167a0-207">N\A</span></span> | <span data-ttu-id="167a0-208">Sí</span><span class="sxs-lookup"><span data-stu-id="167a0-208">Yes</span></span> | <span data-ttu-id="167a0-209">No</span><span class="sxs-lookup"><span data-stu-id="167a0-209">No</span></span> |
| <span data-ttu-id="167a0-210">**Línies de contracte del projecte (salesorderdetails)**</span><span class="sxs-lookup"><span data-stu-id="167a0-210">**Project contract lines (salesorderdetails)**</span></span> | <span data-ttu-id="167a0-211">No</span><span class="sxs-lookup"><span data-stu-id="167a0-211">No</span></span> | <span data-ttu-id="167a0-212">No</span><span class="sxs-lookup"><span data-stu-id="167a0-212">No</span></span> | <span data-ttu-id="167a0-213">N/D</span><span class="sxs-lookup"><span data-stu-id="167a0-213">N\A</span></span> | <span data-ttu-id="167a0-214">No</span><span class="sxs-lookup"><span data-stu-id="167a0-214">No</span></span> | <span data-ttu-id="167a0-215">No</span><span class="sxs-lookup"><span data-stu-id="167a0-215">No</span></span> |
| <span data-ttu-id="167a0-216">**Entitat d'integració per a les relacions de transaccions del projecte (msdyn\_transactionconnections)**</span><span class="sxs-lookup"><span data-stu-id="167a0-216">**Integration entity for project transaction relationships (msdyn\_transactionconnections)**</span></span> | <span data-ttu-id="167a0-217">No</span><span class="sxs-lookup"><span data-stu-id="167a0-217">No</span></span> | <span data-ttu-id="167a0-218">No</span><span class="sxs-lookup"><span data-stu-id="167a0-218">No</span></span> | <span data-ttu-id="167a0-219">N/D</span><span class="sxs-lookup"><span data-stu-id="167a0-219">N\A</span></span> | <span data-ttu-id="167a0-220">No</span><span class="sxs-lookup"><span data-stu-id="167a0-220">No</span></span> | <span data-ttu-id="167a0-221">N/D</span><span class="sxs-lookup"><span data-stu-id="167a0-221">N\A</span></span> |
| <span data-ttu-id="167a0-222">**Fites de línia de contracte d'integració del Project Operations (msdyn\_contractlinesscheduleofvalues)**</span><span class="sxs-lookup"><span data-stu-id="167a0-222">**Project Operations integration contract line milestones (msdyn\_contractlinesscheduleofvalues)**</span></span> | <span data-ttu-id="167a0-223">No</span><span class="sxs-lookup"><span data-stu-id="167a0-223">No</span></span> | <span data-ttu-id="167a0-224">No</span><span class="sxs-lookup"><span data-stu-id="167a0-224">No</span></span> | <span data-ttu-id="167a0-225">N/D</span><span class="sxs-lookup"><span data-stu-id="167a0-225">N\A</span></span> | <span data-ttu-id="167a0-226">No</span><span class="sxs-lookup"><span data-stu-id="167a0-226">No</span></span> | <span data-ttu-id="167a0-227">N/D</span><span class="sxs-lookup"><span data-stu-id="167a0-227">N\A</span></span> |
| <span data-ttu-id="167a0-228">**Entitat d'integració del Project Operations per a l'estimació de despeses (msdyn\_estimateslines)**</span><span class="sxs-lookup"><span data-stu-id="167a0-228">**Project Operations integration entity for expense estimates (msdyn\_estimateslines)**</span></span> | <span data-ttu-id="167a0-229">No</span><span class="sxs-lookup"><span data-stu-id="167a0-229">No</span></span> | <span data-ttu-id="167a0-230">No</span><span class="sxs-lookup"><span data-stu-id="167a0-230">No</span></span> | <span data-ttu-id="167a0-231">N/D</span><span class="sxs-lookup"><span data-stu-id="167a0-231">N\A</span></span> | <span data-ttu-id="167a0-232">No</span><span class="sxs-lookup"><span data-stu-id="167a0-232">No</span></span> | <span data-ttu-id="167a0-233">N/D</span><span class="sxs-lookup"><span data-stu-id="167a0-233">N\A</span></span> |
| <span data-ttu-id="167a0-234">**Entitat d'integració del Project Operations per a l'estimació d'hores (msdyn\_resourceassignments)**</span><span class="sxs-lookup"><span data-stu-id="167a0-234">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="167a0-235">No</span><span class="sxs-lookup"><span data-stu-id="167a0-235">No</span></span> | <span data-ttu-id="167a0-236">No</span><span class="sxs-lookup"><span data-stu-id="167a0-236">No</span></span> | <span data-ttu-id="167a0-237">N/D</span><span class="sxs-lookup"><span data-stu-id="167a0-237">N\A</span></span> | <span data-ttu-id="167a0-238">No</span><span class="sxs-lookup"><span data-stu-id="167a0-238">No</span></span> | <span data-ttu-id="167a0-239">N/D</span><span class="sxs-lookup"><span data-stu-id="167a0-239">N\A</span></span> |
| <span data-ttu-id="167a0-240">**Entitat d'exportació de despeses del projecte d'integració del Project Operations (msdyn\_expenses)**</span><span class="sxs-lookup"><span data-stu-id="167a0-240">**Project Operations integration project expenses export entity (msdyn\_expenses)**</span></span> | <span data-ttu-id="167a0-241">Sí</span><span class="sxs-lookup"><span data-stu-id="167a0-241">Yes</span></span> | <span data-ttu-id="167a0-242">No</span><span class="sxs-lookup"><span data-stu-id="167a0-242">No</span></span> | <span data-ttu-id="167a0-243">N/D</span><span class="sxs-lookup"><span data-stu-id="167a0-243">N\A</span></span> | <span data-ttu-id="167a0-244">No</span><span class="sxs-lookup"><span data-stu-id="167a0-244">No</span></span> | <span data-ttu-id="167a0-245">N/D</span><span class="sxs-lookup"><span data-stu-id="167a0-245">N\A</span></span> |
| <span data-ttu-id="167a0-246">**Entitat d'integració del Project Operations per a l'estimació d'hores (msdyn\_resourceassignments)**</span><span class="sxs-lookup"><span data-stu-id="167a0-246">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="167a0-247">Sí</span><span class="sxs-lookup"><span data-stu-id="167a0-247">Yes</span></span> | <span data-ttu-id="167a0-248">No</span><span class="sxs-lookup"><span data-stu-id="167a0-248">No</span></span> | <span data-ttu-id="167a0-249">N/D</span><span class="sxs-lookup"><span data-stu-id="167a0-249">N\A</span></span> | <span data-ttu-id="167a0-250">No</span><span class="sxs-lookup"><span data-stu-id="167a0-250">No</span></span> | <span data-ttu-id="167a0-251">N/D</span><span class="sxs-lookup"><span data-stu-id="167a0-251">N\A</span></span> |

4. <span data-ttu-id="167a0-252">Per actualitzar l'entitat, seleccioneu el nom de l'assignació i, a continuació, **Actualitza les entitats**.</span><span class="sxs-lookup"><span data-stu-id="167a0-252">To refresh the entity, select the map name, and then select **Refresh entities**.</span></span> 
5. <span data-ttu-id="167a0-253">Continueu amb l'execució de l'assignació després d'haver acabat l'actualització.</span><span class="sxs-lookup"><span data-stu-id="167a0-253">Proceed with running the map after the refresh is complete.</span></span>

![Actualitzar l'assignació](./media/20RefreshMapping.png)

<span data-ttu-id="167a0-255">Abans d'habilitar la següent assignació, verifiqueu que l'assignació de la taula estigui en estat **En execució**.</span><span class="sxs-lookup"><span data-stu-id="167a0-255">Before you enable the next map, verify that the map in the table is in a state of **Running**.</span></span> <span data-ttu-id="167a0-256">L'execució d'assignacions amb un major nombre de requisits previs podria tardar una estona.</span><span class="sxs-lookup"><span data-stu-id="167a0-256">Running maps with a larger number of prerequisites might take some time.</span></span>

<span data-ttu-id="167a0-257">Per executar una assignació amb requisits previs, habiliteu l'opció **Mostra les assignacions d'entitats relacionades**.</span><span class="sxs-lookup"><span data-stu-id="167a0-257">To run a map with prerequisites, enable the **Show related entity maps** toggle.</span></span> <span data-ttu-id="167a0-258">Si la taula indica que la **Sincronització inicial de requisits previs** és **No**, verifiqueu que l'indicador **Sincronització inicial** estigui **desactivat** a totes les assignacions de requisits previs abans d'executar-la.</span><span class="sxs-lookup"><span data-stu-id="167a0-258">If the table indicates **Prerequisite initial sync** is **No**, verify that the **Initial sync** flag is **Off** in all the prerequisite maps before you run it.</span></span>

![Executar l'assignació](./media/21RunMap.png)

6. <span data-ttu-id="167a0-260">Valideu que totes les assignacions relacionades del projecte estiguin en execució.</span><span class="sxs-lookup"><span data-stu-id="167a0-260">Validate all project related maps are in the running state.</span></span>

![Totes les assignacions en execució](./media/22AllMapsRunning.png)

<span data-ttu-id="167a0-262">L'entorn del Project Operations ja està proveït i configurat.</span><span class="sxs-lookup"><span data-stu-id="167a0-262">Your Project Operations environment is now provisioned and configured.</span></span>
