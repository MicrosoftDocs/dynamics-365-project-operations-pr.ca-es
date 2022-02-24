---
title: Configuració dels components facturables d'una línia de contracte de projectes
description: Aquest tema proporciona informació els components inclosos, imputables i no imputables a les línies de contracte.
author: rumant
manager: Annbe
ms.date: 10/12/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 60a2792f7783053a288303e1dcc01a986e948300
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858326"
---
# <a name="configure-chargeable-components-of-a-project-contract-line"></a>Configuració dels components facturables d'una línia de contracte de projectes

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

Una línia de contracte basada en projectes té el concepte de components inclosos, imputables i no imputables.

Els components inclosos estan subjectes al mètode de facturació, les divisions del client, els límits que no es poden excedir i la configuració de freqüència de facturació definits a la línia de contracte basada en el projecte.

Un subconjunt dels components inclosos es pot marcar com a imputable actualitzant el camp **Tipus de facturació**.

Els components imputables es poden definir en funcions i categories de transacció.

Per a una línia de contracte de projecte, la imputabilitat definida en una funció només s'aplica a la classe de transacció **Temps**. Si **Inclou el temps** d'una línia de contracte s'ha establert a **No**, la pestanya **Funcions imputables** no està disponible.

La imputabilitat definida a les categories de transacció d'una línia de contracte de projecte només s'aplica a la classe de transacció **Despesa**. Si **Inclou les despeses** d'una línia de contracte s'ha establert a **No**, la pestanya **Categories imputables** no està disponible.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Actualitzar una funció com a imputable o no imputable

Una funció pot ser imputable o no imputable en una línia de contracte basada en projectes específica.

A la pestanya **Funcions imputables** d'una línia de contracte basada en projectes, a la subquadrícula **Categories imputables**, al camp **Tipus de facturació**, actualitzeu el tipus de facturació d'una funció.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Actualitzar una categoria de transacció com a imputable o no imputable

Una categoria de transacció pot ser imputable o no imputable en una línia de contracte basada en projectes específica.

A la pestanya **Categories imputables** d'una línia de contracte basada en projectes, a la subquadrícula **Categories imputables**, al camp **Tipus de facturació**, actualitzeu el tipus de facturació d'una transacció.

### <a name="resolve-chargeability"></a>Resoldre la imputabilitat

Una estimació o valor real creat per al temps només es considerarà imputable si s'inclou temps en la línia de contracte, i si la funció es configura com a imputable en la línia de contracte.

Una estimació o valor real creat per a la despesa només es considerarà imputable si la despesa s'inclou en la línia de contracte, i si la categoria de transacció es configura com a imputable en la línia de contracte.

| Inclou el temps | Inclou les despeses | Funció | Categoria | Tasca |
| --- | --- | --- | --- | --- |
| Sí | Sí | Imputable | Imputable | Facturació en un valor real de temps: Imputable </br>Tipus de facturació en un valor real de despesa: Imputable |
| Sí | Sí | No imputable | Imputable | Facturació en un valor real de temps: No imputable </br>Tipus de facturació en un valor real de despesa: Imputable |
| Sí | Sí | No imputable | No imputable | Facturació en un valor real de temps: No imputable </br>Tipus de facturació en un valor real de despesa: No imputable |
| No | Sí | No es pot establir | Imputable | Facturació en un valor real de temps: No disponible </br>Tipus de facturació en un valor real de despesa: Imputable |
| No | Sí | No es pot establir | No imputable | Facturació en un valor real de temps: No disponible </br>Tipus de facturació en un valor real de despesa: No imputable |
| Sí | No | Imputable | No es pot establir | Facturació en un valor real de temps: Imputable </br>Tipus de facturació en un valor real de despesa: No disponible |
| Sí | No | No imputable | No es pot establir | Facturació en un valor real de temps: No imputable </br> Tipus de facturació en un valor real de despesa: No disponible |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
