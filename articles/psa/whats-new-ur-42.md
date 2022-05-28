---
title: Novetats o canvis de la versió d'actualització 42 del Project Service Automation, V3
description: En aquest tema s'enumeren les característiques i les correccions disponibles a la Versió 42 d'actualització Microsoft Dynamics 365 Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/05/2022
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
ms.openlocfilehash: 32cb7a4c5fc29d5c0dcec37dd395ae69037435a2
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8589184"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-42-v3"></a>Novetats o canvis de la versió d'actualització 42 del Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Ens complau anunciar l'última actualització de l'aplicació Microsoft Dynamics 365 Project Service Automation. Aquesta versió inclou algunes millores importants per a la qualitat, el rendiment i la usabilitat. És compatible amb el Dynamics 365 9.x. Per actualitzar aquesta versió, visiteu la pàgina de solucions en línia del Centre d'administració del Dynamics 365 i instal·leu l'actualització. Per obtenir més informació, vegeu [Instal·lar, actualitzar o eliminar una solució preferida](/power-platform/admin/install-remove-preferred-solution).

En aquest tema es mostren les característiques i correccions que són noves o s'han canviat per al llançament de l'actualització 42, V3, de Project Service Automation. Aquesta versió té el número de compilació V3.10.73.61 i està disponible de manera general a través d'una actualització automàtica l'abril de 2022.

## <a name="update-release-42"></a>Versió d'actualització 42

### <a name="bug-fixes"></a>Correccions d'errors

S'han corregit els problemes següents.

**Temps i despesa**

- Quan es rebutja un full de temps, l'usuari que l'ha rebutjat s'identifica incorrectament com a **Sistema**.
- Quan s'importen entrades de temps, falta el **valor Categoria de** recursos.
- Els aprovadors de projectes poden aprovar els projectes enviats quan els seus permisos no estiguin definits específicament com a **Pot Aprovar**.

**Vendes**

- Quan els reals es registren en tasques que no són de nivell arrel, els costos reals s'agreguen incorrectament.
