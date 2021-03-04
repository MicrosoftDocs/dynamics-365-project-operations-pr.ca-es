---
title: Reservar de manera flexible un recurs
description: En aquest tema es proporciona informació sobre com planificar provisionalment o de manera flexible els membres de l'equip del projecte.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/25/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.app:
- ProjectOperations
ms.openlocfilehash: 2675096085fc4c673d15741042ffc1b82ed3de8b
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146426"
---
# <a name="soft-book-a-resource"></a>Reservar de manera flexible un recurs

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Podeu planificar de forma temptativa o reservar de forma flexible un recurs en un equip de projecte per mostrar que planegeu l'assignació del recurs al projecte. Les reserves flexibles no consumeixen la capacitat disponible d'un recurs i podeu assignar membres d'equip reservats de manera flexible per a projectes. No obstant això, atès que la reserva flexible no consumeix la capacitat d'un recurs, podreu reservar de forma fixa el recurs per a altres tasques dins el mateix període. Els recursos genèrics no poden reservar-se de manera flexible, ni aquests tipus de reserves poden complir una sol·licitud de recursos genèrics.

Els membres de l'equip del projecte amb reserva flexible s'enumeren a la pestanya **Equip** de la pàgina **Projecte**, amb les seves hores reservades a la columna **Hores amb reserva flexible** a la vista **Membres de l'equip amb nom**. Els membres de l'equip amb reserva flexible també s'inclouen al tauler de planificació. Atès que estan reservats de forma flexible, el tauler de planificació no mostra cap consum de capacitat per a aquests recursos. El temps amb reserva flexible no apareix a la pestanya **Conciliació**, ni es mostra al camp **Amplia les reserves** de la pestanya **Conciliació** del tauler de planificació. 

Hi ha dues maneres de reservar de manera flexible un membre de l'equip en un projecte: directament des del tauler de planificació o afegint al membre de l'equip a la pestanya **Equip**. 

## <a name="soft-book-from-the-schedule-board"></a>Reserva flexible des del tauler de planificació
Completeu els passos següents per fer la reserva flexible d'un recurs des del tauler de planificació. 

1. Obriu el tauler de planificació i a la subfinestra **Requisits de reserva** del tauler de planificació seleccioneu la pestanya **Projecte**.
2. Busqueu el projecte per al qual voleu crear una reserva flexible. Si hi ha un gran nombre de projectes a la llista, seleccioneu la capçalera de la columna **Projecte** i, a continuació, utilitzeu el filtre per cercar un o diversos projectes.
3. Seleccioneu el projecte i després arrossegueu-lo i deixeu-lo anar a la quadrícula de temps del recurs.
5. A la subfinestra **Crea una reserva de recursos**, ajusteu la data d'inici i d'acabament, definiu **Estat de la reserva** a **Flexible** i, a continuació, definiu les hores. 
6. Feu clic a **Reserva**. El recurs ara es mostra a la pestanya **Equip** com un recurs del projecte. A la visualització **Membre de l'equip amb nom**, veureu les hores reservades de manera flexible a la columna **Hores reservades de manera flexible**.

> [!NOTE]
> Ara podeu assignar la reserva flexible a tasques a la pestanya **Planificació**. A la pestanya **Conciliació**, el recurs mostra un dèficit de reserva relatiu a la seva assignació de tasques, ja que la pestanya **Conciliació** només té en compte les reserves fixes. Feu servir la funció **Amplia les reserves** per reservar el recurs de manera fixa per eliminar el dèficit de reserves fixes en comparació amb les assignacions de recursos. Haureu de cancel·lar manualment la reserva flexible del recurs mitjançant **Mantén les reserves**.

## <a name="soft-book-on-the-team-tab"></a>Reserva flexible a la pestanya Equip

Podeu afegir membres de l'equip directament a la pestanya **Equip** i després canviar el seu estat de reserva de **Fix** a **Flexible** amb **Mantén les reserves**. Quan afegiu un membre de l'equip d'aquesta manera, sempre resultarà en una reserva fixa llevat que seleccioneu el mètode d'assignació com a **Cap**.

Per utilitzar aquest mètode, completeu els passos següents.

1. A la pàgina **Projecte**, a la pestanya **Equip**, feu clic a **Crea**.
2. Seleccioneu el recurs reservable, la funció, i les dates d'inici i d'acabament.
3. Seleccioneu un mètode d'assignació diferent de **Cap**.
4. Seleccioneu **Desa**. Veureu el recurs a la quadrícula i les seves hores a la columna **Hores reservades de manera fixa**.
5. Manteniu les reserves del recurs seleccionant **Mantén les reserves**.
6. Quan s'obri el tauler de planificació, expandiu el recurs per mostrar les reserves. Veureu que la reserva es mostra com a **Fixa**.
7. Feu clic amb el botó dret a la reserva, a **Canvia estat**, seleccioneu **Reserva flexible** \> **Flexible**. L'estat de la reserva ara és **Flexible**.
8. Després de tancar el tauler de planificació, si mireu la visualització **Membres de l'equip amb nom**, veureu que les hores del recurs s'han mogut de la columna **Hores reservades de manera fixa** a **Hores reservades de manera flexible** a la quadrícula de la pestanya **Equip**.

> [!NOTE]
> Recordeu que quan utilitzeu **Mantén les reserves** per canviar l'estat de **Fix** a **Flexible**, si reserveu un recurs a l'equip i després assigneu tasques al recurs, es conserven les assignacions de tasques per a aquest recurs. No obstant això, en la pestanya **Conciliació**, el recurs tindrà una deficiència de reserva, ja que només es tenen en compte les reserves fixes quan es concilien les reserves amb les assignacions. Feu servir la funció **Amplia les reserves** de la pestanya **Conciliació** per reservar el recurs de forma fixa per eliminar el dèficit de reserves fixes en comparació amb les assignacions de recursos. Haureu de cancel·lar la reserva flexible del recurs mitjançant **Mantén les reserves**.

Quan estigueu a punt per canviar un recurs de membre de l'equip amb reserva flexible per un amb reserva fixa, feu el següent:

1. Al tauler de planificació, expandiu el recurs per mostrar les reserves. Veureu la reserva com a **Flexible**.
2. Feu clic amb el botó dret a la reserva i, a **Canvia l'estat**, seleccioneu **Reserva fixa** \> **Fixa**. L'estat de la reserva ara és **Fixa**.
3. Després de tancar el tauler de planificació, tornar al projecte i obrir la pestanya **Equip**, si mireu la visualització **Membres de l'equip amb nom**, veureu que les hores del recurs s'han mogut de la columna **Hores reservades de manera flexible** a **Hores reservades de manera fixa** a la quadrícula de la pestanya **Equip**. Si el recurs estava assignat a tasques, ja no es mostrarà un dèficit de reserva a la pestanya **Conciliació** ja que les reserves ara seran fixes.

