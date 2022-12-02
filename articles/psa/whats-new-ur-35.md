---
title: Novetats o canvis de la versió d'actualització 35 del Project Service Automation, V3
description: En aquest article s'enumeren les característiques i les correccions disponibles a la Versió 35 d'actualització Microsoft Dynamics 365 Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 09/03/2021
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
ms.openlocfilehash: 28b4a5ccbfff83c9b1a18cb0b4062af9cdaf8f6e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912826"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-35-v3"></a>Novetats o canvis de la versió d'actualització 35 del Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Ens complau anunciar l'última actualització de l'aplicació Microsoft Dynamics 365 Project Service Automation. Aquesta versió inclou algunes millores importants per a la qualitat, el rendiment i la usabilitat. És compatible amb el Dynamics 365 9.x. Per actualitzar aquesta versió, visiteu la pàgina de solucions en línia del Centre d'administració del Dynamics 365 i instal·leu l'actualització. Per obtenir més informació, vegeu [Instal·lar, actualitzar o eliminar una solució preferida](/power-platform/admin/install-remove-preferred-solution).

En aquest article es mostren les característiques i correccions que són noves o s'han canviat per al llançament de l'actualització 35, V3, de Project Service Automation. Aquesta versió té el número de versió V3.10.56.110 i està disponible de forma general mitjançant una autoactualització el setembre de 2021.

## <a name="update-release-35"></a>Versió d'actualització 35

### <a name="bug-fixes"></a>Correccions d'errors

S'han corregit els problemes següents.

**Temps i despesa**

- L'aprovador del projecte rep un error de privilegis de lectura quan aproven les entrades de despeses amb una funció d'**Aprovador del projecte**.
- L'aprovador del projecte rep un error de privilegi d'escriptura a **msdyn_projectapproval** quan cancel·len una entrada de temps aprovada amb una funció d'**Aprovador del projecte**.
- Quan seleccioneu **Copia la setmana** en una entrada d'hora al mòdul de l'aplicació Dynamics 365 per a telèfons - Centre de recursos del projecte, es produeix l'error següent: "...\OfficeProductivity_RibbonRules.js.map: error HTTP: codi d'estat 404, xarxa::ERR_HTTP_RESPONSE_CODE_FAILURE".
- La política de **Reintent** aprova automàticament les entrades que s'han rebutjat anteriorment.
- La subquadrícula **Conjunts d'aprovació** mostra accions de la franja que no són aplicables.
- Falten icones per a la funció **Tasca del projecte** i **Recurs del projecte** a l'entitat **Entrada de temps**.
- Quan importeu assignacions de recursos, les entrades de temps importades no tenen la durada correcta per a les assignacions creades a través de les tasques en mode manual.
- Falta **Suprimeix** a la pàgina **Cerca avançada per a registres d'entrada de temps**.
- Falta **Desa** a la pàgina **Informació d'entrada de temps**. Aquest problema evita que es desin els canvis quan es tanca la pàgina.

**Planificació del projecte**

- Les quadrícules **Assignació de recursos** i **Reconciliació de recursos** no ordenen els atributs agrupats alfabèticament.
- Les tasques no es poden crear si el comportament de les dates està personalitzat en **Només data**.

**Administració de recursos**

- Si tant el Dynamics 365 Field Service com el Project Service Automation estan instal·lats, es produeixen problemes de superposició quan la **Visualització associada de requisit de recursos** està associada a una pàgina principal.
- Si feu doble clic a **Desa** al quadre de diàleg **Creació ràpida de membre de l'equip**, no es pot crear el requisit de recursos.

**Vendes**

- Es llança una excepció si suprimiu una tasca associada amb una oferta amb l'estat **Guanyada**.
