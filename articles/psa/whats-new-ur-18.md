---
title: Novetats o canvis de la versió d'actualització 18 del Project Service Automation, V3
description: En aquest tema es mostren les característiques i correccions disponibles al Project Service Automation V3, versió d'actualització 18.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 04/27/2020
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
ms.openlocfilehash: 3a6d3ee21ecf742b2253132f3d3cc1cb2b57af75
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4119856"
---
# <a name="project-service-automation-update-release-18-v3"></a>Project Service Automation, versió d'actualització 18, V3

Estem encantats d'anunciar-vos l'última actualització per a l'aplicació Project Service Automation per al Dynamics 365. Aquesta versió inclou algunes millores importants per a la qualitat, el rendiment i la usabilitat. Aquest llançament és compatible amb el Dynamics 365 9.x. Per actualitzar a aquesta versió, visiteu el Centre d'administració del Dynamics 365 en línia i aneu a la pàgina de solucions per instal·lar l'actualització. Per obtenir més informació, vegeu [Instal·lar, actualitzar o eliminar una solució preferida](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

En aquest tema es mostren les característiques i correccions que són noves o s'han canviat per al Project Service Automation V3, versió d'actualització 18. Aquesta versió té el número de compilació V3.10.8.12 i està disponible de manera general a través d'una actualització automàtica l'abril de 2020.

## <a name="update-release-18"></a>Versió d'actualització 18

### <a name="bug-fixes"></a>Correccions d'errors

**Temps i despesa**

- Correcció: els fluxos **Recupera**, **Sol·licita** i **Cancel·la l'aprovació** generen excepcions amb missatges d'error poc clars.
- Correcció: quan **Cancel·la l'aprovació** no funciona amb una despesa, no es genera un error d'excepció rellevant.
- Correcció: la graella d'entrada de temps gestiona incorrectament els dies no laborables a Austràlia després del canvi a horari d'estiu (DST) a l'octubre.
- Correcció: la lògica per defecte incorrecta impedeix l'enviament de les despeses.
- Correcció: quan l'aprovació de l'entrada de temps no funciona, l'aprovació es manté en estat **Pendent**.
- Correcció: errors de l'SQL en l'aprovació massiva (bloqueig/expiració del temps d'espera).
- Correcció: problemes significatius de rendiment a l'experiència de l'usuari provocats per l'actualització dels membres de l'equip en aprovar les entrades de temps.

**Administració de projectes**

- Correcció: s'ha traslladat la notificació de fus horari de la visualització **Conciliació** al formulari principal del **Projecte**.
- Correcció: la plantilla de calendari no pren correctament el valor per defecte quan s'obre un nou formulari de projecte.
- Correcció: en els navegadors basats en Chromium, els usuaris no poden seleccionar fàcilment les tasques predecessores que s'han de suprimir.
- Correcció: la creació o la còpia d'un **Projecte des d'una plantilla buida** recupera assignacions no relacionades.
- Correcció: en alguns casos poc habituals específics, la creació d'una assignació nova des de la quadrícula de tasques provoca la creació de registres duplicats.
- Correcció: en el mode manual, els usuaris no poden actualitzar les dates d'inici de les tasques a una data posterior a la data desada actualment.

**Administració de recursos**

- Correcció: la fila de subtotal de la visualització **Conciliació** calcula incorrectament la diferència de reserves després d'ampliar les reserves.
- Correcció: la visualització **Conciliació** mostra incorrectament les assignacions de recursos quan el recurs reservable té un calendari que no coincideix amb el calendari del projecte.

**Sales**

- Correcció: quan es tornen a aprovar les entrades de temps (**Aprova > Cancel·la >** Torna a aprovar), es crea un valor real no imputable duplicat.
