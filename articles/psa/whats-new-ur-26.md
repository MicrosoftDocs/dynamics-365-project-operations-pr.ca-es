---
title: Novetats o canvis de la versió d'actualització 26 del Project Service Automation, V3
description: En aquest tema es mostren les característiques i correccions disponibles al Project Service Automation V3, versió d'actualització 26.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/12/2021
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
ms.openlocfilehash: 14fcccf5804e5da0926dbc69bdfa040229a7f068
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "5143546"
---
# <a name="project-service-automation-update-release-26-v3"></a><span data-ttu-id="d1fc2-103">Project Service Automation, versió d'actualització 26, V3</span><span class="sxs-lookup"><span data-stu-id="d1fc2-103">Project Service Automation Update Release 26, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="d1fc2-104">Estem encantats d'anunciar-vos l'última actualització per a l'aplicació Project Service Automation per al Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="d1fc2-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="d1fc2-105">Aquesta versió inclou algunes millores importants per a la qualitat, el rendiment i la usabilitat.</span><span class="sxs-lookup"><span data-stu-id="d1fc2-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="d1fc2-106">Aquest llançament és compatible amb el Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="d1fc2-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="d1fc2-107">Per actualitzar a aquesta versió, visiteu el Centre d'administració del Dynamics 365 en línia i aneu a la pàgina de solucions per instal·lar l'actualització.</span><span class="sxs-lookup"><span data-stu-id="d1fc2-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="d1fc2-108">Per obtenir més informació, vegeu [Instal·lar, actualitzar o eliminar una solució preferida](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="d1fc2-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="d1fc2-109">En aquest tema es mostren les característiques i correccions que són noves o s'han canviat per al llançament de l'actualització 26, V3, de Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="d1fc2-109">This topic lists the features and fixes that are new or changed for Project Service Automation Update Release 26, V3.</span></span> <span data-ttu-id="d1fc2-110">Aquesta versió té un número de compilació de V3.10.44.59 i està disponible de manera general a través d'una actualització d'autoservei al desembre de 2020.</span><span class="sxs-lookup"><span data-stu-id="d1fc2-110">This version has a build number of V3.10.44.59 and is generally available through a self-update in December 2020.</span></span>

## <a name="update-release-26"></a><span data-ttu-id="d1fc2-111">Versió d'actualització 26</span><span class="sxs-lookup"><span data-stu-id="d1fc2-111">Update Release 26</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="d1fc2-112">Correccions d'errors</span><span class="sxs-lookup"><span data-stu-id="d1fc2-112">Bug fixes</span></span>

<span data-ttu-id="d1fc2-113">**Temps i despesa**</span><span class="sxs-lookup"><span data-stu-id="d1fc2-113">**Time and Expense**</span></span>

<span data-ttu-id="d1fc2-114">S'han corregit els problemes següents:</span><span class="sxs-lookup"><span data-stu-id="d1fc2-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="d1fc2-115">Els usuaris poden canviar la tasca en un registre de temps que s'ha aprovat o enviat.</span><span class="sxs-lookup"><span data-stu-id="d1fc2-115">Users are able to change the task on a time entry that has been approved/submitted.</span></span>
- <span data-ttu-id="d1fc2-116">Error "referència d'objecte no definida" en desar una entrada de temps.</span><span class="sxs-lookup"><span data-stu-id="d1fc2-116">"Object Reference Not Set" error when saving time entry.</span></span>
- <span data-ttu-id="d1fc2-117">La importació d'entrades de temps a partir de les assignacions de recursos crea anotacions de temps amb valors de data i hora incorrectes.</span><span class="sxs-lookup"><span data-stu-id="d1fc2-117">Time entry import from resource assignments creates time entries with the incorrect DateTime values.</span></span>
- <span data-ttu-id="d1fc2-118">Quan Project Service Automation i l'aplicació Field Service estan instal·lats, el botó **Nou** es visualitza dues vegades a la barra d'ordres per a les entrades de temps a l'aplicació Field Service.</span><span class="sxs-lookup"><span data-stu-id="d1fc2-118">When Project Service Automation and the Field Service app are both installed, the **New** button is displaying twice on the command bar for time entries in the Field Service app.</span></span>
- <span data-ttu-id="d1fc2-119">Les actualitzacions a les cel·les **Permet unitat** i **Grup d'unitats** ara es fan a la quadrícula **Estimacions de despesa**.</span><span class="sxs-lookup"><span data-stu-id="d1fc2-119">**Allow Unit** and **Unit group** cells updates now work on the **Expense Estimates** grid.</span></span>
- <span data-ttu-id="d1fc2-120">El formulari **Actualitza l'edició de l'entrada de temps** inclou **Cronologia**.</span><span class="sxs-lookup"><span data-stu-id="d1fc2-120">**Update Time Entry Edit** form includes **Timeline**.</span></span>
- <span data-ttu-id="d1fc2-121">L'aprovació de temps per a les entrades de temps que no són del projecte bloqueja el sistema en cercar una funció d'aprovador de projecte.</span><span class="sxs-lookup"><span data-stu-id="d1fc2-121">Time approval for non-project time entries blocks the system when searching for a project approver role.</span></span>

<span data-ttu-id="d1fc2-122">**Administració de recursos**</span><span class="sxs-lookup"><span data-stu-id="d1fc2-122">**Resource Management**</span></span>

<span data-ttu-id="d1fc2-123">S'han corregit els problemes següents:</span><span class="sxs-lookup"><span data-stu-id="d1fc2-123">The following issues have been fixed:</span></span>

- <span data-ttu-id="d1fc2-124">S'ha afegit la validació al complement **PostProjectCreate** per comprovar si es compleix un requisit principal abans de crear-ne un.</span><span class="sxs-lookup"><span data-stu-id="d1fc2-124">Added validation in the **PostProjectCreate** plug-in to check for a primary requirement before creating one.</span></span>
- <span data-ttu-id="d1fc2-125">El formulari de creació ràpida **Membre de l'equip de projecte** llança una excepció de referència nul·la si els camps se suprimeixen del formulari.</span><span class="sxs-lookup"><span data-stu-id="d1fc2-125">**Project Team Member** quick create form throws a null reference exception if fields are removed from the form.</span></span>
- <span data-ttu-id="d1fc2-126">Els requisits generació de 12 hores a partir d'1 any fallaran.</span><span class="sxs-lookup"><span data-stu-id="d1fc2-126">Generate requirements for 12 hours over 1 year will fail.</span></span>
- <span data-ttu-id="d1fc2-127">S'ha millorat el missatge d'error d'excepció de referència nul·la durant la creació de requisits de recursos.</span><span class="sxs-lookup"><span data-stu-id="d1fc2-127">Improved error message null reference exception during resource requirement creation.</span></span>

<span data-ttu-id="d1fc2-128">**Administració de projectes**</span><span class="sxs-lookup"><span data-stu-id="d1fc2-128">**Project Management**</span></span>

<span data-ttu-id="d1fc2-129">S'han corregit els problemes següents:</span><span class="sxs-lookup"><span data-stu-id="d1fc2-129">The following issues have been fixed:</span></span>

- <span data-ttu-id="d1fc2-130">S'ha millorat la validació per tractar l'excepció de referència nul·la generada en el complement **PreProjectUpdate**.</span><span class="sxs-lookup"><span data-stu-id="d1fc2-130">Improved validation to address null reference exception generated in the **PreProjectUpdate** plug-in.</span></span>
- <span data-ttu-id="d1fc2-131">Els projectes publicats pel complement de l'escriptori de Microsoft Project suprimeixen assignacions no assignades.</span><span class="sxs-lookup"><span data-stu-id="d1fc2-131">Projects published by the Microsoft Project desktop add-in delete unassigned assignments.</span></span>
- <span data-ttu-id="d1fc2-132">S'ha afegit una validació nova quan la referència del projecte d'una tasca no és vàlida a causa d'una excepció de referència nul·la a **PreValidateProjectTaskUpdate**.</span><span class="sxs-lookup"><span data-stu-id="d1fc2-132">Added new validation when a task’s project reference is invalid due to null reference exception in **PreValidateProjectTaskUpdate** plug-in.</span></span>
- <span data-ttu-id="d1fc2-133">La quadrícula Membres de l'equip no mostra les assignacions diferents del registre dels membres de l'equip.</span><span class="sxs-lookup"><span data-stu-id="d1fc2-133">Team Member grid does not show distinct assignments on the team member record.</span></span>
- <span data-ttu-id="d1fc2-134">S'han afegit nous missatges de validació i d'error a causa de l'excepció de referència nul·la en el complement **PreProjectTaskDelete**.</span><span class="sxs-lookup"><span data-stu-id="d1fc2-134">Added new validation and error messages due to null reference exception in **PreProjectTaskDelete** plug-in.</span></span>

<span data-ttu-id="d1fc2-135">**Sales**</span><span class="sxs-lookup"><span data-stu-id="d1fc2-135">**Sales**</span></span>

<span data-ttu-id="d1fc2-136">S'han corregit els problemes següents:</span><span class="sxs-lookup"><span data-stu-id="d1fc2-136">The following issues have been fixed:</span></span>

- <span data-ttu-id="d1fc2-137">Quan seleccioneu una línia basada en projectes a l'oferta o el contracte, el botó **Suggeriment** només hauria de ser visible en seleccionar una línia basada en productes associada amb un producte existent.</span><span class="sxs-lookup"><span data-stu-id="d1fc2-137">When selecting a project-based line in quote or contract, the **Suggestion** button should only be visible when selecting a product-based line associated with an existing product.</span></span>
- <span data-ttu-id="d1fc2-138">Dividiu el privilegi **Create_Product** del privilegi **Create_ProjectContract**.</span><span class="sxs-lookup"><span data-stu-id="d1fc2-138">Split **Create_Product** privilege from **Create_ProjectContract** privilege.</span></span>
- <span data-ttu-id="d1fc2-139">La supressió d'una línia de factura provoca un error de referència nul·la a **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span><span class="sxs-lookup"><span data-stu-id="d1fc2-139">Deleting an invoice line causes null reference failure on **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span></span>
