---
title: 'Novetats de juny de 2022: Project Operations per a escenaris basats en recursos/no mantinguts en existències'
description: Aquest article proporciona informació sobre les actualitzacions de qualitat que estan disponibles a la versió de Microsoft de juny de Dynamics 365 Project Operations 2022 per a escenaris basats en recursos o no emmagatzemats.
author: sigitac
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: fde1f0be42eecfc5ee809cb9b2191d3aeae57131
ms.sourcegitcommit: 51745acac29dfacba43a4003d86baff4d6ca2fb8
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/14/2022
ms.locfileid: "8959609"
---
# <a name="whats-new-june-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novetats de juny de 2022: Project Operations per a escenaris basats en recursos/no mantinguts en existències

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

Aquest article s'aplica als components i versions següents de Microsoft Dynamics 365 Project Operations:

- 4.43.0.77 d'operacions del projecte en una Dataverse versió d'entorn
- Gestió de projectes i comptabilitat en un entorn Dynamics 365 Finance versió 10.0.27

## <a name="project-operations-dual-write-maps-updates"></a>Actualitzacions de les assignacions de doble ecriptura del Project Operations

La taula següent mostra els mapes de doble escriptura que s'han modificat o afegit a la versió d'operacions del projecte de juny de 2022.

| Assignació d'entitats | Versió actualitzada | Comentaris |
| --- | --- | --- |
| Entitat d'exportació de factura del proveïdor del projecte de la integració del Project Operations (msdyn_projectvendorinvoices) | 1.0.0.1 | S'ha obsolet el camp heretat i s'ha assignat al camp nou per al seguiment de l'estat de la factura del proveïdor. |

Executeu sempre la versió més recent del mapa al vostre entorn i habiliteu tots els mapes de taula relacionats a mesura que actualitzeu la solució d'operacions Dataverse de projecte i la versió de la solució de finançament. És possible que algunes funcions i capacitats no funcionin correctament si l'última versió del mapa no està activada. Podeu visualitzar la versió activa de l'assignació a la columna **Versió** de la pàgina **Escriptura doble**. Per activar una versió nova de l'assignació, seleccioneu **Versions de l'assignació de la taula**, seleccioneu la versió més recent i després deseu la versió seleccionada. Si has personalitzat un mapa de taula fora de caixa, torna a aplicar els canvis. Per a més informació, vegeu [Administració del cicle de vida de les aplicacions](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Si trobeu un problema quan inicieu el mapa, seguiu les instruccions del problema de columnes de la [taula que falten a la secció mapes](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) de la guia de resolució de problemes de doble escriptura.

## <a name="quality-updates"></a>Actualitzacions de qualitat

### <a name="project-operations-on-dataverse"></a>Project Operations a Dataverse

| Àrea de característiques | Número de referència | Actualització de qualitat |
| --- | --- | --- |
| Subcontractació | 2708885 | S'ha corregit el missatge d'error que apareix quan un usuari crea un registre de capçalera de reserva de recurs que es pot reservar on no s'emplena cap recurs que es pot reservar. |
| Planificació i seguiment de projectes | 2629441 | S'ha corregit la lògica activadora del flux de treball per ajudar a evitar un bucle infinit quan s'actualitzen les tasques del projecte. |
| Temps i despeses | 2641209 | Les importacions d'entrades d'hora de les tasques o les reserves han de conservar una referència de recursos que es pot reservar. |
| Planificació i seguiment de projectes | 2651148 | Cal protegir la capçalera del document del projecte.|
| Planificació i seguiment de projectes | 2653145 | S'han afegit validacions per assegurar-vos que no es pot crear un registre de projecte que tingui caràcters no vàlids al seu nom. |
| Temps i despeses | 2654710 | S'ha corregit el filtratge de la **pàgina Aprovacions**. |
| Facturació i preus | 2667805 | S'han afegit validacions per ajudar a evitar que es creïn reals de venda facturada si no existeixen còpies de suport de vendes no facturades. |
| Facturació i preus | 2668378 | S'han afegit validacions per evitar que s'afegeixi una dimensió de preus personalitzada tret que s'ompli un nom lògic i un nom de camp. |
| Subcontractació | 2677485 | S'ha actualitzat la versió de destinació del mapa de doble escriptura de les línies de factura del proveïdor. |
| Temps i despeses | 2700428 | S'ha millorat la lògica de les aprovacions per assegurar-se que altres conjunts d'aprovació del projecte es poden processar fins i tot si un dels conjunts d'aprovació està atrapat en les feines del sistema. |

### <a name="project-management-and-accounting-in-finance"></a>Gestió de projectes i comptabilitat en Finances

Per obtenir informació sobre les correccions d'errors que s'inclouen en aquesta actualització, inicieu la sessió a Microsoft Dynamics Lifecycle Services (LCS) i visualitzeu l'article de la [KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=673271).
