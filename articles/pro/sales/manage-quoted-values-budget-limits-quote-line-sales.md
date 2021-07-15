---
title: Informació general de les línies d'oferta basades en projectes
description: En aquest tema s'ofereix informació sobre l'ús de línies d'oferta basades en projectes per al treball del projecte.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: b7076a4b9280472f8c30d0b58c3aa9b9bc86d651
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369859"
---
# <a name="project-based-quote-lines-overview"></a>Informació general de les línies d'oferta basades en projectes 

_**S'aplica a:** Implementació bàsica: tracte de facturació proforma, Project Operations per a escenaris basats en recursos/sense cotització_

Les línies d'oferta basades en projectes estan dissenyades per ajudar a estimar el treball del projecte en una interacció. L'estructura d'una línia d'oferta basada en projectes s'amplia per a estimacions de projecte amb els conceptes següents:

- Mètode de facturació
- Assignació de projectes i tasques
- Classes de transaccions incloses
- Límit que no s’ha de superar
- Configuració de la imputabilitat
- Estimació mitjançant detalls de la línia d'oferta
- Clients de la línia d’oferta

A la taula següent es proporciona informació sobre els camps de la pestanya **General** de la línia d'oferta basada en projectes. Aquests camps ajuden a configurar la base per a una estimació detallada i des de zero per al treball del projecte.

| **Camp** | **Descripció** | **Impacte descendent** |
| --- | --- | --- |
| Nom | El nom de la línia d'oferta que us ajuda a identificar el component discret de l'oferta que s'està calculant. | Es copia a la línia de contracte del projecte que es crea des d'aquesta línia d'oferta en guanyar l'oferta. |
| Mètode de facturació | En una oferta creada a partir d'una oportunitat, aquest valor es copia des del camp corresponent a la línia d'oportunitat. Aquest camp inclou els dos models de contracte principals compatibles amb el Dynamics 365 Project Operations:</br>- Preu fix</br>- Temps i material.| Aquest valor es copia a la línia de contracte del projecte que es crea a partir d'aquesta línia d'oferta quan es guanya l'oferta. |
| Project | Utilitzeu aquest camp opcional per identificar el projecte que s'utilitzarà per lliurar el treball en aquesta interacció. Quan un projecte s'assigna a una línia d'oferta, ajuda amb la creació de tasques imputables i també amb l'aportació d'una estimació basada en projectes a la línia d'oferta com a detalls de la línia d'oferta. Quan un projecte no està assignat a una línia d'oferta basada en projectes, la estimació s'ha de crear manualment creant cada detall de la línia d'oferta. | Aquest valor es copia a la línia de contracte del projecte que es crea a partir d'aquesta línia d'oferta quan es guanya l'oferta.|
| Tasques incloses | Indica si aquesta línia d'oferta s'utilitza per a totes o algunes de les tasques del projecte seleccionat. Aquest camp té els següents valors possibles:</br>- Totes les tasques de projecte</br>- Només les tasques de projecte seleccionades</br>Un valor en blanc en aquest camp equival a l'opció **Totes les tasques del projecte**. | Quan se selecciona **Només tasques de projecte seleccionades** a la pàgina de projecte, la pestanya **Configuració de facturació de la tasca** us permet seleccionar tasques específiques per associar-les a aquesta línia d'oferta. Aquest valor es copia a la línia de contracte del projecte que es crea a partir d'aquesta línia d'oferta quan es guanya l'oferta. |
| Inclou el temps | Un valor **Sí**/**No** indica si les transaccions de temps o els costos laborals del projecte seleccionat s'inclouran a la previsió en aquesta línia d'oferta. Un valor **No** indica que les transaccions de temps o els costos de treball no s'inclouran a l'estimació en aquesta línia d'oferta. Un valor **Sí** indica que les transaccions de temps o els costos de treball s'inclouran a l'estimació en aquesta línia d'oferta. | Aquest valor es copia a la línia de contracte del projecte que es crea a partir d'aquesta línia d'oferta quan es guanya l'oferta. |
| Inclou la despesa | Un valor **Sí**/**No** indica si els costos de despeses del projecte seleccionat s'inclouran a la previsió en aquesta línia d'oferta. Un valor **No** indica que el cost de despesa no s'inclourà a l'estimació en aquesta línia d'oferta. Un valor **Sí** indica que el cost de despesa s'inclourà a l'estimació en aquesta línia d'oferta. | Aquest valor es copia a la línia de contracte del projecte que es crea a partir d'aquesta línia d'oferta quan es guanya l'oferta. |
| Inclou el material | Un valor **Sí**/**No** indica si els costos de materials del projecte seleccionat s'inclouran a la previsió en aquesta línia d'oferta. Un valor **No** indica que els costos de materials no s'inclouran a la previsió en aquesta línia d'oferta. Un valor **Sí** indica que els costos de materials s'inclouran a la previsió en aquesta línia d'oferta. | Aquest valor es copia a la línia de contracte del projecte que es crea a partir d'aquesta línia d'oferta quan es guanya l'oferta. |
| Inclou la taxa | Un valor **Sí**/**No** indica si les tarifes del projecte seleccionat s'inclouran a la previsió en aquesta línia d'oferta. Un valor **No** indica que les tarifes no s'inclouran a l'estimació en aquesta línia d'oferta. Un valor **Sí** indica que les tarifes s'inclouran a l'estimació en aquesta línia d'oferta. | Aquest valor es copia a la línia de contracte del projecte que es crea a partir d'aquesta línia d'oferta quan es guanya l'oferta. |
| Import de l’oferta | Aquest és l'import que s'oferirà al client per a tots els treballs previstos en aquesta línia d'oferta basada en projectes. En una oferta creada a partir d'una oportunitat, aquest valor es copia des del camp **Pressupost de client** a la línia d'oportunitat. Quan la línia d'oferta basada en projectes té detalls de línia, aquest camp està bloquejat per editar-lo i es resumeix de l'import dels detalls de la línia d'oferta. | Aquest valor es copia a la línia de contracte del projecte que es crea a partir d'aquesta línia d'oferta quan es guanya l'oferta. |
| Impost estimat | Es tracta d'un camp editable per a l'usuari que afegirà l'import de l'impost previst a la línia d'oferta. Quan una línia d'oferta basada en projectes té detalls de línia, aquest camp està bloquejat per editar-lo i es resumeix de l'import d'impostos dels detalls de la línia d'oferta. | Aquest valor es copia a la línia de contracte del projecte que es crea a partir d'aquesta línia d'oferta quan es guanya l'oferta. |
| Import de l’oferta després d’impostos | Aquest camp és l'import de la línia d'oferta després de l'impost i és només de lectura. L'import d'aquest camp es calcula com a *Import de l'oferta + impost*. | Aquest valor es copia a la línia de contracte del projecte que es crea a partir d'aquesta línia d'oferta quan es guanya l'oferta. |
| Límit que no s’ha de superar | Aquest camp és editable i només està disponible a les línies d'oferta basades en el projecte que tenen un mètode de facturació **Temps i material**. | Aquest valor es copia a la línia de contracte del projecte que es crea a partir d'aquesta línia d'oferta quan es guanya l'oferta. |
| Pressupost del client | Aquest camp és editable i es copia des del camp corresponent a la línia d'oportunitat si l'oferta es va crear a partir d'una oportunitat. | Aquest valor es copia a la línia de contracte del projecte que es crea a partir d'aquesta línia d'oferta quan es guanya l'oferta. |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a>Regles de validació per als camps de la pestanya General de línies d'oferta basades en projectes

**Regla 1**: si el camp **Tasques incloses** està en blanc o si està definit com a **Totes les tasques del projecte**, s'inclou un projecte a la línia d'oferta.

**Regla 2**: si el camp **Tasques incloses** està en blanc o si està definit com a **Totes les tasques del projecte**, un projecte i una determinada classe de transacció només es poden incloure en una línia d'oferta basada en projectes d'una oferta.

**Regla 3**: si el camp **Tasques incloses** està definit com a **Només les tasques del projecte seleccionades**, un projecte i una determinada classe de transacció es poden incloure en diverses línies d'oferta basades en projectes d'una oferta.

**Regla 4**: si una oportunitat té diverses ofertes, pot haver-hi línies d'ofertes de diverses ofertes que facin referència al mateix projecte i que incloguin la mateixa classe de transacció.

**Regla 5**: si les ofertes no pertanyen a la mateixa oportunitat, no poden incloure el mateix projecte i classe de transacció.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="59" valign="top">
                <p>
                    <strong>Oportunitat</strong>
                </p>
            </td>
            <td width="39" valign="top">
                <p>
                    <strong>Oferta</strong>
                </p>
            </td>
            <td width="40" valign="top">
                <p>
                    <strong>Línia d’oferta</strong>
                </p>
            </td>
            <td width="41" valign="top">
                <p>
                    <strong>Project</strong>
                </p>
            </td>
            <td width="77" valign="top">
                <p>
                    <strong>Tasques incloses</strong>
                </p>
            </td>
            <td width="45" valign="top">
                <p>
                    <strong>Inclou el temps</strong>
                </p>
            </td>
            <td width="46" valign="top">
                <p>
                    <strong>Inclou la despesa</strong>
                </p>
            </td>
            <td width="43" valign="top">
                <p>
                    <strong>Inclou el material</strong>
                </p>
            </td>
            <td width="41" valign="top">
                <p>
                    <strong>Inclou</strong>
                </p>
                <p>
                    <strong>Tarifa</strong>
                </p>
            </td>
            <td width="49" valign="top">
                <p>
                    <strong>Vàlid/No és vàlid</strong>
                </p>
            </td>
            <td width="200" valign="top">
                <p>
                    <strong>Motiu</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
T1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
En blanc </p>
            </td>
            <td width="45" valign="top">
                <p>
Sí </p>
            </td>
            <td width="46" valign="top">
                <p>
Sí </p>
            </td>
            <td width="43" valign="top">
                <p>
Sí </p>
            </td>
            <td width="41" valign="top">
                <p>
Sí </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
No és vàlid </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Infracció de la regla 2. El temps, les despeses i les tarifes del projecte P1 s'inclouen a les línies d'oferta QL1 i QL2 </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
T1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
En blanc </p>
            </td>
            <td width="45" valign="top">
                <p>
Sí </p>
            </td>
            <td width="46" valign="top">
                <p>
Sí </p>
            </td>
            <td width="43" valign="top">
                <p>
Sí </p>
            </td>
            <td width="41" valign="top">
                <p>
Sí </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
T1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
En blanc </p>
            </td>
            <td width="45" valign="top">
                <p>
Sí </p>
            </td>
            <td width="46" valign="top">
                <p>
No </p>
            </td>
            <td width="43" valign="top">
                <p>
Sí </p>
            </td>
            <td width="41" valign="top">
                <p>
Sí </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
No és vàlid </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Infracció de la regla 2. El temps, el material i les tarifes del projecte P1 s'inclouen a les línies d'oferta QL1 i QL2 </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
T1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
En blanc </p>
            </td>
            <td width="45" valign="top">
                <p>
Sí </p>
            </td>
            <td width="46" valign="top">
                <p>
Sí </p>
            </td>
            <td width="43" valign="top">
                <p>
Sí </p>
            </td>
            <td width="41" valign="top">
                <p>
Sí </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
T1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
En blanc </p>
            </td>
            <td width="45" valign="top">
                <p>
Sí </p>
            </td>
            <td width="46" valign="top">
                <p>
No </p>
            </td>
            <td width="43" valign="top">
                <p>
Sí </p>
            </td>
            <td width="41" valign="top">
                <p>
Sí </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Vàlida </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
El temps, el material i les tarifes del projecte P1 s'inclouen a QL1 <br>
La despesa del projecte P1 s'inclou a QL2 <br>
No se superposa el que s'inclou a cada línia d'oferta i, per tant, és vàlid.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
T1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
En blanc </p>
            </td>
            <td width="45" valign="top">
                <p>
No </p>
            </td>
            <td width="46" valign="top">
                <p>
Sí </p>
            </td>
            <td width="43" valign="top">
                <p>
No </p>
            </td>
            <td width="41" valign="top">
                <p>
No </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
T1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Només les tasques seleccionades </p>
            </td>
            <td width="45" valign="top">
                <p>
Sí </p>
            </td>
            <td width="46" valign="top">
                <p>
Sí </p>
            </td>
            <td width="43" valign="top">
                <p>
Sí </p>
            </td>
            <td width="41" valign="top">
                <p>
Sí </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
No és vàlid </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Infracció de la regla núm. 2 </p>
                <p>
El Q1 inclou temps, material, despeses i tarifes en un subconjunt de tasques al projecte P1 </p>
                <p>
QL2 inclou temps, despeses i tarifes per a tot el projecte P1 i, per tant, se superposa amb el que s'inclou a Q1.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
T1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
En blanc </p>
            </td>
            <td width="45" valign="top">
                <p>
Sí </p>
            </td>
            <td width="46" valign="top">
                <p>
Sí </p>
            </td>
            <td width="43" valign="top">
                <p>
Sí </p>
            </td>
            <td width="41" valign="top">
                <p>
Sí </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
T1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Només les tasques seleccionades </p>
            </td>
            <td width="45" valign="top">
                <p>
Sí </p>
            </td>
            <td width="46" valign="top">
                <p>
Sí </p>
            </td>
            <td width="43" valign="top">
                <p>
Sí </p>
            </td>
            <td width="41" valign="top">
                <p>
Sí </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Vàlida </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Segons la regla núm. 3, </p>
                <p>
El Q1 inclou temps, material, despeses i tarifes en un subconjunt de tasques al projecte P1.
                </p>
                <p>
El QL2 inclou temps, material, despeses i tarifes per a un subconjunt de tasques al projecte P1.
                </p>
                <p>
L'única validació addicional és per al subconjunt de tasques de QL1, que és diferent del subconjunt de tasques de QL2 per assegurar que no hi ha superposició. Això ho fa el sistema quan s'associen les tasques.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
T1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Només les tasques seleccionades </p>
            </td>
            <td width="45" valign="top">
                <p>
Sí </p>
            </td>
            <td width="46" valign="top">
                <p>
Sí </p>
            </td>
            <td width="43" valign="top">
                <p>
Sí </p>
            </td>
            <td width="41" valign="top">
                <p>
Sí </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
T1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Totes les tasques del projecte o en blanc </p>
            </td>
            <td width="45" valign="top">
                <p>
Sí </p>
            </td>
            <td width="46" valign="top">
                <p>
Sí </p>
            </td>
            <td width="43" valign="top">
                <p>
Sí </p>
            </td>
            <td width="41" valign="top">
                <p>
Sí </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Vàlida </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Segons la regla núm. 5, Q1 i Q2 són dues ofertes per a la mateixa oportunitat, de manera que poden calcular ambdós els mateixos components d'un projecte.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
T2 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Totes les tasques del projecte o en blanc </p>
            </td>
            <td width="45" valign="top">
                <p>
Sí </p>
            </td>
            <td width="46" valign="top">
                <p>
Sí </p>
            </td>
            <td width="43" valign="top">
                <p>
Sí </p>
            </td>
            <td width="41" valign="top">
                <p>
Sí </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
T1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Totes les tasques del projecte o en blanc </p>
            </td>
            <td width="45" valign="top">
                <p>
Sí </p>
            </td>
            <td width="46" valign="top">
                <p>
Sí </p>
            </td>
            <td width="43" valign="top">
                <p>
Sí </p>
            </td>
            <td width="41" valign="top">
                <p>
Sí </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
No és vàlid </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Segons la regla núm. 4, Q1 i Q2 són dues ofertes d'oportunitats diferents, de manera que no poden calcular els mateixos components del mateix projecte.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O2 </p>
            </td>
            <td width="39" valign="top">
                <p>
T1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Totes les tasques del projecte o en blanc </p>
            </td>
            <td width="45" valign="top">
                <p>
Sí </p>
            </td>
            <td width="46" valign="top">
                <p>
Sí </p>
            </td>
            <td width="43" valign="top">
                <p>
Sí </p>
            </td>
            <td width="41" valign="top">
                <p>
Sí </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
