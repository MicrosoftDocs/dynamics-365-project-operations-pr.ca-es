---
title: Reservar recursos que es poden reservar a un equip de projecte i assignar tasques
description: En aquest tema es proporciona informació sobre la reserva de recursos amb nom a equips de projecte i assignar-los a tasques.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
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
ms.openlocfilehash: 6169f2bdc107e63d666fb32d34f531fd5d472c2f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291427"
---
# <a name="book-named-bookable-resources-to-a-project-team-and-assign-tasks"></a>Reservar recursos que es poden reservar a un equip de projecte i assignar tasques 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Podeu afegir un recurs amb nom a l'equip del projecte reservant-lo directament a l'equip. Per fer-ho, feu els passos següents:

1. Al Project Service Automation, aneu a **Projectes** i, a continuació, seleccioneu el projecte obert al qual voleu reservar.
2. A la pàgina **Projecte**, a la pestanya **Equip**, feu clic a **Crea**. 

![Afegir un membre de l'equip des de la pestanya Equip](media/RM-how-to-1.png)

3. Al quadre de diàleg **Creació ràpida de membre de l'equip**, seleccioneu el recurs que es pot reservar. El camp **Funció** s'emplenarà amb la funció per defecte del recurs si en té assignada una. Podeu canviar la funció si cal. 
4. Seleccioneu les dates d'origen i finalització en què es necessitaran els recursos i seleccioneu el mètode d'assignació de la capacitat del recurs. 
5. Si voleu que el membre de l'equip sigui un aprovador de projecte, seleccioneu **Sí** al camp **Aprovador de projectes**. Això significarà que el membre de l'equip pot aprovar les entrades de despesa i de despeses enviades per a aquest projecte. 
6. Feu clic a **Desa**.

![Afegir un membre de l'equip al formulari de creació ràpida](media/RM-how-to-2.png)


Ara podeu assignar el recurs reservat a les tasques del projecte. A la pàgina **Projecte**, feu clic a la pestanya **Planificació** per assignar tasques al recurs nou. El selector de recursos que s'inicia des del camp **Recursos** de la quadrícula de tasques mostrarà els membres de l'equip que podeu seleccionar.

![Assignar un membre d'un equip a una tasca de la pestanya Planificació](media/RM-how-to-3.png)

A la versió 3 del Project Service Automation (PSA), les reserves de recursos i les assignacions de tasques no estan vinculades estretament. Això vol dir que quan utilitzeu el selector de recursos de la planificació, podeu assignar tasques als membres de l'equip durant més hores de les cobertes per les reserves en el projecte.
Podeu veure les diferències entre les reserves dels membres de l'equip i les assignacions a la pestanya **Equip** o a la pestanya **Conciliació de recursos**. També podeu conciliar les diferències entre reserves i assignacions per als recursos en un nivell més detallat.

![Pestanya Conciliació de recursos](media/RM-how-to-4.png)

També podeu utilitzar el selector de recursos a la pestanya **Planificació** per cercar i seleccionar altres recursos que encara no formen part de l'equip del projecte. Es mostren al selector de recursos com a **Altres recursos**.

![Assignar un recurs no membre de l'equip a una tasca](media/RM-how-to-5.png)

En fer-ho, el recurs s'afegeix a l'equip del projecte i se l'assigna a la tasca, però no es genera cap reserva.

![Membre de l'equip amb assignacions i sense reserves](media/RM-how-to-6.png)

Podeu utilitzar la capacitat d'ampliació de la reserva de la pestanya **Conciliació** o el **Tauler de planificació** per reservar la capacitat del recurs al projecte.

![Ampliar les reserves d'un membre de l'equip a la pestanya Conciliació de recursos](media/RM-how-to-7.png)

Després d'haver reservat un membre de l'equip al vostre projecte, podeu utilitzar el manteniment de les reserves o utilitzar el Tauler de planificació directament per administrar les seves reserves.


[!INCLUDE[footer-include](../includes/footer-banner.md)]