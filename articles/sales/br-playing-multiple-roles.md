---
title: Estimació de les vendes i els costos del projecte quan un recurs que es pot reservar duu a terme diverses funcions en un projecte
description: En aquest article s'explica com s'utilitzen les dimensions dels preus per donar suport als preus i a les estimacions de costos d'un recurs que omple diverses funcions d'un projecte.
author: rumant
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 9bb59537aaa75d9003925bec37642a2fa7c9ca22
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923452"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-multiple-roles-on-a-project"></a>Estimació de les vendes i els costos del projecte quan un recurs que es pot reservar duu a terme diverses funcions en un projecte 

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense existències, implementació bàsica: tracte de facturació proforma i Project Operations per a escenaris amb existències/basats en producció_ 

Sovint, les empreses basades en projectes tenen la necessitat que un recurs dugui a terme diverses funcions en un projecte. Cada funció pot tenir un preu i un cost diferent. Això vol dir que el mateix temps d'un recurs en un projecte podria tenir una estimació financera diferent en funció de les tarifes de facturació i de costos de cada funció. Podeu configurar els valors del registre de membres de l'equip per al recurs amb nom amb diferents substitucions per a cadascuna de les tasques a les quals està assignat el membre de l'equip.

L'exemple següent us guiarà per la manera com la simple substitució d'un valor permet que un recurs tingui diverses funcions en un projecte que tingui diferents tarifes de costos i de facturació.

## <a name="create-tasks"></a>Creació de tasques
Per crear tasques, heu d'afegir tasques, així com tasques de resum, després del qual haureu d'assignar la tasca abans d'afegir-hi la durada de la tasca. 

### <a name="add-tasks-and-summary-tasks"></a>Afegir tasques i tasques de resum
Per afegir una tasca, feu els passos següents:

1. Aneu a **Projectes** i obriu el projecte al qual voleu afegir tasques.
2. Seleccioneu **Afegeix una tasca nova**. Anomeneu la tasca i, a continuació, premeu **Retorn**.
3. Introduïu un altre nom de tasca i premeu **Retorn**. Repetiu-ho fins que tingueu una llista completa de tasques.
3. Per aplicar sagnia a les tasques de **Tasques de resum**, seleccioneu els tres punts verticals al costat del nom de la tasca i, a continuació, seleccioneu **Crea una subtasca**. 

  > [!TIP]
  > Per seleccionar més d'una tasca, seleccioneu una tasca, manteniu premuda la tecla **Ctrl** i, a continuació, seleccioneu una altra tasca.
  >
  > També podeu triar **Promou la subtasca** per desplaçar les tasques de sota les **Tasques de resum**.

### <a name="assign-tasks"></a>Assignar tasques

Feu els passos següents per assignar tasques.

1. A la columna **Assignada a** d'una tasca, seleccioneu la icona de persona.
2. Trieu un membre de l'equip de la llista o introduïu text per cercar un nom.

### <a name="add-task-duration-and-columns"></a>Afegir la durada i les columnes de la tasca

Sovint és més fàcil començar a construir el vostre projecte amb la durada. Feu els passos següents per afegir la durada d'una tasca.

1. A la columna **Durada** d'una tasca, escriviu el nombre de dies que penseu que trigarà a dur-se a terme la tasca. Si voleu utilitzar una altra unitat de temps, introduïu un nombre i la paraula **hores**, **setmanes** o **mesos**.
2. Si voleu que la tasca aparegui com una fita en forma de diamant a la visualització de la **Cronologia**, a la columna **Durada** introduïu **0 dies**.
3. Premeu **Retorn** per anar al camp **Durada** de la tasca següent i continuar introduint durades.

  > [!NOTE]
  > No podeu introduir una durada per a les tasques de resum.

Podeu afegir columnes al projecte per tal de proporcionar més detalls. Per fer-ho, seleccioneu **Afegeix una columna**. 

Per obtenir més informació, consulteu [Crear un projecte](https://support.microsoft.com/en-us/office/create-a-project-a5b5e823-fb2e-45fd-be00-7d84422d9749).

## <a name="set-up-the-role-and-organization-unit-for-a-generic-project-team-member"></a>Configurar la funció i la unitat d'organització per a un membre genèric de l'equip de projecte
Dueu a terme els passos següents per configurar una funció i una unitat d'organització per a un membre genèric de l'equip.

1. A la pàgina **Tasques**, seleccioneu la fila **Tasca** per a la **Tasca A**. 
2. A **Assignat a**, seleccioneu **Afegeix recurs genèric**. S'obre la pàgina **Creació ràpida d'un membre de l'equip**.
3. A la pàgina **Creació ràpida del membre de l'equip**, especifiqueu els atributs del membre de l'equip genèric que pot dur a terme aquesta tasca.
4. Seleccioneu la funció i la unitat organitzativa adients i, a continuació, seleccioneu **Desa i tanca**. Es crea un membre genèric de l'equip i s'assigna a aquesta tasca. 
5. Repetiu els passos 1 a 4 per a la **Tasca B**. No obstant, la **Tasca B** ha de tenir assignada una funció i una unitat d'organització diferent per al membre de l'equip genèric que la **Tasca A**. 

## <a name="set-up-the-role-and-organization-unit-for-a-project-task"></a>Configurar la funció i la unitat d'organització per a una tasca del projecte
Dueu a terme els passos següents per configurar una funció i una unitat d'organització per a una tasca.

1. Després de crear la **Tasca A**, seleccioneu la tasca i, a continuació, seleccioneu la icona **i** per obrir la subfinestra de **Detalls de la tasca**. 
2. A la subfinestra de **Detalls de la tasca**, desplaceu-vos fins a la part inferior i seleccioneu **Visualitza els detalls** per obrir la pàgina **Detalls de la tasca**.
3. A la pàgina **Detalls de la tasca**, a **Funció** i **Unitat d'organització**, afegiu els valors necessaris per dur a terme aquesta tasca per al recurs. 

  > [!NOTE]
  > Si completeu aquest escenari mitjançant les dades de demostració de Project Operations, seleccioneu **Cap de consultoria** per a la funció i **Fabrikam US** com a unitat d'organització.

4. Seleccioneu **Tasca B** i, a continuació, seleccioneu la tasca.
5. Seleccioneu la icona **i** per obrir la subfinestra de **Detalls de la tasca**. 
6. A la subfinestra de **Detalls de la tasca**, desplaceu-vos fins a la part inferior i seleccioneu **Visualitza els detalls** per obrir la pàgina **Detalls de la tasca**.
7. A la pàgina **Detalls de la tasca**, a **Funció** i **Unitat d'organització**, afegiu els valors necessaris d'un recurs que dugui a terme aquesta tasca. Els valors de **Funció** i **Unitat d'organització** per a la **Tasca B** han de ser diferents que els de la **Tasca A**. 

  > [!NOTE]
  > Si completeu aquest escenari mitjançant les dades de demostració de Project Operations, seleccioneu **Tècnic de xarxes** per a la funció i **Fabrikam US** com a unitat d'organització.

8. Deseu i tanqueu la pàgina **Detalls de la tasca**. 

## <a name="team-member-and-estimates-behavior"></a>Comportament dels membres de l'equip i de les estimacions 
Per entendre el comportament de la quadrícula de **Membre de l'equip** i les estimacions, seguiu els passos següents.

1. A la quadrícula **Membres de l'equip**, seleccioneu els dos membres de l'equip genèric i, a continuació, seleccioneu **Genera requisits**. Això generarà els requisits de recursos. 
2. Seleccioneu la fila de membre de l'equip per al **Cap de consultoria** i, a continuació, seleccioneu **Reserva**. S'obre el tauler de planificació amb una llista de recursos. Seleccioneu un recurs i, a continuació, seleccioneu **Reserva** per reservar el recurs per a aquest requisit.
3. Seleccioneu la fila de membre de l'equip per a **Tècnic de xarxes** i, a continuació, seleccioneu **Reserva**. S'obre el tauler de planificació amb una llista de recursos. Seleccioneu el mateix recurs que a dalt i, a continuació, seleccioneu **Reserva** per reservar el recurs per a aquest requisit.

### <a name="team-member-grid"></a>Quadrícula de membre de l'equip 

A la quadrícula **Membres de l'equip**, se suprimeixen els dos registres dels membres de l'equip genèric i se substitueixen per un sol recurs. Hi ha un conjunt de valors per a aquest recurs, que són un conjunt de valors per defecte per a la **Funció** i la **Unitat organitzativa**.

Quan amplieu la fila d'aquest registre de membres de l'equip, podeu veure les assignacions diferents al registre de membres de l'equip per a ambdues tasques. Cada fila d'assignació té valors específics de la tasca per a **Funció** i **Unitat organitzativa**. 

### <a name="estimates-grid"></a>Quadrícula d’estimacions 

A la quadrícula **Estimacions**, les dues assignacions del mateix recurs tenen un preu diferent. L'assignació del recurs a la **Tasca A** rep el preu en funció del valor de l'atribut **Funció** de **Cap de consultoria**. L'assignació del mateix recurs a la **Tasca B** rep el preu en funció del valor de l'atribut **Funció** de **Tècnic de xarxes**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]