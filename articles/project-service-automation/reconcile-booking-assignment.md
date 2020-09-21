---
title: Conciliar reserves i assignacions
description: Aquest tema proporciona informació sobre els valors reals.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 11/27/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 614352ba-dbd8-4fa5-8225-d54f9ec0e218
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 27fc7b6abb4c9a7a761059a2f392f13bc0dd14f9
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749576"
---
# <a name="reconcile-bookings-and-assignments"></a>Conciliar reserves i assignacions

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Les reserves de projectes dels membres d'un equip del projecte i les assignacions de tasques de projectes estan lleugerament vinculades. Per tant, un recurs pot tenir assignacions de tasques que no corresponen a reserves i reserves que no corresponen a assignacions de tasques. Idealment, les reserves i assignacions de projectes estan alineades perquè els recursos tinguin capacitat confirmada de dur a terme les assignacions de tasques. Tanmateix, la realitat és que les reserves es poden produir segons la disponibilitat, i els temps de les tasques poden canviar al llarg del cicle de vida del projecte. Per tant, la lleugera vinculació permet flexibilitat.

A causa de la lleugera vinculació de les reserves de projectes i de les assignacions de tasques, s'inclou una pestanya **Conciliació** a l'entitat Projecte. Aquesta pestanya ajuda als administradors de projectes conciliar les reserves dels membres de l'equip i els seus treballs per a l'equip del projecte.

Per a cada membre de l'equip, la pestanya **Conciliació** mostra les reserves i les assignacions fins a l'assignació de tasques individuals. Mostra hores a les cel·les que poden representar períodes de temps de mesos a dies.

Al camp **Escala de temps**, podeu seleccionar **Mes**, **Setmana**o **Dia**. Se selecciona **Setmana** per defecte. No obstant, podeu canviar el valor per defecte seleccionant el botó **Configuració**. Quan s'obre la pestanya **Conciliació**, es mostra la data actual, però podeu utilitzar el control de calendari per avançar o retrocedir en el temps. Quan un projecte té una data d'inici que es troba en el futur, la pestanya mostra la data en què s'ha obert. El control de calendari també té opcions que us permeten desplaçar-vos a les dates d'inici i d'acabament del projecte.

Podeu utilitzar els controls d'ampliació a cada recurs per mostrar els detalls de les reserves d'aquest recurs. També podeu expandir les assignacions de cada recurs al nivell de tasca individual.

A la part inferior de la pestanya **Conciliació** es mostra un total net global del projecte i la pestanya també inclou una columna total. Per a cada recurs, la pestanya pren la diferència entre les reserves d'un membre de l'equip al projecte i un valor consolidat de les assignacions de tasques d'aquest membre de l'equip. Idealment, la diferència hauria de ser 0 (zero). En altres paraules, no hi hauria d'haver diferències entre les reserves del recurs i les assignacions de tasques. Qualsevol diferència s'indica amb color i ombrejat per indicar a dues condicions:

- **Manca de reserves**: les manques de reserves es produeixen quan un recurs té més assignacions que reserves. Com que aquesta capacitat no s'ha reservat, un administrador de projecte pot corregir aquesta situació ampliant les reserves del recurs fins a cobrir la manca.
- **Excés de reserves**: un excés de reserves es produeix quan un recurs s'ha reservat al projecte però no s'ha assignat a tasques. Aquesta situació pot ser acceptable, per exemple, si el recurs s'ha reservat abans de l'assignació de tasques. No obstant, en altres casos, pot ser que el recurs no estigui planificat per assignar-se a tasques. En aquests casos, l'administrador del projecte hauria de considerar la cancel·lació de les reserves del recurs, de manera que la capacitat pugui utilitzar-se per a un altre projecte.

> [!NOTE]
> La llegenda d'aquestes condicions podria estar amagada per deixar més espai per a la quadrícula. En aquest cas, podeu fer que la llegenda sigui visible seleccionant el botó **Configuració**.

En alguns casos, quan el camp **Escala de temps** està definit a un nivell superior a **Dia**, les diferències es poden calcular com a 0 (zero). Per exemple, al nivell de **Mes**, la diferència neta per a un recurs podria ser 0 (zero) per indicar que les tasques equivalen a les reserves. No obstant, si ho mireu al nivell de **Setmana**, podeu veure que hi ha assignacions de 0 (zero) hores i reserves de 40 hores a la primera setmana del mes, i assignacions de 40 hores i reserves de 0 (zero) hores a la segona setmana del mes. Tot i que les reserves i assignacions totals per al mes són iguals, difereixen per setmana.

Quan visualitzeu el temps en nivells superiors, la pestanya **Conciliació** mostra un indicador a les cel·les per informar-vos que hi ha diferències en nivells de temps inferiors. Per exemple, en la il·lustració següent, un indicador de cel la apareix a la cel·la per al mes d'octubre de 2018 per al recurs que s'anomena Gabriela Magrinyà. Per tant, podeu veure que, tot i que les reserves i assignacions del recurs són iguals quan s'agreguen a nivell de **Mes**, no coincideixen en els nivells inferiors.

![Assignacions i reserves no coincidents](media/reconcile-assignments-01.JPG)

Feu doble clic en una cel·la per apropar-vos al nivell inferior següent i visualitzar la diferència. Per exemple, si feu doble clic a la diferència d'octubre de 2018 per a la Gabriela Magrinyà, baixareu fins al nivell de **Setmana**. Llavors podeu veure que el recurs té reserves de 16 hores però cap assignació la primera quinzena d'octubre i 16 hores d'assignacions però cap reserva la tercera setmana d'octubre.

![Assignacions i reserves no coincidents](media/reconcile-assignments-02.JPG)

Podeu fer clic amb el botó dret en una cel·la per allunyar el nivell superior següent. També podeu desactivar l'indicador de la cel·la seleccionant el botó **Configuració**. 

També podeu utilitzar els botons **Anterior** i **Següent** sobre la quadrícula per desplaçar-vos per les diferències en el vostre projecte. Per utilitzar aquests botons, heu de seleccionar primer un recurs. Seleccioneu **Següent** per anar a la diferència següent entre les reserves i les assignacions per a aquest recurs. Seleccioneu **Anterior** per tornar a la diferència anterior.

En situacions en què teniu assignacions de tasques per a un recurs però no reserves, podeu seleccionar la manca de reserves i seleccionar **Amplia la reserva**. A continuació, podeu veure la reserva necessària per tal d'abordar la manca del recurs. També podeu visualitzar les reserves del recurs en el projecte actual i en altres projectes. Seleccioneu **D'acord** per crear la reserva del recurs sense tenir en compte la disponibilitat actual. L'administrador de projectes o administrador de recursos poden utilitzar el tauler de planificació per administrar les situacions en què el recurs té un excés de reserves més enllà de la seva capacitat perquè s'han ampliat les reserves.

## <a name="managing-with-time-zones"></a>Administració amb fusos horaris
Per garantir un resultat precís i predictible quan utilitzeu Amplia la reserva, hi ha dos requisits previs clau que s'han de complir:  

- L'usuari ha de configurar el fus horari del dispositiu perquè coincideixi amb el fus horari definit a la Configuració de personalització del sistema.
 
  ![Configuració de fus horari al Windows 10](media/reconcile-assignments-03.png)

  ![Configuració del fus horari a la Configuració de personalització](media/reconcile-assignments-04.png)
 
- El Recurs reservable ha de tenir com a mínim un minut de temps de treball que se solapi amb els contorns que s'utilitzen per definir l'extensió sol·licitada. Per exemple, a l'exemple següent es mostra una revisió de recursos amb hores de feina que cauen entre les 9:00 h i les 19:00 h. 

  ![Comparativa de contorns de recursos](media/reconcile-assignments-05.png)

La taula següent mostra:

- Una plantilla de calendari de projecte.
- Recurs A: aquest recurs té el mateix calendari i es troba al mateix fus horari que el projecte. L'hora d'inici de les reserves serà les 9:00 h.
- Recurs B: aquest recurs es troba en un fus horari diferent del projecte i, per tant, s'inicia a les 7:00 h en el seu fus horari. No obstant això, les reserves començaran a partir de 9:00 h, que és la primera hora d'inici del contorn d'assignació.
- Recursos C i D: els recursos també es troben en fusos horaris diferents, diferents entre si i el projecte, i les seves reserves no comencen abans que les hores d'inici disponibles respectives.

|Entitat  |Calendari  |
|-|-|
|Plantilla de calendari de projecte   | ![calendari de projecte](media/reconcile-assignments-06.png) |
|Recurs A  | ![Calendari del recurs A](media/reconcile-assignments-06.png) |
|Recurs B  |  ![Calendari del recurs B](media/reconcile-assignments-07.png) |
|Recurs C  |  ![Calendari del recurs C](media/reconcile-assignments-08.png) |
|Recurs D  | ![Calendari del recurs D](media/reconcile-assignments-09.png)  |
 
Quan navegueu a la visualització de conciliació, es visualitzaran les assignacions de recursos i les manques de reserva associades.
 ![Visualització de conciliació abans de l'ampliació](media/reconcile-assignments-10.png)

Després d'executar la característica Amplia la reserva en cada recurs, les reserves s'amplien correctament per a cada recurs. Això és degut a que les hores de feina de cada recurs es solapen amb els contorns de la manca.
 ![Visualització de conciliació després de l'ampliació de la reserva](media/reconcile-assignments-11.png) 

No obstant, una visualització més detallada de les reserves mostra diferències en l'hora d'inici de les reserves. Les reserves no començaran abans que l'hora d'inici del contorn d'assignació i ni abans de l'hora d'inici disponible del recurs.
 ![Noves reserves dels recursos al tauler de planificació](media/reconcile-assignments-12.png)
