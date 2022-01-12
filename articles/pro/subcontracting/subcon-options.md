---
title: Opcions de subcontractació per als membres de l'equip del projecte
description: En aquest tema s'expliquen les opcions de subcontractació per als membres de l'equip del projecte a Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: 4db283db728b50ccf76eafabfd643313620bbce2
ms.sourcegitcommit: 04dc8d952e6da3ab3eb2a20131c6f7cee6040876
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 12/10/2021
ms.locfileid: "7903627"
---
# <a name="subcontracting-options-for-project-team-members"></a>Opcions de subcontractació per als membres de l'equip del projecte

[!include [banner](../../includes/dataverse-preview.md)]

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_

A Microsoft Dynamics 365 Project Operations, podeu avaluar les opcions de subcontractació disponibles per a un o més membres de l'equip del projecte. Les opcions de subcontractació disponibles permeten:

- Creeu una subcontracta nova i/o creeu línies noves en una subcontracta existent per als membres seleccionats de l'equip del projecte. 
- Reserva contra una línia de subcontractació i subcontractació ja existent. 

Podeu triar entre les opcions de subcontractació disponibles per als membres genèrics de l'equip del projecte o triar entre els membres de l'equip del projecte que han estat equipats amb un recurs amb nom que és un treballador del contracte. 

No hi ha opcions de subcontractació disponibles per al següent:

- Membres de l'equip del projecte que han estat ateses amb un empleat. 
- Membres de l'equip del projecte que ja estan associats a una línia de subcontractació i subcontractació. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Subcontractar un membre de l'equip del projecte no autoritzat

Per revisar i triar entre les opcions de subcontractació disponibles per a un membre genèric o no autoritzat de l'equip del projecte, seguiu aquests passos:

1. Seleccioneu un o més registres de membres de l'equip del projecte on el recurs és un recurs genèric.
2. Assegureu-vos que cap dels registres de membres de l'equip del projecte seleccionats ja estigui subcontractat. 
3. Seleccioneu **Opcions de subcontractació** a la subquadrícula de membres de l'equip del projecte. **S'obre el diàleg Opcions de subcontractació.** 
4. Si només heu seleccionat un registre de membre de l'equip del projecte al pas 1, estaran disponibles les opcions següents:
    - Crear noves línies de subcontractació. 
    - Reserva contra una subcontracta existent Si heu seleccionat diversos registres de membres de l'equip del projecte al pas 1, l'única opció disponible és crear una línia de subcontractació nova.
5. L'opció de reservar contra una línia de subcontractació existent us permet seleccionar una línia de subcontractació i subcontractació contra la qual voleu reservar. En seleccionar una línia de subcontractació per reservar capacitat, heu d'assegurar-vos que la línia de subcontractació seleccionada sigui per temps i que el paper requerit al membre de l'equip del projecte coincideixi amb el paper que es va comprar a la línia de subcontractació.
6. Quan seleccioneu crear noves línies de subcontractació per als membres de l'equip del projecte, el sistema us permetrà seleccionar la subcontractació que voleu crear aquestes línies. La subcontractació a la que seleccioneu per crear línies noves hauria d'estar en **estat** Esborrany. Amb aquesta opció de crear noves línies de subcontractació per als membres seleccionats de l'equip del projecte, el sistema crearà una línia de subcontractació per al temps per a cada membre de l'equip del projecte. El rol, les hores i les dates es copiaran del membre de l'equip del projecte a cada línia de subcontractació que es creï. 
7. Quan un membre genèric de l'equip estigui associat amb una línia de subcontractació i subcontractació, el **camp Tipus de treballador de la fila de membres** genèrics de l'equip s'actualitzarà al **Treballador contractat i el valor de** **validesa de subcontracta** s'establirà com a **Vàlid**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Subcontractació d'un membre de l'equip del projecte amb personal

Igual que els membres genèrics o no autoritzats de l'equip, també podeu veure opcions de subcontractació per a un membre de l'equip del projecte amb personal sempre que el membre de l'equip amb personal sigui un treballador contractat. Per revisar i triar entre les opcions de subcontractació disponibles per a un membre de l'equip del projecte amb personal o amb nom, seguiu aquests passos:

1. Seleccioneu un o més registres de membres de l'equip del projecte on el recurs sigui un treballador del contracte amb nom.
2. Assegureu-vos que cap dels registres dels membres de l'equip del projecte seleccionats ja estigui subcontractat. 
3. Seleccioneu **Opcions de subcontractació** a la subquadrícula de membres de l'equip del projecte. **S'obre el diàleg Opcions de subcontractació.** 
4. Si només heu seleccionat un registre de membre de l'equip del projecte al pas 1, estaran disponibles les opcions següents:
      - Crear noves línies de subcontractació.
      - Reserva contra una subcontracta existent.
  Si heu seleccionat diversos registres de membres de l'equip del projecte al pas 1, l'única opció disponible és crear una línia de subcontractació nova.
5. L'opció de reservar contra una línia de subcontractació existent us permet seleccionar una línia de subcontractació i subcontractació contra la qual voleu reservar. En seleccionar una línia de subcontractació per reservar capacitat, heu d'assegurar el següent:
      - La línia de subcontractació seleccionada és per temps. 
      - El paper requerit en el membre de l'equip del projecte coincideix amb el paper que es va comprar a la línia de subcontractació. 
      - El proveïdor al qual està associat el treballador del contracte és el mateix que el venedor de la subcontractació.
6. Quan seleccioneu crear noves línies de subcontractació per als membres de l'equip del projecte, el sistema us permetrà seleccionar la subcontractació que voleu crear aquestes línies. Amb aquesta opció, heu d'assegurar-vos que el proveïdor al qual pertany el treballador contractat és el mateix que el venedor de la subcontracta. 
7. La subcontractació a la que seleccioneu per crear línies noves hauria d'estar en **estat** Esborrany. Amb aquesta opció de crear noves línies de subcontractació per als membres seleccionats de l'equip del projecte, el sistema crearà una línia de subcontractació per al temps per a cada membre de l'equip del projecte. El rol, les hores i les dates es copiaran del membre de l'equip del projecte a cada línia de subcontractació que es creï.  
8. Quan un membre de l'equip amb nom estigui associat amb una línia de subcontractació i subcontractació, el **camp Tipus de treballador de la fila de membre de** l'equip amb nom s'actualitzarà al **Treballador contractat i el valor de** **validesa de subcontracta** s'establirà com a **Vàlid**.

## <a name="re-costing-subcontractor-assignments"></a>Re-cost de les assignacions de subcontractistes

Quan un membre de l'equip del projecte (genèric o nomenat) està enllaçat a línies de subcontractació mitjançant el **diàleg d'opcions de** subcontractació, qualsevol tasca a les tasques que tingui el membre de l'equip es rea costarà en funció de la llista de preus de compra adjunta a la subcontractació. A la **pestanya Estimacions** de la pàgina Detalls del **projecte**, seleccioneu el **botó Actualitza els preus per veure els preus** actualitzats i/o els costos resultants de la decisió de subcontractar.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
