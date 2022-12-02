---
title: Opcions de subcontractació per a membres de l'equip del projecte
description: En aquest article s'expliquen les opcions de subcontractació per als membres de l'equip del projecte al Microsoft Dynamics 365 Project Operations.
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

Al Microsoft Dynamics 365 Project Operations, podeu avaluar les opcions de subcontractació disponibles per a un o més membres de l'equip del projecte. Les opcions de subcontractació disponibles us permeten:

- Crear un subcontracte nou o crear línies noves en un subcontracte existent per als membres de l'equip del projecte seleccionats. 
- Reservar per a un subcontracte i una línia de subcontracte existent. 

Podeu triar entre les opcions de subcontractació disponibles per als membres genèrics de l'equip del projecte o triar entre els membres de l'equip del projecte que s'han dotat amb un recurs amb nom que és un treballador de contracte. 

No hi ha cap opció de subcontractació disponible per al següent:

- Membres de l'equip del projecte que s'han dotat amb un empleat. 
- Membres de l'equip del projecte que ja s'han associat amb un subcontracte i una línia de subcontracte. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Subcontractació d'un membre de l'equip del projecte sense dotació

Per revisar i triar entre les opcions de subcontractació disponibles per a un membre de l'equip del projecte genèric o no dotat de personal, seguiu aquests passos:

1. Seleccioneu un o diversos registres de membres de l'equip del projecte on el recurs sigui un recurs genèric.
2. Assegureu-vos que cap dels registres de membres de l'equip del projecte seleccionats estigui ja subcontractat. 
3. Seleccioneu **Opcions de subcontractació** a la subquadrícula de membres de l'equip del projecte. S'obrirà el quadre de diàleg **Opcions de subcontractació**. 
4. Si només heu seleccionat un registre de membre de l'equip del projecte al pas 1, hi haurà disponibles les opcions següents:
    - Creeu noves línies de subcontracte. 
    - Reserveu en un subcontracte existent Si heu seleccionat diversos registres de membres de l'equip de projecte al pas 1, l'única opció disponible és crear una línia de subcontracte nova.
5. L'opció de reservar en una línia de subcontracte existent us permet seleccionar una línia de subcontracte i subcontracte amb els quals vulgueu fer la reserva. Quan seleccioneu una línia de subcontracte per reservar capacitat, heu d'assegurar-vos que la línia de subcontracte seleccionada sigui per al temps i que la funció necessària per al membre de l'equip del projecte coincideixi amb la funció que s'ha comprat a la línia de subcontracte.
6. Quan seleccioneu de crear línies de subcontracte noves per als membres de l'equip del projecte, el sistema us permetrà seleccionar el subcontracte que voleu per crear aquestes línies. El subcontracte que seleccioneu per crear línies noves ha de tenir l'estat **Esborrany**. Amb aquesta opció per crear línies de subcontracte noves per als membres de l'equip del projecte seleccionats, el sistema crearà una línia de subcontracte per al temps per a cada membre de l'equip del projecte. La funció, les hores i les dates es copiaran des del membre de l'equip del projecte a cada línia de subcontracte que es creï. 
7. Quan un membre de l'equip genèric s'associa amb una línia de subcontracte i subcontracte, el camp **Tipus de treballador** de la fila del membre de l'equip genèric s'actualitzarà a **Treballador de contracte** i el valor de **Validesa de subcontracte** es definirà com a **Vàlida**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Subcontractació d'un membre de l'equip del projecte amb dotació

Igual que els membres de l'equip genèrics o no dotats, també podeu visualitzar les opcions de subcontractació d'un membre de l'equip de projecte dotat amb personal sempre que el membre de l'equip amb personal sigui un treballador de contracte. Per revisar i triar entre les opcions de subcontractació disponibles per a un membre de l'equip del projecte dotat o amb nom, seguiu aquests passos:

1. Seleccioneu un o diversos registres de membres de l'equip del projecte on el recurs sigui un treballador de contracte amb nom.
2. Assegureu-vos que cap dels registres de membres de l'equip del projecte seleccionats estigui ja subcontractat. 
3. Seleccioneu **Opcions de subcontractació** a la subquadrícula de membres de l'equip del projecte. S'obrirà el quadre de diàleg **Opcions de subcontractació**. 
4. Si només heu seleccionat un registre de membre de l'equip del projecte al pas 1, hi haurà disponibles les opcions següents:
      - Creeu noves línies de subcontracte.
      - Reservar sobre un subcontracte existent.
  Si heu seleccionat diversos registres de membres de l'equip de projecte al pas 1, l'única opció disponible és crear una línia de subcontracte nova.
5. L'opció de reservar en una línia de subcontracte existent us permet seleccionar una línia de subcontracte i subcontracte amb els quals vulgueu fer la reserva. Quan seleccioneu una línia de subcontracte per reservar capacitat, heu d'assegurar-vos del següent:
      - La línia de subcontracte seleccionada és per temps. 
      - La funció necessària al membre de l'equip del projecte coincideix amb la funció adquirida a la línia de subcontracte. 
      - El proveïdor amb el qual està associat el treballador de contracte és el mateix que el proveïdor del subcontracte.
6. Quan seleccioneu de crear línies de subcontracte noves per als membres de l'equip del projecte, el sistema us permetrà seleccionar el subcontracte que voleu per crear aquestes línies. Amb aquesta opció, us heu d'assegurar que el proveïdor al qual pertany el treballador de contracte sigui el mateix que el proveïdor del subcontracte. 
7. El subcontracte que seleccioneu per crear línies noves ha de tenir l'estat **Esborrany**. Amb aquesta opció per crear línies de subcontracte noves per als membres de l'equip del projecte seleccionats, el sistema crearà una línia de subcontracte per al temps per a cada membre de l'equip del projecte. La funció, les hores i les dates es copiaran des del membre de l'equip del projecte a cada línia de subcontracte que es creï.  
8. Quan un membre de l'equip amb nom s'associa amb una línia de subcontracte i subcontracte, el camp **Tipus de treballador** de la fila del membre de l'equip amb nom s'actualitzarà a **Treballador de contracte** i el valor de **Validesa de subcontracte** es definirà com a **Vàlida**.

## <a name="re-costing-subcontractor-assignments"></a>Tornar a calcular els costos de les assignacions de subcontractista

Quan s'enllaça un membre de l'equip del projecte (genèric o amb nom) amb una línia de subcontracte amb el quadre de diàleg **Opcions de subcontractació**, les assignacions a tasques que té el membre de l'equip es tornen a comptar segons la llista de preus de compra adjunta al subcontracte. A la pestanya **Estimacions** de la pàgina **Detalls del projecte**, seleccioneu el botó **Actualitza els preus** per veure els preus actualitzats i/o el cost resultant de la decisió de subcontractar.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
