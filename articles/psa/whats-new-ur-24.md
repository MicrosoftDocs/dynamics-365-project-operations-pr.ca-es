---
title: Novetats o canvis de la versió d'actualització 24 del Project Service Automation, V3
description: En aquest tema es mostren les característiques i correccions disponibles al Project Service Automation V3, versió d'actualització 24.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 10/02/2020
ms.topic: article
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 3a37e71be2cce259d8aed0621d13393b6bbe4199
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4126561"
---
# <a name="project-service-automation-update-release-24-v3"></a><span data-ttu-id="3a519-103">Project Service Automation, versió d'actualització 24, V3</span><span class="sxs-lookup"><span data-stu-id="3a519-103">Project Service Automation Update Release 24, V3</span></span>

<span data-ttu-id="3a519-104">Estem encantats d'anunciar-vos l'última actualització per a l'aplicació Project Service Automation per al Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="3a519-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="3a519-105">Aquesta versió inclou algunes millores importants per a la qualitat, el rendiment i la usabilitat.</span><span class="sxs-lookup"><span data-stu-id="3a519-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="3a519-106">Aquest llançament és compatible amb el Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="3a519-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="3a519-107">Per actualitzar a aquesta versió, visiteu el Centre d'administració del Dynamics 365 en línia i aneu a la pàgina de solucions per instal·lar l'actualització.</span><span class="sxs-lookup"><span data-stu-id="3a519-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="3a519-108">Per obtenir més informació, vegeu [Instal·lar, actualitzar o eliminar una solució preferida](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="3a519-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="3a519-109">En aquest tema es mostren les característiques i correccions que són noves o s'han canviat per al Project Service Automation V3, versió d'actualització 24.</span><span class="sxs-lookup"><span data-stu-id="3a519-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 24.</span></span> <span data-ttu-id="3a519-110">Aquesta versió té el número de compilació V3.10.42.43 i està disponible de forma general a través d'una actualització automàtica l'octubre de 2020.</span><span class="sxs-lookup"><span data-stu-id="3a519-110">This version has a build number of V 3.10.42.43 and is generally available through a self-update in October 2020.</span></span>

## <a name="update-release-24"></a><span data-ttu-id="3a519-111">Versió d'actualització 24</span><span class="sxs-lookup"><span data-stu-id="3a519-111">Update Release 24</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="3a519-112">Correccions d'errors</span><span class="sxs-lookup"><span data-stu-id="3a519-112">Bug fixes</span></span>

<span data-ttu-id="3a519-113">**Sales**</span><span class="sxs-lookup"><span data-stu-id="3a519-113">**Sales**</span></span>

<span data-ttu-id="3a519-114">S'han corregit els problemes següents:</span><span class="sxs-lookup"><span data-stu-id="3a519-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="3a519-115">Problema en definir la llista de preus per defecte dels productes.</span><span class="sxs-lookup"><span data-stu-id="3a519-115">Problem while setting default price list of products.</span></span>
- <span data-ttu-id="3a519-116">El rendiment en guanyar una oferta és lent a causa de la llista de preus incrustada i la còpia dels registres de preu per funció.</span><span class="sxs-lookup"><span data-stu-id="3a519-116">Performance of Quote win is slow due to the embedded price list and role price records copy.</span></span>
- <span data-ttu-id="3a519-117">**Contracte del projecte/Centre de vendes** > **Element de la línia de productes/Quantitat de la línia de comanda** s'arrodoneix automàticament a l'enter més proper.</span><span class="sxs-lookup"><span data-stu-id="3a519-117">**Project Contract/Sales Hub** > **Product Line Item/Order Line Quantity** is automatically rounded to the nearest integer.</span></span>
- <span data-ttu-id="3a519-118">S'eleven els privilegis del sistema en llegir llistes de preus.</span><span class="sxs-lookup"><span data-stu-id="3a519-118">Elevate to system privileges when reading price lists.</span></span>
- <span data-ttu-id="3a519-119">Es copien els camps d'adreça del client **address1_freighttermscode** i **address1_shippingmethodcode** a l'oferta o la comanda.</span><span class="sxs-lookup"><span data-stu-id="3a519-119">Copy customer address fields **address1_freighttermscode** and **address1_shippingmethodcode** to Quote/Order.</span></span> 


<span data-ttu-id="3a519-120">**Temps i despesa**</span><span class="sxs-lookup"><span data-stu-id="3a519-120">**Time and Expense**</span></span>

<span data-ttu-id="3a519-121">S'han corregit els problemes següents:</span><span class="sxs-lookup"><span data-stu-id="3a519-121">The following issues have been fixed:</span></span>

- <span data-ttu-id="3a519-122">La **quadrícula d'entrada de temps** no admet el comportament de temps **Només data**.</span><span class="sxs-lookup"><span data-stu-id="3a519-122">The **Time Entry Grid** doesn't support **Date Only** time behavior.</span></span>
- <span data-ttu-id="3a519-123">**L'entrada de temps** no s'actualitza automàticament.</span><span class="sxs-lookup"><span data-stu-id="3a519-123">**Time Entry** is not refreshing automatically.</span></span> <span data-ttu-id="3a519-124">Es necessita una actualització manual.</span><span class="sxs-lookup"><span data-stu-id="3a519-124">A manual refresh is required.</span></span>
- <span data-ttu-id="3a519-125">No es poden importar les entrades de temps d'una assignació quan hi ha una pausa (0 hores) a les assignacions d'un recurs.</span><span class="sxs-lookup"><span data-stu-id="3a519-125">Unable to import the time entries from an assignment when there is a break (0 hours) in a resource's assignments.</span></span>
- <span data-ttu-id="3a519-126">Quan creeu una entrada de temps, definiu la data d'inici al mateix valor que **msdyn_date**.</span><span class="sxs-lookup"><span data-stu-id="3a519-126">When creating a time entry, set the start to the same as **msdyn_date**.</span></span>
- <span data-ttu-id="3a519-127">Torna a habilitar l'edició massiva per a l'entrada de temps.</span><span class="sxs-lookup"><span data-stu-id="3a519-127">Re-enable bulk edit for time entry.</span></span>

<span data-ttu-id="3a519-128">**Administració de recursos**</span><span class="sxs-lookup"><span data-stu-id="3a519-128">**Resource Management**</span></span>

<span data-ttu-id="3a519-129">S'han corregit els problemes següents:</span><span class="sxs-lookup"><span data-stu-id="3a519-129">The following issues have been fixed:</span></span>

- <span data-ttu-id="3a519-130">En provar d'actualitzar l'estat d'una reserva entre dies sense un requisit, es generarà una excepció de referència nul·la.</span><span class="sxs-lookup"><span data-stu-id="3a519-130">Trying to update the status of an inter-day booking without a requirement will throw a null-ref exception.</span></span>
- <span data-ttu-id="3a519-131">Error en carregar la **visualització de conciliació**.</span><span class="sxs-lookup"><span data-stu-id="3a519-131">Error loading the **Reconciliation View**.</span></span>


<span data-ttu-id="3a519-132">**Administració de projectes**</span><span class="sxs-lookup"><span data-stu-id="3a519-132">**Project Management**</span></span>

<span data-ttu-id="3a519-133">S'han corregit els problemes següents:</span><span class="sxs-lookup"><span data-stu-id="3a519-133">The following issues have been fixed:</span></span>

- <span data-ttu-id="3a519-134">A la **planificació del projecte**, quan es canvia de **Manual** a **Automàtic**, el desament automàtic no finalitza.</span><span class="sxs-lookup"><span data-stu-id="3a519-134">In the **Project Schedule**, when changing from **Manual** to **Auto**, auto save is not completing.</span></span>
- <span data-ttu-id="3a519-135">Els costos de despesa no s'han de calcular cap a la variació a la **quadrícula de seguiment del projecte**.</span><span class="sxs-lookup"><span data-stu-id="3a519-135">Expense costs should not calculate toward variance on the **Project Tracking Grid**.</span></span>
- <span data-ttu-id="3a519-136">Comportament incoherent per a les columnes **Etiqueta d'estimació** durant la càrrega en comparació amb el canvi del tipus de **fase de temps**.</span><span class="sxs-lookup"><span data-stu-id="3a519-136">Inconsistent behavior for **Estimates tag** columns during load versus changing the **Time-Phase** type.</span></span>
- <span data-ttu-id="3a519-137">Pot ser que el cost real d'un projecte no reflecteixi els totals dels **valors reals**.</span><span class="sxs-lookup"><span data-stu-id="3a519-137">The actual cost on a project may not reflect the totals from **Actuals**.</span></span>
- <span data-ttu-id="3a519-138">La **data de finalització aproximada** a la pestanya **Resum** no coincideix amb la **planificació de WBS**.</span><span class="sxs-lookup"><span data-stu-id="3a519-138">**Estimated Finish Date** on the **Summary** tab does not match the **WBS Schedule**.</span></span>
- <span data-ttu-id="3a519-139">**Actualitza les hores reals** en la sagnia no funciona correctament.</span><span class="sxs-lookup"><span data-stu-id="3a519-139">**Update Actual Hours** on outdent does not work correctly.</span></span>
- <span data-ttu-id="3a519-140">Un administrador de projectes fora de la **unitat de negoci** arrel no pot crear un projecte.</span><span class="sxs-lookup"><span data-stu-id="3a519-140">A Project manager outside of root **BU** can't create a project.</span></span>
- <span data-ttu-id="3a519-141">Els canvis a les tasques o categories a **Estimacions de despesa** no són persistents.</span><span class="sxs-lookup"><span data-stu-id="3a519-141">Changes to task or category on **Expense Estimates** are not persisted.</span></span>
- <span data-ttu-id="3a519-142">**Còpia del contracte** copia les planificacions de factura i l'estat d'execució.</span><span class="sxs-lookup"><span data-stu-id="3a519-142">**Copy of contract** copies the invoice schedules and the run status.</span></span>
- <span data-ttu-id="3a519-143">El botó **Actualitza els valors reals** calcula incorrectament les tasques de resum.</span><span class="sxs-lookup"><span data-stu-id="3a519-143">**Refresh Actuals** button incorrectly calculates summary tasks.</span></span>
- <span data-ttu-id="3a519-144">Complement del Microsoft Project: s'ha esmenat l'error de referència nul·la si un membre de l'equip té una unitat de recursos buida.</span><span class="sxs-lookup"><span data-stu-id="3a519-144">Microsoft Project Add-in: Fix null reference error if any team member has an empty resourcing unit.</span></span>

