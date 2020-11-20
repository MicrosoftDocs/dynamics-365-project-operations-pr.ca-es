---
title: Estimacions de vendes i projectes
description: En aquest tema es proporciona informació sobre com aprofitar la planificació i les estimacions del procés de venda.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: d8bb380519759659dc1b4151b62228a626ee7a26
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120666"
---
# <a name="sales-estimates-and-projects"></a>Estimacions de vendes i projectes

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Durant el procés de vendes, podeu crear estimacions de vendes mitjançant la vinculació d'un projecte a una oferta de vendes. D'aquesta manera, pot produir-se una estimació determinista durant el procés de vendes, per aprofitar les capacitats de planificació i estimació del projecte. Si la venda prospera, la planificació que s'utilitza per a propòsits d'estimació de vendes es pot utilitzar com a base per a un major refinament del pla del projecte.

## <a name="linking-a-project-to-a-quote-line"></a>Enllaçar un projecte amb una línia d'oferta

Quan creeu una línia d'oferta basada en projectes, podeu crear un projecte nou o associar-ne un d'existent a la pàgina **Línia d'oferta**. 

> ![Formulari de línia d'oferta](media/project-8.png)
 
Quan creeu un projecte nou a partir dels detalls de la línia d'oferta, podeu treure partit de les plantilles del projecte. Les plantilles de projecte són projectes model que representen plans de projecte estàndard i estimacions financeres que són típiques d'una organització. També poden representar exemplars de plans de projecte i estimacions de projectes anteriors.

> ![Detalls de la línia d'oferta](media/project-9.png)
  
Quan creeu el projecte a partir de l'oferta, el projecte s'associa automàticament a la línia d'oferta.

## <a name="components-of-estimates-in-a-project"></a>Components de les estimacions d'un projecte

Una planificació us permet dividir el treball en tasques, mantenir una jerarquia de tasques, determinar quins recursos han de completar una tasca i assignar una estimació de l'esforç necessari per completar una tasca.

Podeu definir l'esforç de treball i les estimacions de planificació mitjançant els camps de la pestanya **Planificació** de la pàgina **Projecte**. Com que una llista de preus està associada amb el projecte, les estimacions financeres es calculen mitjançant l'ús de les tarifes de costos i vendes definides a la llista de tarifes.

## <a name="importing-estimates-from-a-project-into-a-quote"></a>Importar estimacions d'un projecte a una oferta

Després de definir estimacions de projecte, podeu importar-les a la línia d'oferta. A la pàgina **Detalls de la línia d'oferta**, seleccioneu **Importa a partir d'estimacions** a la franja per resumir les estimacions de projecte pel tipus de transacció, la funció o el nivell de tasca.
