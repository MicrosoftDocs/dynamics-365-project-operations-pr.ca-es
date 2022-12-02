---
title: Planificació externa
description: Aquest article proporciona informació sobre la planificació externa.
author: ruhercul
ms.date: 10/31/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 746fb3a7c812b2b387ec707e58796d02d2473847
ms.sourcegitcommit: b1a5b9bb8b826678fc52f1d5a3d199a71caccb0a
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 11/03/2022
ms.locfileid: "9736981"
---
# <a name="external-scheduling"></a>Planificació externa

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

El mode de planificació externa us permet crear, actualitzar i suprimir entitats relacionades amb les estructures del desglossament del treball (WBS), però sense els límits actuals que aplica el Microsoft Project for the Web. També proporciona una validació limitada. Aquest mode només l'han d'utilitzar els clients següents:

- Clients que tenen les eines necessàries per definir una WBS fora de la lògica de planificació proporcionada pel Project Operations
- Clients que han d'administrar la jerarquia de planificacions, dependències o la durada de tasques

> [!IMPORTANT]
> És possible que les dades no s'introdueixen correctament a les entitats relacionades amb la WBS no es representin a la quadrícula de reconciliació de recursos, a la quadrícula d'estimacions, a la quadrícula de seguiment o a la quadrícula d'assignació de recursos.

## <a name="configuration"></a>Configuració

Per defecte, aquesta característica està habilitada. Tanmateix, a la pàgina principal estàndard dels projectes, el camp relacionat no és visible per defecte. Per habilitar el camp, al Maker Portal, obriu la pàgina principal de l'entitat del projecte, seleccioneu el camp **Motor de planificació** i, a continuació, canvieu el camp a **Visible per defecte**. Si no utilitzeu la pàgina principal estàndard del projecte, editeu la pàgina existent i afegiu-hi el camp **Motor de planificació**.

## <a name="settings"></a>Configuració

Per utilitzar el mode de planificació externa, primer heu de crear un projecte nou i seleccionar el motor de planificació **Planificat externament** a la llista desplegable de la pàgina principal del projecte. Un cop configurat aquest mode per a un projecte, no es pot canviar.

## <a name="viewing-the-wbs"></a>Visualitzar la WBS

Si es planifica externament un projecte, l'accés al Project for the Web està restringit a aquest projecte. Per visualitzar la WBS, heu d'anar a la quadrícula de seguiment, on es mostra la WBS completa.

## <a name="creating-and-editing-the-wbs"></a>Crear i editar la WBS

Si la planificació externa està habilitada per a un projecte, heu de definir les dades per a totes les entitats relacionades amb la WBS, com ara tasques, membres de l'equip, assignacions de recursos i dependències.

A la il·lustració següent es mostra el model de dades per a la planificació de projectes.

![Model de dades de planificació del projecte.](media/projectplanningdatamodel.png)

## <a name="functional-limitations"></a>Limitacions funcionals

No es permeten les operacions següents als projectes planificats externament.

### <a name="project-planning"></a>Planificació del projecte

- **Còpia del projecte**: aquesta operació no s'admet als projectes planificats externament.
- **Desplaçament del projecte**: els canvis en la data d'inici d'un projecte no faran que es mogui l'inici de les tasques o les assignacions de recursos a la WBS.
- **Actualització de l'administrador del projecte**: els canvis a l'administrador del projecte a la pàgina principal del projecte no crearan automàticament un nou membre de l'equip del projecte fins que s'hagi convertit el projecte.
- **Actualització de la plantilla d'hores de feina del projecte**: els canvis a la plantilla d'hores de feina del projecte no faran que es torni a calcular la planificació del projecte.
- **Contorns de l'assignació de recursos** : la creació d'assignacions de recursos no actualitzarà automàticament el camp **mdyn\_PlannedWork**. Aquest camp s'utilitza per emmagatzemar contorns per a l'esforç d'assignació de recursos. Si mostreu l'esforç per fases de temps a la quadrícula d'assignació de recursos o la quadrícula de reconciliació de recursos, heu de definir contorns d'assignació de recursos vàlids. Aquests contorns s'han de formatar correctament per tal que activin el càlcul tant de contorns de cost com de contorns de preus de venda. Es recomana crear un projecte de prova planificat pel Project for the Web i revisar les dades associades per confirmar els requisits i el format.

### <a name="resource-management"></a>Administració de recursos

- **Compliment de recursos genèrics** : el compliment de recursos genèrics no s'admet per a projectes planificats externament. En intentar complir els requisits oberts actius es crearan membres nous de l'equip del projecte, però no se suprimirà el membre de l'equip genèric ni se substituirà el membre de l'equip genèric en cap assignació de recursos existent.
- **Supressió de membre de l'equip** : la supressió d'un membre de l'equip no suprimirà automàticament les assignacions de recursos.

### <a name="quoting-and-contracting"></a>Ofertes i contractació

- **Importació de detalls de línia d'oferta i de línia de contracte**: quan s'importen detalls de línia d'oferta o de línia de contracte des d'un projecte, l'aplicació s'ha provat per donar suport a un màxim de només 500 tasques a la WBA, amb un límit de 20 assignacions per tasca.

### <a name="actuals-and-invoicing"></a>Valors reals i facturació

- Tot i que no hi ha canvis en les validacions existents entre la WBS i les transaccions financeres, és important que us ajusteu al model de dades estàndard per assegurar-vos que totes les transaccions posteriors s'executin com està previst.
