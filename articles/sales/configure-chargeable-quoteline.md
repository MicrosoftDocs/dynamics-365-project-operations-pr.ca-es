---
title: Configuració dels components imputables d'una línia d'oferta basada en projecte
description: Aquest tema proporciona informació sobre els components inclosos, els factuables i els que no es poden facturar, a les línies de l'oferta basada en projecte.
author: rumant
manager: Annbe
ms.date: 11/18/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 36765ab3687a8aaf3ae4a631516a1d61c14e981e
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642531"
---
# <a name="configure-the-chargeable-components-of-a-project-based-quote-line"></a>Configuració dels components imputables d'una línia d'oferta basada en projecte

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

Una línia d'oferta basada en projecte pot incloure components i components imputables.

Els components inclosos estan subjectes al mètode de facturació, les divisions de client, els límits que no es poden superar i la configuració de la freqüència de factura definits a la línia d'oferta basada en projecte.
Un subconjunt dels components inclosos es pot marcar com a imputable mitjançant el **Tipus de facturació**. Podeu seleccionar una de les opcions següents del camp **Tipus de facturació** en el context d'una línia d'oferta:

   - Imputable
   - No imputable

Els components imputables es poden definir en funcions i categories de transacció.

La imputabilitat que es defineix en les funcions per a una línia d'oferta de projecte només s'aplica a la classe de transacció **Temps**. Si una línia d'oferta de projecte té **Inclou temps** = **No**, la pestanya **Funcions imputables** no està disponible.

La imputabilitat que es defineix en les categories de transacció d'una línia d'oferta de projecte només s'aplica a la classe de transacció **Despesa**. Si una línia d'oferta de projecte té **Inclou despeses** = **No**, la pestanya **Categories imputables** no està disponible.

## <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Actualitzar una funció com a imputable o no imputable
Una funció pot ser imputable o no imputable en una línia d'oferta basada en projecte. El tipus de facturació d'una funció es pot configurar a la pestanya **Funcions imputables** d'una línia d'oferta basada en projecte. Per fer-ho, actualitzeu el **Tipus de facturació** a la subquadrícula **Funcions imputables**. 

## <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Actualitzar una categoria de transacció com a imputable o no imputable
Una categoria de transacció pot ser imputable o no imputable en una línia d'oferta basada en projecte. El tipus de facturació d'una transacció es pot configurar a la pestanya **Categories imputables** d'una línia d'oferta basada en projecte. Per fer-ho, actualitzeu el camp **Tipus de facturació** de la subquadrícula **Categories imputables**. 

## <a name="resolve-chargeability"></a>Resoldre la imputabilitat

Una estimació o un valor real creat per al temps només es considerarà imputable si el temps està inclòs a la línia d'oferta i si la funció està configurada com a imputable.
Una estimació o un valor real creat per al una despesa només es considerarà imputable si la despesa està inclosa a la línia d'oferta i si la categoria de transacció està configurada com a imputable a la línia de l'oferta. A la taula següent es mostra com s'estableixen els valors per defecte d'imputabilitat en cada valor real. Els valors per defecte es basen en els components inclosos i en el tipus de facturació que s'ha configurat a la línia d'oferta.

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