---
title: Proveïment d'un entorn nou
description: En aquest tema s'ofereix informació sobre com proveir un entorn nou del Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 9ed502a1312b702e029d8910d62f72b8e0e4df06
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642947"
---
# <a name="provision-a-new-environment"></a><span data-ttu-id="ee50e-103">Proveïment d'un entorn nou</span><span class="sxs-lookup"><span data-stu-id="ee50e-103">Provision a new environment</span></span>

<span data-ttu-id="ee50e-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_</span><span class="sxs-lookup"><span data-stu-id="ee50e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="ee50e-105">En aquest tema es proporciona informació sobre com proveir un nou entorn de Dynamics 365 Project Operations per a escenaris basats en recursos/sense existències.</span><span class="sxs-lookup"><span data-stu-id="ee50e-105">This topic provides information about how to provision a new Dynamics 365 Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a><span data-ttu-id="ee50e-106">Habilitar el proveïment automatitzat del Project Operations en un projecte del LCS</span><span class="sxs-lookup"><span data-stu-id="ee50e-106">Enable Project Operations automated provisioning in an LCS project</span></span>

<span data-ttu-id="ee50e-107">Seguiu aquests passos per habilitar el flux de proveïment automatitzat del Project Operations per al projecte del LCS.</span><span class="sxs-lookup"><span data-stu-id="ee50e-107">Use following steps to enable the Project Operations automated provisioning flow for your LCS project.</span></span>

1. <span data-ttu-id="ee50e-108">Aneu a [LCS](https://lcs.dynamics.com/v2) i seleccioneu la peça **Administració de característiques de versió preliminar**.</span><span class="sxs-lookup"><span data-stu-id="ee50e-108">Go to [LCS](https://lcs.dynamics.com/v2) and select the **Preview Feature management** tile.</span></span>
2. <span data-ttu-id="ee50e-109">A la llista **Característiques de versió preliminar**, seleccioneu **Característica del Project Operations** i **Característica de versió preliminar habilitada** per habilitar el Project Operations.</span><span class="sxs-lookup"><span data-stu-id="ee50e-109">In the **Preview feature** list, select **Project Operations Feature**, and then select **Preview feature enabled** to enable Project Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="ee50e-110">Aquest pas només es fa una vegada per projecte del LCS.</span><span class="sxs-lookup"><span data-stu-id="ee50e-110">This step is performed only one time per LCS project.</span></span>

## <a name="provision-a-project-operations-environment"></a><span data-ttu-id="ee50e-111">Proveïment d'un entorn del Project Operations</span><span class="sxs-lookup"><span data-stu-id="ee50e-111">Provision a Project Operations environment</span></span>

1. <span data-ttu-id="ee50e-112">Obriu una nova implementació d'un [entorn de demostració](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) o [entorn de producció](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) del Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="ee50e-112">Open a new Dynamics 365 Finance [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) or [sandbox/ production environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) deployment.</span></span> 
2. <span data-ttu-id="ee50e-113">Seguiu els passos de l'auxiliar **Proveïment de l'entorn**.</span><span class="sxs-lookup"><span data-stu-id="ee50e-113">Walk through the **Environment provisioning** wizard.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="ee50e-114">Assegureu-vos que la versió de l'aplicació seleccionada sigui 10.0.13 o superior.</span><span class="sxs-lookup"><span data-stu-id="ee50e-114">Make sure selected application version is 10.0.13 or higher.</span></span>

3. <span data-ttu-id="ee50e-115">Per proveir el Project Operations, a **Configuració avançada**, seleccioneu **Common Data Service**.</span><span class="sxs-lookup"><span data-stu-id="ee50e-115">To provision Project Operations, under **Advance settings**, select **Common Data Service**.</span></span> 
4. <span data-ttu-id="ee50e-116">Habiliteu la **Configuració del Common Data Service** seleccionant **Sí** i, a continuació, introduïu informació als camps obligatoris:</span><span class="sxs-lookup"><span data-stu-id="ee50e-116">Enable the **Common Data Service Setting** by selecting **Yes** and then enter information in the required fields:</span></span>

  - <span data-ttu-id="ee50e-117">Nom</span><span class="sxs-lookup"><span data-stu-id="ee50e-117">Name</span></span>
  - <span data-ttu-id="ee50e-118">Regió</span><span class="sxs-lookup"><span data-stu-id="ee50e-118">Region</span></span>
  - <span data-ttu-id="ee50e-119">Language</span><span class="sxs-lookup"><span data-stu-id="ee50e-119">Language</span></span>
  - <span data-ttu-id="ee50e-120">Moneda</span><span class="sxs-lookup"><span data-stu-id="ee50e-120">Currency</span></span>
 
5. <span data-ttu-id="ee50e-121">Al camp **Plantilla del Common Data Service**, seleccioneu **Project Operations**</span><span class="sxs-lookup"><span data-stu-id="ee50e-121">In the **Common Data Service Template** field, select **Project Operations**</span></span> 

6. <span data-ttu-id="ee50e-122">Seleccioneu el tipus d'entorn per a la implementació.</span><span class="sxs-lookup"><span data-stu-id="ee50e-122">Select the environment type for your deployment.</span></span> <span data-ttu-id="ee50e-123">Una prova basada en subscripció us permetrà implementar un entorn del CDS durant 30 dies.</span><span class="sxs-lookup"><span data-stu-id="ee50e-123">A subscription-based trial will let you deploy a CDS environment for 30 days.</span></span> 

![Configuració de la implementació](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> <span data-ttu-id="ee50e-125">Seleccioneu **Accepto** per reconèixer les condicions del servei i, a continuació, seleccioneu **Fet** per tornar a la configuració de la implementació.</span><span class="sxs-lookup"><span data-stu-id="ee50e-125">Select **Agree** to acknowledge the terms of service and then select **Done** to return to the deployment settings.</span></span>

![Consentiment de la implementació](./media/2DeploymentConsent.png)

7. <span data-ttu-id="ee50e-127">Completeu els camps obligatoris restants a l'auxiliar i confirmeu la implementació.</span><span class="sxs-lookup"><span data-stu-id="ee50e-127">Complete the remaining required fields in the wizard and confirm the deployment.</span></span> <span data-ttu-id="ee50e-128">El temps de proveïment de l'entorn varia segons el tipus d'entorn.</span><span class="sxs-lookup"><span data-stu-id="ee50e-128">Environment provisioning time varies based on the environment type.</span></span> <span data-ttu-id="ee50e-129">El proveïment pot tardar fins a sis hores.</span><span class="sxs-lookup"><span data-stu-id="ee50e-129">Provisioning might take up to six hours.</span></span>

  <span data-ttu-id="ee50e-130">Quan la implementació es completi correctament, l'entorn es mostrarà com a **Implementat**.</span><span class="sxs-lookup"><span data-stu-id="ee50e-130">After the deployment completes successfully, the environment will show as **Deployed**.</span></span>

8. <span data-ttu-id="ee50e-131">Per confirmar que l'entorn s'ha implementat correctament, seleccioneu **Inicia la sessió** i inicieu la sessió a l'entorn per confirmar-ho.</span><span class="sxs-lookup"><span data-stu-id="ee50e-131">To confirm the environment has deployed successfully, select **Login** and log on to the environment to confirm.</span></span>

![Detalls de l'entorn del ](./media/3EnvironmentDetails.png)

## <a name="apply-project-operations-finance-demo-data-optional-step"></a><span data-ttu-id="ee50e-133">Aplicar les dades de demostració del Project Operations Finance (pas opcional)</span><span class="sxs-lookup"><span data-stu-id="ee50e-133">Apply Project Operations Finance demo data (optional step)</span></span>

<span data-ttu-id="ee50e-134">Apliqueu les dades de demostració del Project Operations Finance a l'entorn allotjat al núvol de la versió del servei 10.0.13 com es descriu en [aquest article](resource-apply-finance-demo-data.md).</span><span class="sxs-lookup"><span data-stu-id="ee50e-134">Apply Project Operations Finance demo data to 10.0.13 service release Cloud Hosted Environment as described in [this article](resource-apply-finance-demo-data.md).</span></span>

## <a name="apply-updates-to-the-finance-environment"></a><span data-ttu-id="ee50e-135">Aplicar les actualitzacions a l'entorn del Finance</span><span class="sxs-lookup"><span data-stu-id="ee50e-135">Apply updates to the Finance environment</span></span>

<span data-ttu-id="ee50e-136">El Project Operations requereix un entorn del Finance amb la versió de l'aplicació **10.0.13 (10.0.569.20009)** o superior.</span><span class="sxs-lookup"><span data-stu-id="ee50e-136">Project Operations requires a Finance environment with application version **10.0.13 (10.0.569.20009)** or higher.</span></span>

<span data-ttu-id="ee50e-137">Pot ser que hàgiu d'aplicar actualitzacions de qualitat al vostre entorn del Finance per rebre aquesta versió.</span><span class="sxs-lookup"><span data-stu-id="ee50e-137">You might need to apply quality updates to your Finance environment to receive this version.</span></span>

1. <span data-ttu-id="ee50e-138">Al LCS, a la pàgina **Detalls de l'entorn**, a la secció **Actualitzacions disponibles**, seleccioneu **Visualitza l'actualització**.</span><span class="sxs-lookup"><span data-stu-id="ee50e-138">In LCS, on the **Environment details** page, in the **Available Updates** section, select **View Update**.</span></span>

![Visualitzar les actualitzacions](./media/5ViewUpdates.png)

2. <span data-ttu-id="ee50e-140">A la pàgina **Actualitzacions binàries**, seleccioneu **Desa el paquet.**</span><span class="sxs-lookup"><span data-stu-id="ee50e-140">On the **Binary updates** page, select **Save package.**</span></span>

![Desar el paquet](./media/6SavePackage.png)

3. <span data-ttu-id="ee50e-142">Feu clic a **Selecciona-ho tot** i seleccioneu **Desa el paquet**.</span><span class="sxs-lookup"><span data-stu-id="ee50e-142">Click **Select all** and then select **Save package**.</span></span>

![Revisar i desar les actualitzacions](./media/7ReviewAndSaveUpdates.png)

4. <span data-ttu-id="ee50e-144">Introduïu un nom i una descripció del paquet i, a continuació, seleccioneu **Desa**.</span><span class="sxs-lookup"><span data-stu-id="ee50e-144">Enter a name and a description of the package, and then select **Save**.</span></span> <span data-ttu-id="ee50e-145">En funció de la connexió a Internet, pot ser que aquest procés tardi una estona.</span><span class="sxs-lookup"><span data-stu-id="ee50e-145">Depending on the internet connection, this process might take some time.</span></span>

![Carregar el paquet a la biblioteca d'actius](./media/8UploadPackageToAssetsLibrary.png)

5. <span data-ttu-id="ee50e-147">Un cop desat el paquet, seleccioneu **Fer** i deseu aquest paquet a la biblioteca d'actius del projecte del LCS.</span><span class="sxs-lookup"><span data-stu-id="ee50e-147">After the package is saved, select **Done** and save this package to the Assets library in your LCS project.</span></span>

<span data-ttu-id="ee50e-148">El desament i la validació del paquet poden tardar uns 15 minuts.</span><span class="sxs-lookup"><span data-stu-id="ee50e-148">Saving and validating the package might take ~15 minutes.</span></span>

6. <span data-ttu-id="ee50e-149">Per aplicar l'actualització, aneu a la pàgina **Detalls de l'entorn** del LCS i seleccioneu **Mantén** > **Aplica les actualitzacions**.</span><span class="sxs-lookup"><span data-stu-id="ee50e-149">To apply the update, navigate to the **Environment details** page in LCS and select **Maintain** > **Apply updates**.</span></span>

![Mantenir els entorns](./media/9MaintainEnvironment.png)

7. <span data-ttu-id="ee50e-151">A la llista actualitzacions, seleccioneu el paquet que heu creat i seleccioneu **Aplica**.</span><span class="sxs-lookup"><span data-stu-id="ee50e-151">In the updates list select the package you created, and select **Apply**.</span></span>

![Aplicar les actualitzacions](./media/10ApplyUpdates.png)

<span data-ttu-id="ee50e-153">El procés de servei de l'entorn tardarà una estona.</span><span class="sxs-lookup"><span data-stu-id="ee50e-153">Environment servicing will take some time.</span></span> <span data-ttu-id="ee50e-154">Després d'haver acabat, l'entorn tornarà a un estat implementat.</span><span class="sxs-lookup"><span data-stu-id="ee50e-154">After it is complete, the environment will return to a deployed state.</span></span>

![Entorn implementat](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a><span data-ttu-id="ee50e-156">Establir una connexió d'escriptura doble</span><span class="sxs-lookup"><span data-stu-id="ee50e-156">Establish a Dual Write connection</span></span> 

1. <span data-ttu-id="ee50e-157">Al projecte del LCS, aneu a la pàgina **Detalls de l'entorn**.</span><span class="sxs-lookup"><span data-stu-id="ee50e-157">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="ee50e-158">A **Informació de l'entorn del Common Data Service**, seleccioneu **Enllaça amb el CDS per a aplicacions**.</span><span class="sxs-lookup"><span data-stu-id="ee50e-158">Under **Common Data Service Environment Information**, select **Link to CDS for Apps**.</span></span>
3. <span data-ttu-id="ee50e-159">Després d'haver acabat l'enllaç, torneu a seleccionar **Enllaça amb el CDS per a aplicacions**.</span><span class="sxs-lookup"><span data-stu-id="ee50e-159">After the link is complete, select **Link to CDS for Apps** again.</span></span> <span data-ttu-id="ee50e-160">Se us redirigirà a l'escriptura doble al Finance.</span><span class="sxs-lookup"><span data-stu-id="ee50e-160">You will be redirected to Dual Write in Finance.</span></span>

![Enllaça amb el CDS](./media/12LinktoCDS.png)

4. <span data-ttu-id="ee50e-162">Seleccioneu **Aplica la solució** per accedir a les entitats que s'assignaran a la integració.</span><span class="sxs-lookup"><span data-stu-id="ee50e-162">Select **Apply Solution** to access the entities that will be mapped in the integration.</span></span>

![Aplicar les solucions](./media/13ApplySolutions.png)

5. <span data-ttu-id="ee50e-164">Seleccioneu les dues solucions, el mapa d'entitats del **Dynamics 365 Finance and Operations d'escriptura doble** i els mapes d'entitat del **Dynamics 365 Project Operations d'escriptura doble** i, a continuació, seleccioneu **Aplicar**.</span><span class="sxs-lookup"><span data-stu-id="ee50e-164">Select both solutions, **Dynamics 365 Finance and Operations Dual Write Entity Map** and **Dynamics 365 Project Operations Dual Write Entity Maps**, and then select **Apply**.</span></span>

![Confirmar les solucions](./media/14ConfirmSolutions.png)

<span data-ttu-id="ee50e-166">Després de l'aplicació de les solucions, les entitats d'escriptura doble s'apliquen a l'entorn.</span><span class="sxs-lookup"><span data-stu-id="ee50e-166">After the solutions are applied, the Dual Write entities are applied to the environment.</span></span>

![Aplicar les solucions](./media/15ApplyingSolutions.png)

<span data-ttu-id="ee50e-168">Després d'aplicar les entitats, totes les assignacions disponibles apareixen a la llista de l'entorn.</span><span class="sxs-lookup"><span data-stu-id="ee50e-168">After the entities are applied, all available mappings are listed in the environment.</span></span>

![Assignacions d'escriptura doble](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a><span data-ttu-id="ee50e-170">Actualitzar les entitats de dades després de l'actualització</span><span class="sxs-lookup"><span data-stu-id="ee50e-170">Refresh the data entities after the update</span></span>

1. <span data-ttu-id="ee50e-171">Al Finance, aneu a l'àrea de treball **Administració de dades**.</span><span class="sxs-lookup"><span data-stu-id="ee50e-171">In Finance, go to the **Data management** workspace.</span></span>

![Espai de treball d'administració de dades](./media/16DataManagement.png)

2. <span data-ttu-id="ee50e-173">Seleccioneu la peça **Paràmetres del marc**.</span><span class="sxs-lookup"><span data-stu-id="ee50e-173">Select the **Framework parameters** tile.</span></span>

![Paràmetres del marc](./media/17FrameworkParameters.png)

3. <span data-ttu-id="ee50e-175">A la pàgina **Configuració de l'entitat**, seleccioneu **Actualitza la llista d'entitats**.</span><span class="sxs-lookup"><span data-stu-id="ee50e-175">On the **Entity settings** page, select **Refresh Entity list**.</span></span>

![Actualitzar la llista d'entitats](./media/18RefreshEntityList.png)

<span data-ttu-id="ee50e-177">L'actualització tardarà uns 20 minuts.</span><span class="sxs-lookup"><span data-stu-id="ee50e-177">The refresh is going to take approximately 20 minutes.</span></span> <span data-ttu-id="ee50e-178">Rebreu una alerta quan s'hagi completat.</span><span class="sxs-lookup"><span data-stu-id="ee50e-178">You will receive an alert when it is complete.</span></span>

![Confirmació d'actualització](./media/19RefreshConfirmation.png)

## <a name="run-project-operations-dual-write-maps"></a><span data-ttu-id="ee50e-180">Executar assignacions d'escriptura doble del Project Operations</span><span class="sxs-lookup"><span data-stu-id="ee50e-180">Run Project Operations Dual Write maps</span></span>

1. <span data-ttu-id="ee50e-181">Al projecte del LCS, aneu a la pàgina **Detalls de l'entorn**.</span><span class="sxs-lookup"><span data-stu-id="ee50e-181">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="ee50e-182">A **Informació de l'entorn del Common Data Service**, seleccioneu **Enllaça amb el CDS per a aplicacions.**</span><span class="sxs-lookup"><span data-stu-id="ee50e-182">Under **Common Data Service Environment Information**, select **Link to CDS for Apps.**</span></span> <span data-ttu-id="ee50e-183">Després de seleccionar l'enllaç, se us redirigirà a la llista d'entitats de les assignacions.</span><span class="sxs-lookup"><span data-stu-id="ee50e-183">After you select the link, you will be redirected to the list of entities in the mappings.</span></span>
3. <span data-ttu-id="ee50e-184">Inicieu les assignacions com es descriu a la taula següent.</span><span class="sxs-lookup"><span data-stu-id="ee50e-184">Start the maps as described in the following table.</span></span> <span data-ttu-id="ee50e-185">Assegureu-vos de seguir la seqüència que s'indica a la llista.</span><span class="sxs-lookup"><span data-stu-id="ee50e-185">Make sure to follow the sequence as listed.</span></span>

| <span data-ttu-id="ee50e-186">**Assignació d'entitats**</span><span class="sxs-lookup"><span data-stu-id="ee50e-186">**Entity Map**</span></span> | <span data-ttu-id="ee50e-187">**Actualitzar l'entitat**</span><span class="sxs-lookup"><span data-stu-id="ee50e-187">**Refresh entity**</span></span> | <span data-ttu-id="ee50e-188">**Sincronització inicial**</span><span class="sxs-lookup"><span data-stu-id="ee50e-188">**Initial sync**</span></span> | <span data-ttu-id="ee50e-189">**Mestre per a la sincronització inicial**</span><span class="sxs-lookup"><span data-stu-id="ee50e-189">**Master for initial sync**</span></span> | <span data-ttu-id="ee50e-190">**Requisits previs de l'execució**</span><span class="sxs-lookup"><span data-stu-id="ee50e-190">**Run prerequisites**</span></span> | <span data-ttu-id="ee50e-191">**Sincronització inicial dels requisits previs**</span><span class="sxs-lookup"><span data-stu-id="ee50e-191">**Prerequisites initial sync**</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="ee50e-192">**Funcions de recurs del projecte per a totes les empreses (bookableresourcecategories)**</span><span class="sxs-lookup"><span data-stu-id="ee50e-192">**Project Resource Roles for All Companies (bookableresourcecategories)**</span></span> | <span data-ttu-id="ee50e-193">No</span><span class="sxs-lookup"><span data-stu-id="ee50e-193">No</span></span> | <span data-ttu-id="ee50e-194">Sí</span><span class="sxs-lookup"><span data-stu-id="ee50e-194">Yes</span></span> | <span data-ttu-id="ee50e-195">Common Data Service</span><span class="sxs-lookup"><span data-stu-id="ee50e-195">Common Data Service</span></span> | <span data-ttu-id="ee50e-196">No</span><span class="sxs-lookup"><span data-stu-id="ee50e-196">No</span></span> | <span data-ttu-id="ee50e-197">N/D</span><span class="sxs-lookup"><span data-stu-id="ee50e-197">N\A</span></span> |
| <span data-ttu-id="ee50e-198">**Entitats jurídiques (cdm\_companies)**</span><span class="sxs-lookup"><span data-stu-id="ee50e-198">**Legal entities (cdm\_companies)**</span></span> | <span data-ttu-id="ee50e-199">No</span><span class="sxs-lookup"><span data-stu-id="ee50e-199">No</span></span> | <span data-ttu-id="ee50e-200">Sí</span><span class="sxs-lookup"><span data-stu-id="ee50e-200">Yes</span></span> | <span data-ttu-id="ee50e-201">Aplicacions del Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ee50e-201">Finance and Operations apps</span></span> | <span data-ttu-id="ee50e-202">No</span><span class="sxs-lookup"><span data-stu-id="ee50e-202">No</span></span> | <span data-ttu-id="ee50e-203">N/D</span><span class="sxs-lookup"><span data-stu-id="ee50e-203">N\A</span></span> |
| <span data-ttu-id="ee50e-204">**Llibre major (msdyn_ledgers)**</span><span class="sxs-lookup"><span data-stu-id="ee50e-204">**Ledger (msdyn_ledgers)**</span></span> | <span data-ttu-id="ee50e-205">No</span><span class="sxs-lookup"><span data-stu-id="ee50e-205">No</span></span> | <span data-ttu-id="ee50e-206">Sí</span><span class="sxs-lookup"><span data-stu-id="ee50e-206">Yes</span></span> | <span data-ttu-id="ee50e-207">Aplicacions del Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ee50e-207">Finance and Operations apps</span></span> | <span data-ttu-id="ee50e-208">Sí</span><span class="sxs-lookup"><span data-stu-id="ee50e-208">Yes</span></span> | <span data-ttu-id="ee50e-209">Sí, les aplicacions de Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ee50e-209">Yes, Finance and Operations apps</span></span> |
| <span data-ttu-id="ee50e-210">**Valors reals d'integració del Project Operations (msdyn\_actuals)**</span><span class="sxs-lookup"><span data-stu-id="ee50e-210">**Project Operations integration actuals (msdyn\_actuals)**</span></span> | <span data-ttu-id="ee50e-211">No</span><span class="sxs-lookup"><span data-stu-id="ee50e-211">No</span></span> | <span data-ttu-id="ee50e-212">No</span><span class="sxs-lookup"><span data-stu-id="ee50e-212">No</span></span> | <span data-ttu-id="ee50e-213">N/D</span><span class="sxs-lookup"><span data-stu-id="ee50e-213">N\A</span></span> | <span data-ttu-id="ee50e-214">Sí</span><span class="sxs-lookup"><span data-stu-id="ee50e-214">Yes</span></span> | <span data-ttu-id="ee50e-215">No</span><span class="sxs-lookup"><span data-stu-id="ee50e-215">No</span></span> |
| <span data-ttu-id="ee50e-216">**Línies de contracte del projecte (salesorderdetails)**</span><span class="sxs-lookup"><span data-stu-id="ee50e-216">**Project contract lines (salesorderdetails)**</span></span> | <span data-ttu-id="ee50e-217">No</span><span class="sxs-lookup"><span data-stu-id="ee50e-217">No</span></span> | <span data-ttu-id="ee50e-218">No</span><span class="sxs-lookup"><span data-stu-id="ee50e-218">No</span></span> | <span data-ttu-id="ee50e-219">N/D</span><span class="sxs-lookup"><span data-stu-id="ee50e-219">N\A</span></span> | <span data-ttu-id="ee50e-220">No</span><span class="sxs-lookup"><span data-stu-id="ee50e-220">No</span></span> | <span data-ttu-id="ee50e-221">No</span><span class="sxs-lookup"><span data-stu-id="ee50e-221">No</span></span> |
| <span data-ttu-id="ee50e-222">**Entitat d'integració per a les relacions de transaccions del projecte (msdyn\_transactionconnections)**</span><span class="sxs-lookup"><span data-stu-id="ee50e-222">**Integration entity for project transaction relationships (msdyn\_transactionconnections)**</span></span> | <span data-ttu-id="ee50e-223">No</span><span class="sxs-lookup"><span data-stu-id="ee50e-223">No</span></span> | <span data-ttu-id="ee50e-224">No</span><span class="sxs-lookup"><span data-stu-id="ee50e-224">No</span></span> | <span data-ttu-id="ee50e-225">N/D</span><span class="sxs-lookup"><span data-stu-id="ee50e-225">N\A</span></span> | <span data-ttu-id="ee50e-226">No</span><span class="sxs-lookup"><span data-stu-id="ee50e-226">No</span></span> | <span data-ttu-id="ee50e-227">N/D</span><span class="sxs-lookup"><span data-stu-id="ee50e-227">N\A</span></span> |
| <span data-ttu-id="ee50e-228">**Fites de línia de contracte d'integració del Project Operations (msdyn\_contractlinesscheduleofvalues)**</span><span class="sxs-lookup"><span data-stu-id="ee50e-228">**Project Operations integration contract line milestones (msdyn\_contractlinesscheduleofvalues)**</span></span> | <span data-ttu-id="ee50e-229">No</span><span class="sxs-lookup"><span data-stu-id="ee50e-229">No</span></span> | <span data-ttu-id="ee50e-230">No</span><span class="sxs-lookup"><span data-stu-id="ee50e-230">No</span></span> | <span data-ttu-id="ee50e-231">N/D</span><span class="sxs-lookup"><span data-stu-id="ee50e-231">N\A</span></span> | <span data-ttu-id="ee50e-232">No</span><span class="sxs-lookup"><span data-stu-id="ee50e-232">No</span></span> | <span data-ttu-id="ee50e-233">N/D</span><span class="sxs-lookup"><span data-stu-id="ee50e-233">N\A</span></span> |
| <span data-ttu-id="ee50e-234">**Entitat d'integració del Project Operations per a l'estimació de despeses (msdyn\_estimateslines)**</span><span class="sxs-lookup"><span data-stu-id="ee50e-234">**Project Operations integration entity for expense estimates (msdyn\_estimateslines)**</span></span> | <span data-ttu-id="ee50e-235">No</span><span class="sxs-lookup"><span data-stu-id="ee50e-235">No</span></span> | <span data-ttu-id="ee50e-236">No</span><span class="sxs-lookup"><span data-stu-id="ee50e-236">No</span></span> | <span data-ttu-id="ee50e-237">N/D</span><span class="sxs-lookup"><span data-stu-id="ee50e-237">N\A</span></span> | <span data-ttu-id="ee50e-238">No</span><span class="sxs-lookup"><span data-stu-id="ee50e-238">No</span></span> | <span data-ttu-id="ee50e-239">N/D</span><span class="sxs-lookup"><span data-stu-id="ee50e-239">N\A</span></span> |
| <span data-ttu-id="ee50e-240">**Entitat d'exportació de categories de despeses del projecte d'integració del Project Operations (msdyn\_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="ee50e-240">**Project Operations integration project expense categories export entity (msdyn\_expensecategories)**</span></span> | <span data-ttu-id="ee50e-241">No</span><span class="sxs-lookup"><span data-stu-id="ee50e-241">No</span></span> | <span data-ttu-id="ee50e-242">No</span><span class="sxs-lookup"><span data-stu-id="ee50e-242">No</span></span> | <span data-ttu-id="ee50e-243">N/D</span><span class="sxs-lookup"><span data-stu-id="ee50e-243">N\A</span></span> | <span data-ttu-id="ee50e-244">No</span><span class="sxs-lookup"><span data-stu-id="ee50e-244">No</span></span> | <span data-ttu-id="ee50e-245">N/D</span><span class="sxs-lookup"><span data-stu-id="ee50e-245">N\A</span></span> |
| <span data-ttu-id="ee50e-246">**Entitat d'exportació de despeses del projecte d'integració del Project Operations (msdyn\_expenses)**</span><span class="sxs-lookup"><span data-stu-id="ee50e-246">**Project Operations integration project expenses export entity (msdyn\_expenses)**</span></span> | <span data-ttu-id="ee50e-247">Sí</span><span class="sxs-lookup"><span data-stu-id="ee50e-247">Yes</span></span> | <span data-ttu-id="ee50e-248">No</span><span class="sxs-lookup"><span data-stu-id="ee50e-248">No</span></span> | <span data-ttu-id="ee50e-249">N/D</span><span class="sxs-lookup"><span data-stu-id="ee50e-249">N\A</span></span> | <span data-ttu-id="ee50e-250">No</span><span class="sxs-lookup"><span data-stu-id="ee50e-250">No</span></span> | <span data-ttu-id="ee50e-251">N/D</span><span class="sxs-lookup"><span data-stu-id="ee50e-251">N\A</span></span> |
| <span data-ttu-id="ee50e-252">**Entitat d'integració del Project Operations per a l'estimació d'hores (msdyn\_resourceassignments)**</span><span class="sxs-lookup"><span data-stu-id="ee50e-252">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="ee50e-253">Sí</span><span class="sxs-lookup"><span data-stu-id="ee50e-253">Yes</span></span> | <span data-ttu-id="ee50e-254">No</span><span class="sxs-lookup"><span data-stu-id="ee50e-254">No</span></span> | <span data-ttu-id="ee50e-255">N/D</span><span class="sxs-lookup"><span data-stu-id="ee50e-255">N\A</span></span> | <span data-ttu-id="ee50e-256">No</span><span class="sxs-lookup"><span data-stu-id="ee50e-256">No</span></span> | <span data-ttu-id="ee50e-257">N/D</span><span class="sxs-lookup"><span data-stu-id="ee50e-257">N\A</span></span> |


4. <span data-ttu-id="ee50e-258">Per actualitzar l'entitat, seleccioneu el nom de l'assignació i, a continuació, **Actualitza les entitats**.</span><span class="sxs-lookup"><span data-stu-id="ee50e-258">To refresh the entity, select the map name, and then select **Refresh entities**.</span></span> 


![Actualitzar l'assignació](./media/20RefreshMapping.png)

5. <span data-ttu-id="ee50e-260">Després de completar l'actualització, executeu l'assignació.</span><span class="sxs-lookup"><span data-stu-id="ee50e-260">After the refresh is complete, run the map.</span></span> <span data-ttu-id="ee50e-261">Abans d'habilitar la següent assignació, verifiqueu que l'assignació de la taula estigui en estat **En execució**.</span><span class="sxs-lookup"><span data-stu-id="ee50e-261">Before you enable the next map, verify that the map in the table is in a state of **Running**.</span></span> <span data-ttu-id="ee50e-262">L'execució d'assignacions amb un major nombre de requisits previs podria tardar una estona.</span><span class="sxs-lookup"><span data-stu-id="ee50e-262">Running maps with a larger number of prerequisites might take some time.</span></span>

<span data-ttu-id="ee50e-263">Per executar una assignació amb requisits previs, habiliteu l'opció **Mostra les assignacions d'entitats relacionades**.</span><span class="sxs-lookup"><span data-stu-id="ee50e-263">To run a map with prerequisites, enable the **Show related entity maps** toggle.</span></span> <span data-ttu-id="ee50e-264">Si la taula indica que la **Sincronització inicial de requisits previs** és **No**, verifiqueu que l'indicador **Sincronització inicial** estigui **desactivat** a totes les assignacions de requisits previs abans d'executar-la.</span><span class="sxs-lookup"><span data-stu-id="ee50e-264">If the table indicates **Prerequisite initial sync** is **No**, verify that the **Initial sync** flag is **Off** in all the prerequisite maps before you run it.</span></span>

![Executar l'assignació](./media/21RunMap.png)

6. <span data-ttu-id="ee50e-266">Valideu que totes les assignacions relacionades del projecte estiguin en execució.</span><span class="sxs-lookup"><span data-stu-id="ee50e-266">Validate all project related maps are in the running state.</span></span>

![Totes les assignacions en execució](./media/22AllMapsRunning.png)


## <a name="apply-configuration-data-in-cds-for-project-operations-optional"></a><span data-ttu-id="ee50e-268">Aplicació de les dades de configuració al CDS per al Project Operations (opcional)</span><span class="sxs-lookup"><span data-stu-id="ee50e-268">Apply configuration data in CDS for Project Operations (optional)</span></span>

<span data-ttu-id="ee50e-269">Si heu aplicat dades de demostració a l'entorn del Finance, vegeu [Configurar i aplicar dades de configuració al Common Data Service per al Project Operations](resource-apply-pro-setup-config-data.md) per aplicar dades de demostració a l'entorn del CDS.</span><span class="sxs-lookup"><span data-stu-id="ee50e-269">If you have applied demo data to the Finance environment, see [Set up and apply configuration data in the Common Data Service for Project Operations](resource-apply-pro-setup-config-data.md) to apply demo data to CDS environment.</span></span>


<span data-ttu-id="ee50e-270">L'entorn del Project Operations ja està proveït i configurat.</span><span class="sxs-lookup"><span data-stu-id="ee50e-270">Your Project Operations environment is now provisioned and configured.</span></span> 
