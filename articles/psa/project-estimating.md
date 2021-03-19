---
title: Ingressos i costos del projecte
description: En aquest tema es proporciona informació sobre l'estimació dels costos i dels ingressos del projecte.
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
ms.openlocfilehash: 8afa297190406c7fab8237e16c56cfe232a220af
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5283941"
---
# <a name="project-costs-and-revenue"></a>Ingressos i costos del projecte

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Les estimacions de projecte proporcionen informació visual financera del treball que està previst i planificat a la planificació del projecte. A la pestanya **Estimacions** de la pàgina **Projectes** es mostra l'impacte dels costos i dels ingressos del treball que esteu planejant. També proporciona informació sobre moltes de les dimensions predefinides. 

> ![Pestanya Estimacions](media/project-5.png)

## <a name="cost-and-sales-values-of-the-project"></a>Cost i valors de les vendes del projecte

Les llistes de preus de l' defineixen els índexs de cost i facturació per a les funcions en un projecte. Podeu determinar l'impacte del cost i de l'ingrés del treball segons les funcions associades amb el nom del càrrec i el recurs assignat a una tasca. Si hi ha tasques que no tenen cap assignació (genèrica o amb nom), no podeu obtenir estimacions de cost ni de vendes. Els valors de cost i de vendes tenen en compte la data que es defineix a les llistes de preus.

### <a name="default-cost-price"></a>Preu de cost per defecte  

Cada projecte pertany a una organització. Aquesta organització es mostra en el camp **Unitat de contractació** en el projecte. La llista de preus associada a la unitat de contractació s'utilitza per determinar el preu de cost unitari. Per determinar els preus de cost correctes per a les funcions per a la data definida a les línies d'estimacions, cerqueu la combinació de funció, unitat i unitat organitzativa a la llista de preus de cost. 

Per tal que es puguin calcular els preus de cost, totes les tasques s'han d'assignar a un recurs. Qualsevol tasca no assignada tindrà un preu de cost de 0,00.

Si la combinació entre la funció, la unitat i la unitat organitzativa no retorna un preu de cost de la llista de preus de la unitat de contractació, el sistema ignora la unitat. En lloc d'això, cerca la combinació de només funció i unitat organitzativa. Si es troba un preu de cost, els factors de conversió s'utilitzen per convertir-lo en la unitat que heu seleccionat a la línia d'estimació.

Si la combinació entre la funció i la unitat organitzativa no retorna un preu de cost, el sistema ignora la unitat organitzativa. En lloc d'això, cerca la combinació de funcions i unitats per definir el preu per defecte (després d'aplicar qualsevol conversió).

Si el sistema no troba cap preu per a la funció, el preu de cost a la línia d'estimació per defecte és **0,00**. Tots els imports de costos a les línies d'estimació de cost de projecte es registren en la moneda de la unitat de contractació.

> [!NOTE]
> Per defecte, el Microsoft Dynamics 365 emmagatzema els imports de cost en la moneda base. No obstant, les quantitats de cost que es mostren a la pestanya **Estimacions** es mostren a la moneda de la unitat de contractació.  

### <a name="default-sales-price"></a>Preu de vendes per defecte 

La llista de preus de vendes ve determinada per l'entitat de vendes a la qual està adjunta el projecte o el client del projecte. Quan una entitat de vendes, com ara l'oportunitat, l'oferta o el contracte, està associada amb el projecte, el preu de venda de l'entitat sales ve determinat per la llista de preus associada amb l'oferta o el contracte. Si l'oferta o el contracte té una llista de preus personalitzada, aquesta llista de preus s'utilitza com a llista de preus de venda per defecte per a les estimacions de projecte. Si no hi ha cap associació amb entitats de vendes, la llista de preus de vendes per defecte dels paràmetres s'utilitza com a llista de preus de vendes per defecte del projecte juntament amb la moneda del client definida en el projecte.

Cada línia d'estimació té una unitat de recursos associada. La unitat de recursos indica la unitat organitzativa en què s'han reservat els recursos per completar la tasca. Per determinar el preu de venda de les funcions associades, cerqueu la combinació de funció, unitat i recursos de la unitat a la llista de preus de vendes. Si no hi ha cap assignació sobre la tasca, el preu de venda de la tasca és 0,00.

Si la combinació entre la funció, la unitat i la unitat de recursos no retorna un preu de vendes de la llista de preus de vendes, el sistema ignora la unitat. En lloc d'això, cerca la combinació de només funció i unitat de recursos. Si es troba un preu de vendes, els factors de conversió s'utilitzen per convertir-lo en la unitat que heu seleccionat a la línia d'estimació de vendes. 

Si la combinació entre la funció i la unitat de recursos no retorna un preu de vendes de la llista de preus de vendes, el sistema ignora la unitat de recursos. En lloc d'això, cerca la combinació de funcions i unitats per definir el preu per defecte (després d'aplicar qualsevol conversió).

Si el sistema no troba cap preu per a la funció, el preu de vendes a la línia d'estimació per defecte és **0,00**.

La pestanya **Estimacions** té una visualització de quadrícula que mostra les línies d'estimació. La quadrícula inclou columnes per a la unitat, el preu de cost total i el preu total de venda, com es mostra a la il·lustració següent. 

> ![Visualització de quadrícula de la pestanya Estimacions](media/project-6.png)

## <a name="time-phased-view-of-project-estimates"></a>Visualització per temps de les estimacions del projecte

La visualització per temps d'estimacions del projecte mostra les dades d'estimacions de la visualització de quadrícula a la cronologia, en una escala de temps que seleccioneu. Per defecte, les dades d'estimacions se centren en la dimensió **Funció**.

> ![Visualització per temps de les estimacions del projecte](media/project-7.png)

## <a name="allocating-estimated-effort-based-on-the-task-mode"></a>Assignació d'estimació d'esforç basat en el mode de tasca

A la visualització per temps, distribuïu l'esforç total que s'estima per a la tasca assignant hores d'esforç per període de temps d'unitat a l'escala de temps seleccionada. El mode de tasca determina com s'assigna l'esforç per a tota la duració de la tasca. Els dos tipus d'assignació són **Uniforme** i **Basada en hores de treball**.

### <a name="work-hours-based-allocation"></a>Assignació basada en hores de treball
 
En el mode de tasca de planificació automàtica, les hores per defecte diàries dels recursos de tasques es defineixen a la tarifa per hora de treball completa. Aquest comportament s'aplica quan s'ha assignat l'esforç dividint-lo entre la durada de la tasca a la visualització per temps. Per exemple, si estimeu que una tasca es completarà amb un sol recurs a l'escala de temps **Dia**, l'esforç assignat per dia no serà superior a les hores de treball diàries definides en el calendari del projecte. Per tant, l'assignació de l'esforç sempre garanteix que els recursos s'estimen per utilitzar-se per a una jornada sencera.

### <a name="even-allocation"></a>Assignació uniforme

Al mode de tasca planificada manualment, no s'utilitzen les hores de treball del calendari del projecte. En el seu lloc, la planificació de la tasca es basa en l'entrada de l'usuari. Per a aquestes tasques, l'assignació de l'esforç per període de temps d'unitat de l'escala de temps seleccionada no té cap factor límit. L'esforç total a la tasca es divideix i s'assigna de manera uniforme per a cada període de temps d'unitat a l'escala de temps seleccionada. D'aquesta manera, el mode de tasca definit a la tasca determina la distribució de l'esforç o l'assignació de l'esforç per període de temps d'unitat a les estimacions per temps.

## <a name="grouping-and-time-phasing-options"></a>Opcions d'agrupament i per temps

La visualització per temps us mostra la distribució de les estimacions d'esforç, cost i vendes per dia, setmana, mes o any. Per defecte, les dades d'estimacions se centren en la dimensió **Funció**. No obstant, podeu utilitzar l'opció **Agrupa per** per centrar-la en dues dimensions més: **Categoria** i **Recurs**.

A la visualització de quadrícula i a la visualització per temps, podeu seleccionar els camps que es mostren. Els totals per a cada bloc de temps es mostren a la part inferior del projecte. Mostren el total d'esforç, cost i vendes previstos per al dia, la setmana, el mes o l'any. El preu de cost per defecte i el preu de venda són efectius segons la data. En altres paraules, canvien per cada recurs, basant-se en la visualització de temps que seleccioneu.

## <a name="expense-estimates"></a>Estimacions de despeses

El botó **Afegeix un valor d'estimació de despeses** a la quadrícula us permet registrar les despeses que s'han generat en el projecte, però que no estan directament relacionades amb el treball. Podeu registrar les estimacions de la despesa per a una tasca concreta o per a tot el projecte. Seleccioneu les categories de despeses i la data provisional en què espereu generar la despesa. Si la llista de preus de cost i la llista de preus de venda associades tenen preus per defecte (o percentatges de marge comercial definits per a les categories de despesa), s'introduiran automàticament a la línia d'estimació en el moment de l'associació.


[!INCLUDE[footer-include](../includes/footer-banner.md)]