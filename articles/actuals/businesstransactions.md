---
title: Transaccions empresarials al Project Operations
description: En aquest article es proporciona informació general sobre el concepte de les transaccions empresarials al Microsoft Dynamics 365 Project Operations.
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

Al Microsoft Dynamics 365 Project Operations, una *transacció empresarial* és un concepte abstracte que no està representat per cap entitat. No obstant, alguns camps i processos comuns de les entitats estan dissenyats per utilitzar el concepte de transaccions empresarials. Les entitats següents utilitzen aquesta abstracció:

- Detalls de la línia d'oferta
- Detalls de la línia de contracte
- Línies d'estimació
- Línies del llibre diari
- Valors reals

D'aquestes entitats, els Detalls de la línia d'oferta, els Detalls de la línia de contracte i les Línies d'estimació s'assignen a la *fase d'estimació* del cicle de vida del projecte. Les entitats de Línies del llibre diari i les Valors reals s'assignen a la *fase d'execució* del cicle de vida del projecte.

El Project Operations tracta els registres de totes aquestes cinc entitats com a transaccions empresarials. L'única distinció és que els registres de les entitats que estan assignats a la fase d'estimació (Detalls de la línia d'oferta, Detalls de la línia de contracte i Línies d'estimació) tenen la consideració de *previsions financeres*, mentre que les entitats assignades a la fase d'execució (Línies del llibre diari i Valors reals) es consideren *fets financers* que ja s'han produït.

Per obtenir més informació, vegeu [Estimacions](../project-management/estimating-projects-overview.md) i [Valors reals](actuals-overview.md).

## <a name="concepts-that-are-unique-to-business-transactions"></a>Conceptes únics per a transaccions empresarials

Els conceptes següents són únics per al concepte de transaccions empresarials:

- Tipus de transacció
- Classe de la transacció
- Origen de la transacció
- Connexió de la transacció

### <a name="transaction-type"></a>Tipus de transacció

El tipus de transacció representa el cronometratge i el context de l'impacte financer d'un projecte. Es defineix amb un conjunt d'opcions que té els valors admesos següents al Project Operations:

- Cost
- Contracte de projecte
- Vendes no facturades
- Vendes facturades
- Vendes interorganitzatives
- Cost de la unitat de recursos

### <a name="transaction-class"></a>Classe de la transacció

La classe de la transacció representa els diferents tipus de costos que s'han incorregut en els projectes. Es defineix amb un conjunt d'opcions que té els valors admesos següents al Project Operations:

- Hora
- Despesa
- Material
- Tarifa
- Fita
- Impostos

> [!NOTE]
> El valor **Fita** s'utilitza normalment per la lògica empresarial per a la facturació a preu fix al Project Operations.

### <a name="transaction-origin"></a>Origen de la transacció

L'origen de la transacció és una entitat que emmagatzema l'origen de cada transacció empresarial per ajudar en els informes i la traçabilitat. Quan s'inicia l'execució, cada transacció empresarial crea una altra transacció empresarial que, al seu torn, en crearà una altra i així successivament.

### <a name="transaction-connection"></a>Connexió de la transacció

La connexió de la transacció és una entitat que emmagatzema la relació entre dues transaccions empresarials similars, com ara els valors reals de vendes i costos relacionats o les reversions de transaccions que desencadenen les activitats de facturació, com ara la confirmació de la factura o correccions de la factura.

En conjunt, les entitats Origen de la transacció i Connexió de la transacció us ajudaran a fer un seguiment de les relacions entre transaccions empresarials i accions que han originat la creació d'una transacció empresarial concreta.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
