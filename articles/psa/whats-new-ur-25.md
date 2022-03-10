---
title: Novetats o canvis de la versió d'actualització 25 del Project Service Automation, V3
description: En aquest tema es mostren les característiques i correccions disponibles al Project Service Automation V3, versió d'actualització 25.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/26/2020
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
ms.openlocfilehash: 9d8ac559be2c23396604c61caae83c8a5328869d76218c6d8b3b6a6a6b32c1eb
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6996559"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-25-v3"></a>Novetats o canvis de la versió d'actualització 25 del Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Estem encantats d'anunciar-vos l'última actualització per a l'aplicació Project Service Automation per al Dynamics 365. Aquesta versió inclou algunes millores importants per a la qualitat, el rendiment i la usabilitat. Aquest llançament és compatible amb el Dynamics 365 9.x. Per actualitzar a aquesta versió, visiteu el Centre d'administració del Dynamics 365 en línia i aneu a la pàgina de solucions per instal·lar l'actualització. Per obtenir més informació, vegeu [Instal·lar, actualitzar o eliminar una solució preferida](/power-platform/admin/install-remove-preferred-solution).

Aquest tema enumera les característiques i correccions noves o canviades per al Project Service Automation V3, llançament d'actualització 25 Aquesta versió té el número de compilació V3.10.43.76 i està disponible de manera general a través d'una actualització autoservei l'octubre de 2020.

## <a name="update-release-25"></a>Versió d'actualització 25

### <a name="bug-fixes"></a>Correccions d'errors

**Temps i despesa**

S'ha corregit el problema següent:

- El gràfic d'entrada de temps mostra dades addicionals si es recupera un interval massa gran.

**Administració de recursos**

S'ha corregit el problema següent:

- S'ha afegit codi al Package Deployer per ometre la importació de pedaços de l'Universal Resource Scheduling si ja existeix un pedaç de versió superior.

**Administració de projectes**

S'han corregit els problemes següents:

- S'han corregit discrepàncies d'arrodoniment i tipus de canvi que provocaven un cost planificat incorrecte a la quadrícula de seguiment del projecte.
- S'admet la possibilitat de mostrar dues o més quadrícules de reacció al formulari **Projecte**.
- Es proporciona validació per abordar la possibilitat d'assignar una tasca més enllà de la data de finalització del calendari, que provoca una assignació de recursos amb errors.
- Millora de la gestió d'errors per fer front a l'excepció de referència nul·la generada a partir del següent:

    - Connector **PreValidateProjectTeamMemberCreate**
    - **PreValidateProjectTaskCreate** quan es crea una tasca de projecte sense un projecte associat
    - Connector **PreProjectTeamMemberCreate**
    - Connector **PostProjectTeamMemberDelete**
    - Connector **PreValidateProjectTaskDelete**

**Sales**

S'han corregit els problemes següents:

- Millora de la gestió d'errors per fer front a les excepcions de referència nul·la generades a partir de **Copia el projecte: estimació de l'administració de HelperResource**.
- **No està a punt per facturar** un **registre de facturació de temps i material** no esborra l'estat de facturació.
- S'han corregit els botons de **preus** mal etiquetats a la pestanya **Preu per funció** i **Articles del catàleg**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]