---
title: Subcontractació de membres de l'equip del projecte
description: En aquest article s'explica com subcontractar els membres de l'equip del projecte al Microsoft Dynamics 365 Project Operations.
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

Al Microsoft Dynamics 365 Project Operations, podeu triar de subcontractar membres de l'equip del projecte amb personal o sense personal.

- Els membres de l'equip del projecte sense personal tenen assignat un recurs genèric.
- Els membres de l'equip amb personal tenen assignat un recurs amb nom.

Quan enllaceu un membre de l'equip del projecte amb una línia de subcontracte, les assignacions a tasques que té el membre de l'equip es recompten segons la llista de preus de compra adjunta al subcontracte.  A la pestanya **Estimacions** de la pàgina **Detalls del projecte**, seleccioneu el botó **Actualitza els preus** per veure els preus actualitzats i/o el cost resultant de la decisió de subcontractar. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Subcontractació d'un membre de l'equip del projecte sense dotació
La pàgina **Detalls dels membres de l'equip** té camps de subcontracte i línia de subcontracte que permeten a un administrador de projecte expressar com vol obtenir la capacitat necessària d'un subcontracte. Per subcontractar un membre de l'equip del projecte com a recurs genèric, seguiu aquests passos:

1.  Trieu un subcontracte a la pàgina **Detalls dels membres de l'equip**.

2.  Només podeu seleccionar les subcontractes amb l'estat **Esborrany** o **Confirmat**. **Els subcontractes Tancats** o **Cancel·lats** no es poden seleccionar. 

3.  El camp **Línia de subcontracte** esdevé visible després de seleccionar un subcontracte.

4.  Al camp **Línia de subcontracte**, només podeu seleccionar línies de subcontracte que siguin per al temps. No podeu seleccionar línies de subcontracte per a despeses o material.

5.  La funció per al registre de membre de l'equip del projecte ha de coincidir amb la funció de la línia de subcontracte. D'aquesta manera, es garanteix que el temps de la funció que s'està estimant en el projecte és per a la mateixa funció que es compra a la línia de subcontracte. 

Quan un membre de l'equip genèric s'associa amb una línia de subcontracte i subcontracte, el camp **Tipus de treballador** de la fila del membre de l'equip genèric s'actualitzarà a **Treballador de contracte** i la **Validesa de subcontracte** es definirà com a **Vàlida**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Subcontractació d'un membre de l'equip del projecte amb dotació
Igual que els membres genèrics o no qualificats, la capacitat dels membres de l'equip qualificats necessaris en un projecte també es pot enllaçar a un subcontracte. Per subcontractar un membre de l'equip del projecte amb nom com a recurs genèric, seguiu aquests passos:

1.  Assegureu-vos que el recurs amb nom es configura com a tipus de treballador de contracte de recurs que es pot reservar. A més, assegureu-vos que el camp **Proveïdor** del recurs que es pot reservar coincideixi amb el proveïdor del subcontracte que esteu seleccionant. 

2.  Només podeu seleccionar subcontractes amb l'estat **Esborrany** o **Confirmat**. **Els subcontractes Tancats** o **Cancel·lats** no es poden seleccionar. 

3.  El camp **Línia de subcontracte** esdevé visible després de seleccionar un subcontracte.

4.  Al camp **Línia de subcontracte**, només podeu seleccionar línies de subcontracte que siguin per al temps. No podeu seleccionar línies de subcontracte per a despeses o material.

5.  La funció per al registre de membre de l'equip del projecte ha de coincidir amb la funció de la línia de subcontracte. D'aquesta manera, es garanteix que el temps de la funció que s'està estimant en el projecte és per a la mateixa funció que es compra a la línia de subcontracte. 

Els membres de l'equip de projecte que es configuren amb un tipus de treballador de contracte de **Recurs que es pot reservar** es mostraran amb un estat de validesa del subcontracte de **No vàlid** si no estan enllaçats amb un subcontracte. Quan un membre de l'equip del projecte amb nom s'associa amb una línia de subcontracte i subcontracte, el camp **Tipus de treballador** de la fila del membre de l'equip s'actualitzarà a **Treballador de contracte** i la **Validesa de subcontracte** es definirà com a **Vàlida**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
