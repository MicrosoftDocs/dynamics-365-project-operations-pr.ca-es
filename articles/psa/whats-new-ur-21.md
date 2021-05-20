---
title: Novetats o canvis de la versió d'actualització 21 del Project Service Automation, V3
description: En aquest tema es mostren les característiques i correccions disponibles al Project Service Automation V3, versió d'actualització 21.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 06/19/2020
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
ms.openlocfilehash: ad44f6747486222cc1f48c7b645f2525d382dca3
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949037"
---
# <a name="project-service-automation-update-release-21-v3"></a><span data-ttu-id="048e5-103">Project Service Automation, versió d'actualització 21, V3</span><span class="sxs-lookup"><span data-stu-id="048e5-103">Project Service Automation Update Release 21, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="048e5-104">Estem encantats d'anunciar-vos l'última actualització per a l'aplicació Project Service Automation per al Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="048e5-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="048e5-105">Aquesta versió inclou algunes millores importants per a la qualitat, el rendiment i la usabilitat.</span><span class="sxs-lookup"><span data-stu-id="048e5-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="048e5-106">Aquest llançament és compatible amb el Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="048e5-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="048e5-107">Per actualitzar a aquesta versió, visiteu el Centre d'administració del Dynamics 365 en línia i aneu a la pàgina de solucions per instal·lar l'actualització.</span><span class="sxs-lookup"><span data-stu-id="048e5-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="048e5-108">Per obtenir més informació, vegeu [Instal·lar, actualitzar o eliminar una solució preferida](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="048e5-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="048e5-109">En aquest tema es mostren les característiques i correccions que són noves o s'han canviat per al Project Service Automation V3, versió d'actualització 21.</span><span class="sxs-lookup"><span data-stu-id="048e5-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 21.</span></span> <span data-ttu-id="048e5-110">Aquesta versió té el número de compilació V 3.10.32.50 i està disponible de manera general a través d'una actualització automàtica el juny de 2020.</span><span class="sxs-lookup"><span data-stu-id="048e5-110">This version has a build number of V 3.10.32.50 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-21"></a><span data-ttu-id="048e5-111">Versió d'actualització 21</span><span class="sxs-lookup"><span data-stu-id="048e5-111">Update Release 21</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="048e5-112">Correccions d'errors</span><span class="sxs-lookup"><span data-stu-id="048e5-112">Bug fixes</span></span>

<span data-ttu-id="048e5-113">**Temps i despesa**</span><span class="sxs-lookup"><span data-stu-id="048e5-113">**Time and Expense**</span></span>

<span data-ttu-id="048e5-114">S'han corregit els problemes següents:</span><span class="sxs-lookup"><span data-stu-id="048e5-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="048e5-115">En allotjar el **control de quadrícula Entrada de temps** als escriptoris digitals, la quadrícula no utilitza l'amplada completa del contenidor de quadrícula d'escriptoris digitals.</span><span class="sxs-lookup"><span data-stu-id="048e5-115">When hosting the **Time Entry Grid Control** in Dashboards, the grid does not utilize the full width of the dashboard grid container.</span></span>
- <span data-ttu-id="048e5-116">En fusos horaris específiques, el control de quadrícula **Entrada de temps** no mostra registres.</span><span class="sxs-lookup"><span data-stu-id="048e5-116">For specific time zones, the **Time Entry** grid control does not display records.</span></span>
- <span data-ttu-id="048e5-117">Les entrades de temps posteriors a les 21:00 apareixen en un dia incorrecte.</span><span class="sxs-lookup"><span data-stu-id="048e5-117">Time entries that are after 9:00 PM appear on the wrong day.</span></span>
- <span data-ttu-id="048e5-118">Els usuaris no poden enviar despeses si la categoria de despesa **Rebut de despesa obligatori** no té cap valor.</span><span class="sxs-lookup"><span data-stu-id="048e5-118">Users are unable to submit expenses if the expense category, **Expense receipt required** has no value.</span></span>

<span data-ttu-id="048e5-119">**Administració de recursos**</span><span class="sxs-lookup"><span data-stu-id="048e5-119">**Resource Management**</span></span>

<span data-ttu-id="048e5-120">S'han corregit els problemes següents:</span><span class="sxs-lookup"><span data-stu-id="048e5-120">The following issues have been fixed:</span></span>

- <span data-ttu-id="048e5-121">Les reserves inactives es mostren a la visualització **Conciliació**.</span><span class="sxs-lookup"><span data-stu-id="048e5-121">Inactive bookings are displayed in the **Reconciliation** view.</span></span>
- <span data-ttu-id="048e5-122">Faltava la validació a la gestió de recursos genèrics per garantir que existeixi un estat de reserva vàlid.</span><span class="sxs-lookup"><span data-stu-id="048e5-122">Generic resource fulfillment was missing validation to ensure that a valid booking status exists.</span></span>

<span data-ttu-id="048e5-123">**Administració de projectes**</span><span class="sxs-lookup"><span data-stu-id="048e5-123">**Project Management**</span></span>

<span data-ttu-id="048e5-124">S'han corregit els problemes següents:</span><span class="sxs-lookup"><span data-stu-id="048e5-124">The following issues have been fixed:</span></span>

- <span data-ttu-id="048e5-125">Les quadrícules del formulari **Projecte** (**Assignació de recursos**, **Tasca**, visualització **Conciliació** i **Estimacions de despeses**) es poden continuar editant fins i tot quan un projecte no està actiu.</span><span class="sxs-lookup"><span data-stu-id="048e5-125">The **Project** form grids (**Resource Assignment**, **Task**, **Reconciliation** view, **Expense Estimates**) remain editable even when a project is not active.</span></span>
- <span data-ttu-id="048e5-126">Els clients duplicats no es poden combinar amb els clients enllaçats a contractes de projectes confirmats.</span><span class="sxs-lookup"><span data-stu-id="048e5-126">Duplicate customers can't be merged with customers that are linked to confirmed project contracts.</span></span>
- <span data-ttu-id="048e5-127">Quan s'afegeix un recurs que no té cap calendari vàlid, el sistema no torna un missatge d'error descriptiu a l'usuari.</span><span class="sxs-lookup"><span data-stu-id="048e5-127">When a resource who does not have a valid calendar is added, the system does not return a user friendly-error message.</span></span>
- <span data-ttu-id="048e5-128">El botó **Afegeix una tasca** de la quadrícula de tasques està habilitat quan el projecte està enllaçat amb el **complement del Microsoft Project**.</span><span class="sxs-lookup"><span data-stu-id="048e5-128">The **Add Task** button on the task grid is enabled when the project is linked to **Microsoft Project add-in**.</span></span>
- <span data-ttu-id="048e5-129">L'esforç creix de manera incontrolable quan s'assigna una tasca amb una categoria a un recurs amb una funció per a la qual hi ha un preu de cost definit.</span><span class="sxs-lookup"><span data-stu-id="048e5-129">Effort grows uncontrollably when a task with a category is assigned to a resource with a role for which there is a cost price defined.</span></span>

<span data-ttu-id="048e5-130">**Sales**</span><span class="sxs-lookup"><span data-stu-id="048e5-130">**Sales**</span></span>

<span data-ttu-id="048e5-131">S'han realitzat les millores següents:</span><span class="sxs-lookup"><span data-stu-id="048e5-131">The following enhancements have been made:</span></span>

- <span data-ttu-id="048e5-132">S'han desplaçat **Freqüència de facturació** i **Inici de facturació** a la pestanya **Planificació de facturació**.</span><span class="sxs-lookup"><span data-stu-id="048e5-132">**Invoice Frequency** and **Billing Start** have been moved to the **Invoice Schedule** tab.</span></span>

<span data-ttu-id="048e5-133">S'han corregit els problemes següents:</span><span class="sxs-lookup"><span data-stu-id="048e5-133">The following issues have been fixed:</span></span>

- <span data-ttu-id="048e5-134">El **Preu de venda total** és zero (0) per a la **Categoria** encara que la **Funció** tingui un preu de venda total que no és zero.</span><span class="sxs-lookup"><span data-stu-id="048e5-134">**Total Sales Price** is zero (0) for **Category** even though **Role** has a total sales price that is not zero.</span></span>
- <span data-ttu-id="048e5-135">Els clients no poden canviar el valor del camp **Estat de la factura** a **Preparat per a la facturació** quan un altre procés personalitzat actualitza un camp addicional.</span><span class="sxs-lookup"><span data-stu-id="048e5-135">Customers can't change the value of the **Invoice Status** field to **Ready for invoicing** when another customized process is updating an additional field.</span></span>
- <span data-ttu-id="048e5-136">El botó **Actualitza les línies de factura** pot crear diverses línies duplicades si se selecciona repetidament.</span><span class="sxs-lookup"><span data-stu-id="048e5-136">The **Refresh Invoice Lines** button can create multiple duplicated lines if it is repeatedly selected.</span></span>
- <span data-ttu-id="048e5-137">El botó **Actualitza els preus** no funciona a la subquadrícula **Preus per funció** del formulari **Visualització ràpida**.</span><span class="sxs-lookup"><span data-stu-id="048e5-137">The **Update Prices** button doesn't work on the **Role Prices** subgrid in the **Quick View** form.</span></span>
- <span data-ttu-id="048e5-138">La lògica **Resolució de llistes de preus de vendes** gestiona incorrectament els fusos horaris, la qual cosa deriva en la selecció incorrecta de les llistes de preus.</span><span class="sxs-lookup"><span data-stu-id="048e5-138">The **Sales Price List Resolution** logic improperly handles time zones, resulting in the incorrect selection of price lists.</span></span>
- <span data-ttu-id="048e5-139">El **Cost real total** d'un projecte pot estar rebaixat per un import fraccionat després d'aprovar una sola entrada de temps.</span><span class="sxs-lookup"><span data-stu-id="048e5-139">A project’s **Total Actual Cost** can be off by a fractional amount after a single time entry is approved.</span></span>
- <span data-ttu-id="048e5-140">La lògica **Resolució de preus** no proporciona cap missatge d'error descriptiu a l'usuari si **RolePrice recuperat** no té valors als camps **"Unitat principal"** i **"Preu a la unitat principal"**.</span><span class="sxs-lookup"><span data-stu-id="048e5-140">The **Price Resolution** logic does not provide a user-friendly error message if **Retrieved RolePrice** doesn't have values in **'Primary Unit'** and **'Price In Primary Unit'** fields.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]