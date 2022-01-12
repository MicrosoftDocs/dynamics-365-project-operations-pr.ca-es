---
title: Creació d'una estructura del desglossament del treball
description: En aquest tema s'explica com es crea una estructura de desglossament del treball (WBS) que inclogui els controls bàsics de la nova interfície de planificació.
author: ruhercul
ms.date: 12/16/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 3b8162d256aa145301fc64bee9682caa8737496f
ms.sourcegitcommit: d3f66dfb5978c5c6b7fd51363c7f9278737c49c1
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 12/17/2021
ms.locfileid: "7928603"
---
# <a name="create-a-work-breakdown-structure-wbs"></a>Creació d'una estructura del desglossament del treball (WBS)

Una planificació de projecte comunica quina feina s'ha de completar, quins recursos realitzaran la feina i el termini en el qual s'ha de completar la feina. La planificació reflecteix tota la feina associada amb el lliurament del projecte a temps. Al Dynamics 365 Project Operations, creeu una planificació de projecte mitjançant:

  - Dividir la feina en tasques gestionables.
  - Estimar el temps que és necessari per fer cada tasca.
  - Establir les dependències de les tasques.
  - Definir duracions de la tasca.
  - Estimar els recursos genèrics que realitzaran les tasques. 

La planificació del projecte es crea a la pestanya **Planificació** de la pàgina **Projecte**.

## <a name="tasks"></a>Tasques

El primer pas en la creació d'una planificació del projecte és dividir el treball en porcions gestionables. La planificació al Poroject Operations admet les característiques següents:

- Tasques de resum o de contenidor
- Tasques de node fulla

### <a name="summary-tasks"></a>Tasques de resum

Les tasques de resum poden emmagatzemar altres tasques de resum o tasques de nodes fulla. No tenen cap esforç de treball ni cost propi. En canvi, el seu esforç de treball i cost són un valor consolidat de l'esforç de treball i el cost de les tasques dels contenidors. La data d'inici de la tasca de resum és la data d'inici de les tasques dels contenidors i la data de finalització de les tasques dels contenidors. El nom d'una tasca de resum es pot editar, però les propietats de planificació, incloent-hi esforç, dates i duració, no es poden editar. Si suprimiu una tasca de resum, també heu de suprimir totes les tasques dels contenidors.

### <a name="leaf-node-tasks"></a>Tasques de node fulla

Les tasques de node fulla representen el treball més granulat del projecte. Tenen un esforç previst, recursos, dates d'inici i final planificades i una duració.

## <a name="create-a-task-hierarchy"></a>Creació d'una jerarquia de tasques

### <a name="add-a-task"></a>Afegir una tasca

Feu els passos següents per afegir la durada d'una o més tasques.

1. Aneu a **Projectes** i seleccioneu i obriu el registre de projecte per al qual voleu crear una planificació. 
2. Seleccioneu la pestanya **Tasques**. 
3. Seleccioneu **Afegeix una tasca nova**, introduïu un nom per a la tasca i premeu Retorn.
2. Introduïu un altre nom de tasca i torneu a prémer Retorn fins que aparegui una llista completa de tasques.

### <a name="manage-hierarchy-of-a-task"></a>Administrar la jerarquia d'una tasca

Quan s'afegeix una sagnia a una tasca, es converteix en un element inferior de la tasca directament superior. L'identificador de la planificació de la tasca es torna a calcular per tal que es basi en l'identificador de la planificació del nou element principal i segueix l'esquema de numeració d'esquemes. Ara, la tasca principal és una tasca de resum. Per tant, es converteix en un valor consolidat de les tasques secundàries. Quan una tasca s'ascendeix, ja no és un element secundari de la tasca que li era principal. L'identificador de la planificació es torna a calcular de manera que reflecteixi la profunditat i la posició actualitzades de la tasca a la jerarquia. L'esforç, el cost i les dates de la tasca principal anterior es tornen a calcular per tal que no incloguin aquesta tasca.

Feu els passos següents per indentar o ascendir una tasca.

1. A la pàgina **Projecte**, a la pestany **Tasques**, a **Tasques de resum**, seleccioneu els tres punts verticals al costat del nom de la tasca i, a continuació, seleccioneu **Crea una subtasca**. 
2. Seleccioneu la tasca per indentar o ascendir. Per seleccionar més d'una tasca, seleccioneu una tasca, manteniu premuda la tecla Ctrl i, a continuació, seleccioneu altres tasques.
2. També podeu triar **Indenta** o **Promou la subtasca** per desplaçar les tasques cap a fora o a sota de les tasques de resum.

### <a name="move-tasks-up-and-down"></a>Mou tasques amunt i avall

Les tasques es poden desplaçar a qualsevol nivell de l'estructura del desglossament del treball d'una de dues maneres:

- Seleccioneu una tasca més i arrossegueu-les a la ubicació desitjada.
- Seleccioneu una o diverses tasques, feu clic amb el botó dret del ratolí i seleccioneu **Retalla**, seleccioneu la cel·la de destinació a la planificació i, a continuació, feu clic amb el botó dret del ratolí i seleccioneu **Enganxa**.

## <a name="task-attributes"></a>Atributs de la tasca

Un nom de tasca descriu el treball que s'ha de completar. Al Project Operations, els atributs associats amb una tasca descriuen la planificació de la tasca i els seus requisits de dotació de personal.

## <a name="schedule-attributes"></a>Atributs de planificació

Els atributs **Esforç**, **Data d'inici**, **Data d'acabament** i **Duració** defineixen la planificació de la tasca.

A la taula següent es mostren atributs de planificació addicionals.

| **Nom de visualització definitiu** | **Descripció definitiva** |
| --- | --- |
| Esforç completat (hores) | Treball finalitzat per a la tasca en hores. |
| Durada | Mostra la durada en dies de la tasca. |
| Esforç total | Treball total per a la tasca en hores. |
| Finalització | Data i hora final. |
| % Completat | Percentatge de la tasca que s'ha completat. |
| Dipòsit de projecte | El tauler de tasques es pot agrupar per la dipòsit perquè cada dipòsit tingui la seva pròpia columna. |
| Esforç restant (hores) | El treball restant per a la tasca en hores. |
| Inici | Data i hora inicial. |
| Nom | El nom de la tasca. |
| ID | L’identificador de la tasca a l’estructura del desglossament del treball. |

Com a administrador, podeu definir camps personalitzats a l'entitat de la tasca. No obstant, els camps no es poden visualitzar a la quadrícula de planificació. Per veure els camps personalitzats, afegiu-los a la pàgina de detalls de la **Tasca del projecte**.

## <a name="staffing-attributes"></a>Atributs de personal

Als atributs de personal s'hi accedeix a través del camp **Recursos** a la planificació. Podeu cercar un recurs existent o seleccionar **Crea** i a la subfinestra **Creació ràpida**, afegir un membre d'equip de projecte com a recurs nou.  Quan cerqueu un recurs mitjançant el selector de recursos a la quadrícula de tasques, la visualització del tauler o el gantt, la cerca retorna els membres de l'equip del projecte existents o els recursos actius que es poden reservar.

Els camps **Funció**, **Unitat de recursos** i **Nom del càrrec** s'utilitzen per descriure els requisits de dotació de la tasca. Aquests atributs de personal, juntament amb la planificació de tasques, s'utilitzen per trobar els recursos disponibles per fer aquesta tasca.

   - **Funció** : especifiqueu el tipus de recurs necessari per fer la tasca.,
   - **Unitat de recursos**: especifiqueu la unitat a la qual han d'assignar-se els recursos per a la tasca. Aquest atribut afecta l'estimació de costos i vendes per a la tasca si la tarifa de cost i de facturació del recurs es defineix a partir d'unitats de recursos.
   - **Nom del càrrec**: introduïu un nom amigable per al recurs genèric que serveixi com a contenidor per al recurs que en última instància farà la feina.

El camp **Recursos** conté el nom del càrrec del recurs genèric o el recurs amb nom quan se'n troba un.

El camp **Categoria** conté els valors que indiquen un tipus més ampli de treball en què la tasca es pot agrupar. Aquest camp no afecta la planificació ni la dotació de personal. En lloc d'això, el camp només s'utilitza per als informes.

## <a name="task-dependencies"></a>Dependències de tasca

Podeu utilitzar la planificació al Project Operations per crear relacions de predecessor entre tasques. El camp **Predecessor** fa servir un o diversos valors per indicar les tasques de què depèn una tasca. Quan s'assignen valors de predecessor a una tasca, la tasca només pot començar quan s'hagin completat totes les tasques de predecessor. A causa de la dependència, la data d'inici planificada de la tasca es restableix a la data en què s'han completat les tasques del predecessor.

El mode de la tasca no té cap efecte sobre les actualitzacions que es fan a la data d'inici i d'acabament del treball predecessor o dependent.

## <a name="accessibility-and-keyboard-shortcuts"></a>Dreceres de teclat i accessibilitat

La graella **Planificació** és totalment accessible i es pot utilitzar amb lectors de pantalla com ara el Narrador, JAWS o NVDA. Podeu desplaçar-vos per l'àrea de la quadrícula mitjançant les tecles de fletxa (com al Microsoft Excel), podeu utilitzar la tecla de tabulació per avançar entre els elements de la interfície d'usuari interactius, i podeu utilitzar la tecla de fletxa avall, la tecla Enter o la barra espaiadora per seleccionar i obrir els menús desplegables.

## <a name="project-limitations"></a>Limitacions del projecte 
Heu de tenir en compte les limitacions següents si esteu utilitzant l'estructura del desglossament del treball al Project Operations. Aquests límits s'apliquen a projectes i tasques. Per obtenir més informació, vegeu [Limitacions de Project for the Web](/project-for-the-web/project-for-the-web-limits-and-boundaries).

| **Camp**                                          |  **Límit**           |
|----------------------------------------------------|----------------------|
| Tasques totals màximes per a un projecte                  | 500                  |
| Durada total màxima per a un projecte               | 3.650 dies (10 anys) |
| Recursos totals màxims per a un projecte              | 150                  |
| Enllaços totals màxims (només successor) per a un projecte | 600                  |
| Camps personalitzats totals màxims per a un projecte          | 10                   |
| Màxims elements de la llista de comprovació per tasca                   | 20                   |

**Limitacions de les tasques**

| **Camp**                               |   **Límit**           |
|-----------------------------------------|-----------------------|
| Nivell de jerarquia màxim                 | 10 nivells             |
| Enllaços màxims (successor + predecessor) | 20                    |
| Durada màxima de la tasca de fulla           | 1250 dies             |
| Durada màxima d'una tasca de resum      | 3.650 dies (10 anys)  |
| Recursos màxims assignats a una tasca    | 20 recursos          |
| Interval de dates admès per a una tasca         | 1/1/2000 - 31/12/2149 |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
