---
title: 'Novetats de setembre de 2022: implementació bàsica del Project Operations'
description: En aquest article es proporciona informació sobre les actualitzacions de qualitat que estan disponibles a la versió de setembre de 2022 de la implementació bàsica del Microsoft Dynamics 365 Project Operations.
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

Aquest article s'aplica als components i les versions següents del Microsoft Dynamics 365 Project Operations:

- Project Operations en un entorn del Dataverse, versió 4.46.0.60

## <a name="features-included-in-this-release"></a>Característiques incloses en aquesta versió

| Àrea de característiques | Nom de la característica | Més informació |
| --- | --- | --- |
| Administració d'oportunitats | **Revisió i activació d'ofertes**<br>El Project Operations dona suport complet per al procés de venda. Les ofertes del projecte es poden activar per representar un estat en què l'oferta és només de lectura i s'està revisant. Les ofertes activades es poden revisar per crear ofertes noves que tenen un número de revisió incrementat. Les ofertes del projecte o revisions d'ofertes activades es poden tancar com a guanyades o perdudes. | [Activar i revisar una oferta de projecte](/dynamics365/project-operations/sales/activation-and-revision) |
| Facturació i preus | **Valor per defecte de preu independent del fus horari**<br>El Project Operations ha introduït el concepte de data independent del fus horari a tots els valors reals del projecte. Ara hi ha disponible un camp nou, **Data de la transacció** a les línies del llibre diari i els valors reals, que s'utilitzarà per emmagatzemar la data en què s'ha produït la transacció, però sense convertir aquesta data a temps universal coordinat. Aquesta data s'utilitzarà per als processos posteriors, com ara la creació de factures i els preus per defecte. | <p>[Determinar els percentatges de cost de les estimacions i els valors reals basats en el projecte](/dynamics365/project-operations/pro/pricing-costing/cost-price-resolution-sales)</p><p>[Determinar els preus de venda per a les estimacions i els valors reals basats en el projecte](/dynamics365/project-operations/pro/pricing-costing/sales-price-resolution-sales)</p> |
| Facturació i preus | **Substitucions de preus de data de vigència al Project Operations**<br>Les substitucions de preus de data de vigència proporcionen una manera de substituir o canviar preus específics de la llista de preus. | [Substitucions de preus de data de vigència](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Temps i despesa | **Aprovador global**<br>Aquesta característica permet els proveïdors de programari independents (ISV) i l'aprovació centralitzada, independentment de l'estat del membre del projecte o de l'equip del projecte. | [Seguretat i aprovacions](/dynamics365/project-operations/approvals/approvals-security) |
|Planificació i seguiment de projectes|**Utilitzar les API de planificació de projectes per fer operacions amb entitats de planificació** </br> </br>L'API de contorn d'assignació de recursos permet que els desenvolupadors especifiquin mitjançant programació l'esforç d'una persona assignada a la tasca en qualsevol interval de dates admès per a una planificació de l'esforç més granular.|[Utilitzar les API de planificació de projectes per fer operacions amb entitats de planificació](/dynamics365/project-operations/project-management/schedule-api-preview)|

## <a name="quality-updates"></a>Actualitzacions de qualitat

| Àrea de característiques | Número de referència | Actualització de qualitat |
| --- | --- | --- |
| Facturació i preus | 2754422 | Les estimacions de material i de despeses no flueixen al Dynamics 365 Finance quan es copien els projectes al Dataverse'. |
| Temps i despesa | 2787409 | Un aprovador no vàlid pot aprovar una entrada de temps que no sigui de projecte. |
| Administració d'oportunitats | 2788907 | S'ha actualitzat el missatge d'error en la validació de la unicitat de les línies de comanda que inclouen indicadors. |
| Temps i despesa | 2842253 | Gestió d'excepcions nul·les per a la aprovació de temps. |
| Facturació i preus | 2844181 | Error en obtenir l'ID de correlació que bloqueja la creació de factures. |
| Facturació i preus | 2876628 | QLD, CLD: la resolució de la llista de preus estimats ha d'utilitzar els camps d'interval de dates heretats de la llista de preus. |
| Subcontractació | 2893222 | Si no s'especifica cap funció per a una línia de subcontracte, hauria de ser possible seleccionar aquesta línia en un membre de l'equip per a qualsevol funció. |
