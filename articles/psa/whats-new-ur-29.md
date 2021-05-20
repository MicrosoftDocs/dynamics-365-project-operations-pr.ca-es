---
title: Novetats o canvis de la versió d'actualització 29 del Project Service Automation, V3
description: En aquest tema es mostren les característiques i correccions disponibles al Project Service Automation V3, versió d'actualització 29.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/22/2021
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
ms.openlocfilehash: 2ac47974b9cc8386c7446136faf48724de73efce
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948596"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-29-v3"></a><span data-ttu-id="2b4f7-103">Novetats o canvis de la versió d'actualització 29 del Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="2b4f7-103">What's new or changed in Project Service Automation Update Release 29, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="2b4f7-104">Estem encantats d'anunciar-vos l'última actualització per a l'aplicació Project Service Automation per al Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="2b4f7-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="2b4f7-105">Aquesta versió inclou algunes millores importants per a la qualitat, el rendiment i la usabilitat.</span><span class="sxs-lookup"><span data-stu-id="2b4f7-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="2b4f7-106">Aquest llançament és compatible amb el Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="2b4f7-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="2b4f7-107">Per actualitzar a aquesta versió, visiteu el Centre d'administració del Dynamics 365 en línia i aneu a la pàgina de solucions per instal·lar l'actualització.</span><span class="sxs-lookup"><span data-stu-id="2b4f7-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="2b4f7-108">Per obtenir més informació, vegeu [Instal·lar, actualitzar o eliminar una solució preferida](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="2b4f7-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="2b4f7-109">En aquest tema es mostren les característiques i correccions que són noves o s'han canviat per al Project Service Automation V3, versió d'actualització 29.</span><span class="sxs-lookup"><span data-stu-id="2b4f7-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 29.</span></span> <span data-ttu-id="2b4f7-110">Aquesta versió té un número de compilació de V3.10.47.7 i està disponible de manera general a través d'una actualització d'autoservei al febrer de 2021.</span><span class="sxs-lookup"><span data-stu-id="2b4f7-110">This version has a build number of V3.10.47.7 and is generally available through a self-update in February 2021.</span></span>

## <a name="update-release-29"></a><span data-ttu-id="2b4f7-111">Versió d'actualització 29</span><span class="sxs-lookup"><span data-stu-id="2b4f7-111">Update Release 29</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="2b4f7-112">Correccions d'errors</span><span class="sxs-lookup"><span data-stu-id="2b4f7-112">Bug fixes</span></span>

<span data-ttu-id="2b4f7-113">**Temps i despesa**</span><span class="sxs-lookup"><span data-stu-id="2b4f7-113">**Time and Expense**</span></span>

<span data-ttu-id="2b4f7-114">S'han corregit els problemes següents:</span><span class="sxs-lookup"><span data-stu-id="2b4f7-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="2b4f7-115">Els usuaris no poden veure les hores de feina registrades en dies que no són feiners a la quadrícula d'entrada de temps.</span><span class="sxs-lookup"><span data-stu-id="2b4f7-115">Users can't see working hours logged on non-working days in the time entry grid.</span></span>
- <span data-ttu-id="2b4f7-116">Les entrades de despesa aprovades es poden editar a la quadrícula.</span><span class="sxs-lookup"><span data-stu-id="2b4f7-116">Approved expense entries can be edited on the grid.</span></span>

<span data-ttu-id="2b4f7-117">**Administració de projectes**</span><span class="sxs-lookup"><span data-stu-id="2b4f7-117">**Project Management**</span></span>

<span data-ttu-id="2b4f7-118">S'han corregit els problemes següents:</span><span class="sxs-lookup"><span data-stu-id="2b4f7-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="2b4f7-119">Falta lògica de validació per garantir que les hores d'esforç d'assignació de recursos no poden ser negatives.</span><span class="sxs-lookup"><span data-stu-id="2b4f7-119">Missing validation logic to ensure resource assignment effort hours can't be negative.</span></span>
- <span data-ttu-id="2b4f7-120">L'acció personalitzada **AssignResourcesForTask** actualitza tots els camps en comptes de només camps canviats.</span><span class="sxs-lookup"><span data-stu-id="2b4f7-120">The custom action, **AssignResourcesForTask** updates all fields instead of only changed fields.</span></span>
- <span data-ttu-id="2b4f7-121">Quan es copia un projecte en un entorn amb complements o fluxos de treball registrats a la incidència **CreateProject**, l'atribut **msdyn_bulkgenerationstatus** no s'actualitza si es produeix un error a **CopyWBSToProject**.</span><span class="sxs-lookup"><span data-stu-id="2b4f7-121">When copying a project in an environment with plug-ins or workflows that are registered on the **CreateProject** event, the **msdyn_bulkgenerationstatus** attribute isn't updated if the **CopyWBSToProject** fails.</span></span>
- <span data-ttu-id="2b4f7-122">Quan expandiu el calendari del projecte, els dies feiners no s'ordenen en ordre ascendent, cosa que fa que fallin algunes actualitzacions de tasques del projecte.</span><span class="sxs-lookup"><span data-stu-id="2b4f7-122">When you expand the project calendar, the working days aren't sorted in ascending order causing some project task updates to fail.</span></span>
- <span data-ttu-id="2b4f7-123">Quan canvieu l'Administrador de projectes en un projecte existent, s'activa la lògica per defecte de la unitat organitzativa.</span><span class="sxs-lookup"><span data-stu-id="2b4f7-123">Changing the Project Manager on an existing project triggers the organizational unit defaulting logic.</span></span>

<span data-ttu-id="2b4f7-124">**Vendes**</span><span class="sxs-lookup"><span data-stu-id="2b4f7-124">**Sales**</span></span>

<span data-ttu-id="2b4f7-125">S'han corregit els problemes següents:</span><span class="sxs-lookup"><span data-stu-id="2b4f7-125">The following issues have been fixed:</span></span>

- <span data-ttu-id="2b4f7-126">La pestanya **Rendiment del contracte** de la pàgina **Contracte** falla silenciosament durant la inicialització quan no hi ha cap línia de contracte.</span><span class="sxs-lookup"><span data-stu-id="2b4f7-126">The **Contract Performance** tab on the **Contract** page fails silently during initialization when no contract lines are present.</span></span>