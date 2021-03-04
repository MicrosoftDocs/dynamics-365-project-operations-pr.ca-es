---
title: Planificar un projecte amb una estructura del desglossament del treball
description: Com planificar un projecte amb una estructura del desglossament del treball al Project Service
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: cf12cc3bcf061e1daffafb248cfd76809c6444ec
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149801"
---
# <a name="schedule-a-project-with-a-work-breakdown-structure-project-service"></a><span data-ttu-id="5dc52-103">Planificar un projecte amb una estructura del desglossament del treball (Project Service)</span><span class="sxs-lookup"><span data-stu-id="5dc52-103">Schedule a project with a work breakdown structure (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="5dc52-104">Una planificació de projecte comunica quina feina s'ha de realitzar, quins recursos realitzaran la feina i el termini en el qual s'ha de completar la feina.</span><span class="sxs-lookup"><span data-stu-id="5dc52-104">A project schedule communicates what work needs to be performed, which resources will perform the work, and the timeframe in which that work needs to be completed.</span></span> <span data-ttu-id="5dc52-105">La planificació del projecte reflecteix tota la feina associada amb el lliurament del projecte a temps.</span><span class="sxs-lookup"><span data-stu-id="5dc52-105">The project schedule reflects all the work associated with delivering the project on time.</span></span> <span data-ttu-id="5dc52-106">Un dels primers passos en la fase d'iniciació del projecte és elaborar una planificació de projecte.</span><span class="sxs-lookup"><span data-stu-id="5dc52-106">One of the first steps in the initiation phase of the project is to come up with a project schedule.</span></span> <span data-ttu-id="5dc52-107">Per establir una planificació de projecte, heu de crear una estructura del desglossament del treball.</span><span class="sxs-lookup"><span data-stu-id="5dc52-107">To establish a project schedule, you need to create a work breakdown structure.</span></span>  
  
 <span data-ttu-id="5dc52-108">Creeu una estructura de projecte amb una estructura de desglossament de treball que us ajudi a:</span><span class="sxs-lookup"><span data-stu-id="5dc52-108">Create a project structure with a work breakdown structure, which helps you:</span></span>  
  
- <span data-ttu-id="5dc52-109">Dividir la feina en tasques gestionables</span><span class="sxs-lookup"><span data-stu-id="5dc52-109">Break down work into manageable tasks</span></span>  
  
- <span data-ttu-id="5dc52-110">Calcular el temps necessari per completar una tasca</span><span class="sxs-lookup"><span data-stu-id="5dc52-110">Estimate the time required to complete a task</span></span>  
  
- <span data-ttu-id="5dc52-111">Definir dependències de tasca i la durada de la tasca</span><span class="sxs-lookup"><span data-stu-id="5dc52-111">Set task dependencies and task duration</span></span>  
  
- <span data-ttu-id="5dc52-112">Determinar les funcions necessàries per completar cada tasca</span><span class="sxs-lookup"><span data-stu-id="5dc52-112">Determine the roles required to complete each task</span></span>  
  
  <span data-ttu-id="5dc52-113">La planificació del projecte en l'estructura del desglossament del treball té un aspecte i un funcionament familiars complementat amb un gràfic de Gantt interactiu.</span><span class="sxs-lookup"><span data-stu-id="5dc52-113">The project schedule in the work breakdown structure has a familiar look and feel, complete with an interactive Gantt chart.</span></span>  
  
## <a name="create-a-work-breakdown-structure-for-a-project"></a><span data-ttu-id="5dc52-114">Crear una estructura del desglossament del treball per a un projecte</span><span class="sxs-lookup"><span data-stu-id="5dc52-114">Create a work breakdown structure for a project</span></span>  
 <span data-ttu-id="5dc52-115">Creeu una estructura del desglossament del treball per representar la seqüència de les tasques en un projecte.</span><span class="sxs-lookup"><span data-stu-id="5dc52-115">Create a work breakdown structure to represent the sequence of tasks in a project.</span></span> <span data-ttu-id="5dc52-116">L'estructura del desglossament del treball inclou tasques, requisits per a cada tasca i informació dels ingressos i els costos.</span><span class="sxs-lookup"><span data-stu-id="5dc52-116">The work breakdown structure includes tasks, requirements for each task, and revenue and cost information.</span></span> <span data-ttu-id="5dc52-117">A la vostra estructura del desglossament del treball, podeu afegir:</span><span class="sxs-lookup"><span data-stu-id="5dc52-117">In your work breakdown structure, you can add:</span></span>  
  
-   <span data-ttu-id="5dc52-118">La seqüència de les tasques en una jerarquia</span><span class="sxs-lookup"><span data-stu-id="5dc52-118">The sequence of tasks in a hierarchy</span></span>  
  
-   <span data-ttu-id="5dc52-119">Altres tasques, si escau, que s'han de completar per poder iniciar una tasca</span><span class="sxs-lookup"><span data-stu-id="5dc52-119">Other tasks, if any, that must be completed before a task can be started</span></span>  
  
-   <span data-ttu-id="5dc52-120">La data d'inici, la data final i la durada d'una tasca</span><span class="sxs-lookup"><span data-stu-id="5dc52-120">The starting date, ending date, and duration of a task</span></span>  
  
-   <span data-ttu-id="5dc52-121">Nombre d'hores necessàries per a una tasca</span><span class="sxs-lookup"><span data-stu-id="5dc52-121">The number of hours required for a task</span></span>  
  
-   <span data-ttu-id="5dc52-122">Qualsevol habilitat i formació necessàries d'un treballador</span><span class="sxs-lookup"><span data-stu-id="5dc52-122">Any required worker skills and education</span></span>  
  
-   <span data-ttu-id="5dc52-123">Els treballadors assignats a una tasca</span><span class="sxs-lookup"><span data-stu-id="5dc52-123">The workers who are assigned to a task</span></span>  
  
-   <span data-ttu-id="5dc52-124">Ingressos i costos previstos</span><span class="sxs-lookup"><span data-stu-id="5dc52-124">Estimated revenue and costs</span></span>  
  
## <a name="task-types"></a><span data-ttu-id="5dc52-125">Tipus de tasca</span><span class="sxs-lookup"><span data-stu-id="5dc52-125">Task types</span></span>  
<span data-ttu-id="5dc52-126">Utilitzareu els següents tipus de tasques per crear l'estructura del desglossament del treball:</span><span class="sxs-lookup"><span data-stu-id="5dc52-126">You’ll use the following types of tasks when creating your work breakdown structure:</span></span>  

| | | 
|---------------------------------------|-----------------------------------------------------------------| 
| <span data-ttu-id="5dc52-127">**Node arrel del projecte**</span><span class="sxs-lookup"><span data-stu-id="5dc52-127">**Project root node**</span></span> | <span data-ttu-id="5dc52-128">La tasca de resum de nivell superior per al projecte.</span><span class="sxs-lookup"><span data-stu-id="5dc52-128">The top-level summary task for the project.</span></span> <span data-ttu-id="5dc52-129">Totes les altres tasques de projecte es creen a sota.</span><span class="sxs-lookup"><span data-stu-id="5dc52-129">All other project tasks are created under it.</span></span> <span data-ttu-id="5dc52-130">El nom de la tasca arrel és el nom de projecte.</span><span class="sxs-lookup"><span data-stu-id="5dc52-130">The name of the root task is the project name.</span></span> <span data-ttu-id="5dc52-131">L'esforç, les dates i la duració del node arrel es basen en els valors a la jerarquia que hi ha per sota.</span><span class="sxs-lookup"><span data-stu-id="5dc52-131">The effort, dates, and duration of the root node are based on the values on the hierarchy below it.</span></span> <span data-ttu-id="5dc52-132">No podeu editar les propietats de node arrel ni suprimir el node arrel.</span><span class="sxs-lookup"><span data-stu-id="5dc52-132">You can’t edit root node properties or delete the root node.</span></span> | 
| <span data-ttu-id="5dc52-133">**Tasques de resum o de contenidor**</span><span class="sxs-lookup"><span data-stu-id="5dc52-133">**Summary or container tasks**</span></span> | <span data-ttu-id="5dc52-134">Una tasca de resum és una tasca de la qual pengen subtasques.</span><span class="sxs-lookup"><span data-stu-id="5dc52-134">A summary task is a task that has sub-tasks under it.</span></span> <span data-ttu-id="5dc52-135">Una tasca de resum no té cap esforç de treball ni el cost propi.</span><span class="sxs-lookup"><span data-stu-id="5dc52-135">A summary task doesn’t have any work effort or cost of its own.</span></span> <span data-ttu-id="5dc52-136">El seu esforç i cost de treball són un valor consolidat de les seves subtasques.</span><span class="sxs-lookup"><span data-stu-id="5dc52-136">Its work effort and cost are a rollup of its sub-tasks.</span></span> <span data-ttu-id="5dc52-137">Podeu canviar el nom d'una tasca de resum, però no podeu canviar l'esforç, les dates o la durada perquè es calculen automàticament.</span><span class="sxs-lookup"><span data-stu-id="5dc52-137">You can change the name of a summary task, but you can’t change the effort, dates, or duration, because those are automatically calculated.</span></span> <span data-ttu-id="5dc52-138">Si suprimiu una tasca de resum se suprimeix la tasca i totes les seves subtasques.</span><span class="sxs-lookup"><span data-stu-id="5dc52-138">Deleting a summary task deletes the task and all of its sub-tasks.</span></span>|  
| <span data-ttu-id="5dc52-139">**Tasques de node fulla**</span><span class="sxs-lookup"><span data-stu-id="5dc52-139">**Leaf node tasks**</span></span> | <span data-ttu-id="5dc52-140">Una tasca de node fulla representa el treball més detallat del projecte.</span><span class="sxs-lookup"><span data-stu-id="5dc52-140">A leaf node task represents the most detailed work on the project.</span></span> <span data-ttu-id="5dc52-141">Té un esforç previst, un nombre de recursos planificat, dates d'inici i final planificades i una durada.</span><span class="sxs-lookup"><span data-stu-id="5dc52-141">It has an estimated effort, a planned number of resources, planned start and end dates, and a duration.</span></span>|

  
## <a name="task-hierarchy"></a><span data-ttu-id="5dc52-142">Jerarquia de tasques</span><span class="sxs-lookup"><span data-stu-id="5dc52-142">Task hierarchy</span></span>  
 <span data-ttu-id="5dc52-143">Teniu les opcions següents per crear una jerarquia de tasques:</span><span class="sxs-lookup"><span data-stu-id="5dc52-143">You have the following options when creating a task hierarchy:</span></span>  
  
- <span data-ttu-id="5dc52-144">**Afegeix tasca**.</span><span class="sxs-lookup"><span data-stu-id="5dc52-144">**Add task**.</span></span>   <span data-ttu-id="5dc52-145">Podeu afegir una tasca en una posició que trieu a la jerarquia de tasques.</span><span class="sxs-lookup"><span data-stu-id="5dc52-145">You can add a task at a position you choose in the task hierarchy.</span></span> <span data-ttu-id="5dc52-146">Si no seleccioneu una posició, la vostra nova tasca apareix al final.</span><span class="sxs-lookup"><span data-stu-id="5dc52-146">If you don’t select a position, your new task appears at the end.</span></span>  
  
- <span data-ttu-id="5dc52-147">**Aplica sagnia a tasca**.</span><span class="sxs-lookup"><span data-stu-id="5dc52-147">**Indent task**.</span></span>   <span data-ttu-id="5dc52-148">Aplica sagnia a una tasca per convertir-la en una tasca secundària de la tasca directament superior.</span><span class="sxs-lookup"><span data-stu-id="5dc52-148">Indent a task to make it a child of the task directly above it.</span></span>  
  
- <span data-ttu-id="5dc52-149">**Anul·la sagnia de tasca**</span><span class="sxs-lookup"><span data-stu-id="5dc52-149">**Outdent task**.</span></span>   <span data-ttu-id="5dc52-150">Anul·la una sagnia d'una tasca per deixar que sigui una subtasca de la seva tasca principal original.</span><span class="sxs-lookup"><span data-stu-id="5dc52-150">Outdent a task to make it so it’s no longer a sub-task of its original parent task.</span></span>  
  
- <span data-ttu-id="5dc52-151">**Puja i baixa**.</span><span class="sxs-lookup"><span data-stu-id="5dc52-151">**Move up and Move down**.</span></span>   <span data-ttu-id="5dc52-152">Desplaça les tasques amunt i avall a la jerarquia de la seva tasca principal.</span><span class="sxs-lookup"><span data-stu-id="5dc52-152">Move tasks up and down in the hierarchy of its parent task.</span></span> <span data-ttu-id="5dc52-153">El desplaçament amunt o avall d'una tasca no té cap efecte sobre el seu esforç, cost, dates o durada.</span><span class="sxs-lookup"><span data-stu-id="5dc52-153">Moving a task up or down has no effect on its effort, cost, dates, or duration.</span></span>  
  
## <a name="task-attributes"></a><span data-ttu-id="5dc52-154">Atributs de la tasca</span><span class="sxs-lookup"><span data-stu-id="5dc52-154">Task attributes</span></span>  
 <span data-ttu-id="5dc52-155">Un nom de tasca descriu el treball que s'ha de completar.</span><span class="sxs-lookup"><span data-stu-id="5dc52-155">A task’s name describes the work that needs to be completed.</span></span> <span data-ttu-id="5dc52-156">Utilitzeu diversos atributs de tasca per descriure els requisits de personal i de planificació per a la tasca.</span><span class="sxs-lookup"><span data-stu-id="5dc52-156">You use various task attributes to describe the schedule and staffing requirements for the task.</span></span>  
  
### <a name="schedule-attributes"></a><span data-ttu-id="5dc52-157">Atributs de planificació</span><span class="sxs-lookup"><span data-stu-id="5dc52-157">Schedule attributes</span></span>

 - <span data-ttu-id="5dc52-158">Assigneu valors a **Hores d'esforç**, **Nombre de recursos**, **Data d'inici**, **Data final** i **Durada** per determinar la planificació de la tasca.</span><span class="sxs-lookup"><span data-stu-id="5dc52-158">Assign values to **Effort hours**, **Number of resources**, **Start date**, **End date**, and **Duration** to determine the schedule for the task.</span></span> 
 - <span data-ttu-id="5dc52-159">**Esforç** és una estimació de les hores que es necessiten per completar la tasca.</span><span class="sxs-lookup"><span data-stu-id="5dc52-159">**Effort** is an estimate of the hours it takes to complete the task.</span></span>
 - <span data-ttu-id="5dc52-160">**Nombre de recursos** és una estimació que l'administrador del projecte posa a la tasca per assolir la millor planificació possible.</span><span class="sxs-lookup"><span data-stu-id="5dc52-160">**Number of resources** is an estimate that the project manager puts in the task to help come up with the best possible schedule.</span></span> 
 - <span data-ttu-id="5dc52-161">**Durada** (en dies) indica el nombre de dies laborables que es necessita per completar la tasca.</span><span class="sxs-lookup"><span data-stu-id="5dc52-161">**Duration** (in days) indicates the number of work days it will take to complete the task.</span></span>  
  
### <a name="staffing-attributes"></a><span data-ttu-id="5dc52-162">Atributs de personal</span><span class="sxs-lookup"><span data-stu-id="5dc52-162">Staffing attributes</span></span>

 - <span data-ttu-id="5dc52-163">**Funció**, **Unitat organitzativa de recurs**, **Nombre de recursos** i **Recursos** descriuen els requisits de personal per a la tasca.</span><span class="sxs-lookup"><span data-stu-id="5dc52-163">**Role**, **Resource organizational unit**, **Number of resources**, and **Resources** describe the staffing requirements for the task.</span></span> 
 - <span data-ttu-id="5dc52-164">**Funció** descriu el tipus de recurs necessari per realitzar la tasca.</span><span class="sxs-lookup"><span data-stu-id="5dc52-164">**Role** describes the type of resource needed to perform the task.</span></span> 
 - <span data-ttu-id="5dc52-165">**Unitat organitzativa de recurs** indica la unitat organitzativa de recursos des de la qual els recursos s'han de dotar a la tasca; això també influeix en l'estimació de costos i vendes de la tasca, ja que es té en compte en determinar el preu de venda unitari del recurs.</span><span class="sxs-lookup"><span data-stu-id="5dc52-165">**Resource organizational unit** indicates the organizational unit from which resources should be staffed for that task; this also impacts the cost and sales estimate of the task, since this is accounted for when determining the unit sales price for the resource.</span></span> 
 - <span data-ttu-id="5dc52-166">**Recursos** conté un recurs genèric o un recurs amb nom quan se'n troba un.</span><span class="sxs-lookup"><span data-stu-id="5dc52-166">**Resources** holds a generic resource or a named resource when one is found.</span></span>  
  
## <a name="task-dependencies"></a><span data-ttu-id="5dc52-167">Dependències de tasca</span><span class="sxs-lookup"><span data-stu-id="5dc52-167">Task dependencies</span></span>  
 <span data-ttu-id="5dc52-168">Podeu crear relacions de predecessor entre una o més tasques a l'estructura del desglossament del treball.</span><span class="sxs-lookup"><span data-stu-id="5dc52-168">You can create predecessor relationships between one or more tasks in the work breakdown structure.</span></span> <span data-ttu-id="5dc52-169">Podeu posar un o més valors del camp predecessor a les tasques per indicar les tasques de les quals serà dependent.</span><span class="sxs-lookup"><span data-stu-id="5dc52-169">You can set one or more values for the predecessor field on tasks to indicate the tasks that it will be dependent on.</span></span> <span data-ttu-id="5dc52-170">Quan assigneu un valor de predecessor a una tasca, la tasca només pot començar quan hagin finalitzat totes les tasques de predecessor.</span><span class="sxs-lookup"><span data-stu-id="5dc52-170">When you assign a predecessor value to a task, the task can only start when all the predecessor tasks have completed.</span></span> <span data-ttu-id="5dc52-171">Si definiu aquesta dependència en una tasca, es tornarà a calcular la data d'inici prevista de la tasca com l'últim final de tots els seus predecessors.</span><span class="sxs-lookup"><span data-stu-id="5dc52-171">Setting this dependency on a task will result in the recalculation of the planned start date of the task as the latest end of all of its predecessors.</span></span> <span data-ttu-id="5dc52-172">Els impactes relacionats amb el predecessor en una planificació no es limiten al mode de tasca definit a la tasca.</span><span class="sxs-lookup"><span data-stu-id="5dc52-172">Predecessor-related impacts on a schedule are not limited by the task mode defined on the task.</span></span>  
  
## <a name="task-mode"></a><span data-ttu-id="5dc52-173">Mode de tasca</span><span class="sxs-lookup"><span data-stu-id="5dc52-173">Task mode</span></span>  
 <span data-ttu-id="5dc52-174">El mode de tasca és un dels factors importants que determinen la planificació de les tasques de node fulla.</span><span class="sxs-lookup"><span data-stu-id="5dc52-174">Task mode is one of the important factors that determine scheduling leaf node tasks.</span></span> <span data-ttu-id="5dc52-175">Hi ha dos modes de tasca per a cada tasca: mode de planificació automàtica i mode de planificació manual.</span><span class="sxs-lookup"><span data-stu-id="5dc52-175">There are two task modes for every task: auto scheduling mode and manual scheduling mode.</span></span>  
  
-   <span data-ttu-id="5dc52-176">**Planificació automàtica**.</span><span class="sxs-lookup"><span data-stu-id="5dc52-176">**Auto scheduling**.</span></span>   <span data-ttu-id="5dc52-177">Quan definiu el mode de tasca a Planificat automàticament, el motor de planificació de la tasca utilitza les regles de planificació als següents atributs de tasca per determinar la planificació de la tasca:</span><span class="sxs-lookup"><span data-stu-id="5dc52-177">When you set the task mode to Automatically Scheduled, the task scheduling engine uses the scheduling rules on the following task attributes to determine the schedule for the task:</span></span>  
  
    -   <span data-ttu-id="5dc52-178">Predecessors</span><span class="sxs-lookup"><span data-stu-id="5dc52-178">Predecessors</span></span>  
  
    -   <span data-ttu-id="5dc52-179">Esforç</span><span class="sxs-lookup"><span data-stu-id="5dc52-179">Effort</span></span>  
  
    -   <span data-ttu-id="5dc52-180">Nombre de recursos</span><span class="sxs-lookup"><span data-stu-id="5dc52-180">Number of resources</span></span>  
  
    -   <span data-ttu-id="5dc52-181">Dates d'inici i d'acabament</span><span class="sxs-lookup"><span data-stu-id="5dc52-181">Start and end dates</span></span>  
  
-   <span data-ttu-id="5dc52-182">**Regles de planificació**.</span><span class="sxs-lookup"><span data-stu-id="5dc52-182">**Scheduling rules**.</span></span>   <span data-ttu-id="5dc52-183">La data d'inici d'una tasca de node fulla que no té un predecessor pren per defecte la data d'inici de la planificació del projecte.</span><span class="sxs-lookup"><span data-stu-id="5dc52-183">The start date of a leaf node task that does not have predecessors defaults to the project’s scheduling start date.</span></span> <span data-ttu-id="5dc52-184">La durada d'una tasca de node fulla sempre es calcula com el nombre de dies feiners entre les dates d'inici i final.</span><span class="sxs-lookup"><span data-stu-id="5dc52-184">The duration of a leaf node task is always calculated as the number of working days between its start and end dates.</span></span> <span data-ttu-id="5dc52-185">Quan una tasca es planifica automàticament, el motor de planificació segueix les regles següents:</span><span class="sxs-lookup"><span data-stu-id="5dc52-185">When a task is automatically scheduled, the scheduling engine follows the rules below:</span></span>  
  
    -   <span data-ttu-id="5dc52-186">Les dates d'inici i final d'una tasca sempre han de ser dies hàbils segons calendari de planificació del projecte</span><span class="sxs-lookup"><span data-stu-id="5dc52-186">Start and end dates of a task must always be working days according to the project’s scheduling calendar</span></span>  
  
    -   <span data-ttu-id="5dc52-187">La data d'inici d'una tasca que té antecessors pren per defecte l'última data de finalització dels seus predecessors</span><span class="sxs-lookup"><span data-stu-id="5dc52-187">The start date of a task that has predecessors defaults to the latest end date of its predecessors</span></span>  
  
    -   <span data-ttu-id="5dc52-188">Esforç = Nombre de persones \* Durada \* hores en un dia de treball estàndard del calendari del projecte</span><span class="sxs-lookup"><span data-stu-id="5dc52-188">Effort = Number of people \* Duration \* hours in a standard work day of the project calendar</span></span>  
  
-   <span data-ttu-id="5dc52-189">**Planificació manual**.</span><span class="sxs-lookup"><span data-stu-id="5dc52-189">**Manual scheduling**.</span></span>   <span data-ttu-id="5dc52-190">En alguns casos potser heu de desviar aquestes regles.</span><span class="sxs-lookup"><span data-stu-id="5dc52-190">In some cases, you might want to deviate from these rules.</span></span> <span data-ttu-id="5dc52-191">En aquests casos, podeu definir el mode de tasca per a la tasca que s'ha de planificar manualment.</span><span class="sxs-lookup"><span data-stu-id="5dc52-191">In these cases, you can set the task mode for the task to be manually scheduled.</span></span> <span data-ttu-id="5dc52-192">Això evita que el motor de planificació hagi de calcular els valors d'altres atributs de planificació.</span><span class="sxs-lookup"><span data-stu-id="5dc52-192">This stops the scheduling engine from calculating the values for other scheduling attributes.</span></span> <span data-ttu-id="5dc52-193">La definició de predecessors en tasques sempre influeix en la data d'inici de la tasca dependent.</span><span class="sxs-lookup"><span data-stu-id="5dc52-193">Setting predecessors on tasks always impacts the dependent task’s start date.</span></span>  
  
## <a name="create-a-work-breakdown-structure"></a><span data-ttu-id="5dc52-194">Crear una estructura del desglossament del treball</span><span class="sxs-lookup"><span data-stu-id="5dc52-194">Create a work breakdown structure</span></span>  
  
1.  <span data-ttu-id="5dc52-195">Aneu a **Project Service > Projectes**.</span><span class="sxs-lookup"><span data-stu-id="5dc52-195">Go to **Project Service > Projects**.</span></span>  
  
2.  <span data-ttu-id="5dc52-196">Feu clic al projecte en el qual voleu treballant.</span><span class="sxs-lookup"><span data-stu-id="5dc52-196">Click the project you want to work on.</span></span>  
  
3.  <span data-ttu-id="5dc52-197">A la barra que hi ha a la part superior de la pantalla, seleccioneu la fletxa avall al costat del nom de projecte i, a continuació, feu clic a Estructura del desglossament del treball.</span><span class="sxs-lookup"><span data-stu-id="5dc52-197">In the bar across the top of the screen, select the down arrow next to the project name, and then click Work breakdown structure.</span></span>  
  
4.  <span data-ttu-id="5dc52-198">Per afegir una tasca, feu clic a **Afegeix tasca**.</span><span class="sxs-lookup"><span data-stu-id="5dc52-198">To add a task, click **Add Task**.</span></span> <span data-ttu-id="5dc52-199">Empleneu els camps de la tasca i, a continuació, feu clic a **Desa**.</span><span class="sxs-lookup"><span data-stu-id="5dc52-199">Fill in the fields for the task, and then click **Save**.</span></span>  
  
5.  <span data-ttu-id="5dc52-200">Continueu afegint tasques fins que l'estructura del desglossament del treball estigui completa.</span><span class="sxs-lookup"><span data-stu-id="5dc52-200">Continue adding tasks until your work breakdown structure is complete.</span></span> <span data-ttu-id="5dc52-201">Quan creeu l'estructura del desglossament del treball, podeu fer el següent per organitzar les vostres tasques:</span><span class="sxs-lookup"><span data-stu-id="5dc52-201">While creating your work breakdown structure, you can do the following to organize your tasks:</span></span>  
  
    -   <span data-ttu-id="5dc52-202">Seleccioneu una tasca i feu clic a **Aplica sagnia** per moure-la sota una altra tasca o feu clic a Anul·la sagnia per pujar-la un nivell.</span><span class="sxs-lookup"><span data-stu-id="5dc52-202">Select a task and click **Indent** to move it under another task or click Outdent to move it out a level.</span></span>  
  
    -   <span data-ttu-id="5dc52-203">Seleccioneu una tasca i feu clic a **Desplaça amunt** o **Desplaça avall** per pujar-la o baixar-la a la llista.</span><span class="sxs-lookup"><span data-stu-id="5dc52-203">Select a task and click **Move Up** or **Move Down** to move it up or down in the list.</span></span>  
  
    -   <span data-ttu-id="5dc52-204">Feu clic a **Amaga Gantt** per amagar el gràfic de Gantt i feu clic a **Mostra Gantt** per tornar-lo a mostrar.</span><span class="sxs-lookup"><span data-stu-id="5dc52-204">Click **Hide Gantt** to hide the Gantt chart, and click **Show Gantt** to display it again.</span></span>  
  
    -   <span data-ttu-id="5dc52-205">Seleccioneu un període diferent de temps del gràfic de Gantt a **Escala de temps**.</span><span class="sxs-lookup"><span data-stu-id="5dc52-205">Select a different period of time for the Gantt chart in **Time Scale**.</span></span>  
  
6.  <span data-ttu-id="5dc52-206">Per afegir les funcions que heu especificat a l'estructura del desglossament del treball als membres del vostre equip de projecte, feu clic a **Genera equip de projecte**.</span><span class="sxs-lookup"><span data-stu-id="5dc52-206">To add the roles you specified in your work breakdown structure to your project’s team members, click **Generate Project Team**.</span></span>  
  
7.  <span data-ttu-id="5dc52-207">Feu clic a **Desa** a la cantonada inferior dreta de la pantalla quan hagueu acabat de fer els canvis.</span><span class="sxs-lookup"><span data-stu-id="5dc52-207">Click **Save** at the bottom right corner of the screen when you’re done making changes.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="5dc52-208">Vegeu també</span><span class="sxs-lookup"><span data-stu-id="5dc52-208">See Also</span></span>  
 [<span data-ttu-id="5dc52-209">Guia de l'administrador de projectes</span><span class="sxs-lookup"><span data-stu-id="5dc52-209">Project manager guide</span></span>](../psa/project-manager-guide.md)
