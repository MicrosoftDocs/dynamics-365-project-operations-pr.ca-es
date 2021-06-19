---
title: Novetats o canvis de la versió d'actualització 15 del Project Service Automation, V3
description: En aquest tema es proporciona informació sobre les novetats a la versió d'actualització 15 del Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/27/2020
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
ms.openlocfilehash: 86aadca637939120d0ccd839e7c425e9e8d38aec
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006814"
---
# <a name="project-service-automation-update-release-15-v3"></a><span data-ttu-id="c01cc-103">Project Service Automation, versió d'actualització 15, V3</span><span class="sxs-lookup"><span data-stu-id="c01cc-103">Project Service Automation Update Release 15, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="c01cc-104">Ens complau anunciar la darrera actualització de l'aplicació Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="c01cc-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="c01cc-105">Aquesta versió inclou algunes millores importants per a la qualitat, el rendiment i la usabilitat.</span><span class="sxs-lookup"><span data-stu-id="c01cc-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="c01cc-106">Aquest llançament és compatible amb el Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="c01cc-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="c01cc-107">Per actualitzar a aquesta versió, visiteu el Centre d'administració del Dynamics 365 en línia i aneu a la pàgina de solucions per instal·lar l'actualització.</span><span class="sxs-lookup"><span data-stu-id="c01cc-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="c01cc-108">Per obtenir més informació, vegeu [Instal·lar, actualitzar o eliminar una solució preferida](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="c01cc-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="c01cc-109">En aquest tema es mostren les característiques i correccions que són noves o s'han canviat per al PSA V3, versió d'actualització 15.</span><span class="sxs-lookup"><span data-stu-id="c01cc-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 15.</span></span> <span data-ttu-id="c01cc-110">Aquesta versió té el número de compilació V3.10.5.28 i està disponible de forma general a través d'una actualització automàtica el gener de 2020.</span><span class="sxs-lookup"><span data-stu-id="c01cc-110">This version has a build number of V3.10.5.28 and is generally available through a self-update in January 2020.</span></span>

## <a name="update-release-15"></a><span data-ttu-id="c01cc-111">Versió d'actualització 15</span><span class="sxs-lookup"><span data-stu-id="c01cc-111">Update Release 15</span></span> 

### <a name="enhancements"></a><span data-ttu-id="c01cc-112">Millores</span><span class="sxs-lookup"><span data-stu-id="c01cc-112">Enhancements</span></span>

- <span data-ttu-id="c01cc-113">Administració de projectes</span><span class="sxs-lookup"><span data-stu-id="c01cc-113">Project Management</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="c01cc-114">Correccions d'errors</span><span class="sxs-lookup"><span data-stu-id="c01cc-114">Bug fixes</span></span>

- <span data-ttu-id="c01cc-115">Temps i despesa</span><span class="sxs-lookup"><span data-stu-id="c01cc-115">Time and Expense</span></span>

  - <span data-ttu-id="c01cc-116">Correcció: s'ha afegit la gestió d'errors durant la càrrega a la visualització de conciliació.</span><span class="sxs-lookup"><span data-stu-id="c01cc-116">Fixed: Add on-load error handling in the reconciliation view.</span></span>
  - <span data-ttu-id="c01cc-117">Correcció: Centre de recursos del projecte: s'ha canviat el nom d'**Import** per reduir la ambigüitat.</span><span class="sxs-lookup"><span data-stu-id="c01cc-117">Fixed: Project Resource Hub: Rename **Amount** to reduce ambiguity.</span></span>
  - <span data-ttu-id="c01cc-118">Correcció: s'ha ajustat la visualització **Copia les columnes d'entrada de temps** per incloure el tipus.</span><span class="sxs-lookup"><span data-stu-id="c01cc-118">Fixed: Adjust the view **Copy Time Entry Columns** to include the type.</span></span>
  - <span data-ttu-id="c01cc-119">Correcció: l'edició de la duració d'una entrada de temps a la visualització de quadrícula utilitzant nombres decimals resulta en un error desconegut per a alguns nombres.</span><span class="sxs-lookup"><span data-stu-id="c01cc-119">Fixed: Editing time entry duration in the grid view using decimal numbers results in unknown error for some numbers.</span></span>

- <span data-ttu-id="c01cc-120">Administració de projectes</span><span class="sxs-lookup"><span data-stu-id="c01cc-120">Project Management</span></span>

  - <span data-ttu-id="c01cc-121">Correcció: el menú desplegable per a **Utilitza la visualització de seguiment** ara s'amplia en funció de l'amplada de les opcions.</span><span class="sxs-lookup"><span data-stu-id="c01cc-121">Fixed: The drop-down menu for **Use in Tracking View** now expands based on the width of the options.</span></span>
  - <span data-ttu-id="c01cc-122">Correcció: en administrar projectes al fus horari +13, els càlculs de tasques poden mostrar resultats correctes.</span><span class="sxs-lookup"><span data-stu-id="c01cc-122">Fixed: When managing projects in the +13 time zone, tasks calculations can display inaccurate results.</span></span>
  - <span data-ttu-id="c01cc-123">Correcció: el **Temps de finalització del membre de l'equip** s'ha corregit en utilitzar un calendari de 24 hores.</span><span class="sxs-lookup"><span data-stu-id="c01cc-123">Fixed: **Team Member End Time** has been corrected when using a 24-hour calendar.</span></span>
  - <span data-ttu-id="c01cc-124">Correcció: s'ha tornat a activar el **BPF** en el formulari principal **msdyn_project**.</span><span class="sxs-lookup"><span data-stu-id="c01cc-124">Fixed: Re-activated the **BPF** in **msdyn_project** main form.</span></span>
  - <span data-ttu-id="c01cc-125">Correcció: el càlcul de les assignacions ja no ignora un dia.</span><span class="sxs-lookup"><span data-stu-id="c01cc-125">Fixed: Assignments calculation no longer ignores one day.</span></span>
  - <span data-ttu-id="c01cc-126">Correcció: s'ha afegit un nou bàner de notificació al formulari del projecte quan el fus horari és diferent entre l'usuari i el projecte.</span><span class="sxs-lookup"><span data-stu-id="c01cc-126">Fixed: A new notification banner has been added to the project form when the time zone differs between user and project.</span></span>

- <span data-ttu-id="c01cc-127">Sales</span><span class="sxs-lookup"><span data-stu-id="c01cc-127">Sales</span></span>

  - <span data-ttu-id="c01cc-128">Correcció: la cerca d'una categoria d'estimació de despeses es pot utilitzar per filtrar duplicats.</span><span class="sxs-lookup"><span data-stu-id="c01cc-128">Fixed: Expense estimate category lookup can be used to filter duplicates.</span></span>
  - <span data-ttu-id="c01cc-129">Correcció: el codi a **PluginDomain.ExecuteInTryCatchBlock(..)** ja no amaga l'origen de l'excepció.</span><span class="sxs-lookup"><span data-stu-id="c01cc-129">Fixed: Code in **PluginDomain.ExecuteInTryCatchBlock(..)** no longer hides the origin of the exception.</span></span>
  - <span data-ttu-id="c01cc-130">Correcció: ja no s'obté cap missatge d'error a **Cerca de projectes** al formulari **Línia d'oferta** quan hi ha més de 1000 projectes.</span><span class="sxs-lookup"><span data-stu-id="c01cc-130">Fixed: No longer get an error message in **Project lookup** in the **Quote Line** form when there are more than 1000 projects.</span></span>
  - <span data-ttu-id="c01cc-131">Correcció: la quadrícula **Estimacions** per a estimacions de treball i estimacions de despesa ara mostra el símbol monetari correcte.</span><span class="sxs-lookup"><span data-stu-id="c01cc-131">Fixed: **Estimates** grid for labor estimates and expense estimates now displays the correct currency symbol.</span></span>
  - <span data-ttu-id="c01cc-132">Correcció: després de l'actualització per part d'una organització del PSA de la versió d'actualització 14 a la versió d'actualització 15, la pestanya **Planificació** ja no apareix a en blanc al formulari **Projecte**.</span><span class="sxs-lookup"><span data-stu-id="c01cc-132">Fixed: After an organization updates PSA from Update Release 14 to Update Release 15, the **Schedule** tab no longer appears as blank on the **Project** form.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]