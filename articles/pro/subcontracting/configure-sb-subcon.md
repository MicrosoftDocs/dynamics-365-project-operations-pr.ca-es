---
title: Configurar el tauler de planificació per mostrar els empleats del contracte i la capacitat subcontractada
description: En aquest article es descriu com es configura el Tauler de planificació al Microsoft Dynamics 365 Project Operations per mostrar la capacitat dels recursos subcontractats quan es cobreixin els requisits de recursos del projecte.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 355691b63f437de789afab499369afcdf87e6d3d
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 08/11/2022
ms.locfileid: "9262204"
---
# <a name="configure-schedule-board-to-show-contract-workers-and-subcontracted-capacity"></a>Configurar el tauler de planificació per mostrar els empleats del contracte i la capacitat subcontractada 

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_

El Tauler de planificació del Microsoft Dynamics 365 Project Operations es pot utilitzar per cercar recursos de dues maneres:

- Cerca de recursos general sense el context de cap requisit de recursos basat en projectes específic.
- Cerca de recursos específica del requisit on el requisit del projecte proporcionarà el context dels recursos suggerits.

Per notificar el tauler de planificació de capacitat de recursos subcontractats i empleats contractats, heu de fer actualitzacions a la configuració del Tauler de planificació. Aquestes actualitzacions inclouen: 
- Actualitzar la configuració del Tauler de planificació per a la cerca de recursos generals.
- Actualitzar la configuració del Tauler de planificació per a la cerca de recursos basada en requisits.

## <a name="update-schedule-board-settings-for-general-resource-search"></a>Actualitzar la configuració del Tauler de planificació per a la cerca de recursos generals
### <a name="update-filters-for-general-resource-search"></a>Actualitzar els filtres per a la cerca de recursos generals
Quan cerqueu un recurs, els filtres disponibles al tauler de planificació s'han d'actualitzar per tal que també pugueu cercar recursos externs especificant qualsevol o totes les opcions següents:
  - Tipus de treballador, si els recursos que es mostren han de ser empleats o empleats de contracte.
  - Empresa del proveïdor a la ha de pertànyer el recurs.
  - Recursos que pertanyen a una línia de subcontracte o subcontracte específics.
    
### <a name="update-retrieve-resource-query"></a>Actualitzar la consulta de recuperació de recurs
La consulta que s'utilitza per cercar també s'ha d'actualitzar per utilitzar aquests atributs de filtre addicionals. Seguiu els passos següents per actualitzar la configuració del Tauler de planificació per a la cerca de recursos general:  
1. Obriu la **Configuració del Tauler de planificació** d'un Tauler de planificació específic.
2. Obriu la pestanya **Configuració general** i desplaceu-vos fins a **Altres configuracions**.
3. A la llista de configuracions d'aquesta secció, actualitzeu la **Disposició de filtres** a la **Disposició de filtres per defecte per al Project Operations Lite**.
4. Actualitzeu la **Consulta per recuperar recursos** a **Consulta per recuperar recursos per defecte per al Project Operations Lite**.

![Actualitzar la configuració del Tauler de planificació per a la cerca de recursos generals](../media/BoardSettings.png)  

## <a name="update-schedule-board-settings-for-requirementbased-resource-search"></a>Actualitzar la configuració del Tauler de planificació per a la cerca de recursos basada en requisits
### <a name="update-filters-for-requirement-specific-resource-search"></a>Actualitzar els filtres per a la cerca de recursos específica de requisit 
Quan cerqueu un recurs, els filtres disponibles al tauler de planificació s'han d'actualitzar per tal que també pugueu cercar recursos externs especificant qualsevol o totes les opcions següents:
 - Tipus de treballador, si els recursos que es mostren han de ser empleats o empleats de contracte.
 - Empresa del proveïdor a la ha de pertànyer el recurs.
 - Recursos que pertanyen a una línia de subcontracte o subcontracte específics.

### <a name="update-retrieve-resource-query-for-requirement-specific-resource-search"></a>Actualitzar la consulta de recuperació de recursos per a la cerca de recursos específica de requisit 
La consulta que s'utilitza per cercar també s'ha d'actualitzar per utilitzar aquests atributs de filtre addicionals. Seguiu els passos següents per actualitzar la configuració del Tauler de planificació per a la cerca de recursos basada en requisit:

1. Obriu la **Configuració del Tauler de planificació** d'un Tauler de planificació específic i, a continuació, seleccioneu **Obre la configuració per defecte** per obrir la configuració de la cerca específica de requisits.
2. Obriu la pestanya **Configuració general** i desplaceu-vos fins a **Altres configuracions**.
3. A la llista de configuracions d'aquesta secció, actualitzeu la **Disposició de filtres** a la **Disposició de filtres per defecte per al Project Operations Lite**.
4. Actualitzeu la **Consulta per recuperar recursos** a **Consulta per recuperar recursos per defecte per al Project Operations Lite**.
5. Obriu la pestanya **Tipus de planificació** i aneu a **Projecte**.
6. A la configuració de **Projecte**, actualitzeu l'**Auxiliar de planificació Consulta per recuperar recursos** a **Consulta per recuperar recursos per defecte del Project Operations Lite** i actualitzeu **Auxiliar de planificació Consulta de limitacions de recuperació** a **Consulta de limitacions de recuperació per defecte del Project Operations Lite**.

![Actualitzar la configuració del Tauler de planificació per a la cerca de recursos basada en requisits](../media/SASettings.png)  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
