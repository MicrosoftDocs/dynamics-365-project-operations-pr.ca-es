---
title: Planificació del projecte
description: En aquest tema es proporciona informació sobre com crear una planificació.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 3/01/2019
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
ms.openlocfilehash: 9a6b27050a19d8a7f2ed35f74b42bb4f371ad069
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072247"
---
# <a name="project-schedules"></a>Planificació del projecte 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Una planificació de projecte comunica quina feina s'ha de completar, quins recursos realitzaran la feina i el termini en el qual s'ha de finalitzar la feina. Reflecteix tota la feina associada amb el lliurament del projecte a temps. Al Dynamics 365 Project Service Automation, creeu una planificació de projecte dividint el treball en tasques gestionables, i estimant el temps necessari per fer cada tasca, establint dependències de tasques, establint duracions de les tasques i estimant els recursos genèrics que faran les tasques. La planificació del projecte es crea a la pestanya **Planificació** de la pàgina del projecte.
 
## <a name="tasks"></a>Tasques

El primer pas en la creació d'una planificació del projecte és dividir el treball en porcions gestionables. La planificació al PSA admet les característiques següents:

- Node arrel del projecte
- Tasques de resum o de contenidor
- Tasques de node fulla

### <a name="project-root-node"></a>Node arrel del projecte

El node arrel del projecte és la tasca de resum de nivell superior del projecte. Totes les altres tasques de projecte es creen a sota. El nom de la tasca arrel sempre és el nom de projecte. L'esforç, les dates i la duració del node arrel es resumeixen a partir dels valors a la jerarquia que hi ha per sota. No podeu editar les propietats del node arrel. Tampoc no podeu suprimir el node arrel.

### <a name="summary-or-container-tasks"></a>Tasques de resum o de contenidor 

Les tasques de resum tenen subtasques o tasques de contenidor en nivells inferiors. No tenen cap esforç de treball ni cost propi. En canvi, el seu esforç de treball i cost són un valor consolidat de l'esforç de treball i el cost de les tasques dels contenidors. La data d'inici de la tasca de resum és la data d'inici de les tasques dels contenidors i la data de finalització de les tasques dels contenidors. El nom d'una tasca de resum es pot editar, però les propietats de planificació (esforç, dates i duració) no es poden editar. Si suprimiu una tasca de resum, també heu de suprimir totes les tasques dels contenidors.

### <a name="leaf-node-tasks"></a>Tasques de node fulla

Les tasques de node fulla representen el treball més granulat del projecte. Tenen un esforç previst, recursos, dates d'inici i final planificades i una duració.
 
## <a name="creating-a-task-hierarchy"></a>Crear una jerarquia de tasques

Teniu les opcions següents per crear una jerarquia de tasques:

- Botó **Afegeix una tasca**
- Botó **Afegeix una sagnia a la tasca**
- Botó **Anul·la la sagnia de la tasca**
- Botons **Mou amunt** i **Mou avall**
- Dreceres de teclat i accessibilitat

### <a name="add-task"></a>Afegeix una tasca

El botó **Afegeix una tasca** us permet crear una tasca nova a la jerarquia. Si no seleccioneu una posició, la nova tasca s'insereix al final. 

L'identificador de planificació s'assigna a cada tasca. L'identificador de planificació representa la profunditat i posició de la tasca a la jerarquia. Utilitza la numeració de l'esquema. Per a les tasques del primer nivell sota el node arrel del projecte, s'utilitza un esquema de numeració d' 1, 2, 3, i així successivament. Per a les tasques sota el primer nivell, s'utilitza un esquema de numeració d' 1.1, 1.2, 1.3, i així successivament.

### <a name="indent-task"></a>Aplica una sagnia a la tasca.

Quan s'afegeix una sagnia a una tasca, es converteix en un element inferior de la tasca directament superior. L'identificador de la planificació de la tasca es torna a calcular per tal que es basi en l'identificador de la planificació del nou element principal i segueix l'esquema de numeració d'esquemes. La tasca principal és ara una tasca de resum o d'una tasca de contenidor. Per tant, es converteix en un valor consolidat de les tasques secundàries.

### <a name="outdent-task"></a>Anul·la la sagnia de la tasca 

Quan s'anul·la la sagnia d'una tasca, ja no és un element secundari de la tasca que era principal. L'identificador de la planificació es torna a calcular de manera que reflecteixi la profunditat i la posició actualitzades de la tasca a la jerarquia. L'esforç, el cost i les dates de la tasca principal anterior es tornen a calcular per tal que no incloguin aquesta tasca.

### <a name="move-up-and-move-down"></a>Mou amunt i Mou avall 

Els botons **Mou amunt** i **Mou avall** canvien la posició d'una tasca dins de la jerarquia de l'element principal. Els canvis d'aquest tipus no afecten a l'esforç, cost, data o duració de la tasca. Només es veu afectat l'identificador de planificació de la tasca. L'identificador de la planificació es torna a calcular de manera que reflecteixi la nova posició a la llista principal de tasques secundàries.

### <a name="accessibility-and-keyboard-shortcuts"></a>Dreceres de teclat i accessibilitat

La graella **Planificació** és totalment accessible i es pot utilitzar amb lectors de pantalla com ara el Narrador, JAWS o NVDA. Podeu desplaçar-vos per l'àrea de la quadrícula mitjançant les tecles de fletxa (com al Microsoft Excel), podeu utilitzar la tecla de tabulació per avançar entre els elements de la interfície d'usuari interactius, i podeu utilitzar la tecla de fletxa avall, la tecla Enter o la barra espaiadora per seleccionar i invocar els menús desplegables. Les capçaleres de columna també són interactives. Podeu amagar i mostrar columnes, utilitzar la tecla de tabulació i les tecles de fletxa per desplaçar-vos per les capçaleres de columna i utilitzar els botons d'acció de la barra d'eines. A més, podeu utilitzar les dreceres de teclat següents:

- **Actualitza** : Alt + Maj + F5
- **Afegeix** : Alt + Maj + Insereix
- **Suprimeix** : Alt + Maj + Supr
- **Mou amunt/avall** : Alt + Maj + Fletxes amunt/avall
- **Afegeix/suprimeix la sagnia** : Alt + Maj + Fletxes esquerra/dreta
- **Expandeix/redueix les jerarquies** : Alt + Maj + Tecles més/menys

## <a name="task-attributes"></a>Atributs de la tasca

Un nom de tasca descriu el treball que s'ha de completar. Al PSA, els atributs associats amb una tasca descriuen la planificació de la tasca i els seus requisits de dotació de personal.

> ![Atributs de la tasca](media/project-2.png)
 
### <a name="schedule-attributes"></a>Atributs de planificació

Els atributs **Esforç** , **Data d'inici** , **Data d'acabament** i **Duració** defineixen la planificació de la tasca.

Els atributs de planificació addicionals inclouen:

- **Hores d'esforç** : introduïu una estimació de les hores necessàries per completar la tasca. 
- **Duració** : especifiqueu el nombre de dies laborables necessaris per completar la tasca.
- **ID de planificació** : aquest identificador automàticament generat s'utilitza per ordenar les tasques a la jerarquia. Les dependències entre tasques gestionen l'ordre real en què es treballen les tasques.
 
### <a name="staffing-attributes"></a>Atributs de personal

Als atributs de personal s'hi accedeix a través del camp **Recursos** a la planificació. Podeu cercar un recurs existent o fer clic a **Crea** i a la subfinestra **Creació ràpida** , afegir un membre d'equip de projecte com a recurs nou.

Els camps **Funció** , **Unitat de recursos** i **Nom del càrrec** s'utilitzen per descriure els requisits de dotació de la tasca. Aquests atributs de personal, juntament amb la planificació de tasques, s'utilitzen per trobar els recursos disponibles per fer aquesta tasca.

**Funció** : especifiqueu el tipus de recurs necessari per fer la tasca.

**Unitat de recursos** : especifiqueu la unitat a la qual han d'assignar-se els recursos per a la tasca. Aquest atribut afecta l'estimació de costos i vendes per a la tasca si la tarifa de cost i de facturació del recurs es defineix a partir d'unitats de recursos.

**Nom del càrrec** : introduïu un nom amigable per al recurs genèric que serveixi com a contenidor per al recurs que en última instància farà la feina.

El camp **Recursos** conté el nom del càrrec del recurs genèric o el recurs amb nom quan se'n troba un.

El camp **Categoria** conté els valors que indiquen un tipus més ampli de treball en què la tasca es pot agrupar. Aquest camp no afecta la planificació ni la dotació de personal. Només s'utilitza per a l'informe.

### <a name="task-dependencies"></a>Dependències de tasca 

Podeu utilitzar la planificació al PSA per crear relacions de predecessor entre tasques. El camp **Predecessor** a **Tasques** accepta un o diversos valors per indicar les tasques de què depèn una tasca. Quan s'assignen valors de predecessor a una tasca, la tasca només pot començar quan s'hagin completat totes les tasques de predecessor. A causa de la dependència, la data d'inici planificada de la tasca es restableix a la data en què s'han completat les tasques del predecessor.

El mode de la tasca no té cap efecte sobre les actualitzacions que es fan a la data d'inici i d'acabament del treball predecessor o dependent.

## <a name="task-mode"></a>Mode de tasca 

El mode de tasca determina la planificació de les tasques de nodes fulla. El PSA admet dos modes de tasca per a cada tasca: planificació automàtica i planificació manual.

### <a name="auto-scheduling"></a>Planificació automàtica 
 
Quan definiu el mode de tasca a **Planificat automàticament** , el motor de planificació de la tasca utilitza les regles de planificació als atributs de tasca per determinar la planificació de la tasca.

#### <a name="scheduling-rules"></a>Regles de planificació

Per defecte, si una tasca de node fulla no té un predecessor, pren per la data d'inici de la planificació del projecte. La durada d'una tasca de node fulla sempre es calcula com el nombre de dies feiners entre les dates d'inici i final. Quan una tasca es planifica automàticament, el motor de planificació segueix aquestes regles:

- Les dates d'inici i final de la tasca sempre han de ser dies hàbils segons el calendari de planificació del projecte. 
- Per a qualsevol tasca que té tasques predecessores, la data d'inici es defineix automàticament a l'última data de finalització dels seus predecessors.
- L'esforç es calcula mitjançant aquesta fórmula: nombre de persones × duració × hores en una jornada laboral estàndard en el calendari del projecte.

### <a name="manual-scheduling"></a>Planificació manual

Si les regles de la planificació automàtica no compleixen els vostres requisits, podeu definir el mode de tasca per a la tasca a **Programada manualment**. Aquest paràmetre evita que el motor de planificació hagi de calcular els valors d'altres atributs de planificació. Independentment del mode de la tasca, si definiu els predecessors en les tasques, sempre afecteu la data d'inici de la tasca dependent.
