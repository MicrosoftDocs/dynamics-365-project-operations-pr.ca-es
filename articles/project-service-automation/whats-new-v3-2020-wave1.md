---
title: Novetats o canvis a la versió 3.x fase 1 2020 del Project Service Automation
description: En aquest tema es proporciona informació sobre les novetats i els canvis a la versió 3 fase 1 2020 del Project Service Automation.
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 01/24/2020
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 3.x wave 1 2020
author: stsporen
ms.assetid: 48b408c1-11e7-4005-abac-8fd7c0b064b1
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 478080c0570b71188c9f1e12b18b5aadc13903e5
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749490"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a><span data-ttu-id="9724e-103">Novetats o canvis a la versió 3 fase 1 2020 del Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="9724e-103">What's new or changed in Project Service Automation version 3 wave 1 2020</span></span>
<span data-ttu-id="9724e-104">El tema destaca les consideracions clau d'actualització en migrar al llançament més recent del Project Service Automation (PSA) versió 3.x fase 1 2020.</span><span class="sxs-lookup"><span data-stu-id="9724e-104">The topic highlights key upgrade considerations when moving to the latest release of Project Service Automation (PSA) version 3.x wave 1 2020.</span></span>

## <a name="time-entry"></a><span data-ttu-id="9724e-105">Entrada de temps</span><span class="sxs-lookup"><span data-stu-id="9724e-105">Time entry</span></span>
<span data-ttu-id="9724e-106">L'experiència d'entrada de temps s'ha ampliat per oferir capacitats per ampliar l'entrada de temps a més escenaris de clients.</span><span class="sxs-lookup"><span data-stu-id="9724e-106">The time entry experience has been extended to deliver capabilities for extending time entry into more customer scenarios.</span></span> <span data-ttu-id="9724e-107">Això inclou la capacitat d'afegir tipus d'entrada, que ara tenen un comportament específic segons la **Configuració d'entrada de temps** del nom de l'esquema de temps, que es mostra com a **Origen de temps**.</span><span class="sxs-lookup"><span data-stu-id="9724e-107">This includes the capability to add entry types, which now drive specific behavior based on the field schema name **Time Entry Settings**, displayed as **Time Source**.</span></span>

### <a name="upgrade-consideration"></a><span data-ttu-id="9724e-108">Consideracions sobre l'actualització</span><span class="sxs-lookup"><span data-stu-id="9724e-108">Upgrade consideration</span></span>
<span data-ttu-id="9724e-109">Per admetre a aquesta funcionalitat, s'han actualitzat les funcions dins del PSA per incloure els privilegis nous.</span><span class="sxs-lookup"><span data-stu-id="9724e-109">To support this functionality, the roles within PSA have been updated to include new privileges.</span></span> <span data-ttu-id="9724e-110">Aquests privilegis concedeixen accés de lectura a l'entitat nova, **Configuració d'entrada de temps**.</span><span class="sxs-lookup"><span data-stu-id="9724e-110">These privileges grant read access to the new entity, **Time Entry Settings**.</span></span>

<span data-ttu-id="9724e-111">Els usuaris que necessitin la capacitat de registrar al temps han tenir la funció d'usuari **Usuari d'entrada de temps** a més de les funcions existents.</span><span class="sxs-lookup"><span data-stu-id="9724e-111">Users who require the ability to log time should be granted the user role **Time Entry User** in addition to existing roles.</span></span> <span data-ttu-id="9724e-112">Aquesta funció inclou la funcionalitat nova i garanteix que l'entrada de temps continuarà funcionant.</span><span class="sxs-lookup"><span data-stu-id="9724e-112">This role includes the new functionality and ensures that time entry will continue to work.</span></span>

### <a name="currently-extended-time-entry-changes"></a><span data-ttu-id="9724e-113">Canvis d'entrades de temps ampliades actualment</span><span class="sxs-lookup"><span data-stu-id="9724e-113">Currently extended time entry changes</span></span>
<span data-ttu-id="9724e-114">Per minimitzar l'impacte als usuaris actuals de l'entrada de temps, aquest canvi de funció és l'únic requisit principal necessari per continuar utilitzant l'entrada de temps.</span><span class="sxs-lookup"><span data-stu-id="9724e-114">To minimize the impact to current users of time entry, this role change is the only core requirement necessary to continue utilizing time entry.</span></span> <span data-ttu-id="9724e-115">Si heu creat visualitzacions personalitzades o experiències d'entrada de temps separades, heu de definir els camps **Configuració d'entrada de temps** al valor del PSA correcte.</span><span class="sxs-lookup"><span data-stu-id="9724e-115">If you have created custom views or separate time entry experiences, you must set the **Time Entry Setting** fields to the correct PSA value.</span></span>
