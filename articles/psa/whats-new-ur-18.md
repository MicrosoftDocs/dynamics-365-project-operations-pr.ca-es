---
title: Novetats o canvis de la versió d'actualització 18 del Project Service Automation, V3
description: En aquest tema es mostren les característiques i correccions disponibles al Project Service Automation V3, versió d'actualització 18.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 04/27/2020
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
ms.openlocfilehash: bd6038b3594e8507c4a441b00ddc2eb240f796dc
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949172"
---
# <a name="project-service-automation-update-release-18-v3"></a><span data-ttu-id="b0abe-103">Project Service Automation, versió d'actualització 18, V3</span><span class="sxs-lookup"><span data-stu-id="b0abe-103">Project Service Automation Update Release 18, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="b0abe-104">Estem encantats d'anunciar-vos l'última actualització per a l'aplicació Project Service Automation per al Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="b0abe-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="b0abe-105">Aquesta versió inclou algunes millores importants per a la qualitat, el rendiment i la usabilitat.</span><span class="sxs-lookup"><span data-stu-id="b0abe-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="b0abe-106">Aquest llançament és compatible amb el Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="b0abe-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="b0abe-107">Per actualitzar a aquesta versió, visiteu el Centre d'administració del Dynamics 365 en línia i aneu a la pàgina de solucions per instal·lar l'actualització.</span><span class="sxs-lookup"><span data-stu-id="b0abe-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="b0abe-108">Per obtenir més informació, vegeu [Instal·lar, actualitzar o eliminar una solució preferida](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="b0abe-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="b0abe-109">En aquest tema es mostren les característiques i correccions que són noves o s'han canviat per al Project Service Automation V3, versió d'actualització 18.</span><span class="sxs-lookup"><span data-stu-id="b0abe-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 18.</span></span> <span data-ttu-id="b0abe-110">Aquesta versió té el número de compilació V3.10.8.12 i està disponible de manera general a través d'una actualització automàtica l'abril de 2020.</span><span class="sxs-lookup"><span data-stu-id="b0abe-110">This version has a build number of V3.10.8.12 and is generally available through a self-update in April 2020.</span></span>

## <a name="update-release-18"></a><span data-ttu-id="b0abe-111">Versió d'actualització 18</span><span class="sxs-lookup"><span data-stu-id="b0abe-111">Update Release 18</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="b0abe-112">Correccions d'errors</span><span class="sxs-lookup"><span data-stu-id="b0abe-112">Bug fixes</span></span>

<span data-ttu-id="b0abe-113">**Temps i despesa**</span><span class="sxs-lookup"><span data-stu-id="b0abe-113">**Time and Expense**</span></span>

- <span data-ttu-id="b0abe-114">Correcció: els fluxos **Recupera**, **Sol·licita** i **Cancel·la l'aprovació** generen excepcions amb missatges d'error poc clars.</span><span class="sxs-lookup"><span data-stu-id="b0abe-114">Fixed: **Recall**, **Request**, and **Cancel Approval** flows throw exceptions with unclear error messages.</span></span>
- <span data-ttu-id="b0abe-115">Correcció: quan **Cancel·la l'aprovació** no funciona amb una despesa, no es genera un error d'excepció rellevant.</span><span class="sxs-lookup"><span data-stu-id="b0abe-115">Fixed: When **Cancel Approval** fails for an expense, a relevant exception error is not thrown.</span></span>
- <span data-ttu-id="b0abe-116">Correcció: la graella d'entrada de temps gestiona incorrectament els dies no laborables a Austràlia després del canvi a horari d'estiu (DST) a l'octubre.</span><span class="sxs-lookup"><span data-stu-id="b0abe-116">Fixed: The Time Entry grid incorrectly handles non-working days in Australia after the daylight savings time (DST) switch in October.</span></span>
- <span data-ttu-id="b0abe-117">Correcció: la lògica per defecte incorrecta impedeix l'enviament de les despeses.</span><span class="sxs-lookup"><span data-stu-id="b0abe-117">Fixed: Incorrect defaulting logic prevents submission of expenses.</span></span>
- <span data-ttu-id="b0abe-118">Correcció: quan l'aprovació de l'entrada de temps no funciona, l'aprovació es manté en estat **Pendent**.</span><span class="sxs-lookup"><span data-stu-id="b0abe-118">Fixed: When time entry approval fails, the approval remains in a state of **Pending**.</span></span>
- <span data-ttu-id="b0abe-119">Correcció: errors de l'SQL en l'aprovació massiva (bloqueig/expiració del temps d'espera).</span><span class="sxs-lookup"><span data-stu-id="b0abe-119">Fixed: SQL Errors on bulk approvals (deadlock/timeout).</span></span>
- <span data-ttu-id="b0abe-120">Correcció: problemes significatius de rendiment a l'experiència de l'usuari provocats per l'actualització dels membres de l'equip en aprovar les entrades de temps.</span><span class="sxs-lookup"><span data-stu-id="b0abe-120">Fixed: Significant performance issues in the user experience caused by updating team members while approving time entries.</span></span>

<span data-ttu-id="b0abe-121">**Administració de projectes**</span><span class="sxs-lookup"><span data-stu-id="b0abe-121">**Project Management**</span></span>

- <span data-ttu-id="b0abe-122">Correcció: s'ha traslladat la notificació de fus horari de la visualització **Conciliació** al formulari principal del **Projecte**.</span><span class="sxs-lookup"><span data-stu-id="b0abe-122">Fixed: Time zone notification moved from the **Reconciliation** view to the **Project** main form.</span></span>
- <span data-ttu-id="b0abe-123">Correcció: la plantilla de calendari no pren correctament el valor per defecte quan s'obre un nou formulari de projecte.</span><span class="sxs-lookup"><span data-stu-id="b0abe-123">Fixed: Calendar template is not correctly defaulting when a new project form opens.</span></span>
- <span data-ttu-id="b0abe-124">Correcció: en els navegadors basats en Chromium, els usuaris no poden seleccionar fàcilment les tasques predecessores que s'han de suprimir.</span><span class="sxs-lookup"><span data-stu-id="b0abe-124">Fixed: For chromium-based browsers, users are unable to easily select predecessor tasks to delete.</span></span>
- <span data-ttu-id="b0abe-125">Correcció: la creació o la còpia d'un **Projecte des d'una plantilla buida** recupera assignacions no relacionades.</span><span class="sxs-lookup"><span data-stu-id="b0abe-125">Fixed: Creating or copying **Project from Empty template** fetches unrelated assignments.</span></span>
- <span data-ttu-id="b0abe-126">Correcció: en alguns casos poc habituals específics, la creació d'una assignació nova des de la quadrícula de tasques provoca la creació de registres duplicats.</span><span class="sxs-lookup"><span data-stu-id="b0abe-126">Fixed: In specific edge cases, creating a new assignment from the task grid results in duplicate records being created.</span></span>
- <span data-ttu-id="b0abe-127">Correcció: en el mode manual, els usuaris no poden actualitzar les dates d'inici de les tasques a una data posterior a la data desada actualment.</span><span class="sxs-lookup"><span data-stu-id="b0abe-127">Fixed: In manual mode, users are unable to update task start dates to be later than the current date saved.</span></span>

<span data-ttu-id="b0abe-128">**Administració de recursos**</span><span class="sxs-lookup"><span data-stu-id="b0abe-128">**Resource Management**</span></span>

- <span data-ttu-id="b0abe-129">Correcció: la fila de subtotal de la visualització **Conciliació** calcula incorrectament la diferència de reserves després d'ampliar les reserves.</span><span class="sxs-lookup"><span data-stu-id="b0abe-129">Fixed: **Reconciliation** view subtotal row incorrectly calculates bookings variance after extending bookings.</span></span>
- <span data-ttu-id="b0abe-130">Correcció: la visualització **Conciliació** mostra incorrectament les assignacions de recursos quan el recurs reservable té un calendari que no coincideix amb el calendari del projecte.</span><span class="sxs-lookup"><span data-stu-id="b0abe-130">Fixed: **Reconciliation** view incorrectly displays resource assignments when the bookable resource has a calendar that does not match the project calendar.</span></span>

<span data-ttu-id="b0abe-131">**Sales**</span><span class="sxs-lookup"><span data-stu-id="b0abe-131">**Sales**</span></span>

- <span data-ttu-id="b0abe-132">Correcció: quan es tornen a aprovar les entrades de temps (**Aprova > Cancel·la >** Torna a aprovar), es crea un valor real no imputable duplicat.</span><span class="sxs-lookup"><span data-stu-id="b0abe-132">Fixed: When time entries are re-approved (**Approve > Cancel >** approve again), a duplicate non-chargeable actual is created.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]