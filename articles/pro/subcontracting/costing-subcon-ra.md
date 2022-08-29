---
title: Càlcul de costos d'assignacions de recursos subcontractats
description: En aquest article s'explica com Microsoft Dynamics 365 Project Operations calcula l'estimació de costos de les assignacions de recursos subcontractades.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 5a4d0707f8373b5083272eacb7dc1318e82a23ac
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 08/11/2022
ms.locfileid: "9262047"
---
# <a name="cost-estimation-of-subcontracted-resource-assignments"></a>Càlcul de costos d'assignacions de recursos subcontractats

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_

Les assignacions de tasques dels membres de l'equip de projecte subcontractats es costen mitjançant la llista de **preus de compra** adjunta a la subcontractació al registre de membres de l'equip relacionat. Això és diferent de com es costen les assignacions de recursos dels empleats on es costen les assignacions de tasques dels recursos dels empleats mitjançant la **llista de preus de cost** que s'adjunta a la unitat de contractació del projecte. 

Per als membres genèrics de l'equip del projecte que estan subcontractats, les assignacions tenen un cost mitjançant una configuració de preus basada en rols a la llista de preus de compra adjunta a la subcontractació. Els preus de compra també es poden establir específicament per a cada recurs. Aquests preus específics de recursos tindran prioritat quan les assignacions de tasques dels membres de l'equip del projecte nomenats siguin treballadors contractats. 

La prioritat d'utilitzar el preu de compra específic de cada funció en comparació amb el específic del recurs està impulsada per la configuració de la prioritat de la dimensió de preus a Paràmetres > dimensions de preus basats en **l'import**.

Aquesta funcionalitat de conducció dinàmica de preus basada en la configuració de dimensions per als preus de compra dels subcontractistes és similar a com es deriven les tarifes de costos i factures per als empleats a temps complet. 

## <a name="creating-task-assignments-for-getting-cost-estimates-of-subcontractor-resources"></a>Creació d'assignacions de tasques per obtenir estimacions de costos dels recursos del subcontractista

Les assignacions de tasques per a subcontractistes es poden crear de dues maneres: 
- Ús de la **pestanya Tasques**.
- Ús de la **pestanya Equip**.

### <a name="creating-resources-assignments-using-the-tasks-tab"></a>Creació d'assignacions de recursos mitjançant la pestanya Tasques
Mitjançant la **llista Recursos** de la **pestanya Tasques** per a una tasca específica, podeu crear una tasca per a un recurs amb nom o un recurs genèric. Si seleccioneu un recurs amb nom del menú desplegable Recursos assignats a la tasca i aquest recurs és un treballador amb contracte, el recurs anomenat s'assigna a la tasca i es crea un registre de membre de l'equip del projecte corresponent amb el **tipus de treballador definit com a** Treballador del **contracte i** Validesa **definit com a** No vàlid **.** Com a pas següent, haureu d'obrir el registre de membres de l'equip del projecte i seleccionar una línia de subcontractació i subcontractació. D'aquesta manera s'actualitzarà l'assignació de tasques per tenir una referència a la línia de subcontractació i subcontractació i també s'actualitzarà l'estatus de membre de l'equip a **Vàlid**.

Si decidiu crear un membre de l'equip genèric des del **desplegable Recursos assignats** a la tasca, el diàleg de creació **de membres de l'equip** genèric us permetrà seleccionar una línia de subcontractació i subcontractació. Quan s'assigna el recurs genèric a la tasca i es crea el registre de membre de l'equip del projecte corresponent, notareu que el registre de membre de l'equip del projecte es crea amb el tipus de treballador definit com a **Treballador del** contracte i **Validesa** definit com a **Vàlid**.

### <a name="creating-project-team-members-using-the-team-tab"></a>Creació de membres de l'equip del projecte mitjançant la pestanya Equip
Mitjançant la pestanya Equip del projecte, podeu crear un genèric o un membre de l'equip amb nom. En crear el membre de l'equip, podeu seleccionar la línia de subcontractació i subcontractació. Un cop creat el membre de l'equip, haureu d'assignar el membre de l'equip a una tasca mitjançant el **menú desplegable Recursos assignats** de la tasca. 

## <a name="updating-estimates"></a>Actualització de pressupostos
Després d'assignar membres de l'equip de projecte a tasques, haureu de navegar a la **pestanya Estimacions** del projecte i seleccionar **Actualitza els preus** per assegurar-vos que les taxes de cost de les assignacions de recursos del subcontractista s'actualitzin en funció de la llista de preus de compra adjunta al subcontractista. No es generen estimacions per a tasques no assignades a Microsoft Dynamics 365 Project Operations. Com a resultat, haureu de crear assignacions de tasques per valorar i costar diverses tasques al vostre projecte. 

> [NOTA!] Els membres de l'equip del projecte que tenen **el tipus** de treballador com a treballador **amb** contracte però no tenen cap referència de subcontractació es marquen com a **no vàlids** a la graella de membres **de l'equip** del projecte. Si hi ha algun membre de l'equip del projecte amb aquest estatus, obriu el registre de membres de l'equip del projecte i actualitzeu manualment els camps de subcontractació i subcontractació perquè l'estimació del cost financer reflecteixi amb precisió el cost del subcontractista a la **pestanya Estimacions**. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
