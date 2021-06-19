---
title: Novetats o canvis de la versió d'actualització 32 del Project Service Automation, V3
description: En aquest tema es mostren les característiques i correccions disponibles al Project Service Automation V3, versió d'actualització 32.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/01/2021
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
ms.openlocfilehash: 11bf451ef4f24e2301ffde4f86a556a8a4fe30b0
ms.sourcegitcommit: 886102894244887d72e5a6213071e8d8a52c9d48
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/01/2021
ms.locfileid: "6129654"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-32-v3"></a><span data-ttu-id="eb487-103">Novetats o canvis de la versió d'actualització 32 del Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="eb487-103">What's new or changed in Project Service Automation Update Release 32, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="eb487-104">Ens complau anunciar l'última actualització de l'aplicació Microsoft Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="eb487-104">We're pleased to announce the latest update for the Microsoft Dynamics 365 Project Service Automation app.</span></span> <span data-ttu-id="eb487-105">Aquesta versió inclou algunes millores importants per a la qualitat, el rendiment i la usabilitat.</span><span class="sxs-lookup"><span data-stu-id="eb487-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="eb487-106">És compatible amb el Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="eb487-106">It's compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="eb487-107">Per actualitzar aquesta versió, visiteu la pàgina de solucions en línia del Centre d'administració del Dynamics 365 i instal·leu l'actualització.</span><span class="sxs-lookup"><span data-stu-id="eb487-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page, and install the update.</span></span> <span data-ttu-id="eb487-108">Per obtenir més informació, vegeu [Instal·lar, actualitzar o eliminar una solució preferida](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="eb487-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="eb487-109">En aquest tema es mostren les característiques i correccions que són noves o s'han canviat per al Project Service Automation V3, versió d'actualització 32.</span><span class="sxs-lookup"><span data-stu-id="eb487-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 32.</span></span> <span data-ttu-id="eb487-110">Aquesta versió té el número de compilació V3.10.53.108 i està disponible de manera general a través d'una actualització d'autoservei el juny de 2021.</span><span class="sxs-lookup"><span data-stu-id="eb487-110">This version has a build number of V3.10.53.108 and is generally available through a self-update in June 2021.</span></span>

## <a name="update-release-32"></a><span data-ttu-id="eb487-111">Versió d'actualització 32</span><span class="sxs-lookup"><span data-stu-id="eb487-111">Update Release 32</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="eb487-112">Correccions d'errors</span><span class="sxs-lookup"><span data-stu-id="eb487-112">Bug fixes</span></span>

#### <a name="general"></a><span data-ttu-id="eb487-113">General</span><span class="sxs-lookup"><span data-stu-id="eb487-113">General</span></span>

- <span data-ttu-id="eb487-114">Quan es produeix un error en una actualització principal, només s'han de bloquejar els punts d'entrada principals de l'aplicació per assegurar-vos que les entitats compartides encara siguin accessibles.</span><span class="sxs-lookup"><span data-stu-id="eb487-114">When a major upgrade fails, only the main application entry points should be blocked, to ensure that shared entities are still accessible.</span></span>

#### <a name="time-and-expense"></a><span data-ttu-id="eb487-115">Temps i despesa</span><span class="sxs-lookup"><span data-stu-id="eb487-115">Time and Expense</span></span>

<span data-ttu-id="eb487-116">S'han corregit els problemes següents:</span><span class="sxs-lookup"><span data-stu-id="eb487-116">The following issues have been fixed:</span></span>

- <span data-ttu-id="eb487-117">**TimeEntriesImportFromResourceAssignment** no conserva les hores d'inici i d'acabament de les porcions de contorn d'assignació de recursos.</span><span class="sxs-lookup"><span data-stu-id="eb487-117">**TimeEntriesImportFromResourceAssignment** doesn't maintain the start and end times of the resource assignment contour slice.</span></span>
- <span data-ttu-id="eb487-118">Quan seleccioneu **Obre l'entrada** a la quadrícula **Entrada de temps**, és possible que no pugueu seleccionar altres formularis.</span><span class="sxs-lookup"><span data-stu-id="eb487-118">When you select **Open Entry** on the **Time Entry** grid, you might be prevented from selecting other forms.</span></span>
- <span data-ttu-id="eb487-119">Mentre importeu assignacions a entrades de temps, la consulta de codi de client podria generar una adreça URL llarga que generi un error a la consulta.</span><span class="sxs-lookup"><span data-stu-id="eb487-119">While you import assignments to time entries, the client code query could generate a long URL that fails the query.</span></span>
- <span data-ttu-id="eb487-120">A la quadrícula **Entrada de temps**, després de suprimir un valor d'una cel·la, el focus no es queda a la quadrícula.</span><span class="sxs-lookup"><span data-stu-id="eb487-120">In the **Time Entry** grid, after a value is deleted from a cell, the focus doesn't remain in the grid.</span></span>
- <span data-ttu-id="eb487-121">El botó **Rebutja** s'ha eliminat de la visualització **Aprovacions de processament** per a les aprovacions moderns.</span><span class="sxs-lookup"><span data-stu-id="eb487-121">The **Reject** button has been removed from the **Processing approvals** view for modern approvals.</span></span>
- <span data-ttu-id="eb487-122">L'estabilitat i el rendiment de l'aprovació massiva d'entrades de temps es veuen afectades per bloquejos i un error en gestionar correctament les personalitzacions relacionades amb l'entitat **Entrada de temps**.</span><span class="sxs-lookup"><span data-stu-id="eb487-122">The stability and performance of time entry bulk approval are affected by deadlocks and a failure to appropriately handle customizations that are related to the **Time Entry** entity.</span></span>

#### <a name="project-planning"></a><span data-ttu-id="eb487-123">Planificació del projecte</span><span class="sxs-lookup"><span data-stu-id="eb487-123">Project Planning</span></span>

- <span data-ttu-id="eb487-124">Una excepció de referència nul·la es genera quan actualitzeu un projecte que té un valor nul al camp **Unitat contractant**.</span><span class="sxs-lookup"><span data-stu-id="eb487-124">A null reference exception is generated when you update a project that has a null value in the **Contracting Unit** field.</span></span>
- <span data-ttu-id="eb487-125">**Actualitza els totals del projecte** calcula incorrectament el cost restant i les vendes restants en un projecte.</span><span class="sxs-lookup"><span data-stu-id="eb487-125">**Refresh Project Totals** incorrectly calculates the remaining cost and remaining sales on a project.</span></span>
- <span data-ttu-id="eb487-126">Els càlculs de preus redundants afecten el rendiment relacionat amb les actualitzacions dels contorns d'assignació de recursos.</span><span class="sxs-lookup"><span data-stu-id="eb487-126">Redundant pricing calculations affect performance that is related to updates on resource assignment contours.</span></span>

#### <a name="resource-management"></a><span data-ttu-id="eb487-127">Administració de recursos</span><span class="sxs-lookup"><span data-stu-id="eb487-127">Resource Management</span></span>

<span data-ttu-id="eb487-128">S'ha corregit el problema següent:</span><span class="sxs-lookup"><span data-stu-id="eb487-128">The following issue has been fixed:</span></span>

- <span data-ttu-id="eb487-129">Quan la capacitat de calendari d'un recurs que es pot reservar és més d'1, el Project Service Automation reconeix incorrectament la capacitat com a 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="eb487-129">When a bookable resource's calendar capacity is more than 1, Project Service Automation incorrectly recognizes the capacity as 0 (zero).</span></span> <span data-ttu-id="eb487-130">Per tant, es produeix un bucle infinit a la visualització de planificació.</span><span class="sxs-lookup"><span data-stu-id="eb487-130">Therefore, an infinite loop occurs in the schedule view.</span></span>

#### <a name="sales"></a><span data-ttu-id="eb487-131">Vendes</span><span class="sxs-lookup"><span data-stu-id="eb487-131">Sales</span></span>

<span data-ttu-id="eb487-132">S'han corregit els problemes següents:</span><span class="sxs-lookup"><span data-stu-id="eb487-132">The following issues have been fixed:</span></span>

- <span data-ttu-id="eb487-133">Quan es crea una línia del llibre diari que té un tipus de transacció personalitzat, es produeix l'excepció de referència nul·la següent: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType(TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.</span><span class="sxs-lookup"><span data-stu-id="eb487-133">When a journal line is created that has a custom transaction type, the following null reference exception occurs: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType(TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.</span></span>
- <span data-ttu-id="eb487-134">No afegiu funcions i categories desactivades abans de copiar una oferta a funcions i categories imputables d'una oferta nova copiada.</span><span class="sxs-lookup"><span data-stu-id="eb487-134">Roles and categories that are inactivated before a quotation is copied should not be added to chargeable roles and categories of the newly copied quotation.</span></span>
- <span data-ttu-id="eb487-135">La data i la data de compte del document no estan alineades amb la data d'inici que es proporciona en un detall de la línia de factura que es crea directament en un esborrany de factura.</span><span class="sxs-lookup"><span data-stu-id="eb487-135">The document date and accounting date aren't aligned with the start date that is provided on an invoice line detail that is created directly on a draft invoice.</span></span>
- <span data-ttu-id="eb487-136">Es generen excepcions de referència nul·la en escenaris relacionats amb la inactivació de funcions i categories abans de copiar una oferta.</span><span class="sxs-lookup"><span data-stu-id="eb487-136">Null reference exceptions are generated in scenarios that are related to inactivation of roles and categories before a quotation is copied.</span></span>
- <span data-ttu-id="eb487-137">L'acció **Actualitza els preus** a la pàgina **Projectes** no actualitza les estimacions de despeses ni les estimacions de materials.</span><span class="sxs-lookup"><span data-stu-id="eb487-137">The **Update Prices** action on the **Projects** page doesn't update expense estimates and material estimates.</span></span>
