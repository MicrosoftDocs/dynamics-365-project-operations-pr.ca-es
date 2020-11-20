---
title: Veure l'ús imputable dels recursos
description: En aquest tema es proporciona informació sobre la visualització d'ús dels recursos.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
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
ms.openlocfilehash: a1d1db532c65b2a13f3cf4e1281a5987490b96df
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122151"
---
# <a name="view-chargeable-utilization-for-resources"></a><span data-ttu-id="196f1-103">Veure l'ús imputable dels recursos</span><span class="sxs-lookup"><span data-stu-id="196f1-103">View chargeable utilization for resources</span></span>
 
<span data-ttu-id="196f1-104">La **Visualització d'ús** de la pàgina **Utilització de recursos del Project Service** mostra la utilització imputable per a cada recurs disponible.</span><span class="sxs-lookup"><span data-stu-id="196f1-104">The **Utilization View** on the **Project Service Resource Utilization** page shows the chargeable utilization for each bookable resource.</span></span> <span data-ttu-id="196f1-105">Com que la visualització es basa en el tauler de planificació, trobareu moltes funcions iguals.</span><span class="sxs-lookup"><span data-stu-id="196f1-105">Because the view is based on the schedule board, you’ll find many of the same functions.</span></span>

> ![Captura de pantalla de la visualització d'ús](media/FAQ-utilization-1.png)
 

<span data-ttu-id="196f1-107">El càlcul d'ús facturable funciona de la següent manera:</span><span class="sxs-lookup"><span data-stu-id="196f1-107">The chargeable utilization calculation works as follows:</span></span>

   <span data-ttu-id="196f1-108">Ús facturable = (hores reals facturables) / (capacitat de recursos)</span><span class="sxs-lookup"><span data-stu-id="196f1-108">Chargeable utilization = (Chargeable actual hours) / (resource capacity)</span></span>

<span data-ttu-id="196f1-109">Les cel·les representen l'ús facturable calculat per al període seleccionat (dies, setmanes o mesos).</span><span class="sxs-lookup"><span data-stu-id="196f1-109">The cells represent the calculated chargeable utilization for the selected period (days, weeks, or months).</span></span>

<span data-ttu-id="196f1-110">Els colors de cada cel·la mostren l'ús facturable d'un recurs en comparació amb la seva utilització facturable objectiu.</span><span class="sxs-lookup"><span data-stu-id="196f1-110">The colors in each cell show the chargeable utilization for a resource as compared to their target chargeable utilization.</span></span> 

<span data-ttu-id="196f1-111">L'objectiu d'ús es pot establir en la funció predeterminada del recurs o en el recurs individual en si.</span><span class="sxs-lookup"><span data-stu-id="196f1-111">The target utilization can be set on the resource’s default role or on the individual resource itself.</span></span> <span data-ttu-id="196f1-112">El càlcul primer busca l'objectiu a l'individu, i després a la funció per defecte del recurs.</span><span class="sxs-lookup"><span data-stu-id="196f1-112">The calculation looks at the individual for the target first, and then to the resource’s default role.</span></span>

## <a name="set-target-on-a-resource"></a><span data-ttu-id="196f1-113">Definir l'objectiu en un recurs</span><span class="sxs-lookup"><span data-stu-id="196f1-113">Set target on a resource</span></span>

1. <span data-ttu-id="196f1-114">Aneu a **Recursos** \> **Recursos**.</span><span class="sxs-lookup"><span data-stu-id="196f1-114">Go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="196f1-115">Seleccioneu un recurs per obrir el registre.</span><span class="sxs-lookup"><span data-stu-id="196f1-115">Select a resource to open the record.</span></span> 
3. <span data-ttu-id="196f1-116">A la pestanya **Project Service**, podeu definir l'objectiu d'ús del recurs.</span><span class="sxs-lookup"><span data-stu-id="196f1-116">On the **Project Service** tab, you can set the resource’s target utilization.</span></span>

> ![Captura de pantalla de la utilització del Project Service per definir l'ús objectiu](media/FAQ-utilization-2.png)
 
## <a name="set-target-utilization-on-a-role"></a><span data-ttu-id="196f1-118">Definir l'objectiu d'ús en una funció</span><span class="sxs-lookup"><span data-stu-id="196f1-118">Set target utilization on a role</span></span>

1. <span data-ttu-id="196f1-119">Aneu a **Recursos** \> **Funcions de recurs**.</span><span class="sxs-lookup"><span data-stu-id="196f1-119">Go to **Resources** \> **Resource Roles**.</span></span> 
2. <span data-ttu-id="196f1-120">Seleccioneu una funció i obriu el registre.</span><span class="sxs-lookup"><span data-stu-id="196f1-120">Select a role and open the record.</span></span> 
3. <span data-ttu-id="196f1-121">Establiu l'ús objectiu de la funció.</span><span class="sxs-lookup"><span data-stu-id="196f1-121">Set the target utilization for the role.</span></span>

> ![Captura de pantalla de la utilització de funcions de recurs per definir l'ús objectiu](media/FAQ-utilization-3.png)
 
## <a name="calculate-chargeable-utilization-for-a-resource"></a><span data-ttu-id="196f1-123">Calcular l'ús imputable d'un recurs</span><span class="sxs-lookup"><span data-stu-id="196f1-123">Calculate chargeable utilization for a resource</span></span>

<span data-ttu-id="196f1-124">Per calcular l'ús imputable d'un recurs, haureu de completar alguns requisits previs.</span><span class="sxs-lookup"><span data-stu-id="196f1-124">To calculate chargeable utilization for a resource, you will need to complete some pre-requisites.</span></span> 

### <a name="set-default-role-for-individual-resource"></a><span data-ttu-id="196f1-125">Definir la funció per defecte del recurs individual</span><span class="sxs-lookup"><span data-stu-id="196f1-125">Set default role for individual resource</span></span>

<span data-ttu-id="196f1-126">En primer lloc, l'objectiu d'ús s'ha d'establir en el recurs individual o en les funcions dels recursos.</span><span class="sxs-lookup"><span data-stu-id="196f1-126">First, the target utilization must be set on either the individual resource or on resource roles.</span></span> <span data-ttu-id="196f1-127">Si utilitzeu funcions de recursos per a objectius, cada recurs individual ha de tenir una funció predeterminada.</span><span class="sxs-lookup"><span data-stu-id="196f1-127">If you are using resource roles for targets, each individual resource must have a default role.</span></span> 

1. <span data-ttu-id="196f1-128">Per configurar-ho, aneu a **Recursos** \> **Recursos**.</span><span class="sxs-lookup"><span data-stu-id="196f1-128">To set this, go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="196f1-129">Seleccioneu un recurs, obriu el registre i, a continuació, seleccioneu la pestanya **Project Service**.</span><span class="sxs-lookup"><span data-stu-id="196f1-129">Select a resource, open the record, and then select the **Project Service** tab.</span></span> 
3. <span data-ttu-id="196f1-130">A la quadrícula **Funció del recurs**, assegureu-vos que hi hagi una funció per al recurs i que **Per defecte** s'hagi definit com a **Sí**.</span><span class="sxs-lookup"><span data-stu-id="196f1-130">In the **Resource Role** grid, make sure there’s one role for the resource and **Is Default** is set to **Yes**.</span></span>
 
### <a name="change-billing-type-for-resource-role"></a><span data-ttu-id="196f1-131">Canviar el tipus de facturació d'una funció de recurs</span><span class="sxs-lookup"><span data-stu-id="196f1-131">Change billing type for resource role</span></span>

<span data-ttu-id="196f1-132">Les funcions de recursos s'han de configurar perquè tinguin un tipus de facturació **Imputable**.</span><span class="sxs-lookup"><span data-stu-id="196f1-132">The resource roles must be set to have a billing type of **Chargeable**.</span></span> 

1. <span data-ttu-id="196f1-133">Aneu a **Recursos** \> **Funcions de recurs**.</span><span class="sxs-lookup"><span data-stu-id="196f1-133">Go to **Resources** \> **Resource Roles**.</span></span> 
2. <span data-ttu-id="196f1-134">Obriu el registre que voleu actualitzar i després establiu el tipus de facturació predeterminat a **Imputable**.</span><span class="sxs-lookup"><span data-stu-id="196f1-134">Open the record you want to update, and then set the billing type default to **Chargeable**.</span></span>

### <a name="set-working-hours-for-resource-role"></a><span data-ttu-id="196f1-135">Definir les hores de feina per a la funció de recursos</span><span class="sxs-lookup"><span data-stu-id="196f1-135">Set working hours for resource role</span></span>
 
<span data-ttu-id="196f1-136">El recurs ha de tenir hores de treball per poder realitzar el càlcul de la capacitat.</span><span class="sxs-lookup"><span data-stu-id="196f1-136">The resource must have working hours for the capacity calculation.</span></span> 

1. <span data-ttu-id="196f1-137">Aneu a **Recursos** \> **Recursos**.</span><span class="sxs-lookup"><span data-stu-id="196f1-137">Go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="196f1-138">Seleccioneu un recurs per obrir el registre i després seleccioneu **Mostra les hores de treball**.</span><span class="sxs-lookup"><span data-stu-id="196f1-138">Select a resource to open the record, and then select **Show Work Hours**.</span></span> 
3. <span data-ttu-id="196f1-139">Podeu fer una actualització massiva de la llista de recursos si apliqueu una **Plantilla d'hores de treball** des de la vista **Llista de recursos**.</span><span class="sxs-lookup"><span data-stu-id="196f1-139">You can bulk-update the list of resources by applying a **Work Hour Template** from the **Resource List** view.</span></span>

## <a name="troubleshooting-chargeable-actual-hours"></a><span data-ttu-id="196f1-140">Detecció d'errors a les hores imputables</span><span class="sxs-lookup"><span data-stu-id="196f1-140">Troubleshooting chargeable actual hours</span></span>

<span data-ttu-id="196f1-141">Les hores reals imputables s'obtenen de l'entitat **Dades reals**.</span><span class="sxs-lookup"><span data-stu-id="196f1-141">The chargeable actual hours are sourced from the **Actuals** entity.</span></span> <span data-ttu-id="196f1-142">Les dades reals amb el tipus de facturació **Imputable** estan incloses en el càlcul i, per aquest motiu, han de tenir projectes on els valors reals siguin imputables.</span><span class="sxs-lookup"><span data-stu-id="196f1-142">Actuals with a billing type of **Chargeable** are included in the calculation and, for this reason, you must have projects where the actuals that are chargeable.</span></span>

<span data-ttu-id="196f1-143">Si no esteu veient l'ús facturables, us mostrem algunes coses que podeu comprovar:</span><span class="sxs-lookup"><span data-stu-id="196f1-143">If you are not seeing chargeable utilization, here are some things you can check:</span></span>

- <span data-ttu-id="196f1-144">El recurs té hores de treball definides per la capacitat.</span><span class="sxs-lookup"><span data-stu-id="196f1-144">The resource has working hours defined for capacity.</span></span>
- <span data-ttu-id="196f1-145">El recurs té un objectiu d'ús definit de forma individual o té una funció predeterminada assignada.</span><span class="sxs-lookup"><span data-stu-id="196f1-145">The resource has either an individually defined utilization target or has a default role assigned to it.</span></span> <span data-ttu-id="196f1-146">La funció té un objectiu d'ús definit.</span><span class="sxs-lookup"><span data-stu-id="196f1-146">The role has a utilization target defined for it.</span></span>
- <span data-ttu-id="196f1-147">Les dades reals tenen un tipus de facturació **Imputable** per al període en què s'espera un càlcul d'ús.</span><span class="sxs-lookup"><span data-stu-id="196f1-147">Actuals have a billing type of **Chargeable** for the period you are expecting a utilization calculation for.</span></span> <span data-ttu-id="196f1-148">Comproveu el següent si veieu valors reals amb tipus de facturació diferents d'Imputable:</span><span class="sxs-lookup"><span data-stu-id="196f1-148">Check the following if you are seeing actuals with billing types other than chargeable:</span></span>

  - <span data-ttu-id="196f1-149">La funció utilitzada en el valor real té un tipus de facturació predeterminat que no és facturable.</span><span class="sxs-lookup"><span data-stu-id="196f1-149">The role used on the actual has a default billing type of something other than chargeable.</span></span>
  - <span data-ttu-id="196f1-150">La funció en la línia de contracte de projecte que recolza el projecte s'ha establert com no facturable.</span><span class="sxs-lookup"><span data-stu-id="196f1-150">The role on the project contract line backing the project has been set to non-chargeable.</span></span>
  - <span data-ttu-id="196f1-151">El projecte no té una línia de contracte associada.</span><span class="sxs-lookup"><span data-stu-id="196f1-151">The project does not have an associated contract line.</span></span>

