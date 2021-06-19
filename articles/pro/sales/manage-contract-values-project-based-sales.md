---
title: Informació general de les línies de contracte basades en projectes
description: Aquest tema proporciona informació sobre com treballar amb línies de contracte basades en projectes.
author: rumant
ms.date: 10/28/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 8af32b0475650db9c5862ea23d185588a631ade6
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003124"
---
# <a name="project-based-contract-lines-overview"></a>Informació general de les línies de contracte basades en projectes

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

Les línies de contracte basades en projectes al Dynamics 365 Project Operations estan dissenyades per contenir l'estimació i els acords de facturació per a components específics del treball del projecte en una interacció. L'estructura d'una línia de contracte basada en projectes s'amplia per a les estimacions del projecte i els escenaris de facturació amb els següents conceptes:

- Mètode de facturació
- Assignació de projectes i tasques
- Classes de transaccions incloses
- Límit que no s’ha de superar
- Configuració de la imputabilitat
- Estimacions amb detalls de línia de contracte
- Clients de línia de contracte

A la taula següent s'inclouen els camps de la pestanya **General** de les línies de contracte basades en projectes que ajuden a configurar la base per a ajustaments detallats, d'estimacions des de zero i facturació per al treball basat en el projecte.

| Camp | Descripció | Impacte descendent |
| --- | --- | --- |
| **Nom** | Nom de la línia de contracte. Això identifica el component discret del contracte que s'estima. Per a un contracte de projecte creat a partir d'una oferta, aquest valor es copia d'un valor corresponent de la línia d'oferta basada en el projecte. | Nom que es copia a la línia de factura del projecte que es crea a partir d'aquesta línia de contracte quan es crea la factura. |
| **Mètode de facturació** | En un contracte de projecte creat a partir d'una oferta, aquest valor es copia del camp corresponent de la línia d'oferta. Aquest és un conjunt d'opcions que representa els dos principals models de contractació admesos pel Project Operations:</br>- **Preu fix**</br>- **Temps i material** | En funció del mètode de facturació de la línia de contracte a la qual es fa referència, es processarà la transacció de valors reals. Si la línia de contracte a la qual fa referència el valor real té un mètode de facturació de temps i material, es creen registres de cost i de valor real de vendes no facturades. Si la línia de contracte a la qual fa referència el valor real té un mètode de facturació de preu fix, només es crea un valor real de cost. |
| **Project** | Utilitzeu aquest camp per identificar el projecte que s'utilitzarà per lliurar el treball en aquesta interacció. | Aquest valor s'utilitzarà conjuntament amb **Tasques incloses** i **Classes de transaccions incloses** per resoldre la referència de línia de contracte en un registre de línia real o de previsió. |
| **Tasques incloses** | Indica si aquesta línia de contracte inclou totes les tasques del projecte per al projecte seleccionat o només un subconjunt de les tasques. És un conjunt d'opcions que té els següents valors possibles:</br>- **Totes les tasques de projecte**</br>- **Només les tasques de projecte seleccionades**. Un valor en blanc en aquest camp és igual a seleccionar **Totes les tasques del projecte**. | Si se selecciona **Només les tasques seleccionades**, podeu seleccionar tasques específiques i associar-les a aquesta línia de contracte a la pestanya **Configuració de la facturació de tasques** de la pàgina **Projecte**. El valor s'utilitzarà conjuntament amb **Projecte** i **Classes de transacció incloses** per resoldre la referència de la línia de contracte en un registre de línia real o estimat. |
| **Inclou el temps** | Un valor **Sí**/**No** indica si les transaccions de temps o els costos laborals del projecte seleccionat s'inclouran en aquesta línia de contracte. Un valor **No** indica que les transaccions de temps o els costos laborals no s'inclouran en aquesta línia de contracte. Un valor **Sí** indica que s'inclouran. | Aquest valor s'utilitza conjuntament amb el projecte per resoldre la referència de línia de contracte en un registre real o de línia de previsió. |
| **Inclou la despesa** | Un valor **Sí**/**No** indica si els costos de despeses del projecte seleccionat s'inclouran a la previsió en aquesta línia de contracte. Un valor **No** indica que el cost de despesa no s'inclourà en aquesta línia de contracte. Un valor **Sí** indica que s'inclourà. | Aquest valor s'utilitza conjuntament amb el projecte per resoldre la referència de línia de contracte en un registre real o de línia de previsió. |
| **Inclou els materials** | Un valor **Sí**/**No** indica si els costos de materials del projecte seleccionat s'inclouran a la previsió en aquesta línia de contracte. Un valor **No** indica que els costos de materials no s'inclouran en aquesta línia del contracte. Un valor **Sí** indica que s'inclourà. | Aquest valor s'utilitza conjuntament amb el projecte per resoldre la referència de línia de contracte en un registre real o de línia de previsió. |
| **Inclou la taxa** | Un valor **Sí**/**No** indica si les tarifes del projecte seleccionat s'inclouran a la previsió en aquesta línia de contracte. Un valor **No** indica que els càrrecs no s'inclouran en aquesta línia de contracte. Un valor **Sí** indica que s'inclouran. | Aquest valor s'utilitza conjuntament amb el projecte per resoldre la referència de línia de contracte en un registre real o de línia de previsió. |
| **Import contractat** | En una línia de contracte de preu fix, aquest import és el valor acordat que es facturarà al client per a tots els components de treball associats amb aquesta línia de contracte. En una línia de contracte de temps i material, aquest import és un valor estimat del que es facturarà al client per a tots els components de treball associats a aquesta línia de contracte. En un contracte de projecte creat a partir d'una oferta, aquest valor es copia del camp corresponent de la línia d'oferta. Quan una línia de contracte basada en un projecte té detalls de la línia, aquest camp no es pot editar i es resumeix a partir de l'import dels detalls de la línia de contracte. | Quan la línia de contracte té detalls de la línia, aquest valor es pot modificar canviant els imports als detalls de la línia. En una línia de contracte de preu fix, aquest valor s'utilitza per generar l'import abans de l'impost a les fites de facturació periòdiques. |
| **Impost estimat** | L'usuari pot editar aquest camp per introduir l'import d'impostos estimat en la línia de contracte. Quan una línia de contracte basada en un projecte té detalls de la línia, aquest camp no es pot editar i es resumeix a partir de l'import d'impostos dels detalls de la línia de contracte. | Quan la línia de contracte té detalls de la línia, aquest valor es pot modificar canviant els imports d'impostos als detalls de la línia. En una línia de contracte de preu fix, aquest valor s'utilitza per generar l'impost a les fites de facturació periòdiques. |
| **Import contractat després d’impostos** | Import de la línia de contracte després de l'impost. Aquest camp és de només lectura i es calcula com a **Import contractat + Impostos**. | En una línia de contracte de preu fix, aquest valor s'utilitza per generar fites de facturació periòdiques. |
| **Límit que no s’ha de superar** | L'usuari pot editar aquest camp i només està disponible en línies de contracte basades en projectes que tenen el mètode de facturació definit en temps i material. | L'usuari pot editar aquest camp. Quan un valor real de temps i material fa referència a aquesta línia de contracte per temps i material, l'import del valor real s'avalua amb el límit que no es pot superar de la línia de contracte. Aquesta avaluació es completa un cop comptabilitzats els imports ja gastats i compromesos. |
| **Pressupost del client** | Aquest camp és editable i es copia del camp corresponent de la línia d'oferta si el contracte s'ha creat a partir d'una oferta. | Aquest camp només s'utilitza per a informació i no té cap importància descendent. |

## <a name="validation-rules-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a>Regles de validació per a les opcions a la pestanya General de línies de contracte basades en projectes

Regla 1: si el camp **Tasques incloses** està en blanc o està definit en **Totes les tasques del projecte**, totes les tasques del projecte s'inclouen a la línia de contracte.

Regla 2: quan el camp **Tasques incloses** estigui en blanc o definit explícitament en **Totes les tasques del projecte**, un projecte i una determinada classe de transacció només es poden incloure en una línia de contracte basada en projectes d'un contracte.

Regla 3: quan el camp **Tasques incloses** estigui definit en **Només les tasques del projecte seleccionades**, un projecte i una determinada classe de transacció només es poden incloure en diverses línies de contracte basades en projectes d'un contracte.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="43" valign="top">
                <p>
                    <strong>Contracte</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Línia de contracte</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Project</strong>
                </p>
            </td>
            <td width="67" valign="top">
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
                    <strong>Inclou els materials</strong>
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
            <td width="53" valign="top">
                <p>
                    <strong>Vàlid/No és vàlid</strong>
                </p>
            </td>
            <td width="250" valign="top">
                <p>
                    <strong>Motiu</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
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
            <td width="42" valign="top">
                <p>
Sí </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
No és vàlid </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Infracció de la regla 2. El temps, les despeses, els materials i les tarifes del projecte P1 s'inclouen a les línies de contracte CL1 i CL2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
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
            <td width="42" valign="top">
                <p>
Sí </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
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
            <td width="42" valign="top">
                <p>
Sí </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
No és vàlid </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Infracció de la regla 2. El temps, els materials i les tarifes del projecte P1 s'inclouen a les línies de contracte CL1 i CL2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
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
            <td width="42" valign="top">
                <p>
Sí </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
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
            <td width="42" valign="top">
                <p>
Sí </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Vàlida </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
El temps, els materials i les tarifes del projecte P1 s'inclouen a CL1.
                </p>
                <ul>
                    <li>
La despesa en el projecte P1 s'inclou a CL2.
                    </li>
                </ul>
                <p>
No se superposa el que s'inclou a cada línia de contracte i, per tant, és vàlid.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
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
            <td width="42" valign="top">
                <p>
No </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
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
            <td width="42" valign="top">
                <p>
Sí </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
No és vàlid </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Infracció de la regla núm. 2 </p>
                <p>
El C1 inclou temps, materials, despeses i tarifes en un subconjunt de tasques al projecte P1.
                </p>
                <p>
CL2 inclou temps, materials, despeses i tarifes per a tot el projecte P1 i, per tant, se superposa amb el que s'inclou a C1.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
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
            <td width="42" valign="top">
                <p>
Sí </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
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
            <td width="42" valign="top">
                <p>
Sí </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Vàlida </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Segons la regla 3 </p>
                <p>
El C1 inclou temps, despeses, materials i tarifes en un subconjunt de tasques al projecte P1.
                </p>
                <p>
El CL2 inclou temps, despeses, materials i tarifes per a un subconjunt de tasques al projecte P1.
                </p>
                <p>
L'única validació addicional és per al subconjunt de tasques de CL1, que és diferent del subconjunt de tasques de CL2 per assegurar que no hi ha superposicions. Això ho fa el sistema quan s'associen les tasques.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
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
            <td width="42" valign="top">
                <p>
Sí </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
