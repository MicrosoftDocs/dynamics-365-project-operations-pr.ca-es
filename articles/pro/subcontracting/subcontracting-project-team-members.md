---
title: Subcontractació de membres de l'equip del projecte
description: En aquest article s'explica com subcontractar els membres de l'equip del projecte a Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 9/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: a2f17d6f270029e3a517e99c7bb518cdb19b8d23
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522783"
---
# <a name="subcontracting-project-team-members"></a>Subcontractació de membres de l'equip del projecte

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

A Microsoft Dynamics 365 Project Operations, podeu optar per subcontractar membres de l'equip de projecte sense personal o amb personal.

- Els membres de l'equip del projecte sense personal tenen assignat un recurs genèric.
- Els membres de l'equip amb personal tenen assignat un recurs amb nom.

Quan vinculeu un membre de l'equip del projecte a una línia de subcontractació, les assignacions a tasques que tingui el membre de l'equip es tornaran a plantejar en funció de la llista de preus de compra adjunta a la subcontractació.  A la **pestanya Estimacions de la** pàgina Detalls **del projecte, seleccioneu el** botó Actualitza els preus per veure els **preus actualitzats** i / o els costos resultants de la decisió de subcontractar. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Subcontractació d'un membre de l'equip del projecte sense personal
La **pàgina de detalls** del membre de l'equip disposa de camps de línies de subcontractació i subcontractació que permeten a un gestor de projectes expressar com vol treure la capacitat requerida d'un subcontractat. Per subcontractar un membre de l'equip del projecte com a recurs genèric, seguiu aquests passos:

1.  Trieu un subcontractista a la pàgina de detalls dels membres de l'equip **·**.

2.  Només pots seleccionar subcontractes amb **Estat esborrany** o **confirmat**. **No es poden seleccionar subcontractes tancades** o **cancel·** lades. 

3.  El **camp Línia subcontractada** es fa visible després de seleccionar un subcontractista.

4.  En l'àmbit **Línia de subcontractació**, només es poden seleccionar línies de subcontractació que siguin per temps. No es poden seleccionar línies de subcontractació per a despeses o material.

5.  El paper per al registre de membres de l'equip del projecte ha de coincidir amb el paper a la línia de subcontractació. Això garanteix que el temps per al paper que s'està estimant en el projecte sigui el mateix que es compra a la línia de subcontractació. 

Quan un membre de l'equip genèric estigui associat a una línia de subcontractació i subcontractació, el **camp Tipus** de treballador de la fila genèrica de membres de l'equip s'actualitzarà a **Treballador del** contracte i **la validesa** del subcontractista s'establirà com a **Vàlid**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Subcontractació d'un membre de l'equip del projecte amb personal
Igual que els membres de l'equip genèrics o sense personal, la capacitat dels membres de l'equip requerida en un projecte també es pot vincular a una subcontractació. Per subcontractar un membre de l'equip del projecte amb nom, seguiu aquests passos:

1.  Assegureu-vos que el recurs anomenat estigui configurat com un tipus de recurs que es pot reservar com a treballador del contracte. A més, assegureu-vos que el **camp Proveïdor** del recurs que es pot reservar coincideixi amb el proveïdor de la subcontracta que esteu seleccionant. 

2.  Només pots seleccionar subcontractes en **Estat esborrany** o **confirmat**. **No es poden seleccionar subcontractes tancades** o **cancel·** lades. 

3.  El **camp Línia subcontractada** es fa visible després de seleccionar un subcontractista.

4.  En l'àmbit **Línia de subcontractació**, només es poden seleccionar línies de subcontractació que siguin per temps. No es poden seleccionar línies de subcontractació per a despeses o material.

5.  El paper per al registre de membres de l'equip del projecte ha de coincidir amb el paper a la línia de subcontractació. Això garanteix que el temps per al paper que s'està estimant en el projecte sigui el mateix que es compra a la línia de subcontractació. 

Els membres de l'equip de projecte nomenats que es constitueixin com a treballadors amb contracte tipus de **recurs** Reservable es mostraran amb un estat de validesa de subcontractació de **No vàlid** si no estan vinculats a una subcontractació. Quan un membre de l'equip de projecte nomenat estigui associat a una línia de subcontractació i subcontractació, el **camp Tipus** de treballador de la fila de membres de l'equip s'actualitzarà a **Treballador del** contracte i **La validesa** del subcontractista s'establirà com a **Vàlid**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
