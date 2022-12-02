---
title: Configuració dels components facturables d'una línia de contracte basada en projectes
description: Aquest article proporciona informació sobre com afegir components imputables a les línies de contracte al Project Operations.
author: rumant
ms.date: 10/08/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 0e4118e8e56d45ef75f53d828e267a8a9c1c903a
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922946"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a>Configuració dels components facturables d'una línia de contracte basada en projectes

_**S'aplica a:** Implementació bàsica: tracte de facturació proforma, Project Operations per a escenaris basats en recursos/sense cotització_

Una línia de contracte basada en projectes té components *inclosos* i components *imputables*.

Els components inclosos són els que estan subjectes a:

  - Mètode de facturació i desglossament del client
  - Límits que no s'han de superar 
  - Paràmetres de freqüència de facturació definits a la línia de contracte basada en projectes

Un subconjunt dels components inclosos es pot marcar com a imputable mitjançant el camp **Tipus de facturació**. El camp **Tipus de facturació** és un conjunt d'opcions que permet els següents valors en el context d'una línia de contracte:

  - Imputable
  - No imputable

Els components imputables es poden definir en tasques, rols i categories de transacció.

La imputabilitat es defineix en les tasques d'una línia de contracte de projecte i s'aplica a totes les classes de transacció incloses a la línia. Si el camp **Inclou les tasques** d'una línia de contracte és buit o s'ha establert a **Tot el projecte**, la pestanya **Tasques imputables** no estarà disponible.

La imputabilitat definida a les funcions d'una línia de contracte de projecte només s'aplica a la classe de transacció **Temps**. Si el camp **Inclou el temps** d'una línia de contracte és buit o s'ha establert a **No**, la pestanya **Funcions imputables** no estarà disponible.

La imputabilitat definida a les categories de transacció d'una línia de contracte de projecte només s'aplica a la classe de transacció **Despesa**. Si el camp **Inclou les despeses** s'ha establert a **No**, la pestanya **Categories imputables** no estarà disponible.

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a>Actualitzar una tasca de projecte com a imputable o no imputable

Una tasca de projecte pot ser imputable o no imputable en una línia de contracte específica, cosa que fa possible la configuració següent:

Si una línia de contracte basada en el projecte inclou **Temps** i una tasca determinada, **T1** s'hi associa com a imputable. Si hi ha una segona línia de contracte que inclou **Despesa**, es pot associar la tasca T1 a la línia de contracte com a no imputable. El resultat és que tot el temps que es registra en la tasca és imputable i totes les despeses no són imputables.

El tipus de facturació d'una tasca es pot configurar a la pestanya **Tasques imputables** de la línia de contracte actualitzant el camp **Tipus de facturació** a la subquadrícula de tasques de la línia de contracte. Alternativament, podeu actualitzar el camp **Tipus de facturació** a la subquadrícula de la Configuració de facturació de la tasca d'un projecte que mostra les línies de contracte associades a una tasca.

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a>Actualitzar una funció com a imputable o no imputable

Una funció pot ser imputable o no imputable en una línia de contracte específica.

El tipus de facturació d'una funció es pot configurar a la pestanya **Funcions imputables** d'una línia de contracte. Per fer-ho, actualitzeu el camp **Tipus de facturació** de la subquadrícula **Funcions imputables**.

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a>Actualitzar una categoria de transacció com a imputable o no imputable

Una categoria de transacció pot ser imputable o no imputable en una línia de contracte específica.

El tipus de facturació d'una transacció es pot configurar a la pestanya **Categories imputables** d'una línia de contracte basada en projectes. Per fer-ho, actualitzeu el camp **Tipus de facturació** de la subquadrícula **Categories imputables**.

### <a name="resolve-chargeability"></a>Resoldre la imputabilitat

Una estimació o un valor real creat per a temps només es consideraran imputables si:

   - El **Temps** s'inclou a la línia de contracte.
   - La **Funció** està configurada com a imputable a la línia de contracte.
   - **Tasques incloses** està establert com a **Tasques seleccionades** a la línia de contracte.
 
 Si aquestes tres coses són certes, la tasca es configura com a imputable. 

Una estimació o un valor real creats per a despeses només es consideraran imputables si:

   - La **Despesa** s'inclou a la línia de contracte.
   - **Categoria de transacció** està configurat com a imputable a la línia de contracte.
   - **Tasques incloses** està establert com a **Tasca seleccionada** a la línia de contracte
  
 Si aquestes tres coses són certes, la **Tasca** es configura com a imputable. 

Una estimació o un valor real creats per a materials només es consideraran imputables si:

   - **Materials** s'inclou a la línia de contracte
   - **Tasques incloses** està establert com a **Tasques seleccionades** a la línia de contracte

Si aquestes dues coses són certes, la **Tasca** es configura com a imputable. 

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>Inclou el temps</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>Inclou les despeses</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>Inclou materials</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
                    <strong>Tasques incloses</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Funció</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Categoria</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Tasca</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
                    <strong>Impacte de la imputabilitat</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Sí </p>
            </td>
            <td width="78" valign="top">
                <p>
Sí </p>
            </td>
            <td width="63" valign="top">
                <p>
Sí </p>
            </td>
            <td width="75" valign="top">
                <p>
Tot el projecte </p>
            </td>
            <td width="65" valign="top">
                <p>
Imputable </p>
            </td>
            <td width="70" valign="top">
                <p>
Imputable </p>
            </td>
            <td width="65" valign="top">
                <p>
No es pot establir </p>
            </td>
            <td width="350" valign="top">
                <p>
Facturació en un valor real de temps: <strong>Imputable</strong>
                </p>
                <p>
Tipus de facturació en un valor real de despesa: <strong>Imputable</strong>
                </p>
                <p>
Tipus de facturació del material real: <strong>Imputable</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Sí </p>
            </td>
            <td width="78" valign="top">
                <p>
Sí </p>
            </td>
            <td width="63" valign="top">
                <p>
Sí </p>
            </td>
            <td width="75" valign="top">
                <p>
Només les tasques seleccionades </p>
            </td>
            <td width="65" valign="top">
                <p>
Imputable </p>
            </td>
            <td width="70" valign="top">
                <p>
Imputable </p>
            </td>
            <td width="65" valign="top">
                <p>
Imputable </p>
            </td>
            <td width="350" valign="top">
                <p>
Facturació en un valor real de temps: <strong>Imputable</strong>
                </p>
                <p>
Tipus de facturació en un valor real de despesa: <strong>Imputable</strong>
                </p>
                <p>
Tipus de facturació del material real: <strong>Imputable</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Sí </p>
            </td>
            <td width="78" valign="top">
                <p>
Sí </p>
            </td>
            <td width="63" valign="top">
                <p>
Sí </p>
            </td>
            <td width="75" valign="top">
                <p>
Només les tasques seleccionades </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>No imputable</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
Imputable </p>
            </td>
            <td width="65" valign="top">
                <p>
Imputable </p>
            </td>
            <td width="350" valign="top">
                <p>
Facturació en un valor real de temps: <strong>No imputable</strong>
                </p>
                <p>
Tipus de facturació en un valor real de despesa: Imputable </p>
                <p>
Tipus de facturació del material real: imputable </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Sí </p>
            </td>
            <td width="78" valign="top">
                <p>
Sí </p>
            </td>
            <td width="63" valign="top">
                <p>
Sí </p>
            </td>
            <td width="75" valign="top">
                <p>
Només les tasques seleccionades </p>
            </td>
            <td width="65" valign="top">
                <p>
Imputable </p>
            </td>
            <td width="70" valign="top">
                <p>
Imputable </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>No imputable</strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
Facturació en un valor real de temps: <strong>No imputable</strong>
                </p>
                <p>
Tipus de facturació en un valor real de despesa: <strong>No imputable</strong>
                </p>
                <p>
Tipus de facturació en un valor real de material: <strong>No imputable</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Sí </p>
            </td>
            <td width="78" valign="top">
                <p>
Sí </p>
            </td>
            <td width="63" valign="top">
                <p>
Sí </p>
            </td>
            <td width="75" valign="top">
                <p>
Només les tasques seleccionades </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>No imputable</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
Imputable </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>No imputable</strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
Facturació en un valor real de temps: <strong>No imputable</strong>
                </p>
                <p>
Tipus de facturació en un valor real de despesa: <strong>No imputable</strong>
                </p>
                <p>
Tipus de facturació en un valor real de material: <strong>No imputable</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Sí </p>
            </td>
            <td width="78" valign="top">
                <p>
Sí </p>
            </td>
            <td width="63" valign="top">
                <p>
Sí </p>
            </td>
            <td width="75" valign="top">
                <p>
Només les tasques seleccionades </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>No imputable</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>No imputable</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Imputable </p>
            </td>
            <td width="350" valign="top">
                <p>
Facturació en un valor real de temps: <strong>No imputable</strong>
                </p>
                <p>
Tipus de facturació en un valor real de despesa: <strong>No imputable</strong>
                </p>
                <p>
Tipus de facturació del material real: imputable </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
Sí </p>
            </td>
            <td width="63" valign="top">
                <p>
Sí </p>
            </td>
            <td width="75" valign="top">
                <p>
Tot el projecte </p>
            </td>
            <td width="65" valign="top">
                <p>
No es pot establir </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Imputable</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
No es pot establir </p>
            </td>
            <td width="350" valign="top">
                <p>
Facturació en un valor real de temps: <strong>No disponible</strong>
                </p>
                <p>
Tipus de facturació en un valor real de despesa: Imputable </p>
                <p>
Tipus de facturació del material real: imputable </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
Sí </p>
            </td>
            <td width="63" valign="top">
                <p>
Sí </p>
            </td>
            <td width="75" valign="top">
                <p>
Tot el projecte </p>
            </td>
            <td width="65" valign="top">
                <p>
No es pot establir </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>No imputable</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
No es pot establir </p>
            </td>
            <td width="350" valign="top">
                <p>
Facturació en un valor real de temps: <strong>No disponible</strong>
                </p>
                <p>
Tipus de facturació en un valor real de despesa: <strong>No imputable</strong>
                </p>
                <p>
Tipus de facturació del material real: imputable </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Sí </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
Sí </p>
            </td>
            <td width="75" valign="top">
                <p>
Tot el projecte </p>
            </td>
            <td width="65" valign="top">
                <p>
Imputable </p>
            </td>
            <td width="70" valign="top">
                <p>
No es pot establir </p>
            </td>
            <td width="65" valign="top">
                <p>
No es pot establir </p>
            </td>
            <td width="350" valign="top">
                <p>
Facturació en un valor real de temps: Imputable </p>
                <p>
Tipus de facturació en un valor real de despesa: <strong>No disponible</strong>
                </p>
                <p>
Tipus de facturació del material real: imputable </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Sí </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
Sí </p>
            </td>
            <td width="75" valign="top">
                <p>
Tot el projecte </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>No imputable</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
No es pot establir </p>
            </td>
            <td width="65" valign="top">
                <p>
No es pot establir </p>
            </td>
            <td width="350" valign="top">
                <p>
Facturació en un valor real de temps: <strong>No imputable</strong>
                </p>
                <p>
Tipus de facturació en un valor real de despesa: <strong>No disponible</strong>
                </p>
                <p>
Tipus de facturació del material real: imputable </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Sí </p>
            </td>
            <td width="78" valign="top">
                <p>
Sí </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
Tot el projecte </p>
            </td>
            <td width="65" valign="top">
                <p>
Imputable </p>
            </td>
            <td width="70" valign="top">
                <p>
Imputable </p>
            </td>
            <td width="65" valign="top">
                <p>
No es pot establir </p>
            </td>
            <td width="350" valign="top">
                <p>
Facturació en un valor real de temps: Imputable </p>
                <p>
Tipus de facturació en un valor real de despesa: Imputable </p>
                <p>
Tipus de facturació en un valor real de material: <strong>No disponible</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Sí </p>
            </td>
            <td width="78" valign="top">
                <p>
Sí </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
Tot el projecte </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>No imputable</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>No imputable</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
No es pot establir </p>
            </td>
            <td width="350" valign="top">
                <p>
Facturació en un valor real de temps: <strong>No imputable</strong>
                </p>
                <p>
Tipus de facturació en un valor real de despesa: <strong>No imputable</strong>
                </p>
                <p>
Tipus de facturació en un valor real de material: <strong>No disponible</strong>
                </p>
            </td>
        </tr>
    </tbody>
</table>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
