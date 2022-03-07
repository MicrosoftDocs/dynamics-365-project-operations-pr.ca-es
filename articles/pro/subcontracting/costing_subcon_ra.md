---
title: Estimació de costos de les assignacions de recursos subcontractats
description: Aquest tema explica algunes de les accions que Microsoft Dynamics 365 Project Operations calcula l'estimació de costos de les assignacions de recursos subcontractats.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: 5a94840a3735639532683153105fea85bea99c9d
ms.sourcegitcommit: 45893132bd8bfaf944ee0ac855484684dd1ee945
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 12/09/2021
ms.locfileid: "7902995"
---
# <a name="cost-estimation-of-subcontracted-resource-assignments"></a>Estimació de costos de les assignacions de recursos subcontractats

[!include [banner](../../includes/dataverse-preview.md)]

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_

Les tasques dels membres de l'equip del projecte subcontractats tenen un cost mitjançant la **llista de preus de compra** adjunta a la subcontractació al registre de membres de l'equip relacionat. Això és diferent de com es costen les assignacions de recursos dels empleats quan les tasques de recursos dels empleats es costen mitjançant la **llista de preus de cost que** s'adjunta a la unitat de contractació del projecte. 

Per als membres genèrics de l'equip del projecte que són subcontractats, les tasques es costen mitjançant una configuració de preus basada en funcions a la llista de preus de compra adjunta a la subcontractació. Els preus de compra també es poden configurar específicament per a cada recurs. Aquests preus específics dels recursos tindran prioritat quan les tasques de costos de tasques dels membres de l'equip del projecte amb nom siguin treballadors contractats. 

La prioritat d'utilitzar el preu de compra específic del rol en comparació amb el específic dels recursos està impulsada per la configuració de la prioritat de dimensió de preus a **Paràmetres > dimensions de preus basats en l'import**.

Aquesta funcionalitat de conduir dinàmicament els preus en funció de la configuració de la dimensió per als preus de compra dels subcontractistes és similar a com es deriven les taxes de cost i factura per als empleats a temps complet. 

## <a name="creating-task-assignments-for-getting-cost-estimates-of-subcontractor-resources"></a>Creació d'assignacions de tasques per obtenir estimacions de costos dels recursos dels subcontractistes

Les tasques per a subcontractistes es poden crear de dues maneres: 
- Ús de la **pestanya** Tasques.
- Ús de la **pestanya** Equip.

### <a name="creating-resources-assignments-using-the-tasks-tab"></a>Creació d'assignacions de recursos mitjançant la pestanya Tasques
Mitjançant la **llista Recursos de la** **pestanya Tasques** per a una tasca específica, podeu crear una assignació de tasques per a un recurs amb nom o un recurs genèric. Si seleccioneu un recurs amb nom del **menú desplegable Recursos assignats de la tasca** i aquest recurs és un treballador contractat, el recurs amb nom s'assigna a la tasca i es crea un registre de membre de l'equip del projecte corresponent amb el tipus de treballador definit com a **Treballador contractat i** **Validesa definida com a** **Valoració no vàlida**. Com a pas següent, haureu d'obrir el registre del membre de l'equip del projecte i seleccionar una línia de subcontractació i subcontractació. Això actualitzarà l'assignació de tasques per tenir una referència a la línia de subcontractació i subcontractació i també actualitzarà l'estat del membre de l'equip a **Vàlid**.

Si decidiu crear un membre genèric de l'equip des del **menú desplegable Recursos assignats de la** tasca, el diàleg de creació de membres **genèrics de l'equip** us permetrà seleccionar una línia de subcontractació i subcontractació. Quan el recurs genèric s'assigna a la tasca i es crea el registre de membre de l'equip del projecte corresponent, notareu que el registre del membre de l'equip del projecte es crea amb el tipus de treballador definit com a **Treballador contractat** i **Validesa definit com a Vàlid** **·**.

### <a name="creating-project-team-members-using-the-team-tab"></a>Creació de membres de l'equip del projecte mitjançant la pestanya Equip
Mitjançant la pestanya Equip del projecte, podeu crear un membre genèric o un membre de l'equip amb nom. En crear el membre de l'equip, teniu l'opció de seleccionar la línia de subcontractació i subcontractació. Després de crear el membre de l'equip, haureu d'assignar el membre de l'equip a una tasca mitjançant el **menú desplegable Recursos assignats de la** tasca. 

## <a name="updating-estimates"></a>S'estan actualitzant les estimacions
Després d'haver assignat els membres de l'equip del projecte a les tasques, haureu de navegar a la **pestanya Estimacions** del projecte i seleccionar Actualitza els preus per **assegurar**-vos que les taxes de cost de les assignacions de recursos de subcontractistes s'actualitzin en funció de la llista de preus de compra adjunta a la subcontracta. Tingueu en compte que les estimacions no es generen per a tasques no assignades a Microsoft Dynamics 365 Project Operations. Com a resultat, haureu de crear assignacions de tasques al preu i costeu diverses tasques del vostre projecte. 

> [NOTA!] Els membres de l'equip del projecte que tenen **el tipus Worker com a treballador del contracte però no tenen una referència de** **subcontracta** es marca com a No **vàlids** a la **quadrícula de membres de l'equip del** projecte. Si hi ha membres de l'equip del projecte amb aquest estat, obriu el registre del membre de l'equip del projecte i actualitzeu manualment els camps de línia de subcontractació i subcontractació de manera que l'estimació de costos financers reflecteixi amb precisió el cost del subcontractista a la **pestanya** Estimacions. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
