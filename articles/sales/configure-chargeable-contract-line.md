---
title: Configuració dels components imputables d'una línia de contracte basada en projecte
description: Aquest tema proporciona informació els components inclosos, imputables i no imputables a les línies de contracte.
author: rumant
manager: Annbe
ms.date: 10/12/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: af97904b0171618cb15d060da9bc87fcf6bbabeb
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072149"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a>Configuració dels components imputables d'una línia de contracte basada en projecte

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

Una línia de contracte basada en projectes té el concepte de components inclosos, imputables i no imputables.

Els components inclosos estan subjectes al mètode de facturació, les divisions del client, els límits que no es poden excedir i la configuració de freqüència de facturació definits a la línia de contracte basada en el projecte.

Un subconjunt dels components inclosos es pot marcar com a imputable actualitzant el camp **Tipus de facturació**.

Els components imputables es poden definir en funcions i categories de transacció.

Per a una línia de contracte de projecte, la imputabilitat definida en una funció només s'aplica a la classe de transacció **Temps**. Si **Inclou el temps** d'una línia de contracte s'ha establert a **No** , la pestanya **Funcions imputables** no està disponible.

La imputabilitat definida a les categories de transacció d'una línia de contracte de projecte només s'aplica a la classe de transacció **Despesa**. Si **Inclou les despeses** d'una línia de contracte s'ha establert a **No** , la pestanya **Categories imputables** no està disponible.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Actualitzar una funció com a imputable o no imputable

Una funció pot ser imputable o no imputable en una línia de contracte basada en projectes específica.

En la pestanya **Funcions imputables** d'una línia de contracte basada en projectes, a la subquadrícula **Categories imputables** , en el camp **Tipus de facturació** , actualitzeu el tipus de facturació d'una funció.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Actualitzar una categoria de transacció com a imputable o no imputable

Una categoria de transacció pot ser imputable o no imputable en una línia de contracte basada en projectes específica.

En la pestanya **Categories imputables** d'una línia de contracte basada en projectes, a la subquadrícula **Categories imputables** , en el camp **Tipus de facturació** , actualitzeu el tipus de facturació d'una transacció.

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