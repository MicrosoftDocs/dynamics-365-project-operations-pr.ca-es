---
title: 'Novetats del maig de 2022: Project Operations per a escenaris basats en recursos/no mantinguts en existències'
description: En aquest article s'ofereix informació sobre les actualitzacions de qualitat que estan disponibles a la versió de Microsoft de maig de Dynamics 365 Project Operations 2022 per a escenaris basats en recursos o no emmagatzemats.
author: sigitac
ms.date: 05/02/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: beb75fc4b721d52cddbdaf2d20194218cefced5e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921382"
---
# <a name="whats-new-may-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novetats del maig de 2022: Project Operations per a escenaris basats en recursos/no mantinguts en existències

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

Aquest article s'aplica als components i versions següents de Microsoft Dynamics 365 Project Operations:

- 4.42.0.70 d'operacions del projecte en una Dataverse versió d'entorn
- Gestió de projectes i comptabilitat en un entorn Dynamics 365 Finance versió 10.0.26

## <a name="project-operations-dual-write-maps-updates"></a>Actualitzacions de les assignacions de doble ecriptura del Project Operations

En aquesta versió no hi ha actualitzacions per a les assignacions d'escriptura doble del Project Operations. Per a una llista actual i versions de les assignacions d'escriptura doble del Project Operations, consulteu [Versions de les assignacions d'escriptura doble del Project Operations](../environment/resource-dual-write-maps.md).

Executeu sempre la versió més recent del mapa al vostre entorn i habiliteu tots els mapes de taula relacionats a mesura que actualitzeu la solució d'operacions Dataverse de projecte i la versió de la solució de finançament. És possible que algunes funcions i capacitats no funcionin correctament si l'última versió del mapa no està activada. Podeu visualitzar la versió activa de l'assignació a la columna **Versió** de la pàgina **Escriptura doble**. Per activar una versió nova de l'assignació, seleccioneu **Versions de l'assignació de la taula**, seleccioneu la versió més recent i després deseu la versió seleccionada. Si has personalitzat un mapa de taula fora de caixa, torna a aplicar els canvis. Per a més informació, vegeu [Administració del cicle de vida de les aplicacions](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Si trobeu un problema quan inicieu el mapa, seguiu les instruccions del problema de columnes de la [taula que falten a la secció mapes](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) de la guia de resolució de problemes de doble escriptura.

## <a name="quality-updates"></a>Actualitzacions de qualitat
### <a name="project-operations-on-dataverse"></a>Project Operations a Dataverse

| Àrea de característiques | Número de referència | Actualització de qualitat |
| --- | --- | --- |
| Administració de recursos | 2634019 | S'han millorat els missatges d'error per a les validacions empresarials en afegir membres genèrics de l'equip com a recursos. |
| Planificació i seguiment de projectes | 2648515 | Actualitzacions restringides del **ownerid**, **l'estat** i **l'estat** de les entitats de planificació. |
| Facturació i preus | 2653167 | El **separador decimal de quadrícula Estimacions** ha de seguir la configuració del format a **Opcions** personals. |
| Facturació i preus| 2662251 | Valors dels **camps Unitat** corregida i **grup** Unitat per defecte en crear registres en estimacions de material. |
| Facturació i preus| 2571408 | Els reals de vendes no facturats s'estampen amb un identificador de factura proforma en crear una factura esborrany. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Gestió de projectes i comptabilitat en Dynamics 365 Finance

Per obtenir informació sobre les correccions d'errors que s'inclouen en aquesta actualització, inicieu la sessió a Microsoft Dynamics Lifecycle Services (LCS) i visualitzeu l'article [de la](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864) KB.
