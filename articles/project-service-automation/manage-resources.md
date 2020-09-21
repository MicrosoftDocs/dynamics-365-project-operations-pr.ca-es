---
title: Administrar els recursos
description: En aquest tema es proporciona informació sobre com administrar els recursos.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 05/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 39893019-123b-4bc6-8a2b-a37bc517dc97
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 6c199cbadd1c78e7e29c0cda0febde4236a13d96
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749582"
---
# <a name="manage-resources"></a><span data-ttu-id="c0843-103">Administrar els recursos</span><span class="sxs-lookup"><span data-stu-id="c0843-103">Manage resources</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="c0843-104">El Dynamics 365 Project Service Automation inclou un escriptori digital d'administració de recursos que proporciona una visió general visual de la demanda i l'aprofitament dels recursos a tota l'organització.</span><span class="sxs-lookup"><span data-stu-id="c0843-104">Dynamics 365 Project Service Automation includes a resource manager dashboard that provides a visual overview of resource demand and utilization throughout the organization.</span></span> <span data-ttu-id="c0843-105">Podeu utilitzar els gràfics d'aquest escriptori digital per visualitzar la informació següent:</span><span class="sxs-lookup"><span data-stu-id="c0843-105">You can use the charts on this dashboard to visualize the following information:</span></span>

- <span data-ttu-id="c0843-106">**Demanda de recursos**: el gràfic **Sol·licitud de recursos activa** mostra recursos que s'ha enviat.</span><span class="sxs-lookup"><span data-stu-id="c0843-106">**Resource demand** – The **Active Resource Request** chart shows resources that have been submitted.</span></span> <span data-ttu-id="c0843-107">Els recursos s'agreguen per funció o projecte.</span><span class="sxs-lookup"><span data-stu-id="c0843-107">The resources are aggregated by either role or project.</span></span>
- <span data-ttu-id="c0843-108">**Demanda de recursos no enviats**: el gràfic **Demanda de recursos no assignats** mostra tots els requisits de recursos que no s'han enviat.</span><span class="sxs-lookup"><span data-stu-id="c0843-108">**Unsubmitted resource demand** – The **Unassigned Resource Demand** chart shows all the resource requirements that haven't been submitted.</span></span> <span data-ttu-id="c0843-109">Ajuda els administradors de recursos a veure la demanda que no és ferma i podria ser enviada a través d'una sol·licitud de recursos.</span><span class="sxs-lookup"><span data-stu-id="c0843-109">It helps resource managers view demand that isn't firm and might be submitted through a resource request.</span></span>
- <span data-ttu-id="c0843-110">**Ús facturable durant la setmana passada**: el gràfic **Utilització per funció** mostra el percentatge de l'ús facturable real de l'organització per funció en comparació amb l'objectiu d'ús facturable per funció.</span><span class="sxs-lookup"><span data-stu-id="c0843-110">**Billable utilization for the past week** – The **Utilization by Role** chart shows the percentage of the organization's actual billable utilization by role against its target billable utilization by role.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c0843-111">Per fer que el gràfic **Ús per funció** estigui disponible, creeu una feina que executi el flux de treball UpdateRoleUtilization.</span><span class="sxs-lookup"><span data-stu-id="c0843-111">To make the **Utilization by Role** chart available, create a job that runs the UpdateRoleUtilization workflow.</span></span> <span data-ttu-id="c0843-112">Aquesta feina periòdica s'executa cada set dies per calcular l'ús facturable dels set dies anteriors.</span><span class="sxs-lookup"><span data-stu-id="c0843-112">This recurring job runs every seven days to calculate billable utilization for the previous seven days.</span></span> <span data-ttu-id="c0843-113">Els resultats s'agreguen per funció.</span><span class="sxs-lookup"><span data-stu-id="c0843-113">The results are aggregated by role.</span></span>

## <a name="manage-project-team-members"></a><span data-ttu-id="c0843-114">Administrar membres de l'equip del projecte</span><span class="sxs-lookup"><span data-stu-id="c0843-114">Manage project team members</span></span>

<span data-ttu-id="c0843-115">Els administradors de projecte poden utilitzar l'escriptori digital d'administrador de recursos per administrar els recursos dels projectes.</span><span class="sxs-lookup"><span data-stu-id="c0843-115">Project managers can use the resource manager dashboard to manage the resources on projects.</span></span> <span data-ttu-id="c0843-116">Per exemple, poden afegir un membre de l'equip directament a un projecte i reservar un membre de l'equip per complir els requisits dels recursos que s'han capturat per un recurs genèric.</span><span class="sxs-lookup"><span data-stu-id="c0843-116">For example, they can add a team member directly to a project and book a team member to fulfill the resource requirements that were captured by a generic resource.</span></span>

### <a name="add-a-team-member-directly-to-a-project"></a><span data-ttu-id="c0843-117">Afegir un membre de l'equip directament a un projecte</span><span class="sxs-lookup"><span data-stu-id="c0843-117">Add a team member directly to a project</span></span>

<span data-ttu-id="c0843-118">Per afegir un membre de l'equip directament a un projecte , seleccioneu **Crea** a la pàgina **Projectes** de la pestanya **Equip**.</span><span class="sxs-lookup"><span data-stu-id="c0843-118">To add a team member directly to a project, on the **Projects** page, on the **Team** tab, select **New**.</span></span> <span data-ttu-id="c0843-119">Apareixerà el quadre de diàleg **Creació ràpida: membre de l'equip del projecte**.</span><span class="sxs-lookup"><span data-stu-id="c0843-119">The **Quick Create:Project Team Member** dialog box appears.</span></span> <span data-ttu-id="c0843-120">En aquest quadre de diàleg, podeu dur a terme aquestes tasques:</span><span class="sxs-lookup"><span data-stu-id="c0843-120">In this dialog box, you can perform these tasks:</span></span>

- <span data-ttu-id="c0843-121">**Reservar un recurs amb nom**: al camp **Recursos que es poden reservar**, seleccioneu el nom del recurs.</span><span class="sxs-lookup"><span data-stu-id="c0843-121">**Book a named resource** – In the **Bookable Resource** field, select the name of the resource.</span></span> <span data-ttu-id="c0843-122">A continuació, seleccioneu la funció, definiu el període i seleccioneu un mètode d'assignació.</span><span class="sxs-lookup"><span data-stu-id="c0843-122">Then select the role, set the period, and select an allocation method.</span></span> <span data-ttu-id="c0843-123">El recurs amb nom que heu seleccionat s'afegeix al projecte mitjançant el mètode d'assignació i el calendari de recursos seleccionat.</span><span class="sxs-lookup"><span data-stu-id="c0843-123">The named resource that you selected is added to the project by using the selected allocation method and the resources calendar.</span></span>
- <span data-ttu-id="c0843-124">**Afegir un recurs genèric**: deixeu el camp **Recurs que es pot reservar** en blanc i, a continuació, seleccioneu la funció, definiu el període i seleccioneu el mètode d'assignació preferit.</span><span class="sxs-lookup"><span data-stu-id="c0843-124">**Add a generic resource** – Leave the **Bookable resource** field blank, and then select the role, set the period, and select the preferred allocation method.</span></span> <span data-ttu-id="c0843-125">Un recurs genèric s'afegeix a l'equip com a marcador de posició per mantenir el patró de demanda que s'utilitza per reservar els recursos amb nom a l'equip.</span><span class="sxs-lookup"><span data-stu-id="c0843-125">A generic resource is added to the team as a placeholder to hold the demand pattern that is used to book named resources on the team.</span></span> <span data-ttu-id="c0843-126">El requisit es realitza d'acord amb el calendari del projecte.</span><span class="sxs-lookup"><span data-stu-id="c0843-126">The requirement is made according to the project calendar.</span></span>
- <span data-ttu-id="c0843-127">**Afegir un recurs amb nom a l'equip sense haver de consumir la capacitat dels recursos**: al camp **Recurs que es pot reservar**, seleccioneu un recurs.</span><span class="sxs-lookup"><span data-stu-id="c0843-127">**Add a named resource to the team without consuming resource capacity** – In the **Bookable Resource** field, select a resource.</span></span> <span data-ttu-id="c0843-128">A continuació, seleccioneu el període, i seleccioneu **Cap** com a mètode d'assignació.</span><span class="sxs-lookup"><span data-stu-id="c0843-128">Then select the period, and select **None** as the allocation method.</span></span> <span data-ttu-id="c0843-129">El recurs s'afegeix a l'equip, però la capacitat del recurs no es consumeix a través d'una reserva.</span><span class="sxs-lookup"><span data-stu-id="c0843-129">The resource is added to the team, but the resource's capacity isn't consumed through a booking.</span></span>

### <a name="book-a-team-member-to-fulfill-resource-requirements-for-a-generic-resource"></a><span data-ttu-id="c0843-130">Reserveu un membre de l'equip per complir els requisits de recursos per a un recurs genèric</span><span class="sxs-lookup"><span data-stu-id="c0843-130">Book a team member to fulfill resource requirements for a generic resource</span></span>

<span data-ttu-id="c0843-131">Al PSA, podeu reservar un recurs genèric en un equip del projecte i especificar la funció, la capacitat requerida i la manera com es distribueix aquesta capacitat.</span><span class="sxs-lookup"><span data-stu-id="c0843-131">In PSA, you can book a generic resource on a project team, and can specify the role, the required capacity, and how that capacity is distributed.</span></span> <span data-ttu-id="c0843-132">Al requeriment de recursos, podeu especificar els atributs associats amb el recurs genèric.</span><span class="sxs-lookup"><span data-stu-id="c0843-132">On the resource requirement, you can specify attributes that are associated with the generic resource.</span></span> <span data-ttu-id="c0843-133">Aquests atributs inclouen les aptituds necessàries, la unitat organitzativa preferida i els recursos preferents.</span><span class="sxs-lookup"><span data-stu-id="c0843-133">These attributes include required skills, the preferred organizational unit, and preferred resources.</span></span>

<span data-ttu-id="c0843-134">Seguiu els passos que s'indiquen a continuació per especificar les aptituds necessàries en un recurs genèric per a un desenvolupador.</span><span class="sxs-lookup"><span data-stu-id="c0843-134">Follow these steps to specify required skills on a generic resource for a developer.</span></span>

1. <span data-ttu-id="c0843-135">A la pàgina **Projectes**, a la pestanya **Equip**, seleccioneu **Crea** per reservar un recurs genèric.</span><span class="sxs-lookup"><span data-stu-id="c0843-135">On the **Projects** page, on the **Team** tab, select **New** to book a generic resource.</span></span>

    ![Recurs genèric reservat a l'equip](media/Resource-Management-image9.png)

2. <span data-ttu-id="c0843-137">A la visualització **Tots els membres de l'equip**, a la columna **Requisits de recursos**, seleccioneu l'enllaç per afegir les competències necessàries per al recurs genèric.</span><span class="sxs-lookup"><span data-stu-id="c0843-137">In the **All Team Members** view, in the **Resource Requirement** column, select the link to add required skills for the generic resource.</span></span>

    ![Enllaç de requisit](media/Resource-Management-image10.png)

3. <span data-ttu-id="c0843-139">A la pàgina **Requisit de recursos** que es mostra, a la quadrícula **Aptituds**, seleccioneu els punts suspensius (**...**) i, a continuació, seleccioneu **Afegeix una característica de requisit nova** per afegir les aptituds necessàries per al desenvolupador.</span><span class="sxs-lookup"><span data-stu-id="c0843-139">On the **Resource Requirement** page that appears, in the **Skills** grid, select the ellipsis (**...**) and then select **Add New Requirement Characteristic** to add the required skills for your developer.</span></span>

    ![Ordre Afegeix una característica de requisit nova](media/Resource-Management-image11.png)

4. <span data-ttu-id="c0843-141">Al quadre de diàleg **Creació ràpida: característica de requisit** que apareix, al camp **Característica**, seleccioneu l'aptitud necessària.</span><span class="sxs-lookup"><span data-stu-id="c0843-141">In the **Quick Create: Requirement Characteristic** dialog box that appears, in the **Characteristic** field, select the required skill.</span></span> <span data-ttu-id="c0843-142">A continuació, al camp **Valor de qualificació**, seleccioneu el nivell de competència per a aquesta aptitud.</span><span class="sxs-lookup"><span data-stu-id="c0843-142">Then, in the **Rating value** field, select the proficiency level for that skill.</span></span> <span data-ttu-id="c0843-143">Finalment, al camp **Requisit de recursos**, definiu el requisit dels recursos d'origen d'unitats organitzatives o fins i tot de recursos amb nom.</span><span class="sxs-lookup"><span data-stu-id="c0843-143">Finally, in the **Resource Requirement** field, set the requirement to source resources from organizational units or even named resources.</span></span> <span data-ttu-id="c0843-144">Quan hagueu acabat, trieu **Desa**.</span><span class="sxs-lookup"><span data-stu-id="c0843-144">When you've finished, select **Save**.</span></span>

    ![Quadre de diàleg Creació ràpida: característica de requisit](media/Resource-Management-image12.png)

5. <span data-ttu-id="c0843-146">A la pàgina **Requisits de recursos**, seleccioneu **Reserva** per complir el requisit de recursos.</span><span class="sxs-lookup"><span data-stu-id="c0843-146">On the **Resource Requirement** page, select **Book** to fulfill the resource requirement.</span></span>

    ![Botó Reserva a la pàgina Requisits de recursos](media/Resource-Management-image13.png)

    <span data-ttu-id="c0843-148">També podeu seleccionar el recurs genèric a la quadrícula **Tots els membres de l'equip** i, a continuació, seleccionar **Reserva**.</span><span class="sxs-lookup"><span data-stu-id="c0843-148">You can also select the generic resource in the **All Team Members** grid and then select **Book**.</span></span>

    ![Botó Reserva per sobre de la quadrícula Tots els membres de l'equip](media/Resource-Management-image14.png)

    > [!NOTE]
    > <span data-ttu-id="c0843-150">En aquest exemple, hi ha 40 hores necessàries però no hores reservades reals, perquè els recursos genèrics no tenen reserves.</span><span class="sxs-lookup"><span data-stu-id="c0843-150">In this example, there are 40 required hours but no actual booked hours, because generic resources don't have bookings.</span></span> <span data-ttu-id="c0843-151">A més, no hi ha cap hora assignada, perquè el recurs genèric s'ha afegit directament a l'equip.</span><span class="sxs-lookup"><span data-stu-id="c0843-151">Additionally, there are no assigned hours, because the generic resource was added directly to the team.</span></span> <span data-ttu-id="c0843-152">No s'ha afegit mitjançant l'assignació de tasques.</span><span class="sxs-lookup"><span data-stu-id="c0843-152">It wasn't added by using task assignment.</span></span>

    <span data-ttu-id="c0843-153">A la pàgina **Auxiliar de planificació**, podeu filtrar els recursos disponibles mitjançant els requisits que s'especifiquen al requisit del recurs.</span><span class="sxs-lookup"><span data-stu-id="c0843-153">On the **Scheduling Assistant** page, you can filter available resources by the requirements that are specified on the resource requirement.</span></span> <span data-ttu-id="c0843-154">Els recursos s'ordenen segons els paràmetres d'ordenació que s'especifiquen al Tauler de planificació.</span><span class="sxs-lookup"><span data-stu-id="c0843-154">Resources are sorted according to the sorting parameters that are specified on the Schedule Board.</span></span>

    ![Pàgina Auxiliar de planificació](media/Resource-Management-image15.png)

    <span data-ttu-id="c0843-156">A continuació teniu alguns filtres que s'utilitzen sovint:</span><span class="sxs-lookup"><span data-stu-id="c0843-156">Here are some filters that are often used:</span></span>

    - <span data-ttu-id="c0843-157">**Característiques amb una valoració**: filtreu per competències, certificacions i altres qualitats de recursos, a més d'avaluacions de competència.</span><span class="sxs-lookup"><span data-stu-id="c0843-157">**Characteristics along with a rating** – Filter by skills, certifications, and other resource qualities, in addition to ratings of proficiency.</span></span>
    - <span data-ttu-id="c0843-158">**Funcions**: filtreu per les funcions per defecte que estan assignades a recursos que es poden reservar.</span><span class="sxs-lookup"><span data-stu-id="c0843-158">**Roles** – Filter by the default roles that are assigned to bookable resources.</span></span>
    - <span data-ttu-id="c0843-159">**Unitats organitzatives**: filtreu recursos que es poden reservar per les unitats organitzatives que tenen assignades.</span><span class="sxs-lookup"><span data-stu-id="c0843-159">**Organizational units** – Filter bookable resources by the organizational units that they are assigned to.</span></span>

6. <span data-ttu-id="c0843-160">Si no esteu satisfet amb els resultats de la cerca inicial de requisits, podeu canviar els criteris de filtratge.</span><span class="sxs-lookup"><span data-stu-id="c0843-160">If you aren't satisfied with the results of the initial requirement search, you can change the filter criteria.</span></span> <span data-ttu-id="c0843-161">Expandiu la subfinestra **Filtra la visualització** a l'esquerra i, a continuació, seleccioneu **Cerca** per cercar recursos addicionals.</span><span class="sxs-lookup"><span data-stu-id="c0843-161">Expand the **Filter View** pane on the left, and then select **Search** to find additional resources.</span></span>

    ![Subfinestra Filtra la visualització](media/Resource-Management-image16.png)

7. <span data-ttu-id="c0843-163">Per canviar la manera com s'ordenen els resultats, seleccioneu **Ordena**.</span><span class="sxs-lookup"><span data-stu-id="c0843-163">To change how the results are sorted, select **Sort**.</span></span>

    ![Ordre Ordena](media/Resource-Management-image17.png)

8. <span data-ttu-id="c0843-165">Seleccioneu recursos segons la demanda que s'especifica a l'exigència, tal com s'indicava a la part superior de la quadrícula.</span><span class="sxs-lookup"><span data-stu-id="c0843-165">Select resources according to the demand that is specified on the requirement, as indicated at the top of the grid.</span></span> <span data-ttu-id="c0843-166">Podeu desactivar la selecció de cel·les a la quadrícula i deixar oberta la capacitat d'un recurs.</span><span class="sxs-lookup"><span data-stu-id="c0843-166">You can clear the selection of cells in the grid and leave that resource capacity open.</span></span> <span data-ttu-id="c0843-167">Només es pot seleccionar un recurs cada vegada com a reservat.</span><span class="sxs-lookup"><span data-stu-id="c0843-167">Only one resource at a time can be selected as booked.</span></span>

9. <span data-ttu-id="c0843-168">Seleccioneu **Reserva** per reservar el recurs seleccionat i deixeu obert el Tauler de planificació, de manera que pugueu seleccionar recursos addicionals.</span><span class="sxs-lookup"><span data-stu-id="c0843-168">Select **Book** to book the selected resource and leave the Schedule Board open, so that you can select additional resources.</span></span> <span data-ttu-id="c0843-169">Alternativament, seleccioneu **Reserva i surt** per reservar el recurs seleccionat i tanqueu el Tauler de planificació.</span><span class="sxs-lookup"><span data-stu-id="c0843-169">Alternatively, select **Book & Exit** to book the selected resource and close the Schedule Board.</span></span>

    ![Recurs per reservar](media/Resource-Management-image19.png)

    <span data-ttu-id="c0843-171">Rebreu una notificació sobre les hores reservades.</span><span class="sxs-lookup"><span data-stu-id="c0843-171">You receive a notification about booked hours.</span></span> <span data-ttu-id="c0843-172">Els indicadors de demanda mostren la quantitat de requisits de reserva satisfets i quants en queden.</span><span class="sxs-lookup"><span data-stu-id="c0843-172">The demand indicators show how much the booking requirement is satisfied and how much remains.</span></span> <span data-ttu-id="c0843-173">També podeu veure la quantitat de la capacitat del recurs seleccionat consumida.</span><span class="sxs-lookup"><span data-stu-id="c0843-173">You can also see how much of the selected resource's capacity is consumed.</span></span> <span data-ttu-id="c0843-174">Seleccioneu **Expandeix** per veure més detalls sobre les reserves de recursos.</span><span class="sxs-lookup"><span data-stu-id="c0843-174">Select **Expand** to view more details about resource bookings.</span></span>

9. <span data-ttu-id="c0843-175">Torneu a la visualització **Tots els membres de l'equip**.</span><span class="sxs-lookup"><span data-stu-id="c0843-175">Return to the **All Team Members** view.</span></span> <span data-ttu-id="c0843-176">A la quadrícula, heu de tenir en compte que el recurs genèric s'ha substituït pel recurs amb nom i que les 40 hores es mostren com a reservades per a aquest recurs.</span><span class="sxs-lookup"><span data-stu-id="c0843-176">In the grid, notice that the generic resource has been replaced by the named resource, and 40 hours are listed as booked for that resource.</span></span>

    ![Quadrícula Tots els membres de l'equip actualitzada](media/Resource-Management-image20.png)

    > [!NOTE]
    > <span data-ttu-id="c0843-178">No es mostren les hores assignades, perquè estaven reservades directament a l'equip.</span><span class="sxs-lookup"><span data-stu-id="c0843-178">No assigned hours are shown, because they were booked directly on the team.</span></span> <span data-ttu-id="c0843-179">No s'han reservat mitjançant l'assignació de tasques.</span><span class="sxs-lookup"><span data-stu-id="c0843-179">They weren't booked by using task assignment.</span></span>

## <a name="assign-generic-resources-to-tasks-and-generate-resource-requirements"></a><span data-ttu-id="c0843-180">Assignar recursos genèrics a tasques i generar requisits de recursos</span><span class="sxs-lookup"><span data-stu-id="c0843-180">Assign generic resources to tasks and generate resource requirements</span></span>

<span data-ttu-id="c0843-181">Al PSA, podeu crear tasques i, a continuació, assignar-hi recursos genèrics.</span><span class="sxs-lookup"><span data-stu-id="c0843-181">In PSA, you can create tasks and then assign generic resources to them.</span></span> <span data-ttu-id="c0843-182">D'aquesta manera, la demanda de recursos es pot representar amb marcadors de posició mentre s'estima la planificació i els números financers.</span><span class="sxs-lookup"><span data-stu-id="c0843-182">In this way, resource demand can be represented by placeholders while you estimate your schedule and financial numbers.</span></span> <span data-ttu-id="c0843-183">A continuació, podeu generar requisits de recursos per als recursos genèrics i complir-los.</span><span class="sxs-lookup"><span data-stu-id="c0843-183">You can then generate resource requirements for the generic resources and fulfill them.</span></span>

1. <span data-ttu-id="c0843-184">A la pàgina **Projectes**, a la pestanya **Planificació**, seleccioneu **Afegeix** per crear una tasca.</span><span class="sxs-lookup"><span data-stu-id="c0843-184">On the **Projects** page, on the **Schedule** tab, select **Add** to create a task.</span></span>

    ![Tasca nova creada](media/Resource-Management-image21.png)

2. <span data-ttu-id="c0843-186">Al camp **Recursos**, seleccioneu el símbol **Selector de recursos**.</span><span class="sxs-lookup"><span data-stu-id="c0843-186">In the **Resources** field, select the **Resource Picker** symbol.</span></span> <span data-ttu-id="c0843-187">El Selector de recursos apareix i mostra els membres de l'equip existents per al projecte.</span><span class="sxs-lookup"><span data-stu-id="c0843-187">The Resource Picker appears and shows existing team members for the project.</span></span>

    ![Selector de recursos](media/Resource-Management-image22.png)

3. <span data-ttu-id="c0843-189">Introduïu el nom del recurs genèric nou i, a continuació, seleccioneu **Crea**.</span><span class="sxs-lookup"><span data-stu-id="c0843-189">Enter the name of the new generic resource, and then select **Create**.</span></span>

    ![Nom d'un recurs genèric nou introduït](media/Resource-Management-image23.png)

4. <span data-ttu-id="c0843-191">Al quadre de diàleg **Creació ràpida: membre de l'equip del projecte** que apareix, al camp **Funció**, seleccioneu la funció per al recurs genèric.</span><span class="sxs-lookup"><span data-stu-id="c0843-191">In the **Quick Create: Project Team Member** dialog box that appears, in the **Role** field, select the role for the generic resource.</span></span> <span data-ttu-id="c0843-192">Al camp **Unitat de recursos**, seleccioneu la unitat organitzativa del recurs genèric.</span><span class="sxs-lookup"><span data-stu-id="c0843-192">In the **Resourcing Unit** field, select the organizational unit for the generic resource.</span></span> <span data-ttu-id="c0843-193">A continuació, seleccioneu **Desa**.</span><span class="sxs-lookup"><span data-stu-id="c0843-193">Then select **Save**.</span></span>

    ![Quadre de diàleg Creació ràpida: membre de l'equip del projecte](media/Resource-Management-image24.png)

    <span data-ttu-id="c0843-195">El membre de l'equip genèric ara està assignat a la tasca.</span><span class="sxs-lookup"><span data-stu-id="c0843-195">The generic team member is now assigned to the task.</span></span>

    ![Membre de l'equip genèric assignat a la tasca](media/Resource-Management-image25.png)

    <span data-ttu-id="c0843-197">A la pestanya **Equip**, veureu el nou membre de l'equip genèric.</span><span class="sxs-lookup"><span data-stu-id="c0843-197">On the **Team** tab, you will see the new generic team member.</span></span> <span data-ttu-id="c0843-198">Observeu que només té hores assignades.</span><span class="sxs-lookup"><span data-stu-id="c0843-198">Notice that it has only assigned hours.</span></span> <span data-ttu-id="c0843-199">Aquestes hores són la suma de totes les tasques assignades al membre de l'equip genèric.</span><span class="sxs-lookup"><span data-stu-id="c0843-199">These hours are the sum of all tasks that are assigned to the generic team member.</span></span> <span data-ttu-id="c0843-200">El membre genèric de l'equip encara no té hores obligatòries o un requisit de recurs.</span><span class="sxs-lookup"><span data-stu-id="c0843-200">The generic team member doesn't yet have required hours or a resource requirement.</span></span>

    ![Membre de l'equip genèric a la pestanya Equip](media/Resource-Management-image26.png)

5. <span data-ttu-id="c0843-202">Ara podeu assignar el membre de l'equip genèric a altres tasques mitjançant el Selector de recursos.</span><span class="sxs-lookup"><span data-stu-id="c0843-202">You can now assign the generic team member to other tasks by using the Resource Picker.</span></span>

    ![Membre de l'equip genèric al Selector de recursos](media/Resource-Management-image27.png)

    <span data-ttu-id="c0843-204">Quan hàgiu acabat d'assignar el recurs genèric a les tasques, podeu generar un requisit de recurs per al recurs genèric.</span><span class="sxs-lookup"><span data-stu-id="c0843-204">When you've finished assigning the generic resource to tasks, you can generate a resource requirement for the generic resource.</span></span>

5. <span data-ttu-id="c0843-205">A la pestanya **Equip**, seleccioneu el recurs genèric i, a continuació , seleccioneu **Genera un requisit**.</span><span class="sxs-lookup"><span data-stu-id="c0843-205">On the **Team** tab, select the generic resource, and then select **Generate Requirement**.</span></span>

    ![Ordre Genera un requisit](media/Resource-Management-image28.png)

    <span data-ttu-id="c0843-207">Quan es genera el requisit, el membre de l'equip genèric tindrà hores obligatòries i un enllaç per al requeriment del recurs.</span><span class="sxs-lookup"><span data-stu-id="c0843-207">When the requirement is generated, the generic team member will have required hours and a link for the resource requirement.</span></span>

    ![Enllaç al requisit de recursos](media/Resource-Management-image29.png)

    <span data-ttu-id="c0843-209">Després de reservar un recurs amb nom, el recurs genèric se suprimeix de l'equip i se substitueix pel recurs amb nom.</span><span class="sxs-lookup"><span data-stu-id="c0843-209">After you book a named resource, the generic resource is removed from the team and replaced by the named resource.</span></span>

    ![Recurs genèric substituït pel recurs amb nom](media/Resource-Management-image30.png)

    <span data-ttu-id="c0843-211">A la pestanya **Planificació**, les assignacions de recursos genèrics s'eliminen i se substitueixen pel recurs amb nom.</span><span class="sxs-lookup"><span data-stu-id="c0843-211">On the **Schedule** tab, the generic resource assignments are removed and replaced by the named resource.</span></span>

    ![Assignacions de recursos genèrics substituïdes pel recurs amb nom a la pestanya Planificació](media/Resource-Management-image31.png)

    > [!NOTE]
    > <span data-ttu-id="c0843-213">Aquest comportament només es produeix quan un recurs amb nom està completament reservat per al requisit de recursos genèrics.</span><span class="sxs-lookup"><span data-stu-id="c0843-213">This behavior occurs only when a named resource is fully booked for the generic resource requirement.</span></span> <span data-ttu-id="c0843-214">Quan un recurs amb nom reemplaça parcialment el requisit de recurs genèric o diversos recursos amb nom reemplacen els requisits de recurs genèric, el recurs genèric es manté assignat a la tasca.</span><span class="sxs-lookup"><span data-stu-id="c0843-214">When either a named resource partially replaces the generic resource requirement or multiple named resources replace the generic resource requirement, the generic resource remains assigned to the task.</span></span>

    <span data-ttu-id="c0843-215">A la il·lustració següent, s'ha planificat una tasca de 80 hores per a una duració de cinc dies (16 hores al dia més de cinc dies) i s'assigna al recurs genèric amb el nom **Funcional**.</span><span class="sxs-lookup"><span data-stu-id="c0843-215">In the following illustration, an 80-hour task has been planned for a five-day duration (16 hours per day over five days) and assigned to the generic resource that is named **Functional**.</span></span>

    ![Tasca de vuitanta hores en cinc dies assignada al recurs genèric Funcional](media/Resource-Management-image32.png)

    <span data-ttu-id="c0843-217">En generar el requisit, és de 80 hores al llarg de cinc dies.</span><span class="sxs-lookup"><span data-stu-id="c0843-217">When you generate the requirement, it's for 80 hours over five days.</span></span>

    ![Requisit generat per a 80 hores en cinc dies](media/Resource-Management-image33.png)

    <span data-ttu-id="c0843-219">Com que els recursos disponibles treballen només vuit hores al dia, calen dos recursos per complir el requisit.</span><span class="sxs-lookup"><span data-stu-id="c0843-219">Because available resources work only eight hours per day, two resources are needed to fulfill the requirement.</span></span>

    ![Segon recurs](media/Resource-Management-image35.png)

    <span data-ttu-id="c0843-221">A la pestanya **Equip**, ara podeu veure que el recurs genèric no té hores necessàries, però les hores assignades encara es mostren juntament amb els dos recursos amb nom que formen el compliment.</span><span class="sxs-lookup"><span data-stu-id="c0843-221">On the **Team** tab, you can now see that the generic resource has no required hours, but the assigned hours still appear together with the two named resources that make up the fulfillment.</span></span>

    ![Dos recursos amb nom a la pestanya Equip](media/Resource-Management-image36.png)

    <span data-ttu-id="c0843-223">A la pestanya **Planificació**, el recurs genèric es manté assignat a la tasca.</span><span class="sxs-lookup"><span data-stu-id="c0843-223">On the **Schedule** tab, the generic resource remains assigned to the task.</span></span>

    ![Recursos genèrics a la pestanya Planificació](media/Resource-Management-image37.png)

<span data-ttu-id="c0843-225">El PSA no assigna tots dos recursos a la tasca, perquè aquest comportament produiria una planificació menys predictible.</span><span class="sxs-lookup"><span data-stu-id="c0843-225">PSA doesn't assign both resources to the task, because that behavior would produce a less predictable schedule.</span></span> <span data-ttu-id="c0843-226">En aquest senzill exemple, és fàcil dividir les hores de manera equitativa entre dos recursos.</span><span class="sxs-lookup"><span data-stu-id="c0843-226">In this simple example, it's easy to divide the hours equally between two resources.</span></span> <span data-ttu-id="c0843-227">No obstant, en escenaris més complexos que impliquen diverses tasques i diversos recursos, el PSA hauria de fer suposicions sobre com hauria d'assignar les reserves que es reben per a diversos recursos en diverses tasques.</span><span class="sxs-lookup"><span data-stu-id="c0843-227">However, in more complex scenarios that involve multiple tasks and multiple resources, PSA would have to make assumptions about how it should allocate the bookings that are received for multiple resources across multiple tasks.</span></span>

<span data-ttu-id="c0843-228">Per tant, en aquests escenaris, l'administrador del projecte s'encarrega d'analitzar les diverses reserves i d'assignar-les segons calgui.</span><span class="sxs-lookup"><span data-stu-id="c0843-228">Therefore, in these scenarios, the project manager is responsible for parsing the multiple bookings and assigning them as needed.</span></span> <span data-ttu-id="c0843-229">Per assignar les reserves, l'administrador del projecte assigna les tasques des dels recursos genèrics als recursos amb nom i, a continuació, utilitza la visualització **Conciliació** per assegurar-se que l'assignació funciona amb les reserves.</span><span class="sxs-lookup"><span data-stu-id="c0843-229">To allocate the bookings, the project manager assigns the tasks from the generic resources to the named resources and then uses the **Reconciliation** view to make sure that the allocation works with the bookings.</span></span>

### <a name="edit-a-resource-requirement"></a><span data-ttu-id="c0843-230">Editar un requisit de recursos</span><span class="sxs-lookup"><span data-stu-id="c0843-230">Edit a resource requirement</span></span>

<span data-ttu-id="c0843-231">Després d'haver creat un requisit de recurs, pot ser que un administrador de projectes o un administrador de recursos vulguin editar els detalls per perfeccionar els criteris de cerca quan s'utilitza e Tauler de planificació.</span><span class="sxs-lookup"><span data-stu-id="c0843-231">After a resource requirement has been created, a project manager or resource manager might want to edit the details to refine the search criteria when the Schedule Board is used.</span></span> <span data-ttu-id="c0843-232">Per editar el requisit de recursos, seguiu aquests passos.</span><span class="sxs-lookup"><span data-stu-id="c0843-232">To edit the resource requirement, follow these steps.</span></span>

1. <span data-ttu-id="c0843-233">A la pàgina **Projectes**, a la pestanya **Equip**, seleccioneu l'enllaç a qualsevol requisit en un recurs genèric.</span><span class="sxs-lookup"><span data-stu-id="c0843-233">On the **Projects** page, on the **Team** tab, select the link to any requirement on a generic resource.</span></span>
2. <span data-ttu-id="c0843-234">A la pàgina **Requisits de recursos** que es mostra, podeu actualitzar diversos atributs.</span><span class="sxs-lookup"><span data-stu-id="c0843-234">On the **Resource Requirement** page that appears, you can update several attributes.</span></span> <span data-ttu-id="c0843-235">A continuació trobareu alguns exemples:</span><span class="sxs-lookup"><span data-stu-id="c0843-235">Here are some examples:</span></span>

    - <span data-ttu-id="c0843-236">Nom</span><span class="sxs-lookup"><span data-stu-id="c0843-236">Name</span></span>
    - <span data-ttu-id="c0843-237">Data d'inici</span><span class="sxs-lookup"><span data-stu-id="c0843-237">From Date</span></span>
    - <span data-ttu-id="c0843-238">Data final</span><span class="sxs-lookup"><span data-stu-id="c0843-238">To Date</span></span>
    - <span data-ttu-id="c0843-239">Duració</span><span class="sxs-lookup"><span data-stu-id="c0843-239">Duration</span></span>
    - <span data-ttu-id="c0843-240">Tipus de recurs</span><span class="sxs-lookup"><span data-stu-id="c0843-240">Resource Type</span></span>

<span data-ttu-id="c0843-241">A la pàgina **Requisits de recursos**, l'administrador del projecte o administrador de recursos també pot definir la següent informació:</span><span class="sxs-lookup"><span data-stu-id="c0843-241">On the **Resource Requirement** page, the project manager or resource manager can also define the following information:</span></span>

- <span data-ttu-id="c0843-242">Aptituds</span><span class="sxs-lookup"><span data-stu-id="c0843-242">Skills</span></span>
- <span data-ttu-id="c0843-243">Funcions</span><span class="sxs-lookup"><span data-stu-id="c0843-243">Roles</span></span>
- <span data-ttu-id="c0843-244">Preferències de recursos</span><span class="sxs-lookup"><span data-stu-id="c0843-244">Resource preferences</span></span>
- <span data-ttu-id="c0843-245">Unitat organitzativa preferida</span><span class="sxs-lookup"><span data-stu-id="c0843-245">Preferred organizational unit</span></span>

### <a name="update-resource-bookings-after-they-are-booked-on-a-project"></a><span data-ttu-id="c0843-246">Actualitzar les reserves de recursos un cop s'hagin reservat en un projecte</span><span class="sxs-lookup"><span data-stu-id="c0843-246">Update resource bookings after they are booked on a project</span></span>

<span data-ttu-id="c0843-247">Després d'afegir un recurs genèric o amb nom a un equip de projecte, podeu canviar les reserves del recurs.</span><span class="sxs-lookup"><span data-stu-id="c0843-247">After you've added a generic or named resource to a project team, you can change the resource's bookings.</span></span>

1. <span data-ttu-id="c0843-248">A la pàgina **Projectes**, a la pestanya **Equip**, seleccioneu un membre de l'equip i seleccioneu **Mantén les reserves**.</span><span class="sxs-lookup"><span data-stu-id="c0843-248">On the **Projects** page, on the **Team** tab, select a team member, and then select **Maintain Bookings**.</span></span>

    ![Tauler de planificació obert per al membre de l'equip seleccionat](media/Resource-Management-image40.png)

    <span data-ttu-id="c0843-250">El Tauler de planificació apareix i mostra les reserves de membres de l'equip del projecte.</span><span class="sxs-lookup"><span data-stu-id="c0843-250">The Schedule Board appears and shows the project team member's bookings.</span></span> <span data-ttu-id="c0843-251">Expandiu el registre del membre de l'equip per visualitzar les hores que s'han reservat a aquest projecte i altres projectes que estan consumint la capacitat del membre de l'equip.</span><span class="sxs-lookup"><span data-stu-id="c0843-251">Expand the team member's record to view the hours that have been booked against this project and other projects that are consuming the team member's capacity.</span></span>

2. <span data-ttu-id="c0843-252">Seleccioneu i arrossegueu la reserva per ampliar-la o reduir-la.</span><span class="sxs-lookup"><span data-stu-id="c0843-252">Select and drag the booking to extend or shorten it.</span></span> <span data-ttu-id="c0843-253">Apareix un quadre de diàleg **Crea la reserva de recursos** que us permet ajustar la reserva.</span><span class="sxs-lookup"><span data-stu-id="c0843-253">A **Create Resource Booking** dialog box appears that lets you adjust the booking.</span></span>

    ![Quadre de diàleg Crea la reserva de recursos](media/Resource-Management-image41.png)

3. <span data-ttu-id="c0843-255">Feu clic amb el botó dret a la reserva.</span><span class="sxs-lookup"><span data-stu-id="c0843-255">Right-click the booking.</span></span> <span data-ttu-id="c0843-256">A continuació, podeu utilitzar el menú de drecera per completar les accions següents:</span><span class="sxs-lookup"><span data-stu-id="c0843-256">You can then use the shortcut menu to complete the following actions:</span></span>

    - <span data-ttu-id="c0843-257">Canviar l'estat de la reserva.</span><span class="sxs-lookup"><span data-stu-id="c0843-257">Change the booking status.</span></span>
    - <span data-ttu-id="c0843-258">Editar la reserva.</span><span class="sxs-lookup"><span data-stu-id="c0843-258">Edit the booking.</span></span>
    - <span data-ttu-id="c0843-259">Substituir un recurs a l'equip del projecte.</span><span class="sxs-lookup"><span data-stu-id="c0843-259">Substitute a resource on the project team.</span></span>

### <a name="change-the-booking-status"></a><span data-ttu-id="c0843-260">Canviar l'estat de la reserva</span><span class="sxs-lookup"><span data-stu-id="c0843-260">Change the booking status</span></span>

<span data-ttu-id="c0843-261">Podeu canviar qualsevol estat de reserva per defecte o personalitzat.</span><span class="sxs-lookup"><span data-stu-id="c0843-261">You can change any default or custom booking status.</span></span>

![Ordre Canviar l'estat](media/Resource-Management-image42.png)

<span data-ttu-id="c0843-263">El PSA inclou els estats següents:</span><span class="sxs-lookup"><span data-stu-id="c0843-263">The following statuses are included in PSA:</span></span>

- <span data-ttu-id="c0843-264">**Cancel·lat**: l'estat cancel·la la reserva d'un recurs i allibera la capacitat del recurs.</span><span class="sxs-lookup"><span data-stu-id="c0843-264">**Canceled** – This status cancels a resource's booking and frees up the resource's capacity.</span></span>
- <span data-ttu-id="c0843-265">**Reserva fixa**: l'estat consumeix la capacitat d'un recurs.</span><span class="sxs-lookup"><span data-stu-id="c0843-265">**Hard Book** – This status consumes a resource's capacity.</span></span> <span data-ttu-id="c0843-266">Una reserva normalment té aquest estat quan obriu **Mantén les reserves** a la quadrícula **Tots els membres de l'equip** a la pàgina **Projectes**.</span><span class="sxs-lookup"><span data-stu-id="c0843-266">A booking typically has this status when you open **Maintain Bookings** from the **All Team Members** grid on the **Projects** page.</span></span>
- <span data-ttu-id="c0843-267">**Reserva flexible**: l'estat afegeix un recurs a un equip però no consumeix la capacitat del recurs.</span><span class="sxs-lookup"><span data-stu-id="c0843-267">**Soft Book** – This status adds a resource to a team but doesn't consume the resource's capacity.</span></span> <span data-ttu-id="c0843-268">Indica que el recurs s'ha reservat per a un treball potencial però té capacitat si és necessari en altres feines.</span><span class="sxs-lookup"><span data-stu-id="c0843-268">It indicates that the resource has been reserved for potential work but still has capacity if it's needed on other jobs.</span></span> <span data-ttu-id="c0843-269">A la visualització de la disponibilitat de recursos globals, les reserves flexibles tenen un estat diferent de les reserves fixes.</span><span class="sxs-lookup"><span data-stu-id="c0843-269">In the view of overall resource availability, soft bookings have a different status than hard bookings.</span></span>
- <span data-ttu-id="c0843-270">**Proposat**: l'estat representa una proposta de l'administrador de recursos o l'administrador de projectes per a un recurs.</span><span class="sxs-lookup"><span data-stu-id="c0843-270">**Proposed** – This status represents a resource manager's or project manager's proposal for a resource.</span></span> <span data-ttu-id="c0843-271">Les propostes no consumeixen la capacitat d'un recurs i el recurs no s'afegeix a l'equip del projecte.</span><span class="sxs-lookup"><span data-stu-id="c0843-271">Proposals don't consume the capacity of a resource, and the resource isn't added to the project team.</span></span> <span data-ttu-id="c0843-272">Per reservar el recurs de l'equip, l'administrador del projecte ha d'acceptar la proposta.</span><span class="sxs-lookup"><span data-stu-id="c0843-272">To hard-book the resource on the team, the project manager must accept the proposal.</span></span>

### <a name="submit-resource-requests"></a><span data-ttu-id="c0843-273">Enviar sol·licituds de recurs</span><span class="sxs-lookup"><span data-stu-id="c0843-273">Submit resource requests</span></span>

<span data-ttu-id="c0843-274">Les sol·licituds de recursos s'utilitzen per dur a terme la demanda (requisit de recurs) que ha de complir un administrador de recursos.</span><span class="sxs-lookup"><span data-stu-id="c0843-274">Resource requests are used to carry the demand (resource requirement) that must be fulfilled by a resource manager.</span></span> <span data-ttu-id="c0843-275">Per a un recurs genèric que ja està a l'equip, podeu enviar una sol·licitud de recurs directament.</span><span class="sxs-lookup"><span data-stu-id="c0843-275">For a generic resource thta is already on the team, you can submit a resource request directly.</span></span> <span data-ttu-id="c0843-276">Una sol·licitud de recurs es pot complir de dues maneres:</span><span class="sxs-lookup"><span data-stu-id="c0843-276">A resource request can be fulfilled in two ways:</span></span>

- <span data-ttu-id="c0843-277">L'administrador de recursos compleix directament la sol·licitud.</span><span class="sxs-lookup"><span data-stu-id="c0843-277">The resource manager directly fulfills the request.</span></span> <span data-ttu-id="c0843-278">En aquest cas, el recurs genèric se substitueix per una reserva fixa que té un recurs amb nom.</span><span class="sxs-lookup"><span data-stu-id="c0843-278">In this case, the generic resource is replaced by a hard booking that has a named resource.</span></span>
- <span data-ttu-id="c0843-279">L'administrador de recursos proposa un recurs a l'administrador de projectes i el director del projecte aprova o rebutja el recurs proposat.</span><span class="sxs-lookup"><span data-stu-id="c0843-279">The resource manager proposes a resource to the project manager, and the project manager approves or rejects the proposed resource.</span></span>

#### <a name="direct-fulfillment-of-resource-requests"></a><span data-ttu-id="c0843-280">Compliment directe de sol·licituds de recursos</span><span class="sxs-lookup"><span data-stu-id="c0843-280">Direct fulfillment of resource requests</span></span>

<span data-ttu-id="c0843-281">Quan es genera un requisit de recurs, un administrador de projecte pot enviar una sol·licitud de recurs per a un recurs genèric seleccionant el recurs i, a continuació, seleccionant **Envia la sol·licitud**.</span><span class="sxs-lookup"><span data-stu-id="c0843-281">When a resource requirement is generated, a project manager can submit a resource request for a generic resource by selecting the resource and then selecting **Submit Request**.</span></span>

![Botó Envia la sol·licitud](media/Resource-Management-image45.png)

<span data-ttu-id="c0843-283">Els comentaris sobre el recurs es poden proporcionar a l'administrador de recursos que està complint la sol·licitud.</span><span class="sxs-lookup"><span data-stu-id="c0843-283">Comments about the resource can be provided to the resource manager who is fulfilling the request.</span></span> <span data-ttu-id="c0843-284">Després d'enviar la sol·licitud, el camp **Estat** per al membre de l'equip canvia a **Enviat**.</span><span class="sxs-lookup"><span data-stu-id="c0843-284">After the request is submitted, the **Status** field for the team member is changed to **Submitted**.</span></span>

![Introduir comentaris opcionals](media/Resource-Management-image46.png)

<span data-ttu-id="c0843-286">Quan l'administrador de recursos compleix la sol·licitud, el membre de l'equip genèric se substitueix pel recurs amb nom a la quadrícula **Tots els membres de l'equip**.</span><span class="sxs-lookup"><span data-stu-id="c0843-286">When the resource manager fulfills the request, the generic team member is replaced by the named resource in the **All Team Members** grid.</span></span>

![Membre de l'equip genèric substituït pel recurs amb nom a la quadrícula Tots els membres de l'equip](media/Resource-Management-image47.png)

#### <a name="use-a-resource-proposal-for-resource-requests"></a><span data-ttu-id="c0843-288">Utilitzar una proposta de recurs per a sol·licituds de recursos</span><span class="sxs-lookup"><span data-stu-id="c0843-288">Use a resource proposal for resource requests</span></span>

<span data-ttu-id="c0843-289">En lloc de fer la reserva directament d'un recurs d'una sol·licitud de recurs, un administrador de recursos pot proposar un recurs a l'administrador del projecte.</span><span class="sxs-lookup"><span data-stu-id="c0843-289">Instead of directly booking a resource on a resource request, a resource manager can propose a resource to the project manager.</span></span> <span data-ttu-id="c0843-290">Pot ser que un administrador de recursos utilitzi aquesta opció quan no hi hagi una coincidència exacta per als requisits.</span><span class="sxs-lookup"><span data-stu-id="c0843-290">A resource manager might use this option when an exact match for the requirements isn't available.</span></span> <span data-ttu-id="c0843-291">Quan un administrador de recursos proposa un recurs, l'administrador del projecte veu que el camp **Estat** del membre genèric de l'equip canvia a **Necessita revisió**.</span><span class="sxs-lookup"><span data-stu-id="c0843-291">When a resource manager proposes a resource, the project manager sees that the **Status** field for the generic team member is changed to **Needs Review**.</span></span>

![Estat d'un membre de l'equip genèric canviat a Necessita revisió](media/Resource-Management-image48.png)

<span data-ttu-id="c0843-293">Per visualitzar el recurs proposat juntament amb una visualització de l'efecte de la reserva de la proposta, feu doble clic al membre de l'equip que tingui l'estat **Necessita revisió**.</span><span class="sxs-lookup"><span data-stu-id="c0843-293">To view the proposed resource together with a visualization of the effect of the proposal's booking, double-click the team member that has a status of **Needs Review**.</span></span> <span data-ttu-id="c0843-294">A continuació, seleccioneu la pestanya **Recursos proposats**.</span><span class="sxs-lookup"><span data-stu-id="c0843-294">Then select the **Proposed Resources** tab.</span></span>

![Pestanya Recursos proposats](media/Resource-Management-image49.png)

<span data-ttu-id="c0843-296">Seleccioneu **Accepta totes les propostes** per acceptar tots els recursos proposats o **Rebutja totes les propostes** per rebutjar-les.</span><span class="sxs-lookup"><span data-stu-id="c0843-296">Select **Accept All Proposals** to accept all proposed resources or **Reject All Proposals** to reject them.</span></span> <span data-ttu-id="c0843-297">Si accepteu els recursos proposats, es reserven de manera fixa al projecte com a membres de l'equip i reemplacen els recursos genèrics.</span><span class="sxs-lookup"><span data-stu-id="c0843-297">If you accept the proposed resources, they are hard-booked on the project as team members and replace the generic resources.</span></span>

> [!NOTE]
> <span data-ttu-id="c0843-298">Heu d'acceptar o rebutjar tots els recursos proposats.</span><span class="sxs-lookup"><span data-stu-id="c0843-298">You must either accept or reject all proposed resources.</span></span> <span data-ttu-id="c0843-299">No es poden acceptar ni rebutjar parcialment.</span><span class="sxs-lookup"><span data-stu-id="c0843-299">You can't partially accept or reject them.</span></span>

### <a name="substitute-a-resource-on-the-project-team"></a><span data-ttu-id="c0843-300">Substituir un recurs a l'equip del projecte</span><span class="sxs-lookup"><span data-stu-id="c0843-300">Substitute a resource on the project team</span></span>

<span data-ttu-id="c0843-301">De vegades, un administrador de projecte ha de substituir un membre de l'equip reservat en un projecte.</span><span class="sxs-lookup"><span data-stu-id="c0843-301">Sometimes, a project manager must substitute a booked team member on a project.</span></span>

1. <span data-ttu-id="c0843-302">A la pàgina **Projectes**, a la pestanya **Equip**, seleccioneu el recurs que cal substituir i seleccioneu **Mantén les reserves**.</span><span class="sxs-lookup"><span data-stu-id="c0843-302">On the **Projects** page, on the **Team** tab, select the resource that needs a substitute, and then select **Maintain Bookings**.</span></span>
2. <span data-ttu-id="c0843-303">Expandiu el recurs per visualitzar els projectes als quals està assignat.</span><span class="sxs-lookup"><span data-stu-id="c0843-303">Expand the resource to view the projects that it's assigned to.</span></span>

    ![Recurs ampliat per mostrar els projectes assignats](media/Resource-Management-image50.png)

3. <span data-ttu-id="c0843-305">Feu clic amb el botó dret del ratolí al projecte i seleccioneu **Substitueix el recurs**.</span><span class="sxs-lookup"><span data-stu-id="c0843-305">Right-click the project, and then select **Substitute Resource**.</span></span>
4. <span data-ttu-id="c0843-306">Si coneixeu el recurs que voleu substituir per al recurs actual, seleccioneu o escriviu-ne el nom i, a continuació, seleccioneu **Torna a assignar**.</span><span class="sxs-lookup"><span data-stu-id="c0843-306">If you know the resource that you want to substitute for the current resource, select or type the name, and then select **Re-assign**.</span></span>

    ![Especificar d'un recurs substitut](media/Resource-Management-image51.png)

    <span data-ttu-id="c0843-308">De manera alternativa, seguiu aquests passos per cercar un recurs:</span><span class="sxs-lookup"><span data-stu-id="c0843-308">Alternatively, follow these steps to search for a resource:</span></span>

    1. <span data-ttu-id="c0843-309">Seleccioneu **Cerca una substitució**.</span><span class="sxs-lookup"><span data-stu-id="c0843-309">Select **Find Substitution**.</span></span>

        ![Cercar un recurs substitut](media/Resource-Management-image52.png)

        <span data-ttu-id="c0843-311">L'Auxiliar de planificacions retorna una llista de substituts disponibles.</span><span class="sxs-lookup"><span data-stu-id="c0843-311">The Schedule Assistant returns a list of available substitutes.</span></span> <span data-ttu-id="c0843-312">A l'Auxiliar de planificació, podeu continuar filtrant els recursos disponibles per trobar un substitut adient.</span><span class="sxs-lookup"><span data-stu-id="c0843-312">In the Schedule Assistant, you can further filter the available resources to find a suitable substitute.</span></span>

        ![Llista dels substituts disponibles](media/Resource-Management-image53.png)

    2. <span data-ttu-id="c0843-314">Per substituir el recurs, seleccioneu el recurs que voleu i, a continuació, seleccioneu **Substitueix**.</span><span class="sxs-lookup"><span data-stu-id="c0843-314">To substitute the resource, select the resource that you want, and then select **Substitute**.</span></span>

        ![Recurs substitut seleccionat](media/Resource-Management-image54.png)

    <span data-ttu-id="c0843-316">Les reserves i assignacions es substitueixen pel recurs nou.</span><span class="sxs-lookup"><span data-stu-id="c0843-316">The bookings and assignments are substituted with the new resource.</span></span>

    ![Reserves i assignacions substituïdes pel recurs nou](media/Resource-Management-image55.png)

## <a name="reconcile-team-member-bookings-and-assignments"></a><span data-ttu-id="c0843-318">Conciliar les reserves dels membres de l'equip i les assignacions</span><span class="sxs-lookup"><span data-stu-id="c0843-318">Reconcile team member bookings and assignments</span></span>

<span data-ttu-id="c0843-319">Per als membres de l'equip, les reserves i assignacions estan lleugerament vinculades.</span><span class="sxs-lookup"><span data-stu-id="c0843-319">For team members, bookings and assignments are loosely coupled.</span></span> <span data-ttu-id="c0843-320">En altres paraules, els recursos poden tenir assignacions però no reserves, o poden tenir reserves però no assignacions.</span><span class="sxs-lookup"><span data-stu-id="c0843-320">In other words, resources can have assignments but no bookings, or they can have bookings but no assignments.</span></span> <span data-ttu-id="c0843-321">Idealment, les reserves i assignacions s'han d'alinear perquè els recursos tinguin capacitat confirmada de dur a terme l'assignació de tasques.</span><span class="sxs-lookup"><span data-stu-id="c0843-321">Ideally, bookings and assignments should be aligned, so that resources have committed capacity to perform the task assignments.</span></span> <span data-ttu-id="c0843-322">No obstant, les reserves poden basar-se en la disponibilitat i els temps de treball podrien canviar a mesura que el projecte continua.</span><span class="sxs-lookup"><span data-stu-id="c0843-322">However, the bookings might be based on availability, and task timings might change as the project continues.</span></span> <span data-ttu-id="c0843-323">Per tant, la lleugera vinculació de les reserves i les assignacions proporciona flexibilitat.</span><span class="sxs-lookup"><span data-stu-id="c0843-323">Therefore, the loose coupling of bookings and assignments provides flexibility.</span></span>

<span data-ttu-id="c0843-324">El PSA té una pestanya **Conciliació** que permet als administradors projectar les reserves dels membres de l'equip i els seus treballs per a equips de projectes.</span><span class="sxs-lookup"><span data-stu-id="c0843-324">PSA has a **Reconciliation** tab that lets project managers reconcile team members' bookings and their assignments for project teams.</span></span>

![Pestanya Conciliació](media/Resource-Management-image56.png)

<span data-ttu-id="c0843-326">La pestanya **Conciliació** mostra les reserves i les assignacions al nivell de l'assignació de tasques individuals per a cada membre de l'equip.</span><span class="sxs-lookup"><span data-stu-id="c0843-326">The **Reconciliation** tab shows bookings and assignments down to the level of the individual task assignment for each team member.</span></span> <span data-ttu-id="c0843-327">Mostra hores a les cel·les que representen períodes de temps de mesos a dies.</span><span class="sxs-lookup"><span data-stu-id="c0843-327">It shows hours in cells that represent time periods from months down to days.</span></span>

<span data-ttu-id="c0843-328">La pestanya també mostra un total de la xarxa global per al projecte, juntament amb una columna total.</span><span class="sxs-lookup"><span data-stu-id="c0843-328">The tab also shows an overall net total for the project, together with a total column.</span></span>

<span data-ttu-id="c0843-329">Per a cada recurs, la pestanya calcula la diferència entre les reserves dels membres de l'equip i un valor consolidat de les assignacions de tasques del membre de l'equip.</span><span class="sxs-lookup"><span data-stu-id="c0843-329">For each resource, the tab calculates the difference between the team member's bookings and a rollup of the team member's task assignments.</span></span> <span data-ttu-id="c0843-330">Idealment, aquesta diferència hauria de ser 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="c0843-330">Ideally, this difference should be 0 (zero).</span></span> <span data-ttu-id="c0843-331">En altres paraules, no hi hauria d'haver diferències entre les reserves i les assignacions.</span><span class="sxs-lookup"><span data-stu-id="c0843-331">In other words, there should be no difference between bookings and assignments.</span></span> <span data-ttu-id="c0843-332">Les diferències es marquen amb color i un ombrejat per cridar l'atenció sobre dues condicions:</span><span class="sxs-lookup"><span data-stu-id="c0843-332">Differences are colored and shaded to draw attention to two conditions:</span></span>

- <span data-ttu-id="c0843-333">**Manca de reserves**: una manca de reserves es produeix quan un recurs té més assignacions que reserves.</span><span class="sxs-lookup"><span data-stu-id="c0843-333">**Booking shortage** – A booking shortage occurs when a resource has more assignments than bookings.</span></span> <span data-ttu-id="c0843-334">Com que aquesta capacitat no s'ha reservat, un administrador de projecte pot voler corregir aquesta situació ampliant les reserves del recurs fins a cobrir el dèficit.</span><span class="sxs-lookup"><span data-stu-id="c0843-334">Because this capacity hasn't been reserved, a project manager might want to correct this condition by extending the resource's bookings to cover the deficit.</span></span>
- <span data-ttu-id="c0843-335">**Excés de reserves**: un excés de reserves es produeix quan un recurs s'ha reservat al projecte però no s'ha assignat a tasques.</span><span class="sxs-lookup"><span data-stu-id="c0843-335">**Excess bookings** – Excess bookings occur when a resource has been booked to the project but hasn't been assigned to tasks.</span></span> <span data-ttu-id="c0843-336">Aquesta situació podria ser acceptable en els casos en què s'ha reservat el recurs al projecte abans d'haver produït una assignació de tasques.</span><span class="sxs-lookup"><span data-stu-id="c0843-336">This condition might be acceptable in the cases where the resource was booked to the project before task assignment occurred.</span></span> <span data-ttu-id="c0843-337">No obstant, en altres casos, el recurs no està planificat per assignar-se a tasques.</span><span class="sxs-lookup"><span data-stu-id="c0843-337">However, in other cases, the resource isn't planned to be assigned to tasks.</span></span> <span data-ttu-id="c0843-338">En aquests casos, l'administrador del projecte hauria de considerar la cancel·lació de les reserves del recurs, de manera que la capacitat pugui utilitzar-se per a un altre projecte.</span><span class="sxs-lookup"><span data-stu-id="c0843-338">In these cases, the project manager should consider canceling the resource's bookings, so that the capacity can be used for another project.</span></span>

<span data-ttu-id="c0843-339">En alguns casos, quan visualitzeu temps en un nivell superior al nivell de dia (per exemple, al nivell de mes), pot ser que vegeu una diferència neta de zero per a un recurs (en altres paraules, reserves = assignacions).</span><span class="sxs-lookup"><span data-stu-id="c0843-339">In some cases, when you view time at a higher level than the day level (for example, the month level), you might see a net difference of zero for a resource (in other words, bookings = assignments).</span></span> <span data-ttu-id="c0843-340">No obstant, si visualitzeu temps al nivell de la setmana, podeu veure que hi ha assignacions de zero hores i reserves de 40 hores a la primera setmana, però assignacions de 40 hores i reserves de zero hores a la segona setmana.</span><span class="sxs-lookup"><span data-stu-id="c0843-340">However, if you view time at the week level, you might see that there are assignments of zero hours and bookings of 40 hours in the first week, but assignments of 40 hours and bookings of zero hours in the second week.</span></span> <span data-ttu-id="c0843-341">En general, les reserves i assignacions es concilien, però difereixen d'una setmana a la següent.</span><span class="sxs-lookup"><span data-stu-id="c0843-341">Overall, the bookings and assignments are reconciled, but they differ from one week to the next.</span></span>

<span data-ttu-id="c0843-342">Quan visualitzeu el temps en nivells superiors, les cel·les de la pestanya **Conciliació** tenen un indicador per informar-vos que hi ha diferències en nivells inferiors.</span><span class="sxs-lookup"><span data-stu-id="c0843-342">When you view time at higher levels, cells in the **Reconciliation** tab have an indicator to inform you that there are differences at lower levels.</span></span> <span data-ttu-id="c0843-343">En fer doble clic en una cel·la, podeu apropar el zoom per visualitzar la diferència.</span><span class="sxs-lookup"><span data-stu-id="c0843-343">By double-clicking in a cell, you can zoom in to view the difference.</span></span> <span data-ttu-id="c0843-344">A continuació, podeu fer clic amb el botó dret per allunyar-vos. En seleccionar un recurs i utilitzar el control **Diferència següent** a la barra d'eines de la quadrícula, podeu anar a la diferència següent entre les reserves i les assignacions d'aquest recurs.</span><span class="sxs-lookup"><span data-stu-id="c0843-344">You can then right-click to zoom out. By selecting a resource and then using the **Next difference** control on the grid toolbar, you can go to the next difference between bookings and assignments for that resource.</span></span> <span data-ttu-id="c0843-345">A continuació, podeu utilitzar el control **Diferència anterior** per tornar enrere.</span><span class="sxs-lookup"><span data-stu-id="c0843-345">You can then use the **Previous difference** control to go back.</span></span> <span data-ttu-id="c0843-346">També podeu desactivar l'indicador de diferències i el comportament de la navegació a **Configuració**.</span><span class="sxs-lookup"><span data-stu-id="c0843-346">You can also turn off the difference indicator and navigation behavior under **Settings**.</span></span>

![Indicador de diferències](media/Resource-Management-image57.png)

<span data-ttu-id="c0843-348">Si teniu assignacions de tasca per a un recurs però no hi ha cap reserva, a la pàgina **Projectes**, a la pestanya **Conciliació**, seleccioneu la manca de reserves i, a continuació, seleccioneu **Amplia la reserva**.</span><span class="sxs-lookup"><span data-stu-id="c0843-348">If you have task assignments for a resource but no bookings, on the **Projects** page, on the **Reconciliation** tab, select the booking shortage, and then select **Extend Booking**.</span></span> <span data-ttu-id="c0843-349">El quadre de diàleg **Amplia la reserva** apareix i mostra la reserva necessària per fer front a la manca del recurs.</span><span class="sxs-lookup"><span data-stu-id="c0843-349">The **Extend Booking** dialog box appears and shows the booking that is needed to address the resource's shortage.</span></span> <span data-ttu-id="c0843-350">També mostra les reserves existents del recurs en tots els projectes o altres entitats planificables.</span><span class="sxs-lookup"><span data-stu-id="c0843-350">It also shows the resource's existing bookings across all projects or other schedulable entities.</span></span> <span data-ttu-id="c0843-351">Si seleccioneu **D'acord** per crear la reserva del recurs, independentment de la disponibilitat del recurs, pot ser que hi hagi un excés de reserves.</span><span class="sxs-lookup"><span data-stu-id="c0843-351">If you select **OK** to create the booking for the resource, regardless of that resource's availability, you might cause overbooking.</span></span>

![Quadre de diàleg Amplia la reserva](media/Resource-Management-image58.png)

<span data-ttu-id="c0843-353">L'administrador de projectes o administrador de recursos poden utilitzar el Tauler de planificació per administrar les situacions en què el recurs té un excés de reserves més enllà de la seva capacitat.</span><span class="sxs-lookup"><span data-stu-id="c0843-353">The project manager or resource manager can then use the Schedule Board to manage any situations where a resource is overbooked beyond its capacity.</span></span>