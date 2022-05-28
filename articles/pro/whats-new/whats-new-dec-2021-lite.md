---
title: Novetats de desembre de 2021 - Desplegament de lite d'operacions de projectes
description: Aquest tema proporciona informació sobre les actualitzacions de qualitat que estan disponibles a la versió de desembre de 2021 de la implementació lite d'operacions del projecte.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b1ff0a14bf6cb445913bcba11f83234826014857
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8585366"
---
# <a name="whats-new-december-2021---project-operations-lite-deployment"></a>Novetats de desembre de 2021 - Desplegament de lite d'operacions de projectes

_S'aplica a: implementació bàsica: tracte de facturació proforma_

Aquest tema s'aplica als components i versions següents de Microsoft Dynamics 365 Project Operations:

- Operacions del projecte en una Dataverse versió d'entorn 4.27.0.195, 4.27.0.242, 4.27.0.244


## <a name="features-included-in-this-release"></a>Característiques incloses en aquesta versió

### <a name="subcontract-management"></a>Gestió de subcontractacions 

- [Subcontractació de membres](../subcontracting/subcontracting-project-team-members.md) de l'equip del projecte: Un gestor de projectes pot crear membres d'equips nomenats o genèrics amb subcontractacions i línies de subcontractació per impactar en el personal i l'estimació.
- [Opcions de subcontractació per als membres](../subcontracting/subcon-options.md) de l'equip del projecte: quan es prenen opcions de personal per als membres de l'equip de projecte nomenats o genèrics, el gestor del projecte pot revisar les subcontractes existents o crear noves subcontractacions per a un o més membres de l'equip del projecte. 
- [Estimació de costos de les assignacions](../subcontracting/costing-subcon-ra.md) de recursos subcontractats: l'estimació de costos del projecte tindrà en compte les assignacions de recursos subcontractades i els costarà utilitzar les llistes de preus de compra associades a subcontractes. 
- [Configureu La junta de planificació per mostrar els treballadors contractats i la capacitat](../subcontracting/configure-sb-subcon.md) subcontractada: el tauler de planificació a Les operacions del projecte ara es pot configurar per cercar i suggerir el tipus de treballador contractat de recursos que es poden reservar i la capacitat subcontractada juntament amb els empleats. Aquesta configuració es pot aplicar quan es busquen recursos en el context del personal per a un requisit específic del projecte o quan es fa una cerca fora del context d'un requisit de projecte.
- [Personal d'un projecte amb treballadors contractats i capacitat](../subcontracting/staffing-cw.md) subcontractada: Els treballadors contractats ja es poden reservar en projectes aprofitant experiències de calendari.
- [Temps d'enregistrament, despeses i ús de material en projectes per a components](../subcontracting/recording-subcon-actuals.md) subcontractats: els treballadors contractats poden registrar temps i despeses, i els membres de l'equip del projecte també poden registrar l'ús de materials comprats mitjançant una subcontracta en un projecte. Això es traduirà en el registre de costos precisos en projectes que utilitzen la capacitat o els materials adquirits.
- [Transicions estatals en una subcontracta](../subcontracting/subcon-states.md): les subcontractes es poden confirmar per completar la negociació amb el proveïdor, tancades per indicar la finalització del lliurament o cancel·lades per indicar la rescissió del contracte amb el proveïdor abans de completar el lliurament.

### <a name="task-planning"></a>Planificació de tasques
- S'ha millorat la resolució de problemes per als administradors del sistema. Quan un usuari no pot obrir un projecte, l'administrador pot revisar els errors relacionats amb la llicència generats des [del Project for the web als](../../project-management/schedule-api-logs.md) registres de planificació del Projecte.
- [Utilitzeu llistes de comprovació de tasques al Microsoft Project per al web](https://support.microsoft.com/en-us/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c). Al Microsoft Project per al web, podeu afegir una llista de comprovació a una tasca per fer un seguiment d'elements específics.

## <a name="quality-updates"></a>Actualitzacions de qualitat

| **Àrea de característiques** | **Número de referència** | **Actualització de qualitat** |
| --- | --- | --- |
| Planificació i seguiment | 2392596 | Planifica les API ara permeten actualitzacions dels **camps Esforç restant**, **Esforç completat** i **% Completat**. |
| Planificació i seguiment | 2478497 | Programar els camps Programar el número **d'activitat de les API** i **l'identificador** de tasca a l'entrada perquè el sistema els emplenarà mitjançant la numeració automàtica.|
| Temps i despesa | 2468135 | El nombre de candidatures d'aprovació es redueix de cinc a tres. |
| Temps i despesa | 2468188 | S'ha corregit el problema amb el text de registre que excedeix la longitud màxima de l'atribut **notetext** de l'entitat **d'anotació**. |
