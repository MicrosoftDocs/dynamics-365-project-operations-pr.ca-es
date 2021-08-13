---
title: Novetats o canvis de la versió d'actualització 29 del Project Service Automation, V3
description: En aquest tema es mostren les característiques i correccions disponibles al Project Service Automation V3, versió d'actualització 29.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/22/2021
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
ms.openlocfilehash: 87f10d793f9edc055444a3cecea9ea709c1fd7ff7213d6cfaf6b3cbe83a6a5a6
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6985084"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-29-v3"></a>Novetats o canvis de la versió d'actualització 29 del Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Estem encantats d'anunciar-vos l'última actualització per a l'aplicació Project Service Automation per al Dynamics 365. Aquesta versió inclou algunes millores importants per a la qualitat, el rendiment i la usabilitat. Aquest llançament és compatible amb el Dynamics 365 9.x. Per actualitzar a aquesta versió, visiteu el Centre d'administració del Dynamics 365 en línia i aneu a la pàgina de solucions per instal·lar l'actualització. Per obtenir més informació, vegeu [Instal·lar, actualitzar o eliminar una solució preferida](/power-platform/admin/install-remove-preferred-solution).

En aquest tema es mostren les característiques i correccions que són noves o s'han canviat per al Project Service Automation V3, versió d'actualització 29. Aquesta versió té un número de compilació de V3.10.47.7 i està disponible de manera general a través d'una actualització d'autoservei al febrer de 2021.

## <a name="update-release-29"></a>Versió d'actualització 29

### <a name="bug-fixes"></a>Correccions d'errors

**Temps i despesa**

S'han corregit els problemes següents:

- Els usuaris no poden veure les hores de feina registrades en dies que no són feiners a la quadrícula d'entrada de temps.
- Les entrades de despesa aprovades es poden editar a la quadrícula.

**Administració de projectes**

S'han corregit els problemes següents:

- Falta lògica de validació per garantir que les hores d'esforç d'assignació de recursos no poden ser negatives.
- L'acció personalitzada **AssignResourcesForTask** actualitza tots els camps en comptes de només camps canviats.
- Quan es copia un projecte en un entorn amb complements o fluxos de treball registrats a la incidència **CreateProject**, l'atribut **msdyn_bulkgenerationstatus** no s'actualitza si es produeix un error a **CopyWBSToProject**.
- Quan expandiu el calendari del projecte, els dies feiners no s'ordenen en ordre ascendent, cosa que fa que fallin algunes actualitzacions de tasques del projecte.
- Quan canvieu l'Administrador de projectes en un projecte existent, s'activa la lògica per defecte de la unitat organitzativa.

**Vendes**

S'han corregit els problemes següents:

- La pestanya **Rendiment del contracte** de la pàgina **Contracte** falla silenciosament durant la inicialització quan no hi ha cap línia de contracte.