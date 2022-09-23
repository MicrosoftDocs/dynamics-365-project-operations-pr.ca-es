---
title: Dotar de personal un projecte amb empleats de contracte i capacitat subcontractada
description: En aquest article s'explica com es poden personalitzar els requisits del projecte mitjançant treballadors contractats o capacitat subcontractada a Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 30e16efeed93ab4568eac57fb3ed46067a08524d
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522423"
---
# <a name="staffing-a-project-with-contract-workers-and-subcontracted-capacity"></a>Dotar de personal un projecte amb empleats de contracte i capacitat subcontractada

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

Els membres genèrics de l'equip del projecte poden ser empleats o treballadors contractats. Quan personalitzeu un projecte amb treballadors contractats, podeu limitar les vostres opcions de personal a treballadors amb contracte específics que estiguin assignats a una línia de subcontractació. 

## <a name="search-for-staff-resource-requirements-with-contract-workers-that-belong-to-a-specific-subcontract-line"></a>Cerca de necessitats de recursos de personal amb treballadors contractats que pertanyin a una línia de subcontractació específica

Per cercar i sol·licitar recursos de personal amb treballadors contractats que pertanyin a una línia de subcontractació específica, seguiu aquests passos:

1. Crear un membre genèric de l'equip de projecte que faci referència a una línia de subcontractació i subcontractació.
2. Genereu un requisit de recurs per a aquest membre genèric de l'equip del projecte mitjançant el **botó Genera requeriments** de la subquadrícula de membres de l'equip del projecte.
3. Seleccioneu la fila de membres de l'equip i, a continuació, seleccioneu el **botó Reserva** a la subquadrícula. 
4. Això obre el tauler de planificació amb el context de requisits. Juntament amb altres atributs, com ara les dates, la funció i els camps de la unitat organitzativa, els filtres del tauler de planificació també s'emplenen automàticament amb els camps de línia de proveïdor, subcontractació i subcontractació del requisit de recursos.
5. El sistema cerca recursos que compleixin els criteris de filtre i els enumera. 
6. Seleccioneu un dels recursos filtrats i reserveu el recurs per al requisit. 
7. Es crea un membre de l'equip del projecte i s'actualitza amb referències de línies de subcontractació i subcontractació. Aneu a **Estimacions** de projecte i seleccioneu **Actualitza els preus** per veure el cost actualitzat de l'assignació de recursos. 

> [!NOTE]
> L'actualització del membre de l'equip del projecte amb una referència de línia de subcontractació i subcontractació pot no ser sempre possible durant la reserva si el recurs s'assigna a diverses línies de subcontractació. Si el sistema no pot actualitzar el membre de l'equip del projecte amb una línia de subcontractació i subcontractació, obriu el registre de membres de l'equip del projecte i actualitzeu manualment aquests camps de manera que l'estimació del cost financer reflecteixi amb precisió el cost del subcontractista.

## <a name="search-for-and-staff-resource-requirements-with-any-contract-worker"></a>Cerca i requeriments de recursos del personal amb qualsevol treballador contractat

Per cercar i sol·licitar recursos del personal amb qualsevol treballador contractat, seguiu aquests passos:

1. Creeu un membre genèric de l'equip del projecte.
2. Genereu un requisit de recurs per a aquest membre genèric de l'equip del projecte mitjançant el **botó Genera requeriments** de la subquadrícula de membres de l'equip del projecte.
3. Seleccioneu la fila de membres de l'equip i, a continuació, seleccioneu el **botó Reserva** a la subquadrícula. 
4. Això obre el tauler de planificació amb el context de requisits. Juntament amb altres atributs, com ara les dates, la funció i els camps de la unitat organitzativa, els filtres del tauler de planificació també s'emplenen automàticament amb els camps de línia de proveïdor, subcontractació i subcontractació del requisit de recursos. Com que el requisit no tenia cap valor de línia de subcontractació o subcontractació emplenat, aquests atributs quedaran buits al panell de filtres.
5. El sistema cerca recursos que compleixin els criteris de filtre i els enumera.
6. Actualitzeu el **camp Tipus** de treballador de la subfinestra del filtre a **Treballador** contractat per limitar la cerca de treballadors contractats. Actualitzeu **Proveïdor** a la subfinestra de filtres per seleccionar un proveïdor que limiti la cerca per mostrar només els treballadors amb contracte que pertanyen a una empresa proveïdora específica.
7. Seleccioneu un treballador amb contracte de la llista i reserveu el recurs per al requisit.
8. Es crea un membre de l'equip del projecte. No obstant això, el membre de l'equip del projecte no està actualitzat amb cap línia de subcontractació o subcontractació i, per tant, l'assignació de recursos no es costarà amb el preu de la subcontractació. Actualitzeu manualment el membre de l'equip del projecte amb una línia de subcontractació i aneu a **Estimacions** del projecte i seleccioneu **Actualitza els preus** per veure el cost actualitzat de l'assignació de recursos.

> [!NOTE]
> Els membres de l'equip del projecte que tenen **el tipus** de treballador com a treballador **amb** contracte però no tenen cap referència de subcontractació es marquen com a **no vàlids** a la graella de membres **de l'equip** del projecte. Si hi ha algun membre de l'equip del projecte amb aquest estatus, obriu el registre de membres de l'equip del projecte i actualitzeu manualment els camps de subcontractació i subcontractació perquè l'estimació del cost financer reflecteixi amb precisió el cost del subcontractista a la **pestanya Estimacions**. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
