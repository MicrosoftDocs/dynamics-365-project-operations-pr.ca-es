---
title: 'Novetats de juliol de 2022: Project Operations per a escenaris basats en recursos/no mantinguts en existències'
description: Aquest article proporciona informació sobre les actualitzacions de qualitat que estan disponibles a la versió de juliol de 2022 del Microsoft Dynamics 365 Project Operations per a escenaris basats en recursos/no mantinguts en existències.
author: ramagadu
ms.date: 07/19/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: e63b29741dbaa400a2176ff8b4c35c6d64dfeab4
ms.sourcegitcommit: 7ed8e77a92917f2d242988ca02bd7de9571cce5e
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 09/02/2022
ms.locfileid: "9403939"
---
# <a name="whats-new-july-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novetats de juliol de 2022: Project Operations per a escenaris basats en recursos/no mantinguts en existències

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

Aquest article s'aplica als components i les versions següents del Microsoft Dynamics 365 Project Operations:

- Project Operations en un entorn del Dataverse, versió 4.44.0.22
- Administració de projectes i comptabilitat en un entorn del Dynamics 365 Finance, versió 10.0.28

## <a name="project-operations-dual-write-maps-updates"></a>Actualitzacions de les assignacions de doble ecriptura del Project Operations

En aquesta versió no hi ha actualitzacions per a les assignacions d'escriptura doble del Project Operations. Per a una llista actual i versions de les assignacions d'escriptura doble del Project Operations, consulteu [Versions de les assignacions d'escriptura doble del Project Operations](../environment/resource-dual-write-maps.md).

Executeu sempre la versió més recent de l'assignació a l'entorn i habiliteu totes les assignacions de taules relacionades a mida que actualitzeu la versió de la solució del Finance i del Dataverse del Project Operations. És possible que algunes característiques i capacitats no funcionin correctament si la versió més recent del mapa no s'activa. Podeu visualitzar la versió activa de l'assignació a la columna **Versió** de la pàgina **Escriptura doble**. Per activar una versió nova de l'assignació, seleccioneu **Versions de l'assignació de la taula**, seleccioneu la versió més recent i després deseu la versió seleccionada. Si heu personalitzat una assignació de taules llesta per al seu ús, torneu a aplicar els canvis. Per a més informació, vegeu [Administració del cicle de vida de les aplicacions](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Si teniu qualsevol problema quan inicieu l'assignació, seguiu les instruccions de la secció [Problemes de columnes de la taula que falten](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) de la guia de detecció d'errors de doble escriptura.

## <a name="quality-updates"></a>Actualitzacions de qualitat

### <a name="project-operations-on-dataverse"></a>Project Operations a Dataverse

| Àrea de característiques | Número de referència | Actualització de qualitat |
| --- | --- | --- |
| Implementació i configuració | 2761472 | Es resol un error d'instal·lació del Project Operations. |
| Facturació i preus | 2746940 | El nom de la línia de subcontracte ha de tenir una longitud màxima de 100 caràcters. |
| Facturació i preus | 2739162 | Els clients han de poder veure els botons de la franja a la visualització de la quadrícula de valors reals. |
| Planificació i seguiment de projectes | 2730318 | S'ha actualitzat la validació de caràcters no admesos en el tema del projecte. |
| Facturació i preus | 2705361 | S'han d'incloure els valors reals de les vendes facturades als camps de seguiment del projecte. |
| Facturació i preus | 2675880 | Eviteu que un projecte s'enllaci amb una línia de contracte que no estigui basada en el treball. |
| Facturació i preus | 2664396 | Si una llista de preus de l'oferta es desa sense cap oferta, ha d'haver-hi un error que indiqui que l'oferta no pot estar buida. |
| Facturació i preus | 2184019 | La pestanya **Facturació basada en tasques** no s'ha de mostrar per als projectes que no tenen cap contracte o oferta de suport. |
| Temps i despesa | 2754459 | Quan el flux de núvol de planificació recurrent està inactiu, mostra el bàner i omet el processament asíncron. |
| Facturació i preus | 2724391 | Es produeix una excepció incorrecta quan falta un valor de client a la regla de facturació per divisió de contractes del projecte. |
| Facturació i preus | 2708638 | El registre no s'ha trobat quan es cercava amb la cerca de quadrícula a Usos de materials i Aprovacions per a Usos de materials.|
| Facturació i preus | 2686977 | Evitar la validació de la línia de factura durant la creació de la factura. |
| Facturació i preus | 2683032 | La còpia de funcions i categories que es poden cobrar no s'escala més enllà dels 5.000 registres.|
| Facturació i preus | 2673363 | El % de consum del cost al Projecte es malmet quan existeixen estimacions d'Esforç i Despesa i els valors reals per a un projecte. |

### <a name="project-management-and-accounting-in-finance"></a>Administració de projectes i comptabilitat al Finance

Per obtenir informació sobre les correccions d'errors incloses en aquesta actualització, inicieu la sessió al Microsoft Dynamics Lifecycle Services (LCS) i vegeu l'[article de la KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438).

## <a name="features-turned-on-by-default-in-upcoming-release"></a>Característiques activades per defecte a la propera versió

A la taula següent s'enumeren les característiques activades per defecte a la versió 10.0.29. La majoria de les característiques activades automàticament es poden desactivar a [Administració de característiques](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview). En endavant, algunes característiques que s'han activat automàticament podrien suprimir-se d'Administració de característiques i passar a ser obligatòries. Aquest canvi garanteix que els clients utilitzin la funcionalitat actual per tal que les millores es puguin afegir a la funcionalitat actual a mida que s'afegeixin. Les característiques no s'habilitaran mai automàticament en menys d'un any, si no es determina que són essencials.

| Nom de la característica | Data d'habilitació | Característica afegida | Estat de la característica | Mòdul |
| --- | --- | --- |--- |--- |
| Habilitar l'ajustament de la transacció d'hores en funció dels canvis en l'assignació de les regles de finançament | 16 de setembre de 2022 | 7 d'octubre de 2020 | Activat per defecte | Administració i comptabilitat de projectes |
| Característica de reversió de la factura de pagament anticipat d'una comanda del projecte | 16 de setembre de 2022 | 6 d'octubre de 2021 | Activat per defecte | Administració i comptabilitat de projectes |
| Eliminar línies de proposta de factura en utilitzar el Project Operations per a escenaris basats en recursos/no mantinguts en existències | 16 de setembre de 2022 | 6 d'octubre de 2021 | Activat per defecte | Administració i comptabilitat de projectes |
| Ajustar la comptabilitat en una transacció de projecte comptabilitzada | 16 de setembre de 2022 | 10 de maig de 2020 | Activat per defecte | Administració i comptabilitat de projectes |
| Habilitar la configuració de la comptabilitat per defecte per al projecte | 16 de setembre de 2022 | 19 de febrer de 2020 | Activat per defecte | Administració i comptabilitat de projectes |
| Habilitar diverses línies de contracte per a un projecte | 16 de setembre de 2022 | 29 de juny de 2020 | Activat per defecte | Administració i comptabilitat de projectes |
| Fer que els llibres diari Hores del projecte siguin només de lectura si l'estat d'aprovació actual no permet l'edició | 16 de setembre de 2022 | 6 d'octubre de 2021 | Activat per defecte | Administració i comptabilitat de projectes |
| Habilitar la sincronització de les línies de vendes des de les línies de compra quan s'actualitzen les línies de compra i el paràmetre d'administració de canvis de comanda de compra està activat | 16 de setembre de 2022 | 7 d'octubre de 2020 | Activat per defecte | Administració i comptabilitat de projectes |
| Habilitar el Project Operations al Dynamics 365 Customer Engagement | 16 de setembre de 2022 | 29 de juny de 2020 | Activat per defecte | Administració i comptabilitat de projectes |
| Característica de correcció de reversió de transaccions del projecte | 16 de setembre de 2022 | 13 de juliol de 2020 | Activat per defecte | Administració i comptabilitat de projectes |

## <a name="features-that-become-mandatory-in-the-upcoming-release"></a>Característiques que passen a ser obligatòries a la propera versió

A la taula següent s'enumeren les característiques que passen a ser obligatòries a partir de la versió 10.0.29.

| Nom de la característica | Data d'habilitació | Característica afegida | Estat de la característica | Mòdul |
| --- | --- | --- | --- | --- |
| Calcular el valor compromès sobre la font de finançament sense arrodonir el tipus de canvi | 16 de setembre de 2022 | 14 de juny de 2020 | Obligatori | Administració i comptabilitat de projectes |
| Habilitar la comptabilització d'ajustaments del projecte amb el mateix compte de llibre de comptabilitat que la transacció original | 16 de setembre de 2022 | 14 de juny de 2020 | Obligatori | Administració i comptabilitat de projectes |
| Detall de l'import compromès del contracte del projecte | 16 de setembre de 2022 | 31 d'agost del 2019 | Obligatori | Administració i comptabilitat de projectes |
| Habilitar l'ordenació per recurs durant la creació de la factura de projecte | 16 de setembre de 2022 | 31 d'agost del 2019 | Obligatori | Administració i comptabilitat de projectes |
