---
title: Configuració del projecte
description: Aquest tema proporciona informació sobre la configuració de l'administració de projectes.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: ca5fc63d56ddd84871949e38f421bcdfe38d478e
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148136"
---
# <a name="project-settings"></a>Configuració del projecte

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Utilitzeu la configuració següent per accedir a les característiques de planificació del projecte.

## <a name="work-template"></a>Plantilla de treball

Per crear una planificació de projecte, creeu uns plantilla de calendari de projecte que defineixi el nombre d'hores de treball al dia i qualsevol tancament de negoci. Per crear una plantilla de calendari de projecte, associeu una plantilla de treball amb el camp **Plantilla de calendari** per al projecte. Seguiu els passos que es descriuen a continuació per crear una plantilla de treball.

1. Al PSA, a la subfinestra de navegació de l'esquerra, feu clic a **Recursos**. 
2. A la pàgina de la llista **Recursos**, obriu un registre d'usuari i després seleccioneu **Mostra les hores de treball**.

  > [!NOTE]
  > Assegureu-vos que permeteu les finestres emergents a la pàgina del navegador. Això us permet veure les hores de feina definides per al recurs.
  
3. A la pestanya **Visualització mensual**, feu clic a **Configura**. Es mostra una llista de tres opcions: 

  - Planificació setmanal nova
  - Planificació de treball per a un dia
  - Temps lliure

> ![Configurar les opcions](media/project-13.png)

4. Seleccioneu **Planificació setmanal nova** i, a continuació, definiu les opcions d'aquesta planificació de recursos. Podeu definir una planificació setmanal periòdica, paràmetres d'hores diàries, tancaments d'empresa, etc.
5. Definiu l'interval de dates ,seleccioneu **Desa** i, a continuació, feu clic a **Tanca**. 
6. Torneu a la pàgina de la llista **Recursos** i seleccioneu el recurs per al qual definiu les hores de feina. 
7. Seleccioneu **Defineix el calendari com a** per definir la plantilla de treball. 
8. Al quadre de diàleg **Plantilla de treball** introduïu el nom de la plantilla de treball i després seleccioneu **Aplica**. 

Ara podeu associar la plantilla de treball amb una plantilla de calendari de projectes.

## <a name="resource-roles"></a>Funcions de recursos

El terme *funció de recurs* fa referència al conjunt d'aptituds, competències i certificacions que ha de tenir una persona per dur a terme un conjunt específic de tasques en un projecte. El PSA us permet calcular i facturar el temps d'un recurs a partir la funció amb la qual està associat el recurs. Cada organització ha de configurar aquestes funcions mitjançant la navegació esquerra al menú **Project Service**.

Cada organització ha de configurar aquestes funcions a la pàgina **Categories de recursos actives**. Per obrir aquesta pàgina, a la subfinestra de navegació esquerra, seleccioneu **Funcions de recurs**.

## <a name="price-lists"></a>Llistes de preus

Les llistes de preus us permeten definir costos i preus de venda per a les funcions de recursos, categories de despeses i altres elements d'una organització. Abans de definir previsions financeres dels treballs que s'han de lliurar per a projecte, hauríeu de crear un cost de reserva i una llista de preus de venda. A la secció de paràmetres, també heu de configurar una llista de preus i costos de vendes per defecte que s'apliqui a tots els projectes que es creen a l'organització. A la pàgina **Paràmetres del projecte actius**, assegureu-vos de configurar una llista de preus i costos de vendes per defecte.


[!INCLUDE[footer-include](../includes/footer-banner.md)]