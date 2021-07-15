---
title: Integració del Microsoft Project Client
description: La planificació i el manteniment d'una planificació de projecte poden ser complexos, de manera que els administradors de projectes han d'utilitzar eines que els ajudin a administrar aquesta tasca. La integració amb el Microsoft Project Client proporciona suport per obrir i administrar una estructura de desglossament del treball del projecte.
author: Yowelle
ms.date: 06/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: b312ec5b1f4e6a98a2cbf1667b2f55b758b2d613
ms.sourcegitcommit: 3a4b181be08ef0428104d72b54a3e61ac2782f14
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/17/2021
ms.locfileid: "6269823"
---
# <a name="microsoft-project-client-integration"></a><span data-ttu-id="9950b-104">Integració del Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="9950b-104">Microsoft Project client integration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9950b-105">La planificació i el manteniment d'una planificació de projecte poden ser complexos, de manera que els administradors de projectes han d'utilitzar eines que els ajudin a administrar aquesta tasca.</span><span class="sxs-lookup"><span data-stu-id="9950b-105">Planning and maintaining a project schedule can be complex, so project managers need to use tools that help them manage this task.</span></span> <span data-ttu-id="9950b-106">La integració amb el Microsoft Project Client proporciona suport per obrir i administrar una estructura de desglossament del treball del projecte.</span><span class="sxs-lookup"><span data-stu-id="9950b-106">Integration with Microsoft Project Client provides support to open and manage a project work breakdown structure.</span></span> <span data-ttu-id="9950b-107">L'administrador del projecte pot publicar qualsevol canvi a l'estructura del desglossament del treball del projecte del Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="9950b-107">The project manager can publish any changes back to the Dynamics 365 Finance project work breakdown structure.</span></span>

> [!NOTE]
> <span data-ttu-id="9950b-108">Si utilitzeu l'actualització de juliol (versió 10.0.4), heu d'instal·lar els KB 4054797 i el 4055884.</span><span class="sxs-lookup"><span data-stu-id="9950b-108">If you are using the July update (version 10.0.4), you must install KB 4054797 and 4055884.</span></span>

## <a name="configure-the-microsoft-project-client-add-in"></a><span data-ttu-id="9950b-109">Configurar el complement del Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="9950b-109">Configure the Microsoft Project Client add-in</span></span>
<span data-ttu-id="9950b-110">Per habilitar la integració amb el Microsoft Project Client, cal que s'instal·li un complement del Microsoft Dynamics 365 a l'aplicació client del Microsoft Project de l'usuari.</span><span class="sxs-lookup"><span data-stu-id="9950b-110">To enable the integration with Microsoft Project Client, a Microsoft Dynamics 365 add-in is required to be installed in the user’s client Microsoft Project application.</span></span> <span data-ttu-id="9950b-111">Això es fa obrint l'**àrea de treball Administració de projectes**.</span><span class="sxs-lookup"><span data-stu-id="9950b-111">This is done by opening the **Project management workspace**.</span></span>

<span data-ttu-id="9950b-112">• Feu clic a **Configura el complement de client del Project** des de la secció **Enllaços** > **Configuració** de l'àrea de treball.</span><span class="sxs-lookup"><span data-stu-id="9950b-112">•   Click **Configure project client add-in** from the **Links** > **Setup** section of the workspace.</span></span>

<span data-ttu-id="9950b-113">• Feu clic a **Obre** i, a continuació, feu clic a **Executa** quan se us demani.</span><span class="sxs-lookup"><span data-stu-id="9950b-113">•   Click **Open**, then click **Run** when prompted.</span></span>

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a><span data-ttu-id="9950b-114">Obrir i editar una estructura de desglossament del treball existent d'esborrany al Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="9950b-114">Open and edit an existing draft work breakdown structure in Microsoft Project Client</span></span>
<span data-ttu-id="9950b-115">Si un projecte del Dynamics 365 Finance ja té una estructura de desglossament del treball creada, l'estructura del desglossament del treball es pot obrir a l'aplicació Microsoft Project Client si l'estructura del desglossament del treball està en un estat d'esborrany.</span><span class="sxs-lookup"><span data-stu-id="9950b-115">If a project in Dynamics 365 Finance already has a work breakdown structure created, the work breakdown structure can be opened in the Microsoft Project Client application if the work breakdown structure is in a draft status.</span></span> <span data-ttu-id="9950b-116">Per obrir-la des de la pàgina **Projecte**, feu clic a l'enllaç **Obre al Microsoft Project** des de la pestanya **Pla**. Aquesta pàgina també es pot obrir des de l'aplicació Microsoft Project Client fent clic a **Obre** la pestanya **Microsoft Dynamics 365**. Seleccioneu una **Entitat jurídica** i **Projecte** de la llista.</span><span class="sxs-lookup"><span data-stu-id="9950b-116">To open from the **Project** page, click **Open in Microsoft Project** link from the **Plan** tab. This page can also be opened from within the Microsoft Project Client application by clicking **Open** in the **Microsoft Dynamics 365** tab. Select the **Legal entity** and **Project** from the list.</span></span>

> [!NOTE]
> <span data-ttu-id="9950b-117">Si utilitzeu l'Internet Explorer com a navegador, haureu de fer clic a **Desa** per obrir manualment la ubicació a la qual es descarrega el fitxer.</span><span class="sxs-lookup"><span data-stu-id="9950b-117">If you're using Internet Explorer as your browser, you will need to click **Save** to manually open from the location that the file is downloaded to.</span></span> <span data-ttu-id="9950b-118">O bé, feu clic a **Desa i obre** per obrir el fitxer Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="9950b-118">Or, click **Save and open** to open the file in Microsoft Project Client.</span></span> <span data-ttu-id="9950b-119">No canvieu el nom del fitxer en desar-lo.</span><span class="sxs-lookup"><span data-stu-id="9950b-119">Do not rename the file name when saving.</span></span>

<span data-ttu-id="9950b-120">Abans de fer cap modificació al fitxer amb el Microsoft Project Client, heu de desprotegir-lo. Feu clic **Desprotegeix** a la pestanya **Microsoft Dynamics 365**. Això evitarà que altres usuaris editin l'estructura del desglossament del treball des del Finance al mateix temps.</span><span class="sxs-lookup"><span data-stu-id="9950b-120">Before making any edits to the file using Microsoft Project Client, you need to check it out. Click **Check out** in the **Microsoft Dynamics 365** tab. This will prevent other users from editing the work breakdown structure from within Finance at the same time.</span></span> <span data-ttu-id="9950b-121">Per publicar l'estructura del desglossament de la feina després d'haver completat les edicions, feu clic **Protegeix** a la pestanya **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="9950b-121">To publish the work breakdown structure after completing any edits, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

<span data-ttu-id="9950b-122">Si un equip del projecte ja s'ha afegit al projecte al Finance, la llista de recursos s'emplenarà amb els membres de l'equip.</span><span class="sxs-lookup"><span data-stu-id="9950b-122">If a project team has already been added to the project in Finance, the resource list will be populated with the team members.</span></span> <span data-ttu-id="9950b-123">Si encara no s'ha afegit un equip del projecte al projecte, podeu seleccionar recursos i crear l'equip al Microsoft Project Client fent clic al botó **Recursos** de la pestanya **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="9950b-123">If a project team has not yet been added to the project, you can select resources and build the team within Microsoft Project Client by clicking the **Resources** button on the **Microsoft Dynamics 365** tab.</span></span> 

<span data-ttu-id="9950b-124">Les dades següents se sincronitzen de nou al Finance com a part del procés de desprotecció:</span><span class="sxs-lookup"><span data-stu-id="9950b-124">The following data will be synced back to Finance as part of the check-in process:</span></span>

<span data-ttu-id="9950b-125">• Nom de la tasca</span><span class="sxs-lookup"><span data-stu-id="9950b-125">•   Task name</span></span>

<span data-ttu-id="9950b-126">• Data d'inici</span><span class="sxs-lookup"><span data-stu-id="9950b-126">•   Start date</span></span>

<span data-ttu-id="9950b-127">• Data de finalització</span><span class="sxs-lookup"><span data-stu-id="9950b-127">•   Finish date</span></span>

<span data-ttu-id="9950b-128">• Predecessors</span><span class="sxs-lookup"><span data-stu-id="9950b-128">•   Predecessors</span></span>

<span data-ttu-id="9950b-129">• Noms dels recursos</span><span class="sxs-lookup"><span data-stu-id="9950b-129">•   Resource names</span></span>

<span data-ttu-id="9950b-130">• Categoria</span><span class="sxs-lookup"><span data-stu-id="9950b-130">•   Category</span></span>

<span data-ttu-id="9950b-131">• Categoria del recurs</span><span class="sxs-lookup"><span data-stu-id="9950b-131">•   Resource category</span></span>

<span data-ttu-id="9950b-132">• Hores de treball</span><span class="sxs-lookup"><span data-stu-id="9950b-132">•   Work hours</span></span>

<span data-ttu-id="9950b-133">• Notes</span><span class="sxs-lookup"><span data-stu-id="9950b-133">•   Notes</span></span>

<span data-ttu-id="9950b-134">• Prioritat</span><span class="sxs-lookup"><span data-stu-id="9950b-134">•   Priority</span></span>

> [!NOTE]
> <span data-ttu-id="9950b-135">Si afegiu altres columnes al fitxer del Microsoft Project Client, no es desaran al fitxer i no es mostraran quan el fitxer torni a obrir-se.</span><span class="sxs-lookup"><span data-stu-id="9950b-135">If you add any other columns to your Microsoft Project Client file, they will not be saved to the file and will not be displayed when the file is opened again.</span></span>

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="9950b-136">Crear l'estructura del desglossament del treball per a un projecte existent amb Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="9950b-136">Create the work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="9950b-137">Per crear una nova estructura del desglossament del treball amb el Microsoft Project Client, seguiu aquests passos:</span><span class="sxs-lookup"><span data-stu-id="9950b-137">To create a new work breakdown structure using Microsoft Project Client, follow these steps:</span></span>


1.  <span data-ttu-id="9950b-138">Obriu el Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="9950b-138">Open Microsoft Project Client.</span></span>

2.  <span data-ttu-id="9950b-139">A la pestanya **Microsoft Dynamics 365**, feu clic a **Obre**.</span><span class="sxs-lookup"><span data-stu-id="9950b-139">On the **Microsoft Dynamics 365** tab, click **Open**.</span></span>

3.  <span data-ttu-id="9950b-140">Seleccioneu l'**Entitat jurídica** per al projecte.</span><span class="sxs-lookup"><span data-stu-id="9950b-140">Select the **Legal entity** for the project.</span></span>

4.  <span data-ttu-id="9950b-141">Seleccioneu el **Projecte**.</span><span class="sxs-lookup"><span data-stu-id="9950b-141">Select the **Project**.</span></span>

5.  <span data-ttu-id="9950b-142">Feu clic a **Desprotegeix** a la pestanya **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="9950b-142">Click **Check out** on the **Microsoft Dynamics 365** tab.</span></span>

6.  <span data-ttu-id="9950b-143">Quan estigueu a punt per publicar-ho al Finance, feu clic a **Protegeix** a la pestanya **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="9950b-143">When ready to publish to Finance, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="9950b-144">Substituir l'estructura del desglossament del treball existent per a un projecte existent amb Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="9950b-144">Replace the existing work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="9950b-145">Per crear una nova estructura del desglossament del treball amb el Microsoft Project Client i substituir una estructura del desglossament del treball existent per a un projecte existent, seguiu aquests passos:</span><span class="sxs-lookup"><span data-stu-id="9950b-145">To create a new work breakdown structure using Microsoft Project Client and replace an existing work breakdown structure for an existing project, follow these steps:</span></span>

1.  <span data-ttu-id="9950b-146">Obriu el Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="9950b-146">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="9950b-147">Creeu una planificació al Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="9950b-147">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="9950b-148">A la pestanya **Microsoft Dynamics 365**, feu clic a **Desa els canvis** > **Substitueix un projecte existent**.</span><span class="sxs-lookup"><span data-stu-id="9950b-148">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Replace existing project**.</span></span>

4.  <span data-ttu-id="9950b-149">Seleccioneu l'**Entitat jurídica** per al projecte.</span><span class="sxs-lookup"><span data-stu-id="9950b-149">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="9950b-150">Seleccioneu el **Projecte**.</span><span class="sxs-lookup"><span data-stu-id="9950b-150">Select the **Project**.</span></span>

6.  <span data-ttu-id="9950b-151">Feu clic a **D'acord**.</span><span class="sxs-lookup"><span data-stu-id="9950b-151">Click **OK**.</span></span>

## <a name="create-a-new-project-from-within-microsoft-project-client"></a><span data-ttu-id="9950b-152">Crear un projecte nou des del Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="9950b-152">Create a new project from within Microsoft Project Client</span></span>


1.  <span data-ttu-id="9950b-153">Obriu el Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="9950b-153">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="9950b-154">Creeu una planificació al Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="9950b-154">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="9950b-155">A la pestanya **Microsoft Dynamics 365**, feu clic a **Desa els canvis** > **Desa en un projecte nou**.</span><span class="sxs-lookup"><span data-stu-id="9950b-155">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Save to new Project**.</span></span>

4.  <span data-ttu-id="9950b-156">Seleccioneu l'**Entitat jurídica** per al projecte.</span><span class="sxs-lookup"><span data-stu-id="9950b-156">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="9950b-157">Introduïu l'**Identificador del projecte**, si cal.</span><span class="sxs-lookup"><span data-stu-id="9950b-157">Enter the **Project ID**, if necessary.</span></span>

6.  <span data-ttu-id="9950b-158">Introduïu el **Nom del projecte**.</span><span class="sxs-lookup"><span data-stu-id="9950b-158">Enter the **Project name**.</span></span>

7.  <span data-ttu-id="9950b-159">Seleccioneu el **Tipus de projecte**, el **Grup de projectes** i l'**Identificador del contracte del projecte**.</span><span class="sxs-lookup"><span data-stu-id="9950b-159">Select the **Project type**, **Project group** and the **Project contract ID**.</span></span> <span data-ttu-id="9950b-160">O bé, podeu crear un contracte de projecte nou fent clic a **Nou**.</span><span class="sxs-lookup"><span data-stu-id="9950b-160">Alternatively, you can create a new project contract by clicking **New**.</span></span>

8.  <span data-ttu-id="9950b-161">Seleccioneu el **calendari** que s'utilitzarà per als recursos.</span><span class="sxs-lookup"><span data-stu-id="9950b-161">Select the **Calendar** to be used for resourcing.</span></span>

11. <span data-ttu-id="9950b-162">Feu clic a **D'acord**.</span><span class="sxs-lookup"><span data-stu-id="9950b-162">Click **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="9950b-163">El complement Client del projecte no admet els caràcters següents per al format d'ID del projecte:</span><span class="sxs-lookup"><span data-stu-id="9950b-163">The Project Client add-in doesn’t support the following characters in the project ID format:</span></span>
> 
>   - <span data-ttu-id="9950b-164">Subratllat</span><span class="sxs-lookup"><span data-stu-id="9950b-164">Underscore</span></span>
>   - <span data-ttu-id="9950b-165">Període</span><span class="sxs-lookup"><span data-stu-id="9950b-165">Period</span></span>
>   - <span data-ttu-id="9950b-166">Espai</span><span class="sxs-lookup"><span data-stu-id="9950b-166">Space</span></span>
>   - <span data-ttu-id="9950b-167">Barra</span><span class="sxs-lookup"><span data-stu-id="9950b-167">Slash</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
