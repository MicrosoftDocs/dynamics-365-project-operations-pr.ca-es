---
title: Novetats o canvis de la versió d'actualització 15 del Project Service Automation, V3
description: En aquest article s'ofereix informació sobre les novetats de la versió 15, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/27/2020
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
ms.openlocfilehash: b87cae2cd8913457c2931d1661a57509d1398d29
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915632"
---
# <a name="project-service-automation-update-release-15-v3"></a>Project Service Automation, versió d'actualització 15, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Ens complau anunciar la darrera actualització de l'aplicació Dynamics 365 Project Service Automation (PSA). Aquesta versió inclou algunes millores importants per a la qualitat, el rendiment i la usabilitat. Aquest llançament és compatible amb el Dynamics 365 9.x. Per actualitzar a aquesta versió, visiteu el Centre d'administració del Dynamics 365 en línia i aneu a la pàgina de solucions per instal·lar l'actualització. Per obtenir més informació, vegeu [Instal·lar, actualitzar o eliminar una solució preferida](/power-platform/admin/install-remove-preferred-solution).

En aquest article s'enumeren les característiques i correccions que són noves o canviades per pSA V3, Actualització versió 15. Aquesta versió té el número de compilació V3.10.5.28 i està disponible de forma general a través d'una actualització automàtica el gener de 2020.

## <a name="update-release-15"></a>Versió d'actualització 15 

### <a name="enhancements"></a>Millores

- Administració de projectes

### <a name="bug-fixes"></a>Correccions d'errors

- Temps i despesa

  - Correcció: s'ha afegit la gestió d'errors durant la càrrega a la visualització de conciliació.
  - Correcció: Centre de recursos del projecte: s'ha canviat el nom d'**Import** per reduir la ambigüitat.
  - Correcció: s'ha ajustat la visualització **Copia les columnes d'entrada de temps** per incloure el tipus.
  - Correcció: l'edició de la duració d'una entrada de temps a la visualització de quadrícula utilitzant nombres decimals resulta en un error desconegut per a alguns nombres.

- Administració de projectes

  - Correcció: el menú desplegable per a **Utilitza la visualització de seguiment** ara s'amplia en funció de l'amplada de les opcions.
  - Correcció: en administrar projectes al fus horari +13, els càlculs de tasques poden mostrar resultats correctes.
  - Correcció: el **Temps de finalització del membre de l'equip** s'ha corregit en utilitzar un calendari de 24 hores.
  - Correcció: s'ha tornat a activar el **BPF** en el formulari principal **msdyn_project**.
  - Correcció: el càlcul de les assignacions ja no ignora un dia.
  - Correcció: s'ha afegit un nou bàner de notificació al formulari del projecte quan el fus horari és diferent entre l'usuari i el projecte.

- Sales

  - Correcció: la cerca d'una categoria d'estimació de despeses es pot utilitzar per filtrar duplicats.
  - Correcció: el codi a **PluginDomain.ExecuteInTryCatchBlock(..)** ja no amaga l'origen de l'excepció.
  - Correcció: ja no s'obté cap missatge d'error a **Cerca de projectes** al formulari **Línia d'oferta** quan hi ha més de 1000 projectes.
  - Correcció: la quadrícula **Estimacions** per a estimacions de treball i estimacions de despesa ara mostra el símbol monetari correcte.
  - Correcció: després de l'actualització per part d'una organització del PSA de la versió d'actualització 14 a la versió d'actualització 15, la pestanya **Planificació** ja no apareix a en blanc al formulari **Projecte**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
