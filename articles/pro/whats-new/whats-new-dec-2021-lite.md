---
title: 'Novetats de desembre de 2021: implementació bàsica del Project Operations'
description: Aquest article proporciona informació sobre les actualitzacions de qualitat que hi ha disponibles a la implementació bàsica de la versió de desembre de 2021 del Project Operations.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 301acc5be76fb0318d6298820b62ae5bb05efac3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914068"
---
# <a name="whats-new-december-2021---project-operations-lite-deployment"></a>Novetats de desembre de 2021: implementació bàsica del Project Operations

_S'aplica a: implementació bàsica: tracte de facturació proforma_

Aquest article s'aplica als components i les versions següents del Microsoft Dynamics 365 Project Operations:

- Project Operations en un entorn del Dataverse, versió 4.27.0.195, 4.27.0.242, 4.27.0.244


## <a name="features-included-in-this-release"></a>Característiques incloses en aquesta versió

### <a name="subcontract-management"></a>Administració de subcontractes 

- [Membres de l'equip del projecte de subcontractació](../subcontracting/subcontracting-project-team-members.md): un administrador de projecte pot crear membres de l'equip amb nom o genèrics amb subcontractes i línies de subcontracte per tenir un impacte en el personal i l'estimació.
- [Opcions de subcontractació per als membres de l'equip del projecte](../subcontracting/subcon-options.md): quan es prenen decisions de personal per als membres de l'equip del projecte amb nom o genèrics, l'administrador del projecte pot revisar els subcontractes existents o crear subcontractes nous per a un o més membres de l'equip del projecte. 
- [Càlcul de costos d'assignacions de recursos subcontractats](../subcontracting/costing-subcon-ra.md): l'estimació de cost del projecte tindrà en compte les assignacions de recursos subcontractats i els comptabilitzarà utilitzant les llistes de preus de compra associades amb subcontractes. 
- [Configurar el Tauler de planificació per mostrar els empleats de contracte i la capacitat subcontractada](../subcontracting/configure-sb-subcon.md): el Tauler de planificació al Project Operations ara es pot configurar per cercar i suggerir el tipus de treballador de contracte de recursos que es poden reservar i la capacitat subcontractada juntament amb els empleats. Aquesta configuració es pot aplicar quan se cerquin recursos dins del context de personal per a un requisit de projecte específic o quan se cerca fora del context d'un requisit de projecte.
- [Personal per a un projecte a partir d'empleats de contracte i capacitat subcontractada](../subcontracting/staffing-cw.md): ara, els empleats de contracte es poden reservar en projectes que ofereixen experiències amb el tauler de planificació.
- [Registrar temps, despeses i ús de materials als projectes per a components subcontractats](../subcontracting/recording-subcon-actuals.md): els empleats de contracte poden registrar temps i despeses, i els membres de l'equip del projecte també poden registrar l'ús de materials comprats mitjançant un subcontracte en un projecte. Això farà que es registren costos exactes en els projectes que utilitzen capacitat o materials adquirits.
- [Transicions d'estat en un subcontracte](../subcontracting/subcon-states.md): els subcontractes es poden confirmar per completar la negociació amb el proveïdor, tancar per indicar la finalització del lliurament o cancel·lar per indicar la finalització del contracte amb el proveïdor abans de completar el lliurament.

### <a name="task-planning"></a>Planificació de tasques
- Millora de la resolució de problemes per a administradors del sistema. Quan un usuari no pot obrir un projecte, l'administrador pot revisar els errors relacionats amb la manca de llicència que es generen des de Project for the Web als [Registres de planificació del projecte](../../project-management/schedule-api-logs.md).
- [Utilitzar les llistes de verificació de tasques al Microsoft Project for the Web](https://support.microsoft.com/en-us/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c). Al Microsoft Project for the Web, podeu afegir una llista de verificació a una tasca per fer el seguiment d'elements específics.

## <a name="quality-updates"></a>Actualitzacions de qualitat

| **Àrea de característiques** | **Número de referència** | **Actualització de qualitat** |
| --- | --- | --- |
| Planificació i seguiment | 2392596 | Ara, les API de planificació permeten actualitzacions dels camps **Esforç restant**, **Esforç completat** i **% completat**. |
| Planificació i seguiment | 2478497 | Els camps **Número d'activitat** i **ID de tasca** de les API de planificació poden estar buits en fer l'entrada perquè el sistema els emplenarà amb la numeració automatitzada.|
| Temps i despesa | 2468135 | El nombre de reintents d'aprovació es redueix de cinc a tres. |
| Temps i despesa | 2468188 | S'ha corregit el problema del text del registre que supera la longitud màxima de l'atribut **notetext** de l'entitat d'**anotació**. |
