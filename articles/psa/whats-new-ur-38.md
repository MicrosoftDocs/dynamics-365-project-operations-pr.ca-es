---
title: Novetats o canvis de la versió d'actualització 38 del Project Service Automation, V3
description: En aquest article s'enumeren les característiques i les correccions disponibles a la Versió 38 d'actualització Microsoft Dynamics 365 Project Service Automation, V3.
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

En aquest article es mostren les característiques i correccions que són noves o s'han canviat per al llançament de l'actualització 38, V3, de Project Service Automation. Aquesta versió té un número de compilació de V3.10.59.117 i està disponible de manera general a través d'una actualització d'autoservei al desembre de 2021.

## <a name="update-release-38"></a>Versió d'actualització 38

### <a name="bug-fixes"></a>Correccions d'errors

S'han corregit els problemes següents.

**Temps i despesa**

- Una excepció es produeix quan la longitud dels registres del conjunt d'aprovació supera els 100.000 registres.
- Els usuaris no poden accedir a la quadrícula **Entrada de temps** des de la pàgina principal d'**Entrada de temps**.
- El quadre de diàleg **Importació d'entrada de temps** no mostra cap text quan no es pot importar cap element.
- Els usuaris poden crear conjunts d'aprovació en què el camp **Estat de destinació** està definit com a **Desconegut**.

**Administració de projectes**

- Els contorns no es mostren correctament en les assignacions de recursos per a UTC (+09:30) i UTC (+10:00) quan s'inicia l'horari d'estiu.
- El camp **Columna addicional** per a les estructures desglossament del treball s'amaga en algunes configuracions regionals.
- El selector de dates del control de calendari a la quadrícula **Tasca de projecte** no està correctament localitzat per al xinès.

**Vendes**

- Els valors de **Rendiment del contracte** i **Cost real del projecte** no coincideixen quan els recursos que es poden reservar tenen entrades d'enviament de temps d'unitats de contracte i monedes diferents.
- Un flux de treball personalitzat per confirmar automàticament les factures falla quan les factures s'importen com una solució administrada. Es mostra el missatge següent: "Microsoft.Xrm.Sdk.InvalidPluginExecutionException Message: Estat de la factura no vàlid".
- Quan se selecciona **Arrel** com l'opció de resum i el projecte té estimacions d'una barreja de classes de transaccions (per exemple, una combinació de temps, despesa i estimacions de materials), el sistema resumeix totes les classes de transaccions com una sola línia de tarifa.
- Als escenaris en què s'afegeix una línia de despesa abans que s'associï una línia de contracte amb un projecte, els preus correctes no s'introdueixen com a valor per defecte al camp **Actualitza el preu**.
- No es permeten els imports de vendes negatius a les entitats **Projecte** i **Tasca**.
