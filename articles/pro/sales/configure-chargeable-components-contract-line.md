---
title: Configuració dels components imputables d'una línia de contracte basada en projectes
description: Aquest tema proporciona informació sobre com afegir components imputables a les línies de contracte al Project Operations.
author: rumant
manager: Annbe
ms.date: 10/08/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4d665a6351d2315d185e64e4eb6b0b8859f7bbc4
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072119"
---
# <a name="configuring-chargeable-components-of-a-project-based-contract-line"></a>Configuració dels components imputables d'una línia de contracte basada en projectes

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_

Una línia de contracte basada en projectes té components *inclosos* i components *imputables*.

Els components inclosos són els que estan subjectes a:

  - Mètode de facturació i desglossament del client
  - Límits que no s'han de superar 
  - Paràmetres de freqüència de facturació definits a la línia de contracte basada en projectes

Un subconjunt dels components inclosos es pot marcar com a imputable mitjançant el camp **Tipus de facturació**. El camp **Tipus de facturació** és un conjunt d'opcions que permet els següents valors en el context d'una línia de contracte:

  - Imputable
  - No imputable

Els components imputables es poden definir en tasques, rols i categories de transacció.

La imputabilitat es defineix en les tasques d'una línia de contracte de projecte i s'aplica a totes les classes de transacció incloses a la línia. Si el camp **Inclou les tasques** d'una línia de contracte és buit o s'ha establert a **Tot el projecte** , la pestanya **Tasques imputables** no estarà disponible.

La imputabilitat definida a les funcions d'una línia de contracte de projecte només s'aplica a la classe de transacció **Temps**. Si el camp **Inclou el temps** d'una línia de contracte és buit o s'ha establert a **No** , la pestanya **Funcions imputables** no estarà disponible.

La imputabilitat definida a les categories de transacció d'una línia de contracte de projecte només s'aplica a la classe de transacció **Despesa**. Si el camp **Inclou les despeses** s'ha establert a **No** , la pestanya **Categories imputables** no estarà disponible.

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a>Actualitzar una tasca de projecte com a imputable o no imputable

Una tasca de projecte pot ser imputable o no imputable en una línia de contracte específica que fa possible la següent configuració:

Si una línia de contracte basada en el projecte inclou **Temps** i una tasca determinada, **T1** s'hi associa com a imputable. Si hi ha una segona línia de contracte que inclou **Despesa** , es pot associar la tasca T1 a la línia de contracte com a no imputable. El resultat és que tot el temps que es registra en la tasca és imputable i totes les despeses no són imputables.

El tipus de facturació d'una tasca es pot configurar a la pestanya **Tasques imputables** de la línia de contracte actualitzant el camp **Tipus de facturació** a la subquadrícula de les tasques de la línia de contracte. Alternativament, podeu actualitzar el camp **Tipus de facturació** a la subquadrícula de la tasca Configuració de facturació d'un projecte que mostra les línies de contracte associades a una tasca.

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a>Actualitzar una funció com a imputable o no imputable

Una funció pot ser imputable o no imputable en una línia de contracte específica.

El tipus de facturació d'una funció es pot configurar a la pestanya **Funcions imputables** d'una línia de contracte. Per fer-ho, actualitzeu el camp **Tipus de facturació** a la subquadrícula **Funcions imputables**.

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a>Actualitzar una categoria de transacció com a imputable o no imputable

Una categoria de transacció pot ser imputable o no imputable en una línia de contracte específica.

El tipus de facturació d'una transacció es pot configurar a la pestanya **Categories imputables** d'una línia de contracte basada en projectes. Per fer-ho, actualitzeu el camp **Tipus de facturació** a la subquadrícula **Categories imputables**.

### <a name="resolve-chargeability"></a>Resoldre la imputabilitat

Una estimació o valor real creat per al temps només es considerarà imputable si **Temps** s'inclou en la línia de contracte, i si **Tasca** i **Funció** es configuren com a imputables en la línia de contracte.

Una estimació o valor real creat per a la despesa només es considerarà imputable si **Despesa** s'inclou en la línia de contracte, i si les categories **Tasca** i **Transacció** es configuren com a imputables en la línia de contracte.


| Inclou el temps | Inclou les despeses | Inclou les tasques | Funció           | Categoria       | Tasca                                                                                                      |
|---------------|------------------|----------------|----------------|----------------|-----------------------------------------------------------------------------------------------------------|
| Sí           | Sí              | Tot el projecte | Imputable     | Imputable     | Facturació en un valor real de temps: **Imputable** </br> Tipus de facturació en un valor real de despesa: **Imputable**           |
| Sí           | Sí              | Tasques seleccionades | Imputable     | Imputable     | Facturació en un valor real de temps: **Imputable** </br> Tipus de facturació en un valor real de despesa: **Imputable**           |
| Sí           | Sí              | Tasques seleccionades | No imputable | Imputable     | Facturació en un valor real de temps: **No imputable** </br> Tipus de facturació en un valor real de despesa: **Imputable**       |
| Sí           | Sí              | Tasques seleccionades | Imputable     | Imputable     | Facturació en un valor real de temps: **No imputable** </br> Tipus de facturació en un valor real de despesa: **No imputable** |
| Sí           | Sí              | Tasques seleccionades | No imputable | Imputable     | Facturació en un valor real de temps: **No imputable** </br> Tipus de facturació en un valor real de despesa: **No imputable** |
| Sí           | Sí              | Tasques seleccionades | No imputable | No imputable | Facturació en un valor real de temps: **No imputable** </br> Tipus de facturació en un valor real de despesa: **No imputable** |
| No            | Sí              | Tot el projecte | No es pot establir   | Imputable     | Facturació en un valor real de temps: **No disponible**</br>Tipus de facturació en un valor real de despesa: **Imputable**          |
| No            | Sí              | Tot el projecte | No es pot establir   | No imputable | Facturació en un valor real de temps: **No disponible**</br> Tipus de facturació en un valor real de despesa: **No imputable**     |
| Sí           | No               | Tot el projecte | Imputable     | No es pot establir   | Facturació en un valor real de temps: **Imputable** </br> Tipus de facturació en un valor real de despesa: **No disponible**        |
| Sí           | No               | Tot el projecte | No imputable | No es pot establir   | Facturació en un valor real de temps: **No imputable** </br>Tipus de facturació en un valor real de despesa: **No disponible**   |
