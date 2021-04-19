---
title: Seguiment de l'esforç del projecte
description: En aquest tema es proporciona informació sobre com fer el seguiment de l'esforç del projecte i el progrés de la feina.
author: ruhercul
manager: AnnBe
ms.date: 03/22/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: ead8821c8861ded1e7afd5c192af414f758edef9
ms.sourcegitcommit: a1f9f92546ab5d8d8e5a4710ce4c96414ea55d14
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 03/24/2021
ms.locfileid: "5710928"
---
# <a name="project-effort-tracking"></a>Seguiment de l'esforç del projecte

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

La necessitat de fer un seguiment del progrés davant d'una planificació varia segons la indústria. Algunes indústries fan el seguiment en un nivell granular, mentre que altres indústries fan el seguiment en un nivell superior. En aquest tema es mostra la manera de planificar per tal de satisfer els requisits de la vostra organització.

## <a name="effort-tracking-view"></a>Vista Seguiment de l'esforç

La visualització **Seguiment de l'esforç** fa el seguiment del progrés de les tasques a la planificació comparant les hores d'esforç reals dedicades a una tasca i les hores d'esforç planificades de la tasca. El Dynamics 365 Project Operations utilitza les fórmules següents per calcular les mètriques de seguiment:

- **Percentatge de progrés**: Esforç real dedicat fins al moment ÷ Estimació per completar (EAC) 
- **Esforç restant**: esforç previst en estat completat – esforç real dedicat fins al moment 
- **EAC**: Esforç restant + Esforç real dedicat fins al moment 
- **Variació d'esforç previst**: Esforç planificat – EAC

El Project Operations mostra una projecció de la variació de l'esforç en la tasca. Si l'EAC és major que l'esforç planificat, es preveu que la tasca comporti més temps del que s'havia planejat originalment i duu retard. Si l'EAC és menor que l'esforç planificat, es preveu que la tasca comporti menys temps del que s'havia planejat originalment i va avançada.

## <a name="reprojecting-effort-on-leaf-node-tasks"></a>Tornar a projectar l'esforç en tasques de nodes fulla

Sovint, els administradors de projectes revisen les estimacions originals d'una tasca. Les reprojeccions de projectes són la percepció de les estimacions d'un administrador de projecte, donat l'estat actual del projecte. No obstant això, no recomanem que els administradors de projectes canviïn les quantitats d'esforç previstes. Això es deu al fet que l'esforç previst del projecte representa la font de veritat establerta per a la planificació del projecte i l'estimació de costos, i tots els grups d'interès del projecte ho han acceptat.

Un administrador de projectes pot tornar a projectar l'esforç de les tasques actualitzant el valor per defecte de l'**Esforç restant** amb una nova estimació en la tasca. Aquesta actualització fa que es torni a calcular la previsió de la tasca en estat completat (EAC), el percentatge de progrés i la variància de l'esforç previst en una tasca. També es torna a calcular l'EAC, l'ETC i el percentatge de progrés de les tasques de resum, i produeixen una nova projecció de la variació d'esforç.

## <a name="reprojection-of-effort-on-summary-tasks"></a>Reprojecció de l'esforç en tasques de resum

Es pot tornar a projectar l'esforç en tasques de resum o contenidor. Els administradors de projectes poden actualitzar l'esforç restant en les tasques de resum. L'actualització de l'esforç restant desencadena el següent conjunt de càlculs en l'aplicació:

- El valor de l'EAC i el percentatge de progrés de la tasca es calculen.
- El nou EAC es distribueix cap avall a les tasques secundàries en la mateixa proporció que l'EAC original era a la tasca.
- Es calcula l'EAC nou en cadascuna de les tasques individuals fins a les tasques de node fulla. 
- Es torna a calcular l'esforç restant i el percentatge de progrés per a les tasques secundàries afectades fins als nodes fulla en funció del valor de l'EAC. Això es tradueix en una nova projecció per a la variació de l'esforç de la tasca. 
- Els EAC de les tasques de resum es tornen a calcular fins al node arrel.


## <a name="project-status-summary"></a>Resum de l'estat del projecte

El seguiment de dades a les visualitzacions **Seguiment de l'esforç** i **Seguiment del cost** mostra el progrés i el consum de costos als nivells de node arrel del projecte, tasques de resum i tasques de nodes fulla. La secció **Estat** de la pàgina **Entitat del projecte** mostra un resum de l'estat a nivell del projecte.

## <a name="status-summary-fields"></a>Camps de resum d'estat

El camp **Estat global del projecte** és un camp editable que mostra l'estat general del projecte. Utilitza una codificació de color, com ara verd, groc i vermell, per indicar un risc cada vegada major. El camp **Comentaris** permet a l'administrador del projecte introduir comentaris específics sobre l'estat. El camp **Estat actualitzat el** no és editable i el valor és una marca de temps que indica quan es va actualitzar l'estat per última vegada.

Els camps **Rendiment de la programació** i **Rendiment del cost** es defineixen a partir de la data de seguiment. Quan la variació de planificació i costos per al node arrel de la visualització **Seguiment de l'esforç** és positiva, podeu definir aquests camps com a **Per davant**. Quan la variació de planificació i costos per al node arrel és negativa, podeu definir-los com a **Per darrere**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
