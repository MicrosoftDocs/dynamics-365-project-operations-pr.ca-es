---
title: Novetats o canvis de la versió d'actualització 16 del Project Service Automation, V3
description: En aquest tema es mostren les característiques i correccions disponibles al Project Service Automation V3, versió d'actualització 16.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/18/2020
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
ms.openlocfilehash: 33a711816e8cca34c4595aa0929de9a808a48b0f
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949358"
---
# <a name="project-service-automation-update-release-16-v3"></a><span data-ttu-id="0b126-103">Project Service Automation, versió d'actualització 16, V3</span><span class="sxs-lookup"><span data-stu-id="0b126-103">Project Service Automation Update Release 16, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="0b126-104">Estem encantats d'anunciar-vos l'última actualització per a l'aplicació Project Service Automation per al Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="0b126-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="0b126-105">Aquesta versió inclou algunes millores importants per a la qualitat, el rendiment i la usabilitat.</span><span class="sxs-lookup"><span data-stu-id="0b126-105">This release includes some important improvements to quality, performance, and usability.</span></span>  <span data-ttu-id="0b126-106">Aquest llançament és compatible amb el Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="0b126-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="0b126-107">Per actualitzar a aquesta versió, visiteu el Centre d'administració del Dynamics 365 en línia i aneu a la pàgina de solucions per instal·lar l'actualització.</span><span class="sxs-lookup"><span data-stu-id="0b126-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="0b126-108">Per obtenir més informació, vegeu [Instal·lació, actualització o supressió d'una solució preferida](/dynamics365/project-service/upgrade-psa-home-page).</span><span class="sxs-lookup"><span data-stu-id="0b126-108">For more information, see [Install, Update a Preferred Solution](/dynamics365/project-service/upgrade-psa-home-page).</span></span>
<span data-ttu-id="0b126-109">En aquest tema es mostren les característiques i correccions que són noves o s'han canviat per al PSA V3, versió d'actualització 16.</span><span class="sxs-lookup"><span data-stu-id="0b126-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 16.</span></span> <span data-ttu-id="0b126-110">Aquesta versió té el número de compilació V3.10.6.34 i està disponible de forma general a través d'una actualització automàtica el gener de 2020.</span><span class="sxs-lookup"><span data-stu-id="0b126-110">This version has a build number of V3.10.6.34 and is generally available through a self-update in January 2020.</span></span>


## <a name="update-release-16"></a><span data-ttu-id="0b126-111">Versió d'actualització 16</span><span class="sxs-lookup"><span data-stu-id="0b126-111">Update Release 16</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="0b126-112">Correccions d'errors</span><span class="sxs-lookup"><span data-stu-id="0b126-112">Bug fixes</span></span>

-   <span data-ttu-id="0b126-113">Temps i despesa</span><span class="sxs-lookup"><span data-stu-id="0b126-113">Time and Expense</span></span>

    -   <span data-ttu-id="0b126-114">Correcció: els usuaris que intentaven enviar entrades de despesa i de temps suprimits per a les aprovacions rebran ara missatges d'error pertinents.</span><span class="sxs-lookup"><span data-stu-id="0b126-114">Fixed: Users attempting to submit deleted time and expense entries for approvals will now receive relevant error messages.</span></span>

-   <span data-ttu-id="0b126-115">Administració de projectes</span><span class="sxs-lookup"><span data-stu-id="0b126-115">Project Management</span></span>

    -   <span data-ttu-id="0b126-116">Correcció: les unitats de recursos definides per als membres de l'equip a les plantilles es respecten amb les plantilles que s'apliquen a un nou projecte.</span><span class="sxs-lookup"><span data-stu-id="0b126-116">Fixed: The resourcing units defined for team members in templates are respected with the templates are applied to a new project.</span></span>

    -   <span data-ttu-id="0b126-117">Correcció: s'ha millorat la gestió de la reassignació de la propietat del registre.</span><span class="sxs-lookup"><span data-stu-id="0b126-117">Fixed: Improved handling of the re-assignment of record ownership.</span></span>

    -   <span data-ttu-id="0b126-118">Correcció: els projectes que estan en procés de copiar-se no es podran copiar fins que s'hagin completat totes les operacions de còpia.</span><span class="sxs-lookup"><span data-stu-id="0b126-118">Fixed: Projects that are in the process of being copied will not be permitted to copied until all copy operations are complete.</span></span>

-   <span data-ttu-id="0b126-119">Administració de recursos</span><span class="sxs-lookup"><span data-stu-id="0b126-119">Resource Management</span></span>

    -   <span data-ttu-id="0b126-120">Correcció: el perllongament de les reserves ara gestiona la duració curta correctament i ja no es crea el valor de zero hores per a reserves prolongades.</span><span class="sxs-lookup"><span data-stu-id="0b126-120">Fixed: Extend bookings now handles short durations correctly and no longer creates zero hours for extended bookings.</span></span>

    -   <span data-ttu-id="0b126-121">Correcció: la visualització de conciliació ara es mostra quan el fus horari del projecte és +5:30 GMT i el de l'usuari és diferent.</span><span class="sxs-lookup"><span data-stu-id="0b126-121">Fixed: The reconciliation view now renders when the project time zone is +5:30 GMT and the user’s time aone is different.</span></span>

-   <span data-ttu-id="0b126-122">Sales</span><span class="sxs-lookup"><span data-stu-id="0b126-122">Sales</span></span>

    -   <span data-ttu-id="0b126-123">Correcció: quan un projecte que s'ha assignat a una línia de contracte se suprimeix i s'assigna un projecte nou, significa que els registres reals del projecte nou no s'estaven reavaluant basant-se en les regles de facturació i de preus definides a la línia de contracte.</span><span class="sxs-lookup"><span data-stu-id="0b126-123">Fixed: When a project mapped to a contract line is removed and a new project is mapped, the actual records on the new project were not getting re-evaluated based on the billing and pricing rules defined on the contract line.</span></span> <span data-ttu-id="0b126-124">S'ha solucionat en aquesta versió.</span><span class="sxs-lookup"><span data-stu-id="0b126-124">This has been fixed in this release.</span></span> <span data-ttu-id="0b126-125">Els preus i els registres reals del projecte acabat d'assignar s'invertiran i es tornaran a crear correctament basant-se en les regles de preus i de facturació de la línia de contracte.</span><span class="sxs-lookup"><span data-stu-id="0b126-125">Pricing and actual records on the newly mapped project will get reversed and re-created correctly based on the pricing and billing rules of the contract line.</span></span> <span data-ttu-id="0b126-126">Els registres reals del projecte no assignat també es tornaran a avaluar i crear com a conseqüència.</span><span class="sxs-lookup"><span data-stu-id="0b126-126">The actual records of the un-mapped project will also get re-evaluated and re-created as a consequence.</span></span>

    -   <span data-ttu-id="0b126-127">Correccions: s'ha afegit una validació addicional al camp **Import** de la línia d'estimació per garantir que no s'hagin persistit els valors nuls.</span><span class="sxs-lookup"><span data-stu-id="0b126-127">Fixed: Additional validation has been added to an estimate line’s **Amount** field to ensure that null values are not persisted.</span></span>

    -   <span data-ttu-id="0b126-128">Correcció: quan s'han actualitzat els valors reals en un projecte, s'afegeix un botó d'actualització al formulari principal del projecte per permetre als usuaris tornar a sincronitzar els valors reals.</span><span class="sxs-lookup"><span data-stu-id="0b126-128">Fixed: When actuals have been updated on a project, a refresh button has been added to the project main form to allow users to re-sync the actuals.</span></span>

    -   <span data-ttu-id="0b126-129">Correcció: quan els usuaris facin l'actualització de 2.X a 3.X, es permetran projectes amb un valor NULL per al nom del projecte.</span><span class="sxs-lookup"><span data-stu-id="0b126-129">Fixed: When users upgrade from 2.X to 3.X, projects with a NULL value for project name will be permitted.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]