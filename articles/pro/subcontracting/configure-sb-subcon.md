---
title: Configurar el tauler de planificació per mostrar els empleats del contracte i la capacitat subcontractada
description: En aquest article es descriu com configurar el Tauler de planificació a Microsoft Dynamics 365 Project Operations per mostrar la capacitat de recursos subcontractats quan es compleixen els requisits de recursos del projecte.
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

El tauler de planificació a Microsoft Dynamics 365 Project Operations es pot utilitzar per cercar recursos de dues maneres:

- Cerca general de recursos sense el context de cap requisit específic de recurs basat en projectes.
- Cerca de recursos específics per a requisits on el requisit del projecte proporcionarà el context dels recursos suggerits.

Per notificar al tauler d'horaris la capacitat de recursos subcontractats i els treballadors contractats, heu de fer actualitzacions a la configuració del tauler de planificació. Aquestes actualitzacions inclouen: 
- Actualitzeu la configuració del tauler de planificació per a la cerca general de recursos.
- Actualització de la configuració del tauler de planificació per a la cerca de recursos basada en requisits.

## <a name="update-schedule-board-settings-for-general-resource-search"></a>Actualització de la configuració del tauler de planificació per a la cerca general de recursos
### <a name="update-filters-for-general-resource-search"></a>Actualitzar els filtres per a la cerca general de recursos
Quan cerqueu un recurs, els filtres disponibles al tauler de planificació s'han d'actualitzar de manera que també pugueu cercar recursos externs especificant algun o tots els elements següents:
  - Tipus de treballador, tant si els recursos mostrats han de ser treballadors contractats com treballadors per compte d'altri.
  - Empresa venedora a la qual hauria de pertànyer un recurs.
  - Recursos que pertanyen a una línia específica de subcontractació o subcontractació.
    
### <a name="update-retrieve-resource-query"></a>Actualitzar recuperar la consulta del recurs
La consulta utilitzada per a la cerca també s'ha d'actualitzar per utilitzar aquests atributs de filtre addicionals. Utilitzeu els passos següents per actualitzar la configuració del tauler de planificació per a la cerca general de recursos:  
1. Obriu **configuració del tauler de planificació** per a un tauler de planificació específic.
2. Obriu la **pestanya Configuració** general i desplaceu-vos fins a **Altres configuracions**.
3. A la llista de paràmetres d'aquesta secció, actualitzeu la disposició del filtre a **la** **disposició del filtre per defecte per al Project Operations Lite**.
4. Update **Retrieve Resources Query** to **Default Retrieve Resources Query for Project Operations Lite**.

![Actualització de la configuració del tauler de planificació per a la cerca general de recursos](../media/BoardSettings.png)  

## <a name="update-schedule-board-settings-for-requirementbased-resource-search"></a>Actualització de la configuració del tauler de planificació per a la cerca de recursos basada en requisits
### <a name="update-filters-for-requirement-specific-resource-search"></a>Actualitzar els filtres per a la cerca de recursos específics de requisits 
Quan cerqueu un recurs, els filtres disponibles al tauler de planificació s'han d'actualitzar de manera que també pugueu cercar recursos externs especificant algun o tots els elements següents:
 - Tipus de treballador, tant si els recursos mostrats han de ser treballadors contractats com treballadors per compte d'altri.
 - Empresa venedora a la qual hauria de pertànyer un recurs.
 - Recursos que pertanyen a una línia específica de subcontractació o subcontractació.

### <a name="update-retrieve-resource-query-for-requirement-specific-resource-search"></a>Update retrieve resource query per a la cerca de recursos específics del requisit 
La consulta utilitzada per a la cerca també s'ha d'actualitzar per utilitzar aquests atributs de filtre addicionals. Utilitzeu els passos següents per actualitzar la configuració del tauler de planificació per a la cerca de recursos basada en requisits:

1. Obriu **Configuració del tauler de** planificació per a un tauler de planificació específic i, a continuació, seleccioneu **Obre la configuració** per defecte per obrir la configuració per a la cerca específica dels requisits.
2. Obriu la **pestanya Configuració** general i desplaceu-vos fins a **Altres configuracions**.
3. A la llista de paràmetres d'aquesta secció, actualitzeu la disposició del filtre a **la** **disposició del filtre per defecte per al Project Operations Lite**.
4. Update **Retrieve Resources Query** to **Default Retrieve Resources Query for Project Operations Lite**.
5. Obriu la **pestanya Tipus de** planificació i aneu a **Projecte**.
6. A la configuració del projecte, actualitzeu **l'Assistent** de planificació Recupereu la consulta **de recursos a la consulta de recursos de recuperació per defecte per al** Project Operations Lite **i actualitzeu** l'Assistent de planificació Recupereu restriccions Consulta **per defecte per a** les operacions del Projecte Lite **.**

![Actualització de la configuració del tauler de planificació per a la cerca de recursos basada en requisits](../media/SASettings.png)  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
