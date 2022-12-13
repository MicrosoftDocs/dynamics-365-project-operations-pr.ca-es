---
title: Crear assignacions de recursos
description: Aquest article proporciona informació sobre la creació d'assignacions de recursos genèriques i amb nom.
author: ruhercul
ms.date: 11/22/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 42dd2906ce8db8844bf4dea232f24aca58a5d951
ms.sourcegitcommit: 9b1136d95f19cc039d675a4a1b0962ca3ec61646
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 11/30/2022
ms.locfileid: "9811981"
---
# <a name="create-resource-assignments"></a>Crear assignacions de recursos

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_


Una assignació de recursos és l'associació directa d'un membre d'un equip de projecte a una tasca de node fulla. En aquest article es proporciona informació sobre les diferents maneres d'assignar recursos.

## <a name="create-a-generic-team-member-through-task-assignment"></a>Crear un membre de l'equip genèric a través de l'assignació de tasques


Quan creeu un membre de l'equip genèric mitjançant l'assignació de tasques, creeu un contenidor o un recurs genèric. Aquest recurs genèric descriu les característiques del recurs anomenat que, en última instància, voleu treballar en les tasques. A continuació, genereu un requisit o envieu una sol·licitud mitjançant el requisit que s'utilitza per cercar i reservar el recurs amb nom.

1. A la quadrícula Planificació d'una tasca, seleccioneu la icona Recurs a la cel·la **Recurs**.
2. Escriviu un nom perquè serveixi com a nom del recurs de marcador de posició. Per exemple: Administrador.
3. Seleccioneu **Crea** i al camp **Creació ràpida del membre de l'equip de projecte**, establiu la funció per al recurs genèric.
4. Assigneu les tasques com calgui a aquest recurs de contenidor si seleccioneu el recurs al **Selector de recursos** per a la tasca. Els recursos enumerats a l'apartat **Membres de l'equip**.
5. Quan hàgiu acabat d'assignar el recurs genèric, a la **pestanya Equip**, seleccioneu el recurs genèric i, a continuació, seleccioneu **Genera un requisit** per crear un requisit de recurs per al recurs genèric.
6. Seleccioneu **Reserva** per al recurs genèric i després utilitzeu el tauler de planificació per buscar i reservar un recurs real. També podeu enviar el requisit de compliment per un administrador de recursos.
7. Quan el recurs genèric es compleix completament amb un recurs amb nom, el recurs genèric s'elimina de l'equip. (El compliment parcial dels requisits de recursos no donarà lloc a una assignació de recursos.) Les assignacions de tasques del recurs genèric s'assignen al recurs anomenat que complia el requisit de recurs genèric.

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a>Assignar un recurs amb nom de la llista de tots els recursos que es poden reservar

Feu servir el quadre de cerca del **Selector de recursos** per cercar tots els recursos reservables actius i assignar-los a una tasca de node fulla. Els recursos assignats d'aquesta manera s'afegeixen a l'equip sense cap tipus de reserves. Això és similar a l'addició d'un membre de l'equip i a seleccionar **Cap** com a mètode d'assignació. El recurs es mostra a les pestanyes **Equip**, **Assignació de recursos** i **Conciliació** com a recursos només amb assignacions i un dèficit de reserves. Si voleu utilitzar-ne la disponibilitat, els podeu reservar.

1. Des de la quadrícula de tasques, el tauler o la cronologia, desplaceu-vos a la cel·la **Assignat a**.
2. Al quadre de cerca, comenceu a escriure un nom. Els resultats de cerca per al nom es mostren al **Selector de recursos** a l'apartat **Altres recursos**.
3. Seleccioneu el recurs que voleu assignar a la tasca o seleccioneu el nom del recurs a **Altres recursos de l'equip**.

## <a name="editing-resource-assignment-contours"></a>Edició dels contorns de l'assignació de recursos

Per defecte, quan els recursos s'assignen a una tasca de la planificació, el seu esforç es distribueix linealment a cada recurs, en funció de les hores de treball d'aquest recurs i del mode de planificació del projecte. Un gestor de projectes pot utilitzar la quadrícula d'assignació de recursos per refinar les estimacions d'esforç de cada recurs assignat a una o moltes tasques en les diferents escales de temps. Aquesta característica ajuda els gestors de projectes a produir estimacions de costos i vendes més precises, que es basen en els contorns d'assignació de recursos que es generen quan s'assigna un recurs a una tasca. A més, els gestors de projectes poden reflectir més fàcilment la demanda de recursos necessària per crear la demanda en un requisit de recursos.

### <a name="navigation"></a>Navegació

Per accedir a la quadrícula d'edició del contorn, el gestor de projectes primer selecciona la **pestanya Tasques** a la pàgina principal del projecte i, a continuació, selecciona la **pestanya Tasques** .

![Pestanya Tasques a la pestanya Tasques de la pàgina principal del projecte.](media/AssignmentGrid.png)

La quadrícula admet dos mètodes d'agrupació: **grup per recurs** i **grup per tasca**. A diferència de la vista de quadrícula, les columnes no són configurables. Les úniques columnes visibles s'assignen a, Nom de la tasca, **Inici** **de l'assignació, Finalització** de la tasca i **Esforç d'assignació**. **·** **·**

Quan la quadrícula es representa inicialment, comença al contorn d'assignació més primerenc. Si la vostra planificació no conté tasques que tinguin esforç, la quadrícula quedarà en blanc i no representarà res.

![Quadrícula d'assignació en blanc.](media/emptyassignmentgrid.png)

Si voleu veure els vostres contorns i diferents escales de temps, la quadrícula d'assignació de recursos només de lectura i la quadrícula de conciliació de recursos també estan disponibles.

### <a name="resource-calendars"></a>Calendaris de recursos

La possibilitat d'editar un contorn per a un dia concret es regeix pels dies laborables del recurs, tal com es reflecteix al seu calendari. Si una cel·la està inhabilitada per a un recurs determinat, aquest recurs no té dies laborables durant aquest període.

Els contorns d'un recurs es poden estendre més enllà de les dates d'inici i finalització actuals de la tasca assignada. Si s'actualitza un contorn de manera que sigui posterior a l'última data de finalització d'una tasca o a la data d'inici més primerenca d'una tasca, es canviarà la data de finalització o la data d'inici de la tasca segons correspongui. Tanmateix, si s'actualitza un contorn de manera que sigui anterior a la data d'inici d'una tasca vinculada a un predecessor, l'actualització fallarà perquè l'assignació activarà que la tasca comenci abans que es completi el seu predecessor i aquest comportament no és compatible actualment.

### <a name="co-authoring"></a>Coautoria

Els canvis a la quadrícula d'assignació de recursos es reflecteixen automàticament en totes les visualitzacions associades, incloses les visualitzacions de gràfic, cronologia, tauler i quadrícula. Si diversos usuaris revisen el projecte al mateix temps, els canvis que faci un usuari es reflectiran a la quadrícula. Per contra, qualsevol canvi que es faci a la quadrícula d'assignació de recursos es mostrarà a la resta d'usuaris que visualitzin el projecte en la mateixa sessió.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
