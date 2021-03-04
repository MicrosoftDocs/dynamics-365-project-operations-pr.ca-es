---
title: Novetats o canvis de la versió d'actualització 19 del Project Service Automation, V3
description: En aquest tema es mostren les característiques i correccions disponibles al Project Service Automation V3, versió d'actualització 19.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 05/05/2020
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
ms.openlocfilehash: 8a73a6acd4ce4c9559cdf4591ede735a613f4d52
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "5143594"
---
# <a name="project-service-automation-update-release-19-v3"></a><span data-ttu-id="0e0b7-103">Project Service Automation, versió d'actualització 19, V3</span><span class="sxs-lookup"><span data-stu-id="0e0b7-103">Project Service Automation Update Release 19, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="0e0b7-104">Estem encantats d'anunciar-vos l'última actualització per a l'aplicació Project Service Automation per al Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="0e0b7-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="0e0b7-105">Aquesta versió inclou algunes millores importants per a la qualitat, el rendiment i la usabilitat.</span><span class="sxs-lookup"><span data-stu-id="0e0b7-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="0e0b7-106">Aquest llançament és compatible amb el Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="0e0b7-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="0e0b7-107">Per actualitzar a aquesta versió, visiteu el Centre d'administració del Dynamics 365 en línia i aneu a la pàgina de solucions per instal·lar l'actualització.</span><span class="sxs-lookup"><span data-stu-id="0e0b7-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="0e0b7-108">Per obtenir més informació, vegeu [Instal·lar, actualitzar o eliminar una solució preferida](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="0e0b7-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="0e0b7-109">En aquest tema es mostren les característiques i correccions que són noves o s'han canviat per al PSA V3, versió d'actualització 19.</span><span class="sxs-lookup"><span data-stu-id="0e0b7-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 19.</span></span> <span data-ttu-id="0e0b7-110">Aquesta versió té el número de compilació V3.10.30.41 i està disponible de manera general a través d'una actualització automàtica el maig de 2020.</span><span class="sxs-lookup"><span data-stu-id="0e0b7-110">This version has a build number of V3.10.30.41 and is generally available through a self-update in May 2020.</span></span>

## <a name="update-release-19"></a><span data-ttu-id="0e0b7-111">Versió d'actualització 19</span><span class="sxs-lookup"><span data-stu-id="0e0b7-111">Update Release 19</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="0e0b7-112">Correccions d'errors</span><span class="sxs-lookup"><span data-stu-id="0e0b7-112">Bug fixes</span></span>

<span data-ttu-id="0e0b7-113">**Temps i despesa**</span><span class="sxs-lookup"><span data-stu-id="0e0b7-113">**Time and Expense**</span></span>

<span data-ttu-id="0e0b7-114">S'han corregit els problemes següents:</span><span class="sxs-lookup"><span data-stu-id="0e0b7-114">The following issues have been fixed:</span></span> 

- <span data-ttu-id="0e0b7-115">Els errors derivats de les importacions d'entrades de temps no emergien correctament.</span><span class="sxs-lookup"><span data-stu-id="0e0b7-115">Errors derived from time entry imports are not surfaced correctly.</span></span>
- <span data-ttu-id="0e0b7-116">La quadrícula d'entrada de temps no admet el comportament del camp **Només data**.</span><span class="sxs-lookup"><span data-stu-id="0e0b7-116">Time Entry Grid does not support **Date Only** field behavior.</span></span>
- <span data-ttu-id="0e0b7-117">Els recursos del projecte no poden crear una despesa amb un projecte.</span><span class="sxs-lookup"><span data-stu-id="0e0b7-117">Project Resources are unable to create an expense with a project.</span></span>

<span data-ttu-id="0e0b7-118">**Administració de projectes**</span><span class="sxs-lookup"><span data-stu-id="0e0b7-118">**Project Management**</span></span>

<span data-ttu-id="0e0b7-119">S'han corregit els problemes següents:</span><span class="sxs-lookup"><span data-stu-id="0e0b7-119">The following issues have been fixed:</span></span> 

-  <span data-ttu-id="0e0b7-120">La tasca descendent secundària provoca una estimació de l'esforç incorrecta durant el càlcul de la finalització (EAC).</span><span class="sxs-lookup"><span data-stu-id="0e0b7-120">Grandchild task causes an incorrect effort estimate during the Completion (EAC) Calculation.</span></span>

<span data-ttu-id="0e0b7-121">**Sales**</span><span class="sxs-lookup"><span data-stu-id="0e0b7-121">**Sales**</span></span>

<span data-ttu-id="0e0b7-122">S'han corregit els problemes següents:</span><span class="sxs-lookup"><span data-stu-id="0e0b7-122">The following issues have been fixed:</span></span> 

- <span data-ttu-id="0e0b7-123">L'acció **Torna a calcular** no funciona amb els detalls de la línia de contracte de la despesa ni els detalls de la línia d'oferta.</span><span class="sxs-lookup"><span data-stu-id="0e0b7-123">The **Recalculate** action does not work with expense contract line details or quote line details.</span></span>
- <span data-ttu-id="0e0b7-124">**Actualitza els preus** falta a l'estimació de la despesa.</span><span class="sxs-lookup"><span data-stu-id="0e0b7-124">**Update Prices** is missing for expense estimates.</span></span>
-  <span data-ttu-id="0e0b7-125">Els clients no poden seleccionar motius d'estat de contracte personalitzats des de la pàgina **Contracte del projecte**.</span><span class="sxs-lookup"><span data-stu-id="0e0b7-125">Customers are unable to select custom contract status reasons from the **Project Contract** page.</span></span>
- <span data-ttu-id="0e0b7-126">Els clients experimenten un rendiment degradat en crear una llista de preus personalitzada a partir d'una oferta.</span><span class="sxs-lookup"><span data-stu-id="0e0b7-126">Customers experience degraded performance when creating a custom price list from a quote.</span></span>
- <span data-ttu-id="0e0b7-127">Els clients experimenten una incoherència amb el valor per defecte d'**unitat** a les pàgines **Detalls de la línia d'oferta** i **Detalls de la línia de contracte**.</span><span class="sxs-lookup"><span data-stu-id="0e0b7-127">Customers experience inconsistency with **unit** defaults on **Quote Line Details** and **Contract Line Details** pages.</span></span>
- <span data-ttu-id="0e0b7-128">L'addició d'elements de categoria no facturables a una línia de contracte facturable no respectarà el tipus de facturació **No facturable** de la categoria de la transacció.</span><span class="sxs-lookup"><span data-stu-id="0e0b7-128">Adding non-chargeable transaction category items to a chargeable contract line will not respect the **Non-chargeable** billing type of the transaction category.</span></span>
- <span data-ttu-id="0e0b7-129">Els clients no poden utilitzar les funcions i la categoria acabades d'afegir als contractes creats prèviament.</span><span class="sxs-lookup"><span data-stu-id="0e0b7-129">Customers can't use the newly added roles and category on previously created contracts.</span></span>
- <span data-ttu-id="0e0b7-130">Els clients experimenten un rendiment degradat per una recuperació innecessària a PreValidateProjectTeamMemberUpdate.cs</span><span class="sxs-lookup"><span data-stu-id="0e0b7-130">Customers experience degraded performance Unnecessary retrieve in PreValidateProjectTeamMemberUpdate.cs</span></span>
- <span data-ttu-id="0e0b7-131">Les funcions configurades com a no facturables a la llista **Categories de recursos** s'han d'afegir a la pestanya **Funcions facturables** com a **No facturables** a la línia de contracte d'un projecte.</span><span class="sxs-lookup"><span data-stu-id="0e0b7-131">Roles set up as non-chargeable in the **Resource Categories** list should be added to the **Chargeable Roles** tab as **Non0chargeable** on the contract line for a project.</span></span>
- <span data-ttu-id="0e0b7-132">Els clients poden experimentar un rendiment degradat en crear un projecte perquè **GetBookableResourceIdFromUser** recupera totes les columnes de recursos disponibles en comptes de només l'identificador principal.</span><span class="sxs-lookup"><span data-stu-id="0e0b7-132">Customers may experience degraded performance when creating a project because **GetBookableResourceIdFromUser** retrieves all columns of bookable resources instead of just the primary ID.</span></span>
- <span data-ttu-id="0e0b7-133">L'entitat **TransactionType** no té el complement d'actualització de la prevalidació per impedir que els usuaris ingressin **Unitats** i **Grups d'unitats** que no són vàlids per als tipus de transaccions.</span><span class="sxs-lookup"><span data-stu-id="0e0b7-133">**TransactionType** entity missing the pre-validation update plug-in to prevent users from entering **Units** and **UnitGroups** that are not valid for transaction types.</span></span>
- <span data-ttu-id="0e0b7-134">El pas **Suprimeix** no funciona per a la importació d'entrades de temps.</span><span class="sxs-lookup"><span data-stu-id="0e0b7-134">The **Remove** step does not work for time entry import.</span></span>
