---
title: Novetats o canvis de la versió d'actualització 23 del Project Service Automation, V3
description: En aquest tema es mostren les característiques i correccions disponibles al Project Service Automation V3, versió d'actualització 23.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 08/25/2020
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
ms.openlocfilehash: 87f89828aeff22d9b473539e294d5cf04d46a203
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150026"
---
# <a name="project-service-automation-update-release-23-v3"></a><span data-ttu-id="de9eb-103">Project Service Automation, versió d'actualització 23, V3</span><span class="sxs-lookup"><span data-stu-id="de9eb-103">Project Service Automation Update Release 23, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="de9eb-104">Estem encantats d'anunciar-vos l'última actualització per a l'aplicació Project Service Automation per al Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="de9eb-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="de9eb-105">Aquesta versió inclou algunes millores importants per a la qualitat, el rendiment i la usabilitat.</span><span class="sxs-lookup"><span data-stu-id="de9eb-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="de9eb-106">Aquest llançament és compatible amb el Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="de9eb-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="de9eb-107">Per actualitzar a aquesta versió, visiteu el Centre d'administració del Dynamics 365 en línia i aneu a la pàgina de solucions per instal·lar l'actualització.</span><span class="sxs-lookup"><span data-stu-id="de9eb-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="de9eb-108">Per obtenir més informació, vegeu [Instal·lar, actualitzar o eliminar una solució preferida](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="de9eb-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="de9eb-109">En aquest tema es mostren les característiques i correccions que són noves o s'han canviat per al Project Service Automation V3, versió d'actualització 23.</span><span class="sxs-lookup"><span data-stu-id="de9eb-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 23.</span></span> <span data-ttu-id="de9eb-110">Aquesta versió té el número de compilació V3.10.34.30 i està disponible de forma general a través d'una actualització automàtica l'agost de 2020.</span><span class="sxs-lookup"><span data-stu-id="de9eb-110">This version has a build number of V 3.10.34.30 and is generally available through a self-update in August 2020.</span></span>

## <a name="update-release-23"></a><span data-ttu-id="de9eb-111">Versió d'actualització 23</span><span class="sxs-lookup"><span data-stu-id="de9eb-111">Update Release 23</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="de9eb-112">Correccions d'errors</span><span class="sxs-lookup"><span data-stu-id="de9eb-112">Bug fixes</span></span>

<span data-ttu-id="de9eb-113">**Temps i despesa**</span><span class="sxs-lookup"><span data-stu-id="de9eb-113">**Time and Expense**</span></span>

<span data-ttu-id="de9eb-114">S'han corregit els problemes següents:</span><span class="sxs-lookup"><span data-stu-id="de9eb-114">The following issues have been fixed:</span></span>
- <span data-ttu-id="de9eb-115">Es gestiona un cas excepcional a **Supressió de membre de l'equip del projecte** per proporcionar una excepció significativa.</span><span class="sxs-lookup"><span data-stu-id="de9eb-115">Handle edge case in **Project Team Member Delete** to provide a meaningful exception.</span></span>
- <span data-ttu-id="de9eb-116">Una importació d'assignació provoca una pantalla de supressió en blanc.</span><span class="sxs-lookup"><span data-stu-id="de9eb-116">Assignment import results in a blank remove screen.</span></span>

<span data-ttu-id="de9eb-117">**Administració de recursos**</span><span class="sxs-lookup"><span data-stu-id="de9eb-117">**Resource Management**</span></span>

<span data-ttu-id="de9eb-118">S'han corregit els problemes següents:</span><span class="sxs-lookup"><span data-stu-id="de9eb-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="de9eb-119">La **targeta de recursos de la quadrícula d'ús de recursos** mostra dades incorrectes quan l'escala de temps té més de cinc dies.</span><span class="sxs-lookup"><span data-stu-id="de9eb-119">The **Resource utilization grid resource card** shows incorrect data when the time scale is more than five days.</span></span>
- <span data-ttu-id="de9eb-120">Quan els clients creen un recurs reservable, el complement de manera intermitent no afegeix automàticament el recurs a un grup del Microsoft Office 365.</span><span class="sxs-lookup"><span data-stu-id="de9eb-120">When customers create a bookable resource, the plug-in intermittently fails to automatically add the resource to a Microsoft Office 365 group.</span></span>
- <span data-ttu-id="de9eb-121">La visualització **Conciliació** mostra els contorns manuals incorrectament a la visualització **Setmana** o **Mes**.</span><span class="sxs-lookup"><span data-stu-id="de9eb-121">**Reconciliation** view displays manual contours incorrectly in the **Week** or **Month** view.</span></span>

<span data-ttu-id="de9eb-122">**Administració de projectes**</span><span class="sxs-lookup"><span data-stu-id="de9eb-122">**Project Management**</span></span>

<span data-ttu-id="de9eb-123">S'han corregit els problemes següents:</span><span class="sxs-lookup"><span data-stu-id="de9eb-123">The following issues have been fixed:</span></span>

- <span data-ttu-id="de9eb-124">Un nombre excessiu d'entitats **RetrieveMultiple per a usersettings** provoca un rendiment degradat per a les aprovacions de projectes i altres operacions.</span><span class="sxs-lookup"><span data-stu-id="de9eb-124">An excessive number of **RetrieveMultiple for usersettings** entities are causing degraded performance for project approvals and other operations.</span></span>
- <span data-ttu-id="de9eb-125">La cerca de recursos de la quadrícula **Planificació de tasques** es limita a mostrar només cinc membres de l'equip a l'equip del projecte.</span><span class="sxs-lookup"><span data-stu-id="de9eb-125">The **Task Planning** grid resource lookup is limited to only show up to five team members from the project team.</span></span> 
- <span data-ttu-id="de9eb-126">La cerca de recursos de la quadrícula **Planificació de tasques** no filtra els recursos inactius.</span><span class="sxs-lookup"><span data-stu-id="de9eb-126">The **Task Planning** grid resource lookup does not filter inactive resources.</span></span>
- <span data-ttu-id="de9eb-127">El mode manual no funciona com s'esperava a l'estructura del desglossament del treball de la planificació del projecte.</span><span class="sxs-lookup"><span data-stu-id="de9eb-127">Manual mode is not working as expected in the project planning work breakdown structure.</span></span>
- <span data-ttu-id="de9eb-128">La quadrícula **Planificació de tasques** mostra **Categories de transaccions inactives**.</span><span class="sxs-lookup"><span data-stu-id="de9eb-128">The **Task Planning** grid shows **Inactive Transaction Categories**.</span></span>
- <span data-ttu-id="de9eb-129">La quadrícula **Assignació de recursos** arrodoneix incorrectament quan una tasca té diverses assignacions.</span><span class="sxs-lookup"><span data-stu-id="de9eb-129">The **Resource Assignment** grid rounds incorrectly when a task has multiple assignments.</span></span>
- <span data-ttu-id="de9eb-130">Els valors d'arrodoniment són diferents entre el cost previst i el cost real per a una sola tasca.</span><span class="sxs-lookup"><span data-stu-id="de9eb-130">Rounding values are different between planned cost and actual cost for a single task.</span></span>

<span data-ttu-id="de9eb-131">**Sales**</span><span class="sxs-lookup"><span data-stu-id="de9eb-131">**Sales**</span></span>

<span data-ttu-id="de9eb-132">S'han corregit els problemes següents:</span><span class="sxs-lookup"><span data-stu-id="de9eb-132">The following issues have been fixed:</span></span>

- <span data-ttu-id="de9eb-133">En fer doble clic a **Recupera totes les categories de transaccions**, es creen diverses línies.</span><span class="sxs-lookup"><span data-stu-id="de9eb-133">**Fetch All Transaction Categories** double-click creates multiple lines.</span></span>
