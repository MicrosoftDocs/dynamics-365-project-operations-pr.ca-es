---
title: Novetats o canvis de la versió d'actualització 30 del Project Service Automation, V3
description: En aquest tema es mostren les característiques i correccions disponibles al Project Service Automation V3, versió d'actualització 30.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 04/01/2021
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
ms.openlocfilehash: 1169ee13c42e982cb30a40d92df660f8933786a9
ms.sourcegitcommit: b4a05c7d5512d60abdb0d05bedd390e288e8adc9
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/02/2021
ms.locfileid: "5852831"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-30-v3"></a><span data-ttu-id="2a6e8-103">Novetats o canvis de la versió d'actualització 30 del Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="2a6e8-103">What's new or changed in Project Service Automation Update Release 30, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="2a6e8-104">Estem encantats d'anunciar-vos l'última actualització per a l'aplicació Project Service Automation per al Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="2a6e8-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="2a6e8-105">Aquesta versió inclou algunes millores importants per a la qualitat, el rendiment i la usabilitat.</span><span class="sxs-lookup"><span data-stu-id="2a6e8-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="2a6e8-106">Aquest llançament és compatible amb el Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="2a6e8-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="2a6e8-107">Per actualitzar a aquesta versió, visiteu el Centre d'administració del Dynamics 365 en línia i aneu a la pàgina de solucions per instal·lar l'actualització.</span><span class="sxs-lookup"><span data-stu-id="2a6e8-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="2a6e8-108">Per obtenir més informació, vegeu [Instal·lar, actualitzar o eliminar una solució preferida](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="2a6e8-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="2a6e8-109">En aquest tema es mostren les característiques i correccions que són noves o s'han canviat per al Project Service Automation V3, versió d'actualització 30.</span><span class="sxs-lookup"><span data-stu-id="2a6e8-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 30.</span></span> <span data-ttu-id="2a6e8-110">Aquesta versió té el número de compilació V3.10.51.61 i està disponible de manera general a través d'una actualització automàtica l'abril de 2021.</span><span class="sxs-lookup"><span data-stu-id="2a6e8-110">This version has a build number of V3.10.51.61 and is generally available through a self-update in April 2021.</span></span>

## <a name="update-release-30"></a><span data-ttu-id="2a6e8-111">Versió d'actualització 30</span><span class="sxs-lookup"><span data-stu-id="2a6e8-111">Update Release 30</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="2a6e8-112">Correccions d'errors</span><span class="sxs-lookup"><span data-stu-id="2a6e8-112">Bug fixes</span></span>

<span data-ttu-id="2a6e8-113">**Temps i despesa**</span><span class="sxs-lookup"><span data-stu-id="2a6e8-113">**Time and Expense**</span></span>

<span data-ttu-id="2a6e8-114">S'han corregit els problemes següents:</span><span class="sxs-lookup"><span data-stu-id="2a6e8-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="2a6e8-115">Es produeix un error quan creeu i deseu una entrada de temps a la pàgina **Creació ràpida** si el camp **Funció** s'elimina.</span><span class="sxs-lookup"><span data-stu-id="2a6e8-115">An error occurs when you create and save a time entry on the **Quick Create** page if the **Role** field is removed.</span></span>
- <span data-ttu-id="2a6e8-116">El filtre Entrada de temps aplica l'operador de filtre erroni.</span><span class="sxs-lookup"><span data-stu-id="2a6e8-116">The Time Entry filter applies the wrong filter operator.</span></span>
- <span data-ttu-id="2a6e8-117">Els fulls de temps copiats no es visualitzen automàticament quan seleccioneu **Copia la setmana** al control d'entrada de l'hora.</span><span class="sxs-lookup"><span data-stu-id="2a6e8-117">Copied timesheets aren't automatically displayed when you select **Copy Week** on the time entry control.</span></span>

<span data-ttu-id="2a6e8-118">**Administració de recursos**</span><span class="sxs-lookup"><span data-stu-id="2a6e8-118">**Resource Management**</span></span>

<span data-ttu-id="2a6e8-119">S'han corregit els problemes següents:</span><span class="sxs-lookup"><span data-stu-id="2a6e8-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="2a6e8-120">Quan amplieu una reserva, l'estat de la reserva assignat a la reserva ferma no és correcte.</span><span class="sxs-lookup"><span data-stu-id="2a6e8-120">When you extend a booking, the booking status assigned to the hard booking is incorrect.</span></span> <span data-ttu-id="2a6e8-121">L'extensió d'una reserva respecta l'estat de la reserva definit com a **Compromès** a les metadades de configuració de la reserva.</span><span class="sxs-lookup"><span data-stu-id="2a6e8-121">Extending a booking respects the booking status defined as **Committed** in the booking setup metadata.</span></span>
- <span data-ttu-id="2a6e8-122">Quan no s'especifica un estat de reserva vàlid, el missatge d'error no es localitza correctament.</span><span class="sxs-lookup"><span data-stu-id="2a6e8-122">When a valid booking status isn't specified, the error message is not correctly localized.</span></span>

<span data-ttu-id="2a6e8-123">**Administració de projectes**</span><span class="sxs-lookup"><span data-stu-id="2a6e8-123">**Project Management**</span></span>

<span data-ttu-id="2a6e8-124">S'han corregit els problemes següents:</span><span class="sxs-lookup"><span data-stu-id="2a6e8-124">The following issues have been fixed:</span></span>

- <span data-ttu-id="2a6e8-125">Els projectes no es poden crear en una moneda i incloure-hi tasques relacionades en una altra moneda.</span><span class="sxs-lookup"><span data-stu-id="2a6e8-125">Projects can't be created in one currency and include related tasks in another currency.</span></span>

<span data-ttu-id="2a6e8-126">**Vendes**</span><span class="sxs-lookup"><span data-stu-id="2a6e8-126">**Sales**</span></span>

<span data-ttu-id="2a6e8-127">S'han corregit els problemes següents:</span><span class="sxs-lookup"><span data-stu-id="2a6e8-127">The following issues have been fixed:</span></span>

- <span data-ttu-id="2a6e8-128">Quan es copia una llista de preus, els preus no s'actualitzen.</span><span class="sxs-lookup"><span data-stu-id="2a6e8-128">When a price list is copied, prices aren't updated.</span></span>
- <span data-ttu-id="2a6e8-129">El tancament d'una oferta com a guanyada falla quan el detall del cost té un valor d'origen.</span><span class="sxs-lookup"><span data-stu-id="2a6e8-129">Closing a quote as won fails when the cost detail has a value for origin.</span></span>
- <span data-ttu-id="2a6e8-130">A l'entitat **Tasca de projecte**, el **Cost previst** s'ha canviat a **Cost previst (base)**.</span><span class="sxs-lookup"><span data-stu-id="2a6e8-130">On the **Project Task** entity, **Estimated Cost** has been renamed to **Planned Cost (Base)**.</span></span>
- <span data-ttu-id="2a6e8-131">Es genera una excepció de referència nul·la quan es creen o se suprimeixen factures.</span><span class="sxs-lookup"><span data-stu-id="2a6e8-131">A null reference exception is generated when invoices are created or deleted.</span></span>
