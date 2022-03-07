---
title: 'Novetats de setembre de 2021: Project Operations per a escenaris basats en recursos/no mantinguts en existències'
description: Aquest tema proporciona informació sobre les actualitzacions de qualitat disponibles a la versió de setembre de 2021 del Project Operations per als escenaris basats en recursos/no mantinguts en existències.
author: sigitac
ms.date: 09/12/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 842ea95892fa4f7a29a778cfd2c33a66e84f676c
ms.sourcegitcommit: 74a7e1c9c338fb8a4b0ad57c5560a88b6e02d0b2
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 09/23/2021
ms.locfileid: "7547142"
---
# <a name="whats-new-september-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novetats de setembre de 2021: Project Operations per a escenaris basats en recursos/no mantinguts en existències

*S'aplica a: Project Operations per a escenaris basats en recursos/sense cotització*

Aquest tema s'aplica als components i versions següents del Dynamics 365 Project Operations:

   - Project Operations en un entorn del Microsoft Dataverse, versió 4.14.0.99.
   - Administració de projectes i comptabilitat a l'entorn del Dynamics 365 Finance versió 10.0.20.

## <a name="project-operations-dual-write-maps-updates"></a>Actualitzacions de les assignacions de doble ecriptura del Project Operations

En aquesta versió no hi ha actualitzacions per a les assignacions d'escriptura doble del Project Operations. Per a una llista actual i versions de les assignacions d'escriptura doble del Project Operations, consulteu [Versions de les assignacions d'escriptura doble del Project Operations](../environment/resource-dual-write-maps.md).

Executeu sempre la versió més recent de l'assignació a l'entorn i habiliteu totes les assignacions de taules relacionades a mida que actualitzeu la versió de la solució del Finance i del Dataverse del Project Operations. És possible que algunes característiques i capacitats no funcionin correctament si la versió més recent del mapa no s'activa. Podeu veure la versió activa de l'assignació a la pàgina **Escriptura doble**, a la columna **Versió**. Per activar una versió nova de l'assignació, seleccioneu **Versions de l'assignació de la taula**, seleccioneu la versió més recent i després deseu la versió seleccionada. Si heu personalitzat una assignació de taules llesta per al seu ús, torneu a aplicar els canvis. Per a més informació, vegeu [Administració del cicle de vida de les aplicacions](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Si teniu qualsevol problema relacionat amb l'inici de l'assignació, seguiu les instruccions de la secció [Falten columnes de taula a les assignacions](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) de la guia de detecció d'errors de doble escriptura.

## <a name="quality-updates"></a>Actualitzacions de qualitat

### <a name="project-operations-on-dataverse"></a>Project Operations a Dataverse

| **Àrea de característiques** | **Número de referència** | **Actualització de qualitat** |
| --- | --- | --- |
| Temps i despeses | 1811407 | S'ha ajustat la funció de seguretat Aprovador de projecte per a les aprovacions d'entrada de despeses. |
| Temps i despeses | 1811438 | S'ha ajustat la funció de seguretat Aprovador de projecte per a la cancel·lació d'aprovacions d'entrada de temps. |
| Temps i despeses | 2370126 | S'han actualitzat les icones de **Tasca de projecte** i **Funció** a l'entitat **Entrada de temps**. |
| Temps i despeses | 2379879 | S'ha corregit la funció **Copia la setmana** a l'entrada de temps quan s'utilitza el Dynamics 365 per a telèfons. |
| Facturació i preus | 2371906 | L'import total de la factura proforma no ha de ser ajustable al Project Operations per a implementacions basades en recursos. |
| Facturació i preus | 2385802 | S'ha corregit l'error que es produeix amb hores reals negatives quan s'actualitzen els totals del projecte. |
| Facturació i preus | 2389675 | Comportament millorat de confirmació de factura proforma. L'entitat de feines que duren molt de temps ha de tenir en compte l'activitat necessària per escriure resultats de confirmació de comptabilitat. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Administració de projectes i comptabilitat al Dynamics 365 Finance

| Àrea de característiques | Número de referència | Actualització de qualitat |
| --- | --- | --- |
| Viatge i despesa | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Els imports de les transaccions fiscals de proveïdors i de vendes que es publiquen a partir d'una despesa creada a partir d'una transacció de targeta de crèdit no són correctes. |
| Viatge i despesa | [4620366](https://fix.lcs.dynamics.com/Issue/Details?kb=4620366&amp;bugId=579485&amp;dbType=3&amp;qc=e864789bd95505ea624c537d585bf113c2de60b97c88439d44693dbd85aa8e92) | Quan es genera el diari de pagaments, es creen les línies de liquidació errònies. |
| Viatge i despesa | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Els imports de les transaccions fiscals de vendes que es publiquen a partir d'una despesa creada a partir d'una transacció de targeta de crèdit no són correctes. |
| Viatge i despesa | [4621765](https://fix.lcs.dynamics.com/Issue/Details?kb=4621765&amp;bugId=587306&amp;dbType=3&amp;qc=6fbfad0123d4e95eaf8d5a5a2f6c354577c991b7905c852ab02d1f94e728a876) | La supressió d'una línia de despesa pot trigar molt temps. |
| Comptabilitat del projecte | [4623737](https://fix.lcs.dynamics.com/Issue/Details?kb=4623737&amp;bugId=598109&amp;dbType=3&amp;qc=4101fc5865201e21815299f2ff11ae46d5d5370510868df86c25ee09a8ca1a0c) | Després d'aplicar la KB 4619395, el canvi de seqüència numèrica a **Contínua** no està admès i quan publiqueu una estimació, es produeix l'error següent: "El sistema no admet la configuració "contínua" de seqüència numèrica Proj_X". |
| Comptabilitat del projecte | [4623332](https://fix.lcs.dynamics.com/Issue/Details?kb=4623332&amp;bugId=586034&amp;dbType=3&amp;qc=2f64bb1977c4a9c9dd2ce9de7e72230b86eca14b6295c5bbfb614ea97ad81caf) | Pot ser que en publicar una factura de proveïdor es produeixi un error amb el missatge següent: "Les transaccions sobre vals no s'equilibraran segons a partir del 17/5/2021. (moneda comptable: 0.00 - moneda d'informes: 0.01)." |
