---
title: Com puc personalitzar el flux del procés de negoci del Project Stages?
description: Informació general sobre com personalitzar el flux del procés de negoci de les fases del projecte.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 10/11/2018
ms.topic: article
author: JohnPBurrows
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: a999bbffff848db7a6349df380d9ed5e73c143ab
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4125015"
---
# <a name="how-do-i-customize-the-project-stages-business-process-flow"></a><span data-ttu-id="b9fba-103">Com puc personalitzar el flux del procés de negoci del Project Stages?</span><span class="sxs-lookup"><span data-stu-id="b9fba-103">How do I customize the Project Stages business process flow?</span></span>
[!INCLUDE[cc-applies-to-psa-app-2-4x-9-0-platform](../includes/cc-applies-to-psa-app-2-4x-9-0-platform.md)]
[!INCLUDE[cc-applies-to-psa-app-1x-8-2-platform](../includes/cc-applies-to-psa-app-1x-8-2-platform.md)]

<span data-ttu-id="b9fba-104">Hi ha una limitació coneguda en les versions anteriors de l'aplicació del Project Service que els noms de les etapes en el flux del procés de negoci del Project Stages han de coincidir exactament amb els noms esperats en anglès (**Quote**, **Plan**, **Close**).</span><span class="sxs-lookup"><span data-stu-id="b9fba-104">There's a known limitation in earlier versions of the Project Service application that the names of the stages in the Project Stages business process flow must exactly match the expected English names (**Quote**, **Plan**, **Close**).</span></span> <span data-ttu-id="b9fba-105">En cas contrari, la lògica empresarial, que es basa en els noms de les etapes en anglès, no funcionarà com s'espera.</span><span class="sxs-lookup"><span data-stu-id="b9fba-105">Otherwise, the business logic, which relies on the English stage names, doesn't work as expected.</span></span> <span data-ttu-id="b9fba-106">És per això que no hi ha accions familiars com **Canvia el procés** o **Edita el procés** disponibles al formulari del projecte i no es recomana personalitzar el flux del procés de negoci.</span><span class="sxs-lookup"><span data-stu-id="b9fba-106">That's why you don't see familiar actions such as **Switch Process** or **Edit Process** available on the project form, and customizing the business process flow isn't encouraged.</span></span> 

<span data-ttu-id="b9fba-107">Aquesta limitació s'ha corregit a la versió 2.4.5.48 i posterior.</span><span class="sxs-lookup"><span data-stu-id="b9fba-107">This limitation has been addressed in version 2.4.5.48 and later.</span></span> <span data-ttu-id="b9fba-108">Aquest article proporciona solucions alternatives suggerides per si ha de personalitzar el flux del procés de negoci predeterminat en versions anteriors.</span><span class="sxs-lookup"><span data-stu-id="b9fba-108">This article provides suggested workarounds if you need to customize the default business process flow for earlier versions.</span></span>  

## <a name="business-logic-requires-an-exact-match-with-english-stage-names"></a><span data-ttu-id="b9fba-109">La lògica empresarial requereix una coincidència exacta amb els noms de les etapes en anglès</span><span class="sxs-lookup"><span data-stu-id="b9fba-109">Business logic requires an exact match with English stage names</span></span>

<span data-ttu-id="b9fba-110">El flux del procés de negoci del Project Stages inclou la lògica empresarial que impulsa els següents comportaments en l'aplicació:</span><span class="sxs-lookup"><span data-stu-id="b9fba-110">The Project Stages business process flow includes business logic that drives the following behaviors in the app:</span></span>
- <span data-ttu-id="b9fba-111">Quan el projecte està associat a una oferta, el codi estableix el flux del procés de negoci en l'etapa de **Quote**.</span><span class="sxs-lookup"><span data-stu-id="b9fba-111">When the project is associated with a quote, the code sets the business process flow to the **Quote** stage.</span></span>
- <span data-ttu-id="b9fba-112">Quan el projecte està associat a un contracte, el codi estableix el flux del procés de negoci en l'etapa de **Plan**.</span><span class="sxs-lookup"><span data-stu-id="b9fba-112">When the project is associated with a contract, the code sets the business process flow to the **Plan** stage.</span></span>
- <span data-ttu-id="b9fba-113">Quan el flux del procés de negoci avança fins a l'etapa **Close**, el registre del projecte es desactiva.</span><span class="sxs-lookup"><span data-stu-id="b9fba-113">When the business process flow is advanced to the **Close** stage, the project record is deactivated.</span></span> <span data-ttu-id="b9fba-114">Quan el projecte està desactivat, el formulari del projecte i l'estructura del desglossament del treball (WBS) es configuren com de només lectura, es publiquen les reserves de recursos amb nom i es desactiven les llistes de preus associades.</span><span class="sxs-lookup"><span data-stu-id="b9fba-114">When the project is deactivated, the project form and work breakdown structure (WBS) are set to read-only, the named resource bookings are released, and any associated price lists are deactivated.</span></span>

<span data-ttu-id="b9fba-115">Aquesta lògica empresarial es basa en els noms en anglès per a les etapes del projecte.</span><span class="sxs-lookup"><span data-stu-id="b9fba-115">This business logic relies on the English names for the project stages.</span></span> <span data-ttu-id="b9fba-116">Aquesta dependència dels noms d'etapa en anglès és la principal raó per la qual no es recomana personalitzar el flux del procés de negoci del Project Stages, i per la qual no es veuen les accions comunes com **Canvia el procés** o **Edita el procés** a l'entitat del projecte.</span><span class="sxs-lookup"><span data-stu-id="b9fba-116">This dependency on the English stage names is the main reason why customization of the Project Stages business process flow isn't encouraged, as well as why you don’t see the common business process flow actions like **Switch Process** or **Edit Process** on the project entity.</span></span>

## <a name="what-happens-if-the-stage-names-dont-match-the-english-names"></a><span data-ttu-id="b9fba-117">Què passa si els noms de les etapes no coincideixen amb els noms en anglès?</span><span class="sxs-lookup"><span data-stu-id="b9fba-117">What happens if the stage names don't match the English names?</span></span>

<span data-ttu-id="b9fba-118">En la versió 1.x de l'aplicació Project Service a la plataforma 8.2, quan els noms d'etapa en el flux del procés de negoci no coincideixen exactament amb els noms d'etapa en anglès, s'omet la lògica empresarial que estableix la fase correcta per a ofertes o contractes, o que tanca el projecte.</span><span class="sxs-lookup"><span data-stu-id="b9fba-118">In the Project Service app version 1.x on the 8.2 platform, when the stage names in the business process flow don’t match the English stage names exactly, the business logic that sets the right stage for quotes or contracts, or that closes the project, is skipped.</span></span> <span data-ttu-id="b9fba-119">No es mostren missatges d'error.</span><span class="sxs-lookup"><span data-stu-id="b9fba-119">No error messages are displayed.</span></span> <span data-ttu-id="b9fba-120">Per tant, sembla que podeu personalitzar el flux del procés de negoci del Project Stages.</span><span class="sxs-lookup"><span data-stu-id="b9fba-120">Therefore it appears that you are able to customize the Project Stages business process flow.</span></span> <span data-ttu-id="b9fba-121">No obstant això, no veureu cap dels processos automàtics treballant per a ofertes, contractes ni tancament de projecte.</span><span class="sxs-lookup"><span data-stu-id="b9fba-121">However, you won’t see any of the automatic processes working for quotes, contracts, and project close.</span></span>

<span data-ttu-id="b9fba-122">A l'aplicació del Project Service versió 2.4.4.30 o anterior a la plataforma 9.0, hi va haver un canvi arquitectònic significatiu en els fluxos del procés de negoci que va requerir una reescriptura de la lògica empresarial.</span><span class="sxs-lookup"><span data-stu-id="b9fba-122">In the Project Service app version 2.4.4.30 or earlier on the 9.0 platform, there was a significant architectural change to business process flows, which required a re-write of the business process flow business logic.</span></span> <span data-ttu-id="b9fba-123">Com a resultat, si els noms d'etapa del procés no coincideixen amb els noms en anglès esperats, apareixerà un missatge d'error.</span><span class="sxs-lookup"><span data-stu-id="b9fba-123">As a result, if the process stage names don’t match the expected English names, you do receive an error message.</span></span> 

<span data-ttu-id="b9fba-124">Per tant, si desitgeu personalitzar el flux del procés de negoci del Project Stages per a l'entitat del projecte, només podreu afegir noves etapes al flux predeterminat per l'entitat del projecte, si manteniu les fases **Quote**, **Plan** i **Close** tal com estan.</span><span class="sxs-lookup"><span data-stu-id="b9fba-124">Therefore, if you want to customize the Project Stages business process flow for the project entity, you can only add brand new stages to the default business process flow for the project entity, while keeping the **Quote**, **Plan**, and **Close** stages as-is.</span></span> <span data-ttu-id="b9fba-125">Aquesta restricció garanteix que no apareguin errors de lògica empresarial que esperen els noms de les fases en anglès en el flux del procés de negoci.</span><span class="sxs-lookup"><span data-stu-id="b9fba-125">This restriction ensures that you don’t get errors from the business logic that expects the English stage names in the business process flow.</span></span>

<span data-ttu-id="b9fba-126">En la versió 2.4.5.48 o posterior, la lògica empresarial descrita en aquest article s'ha eliminat del flux del procés de negoci predeterminat per l'entitat del projecte.</span><span class="sxs-lookup"><span data-stu-id="b9fba-126">In version 2.4.5.48 or later, the business logic described in this article has been removed from the default business process flow for the project entity.</span></span> <span data-ttu-id="b9fba-127">L'actualització a aquesta versió o posterior permetrà personalitzar o reemplaçar el flux del procés de negoci predeterminat per un de propi.</span><span class="sxs-lookup"><span data-stu-id="b9fba-127">Upgrading to that version or later will let you customize or replace the default business process flow with one of your own.</span></span> 

## <a name="workarounds-for-earlier-versions"></a><span data-ttu-id="b9fba-128">Solucions provisionals per a versions anteriors</span><span class="sxs-lookup"><span data-stu-id="b9fba-128">Workarounds for earlier versions</span></span>

<span data-ttu-id="b9fba-129">Si l'actualització no és una opció, podeu personalitzar el flux del procés de negoci del Project Stages per a l'entitat del projecte d'una d'aquestes dues maneres:</span><span class="sxs-lookup"><span data-stu-id="b9fba-129">If upgrading isn't an option, you can customize the Project Stages business process flow for the project entity in one of these two ways:</span></span>

1. <span data-ttu-id="b9fba-130">Afegiu fases addicionals a la configuració per defecte i conserveu els noms en anglès per a **Quote**, **Plan** i **Close**.</span><span class="sxs-lookup"><span data-stu-id="b9fba-130">Add additional stages to the default configuration, while retaining the English stage names for **Quote**, **Plan**, and **Close**.</span></span>


![Captura de pantalla que mostra com afegir fases a la configuració per defecte](media/FAQ-Customize-BPF-1.png)
 
2. <span data-ttu-id="b9fba-132">Creu el vostre propi flux del procés de negoci i convertiu-lo en el flux principal per a l'entitat del projecte i podreu tenir els noms que vulgueu per a les fases.</span><span class="sxs-lookup"><span data-stu-id="b9fba-132">Create your own business process flow and make it the primary business process flow for the project entity, which lets you have any stage names you want.</span></span> <span data-ttu-id="b9fba-133">No obstant això, si voleu utilitzar les mateixes fases de projecte estàndard **Quote**, **Plan** i **Close**, heu de realitzar algunes personalitzacions que eliminaran els vostres noms personalitzats.</span><span class="sxs-lookup"><span data-stu-id="b9fba-133">However, if you want to use the same standard project stages **Quote**, **Plan**, and **Close**, you need to do some customizations that are driven off your custom stage names.</span></span> <span data-ttu-id="b9fba-134">La lògica més complexa es troba en el tancament del projecte però la podeu activar simplement desactivant el registre del projecte.</span><span class="sxs-lookup"><span data-stu-id="b9fba-134">The more complex logic is in the closing of the project, which you can still trigger by just deactivating the project record.</span></span>

![Personalització del BPF](media/FAQ-Customize-BPF-2.png)

### <a name="additional-considerations-for-project-service-app-version-24430-or-earlier-on-platform-90"></a><span data-ttu-id="b9fba-136">Consideracions addicionals per a l'aplicació Project Service versió 2.4.4.30 o anterior a la plataforma 9.</span><span class="sxs-lookup"><span data-stu-id="b9fba-136">Additional considerations for Project Service app version 2.4.4.30 or earlier on platform 9.0</span></span>

<span data-ttu-id="b9fba-137">Al Project Service 2.4.4.30 o anterior a la plataforma 9.0, amb un flux del procés de negoci personalitzat, el camp **Nom de fase** en l'entitat de projecte que s'utilitza en el gràfic **Projecte per fase** i les vistes de llista de projectes no s'actualitzaran, perquè està acoblat al flux del procés de negoci de les fases del projecte per defecte.</span><span class="sxs-lookup"><span data-stu-id="b9fba-137">In Project Service 2.4.4.30 or earlier on platform 9.0, with a custom business process flow the **Stage Name** field on the project entity used in the **Project By Stage** chart and project list views won’t update, because it’s coupled to the default Project Stages business process flow.</span></span> <span data-ttu-id="b9fba-138">Podeu solucionar aquest problema amb els passos següents:</span><span class="sxs-lookup"><span data-stu-id="b9fba-138">You can address this issue with the following steps:</span></span>

- <span data-ttu-id="b9fba-139">Afegiu un camp personalitzat per capturar la fase del flux del procés de negoci actual que s'actualitza a mesura que l'usuari avança a través del flux personalitzat.</span><span class="sxs-lookup"><span data-stu-id="b9fba-139">Add a custom field to capture the current business process flow stage that is updated as the user advances through the custom business process flow.</span></span>

- <span data-ttu-id="b9fba-140">Modifiqueu el gràfic **Projecte per fase** perquè funcioni amb el vostre camp personalitzat en lloc de amb la configuració predeterminada.</span><span class="sxs-lookup"><span data-stu-id="b9fba-140">Modify the **Project By Stage** chart to work with your custom field instead of the default configuration.</span></span>

### <a name="steps-to-create-your-own-business-process-flow-for-the-project-entity"></a><span data-ttu-id="b9fba-141">Passos per crear el vostre propi flux del procés de negoci per a l'entitat del projecte</span><span class="sxs-lookup"><span data-stu-id="b9fba-141">Steps to create your own business process flow for the project entity</span></span>

<span data-ttu-id="b9fba-142">Per crear el vostre propi flux del procés de negoci per a l'entitat del projecte, feu el següent:</span><span class="sxs-lookup"><span data-stu-id="b9fba-142">To create your own business process flow for the project entity do the following:</span></span>

1. <span data-ttu-id="b9fba-143">Aneu a **Configuració** > **Centre de processos**.</span><span class="sxs-lookup"><span data-stu-id="b9fba-143">Go to **Settings** > **Process Center**.</span></span> <span data-ttu-id="b9fba-144">No copieu el flux del procés de negoci de les Etapes del projecte perquè aquesta acció també copia la lògica de negocis del Project Service.</span><span class="sxs-lookup"><span data-stu-id="b9fba-144">Don’t copy the Project Stages business process flow because that also copies the Project Service business logic.</span></span>

  ![Crear un procés](media/FAQ-Customize-BPF-3.png)

2. <span data-ttu-id="b9fba-146">Utilitzeu el Dissenyador de processos per crear els noms de fases que desitgeu.</span><span class="sxs-lookup"><span data-stu-id="b9fba-146">Use the Process Designer to create the stage names you want.</span></span> <span data-ttu-id="b9fba-147">Si desitgeu la mateixa funcionalitat que les fases predeterminades per a **Quote**, **Plan** i **Close**, haureu de crear-la en funció dels noms de fase del flux del procés de negoci personalitzats.</span><span class="sxs-lookup"><span data-stu-id="b9fba-147">If you want the same functionality as the default stages for **Quote**, **Plan**, and **Close**, you’ll have to create that based on your custom business process flow’s stage names.</span></span>

   ![Captura de pantalla del dissenyador de processos utilitzat per personalitzar BPF](media/FAQ-Customize-BPF-4.png) 

3. <span data-ttu-id="b9fba-149">En el Dissenyador de processos, feu clic a **Flux del procés de la comanda** per fer que el flux del procés de negoci personalitzat sigui el flux principal per a l'entitat del projecte, moveu-lo per sobre del flux de les Fases del projecte al principi de la llista.</span><span class="sxs-lookup"><span data-stu-id="b9fba-149">In the Process Designer, click **Order Process Flow** to make the custom business process flow the primary business process flow for the project entity by moving it above the Project Stages business process flow to the top of the list.</span></span>


   [<span data-ttu-id="b9fba-150">Captura de pantalla de l'ús del Flux del procés de la comanda</span><span class="sxs-lookup"><span data-stu-id="b9fba-150">Screenshot of using Order Process Flow</span></span>](media/FAQ-Customize-BPF-5-720.png)

### <a name="the-following-steps-apply-to-project-service-app-24430-or-earlier-on-the-90-platform"></a><span data-ttu-id="b9fba-151">Els següents passos s'apliquen a l'aplicació del Project Service 2.4.4.30 o anterior a la plataforma 9.0</span><span class="sxs-lookup"><span data-stu-id="b9fba-151">The following steps apply to Project Service app 2.4.4.30 or earlier on the 9.0 platform</span></span>

4. <span data-ttu-id="b9fba-152">Afegiu un camp personalitzat nou a l'entitat del projecte per capturar les fases personalitzades al vostre flux del procés de negoci personalitzat.</span><span class="sxs-lookup"><span data-stu-id="b9fba-152">Add a new custom field to the project entity to capture the custom stages in your custom business process flow.</span></span> <span data-ttu-id="b9fba-153">Us cal afegir lògica empresarial (complement/flux de treball) per actualitzar aquest camp quan s'actualitzi la fase en el flux del procés de negoci personalitzat.</span><span class="sxs-lookup"><span data-stu-id="b9fba-153">You’ll need to add business logic (plugin/workflow) to update this field when the stage on the custom business process flow is updated.</span></span>

   ![Captura de pantalla de la personalització de l'entitat del projecte](media/FAQ-Customize-BPF-6-720.png)

5. <span data-ttu-id="b9fba-155">Modifiqueu el gràfic **Projecte per fase** per usar el vostre camp personalitzat nou per a les fases.</span><span class="sxs-lookup"><span data-stu-id="b9fba-155">Modify the **Project By Stage** chart to use your new custom field for stages.</span></span>

   ![Captura de pantalla de l'ús del gràfic Projecte per fase](media/FAQ-Customize-BPF-7-720.png)

6. <span data-ttu-id="b9fba-157">Modifiqueu les vistes de l'entitat del projecte per incloure el vostre camp personalitzat nou per a les fases.</span><span class="sxs-lookup"><span data-stu-id="b9fba-157">Modify any views for the project entity to include your new custom field for stages.</span></span>

   ![Captura de pantalla de la modificació de les visualitzacions de l'entitat del projecte](media/FAQ-Customize-BPF-8-720.png)

