---
title: Novetats o canvis de la versió d'actualització 33 del Project Service Automation, V3
description: En aquest article s'enumeren les característiques i les correccions que estan disponibles a la versió 33, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/30/2021
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
ms.openlocfilehash: d9c282e8b95b111ce71fb441e4dbb2d04f904e0f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915402"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-33-v3"></a>Novetats o canvis de la versió d'actualització 33 del Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Ens complau anunciar l'última actualització de l'aplicació Microsoft Dynamics 365 Project Service Automation. Aquesta versió inclou algunes millores importants per a la qualitat, el rendiment i la usabilitat. És compatible amb el Dynamics 365 9.x. Per actualitzar aquesta versió, visiteu la pàgina de solucions en línia del Centre d'administració del Dynamics 365 i instal·leu l'actualització. Per obtenir més informació, vegeu [Instal·lar, actualitzar o eliminar una solució preferida](/power-platform/admin/install-remove-preferred-solution).

En aquest article s'enumeren les característiques i les correccions que són noves o canviades per al Project Service Automation V3, Update Release 33. Aquesta versió té el número de versió V3.10.54.98 i està disponible de forma general mitjançant una autoactualització el juliol de 2021.

## <a name="update-release-33"></a>Versió d'actualització 33

### <a name="bug-fixes"></a>Correccions d'errors

**Temps i despesa**

S'han corregit els problemes següents:

- Dos camps bloquejats, **msdyn_description** i **msdyn_externaldescription** es poden editar després de l'enviament.
- Es mostra un missatge d'error si es crea una despesa que no està relacionada amb un projecte.
- Quan es crea una entrada d'hora, la funció del recurs canvia per defecte a una funció inactiva.
- Les línies del llibre diari associades a una despesa recuperada i suprimida no s'eliminen.
- Al **Formulari de creació ràpida d'entrades de temps**, actualitzeu la visualització **Llista de tasques del projecte** per canviar la data visualitzada per defecte com a data d'inici de la tasca.
- Quan creeu una entrada de temps des de la pestanya **Relacionat** del recurs que es pot reservar, l'entrada de temps no es crea correctament per a l'usuari que ha iniciat la sessió en comptes del recurs principal que es pot reservar.
- S'afegeixen camps nous al quadre de diàleg **MDD d'aprovació massiva**.

**Planificació del projecte**

S'han corregit els problemes següents:
- El rendiment de creació de projectes s'alenteix quan les plantilles d'hores de feina del projecte s'apliquen a calendaris complexos.
- Quan la data d'inici és posterior a la data de finalització, es visualitza un error a la plantilla del projecte de còpia a causa de les diferències en el component horari de cada camp.

**Administració de recursos**

S'han corregit els problemes següents:
- S'utilitza un paràmetre incorrecte a la consulta d'ús del recurs i els clients potencials XML per filtrar incorrectament resultats a la quadrícula **Ús de recurs**.
- La confirmació **Amplia les reserves** mostra una data de finalització incorrecta per a les reserves.

**Vendes**

S'han corregit els problemes següents:
- Es mostra un missatge d'error si es crea un preu de categoria on falten valors.
- Es mostra un missatge d'error si es crea una fita de línia de contracte sense una línia de comanda.
