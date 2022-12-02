---
title: "Novetats d'agost de 2022: Project Operations per a escenaris basats en recursos/no mantinguts en existències"
description: Aquest article proporciona informació sobre les actualitzacions de qualitat que estan disponibles a la versió d'agost de 2022 del Microsoft Dynamics 365 Project Operations per a escenaris basats en recursos/no mantinguts en existències.
author: ramagadu
ms.date: 07/19/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 4042dca72a33f48e04e51af2a3cfd2da83146afd
ms.sourcegitcommit: 7ed8e77a92917f2d242988ca02bd7de9571cce5e
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 09/02/2022
ms.locfileid: "9403844"
---
# <a name="whats-new-august-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novetats d'agost de 2022: Project Operations per a escenaris basats en recursos/no mantinguts en existències

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

Aquest article s'aplica als components i les versions següents del Microsoft Dynamics 365 Project Operations:

- Project Operations en un entorn del Dataverse, versió 4.45.0.53
- Administració de projectes i comptabilitat en un entorn del Dynamics 365 Finance, versió 10.0.28

## <a name="project-operations-dual-write-maps-updates"></a>Actualitzacions de les assignacions de doble ecriptura del Project Operations

En aquesta versió no hi ha actualitzacions per a les assignacions d'escriptura doble del Project Operations. Per a una llista actual i versions de les assignacions d'escriptura doble del Project Operations, consulteu [Versions de les assignacions d'escriptura doble del Project Operations](../environment/resource-dual-write-maps.md).

Executeu sempre la versió més recent de l'assignació a l'entorn i habiliteu totes les assignacions de taules relacionades a mida que actualitzeu la versió de la solució del Finance i del Dataverse del Project Operations. És possible que algunes característiques i capacitats no funcionin correctament si la versió més recent del mapa no s'activa. Podeu visualitzar la versió activa de l'assignació a la columna **Versió** de la pàgina **Escriptura doble**. Per activar una versió nova de l'assignació, seleccioneu **Versions de l'assignació de la taula**, seleccioneu la versió més recent i després deseu la versió seleccionada. Si heu personalitzat una assignació de taules llesta per al seu ús, torneu a aplicar els canvis. Per a més informació, vegeu [Administració del cicle de vida de les aplicacions](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Si teniu qualsevol problema quan inicieu l'assignació, seguiu les instruccions de la secció [Problemes de columnes de la taula que falten](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) de la guia de detecció d'errors de doble escriptura.

## <a name="quality-updates"></a>Actualitzacions de qualitat

### <a name="project-operations-on-dataverse"></a>Project Operations a Dataverse

| Àrea de característiques | Número de referència | Actualització de qualitat |
| --- | --- | --- |
|   Administració d'oportunitats | 2762089 | Es produeix un error mentre es tanca el contracte com a perdut si el desament automàtic està inhabilitat a l'organització.|
|Planificació i seguiment de projectes | 2767841 | La telemetria actualitza els escenaris de creació o actualització de l'entitat Projecte.|
|Facturació i preus | 2771072 | Gestió d'excepcions de referència nul·la en guanyar una oferta.|
|Facturació i preus | 2844181 |Es produeix un error a l'hora d'obtenir un id de correlació i bloquejar la creació d'una factura.|
|Facturació i preus | 2852836 | Falten valors reals entre empreses per a la despesa entre empreses creada i aprovada a la CE.|


### <a name="project-management-and-accounting-in-finance"></a>Administració de projectes i comptabilitat al Finance

Per obtenir informació sobre les correccions d'errors incloses en aquesta actualització, inicieu la sessió al Microsoft Dynamics Lifecycle Services (LCS) i vegeu l'[article de la KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438).
