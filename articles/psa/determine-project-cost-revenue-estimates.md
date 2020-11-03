---
title: Determinar les estimacions de costos i ingressos del projecte
description: Com determinar les estimacions de costos i ingressos del projecte al Project Service
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 1652b39b6c8a703bf198a990eb9047eff9dc9f4c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072220"
---
# <a name="determine-project-cost-and-revenue-estimates"></a>Determinar les estimacions de costos i ingressos del projecte 

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Les estimacions de projecte proporcionen informació visual financera de la feina prevista i planificada a l'estructura del desglossament del treball. La visualització de les estimacions us informa de l'impacte dels costos i dels ingressos de la feina prevista. La visualització d'estimacions proporciona una eina per veure la informació sobre un nombre de dimensions predefinides per informar-vos millor de l'impacte econòmic del projecte.  
  
## <a name="cost-and-sales-value-of-the-project"></a>Cost i valor de les vendes del projecte  
Les llistes de preus de l'[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] defineixen els índexs de cost i facturació per a les funcions que els projectes utilitzen. A partir de les funcions associades a les tasques en l'estructura del desglossament del treball del projecte, podeu determinar l'impacte de costos i ingressos del treball.  
  
## <a name="cost-price-defaulting"></a>Preu de cost per defecte  
Cada projecte pertany a una organització (indicat a **Unitat propietària** en el projecte). La llista de preus associada a la unitat organitzativa propietària determina el preu de cost unitari. L'[!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] determina els preus de cost per a les funcions cercant la combinació de funció, unitat i unitat organitzativa a la llista de preus de cost per obtenir el preu de cost correcte per a la data efectiva en les línies d'estimació.  
  
Si la combinació de funció, unitat i unitat organitzativa no dóna lloc a un preu de cost de la llista de preus de la unitat propietària, la unitat és descarta en favor de la combinació de funció i unitat organitzativa. Si hi ha un preu de cost, aquest preu és converteix a la unitat que heu triat a la línia d'estimació.  
  
Si la combinació de funció i unitat organitzativa no dóna lloc a un preu de cost, la unitat organitzativa es descarta en favor de la combinació de funció i unitat, i s'utilitza el preu per defecte després d'aplicar qualsevol conversió, si és necessari.  
  
 Si no hi ha cap preu per a la funció, aleshores el preu de cost per defecte és 0,00 a la línia d'estimació.  
  
 Tots els imports de costos a les línies d'estimació de cost de projecte utilitzen la moneda de la unitat organitzativa propietària.  
  
## <a name="sales-price-defaulting"></a>Preu de venda per defecte  
La llista de preus de venda es basa en l'entitat de venda a la qual està associada el projecte. La llista de preus de venda associada a l'oferta o contracte determina el preu de venda unitari. Si l'oferta o el contracte té una llista de preus personalitzada, aquesta serà la llista de preus de venda per defecte per a les estimacions de projecte. Si no hi ha cap associació a les entitats de venda, aleshores la llista de preus de venda per defecte configurada a la configuració dels paràmetres serà la llista de preus de venda per defecte del projecte. Cada línia d'estimació té associada una unitat organitzativa de recursos per indicar la unitat organitzativa de la qual es reservaran els recursos per completar la tasca. Els preus de venda per a les funcions associades es determinen cercant la combinació de funció, unitat i unitat organitzativa de recurs a la llista de preus de venda per obtenir el preu de venda correcte per a la data efectiva en les línies d'estimació.  
  
Si la combinació de funció, unitat i unitat organitzativa de recurs no dóna lloc a un preu de venda de la llista de preus de venda, el sistema rebutjarà la unitat i buscarà la combinació de funció i unitat organitzativa de recurs. Si es troba un preu de venda, es convertirà a la unitat que heu triat a la línia d'estimació de venda.  
  
Si el sistema no troba cap preu per a la funció, aleshores el preu de venda per defecte és 0,00 a la línia d'estimació.  
  
La visualització d'estimacions té una visualització de quadrícula que mostra una quadrícula plana de línies de pressupost amb la unitat i el cost total i el preu de venda.  
  
## <a name="time-phased-view-of-project-estimates"></a>Visualització per temps de les estimacions del projecte  
A la visualització per temps per a les estimacions de projecte, les dades de les estimacions de la visualització de quadrícula giren per defecte per funció i mostren una propagació de les dades per la cronologia en l'escala de temps triada.  
  
## <a name="effort-estimate-allocation-based-on-task-mode"></a>Assignació d'estimació d'esforç basat en el mode de tasca  
A la visualització per temps, l'esforç total calculat per a la tasca es distribueix assignant un cert nombre d'hores d'esforç per període de temps d'unitat a l'escala de temps escollida. Al Project Service, el mode de tasca determina com s'assigna l'esforç per a tota la durada de la tasca. Els dos tipus d'assignació són l'assignació uniforme i les hores de feina basades en assignació.  
  
## <a name="work-hours-based-allocation"></a>Hores de feina basades en assignació  
El mode de tasca de planificació automàtica regula que el nombre de recursos calculat per a la tasca s'utilitzi durant totes les hores laborals per dia. Això també s'aplica quan s'està assignant l'esforç dividint-lo entre la durada de les tasques a la visualització per temps. Per exemple, una escala de temps "Dia" per a una tasca que es calcula que es completarà amb un sol recurs, l'esforç assignat per dia no serà superior a les hores de treball diàries definides en el calendari del projecte. Per tant, l'assignació de l'esforç sempre garanteix que els recursos es calculen per utilitzar-se per a una jornada sencera.  
  
## <a name="even-distribution"></a>Distribució uniforme  
El mode de tasca planificada manualment no respecta les hores de treball, el calendari del projecte o el nombre de recursos definit a la tasca. La planificació de la tasca es basa en l'entrada de l'usuari. Per a aquestes tasques, l'assignació de l'esforç per període de temps d'unitat de l'escala de temps escollida no té cap factor límit. L'esforç total a la tasca és divideix i s'assigna de manera uniforme per a cada període de temps d'unitat a l'escala de temps escollida.  
  
D'aquesta manera, el mode de tasca definit a la tasca determina la distribució de l'esforç o l'assignació de l'esforç per període de temps d'unitat a les estimacions per temps.  
  
## <a name="grouping-and-time-phasing-options"></a>Opcions d'agrupament i per temps  
Aquesta visualització us ajuda a entendre la distribució de les estimacions d'esforç, cost i vendes per dia, setmana, mes o any. L'opció Agrupa per permet girar les dades de les estimacions en dues dimensions més: categoria i recurs. Tant a la visualització de quadrícula com a la visualització per temps, podeu triar els camps que es visualitzaran. Els totals per a cada bloc de temps es visualitzen a la part inferior indicant l'esforç, el cost i les vendes totals aproximats per al dia, setmana, mes o any.  
  
El preu de cost i vendes per defecte té efecte per data: quan les tarifes per a les funciones canvien, serà més transparent a la visualització per temps quan es visualitzen les dades d'estimació girades sobre "Recurs" i per temps per setmana.  
  
## <a name="expense-estimates"></a>Estimacions de despeses  
Qualsevol despesa generada en el projecte no relacionada directament amb el treball, es pot registrar a les estimacions de projecte en la visualització de quadrícula. Ho podeu aconseguir mitjançant l'opció **Afegeix estimació de despeses** de la visualització de quadrícula. Les estimacions de despeses es poden registrar per a una tasca específica o per a tot el projecte; podeu escollir categories de despesa en aquestes línies i triar una data provisional en què s'espera que es generi la despesa. Si el cost i la llista de preus de venda associats té preus per defecte, o percentatges de marge comercial definits per a les categories de despesa, s'utilitzarà per defecte la línia d'estimació durant l'associació.  
  
### <a name="see-also"></a>Vegeu també  
 [Guia d'administrador de projectes](../psa/project-manager-guide.md)
