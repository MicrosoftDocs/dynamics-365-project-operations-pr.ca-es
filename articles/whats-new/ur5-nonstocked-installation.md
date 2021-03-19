---
title: Actualitzeu el Project Operations a l'entorn de finances
description: Aquest tema proporciona informació sobre com actualitzar el Project Operations al vostre entorn del Dynamics 365 Finance.
author: ruhercul
manager: tfehr
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: d68296ec59f0bd58f848154c90e02c58f275ab12
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291967"
---
# <a name="update-project-operations-in-your-finance-environment"></a><span data-ttu-id="6faae-103">Actualitzeu el Project Operations a l'entorn de finances</span><span class="sxs-lookup"><span data-stu-id="6faae-103">Update Project Operations in your Finance environment</span></span>

<span data-ttu-id="6faae-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_</span><span class="sxs-lookup"><span data-stu-id="6faae-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="6faae-105">Aquest tema proporciona informació sobre com actualitzar el Dynamics 365 Project Operations al vostre entorn del Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="6faae-105">This topic provides information about how to update Dynamics 365 Project Operations in your Dynamics 365 Finance environment.</span></span> <span data-ttu-id="6faae-106">Hi ha tres procediments que són necessaris per actualitzar el Project Operations a l'actualització 5 (UR5):</span><span class="sxs-lookup"><span data-stu-id="6faae-106">There are three procedures that are required to update Project Operations to Update 5 (UR5):</span></span>

- [<span data-ttu-id="6faae-107">Importa el paquet al vostre projecte de visualització prèvia</span><span class="sxs-lookup"><span data-stu-id="6faae-107">Import the package into your preview project</span></span>](#import)
- [<span data-ttu-id="6faae-108">Aplica l'actualització</span><span class="sxs-lookup"><span data-stu-id="6faae-108">Apply the update</span></span>](#apply)
- [<span data-ttu-id="6faae-109">Configuració del vostre entorn del Dataverse</span><span class="sxs-lookup"><span data-stu-id="6faae-109">Update your Dataverse environment</span></span>](#update)

## <a name="import-the-package-into-your-lcs-project"></a><a name="import"></a><span data-ttu-id="6faae-110">Importa el paquet al vostre projecte LCS</span><span class="sxs-lookup"><span data-stu-id="6faae-110">Import the package into your LCS project</span></span>

1. <span data-ttu-id="6faae-111">Inicieu sessió als [Lifecycle Services (LCS)](https://lcs.dynamics.com/) com a propietari del projecte o administrador de l'entorn.</span><span class="sxs-lookup"><span data-stu-id="6faae-111">Sign in to [Lifecycle Services (LCS)](https://lcs.dynamics.com/) as a Project Owner or Environment manager.</span></span>
2. <span data-ttu-id="6faae-112">A la llista de projectes, seleccioneu el vostre projecte LCS.</span><span class="sxs-lookup"><span data-stu-id="6faae-112">From the list of projects, select your LCS project.</span></span>
3. <span data-ttu-id="6faae-113">A la pàgina **Projecte**, al grup **Entorns**, obriu l'entorn que voleu actualitzar.</span><span class="sxs-lookup"><span data-stu-id="6faae-113">On the **Project** page, in the **Environments** group, open the environment that you want to update.</span></span>
4. <span data-ttu-id="6faae-114">Comproveu que l'entorn s'estigui executant.</span><span class="sxs-lookup"><span data-stu-id="6faae-114">Verify that the environment is running.</span></span> <span data-ttu-id="6faae-115">Si no s'ha iniciat, inicieu l'entorn.</span><span class="sxs-lookup"><span data-stu-id="6faae-115">If it isn't started, start the environment.</span></span>
5. <span data-ttu-id="6faae-116">A la secció **Nova versió**, a **Actualitzacions disponibles**, seleccioneu **Visualitza l'actualització** per a 10.0.15.</span><span class="sxs-lookup"><span data-stu-id="6faae-116">In the **New release** section under **Available updates**, select **View update** for 10.0.15.</span></span>

![Visualitza el botó d'actualització](media/view-update.png)

6. <span data-ttu-id="6faae-118">A la pàgina **Actualitzacions binàries**, seleccioneu **Desa el paquet**.</span><span class="sxs-lookup"><span data-stu-id="6faae-118">On the **Binary updates** page, select **Save package**.</span></span>
7. <span data-ttu-id="6faae-119">A la pàgina **Revisa i desa actualitzacions**, seleccioneu **Desa el paquet**.</span><span class="sxs-lookup"><span data-stu-id="6faae-119">On the **Review and save updates** page, select **Save package**.</span></span>
8. <span data-ttu-id="6faae-120">Al panell **Desa el paquet a la biblioteca d'actius** que s'obre, introduïu el nom del paquet i seleccioneu **Desa el paquet**.</span><span class="sxs-lookup"><span data-stu-id="6faae-120">On the **Save package to asset library** pane that opens, enter the package name and then select **Save package**.</span></span>
9. <span data-ttu-id="6faae-121">Quan l'LCS hagi desat el paquet, el botó **Fet** està habilitat.</span><span class="sxs-lookup"><span data-stu-id="6faae-121">When LCS has finished saving the package, the **Done** button is enabled.</span></span> <span data-ttu-id="6faae-122">Seleccioneu **Fet**.</span><span class="sxs-lookup"><span data-stu-id="6faae-122">Select **Done**.</span></span> <span data-ttu-id="6faae-123">L'LCS verificarà el paquet.</span><span class="sxs-lookup"><span data-stu-id="6faae-123">LCS will verify the package.</span></span> <span data-ttu-id="6faae-124">La verificació pot trigar uns minuts o fins a una hora.</span><span class="sxs-lookup"><span data-stu-id="6faae-124">Verification can take a few minutes or up to one hour.</span></span>


## <a name="apply-the-package-update"></a><a name="apply"></a><span data-ttu-id="6faae-125">Aplica l'actualització del paquet</span><span class="sxs-lookup"><span data-stu-id="6faae-125">Apply the package update</span></span>

1. <span data-ttu-id="6faae-126">A l'LCS, a la pàgina **Detalls de l'entorn**, seleccioneu **Conserva** > **Aplica actualitzacions**.</span><span class="sxs-lookup"><span data-stu-id="6faae-126">In LCS, on the **Environment details** page, select **Maintain** > **Apply Updates**.</span></span>
2. <span data-ttu-id="6faae-127">A la llista, seleccioneu el paquet que heu desat abans i, a continuació, seleccioneu **Aplica**.</span><span class="sxs-lookup"><span data-stu-id="6faae-127">From the list, select the package that you saved earlier, and then select **Apply**.</span></span>
3. <span data-ttu-id="6faae-128">Seleccioneu **Sí** per confirmar que voleu implementar el paquet.</span><span class="sxs-lookup"><span data-stu-id="6faae-128">Select **Yes** to confirm that you want to deploy the package.</span></span>

![Quadre de diàleg Confirmació de la implementació del paquet](media/confirm-package-deployment.png)

4. <span data-ttu-id="6faae-130">Seleccioneu **Sí** per confirmar que voleu actualitzar l'aplicació.</span><span class="sxs-lookup"><span data-stu-id="6faae-130">Select **Yes** to confirm that you want to update the application.</span></span>

![Quadre de diàleg Confirmació de l'actualització de l'aplicació](media/confirm-application-update.png)

<span data-ttu-id="6faae-132">S'iniciarà la implementació i l'actualització de l'aplicació.</span><span class="sxs-lookup"><span data-stu-id="6faae-132">The deployment and application update will start.</span></span> 

<span data-ttu-id="6faae-133">A la pàgina **Detalls de l'entorn**, a la part superior dreta, l'estat de l'entorn s'actualitzarà a **Manteniment**.</span><span class="sxs-lookup"><span data-stu-id="6faae-133">On the **Environment details** page, in the top-right corner, the environment status will update to **Servicing**.</span></span> <span data-ttu-id="6faae-134">Aproximadament en dues hores, l'actualització es completarà.</span><span class="sxs-lookup"><span data-stu-id="6faae-134">In approximately two hours, the update will be complete.</span></span> <span data-ttu-id="6faae-135">La informació de la versió de l'aplicació s'actualitzarà a **Microsoft Dynamics 365 for Finance and Operations 10.0.15)** i l'estat de l'entorn s'actualitzarà a **Implementat**.</span><span class="sxs-lookup"><span data-stu-id="6faae-135">The application release information will update to **Microsoft Dynamics 365 for Finance and Operations 10.0.15)** and the environment status will update to **Deployed**.</span></span>


## <a name="update-your-dataverse-environment"></a><a name="update"></a><span data-ttu-id="6faae-136">Actualització del vostre entorn del Dataverse</span><span class="sxs-lookup"><span data-stu-id="6faae-136">Update your Dataverse environment</span></span>

1. <span data-ttu-id="6faae-137">Inicieu la sessió al [Centre d'administració del Power Platform](https://admin.powerplatform.com/).</span><span class="sxs-lookup"><span data-stu-id="6faae-137">Sign in to the [Power Platform admin center](https://admin.powerplatform.com/).</span></span>
2. <span data-ttu-id="6faae-138">A la llista, cerqueu i obriu l'entorn que heu utilitzat per instal·lar el Project Operations.</span><span class="sxs-lookup"><span data-stu-id="6faae-138">In the list, find and open the environment that you used to install Project Operations.</span></span>
3. <span data-ttu-id="6faae-139">A la pàgina **Entorns**, seleccioneu **Recurs** > **Aplicacions del Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="6faae-139">On the **Environments** page, select **Resource** > **Dynamics 365 apps**.</span></span>
4. <span data-ttu-id="6faae-140">A la llista, localitzeu el **Microsoft Dynamics 365 Project Operations** i, a la columna **Estat**, seleccioneu **Actualització disponible**.</span><span class="sxs-lookup"><span data-stu-id="6faae-140">In the list, locate **Microsoft Dynamics 365 Project Operations**, and in the **Status** column, select **Update Available**.</span></span>
5. <span data-ttu-id="6faae-141">Activeu la casella de selecció **Accepto les condicions del servei** i, a continuació, seleccioneu **Actualitza**.</span><span class="sxs-lookup"><span data-stu-id="6faae-141">Select the **I agree to the terms of service** check box, and then select **Update**.</span></span> <span data-ttu-id="6faae-142">S'instal·larà la versió més recent de la solució.</span><span class="sxs-lookup"><span data-stu-id="6faae-142">The latest version of the solution will be installed.</span></span>

<span data-ttu-id="6faae-143">Un cop completada la instal·lació, tindreu instal·lada la versió 4.5.0.134.</span><span class="sxs-lookup"><span data-stu-id="6faae-143">After the installation is complete, you'll have version 4.5.0.134 installed.</span></span>

## <a name="configure-new-features"></a><span data-ttu-id="6faae-144">Configura característiques noves</span><span class="sxs-lookup"><span data-stu-id="6faae-144">Configure new features</span></span>

### <a name="enable-dual-write-mapping"></a><span data-ttu-id="6faae-145">Habilita les assignacions d'escriptura doble</span><span class="sxs-lookup"><span data-stu-id="6faae-145">Enable dual-write mapping</span></span>

<span data-ttu-id="6faae-146">Un cop completada l'actualització als entorns de Finances i del Dataverse, podeu habilitar les assignacions d'escriptura doble necessàries.</span><span class="sxs-lookup"><span data-stu-id="6faae-146">After you complete the update on the Finance and Dataverse environments, you can enable the required dual-write mappings.</span></span> <span data-ttu-id="6faae-147">Completeu els següents passos per habilitar les assignacions d’escriptura doble.</span><span class="sxs-lookup"><span data-stu-id="6faae-147">Complete the following procedures to enable dual-write mappings.</span></span>

- [<span data-ttu-id="6faae-148">Actualitza la configuració de seguretat de l'entorn del Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="6faae-148">Update security settings on Customer Engagement environment</span></span>](#security)
- [<span data-ttu-id="6faae-149">Actualitza les entitats de dades</span><span class="sxs-lookup"><span data-stu-id="6faae-149">Refresh data entities</span></span>](#refresh)
- [<span data-ttu-id="6faae-150">Actualitza i executa les assignacions d'escriptura doble</span><span class="sxs-lookup"><span data-stu-id="6faae-150">Update and run the dual-write mappings</span></span>](#run)

### <a name="update-security-settings-on-the-dataverse-environment"></a><a name="security"></a><span data-ttu-id="6faae-151">Actualitza la configuració de seguretat de l'entorn del Dataverse</span><span class="sxs-lookup"><span data-stu-id="6faae-151">Update security settings on the Dataverse environment</span></span>

<span data-ttu-id="6faae-152">Les actualitzacions següents per als privilegis de seguretat per a les entitats són necessàries com a part de l'actualització a UR5.</span><span class="sxs-lookup"><span data-stu-id="6faae-152">The following updates to the security privileges for entities are required as part of the update to UR5.</span></span>

1. <span data-ttu-id="6faae-153">Al vostre entorn del Dataverse, aneu a **Configuració** i, al grup **Sistema**, seleccioneu **Seguretat**.</span><span class="sxs-lookup"><span data-stu-id="6faae-153">In your Dataverse environment, go to **Settings**, and in the **System** group, select **Security**.</span></span>

![Configuració de l'entorn del Dataverse](media/Picture21.png)

2. <span data-ttu-id="6faae-155">Seleccioneu **Funcions de seguretat**.</span><span class="sxs-lookup"><span data-stu-id="6faae-155">Select **Security Roles**.</span></span>
3. <span data-ttu-id="6faae-156">A la llista de funcions, seleccioneu **usuari de l'aplicació de doble escriptura** i seleccioneu la pestanya **Entitats personalitzades**.</span><span class="sxs-lookup"><span data-stu-id="6faae-156">From the list of roles, select **dual-write app user** and select the **Custom Entities** tab.</span></span> 
4. <span data-ttu-id="6faae-157">Verifiqueu que la funció té permisos de **Lectura** i **Annexa a**:</span><span class="sxs-lookup"><span data-stu-id="6faae-157">Verify that the role has **Read** and **Append To** permissions for:</span></span>

      - <span data-ttu-id="6faae-158">**Tipus de canvi de moneda**</span><span class="sxs-lookup"><span data-stu-id="6faae-158">**Currency Exchange Rate Type**</span></span>
      - <span data-ttu-id="6faae-159">**Taula de comptes**</span><span class="sxs-lookup"><span data-stu-id="6faae-159">**Chart Of Accounts**</span></span> 
      - <span data-ttu-id="6faae-160">**Calendari fiscal**</span><span class="sxs-lookup"><span data-stu-id="6faae-160">**Fiscal Calendar**</span></span> 
      - <span data-ttu-id="6faae-161">**Llibre major**</span><span class="sxs-lookup"><span data-stu-id="6faae-161">**Ledger**</span></span>

5. <span data-ttu-id="6faae-162">Quan la funció de seguretat s'actualitzi, aneu **Configuració** > **Seguretat** > **Equips**.</span><span class="sxs-lookup"><span data-stu-id="6faae-162">After the security role is updated, go to **Settings** > **Security** > **Teams**.</span></span> <span data-ttu-id="6faae-163">Verifiqueu que la funció d'**usuari de l'aplicació de doble escriptura** s'hagi aplicat a l'equip.</span><span class="sxs-lookup"><span data-stu-id="6faae-163">Verify that the **dual-write app user** role has been applied to the team.</span></span> 

### <a name="refresh-data-entities-from-the-update"></a><a name="refresh"></a><span data-ttu-id="6faae-164">Actualitza les entitats de dades des de l'actualització</span><span class="sxs-lookup"><span data-stu-id="6faae-164">Refresh data entities from the update</span></span>

1. <span data-ttu-id="6faae-165">A l'entorn de finances, obriu l'espai de treball **Administració de dades** i, a continuació, obriu la pàgina **Paràmetres del marc**.</span><span class="sxs-lookup"><span data-stu-id="6faae-165">In your Finance environment, open the **Data management** workspace, and then open the **Framework parameters** page.</span></span>
2. <span data-ttu-id="6faae-166">A la pestanya **Configuració d'entitat**, seleccioneu **Actualitza la llista d'entitats**.</span><span class="sxs-lookup"><span data-stu-id="6faae-166">On the **Entity settings** tab, select **Refresh entity list**.</span></span>
3. <span data-ttu-id="6faae-167">Seleccioneu **Tanca** per confirmar l'actualització de l'entitat.</span><span class="sxs-lookup"><span data-stu-id="6faae-167">Select **Close** to confirm the entity refresh.</span></span>

 > [!NOTE]
 > <span data-ttu-id="6faae-168">Aquest procés trigarà 20 aproximadament.</span><span class="sxs-lookup"><span data-stu-id="6faae-168">This process will take approximately 20 minutes to complete.</span></span> <span data-ttu-id="6faae-169">Quan l'actualització finalitzi, se us notificarà.</span><span class="sxs-lookup"><span data-stu-id="6faae-169">You will be notified when the refresh is complete.</span></span>

### <a name="update-dual-write-mappings"></a><a name="run"></a><span data-ttu-id="6faae-170">Actualitza les assignacions d'escriptura doble</span><span class="sxs-lookup"><span data-stu-id="6faae-170">Update dual-write mappings</span></span>

1. <span data-ttu-id="6faae-171">A l'àrea de treball **Administració de dades**, seleccioneu **Escriptura doble**.</span><span class="sxs-lookup"><span data-stu-id="6faae-171">In the **Data management** workspace, select **Dual-write**.</span></span>
2. <span data-ttu-id="6faae-172">Seleccioneu **Aplicar solucions**, seleccioneu les dues solucions a la llista i, a continuació, seleccioneu **Aplica**.</span><span class="sxs-lookup"><span data-stu-id="6faae-172">Select **Apply solutions**, select both solutions in the list, and then select **Apply**.</span></span>
3. <span data-ttu-id="6faae-173">A la pàgina **Escriptura doble**, seleccioneu les assignacions de taula següents i, a continuació, seleccioneu **Atura**.</span><span class="sxs-lookup"><span data-stu-id="6faae-173">On the **Dual-write** page, select the following table maps, and then select **Stop**.</span></span>

    - <span data-ttu-id="6faae-174">**Valors reals d'integració del Project Operations (msdyn_actuals)**</span><span class="sxs-lookup"><span data-stu-id="6faae-174">**Project Operations integration actuals (msdyn_actuals)**</span></span>
    - <span data-ttu-id="6faae-175">**Categories de despeses del projecte d'integració del Project Operations (msdyn_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="6faae-175">**Project Operations integration project expense categories (msdyn_expensecategories)**</span></span>
    - <span data-ttu-id="6faae-176">**Entitat d'exportació de despeses del projecte d'integració del Project Operations (msdyn_expenses)**</span><span class="sxs-lookup"><span data-stu-id="6faae-176">**Project Operations integration actuals project expenses export entity (msdyn_expenses)**</span></span>

4. <span data-ttu-id="6faae-177">A la pàgina **Vversió de l'assignació de la taula**, apliqueu una versió nova del mapa a cadascuna de les tres entitats.</span><span class="sxs-lookup"><span data-stu-id="6faae-177">On the **Table map version** page, apply a new version of the map to each of the three entities.</span></span>
5. <span data-ttu-id="6faae-178">A la pàgina **Escriptura doble**, seleccioneu executa per reiniciar les assignacions.</span><span class="sxs-lookup"><span data-stu-id="6faae-178">On the **Dual-write** page, select run to restart the maps.</span></span>
6. <span data-ttu-id="6faae-179">A la llista de mapes, seleccioneu l'assignació **Llibre major (msdyn_ledgers)** amb tots els requisits previs i activeu la casella de selecció **Sincronització inicial**.</span><span class="sxs-lookup"><span data-stu-id="6faae-179">From the list of maps, select the **Ledger (msdyn_ledgers)** map with all prerequisites and select the **Initial sync** check box.</span></span> 
7. <span data-ttu-id="6faae-180">Al camp **Mestre per a la sincronització inicial**, seleccioneu les **aplicacions Finance and Operations** i, a continuació, seleccioneu **Executa**.</span><span class="sxs-lookup"><span data-stu-id="6faae-180">In the **Master for initial sync** field, select **Finance and Operations apps** and then select **Run**.</span></span>
 
 ![Sincronització de l'assignació de llibres majors](media/DW6.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]