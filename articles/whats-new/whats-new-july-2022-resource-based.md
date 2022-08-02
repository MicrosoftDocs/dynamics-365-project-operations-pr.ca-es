---
title: 'Novetats de juliol de 2022: Project Operations per a escenaris basats en recursos/no mantinguts en existències'
description: Aquest article proporciona informació sobre les actualitzacions de qualitat disponibles a la versió de juliol de 2022 de Microsoft Dynamics 365 Project Operations per a escenaris basats en recursos o no emmagatzemats.
author: ramagadu
ms.date: 07/19/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: cbee9281d2fae485a3ebcd38bb884a2b2322f8d1
ms.sourcegitcommit: 66e376675e6df8efc86fa84ec24e9aad6a980304
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 07/21/2022
ms.locfileid: "9183874"
---
# <a name="whats-new-july-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novetats de juliol de 2022: Project Operations per a escenaris basats en recursos/no mantinguts en existències

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

Aquest article s'aplica als components i versions de Microsoft Dynamics 365 Project Operations següents:

- Project Operations en una Dataverse versió d'entorn 4.44.0.22
- Administració i comptabilitat de projectes en un entorn Dynamics 365 Finance versió 10.0.28

## <a name="project-operations-dual-write-maps-updates"></a>Actualitzacions de les assignacions de doble ecriptura del Project Operations

En aquesta versió no hi ha actualitzacions per a les assignacions d'escriptura doble del Project Operations. Per a una llista actual i versions de les assignacions d'escriptura doble del Project Operations, consulteu [Versions de les assignacions d'escriptura doble del Project Operations](../environment/resource-dual-write-maps.md).

Executeu sempre la versió més recent del mapa al vostre entorn i activeu tots els mapes de taula relacionats a mesura que actualitzeu la versió de la solució Project Operations Dataverse i la versió de la solució Finance. És possible que algunes funcions i capacitats no funcionin correctament si la versió més recent del mapa no està activada. Podeu visualitzar la versió activa de l'assignació a la columna **Versió** de la pàgina **Escriptura doble**. Per activar una versió nova de l'assignació, seleccioneu **Versions de l'assignació de la taula**, seleccioneu la versió més recent i després deseu la versió seleccionada. Si heu personalitzat un mapa de taula estàndard, torneu a aplicar els canvis. Per a més informació, vegeu [Administració del cicle de vida de les aplicacions](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Si trobeu un problema en iniciar el mapa, seguiu les instruccions del problema Falten columnes de taula a la [secció mapes](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) de la guia de resolució de problemes de doble escriptura.

## <a name="quality-updates"></a>Actualitzacions de qualitat

### <a name="project-operations-on-dataverse"></a>Project Operations a Dataverse

| Àrea de característiques | Número de referència | Actualització de qualitat |
| --- | --- | --- |
| Implementació i configuració | 2761472 | Es gestiona un error d'instal·lació del Project Operations. |
| Facturació i preus | 2746940 | El nom de la línia subcontractada ha de tenir una longitud màxima de 100 caràcters. |
| Facturació i preus | 2739162 | Els clients han de poder veure els botons de la cinta a la vista de quadrícula real. |
| Planificació i seguiment de projectes | 2730318 | Validació actualitzada per a caràcters no admesos en l'assignatura del projecte. |
| Facturació i preus | 2705361 | Els reals de vendes facturats per fites s'han d'incloure als camps de seguiment del projecte. |
| Facturació i preus | 2675880 | Eviteu que un projecte estigui vinculat a una línia de contracte que no estigui basada en la feina. |
| Facturació i preus | 2664396 | Si es desa una llista de preus d'un pressupost sense pressupost, hi ha d'haver un error que indiqui que l'oferta no es pot buidar. |
| Facturació i preus | 2184019 | La **pestanya Facturació** basada en tasques no s'ha de mostrar per als projectes que no tenen cap contracte ni pressupost de suport. |

### <a name="project-management-and-accounting-in-finance"></a>Administració i comptabilitat de projectes en finances

Per obtenir informació sobre les correccions d'errors que s'inclouen en aquesta actualització, inicieu la sessió a Microsoft Dynamics Lifecycle Services (LCS) i visualitzeu l'article de la [KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438).

## <a name="features-turned-on-by-default-in-upcoming-release"></a>Funcions activades de manera predeterminada en la propera versió

La taula següent mostra les característiques que estan activades per defecte a la versió 10.0.29. La majoria de funcions que s'han activat automàticament es poden desactivar a l'Administració [de funcions](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview). En el futur, és possible que algunes funcions que s'hagin activat automàticament s'eliminin de la gestió de funcions i esdevinguin obligatòries. Aquest canvi garanteix que els clients utilitzin la funcionalitat actual, de manera que les millores es puguin basar en la funcionalitat actual a mesura que s'afegeixen. Les funcions mai s'activaran automàticament en menys d'un any, tret que es determini que són imprescindibles.

| Nom de la característica | Activa la data | Característica afegida | Estat de les característiques | Mòdul |
| --- | --- | --- |--- |--- |
| Permetre l'ajust de la transacció horària en funció del canvi en l'assignació de regles de finançament | 16 de setembre de 2022 | 7 d'octubre de 2020 | Activat per defecte | Administració i comptabilitat de projectes |
| Funció de reversió de factures de prepagament de l'ordre de compra del projecte | 16 de setembre de 2022 | 6 d'octubre de 2021 | Activat per defecte | Administració i comptabilitat de projectes |
| Suprimir línies de proposta de factura quan utilitzeu Project Operations per a escenaris basats en recursos o no emmagatzemats | 16 de setembre de 2022 | 6 d'octubre de 2021 | Activat per defecte | Administració i comptabilitat de projectes |
| Ajusteu la comptabilitat en una transacció de projecte comptabilitzada | 16 de setembre de 2022 | 10 de maig de 2020 | Activat per defecte | Administració i comptabilitat de projectes |
| Habilitar la configuració de comptabilitat per defecte per al projecte | 16 de setembre de 2022 | 19 de febrer de 2020 | Activat per defecte | Administració i comptabilitat de projectes |
| Habilitar diverses línies de contracte per a un projecte | 16 de setembre de 2022 | 29 de juny de 2020 | Activat per defecte | Administració i comptabilitat de projectes |
| Fer que les revistes del Project Hour siguin només de lectura si l'estat d'aprovació actual no permet l'edició | 16 de setembre de 2022 | 6 d'octubre de 2021 | Activat per defecte | Administració i comptabilitat de projectes |
| Habiliteu la sincronització de les línies de vendes de les línies de compra quan s'actualitzin les línies de compra i s'activi el paràmetre de gestió del canvi de comanda de compra | 16 de setembre de 2022 | 7 d'octubre de 2020 | Activat per defecte | Administració i comptabilitat de projectes |
| Habiliteu les operacions del Projecte a Dynamics 365 Customer Engagement | 16 de setembre de 2022 | 29 de juny de 2020 | Activat per defecte | Administració i comptabilitat de projectes |
| Funció de correcció de reversió de transaccions del projecte | 16 de setembre de 2022 | 13 de juliol de 2020 | Activat per defecte | Administració i comptabilitat de projectes |

## <a name="features-that-become-mandatory-in-the-upcoming-release"></a>Característiques que esdevenen obligatòries en la propera versió

La taula següent enumera les característiques que són obligatòries a partir de la versió 10.0.29.

| Nom de la característica | Activa la data | Característica afegida | Estat de les característiques | Mòdul |
| --- | --- | --- | --- | --- |
| Calcular el valor compromès sobre la font de finançament sense arrodonir el tipus de canvi | 16 de setembre de 2022 | 14 de juny de 2020 | Obligatori | Administració i comptabilitat de projectes |
| Habiliteu la publicació d'ajustos del projecte amb el mateix compte comptable que la transacció original | 16 de setembre de 2022 | 14 de juny de 2020 | Obligatori | Administració i comptabilitat de projectes |
| Detall de l'import compromès del contracte del projecte | 16 de setembre de 2022 | 31 d'agost del 2019 | Obligatori | Administració i comptabilitat de projectes |
| Habilitar l'ordenació per recurs durant la creació de propostes de factura del projecte | 16 de setembre de 2022 | 31 d'agost del 2019 | Obligatori | Administració i comptabilitat de projectes |
