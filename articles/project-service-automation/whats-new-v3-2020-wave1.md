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
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a>Novetats o canvis a la versió 3 fase 1 2020 del Project Service Automation
El tema destaca les consideracions clau d'actualització en migrar al llançament més recent del Project Service Automation (PSA) versió 3.x fase 1 2020.

## <a name="time-entry"></a>Entrada de temps
L'experiència d'entrada de temps s'ha ampliat per oferir capacitats per ampliar l'entrada de temps a més escenaris de clients. Això inclou la capacitat d'afegir tipus d'entrada, que ara tenen un comportament específic segons la **Configuració d'entrada de temps** del nom de l'esquema de temps, que es mostra com a **Origen de temps**.

### <a name="upgrade-consideration"></a>Consideracions sobre l'actualització
Per admetre a aquesta funcionalitat, s'han actualitzat les funcions dins del PSA per incloure els privilegis nous. Aquests privilegis concedeixen accés de lectura a l'entitat nova, **Configuració d'entrada de temps**.

Els usuaris que necessitin la capacitat de registrar al temps han tenir la funció d'usuari **Usuari d'entrada de temps** a més de les funcions existents. Aquesta funció inclou la funcionalitat nova i garanteix que l'entrada de temps continuarà funcionant.

### <a name="currently-extended-time-entry-changes"></a>Canvis d'entrades de temps ampliades actualment
Per minimitzar l'impacte als usuaris actuals de l'entrada de temps, aquest canvi de funció és l'únic requisit principal necessari per continuar utilitzant l'entrada de temps. Si heu creat visualitzacions personalitzades o experiències d'entrada de temps separades, heu de definir els camps **Configuració d'entrada de temps** al valor del PSA correcte.
