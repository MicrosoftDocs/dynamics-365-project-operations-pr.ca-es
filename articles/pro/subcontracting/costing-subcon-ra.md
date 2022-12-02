---
title: Càlcul de costos d'assignacions de recursos subcontractats
description: En aquest article s'explica com calcula el Microsoft Dynamics 365 Project Operations l'estimació de cost de les assignacions de recursos subcontractades.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 9fded1baa63d2defc134994c858dfc6c09f75082
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522642"
---
# <a name="cost-estimation-of-subcontracted-resource-assignments"></a>Càlcul de costos d'assignacions de recursos subcontractats

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

Les assignacions de tasques dels membres de l'equip del projecte subcontractats es comptabilitzen amb la llista de preus de **Compra** adjuntada al subcontracte del registre de membre de l'equip relacionat. Això és diferent de com es comptabilitzen les assignacions de recursos dels empleats quan les assignacions de tasques dels recursos d'empleats es compten amb la llista de preus **Cost** adjuntada a la unitat de contracte del projecte. 

Per als membres de l'equip del projecte genèric que són subcontractats, les assignacions es comptabilitzen amb una llista de preus basada en les funcions a la llista de preus de compra adjunta al subcontracte. Els preus de compra també es poden configurar específicament per a cada recurs. Aquests preus específics de recursos tindran prioritat quan comptabilitzeu les assignacions de tasques de noms de membres de l'equip del projecte anomenats que són empleats de contracte. 

La prioritat de l'ús d'un preu de compra d'una funció específica o d'un recurs específic es deriva de la configuració de la prioritat de la dimensió de preus a **Paràmetres > Dimensions de preus basades en l'import**.

Aquesta funcionalitat de preus calculats dinàmicament a partir de la configuració de la dimensió per als preus de compra dels subcontractistes és semblant a la manera com s'obtenen els percentatges de cost i facturació per als empleats a temps complet. 

## <a name="creating-task-assignments-for-getting-cost-estimates-of-subcontractor-resources"></a>Crear assignacions de tasques per obtenir estimacions de cost dels recursos de subcontractista

Les assignacions de tasques per a subcontractistes es poden crear de dues maneres: 
- Amb la pestanya **Tasques**.
- Amb la pestanya **Equip**.

### <a name="creating-resources-assignments-using-the-tasks-tab"></a>Crear assignacions de recursos mitjançant la pestanya Tasques
Mitjançant la llista **Recursos** de la pestanya **Tasques** per a una tasca específica, podeu crear una assignació de tasques per a un recurs amb nom o un recurs genèric. Si seleccioneu un recurs amb nom al desplegable **Recursos assignats** de la tasca i aquest recurs és un treballador de contracte, el recurs amb nom s'assigna a la tasca i es crea un registre de membre de l'equip de projecte corresponent amb el tipus de treballador definit com a **Treballador de contracte** i **Validesa** es defineix com a **No vàlid**. En el pas següent, haureu d'obrir el registre de membre de l'equip del projecte i seleccionar una línia de subcontracte i subcontracte. S'actualitzarà l'assignació de la tasca per fer referència a la línia de subcontracte i el subcontracte i també s'actualitzarà l'estat del membre de l'equip a **Vàlid**.

Si trieu de crear un membre de l'equip genèric al quadre desplegable **Recursos assignats** de la tasca, el quadre de diàleg **Creació de membres de l'equip genèric** us permetrà seleccionar una línia de subcontracte i subcontracte. Quan el recurs genèric s'assigna a la tasca i es crea el registre de membre de l'equip de projecte corresponent, veureu que el registre de membre de l'equip del projecte es crea amb el tipus de treballador de contracte definit com a **Treballador de contracte** i **Validesa** definit com a **Vàlid**.

### <a name="creating-project-team-members-using-the-team-tab"></a>Creació de membres de l'equip de projecte amb la pestanya Equip
Amb la pestanya Equip del projecte, podeu crear un membre d'equip genèric o amb nom. Quan creeu el membre de l'equip, podeu seleccionar la línia de subcontracte i el subcontracte. Un cop creat el membre de l'equip, haureu d'assignar el membre de l'equip a una tasca amb el desplegable **Recursos assignats** de la tasca. 

## <a name="updating-estimates"></a>Actualització d'estimacions
Un cop assignats els membres de l'equip del projecte a les tasques, haureu de navegar a la pestanya **Estimacions** al projecte i seleccionar **Actualitza els preus** per assegurar-vos que els percentatges de cost de les assignacions de recursos del subcontractista s'actualitzin segons la llista de preus de compra adjuntada al subcontracte. Les estimacions no es generen per a les tasques no assignades al Microsoft Dynamics 365 Project Operations. Per aquest motiu, haureu de crear assignacions de tasques per calcular al preu i el cost de diverses tasques del projecte. 

> [NOTA!] Els membres de l'equip de projecte que tenen el **Tipus de treballador** definit com a **Treballador de contracte** però no tenen una referència de subcontracte es marquen com a **No vàlid** a la quadrícula **Membres de l'equip del projecte**. Si hi ha algun membre de l'equip de projecte amb aquest estatus, obriu el registre de membre de l'equip del projecte i actualitzeu manualment els camps de subcontracte i línia de subcontracte per tal que l'estimació del cost financer reflecteixi amb precisió el cost del subcontractista a la pestanya **Estimacions**. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
