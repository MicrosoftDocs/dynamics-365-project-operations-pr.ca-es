---
title: Novetats o canvis de la versió d'actualització 31 del Project Service Automation, V3
description: En aquest tema es mostren les característiques i correccions disponibles al Project Service Automation V3, versió d'actualització 31.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 04/26/2021
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
ms.openlocfilehash: a595c0a129ac35d3416984e57908e73e1eaef2fd
ms.sourcegitcommit: 6e1498502461e86cff722ccaf8795ff11c7c47ad
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/27/2021
ms.locfileid: "5945523"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-31-v3"></a><span data-ttu-id="dbc2e-103">Novetats o canvis de la versió d'actualització 31 del Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="dbc2e-103">What's new or changed in Project Service Automation Update Release 31, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="dbc2e-104">Estem encantats d'anunciar-vos l'última actualització per a l'aplicació Project Service Automation per al Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="dbc2e-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="dbc2e-105">Aquesta versió inclou algunes millores importants per a la qualitat, el rendiment i la usabilitat.</span><span class="sxs-lookup"><span data-stu-id="dbc2e-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="dbc2e-106">Aquest llançament és compatible amb el Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="dbc2e-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="dbc2e-107">Per actualitzar a aquesta versió, visiteu el Centre d'administració del Dynamics 365 en línia i aneu a la pàgina de solucions per instal·lar l'actualització.</span><span class="sxs-lookup"><span data-stu-id="dbc2e-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="dbc2e-108">Per obtenir més informació, vegeu [Instal·lar, actualitzar o eliminar una solució preferida](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="dbc2e-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="dbc2e-109">En aquest tema es mostren les característiques i correccions que són noves o s'han canviat per al Project Service Automation V3, versió d'actualització 31.</span><span class="sxs-lookup"><span data-stu-id="dbc2e-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 31.</span></span> <span data-ttu-id="dbc2e-110">Aquesta versió té el número de compilació V3.10.52.77 i està disponible de manera general a través d'una actualització automàtica el maig de 2021.</span><span class="sxs-lookup"><span data-stu-id="dbc2e-110">This version has a build number of V3.10.52.77 and is generally available through a self-update in May 2021.</span></span>

## <a name="update-release-31"></a><span data-ttu-id="dbc2e-111">Versió d'actualització 31</span><span class="sxs-lookup"><span data-stu-id="dbc2e-111">Update Release 31</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="dbc2e-112">Correccions d'errors</span><span class="sxs-lookup"><span data-stu-id="dbc2e-112">Bug fixes</span></span>

<span data-ttu-id="dbc2e-113">**Temps i despesa**</span><span class="sxs-lookup"><span data-stu-id="dbc2e-113">**Time and Expense**</span></span>

<span data-ttu-id="dbc2e-114">S'han corregit els problemes següents:</span><span class="sxs-lookup"><span data-stu-id="dbc2e-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="dbc2e-115">Els botons de l'ordre control d'entrada de temps de la pàgina **Recurs que es pot reservar** eren confusos.</span><span class="sxs-lookup"><span data-stu-id="dbc2e-115">Time entry control command buttons on the **Bookable Resource** page were confusing.</span></span>
- <span data-ttu-id="dbc2e-116">Es generava una excepció de referència nul·la a **Project.SetTrackingFields** quan s'aprovava una entrada de temps.</span><span class="sxs-lookup"><span data-stu-id="dbc2e-116">A null reference exception was generated in **Project.SetTrackingFields** when approving a time entry.</span></span>

<span data-ttu-id="dbc2e-117">**Administració de recursos**</span><span class="sxs-lookup"><span data-stu-id="dbc2e-117">**Resource Management**</span></span>

<span data-ttu-id="dbc2e-118">S'han corregit els problemes següents:</span><span class="sxs-lookup"><span data-stu-id="dbc2e-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="dbc2e-119">**Crea un membre de l'equip** no mostra correctament la configuració de les metadades de configuració de la reserva per a **Estat confirmat per defecte de la reserva**.</span><span class="sxs-lookup"><span data-stu-id="dbc2e-119">**Create Team Member** doesn't correctly display the booking setup metadata setting for **Default Booking Committed Status**.</span></span>
- <span data-ttu-id="dbc2e-120">Quan s'actualitza de PSA 1.X a 3.X, el procés d'actualització falla a **UpgradeResourceRequirements**.</span><span class="sxs-lookup"><span data-stu-id="dbc2e-120">When upgrading from PSA 1.X to 3.X, the upgrade process fails at **UpgradeResourceRequirements**.</span></span>


<span data-ttu-id="dbc2e-121">**Vendes**</span><span class="sxs-lookup"><span data-stu-id="dbc2e-121">**Sales**</span></span>

<span data-ttu-id="dbc2e-122">S'han corregit els problemes següents:</span><span class="sxs-lookup"><span data-stu-id="dbc2e-122">The following issues have been fixed:</span></span>

- <span data-ttu-id="dbc2e-123">Els ingressos reals converteixen els imports a la moneda del projecte a la quadrícula de seguiment.</span><span class="sxs-lookup"><span data-stu-id="dbc2e-123">Actual revenue converts the amounts to the project currency in the tracking grid.</span></span>
- <span data-ttu-id="dbc2e-124">El valor per defecte de la moneda no està clar quan es creen línies del llibre diari, línies d'oferta i línies de contracte en casos en què la moneda base d'una organització és diferent de la moneda del projecte.</span><span class="sxs-lookup"><span data-stu-id="dbc2e-124">The currency default is unclear when creating journal lines, quote lines, and contract lines in scenarios where an organization's base currency differs from the project currency.</span></span>
- <span data-ttu-id="dbc2e-125">La consulta **Validació del llibre diari de correcció pendent** no filtra per projecte.</span><span class="sxs-lookup"><span data-stu-id="dbc2e-125">**Pending correction journal validation** query doesn't filter by project.</span></span>
- <span data-ttu-id="dbc2e-126">La resta de vendes no es calcula correctament en un projecte.</span><span class="sxs-lookup"><span data-stu-id="dbc2e-126">Remaining sales are calculated incorrectly on a project.</span></span>
- <span data-ttu-id="dbc2e-127">Les ofertes basades en un contacte fallen quan es creen sense una llista de preus.</span><span class="sxs-lookup"><span data-stu-id="dbc2e-127">Quotes based on a contact fail when they are created without a price list.</span></span>
- <span data-ttu-id="dbc2e-128">No es mostra cap indicador giratori de processament quan seleccioneu **Confirma la factura**.</span><span class="sxs-lookup"><span data-stu-id="dbc2e-128">No processing spinner is shown when you select **Confirm Invoice**.</span></span>
- <span data-ttu-id="dbc2e-129">No es mostra cap indicador giratori de processament quan seleccioneu **Crea la factura**.</span><span class="sxs-lookup"><span data-stu-id="dbc2e-129">No processing spinner is shown when you select **Create Invoice**.</span></span>
- <span data-ttu-id="dbc2e-130">El tancament d'una oferta com a perduda no cancel·la les reserves.</span><span class="sxs-lookup"><span data-stu-id="dbc2e-130">Closing a quote as lost doesn't cancel the bookings.</span></span>







