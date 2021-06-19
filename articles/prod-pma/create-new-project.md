---
title: Crear un projecte nou
description: Aquest tema proporciona informació sobre com crear un projecte nou.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8218747366be8536601cb007318c642ac122536b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006229"
---
# <a name="create-a-new-project"></a><span data-ttu-id="349b1-103">Crear un projecte nou</span><span class="sxs-lookup"><span data-stu-id="349b1-103">Create a new project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="349b1-104">Completeu els passos següents per crear un projecte nou.</span><span class="sxs-lookup"><span data-stu-id="349b1-104">Complete the following steps to create a new project.</span></span>

1. <span data-ttu-id="349b1-105">A la pàgina **Administració de projectes**, seleccioneu **Projecte nou** i introduïu els valors següents:</span><span class="sxs-lookup"><span data-stu-id="349b1-105">On the **Project management** page, select **New project**, and enter the following values:</span></span>

    - <span data-ttu-id="349b1-106">**Tipus de projecte:** temps i material</span><span class="sxs-lookup"><span data-stu-id="349b1-106">**Project type:** Time and material</span></span>
    - <span data-ttu-id="349b1-107">**Nom del projecte:** Fase 2 d'actualització d'XYZ</span><span class="sxs-lookup"><span data-stu-id="349b1-107">**Project name:** XYZ Upgrade Phase 2</span></span>
    - <span data-ttu-id="349b1-108">**Grup de projectes:** TM\_WIP</span><span class="sxs-lookup"><span data-stu-id="349b1-108">**Project group:** TM\_WIP</span></span>
    - <span data-ttu-id="349b1-109">**Identificador de contracte de projecte**: 00000002</span><span class="sxs-lookup"><span data-stu-id="349b1-109">**Project contract ID:** 00000002</span></span>

2. <span data-ttu-id="349b1-110">Seleccioneu **Crea el projecte**.</span><span class="sxs-lookup"><span data-stu-id="349b1-110">Select **Create project**.</span></span>

## <a name="assign-a-resource-to-a-project"></a><span data-ttu-id="349b1-111">Assignació d'un recurs a un projecte</span><span class="sxs-lookup"><span data-stu-id="349b1-111">Assign a resource to a project</span></span>

1. <span data-ttu-id="349b1-112">A la pàgina **Treballadors**, a la llista **Treballadors**, seleccioneu el registre del treballador per al qual heu configurat les competències anteriorment i obriu el registre del treballador.</span><span class="sxs-lookup"><span data-stu-id="349b1-112">On the **Workers** page, in the **Workers** list, select the record for the worker that you previously set up competencies for, and open the worker record.</span></span>
2. <span data-ttu-id="349b1-113">A la subfinestra d'acció, a la pestanya **projecte**, al grup **Configuració**, seleccioneu **Assigna projectes**.</span><span class="sxs-lookup"><span data-stu-id="349b1-113">On the Action Pane, on the **Project** tab, in the **Setup** group, select **Assign projects**.</span></span>
3. <span data-ttu-id="349b1-114">A la pàgina **Assignacions de projecte de validació de recursos**, a la pestanya **Projectes**, al camp **Afegeix el projecte als projectes seleccionats**, filtreu el projecte **Fase 2 d'actualització d'XYZ**.</span><span class="sxs-lookup"><span data-stu-id="349b1-114">On the **Resource validation project assignments** page, on the **Projects** tab, in the **Add the project to selected projects** field, filter on the **XYZ Upgrade Phase 2** project.</span></span>
4. <span data-ttu-id="349b1-115">A la subfinestra **Projectes restants**, seleccioneu un projecte i, a continuació, seleccioneu el botó de fletxa per afegir-lo a la subfinestra **Projectes seleccionats**.</span><span class="sxs-lookup"><span data-stu-id="349b1-115">In the **Remaining projects** pane, select a project, and then select the arrow button to add it to the **Selected projects** pane.</span></span>

<span data-ttu-id="349b1-116">També podeu assignar categories per a un recurs a mesura que les necessiteu.</span><span class="sxs-lookup"><span data-stu-id="349b1-116">You can also assign categories for a resource as you require.</span></span> <span data-ttu-id="349b1-117">El tipus de categoria és **Cost** o **Ingrés**.</span><span class="sxs-lookup"><span data-stu-id="349b1-117">The category type is either **Cost** or **Revenue**.</span></span> <span data-ttu-id="349b1-118">El tipus de categoria ve determinat per la vostra organització.</span><span class="sxs-lookup"><span data-stu-id="349b1-118">The category type is determined by your organization.</span></span> <span data-ttu-id="349b1-119">Si no s'assigna cap categoria a un recurs, el Finance cerca la categoria per defecte a preus per hora per als costos i els ingressos.</span><span class="sxs-lookup"><span data-stu-id="349b1-119">If no categories are assigned for a resource, Finance looks up the default category on hour prices for cost and revenue.</span></span>

## <a name="set-up-project-resource-and-role-characteristics"></a><span data-ttu-id="349b1-120">Configurar els recursos del projecte i les característiques de la funció</span><span class="sxs-lookup"><span data-stu-id="349b1-120">Set up project resource and role characteristics</span></span>

<span data-ttu-id="349b1-121">Un administrador de projectes pot utilitzar la funcionalitat de recursos de projecte per crear les funcions necessàries per al projecte.</span><span class="sxs-lookup"><span data-stu-id="349b1-121">A project manager can use the project resourcing functionality to create the roles that are required for the project.</span></span> <span data-ttu-id="349b1-122">Es poden utilitzar funcions si els recursos confirmats es desconeixen quan es reserven els recursos.</span><span class="sxs-lookup"><span data-stu-id="349b1-122">Roles can be used if confirmed resources are still unknown when resources are being reserved.</span></span> <span data-ttu-id="349b1-123">Les funcions es poden reservar temporalment com a recursos planificats per tal de poder continuar la fase de planificació del projecte.</span><span class="sxs-lookup"><span data-stu-id="349b1-123">Roles can be temporarily reserved as planned resources, so that you can continue the project planning stages.</span></span>

<span data-ttu-id="349b1-124">[![Exemple d'una funció](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span><span class="sxs-lookup"><span data-stu-id="349b1-124">[![Example of a role](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span></span> 

<span data-ttu-id="349b1-125">**Escenari:** Contoso ha rebut un contracte per completar un projecte de temps i materials que té una carta de projecte aprovada.</span><span class="sxs-lookup"><span data-stu-id="349b1-125">**Scenario:** Contoso was hired to complete a Time and material project that has an approved project charter.</span></span> <span data-ttu-id="349b1-126">L'administrador de projectes júnior encara està completant l'àmbit del projecte.</span><span class="sxs-lookup"><span data-stu-id="349b1-126">The junior project manager is still completing the scope of the project.</span></span> <span data-ttu-id="349b1-127">L'administrador de recursos està identificant actualment els recursos específics que es reservaran per treballar en el nou projecte.</span><span class="sxs-lookup"><span data-stu-id="349b1-127">The resource manager is currently identifying specific resources that will be reserved to work on the new project.</span></span> <span data-ttu-id="349b1-128">A causa del caràcter crític del projecte, el patrocinador del projecte ha sol·licitat l'administrador de projectes sènior com una de les funcions.</span><span class="sxs-lookup"><span data-stu-id="349b1-128">Because of the critical nature of the project, the project sponsor requested Senior project manager as one of the roles.</span></span> <span data-ttu-id="349b1-129">L'administrador de recursos ha d'adquirir el recurs nou i definir la funció en el sistema en cas que l'administrador de projectes júnior requereixi la informació del recurs durant la planificació del projecte.</span><span class="sxs-lookup"><span data-stu-id="349b1-129">The resource manager must acquire the new resource and define the role in the system in case the junior project manager requires the resource information during project planning.</span></span>

<span data-ttu-id="349b1-130">Els passos següents mostren com l'administrador de recursos pot configurar la funció Administrador de projectes sènior i associar-hi les característiques del recurs.</span><span class="sxs-lookup"><span data-stu-id="349b1-130">The following steps show how the resource manager can set up the Senior project manager role and associate resource characteristics with it.</span></span> <span data-ttu-id="349b1-131">Més endavant, la funció es pot utilitzar per cercar recursos disponibles que coincideixin amb les competències de recursos necessàries.</span><span class="sxs-lookup"><span data-stu-id="349b1-131">Later, the role can be used to search for available resources that match the required resource competencies.</span></span>

1. <span data-ttu-id="349b1-132">A la pàgina **Configura les funcions**, seleccioneu **Nou** i introduïu els valors següents:</span><span class="sxs-lookup"><span data-stu-id="349b1-132">On the **Setup roles** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="349b1-133">**Identificador de funció:** administrador de projectes sènior</span><span class="sxs-lookup"><span data-stu-id="349b1-133">**Role ID:** Senior Project Manager</span></span>
    - <span data-ttu-id="349b1-134">**Descripció:** administrador de projectes sènior</span><span class="sxs-lookup"><span data-stu-id="349b1-134">**Description:** Senior Project Manager</span></span>

2. <span data-ttu-id="349b1-135">Seleccioneu **Crea**.</span><span class="sxs-lookup"><span data-stu-id="349b1-135">Select **Create**.</span></span>
3. <span data-ttu-id="349b1-136">Seleccioneu la funció **Administrador de projectes sènior** i, a continuació, seleccioneu **Configura les característiques**.</span><span class="sxs-lookup"><span data-stu-id="349b1-136">Select the **Senior Project Manager** role, and then select **Configure characteristics**.</span></span>
4. <span data-ttu-id="349b1-137">Al camp **Tipus de característiques**, seleccioneu **Habilitat**.</span><span class="sxs-lookup"><span data-stu-id="349b1-137">In the **Characteristics type** field, select **Skill**.</span></span>
5. <span data-ttu-id="349b1-138">Al camp **Característiques disponibles**, introduïu l'habilitat que voleu cercar.</span><span class="sxs-lookup"><span data-stu-id="349b1-138">In the **Available characteristics** field, enter the skill to search for.</span></span>
6. <span data-ttu-id="349b1-139">Al camp **Tipus de característiques**, seleccioneu **Certificat**.</span><span class="sxs-lookup"><span data-stu-id="349b1-139">In the **Characteristic type** field, select **Certificate**.</span></span>
7. <span data-ttu-id="349b1-140">Al camp **Característiques disponibles**, introduïu el tipus de certificat que voleu cercar.</span><span class="sxs-lookup"><span data-stu-id="349b1-140">In the **Available characteristics** field, enter the certificate type to search for.</span></span>

## <a name="assign-a-project-resource-to-a-project"></a><span data-ttu-id="349b1-141">Assignació d'un recurs de projecte a un projecte</span><span class="sxs-lookup"><span data-stu-id="349b1-141">Assign a project resource to a project</span></span>

1. <span data-ttu-id="349b1-142">A la pàgina **Tots els projectes**, seleccioneu el projecte **Fase 2 d'actualització d'XYZ**.</span><span class="sxs-lookup"><span data-stu-id="349b1-142">On the **All projects** page, select the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="349b1-143">A la pestanya **Equip del projecte i planificació**, seleccioneu **Afegeix**.</span><span class="sxs-lookup"><span data-stu-id="349b1-143">On the **Project team and scheduling** tab, select **Add**.</span></span>
3. <span data-ttu-id="349b1-144">Al camp **Funció**, seleccioneu **Membre de l'equip**.</span><span class="sxs-lookup"><span data-stu-id="349b1-144">In the **Role** field, select **Team member**.</span></span>
4. <span data-ttu-id="349b1-145">Seleccioneu **Reserva des del calendari**.</span><span class="sxs-lookup"><span data-stu-id="349b1-145">Select **Book from calendar**.</span></span>
5. <span data-ttu-id="349b1-146">A la pàgina **Disponibilitat de recursos**, seleccioneu **Visualitza la configuració**.</span><span class="sxs-lookup"><span data-stu-id="349b1-146">On the **Resource availability** page, select **View settings**.</span></span>
6. <span data-ttu-id="349b1-147">A la pàgina **Ajusta la configuració de visualització**, introduïu els valors següents:</span><span class="sxs-lookup"><span data-stu-id="349b1-147">On the **Adjust view settings** page, enter the following values:</span></span>

    - <span data-ttu-id="349b1-148">**Format per a la visualització d'interval de dates:** dia</span><span class="sxs-lookup"><span data-stu-id="349b1-148">**Format for date range view:** Day</span></span>
    - <span data-ttu-id="349b1-149">**Mostra les descripcions de disponibilitat:** Sí</span><span class="sxs-lookup"><span data-stu-id="349b1-149">**Display availability descriptions:** Yes</span></span>
    - <span data-ttu-id="349b1-150">**Mostra la capacitat restant:** Sí</span><span class="sxs-lookup"><span data-stu-id="349b1-150">**Display remaining capacity:** Yes</span></span>

7. <span data-ttu-id="349b1-151">Seleccioneu un recurs de la llista de recursos.</span><span class="sxs-lookup"><span data-stu-id="349b1-151">In the list of resources, select a resource.</span></span>
8. <span data-ttu-id="349b1-152">Seleccioneu **Reserva fixa** i **Capacitat completa**.</span><span class="sxs-lookup"><span data-stu-id="349b1-152">Select **Hard book** and **Full capacity**.</span></span>

## <a name="assign-a-resource-to-a-default-role"></a><span data-ttu-id="349b1-153">Assignar un recurs a una funció per defecte</span><span class="sxs-lookup"><span data-stu-id="349b1-153">Assign a resource to a default role</span></span>

<span data-ttu-id="349b1-154">Per ajudar els administradors de projecte o de recursos, podeu desglossar els recursos que es poden reservar per a un projecte.</span><span class="sxs-lookup"><span data-stu-id="349b1-154">To help project or resource managers can drill down further on the resources that can be reserved for a project.</span></span> <span data-ttu-id="349b1-155">Podeu associar una funció per defecte amb un recurs existent o un recurs adquirit recentment.</span><span class="sxs-lookup"><span data-stu-id="349b1-155">You can associate a default role with an existing resource or a newly acquired resource.</span></span> <span data-ttu-id="349b1-156">Per exemple, quan Daniel va ser contractat, tenia l'experiència i les habilitats necessàries per cobrir la funció d'analista de negocis.</span><span class="sxs-lookup"><span data-stu-id="349b1-156">For example, when Daniel was hired, he had the experience and skills to fill the Business analyst role.</span></span> <span data-ttu-id="349b1-157">L'administrador de recursos ha assignat aquesta funció com a funció per defecte del Daniel.</span><span class="sxs-lookup"><span data-stu-id="349b1-157">The resource manager assigned this role as Daniel's default role.</span></span> <span data-ttu-id="349b1-158">Per tant, l'administrador de recursos ha afegit en Daniel a un grup d'analistes de negoci que estan disponibles per treballar en projectes.</span><span class="sxs-lookup"><span data-stu-id="349b1-158">Therefore, the resource manager added Daniel to a pool of business analysts who are available to work on projects.</span></span>

<span data-ttu-id="349b1-159">Durant la reserva de recursos, els administradors de projectes poden filtrar els recursos de la funció que estan disponibles per treballar en projectes.</span><span class="sxs-lookup"><span data-stu-id="349b1-159">During resource reservation, project managers can filter the role resources that are available to work on projects.</span></span> <span data-ttu-id="349b1-160">Poden utilitzar aquesta informació com un criteri quan realitzen una anàlisi de decisió de diversos criteris durant el compliment dels recursos.</span><span class="sxs-lookup"><span data-stu-id="349b1-160">They can use this information as one criterion when they perform multi-criteria decision analysis during resource fulfillment.</span></span> <span data-ttu-id="349b1-161">També poden afegir altres característiques de recursos al filtre per cercar recursos que tinguin habilitats, formació i experiència específics per a un projecte concret.</span><span class="sxs-lookup"><span data-stu-id="349b1-161">They can also add other resource characteristics to the filter to search for resources that have specific skills, education, and experience for a given project.</span></span>

<span data-ttu-id="349b1-162">**Escenari:** s'ha iniciat un projecte aprovat i la funció Administrador de projectes sènior s'ha reservat com a recurs planificat durant la fase de planificació del projecte.</span><span class="sxs-lookup"><span data-stu-id="349b1-162">**Scenario:** An approved project has started, and the Senior project manager role was reserved as a planned resource during the project planning stage.</span></span> <span data-ttu-id="349b1-163">L'administrador de recursos ha adquirit un recurs per cobrir la funció Administrador de projectes sènior.</span><span class="sxs-lookup"><span data-stu-id="349b1-163">The resource manager has now acquired a resource to fulfill the Senior project manager role.</span></span>

1. <span data-ttu-id="349b1-164">A la pàgina **Llista de recursos**, seleccioneu **Daniel Goldschmidt**.</span><span class="sxs-lookup"><span data-stu-id="349b1-164">On the **Resources list** page, select **Daniel Goldschmidt**.</span></span>
2. <span data-ttu-id="349b1-165">A la pàgina **Funció del recurs**, seleccioneu **Nova** i introduïu els valors següents:</span><span class="sxs-lookup"><span data-stu-id="349b1-165">On the **Resource role** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="349b1-166">**Efectivitat:** introduïu la data actual.</span><span class="sxs-lookup"><span data-stu-id="349b1-166">**Effective:** Enter the current date.</span></span>
    - <span data-ttu-id="349b1-167">**Venciment:** introduïu **Mai**.</span><span class="sxs-lookup"><span data-stu-id="349b1-167">**Expiration:** Enter **Never**.</span></span>
    - <span data-ttu-id="349b1-168">**Funció:** introduïu **Administrador de projectes sènior**.</span><span class="sxs-lookup"><span data-stu-id="349b1-168">**Role:** Enter **Senior Project Manager**.</span></span>

3. <span data-ttu-id="349b1-169">Seleccioneu **Desa** i, a continuació, tanqueu la pàgina.</span><span class="sxs-lookup"><span data-stu-id="349b1-169">Select **Save**, and then close the page.</span></span>
4. <span data-ttu-id="349b1-170">A la pestanya **Competències**, afegiu l'habilitat **ProjectMgmt** i el certificat **PMP**.</span><span class="sxs-lookup"><span data-stu-id="349b1-170">On the **Competencies** tab, add the **ProjectMgmt** skill and the **PMP** certificate.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]