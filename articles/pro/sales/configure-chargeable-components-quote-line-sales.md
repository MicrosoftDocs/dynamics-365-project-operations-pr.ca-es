---
title: Configurar components que es poden carregar a les línies de pressupostos del projecte
description: Aquest article proporciona informació sobre la configuració de components imputables i no imputables en una línia d'oferta basada en el projecte.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 1e454278a1c5c24ac346c537c778b25448d9ea03
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 12/05/2022
ms.locfileid: "9825505"
---
# <a name="configure-chargeable-components-on-project-quote-lines"></a>Configurar components que es poden carregar a les línies de pressupostos del projecte

_**S'aplica a:** Implementació bàsica: tracte de facturació proforma, Project Operations per a escenaris basats en recursos/sense cotització_

Una línia d'oferta basada en projectes té el concepte de components *inclosos* i components *imputables*.

Els components inclosos estan subjectes a:

  - Mètode de facturació i desglossament del client
  - Límits que no s'han de superar 
  - Paràmetres de freqüència de facturació definits a la línia d'oferta basada en projectes

Un subconjunt dels components inclosos es pot marcar com a imputable mitjançant el camp **Tipus de facturació**. El camp **Tipus de facturació** és un conjunt d'opcions que permet els següents valors en el context d'una línia d'oferta:

  - Imputable
  - No imputable

Els components imputables es poden definir en tasques, rols i categories de transacció.

La imputabilitat es defineix en les tasques d'una línia d'oferta i s'aplica a totes les classes de transacció incloses a la línia. Si el camp **Inclou les tasques** és buit o s'ha establert a **Tot el projecte**, la pestanya **Tasques imputables** no està disponible.

La imputabilitat definida a les funcions d'una línia d'oferta i només s'aplica a la classe de transacció **Temps**. Si el camp **Inclou el temps** d'una línia d'oferta de projecte s'ha establert a **No**, la pestanya **Funcions imputables** no està disponible.

La imputabilitat definida a les categories de transacció d'una línia d'oferta i només s'aplica a la classe de transacció **Despesa**. Si el camp **Inclou les despeses** d'una línia d'oferta de projecte s'ha establert a **No**, la pestanya **Categories imputables** no està disponible.

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a>Actualitzar una tasca de projecte com a imputable o no imputable

Una tasca de projecte pot ser imputable o no imputable en el context d'una línia d'oferta basada en projectes específica, cosa que fa possible la configuració següent.

Si una línia d'oferta basada en projectes inclou **Temps** i la tasca **T1**, la tasca s'associa a la línia d'oferta com a imputable. Si hi ha una segona línia d'oferta que inclou **Despeses**, es pot associar la tasca **T1** a la línia d'oferta com a no imputable. El resultat és que tot el temps que es registra en la tasca és imputable i totes les despeses registrades a la tasca no són imputables.

El tipus de facturació d'una tasca es pot configurar a la pestanya **Tasques imputables** de la línia de d'oferta basada en projectes actualitzant el camp **Tipus de facturació** a la subquadrícula **Tasques de la línia d'oferta**. Alternativament, podeu actualitzar el tipus de facturació per a una tasca de projecte al camp **Tipus de facturació** a la subquadrícula de configuració de la facturació de la tasca d'un projecte que mostra les línies de contracte associades a una tasca.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Actualitzar una funció com a imputable o no imputable

Una funció pot ser imputable o no imputable en el context d'una línia d'oferta basada en projectes específica.

El tipus de facturació d'una funció es pot configurar a la pestanya **Funcions imputables** de la línia de d'oferta actualitzant el camp **Tipus de facturació** a la subquadrícula **Funcions imputables**.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Actualitzar una categoria de transacció com a imputable o no imputable

Una categoria de transacció pot ser imputable o no imputable en una línia d'oferta específica.

El tipus de facturació d'una transacció es pot configurar a la pestanya **Categories imputables** de la línia de d'oferta actualitzant el camp **Tipus de facturació** a la subquadrícula **Categories imputables**.

### <a name="resolve-chargeability"></a>Resoldre la imputabilitat
Una estimació o un valor real creats per al temps només es consideraran imputables si:

   - El **Temps** s'inclou a la línia d'oferta.
   - La **Funció** està configurada com a imputable a la línia d'oferta.
   - **Tasques incloses** està establert com a **Tasques seleccionades** a la línia d'oferta. 

Si aquestes tres coses són certes, la **Tasca** també es configura com a imputable. 

Una estimació o un valor real creats per a despeses només es consideraran imputables si: 

   - La **Despesa** s'inclou a la línia d'oferta.
   - **Categoria de transacció** està configurat com a imputable a la línia d'oferta.
   - **Tasques incloses** està establert com a **Tasques seleccionades** a la línia d'oferta.

Si aquestes tres coses són certes, la **Tasca** també es configura com a imputable. 

Una estimació o un valor real creats per al material només es consideraran imputables si:

   - **Materials** s'inclou a la línia d'oferta.
   - **Tasques incloses** està establert com a **Tasques seleccionades** a la línia d'oferta.

Si aquestes dues coses són certes, la **Tasca** també s'hauria de configurar com a imputable. 


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
No es pot definir </p>
            </td>
            <td width="350" valign="top">
                <p>
Facturació en un valor real de temps: Imputable </p>
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
Imputable </p>
            </td>
            <td width="350" valign="top">
                <p>
Facturació en un valor real de temps: Imputable </p>
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
No es pot definir </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Imputable</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
No es pot definir </p>
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
No es pot definir </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>No imputable</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
No es pot definir </p>
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
No es pot definir </p>
            </td>
            <td width="65" valign="top">
                <p>
No es pot definir </p>
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
No es pot definir </p>
            </td>
            <td width="65" valign="top">
                <p>
No es pot definir </p>
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
No es pot definir </p>
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
No es pot definir </p>
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
