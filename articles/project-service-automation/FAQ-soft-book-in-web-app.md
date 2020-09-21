---
title: Com puc reservar recursos amb la reserva flexible a la versió 2.x de l'aplicació?
description: En aquest article es descriu com reservar membres de l'equip del projecte mitjançant la reserva flexible amb el Project Service.
author: JohnPBurrows
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.prod: Applies to Project Service version 2.x
ms.technology: ''
ms.assetid: 27063de4-cb0c-436f-970e-c87ebcab92db
ms.author: john.burrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: aad119c0907cdd31220a0d73e6e7d99ee63e2e13
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749505"
---
# <a name="how-do-i-soft-book-resources-in-the-web-app-project-service-app-v2x"></a>Com puc reservar recursos amb la reserva flexible a l'aplicació web (v2.x de l'aplicació del Project Service)?

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Podeu planificar de forma temptativa o reservar de forma flexible un recurs en un equip de projecte per mostrar que planegeu l'assignació del recurs a un projecte. Les reserves flexibles no consumeixen la capacitat disponible d'un recurs. Els membres de l'equip reservat amb flexibilitat no poden assignar-se a les tasques del projecte. Només els recursos amb l'estat Reserva fixa i tipus de confirmació Confirmada poden assignar-se a tasques (suposant que tinguin suficients hores de reserva fixes per cobrir l'esforç d'assignació).

Els membres de l'equip del projecte amb reserva flexible apareixen a la quadrícula Membre de l'equip amb les seves hores reservades de manera flexible que es mostren a la columna Reserva flexible. També apareixen al tauler de planificació. Novament, no indiquen cap consum de capacitat ja que la reserva flexible no consumeix la capacitat d'un recurs.

Hi ha tres formes de reservar un membre de l'equip de forma flexible en un projecte amb el Project Service versió 2.x. Pot fer-se amb el tauler de programació, amb la funció Manteniment de reserves o amb un recurs genèric. Aquests mètodes es descriuen a continuació.

## <a name="soft-book-with-the-schedule-board"></a>Reserva flexible amb el tauler de planificació

Per reservar de manera flexible amb el tauler de programació, seguiu aquest procediment: 
1. Obriu el tauler la planificació.
2. Seleccioneu la pestanya Projecte a la part inferior de la subfinestra Requisits de reserva del tauler de planificació.
3. Busqueu el projecte en el qual voleu crear una reserva flexible. Si teniu molts projectes, feu clic a la capçalera de la columna Projecte i utilitzeu el filtre per trobar el projecte.
4. Feu clic en el projecte, després arrossegueu-lo i deixeu-lo anar a la quadrícula de temps del recurs.
5. Aquesta acció obre la subfinestra Crear la reserva de recursos a la dreta. Ajusteu la data d'inici i finalització, seleccioneu l'estat de la reserva com Flexible i configureu les hores. 
6. Feu clic a Reserva.
7. Al projecte, el recurs ara es mostrarà com un membre de l'equip amb les hores reservades de manera flexible a la columna Reserva flexible.

Tingueu en compte que no podeu assignar-los a les tasques en l'estructura del desglossament del treball (WBS) ja que, perquè s'assignin, els recursos s'han de reservar de manera fixa en l'equip.

## <a name="soft-book-using-the-maintain-bookings-feature"></a>Reserva flexible amb la funció Manteniment de reserves

Per reservar de manera flexible amb la funció Manteniment de reserves, seguiu aquest procediment:
1. Des de la quadrícula membre de l'equip, feu clic a Crea.
2. Seleccioneu el recurs reservable, la funció, des de/fins a.
3. Seleccioneu un mètode d'assignació diferent de Cap:
- Capacitat total
- Capacitat percentual
- Per hores distribuïdes uniformement
- Per hores amb la càrrega frontal
4. Feu clic a Desa. Veureu el recurs a la quadrícula de l'equip i les seves hores indicades com Fixes.
5. Manteniu les reserves del recurs fent clic a Manteniment de reserves.
6. Quan s'obri el tauler de planificació, expandiu el recurs per mostrar les reserves. Veureu que la reserva s'indica com a Fixa.
7. Feu clic amb el botó dret a la reserva, a Canvia estat, seleccioneu Reserva flexible i després Flexible. L'estat de la reserva ara és Flexible.
8. Després de tancar el tauler de planificació, veureu que les hores del recurs han canviat de Fixes a Flexibles en la quadrícula de membres de l'equip.
Recordeu que si reserveu un recurs a l'equip i després assigneu tasques al WBS, quan utilitzeu el manteniment de les reserves per canviar l'estat de Fix a Flexible, s'eliminaran les assignacions de les tasques per a aquest recurs, ja que només es poden assignar a les tasques els recursos reservats de forma fixa.

## <a name="soft-book-by-creating-a-generic-resource"></a>Reserva flexible mitjançant la creació d'un recurs genèric

Genereu un membre de l'equip de recurs genèric, compliu amb el tauler de planificació o la Sol·licitud de recursos i canvieu el tipus durant la reserva per crear una reserva flexible.
Per fer-ho, utilitzeu el següent procediment:

1. En el projecte WBS, assigneu funcions a les tasques per a les quals voleu generar membres genèrics de l'equip.
2. Feu clic a Genera un equip de projecte.
3. A la quadrícula del membre de l'equip del projecte, seleccioneu el recurs genèric i feu clic a Reserva.
4. Al tauler de planificació, seleccioneu el recurs que voleu reservar.
5. A la subfinestra Crea la reserva de recursos del tauler de planificació, canvieu l'estat de la reserva a Flexible.
6. Feu clic a Reserva o a Reserva i surt.

Després de tancar el tauler de planificació, veureu el recurs seleccionat agregat a l'equip amb les hores reservades de forma flexible i les hores assignades. També veureu que el recurs genèric roman a l'equip com a indicador de les tasques que estan assignades a un membre de l'equip reservat de forma flexible.

Quan estigueu a punt per canviar un recurs de membre de l'equip reservat de manera flexible per un de fix per poder assignar-lo a les tasques, feu el següent:

1. Seleccioneu aquest recurs i feu clic a Manteniment de les reserves.
2. Quan s'obri el tauler de planificació, expandiu el recurs per mostrar les reserves. Veureu la reserva marcada com Flexible.
3. Feu clic amb el botó dret a la reserva, a Canvia estat, seleccioneu Reserva fixa i després Fixa. L'estat de la reserva ara és Fix.
4. Després de tancar el tauler de planificació, veureu que les hores del recurs han canviat de Flexibles a Fixes en la quadrícula de membres de l'equip. Ara podeu assignar el recurs a les tasques (sempre que hi hagi una alineació entre les hores reservades de manera fixa i les hores d'esforç de la tasca per a l'assignació). Recordeu que si heu seguit els passos de compliment de recursos genèrics en l'element núm. 3 anterior, quan canvieu l'estat del recurs reservable de flexible a fix, el membre genèric de l'equip s'eliminarà.
