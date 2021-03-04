---
title: Novetats o canvis de la versió d'actualització 22 del Project Service Automation, V3
description: En aquest tema es mostren les característiques i correccions disponibles al Project Service Automation V3, versió d'actualització 22.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 07/28/2020
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
ms.openlocfilehash: db4cbb9f9daadcb1911325f8bee987d5e480e1cf
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150971"
---
# <a name="project-service-automation-update-release-22-v3"></a><span data-ttu-id="0fd85-103">Project Service Automation, versió d'actualització 22, V3</span><span class="sxs-lookup"><span data-stu-id="0fd85-103">Project Service Automation Update Release 22, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="0fd85-104">Estem encantats d'anunciar-vos l'última actualització per a l'aplicació Project Service Automation per al Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="0fd85-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="0fd85-105">Aquesta versió inclou algunes millores importants per a la qualitat, el rendiment i la usabilitat.</span><span class="sxs-lookup"><span data-stu-id="0fd85-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="0fd85-106">Aquest llançament és compatible amb el Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="0fd85-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="0fd85-107">Per actualitzar a aquesta versió, visiteu el Centre d'administració del Dynamics 365 en línia i aneu a la pàgina de solucions per instal·lar l'actualització.</span><span class="sxs-lookup"><span data-stu-id="0fd85-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="0fd85-108">Per obtenir més informació, vegeu [Instal·lar, actualitzar o eliminar una solució preferida](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="0fd85-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="0fd85-109">En aquest tema es mostren les característiques i correccions que són noves o s'han canviat per al Project Service Automation V3, versió d'actualització 22.</span><span class="sxs-lookup"><span data-stu-id="0fd85-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 22.</span></span> <span data-ttu-id="0fd85-110">Aquesta versió té el número de compilació V 3.10.33.48 i està disponible de manera general a través d'una actualització automàtica el juny de 2020.</span><span class="sxs-lookup"><span data-stu-id="0fd85-110">This version has a build number of V 3.10.33.48 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-22"></a><span data-ttu-id="0fd85-111">Versió d'actualització 22</span><span class="sxs-lookup"><span data-stu-id="0fd85-111">Update Release 22</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="0fd85-112">Correccions d'errors</span><span class="sxs-lookup"><span data-stu-id="0fd85-112">Bug fixes</span></span>



<span data-ttu-id="0fd85-113">**Temps i despesa**</span><span class="sxs-lookup"><span data-stu-id="0fd85-113">**Time and Expense**</span></span>

<span data-ttu-id="0fd85-114">S'han corregit els problemes següents:</span><span class="sxs-lookup"><span data-stu-id="0fd85-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="0fd85-115">Les **Entrades de temps** no s'afegeixen automàticament a la planificació d'entrades de temps després de la importació.</span><span class="sxs-lookup"><span data-stu-id="0fd85-115">**Time entries** are not automatically added in the Time entries schedule after import.</span></span>
- <span data-ttu-id="0fd85-116">El selector de data de la quadrícula **Entrada de temps** no reconeix la configuració regional d'un usuari.</span><span class="sxs-lookup"><span data-stu-id="0fd85-116">The **Time Entry** grid date picker does not recognize a user's regional settings.</span></span>

<span data-ttu-id="0fd85-117">**Administració de recursos**</span><span class="sxs-lookup"><span data-stu-id="0fd85-117">**Resource Management**</span></span>

<span data-ttu-id="0fd85-118">S'han corregit els problemes següents:</span><span class="sxs-lookup"><span data-stu-id="0fd85-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="0fd85-119">Al mode manual, els canvis als contorns de l'opció **Assignació de recursos** no es reconeixen en generar **Requisits de recursos**.</span><span class="sxs-lookup"><span data-stu-id="0fd85-119">In manual mode, changes to **Resource Assignment** contours are not recognized when generating **Resource Requirements**.</span></span>
- <span data-ttu-id="0fd85-120">Les **Sol·licituds de recursos** no admeten els estats de sol·licituds personalitzades.</span><span class="sxs-lookup"><span data-stu-id="0fd85-120">**Resource Requests** do not support custom request statuses.</span></span>

<span data-ttu-id="0fd85-121">**Administració de projectes**</span><span class="sxs-lookup"><span data-stu-id="0fd85-121">**Project Management**</span></span>

<span data-ttu-id="0fd85-122">S'han corregit els problemes següents:</span><span class="sxs-lookup"><span data-stu-id="0fd85-122">The following issues have been fixed:</span></span>

- <span data-ttu-id="0fd85-123">L'ús del doble clic a EstimateGridControl no analitza correctament els números en format neerlandès.</span><span class="sxs-lookup"><span data-stu-id="0fd85-123">Using double-click on EstimateGridControl will not correctly parse Dutch format numbers.</span></span>
- <span data-ttu-id="0fd85-124">Les hores assignades no s'actualitzen correctament quan es canvien les assignacions mitjançant el complement del client d'escriptori del Microsoft Project.</span><span class="sxs-lookup"><span data-stu-id="0fd85-124">Assigned hours do not update correctly when assignments are changed using the Microsoft Project desktop client add-in.</span></span>
- <span data-ttu-id="0fd85-125">Les quadrícules Estimacions i Seguiment del projecte mostren un codi de moneda de vendes incorrecte quan la moneda del contracte és diferent de la moneda del client i l'organització està configurada per mostrar codis de moneda en comptes de símbols monetaris.</span><span class="sxs-lookup"><span data-stu-id="0fd85-125">Project Tracking and Estimates grids display incorrect sales currency code when contract currency is different than customer currency and organization is configured to display currency codes instead of currency symbols.</span></span>
- <span data-ttu-id="0fd85-126">La data de finalització d'un membre de l'equip afegirà un dia si la planificació d'hores de feina és de 24 hores al dia.</span><span class="sxs-lookup"><span data-stu-id="0fd85-126">A Team member's finish date will add one day if the work hour schedule is 24-hours per day.</span></span>
- <span data-ttu-id="0fd85-127">A la Planificació del projecte, si s'afegeix una Categoria de transacció a una tasca, no es dispara el desament automàtic.</span><span class="sxs-lookup"><span data-stu-id="0fd85-127">On the Project Schedule, adding a Transaction Category to a task does not trigger auto save.</span></span>
- <span data-ttu-id="0fd85-128">L'error següent es mostra quan s'afegeix un membre de l'equip a la Plantilla de projecte: "Els requisits de recursos no es poden associar amb plantilles de projecte".</span><span class="sxs-lookup"><span data-stu-id="0fd85-128">The following error is displayed when adding a team member to the Project Template: "Resource requirements cannot be associated with project templates".</span></span> 
- <span data-ttu-id="0fd85-129">L'script de la regla de la franja "msdyn.Approval.CanApproveOrReject" mostra un error del temps d'espera.</span><span class="sxs-lookup"><span data-stu-id="0fd85-129">Ribbon rule script "msdyn.Approval.CanApproveOrReject" displays a timeout error.</span></span>

<span data-ttu-id="0fd85-130">**Sales**</span><span class="sxs-lookup"><span data-stu-id="0fd85-130">**Sales**</span></span>

<span data-ttu-id="0fd85-131">S'han corregit els problemes següents:</span><span class="sxs-lookup"><span data-stu-id="0fd85-131">The following issues have been fixed:</span></span>

- <span data-ttu-id="0fd85-132">No es mostra el missatge d'error de validació quan se selecciona una Llista de preus de cost a la cerca Llista de preus al formulari o entitat "Nova llista de preus de projecte d'ofertes".</span><span class="sxs-lookup"><span data-stu-id="0fd85-132">Validation error message not displayed when a Cost Price List is selected in Price List lookup on 'New Quote Project Price List' form/entity.</span></span>
- <span data-ttu-id="0fd85-133">El tancament de l'oferta com a guanyada no dirigeix al contracte creat si un BPF adjunt a l'oferta és a la fase final.</span><span class="sxs-lookup"><span data-stu-id="0fd85-133">Closing the quote as won does not navigate to the created contract if a BPF attached to the quote is in the final stage.</span></span>
- <span data-ttu-id="0fd85-134">Revertir les **Vendes no facturades** s'enllaça al cost original quan es recupera una entrada de temps.</span><span class="sxs-lookup"><span data-stu-id="0fd85-134">Reversing **Unbilled Sales** is linked to original cost when a time entry is recalled.</span></span>
- <span data-ttu-id="0fd85-135">Després de seleccionar el botó **Confirma**, l'estat de la factura no canvia a **Confirmada** si no s'actualitza la factura.</span><span class="sxs-lookup"><span data-stu-id="0fd85-135">After selecting the **Confirm** button, the invoice status doesn't change to **Confirmed** unless the invoice is refreshed.</span></span>
