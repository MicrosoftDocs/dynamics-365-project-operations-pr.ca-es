---
title: Seguiment del cost del projecte
description: Aquest tema proporciona informació sobre com el Project Operations fa el seguiment del progrés segons el cost laboral i la despesa d'un projecte.
author: rumant
ms.date: 03/22/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d37df64db1808722b7851c952c20be731aa2d670fe066c02ef90386712487407
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6987784"
---
# <a name="labor-cost-tracking-on-projects"></a>Seguiment de costos laborals en projectes

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

El Dynamics 365 Project Operations fa el seguiment de les estimacions laborals i de la despesa en la granularitat necessària més baixa del pla del projecte. La previsió financera del cost laboral es basa en l'esforç previst i en els recursos genèrics o amb nom que s'assignen a cada tasca de cada node secundari del pla del projecte. Quan el projecte comença i les persones comencen a anotar temps en diverses tasques del projecte, es resumeix la despesa real de mà d'obra, que inicia un càlcul de les projeccions.

## <a name="labor-cost-tracking-view"></a>Visualització del seguiment del cost laboral

A la pàgina **Projectes**, a la pestanya **Seguiment**, podeu seleccionar **Seguiment** > **Cost** per obrir la visualització **Seguiment de costos** i veure el progrés de la despesa laboral en cada tasca del pla del projecte. Aquesta visualització també compara el cost laboral real invertit en una tasca amb el cost laboral previst de la tasca. El Project Operations utilitza les fórmules següents per calcular les mètriques de cost laboral:

- **Cost previst**: cost previst de totes les assignacions de recursos a cada tasca de node fulla
- **Cost real**: suma de tots els valors reals de cost per al temps registrat a la tasca
- **Percentatge de consum del cost**: cost real ÷ previsió de cost en estat complet
- **Cost restant**: previsió de cost en estat complet ÷ cost real
- **Cost en estat complet**: cost restant ÷ cost real
- **Variància de cost**: cost planificat – previsió de cost en estat complet

Cada tasca mostra una projecció de la variància del cost en la tasca. Si la previsió de cost en estat completat és superior al cost planificat, es preveu que la tasca superi el pressupost. Si la previsió de cost en estat completat és inferior al cost planificat, es preveu que la tasca no esgoti el pressupost.

>[!NOTE]
> El Project Operations només mostra els costos laborals a la pàgina **Projecte** a la pestanya **Seguiment**. Tot i que els materials i les despeses es poden calcular i fer-ne el seguiment del consum, aquests costos no s'inclouen als costos que es mostren a la pestanya **Seguiment**. Aquesta pestanya està dissenyada per funcionar només per tornar a projectar els costos laborals amb una nova projecció de l'esforç.
Tots els imports de cost que es mostren es converteixen a la moneda de cost del projecte des de la moneda de preu de cost del projecte utilitzada per determinar la taxa de cost. La moneda de cost del projecte és la moneda de la unitat de contractació del projecte. Els valors de cost previstos per al temps que es mostren a la pestanya **Estimacions** de la pàgina **Projecte** podria ser que no se sumessin al cost planificat a la pestanya **Seguiment**. La raó d'aquesta discrepància són les diferències en la manera com es resumeix el cost previst a la quadrícula **Estimacions** i la manera com es calcula el cost previst a la quadrícula de **Seguiment**. 
>
> - La pestanya **Estimacions** calcula el cost previst utilitzant la mateixa moneda de la taxa de cost de la llista de preus. A continuació, el cost previst en la moneda de la llista de preus es converteix al cost previst en la moneda de cost del projecte. El cost previst en la moneda del projecte es mostra arrodonit a 2 decimals. En cap moment durant aquesta conversió s'aplica la precisió de moneda. 
> - A la pestanya **Seguiment**, el càlcul del cost previst segueix un ordre de càlcul lleugerament diferent de l'ordre de càlcul, que consisteix a aplicar la precisió de moneda en dues fases: 
   ><ol>
   ><li>L'import de cost previst en la moneda de la llista de preus es converteix a la moneda base (conversió 1).</li>
   ><li>L'import de cost previst en la moneda base es converteix a la moneda del cost previst (conversió 2). </li>
   ></ol>
   >La precisió de moneda s'aplica en dos passos per obtenir un cost previst (a la pestanya **Seguiment**) que es desvia lleugerament del cost previst (a la visualització **Temps: per fases** de la pestanya **Estimacions**). 
   
## <a name="reprojecting-costs-on-leaf-node-tasks"></a>Tornar a projectar els costos en les tasques dels nodes fulla

Els costos laborals en una tasca de node es poden tornar a projectar directament a la pestanya **Seguiment** de la **Pàgina del projecte**. Tanmateix, podeu utilitzar la visualització **Seguiment de l'esforç** per tornar a projectar l'esforç restant d'una tasca. Això fa que es torni a calcular el cost restant a la tasca. A continuació es mostra una descripció de com funciona això.

1. Un administrador de projecte pot tornar a projectar l'esforç de les tasques actualitzant el valor per defecte del camp **Esforç restant** amb una nova estimació de l'esforç restant en la tasca. La nova projecció fa que es torni a calcular la previsió d'esforç de la tasca en estat completat (EAC), el percentatge de progrés i la variància de l'esforç previst en una tasca. També es torna a calcular l'EAC, l'estimació per completar (ETC) i el percentatge de progrés de les tasques de resum, i produeixen una nova projecció de la variació d'esforç.
2. Segons el valor nou de l'esforç restant de la tasca, el sistema calcula el cost restant a la visualització **Seguiment de costos**. Per calcular el cost restant segons l'esforç restant, el sistema calcula primer el cost mitjà d'una hora d'esforç en la tasca com a cost o esforç previst. El cost previst és la suma del cost de totes les assignacions de recursos de la tasca. El cost mitjà per hora s'utilitza per calcular el cost restant de l'esforç restant que s'ha projectat recentment a la tasca.
3. Es torna a calcular el cost en estat complet i el percentatge de consum del cost de la tasca del node fulla.
4. Es torna a calcular el valor del cost en estat complet de les tasques de resum fins al node arrel.

## <a name="reprojecting-costs-on-summary-tasks"></a>Tornar a projectar els costos en les tasques de resum

Podeu tornar a projectar els costos laborals en tasques de resum o tasques de contenidor. Amb tot, no podeu tornar a projectar directament els costos laborals en una tasca de projecte de resum a la pestanya **Seguiment** de la pàgina **Projecte**. De manera similar a les tasques dels nodes fulla, la nova projecció de tasques de resum i de contenidor es pot fer mitjançant la visualització **Seguiment d'esforços**. En aquesta visualització, podeu tornar a projectar l'esforç restant d'una tasca de resum, cosa que farà que es torni a calcular el cost restant de la tasca de resum. A continuació es mostra una descripció de com funciona això.

1. Un administrador de projecte pot tornar a projectar l'esforç de les tasques de resum actualitzant el valor per defecte de l'esforç restant amb una nova estimació en la tasca. Aquesta actualització fa que es torni a calcular la previsió de la tasca de resum en estat completat (EAC), el percentatge de progrés i la variància de l'esforç previst en una tasca. També es torna a calcular l'EAC, l'ETC i el percentatge de progrés de les tasques de resum, i produeixen una nova projecció de la variació d'esforç.
2. Segons el valor nou de l'esforç restant de la tasca de resum, el sistema calcula el cost restant a la visualització **Seguiment de costos**. Per calcular el cost restant segons l'esforç restant, el sistema calcula primer el cost mitjà d'una hora d'esforç en la tasca de resum com a cost o esforç previst. El cost mitjà per hora s'utilitza per calcular el cost de l'esforç restant que s'ha tornat a projectar recentment a la tasca de resum.
3. Es torna a calcular el cost en estat complet i el percentatge de consum del cost de la tasca de resum.
4. El nou cost en estat completat es distribueix cap avall a les tasques secundàries en la mateixa proporció que el cost previst original era a la tasca.
5. Es calcula el valor del cost en estat completat nou en cadascuna de les tasques individuals fins a les tasques de node fulla. Segons aquest valor, a les tasques secundàries afectades per sota dels nodes fulla es tornarà a calcular el cost restant i el percentatge de cost en percentatge basant-se en el cost en estat completat. Aquest valor es tradueix en una nova projecció per a la variància del cost de la tasca. 


El camp **Rendiment del cost** es pot definir a partir de les dades de seguiment. Quan la variància de cost per al node arrel a la visualització **Seguiment de costos** és negatiu, podeu definir aquest camp com a **Per sota del pressupost**. Quan la variància de cost per al node arrel és positiva, podeu definir el valor en **Per sobre del pressupost**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
