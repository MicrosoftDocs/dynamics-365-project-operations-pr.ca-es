---
title: Proveïment d'un entorn nou
description: En aquest tema s'ofereix informació sobre com proveir un entorn nou del Project Operations.
author: sigitac
manager: Annbe
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 9ee9e4c31d1972e3a75ad214071b31527f0ca826
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950522"
---
# <a name="provision-a-new-environment"></a><span data-ttu-id="c2dc3-103">Proveïment d'un entorn nou</span><span class="sxs-lookup"><span data-stu-id="c2dc3-103">Provision a new environment</span></span>

<span data-ttu-id="c2dc3-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_</span><span class="sxs-lookup"><span data-stu-id="c2dc3-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="c2dc3-105">En aquest tema es proporciona informació sobre com proveir un nou entorn de Dynamics 365 Project Operations per a escenaris basats en recursos/sense existències.</span><span class="sxs-lookup"><span data-stu-id="c2dc3-105">This topic provides information about how to provision a new Dynamics 365 Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a><span data-ttu-id="c2dc3-106">Habilitar el proveïment automatitzat del Project Operations en un projecte del LCS</span><span class="sxs-lookup"><span data-stu-id="c2dc3-106">Enable Project Operations automated provisioning in an LCS project</span></span>

<span data-ttu-id="c2dc3-107">Seguiu aquests passos per habilitar el flux de proveïment automatitzat del Project Operations per al projecte del LCS.</span><span class="sxs-lookup"><span data-stu-id="c2dc3-107">Use following steps to enable the Project Operations automated provisioning flow for your LCS project.</span></span>

1. <span data-ttu-id="c2dc3-108">Aneu a [LCS](https://lcs.dynamics.com/v2) i seleccioneu la peça **Administració de característiques de versió preliminar**.</span><span class="sxs-lookup"><span data-stu-id="c2dc3-108">Go to [LCS](https://lcs.dynamics.com/v2) and select the **Preview Feature management** tile.</span></span>
2. <span data-ttu-id="c2dc3-109">A la llista **Característiques de versió preliminar**, seleccioneu **Característica del Project Operations** i **Característica de versió preliminar habilitada** per habilitar el Project Operations.</span><span class="sxs-lookup"><span data-stu-id="c2dc3-109">In the **Preview feature** list, select **Project Operations Feature**, and then select **Preview feature enabled** to enable Project Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="c2dc3-110">Aquest pas només es fa una vegada per projecte del LCS.</span><span class="sxs-lookup"><span data-stu-id="c2dc3-110">This step is performed only one time per LCS project.</span></span>

## <a name="provision-a-project-operations-environment"></a><span data-ttu-id="c2dc3-111">Proveïment d'un entorn del Project Operations</span><span class="sxs-lookup"><span data-stu-id="c2dc3-111">Provision a Project Operations environment</span></span>

1. <span data-ttu-id="c2dc3-112">Obriu una nova implementació d'un [entorn de demostració](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) o [entorn de producció](/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) del Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="c2dc3-112">Open a new Dynamics 365 Finance [demo environment](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) or [sandbox/ production environment](/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) deployment.</span></span> 
2. <span data-ttu-id="c2dc3-113">Seguiu els passos de l'auxiliar **Proveïment de l'entorn**.</span><span class="sxs-lookup"><span data-stu-id="c2dc3-113">Walk through the **Environment provisioning** wizard.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="c2dc3-114">Assegureu-vos que la versió de l'aplicació seleccionada sigui 10.0.13 o superior.</span><span class="sxs-lookup"><span data-stu-id="c2dc3-114">Make sure selected application version is 10.0.13 or higher.</span></span>

3. <span data-ttu-id="c2dc3-115">Per proveir el Project Operations, a **Configuració avançada**, seleccioneu **Common Data Service**.</span><span class="sxs-lookup"><span data-stu-id="c2dc3-115">To provision Project Operations, under **Advance settings**, select **Common Data Service**.</span></span> 
4. <span data-ttu-id="c2dc3-116">Habiliteu la **Configuració del Common Data Service** seleccionant **Sí** i, a continuació, introduïu informació als camps obligatoris:</span><span class="sxs-lookup"><span data-stu-id="c2dc3-116">Enable the **Common Data Service Setting** by selecting **Yes** and then enter information in the required fields:</span></span>

  - <span data-ttu-id="c2dc3-117">Nom</span><span class="sxs-lookup"><span data-stu-id="c2dc3-117">Name</span></span>
  - <span data-ttu-id="c2dc3-118">Regió</span><span class="sxs-lookup"><span data-stu-id="c2dc3-118">Region</span></span>
  - <span data-ttu-id="c2dc3-119">Language</span><span class="sxs-lookup"><span data-stu-id="c2dc3-119">Language</span></span>
  - <span data-ttu-id="c2dc3-120">Moneda</span><span class="sxs-lookup"><span data-stu-id="c2dc3-120">Currency</span></span>
 
5. <span data-ttu-id="c2dc3-121">Al camp **Plantilla del Common Data Service**, seleccioneu **Project Operations**</span><span class="sxs-lookup"><span data-stu-id="c2dc3-121">In the **Common Data Service Template** field, select **Project Operations**</span></span> 

6. <span data-ttu-id="c2dc3-122">Seleccioneu el tipus d'entorn per a la implementació.</span><span class="sxs-lookup"><span data-stu-id="c2dc3-122">Select the environment type for your deployment.</span></span> <span data-ttu-id="c2dc3-123">Una prova basada en subscripció us permetrà implementar un entorn del CDS durant 30 dies.</span><span class="sxs-lookup"><span data-stu-id="c2dc3-123">A subscription-based trial will let you deploy a CDS environment for 30 days.</span></span> 

![Configuració de la implementació](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> <span data-ttu-id="c2dc3-125">Seleccioneu **Accepto** per reconèixer les condicions del servei i, a continuació, seleccioneu **Fet** per tornar a la configuració de la implementació.</span><span class="sxs-lookup"><span data-stu-id="c2dc3-125">Select **Agree** to acknowledge the terms of service and then select **Done** to return to the deployment settings.</span></span>

![Consentiment de la implementació](./media/2DeploymentConsent.png)

7. <span data-ttu-id="c2dc3-127">Opcional: aplicar dades de demostració a l'entorn.</span><span class="sxs-lookup"><span data-stu-id="c2dc3-127">Optional - Apply demo data to the environment.</span></span> <span data-ttu-id="c2dc3-128">Aneu a **Configuració avançada**, seleccioneu **Personalitza la configuració de la base de dades SQL** i definiu **Especifica un conjunt de dades per a la base de dades d'aplicacions** a **Demostració**.</span><span class="sxs-lookup"><span data-stu-id="c2dc3-128">Go to **Advanced settings**, select **Customize SQL Database Configuration**, and set **Specify a dataset for Application database** to **Demo**.</span></span>

8. <span data-ttu-id="c2dc3-129">Completeu els camps obligatoris restants a l'auxiliar i confirmeu la implementació.</span><span class="sxs-lookup"><span data-stu-id="c2dc3-129">Complete the remaining required fields in the wizard and confirm the deployment.</span></span> <span data-ttu-id="c2dc3-130">El temps de proveïment de l'entorn varia segons el tipus d'entorn.</span><span class="sxs-lookup"><span data-stu-id="c2dc3-130">The time to provision the environment varies based on the environment type.</span></span> <span data-ttu-id="c2dc3-131">El proveïment pot tardar fins a sis hores.</span><span class="sxs-lookup"><span data-stu-id="c2dc3-131">Provisioning might take up to six hours.</span></span>

  <span data-ttu-id="c2dc3-132">Quan la implementació es completi correctament, l'entorn es mostrarà com a **Implementat**.</span><span class="sxs-lookup"><span data-stu-id="c2dc3-132">After the deployment completes successfully, the environment will show as **Deployed**.</span></span>

9. <span data-ttu-id="c2dc3-133">Per confirmar que l'entorn s'ha implementat correctament, seleccioneu **Inicia la sessió** i inicieu la sessió a l'entorn per confirmar-ho.</span><span class="sxs-lookup"><span data-stu-id="c2dc3-133">To confirm that the environment has deployed successfully, select **Login** and log on to the environment to confirm.</span></span>

![Detalls de l'entorn del ](./media/3EnvironmentDetails.png)

## <a name="apply-updates-to-the-finance-environment"></a><span data-ttu-id="c2dc3-135">Aplicar les actualitzacions a l'entorn del Finance</span><span class="sxs-lookup"><span data-stu-id="c2dc3-135">Apply updates to the Finance environment</span></span>

<span data-ttu-id="c2dc3-136">El Project Operations requereix un entorn del Finance amb la versió de l'aplicació **10.0.13 (10.0.569.20009)** o superior.</span><span class="sxs-lookup"><span data-stu-id="c2dc3-136">Project Operations requires a Finance environment with application version **10.0.13 (10.0.569.20009)** or higher.</span></span>

<span data-ttu-id="c2dc3-137">Pot ser que hàgiu d'aplicar actualitzacions de qualitat al vostre entorn del Finance per rebre aquesta versió.</span><span class="sxs-lookup"><span data-stu-id="c2dc3-137">You might need to apply quality updates to your Finance environment to receive this version.</span></span>

1. <span data-ttu-id="c2dc3-138">Al LCS, a la pàgina **Detalls de l'entorn**, a la secció **Actualitzacions disponibles**, seleccioneu **Visualitza l'actualització**.</span><span class="sxs-lookup"><span data-stu-id="c2dc3-138">In LCS, on the **Environment details** page, in the **Available Updates** section, select **View Update**.</span></span>

![Visualitzar les actualitzacions](./media/5ViewUpdates.png)

2. <span data-ttu-id="c2dc3-140">A la pàgina **Actualitzacions binàries**, seleccioneu **Desa el paquet.**</span><span class="sxs-lookup"><span data-stu-id="c2dc3-140">On the **Binary updates** page, select **Save package.**</span></span>

![Desar el paquet](./media/6SavePackage.png)

3. <span data-ttu-id="c2dc3-142">Feu clic a **Selecciona-ho tot** i seleccioneu **Desa el paquet**.</span><span class="sxs-lookup"><span data-stu-id="c2dc3-142">Click **Select all** and then select **Save package**.</span></span>

![Revisar i desar les actualitzacions](./media/7ReviewAndSaveUpdates.png)

4. <span data-ttu-id="c2dc3-144">Introduïu un nom i una descripció del paquet i, a continuació, seleccioneu **Desa**.</span><span class="sxs-lookup"><span data-stu-id="c2dc3-144">Enter a name and a description of the package, and then select **Save**.</span></span> <span data-ttu-id="c2dc3-145">En funció de la connexió a Internet, pot ser que aquest procés tardi una estona.</span><span class="sxs-lookup"><span data-stu-id="c2dc3-145">Depending on the internet connection, this process might take some time.</span></span>

![Carregar el paquet a la biblioteca d'actius](./media/8UploadPackageToAssetsLibrary.png)

5. <span data-ttu-id="c2dc3-147">Un cop desat el paquet, seleccioneu **Fer** i deseu aquest paquet a la biblioteca d'actius del projecte del LCS.</span><span class="sxs-lookup"><span data-stu-id="c2dc3-147">After the package is saved, select **Done** and save this package to the Assets library in your LCS project.</span></span>

<span data-ttu-id="c2dc3-148">El desament i la validació del paquet poden tardar uns 15 minuts.</span><span class="sxs-lookup"><span data-stu-id="c2dc3-148">Saving and validating the package might take ~15 minutes.</span></span>

6. <span data-ttu-id="c2dc3-149">Per aplicar l'actualització, aneu a la pàgina **Detalls de l'entorn** del LCS i seleccioneu **Mantén** > **Aplica les actualitzacions**.</span><span class="sxs-lookup"><span data-stu-id="c2dc3-149">To apply the update, navigate to the **Environment details** page in LCS and select **Maintain** > **Apply updates**.</span></span>

![Mantenir els entorns](./media/9MaintainEnvironment.png)

7. <span data-ttu-id="c2dc3-151">A la llista actualitzacions, seleccioneu el paquet que heu creat i seleccioneu **Aplica**.</span><span class="sxs-lookup"><span data-stu-id="c2dc3-151">In the updates list select the package you created, and select **Apply**.</span></span>

![Aplicar les actualitzacions](./media/10ApplyUpdates.png)

<span data-ttu-id="c2dc3-153">El procés de servei de l'entorn tardarà una estona.</span><span class="sxs-lookup"><span data-stu-id="c2dc3-153">Environment servicing will take some time.</span></span> <span data-ttu-id="c2dc3-154">Després d'haver acabat, l'entorn tornarà a un estat implementat.</span><span class="sxs-lookup"><span data-stu-id="c2dc3-154">After it is complete, the environment will return to a deployed state.</span></span>

![Entorn implementat](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a><span data-ttu-id="c2dc3-156">Establir una connexió d'escriptura doble</span><span class="sxs-lookup"><span data-stu-id="c2dc3-156">Establish a Dual Write connection</span></span> 

1. <span data-ttu-id="c2dc3-157">Al projecte del LCS, aneu a la pàgina **Detalls de l'entorn**.</span><span class="sxs-lookup"><span data-stu-id="c2dc3-157">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="c2dc3-158">A **Informació de l'entorn del Common Data Service**, seleccioneu **Enllaça amb el CDS per a aplicacions**.</span><span class="sxs-lookup"><span data-stu-id="c2dc3-158">Under **Common Data Service Environment Information**, select **Link to CDS for Apps**.</span></span>
3. <span data-ttu-id="c2dc3-159">Després d'haver acabat l'enllaç, torneu a seleccionar **Enllaça amb el CDS per a aplicacions**.</span><span class="sxs-lookup"><span data-stu-id="c2dc3-159">After the link is complete, select **Link to CDS for Apps** again.</span></span> <span data-ttu-id="c2dc3-160">Se us redirigirà a l'escriptura doble al Finance.</span><span class="sxs-lookup"><span data-stu-id="c2dc3-160">You will be redirected to Dual Write in Finance.</span></span>

![Enllaça amb el CDS](./media/12LinktoCDS.png)

4. <span data-ttu-id="c2dc3-162">Seleccioneu **Aplica la solució** per accedir a les entitats que s'assignaran a la integració.</span><span class="sxs-lookup"><span data-stu-id="c2dc3-162">Select **Apply Solution** to access the entities that will be mapped in the integration.</span></span>

![Aplicar les solucions](./media/13ApplySolutions.png)

5. <span data-ttu-id="c2dc3-164">Seleccioneu les dues solucions, el mapa d'entitats del **Dynamics 365 Finance and Operations d'escriptura doble** i els mapes d'entitat del **Dynamics 365 Project Operations d'escriptura doble** i, a continuació, seleccioneu **Aplicar**.</span><span class="sxs-lookup"><span data-stu-id="c2dc3-164">Select both solutions, **Dynamics 365 Finance and Operations Dual Write Entity Map** and **Dynamics 365 Project Operations Dual Write Entity Maps**, and then select **Apply**.</span></span>

![Confirmar les solucions](./media/14ConfirmSolutions.png)

<span data-ttu-id="c2dc3-166">Després de l'aplicació de les solucions, les entitats d'escriptura doble s'apliquen a l'entorn.</span><span class="sxs-lookup"><span data-stu-id="c2dc3-166">After the solutions are applied, the Dual Write entities are applied to the environment.</span></span>

![Aplicar les solucions](./media/15ApplyingSolutions.png)

<span data-ttu-id="c2dc3-168">Després d'aplicar les entitats, totes les assignacions disponibles apareixen a la llista de l'entorn.</span><span class="sxs-lookup"><span data-stu-id="c2dc3-168">After the entities are applied, all available mappings are listed in the environment.</span></span>

![Assignacions d'escriptura doble](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a><span data-ttu-id="c2dc3-170">Actualitzar les entitats de dades després de l'actualització</span><span class="sxs-lookup"><span data-stu-id="c2dc3-170">Refresh the data entities after the update</span></span>

1. <span data-ttu-id="c2dc3-171">Al Finance, aneu a l'àrea de treball **Administració de dades**.</span><span class="sxs-lookup"><span data-stu-id="c2dc3-171">In Finance, go to the **Data management** workspace.</span></span>

![Espai de treball d'administració de dades](./media/16DataManagement.png)

2. <span data-ttu-id="c2dc3-173">Seleccioneu la peça **Paràmetres del marc**.</span><span class="sxs-lookup"><span data-stu-id="c2dc3-173">Select the **Framework parameters** tile.</span></span>

![Paràmetres del marc](./media/17FrameworkParameters.png)

3. <span data-ttu-id="c2dc3-175">A la pàgina **Configuració de l'entitat**, seleccioneu **Actualitza la llista d'entitats**.</span><span class="sxs-lookup"><span data-stu-id="c2dc3-175">On the **Entity settings** page, select **Refresh Entity list**.</span></span>

![Actualitzar la llista d'entitats](./media/18RefreshEntityList.png)

<span data-ttu-id="c2dc3-177">L'actualització tardarà uns 20 minuts.</span><span class="sxs-lookup"><span data-stu-id="c2dc3-177">The refresh is going to take approximately 20 minutes.</span></span> <span data-ttu-id="c2dc3-178">Rebreu una alerta quan s'hagi completat.</span><span class="sxs-lookup"><span data-stu-id="c2dc3-178">You will receive an alert when it is complete.</span></span>

![Confirmació d'actualització](./media/19RefreshConfirmation.png)

## <a name="update-security-settings-on-project-operations-on-dataverse"></a><span data-ttu-id="c2dc3-180">Actualitzar la configuració de seguretat del Project Operations al Dataverse</span><span class="sxs-lookup"><span data-stu-id="c2dc3-180">Update security settings on Project Operations on Dataverse</span></span>

1. <span data-ttu-id="c2dc3-181">Aneu al Project Operations del vostre entorn del Dataverse.</span><span class="sxs-lookup"><span data-stu-id="c2dc3-181">Go to Project Operations on your Dataverse environment.</span></span> 
2. <span data-ttu-id="c2dc3-182">Aneu a **Configuració** > **Seguretat** > **Funcions de seguretat**.</span><span class="sxs-lookup"><span data-stu-id="c2dc3-182">Go to **Settings** > **Security** > **Security roles**.</span></span> 
3. <span data-ttu-id="c2dc3-183">A la pàgina **Funcions de seguretat**, a la llista de funcions, seleccioneu **usuari de l'aplicació de doble escriptura** i seleccioneu la pestanya **Entitats personalitzades**.</span><span class="sxs-lookup"><span data-stu-id="c2dc3-183">On the **Security roles** page, in the list of roles, select **dual-write app user** and select the **Custom Entities** tab.</span></span>  
4. <span data-ttu-id="c2dc3-184">Verifiqueu que la funció té permisos de **Lectura** i **Annexa a** per a:</span><span class="sxs-lookup"><span data-stu-id="c2dc3-184">Verify that the role has **Read** and **Append To** permissions for the:</span></span>
      
      - <span data-ttu-id="c2dc3-185">**Tipus de canvi de moneda**</span><span class="sxs-lookup"><span data-stu-id="c2dc3-185">**Currency Exchange Rate Type**</span></span>
      - <span data-ttu-id="c2dc3-186">**Taula de comptes**</span><span class="sxs-lookup"><span data-stu-id="c2dc3-186">**Chart Of Accounts**</span></span>
      - <span data-ttu-id="c2dc3-187">**Calendari fiscal**</span><span class="sxs-lookup"><span data-stu-id="c2dc3-187">**Fiscal Calendar**</span></span>
      - <span data-ttu-id="c2dc3-188">**Llibre major**</span><span class="sxs-lookup"><span data-stu-id="c2dc3-188">**Ledger**</span></span>

5. <span data-ttu-id="c2dc3-189">Quan la funció de seguretat s'actualitzi, aneu a **Configuració** > **Seguretat** > **Equips** i seleccioneu l'equip per defecte a la visualització d'equips **Propietari de l'empresa local**.</span><span class="sxs-lookup"><span data-stu-id="c2dc3-189">After the security role is updated, go to **Settings** > **Security** > **Teams**, and select the default team in the **Local Business Owner** team view.</span></span>
6. <span data-ttu-id="c2dc3-190">Seleccioneu **Administra les funcions** i verifiqueu que s'aplica el privilegi de seguretat **usuari de l'aplicació de doble escriptura** a aquest equip.</span><span class="sxs-lookup"><span data-stu-id="c2dc3-190">Select **Manage Roles** and verify that the **dual-write app user** security privilege is applied to this team.</span></span>

## <a name="run-project-operations-dual-write-maps"></a><span data-ttu-id="c2dc3-191">Executar assignacions d'escriptura doble del Project Operations</span><span class="sxs-lookup"><span data-stu-id="c2dc3-191">Run Project Operations Dual Write maps</span></span>

1. <span data-ttu-id="c2dc3-192">Al projecte del LCS, aneu a la pàgina **Detalls de l'entorn**.</span><span class="sxs-lookup"><span data-stu-id="c2dc3-192">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="c2dc3-193">A **Informació de l'entorn del Common Data Service**, seleccioneu **Enllaça amb el CDS per a aplicacions.**</span><span class="sxs-lookup"><span data-stu-id="c2dc3-193">Under **Common Data Service Environment Information**, select **Link to CDS for Apps.**</span></span> <span data-ttu-id="c2dc3-194">Després de seleccionar l'enllaç, se us redirigirà a la llista d'entitats de les assignacions.</span><span class="sxs-lookup"><span data-stu-id="c2dc3-194">After you select the link, you will be redirected to the list of entities in the mappings.</span></span>
3. <span data-ttu-id="c2dc3-195">Inicieu les assignacions com es descriu a la taula següent.</span><span class="sxs-lookup"><span data-stu-id="c2dc3-195">Start the maps as described in the following table.</span></span> <span data-ttu-id="c2dc3-196">Assegureu-vos de seguir la seqüència que s'indica a la llista.</span><span class="sxs-lookup"><span data-stu-id="c2dc3-196">Make sure to follow the sequence as listed.</span></span>

| <span data-ttu-id="c2dc3-197">**Assignació d'entitats**</span><span class="sxs-lookup"><span data-stu-id="c2dc3-197">**Entity Map**</span></span> | <span data-ttu-id="c2dc3-198">**Actualitzar l'entitat**</span><span class="sxs-lookup"><span data-stu-id="c2dc3-198">**Refresh entity**</span></span> | <span data-ttu-id="c2dc3-199">**Sincronització inicial**</span><span class="sxs-lookup"><span data-stu-id="c2dc3-199">**Initial sync**</span></span> | <span data-ttu-id="c2dc3-200">**Mestre per a la sincronització inicial**</span><span class="sxs-lookup"><span data-stu-id="c2dc3-200">**Master for initial sync**</span></span> | <span data-ttu-id="c2dc3-201">**Requisits previs de l'execució**</span><span class="sxs-lookup"><span data-stu-id="c2dc3-201">**Run prerequisites**</span></span> | <span data-ttu-id="c2dc3-202">**Sincronització inicial dels requisits previs**</span><span class="sxs-lookup"><span data-stu-id="c2dc3-202">**Prerequisites initial sync**</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="c2dc3-203">**Funcions de recurs del projecte per a totes les empreses (bookableresourcecategories)**</span><span class="sxs-lookup"><span data-stu-id="c2dc3-203">**Project Resource Roles for All Companies (bookableresourcecategories)**</span></span> | <span data-ttu-id="c2dc3-204">No</span><span class="sxs-lookup"><span data-stu-id="c2dc3-204">No</span></span> | <span data-ttu-id="c2dc3-205">Sí</span><span class="sxs-lookup"><span data-stu-id="c2dc3-205">Yes</span></span> | <span data-ttu-id="c2dc3-206">Common Data Service</span><span class="sxs-lookup"><span data-stu-id="c2dc3-206">Common Data Service</span></span> | <span data-ttu-id="c2dc3-207">No</span><span class="sxs-lookup"><span data-stu-id="c2dc3-207">No</span></span> | <span data-ttu-id="c2dc3-208">N/D</span><span class="sxs-lookup"><span data-stu-id="c2dc3-208">N\A</span></span> |
| <span data-ttu-id="c2dc3-209">**Entitats jurídiques (cdm\_companies)**</span><span class="sxs-lookup"><span data-stu-id="c2dc3-209">**Legal entities (cdm\_companies)**</span></span> | <span data-ttu-id="c2dc3-210">No</span><span class="sxs-lookup"><span data-stu-id="c2dc3-210">No</span></span> | <span data-ttu-id="c2dc3-211">Sí</span><span class="sxs-lookup"><span data-stu-id="c2dc3-211">Yes</span></span> | <span data-ttu-id="c2dc3-212">Aplicacions del Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c2dc3-212">Finance and Operations apps</span></span> | <span data-ttu-id="c2dc3-213">No</span><span class="sxs-lookup"><span data-stu-id="c2dc3-213">No</span></span> | <span data-ttu-id="c2dc3-214">N/D</span><span class="sxs-lookup"><span data-stu-id="c2dc3-214">N\A</span></span> |
| <span data-ttu-id="c2dc3-215">**Llibre major (msdyn_ledgers)**</span><span class="sxs-lookup"><span data-stu-id="c2dc3-215">**Ledger (msdyn_ledgers)**</span></span> | <span data-ttu-id="c2dc3-216">No</span><span class="sxs-lookup"><span data-stu-id="c2dc3-216">No</span></span> | <span data-ttu-id="c2dc3-217">Sí</span><span class="sxs-lookup"><span data-stu-id="c2dc3-217">Yes</span></span> | <span data-ttu-id="c2dc3-218">Aplicacions del Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c2dc3-218">Finance and Operations apps</span></span> | <span data-ttu-id="c2dc3-219">Sí</span><span class="sxs-lookup"><span data-stu-id="c2dc3-219">Yes</span></span> | <span data-ttu-id="c2dc3-220">Sí, les aplicacions de Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c2dc3-220">Yes, Finance and Operations apps</span></span> |
| <span data-ttu-id="c2dc3-221">**Valors reals d'integració del Project Operations (msdyn\_actuals)**</span><span class="sxs-lookup"><span data-stu-id="c2dc3-221">**Project Operations integration actuals (msdyn\_actuals)**</span></span> | <span data-ttu-id="c2dc3-222">No</span><span class="sxs-lookup"><span data-stu-id="c2dc3-222">No</span></span> | <span data-ttu-id="c2dc3-223">No</span><span class="sxs-lookup"><span data-stu-id="c2dc3-223">No</span></span> | <span data-ttu-id="c2dc3-224">N/D</span><span class="sxs-lookup"><span data-stu-id="c2dc3-224">N\A</span></span> | <span data-ttu-id="c2dc3-225">Sí</span><span class="sxs-lookup"><span data-stu-id="c2dc3-225">Yes</span></span> | <span data-ttu-id="c2dc3-226">No</span><span class="sxs-lookup"><span data-stu-id="c2dc3-226">No</span></span> |
| <span data-ttu-id="c2dc3-227">**Línies de contracte del projecte (salesorderdetails)**</span><span class="sxs-lookup"><span data-stu-id="c2dc3-227">**Project contract lines (salesorderdetails)**</span></span> | <span data-ttu-id="c2dc3-228">No</span><span class="sxs-lookup"><span data-stu-id="c2dc3-228">No</span></span> | <span data-ttu-id="c2dc3-229">No</span><span class="sxs-lookup"><span data-stu-id="c2dc3-229">No</span></span> | <span data-ttu-id="c2dc3-230">N/D</span><span class="sxs-lookup"><span data-stu-id="c2dc3-230">N\A</span></span> | <span data-ttu-id="c2dc3-231">No</span><span class="sxs-lookup"><span data-stu-id="c2dc3-231">No</span></span> | <span data-ttu-id="c2dc3-232">No</span><span class="sxs-lookup"><span data-stu-id="c2dc3-232">No</span></span> |
| <span data-ttu-id="c2dc3-233">**Entitat d'integració per a les relacions de transaccions del projecte (msdyn\_transactionconnections)**</span><span class="sxs-lookup"><span data-stu-id="c2dc3-233">**Integration entity for project transaction relationships (msdyn\_transactionconnections)**</span></span> | <span data-ttu-id="c2dc3-234">No</span><span class="sxs-lookup"><span data-stu-id="c2dc3-234">No</span></span> | <span data-ttu-id="c2dc3-235">No</span><span class="sxs-lookup"><span data-stu-id="c2dc3-235">No</span></span> | <span data-ttu-id="c2dc3-236">N/D</span><span class="sxs-lookup"><span data-stu-id="c2dc3-236">N\A</span></span> | <span data-ttu-id="c2dc3-237">No</span><span class="sxs-lookup"><span data-stu-id="c2dc3-237">No</span></span> | <span data-ttu-id="c2dc3-238">N/D</span><span class="sxs-lookup"><span data-stu-id="c2dc3-238">N\A</span></span> |
| <span data-ttu-id="c2dc3-239">**Fites de línia de contracte d'integració del Project Operations (msdyn\_contractlinesscheduleofvalues)**</span><span class="sxs-lookup"><span data-stu-id="c2dc3-239">**Project Operations integration contract line milestones (msdyn\_contractlinesscheduleofvalues)**</span></span> | <span data-ttu-id="c2dc3-240">No</span><span class="sxs-lookup"><span data-stu-id="c2dc3-240">No</span></span> | <span data-ttu-id="c2dc3-241">No</span><span class="sxs-lookup"><span data-stu-id="c2dc3-241">No</span></span> | <span data-ttu-id="c2dc3-242">N/D</span><span class="sxs-lookup"><span data-stu-id="c2dc3-242">N\A</span></span> | <span data-ttu-id="c2dc3-243">No</span><span class="sxs-lookup"><span data-stu-id="c2dc3-243">No</span></span> | <span data-ttu-id="c2dc3-244">N/D</span><span class="sxs-lookup"><span data-stu-id="c2dc3-244">N\A</span></span> |
| <span data-ttu-id="c2dc3-245">**Entitat d'integració del Project Operations per a l'estimació de despeses (msdyn\_estimateslines)**</span><span class="sxs-lookup"><span data-stu-id="c2dc3-245">**Project Operations integration entity for expense estimates (msdyn\_estimateslines)**</span></span> | <span data-ttu-id="c2dc3-246">No</span><span class="sxs-lookup"><span data-stu-id="c2dc3-246">No</span></span> | <span data-ttu-id="c2dc3-247">No</span><span class="sxs-lookup"><span data-stu-id="c2dc3-247">No</span></span> | <span data-ttu-id="c2dc3-248">N/D</span><span class="sxs-lookup"><span data-stu-id="c2dc3-248">N\A</span></span> | <span data-ttu-id="c2dc3-249">No</span><span class="sxs-lookup"><span data-stu-id="c2dc3-249">No</span></span> | <span data-ttu-id="c2dc3-250">N/D</span><span class="sxs-lookup"><span data-stu-id="c2dc3-250">N\A</span></span> |
| <span data-ttu-id="c2dc3-251">**Entitat d'exportació de categories de despeses del projecte d'integració del Project Operations (msdyn\_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="c2dc3-251">**Project Operations integration project expense categories export entity (msdyn\_expensecategories)**</span></span> | <span data-ttu-id="c2dc3-252">No</span><span class="sxs-lookup"><span data-stu-id="c2dc3-252">No</span></span> | <span data-ttu-id="c2dc3-253">No</span><span class="sxs-lookup"><span data-stu-id="c2dc3-253">No</span></span> | <span data-ttu-id="c2dc3-254">N/D</span><span class="sxs-lookup"><span data-stu-id="c2dc3-254">N\A</span></span> | <span data-ttu-id="c2dc3-255">No</span><span class="sxs-lookup"><span data-stu-id="c2dc3-255">No</span></span> | <span data-ttu-id="c2dc3-256">N/D</span><span class="sxs-lookup"><span data-stu-id="c2dc3-256">N\A</span></span> |
| <span data-ttu-id="c2dc3-257">**Entitat d'exportació de despeses del projecte d'integració del Project Operations (msdyn\_expenses)**</span><span class="sxs-lookup"><span data-stu-id="c2dc3-257">**Project Operations integration project expenses export entity (msdyn\_expenses)**</span></span> | <span data-ttu-id="c2dc3-258">Sí</span><span class="sxs-lookup"><span data-stu-id="c2dc3-258">Yes</span></span> | <span data-ttu-id="c2dc3-259">No</span><span class="sxs-lookup"><span data-stu-id="c2dc3-259">No</span></span> | <span data-ttu-id="c2dc3-260">N/D</span><span class="sxs-lookup"><span data-stu-id="c2dc3-260">N\A</span></span> | <span data-ttu-id="c2dc3-261">No</span><span class="sxs-lookup"><span data-stu-id="c2dc3-261">No</span></span> | <span data-ttu-id="c2dc3-262">N/D</span><span class="sxs-lookup"><span data-stu-id="c2dc3-262">N\A</span></span> |
| <span data-ttu-id="c2dc3-263">**Entitat d'integració del Project Operations per a l'estimació d'hores (msdyn\_resourceassignments)**</span><span class="sxs-lookup"><span data-stu-id="c2dc3-263">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="c2dc3-264">Sí</span><span class="sxs-lookup"><span data-stu-id="c2dc3-264">Yes</span></span> | <span data-ttu-id="c2dc3-265">No</span><span class="sxs-lookup"><span data-stu-id="c2dc3-265">No</span></span> | <span data-ttu-id="c2dc3-266">N/D</span><span class="sxs-lookup"><span data-stu-id="c2dc3-266">N\A</span></span> | <span data-ttu-id="c2dc3-267">No</span><span class="sxs-lookup"><span data-stu-id="c2dc3-267">No</span></span> | <span data-ttu-id="c2dc3-268">N/D</span><span class="sxs-lookup"><span data-stu-id="c2dc3-268">N\A</span></span> |


4. <span data-ttu-id="c2dc3-269">Per actualitzar l'entitat, seleccioneu el nom de l'assignació i, a continuació, **Actualitza les entitats**.</span><span class="sxs-lookup"><span data-stu-id="c2dc3-269">To refresh the entity, select the map name, and then select **Refresh entities**.</span></span> 


![Actualitzar l'assignació](./media/20RefreshMapping.png)

5. <span data-ttu-id="c2dc3-271">Després de completar l'actualització, executeu l'assignació.</span><span class="sxs-lookup"><span data-stu-id="c2dc3-271">After the refresh is complete, run the map.</span></span> <span data-ttu-id="c2dc3-272">Abans d'habilitar la següent assignació, verifiqueu que l'assignació de la taula estigui en estat **En execució**.</span><span class="sxs-lookup"><span data-stu-id="c2dc3-272">Before you enable the next map, verify that the map in the table is in a state of **Running**.</span></span> <span data-ttu-id="c2dc3-273">L'execució d'assignacions amb un major nombre de requisits previs podria tardar una estona.</span><span class="sxs-lookup"><span data-stu-id="c2dc3-273">Running maps with a larger number of prerequisites might take some time.</span></span>

<span data-ttu-id="c2dc3-274">Per executar una assignació amb requisits previs, habiliteu l'opció **Mostra les assignacions d'entitats relacionades**.</span><span class="sxs-lookup"><span data-stu-id="c2dc3-274">To run a map with prerequisites, enable the **Show related entity maps** toggle.</span></span> <span data-ttu-id="c2dc3-275">Si la taula indica que la **Sincronització inicial de requisits previs** és **No**, verifiqueu que l'indicador **Sincronització inicial** estigui **desactivat** a totes les assignacions de requisits previs abans d'executar-la.</span><span class="sxs-lookup"><span data-stu-id="c2dc3-275">If the table indicates **Prerequisite initial sync** is **No**, verify that the **Initial sync** flag is **Off** in all the prerequisite maps before you run it.</span></span>

![Executar l'assignació](./media/21RunMap.png)

6. <span data-ttu-id="c2dc3-277">Valideu que totes les assignacions relacionades del projecte estiguin en execució.</span><span class="sxs-lookup"><span data-stu-id="c2dc3-277">Validate all project related maps are in the running state.</span></span>

![Totes les assignacions en execució](./media/22AllMapsRunning.png)


## <a name="apply-configuration-data-in-cds-for-project-operations-optional"></a><span data-ttu-id="c2dc3-279">Aplicació de les dades de configuració al CDS per al Project Operations (opcional)</span><span class="sxs-lookup"><span data-stu-id="c2dc3-279">Apply configuration data in CDS for Project Operations (optional)</span></span>

<span data-ttu-id="c2dc3-280">Si heu aplicat dades de demostració a l'entorn del Finance, vegeu [Configurar i aplicar dades de configuració al Common Data Service per al Project Operations](resource-apply-pro-setup-config-data.md) per aplicar dades de demostració a l'entorn del CDS.</span><span class="sxs-lookup"><span data-stu-id="c2dc3-280">If you have applied demo data to the Finance environment, see [Set up and apply configuration data in the Common Data Service for Project Operations](resource-apply-pro-setup-config-data.md) to apply demo data to CDS environment.</span></span>


<span data-ttu-id="c2dc3-281">L'entorn del Project Operations ja està proveït i configurat.</span><span class="sxs-lookup"><span data-stu-id="c2dc3-281">Your Project Operations environment is now provisioned and configured.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]