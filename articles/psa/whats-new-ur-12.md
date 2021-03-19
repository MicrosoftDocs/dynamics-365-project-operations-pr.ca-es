---
title: Novetats o canvis de la versió d'actualització 12 del Project Service Automation, V3
description: En aquest tema es proporciona informació sobre les novetats a la versió d'actualització 12 del Project Service Automation, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
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
ms.openlocfilehash: f1b2fdc37fa2c2e31537b89b7027d2833e905578
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5281061"
---
# <a name="project-service-automation-update-release-12-v3"></a><span data-ttu-id="f013e-103">Project Service Automation, versió d'actualització 12, V3</span><span class="sxs-lookup"><span data-stu-id="f013e-103">Project Service Automation Update Release 12, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="f013e-104">Ens complau anunciar la darrera actualització de l'aplicació Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="f013e-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="f013e-105">Aquesta versió inclou algunes millores importants per a la qualitat, el rendiment i la usabilitat.</span><span class="sxs-lookup"><span data-stu-id="f013e-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="f013e-106">Aquest llançament és compatible amb el Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="f013e-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="f013e-107">Per actualitzar a aquesta versió, visiteu el Centre d'administració del Dynamics 365 en línia i aneu a la pàgina de solucions per instal·lar l'actualització.</span><span class="sxs-lookup"><span data-stu-id="f013e-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="f013e-108">Per obtenir més informació, vegeu [Instal·lar, actualitzar o eliminar una solució preferida](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="f013e-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="f013e-109">En aquest tema es mostren les característiques i correccions que són noves o s'han canviat per al Project Service Automation V3, versió d'actualització 12.</span><span class="sxs-lookup"><span data-stu-id="f013e-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 12.</span></span> <span data-ttu-id="f013e-110">Aquesta versió té el número de compilació V3.10.2.34 i està disponible de forma general a través d'una actualització automàtica l'octubre de 2019.</span><span class="sxs-lookup"><span data-stu-id="f013e-110">This version has a build number of V3.10.2.34 and is generally available through a self-update in October 2019.</span></span>

## <a name="update-release-12"></a><span data-ttu-id="f013e-111">Versió d'actualització 12</span><span class="sxs-lookup"><span data-stu-id="f013e-111">Update Release 12</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="f013e-112">Correccions d'errors</span><span class="sxs-lookup"><span data-stu-id="f013e-112">Bug fixes</span></span>

- <span data-ttu-id="f013e-113">Temps i despesa</span><span class="sxs-lookup"><span data-stu-id="f013e-113">Time and Expense</span></span>

    - <span data-ttu-id="f013e-114">Correcció: s'ha actualitzat la missatgeria d'errors d'entrada de temps amb un context més rellevant.</span><span class="sxs-lookup"><span data-stu-id="f013e-114">Fixed: Time entry error messaging has been updated with more relevant context.</span></span>
    - <span data-ttu-id="f013e-115">Correcció: la quadrícula d'entrada de temps i la planificació mostren correctament la barra de desplaçament vertical quan cal.</span><span class="sxs-lookup"><span data-stu-id="f013e-115">Fixed: Time entry grid and schedule correctly displays the vertical scrollbar when required.</span></span>
    - <span data-ttu-id="f013e-116">Correcció: les entrades de despeses i temps enviades es poden aprovar.</span><span class="sxs-lookup"><span data-stu-id="f013e-116">Fixed: Submitted expense and time entries can be approved.</span></span>
    - <span data-ttu-id="f013e-117">Correcció: el missatge del diàleg de confirmació de cancel·lació de l'aprovació s'ha corregit per reflectir l'estat d'aprovació quan s'ha canviat d'**Aprovat** a **Enviat**.</span><span class="sxs-lookup"><span data-stu-id="f013e-117">Fixed: Cancel approval confirmation dialog message has been corrected to reflect the status of the approval when changed from **Approved** to **Submitted**.</span></span>
    - <span data-ttu-id="f013e-118">Correcció: els camps **Preu**, **Unitat** i **Quantitat** ara es bloquegen al registre Despesa després d'haver-se aprovat.</span><span class="sxs-lookup"><span data-stu-id="f013e-118">Fixed: **Price**, **Unit**, and **Quantity** fields are now locked on the Expense record after it is has been approved.</span></span>

- <span data-ttu-id="f013e-119">Administració de projectes</span><span class="sxs-lookup"><span data-stu-id="f013e-119">Project Management</span></span>

    - <span data-ttu-id="f013e-120">Correcció: s'ha suprimit l'acció **Nova** en el formulari principal **Membre de l'equip**.</span><span class="sxs-lookup"><span data-stu-id="f013e-120">Fixed: **New** action on **Team member** main form has been removed.</span></span>
    - <span data-ttu-id="f013e-121">Correcció: les assignacions de recursos s'ha actualitzat per tenir en compte errors d'arrodoniment inexactes que condueixen a un canvi de la data de finalització d'una tasca.</span><span class="sxs-lookup"><span data-stu-id="f013e-121">Fixed: Resource assignments have been updated to account for inaccurate rounding errors, which lead to a shift in a task’s end date.</span></span>
    - <span data-ttu-id="f013e-122">Correcció: a la quadrícula de tasques, els errors importants del servidor es mostraran a l'usuari.</span><span class="sxs-lookup"><span data-stu-id="f013e-122">Fixed: In the task grid, relevant server-side errors will be surfaced to the user.</span></span>
    - <span data-ttu-id="f013e-123">Correcció: el nom del membre de l'equip ara es mostra al selector de persones de la tasca en comptes del nom del càrrec.</span><span class="sxs-lookup"><span data-stu-id="f013e-123">Fixed: The team member’s name now renders in the task people picker instead of the position name.</span></span>

- <span data-ttu-id="f013e-124">Administració de recursos</span><span class="sxs-lookup"><span data-stu-id="f013e-124">Resource Management</span></span>

    - <span data-ttu-id="f013e-125">Correcció: els detalls dels requisits dels recursos dels projectes creats a partir d'una plantilla utilitzen ara el calendari del projecte.</span><span class="sxs-lookup"><span data-stu-id="f013e-125">Fixed: Resource requirement details for projects created from a template now use the project calendar.</span></span>
    - <span data-ttu-id="f013e-126">Correcció: les aptituds i les competències ara s'obtenen per defecte de les dades mestres de la funció al requisit del recurs creat per a aquesta funció.</span><span class="sxs-lookup"><span data-stu-id="f013e-126">Fixed: Skills and competencies now default from role master data to the resource requirement created for that role.</span></span>

- <span data-ttu-id="f013e-127">Sales</span><span class="sxs-lookup"><span data-stu-id="f013e-127">Sales</span></span>

    - <span data-ttu-id="f013e-128">Correcció: s'han trobat identificadors d'objecte duplicats trobats al formulari **Contracte principal**.</span><span class="sxs-lookup"><span data-stu-id="f013e-128">Fixed: Duplicate object IDs found on the **Contract main** form.</span></span>
    - <span data-ttu-id="f013e-129">Correcció: s'ha actualitzat la lògica per fer visible la pestanya **Anàlisi de l'oferta** perquè es visualitzi la configuració de les metadades de la pestanya.</span><span class="sxs-lookup"><span data-stu-id="f013e-129">Fixed: Logic has been updated to make the **Quote Analysis** tab visible so that it displays the metadata setup of the tab.</span></span>
    - <span data-ttu-id="f013e-130">Correcció: la data comptable en el registre actual prové de la data de l'entrada de temps o despesa i no la data de l'aprovació.</span><span class="sxs-lookup"><span data-stu-id="f013e-130">Fixed: Accounting date on the actual record now comes from the date of the time/expense entry date and not the date of the approval.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]