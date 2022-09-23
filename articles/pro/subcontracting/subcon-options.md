---
title: Opcions de subcontractació per a membres de l'equip del projecte
description: En aquest article s'expliquen les opcions de subcontractació per als membres de l'equip del projecte a Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 046b5d38ef7e433d02e3eac2e858a3333e941c45
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522266"
---
# <a name="subcontracting-options-for-project-team-members"></a>Opcions de subcontractació per a membres de l'equip del projecte

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

A Microsoft Dynamics 365 Project Operations, podeu avaluar les opcions de subcontractació disponibles per a un o més membres de l'equip del projecte. Les opcions de subcontractació disponibles permeten:

- Crear una nova subcontractació i/o crear noves línies sobre una subcontractació existent per als membres de l'equip de projecte seleccionats. 
- Reserva contra una línia de subcontractació i subcontractació ja existent. 

Podeu triar entre les opcions de subcontractació disponibles per als membres genèrics de l'equip del projecte o triar entre els membres de l'equip del projecte que han estat empleats amb un recurs anomenat que és un treballador amb contracte. 

No hi ha opcions de subcontractació disponibles per a les següents:

- Membres de l'equip del projecte que han estat contractats amb un empleat. 
- Membres de l'equip del projecte que ja estan associats a una línia de subcontractació i subcontractació. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Subcontractació d'un membre de l'equip del projecte sense personal

Per revisar i triar entre les opcions de subcontractació disponibles per a un membre genèric o sense personal de l'equip del projecte, seguiu aquests passos:

1. Seleccioneu un o més registres de membres de l'equip del projecte on el recurs és un recurs genèric.
2. Assegureu-vos que cap dels registres de membres de l'equip del projecte seleccionats ja estigui subcontractat. 
3. Seleccioneu **Opcions** de subcontractació a la subxarxa de membres de l'equip del projecte. S'obre **el diàleg Opcions de subcontractació**. 
4. Si només heu seleccionat un registre de membre de l'equip del projecte al pas 1, hi haurà disponibles les opcions següents:
    - Crear noves línies de subcontractació. 
    - Reserva contra una subcontracta existent Si heu seleccionat diversos registres de membres de l'equip del projecte al pas 1, l'única opció disponible és crear noves línies de subcontractació.
5. L'opció de reservar contra una línia de subcontractació existent permet seleccionar una línia de subcontractació i subcontractació a la qual es vol reservar. Quan seleccioneu una línia de subcontractació per reservar capacitat, heu d'assegurar-vos que la línia de subcontractació seleccionada sigui per temps i que el paper requerit al membre de l'equip del projecte coincideixi amb el paper que es va comprar a la línia de subcontractació.
6. Quan seleccioneu crear noves línies de subcontractació per als membres de l'equip del projecte, el sistema us permetrà seleccionar la subcontractació que voleu crear aquestes línies. La subcontracta que seleccioneu per crear noves línies ha d'estar en **estat Esborrany**. Amb aquesta opció de crear noves línies de subcontractació per als membres de l'equip de projecte seleccionats, el sistema crearà una línia de subcontractació per temps per a cada membre de l'equip del projecte. El rol, les hores i les dates es copiaran del membre de l'equip del projecte a cada línia de subcontractació que es creï. 
7. Quan un membre de l'equip genèric estigui associat a una línia de subcontractació i subcontractació, el **camp Tipus** de treballador de la fila genèrica de membres de l'equip s'actualitzarà a **Treballador contractat** i el valor de validesa **del** subcontractista s'establirà com a **Vàlid**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Subcontractació d'un membre de l'equip del projecte amb personal

Igual que els membres de l'equip genèrics o sense personal, també podeu veure opcions de subcontractació per a un membre de l'equip del projecte amb personal sempre que el membre de l'equip amb personal sigui un treballador amb contracte. Per revisar i triar entre les opcions de subcontractació disponibles per a un membre de l'equip del projecte amb personal o nomenat, seguiu aquests passos:

1. Seleccioneu un o més registres de membres de l'equip del projecte on el recurs és un treballador amb contracte anomenat.
2. Assegureu-vos que cap dels registres dels membres de l'equip del projecte seleccionats ja estigui subcontractat. 
3. Seleccioneu **Opcions** de subcontractació a la subxarxa de membres de l'equip del projecte. S'obre **el diàleg Opcions de subcontractació**. 
4. Si només heu seleccionat un registre de membre de l'equip del projecte al pas 1, hi haurà disponibles les opcions següents:
      - Crear noves línies de subcontractació.
      - Reserva contra una subcontractació existent.
  Si heu seleccionat diversos registres de membres de l'equip del projecte al pas 1, l'única opció disponible és crear noves línies de subcontractació.
5. L'opció de reservar contra una línia de subcontractació existent permet seleccionar una línia de subcontractació i subcontractació a la qual es vol reservar. A l'hora de seleccionar una línia de subcontractació per reservar capacitat, heu d'assegurar-vos del següent:
      - La línia de subcontractació seleccionada és per temps. 
      - El paper requerit al membre de l'equip del projecte coincideix amb el paper que es va comprar a la línia de subcontractació. 
      - El venedor al qual està associat el treballador contractat és el mateix que el venedor de la subcontracta.
6. Quan seleccioneu crear noves línies de subcontractació per als membres de l'equip del projecte, el sistema us permetrà seleccionar la subcontractació que voleu crear aquestes línies. Amb aquesta opció, t'has d'assegurar que el venedor al qual pertany el treballador contractat és el mateix que el venedor de la subcontractació. 
7. La subcontracta que seleccioneu per crear noves línies ha d'estar en **estat Esborrany**. Amb aquesta opció de crear noves línies de subcontractació per als membres de l'equip de projecte seleccionats, el sistema crearà una línia de subcontractació per temps per a cada membre de l'equip del projecte. El rol, les hores i les dates es copiaran del membre de l'equip del projecte a cada línia de subcontractació que es creï.  
8. Quan un membre de l'equip nomenat estigui associat a una línia de subcontractació i subcontractació, el **camp Tipus** de treballador de la fila de membres de l'equip nomenat s'actualitzarà a **Treballador** contractat i el valor de validesa **del** subcontractista s'establirà com a **Vàlid**.

## <a name="re-costing-subcontractor-assignments"></a>Reimpulsar les assignacions de subcontractistes

Quan un membre de l'equip del projecte (genèric o nomenat) estigui vinculat a línies de subcontractació mitjançant el **diàleg Opcions de subcontractació**, les assignacions a tasques que tingui el membre de l'equip es tornaran a costejar en funció de la llista de preus de compra adjunta a la subcontractació. A la **pestanya Estimacions de la** pàgina Detalls **del projecte, seleccioneu el** botó Actualitza els preus per veure els **preus actualitzats** i / o els costos resultants de la decisió de subcontractar.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
