---
title: 'Novetats de juny de 2022: Project Operations per a escenaris basats en recursos/no mantinguts en existències'
description: Aquest article proporciona informació sobre les actualitzacions de qualitat que estan disponibles a la versió de juny de 2022 del Microsoft Dynamics 365 Project Operations per a escenaris basats en recursos/no mantinguts en existències.
author: sigitac
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 32bc7793c5a0ee8c04272d3ffcbd290b39fce4cc
ms.sourcegitcommit: 7772d72a7c96a44ffb23369f8ffb436813449239
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/20/2022
ms.locfileid: "9031319"
---
# <a name="whats-new-june-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novetats de juny de 2022: Project Operations per a escenaris basats en recursos/no mantinguts en existències

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

Aquest article s'aplica als components i les versions següents del Microsoft Dynamics 365 Project Operations:

- Project Operations en un entorn del Dataverse, versió 4.43.0.77 o 4.43.0.119
- Administració de projectes i comptabilitat en un entorn del Dynamics 365 Finance, versió 10.0.27

## <a name="project-operations-dual-write-maps-updates"></a>Actualitzacions de les assignacions de doble ecriptura del Project Operations

A la taula següent es mostren les assignacions de doble escriptura que s'han modificat o afegit a la versió de juny de 2022 del Project Operations.

| Assignació d'entitats | Versió actualitzada | Comentaris |
| --- | --- | --- |
| Entitat d'exportació de factura del proveïdor del projecte de la integració del Project Operations (msdyn_projectvendorinvoices) | 1.0.0.1 | S'ha definit com a obsolet el camp heretat i s'ha assignat al camp nou per al seguiment de l'estat de la factura de proveïdor. |

Executeu sempre la versió més recent de l'assignació a l'entorn i habiliteu totes les assignacions de taules relacionades a mida que actualitzeu la versió de la solució del Finance i del Dataverse del Project Operations. És possible que algunes característiques i capacitats no funcionin correctament si la versió més recent del mapa no s'activa. Podeu visualitzar la versió activa de l'assignació a la columna **Versió** de la pàgina **Escriptura doble**. Per activar una versió nova de l'assignació, seleccioneu **Versions de l'assignació de la taula**, seleccioneu la versió més recent i després deseu la versió seleccionada. Si heu personalitzat una assignació de taules llesta per al seu ús, torneu a aplicar els canvis. Per a més informació, vegeu [Administració del cicle de vida de les aplicacions](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Si teniu qualsevol problema quan inicieu l'assignació, seguiu les instruccions de la secció [Problemes de columnes de la taula que falten](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) de la guia de detecció d'errors de doble escriptura.

## <a name="quality-updates"></a>Actualitzacions de qualitat

### <a name="project-operations-on-dataverse"></a>Project Operations a Dataverse

| Àrea de característiques | Número de referència | Actualització de qualitat |
| --- | --- | --- |
| Subcontractació | 2708885 | S'ha corregit el missatge d'error que apareix quan un usuari crea un registre de capçalera de reserva de recurs que es pot reservar que no s'emplena amb cap recurs que es pot reservar. |
| Planificació i seguiment de projectes | 2629441 | S'ha corregit la lògica d'activació del flux de treball per evitar un bucle infinit quan s'actualitzen les tasques de projecte. |
| Temps i despeses | 2641209 | Les importacions d'entrades de temps des d'assignacions/reserves han de conservar una referència de recurs que es pot reservar. |
| Planificació i seguiment de projectes | 2651148 | La capçalera del document del projecte s'ha de protegir.|
| Planificació i seguiment de projectes | 2653145 | S'han afegit validacions per garantir que no es pugui crear un registre de projecte que té caràcters no vàlids al nom. |
| Temps i despeses | 2654710 | S'ha corregit el filtre de la pàgina **Aprovacions**. |
| Facturació i preus | 2667805 | S'han afegit validacions per evitar que es creïn valors reals de venda facturada si no existeixen valors reals de vendes no facturades de suport. |
| Facturació i preus | 2668378 | S'han afegit validacions per evitar que s'afegeixi una dimensió de preus personalitzada tret que s'especifiqui un nom lògic i s'empleni un nom de camp. |
| Subcontractació | 2677485 | S'ha actualitzat la versió de destinació de l'assignació de doble escriptura de línies de factura de proveïdor. |
| Temps i despeses | 2700428 | S'ha millorat la lògica d'aprovació per assegurar que altres conjunts d'aprovació del projecte es puguin processar encara que un dels conjunts d'aprovació estigui encallat en feines del sistema. |

### <a name="project-management-and-accounting-in-finance"></a>Administració de projectes i comptabilitat al Finance

Per obtenir informació sobre les correccions d'errors incloses en aquesta actualització, inicieu la sessió al Microsoft Dynamics Lifecycle Services (LCS) i vegeu l'[article de la KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=673271).
