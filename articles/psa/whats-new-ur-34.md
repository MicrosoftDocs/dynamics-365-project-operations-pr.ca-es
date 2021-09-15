---
title: Novetats o canvis de la versió d'actualització 34 del Project Service Automation, V3
description: En aquest tema es mostren les característiques i correccions disponibles al Project Service Automation V3, versió d'actualització 34.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 08/05/2021
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
ms.openlocfilehash: 1c8ef43b953ad282a1f5fed6eeeb1e1a991e715100b66938be03b5b5f3da575e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "7009744"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-34-v3"></a>Novetats o canvis de la versió d'actualització 34 del Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Ens complau anunciar l'última actualització de l'aplicació Microsoft Dynamics 365 Project Service Automation. Aquesta versió inclou algunes millores importants per a la qualitat, el rendiment i la usabilitat. És compatible amb el Dynamics 365 9.x. Per actualitzar aquesta versió, visiteu la pàgina de solucions en línia del Centre d'administració del Dynamics 365 i instal·leu l'actualització. Per obtenir més informació, vegeu [Instal·lar, actualitzar o eliminar una solució preferida](/power-platform/admin/install-remove-preferred-solution).

En aquest tema es mostren les característiques i correccions que són noves o s'han canviat per al Project Service Automation V3, versió d'actualització 34. Aquesta versió té el número de versió V3.10.55.38 i està disponible de forma general mitjançant una autoactualització el juliol de 2021.

## <a name="update-release-34"></a>Versió d'actualització 34

### <a name="bug-fixes"></a>Correccions d'errors
S'han corregit els problemes següents.

**General**

- Les actualitzacions impulsades pels editors no activen el nou flux de treball d'aprovació modern.
- Falten els atributs **Estat de destinació** i **Tipus d'acció** a la pàgina principal **Conjunt d'aprovació**.

**Temps i despesa**

- No es pot aprovar una sol·licitud de recuperació utilitzant el flux d'aprovació modern.
- Copiar una setmana d'entrades de temps no funciona quan es copien entrades que no estan relacionades amb l'usuari que ha iniciat la sessió.

**Planificació del projecte**

- Els contorns d'assignació de recursos estan malmesos en importar des del complement d'escriptori del Microsoft Project.

**Administració de recursos**

- Quan publiqueu un projecte des del complement del client d'escriptori del Microsoft Project, es canvia la data d'acabament dels requisits existents.
- La precisió decimal supera les dues posicions decimals al quadre de diàleg Amplia la confirmació de reserves.

**Vendes**

- Quan afegiu una línia basada en productes amb un producte existent a un contracte de projecte, es mostrarà una execpció **No es troba la clau al diccionari**.
- Els clients potencials no es poden qualificar quan un tipus de comanda s'assigna d'un client potencial a una oportunitat.