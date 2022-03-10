---
title: Novetats o canvis de la versió d'actualització 23 del Project Service Automation, V3
description: En aquest tema es mostren les característiques i correccions disponibles al Project Service Automation V3, versió d'actualització 23.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 08/25/2020
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
ms.openlocfilehash: ec27d2344f14e61a50be2771ee3d7952f16abd736927de7c3c5a019351a3e067
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6996604"
---
# <a name="project-service-automation-update-release-23-v3"></a>Project Service Automation, versió d'actualització 23, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Estem encantats d'anunciar-vos l'última actualització per a l'aplicació Project Service Automation per al Dynamics 365. Aquesta versió inclou algunes millores importants per a la qualitat, el rendiment i la usabilitat. Aquest llançament és compatible amb el Dynamics 365 9.x. Per actualitzar a aquesta versió, visiteu el Centre d'administració del Dynamics 365 en línia i aneu a la pàgina de solucions per instal·lar l'actualització. Per obtenir més informació, vegeu [Instal·lar, actualitzar o eliminar una solució preferida](/power-platform/admin/install-remove-preferred-solution).

En aquest tema es mostren les característiques i correccions que són noves o s'han canviat per al Project Service Automation V3, versió d'actualització 23. Aquesta versió té el número de compilació V3.10.34.30 i està disponible de forma general a través d'una actualització automàtica l'agost de 2020.

## <a name="update-release-23"></a>Versió d'actualització 23

### <a name="bug-fixes"></a>Correccions d'errors

**Temps i despesa**

S'han corregit els problemes següents:
- Es gestiona un cas excepcional a **Supressió de membre de l'equip del projecte** per proporcionar una excepció significativa.
- Una importació d'assignació provoca una pantalla de supressió en blanc.

**Administració de recursos**

S'han corregit els problemes següents:

- La **targeta de recursos de la quadrícula d'ús de recursos** mostra dades incorrectes quan l'escala de temps té més de cinc dies.
- Quan els clients creen un recurs reservable, el complement de manera intermitent no afegeix automàticament el recurs a un grup del Microsoft Office 365.
- La visualització **Conciliació** mostra els contorns manuals incorrectament a la visualització **Setmana** o **Mes**.

**Administració de projectes**

S'han corregit els problemes següents:

- Un nombre excessiu d'entitats **RetrieveMultiple per a usersettings** provoca un rendiment degradat per a les aprovacions de projectes i altres operacions.
- La cerca de recursos de la quadrícula **Planificació de tasques** es limita a mostrar només cinc membres de l'equip a l'equip del projecte. 
- La cerca de recursos de la quadrícula **Planificació de tasques** no filtra els recursos inactius.
- El mode manual no funciona com s'esperava a l'estructura del desglossament del treball de la planificació del projecte.
- La quadrícula **Planificació de tasques** mostra **Categories de transaccions inactives**.
- La quadrícula **Assignació de recursos** arrodoneix incorrectament quan una tasca té diverses assignacions.
- Els valors d'arrodoniment són diferents entre el cost previst i el cost real per a una sola tasca.

**Sales**

S'han corregit els problemes següents:

- En fer doble clic a **Recupera totes les categories de transaccions**, es creen diverses línies.


[!INCLUDE[footer-include](../includes/footer-banner.md)]