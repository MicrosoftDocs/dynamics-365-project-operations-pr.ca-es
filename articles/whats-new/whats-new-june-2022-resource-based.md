---
title: 'Novetats de juny de 2022: Project Operations per a escenaris basats en recursos/no mantinguts en existències'
description: Aquest article proporciona informació sobre les actualitzacions de qualitat disponibles a la versió de juny de 2022 de Microsoft Dynamics 365 Project Operations per a escenaris basats en recursos o no emmagatzemats.
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

Aquest article s'aplica als components i versions de Microsoft Dynamics 365 Project Operations següents:

- Project Operations en una Dataverse versió d'entorn 4.43.0.77 o 4.43.0.119
- Administració i comptabilitat de projectes en un entorn Dynamics 365 Finance versió 10.0.27

## <a name="project-operations-dual-write-maps-updates"></a>Actualitzacions de les assignacions de doble ecriptura del Project Operations

La taula següent mostra els mapes de doble escriptura que s'han modificat o afegit a la versió operacions del projecte de juny de 2022.

| Assignació d'entitats | Versió actualitzada | Comentaris |
| --- | --- | --- |
| Entitat d'exportació de factura del proveïdor del projecte de la integració del Project Operations (msdyn_projectvendorinvoices) | 1.0.0.1 | S'ha obsolet el camp heretat i s'ha assignat al camp nou per al seguiment de l'estat de les factures dels proveïdors. |

Executeu sempre la versió més recent del mapa al vostre entorn i activeu tots els mapes de taula relacionats a mesura que actualitzeu la versió de la solució Project Operations Dataverse i la versió de la solució Finance. És possible que algunes funcions i capacitats no funcionin correctament si la versió més recent del mapa no està activada. Podeu visualitzar la versió activa de l'assignació a la columna **Versió** de la pàgina **Escriptura doble**. Per activar una versió nova de l'assignació, seleccioneu **Versions de l'assignació de la taula**, seleccioneu la versió més recent i després deseu la versió seleccionada. Si heu personalitzat un mapa de taula estàndard, torneu a aplicar els canvis. Per a més informació, vegeu [Administració del cicle de vida de les aplicacions](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Si trobeu un problema en iniciar el mapa, seguiu les instruccions del problema Falten columnes de taula a la [secció mapes](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) de la guia de resolució de problemes de doble escriptura.

## <a name="quality-updates"></a>Actualitzacions de qualitat

### <a name="project-operations-on-dataverse"></a>Project Operations a Dataverse

| Àrea de característiques | Número de referència | Actualització de qualitat |
| --- | --- | --- |
| Subcontractació | 2708885 | S'ha corregit el missatge d'error que apareix quan un usuari crea un registre de capçalera de reserva de recursos que es pot reservar on no s'emplena cap recurs que es pot reservar. |
| Planificació i seguiment de projectes | 2629441 | S'ha corregit la lògica d'activació del flux de treball per ajudar a evitar un bucle infinit quan s'actualitzen les tasques del projecte. |
| Temps i despeses | 2641209 | Les importacions d'entrades de temps de les tasques/reserves han de conservar una referència de recurs que es pot reservar. |
| Planificació i seguiment de projectes | 2651148 | S'ha de custodiar la capçalera del document del projecte.|
| Planificació i seguiment de projectes | 2653145 | S'han afegit validacions per garantir que no es pugui crear un registre de projecte que tingui caràcters no vàlids al seu nom. |
| Temps i despeses | 2654710 | S'ha corregit el filtratge a la **pàgina Aprovacions**. |
| Facturació i preus | 2667805 | S'han afegit validacions per ajudar a evitar que es creïn reals de venda facturats si no existeixen còpies de seguretat reals de vendes no regulades. |
| Facturació i preus | 2668378 | S'han afegit validacions per evitar que s'afegeixi una dimensió de preus personalitzada tret que s'empleni un nom lògic i un nom de camp. |
| Subcontractació | 2677485 | S'ha actualitzat la versió de destinació de les línies de factures del proveïdor de doble mapa d'escriptura. |
| Temps i despeses | 2700428 | S'ha millorat la lògica d'aprovacions per garantir que es puguin tramitar altres conjunts d'aprovació del projecte encara que un dels conjunts d'aprovació estigui encallat en els treballs del sistema. |

### <a name="project-management-and-accounting-in-finance"></a>Administració i comptabilitat de projectes en finances

Per obtenir informació sobre les correccions d'errors que s'inclouen en aquesta actualització, inicieu la sessió a Microsoft Dynamics Lifecycle Services (LCS) i visualitzeu l'article de la [KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=673271).
