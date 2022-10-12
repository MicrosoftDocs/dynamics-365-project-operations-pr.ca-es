---
title: 'Novetats de setembre de 2022: Project Operations per a escenaris basats en recursos/no mantinguts en existències'
description: Aquest article proporciona informació sobre les actualitzacions de qualitat disponibles a la versió de setembre de 2022 de Microsoft Dynamics 365 Project Operations per a escenaris basats en recursos o no emmagatzemats.
author: ramagadu
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: ef8b4dd98d64dac1e2420f8e6a104258f126f112
ms.sourcegitcommit: a2d720ac6d7ddb20a0967fe87992a376b2478208
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/04/2022
ms.locfileid: "9621322"
---
# <a name="whats-new-september-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novetats de setembre de 2022: Project Operations per a escenaris basats en recursos/no mantinguts en existències

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

Aquest article s'aplica als components i versions de Microsoft Dynamics 365 Project Operations següents:

- Project Operations en una Dataverse versió d'entorn 4.46.0.60
- Administració i comptabilitat de projectes en un entorn Dynamics 365 Finance versió 10.0.29

## <a name="features-included-in-this-release"></a>Característiques incloses en aquesta versió

| Àrea de característiques | Nom de la característica | Més informació |
| --- | --- | --- |
| Administració d'oportunitats | **Revisió i activació de pressupostos**<br>Project Operations aporta tot el suport del procés de venda. Les cotitzacions del projecte es poden activar per representar un estat on l'oferta és només de lectura i s'està revisant. Les cotitzacions activades es poden revisar per crear noves ofertes que tinguin un número de revisió incrementat. Les ofertes de projecte activades o les revisions de pressupostos es poden tancar com a guanyades o perdudes. | [Activar i revisar una oferta de projecte](/dynamics365/project-operations/sales/activation-and-revision) |
| Facturació i preus | **Impagament de preus agnòstics de zona horària**<br>Project Operations ha introduït el concepte de data agnòstica de zona horària en tots els reals del projecte. Un camp nou, **Data de transacció**, ja està disponible a les línies de diari i als reals, i s'utilitzarà per emmagatzemar la data en què es va produir la transacció, però sense convertir aquesta data a hora universal coordinada. Aquesta data s'utilitzarà per a processos aigües avall, com ara l'impagament de preus i la creació de factures. | <p>[Determineu les taxes de cost per a estimacions i reals basades en projectes](/dynamics365/project-operations/pricing-costing/cost-price-resolution)</p><p>[Determinar els preus de venda de les estimacions i els reals basats en projectes](/dynamics365/project-operations/pricing-costing/sales-price-resolution)</p> |
| Facturació i preus | **Substitució de preus data-efectiva a Project Operations**<br>Les substitucions de preus efectives amb data proporcionen una manera d'anul·lar o canviar preus específics de la llista de preus. | [El preu efectiu de la data substitueix](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Subcontractació | **Conciliació de factures de subcontractació i proveïdors**<br>Aquesta característica permet als clients crear subcontractes per comprar temps de recursos, categories de despeses i materials que s'utilitzen per al treball per projectes. També permet als clients registrar, en aplicacions de finances i operacions, factures de proveïdors que estaran disponibles per als gestors de projectes per a la Dataverse seva verificació. | <p>[Gestió de subcontractes](/dynamics365/project-operations/pro/subcontracting/managing-subcontracts-overview)</p><p>[Crea factures del proveïdor](/dynamics365/project-operations/procurement/vendor-invoicing-concept-and-creation)</p> |
| Temps i despesa | **Aprovador global**<br>Aquesta característica permet un proveïdor de programari independent (ISV) i una aprovació centralitzada, independentment de l'estatus del projecte o membre de l'equip del projecte. | [Seguretat i aprovacions](/dynamics365/project-operations/approvals/approvals-security) |
| Administració de despeses | **Possibilitat de publicar la responsabilitat de despeses en la moneda del proveïdor**<br>Aquesta funció permet publicar informes de despeses en una moneda de proveïdor per a la forma de pagament en efectiu. | [Possibilitat de publicar la responsabilitat de despeses en la moneda del proveïdor](/dynamics365/project-operations/expense/posting-expense-reports#enable-the-ability-to-post-expense-liability-in-vendor-currency-for-cash-payment-method-feature) |
| Contractació de projectes | **Pagar quan es paguin pagaments al proveïdor**<br>Aquesta característica permet utilitzar la funció Pay when paid (PWP) amb entorns que no són d'estoc del Project Operations. Permet bloquejar / retenir els pagaments del proveïdor, en funció dels terminis de retenció, fins que es rebi el pagament del client. | [Pagar quan es paguin pagaments al proveïdor](/dynamics365/project-operations/procurement/pay-when-paid) |
| Contractació de projectes | **Sol·licituds de compra de projectes**<br>Aquesta característica permet als usuaris crear ordres de compra relacionades amb el projecte en entitats jurídiques on el Project Operations on Dynamics 365 Customer Engagement integració està habilitada. Les ordres de compra del projecte es poden utilitzar per registrar la contractació de material no emmagatzemat contra el projecte per part del departament de Contractació persona. Les ordres de compra del projecte no se sincronitzaran amb Dataverse. Tanmateix, podeu utilitzar una entitat virtual per mostrar línies de comandes de compra de projectes per obtenir Dataverse informació sobre el gestor de projectes. El cost de la factura del proveïdor relacionat amb el projecte s'integra amb l'entitat Project Actuals a Dataverse. El cost del projecte es registra al subledger Del projecte mitjançant el diari Project Operations Integration. | |

## <a name="project-operations-dual-write-maps-updates"></a>Actualitzacions de les assignacions de doble ecriptura del Project Operations

La taula següent mostra els mapes de doble escriptura que s'han modificat o afegit a la versió de setembre de 2022 d'Operacions del projecte.

| Assignació d'entitats | Versió actualitzada | Comentaris |
| -------------- | ------------------- | ------------|
| Valors reals d'integració del Project Operations (msdyn_actuals) | 1.0.0.15 | Aquest mapa dóna suport al processament de reals de subcontractació amb Project Operations per a escenaris basats en recursos. |
| Entitat d'exportació de factura del proveïdor del projecte de la integració del Project Operations (msdyn_projectvendorinvoices) | 1.0.0.2 | Aquest mapa dóna suport al processament de reals de subcontractació amb Project Operations per a escenaris basats en recursos. |
| Entitat d'exportació de la línia de factura del proveïdor del projecte de la integració del Project Operations (msdyn_projectvendorinvoicelines) | 1.0.0.5 | Aquest mapa dóna suport al processament de reals de subcontractació amb Project Operations per a escenaris basats en recursos. |

Executeu sempre la versió més recent del mapa al vostre entorn i activeu tots els mapes de taula relacionats a mesura que actualitzeu la versió de la solució Project Operations Dataverse i la versió de la solució Finance. És possible que algunes funcions i capacitats no funcionin correctament si la versió més recent del mapa no està activada. Podeu visualitzar la versió activa de l'assignació a la columna **Versió** de la pàgina **Escriptura doble**. Per activar una versió nova de l'assignació, seleccioneu **Versions de l'assignació de la taula**, seleccioneu la versió més recent i després deseu la versió seleccionada. Si heu personalitzat un mapa de taula estàndard, torneu a aplicar els canvis. Per a més informació, vegeu [Administració del cicle de vida de les aplicacions](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Si trobeu un problema en iniciar el mapa, seguiu les instruccions del problema Falten columnes de taula a la [secció mapes](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) de la guia de resolució de problemes de doble escriptura.

## <a name="quality-updates"></a>Actualitzacions de qualitat

### <a name="project-operations-on-dataverse"></a>Project Operations a Dataverse

| Àrea de característiques | Número de referència | Actualització de qualitat |
| --- | --- | --- |
| Facturació i preus | 2754422 | Les estimacions de material i despeses no flueixen a Finances quan els projectes es copien en Dataverse. |
| Temps i despesa | 2787409 | Un aprovador no vàlid pot aprovar una entrada de temps no prevista per al projecte. |
| Administració d'oportunitats | 2788907 | Missatge d'error actualitzat sobre validació de la unicitat per a línies de comanda que inclouen banderes. |
| Temps i despesa | 2842253 | Nul·la tramitació d'excepcions per a l'aprovació del temps. |
| Facturació i preus | 2844181 | El fet de no obtenir l'identificador de correlació bloqueja la creació de factures. |
| Facturació i preus | 2876628 | QLD, CLD - La resolució de la llista de preus d'estimació ha d'utilitzar camps d'interval de dates heretats de la llista de preus. |
| Subcontractació | 2893222 | Si no s'especifica cap rol per a una línia de subcontractació, hauria de ser possible seleccionar aquesta línia en un membre de l'equip per a qualsevol funció. |

### <a name="project-management-and-accounting-in-finance"></a>Administració i comptabilitat de projectes en finances

Per obtenir informació sobre les correccions d'errors que s'inclouen en aquesta actualització, inicieu la sessió a Microsoft Dynamics Lifecycle Services i visualitzeu l'article [de la](https://fix.lcs.dynamics.com/Issue/Details?bugId=726559) KB.

## <a name="features-turned-on-by-default-in-upcoming-release"></a>Funcions activades de manera predeterminada en la propera versió

La taula següent mostra les característiques que estan activades per defecte a la versió 10.0.30. La majoria de funcions que s'han activat automàticament es poden desactivar a l'Administració [de](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview) funcions. En el futur, és possible que algunes funcions que s'hagin activat automàticament s'eliminin de la gestió de funcions i esdevinguin obligatòries. Aquest canvi garanteix que els clients utilitzin la funcionalitat actual, de manera que les millores es puguin basar en la funcionalitat actual a mesura que s'afegeixen. Les funcions mai s'activaran automàticament en menys d'un any, tret que es determini que són imprescindibles.

| Nom de la característica | Activa la data | Característica afegida | Estat de la característica | Mòdul |
| --- | --- | --- |--- |--- |
| Habilitar l'operació async quan l'usuari ha de canviar entre operacions de sincronització i async | 21 d'octubre de 2022 | 9 d'abril de 2021 | Activat per defecte | Administració de despeses |
| Avaluació de la política de despeses dels rebuts requerits | 21 d'octubre de 2022 | 20 de desembre de 2021 | Activat per defecte | Administració de despeses |
| Llistat vista d'informes de despeses elaborats per treballadors delegats | 21 d'octubre de 2022 | 19 de febrer de 2020 | Activat per defecte | Administració de despeses |
| Càlcul de totals de quilometratge per exercici fiscal | 21 d'octubre de 2022 | 10 de maig de 2022 | Activat per defecte | Administració de despeses |
