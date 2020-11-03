---
title: Administració de fusos horaris
description: Quan es crea un projecte, el seu fus horari es basa en el fus horari definit a la plantilla d'hores de treball aplicada.
author: ruhercul
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 27f58f0dacc3404119a719547ad374629c740740
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072150"
---
# <a name="manage-time-zones"></a>Administració de fusos horaris

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_


## <a name="projects"></a>Projectes

Quan es crea un projecte, el fus horari es basa en el fus horari definit a la plantilla d'hores de treball aplicada. A **Projecte** , les dates sempre són relatives a la zona horària de l'usuari que ha iniciat la sessió a cada pestanya, tret de la pestanya de la **Tasca** . Quan visualitzeu l'estructura del desglossament del treball, les dates es mostraran sempre a la zona horària del projecte.

## <a name="tasks"></a>Tasques

Quan es crea una tasca, l'hora d'inici, l'hora d'acabament i les hores/dia estan controlades per les hores de treball del projecte. Per exemple, si es crea una tasca amb un projecte la zona horària del qual és -8 PST i té les següents hores de feina: 9:00 h a 17:00 h de dilluns a divendres, qualsevol tasca creada sense assignació respectarà l'hora d'inici i l'hora d'acabament del calendari del projecte.

## <a name="manage-resources-with-time-zones"></a>Administrar recursos amb fusos horaris

Per obtenir resultats precisos i predictibles quan s'utilitza **Amplia la reserva** , hi ha dos prerequisits clau que s'han de complir:  

- L'usuari ha de configurar el fus horari del dispositiu perquè coincideixi amb el fus horari definit a la **configuració de personalització** del sistema.
 
  ![Configuració de fus horari al Windows 10](media/reconcile-assignments-03.png)

  ![Configuració del fus horari a la Configuració de personalització](media/reconcile-assignments-04.png)
 
- El recurs reservable ha de tenir com a mínim un minut de temps de treball que se solapi amb els contorns que s'utilitzen per definir l'extensió sol·licitada. Per exemple, els recursos següents amb hores de feina entre les 9:00 h i les 19:00 h. 

  ![Comparativa de contorns de recursos](media/reconcile-assignments-05.png)

La taula següent mostra:

- Una plantilla de calendari de projecte
- Recurs A: aquest recurs té el mateix calendari i es troba al mateix fus horari que el projecte. L'hora d'inici de les reserves serà les 9:00 h.
- Recurs B: aquest recurs es troba en un fus horari diferent del projecte i comença a les 7:00 h del seu fus horari. No obstant això, les reserves començaran a partir de 9:00 h, que és la primera hora d'inici del contorn d'assignació.
- Recursos C i D: els recursos es troben ubicats en diferents fusos horaris, diferents entre si i el projecte, i les seves reserves no comencen abans de les seves respectives hores d'inici disponibles.

|Entitat  |Calendari  |
|-|-|
|Plantilla de calendari de projecte   | ![calendari de projecte](media/reconcile-assignments-06.png) |
|Recurs A  | ![Calendari del recurs A](media/reconcile-assignments-06.png) |
|Recurs B  |  ![Calendari del recurs B](media/reconcile-assignments-07.png) |
|Recurs C  |  ![Calendari del recurs C](media/reconcile-assignments-08.png) |
|Recurs D  | ![Calendari del recurs D](media/reconcile-assignments-09.png)  |
 
Quan navegueu a la visualització **Conciliació** , es mostren les assignacions de recursos i les mancances de reserva associades.

![Visualització de conciliació abans de l'ampliació](media/reconcile-assignments-10.png)

Un cop s'ha utilitzat la funcionalitat d'ampliació de la reserva per a cada recurs, les reserves s'amplien correctament per a cada recurs, perquè les hores de feina de cada recurs se superposen amb els contorns de la manca.

![Visualització de conciliació després de l'ampliació de la reserva](media/reconcile-assignments-11.png) 

Observeu que una mirada més profunda dels detalls de les reserves mostra diferències en l'hora d'inici de les reserves. Les reserves no comencen abans de l'hora d'inici del contorn d'assignació ni abans de l'hora d'inici disponible del recurs.

![Noves reserves dels recursos al tauler de planificació](media/reconcile-assignments-12.png)
