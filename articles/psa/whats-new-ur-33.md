---
title: Novetats o canvis de la versió d'actualització 33 del Project Service Automation, V3
description: En aquest tema es mostren les característiques i correccions disponibles al Project Service Automation V3, versió d'actualització 33.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/30/2021
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
ms.openlocfilehash: 2c96e4abd484bb66285421baaad82ead9589bbe9
ms.sourcegitcommit: be5beba71ee9770c0083b4fe5cc89e7ec6b741b8
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334506"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-33-v3"></a><span data-ttu-id="8cf39-103">Novetats o canvis de la versió d'actualització 33 del Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="8cf39-103">What's new or changed in Project Service Automation Update Release 33, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="8cf39-104">Ens complau anunciar l'última actualització de l'aplicació Microsoft Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="8cf39-104">We're pleased to announce the latest update for the Microsoft Dynamics 365 Project Service Automation app.</span></span> <span data-ttu-id="8cf39-105">Aquesta versió inclou algunes millores importants per a la qualitat, el rendiment i la usabilitat.</span><span class="sxs-lookup"><span data-stu-id="8cf39-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="8cf39-106">És compatible amb el Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="8cf39-106">It's compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="8cf39-107">Per actualitzar aquesta versió, visiteu la pàgina de solucions en línia del Centre d'administració del Dynamics 365 i instal·leu l'actualització.</span><span class="sxs-lookup"><span data-stu-id="8cf39-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page, and install the update.</span></span> <span data-ttu-id="8cf39-108">Per obtenir més informació, vegeu [Instal·lar, actualitzar o eliminar una solució preferida](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="8cf39-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="8cf39-109">En aquest tema es mostren les característiques i correccions que són noves o s'han canviat per al Project Service Automation V3, versió d'actualització 33.</span><span class="sxs-lookup"><span data-stu-id="8cf39-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 33.</span></span> <span data-ttu-id="8cf39-110">Aquesta versió té el número de versió V3.10.54.98 i està disponible de forma general mitjançant una autoactualització el juliol de 2021.</span><span class="sxs-lookup"><span data-stu-id="8cf39-110">This version has a build number of V3.10.54.98 and is generally available through a self-update in July 2021.</span></span>

## <a name="update-release-33"></a><span data-ttu-id="8cf39-111">Versió d'actualització 33</span><span class="sxs-lookup"><span data-stu-id="8cf39-111">Update Release 33</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="8cf39-112">Correccions d'errors</span><span class="sxs-lookup"><span data-stu-id="8cf39-112">Bug fixes</span></span>

<span data-ttu-id="8cf39-113">**Temps i despesa**</span><span class="sxs-lookup"><span data-stu-id="8cf39-113">**Time and Expense**</span></span>

<span data-ttu-id="8cf39-114">S'han corregit els problemes següents:</span><span class="sxs-lookup"><span data-stu-id="8cf39-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="8cf39-115">Dos camps bloquejats, **msdyn_description** i **msdyn_externaldescription** es poden editar després de l'enviament.</span><span class="sxs-lookup"><span data-stu-id="8cf39-115">Two locked fields, **msdyn_description** and **msdyn_externaldescription** are editable after submission.</span></span>
- <span data-ttu-id="8cf39-116">Es mostra un missatge d'error si es crea una despesa que no està relacionada amb un projecte.</span><span class="sxs-lookup"><span data-stu-id="8cf39-116">An error message occurs if an expense is created that isn't related to a project.</span></span>
- <span data-ttu-id="8cf39-117">Quan es crea una entrada d'hora, la funció del recurs canvia per defecte a una funció inactiva.</span><span class="sxs-lookup"><span data-stu-id="8cf39-117">When a time entry is created, the resource role defaults to an inactive role.</span></span>
- <span data-ttu-id="8cf39-118">Les línies del llibre diari associades a una despesa recuperada i suprimida no s'eliminen.</span><span class="sxs-lookup"><span data-stu-id="8cf39-118">Journal lines associated with a recalled and deleted expense aren't deleted.</span></span>
- <span data-ttu-id="8cf39-119">Al **Formulari de creació ràpida d'entrades de temps**, actualitzeu la visualització **Llista de tasques del projecte** per canviar la data visualitzada per defecte com a data d'inici de la tasca.</span><span class="sxs-lookup"><span data-stu-id="8cf39-119">On the **Time entry Quick Create Form**, update the **Project Task List** view to change the date displayed by default to the start date of the task.</span></span>
- <span data-ttu-id="8cf39-120">Quan creeu una entrada de temps des de la pestanya **Relacionat** del recurs que es pot reservar, l'entrada de temps no es crea correctament per a l'usuari que ha iniciat la sessió en comptes del recurs principal que es pot reservar.</span><span class="sxs-lookup"><span data-stu-id="8cf39-120">When you create a time entry from the **Related** tab of the bookable resource, the time entry is incorrectly created for the signed-in user instead of the parent bookable resource.</span></span>
- <span data-ttu-id="8cf39-121">S'afegeixen camps nous al quadre de diàleg **MDD d'aprovació massiva**.</span><span class="sxs-lookup"><span data-stu-id="8cf39-121">New fields are added to the **Bulk approval MDD** dialog box.</span></span>

<span data-ttu-id="8cf39-122">**Planificació del projecte**</span><span class="sxs-lookup"><span data-stu-id="8cf39-122">**Project planning**</span></span>

<span data-ttu-id="8cf39-123">S'han corregit els problemes següents:</span><span class="sxs-lookup"><span data-stu-id="8cf39-123">The following issues have been fixed:</span></span>
- <span data-ttu-id="8cf39-124">El rendiment de creació de projectes s'alenteix quan les plantilles d'hores de feina del projecte s'apliquen a calendaris complexos.</span><span class="sxs-lookup"><span data-stu-id="8cf39-124">Slow project creation performance when project work hour templates are applied with complex calendars.</span></span>
- <span data-ttu-id="8cf39-125">Quan la data d'inici és posterior a la data de finalització, es visualitza un error a la plantilla del projecte de còpia a causa de les diferències en el component horari de cada camp.</span><span class="sxs-lookup"><span data-stu-id="8cf39-125">When the start date is greater than the end date, an error displays on the copy project template because of differences in the time component of each field.</span></span>

<span data-ttu-id="8cf39-126">**Administració de recursos**</span><span class="sxs-lookup"><span data-stu-id="8cf39-126">**Resource management**</span></span>

<span data-ttu-id="8cf39-127">S'han corregit els problemes següents:</span><span class="sxs-lookup"><span data-stu-id="8cf39-127">The following issues have been fixed:</span></span>
- <span data-ttu-id="8cf39-128">S'utilitza un paràmetre incorrecte a la consulta d'ús del recurs i els clients potencials XML per filtrar incorrectament resultats a la quadrícula **Ús de recurs**.</span><span class="sxs-lookup"><span data-stu-id="8cf39-128">An incorrect parameter is used in the resource utilization query and the XML leads to incorrect filter results on the **Resource Utilization** grid.</span></span>
- <span data-ttu-id="8cf39-129">La confirmació **Amplia les reserves** mostra una data de finalització incorrecta per a les reserves.</span><span class="sxs-lookup"><span data-stu-id="8cf39-129">The **Extend Bookings** confirmation displays incorrect end date for bookings.</span></span>

<span data-ttu-id="8cf39-130">**Vendes**</span><span class="sxs-lookup"><span data-stu-id="8cf39-130">**Sales**</span></span>

<span data-ttu-id="8cf39-131">S'han corregit els problemes següents:</span><span class="sxs-lookup"><span data-stu-id="8cf39-131">The following issues have been fixed:</span></span>
- <span data-ttu-id="8cf39-132">Es mostra un missatge d'error si es crea un preu de categoria on falten valors.</span><span class="sxs-lookup"><span data-stu-id="8cf39-132">An error message occurs if a category price is created with missing values.</span></span>
- <span data-ttu-id="8cf39-133">Es mostra un missatge d'error si es crea una fita de línia de contracte sense una línia de comanda.</span><span class="sxs-lookup"><span data-stu-id="8cf39-133">An error message occurs if a contract line milestone is created without an order line.</span></span>
