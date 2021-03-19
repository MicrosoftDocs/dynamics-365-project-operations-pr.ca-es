---
title: Novetats o canvis de la versió d'actualització 27.6 del Project Service Automation revisió, V3
description: En aquest tema es mostren les característiques i correccions que hi ha disponibles per al llançament de l'actualització 27.6, V3, de Project Service Automation.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/17/2021
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
ms.openlocfilehash: f6576c6c5660ff6e8e53286ae226c8278a33f2be
ms.sourcegitcommit: 24528bb9c0ef8898077cb3bc672daa211c0e73aa
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 03/04/2021
ms.locfileid: "5481224"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-276-v3"></a><span data-ttu-id="356aa-103">Novetats o canvis de la versió d'actualització 27.6 del Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="356aa-103">What's new or changed in Project Service Automation Update Release 27.6, V3</span></span>

<span data-ttu-id="356aa-104">Estem encantats d'anunciar-vos l'última actualització per a l'aplicació Project Service Automation per al Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="356aa-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="356aa-105">Aquesta versió inclou algunes millores importants per a la qualitat, el rendiment i la usabilitat.</span><span class="sxs-lookup"><span data-stu-id="356aa-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="356aa-106">Aquest llançament és compatible amb el Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="356aa-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="356aa-107">Per actualitzar a aquesta versió, visiteu el Centre d'administració del Dynamics 365 en línia i aneu a la pàgina de solucions per instal·lar l'actualització.</span><span class="sxs-lookup"><span data-stu-id="356aa-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="356aa-108">Per obtenir més informació, vegeu [Instal·lar, actualitzar o eliminar una solució preferida](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="356aa-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="356aa-109">En aquest tema es mostren les característiques i correccions que són noves o s'han canviat per al Project Service Automation V3, versió d'actualització 27.6.</span><span class="sxs-lookup"><span data-stu-id="356aa-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 27.6.</span></span> <span data-ttu-id="356aa-110">Aquesta versió té el número de compilació V3.10.45.120 i està disponible de forma general a través d'una actualització automàtica el gener de 2021.</span><span class="sxs-lookup"><span data-stu-id="356aa-110">This version has a build number of V3.10.45.120 and is generally available through a self-update in January 2021.</span></span>

## <a name="update-release-276"></a><span data-ttu-id="356aa-111">Versió d'actualització 27.6</span><span class="sxs-lookup"><span data-stu-id="356aa-111">Update Release 27.6</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="356aa-112">Correccions d'errors</span><span class="sxs-lookup"><span data-stu-id="356aa-112">Bug fixes</span></span>


<span data-ttu-id="356aa-113">**Administració de recursos**</span><span class="sxs-lookup"><span data-stu-id="356aa-113">**Resource Management**</span></span>

<span data-ttu-id="356aa-114">S'han corregit els problemes següents:</span><span class="sxs-lookup"><span data-stu-id="356aa-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="356aa-115">Quan se cerca la disponibilitat de recursos, es crida **ExpandCalendar** per a cada recurs que no té regles de calendari aplicades.</span><span class="sxs-lookup"><span data-stu-id="356aa-115">When finding resource availability, **ExpandCalendar** is called for each resource that has no calendar rules applied.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
