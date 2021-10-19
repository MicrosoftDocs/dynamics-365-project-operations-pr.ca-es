---
title: Novetats o canvis de la versió d'actualització 36 del Project Service Automation, V3
description: En aquest tema s'enumeren les característiques i les correccions disponibles a la Versió 36 d'actualització Microsoft Dynamics 365 Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/06/2021
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
ms.openlocfilehash: 9b85aed79acb7e7784a23f54a2e9af1cc83f5f4d
ms.sourcegitcommit: 6d9fc4dc851814664bf71729904ab4bedd85fe70
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/06/2021
ms.locfileid: "7606725"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-36-v3"></a>Novetats o canvis de la versió d'actualització 36 del Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Ens complau anunciar l'última actualització de l'aplicació Microsoft Dynamics 365 Project Service Automation. Aquesta versió inclou algunes millores importants per a la qualitat, el rendiment i la usabilitat. És compatible amb el Dynamics 365 9.x. Per actualitzar aquesta versió, visiteu la pàgina de solucions en línia del Centre d'administració del Dynamics 365 i instal·leu l'actualització. Per obtenir més informació, vegeu [Instal·lar, actualitzar o eliminar una solució preferida](/power-platform/admin/install-remove-preferred-solution).

En aquest tema es mostren les característiques i correccions que són noves o s'han canviat per al llançament de l'actualització 36, V3, de Project Service Automation. Aquesta versió té el número de compilació V3.10.57.152 i està disponible de forma general a través d'una actualització automàtica l'octubre de 2021.

## <a name="update-release-36"></a>Versió d'actualització 36

### <a name="bug-fixes"></a>Correccions d'errors

S'han corregit els problemes següents.

**General**
- El nom del camp **Plantilla d'hora de treball per defecte** no està traduït correctament a la pàgina **Paràmetres del projecte**.
- Els complements asíncrons no gestionen correctament les excepcions relacionades amb **SharedVariableService**.

**Temps i despesa**
- Quan falten línies del llibre diari o l'usuari no té els privilegis correctes per llegir les línies del llibre diari, es produeix un error incorrecte quan es cancel·len les aprovacions del projecte.
- Els usuaris no poden cancel·lar una aprovació quan una despesa o una entrada de temps té més d'una aprovació de projecte associada.
- **Absència** i **Vacances** no estan traduïts correctament per a la llengua xinesa en una cerca de la pàgina de creació ràpida **Entrada de temps**.

**Administració de recursos**
- L'usuari no pot cercar recursos a l'**Auxiliar de planificació** quan el mode de visualització està definit com a **Dia**, **Setmana** o **Mes**.
- Es permet incorrectament que els recursos genèrics tinguin noms de posició buits. 
- El tancament d'un contracte com a perdut no cancel·la les reserves futures.

**Vendes**
- Quan un entorn té un gran volum de productes, el rendiment es degrada a la quadrícula **Estimació de materials**.
- En crear un projecte a partir d'una plantilla, la moneda del projecte no és per defecte la de la unitat de contracte de l'Administrador de projecte corresponent.
- Els imports reals no sempre coincideixen amb els que es reflecteixen en el venciment del projecte o els imports es converteixen en negatius en escenaris específics de retenció.
- Es produeix un error quan s'associa un projecte creat des de la plantilla de projecte a una línia de contracte.
- Els usuaris poden suprimir una línia de contracte amb les fites, **Preparat per facturar** i **Factura creada**. Això no s'hauria de permetre.
- Quan s'importen estimacions des d'un projecte, la capacitat de càrrega de detall de la línia d'oferta no es defineix correctament quan la facturació basada en tasques està habilitada per a la línia d'oferta.
- Quan s'afegeix una subquadrícula de facturació de preu fix, la fita no queda reflectida a la subquadrícula de fita fins que s'actualitza la pàgina.
- Es genera una excepció de referència nul·la quan es crea un contracte de projecte amb un nom d'oferta nul.
- Les tasques en mode manual en què la moneda del projecte és diferent de la moneda del recurs generen estimacions de preu incorrectes.
- Els usuaris no poden recuperar una transacció que s'ha corregit correctament amb una factura correctiva.
- Les categories de transacció desactivades apareixen a la quadrícula **Estimacions de despeses**.



