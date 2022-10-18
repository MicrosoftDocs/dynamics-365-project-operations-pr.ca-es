---
title: 'Novetats de setembre de 2022: implementació bàsica del Project Operations'
description: Aquest article proporciona informació sobre les actualitzacions de qualitat disponibles a la versió de setembre de 2022 de la implementació del Microsoft Dynamics 365 Project Operations lite.
author: ramagadu
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: a02ac7a69489bc7974eb0e63c11fa5de74795b78
ms.sourcegitcommit: b3a70bc4f2850cff5c2b7114cff7bd61ec298143
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/06/2022
ms.locfileid: "9634840"
---
# <a name="whats-new-september-2022---project-operations-lite-deployment"></a>Novetats de setembre de 2022: implementació bàsica del Project Operations

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_

Aquest article s'aplica als components i versions de Microsoft Dynamics 365 Project Operations següents:

- Project Operations en una Dataverse versió d'entorn 4.46.0.60

## <a name="features-included-in-this-release"></a>Característiques incloses en aquesta versió

| Àrea de característiques | Nom de la característica | Més informació |
| --- | --- | --- |
| Administració d'oportunitats | **Revisió i activació de pressupostos**<br>Project Operations aporta tot el suport del procés de venda. Les cotitzacions del projecte es poden activar per representar un estat on l'oferta és només de lectura i s'està revisant. Les cotitzacions activades es poden revisar per crear noves ofertes que tinguin un número de revisió incrementat. Les ofertes de projecte activades o les revisions de pressupostos es poden tancar com a guanyades o perdudes. | [Activar i revisar una oferta de projecte](/dynamics365/project-operations/sales/activation-and-revision) |
| Facturació i preus | **Impagament de preus agnòstics de zona horària**<br>Project Operations ha introduït el concepte de data agnòstica de zona horària en tots els reals del projecte. Un camp nou, **Data de transacció**, ja està disponible a les línies de diari i als reals, i s'utilitzarà per emmagatzemar la data en què es va produir la transacció, però sense convertir aquesta data a hora universal coordinada. Aquesta data s'utilitzarà per a processos aigües avall, com ara l'impagament de preus i la creació de factures. | <p>[Determineu les taxes de cost per a estimacions i reals basades en projectes](/dynamics365/project-operations/pro/pricing-costing/cost-price-resolution-sales)</p><p>[Determinar els preus de venda de les estimacions i els reals basats en projectes](/dynamics365/project-operations/pro/pricing-costing/sales-price-resolution-sales)</p> |
| Facturació i preus | **Substitució de preus data-efectiva a Project Operations**<br>Les substitucions de preus efectives amb data proporcionen una manera d'anul·lar o canviar preus específics de la llista de preus. | [El preu efectiu de la data substitueix](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Temps i despesa | **Aprovador global**<br>Aquesta característica permet un proveïdor de programari independent (ISV) i una aprovació centralitzada, independentment de l'estatus del projecte o membre de l'equip del projecte. | [Seguretat i aprovacions](/dynamics365/project-operations/approvals/approvals-security) |
|Planificació i seguiment de projectes|**Utilitzar les API de planificació de projectes per fer operacions amb entitats de planificació** </br> </br>L'API d'edició de contorn d'assignació de recursos permet als desenvolupadors especificar programàticament l'esforç d'un cessionari de tasques en qualsevol interval de dates admès per a una planificació d'esforç per fases de temps més granular.|[Utilitzar les API de planificació de projectes per fer operacions amb entitats de planificació](/dynamics365/project-operations/project-management/schedule-api-preview)|

## <a name="quality-updates"></a>Actualitzacions de qualitat

| Àrea de característiques | Número de referència | Actualització de qualitat |
| --- | --- | --- |
| Facturació i preus | 2754422 | Les estimacions de materials i despeses no flueixen a Dynamics 365 Finance quan es copien els projectes a Dataverse. |
| Temps i despesa | 2787409 | Un aprovador no vàlid pot aprovar una entrada de temps no prevista per al projecte. |
| Administració d'oportunitats | 2788907 | Missatge d'error actualitzat sobre validació de la unicitat per a línies de comanda que inclouen banderes. |
| Temps i despesa | 2842253 | Nul·la tramitació d'excepcions per a l'aprovació del temps. |
| Facturació i preus | 2844181 | El fet de no obtenir l'identificador de correlació bloqueja la creació de factures. |
| Facturació i preus | 2876628 | QLD, CLD - La resolució de la llista de preus d'estimació ha d'utilitzar camps d'interval de dates heretats de la llista de preus. |
| Subcontractació | 2893222 | Si no s'especifica cap rol per a una línia de subcontractació, hauria de ser possible seleccionar aquesta línia en un membre de l'equip per a qualsevol funció. |
