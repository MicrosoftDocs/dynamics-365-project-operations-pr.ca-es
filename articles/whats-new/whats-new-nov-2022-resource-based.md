---
title: 'Novetats de novembre de 2022: Project Operations per a escenaris basats en recursos/no mantinguts en existències'
description: Aquest article proporciona informació sobre les actualitzacions de qualitat disponibles a la versió de novembre de 2022 de Microsoft Dynamics 365 Project Operations per a escenaris basats en recursos o no emmagatzemats.
author: ryansandness
ms.date: 12/16/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ryansandness
ms.openlocfilehash: 509e303aeb0567627590fd89c6888b59a414c6f1
ms.sourcegitcommit: 952fcefe33de192ad48f4108c3adbe658fd7b94f
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 12/08/2022
ms.locfileid: "9831123"
---
# <a name="whats-new-november-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novetats de novembre de 2022: Project Operations per a escenaris basats en recursos/no mantinguts en existències

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

Aquest article s'aplica als components i les versions següents del Microsoft Dynamics 365 Project Operations:

- Project Operations en un entorn del Dataverse, versió 4.58.0.119
- Administració de projectes i comptabilitat en un entorn del Dynamics 365 Finance, versió 10.0.30

## <a name="project-operations-dual-write-maps-updates"></a>Actualitzacions de les assignacions de doble ecriptura del Project Operations

En aquesta versió no hi ha actualitzacions per a les assignacions d'escriptura doble del Project Operations. Per a una llista actual i versions de les assignacions d'escriptura doble del Project Operations, consulteu [Versions de les assignacions d'escriptura doble del Project Operations](../environment/resource-dual-write-maps.md).

Executeu sempre la versió més recent de l'assignació a l'entorn i habiliteu totes les assignacions de taules relacionades a mida que actualitzeu la versió de la solució del Finance i del Dataverse del Project Operations. És possible que algunes característiques i capacitats no funcionin correctament si la versió més recent del mapa no s'activa. Podeu visualitzar la versió activa de l'assignació a la columna **Versió** de la pàgina **Escriptura doble**. Per activar una versió nova de l'assignació, seleccioneu **Versions de l'assignació de la taula**, seleccioneu la versió més recent i després deseu la versió seleccionada. Si heu personalitzat una assignació de taules llesta per al seu ús, torneu a aplicar els canvis. Per a més informació, vegeu [Administració del cicle de vida de les aplicacions](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Si teniu qualsevol problema quan inicieu l'assignació, seguiu les instruccions de la secció [Problemes de columnes de la taula que falten](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) de la guia de detecció d'errors de doble escriptura.

## <a name="quality-updates"></a>Actualitzacions de qualitat

### <a name="project-operations-on-dataverse"></a>Project Operations a Dataverse

| Àrea de característiques | Número de referència | Actualització de qualitat |
| --- | --- | --- |
| Facturació i preus | 2781818 | La clau no ha trobat l'error mentre s'omet el preu per al registre d'ús de material. |
| Facturació i preus | 2922373 | No es pot enllaçar la línia de pressupost amb el projecte que s'ha tancat com a pressupost perdut. |
| Facturació i preus | 2943206 | **El camp Línia de** contracte de l'entitat del projecte hauria de ser opcional. |
| Facturació i preus | 2953182 | Millorar el missatge d'error de les factures rectificatives.|
| Facturació i preus | 2959500 | No es pot enllaçar la línia de pressupost a una tasca del projecte que ja està associada a una oferta perduda.|
| Facturació i preus | 2959560 | Missatge "Aquest client ja està en el Project Contract" rebut mentre es tanca el pressupost com guanyat en determinats locals. |
| Facturació i preus | 3031727 | Les assignacions de recursos fallen amb El camp obligatori "msdyn_Company" falta a l'error. |
| Facturació i preus | 3036905 | L'empresa propietària mai no s'inicialitza al ProjectTeamMember. |
| Administració d'oportunitats | 2763519 | Error de referència nul a EnsureProjectContractAllowsUpdates. |
| Administració d'oportunitats | 2783798 | Quan s'importen estimacions de projecte en línia de pressupost, falten descripcions de tasques per a estimacions de despeses i materials.|
| Administració d'oportunitats | 2988635 | Milloreu la descripció de msg d'error en suprimir el client a l'oferta. |
| Administració d'oportunitats | 3001191 | No es pot crear una oferta des d'Opportunity on el mètode de facturació s'especifica com a nul. |
| Actualització | 3012324 | La conversió de projecte ha fallat en un projecte amb caràcters de control com Tab al seu nom. || Planificació i seguiment de projectes | 2790384 | El temps d'espera pendent d'OperacióSet és massa curt. |
| Planificació i seguiment de projectes | 3044275 | Falta localització per a: missingProjectSchedulerErrorMessage. |
| Planificació i seguiment de projectes | 3044277 | La quadrícula Project Recon no es carrega quan el planificador no està configurat.|
| Administració de recursos | 2943153 | Actualitzeu la pestanya Seguiment per mostrar dos decimals durant la durada.|
| Subcontractació | 2932774 | Línia de factura del proveïdor Llegiu només l'error de llançament incorrecte. |
| Subcontractació | 2939556 | L'estat de la capçalera de factura de proveïdor no s'ha d'establir com a Esborrany de supressió en línia si no està actiu. |
| Temps i despesa | 2939998 | Captació de la nova versió TESA a ProjOps. |


### <a name="project-management-and-accounting-in-finance"></a>Administració de projectes i comptabilitat al Finance

Per obtenir informació sobre les correccions d'errors incloses en aquesta actualització, inicieu la sessió al Microsoft Dynamics Lifecycle Services i vegeu l'[article de la KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468).
