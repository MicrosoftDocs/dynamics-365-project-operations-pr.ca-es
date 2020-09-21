---
title: Progrés dels projectes i consum de cost
description: En aquest tema es proporciona informació sobre com fer el seguiment del progrés del projecte i del consum de costos.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 0d742164-5469-421d-8917-63160a81f651
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8aa5814938129f30885d8161a7c86197ab013364
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749553"
---
# <a name="project-progress-and-cost-consumption"></a>Progrés dels projectes i consum de cost

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

La necessitat de fer un seguiment del progrés davant d'una planificació varia segons la indústria. Algunes indústries fan el seguiment en un nivell granular, mentre que altres indústries fan el seguiment en un nivell superior. En aquest tema es mostra la manera de planificar per tal de satisfer els requisits de la vostra organització.

## <a name="effort-tracking-view"></a>Vista Seguiment de l'esforç

La visualització **Seguiment de l'esforç** segueix el progrés de les tasques a la planificació. Compara les hores d'esforç real que s'han invertit en una tasca amb les hores d'esforç planificades per a aquesta tasca. El PSA utilitza les següents fórmules per calcular les mètriques de seguiment:

- Percentatge de progrés = Esforç real invertit fins al moment ÷ Esforç planificat per a la tasca 
- Estimació per completar (ETC) = Esforç planificat - Esforç real dedicat fins al moment 
- Estimació per completar (EAC) = Esforç restant + Esforç real dedicat fins al moment 
- Variació d'esforç previst = Esforç planificat – EAC

El PSA mostra una projecció de la variació de l'esforç en la tasca. Si l'EAC és més gran que l'esforç planificat, es preveu que la tasca comporti més temps del que s'ha planejat originalment. Per tant, va per darrere de la planificació. Si l'EAC és més petit que l'esforç planificat, es preveu que la tasca comporti menys temps del que s'ha planejat originalment. Per tant, va per davant de la planificació.

## <a name="re-projecting-effort"></a>Tornar a projectar l'esforç

És habitual que un administrador de projecte revisi les estimacions originals d'una tasca. Les reprojeccions de projectes són la percepció de les estimacions d'un administrador de projecte, donat l'estat actual del projecte. No obstant, no recomanem que els administradors de projectes canviïn els números de la línia de base, ja que la línia de base del projecte representa la font de veritat establerta de l'estimació de la planificació i el cost del projecte, i totes les parts interessades del projecte l'han acordat.

Hi ha dues maneres de fer que un administrador del projecte pugui tornar a projectar l'esforç de les tasques:

- Substituir l'ETC per defecte amb una nova estimació de l'esforç real restant de la tasca. 
- Substituir el percentatge de progrés per defecte amb una nova estimació del progrés real de la tasca.

Cadascuna d'aquestes aproximacions provoca un nou càlcul de l'ETC de la tasca, l'EAC i el percentatge de progrés, i la variació de l'esforç projectat d'una tasca. També es torna a calcular l'EAC, l'ETC i el percentatge de progrés de les tasques de resum, i produeixen una nova projecció de la variació d'esforç.

## <a name="re-projection-of-effort-on-summary-tasks"></a>Reprojecció de l'esforç en tasques de resum

Es pot tornar a projectar l'esforç en tasques de resum o contenidor. Independentment de si l'usuari torna a fer una projecció amb l'esforç restant o el percentatge de progrés de les tasques de resum, s'inicia el següent conjunt de càlculs:

- El valor de l'EAC, l'ETC i el percentatge de progrés de la tasca es calculen.
- El nou EAC es distribueix cap avall a les tasques secundàries en la mateixa proporció que l'EAC original era a la tasca.
- Es calcula l'EAC nou en cadascuna de les tasques individuals fins a les tasques de node fulla. 
- Es torna a calcular l'ETC i el percentatge de progrés per a les tasques secundàries afectades fins als nodes fulla en funció del valor de l'EAC. Això es tradueix en una nova projecció per a la variació de l'esforç de la tasca. 
- Els EAC de les tasques de resum es tornen a calcular fins al node arrel.

### <a name="cost-tracking-view"></a>Visualització de seguiment del cost 

La visualització **Seguiment del cost** compara el cost real que va comportar una tasca amb el cost previst en una tasca. 

> [!NOTE]
> Aquesta visualització només mostra els costos de treball i no inclou els costos de les estimacions de la despesa. 

El PSA utilitza les següents fórmules per calcular les mètriques de seguiment:

- Percentatge de cost consumit = Cost real fins al moment ÷ Cost previst per a la tasca
- Cost per completar (CTC) = Cost planificat - Cost real fins al moment
- EAC = CTC + Cost real fins al moment
- Variació de costos projectats = Cost previst – EAC

Es mostra una projecció de la variació del cost en la tasca. Si l'EAC és més gran que el cost planificat, es preveu que la tasca costi més del que s'ha planejat originalment. Per tant, està per sobre del pressupost. Si l'EAC és més petit que el cost planificat, es preveu que la tasca costi menys del que s'ha planejat originalment. Per tant, està per sota del pressupost.

## <a name="project-managers-re-projection-of-cost"></a>Reprojecció del cost de l'administrador de projectes

Quan es torna a projectar l'esforç, el CTC, l'EAC, el percentatge de cost consumit i la variació de costos projectats es tornen a calcular a la visualització **Seguiment del cost**.

## <a name="project-status-summary"></a>Resum de l'estat del projecte

El seguiment de dades a les visualitzacions **Seguiment de l'esforç** i **Seguiment del cost** mostra el progrés i el consum de costos als nivells de node arrel del projecte, tasques de resum i tasques de nodes fulla. La secció **Estat** de la pàgina **Entitat del projecte** mostra un resum de l'estat a nivell del projecte.

## <a name="status-summary-fields"></a>Camps de resum d'estat

El camp **Estat global del projecte** és un camp editable que mostra l'estat general del projecte. Utilitza una codificació de color, com ara verd, groc i vermell, per indicar un risc cada vegada major. El camp **Comentaris** permet a l'administrador del projecte introduir comentaris específics sobre l'estat. El camp **Estat actualitzat el** no és editable i el valor és una marca de temps que indica quan es va actualitzar l'estat per última vegada.

Els camps **Rendiment de la programació** i **Rendiment del cost** es defineixen a partir de la data de seguiment. Quan la variació de planificació i costos per al node arrel de la visualització **Seguiment de l'esforç** és positiva, podeu definir aquests camps com a **Per davant**. Quan la variació de planificació i costos per al node arrel és negativa, podeu definir-los com a **Per darrere**.
