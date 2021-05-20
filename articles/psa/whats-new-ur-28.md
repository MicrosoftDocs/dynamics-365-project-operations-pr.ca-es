---
title: Novetats o canvis de la versió d'actualització 28 del Project Service Automation, V3
description: En aquest tema es mostren les característiques i correccions disponibles al Project Service Automation V3, versió d'actualització 28.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/26/2021
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
ms.openlocfilehash: 2d5e8c629f8108ed039948ca70842c9d8afebfa6
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948655"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-28-v3"></a><span data-ttu-id="d22e8-103">Novetats o canvis de la versió d'actualització 28 del Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="d22e8-103">What's new or changed in Project Service Automation Update Release 28, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="d22e8-104">Estem encantats d'anunciar-vos l'última actualització per a l'aplicació Project Service Automation per al Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="d22e8-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="d22e8-105">Aquesta versió inclou algunes millores importants per a la qualitat, el rendiment i la usabilitat.</span><span class="sxs-lookup"><span data-stu-id="d22e8-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="d22e8-106">Aquest llançament és compatible amb el Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="d22e8-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="d22e8-107">Per actualitzar a aquesta versió, visiteu el Centre d'administració del Dynamics 365 en línia i aneu a la pàgina de solucions per instal·lar l'actualització.</span><span class="sxs-lookup"><span data-stu-id="d22e8-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="d22e8-108">Per obtenir més informació, vegeu [Instal·lar, actualitzar o eliminar una solució preferida](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="d22e8-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="d22e8-109">Aquest tema enumera les característiques i correccions noves o canviades per al Project Service Automation V3, llançament d'actualització 28 Aquesta versió té el número de compilació V3.10.46.32 i està disponible de manera general a través d'una actualització autoservei el gener de 2021.</span><span class="sxs-lookup"><span data-stu-id="d22e8-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 28 This version has a build number of V3.10.46.32 and is generally available through a self-update in January 2021.</span></span>

## <a name="update-release-28"></a><span data-ttu-id="d22e8-110">Versió d'actualització 28</span><span class="sxs-lookup"><span data-stu-id="d22e8-110">Update Release 28</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="d22e8-111">Correccions d'errors</span><span class="sxs-lookup"><span data-stu-id="d22e8-111">Bug fixes</span></span>

<span data-ttu-id="d22e8-112">**Temps i despesa**</span><span class="sxs-lookup"><span data-stu-id="d22e8-112">**Time and Expense**</span></span>

<span data-ttu-id="d22e8-113">S'han corregit els problemes següents:</span><span class="sxs-lookup"><span data-stu-id="d22e8-113">The following issues have been fixed:</span></span>

- <span data-ttu-id="d22e8-114">Els usuaris poden utilitzar **Edició massiva** per actualitzar entrades de temps que s'han aprovat i enviat.</span><span class="sxs-lookup"><span data-stu-id="d22e8-114">Users can use **Bulk Edit** to update time entries that have been approved and submitted.</span></span>

<span data-ttu-id="d22e8-115">**Administració de projectes**</span><span class="sxs-lookup"><span data-stu-id="d22e8-115">**Project Management**</span></span>

<span data-ttu-id="d22e8-116">S'han corregit els problemes següents:</span><span class="sxs-lookup"><span data-stu-id="d22e8-116">The following issues have been fixed:</span></span>

- <span data-ttu-id="d22e8-117">En els casos en què el GUID de la tasca s'interpreta com un nombre, les tasques no es poden obrir per editar-les mitjançant **Edita la tasca** a la franja de la pàgina **Estructura del desglossament del treball**.</span><span class="sxs-lookup"><span data-stu-id="d22e8-117">In cases where the task GUID is interpreted as a number, tasks can't be opened for edit using **Edit Task** in the ribbon on the **Work Breakdown Structure** page.</span></span>

<span data-ttu-id="d22e8-118">**Sales**</span><span class="sxs-lookup"><span data-stu-id="d22e8-118">**Sales**</span></span>

<span data-ttu-id="d22e8-119">S'han corregit els problemes següents:</span><span class="sxs-lookup"><span data-stu-id="d22e8-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="d22e8-120">Es genera una excepció de referència nul·la quan s'invoca el complement **GetEstimatesForProject**.</span><span class="sxs-lookup"><span data-stu-id="d22e8-120">A null reference exception is generated when the **GetEstimatesForProject** plug-in is invoked.</span></span>
- <span data-ttu-id="d22e8-121">**Marca a punt per facturar** a la quadrícula de fites només actualitza parcialment els atributs, excepte l'atribut **InvoiceStatus**, que s'actualitza.</span><span class="sxs-lookup"><span data-stu-id="d22e8-121">**Mark ready to invoice** on the milestone grid only partially updates attributes, except for the **InvoiceStatus** attribute, which is updated.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]