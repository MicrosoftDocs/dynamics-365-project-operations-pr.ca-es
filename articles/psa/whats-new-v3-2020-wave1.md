---
title: Novetats o canvis a la versió 3.x fase 1 2020 del Project Service Automation
description: En aquest tema es proporciona informació sobre les novetats i els canvis a la versió 3 fase 1 2020 del Project Service Automation.
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
ms.openlocfilehash: f77c881c62428e423e0dab66eb34b033628a2a1b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996824"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a>Novetats o canvis a la versió 3 fase 1 2020 del Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

El tema destaca les consideracions clau d'actualització en migrar al llançament més recent del Project Service Automation (PSA) versió 3.x fase 1 2020.

## <a name="time-entry"></a>Entrada de temps
L'experiència d'entrada de temps s'ha ampliat per oferir capacitats per ampliar l'entrada de temps a més escenaris de clients. Això inclou la capacitat d'afegir tipus d'entrada, que ara tenen un comportament específic segons la **Configuració d'entrada de temps** del nom de l'esquema de temps, que es mostra com a **Origen de temps**. S'ha afegit una solució nova, anomenada Temps, Despesa, Estat i Aprovacions (TESA) per donar suport a aquesta funcionalitat.

### <a name="upgrade-consideration"></a>Consideracions sobre l'actualització
Per admetre a aquesta funcionalitat, s'han actualitzat les funcions dins del PSA per incloure els privilegis nous. Aquests privilegis concedeixen accés de lectura a l'entitat nova, **Configuració d'entrada de temps**.

Els usuaris que necessitin la capacitat de registrar al temps han tenir la funció d'usuari **Usuari d'entrada de temps** a més de les funcions existents. Aquesta funció inclou la funcionalitat nova i garanteix que l'entrada de temps continuarà funcionant.

A més, si teniu mòduls d'aplicacions personalitzades que inclouen tots els formularis per a l'entitat d'entrada de temps, se us demanarà que suprimiu el **Formulari de creació ràpida d'entrades de temps TESA** del mòdul.

### <a name="currently-extended-time-entry-changes"></a>Canvis d'entrades de temps ampliades actualment
Per minimitzar l'impacte als usuaris actuals de l'entrada de temps, aquest canvi de funció és l'únic requisit principal necessari per continuar utilitzant l'entrada de temps. Si heu creat visualitzacions personalitzades o experiències d'entrada de temps separades, heu de definir els camps **Configuració d'entrada de temps** al valor del PSA correcte.


[!INCLUDE[footer-include](../includes/footer-banner.md)]