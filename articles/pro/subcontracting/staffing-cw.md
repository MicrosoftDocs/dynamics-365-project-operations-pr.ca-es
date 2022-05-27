---
title: Dotar de personal un projecte amb empleats de contracte i capacitat subcontractada
description: Aquest tema explica com es poden utilitzar els requisits del projecte mitjançant treballadors contractats o capacitat subcontractada a Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: a0efea80484dfca0a9dae8404837c3376dfecaed
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8574630"
---
# <a name="staffing-a-project-with-contract-workers-and-subcontracted-capacity"></a>Dotar de personal un projecte amb empleats de contracte i capacitat subcontractada

[!include [banner](../../includes/dataverse-preview.md)]

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_

Els membres genèrics de l'equip del projecte poden ser empleats o treballadors contractats. Quan treballes en plantilla un projecte amb treballadors contractats, pots limitar les teves opcions de personal a treballadors contractats específics que s'assignin a una línia de subcontractació. 

## <a name="search-for-staff-resource-requirements-with-contract-workers-that-belong-to-a-specific-subcontract-line"></a>Cerca de requisits de recursos de personal amb treballadors contractats que pertanyin a una línia de subcontractació específica

Per cercar i requisits de recursos de personal amb treballadors contractats que pertanyen a una línia de subcontractació específica, seguiu aquests passos:

1. Creeu un membre genèric de l'equip del projecte que fa referència a una línia de subcontractació i subcontractació.
2. Genereu un requisit de recurs per a aquest membre genèric de l'equip del projecte mitjançant el botó Genera el **requisit** de la subquadrícula dels membres de l'equip del projecte.
3. Seleccioneu la fila de membres de l'equip i, a continuació, seleccioneu el **botó Llibre** a la subquadrícula. 
4. Això obre el tauler de planificació amb el context de requisit. Juntament amb altres atributs, com ara les dates, la funció i els camps d'unitat organitzativa, els filtres del Tauler de planificació també s'emplenen automàticament amb els camps de línia de proveïdor, subcontractació i subcontractació del requisit de recurs.
5. El sistema cerca recursos que compleixin els criteris de filtre i els enumeri. 
6. Seleccioneu un dels recursos filtrats i reserveu el recurs per al requisit. 
7. Es crea i actualitza un membre de l'equip del projecte amb referències de línies de subcontractació i subcontractació. Aneu a **Estimacions** del projecte i seleccioneu **Actualitza els preus** per veure el cost actualitzat de l'assignació de recursos. 

> [!NOTE]
> És possible que l'actualització del membre de l'equip del projecte amb una referència de línia de subcontractació i subcontractació no sempre sigui possible durant la reserva si el recurs s'assigna a diverses línies de subcontractació. Si el sistema no pot actualitzar el membre de l'equip del projecte amb una línia de subcontractació i subcontractació, obriu el registre del membre de l'equip del projecte i actualitzeu manualment aquests camps perquè l'estimació del cost financer reflecteixi amb precisió el cost del subcontractista.

## <a name="search-for-and-staff-resource-requirements-with-any-contract-worker"></a>Cerca i requisits de recursos de personal amb qualsevol treballador contractat

Per cercar i obtenir requisits de recursos de personal amb qualsevol treballador contractat, seguiu aquests passos:

1. Crear un membre genèric de l'equip del projecte.
2. Genereu un requisit de recurs per a aquest membre genèric de l'equip del projecte mitjançant el botó Genera el **requisit** de la subquadrícula dels membres de l'equip del projecte.
3. Seleccioneu la fila de membres de l'equip i, a continuació, seleccioneu el **botó Llibre** a la subquadrícula. 
4. Això obre el tauler de planificació amb el context de requisit. Juntament amb altres atributs, com ara les dates, la funció i els camps d'unitat organitzativa, els filtres del Tauler de planificació també s'emplenen automàticament amb els camps de línia de proveïdor, subcontractació i subcontractació del requisit de recurs. Com que el requisit no tenia cap valor de línia de subcontractació o subcontractada emplenat, aquests atributs estaran buits a la subfinestra de filtre.
5. El sistema cerca recursos que compleixin els criteris de filtre i els enumeri.
6. Actualitzeu el **camp Tipus** De treballador de la subfinestra de filtre al **Treballador** contractat per limitar la cerca als treballadors contractats. Actualitzeu **el proveïdor** a la subfinestra de filtre per seleccionar un proveïdor per limitar la cerca a mostrar només els treballadors contractats que pertanyen a una empresa de proveïdors específica.
7. Seleccioneu un treballador contractat de la llista i reserveu el recurs per al requisit.
8. Es crea un membre de l'equip del projecte. No obstant això, el membre de l'equip del projecte no s'actualitza amb cap línia de subcontractació o subcontractació i, per tant, l'assignació de recursos no es costarà utilitzant els preus de subcontractació. Actualitzeu manualment el membre de l'equip del projecte amb una línia de subcontractació i aneu a **Estimacions** del projecte i seleccioneu **Actualitza els preus** per veure el cost actualitzat de l'assignació de recursos.

> [!NOTE]
> Els membres de l'equip del projecte que tenen **el tipus** Worker com a **treballador** del contracte però no tenen una referència de subcontracta es marca com a **No vàlids** a la quadrícula de membres **de l'equip** del projecte. Si hi ha membres de l'equip del projecte amb aquest estat, obriu el registre del membre de l'equip del projecte i actualitzeu manualment els camps de línia de subcontractació i subcontractació de manera que l'estimació de costos financers reflecteixi amb precisió el cost del subcontractista a la **pestanya Estimacions**. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
