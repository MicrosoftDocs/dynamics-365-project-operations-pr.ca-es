---
title: Informació general de les línies d'oferta basades en projectes (bàsic)
description: En aquest tema s'ofereix informació sobre l'ús de línies d'oferta basades en projectes per al treball del projecte. (Pro)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: be1663c0d226fa19fe4b9df566e16d215f1fc08e
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181080"
---
# <a name="project-based-quote-lines-overview---lite"></a>Informació general de les línies d'oferta basades en projectes (bàsic)

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_

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
| Nom | Nom de la línia d'oferta que hauria d'ajudar-vos a identificar el component discret de l'oferta que s'està estimant. | Es copia a la línia de contracte del projecte que es crea des d'aquesta línia d'oferta en guanyar l'oferta. |
| Mètode de facturació | En una oferta creada a partir d'una oportunitat, aquest valor es copia des del camp corresponent a la línia d'oportunitat. Aquest camp inclou els dos models principals de contractació admesos pel Dynamics 365 Project Operations:</br>- Preu fix</br>- Temps i material.| El valor d'aquest camp es copia a la línia de contracte del projecte que es crea des d'aquesta línia d'oferta en guanyar l'oferta. |
| Project | Utilitzeu aquest camp opcional per identificar el projecte que s'utilitzarà per lliurar el treball en aquesta interacció. Quan un projecte s'assigna a una línia d'oferta, ajuda amb la creació de tasques imputables i també amb l'aportació d'una estimació basada en projectes a la línia d'oferta com a detalls de la línia d'oferta. Quan un projecte no està assignat a una línia d'oferta basada en projectes, la estimació s'ha de crear manualment creant cada detall de la línia d'oferta. | El valor d'aquest camp es copia a la línia de contracte del projecte que es crea des d'aquesta línia d'oferta en guanyar l'oferta.|
| Tasques incloses | Indica si aquesta línia d'oferta s'utilitza per a totes o algunes de les tasques del projecte seleccionat. Aquest camp té els següents valors possibles:</br>- Totes les tasques de projecte</br>- Només les tasques de projecte seleccionades</br>Un valor en blanc en aquest camp equival a l'opció **Totes les tasques del projecte**. | Quan **Només les tasques de projecte seleccionades** se seleccionen a la pàgina del projecte, la pestanya **Configuració de facturació de la tasca** us permet seleccionar tasques específiques per associar-les a aquesta línia d'oferta. El valor d'aquest camp es copia a la línia de contracte del projecte que es crea des d'aquesta línia d'oferta en guanyar l'oferta. |
| Inclou el temps | Una marca **Sí**/**No** indica si les transaccions de temps o els costos de treball del projecte seleccionat s'inclouran a l'estimació en aquesta línia d'oferta. Un valor **No** indica que les transaccions de temps o els costos de treball no s'inclouran a l'estimació en aquesta línia d'oferta. Un valor **Sí** indica que les transaccions de temps o els costos de treball s'inclouran a l'estimació en aquesta línia d'oferta. | El valor d'aquest camp es copia a la línia de contracte del projecte que es crea des d'aquesta línia d'oferta en guanyar l'oferta. |
| Inclou la despesa | Una marca **Sí**/**No** indica si els costos de despesa del projecte seleccionat s'inclouran a l'estimació en aquesta línia d'oferta. Un valor **No** indica que el cost de despesa no s'inclourà a l'estimació en aquesta línia d'oferta. Un valor **Sí** indica que el cost de despesa s'inclourà a l'estimació en aquesta línia d'oferta. | El valor d'aquest camp es copia a la línia de contracte del projecte que es crea des d'aquesta línia d'oferta en guanyar l'oferta. |
| Inclou la taxa | Una marca **Sí**/**No** indica si les taxes del projecte seleccionat s'inclouran a l'estimació en aquesta línia d'oferta. Un valor **No** indica que les taxes no s'inclouran a l'estimació en aquesta línia d'oferta. Un valor **Sí** indica que les taxes s'inclouran a l'estimació en aquesta línia d'oferta. | El valor d'aquest camp es copia a la línia de contracte del projecte que es crea des d'aquesta línia d'oferta en guanyar l'oferta. |
| Import de l’oferta | Això és una quantitat que s'oferirà al client per a tot el treball previst en aquesta línia d'oferta basada en el projecte. En una oferta creada a partir d'una oportunitat, aquest valor es copia des del camp **Pressupost de client** a la línia d'oportunitat. Quan la línia d'oferta basada en projectes té detalls de línia, aquest camp està bloquejat per editar-lo i es resumeix de l'import dels detalls de la línia d'oferta. | El valor d'aquest camp es copia a la línia de contracte del projecte que es crea des d'aquesta línia d'oferta en guanyar l'oferta. |
| Impost estimat | Es tracta d'un camp editable per a l'usuari que afegirà l'import de l'impost previst a la línia d'oferta. Quan una línia d'oferta basada en projectes té detalls de línia, aquest camp està bloquejat per editar-lo i es resumeix de l'import d'impostos dels detalls de la línia d'oferta. | El valor d'aquest camp es copia a la línia de contracte del projecte que es crea des d'aquesta línia d'oferta en guanyar l'oferta. |
| Import de l’oferta després d’impostos | Aquest camp és l'import de la línia d'oferta després de l'impost i és només de lectura. L'import d'aquest camp es calcula com a *Import de l'oferta + impost*. | El valor d'aquest camp es copia a la línia de contracte del projecte que es crea des d'aquesta línia d'oferta en guanyar l'oferta. |
| Límit que no s’ha de superar | Aquest camp és editable i només està disponible a les línies d'oferta basades en el projecte que tenen un mètode de facturació **Temps i material**. | El valor d'aquest camp es copia a la línia de contracte del projecte que es crea des d'aquesta línia d'oferta en guanyar l'oferta. |
| Pressupost del client | Aquest camp és editable i es copia des del camp corresponent a la línia d'oportunitat si l'oferta es va crear a partir d'una oportunitat. | El valor d'aquest camp es copia a la línia de contracte del projecte que es crea des d'aquesta línia d'oferta en guanyar l'oferta. |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a>Regles de validació per als camps de la pestanya General de línies d'oferta basades en projectes

**Regla 1**: si el camp **Tasques incloses** està en blanc o si està definit com a **Totes les tasques del projecte**, s'inclou un projecte a la línia d'oferta.

**Regla 2**: si el camp **Tasques incloses** està en blanc o si està definit com a **Totes les tasques del projecte**, un projecte i una determinada classe de transacció només es poden incloure en una línia d'oferta basada en projectes d'una oferta.

**Regla 3**: si el camp **Tasques incloses** està definit com a **Només les tasques del projecte seleccionades**, un projecte i una determinada classe de transacció es poden incloure en diverses línies d'oferta basades en projectes d'una oferta.

**Regla 4**: si una oportunitat té diverses ofertes, pot haver-hi línies d'ofertes de diverses ofertes que facin referència al mateix projecte i que incloguin la mateixa classe de transacció.

**Regla 5**: si les ofertes no pertanyen a la mateixa oportunitat, no poden incloure el mateix projecte i classe de transacció.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p>
                    <strong>Oportunitat</strong>
                </p>
            </td>
            <td width="41" valign="top">
                <p>
                    <strong>Oferta</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Línia d’oferta</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Project</strong>
                </p>
            </td>
            <td width="90" valign="top">
                <p>
                    <strong>Tasques incloses</strong>
                </p>
            </td>
            <td width="48" valign="top">
                <p>
                    <strong>Inclou el temps</strong>
                </p>
            </td>
            <td width="48" valign="top">
                <p>
                    <strong>Inclou la despesa</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Inclou</strong>
                </p>
                <p>
                    <strong>Tarifa</strong>
                </p>
            </td>
            <td width="54" valign="top">
                <p>
                    <strong>Vàlid/No és vàlid</strong>
                </p>
            </td>
            <td width="308" valign="top">
                <p>
                    <strong>Motiu</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
T1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
En blanc </p>
            </td>
            <td width="48" valign="top">
                <p>
Sí </p>
            </td>
            <td width="48" valign="top">
                <p>
Sí </p>
            </td>
            <td width="42" valign="top">
                <p>
Sí </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
No és vàlid </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Infracció de la regla 2. El temps, les despeses i els impostos en el projecte P1 s'inclouen a les línies d'oferta QL1 i QL2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
T1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
En blanc </p>
            </td>
            <td width="48" valign="top">
                <p>
Sí </p>
            </td>
            <td width="48" valign="top">
                <p>
Sí </p>
            </td>
            <td width="42" valign="top">
                <p>
Sí </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
T1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
En blanc </p>
            </td>
            <td width="48" valign="top">
                <p>
Sí </p>
            </td>
            <td width="48" valign="top">
                <p>
No </p>
            </td>
            <td width="42" valign="top">
                <p>
Sí </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
No és vàlid </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Infracció de la regla 2. El temps i els impostos en el projecte P1 s'inclouen a les línies d'oferta QL1 i QL2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
T1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
En blanc </p>
            </td>
            <td width="48" valign="top">
                <p>
Sí </p>
            </td>
            <td width="48" valign="top">
                <p>
Sí </p>
            </td>
            <td width="42" valign="top">
                <p>
Sí </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
T1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
En blanc </p>
            </td>
            <td width="48" valign="top">
                <p>
Sí </p>
            </td>
            <td width="48" valign="top">
                <p>
No </p>
            </td>
            <td width="42" valign="top">
                <p>
Sí </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
Vàlid </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                  <p>
El temps i els impostos en el projecte P1 s'inclouen a QL1.
La despesa en el projecte P1 s'inclou a QL2.
No se superposa el que s'inclou a cada línia d'oferta i és vàlid.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
T1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
En blanc </p>
            </td>
            <td width="48" valign="top">
                <p>
No </p>
            </td>
            <td width="48" valign="top">
                <p>
Sí </p>
            </td>
            <td width="42" valign="top">
                <p>
No </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
T1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Només les tasques seleccionades </p>
            </td>
            <td width="48" valign="top">
                <p>
Sí </p>
            </td>
            <td width="48" valign="top">
                <p>
Sí </p>
            </td>
            <td width="42" valign="top">
                <p>
Sí </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
No és vàlid </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Infracció de la regla 2 anterior </p>
                <p>
Q1 inclou el temps, les despeses i els impostos d'un subconjunt de tasques del projecte P1.
                </p>
                <p>
QL2 inclou el temps, les despeses i els impostos per a tot el projecte P1 i se superposa amb el que s'inclou a Q1.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
T1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
En blanc </p>
            </td>
            <td width="48" valign="top">
                <p>
Sí </p>
            </td>
            <td width="48" valign="top">
                <p>
Sí </p>
            </td>
            <td width="42" valign="top">
                <p>
Sí </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
T1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Només les tasques seleccionades </p>
            </td>
            <td width="48" valign="top">
                <p>
Sí </p>
            </td>
            <td width="48" valign="top">
                <p>
Sí </p>
            </td>
            <td width="42" valign="top">
                <p>
Sí </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
Vàlid </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Segons la regla 3 anterior, </p>
                <p>
Q1 inclou el temps, les despeses i els impostos d'un subconjunt de tasques del projecte P1.
                </p>
                <p>
QL2 inclou el temps, les despeses i els impostos d'un subconjunt de tasques del projecte P1.
                </p>
                <p>
L'única validació addicional és pel que fa al subconjunt de tasques a QL1 que són diferents del subconjunt de tasques de QL2. Això assegura que no hi ha cap superposició. Això ho fa el sistema quan s'associen les tasques.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
T1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Només les tasques seleccionades </p>
            </td>
            <td width="48" valign="top">
                <p>
Sí </p>
            </td>
            <td width="48" valign="top">
                <p>
Sí </p>
            </td>
            <td width="42" valign="top">
                <p>
Sí </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
T1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Totes les tasques del projecte o en blanc </p>
            </td>
            <td width="48" valign="top">
                <p>
Sí </p>
            </td>
            <td width="48" valign="top">
                <p>
Sí </p>
            </td>
            <td width="42" valign="top">
                <p>
Sí </p>
            </td>
            <td width="54" valign="top">
                <p>
Vàlid </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Segons la regla 5, Q1 i Q2 són dues ofertes de la mateixa oportunitat, per la qual cosa poden estimar-se per als mateixos components d'un projecte.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
T2 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Totes les tasques del projecte o en blanc </p>
            </td>
            <td width="48" valign="top">
                <p>
Sí </p>
            </td>
            <td width="48" valign="top">
                <p>
Sí </p>
            </td>
            <td width="42" valign="top">
                <p>
Sí </p>
            </td>
            <td width="54" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
T1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Totes les tasques del projecte o en blanc </p>
            </td>
            <td width="48" valign="top">
                <p>
Sí </p>
            </td>
            <td width="48" valign="top">
                <p>
Sí </p>
            </td>
            <td width="42" valign="top">
                <p>
Sí </p>
            </td>
            <td width="54" valign="top">
                <p>
Vàlid </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Segons la regla 4, Q1 i Q2 són dues ofertes d'oportunitats diferents, per la qual cosa no poden estimar-se per als mateixos components d'un mateix projecte.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O2 </p>
            </td>
            <td width="41" valign="top">
                <p>
T1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Totes les tasques del projecte o en blanc </p>
            </td>
            <td width="48" valign="top">
                <p>
Sí </p>
            </td>
            <td width="48" valign="top">
                <p>
Sí </p>
            </td>
            <td width="42" valign="top">
                <p>
Sí </p>
            </td>
            <td width="54" valign="top">
                <p>
No és vàlid </p>
            </td>
        </tr>
    </tbody>
</table>

