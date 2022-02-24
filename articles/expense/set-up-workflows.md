---
title: Configurar fluxos de treball per a l'administració de despeses
description: Podeu configurar un procés de flux de treball que s'utilitzi per revisar i aprovar els documents de viatges i de despeses.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: af6463b07e282ae1ff6aa7dc1a540ff7c8cc318a
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127686"
---
# <a name="set-up-workflows-for-expense-management"></a>Configurar fluxos de treball per a l'administració de despeses

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

Podeu configurar un procés de flux de treball per revisar i aprovar els documents de viatges i de despeses. Podeu definir fluxos de treball per a informes de despeses, requisicions de viatge i sol·licituds d'avançament en efectiu.

Un flux de treball representa un procés de negoci i defineix com un document flueix pel sistema. El flux de treball també indica qui ha de completar una tasca o aprovar un document. Hi ha diversos avantatges d'utilitzar el sistema de flux de treball a l'organització:

- **Processos coherents**: podeu definir el procés d'aprovació per a documents específics, com ara les requisicions de compra i els informes de despeses. L'ús del sistema de flux de treball ajuda a garantir que els documents es processen i s'aproven de manera coherent i eficient.
- **Visibilitat de procés**: podeu fer el seguiment de l'estat, de l'historial i de les mètriques de rendiment d'una instància de flux de treball concreta. Això us ajudarà a determinar si s'han de fer canvis al flux de treball per millorar l'eficiència.
- **Llista de treball centralitzada**: els usuaris poden visualitzar una llista de treball centralitzada per visualitzar les tasques del flux de treball i les aprovacions assignades. 

## <a name="workflow-types"></a>Tipus de flux de treball

A la taula següent s'enumeren els tipus de fluxos de treball que es poden crear a **Administració de despeses**.


|              <strong>Tipus</strong>              |                   <strong>Utilitzeu aquest tipus per</strong>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|   <strong>Aprovació automàtica d'informes de despeses</strong> |            Crear fluxos de treball d'aprovació per a informes de despeses.             |
|  <strong>Publicació automàtica d'informes de despeses</strong>   |        Crear fluxos de treball de publicació automàtica per a informes de despeses.        |
|       <strong>Element de línia de despesa</strong>        |     Crear fluxos de treball d'aprovació per a elements de línia d'informes de despeses.      |
| <strong>Publicació automàtica d'elements de línies de despesa</strong> | Crear fluxos de treball de publicació automàtica per a elements de línia d'informes de despeses. |
|       <strong>Petició de viatge</strong>       |          Crear fluxos de treball d'aprovació per a requisicions de viatge.           |
|      <strong>Sol·licitud d'avançament d'efectiu</strong>      |         Crear fluxos de treball d'aprovació per a sol·licituds d'avançament d'efectiu.          |
|        <strong>Recuperació de l'IVA</strong>        | Crear fluxos de treball d'aprovació per a la recuperació de l'impost sobre el valor afegit (IVA).  |
