---
title: Subcontractació de membres de l'equip del projecte
description: En aquest tema s'explica com subcontractar els membres de l'equip del projecte a Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f43f817e59ef83fbf4dda6267327080f7c56e0f7
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8587821"
---
# <a name="subcontracting-project-team-members"></a>Subcontractació de membres de l'equip del projecte

[!include [banner](../../includes/dataverse-preview.md)]

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_

A Microsoft Dynamics 365 Project Operations, podeu triar subcontractar membres de l'equip del projecte no autoritzats o amb personal.

- Els membres de l'equip del projecte no autoritzats tenen assignat un recurs genèric.
- Els membres de l'equip amb personal tenen assignat un recurs amb nom.

Quan enllaceu un membre de l'equip del projecte a una línia de subcontractació, les assignacions a les tasques que tingui el membre de l'equip es tornaran a abordar en funció de la llista de preus de compra adjunta a la subcontractació.  A la **pestanya Estimacions** de la **pàgina Detalls** del projecte, seleccioneu el **botó Actualitza els preus per veure els** preus actualitzats i/o els costos resultants de la decisió de subcontractar. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Subcontractar un membre de l'equip del projecte no autoritzat
La **pàgina Detalls del membre de** l'equip té camps de línia de subcontractació i subcontractació que permeten a un gestor de projectes expressar com li agradaria extreure la capacitat requerida d'una subcontracta. Per subcontractar un membre de l'equip del projecte com a recurs genèric, seguiu aquests passos:

1.  Trieu una subcontracta a la pàgina Detall **del membre de l'equip**.

2.  Només podeu seleccionar subcontractes amb **l'estat Esborrany** o **Confirmat**. **No es poden seleccionar subcontractes tancades** o **cancel·lades**. 

3.  El **camp Línia** subcontractada es fa visible després de seleccionar una subcontracta.

4.  **Al camp Línia** subcontractada, només podeu seleccionar les línies de subcontractació que siguin per temps. No podeu seleccionar línies de subcontractació per a despeses o materials.

5.  El rol del registre del membre de l'equip del projecte ha de coincidir amb el rol de la línia de subcontractació. Això assegura que el temps per al paper que s'està estimant en el projecte és el mateix paper que es compra a la línia de subcontractació. 

Quan un membre genèric de l'equip estigui associat amb una línia de subcontractació i subcontractació, el **camp tipus** de treballador de la fila de membres genèrics de l'equip s'actualitzarà a **Treballador** contractat i **la validesa** de subcontractació s'establirà com a **Vàlida**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Subcontractació d'un membre de l'equip del projecte amb personal
Igual que els membres genèrics o no autoritzats de l'equip, la capacitat de membre de l'equip necessari en un projecte també es pot vincular a una subcontracta. Per subcontractar un membre de l'equip del projecte amb nom, seguiu aquests passos:

1.  Assegureu-vos que el recurs amb nom estigui configurat com a tipus de recurs que es pot reservar per a treballadors contractats. A més, assegureu-vos que el **camp Venedor** del recurs que es pot reservar coincideixi amb el proveïdor de la subcontractació que esteu seleccionant. 

2.  Només podeu seleccionar subcontractes a l'estat **Esborrany** o **Confirmat**. **No es poden seleccionar subcontractes tancades** o **cancel·lades**. 

3.  El **camp Línia** subcontractada es fa visible després de seleccionar una subcontracta.

4.  **Al camp Línia** subcontractada, només podeu seleccionar les línies de subcontractació que siguin per temps. No podeu seleccionar línies de subcontractació per a despeses o materials.

5.  El rol del registre del membre de l'equip del projecte ha de coincidir amb el rol de la línia de subcontractació. Això assegura que el temps per al paper que s'està estimant en el projecte és el mateix paper que es compra a la línia de subcontractació. 

Els membres de l'equip del projecte nomenats que es configuren com a tipus de recurs reservable per a treballadors contractats **es** mostraran amb un estat de validesa de subcontracta que **no és vàlid** si no estan vinculats amb una subcontracta. Quan un membre de l'equip del projecte amb nom estigui associat amb una línia de subcontractació i subcontractació, el **camp tipus** de treballador de la fila membre de l'equip s'actualitzarà a **Contract Worker** i **La validesa** de subcontractació s'establirà com a **Vàlida**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
