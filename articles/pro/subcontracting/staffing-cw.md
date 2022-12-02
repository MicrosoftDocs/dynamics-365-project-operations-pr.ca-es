---
title: Dotar de personal un projecte amb empleats de contracte i capacitat subcontractada
description: En aquest article s'explica com es poden dotar de personal els requisits del projecte mitjançant empleats de contracte o capacitat subcontractada al Microsoft Dynamics 365 Project Operations.
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

Els membres genèrics de l'equip del projecte es poden assignar amb empleats o empleats de contracte. Quan assigneu empleats de contracte a un projecte, podeu limitar les opcions de dotació de personal a empleats de contracte específics assignats a una línia de subcontracte. 

## <a name="search-for-staff-resource-requirements-with-contract-workers-that-belong-to-a-specific-subcontract-line"></a>Cercar requisits de recursos de personal amb empleats de contracte que pertanyen a una línia de subcontracte específica

Per cercar i dotar els recursos de personal amb empleats de contracte que pertanyen a una línia de subcontracte específica, seguiu aquests passos:

1. Creeu un membre de l'equip de projecte genèric que faci referència a un subcontracte o línia de subcontracte.
2. Genereu un requisit de recursos per a aquest membre de l'equip de projecte genèric utilitzant el botó **Genera un requisit** a la subquadrícula de membres de l'equip del projecte.
3. Seleccioneu la fila de membre de l'equip i, a continuació, seleccioneu el botó **Llibre** de la subquadrícula. 
4. S'obre el Tauler de planificació amb el context del requisit. Juntament amb altres atributs, com ara els camps de data, funció i unitat d'organització, els filtres del Tauler de planificació també s'emplenaran automàticament amb els camps de proveïdor, subcontracte i línia de subcontracte del requisit de recursos.
5. El sistema cerca recursos que compleixin els criteris de filtre i els mostra. 
6. Seleccioneu un dels recursos filtrats i reserveu el recurs per al requisit. 
7. Es crea un membre de l'equip de projecte i s'actualitza amb referències de subcontracte o línia de subcontracte. Aneu a **Estimacions del projecte** i seleccioneu **Actualitza els preus** per veure el cost actualitzat de l'assignació de recursos. 

> [!NOTE]
> L'actualització del membre de l'equip del projecte amb una referència de subcontracte i línia de subcontracte pot ser que no sempre sigui possible durant la reserva si el recurs està assignat a diverses línies de subcontracte. Si el sistema no pot actualitzar el membre de l'equip de projecte amb un subcontracte o línia de subcontracte, obriu el registre de membre de l'equip del projecte i actualitzeu manualment aquests camps per tal que l'estimació del cost financer reflecteixi amb precisió el cost del subcontractista.

## <a name="search-for-and-staff-resource-requirements-with-any-contract-worker"></a>Cercar i dotar de personal els requisits de recursos amb qualsevol treballador de contracte

Per cercar i dotar de personal els requisits de recursos amb qualsevol treballador de contracte, seguiu aquests passos:

1. Creeu un membre de l'equip de projecte genèric.
2. Genereu un requisit de recursos per a aquest membre de l'equip de projecte genèric utilitzant el botó **Genera un requisit** a la subquadrícula de membres de l'equip del projecte.
3. Seleccioneu la fila de membre de l'equip i, a continuació, seleccioneu el botó **Llibre** de la subquadrícula. 
4. S'obre el Tauler de planificació amb el context del requisit. Juntament amb altres atributs, com ara els camps de data, funció i unitat d'organització, els filtres del Tauler de planificació també s'emplenaran automàticament amb els camps de proveïdor, subcontracte i línia de subcontracte del requisit de recursos. Com que el requisit no tenia cap valor de subcontracte o línia de subcontracte emplenat, aquests atributs estaran buits a la subfinestra de filtres.
5. El sistema cerca recursos que compleixin els criteris de filtre i els mostra.
6. Actualitzeu el camp **Tipus de treballador** de la subfinestra de filtres a **Treballador de contracte** per limitar la cerca als empleats de contracte. Actualitzeu el **Proveïdor** a la subfinestra de filtre per seleccionar un proveïdor i limiteu la cerca per mostrar només els empleats de contracte que pertanyen a una empresa proveïdora específica.
7. Seleccioneu un treballador de contracte a la llista i reserveu el recurs per al requisit.
8. Es crea un membre de l'equip de projecte. Tanmateix, el membre de l'equip del projecte no s'actualitza amb cap subcontracte o línia de subcontracte i, per tant, l'assignació de recursos no es comptabilitzarà amb els preus del subcontracte. Actualitzeu manualment el membre de l'equip del projecte amb una línia de subcontracte i aneu a **Estimacions del projecte** i seleccioneu **Actualitza els preus** per veure el cost actualitzat de l'assignació de recursos.

> [!NOTE]
> Els membres de l'equip de projecte que tenen el **Tipus de treballador** definit com a **Treballador de contracte** però no tenen una referència de subcontracte es marquen com a **No vàlid** a la quadrícula **Membres de l'equip del projecte**. Si hi ha algun membre de l'equip de projecte amb aquest estatus, obriu el registre de membre de l'equip del projecte i actualitzeu manualment els camps de subcontracte i línia de subcontracte per tal que l'estimació del cost financer reflecteixi amb precisió el cost del subcontractista a la pestanya **Estimacions**. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
