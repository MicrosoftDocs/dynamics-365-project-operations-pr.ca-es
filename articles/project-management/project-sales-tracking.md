---
title: Seguiment de les vendes del projecte
description: Aquest tema proporciona informació sobre com el Project Operations fa el seguiment del progrés segons els ingressos laborals d'un projecte.
author: rumant
manager: AnnBe
ms.date: 03/24/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 438c44dcfaf9677075eb07688c1e65c6e7053755
ms.sourcegitcommit: a1f9f92546ab5d8d8e5a4710ce4c96414ea55d14
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 03/24/2021
ms.locfileid: "5711025"
---
# <a name="project-sales-tracking"></a>Seguiment de les vendes del projecte

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

El Dynamics 365 Project Operations fa el seguiment de les estimacions laborals i dels ingressos en la granularitat necessària més baixa del pla del projecte. La previsió financera dels ingressos laborals es basa en l'esforç previst i en els recursos genèrics o amb nom que s'assignen a cada tasca de cada node secundari del pla del projecte. Quan el projecte comença i les persones comencen a anotar temps en diverses tasques del projecte, es resumeixen els ingressos reals de mà d'obra, que inicia un càlcul de les projeccions.

## <a name="labor-revenue-tracking-view"></a>Visualització del seguiment dels ingressos laborals

A la pàgina **Projectes**, a la pestanya **Seguiment**, podeu seleccionar **Seguiment** > **Cost** per obrir la visualització **Seguiment de costos**. També podeu seleccionar **Utilitza** > **Taxa de facturació** per obrir la visualització **Seguiment d'ingressos**, que mostra el progrés dels ingressos laborals en cada tasca del pla del projecte. Aquesta visualització també compara els ingressos laborals reals invertits en una tasca amb els ingressos laborals previstos de la tasca. El Project Operations utilitza les fórmules següents per calcular les mètriques d'ingressos laborals:

- **Ingressos previstos**: valors de vendes previstos de totes les assignacions de recursos a cada tasca de node fulla
- **Ingressos reals**: suma de totes les vendes reals sense facturar per al temps registrat a la tasca
- **Ingressos facturables%**: ingressos reals ÷ estimació ingressos en estat completat
- **Ingressos restants**: estimació d'ingressos en estat completat ÷ ingressos reals
- **Estimació d'ingressos en estat completat**: ingressos restants ÷ ingressos reals
- **Variància d'ingressos**: ingressos previstos ÷ ingressos previstos en estat completat


> [!NOTE]
> El Project Operations només mostra els ingressos laborals a la pàgina **Projecte** a la pestanya **Seguiment**. Tot i que els materials i les despeses es poden calcular i fer-ne el seguiment del consum, aquests ingressos no s'inclouen als ingressos que es mostren a la pestanya **Seguiment**. Aquesta pestanya està dissenyada per funcionar només per tornar a projectar els ingressos laborals amb una nova projecció de l'esforç.  
> Tots els imports d'ingressos mostrats es converteixen a la moneda de cost del projecte. La moneda de cost del projecte és la moneda de la unitat de contractació del projecte. Per als projectes de preu fix, les xifres d'ingressos de la visualització **Seguiment d'ingressos laborals** no són rellevants perquè els valors reals de vendes no facturades no es registren en l'aprovació del temps.
> Els valors de vendes estimats per al temps que es mostren a la pestanya **Estimació del projecte** no poden tenir un valor superior al valor dels ingressos previstos de la pestanya **Seguiment**. L'origen d'aquesta discrepància es deu a dos possibles motius:
><ol>
   ><li> A la pestanya <b>Estimacions</b> es mostren els ingressos estimats en la moneda de vendes, mentre que a la pestanya <b>Seguiment</b> es mostren els ingressos previstos convertits a la moneda de cost. </li>
   ><li> Quan les vendes estimades es converteixen a la moneda del contracte tal com es mostra a la pestanya <b>Estimacions</b>, a la moneda del projecte, la conversió implica passos que podrien provocar alguna pèrdua de precisió: </li>
><ol>
><li> L'import de vendes previst en la moneda del contracte es converteix primer a la moneda base (conversió 1).</li>
><li> L'import de vendes previst en la moneda base es converteix a la moneda de cost del projecte (conversió 2). </li>
></ol>
></ol>
> La precisió de moneda s'aplica en ambdós passos, la qual cosa es tradueix en una desviació dels ingressos previstos en la moneda del projecte a partir de les vendes previstes en la moneda del contracte.
   

## <a name="reprojecting-revenues-on-leaf-node-tasks"></a>Tornar a projectar els ingressos en les tasques dels nodes fulla

Els ingressos laborals en una tasca de node fulla es poden tornar a projectar directament a la pestanya **Seguiment** de la pàgina **Projecte**. Tanmateix, podeu utilitzar la visualització **Seguiment de l'esforç** per tornar a projectar l'esforç restant d'una tasca. Això fa que es tornin a calcular els ingressos restants a la tasca. A continuació es mostra una descripció de com funciona això.

1. Un administrador de projecte pot tornar a projectar l'esforç de les tasques actualitzant el valor per defecte del camp **Esforç restant** amb una nova estimació de l'esforç restant en la tasca. La nova projecció fa que es torni a calcular la previsió d'esforç de la tasca en estat completat (EAC), el percentatge de progrés i la variància de l'esforç previst en una tasca. També es torna a calcular l'EAC, l'estimació per completar (ETC) i el percentatge de progrés de les tasques de resum, i produeixen una nova projecció de la variació d'esforç.
2. Segons el valor nou de l'esforç restant de la tasca, el sistema calcula els ingressos restants a la visualització **Seguiment dels ingressos**. Per calcular els ingressos restants segons l'esforç restant, el sistema calcula primer els ingressos mitjans d'una hora d'esforç en la tasca de resum com a ingressos o esforç previstos. Els ingressos previstos són la suma dels ingressos de totes les assignacions de recursos de la tasca. Els ingressos mitjans per hora s'utilitzen per calcular els ingressos restants de l'esforç restant que s'ha projectat recentment a la tasca.
3. Es tornen a calcular els ingressos previstos en estat complet i el percentatge de consum dels ingressos de la tasca del node fulla.
4. Es torna a calcular el valor dels ingressos en estat complet de les tasques de resum fins al node arrel.

## <a name="reprojecting-revenues-on-summary-tasks"></a>Tornar a projectar els ingressos en les tasques de resum

Podeu tornar a projectar els ingressos laborals en tasques de resum o tasques de contenidor. Amb tot, no podeu tornar a projectar directament els ingressos laborals en una tasca de projecte de resum a la pestanya **Seguiment** de la pàgina **Projecte**. De manera similar a les tasques dels nodes fulla, la nova projecció de tasques de resum i de contenidor es pot fer mitjançant la visualització **Seguiment d'esforços**. En aquesta visualització, podeu tornar a projectar l'esforç restant d'una tasca de resum, cosa que farà que es tornin a calcular els ingressos restants de la tasca de resum. A continuació es mostra una descripció de com funciona això.

1. Un administrador de projecte pot tornar a projectar l'esforç de les tasques actualitzant el valor per defecte del camp **Esforç restant** amb una nova estimació de l'**Esforç restant** en la tasca. La nova projecció fa que es torni a calcular l'estimació de la tasca en estat completat (EAC), el percentatge de progrés i la variància de l'esforç previst en una tasca. També es torna a calcular l'EAC, l'ETC i el percentatge de progrés de les tasques de resum, i produeixen una nova projecció de la variació d'esforç.
2. Segons el valor nou del camp **Esforç restant** de la tasca, el sistema calcula els ingressos restants a la visualització **Seguiment dels ingressos**. Per calcular els ingressos restants segons l'esforç restant, el sistema calcula primer els ingressos mitjans d'una hora d'esforç en la tasca de resum com a ingressos o esforç previstos. Els ingressos previstos són la suma dels ingressos de totes les assignacions de recursos de la tasca. Aquests ingressos mitjans per hora s'utilitzen aleshores per calcular els ingressos de l'esforç restant que s'ha projectat recentment a la tasca.
3. Es tornen a calcular els ingressos previstos en estat complet i els percentatges de consum dels ingressos de la tasca de resum.
4. El nou valor dels ingressos previstos en estat completat es distribueix cap avall a les tasques secundàries en la mateixa proporció que els ingressos previstos originals eren a la tasca.
5. Es calculen els nous ingressos previstos en estat completat nou en cadascuna de les tasques individuals fins a les tasques de node fulla. Segons aquest valor, a les tasques secundàries afectades per sota dels nodes fulla es tornaran a calcular els ingressos restants i el percentatge d'ingressos basant-se en els ingressos en estat completat. Això es tradueix en una nova projecció per a la variància dels ingressos de la tasca. 
6. Es torna a calcular el valor dels ingressos en estat complet de les tasques de resum fins al node arrel.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

