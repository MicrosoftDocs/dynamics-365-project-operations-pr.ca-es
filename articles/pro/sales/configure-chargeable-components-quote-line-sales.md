---
title: Configuració dels components imputables d'una línia d'oferta
description: Aquest tema proporciona informació sobre la configuració de components imputables i no imputables en una línia d'oferta basada en el projecte.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: e0b64d7edb21df127bf7544f044de7f3c496dfe3
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072333"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a>Configuració dels components imputables d'una línia d'oferta

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_

Una línia d'oferta basada en projectes té el concepte de components *inclosos* i components *imputables*.

Els components inclosos estan subjectes a:

  - Mètode de facturació i desglossament del client
  - Límits que no s'han de superar 
  - Paràmetres de freqüència de facturació definits a la línia d'oferta basada en projectes

Un subconjunt dels components inclosos es pot marcar com a imputable mitjançant el camp **Tipus de facturació**. El camp **Tipus de facturació** és un conjunt d'opcions que permet els següents valors en el context d'una línia d'oferta:

  - Imputable
  - No imputable

Els components imputables es poden definir en tasques, rols i categories de transacció.

La imputabilitat es defineix en les tasques d'una línia d'oferta i s'aplica a totes les classes de transacció incloses a la línia. Si el camp **Inclou les tasques** és buit o s'ha establert a **Tot el projecte** , la pestanya **Tasques imputables** no està disponible.

La imputabilitat definida a les funcions d'una línia d'oferta i només s'aplica a la classe de transacció **Temps**. Si el camp **Inclou el temps** d'una línia d'oferta de projecte s'ha establert a **No** , la pestanya **Funcions imputables** no està disponible.

La imputabilitat definida a les categories de transacció d'una línia d'oferta i només s'aplica a la classe de transacció **Despesa**. Si el camp **Inclou les despeses** d'una línia d'oferta de projecte s'ha establert a **No** , la pestanya **Categories imputables** no està disponible.

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a>Actualitzar una tasca de projecte com a imputable o no imputable

Una tasca de projecte pot ser imputable o no imputable en el context d'una línia d'oferta basada en projectes específica que fa possible la següent configuració:

Si una línia d'oferta basada en projectes inclou **Temps** i la tasca **T1** , la tasca s'associa a la línia d'oferta com a imputable. Si hi ha una segona línia d'oferta que inclou **Despeses** , es pot associar la tasca **T1** a la línia d'oferta com a no imputable. El resultat és que tot el temps que es registra en la tasca és imputable i totes les despeses registrades a la tasca no són imputables.

El tipus de facturació d'una tasca es pot configurar a la pestanya **Tasques imputables** d'una línia d'oferta basada en projectes actualitzant el camp **Tipus de facturació** a la subquadrícula **Tasques de la línia d'oferta**. Alternativament, podeu actualitzar el tipus de facturació per a una tasca del projecte el camp **Tipus de facturació** a la subquadrícula de la tasca Configuració de facturació d'un projecte que mostra les línies de contracte associades a una tasca.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Actualitzar una funció com a imputable o no imputable

Una funció pot ser imputable o no imputable en el context d'una línia d'oferta basada en projectes específica.

El tipus de facturació d'una funció es pot configurar a la pestanya **Funcions imputables** d'una línia d'oferta actualitzant el camp **Tipus de facturació** a la subquadrícula **Funcions imputables**.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Actualitzar una categoria de transacció com a imputable o no imputable

Una categoria de transacció pot ser imputable o no imputable en una línia d'oferta específica.

El tipus de facturació d'una transacció es pot configurar a la pestanya **Categories imputables** d'una línia d'oferta actualitzant el camp **Tipus de facturació** a la subquadrícula **Categories imputables**.

### <a name="resolve-chargeability"></a>Resoldre la imputabilitat
Una estimació o valor real creat per al temps només es considerarà imputable si **Temps** s'inclou en la línia d'oferta, i si **Tasca** i **Funció** es configuren com a imputables en la línia d'oferta.

Una estimació o valor real creat per a la despesa només es considerarà imputable si **Despesa** s'inclou en la línia d'oferta, i si les categories **Tasca** i **Categoria** es configuren com a imputables en la línia d'oferta.

| Inclou el temps | Inclou les despeses | Tasques incloses | Funció | Categoria | Tasca | Facturació |
| --- | --- | --- | --- | --- | --- | --- |
| Sí | Sí | Tot el projecte | Imputable | Imputable | No es pot establir | Facturació en un valor real de temps: Imputable </br>Tipus de facturació en un valor real de despesa: Imputable |
| Sí | Sí | Només les tasques seleccionades | Imputable | Imputable | Imputable | Facturació en un valor real de temps: Imputable</br>Tipus de facturació en un valor real de despesa: Imputable |
| Sí | Sí | Només les tasques seleccionades | No imputable | Imputable | Imputable | Facturació en un valor real de temps: No imputable</br>Tipus de facturació en un valor real de despesa: Imputable |
| Sí | Sí | Només les tasques seleccionades | Imputable | Imputable | No imputable | Facturació en un valor real de temps: No imputable</br> Tipus de facturació en un valor real de despesa: No imputable |
| Sí | Sí | Només les tasques seleccionades | No imputable | Imputable | No imputable | Facturació en un valor real de temps: No imputable</br> Tipus de facturació en un valor real de despesa: No imputable |
| Sí | Sí | Només les tasques seleccionades | No imputable | No imputable | Imputable | Facturació en un valor real de temps: No imputable</br> Tipus de facturació en un valor real de despesa: No imputable |
| No | Sí | Tot el projecte | No es pot establir | Imputable | No es pot establir | Facturació en un valor real de temps: No disponible </br>Tipus de facturació en un valor real de despesa: Imputable |
| No | Sí | Tot el projecte | No es pot establir | No imputable | No es pot establir | Facturació en un valor real de temps: No disponible </br>Tipus de facturació en un valor real de despesa: No imputable |
| Sí | No | Tot el projecte | Imputable | No es pot establir | No es pot establir | Facturació en un valor real de temps: Imputable</br>Tipus de facturació en un valor real de despesa: No disponible |
| Sí | No | Tot el projecte | No imputable | No es pot establir | No es pot establir | Facturació en un valor real de temps: No imputable </br>Tipus de facturació en un valor real de despesa: No disponible |
