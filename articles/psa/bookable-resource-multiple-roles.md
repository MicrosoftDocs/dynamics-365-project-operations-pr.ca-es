---
title: Estimació de les vendes i els costos del projecte quan un recurs que es pot reservar duu a terme diverses funcions per a un projecte
description: En aquest tema es proporciona informaciçó sobre la manera que es pot utilitzar les dimensions de la fixació de preus i els costos d'un recurs que duu a terme diverses funcions en un projecte.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 5b2b57f5268a92168952b6da5123886df70cd4e2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013249"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-multiple-roles-for-a-project"></a>Estimació de les vendes i els costos del projecte quan un recurs que es pot reservar duu a terme diverses funcions per a un projecte 

[!include [banner](../includes/psa-now-project-operations.md)]

Sovint, les empreses basades en projectes tenen la necessitat que un recurs realitzi diverses funcions en un projecte. Cadascuna d'aquestes funcions podria tenir un preu i un cost diferent, la qual cosa significa que el mateix recurs en el projecte podria rebre una estimació econòmica diferent en funció de les tarifes de facturació i cost de cadascuna de les funcions. El Project Service Automation permet la configuració dels valors al registre de membres de l'equip per al recurs amb nom i permet diverses substitucions en cadascuna de les tasques a les quals s'assigna el membre de l'equip.

A l'exemple següent s'explica com la simple substitució d'aquest valor permet que un recurs tingui diverses funcions en un projecte que tingui diferents tarifes de cost i facturació.

## <a name="create-tasks"></a>Creació de tasques
Creeu dues tasques de projecte de 40 hores cadascuna, la tasca A i la tasca B. Seleccioneu la tasca A com a antecessora de la tasca B.

## <a name="set-up-role-and-organization-unit-for-a-generic-project-team-member"></a>Configurar la funció i unitat organitzativa per a un membre de l'equip del projecte genèric

1. A la pàgina **Planificació**, seleccioneu la fila **Tasca** per a la tasca A. 
2. Al camp **Recursos**, seleccioneu **Crea** a la llista desplegable.
3. A la pàgina **Creació ràpida del membre de l'equip**, especifiqueu els atributs del membre de l'equip genèric que pot dur a terme aquesta tasca.
4. Seleccioneu la funció i la unitat organitzativa adients i, a continuació, seleccioneu **Desa i tanca**. Es crea un membre genèric de l'equip i s'assigna a aquesta tasca. 

Repetiu aquests passos per a la tasca B i assegureu-vos que la funció i la unitat organitzativa del membre de l'equip genèric creades per a la tasca B siguin diferents de la tasca A. 

## <a name="set-up-role-and-organization-unit-for-a-project-task"></a>Configurar la funció i unitat organitzativa per a una tasca del projecte

1. Després de crear la tasca A, seleccioneu la tasca i, a continuació, seleccioneu **Edita la tasca**.
2. A la pàgina **Detalls de la tasca**, localitzeu els camps **Funció** i **Unitat organitzativa** i afegiu els valors necessaris d'un recurs que ha de dur a terme aquesta tasca. 

  > [!NOTE]
  > Si completeu aquests escenaris amb les dades de demostració del Project Service Automation, seleccioneu **Cap de consultoria** per a la funció i **Fabrikam US** com a unitat organitzativa.

3. Seleccioneu la tasca B i, a continuació, **Edita la tasca**.
4. A la pàgina **Detalls de la tasca**, localitzeu els camps **Funció** i **Unitat organitzativa** i afegiu els valors necessaris d'un recurs que ha de dur a terme aquesta tasca. Assegureu-vos que els valors dels camps **Funció** i **Unitat organitzativa** siguin diferents per a la tasca B dels valors de la tasca A. 

  > [!NOTE]
  > Si completeu aquests escenaris amb les dades de demostració del Project Service Automation, seleccioneu **Tècnic de xarxa** per a la funció i **Fabrikam US** com a unitat organitzativa.

5. Deseu i tanqueu la pàgina **Detalls de la tasca**. 

## <a name="team-member-and-estimates-behavior"></a>Comportament dels membres de l'equip i de les estimacions 

1. A la pàgina **Detalls de la tasca**, a **Membre de l'equip**, seleccioneu els dos membres de l'equip genèrics i, a continuació, seleccioneu **Genera els requisits**. 
2. Seleccioneu la fila de membre de l'equip per al **Cap de consultoria** i, a continuació, seleccioneu **Reserva**. El tauler de planificació s'obre i reserva un recurs al requisit.
3. Seleccioneu la fila de membre de l'equip per al **Tècnic de xarxa** i, a continuació, seleccioneu **Reserva**. El tauler de planificació s'obre i reserva el mateix recurs al requisit.

### <a name="team-member-grid"></a>Quadrícula de membre de l'equip 
A la quadrícula **Membre de l'equip**, fixeu-vos que els dos registres de membres de l'equip genèrics s'han suprimit i s'han substituït per un recurs. Hi ha un conjunt de valors per a aquest recurs que mostra un conjunt de valors per defecte per a **Funció** i **Unitat organitzativa**.
Quan expandiu la fila d'aquest registre de membre de l'equip, podeu veure assignacions diferents al registre de membre de l'equip per a les dues tasques. Cada fila d'assignació té valors específics de la tasca per a **Funció** i **Unitat organitzativa**. 

### <a name="estimates-grid"></a>Quadrícula d’estimacions 
Quan navegueu a la quadrícula **Estimacions**, us adonareu que ambdues assignacions del mateix recurs tenen un preu diferent.
L'assignació del recurs a la tasca A rep el preu en funció del valor de l'atribut **Funció** de **Cap de consultoria**. L'assignació del mateix recurs a la tasca B rep el preu en funció del valor de l'atribut **Funció** de **Tècnic de xarxa**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]