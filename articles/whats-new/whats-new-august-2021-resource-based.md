---
title: "Novetats d'agost de 2021: Project Operations per a escenaris basats en recursos/no mantinguts en existències"
description: Aquest tema proporciona informació sobre les actualitzacions de qualitat disponibles a la versió d'agost de 2021 del Project Operations per a escenaris basats en recursos/no mantinguts en existències.
author: sigitac
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 144a8c0d5ac47ad6fee54850c149a349f1698049
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8594152"
---
# <a name="whats-new-august-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novetats d'agost de 2021: Project Operations per a escenaris basats en recursos/no mantinguts en existències

*S'aplica a: Project Operations per a escenaris basats en recursos/sense cotització*

Aquest tema s'aplica als components i versions següents del Dynamics 365 Project Operations:

   - Project Operations en un entorn del Microsoft Dataverse, versió 4.13.0.152.
   - Gestió de projectes i comptabilitat en Dynamics 365 Finance entorn versió 10.0.20.

## <a name="features-included-in-this-release"></a>Característiques incloses en aquesta versió

En aquesta versió s'inclouen les característiques següents:

- **Conjunts d'aprovació**: els conjunts d'aprovació agrupen sol·licituds d'aprovació de temps, despeses o ús de materials en subconjunts d'operacions més petits. Aquest agrupament permet processar les aprovacions en un ordre específic per projecte i tornar a provar i seqüenciar. L'agrupació de les sol·licituds millora la fiabilitat i la traçabilitat del processament d'aprovacions per a grans volums d'aprovacions. Per obtenir més informació, [Conjunts d'aprovació](../approvals/approval-sets.md).

## <a name="project-operations-dual-write-maps-updates"></a>Actualitzacions de les assignacions de doble ecriptura del Project Operations

En aquesta versió no hi ha actualitzacions per a les assignacions d'escriptura doble del Project Operations.

Per a una llista actual i versions de les assignacions d'escriptura doble del Project Operations, consulteu [Versions de les assignacions d'escriptura doble del Project Operations](../environment/resource-dual-write-maps.md).

Executeu sempre la versió més recent de l'assignació a l'entorn i habiliteu totes les assignacions de taules relacionades a mida que actualitzeu la versió de la solució del Finance i del Dataverse del Project Operations. És possible que algunes característiques i capacitats no funcionin correctament si la versió més recent del mapa no s'activa. Podeu veure la versió activa de l'assignació a la pàgina **Escriptura doble**, a la columna **Versió**. Per activar una versió nova de l'assignació, seleccioneu les **Versions de l’assignació de taules**, seleccioneu la versió més recent i deseu la versió seleccionada. Si heu personalitzat una assignació de taules llesta per al seu ús, torneu a aplicar els canvis. Per a més informació, vegeu [Administració del cicle de vida de les aplicacions](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Si teniu qualsevol problema relacionat amb l'inici de l'assignació, seguiu les instruccions de la secció [Problema Falten columnes de la taula a les assignacions](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) de la guia de solució de problemes de l'escriptura doble.

## <a name="quality-updates"></a>Actualitzacions de qualitat

### <a name="project-operations-on-dataverse"></a>Project Operations a Dataverse

| **Àrea de característiques** | **Número de referència** | **Actualització de qualitat** |
| --- | --- | --- |
| Facturació i preus | 2295625 | La fita s'ha de copiar des de la planificació de facturació al detall de la línia de factura. |
| Facturació i preus | 2316323 | El descompte no s'ha de poder editar en una factura proforma al Project Operations per a escenaris basats en recursos. |
|   Administració d'oportunitats | 2338619 | Les regles de negocis **Oportunitat** i **Oferta** només s'han d'invocar a les pàgines. |
| Administració de recursos | 2316523 | L'ús d'**Envia la sol·licitud** d'un requisit de recursos que té una funció adjunta no hauria de mostrar un error. |
| Administració de recursos | 2326885 | La creació d'un requisit de recursos a través d'un projecte no hauria de mostrar un error. |
| Temps i despeses | 2335584 | Fluxos de tasca obsolets a l'entrada de temps. |
| Temps i despeses | 2336884 | El botó **Copia l'hora de la setmana** ha de funcionar per a més que l'usuari actual. |


### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Gestió de projectes i comptabilitat sobre Dynamics 365 Finance

| Àrea de característiques | Número de referència | Actualització de qualitat |
| --- | --- | --- |
| Viatge i despesa | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Es publiquen imports de transacció de proveïdor i de transacció amb impost sobre les vendes incorrectes quan es crea una despesa a partir d'una transacció de targeta de crèdit. |
| Viatge i despesa | [4620366](https://fix.lcs.dynamics.com/Issue/Details?kb=4620366&amp;bugId=579485&amp;dbType=3&amp;qc=e864789bd95505ea624c537d585bf113c2de60b97c88439d44693dbd85aa8e92) | Quan es genera el diari de pagament, es creen línies de liquidació incorrectes. |
| Viatge i despesa | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Es publiquen imports de transacció amb impost sobre les vendes incorrectes quan es crea una despesa a partir d'una transacció de targeta de crèdit. |
| Viatge i despesa | [4621765](https://fix.lcs.dynamics.com/Issue/Details?kb=4621765&amp;bugId=587306&amp;dbType=3&amp;qc=6fbfad0123d4e95eaf8d5a5a2f6c354577c991b7905c852ab02d1f94e728a876) | La supressió d'una línia de despesa pot trigar molt temps. |
| Comptabilitat del projecte | [4623737](https://fix.lcs.dynamics.com/Issue/Details?kb=4623737&amp;bugId=598109&amp;dbType=3&amp;qc=4101fc5865201e21815299f2ff11ae46d5d5370510868df86c25ee09a8ca1a0c) | El sistema no admet la configuració de la seqüenciació de nombres continus quan publiqueu una estimació després d'aplicar KB 4619395. |
| Comptabilitat del projecte | [4623332](https://fix.lcs.dynamics.com/Issue/Details?kb=4623332&amp;bugId=586034&amp;dbType=3&amp;qc=2f64bb1977c4a9c9dd2ce9de7e72230b86eca14b6295c5bbfb614ea97ad81caf) | La publicació de la factura del proveïdor podria fallar amb el missatge d'error: "Les transaccions del val no s'equilibren a 17/5/2021. (moneda comptable: 0.00 - moneda d'informes: 0.01)" |
