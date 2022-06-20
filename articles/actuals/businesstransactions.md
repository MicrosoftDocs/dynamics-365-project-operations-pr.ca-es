---
title: Transaccions empresarials al Project Operations
description: En aquest article s'ofereix una visió general del concepte de transaccions comercials a Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 01/31/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2022-01-31
ms.openlocfilehash: fab0061af6e615c25d0fbf79d024370285dc6f86
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923268"
---
# <a name="business-transactions-in-project-operations"></a>Transaccions empresarials al Project Operations

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

A Microsoft Dynamics 365 Project Operations, *la transacció* comercial és un concepte abstracte que no està representat per cap entitat. No obstant, alguns camps i processos comuns de les entitats estan dissenyats per utilitzar el concepte de transaccions empresarials. Les entitats següents utilitzen aquesta abstracció:

- Detalls de la línia d'oferta
- Detalls de la línia de contracte
- Línies d'estimació
- Línies del llibre diari
- Valors reals

D'aquestes entitats, els detalls de la línia d'oferta, els detalls de la línia del contracte i les línies d'estimació s'assignen a la fase *d'estimació* del cicle de vida del projecte. Les línies del Diari i les entitats actuals s'assignen a la fase *d'execució* del cicle de vida del projecte.

Project Operations tracta els registres de les cinc entitats com a transaccions comercials. L'única distinció és que els registres de les entitats que s'assignen a la fase d'estimació (detalls de la línia de cotització, detalls de la línia del contracte i línies d'estimació) es consideren *previsions* financeres, mentre que els registres de les entitats que s'assignen a la fase d'execució (Línies de diari i reals) es consideren *fets* financers que ja s'han produït.

Per obtenir més informació, vegeu [Estimacions](../project-management/estimating-projects-overview.md) i [Valors reals](actuals-overview.md).

## <a name="concepts-that-are-unique-to-business-transactions"></a>Conceptes únics per a transaccions empresarials

Els conceptes següents són únics per al concepte de transaccions empresarials:

- Tipus de transacció
- Classe de la transacció
- Origen de la transacció
- Connexió de la transacció

### <a name="transaction-type"></a>Tipus de transacció

El tipus de transacció representa el cronometratge i el context de l'impacte financer d'un projecte. Es defineix per un conjunt d'opcions que té els valors admesos següents a les operacions del projecte:

- Cost
- Contracte de projecte
- Vendes no facturades
- Vendes facturades
- Vendes interorganitzatives
- Cost de la unitat de recursos

### <a name="transaction-class"></a>Classe de la transacció

La classe de la transacció representa els diferents tipus de costos que s'han incorregut en els projectes. Es defineix per un conjunt d'opcions que té els valors admesos següents a les operacions del projecte:

- Hora
- Despesa
- Material
- Tarifa
- Fita
- Impostos

> [!NOTE]
> El **valor Milestone** normalment l'utilitza la lògica empresarial per a la facturació de preu fix a les operacions del projecte.

### <a name="transaction-origin"></a>Origen de la transacció

L'origen de la transacció és una entitat que emmagatzema l'origen de cada transacció comercial per ajudar amb la presentació d'informes i la traçabilitat. A mesura que s'inicia l'execució del projecte, cada transacció comercial crea una altra transacció comercial que, al seu torn, crearà una altra transacció comercial, i així successivament.

### <a name="transaction-connection"></a>Connexió de la transacció

La connexió de transacció és una entitat que emmagatzema la relació entre dues transaccions comercials similars, com ara els reals de costos i vendes relacionades o les reversions de transaccions que s'activen per activitats de facturació, com ara la confirmació de la factura o les correccions de factures.

En conjunt, les entitats Origen de transacció i connexió de transacció us ajuden a fer un seguiment de les relacions entre les transaccions comercials i les accions que han provocat la creació d'una transacció comercial específica.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
