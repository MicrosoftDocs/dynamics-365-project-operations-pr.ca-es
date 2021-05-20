---
title: Novetats o canvis de la versió d'actualització 24 del Project Service Automation, V3
description: En aquest tema es mostren les característiques i correccions disponibles al Project Service Automation V3, versió d'actualització 24.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 10/02/2020
ms.topic: article
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 956dcd2a06fad1eec488ad81bec2de4bd0550e82
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948903"
---
# <a name="project-service-automation-update-release-24-v3"></a>Project Service Automation, versió d'actualització 24, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Estem encantats d'anunciar-vos l'última actualització per a l'aplicació Project Service Automation per al Dynamics 365. Aquesta versió inclou algunes millores importants per a la qualitat, el rendiment i la usabilitat. Aquest llançament és compatible amb el Dynamics 365 9.x. Per actualitzar a aquesta versió, visiteu el Centre d'administració del Dynamics 365 en línia i aneu a la pàgina de solucions per instal·lar l'actualització. Per obtenir més informació, vegeu [Instal·lar, actualitzar o eliminar una solució preferida](/power-platform/admin/install-remove-preferred-solution).

En aquest tema es mostren les característiques i correccions que són noves o s'han canviat per al Project Service Automation V3, versió d'actualització 24. Aquesta versió té el número de compilació V3.10.42.43 i està disponible de forma general a través d'una actualització automàtica l'octubre de 2020.

## <a name="update-release-24"></a>Versió d'actualització 24

### <a name="bug-fixes"></a>Correccions d'errors

**Sales**

S'han corregit els problemes següents:

- Problema en definir la llista de preus per defecte dels productes.
- El rendiment en guanyar una oferta és lent a causa de la llista de preus incrustada i la còpia dels registres de preu per funció.
- **Contracte del projecte/Centre de vendes** > **Element de la línia de productes/Quantitat de la línia de comanda** s'arrodoneix automàticament a l'enter més proper.
- S'eleven els privilegis del sistema en llegir llistes de preus.
- Es copien els camps d'adreça del client **address1_freighttermscode** i **address1_shippingmethodcode** a l'oferta o la comanda. 


**Temps i despesa**

S'han corregit els problemes següents:

- La **quadrícula d'entrada de temps** no admet el comportament de temps **Només data**.
- **L'entrada de temps** no s'actualitza automàticament. Es necessita una actualització manual.
- No es poden importar les entrades de temps d'una assignació quan hi ha una pausa (0 hores) a les assignacions d'un recurs.
- Quan creeu una entrada de temps, definiu la data d'inici al mateix valor que **msdyn_date**.
- Torna a habilitar l'edició massiva per a l'entrada de temps.

**Administració de recursos**

S'han corregit els problemes següents:

- En provar d'actualitzar l'estat d'una reserva entre dies sense un requisit, es generarà una excepció de referència nul·la.
- Error en carregar la **visualització de conciliació**.


**Administració de projectes**

S'han corregit els problemes següents:

- A la **planificació del projecte**, quan es canvia de **Manual** a **Automàtic**, el desament automàtic no finalitza.
- Els costos de despesa no s'han de calcular cap a la variació a la **quadrícula de seguiment del projecte**.
- Comportament incoherent per a les columnes **Etiqueta d'estimació** durant la càrrega en comparació amb el canvi del tipus de **fase de temps**.
- Pot ser que el cost real d'un projecte no reflecteixi els totals dels **valors reals**.
- La **data de finalització aproximada** a la pestanya **Resum** no coincideix amb la **planificació de WBS**.
- **Actualitza les hores reals** en la sagnia no funciona correctament.
- Un administrador de projectes fora de la **unitat de negoci** arrel no pot crear un projecte.
- Els canvis a les tasques o categories a **Estimacions de despesa** no són persistents.
- **Còpia del contracte** copia les planificacions de factura i l'estat d'execució.
- El botó **Actualitza els valors reals** calcula incorrectament les tasques de resum.
- Complement del Microsoft Project: s'ha esmenat l'error de referència nul·la si un membre de l'equip té una unitat de recursos buida.



[!INCLUDE[footer-include](../includes/footer-banner.md)]