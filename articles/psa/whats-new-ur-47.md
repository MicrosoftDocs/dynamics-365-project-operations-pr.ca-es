---
title: Novetats o canvis de la versió d'actualització 47 del Project Service Automation, V3
description: En aquest article s'enumeren les característiques i les correccions disponibles a la Versió 47 d'actualització Microsoft Dynamics 365 Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 09/14/2022
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
ms.openlocfilehash: 08e8fa9c41bdd77d93e4d5207266115022fba1b2
ms.sourcegitcommit: 498a5d5a33c47cab788fac4215fc47662042155a
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 09/14/2022
ms.locfileid: "9477276"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-47-v3"></a>Novetats o canvis de la versió d'actualització 47 del Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Ens complau anunciar l'última actualització de l'aplicació Microsoft Dynamics 365 Project Service Automation. Aquesta versió inclou algunes millores importants per a la qualitat, el rendiment i la usabilitat. És compatible amb el Dynamics 365 9.x. Per actualitzar aquesta versió, visiteu la pàgina de solucions en línia del Centre d'administració del Dynamics 365 i instal·leu l'actualització. Per obtenir més informació, vegeu [Instal·lar, actualitzar o eliminar una solució preferida](/power-platform/admin/install-remove-preferred-solution).

En aquest article es mostren les característiques i correccions que són noves o s'han canviat per al llançament de l'actualització 45, V3, de Project Service Automation. Aquesta versió té el número de versió V3.10.78.8 i està disponible de forma general mitjançant una autoactualització el juliol de 2022.

## <a name="update-release-47"></a>Versió d'actualització 47

### <a name="bug-fixes"></a>Correccions d'errors

S'han corregit els problemes següents.

**Administració de recursos**
- S'ha actualitzat una validació per assegurar que els usuaris no poden activar una excepció de referència nul·la quan intenten crear un membre de l'equip del projecte sense un **Recurs que es pot reservar**.
