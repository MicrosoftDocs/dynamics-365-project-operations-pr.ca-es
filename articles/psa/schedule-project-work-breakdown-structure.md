---
title: Planificar un projecte amb una estructura del desglossament del treball
description: Com planificar un projecte amb una estructura del desglossament del treball al Project Service
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 027bcbc8995ed39af78c7ff9b1028f401c3b0d4d
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6008569"
---
# <a name="schedule-a-project-with-a-work-breakdown-structure-project-service"></a>Planificar un projecte amb una estructura del desglossament del treball (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Una planificació de projecte comunica quina feina s'ha de realitzar, quins recursos realitzaran la feina i el termini en el qual s'ha de completar la feina. La planificació del projecte reflecteix tota la feina associada amb el lliurament del projecte a temps. Un dels primers passos en la fase d'iniciació del projecte és elaborar una planificació de projecte. Per establir una planificació de projecte, heu de crear una estructura del desglossament del treball.  
  
 Creeu una estructura de projecte amb una estructura de desglossament de treball que us ajudi a:  
  
- Dividir la feina en tasques gestionables  
  
- Calcular el temps necessari per completar una tasca  
  
- Definir dependències de tasca i la durada de la tasca  
  
- Determinar les funcions necessàries per completar cada tasca  
  
  La planificació del projecte en l'estructura del desglossament del treball té un aspecte i un funcionament familiars complementat amb un gràfic de Gantt interactiu.  
  
## <a name="create-a-work-breakdown-structure-for-a-project"></a>Crear una estructura del desglossament del treball per a un projecte  
 Creeu una estructura del desglossament del treball per representar la seqüència de les tasques en un projecte. L'estructura del desglossament del treball inclou tasques, requisits per a cada tasca i informació dels ingressos i els costos. A la vostra estructura del desglossament del treball, podeu afegir:  
  
-   La seqüència de les tasques en una jerarquia  
  
-   Altres tasques, si escau, que s'han de completar per poder iniciar una tasca  
  
-   La data d'inici, la data final i la durada d'una tasca  
  
-   Nombre d'hores necessàries per a una tasca  
  
-   Qualsevol habilitat i formació necessàries d'un treballador  
  
-   Els treballadors assignats a una tasca  
  
-   Ingressos i costos previstos  
  
## <a name="task-types"></a>Tipus de tasca  
Utilitzareu els següents tipus de tasques per crear l'estructura del desglossament del treball:  

| | | 
|---------------------------------------|-----------------------------------------------------------------| 
| **Node arrel del projecte** | La tasca de resum de nivell superior per al projecte. Totes les altres tasques de projecte es creen a sota. El nom de la tasca arrel és el nom de projecte. L'esforç, les dates i la duració del node arrel es basen en els valors a la jerarquia que hi ha per sota. No podeu editar les propietats de node arrel ni suprimir el node arrel. | 
| **Tasques de resum o de contenidor** | Una tasca de resum és una tasca de la qual pengen subtasques. Una tasca de resum no té cap esforç de treball ni el cost propi. El seu esforç i cost de treball són un valor consolidat de les seves subtasques. Podeu canviar el nom d'una tasca de resum, però no podeu canviar l'esforç, les dates o la durada perquè es calculen automàticament. Si suprimiu una tasca de resum se suprimeix la tasca i totes les seves subtasques.|  
| **Tasques de node fulla** | Una tasca de node fulla representa el treball més detallat del projecte. Té un esforç previst, un nombre de recursos planificat, dates d'inici i final planificades i una durada.|

  
## <a name="task-hierarchy"></a>Jerarquia de tasques  
 Teniu les opcions següents per crear una jerarquia de tasques:  
  
- **Afegeix tasca**.   Podeu afegir una tasca en una posició que trieu a la jerarquia de tasques. Si no seleccioneu una posició, la vostra nova tasca apareix al final.  
  
- **Aplica sagnia a tasca**.   Aplica sagnia a una tasca per convertir-la en una tasca secundària de la tasca directament superior.  
  
- **Anul·la sagnia de tasca**   Anul·la una sagnia d'una tasca per deixar que sigui una subtasca de la seva tasca principal original.  
  
- **Puja i baixa**.   Desplaça les tasques amunt i avall a la jerarquia de la seva tasca principal. El desplaçament amunt o avall d'una tasca no té cap efecte sobre el seu esforç, cost, dates o durada.  
  
## <a name="task-attributes"></a>Atributs de la tasca  
 Un nom de tasca descriu el treball que s'ha de completar. Utilitzeu diversos atributs de tasca per descriure els requisits de personal i de planificació per a la tasca.  
  
### <a name="schedule-attributes"></a>Atributs de planificació

 - Assigneu valors a **Hores d'esforç**, **Nombre de recursos**, **Data d'inici**, **Data final** i **Durada** per determinar la planificació de la tasca. 
 - **Esforç** és una estimació de les hores que es necessiten per completar la tasca.
 - **Nombre de recursos** és una estimació que l'administrador del projecte posa a la tasca per assolir la millor planificació possible. 
 - **Durada** (en dies) indica el nombre de dies laborables que es necessita per completar la tasca.  
  
### <a name="staffing-attributes"></a>Atributs de personal

 - **Funció**, **Unitat organitzativa de recurs**, **Nombre de recursos** i **Recursos** descriuen els requisits de personal per a la tasca. 
 - **Funció** descriu el tipus de recurs necessari per realitzar la tasca. 
 - **Unitat organitzativa de recurs** indica la unitat organitzativa de recursos des de la qual els recursos s'han de dotar a la tasca; això també influeix en l'estimació de costos i vendes de la tasca, ja que es té en compte en determinar el preu de venda unitari del recurs. 
 - **Recursos** conté un recurs genèric o un recurs amb nom quan se'n troba un.  
  
## <a name="task-dependencies"></a>Dependències de tasca  
 Podeu crear relacions de predecessor entre una o més tasques a l'estructura del desglossament del treball. Podeu posar un o més valors del camp predecessor a les tasques per indicar les tasques de les quals serà dependent. Quan assigneu un valor de predecessor a una tasca, la tasca només pot començar quan hagin finalitzat totes les tasques de predecessor. Si definiu aquesta dependència en una tasca, es tornarà a calcular la data d'inici prevista de la tasca com l'últim final de tots els seus predecessors. Els impactes relacionats amb el predecessor en una planificació no es limiten al mode de tasca definit a la tasca.  
  
## <a name="task-mode"></a>Mode de tasca  
 El mode de tasca és un dels factors importants que determinen la planificació de les tasques de node fulla. Hi ha dos modes de tasca per a cada tasca: mode de planificació automàtica i mode de planificació manual.  
  
-   **Planificació automàtica**.   Quan definiu el mode de tasca a Planificat automàticament, el motor de planificació de la tasca utilitza les regles de planificació als següents atributs de tasca per determinar la planificació de la tasca:  
  
    -   Predecessors  
  
    -   Esforç  
  
    -   Nombre de recursos  
  
    -   Dates d'inici i d'acabament  
  
-   **Regles de planificació**.   La data d'inici d'una tasca de node fulla que no té un predecessor pren per defecte la data d'inici de la planificació del projecte. La durada d'una tasca de node fulla sempre es calcula com el nombre de dies feiners entre les dates d'inici i final. Quan una tasca es planifica automàticament, el motor de planificació segueix les regles següents:  
  
    -   Les dates d'inici i final d'una tasca sempre han de ser dies hàbils segons calendari de planificació del projecte  
  
    -   La data d'inici d'una tasca que té antecessors pren per defecte l'última data de finalització dels seus predecessors  
  
    -   Esforç = Nombre de persones * Durada * hores en un dia de treball estàndard del calendari del projecte  
  
-   **Planificació manual**.   En alguns casos potser heu de desviar aquestes regles. En aquests casos, podeu definir el mode de tasca per a la tasca que s'ha de planificar manualment. Això evita que el motor de planificació hagi de calcular els valors d'altres atributs de planificació. La definició de predecessors en tasques sempre influeix en la data d'inici de la tasca dependent.  
  
## <a name="create-a-work-breakdown-structure"></a>Crear una estructura del desglossament del treball  
  
1.  Aneu a **Project Service > Projectes**.  
  
2.  Feu clic al projecte en el qual voleu treballant.  
  
3.  A la barra que hi ha a la part superior de la pantalla, seleccioneu la fletxa avall al costat del nom de projecte i, a continuació, feu clic a Estructura del desglossament del treball.  
  
4.  Per afegir una tasca, feu clic a **Afegeix tasca**. Empleneu els camps de la tasca i, a continuació, feu clic a **Desa**.  
  
5.  Continueu afegint tasques fins que l'estructura del desglossament del treball estigui completa. Quan creeu l'estructura del desglossament del treball, podeu fer el següent per organitzar les vostres tasques:  
  
    -   Seleccioneu una tasca i feu clic a **Aplica sagnia** per moure-la sota una altra tasca o feu clic a Anul·la sagnia per pujar-la un nivell.  
  
    -   Seleccioneu una tasca i feu clic a **Desplaça amunt** o **Desplaça avall** per pujar-la o baixar-la a la llista.  
  
    -   Feu clic a **Amaga Gantt** per amagar el gràfic de Gantt i feu clic a **Mostra Gantt** per tornar-lo a mostrar.  
  
    -   Seleccioneu un període diferent de temps del gràfic de Gantt a **Escala de temps**.  
  
6.  Per afegir les funcions que heu especificat a l'estructura del desglossament del treball als membres del vostre equip de projecte, feu clic a **Genera equip de projecte**.  
  
7.  Feu clic a **Desa** a la cantonada inferior dreta de la pantalla quan hagueu acabat de fer els canvis.  
  
### <a name="see-also"></a>Vegeu també  
 [Guia de l'administrador de projectes](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]