---
title: Novetats o canvis de la versió d'actualització 38 del Project Service Automation, V3
description: En aquest article s'enumeren les característiques i les correccions que estan disponibles a Microsoft Dynamics 365 Project Service Automation Update Release 38, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 12/06/2021
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
ms.openlocfilehash: ccc08cd0bc365bd4761424a4c0ceac91985e7c89
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915173"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-38-v3"></a>Novetats o canvis de la versió d'actualització 38 del Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Ens complau anunciar l'última actualització de l'aplicació Microsoft Dynamics 365 Project Service Automation. Aquesta versió inclou algunes millores importants per a la qualitat, el rendiment i la usabilitat. És compatible amb el Dynamics 365 9.x. Per actualitzar aquesta versió, visiteu la pàgina de solucions en línia del Centre d'administració del Dynamics 365 i instal·leu l'actualització. Per obtenir més informació, vegeu [Instal·lar, actualitzar o eliminar una solució preferida](/power-platform/admin/install-remove-preferred-solution).

En aquest article s'enumeren les característiques i les correccions que són noves o canviades per a la versió 38, V3. Aquesta versió té un número de compilació de V3.10.59.117 i està disponible de manera general a través d'una actualització d'autoservei al desembre de 2021.

## <a name="update-release-38"></a>Versió d'actualització 38

### <a name="bug-fixes"></a>Correccions d'errors

S'han corregit els problemes següents.

**Temps i despesa**

- Una excepció es produeix quan la longitud dels registres del conjunt d'aprovació supera els 100.000 registres.
- Els usuaris no poden accedir a la **quadrícula d'entrada** de temps des de la pàgina principal de l'entrada **de l'hora**.
- El **quadre de diàleg Importació d'entrades** d'hora no mostra cap text quan no hi ha elements aptes per a la importació.
- Els usuaris poden crear conjunts d'aprovació on el camp Estat de **destinació** està definit com a **Desconegut**.

**Administració de projectes**

- Els contorns no es mostren correctament a les assignacions de recursos per a UTC(+09:30) i UTC(+10:00) quan s'inicia l'horari d'estiu.
- El **camp Columna** addicional per a les estructures de desglossament de treball està amagat en alguns llocs.
- El selectador de dates per al control de calendari a la quadrícula Tasques **del** projecte no està localitzat correctament per al xinès.

**Vendes**

- **Els valors rendiment del** contracte i **cost** real del projecte no coincideixen quan els recursos que es poden reservar que tenen diferents unitats de contractació i monedes envien entrades de temps.
- Un flux de treball personalitzat per confirmar automàticament les factures falla quan les factures s'importen com a solució administrada. Es mostra el missatge següent: "Microsoft.Xrm.Sdk.InvalidPluginExecutionException Message: Estat de la factura no vàlid".
- Quan **Root** és seleccionat com l'opció de resum, i el projecte té estimacions d'una barreja de classes de transaccions (per exemple, una combinació de temps, despesa i estimacions de materials), el sistema es resumeix entre les classes de transaccions com una sola línia de tarifa.
- En els escenaris en què s'afegeix una línia de despeses abans que una línia de contracte s'associï amb un projecte, el preu correcte no s'introdueix com a valor per defecte al camp Actualitza el **preu**.
- No es permeten quantitats de vendes negatives a les **entitats projecte** i **tasca**.
