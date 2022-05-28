---
title: Novetats o canvis de la versió d'actualització 43 del Project Service Automation, V3
description: En aquest tema s'enumeren les característiques i les correccions disponibles a la Versió 43 d'actualització Microsoft Dynamics 365 Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 05/04/2022
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
ms.reviewer: johnmichalak
ms.openlocfilehash: fcf18a24b3bc354a16a415368063133743e79696
ms.sourcegitcommit: 7e419a5f73f80fa887084e3b212c90586fc397dd
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/05/2022
ms.locfileid: "8710120"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-43-v3"></a>Novetats o canvis de la versió d'actualització 43 del Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Ens complau anunciar l'última actualització de l'aplicació Microsoft Dynamics 365 Project Service Automation. Aquesta versió inclou algunes millores importants per a la qualitat, el rendiment i la usabilitat. És compatible amb el Dynamics 365 9.x. Per actualitzar aquesta versió, visiteu la pàgina de solucions en línia del Centre d'administració del Dynamics 365 i instal·leu l'actualització. Per obtenir més informació, vegeu [Instal·lar, actualitzar o eliminar una solució preferida](/power-platform/admin/install-remove-preferred-solution).

En aquest tema es mostren les característiques i correccions que són noves o s'han canviat per al llançament de l'actualització 43, V3, de Project Service Automation. Aquesta versió té el número de compilació V3.10.74.200 i està disponible de manera general a través d'una actualització automàtica el maig de 2022.

## <a name="update-release-43"></a>Versió d'actualització 43

### <a name="bug-fixes"></a>Correccions d'errors

S'han corregit els problemes següents.


**Temps i despesa**

- Quan s'importen entrades de temps des de reserves o assignacions de recursos, no es manté la referència al recurs que es pot reservar relacionat.
- Quan la quadrícula d'entrada de temps s'expandeix a pantalla completa, navegar per la quadrícula amb la tecla de pestanya no funciona.
- Quan envieu una entrada de temps creada per un altre usuari, el **camp Enviat per** s'emplena incorrectament amb l'usuari que ha creat el full de temps.
