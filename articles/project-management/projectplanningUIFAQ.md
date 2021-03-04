---
title: Solucionar problemes de funcionament a la quadrícula de tasques
description: En aquest tema es proporciona informació sobre la detecció d'errors que es necessita quan es treballa a la quadrícula de tasques.
author: ruhercul
manager: tfehr
ms.date: 01/19/2021
ms.topic: article
ms.product: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 89bbad62c2a0a5693a57cf5c9a812ab644486469
ms.sourcegitcommit: c9edb4fc3042d97cb1245be627841e0a984dbdea
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 01/19/2021
ms.locfileid: "5031525"
---
# <a name="troubleshoot-working-in-the-task-grid"></a><span data-ttu-id="00183-103">Solucionar problemes de funcionament a la quadrícula de tasques</span><span class="sxs-lookup"><span data-stu-id="00183-103">Troubleshoot working in the Task grid</span></span> 

<span data-ttu-id="00183-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_</span><span class="sxs-lookup"><span data-stu-id="00183-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="00183-105">En aquest tema es descriu com solucionar els problemes amb què us podeu trobar mentre treballeu amb l'administració de costos.</span><span class="sxs-lookup"><span data-stu-id="00183-105">This topic describes how to fix issues that you might encounter while working with cost management.</span></span>

## <a name="enable-cookies"></a><span data-ttu-id="00183-106">Habilita les galetes:</span><span class="sxs-lookup"><span data-stu-id="00183-106">Enable cookies</span></span>

<span data-ttu-id="00183-107">El Project Operations requereix que s'habilitin galetes de tercers per representar l'estructura del desglossament del treball.</span><span class="sxs-lookup"><span data-stu-id="00183-107">Project Operations requires that third-party cookies be enabled in order to render the work breakdown structure.</span></span> <span data-ttu-id="00183-108">Quan les galetes de tercers no estan habilitades, en lloc de veure les tasques, veureu una pàgina en blanc quan seleccioneu la pestanya **Tasques** a la pàgina **Projecte**.</span><span class="sxs-lookup"><span data-stu-id="00183-108">When third-party cookies aren't enabled, instead of seeing tasks, you will see a blank page when you select the **Tasks** tab on the **Project** page.</span></span>

![Pestanya en blanc quan les galetes de tercers no estan habilitades](media/blankschedule.png)


### <a name="workaround"></a><span data-ttu-id="00183-110">Solució alternativa</span><span class="sxs-lookup"><span data-stu-id="00183-110">Workaround</span></span>
<span data-ttu-id="00183-111">Per als navegadors Microsoft Edge o Google Chrome, a continuació s'explica com s'actualitza la configuració del navegador per habilitar les galetes de tercers.</span><span class="sxs-lookup"><span data-stu-id="00183-111">For Microsoft Edge or Google Chrome browsers, the following procedures outline how to update your browser setting to enable third-party cookies.</span></span>

#### <a name="microsoft-edge"></a><span data-ttu-id="00183-112">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="00183-112">Microsoft Edge</span></span>

1. <span data-ttu-id="00183-113">Obriu el navegador Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="00183-113">Open your Edge browser.</span></span>
2. <span data-ttu-id="00183-114">A la cantonada superior dreta, seleccioneu la **el·lipsi** (...) i, a continuació, seleccioneu **Configuració**.</span><span class="sxs-lookup"><span data-stu-id="00183-114">In the upper-right corner, select the **ellipsis** (...), and then select **Settings**.</span></span>
3. <span data-ttu-id="00183-115">A **Galetes i permisos del lloc**, seleccioneu **Galetes i dades del lloc**.</span><span class="sxs-lookup"><span data-stu-id="00183-115">Under **Cookies and site permissions**, select **Cookies and site data**.</span></span>
4. <span data-ttu-id="00183-116">Desactiveu **Bloqueja les galetes de tercers**.</span><span class="sxs-lookup"><span data-stu-id="00183-116">Turn off **Block third-party cookies**.</span></span>

#### <a name="google-chrome"></a><span data-ttu-id="00183-117">Google Chrome</span><span class="sxs-lookup"><span data-stu-id="00183-117">Google Chrome</span></span>

1. <span data-ttu-id="00183-118">Obriu el navegador Chrome.</span><span class="sxs-lookup"><span data-stu-id="00183-118">Open your Chrome browser.</span></span>
2. <span data-ttu-id="00183-119">A la cantonada superior dreta, seleccioneu els tres punts verticals i, a continuació, seleccioneu **Configuració**.</span><span class="sxs-lookup"><span data-stu-id="00183-119">In the upper-right corner, select the three vertical dots, and then select **Settings**.</span></span>
3. <span data-ttu-id="00183-120">A **Privades i seguretat**, seleccioneu **Galetes i altres dades dels llocs web**.</span><span class="sxs-lookup"><span data-stu-id="00183-120">Under **Privacy and security**, select **Cookies and other site data**.</span></span>
4. <span data-ttu-id="00183-121">Seleccioneu **Permet totes les galetes**.</span><span class="sxs-lookup"><span data-stu-id="00183-121">Select **Allow all cookies**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="00183-122">Si bloquegeu les galetes de tercers, totes les galetes i les dades de llocs d'altres llocs es bloquejaran, encara que el lloc estigui autoritzat a la vostra llista d'excepcions.</span><span class="sxs-lookup"><span data-stu-id="00183-122">If you block third-party cookies, all cookies and site data from other sites will be blocked, even if the site is allowed on your exceptions list.</span></span>

## <a name="pex-endpoint"></a><span data-ttu-id="00183-123">Extrem PEX</span><span class="sxs-lookup"><span data-stu-id="00183-123">PEX Endpoint</span></span>

<span data-ttu-id="00183-124">El Project Operations requereix que un paràmetre de projecte faci referència a l'extrem del PEX.</span><span class="sxs-lookup"><span data-stu-id="00183-124">Project Operations requires that a project parameter reference the PEX Endpoint.</span></span> <span data-ttu-id="00183-125">Aquest extrem es necessita per comunicar-se amb el servei utilitzat per representar l'estructura del desglossament del treball.</span><span class="sxs-lookup"><span data-stu-id="00183-125">This endpoint is required to communicate with the service used to render the work breakdown structure.</span></span> <span data-ttu-id="00183-126">Si el paràmetre no està habilitat, rebreu l'error "El paràmetre de projecte no és vàlid".</span><span class="sxs-lookup"><span data-stu-id="00183-126">If the parameter isn't enabled, you will receive the error, "The project parameter is not valid".</span></span> 

### <a name="workaround"></a><span data-ttu-id="00183-127">Solució alternativa</span><span class="sxs-lookup"><span data-stu-id="00183-127">Workaround</span></span>
 ![Camp extrem del PEX al paràmetre de projecte](media/projectparameter.png)

1. <span data-ttu-id="00183-129">Afegiu el camp **extrem del PEX** a la pàgina **Paràmetres del projecte**.</span><span class="sxs-lookup"><span data-stu-id="00183-129">Add the **PEX Endpoint** field to the **Project Parameters** page.</span></span>
2. <span data-ttu-id="00183-130">Actualitzeu el camp amb el següent valor: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=\<id>&type=2`</span><span class="sxs-lookup"><span data-stu-id="00183-130">Update the field with the following value: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=\<id>&type=2`</span></span>
3. <span data-ttu-id="00183-131">Suprimiu el camp de la pàgina **Paràmetres del projecte**.</span><span class="sxs-lookup"><span data-stu-id="00183-131">Remove the field from the **Project Parameters** page.</span></span>

## <a name="privileges-for-project-for-the-web"></a><span data-ttu-id="00183-132">Privilegis per al projecte per al web</span><span class="sxs-lookup"><span data-stu-id="00183-132">Privileges for Project for the Web</span></span>

<span data-ttu-id="00183-133">El Project Operations es basa en un servei de planificació extern.</span><span class="sxs-lookup"><span data-stu-id="00183-133">Project Operations relies on an external scheduling service.</span></span> <span data-ttu-id="00183-134">El servei requereix que un usuari tingui assignades diverses funcions per llegir i escriure a entitats relacionades amb l'estructura del desglossament del treball.</span><span class="sxs-lookup"><span data-stu-id="00183-134">The service requires that a user have several roles assigned to read and write to entities related to the work breakdown structure.</span></span> <span data-ttu-id="00183-135">Aquestes entitats inclouen tasques de projecte, assignacions de recursos i dependències de tasques.</span><span class="sxs-lookup"><span data-stu-id="00183-135">These entities include project tasks, resource assignments, and task dependencies.</span></span> <span data-ttu-id="00183-136">Si un usuari no pot representar l'estructura del desglossament del treball quan va a la pestanya **Tasques**, probablement és perquè projecte per al Project Operations no s'ha habilitat.</span><span class="sxs-lookup"><span data-stu-id="00183-136">If a user can't render the work breakdown structure when they go to the **Tasks** tab, it's probably because Project for Project Operations hasn't been enabled.</span></span> <span data-ttu-id="00183-137">Un usuari pot rebre un error de funció de seguretat o un error relacionat amb una denegació d'accés.</span><span class="sxs-lookup"><span data-stu-id="00183-137">A user might receive either a security role error, or an error related to a denial of access.</span></span>


## <a name="workaround"></a><span data-ttu-id="00183-138">Solució alternativa</span><span class="sxs-lookup"><span data-stu-id="00183-138">Workaround</span></span>

1. <span data-ttu-id="00183-139">Aneu a **Configuració > Seguretat > Usuaris > Usuaris d'aplicació**.</span><span class="sxs-lookup"><span data-stu-id="00183-139">Go to **Setting > Security > Users > Application Users**.</span></span>  

   ![Lector de l'aplicació](media/applicationuser.jpg)
   
2. <span data-ttu-id="00183-141">Feu doble clic al registre d'usuari de l'aplicació per verificar el següent:</span><span class="sxs-lookup"><span data-stu-id="00183-141">Double-click the application user record to verify the following:</span></span>

 - <span data-ttu-id="00183-142">L'usuari té accés al projecte.</span><span class="sxs-lookup"><span data-stu-id="00183-142">The user has access to the project.</span></span> <span data-ttu-id="00183-143">Normalment, aquesta verificació es fa comprovant que l'usuari té la funció de seguretat **Administrador del projecte**.</span><span class="sxs-lookup"><span data-stu-id="00183-143">This verification is typically done by ensuring that the user has **Project Manager** security role.</span></span>
 - <span data-ttu-id="00183-144">L'usuari de l'aplicació Microsoft Project existeix i està configurat correctament.</span><span class="sxs-lookup"><span data-stu-id="00183-144">The Microsoft Project application user exists and is configured correctly.</span></span>
 
3. <span data-ttu-id="00183-145">Si aquest usuari no existeix, podeu crear un registre d'usuari nou.</span><span class="sxs-lookup"><span data-stu-id="00183-145">If this user doesn't exist, you can create a new user record.</span></span> <span data-ttu-id="00183-146">Seleccioneu **Usuaris nous**.</span><span class="sxs-lookup"><span data-stu-id="00183-146">Select **New Users**.</span></span> <span data-ttu-id="00183-147">Canvieu el formulari d'entrada a **Usuari de l'aplicació** i, a continuació, afegiu **l'identificador de l'aplicació**.</span><span class="sxs-lookup"><span data-stu-id="00183-147">Change the entry form to **Application User**, and then add the **Application ID**.</span></span>

   ![Detalls de l'usuari de l'aplicació](media/applicationuserdetails.jpg)

4. <span data-ttu-id="00183-149">Verifiqueu que s'hagi assignat la llicència correcta a l'usuari i que el servei estigui habilitat als detalls dels plans de servei de la llicència.</span><span class="sxs-lookup"><span data-stu-id="00183-149">Verify that the user has been assigned the correct license and that the service is enabled in the service plans details of the license.</span></span>
5. <span data-ttu-id="00183-150">Verifiqueu que l'usuari pot obrir project.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="00183-150">Verify that the user can open project.microsoft.com.</span></span>
6. <span data-ttu-id="00183-151">Verifiqueu a través dels paràmetres de projecte que el sistema assenyala a l'extrem del projecte correcte.</span><span class="sxs-lookup"><span data-stu-id="00183-151">Verify through the project parameters that the system is pointing to the correct project endpoint.</span></span>
7. <span data-ttu-id="00183-152">Verifiqueu que s'hagi creat l'usuari de l'aplicació de projecte.</span><span class="sxs-lookup"><span data-stu-id="00183-152">Verify that the project application user is created.</span></span>
8. <span data-ttu-id="00183-153">Apliqueu les funcions de seguretat següents a l'usuari:</span><span class="sxs-lookup"><span data-stu-id="00183-153">Apply the following security roles to the user:</span></span>

  - <span data-ttu-id="00183-154">Usuari del Dataverse</span><span class="sxs-lookup"><span data-stu-id="00183-154">Dataverse User</span></span>
  - <span data-ttu-id="00183-155">Sistema del Project Operations</span><span class="sxs-lookup"><span data-stu-id="00183-155">Project Operations System</span></span>
  - <span data-ttu-id="00183-156">Sistema del projecte</span><span class="sxs-lookup"><span data-stu-id="00183-156">Project System</span></span>

## <a name="error-when-updating-the-work-breakdown-structure"></a><span data-ttu-id="00183-157">Es produeix un error quan s'actualitza l'estructura del desglossament del treball</span><span class="sxs-lookup"><span data-stu-id="00183-157">Error when updating the work breakdown structure</span></span>

<span data-ttu-id="00183-158">Quan es fan una o més actualitzacions a l'estructura del desglossament del treball, els canvis finalment fallen i no es desen.</span><span class="sxs-lookup"><span data-stu-id="00183-158">When one or more updates are made to the work breakdown structure, the changes eventually fail and aren't saved.</span></span> <span data-ttu-id="00183-159">S'ha produït un error a la quadrícula de planificació i s'ha especificat que "Els canvis recents que heu fet no s'han pogut desar".</span><span class="sxs-lookup"><span data-stu-id="00183-159">An error occurs in the schedule grid noting that “Recent change you’ve made couldn’t be saved.”</span></span>

### <a name="workaround"></a><span data-ttu-id="00183-160">Solució alternativa</span><span class="sxs-lookup"><span data-stu-id="00183-160">Workaround</span></span>

1. <span data-ttu-id="00183-161">Verifiqueu que s'hagi assignat la llicència correcta a l'usuari i que el servei estigui habilitat als detalls dels plans de servei de la llicència.</span><span class="sxs-lookup"><span data-stu-id="00183-161">Verify that the user has been assigned the correct license and that the service is enabled in the service plans details of the license.</span></span>
2. <span data-ttu-id="00183-162">Verifiqueu que l'usuari pot obrir project.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="00183-162">Verify that the user can open project.microsoft.com.</span></span>
3. <span data-ttu-id="00183-163">Verifiqueu que el sistema assenyala l'extrem del projecte correcte.</span><span class="sxs-lookup"><span data-stu-id="00183-163">Verify that the system is pointing to the correct project endpoint,.</span></span>
4. <span data-ttu-id="00183-164">Verifiqueu que s'ha creat l'usuari de l'aplicació de projecte.</span><span class="sxs-lookup"><span data-stu-id="00183-164">Verify that the Project Application user has been created.</span></span>
5. <span data-ttu-id="00183-165">Apliqueu les funcions de seguretat següents a l'usuari:</span><span class="sxs-lookup"><span data-stu-id="00183-165">Apply the following security roles to the user:</span></span>
  
  - <span data-ttu-id="00183-166">Usuari del Dataverse o usuari base</span><span class="sxs-lookup"><span data-stu-id="00183-166">Dataverse user or Base user</span></span>
  - <span data-ttu-id="00183-167">Sistema del Project Operations</span><span class="sxs-lookup"><span data-stu-id="00183-167">Project Operations System</span></span>
  - <span data-ttu-id="00183-168">Sistema del projecte</span><span class="sxs-lookup"><span data-stu-id="00183-168">Project System</span></span>
  - <span data-ttu-id="00183-169">Sistema d'escriptura doble del Project Operations (aquesta funció és necessària si esteu implementant l'escenari basat en el recurs/sense existències del Project Operations.)</span><span class="sxs-lookup"><span data-stu-id="00183-169">Project Operations Dual Write System (This role is required if you are deploying the resource/non-stocked based scenario of Project Operations.)</span></span>
