---
title: Novetats o canvis de la versió d'actualització 45 del Project Service Automation, V3
description: En aquest article s'enumeren les característiques i les correccions disponibles a la Versió 45 d'actualització Microsoft Dynamics 365 Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 07/14/2022
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
ms.openlocfilehash: 98f7c973917d7d6334e6e0aeb15214c538b33143
ms.sourcegitcommit: 36fda4f45ddeb0f81d30bd1e22852727df644754
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 07/16/2022
ms.locfileid: "9169174"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-45-v3"></a>Novetats o canvis de la versió d'actualització 45 del Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Ens complau anunciar l'última actualització de l'aplicació Microsoft Dynamics 365 Project Service Automation. Aquesta versió inclou algunes millores importants per a la qualitat, el rendiment i la usabilitat. És compatible amb el Dynamics 365 9.x. Per actualitzar aquesta versió, visiteu la pàgina de solucions en línia del Centre d'administració del Dynamics 365 i instal·leu l'actualització. Per obtenir més informació, vegeu [Instal·lar, actualitzar o eliminar una solució preferida](/power-platform/admin/install-remove-preferred-solution).

En aquest article es mostren les característiques i correccions que són noves o s'han canviat per al llançament de l'actualització 45, V3, de Project Service Automation. Aquesta versió té el número de versió V3.10.76.168 i està disponible de forma general mitjançant una autoactualització el juliol de 2022.

## <a name="update-release-45"></a>Versió d'actualització 45

### <a name="bug-fixes"></a>Correccions d'errors

S'han corregit els problemes següents.

**Vendes**

- Els usuaris no poden crear factures correctament després d'intentar crear una factura sense vendes no facturades, si també visualitzen la mateixa instància de la pàgina i no l'actualitzen.

**Temps i despesa**

- Quan s'habilita Aprovacions modernes i s'aprova una aprovació de projecte recuperada, la fase del registre s'actualitza incorrectament a **Sol ·licitud de recuperació aprovada**.
- Quan s'habilita Aprovacions modernes i Fluxos del núvol està inactiu, el procés d'aprovació no es duu a terme correctament i no es notifica als usuaris que l'envien o l'aproven.
