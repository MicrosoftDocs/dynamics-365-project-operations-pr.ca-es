---
title: Novetats o canvis de la versió d'actualització 31 del Project Service Automation, V3
description: En aquest tema es mostren les característiques i correccions disponibles al Project Service Automation V3, versió d'actualització 31.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/26/2021
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
ms.openlocfilehash: 160187ba7b96547e85a7a4ec4bf84c86d8fd8257
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999119"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-31-v3"></a>Novetats o canvis de la versió d'actualització 31 del Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Estem encantats d'anunciar-vos l'última actualització per a l'aplicació Project Service Automation per al Dynamics 365. Aquesta versió inclou algunes millores importants per a la qualitat, el rendiment i la usabilitat. Aquest llançament és compatible amb el Dynamics 365 9.x. Per actualitzar a aquesta versió, visiteu el Centre d'administració del Dynamics 365 en línia i aneu a la pàgina de solucions per instal·lar l'actualització. Per obtenir més informació, vegeu [Instal·lar, actualitzar o eliminar una solució preferida](/power-platform/admin/install-remove-preferred-solution).

En aquest tema es mostren les característiques i correccions que són noves o s'han canviat per al Project Service Automation V3, versió d'actualització 31. Aquesta versió té el número de compilació V3.10.52.77 i està disponible de manera general a través d'una actualització automàtica el maig de 2021.

## <a name="update-release-31"></a>Versió d'actualització 31

### <a name="bug-fixes"></a>Correccions d'errors

**Temps i despesa**

S'han corregit els problemes següents:

- Els botons de l'ordre control d'entrada de temps de la pàgina **Recurs que es pot reservar** eren confusos.
- Es generava una excepció de referència nul·la a **Project.SetTrackingFields** quan s'aprovava una entrada de temps.

**Administració de recursos**

S'han corregit els problemes següents:

- **Crea un membre de l'equip** no mostra correctament la configuració de les metadades de configuració de la reserva per a **Estat confirmat per defecte de la reserva**.
- Quan s'actualitza de PSA 1.X a 3.X, el procés d'actualització falla a **UpgradeResourceRequirements**.


**Vendes**

S'han corregit els problemes següents:

- Els ingressos reals converteixen els imports a la moneda del projecte a la quadrícula de seguiment.
- El valor per defecte de la moneda no està clar quan es creen línies del llibre diari, línies d'oferta i línies de contracte en casos en què la moneda base d'una organització és diferent de la moneda del projecte.
- La consulta **Validació del llibre diari de correcció pendent** no filtra per projecte.
- La resta de vendes no es calcula correctament en un projecte.
- Les ofertes basades en un contacte fallen quan es creen sense una llista de preus.
- No es mostra cap indicador giratori de processament quan seleccioneu **Confirma la factura**.
- No es mostra cap indicador giratori de processament quan seleccioneu **Crea la factura**.
- El tancament d'una oferta com a perduda no cancel·la les reserves.







