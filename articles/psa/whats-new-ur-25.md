---
title: Novetats o canvis de la versió d'actualització 25 del Project Service Automation, V3
description: En aquest tema es mostren les característiques i correccions disponibles al Project Service Automation V3, versió d'actualització 25.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 10/26/2020
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
ms.openlocfilehash: 3aa10e1d4b23fbe6c2743d71497bdef840776008
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948859"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-25-v3"></a><span data-ttu-id="fb159-103">Novetats o canvis de la versió d'actualització 25 del Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="fb159-103">What's new or changed in Project Service Automation Update Release 25, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="fb159-104">Estem encantats d'anunciar-vos l'última actualització per a l'aplicació Project Service Automation per al Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="fb159-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="fb159-105">Aquesta versió inclou algunes millores importants per a la qualitat, el rendiment i la usabilitat.</span><span class="sxs-lookup"><span data-stu-id="fb159-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="fb159-106">Aquest llançament és compatible amb el Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="fb159-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="fb159-107">Per actualitzar a aquesta versió, visiteu el Centre d'administració del Dynamics 365 en línia i aneu a la pàgina de solucions per instal·lar l'actualització.</span><span class="sxs-lookup"><span data-stu-id="fb159-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="fb159-108">Per obtenir més informació, vegeu [Instal·lar, actualitzar o eliminar una solució preferida](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="fb159-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="fb159-109">Aquest tema enumera les característiques i correccions noves o canviades per al Project Service Automation V3, llançament d'actualització 25 Aquesta versió té el número de compilació V3.10.43.76 i està disponible de manera general a través d'una actualització autoservei l'octubre de 2020.</span><span class="sxs-lookup"><span data-stu-id="fb159-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 25 This version has a build number of V 3.10.43.76 and is generally available through a self-update in October 2020.</span></span>

## <a name="update-release-25"></a><span data-ttu-id="fb159-110">Versió d'actualització 25</span><span class="sxs-lookup"><span data-stu-id="fb159-110">Update Release 25</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="fb159-111">Correccions d'errors</span><span class="sxs-lookup"><span data-stu-id="fb159-111">Bug fixes</span></span>

<span data-ttu-id="fb159-112">**Temps i despesa**</span><span class="sxs-lookup"><span data-stu-id="fb159-112">**Time and Expense**</span></span>

<span data-ttu-id="fb159-113">S'ha corregit el problema següent:</span><span class="sxs-lookup"><span data-stu-id="fb159-113">The following issue has been fixed:</span></span>

- <span data-ttu-id="fb159-114">El gràfic d'entrada de temps mostra dades addicionals si es recupera un interval massa gran.</span><span class="sxs-lookup"><span data-stu-id="fb159-114">Time entry chart showing additional data based on too large of an interval being retrieved.</span></span>

<span data-ttu-id="fb159-115">**Administració de recursos**</span><span class="sxs-lookup"><span data-stu-id="fb159-115">**Resource Management**</span></span>

<span data-ttu-id="fb159-116">S'ha corregit el problema següent:</span><span class="sxs-lookup"><span data-stu-id="fb159-116">The following issue has been fixed:</span></span>

- <span data-ttu-id="fb159-117">S'ha afegit codi al Package Deployer per ometre la importació de pedaços de l'Universal Resource Scheduling si ja existeix un pedaç de versió superior.</span><span class="sxs-lookup"><span data-stu-id="fb159-117">Added package deployer code to skip the Universal Resource Scheduling patch import if a higher version patch already exists.</span></span>

<span data-ttu-id="fb159-118">**Administració de projectes**</span><span class="sxs-lookup"><span data-stu-id="fb159-118">**Project Management**</span></span>

<span data-ttu-id="fb159-119">S'han corregit els problemes següents:</span><span class="sxs-lookup"><span data-stu-id="fb159-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="fb159-120">S'han corregit discrepàncies d'arrodoniment i tipus de canvi que provocaven un cost planificat incorrecte a la quadrícula de seguiment del projecte.</span><span class="sxs-lookup"><span data-stu-id="fb159-120">Corrected rounding and exchange rate discrepancies resulting in incorrect planned cost in the project tracking grid.</span></span>
- <span data-ttu-id="fb159-121">S'admet la possibilitat de mostrar dues o més quadrícules de reacció al formulari **Projecte**.</span><span class="sxs-lookup"><span data-stu-id="fb159-121">Support the ability to display two or more react grids on the **Project** form.</span></span>
- <span data-ttu-id="fb159-122">Es proporciona validació per abordar la possibilitat d'assignar una tasca més enllà de la data de finalització del calendari, que provoca una assignació de recursos amb errors.</span><span class="sxs-lookup"><span data-stu-id="fb159-122">Provided validation to address the ability to assign a task past the calendar end date, which results in a failed resource assignment.</span></span>
- <span data-ttu-id="fb159-123">Millora de la gestió d'errors per fer front a l'excepció de referència nul·la generada a partir del següent:</span><span class="sxs-lookup"><span data-stu-id="fb159-123">Improved error handling to address Null Reference Exception generated from the following:</span></span>

    - <span data-ttu-id="fb159-124">Connector **PreValidateProjectTeamMemberCreate**</span><span class="sxs-lookup"><span data-stu-id="fb159-124">**PreValidateProjectTeamMemberCreate** plug-in</span></span>
    - <span data-ttu-id="fb159-125">**PreValidateProjectTaskCreate** quan es crea una tasca de projecte sense un projecte associat</span><span class="sxs-lookup"><span data-stu-id="fb159-125">**PreValidateProjectTaskCreate** when a project task is created without an associated project</span></span>
    - <span data-ttu-id="fb159-126">Connector **PreProjectTeamMemberCreate**</span><span class="sxs-lookup"><span data-stu-id="fb159-126">**PreProjectTeamMemberCreate** plug-in</span></span>
    - <span data-ttu-id="fb159-127">Connector **PostProjectTeamMemberDelete**</span><span class="sxs-lookup"><span data-stu-id="fb159-127">**PostProjectTeamMemberDelete** plug-in</span></span>
    - <span data-ttu-id="fb159-128">Connector **PreValidateProjectTaskDelete**</span><span class="sxs-lookup"><span data-stu-id="fb159-128">**PreValidateProjectTaskDelete** plug-in</span></span>

<span data-ttu-id="fb159-129">**Sales**</span><span class="sxs-lookup"><span data-stu-id="fb159-129">**Sales**</span></span>

<span data-ttu-id="fb159-130">S'han corregit els problemes següents:</span><span class="sxs-lookup"><span data-stu-id="fb159-130">The following issues have been fixed:</span></span>

- <span data-ttu-id="fb159-131">Millora de la gestió d'errors per fer front a les excepcions de referència nul·la generades a partir de **Copia el projecte: estimació de l'administració de HelperResource**.</span><span class="sxs-lookup"><span data-stu-id="fb159-131">Improved error handling to address Null Reference Exceptions generated from **Copy Project: Estimates HelperResource Management**.</span></span>
- <span data-ttu-id="fb159-132">**No està a punt per facturar** un **registre de facturació de temps i material** no esborra l'estat de facturació.</span><span class="sxs-lookup"><span data-stu-id="fb159-132">**Not ready to Invoice** on a **Time and Material Billing Backlog** doesn't clear the billing status.</span></span>
- <span data-ttu-id="fb159-133">S'han corregit els botons de **preus** mal etiquetats a la pestanya **Preu per funció** i **Articles del catàleg**.</span><span class="sxs-lookup"><span data-stu-id="fb159-133">Corrected mislabeled **Prices** buttons on the **Role Price** and **Catalog Items** tab.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]