---
title: 'Novetats de novembre de 2021: Project Operations per a escenaris basats en recursos/no mantinguts en existències'
description: Aquest article proporciona informació sobre les actualitzacions de qualitat que estan disponibles en el llançament de novembre de 2021 del Project Operations per a escenaris de recursos/sense existències.
author: sigitac
ms.date: 11/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d5b58965f728321cc30d4e476b0dacf621fdec71
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932882"
---
# <a name="whats-new-november-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novetats de novembre de 2021: Project Operations per a escenaris basats en recursos/no mantinguts en existències

*S'aplica a: Project Operations per a escenaris basats en recursos/sense cotització*

Aquest article s'aplica als components i les versions següents del Microsoft Dynamics 365 Project Operations:

- Project Operations en un entorn del Dataverse, versió 4.26.0.145, 4.26.0.148, 4.26.0.150, 4.26.0.155
- Administració de projectes i comptabilitat en un entorn del Dynamics 365 Finance, versió 10.0.22

## <a name="features-included-in-this-release"></a>Característiques incloses en aquesta versió

En aquesta versió s'inclouen les característiques següents:

- Les interfícies de programació d'aplicacions (API) de Planificació de projectes admeten ara la capacitat de crear i suprimir conjunts de projectes.

## <a name="project-operations-dual-write-maps-updates"></a>Actualitzacions de les assignacions de doble ecriptura del Project Operations

En aquesta versió no hi ha actualitzacions per a les assignacions d'escriptura doble del Project Operations. Per a una llista actual i versions de les assignacions d'escriptura doble del Project Operations, consulteu [Versions de les assignacions d'escriptura doble del Project Operations](/dynamics365/project-operations/environment/resource-dual-write-maps).

Executeu sempre la versió més recent de l'assignació a l'entorn i habiliteu totes les assignacions de taules relacionades a mida que actualitzeu la versió de la solució del Finance i del Dataverse del Project Operations. És possible que algunes característiques i capacitats no funcionin correctament si la versió més recent del mapa no s'activa. Podeu visualitzar la versió activa de l'assignació a la columna **Versió** de la pàgina **Escriptura doble**. Per activar una versió nova de l'assignació, seleccioneu **Versions de l'assignació de la taula**, seleccioneu la versió més recent i després deseu la versió seleccionada. Si heu personalitzat una assignació de taules llesta per al seu ús, torneu a aplicar els canvis. Per a més informació, vegeu [Administració del cicle de vida de les aplicacions](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Si teniu qualsevol problema quan inicieu l'assignació, seguiu les instruccions de la secció [Problemes de columnes de la taula que falten](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) de la guia de detecció d'errors de doble escriptura.

## <a name="quality-updates"></a>Actualitzacions de qualitat

### <a name="project-operations-in-dataverse"></a>Project Operations al Dataverse

| Àrea de característiques | Número de referència | Actualització de qualitat |
| --- | --- | --- |
| Facturació i preus | 2240080 | El camp **Condicions de pagament** no pot estar duplicat a la factura proforma. |
| Facturació i preus | 2358236 | La correcció de factures ha de permetre correccions que tinguin línies de preu zero. |
| Administració de recursos | 2410072 | Permetre la configuració d'un recurs que s'ha assignat a la tasca com a administrador del projecte. |
| Facturació i preus | 2430234 | Corregir un problema de càlcul del rendiment de cost. |
| Temps i despesa | 2436978 | Permetre que s'introdueixi l'hora en format hh:mm. |
| Facturació i preus | 2448623 | Permetre que les llistes de preus s'actualitzin després que s'associïn a una unitat organitzativa. |
| Temps i despesa | 2460396 | Permetre suprimir una entrada de temps esborrant la cel·la. |
| Facturació i preus | 2467386 | Permetre suprimir un projecte que té una tasca, encara que la tasca estigui associada a una oferta guanyada. |
| Temps i despesa | 2461744 | La visualització **La meva aprovació fallida** només conté les aprovacions del projecte de la fase **Enviat**. |
| Temps i despesa | 2464082 | Suprimir l'enllaç de les aprovacions del projecte a l'aprovació definida quan coincideix amb un estat de destinació. |
| Temps i despesa | 2468108 | La feina de planificació no ha de definir un estat de **Processament** per al conjunt d'aprovació. |
| Temps i despesa | 2471503 | Suprimir conjunts d'aprovació que tenen set dies d'antiguitat. |
| Facturació i preus | 2480687 | La referència de la línia d'oferta no s'ha d'eliminar quan es crea una fita de línia d'oferta. |

### <a name="project-management-and-accounting-in-finance"></a>Administració de projectes i comptabilitat al Finance

| Àrea de característiques | Número de referència | Actualització de qualitat |
| --- | --- | --- |
| Administració i comptabilitat de projectes | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | Els imports del proveïdor retinguts en les transaccions de despesa del projecte no es mostren a la llista de transaccions. |
| Administració i comptabilitat de projectes | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | La factura del proveïdor entre empreses falla quan la integració de factures del proveïdor està activada. |
| Administració i comptabilitat de projectes | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | Les condicions de pagament de les factures del projecte no funcionen com està previst. |
| Administració i comptabilitat de projectes | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | Quan s'allibera la retenció a proveïdors, la comptabilització de vals té línies addicionals que són incorrectes. |
| Administració i comptabilitat de projectes | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | Quan es publica la integració del Project Operations, falla a causa de la falta de dimensions per a un compte en què no s'està comptabilitzat. |
| Administració i comptabilitat de projectes | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | La pestanya **Projecte** no es pot editar en una factura del proveïdor pendent quan la categoria de proveïment està assignada a l'element. |
| Administració i comptabilitat de projectes | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Falta la subfinestra de navegació si no heu iniciat la sessió al Project Operations Dataverse. |
| Administració i comptabilitat de projectes | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Quan comptabilitzeu ingressos d'una factura del projecte en un cas amb bestreta aplicada, es produeix un error perquè les transaccions del val no es compensen. |
| Administració i comptabilitat de projectes | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | La creació d'una estimació després de comptabilitzar una proposta de factura fa que es bloquegin les línies de correcció contra la importació. |
| Administració i comptabilitat de projectes | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | No hauria de ser possible modificar un registre de fita totalment facturat. |
| Viatge i despesa | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Tots els informes de despesa estan visibles quan cerqueu una categoria a l'aplicació mòbil de despesa. |
| Viatge i despesa | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | Els imports incorrectes de les transaccions de proveïdors i d'impostos de la venda es comptabilitzen des d'una despesa creada a partir d'una transacció de targeta de crèdit. |
| Viatge i despesa | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Quan actualitzeu la pàgina **Informe de despeses**, es produeix un advertiment irrellevant. |
| Viatge i despesa | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | S'utilitza l'aprovador temporal erroni quan suprimiu un aprovador temporal i, a continuació, torneu a enviar un informe de despesa a través del flux de treball. |
| Viatge i despesa | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Es produeix un error de comptabilització relacionat amb la configuració del quilometratge. |
