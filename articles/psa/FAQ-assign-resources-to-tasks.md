---
title: Assignar un recurs a una tasca
description: En aquest tema es proporciona informació sobre la manera d'assignar recursos a tasques.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 9/27/2019
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
ms.openlocfilehash: 3f96344b917f088f1d5782c5cee1d84f1aff47bc1bad7c8f6b33307d1df340fa
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6987649"
---
# <a name="assign-a-resource-to-a-task"></a>Assignació d'un recurs a una tasca

[!include [banner](../includes/psa-now-project-operations.md)]

Hi ha tres maneres d'assignar un recurs a una tasca al Microsoft Dynamics 365 Project Service Automation.

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a>Reservar un recurs com a membre de l'equip i després assignar-lo a una tasca

Podeu afegir un recurs a l'equip del projecte i després assignar-lo a tasques en la planificació del projecte.

1. A la pestanya **Membre de l'equip**, afegiu un nou membre de l'equip amb **Crea**. 

2. S'obre la subfinestra **Creació ràpida d'un membre de l'equip**, on es pot seleccionar el nom del recurs que es pot reservar i establir una funció. 

    Seleccioneu un dels següents mètodes d'assignació per a la reserva del recurs:

    - **Capacitat total**: reserva la capacitat total del recurs per a les dates especificades des de i fins a.
    - **Capacitat percentual**: reserva el recurs per a un percentatge de capacitat del recurs per a les dates especificades des de i fins a.
    - **Per hores distribuïdes uniformement**: reserva el recurs durant un nombre específic d'hores i les distribueix de manera uniforme per dia durant les dates d'inici i finalització especificades.
    - **Per hores amb la càrrega frontal**: reserva el recurs durant un nombre específic d'hores, carrega les hores per dia durant les dates especificades des de i fins a.
    - **Cap**: afegeix el recurs a l'equip, però no crea cap reserva que absorbeixi la seva capacitat.

3. A la quadrícula **Planificació** per a una tasca, seleccioneu la icona **Recurs** a la cel·la de recursos i, a continuació, a **Membres de l'equip** seleccioneu el membre de l'equip que acabeu d'afegir. 

> [!NOTE]
> A les pestanyes **Membre de l'equip** i **Conciliació**, el recurs mostra les hores reservades i les assignades. Aquestes hores han de ser iguals, però no són obligatòries perquè les reserves i les assignacions no estan estretament unides. La pestanya **Conciliació** aporta detalls quan són diferents, com quan s'assignen a un recurs més hores de les que heu reservat. Si cal, podeu prendre mesures correctives ampliant les reserves del recurs o canviar-ne l'assignació.

## <a name="create-a-generic-team-member-through-task-assignment"></a>Crear un membre de l'equip genèric a través de l'assignació de tasques

Quan creeu un membre d'equip genèric a través d'una assignació de tasques, heu de crear un contenidor o un recurs genèric que descrigui les característiques del recurs amb nom en el qual voleu treballar en les tasques. A continuació, genereu un requisit (o envieu una sol·licitud amb el requisit) que s'utilitzi per buscar i reservar el recurs amb nom.

1. A la quadrícula **Planificació** d'una tasca, seleccioneu la icona **Recurs** a la cel·la de recursos.

2. Introduïu un nom que servirà per al recurs contenidor. Per exemple: Administrador.

3. Seleccioneu **Crea** i al camp **Creació ràpida del membre de l'equip de projecte**, establiu la funció per al recurs genèric.

4. Podeu seguir assignant tasques a aquest recurs de contenidor si seleccioneu el recurs al **Selector de recursos** per a la tasca. S'enumeren a l'apartat **Membres de l'equip**.

5. Quan hàgiu acabat d'assignar el recurs genèric, seleccioneu-lo a la pestanya **Equip** i, a continuació, seleccioneu **Genera un requisit** per crear un requisit de recursos per al recurs genèric.

6. Seleccioneu **Reserva** per al recurs genèric. A continuació, podeu utilitzar el Tauler de planificació per buscar i reservar un recurs real. També podeu enviar el requisit de compliment per un administrador de recursos.

7. Quan el recurs genèric es compleix amb un recurs amb nom, el genèric s'elimina de l'equip i les assignacions de tasques s'assignen al recurs amb nom que va complir els requisits de recursos del recurs genèric.

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a>Assignar un recurs amb nom de la llista de tots els recursos que es poden reservar

Feu servir el quadre de cerca del **Selector de recursos** per buscar tots els recursos reservables i assignar-los a una tasca.

Els recursos assignats d'aquesta manera s'afegeixen a l'equip sense cap tipus de reserves. Això és similar a l'addició d'un membre de l'equip i a seleccionar Cap com a mètode d'assignació. El recurs es mostra a la pestanya **Equip** i a la pestanya **Conciliació** com a recursos només amb assignacions i un dèficit de reserves. Si voleu utilitzar-ne la disponibilitat, els podeu reservar.

1. A la quadrícula **Planificació** d'una tasca, seleccioneu la icona **Recurs** a la cel·la de recursos.

2. Comenceu a escriure un nom. Els resultats de cerca per al nom es mostren al **Selector de recursos** a l'apartat **Altres recursos**.

3. Seleccioneu el recurs que voleu assignar a la tasca.



[!INCLUDE[footer-include](../includes/footer-banner.md)]