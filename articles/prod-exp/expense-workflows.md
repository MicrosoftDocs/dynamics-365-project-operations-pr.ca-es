---
title: Configurar els fluxos de treball d'administració de despeses
description: Podeu configurar un procés de flux de treball per revisar i aprovar els documents de viatges i de despeses.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8f3235d12499c68a52f9d1c7e118e7bc91dc3a0a
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960505"
---
# <a name="set-up-expense-management-workflows"></a>Configurar els fluxos de treball d'administració de despeses

Podeu configurar un procés de flux de treball que s'utilitzi per revisar i aprovar els documents de viatges i de despeses. Els documents per als quals es poden definir fluxos de treball inclouen informes de despeses, peticions de viatges i sol·licituds d'avançament d'efectiu.

Un flux de treball representa un procés de negoci. Defineix com passa un document pel sistema i indica qui ha de completar una tasca o aprovar un document. Hi ha diversos avantatges d'utilitzar el sistema de flux de treball a l'organització:

-   **Processos coherents**: podeu definir el procés d'aprovació per a documents específics, com ara les requisicions de compra i els informes de despeses. L'ús del sistema de flux de treball ajuda a garantir que els documents es processen i s'aproven de manera coherent i eficient.

-   Visibilitat de procés: podeu fer el seguiment de l'estat, de l'historial i de les mètriques de rendiment d'una instància de flux de treball concreta. Això us ajudarà a determinar si s'han de fer canvis al flux de treball per millorar l'eficiència.

-   Llista de treball centralitzada: els usuaris poden visualitzar una llista de treball centralitzada per visualitzar les tasques del flux de treball i les aprovacions assignades. 

**Tipus de fluxos de treball que podeu crear**

A la taula següent s'enumeren els tipus de fluxos de treball que es poden crear a **Despesa**.


|              <strong>Tipus</strong>              |                   <strong>Utilitzeu aquest tipus per</strong>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|         <strong>Informe de despeses</strong>         |            Crear fluxos de treball d'aprovació per a informes de despeses.             |
|  <strong>Publicació automàtica d'informes de despeses</strong>   |        Crear fluxos de treball de publicació automàtica per a informes de despeses.        |
|       <strong>Element de línia de despesa</strong>        |     Crear fluxos de treball d'aprovació per a elements de línia d'informes de despeses.      |
| <strong>Publicació automàtica d'elements de línies de despesa</strong> | Crear fluxos de treball de publicació automàtica per a elements de línia d'informes de despeses. |
|       <strong>Petició de viatge</strong>       |          Crear fluxos de treball d'aprovació per a requisicions de viatge.           |
|      <strong>Sol·licitud d'avançament d'efectiu</strong>      |         Crear fluxos de treball d'aprovació per a sol·licituds d'avançament d'efectiu.          |
|        <strong>Recuperació de l'IVA</strong>        | Crear fluxos de treball d'aprovació per a la recuperació de l'impost sobre el valor afegit (IVA).  |



[!INCLUDE[footer-include](../includes/footer-banner.md)]