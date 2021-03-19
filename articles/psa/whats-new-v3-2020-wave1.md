---
title: Novetats o canvis a la versió 3.x fase 1 2020 del Project Service Automation
description: En aquest tema es proporciona informació sobre les novetats i els canvis a la versió 3 fase 1 2020 del Project Service Automation.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/15/2020
ms.topic: article
author: stsporen
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: fef9cb62e989c693c8b3d00cb15441c284f66554
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280161"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a><span data-ttu-id="d9832-103">Novetats o canvis a la versió 3 fase 1 2020 del Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="d9832-103">What's new or changed in Project Service Automation version 3 wave 1 2020</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="d9832-104">El tema destaca les consideracions clau d'actualització en migrar al llançament més recent del Project Service Automation (PSA) versió 3.x fase 1 2020.</span><span class="sxs-lookup"><span data-stu-id="d9832-104">The topic highlights key upgrade considerations when moving to the latest release of Project Service Automation (PSA) version 3.x wave 1 2020.</span></span>

## <a name="time-entry"></a><span data-ttu-id="d9832-105">Entrada de temps</span><span class="sxs-lookup"><span data-stu-id="d9832-105">Time entry</span></span>
<span data-ttu-id="d9832-106">L'experiència d'entrada de temps s'ha ampliat per oferir capacitats per ampliar l'entrada de temps a més escenaris de clients.</span><span class="sxs-lookup"><span data-stu-id="d9832-106">The time entry experience has been extended to deliver capabilities for extending time entry into more customer scenarios.</span></span> <span data-ttu-id="d9832-107">Això inclou la capacitat d'afegir tipus d'entrada, que ara tenen un comportament específic segons la **Configuració d'entrada de temps** del nom de l'esquema de temps, que es mostra com a **Origen de temps**.</span><span class="sxs-lookup"><span data-stu-id="d9832-107">This includes the capability to add entry types, which now drive specific behavior based on the field schema name **Time Entry Settings**, displayed as **Time Source**.</span></span> <span data-ttu-id="d9832-108">S'ha afegit una solució nova, anomenada Temps, Despesa, Estat i Aprovacions (TESA) per donar suport a aquesta funcionalitat.</span><span class="sxs-lookup"><span data-stu-id="d9832-108">A new solution, called Time, Expense, Statusing, and Approvals (TESA) has been added to support this functionality.</span></span>

### <a name="upgrade-consideration"></a><span data-ttu-id="d9832-109">Consideracions sobre l'actualització</span><span class="sxs-lookup"><span data-stu-id="d9832-109">Upgrade consideration</span></span>
<span data-ttu-id="d9832-110">Per admetre a aquesta funcionalitat, s'han actualitzat les funcions dins del PSA per incloure els privilegis nous.</span><span class="sxs-lookup"><span data-stu-id="d9832-110">To support this functionality, the roles within PSA have been updated to include new privileges.</span></span> <span data-ttu-id="d9832-111">Aquests privilegis concedeixen accés de lectura a l'entitat nova, **Configuració d'entrada de temps**.</span><span class="sxs-lookup"><span data-stu-id="d9832-111">These privileges grant read access to the new entity, **Time Entry Settings**.</span></span>

<span data-ttu-id="d9832-112">Els usuaris que necessitin la capacitat de registrar al temps han tenir la funció d'usuari **Usuari d'entrada de temps** a més de les funcions existents.</span><span class="sxs-lookup"><span data-stu-id="d9832-112">Users who require the ability to log time should be granted the user role **Time Entry User** in addition to existing roles.</span></span> <span data-ttu-id="d9832-113">Aquesta funció inclou la funcionalitat nova i garanteix que l'entrada de temps continuarà funcionant.</span><span class="sxs-lookup"><span data-stu-id="d9832-113">This role includes the new functionality and ensures that time entry will continue to work.</span></span>

<span data-ttu-id="d9832-114">A més, si teniu mòduls d'aplicacions personalitzades que inclouen tots els formularis per a l'entitat d'entrada de temps, se us demanarà que suprimiu el **Formulari de creació ràpida d'entrades de temps TESA** del mòdul.</span><span class="sxs-lookup"><span data-stu-id="d9832-114">Additionally, if you have any custom app modules that include all forms for the time entry entity, you will be required to remove the **TESA time Entry Quick Create Form** from the module.</span></span>

### <a name="currently-extended-time-entry-changes"></a><span data-ttu-id="d9832-115">Canvis d'entrades de temps ampliades actualment</span><span class="sxs-lookup"><span data-stu-id="d9832-115">Currently extended time entry changes</span></span>
<span data-ttu-id="d9832-116">Per minimitzar l'impacte als usuaris actuals de l'entrada de temps, aquest canvi de funció és l'únic requisit principal necessari per continuar utilitzant l'entrada de temps.</span><span class="sxs-lookup"><span data-stu-id="d9832-116">To minimize the impact to current users of time entry, this role change is the only core requirement necessary to continue utilizing time entry.</span></span> <span data-ttu-id="d9832-117">Si heu creat visualitzacions personalitzades o experiències d'entrada de temps separades, heu de definir els camps **Configuració d'entrada de temps** al valor del PSA correcte.</span><span class="sxs-lookup"><span data-stu-id="d9832-117">If you have created custom views or separate time entry experiences, you must set the **Time Entry Setting** fields to the correct PSA value.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]