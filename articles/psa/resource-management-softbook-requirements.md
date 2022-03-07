---
title: Reservar requisits manera flexible
description: En aquest tema es proporciona informació sobre com reservar requisits de manera flexible.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: 95f064e0f83d2052ac4ae9673b4fcdcd16a2574246d3320e1ed3798cd6ff062b
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "7006999"
---
# <a name="soft-book-requirements"></a>Reservar requisits manera flexible

[!include [banner](../includes/psa-now-project-operations.md)]

Un requisit de recursos es pot reservar de manera fixa. Una reserva fixa crea una proposta que consumeix la capacitat d'un recurs. La proposta s'envia novament al sol·licitant per a la seva aprovació. Una reserva flexible afegeix provisionalment un recurs a un equip del projecte i té un estat diferent al Tauler de planificació, però no consumeix la capacitat del recurs. Per reservar un recurs de manera flexible al Tauler de planificació, definiu el camp **Estat de la reserva** a **Flexible**.

![Estat de la reserva definit com a Flexible.](media/Resource-Management-image77.png)

Quan la pestanya **Equip** està a la visualització **Membres de l'equip amb nom**, el recurs hi apareix. Les hores reservades de manera flexible es comuniquen a la columna **Hores reservades de manera flexible**.

![Hores reservades de manera flexible a la visualització Membres de l'equip amb nom.](media/Resource-Management-image78.png)

Els membres de l'equip reservats de manera flexible no poden assignar-se a tasques.

![Membre de l'equip reservat de manera flexible assignat a una tasca.](media/Resource-Management-image79.png)

A la pestanya **Conciliació**, no es mostra cap reserva per a un recurs reservat de manera flexible , ja que la pestanya **Conciliació** només té en compte les reserves fixes.

![Recurs reservat de manera flexible sense reserves a la pestanya Conciliació.](media/Resource-Management-image80.png)

> [!NOTE]
> No es pot reservar un recurs de manera flexible d'un requisit generat a partir d'un membre de l'equip genèric.

Al Tauler de planificació, s'utilitza un color diferent per a les reserves flexibles d'un recurs.

![Reserves flexibles al Tauler de planificació.](media/Resource-Management-image81.png)

Per convertir una reserva flexible en una reserva fixa, al Tauler de planificació, feu clic amb el botó dret a la reserva flexible i, a continuació, seleccioneu **Canvia l'estat** \> **Reserva fixa** \> **Fixa**.

![Canviar l'estat de la reserva a Fixa.](media/Resource-Management-image82.png)

Es canvia la reserva i l'estat canvia al Tauler de planificació. Com que l'estat de la reserva ara és **Fixa**, el recurs es mostra com a reservat i la seva capacitat i disponibilitat s'ajusten.

Podeu utilitzar el mateix mètode per cancel·lar una reserva fixa o una reserva flexible al Tauler de planificació.

Per convertir un recurs reservat de manera flexible a reservat de manera fixa a la pestanya **Equip** del projecte, seleccioneu el recurs i, a continuació, seleccioneu **Confirma**.

![Ordre Confirma.](media/Resource-Management-image83.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]