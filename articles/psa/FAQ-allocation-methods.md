---
title: Mètodes d'assignació de reserves al Project Service Automation
description: En aquest tema es proporciona informació sobre les diferents maneres de fer la reserva d'assignacions.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
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
ms.openlocfilehash: 3dc87a66a4b881a06f2b888c26d9dfaefb419f16
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131332"
---
# <a name="booking-allocation-methods-in-project-service-automation"></a>Mètodes d'assignació de reserves al Project Service Automation

Si afegiu un membre de l'equip directament a un projecte a la pestanya **Equip**, o reserveu un recurs per a un projecte o requisit del Tauler de planificació, hi ha alguns mètodes d'assignació de reserva diferents que podeu utilitzar. Aquest tema explica com funciona cada mètode i quins mètodes podrien dur-vos a l'excés de reserves de recursos.

## <a name="full-capacity"></a>Capacitat total 
El mètode Capacitat total reserva la capacitat total del recurs per a les dates d'inici i fi especificades. Per exemple, si un recurs té un calendari configurat per treballar vuit hores al dia, cinc dies a la setmana, en establir una data d'inici i final que cobreix cinc dies hàbils, es reserva el recurs durant 40 hores. La reserva es realitza sense tenir en compte la capacitat restant del recurs. Si un recurs ja està reservat durant aquest període en altres projectes, les 40 hores es reserven com a hores addicionals, acció que podria derivar en un excés de reserva.

## <a name="remaining-capacity"></a>Capacitat restant
El mètode Capacitant restant només està disponible quan es reserva directament en un projecte mitjançant el Tauler de planificació. Aquest mètode reserva la capacitat disponible del recurs dins de l'interval de dates especificat. Per exemple, si un recurs té una capacitat de 40 hores per setmana i ja s'han reservat 10 hores, fer la reserva per a la mateixa setmana dona com a resultat una reserva per a les 30 hores restants d'aquesta setmana.

## <a name="percentage-capacity"></a>Capacitat percentual
El mètode Capacitat percentual reserva el recurs per a un percentatge de capacitat per a les dates d'inici i final especificades. Per exemple, si un recurs té un calendari configurat per treballar vuit hores al dia, cinc dies a la setmana, en establir una data d'inici i final que cobreix cinc dies hàbils al 50% de la capacitat, es reserva el recurs durant 20 hores. Les reserves individuals per dia es reparteixen equitativament al llarg del període, per exemple, quatre hores per dia en aquest cas. La reserva es realitza sense tenir en compte la capacitat restant del recurs. Si el recurs ja està reservat durant aquest període en altres projectes, les 20 hores es reserven com a hores addicionals, acció que podria derivar en un excés de reserva.

## <a name="evenly-distribute-hours"></a>Hores distribuïdes uniformement
El mètode Hores distribuïdes uniformement reserva el recurs durant un nombre específic d'hores i les distribueix el temps de manera uniforme per dia durant les dates d'inici i fi especificades. Per exemple, si es reserva un recurs durant 20 hores durant un període de cinc dies, aquest mètode distribueix les 20 hores de manera equitativa a quatre hores per dia. La reserva es realitza sense tenir en compte la capacitat restant del recurs. Si el recurs ja està reservat durant aquest període en altres projectes, les 20 hores es reserven com a hores addicionals, acció que podria derivar en un excés de reserva.

## <a name="front-load-hours"></a>Hores de càrrega frontal
El mètode Hores amb càrrega frontal reserva el recurs durant un nombre específic d'hores, carregant les hores per dia durant les dates d'inici i final especificades. La càrrega frontal consumeix la capacitat disponible del recurs en una comanda de "la llei del més ràpid". Per exemple, si la planificació de treball d'un recurs és de vuit hores per dia, cinc dies per setmana i no té reserves actuals, reservar el recurs durant 20 hores en un període de cinc dies hàbils dona com a resultat el següent patró de reserva diària: 

|         Reserves          |    Dia 1    |    Dia 2    |    Dia 3    |    Dia 4    |    Dia 5    |    Total    |
|---------------------------|-------------|-------------|-------------|-------------|-------------|-------------|
|    Reserves existents    |    0        |    0        |    0        |    0        |    0        |    0        |
|    Nova reserva          |    8        |    8        |    4        |    0        |    0        |    20       |

El mètode de càrrega frontal té en compte les reserves existents i la capacitat disponible. Per exemple, si el mateix recurs ja té 20 hores de reserves a la setmana de treball, les noves reserves consumeixen la capacitat restant de la següent manera:

|   Reserves          | Dia 1 | Dia 2 | Dia 3 | Dia 4 | Dia 5 | Total |
|---------------------|-------|-------|-------|-------|-------|-------|
| Reserves existents | 8     | 8     | 4     | 0     | 0     | 20    |
| Nova reserva       | 0     | 0     | 4     | 8     | 8     | 20    |

Atès que es té en compte la capacitat disponible, podeu rebre un missatge d'error si el recurs no té capacitat restant que la reserva pugui absorbir. Amb aquest mètode, no hi pot haver excés de reserves.

## <a name="none"></a>cap
El mètode Cap només està disponible quan es fa la reserva des de la pestanya **Equip** dins d'un projecte. Aquest mètode afegeix el recurs com a membre de l'equip en el projecte, però no crea cap reserva que absorbeixi la capacitat del recurs. Es fa servir quan el membre de l'equip de l'administrador de projectes per defecte s'agrega quan es crea un projecte. L'usuari de l'administrador del projecte que va crear el projecte s'agrega per defecte al projecte, de manera que el registre de l'entitat del projecte té un propietari i hi ha un aprovador. Com que aquest usuari no té cap reserva, si desitgeu reservar el recurs, podeu eliminar-lo i després tornar-lo a afegir mitjançant un mètode d'assignació diferent, o podeu afegir el recurs a les tasques i aleshores utilitzar **Amplia les reserves** a la pestanya **Conciliació** per crear reserves per a les assignacions.

## <a name="allocation-methods-that-lead-to-overbooking"></a>Mètodes d'assignació que condueixen a un excés de reserves
En resum, els següents mètodes d'assignació condueixen a la sobrerreserva si el recurs ja està compromès en altres projectes (o amb altres ordres de treball o entitats programables):

- Capacitat total
- Capacitat percentual
- Hores distribuïdes uniformement

Quan feu servir algun d'aquests tres mètodes d'assignació, no se us notificarà l'excés de reserva de recursos. Per corregir l'excés de reserva, hauríeu d'utilitzar el Tauler de planificació.
