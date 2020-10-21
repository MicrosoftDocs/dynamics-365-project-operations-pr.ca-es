---
title: Reserva per a un projecte
description: En aquest tema es proporciona informació sobre la reserva d'un recurs a un projecte.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 19128264ed3db7efeeba948155f0ddbdc806c2a0
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/01/2020
ms.locfileid: "3907909"
---
# <a name="book-to-a-project"></a>Reserva per a un projecte

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

Hi ha moments en què un administrador de projectes o un administrador de recursos haurà d'assignar un recurs a un projecte sense un requisit específic que es defineixi a partir d'un membre de l'equip genèric. Això es pot aconseguir d'una de tres maneres.

- Reserva des de la quadrícula membre de l'equip
- Reserva des del tauler de planificació
- Reserva des del formulari **Projecte**

## <a name="book-from-the-team-member-grid"></a>Reserva des de la quadrícula membre de l'equip

Si l'organització opera en mode d'assignació de recursos híbrid, l'administrador del projecte pot reservar un recurs directament al projecte completant els passos següents.

1. Des del projecte, aneu a la quadrícula membres de l'equip i seleccioneu **Nou**.
2. Definiu el nom del càrrec i la funció del recurs.
3. Seleccioneu el recurs que es pot reservar des de la cerca disponible.
4. Després de seleccionar el recurs, definiu la següent informació de camp per reservar el recurs:

    - Data d'inici
    - Data de finalització
    - Mètode d'assignació
    - Hores, si escau
    - Aprovador del projecte

6. Seleccioneu **Desa i tanca**

## <a name="book-from-the-schedule-board"></a>Reserva des del tauler de planificació

Quan un administrador de recursos necessita reservar un recurs directament en un projecte, pot utilitzar el tauler de planificacions i el requisit del projecte. El requisit de projecte és un requisit de recurs que està sempre disponible per a la reserva. Completeu els passos següents per fer una reserva directament a un formulari de projecte des del tauler de planificació.

1. Aneu al tauler de planificació i a la pàgina esquerra, filtreu els recursos que esteu considerant per al requisit.
2. A la subfinestra inferior, seleccioneu la pestanya **Projecte** per visualitzar una llista dels requisits del projecte.
3. Arrossegueu el requisit en un recurs i definiu la informació següent:

    - Data d'inici
    - Data de finalització
    - Estat de la reserva
    - Mètode de reserva
    - Durada

## <a name="book-from-the-project-form"></a>Reserva des del formulari Projecte

Com a administrador de projectes, pot ser que hàgiu de reservar un recurs en un projecte, però només conegueu els criteris en comptes del nom del recurs. Completeu els passos següents per utilitzar l'auxiliar de planificacions per cercar un recurs basat en tots els atributs disponibles del recurs. 

1. Aneu al projecte i seleccioneu **Reserva** per obrir l'auxiliar de planificació.
2. Mitjançant els filtres del costat esquerre de l'auxiliar de planificació, delimiteu els criteris i seleccioneu **Cerca.**
3. Basant-vos en els recursos retornats pels resultats, podeu reservar un recurs.

> [!NOTE]
> Aquest mètode no crea cap reserva per al recurs. En comptes d'això, afegeix el recurs a l'equip. Un cop s'ha afegit el membre de l'equip al projecte, l'administrador del projecte mantenir les reserves o ampliar les reserves per afegir les reserves necessàries al recurs.
