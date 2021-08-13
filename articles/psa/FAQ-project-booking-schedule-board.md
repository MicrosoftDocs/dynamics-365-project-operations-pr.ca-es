---
title: Crear una reserva de projecte des del tauler de planificació
description: En aquest tema es proporciona informació sobre com crear una reserva de projecte des del tauler de planificació.
author: ruhercul
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
ms.openlocfilehash: 513f7fe75cfb7b1658b4be71ed0a17da7b64a1023992e1dada9adca8f0dbf21e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6987604"
---
# <a name="create-a-project-booking-from-the-schedule-board"></a>Crear una reserva de projecte des del tauler de planificació

[!include [banner](../includes/psa-now-project-operations.md)]

Podeu reservar un recurs en un projecte directament a la pestanya **Equip** del projecte o generant un requisit de recursos d'una assignació del membre de l'equip genèric i complint després amb el requisit generat amb un membre de l'equip del projecte.

També podeu reservar un recurs en un projecte directament des del Tauler de planificació. Hi ha dues maneres de fer-ho:

- :**Reserva a partir d'un requisit de recurs generat:** podeu generar un requisit de recurs després de crear un recurs genèric i assignar tasques dins d'un projecte.

- **Reserva des del requisit principal:** els requisits principals es mostren al tauler de planificació de la pestanya **Projecte**. 

- **Reserva des d'un requisit de recurs nou:** podeu crear un requisit de recursos des de zero i associar-lo amb un projecte. Al Tauler de planificació, el requisit de recursos apareix a la pestanya **Obre els requisits**.

## <a name="book-from-a-generated-resource-requirement"></a>Reservar a partir d'un requisit de recursos generat

Podeu crear un recurs genèric i assignar-li una o diverses tasques dins d'un projecte. A continuació podeu generar un requisit de recursos des del membre de l'equip genèric. 

1.  Al Tauler de planificació, aquest recurs apareixerà a la pestanya **Obre els requisits**. És possible que hàgiu d'utilitzar filtres de columna a la quadrícula si teniu molts requisits oberts. 

    ![Pestanya Requisits oberts al Tauler de planificació.](media/FAQ-Project-Booking-Schedule-Board-1.png "Captura de pantalla de la taula de reserves i assignacions")

2. Seleccioneu el requisit. La pestanya **Cerca la disponibilitat** apareixerà a la part superior de la fila seleccionada.
 
3. En seleccionar la pestanya s'obre el mode Auxiliar de programació del Tauler de planificació i filtra els recursos disponibles que compleixen amb els requisits de recursos. Tot seguit, podeu reservar un recurs.

4. També podeu arrossegar i deixar anar la fila seleccionada des de la part inferior del Tauler de planificació a una cel·la de recurs a la quadrícula anterior. Quan el deixeu anar, s'obre la subfinestra **Crea la reserva de recursos** a la dreta.

    Si seleccioneu **Reserva** es reserva el recurs a l'equip del projecte.

![Subfinestra Crea la reserva de recursos.](media/FAQ-Project-Booking-Schedule-Board-6.png "")
 

## <a name="book-from-the-primary-requirement"></a>Reservar des del requisit principal

La creació d'un projecte al Project Service crea automàticament un requisit de recurs denominat Requisit principal. És un requisit buit que s'utilitza per reservar ràpidament un recurs amb el Tauler de planificació sense generar un requisit ni crear-ne un des de zero. Atès que el requisit està buit, haureu d'especificar les dates, així com el mètode d'assignació i les hores, si és necessari. 

1. Per reservar un recurs amb el Requisit principal, al tauler de planificació, seleccioneu la pestanya **Projecte**. Si teniu molts projectes, és possible que hagueu d'utilitzar el filtre de columna a la columna **Projecte**.

   ![Filtres de columna al Tauler de planificació.](media/FAQ-Project-Booking-Schedule-Board-2.png "Captura de pantalla de la taula de reserves i assignacions")

2. Seleccioneu el requisit que té el nom del projecte que busqueu i té una durada de zero (0).

3. Seleccioneu la pestanya **Cerca la disponibilitat** que apareix a la fila. Aquesta acció posa el tauler de planificació en el mode Assistent de planificació i mostra els recursos disponibles que es poden reservar en el projecte.

4. Com que un **Requisit principal** és un requisit buit amb una durada de zero (0), haureu d'establir la duració en la subfinestra **Crea la reserva de recursos** en seleccionar i reservar un recurs.

5. També podeu seleccionar el **Requisit principal del projecte** a la part inferior del tauler de planificació i arrossegar-lo i deixar-lo anar en un recurs per reservar-lo.
 
    Com que un **Requisit principal** és un requisit buit amb una durada de zero (0), haureu d'establir la duració en la subfinestra **Crea la reserva de recursos** en seleccionar i reservar un recurs.
 
    Quan reserveu un recurs mitjançant el **Requisit principal** al tauler de planificació, l'afegiu a l'equip del projecte sense cap assignació.
 
## <a name="book-from-a-new-resource-requirement"></a>Reservar a partir d'un requisit de recursos nou
Completeu els passos següents per fer la reserva des d'un requisit de recurs nou. 

1. Aneu a **Requisits de recursos** i seleccioneu **Crea** per crear un requisit de recursos nou.

2. A la pestanya **Projecte**, seleccioneu un projecte per associar el requisit al projecte.
 
    Al tauler de planificació, aquest requisit acabat de crear es mostra com a **Requisit obert** que podeu complir.

3. Reserveu el recurs per afegir-lo a l'equip del projecte.

4. Ara que el recurs està reservat, heu d'assignar tasques manualment.



[!INCLUDE[footer-include](../includes/footer-banner.md)]