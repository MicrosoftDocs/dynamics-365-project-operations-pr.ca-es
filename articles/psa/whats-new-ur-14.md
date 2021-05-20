---
title: Novetats o canvis de la versió d'actualització 14 del Project Service Automation, V3
description: En aquest tema es proporciona informació sobre les novetats a la versió d'actualització 14 del Project Service Automation, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/29/2020
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
ms.openlocfilehash: 1d0aeb4684ae04d8774a31a51664ceb84307b10d
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949355"
---
# <a name="project-service-automation-update-release-14-v3"></a><span data-ttu-id="919e0-103">Project Service Automation, versió d'actualització 14, V3</span><span class="sxs-lookup"><span data-stu-id="919e0-103">Project Service Automation Update Release 14, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="919e0-104">Ens complau anunciar la darrera actualització de l'aplicació Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="919e0-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="919e0-105">Aquesta versió inclou algunes millores importants per a la qualitat, el rendiment i la usabilitat.</span><span class="sxs-lookup"><span data-stu-id="919e0-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="919e0-106">Aquest llançament és compatible amb el Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="919e0-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="919e0-107">Per actualitzar a aquesta versió, visiteu el Centre d'administració del Dynamics 365 en línia i aneu a la pàgina de solucions per instal·lar l'actualització.</span><span class="sxs-lookup"><span data-stu-id="919e0-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="919e0-108">Per obtenir més informació, vegeu [Instal·lar, actualitzar o eliminar una solució preferida](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="919e0-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="919e0-109">En aquest tema es mostren les característiques i correccions que són noves o s'han canviat per al PSA V3, versió d'actualització 14.</span><span class="sxs-lookup"><span data-stu-id="919e0-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 14.</span></span> <span data-ttu-id="919e0-110">Aquesta versió té el número de compilació V3.10.4.21 i està disponible segons la planificació següent:</span><span class="sxs-lookup"><span data-stu-id="919e0-110">This version has a build number of V3.10.4.21 and is available on the following schedule:</span></span>

- <span data-ttu-id="919e0-111">**Disponibilitat general (actualització automàtica):** gener de 2020</span><span class="sxs-lookup"><span data-stu-id="919e0-111">**General availability (self-update):** January 2020</span></span>
- <span data-ttu-id="919e0-112">**Actualització automàtica:** febrer de 2020</span><span class="sxs-lookup"><span data-stu-id="919e0-112">**Auto-update:** February 2020</span></span>

## <a name="update-release-14"></a><span data-ttu-id="919e0-113">Versió d'actualització 14</span><span class="sxs-lookup"><span data-stu-id="919e0-113">Update Release 14</span></span>

### <a name="enhancements"></a><span data-ttu-id="919e0-114">Millores</span><span class="sxs-lookup"><span data-stu-id="919e0-114">Enhancements</span></span>

- <span data-ttu-id="919e0-115">Sales</span><span class="sxs-lookup"><span data-stu-id="919e0-115">Sales</span></span>

     - <span data-ttu-id="919e0-116">Els valors de camp personalitzats de **Detalls de la línia d'oferta** es copien a **Detalls de la línia de contracte del projecte** quan s'actualitza una oferta a **Tancada com a guanyada**.</span><span class="sxs-lookup"><span data-stu-id="919e0-116">Custom field values from **Quote Line Details** are copied to **Project Contract Line Details** when a quote is updated to **Closed as won**.</span></span>
     - <span data-ttu-id="919e0-117">Els projectes confirmats es poden **Tancar com a perduts**.</span><span class="sxs-lookup"><span data-stu-id="919e0-117">Confirmed projects can be **Closed as lost**.</span></span>

- <span data-ttu-id="919e0-118">Administració de recursos</span><span class="sxs-lookup"><span data-stu-id="919e0-118">Resource Management</span></span>

     - <span data-ttu-id="919e0-119">En ampliar les reserves, es demanarà als usuaris amb un quadre de diàleg de confirmació que resumeixin els resultats de la reserva i proporcionin un enllaç per mantenir les reserves.</span><span class="sxs-lookup"><span data-stu-id="919e0-119">When extending bookings, users will be prompted with a confirmation dialog box to summarize booking results and provide a link to Maintain Bookings.</span></span>


### <a name="bug-fixes"></a><span data-ttu-id="919e0-120">Correccions d'errors</span><span class="sxs-lookup"><span data-stu-id="919e0-120">Bug fixes</span></span>

- <span data-ttu-id="919e0-121">Temps i despesa</span><span class="sxs-lookup"><span data-stu-id="919e0-121">Time and Expense</span></span>

     - <span data-ttu-id="919e0-122">Correcció: s'ha millorat l'experiència de l'usuari quan l'usuari no ha seleccionat cap entrada per corregir-la.</span><span class="sxs-lookup"><span data-stu-id="919e0-122">Fixed: Improved the user experience when the user has not selected any entries to be corrected.</span></span>

- <span data-ttu-id="919e0-123">Administració de recursos</span><span class="sxs-lookup"><span data-stu-id="919e0-123">Resource Management</span></span>

     - <span data-ttu-id="919e0-124">Correcció: si es reserva un recurs diverses vegades es desborda el nom del recurs reservable.</span><span class="sxs-lookup"><span data-stu-id="919e0-124">Fixed: Booking a resource multiple times overflows the name of the bookable resource.</span></span>

- <span data-ttu-id="919e0-125">Sales</span><span class="sxs-lookup"><span data-stu-id="919e0-125">Sales</span></span>

     - <span data-ttu-id="919e0-126">Correcció: el preu total de venda no es calcula fins que l'usuari també introdueix un preu de cost per a l'estimació de despeses en un projecte.</span><span class="sxs-lookup"><span data-stu-id="919e0-126">Fixed: The total sales price is not calculated until the user also inputs a cost price for expense estimates on a project.</span></span>
     - <span data-ttu-id="919e0-127">Correcció: el tancament d'una oferta com a **Guanyada** falla si el contracte del projecte associat no està en estat **Esborrany**.</span><span class="sxs-lookup"><span data-stu-id="919e0-127">Fixed: Closing a quote as **Won** fails if the associated project contract is not in a **Draft** state.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]