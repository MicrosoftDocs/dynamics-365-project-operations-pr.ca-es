---
title: "Novetats d'agost de 2022: Project Operations per a escenaris basats en recursos/no mantinguts en existències"
description: Aquest article proporciona informació sobre les actualitzacions de qualitat disponibles a la versió d'agost de 2022 de Microsoft Dynamics 365 Project Operations per a escenaris basats en recursos o no emmagatzemats.
author: ramagadu
ms.date: 07/19/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 112dbb98de09ef342c03d122a29cb8025058e47f
ms.sourcegitcommit: 6b6c2bfd04e3e613ed1f38355c7cd47c3a56748d
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 08/24/2022
ms.locfileid: "9348093"
---
# <a name="whats-new-august-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novetats d'agost de 2022: Project Operations per a escenaris basats en recursos/no mantinguts en existències

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

Aquest article s'aplica als components i versions de Microsoft Dynamics 365 Project Operations següents:

- Project Operations en una Dataverse versió d'entorn 4.45.0.53
- Administració i comptabilitat de projectes en un entorn Dynamics 365 Finance versió 10.0.28

## <a name="project-operations-dual-write-maps-updates"></a>Actualitzacions de les assignacions de doble ecriptura del Project Operations

En aquesta versió no hi ha actualitzacions per a les assignacions d'escriptura doble del Project Operations. Per a una llista actual i versions de les assignacions d'escriptura doble del Project Operations, consulteu [Versions de les assignacions d'escriptura doble del Project Operations](../environment/resource-dual-write-maps.md).

Executeu sempre la versió més recent del mapa al vostre entorn i activeu tots els mapes de taula relacionats a mesura que actualitzeu la versió de la solució Project Operations Dataverse i la versió de la solució Finance. És possible que algunes funcions i capacitats no funcionin correctament si la versió més recent del mapa no està activada. Podeu visualitzar la versió activa de l'assignació a la columna **Versió** de la pàgina **Escriptura doble**. Per activar una versió nova de l'assignació, seleccioneu **Versions de l'assignació de la taula**, seleccioneu la versió més recent i després deseu la versió seleccionada. Si heu personalitzat un mapa de taula estàndard, torneu a aplicar els canvis. Per a més informació, vegeu [Administració del cicle de vida de les aplicacions](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Si trobeu un problema en iniciar el mapa, seguiu les instruccions del problema Falten columnes de taula a la [secció mapes](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) de la guia de resolució de problemes de doble escriptura.

## <a name="quality-updates"></a>Actualitzacions de qualitat

### <a name="project-operations-on-dataverse"></a>Project Operations a Dataverse

| Àrea de característiques | Número de referència | Actualització de qualitat |
| --- | --- | --- |
|   Administració d'oportunitats | 2762089 | Gestió d'errors en tancar el contracte com a perdut si el desament automàtic està desactivat a l'organització.|

### <a name="project-management-and-accounting-in-finance"></a>Administració i comptabilitat de projectes en finances

Per obtenir informació sobre les correccions d'errors que s'inclouen en aquesta actualització, inicieu la sessió a Microsoft Dynamics Lifecycle Services (LCS) i visualitzeu l'article de la [KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438).
