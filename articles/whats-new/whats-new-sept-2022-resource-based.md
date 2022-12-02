---
title: 'Novetats de setembre de 2022: Project Operations per a escenaris basats en recursos/no mantinguts en existències'
description: Aquest article proporciona informació sobre les actualitzacions de qualitat que estan disponibles a la versió de setembre de 2022 del Microsoft Dynamics 365 Project Operations per a escenaris basats en recursos/no mantinguts en existències.
author: ramagadu
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 04b5f2f8223cdc80028860dd880dde314be244eb
ms.sourcegitcommit: b3a70bc4f2850cff5c2b7114cff7bd61ec298143
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/06/2022
ms.locfileid: "9634793"
---
# <a name="whats-new-september-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novetats de setembre de 2022: Project Operations per a escenaris basats en recursos/no mantinguts en existències

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

Aquest article s'aplica als components i les versions següents del Microsoft Dynamics 365 Project Operations:

- Project Operations en un entorn del Dataverse, versió 4.46.0.60
- Administració de projectes i comptabilitat en un entorn del Dynamics 365 Finance, versió 10.0.29

## <a name="features-included-in-this-release"></a>Característiques incloses en aquesta versió

| Àrea de característiques | Nom de la característica | Més informació |
| --- | --- | --- |
| Administració d'oportunitats | **Revisió i activació d'ofertes**<br>El Project Operations dona suport complet per al procés de venda. Les ofertes del projecte es poden activar per representar un estat en què l'oferta és només de lectura i s'està revisant. Les ofertes activades es poden revisar per crear ofertes noves que tenen un número de revisió incrementat. Les ofertes del projecte o revisions d'ofertes activades es poden tancar com a guanyades o perdudes. | [Activar i revisar una oferta de projecte](/dynamics365/project-operations/sales/activation-and-revision) |
| Facturació i preus | **Valor per defecte de preu independent del fus horari**<br>El Project Operations ha introduït el concepte de data independent del fus horari a tots els valors reals del projecte. Ara hi ha disponible un camp nou, **Data de la transacció** a les línies del llibre diari i els valors reals, que s'utilitzarà per emmagatzemar la data en què s'ha produït la transacció, però sense convertir aquesta data a temps universal coordinat. Aquesta data s'utilitzarà per als processos posteriors, com ara la creació de factures i els preus per defecte. | <p>[Determinar els percentatges de cost de les estimacions i els valors reals basats en el projecte](/dynamics365/project-operations/pricing-costing/cost-price-resolution)</p><p>[Determinar els preus de venda per a les estimacions i els valors reals basats en el projecte](/dynamics365/project-operations/pricing-costing/sales-price-resolution)</p> |
| Facturació i preus | **Substitucions de preus de data de vigència al Project Operations**<br>Les substitucions de preus de data de vigència proporcionen una manera de substituir o canviar preus específics de la llista de preus. | [Substitucions de preus de data de vigència](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Subcontractació | **Subcontractació i reconciliació de factura de proveïdor**<br>Aquesta característica permet als clients crear subcontractes per adquirir temps de recursos, categories de despeses i materials que s'utilitzen per al treball del projecte. També permet als clients registrar, a les aplicacions de finances i operacions, factures de proveïdor que estaran disponibles per als gestors de projecte al Dataverse per a la verificació. | <p>[Administració de subcontractes](/dynamics365/project-operations/pro/subcontracting/managing-subcontracts-overview)</p><p>[Crea factures del proveïdor](/dynamics365/project-operations/procurement/vendor-invoicing-concept-and-creation)</p> |
| Temps i despesa | **Aprovador global**<br>Aquesta característica permet els proveïdors de programari independents (ISV) i l'aprovació centralitzada, independentment de l'estat del membre del projecte o de l'equip del projecte. | [Seguretat i aprovacions](/dynamics365/project-operations/approvals/approvals-security) |
| Administració de despeses | **Capacitat de comptabilitzar la responsabilitat de despeses en la moneda del proveïdor**<br>Aquesta característica permet comptabilitzar els informes de despeses en la moneda del proveïdor per al mètode de pagament en efectiu. | [Capacitat de comptabilitzar la responsabilitat de despeses en la moneda del proveïdor](/dynamics365/project-operations/expense/posting-expense-reports#enable-the-ability-to-post-expense-liability-in-vendor-currency-for-cash-payment-method-feature) |
| Procés de proveïment | **Pagaments de proveïdors després del cobrament**<br>Aquesta característica permet utilitzar la característica Pagament després del cobrament (PWP) amb entorns que no són d'existències del Project Operations. Permet bloquejar o retenir pagaments de proveïdor a partir de les condicions de retenció fins que es rep el pagament del client. | [Pagaments de proveïdors després del cobrament](/dynamics365/project-operations/procurement/pay-when-paid) |
| Procés de proveïment | **Peticions de comandes de compra**<br>Aquesta característica permet als usuaris crear ordres de compra relacionades amb el projecte en entitats jurídiques en les quals s'ha habilitat la integració del Project Operations al Dynamics 365 Customer Engagement. Les comandes de compra de projectes es poden utilitzar per registrar el proveïment de material sense existències al projecte per part del personal del departament de proveïment. Les comandes de compra de projectes no se sincronitzaran amb el Dataverse. Tanmateix, podeu utilitzar una entitat virtual per tal de visualitzar les línies d'ordre de compra del projecte al Dataverse com a informació per a l'administrador del projecte. El cost de la factura del proveïdor relacionat amb el projecte s'integra amb l'entitat Valors reals del projecte al Dataverse. El cost del projecte es registra en el subllibre del projecte mitjançant el diari d'integració del Project Operations. | |
|Planificació i seguiment de projectes|**Utilitzar les API de planificació de projectes per fer operacions amb entitats de planificació** </br> </br>L'API de contorn d'assignació de recursos permet que els desenvolupadors especifiquin mitjançant programació l'esforç d'una persona assignada a la tasca en qualsevol interval de dates admès per a una planificació de l'esforç més granular.|[Utilitzar les API de planificació de projectes per fer operacions amb entitats de planificació](/dynamics365/project-operations/project-management/schedule-api-preview)|

## <a name="project-operations-dual-write-maps-updates"></a>Actualitzacions de les assignacions de doble ecriptura del Project Operations

A la taula següent es mostren les assignacions de doble escriptura que s'han modificat o afegit a la versió de setembre de 2022 del Project Operations.

| Assignació d'entitats | Versió actualitzada | Comentaris |
| -------------- | ------------------- | ------------|
| Valors reals d'integració del Project Operations (msdyn_actuals) | 1.0.0.15 | Aquesta assignació admet el processament de valors reals de subcontracte amb el Project Operations per a escenaris basats en recursos. |
| Entitat d'exportació de factura del proveïdor del projecte de la integració del Project Operations (msdyn_projectvendorinvoices) | 1.0.0.2 | Aquesta assignació admet el processament de valors reals de subcontracte amb el Project Operations per a escenaris basats en recursos. |
| Entitat d'exportació de la línia de factura del proveïdor del projecte de la integració del Project Operations (msdyn_projectvendorinvoicelines) | 1.0.0.5 | Aquesta assignació admet el processament de valors reals de subcontracte amb el Project Operations per a escenaris basats en recursos. |

Executeu sempre la versió més recent de l'assignació a l'entorn i habiliteu totes les assignacions de taules relacionades a mida que actualitzeu la versió de la solució del Finance i del Dataverse del Project Operations. És possible que algunes característiques i capacitats no funcionin correctament si la versió més recent del mapa no s'activa. Podeu visualitzar la versió activa de l'assignació a la columna **Versió** de la pàgina **Escriptura doble**. Per activar una versió nova de l'assignació, seleccioneu **Versions de l'assignació de la taula**, seleccioneu la versió més recent i després deseu la versió seleccionada. Si heu personalitzat una assignació de taules llesta per al seu ús, torneu a aplicar els canvis. Per a més informació, vegeu [Administració del cicle de vida de les aplicacions](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Si teniu qualsevol problema quan inicieu l'assignació, seguiu les instruccions de la secció [Problemes de columnes de la taula que falten](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) de la guia de detecció d'errors de doble escriptura.

## <a name="quality-updates"></a>Actualitzacions de qualitat

### <a name="project-operations-on-dataverse"></a>Project Operations a Dataverse

| Àrea de característiques | Número de referència | Actualització de qualitat |
| --- | --- | --- |
| Facturació i preus | 2754422 | Les estimacions de material i de despeses no flueixen a Finance quan es copien els projectes al Dataverse'. |
| Temps i despesa | 2787409 | Un aprovador no vàlid pot aprovar una entrada de temps que no sigui de projecte. |
| Administració d'oportunitats | 2788907 | S'ha actualitzat el missatge d'error en la validació de la unicitat de les línies de comanda que inclouen indicadors. |
| Temps i despesa | 2842253 | Gestió d'excepcions nul·les per a la aprovació de temps. |
| Facturació i preus | 2844181 | Error en obtenir l'ID de correlació que bloqueja la creació de factures. |
| Facturació i preus | 2876628 | QLD, CLD: la resolució de la llista de preus estimats ha d'utilitzar els camps d'interval de dates heretats de la llista de preus. |
| Subcontractació | 2893222 | Si no s'especifica cap funció per a una línia de subcontracte, hauria de ser possible seleccionar aquesta línia en un membre de l'equip per a qualsevol funció. |

### <a name="project-management-and-accounting-in-finance"></a>Administració de projectes i comptabilitat al Finance

Per obtenir informació sobre les correccions d'errors incloses en aquesta actualització, inicieu la sessió al Microsoft Dynamics Lifecycle Services i vegeu l'[article de la KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=726559).

## <a name="features-turned-on-by-default-in-upcoming-release"></a>Característiques activades per defecte a la propera versió

A la taula següent s'enumeren les característiques activades per defecte a la versió 10.0.30. La majoria de les característiques activades automàticament es poden desactivar a [Administració de característiques](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview). En endavant, algunes característiques que s'han activat automàticament podrien suprimir-se d'Administració de característiques i passar a ser obligatòries. Aquest canvi garanteix que els clients utilitzin la funcionalitat actual per tal que les millores es puguin afegir a la funcionalitat actual a mida que s'afegeixin. Les característiques no s'habilitaran mai automàticament en menys d'un any, si no es determina que són essencials.

| Nom de la característica | Data d'habilitació | Característica afegida | Estat de la característica | Mòdul |
| --- | --- | --- |--- |--- |
| Habilita l'operació asíncrona quan l'usuari ha de canviar entre les operacions síncrona i asíncrona | 21 d'octubre de 2022 | 9 d'abril de 2021 | Activat per defecte | Administració de despeses |
| Avaluació de la norma de despeses per a rebuts necessària | 21 d'octubre de 2022 | 20 de desembre de 2021 | Activat per defecte | Administració de despeses |
| Visualització de llista dels informes de despeses creats delegant treballadors | 21 d'octubre de 2022 | 19 de febrer de 2020 | Activat per defecte | Administració de despeses |
| Càlcul de totals de quilometratge per exercici fiscal | 21 d'octubre de 2022 | 10 de maig de 2022 | Activat per defecte | Administració de despeses |
