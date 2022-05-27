---
title: Crear assignacions de recursos
description: Aquest tema proporciona informació sobre la creació d'assignacions de recursos genèriques i amb nom.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 2b918392fbcde1071aa52ffa7834938be1acd383
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8576534"
---
# <a name="create-resource-assignments"></a>Crear assignacions de recursos

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_


Una assignació de recursos és l'associació directa d'un membre d'un equip de projecte a una tasca de node fulla. En aquest tema es proporciona informació sobre les diferents maneres d'assignar recursos.

## <a name="create-a-generic-team-member-through-task-assignment"></a>Crear un membre de l'equip genèric a través de l'assignació de tasques


Quan creeu un membre de l'equip genèric mitjançant l'assignació de tasques, creeu un contenidor o un recurs genèric. Aquest recurs genèric descriu les característiques del recurs amb nom en el qual voleu treballar en les tasques. A continuació, genereu un requisit o envieu una sol·licitud amb el requisit que s'utilitzi per buscar i reservar el recurs amb nom.

1. A la quadrícula Planificació d'una tasca, seleccioneu la icona Recurs a la cel·la **Recurs**.
2. Introduïu un nom que servirà per al recurs contenidor. Per exemple: Administrador.
3. Seleccioneu **Crea** i al camp **Creació ràpida del membre de l'equip de projecte**, establiu la funció per al recurs genèric.
4. Assigneu les tasques com calgui a aquest recurs de contenidor si seleccioneu el recurs al **Selector de recursos** per a la tasca. Els recursos enumerats a l'apartat **Membres de l'equip**.
5. Quan hàgiu acabat d'assignar el recurs genèric, a la pestanya **Equip**, seleccioneu el recurs genèric i, a continuació, seleccioneu **Genera un requisit** per crear un requisit de recursos per al recurs genèric.
6. Seleccioneu **Reserva** per al recurs genèric i després utilitzeu el tauler de planificació per buscar i reservar un recurs real. També podeu enviar el requisit de compliment per un administrador de recursos.
7. Quan el recurs genèric es compleix totalment (el compliment de requisit de recursos parcial no resultarà en una assignació de recurs) amb un recurs amb nom, el recurs genèric se suprimeix de l'equip. Les assignacions de tasques del recurs genèric s'assignen als recursos amb nom que han complert els requisits de recursos del recurs genèric.

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a>Assignar un recurs amb nom de la llista de tots els recursos que es poden reservar

Feu servir el quadre de cerca del **Selector de recursos** per cercar tots els recursos reservables actius i assignar-los a una tasca de node fulla. Els recursos assignats d'aquesta manera s'afegeixen a l'equip sense cap tipus de reserves. Això és similar a l'addició d'un membre de l'equip i a seleccionar **Cap** com a mètode d'assignació. El recurs es mostra a les pestanyes **Equip**, **Assignació de recursos** i **Conciliació** com a recursos només amb assignacions i un dèficit de reserves. Si voleu utilitzar-ne la disponibilitat, els podeu reservar.

1. Des de la quadrícula de tasques, el tauler o la cronologia, desplaceu-vos a la cel·la **Assignat a**.
2. Al quadre de cerca, comenceu a escriure un nom. Els resultats de cerca per al nom es mostren al **Selector de recursos** a l'apartat **Altres recursos**.
3. Seleccioneu el recurs que voleu assignar a la tasca o seleccioneu el nom del recurs a **Altres recursos de l'equip**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]