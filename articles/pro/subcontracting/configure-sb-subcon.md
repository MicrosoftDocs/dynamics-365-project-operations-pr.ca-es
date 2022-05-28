---
title: Configurar el tauler de planificació per mostrar els empleats del contracte i la capacitat subcontractada
description: Aquest tema descriu com configurar el Tauler de planificació a Microsoft Dynamics 365 Project Operations per mostrar la capacitat de recursos subcontractada quan es personalitza els requisits de recursos del projecte.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 6e382b33fafe91c8b96a91d033fe12b998114bdc
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8587804"
---
# <a name="configure-schedule-board-to-show-contract-workers-and-subcontracted-capacity"></a>Configurar el tauler de planificació per mostrar els empleats del contracte i la capacitat subcontractada 

[!include [banner](../../includes/dataverse-preview.md)]

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_

El Tauler de planificació de Microsoft Dynamics 365 Project Operations es pot utilitzar per cercar recursos de dues maneres:

- Cerca general de recursos sense el context de cap requisit específic de recursos basats en projectes.
- Cerca de recursos específics per a requisits on el requisit del projecte proporcionarà el context dels recursos suggerits.

Per notificar al tauler de planificació la capacitat de recursos subcontractada i els treballadors contractats, heu de fer actualitzacions de la configuració del Tauler de planificació. Aquestes actualitzacions inclouen: 
- Actualitza la configuració del Tauler de planificació per a la cerca general de recursos.
- Actualitza la configuració del Tauler de planificació per a la cerca de recursos basada en requisits.

## <a name="update-schedule-board-settings-for-general-resource-search"></a>Actualitza la configuració del Tauler de planificació per a la cerca general de recursos
### <a name="update-filters-for-general-resource-search"></a>Actualitza els filtres per a la cerca general de recursos
Quan cerqueu un recurs, els filtres disponibles al tauler de planificació s'han d'actualitzar perquè també pugueu cercar recursos externs especificant qualsevol o tots els següents:
  - Tipus de treballador, si els recursos mostrats han de ser treballadors contractats o empleats.
  - Empresa venedora a la qual ha de pertànyer un recurs.
  - Recursos que pertanyen a una línia específica de subcontractació o subcontractació.
    
### <a name="update-retrieve-resource-query"></a>Actualitza la consulta de recursos de recuperació
La consulta utilitzada per a la cerca també s'ha d'actualitzar per utilitzar aquests atributs de filtre addicionals. Utilitzeu els passos següents per actualitzar la configuració del Tauler de planificació per a la cerca general de recursos:  
1. Obre **la configuració del tauler de planificació** per a un tauler de planificació específic.
2. Obriu la **pestanya Configuració general i desplaceu-vos** fins a **Altres opcions de configuració**.
3. A la llista de paràmetres d'aquesta secció, actualitzeu la disposició del filtre a la **disposició** de filtre per defecte per al Lite d'operacions del projecte **.**
4. Actualitza recupera **la consulta** de recursos per recuperar la **consulta de recursos per defecte per al Lite** d'operacions del projecte.

![Actualitza la configuració del Tauler de planificació per a la cerca general de recursos](../media/BoardSettings.png)  

## <a name="update-schedule-board-settings-for-requirementbased-resource-search"></a>Actualitza la configuració del Tauler de planificació per a la cerca de recursos basada en requisits
### <a name="update-filters-for-requirement-specific-resource-search"></a>Actualitza els filtres per a la cerca de recursos específics dels requisits 
Quan cerqueu un recurs, els filtres disponibles al tauler de planificació s'han d'actualitzar perquè també pugueu cercar recursos externs especificant qualsevol o tots els següents:
 - Tipus de treballador, si els recursos mostrats han de ser treballadors contractats o empleats.
 - Empresa venedora a la qual ha de pertànyer un recurs.
 - Recursos que pertanyen a una línia específica de subcontractació o subcontractació.

### <a name="update-retrieve-resource-query-for-requirement-specific-resource-search"></a>Actualitza la consulta de recursos de recuperació per a la cerca de recursos específics per a requisits 
La consulta utilitzada per a la cerca també s'ha d'actualitzar per utilitzar aquests atributs de filtre addicionals. Utilitzeu els passos següents per actualitzar la configuració del Tauler de planificació per a la cerca de recursos basada en requisits:

1. Obriu **La configuració** del tauler de planificació per a un tauler de planificació específic i seleccioneu **Obre la configuració** per defecte per obrir la configuració de la cerca específica de requisits.
2. Obriu la **pestanya Configuració general i desplaceu-vos** fins a **Altres opcions de configuració**.
3. A la llista de paràmetres d'aquesta secció, actualitzeu la disposició del filtre a la **disposició** de filtre per defecte per al Lite d'operacions del projecte **.**
4. Actualitza recupera **la consulta** de recursos per recuperar la **consulta de recursos per defecte per al Lite** d'operacions del projecte.
5. Obriu la **pestanya Tipus de** planificació i aneu al **projecte**.
6. A la configuració del Projecte **, actualitzeu** la consulta **de l'Auxiliar de planificació Per recuperar recursos per defecte per recuperar** la consulta de recursos per al projecte Operations Lite **i actualitzeu** la consulta **de l'Auxiliar de planificació Retrievea restriccions per defecte** per recuperar la consulta per al projecte Operacions Lite **.**

![Actualitza la configuració del Tauler de planificació per a la cerca de recursos basada en requisits](../media/SASettings.png)  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
