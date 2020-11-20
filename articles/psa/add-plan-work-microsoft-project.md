---
title: Utilitzar el complement Project Service per planificar el vostre treball al Microsoft Project | MicrosoftDocs
description: En aquest tema es proporciona informació sobre com afegir, configurar i utilitzar el complement del Microsoft Project per al Microsoft Project Service.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 04/06/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 6bc74442866caccc02e53afc913a55aab81f9629
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4129666"
---
# <a name="use-the-project-service-automation-add-in-to-plan-your-work-in-microsoft-project"></a><span data-ttu-id="75f5e-103">Utilitzar el complement Project Service Automation per planificar el vostre treball al Microsoft Project</span><span class="sxs-lookup"><span data-stu-id="75f5e-103">Use the Project Service Automation Add-in to plan your work in Microsoft Project</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="75f5e-104">El [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] us facilita la planificació del projecte, incloent-hi les estimacions.</span><span class="sxs-lookup"><span data-stu-id="75f5e-104">[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] makes it easier for you to do your project planning, including estimates.</span></span> <span data-ttu-id="75f5e-105">Podeu definir el treball perquè els costos, l'esforç i el valor de les vendes siguin clars quan es presenti la proposta final.</span><span class="sxs-lookup"><span data-stu-id="75f5e-105">You can define the work so that costs, effort, and sales value are clear as the final proposal is submitted.</span></span>  

 <span data-ttu-id="75f5e-106">Ara podeu instal·lar el [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] i realitzar la planificació del treball en l'entorn familiar del [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="75f5e-106">Now you can install the [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] and do your planning work in the familiar environment of [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span> <span data-ttu-id="75f5e-107">Utilitzeu les capacitats de planificació i gestió robustes del [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] i actualitzeu el pla del vostre projecte al Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="75f5e-107">Use the robust planning and management capabilities of [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and then update your project plan in Project Service Automation.</span></span>  

> [!IMPORTANT]
> - <span data-ttu-id="75f5e-108">Per utilitzar la característica d'administració de documents del SharePoint per emmagatzemar els vostres fitxers del [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] per als projectes del [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], l'administrador del [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] haurà d'activar l'administració de documents.</span><span class="sxs-lookup"><span data-stu-id="75f5e-108">To use SharePoint document management to store your [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] files for [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] projects, your [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] admin will need to turn on document management.</span></span> 
> - <span data-ttu-id="75f5e-109">El [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] només és compatible amb el [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition.</span><span class="sxs-lookup"><span data-stu-id="75f5e-109">The [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] is only compatible with [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition.</span></span>  

## <a name="download-and-install-the-add-in"></a><span data-ttu-id="75f5e-110">Descarregar i instal·lar el complement</span><span class="sxs-lookup"><span data-stu-id="75f5e-110">Download and install the add-in</span></span>  
 <span data-ttu-id="75f5e-111">Heu de tenir la informació d'inici de sessió del [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] preparada.</span><span class="sxs-lookup"><span data-stu-id="75f5e-111">Have your [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] sign-in information ready.</span></span> <span data-ttu-id="75f5e-112">Necessitareu aquesta informació per connectar-vos del [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] al [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="75f5e-112">You will need this information to connect from [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

1.  <span data-ttu-id="75f5e-113">Al centre de baixades, baixeu el complement per a la versió compatible del servei del Project Service, ja sigui la [V2.X](https://go.microsoft.com/fwlink/?linkid=828268) o la [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956).</span><span class="sxs-lookup"><span data-stu-id="75f5e-113">From the Download Center, download the add-in for your supported version of Project Service, either [V2.X](https://go.microsoft.com/fwlink/?linkid=828268) or [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956).</span></span>  

2.  <span data-ttu-id="75f5e-114">Feu clic a l'enllaç de descàrrega.</span><span class="sxs-lookup"><span data-stu-id="75f5e-114">Click the download link.</span></span>  

3.  <span data-ttu-id="75f5e-115">Quan s'hagi completat la descàrrega, feu clic a **Sí** per instal·lar el complement.</span><span class="sxs-lookup"><span data-stu-id="75f5e-115">When the download is complete, click **Yes** to install the add-in.</span></span>  

## <a name="configure-the-add-in"></a><span data-ttu-id="75f5e-116">Configurar el complement</span><span class="sxs-lookup"><span data-stu-id="75f5e-116">Configure the add-in</span></span>  

1. <span data-ttu-id="75f5e-117">Obriu el [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] i feu clic a la pestanya **Project Service**.</span><span class="sxs-lookup"><span data-stu-id="75f5e-117">Open [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and click the **Project Service** tab.</span></span>  

2. <span data-ttu-id="75f5e-118">Feu clic a **Connecta**.</span><span class="sxs-lookup"><span data-stu-id="75f5e-118">Click **Connect**.</span></span>  

3. <span data-ttu-id="75f5e-119">Introduïu la vostra informació d'inici de sessió i feu clic a **Inicia sessió**.</span><span class="sxs-lookup"><span data-stu-id="75f5e-119">Enter your sign-in information and then click **Sign in**.</span></span>  

   <span data-ttu-id="75f5e-120">Ara podeu començar a utilitzar el complement.</span><span class="sxs-lookup"><span data-stu-id="75f5e-120">Now you can start using the add-in.</span></span>  

## <a name="read-from-a-template"></a><span data-ttu-id="75f5e-121">Llegir d'una plantilla</span><span class="sxs-lookup"><span data-stu-id="75f5e-121">Read from a template</span></span>  
 <span data-ttu-id="75f5e-122">Llegiu des d'una plantilla que hàgiu creat al [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] i copiat al [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] per començar la planificació del projecte.</span><span class="sxs-lookup"><span data-stu-id="75f5e-122">Read from a template that you created in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] and copied into [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] to start your project planning.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="75f5e-123">[Crear una plantilla de projecte (Project Service Automation)](../psa/create-project-template.md)</span><span class="sxs-lookup"><span data-stu-id="75f5e-123">[Create a project template (Project Service Automation)](../psa/create-project-template.md)</span></span>  

1.  <span data-ttu-id="75f5e-124">A la pestanya **Project Service**, feu clic a **Lectura** > **Plantilla de projecte del Project Service Automation**.</span><span class="sxs-lookup"><span data-stu-id="75f5e-124">From the **Project Service** tab, click **Read** > **Project Service Automation Project Template**.</span></span>  

2.  <span data-ttu-id="75f5e-125">Trieu una plantilla de projecte de la llista i feu clic a **Obre**.</span><span class="sxs-lookup"><span data-stu-id="75f5e-125">Choose a project template from the list and then click **Open**.</span></span>  

    > [!NOTE]
    >  <span data-ttu-id="75f5e-126">Per defecte, les tasques que es copien de la plantilla al projecte es defineixes com planificades manualment.</span><span class="sxs-lookup"><span data-stu-id="75f5e-126">By default, the tasks that are copied from the template into Project are set as manually scheduled.</span></span>  

## <a name="assign-pn_project_service_auto-roles-to-project-resources"></a><span data-ttu-id="75f5e-127">Assignar funcions del [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] als recursos del projecte</span><span class="sxs-lookup"><span data-stu-id="75f5e-127">Assign [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] roles to project resources</span></span>  

1.  <span data-ttu-id="75f5e-128">Obriu un projecte i feu clic a la franja **Tasca**.</span><span class="sxs-lookup"><span data-stu-id="75f5e-128">Open a project and click the **Task** ribbon.</span></span>  

2.  <span data-ttu-id="75f5e-129">Feu clic al menú **Gràfic de Gantt** i seleccioneu **Full de recurs**.</span><span class="sxs-lookup"><span data-stu-id="75f5e-129">Click the **Gantt Chart** menu and then choose **Resource Sheet**.</span></span>  

3.  <span data-ttu-id="75f5e-130">Al full de recurs, feu clic al menú desplegable **Funció de recurs del Project Service** i seleccioneu una funció del Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="75f5e-130">On the Resource Sheet, click the **Project Service Resource Role** drop-down menu and choose a Project Service Automation role.</span></span>  

## <a name="staff-your-project-with-resources"></a><span data-ttu-id="75f5e-131">Seleccionar el personal del projecte amb recursos</span><span class="sxs-lookup"><span data-stu-id="75f5e-131">Staff your project with resources</span></span>  

1.  <span data-ttu-id="75f5e-132">A la pestanya Project Service, seleccioneu una fila i feu clic a **Cerca recursos**.</span><span class="sxs-lookup"><span data-stu-id="75f5e-132">From the Project Service tab, select a row and click **Find Resources**.</span></span>  

2.  <span data-ttu-id="75f5e-133">A la pantalla **Reserva el recurs**, seleccioneu el recurs que voleu utilitzar per al projecte.</span><span class="sxs-lookup"><span data-stu-id="75f5e-133">On the **Book Resource** screen, select the resource that you want to use for the project.</span></span>  

3.  <span data-ttu-id="75f5e-134">Feu clic a **Reserva** i, a continuació, a **D'acord**.</span><span class="sxs-lookup"><span data-stu-id="75f5e-134">Click **Book** and then click **OK**.</span></span>  

## <a name="publish-your-project"></a><span data-ttu-id="75f5e-135">Publicar el projecte</span><span class="sxs-lookup"><span data-stu-id="75f5e-135">Publish your project</span></span>  
<span data-ttu-id="75f5e-136">Quan s'hagi completat la planificació del projecte, el següent pas és importar i publicar el projecte al [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="75f5e-136">When your project planning is complete, the next step is to import and publish the project in to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

<span data-ttu-id="75f5e-137">El projecte s'importarà al [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="75f5e-137">The project will import into [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span> <span data-ttu-id="75f5e-138">S'aplica el procés de generació de preus i d'equip.</span><span class="sxs-lookup"><span data-stu-id="75f5e-138">The pricing and team generation process are applied.</span></span> <span data-ttu-id="75f5e-139">Obriu el projecte al [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] per veure que s'ha generat l'equip, les estimacions del projecte i l'estructura del desglossament del treball.</span><span class="sxs-lookup"><span data-stu-id="75f5e-139">Open the project in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to see that the team, project estimates, and work breakdown structure has been generated.</span></span> <span data-ttu-id="75f5e-140">La taula següent mostra on trobar els resultats:</span><span class="sxs-lookup"><span data-stu-id="75f5e-140">The following table shows where to find the results:</span></span>


|                                                                                          |                                                                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|  [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] <span data-ttu-id="75f5e-141">**Gràfic de Gantt**</span><span class="sxs-lookup"><span data-stu-id="75f5e-141">**Gantt Chart**</span></span>   | <span data-ttu-id="75f5e-142">Importa a la pantalla de l-**estructura del desglossament del treball** del [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="75f5e-142">Imports into the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Work Breakdown Structure** screen.</span></span> |
| [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] <span data-ttu-id="75f5e-143">**Full de recursos**</span><span class="sxs-lookup"><span data-stu-id="75f5e-143">**Resource Sheet**</span></span> |   <span data-ttu-id="75f5e-144">Importa a la pantalla dels **membres de l'equip del projecte** del [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="75f5e-144">Imports into the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Project Team Members** screen.</span></span>   |
|   [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] <span data-ttu-id="75f5e-145">**Utilitzar l'ús**</span><span class="sxs-lookup"><span data-stu-id="75f5e-145">**Use Usage**</span></span>    |    <span data-ttu-id="75f5e-146">Importa a la pantalla d'**estimacions del projecte** del [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="75f5e-146">Omports into the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Project Estimates** screen.</span></span>     |

<span data-ttu-id="75f5e-147">**Per importar i publicar el vostre projecte**</span><span class="sxs-lookup"><span data-stu-id="75f5e-147">**To import and publish your project**</span></span>  
1. <span data-ttu-id="75f5e-148">A la pestanya **Project Service**, feu clic a **Publica** > **Nou projecte del Project Service Automation**.</span><span class="sxs-lookup"><span data-stu-id="75f5e-148">From the **Project Service** tab, click **Publish** > **New Project Service Automation Project**.</span></span>  

2. <span data-ttu-id="75f5e-149">Al quadre de diàleg **Publicació en un projecte nou del Project Service**, introduïu el **Nom del projecte** i seleccioneu el **Client**.</span><span class="sxs-lookup"><span data-stu-id="75f5e-149">On **Publish to a new project in Project Service** dialog box, enter the **Project Name** and select the **Customer**.</span></span>  

3. <span data-ttu-id="75f5e-150">De forma opcional, marqueu la casella **Enllaça el pla de projecte al Project Service Automation** per enllaçar el fitxer de projecte de pla al Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="75f5e-150">Optionally check the **Link project plan to Project Service Automation** to link the plan Project file to Project Service Automation.</span></span>  

4. <span data-ttu-id="75f5e-151">Feu clic a **Publica**.</span><span class="sxs-lookup"><span data-stu-id="75f5e-151">Click **Publish**.</span></span>  

   <span data-ttu-id="75f5e-152">Enllaçar el fitxer del Project al [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] farà que el fitxer del Project sigui el fitxer mestre i defineix l'estructura del desglossament del treball al [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] com només de lectura.</span><span class="sxs-lookup"><span data-stu-id="75f5e-152">Linking the Project file to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] makes the Project file the master and sets the work breakdown structure in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to read-only.</span></span>  <span data-ttu-id="75f5e-153">Per fer canvis al pla del projecte, cal fer-los al [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] i publicar-los com a actualitzacions del [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="75f5e-153">In order to make changes to the project plan, you need to make them in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and publish them as updates to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

## <a name="edit-a-project-thats-been-imported"></a><span data-ttu-id="75f5e-154">Editar un projecte que s'ha importat</span><span class="sxs-lookup"><span data-stu-id="75f5e-154">Edit a project that’s been imported</span></span>  
 <span data-ttu-id="75f5e-155">Per fer canvis en un pla de projecte que s'ha importat al [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], teniu dues opcions:</span><span class="sxs-lookup"><span data-stu-id="75f5e-155">To make changes to a project plan that's been imported into [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], you have two options:</span></span>  

- <span data-ttu-id="75f5e-156">Obriu el fitxer mestre i editeu-lo al [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="75f5e-156">Open the master file and edit it in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

- <span data-ttu-id="75f5e-157">Desenllaçar el fitxer i editar-lo directament al Project Service.</span><span class="sxs-lookup"><span data-stu-id="75f5e-157">Unlink the file and edit it directly in Project Service.</span></span> <span data-ttu-id="75f5e-158">Per defecte, un projecte que s'ha carregat del [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] està bloquejat i només es pot editar al Project.</span><span class="sxs-lookup"><span data-stu-id="75f5e-158">By default, a project that’s been uploaded from [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] is locked and can only be edited in Project.</span></span> <span data-ttu-id="75f5e-159">Per editar el fitxer al [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], el fitxer ha d'estar desenllaçat.</span><span class="sxs-lookup"><span data-stu-id="75f5e-159">To edit the file in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], the file has to be unlinked.</span></span>  

### <a name="edit-in-pn_microsoft_project"></a><span data-ttu-id="75f5e-160">Editeu-ho al [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]</span><span class="sxs-lookup"><span data-stu-id="75f5e-160">Edit in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]</span></span>  

1. <span data-ttu-id="75f5e-161">Des del menú principal, feu clic a **Project Service** > **Projectes**.</span><span class="sxs-lookup"><span data-stu-id="75f5e-161">From the main menu, click **Project Service** > **Projects**.</span></span>  

2. <span data-ttu-id="75f5e-162">A la llista de projectes, obriu el que vàreu crear al [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="75f5e-162">From the list of projects, open the one you created in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

3. <span data-ttu-id="75f5e-163">Feu clic a **Obre al MS Project** de la franja.</span><span class="sxs-lookup"><span data-stu-id="75f5e-163">Click **Open in MS Project** from the ribbon.</span></span> <span data-ttu-id="75f5e-164">Això obrirà el fitxer mestre enllaçat al [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="75f5e-164">This will open the linked master file in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

### <a name="unlink-a-file-and-edit-in-pn_microsoft_project-service"></a><span data-ttu-id="75f5e-165">Desenllaçar un fitxer i editar-lo al [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service</span><span class="sxs-lookup"><span data-stu-id="75f5e-165">Unlink a file and edit in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service</span></span>  

1. <span data-ttu-id="75f5e-166">Des del menú principal, feu clic a **Project Service** > **Projectes**.</span><span class="sxs-lookup"><span data-stu-id="75f5e-166">From the main menu, click **Project Service** > **Projects**.</span></span>  

2. <span data-ttu-id="75f5e-167">A la llista de projectes, obriu el que vàreu crear al [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="75f5e-167">From the list of projects, open the one you created in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

3. <span data-ttu-id="75f5e-168">Feu clic a **Desenllaça del MS Project** de la franja.</span><span class="sxs-lookup"><span data-stu-id="75f5e-168">Click **Unlink from MS Project** from the ribbon.</span></span>  

## <a name="upload-a-project-file-to-sharepoint-or-office-groups"></a><span data-ttu-id="75f5e-169">Carregar un fitxer del Project al SharePoint o als grups de l'Office</span><span class="sxs-lookup"><span data-stu-id="75f5e-169">Upload a Project file to SharePoint or Office Groups</span></span>  
 <span data-ttu-id="75f5e-170">Podeu carregar el fitxer del Project al SharePoint i trobar-lo als documents associats del projecte del [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="75f5e-170">You can upload your Project file to SharePoint and find it under the Associated Documents for your [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] project.</span></span>  <span data-ttu-id="75f5e-171">Heu de demanar a l'administrador que configuri l'administració de documents del SharePoint i l'activi per a l'entitat del Project.</span><span class="sxs-lookup"><span data-stu-id="75f5e-171">You need to have your administrator configure SharePoint document management and turn it on for the Project entity.</span></span> 

 <span data-ttu-id="75f5e-172">També podeu carregar el fitxer del Project al [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)] si heu configurat els Grups de l'Office.</span><span class="sxs-lookup"><span data-stu-id="75f5e-172">You can also upload your Project file to [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)] if you have Office Groups set up.</span></span>

### <a name="upload-a-file-for-sharepoint"></a><span data-ttu-id="75f5e-173">Pujar un fitxer per al SharePoint</span><span class="sxs-lookup"><span data-stu-id="75f5e-173">Upload a file for SharePoint</span></span>  

1. <span data-ttu-id="75f5e-174">Des del menú principal, feu clic a **Project Service** > **Carrega**.</span><span class="sxs-lookup"><span data-stu-id="75f5e-174">From the main menu, click **Project Service** > **Upload**.</span></span>  

2. <span data-ttu-id="75f5e-175">Seleccioneu **Als documents del projecte de Project Service Automation**.</span><span class="sxs-lookup"><span data-stu-id="75f5e-175">Select **To Project Service Automation Project Documents**.</span></span>  

3. <span data-ttu-id="75f5e-176">Al diàleg **Permet l'obertura al [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]**, seleccioneu **Sí** o **No**.</span><span class="sxs-lookup"><span data-stu-id="75f5e-176">On the **Enable Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** dialog, select **Yes** or **No**.</span></span>  

   - <span data-ttu-id="75f5e-177">Si feu clic a **Sí**, podreu seleccionar el botó **Obre al [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** al Project Service Automation, executar el [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] i carregar el fitxer del Project de la biblioteca de documents del SharePoint.</span><span class="sxs-lookup"><span data-stu-id="75f5e-177">If you click **Yes**, you'll be able select the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button in Project Service Automation, launch [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], and load the Project file from the SharePoint document library.</span></span>  

   - <span data-ttu-id="75f5e-178">Si feu clic a **No**, l'enllaç del botó **Obre al [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** no funcionarà.</span><span class="sxs-lookup"><span data-stu-id="75f5e-178">If you click **No**, the link for the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button won't work.</span></span>  

4. <span data-ttu-id="75f5e-179">Es pot trobar el fitxer del [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] al [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] a **Documents** per al projecte específic del [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="75f5e-179">The [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] file can be found in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] under **Documents** for the specific [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] project.</span></span>  

### <a name="upload-a-file-for-office-groups"></a><span data-ttu-id="75f5e-180">Carregar un fitxer per als Grups de l'Office</span><span class="sxs-lookup"><span data-stu-id="75f5e-180">Upload a file for Office Groups</span></span>  

1. <span data-ttu-id="75f5e-181">Des del menú principal, feu clic a **Project Service** > **Carrega**.</span><span class="sxs-lookup"><span data-stu-id="75f5e-181">From the main menu, click **Project Service** > **Upload**.</span></span>  

2. <span data-ttu-id="75f5e-182">Seleccioneu **Als documents del projecte de Project Service Automation**.</span><span class="sxs-lookup"><span data-stu-id="75f5e-182">Select **To Project Service Automation Project Documents**.</span></span>  

3. <span data-ttu-id="75f5e-183">Al diàleg **Permet l'obertura al [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]**, seleccioneu **Sí** o **No**.</span><span class="sxs-lookup"><span data-stu-id="75f5e-183">On the **Enable Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** dialog, select **Yes** or **No**.</span></span>  

   - <span data-ttu-id="75f5e-184">Si feu clic a **Sí**, podreu seleccionar el botó **Obre al [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** al Project Service Automation, executar el [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] i carregar el fitxer del Project de la biblioteca de documents del SharePoint.</span><span class="sxs-lookup"><span data-stu-id="75f5e-184">If you click **Yes**, you'll be able to select the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button in Project Service Automation, launch [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], and load the Project file from the SharePoint document library.</span></span>  

   - <span data-ttu-id="75f5e-185">Si feu clic a **No**, l'enllaç del botó **Obre al [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** no funcionarà.</span><span class="sxs-lookup"><span data-stu-id="75f5e-185">If you click **No**, the link for the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button won't work.</span></span>  

4. <span data-ttu-id="75f5e-186">Es pot trobar el fitxer del [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] al [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] a **Documents** per al projecte específic del [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="75f5e-186">The [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] file can be found in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] under **Documents** for the specific [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] project.</span></span>  

## <a name="publish--your-project-as-a-template"></a><span data-ttu-id="75f5e-187">Publicar el vostre projecte com a plantilla</span><span class="sxs-lookup"><span data-stu-id="75f5e-187">Publish  your project as a template</span></span>  
 <span data-ttu-id="75f5e-188">Podeu desar el vostre projecte i reutilitzar-lo desant-lo com a plantilla de projecte al [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="75f5e-188">You can save your project and reuse it by saving it as a project template in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  <span data-ttu-id="75f5e-189">Les plantilles de projecte són plans de projecte reutilitzables al [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="75f5e-189">Project templates are reusable project plans in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="75f5e-190">[Crear una plantilla de projecte (Project Service Automation)](../psa/create-project-template.md)</span><span class="sxs-lookup"><span data-stu-id="75f5e-190">[Create a project template (Project Service Automation)](../psa/create-project-template.md)</span></span>  

1. <span data-ttu-id="75f5e-191">A la pestanya **Project Service**, feu clic a **Publica** > **Nova plantilla de projecte del Project Service Automation**.</span><span class="sxs-lookup"><span data-stu-id="75f5e-191">From the **Project Service** tab, click **Publish** > **New Project Service Automation Project Template**.</span></span>  

2. <span data-ttu-id="75f5e-192">Al quadre de diàleg **Publicació en una plantilla nova del Project Service**, introduïu el **Nom de la plantilla del projecte**.</span><span class="sxs-lookup"><span data-stu-id="75f5e-192">On the **Publish to a new project in Project Service template** dialog box, enter the **Project template name**.</span></span>  

3. <span data-ttu-id="75f5e-193">De forma opcional, marqueu la casella **Enllaça el pla de projecte al Project Service Automation** per enllaçar el fitxer del Project al [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="75f5e-193">Optionally, check the **Link project plan to Project Service Automation** to link the Project file to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

4. <span data-ttu-id="75f5e-194">Feu clic a **Publica**.</span><span class="sxs-lookup"><span data-stu-id="75f5e-194">Click **Publish**.</span></span>  

<span data-ttu-id="75f5e-195">Enllaçar el fitxer del Project al [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] farà que el fitxer del Project sigui el fitxer mestre i defineix l'estructura del desglossament del treball al [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] com plantilla només de lectura.</span><span class="sxs-lookup"><span data-stu-id="75f5e-195">Linking the Project file to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] makes the Project file the master and sets the work breakdown structure in the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] template to read-only.</span></span>  <span data-ttu-id="75f5e-196">Per fer canvis al pla del projecte, cal fer-los al [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] i publicar-los com a actualitzacions del [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="75f5e-196">In order to make changes to the project plan, you need to make them in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and publish them as updates to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>

### <a name="see-also"></a><span data-ttu-id="75f5e-197">Vegeu també</span><span class="sxs-lookup"><span data-stu-id="75f5e-197">See Also</span></span>  
 [<span data-ttu-id="75f5e-198">Guia d'administrador de projectes</span><span class="sxs-lookup"><span data-stu-id="75f5e-198">Project Manager Guide</span></span>](../psa/project-manager-guide.md)
