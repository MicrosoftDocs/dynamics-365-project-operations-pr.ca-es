---
title: Informació general dels valors reals
description: Aquest tema proporciona informació sobre els valors reals del projecte.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 08/03/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: c4a3424bed704243dfb5524fa541c3fcc0899e57
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5285606"
---
# <a name="actuals-overview"></a>Informació general dels valors reals

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Els valors reals són la quantitat de treball que s'ha completat en un projecte. Els valors reals del projecte es remunten als seus documents d'origen. Aquests documents d'origen inclouen entrades de temps, despeses i del llibre diari, i també factures.

![Com es remunten els valors reals als documents d'origen](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a>Enviant una entrada de temps

Al PSA, quan s'envia una entrada de temps per a un projecte assignat a una línia de contracte de temps i materials, es creen dues línies del llibre diari. Una línia és per al cost i l'altra línia és per a les vendes no facturades. Quan s'envia una entrada de temps per a un projecte assignat a una línia de contracte de preu fix, es crea una línia del llibre diari només per al cost. 

La lògica per introduir els preus per defecte resideix a la línia del llibre diari. Tots els valors de camp d'una entrada de temps es copien a la línia del llibre diari. Aquests camps són la data de la transacció, la línia de contracte a la qual està assignada el projecte i el resultat de moneda a la llista de preus adequada. 

Els camps que afecten els preus per defecte, **com** ara Funció i **Unitat organitzativa**, fan que s'introdueixi per defecte un preu adient a la línia del llibre diari. Si afegiu un camp personalitzat a l'entrada de temps i voleu que el valor del camp es propagui a valors reals, creeu el camp a l'entitat Valors reals i utilitzeu assignacions de camps per copiar el camp de l'entrada de temps al valor real.

## <a name="submitting-an-expense-entry"></a>Enviar una entrada de despesa

Al PSA, quan s'envia una entrada de despesa per a un projecte assignat a una línia de contracte de temps i materials, es creen dues línies del llibre diari. Una línia és per al cost i l'altra línia és per a les vendes no facturades. Quan s'envia una entrada de despesa per a un projecte assignat a una línia de contracte de preu fix, es crea una línia del llibre diari només per al cost.

La lògica per a la introducció dels preus per defecte de les despeses es basa en la categoria de despeses que s'ha seleccionat a la pàgina **Entrada de despeses**. La data de la transacció, la línia de contracte a la qual està assignada el projecte i la moneda s'utilitzen per determinar la llista de preus adequada. No obstant, per al preu en si mateix, l'import que l'usuari ha introduït es defineix directament a les línies del llibre diari de despesa relacionades per al cost i les vendes per defecte.

A la versió actual del PSA, l'entrada basada en categories per a preus per unitat per defecte a les entrades de despesa no està disponible.

## <a name="using-entry-journals-to-record-costs"></a>Utilitzar llibres diaris d'entrada per registrar costos de registre

Al PSA, els llibres diaris d'entrada permeten registrar els costos o ingressos en classes de material, quota, temps, despeses o transaccions tributàries. Un llibre diari té una capçalera, línies i una acció **Confirmació**. Aquests són alguns escenaris en què podeu utilitzar un llibre diari:

- Heu de registrar els costos reals materials i les vendes d'un projecte.
- Heu d'avançar els valors reals de la transacció des d'un altre sistema al PSA.
- Heu de registrar les despeses que s'han produït en un altre sistema, com ara les despeses d'adquisició o subcontractacions.

> [!IMPORTANT]
> L'ús de diaris d'entrada per a la creació de valors reals només l'ha de fer un usuari plenament conscient de l'impacte comptable que tenen els valors reals al projecte. El motiu és que l'aplicació no valida el tipus de línia del llibre diari ni el preu relacionat que s'introdueix a la línia del llibre diari. A causa de l'impacte d'aquest tipus de llibre diari, actueu amb extremada cura en relació amb qui té accés a la creació de llibres diaris d'entrada.     


## <a name="recording-actuals-based-on-project-events"></a>Enregistrament de valors reals a partir d'esdeveniments de projecte

El PSA registra totes les transaccions financeres que es produeixen durant un projecte. Aquestes transaccions es registren com a **valors reals**. Les taules següents mostren els diferents tipus de valors reals que s'han creat, en funció de si el projecte és un projecte de temps i materials o de preu fix, si es troba a la fase de prevenda o si és un projecte intern.

**El recurs pertany a la mateixa unitat organitzativa que la unitat de contractació del projecte**

<table>
<thead>
<tr>
<th rowspan="3">Incidència</th>
<th colspan="4">Projecte facturable o venut</th>
<th rowspan="3">Projecte a la fase de prevenda</th>
<th rowspan="3">Projecte intern</th>
</tr>
<tr>
<th colspan="2">Temps i materials</th>
<th colspan="2">Preu fix</th>
</tr>
<tr>
<th>Valors reals</th>
<th>Moneda de transacció</th>
<th>Preu fix</th>
<th>Moneda de transacció</th>
</tr>
</thead>
<tbody>
<tr>
<td>Es crea una entrada de temps.</td>
<td colspan="6">No hi ha activitat a l'entitat Valors reals</td>
</tr>
<tr>
<td>S'envia una entrada de temps.</td>
<td colspan="6">No hi ha activitat a l'entitat Valors reals</td>
</tr>
<tr>
<td rowspan="2">El temps s'aprova, i no es produeix cap canvi o augment de les hores facturables durant l'aprovació.</td>
<td>Valor real de cost</td>
<td>Moneda de la unitat de contractació</td>
<td rowspan="2">Valor real de cost</td>
<td rowspan="2">Moneda de la unitat de contractació
<td rowspan="2">Valor real de cost</td>
<td rowspan="2">Valor real de cost</td>
</tr>
<tr>
<td>Valor real de les vendes no facturades - Imputable</td>
<td>Moneda del contracte del projecte</td>
</tr>
<tr>
<td rowspan="3">El temps s'aprova, i es produeix una reducció de les hores facturables durant l'aprovació.</td>
<td>Valor real de cost</td>
<td>Moneda de la unitat de contractació</td>
<td rowspan="3">Valor real de cost</td>
<td rowspan="3">Moneda de la unitat de contractació</td>
<td rowspan="3">Valor real de cost</td>
<td rowspan="3">Valor real de cost</td>
</tr>
<tr>
<td>Valor real de les vendes no facturades - Imputable per a la nova quantitat</td>
<td>Moneda del contracte del projecte</td>
</tr>
<tr>
<td>Valor real de les vendes no facturades - No imputable per la diferència</td>
<td>Moneda del contracte del projecte</td>
</tr>
<tr>
<td rowspan="2">Es confirma una factura, i no es produeix cap canvi o augment de les hores facturables.</td>
<td>Reversió de vendes no facturades</td>
<td>Moneda del contracte del projecte</td>
<td rowspan="2">Vendes facturades per fita</td>
<td rowspan="2">Moneda del contracte del projecte</td>
<td rowspan="2">No aplicable</td>
<td rowspan="2">No aplicable</td>
</tr>
<tr>
<td>Vendes facturades</td>
<td>Moneda del contracte del projecte</td>
</tr>
<tr>
<td rowspan="3">Es confirma una factura, i es produeix una disminució de les hores facturables.</td>
<td>Reversió de vendes no facturades</td>
<td>Moneda del contracte del projecte</td>
<td rowspan="3">No aplicable</td>
<td rowspan="3">No aplicable</td>
<td rowspan="3">No aplicable</td>
<td rowspan="3">No aplicable</td>
</tr>
<tr>
<td>Vendes facturades - Imputable per a la nova quantitat</td>
<td>Moneda del contracte del projecte</td>
</tr>
<tr>
<td>Vendes facturades - No imputable per la diferència</td>
<td>Moneda del contracte del projecte</td>
</tr>
<tr>
<td rowspan="2">Una factura es corregeix per augmentar la quantitat imputable.</td>
<td>Vendes facturades - Reversió</td>
<td>Moneda del contracte del projecte</td>
<td rowspan="5">
<ul>
<li>Reversió de vendes facturades per fita</li>
<li>Canvi en l'estat de la fita de <strong>Facturada</strong> a <strong>Llesta per facturar</strong></li>
</ul>
</td>
<td rowspan="5">Moneda del contracte del projecte</td>
<td rowspan="5">No aplicable</td>
<td rowspan="5">No aplicable</td>
</tr>
<tr>
<td>Vendes facturades</td>
<td>Moneda del contracte del projecte</td>
</tr>
<tr>
<td rowspan="3">Una factura es corregeix per reduir la quantitat imputable.</td>
<td>Vendes facturades - Reversió</td>
<td>Moneda del contracte del projecte</td>
</tr>
<tr>
<td>Vendes facturades per a la nova quantitat</td>
<td>Moneda del contracte del projecte</td>
</tr>
<tr>
<td>Vendes no facturades - Imputable per la diferència</td>
<td>Moneda del contracte del projecte</td>
</tr>
</tbody>
</table>

**El recurs pertany a una unitat organitzativa diferent de la unitat de contractació del projecte**

<table>
<thead>
<tr>
<th rowspan="3">Incidència</th>
<th colspan="4">Projecte facturable o venut</th>
<th rowspan="3">Projecte a la fase de prevenda</th>
<th rowspan="3">Projecte intern</th>
</tr>
<tr>
<th colspan="2">Temps i materials</th>
<th colspan="2">Preu fix</th>
</tr>
<tr>
<th>Valors reals</th>
<th>Moneda de transacció</th>
<th>Preu fix</th>
<th>Moneda de transacció</th>
</tr>
</thead>
<tbody>
<tr>
<td>Es crea una entrada de temps.</td>
<td colspan="6">No hi ha activitat a l'entitat Valors reals</td>
</tr>
<tr>
<td>S'envia una entrada de temps.</td>
<td colspan="6">No hi ha activitat a l'entitat Valors reals</td>
</tr>
<tr>
<td rowspan="4">El temps s'aprova, i no es produeix cap canvi o augment de les hores facturables durant l'aprovació.</td>
<td>Valor real de cost</td>
<td>Moneda de la unitat de contractació</td>
<td rowspan="4">Valor real de cost</td>
<td rowspan="4">Moneda de la unitat de contractació</td>
<td rowspan="4">Valor real de cost</td>
<td rowspan="4">Valor real de cost</td>
</tr>
<tr>
<td>Valor real de les vendes no facturades - Imputable</td>
<td>Moneda del contracte del projecte</td>
</tr>
<tr>
<td>Cost de la unitat de recursos</td>
<td>Moneda de la unitat de recursos</td>
</tr>
<tr>
<td>Vendes interorganitzatives</td>
<td>Moneda de la unitat de contractació</td>
</tr>
<tr>
<td rowspan="5">El temps s'aprova, i es produeix una reducció de les hores facturables durant l'aprovació.</td>
<td>Valor real de cost</td>
<td>Moneda de la unitat de contractació</td>
<td rowspan="5">Valor real de cost</td>
<td rowspan="5">Moneda de la unitat de contractació</td>
<td rowspan="5">Valor real de cost</td>
<td rowspan="5">Valor real de cost</td>
</tr>
<tr>
<td>Cost de la unitat de recursos</td>
<td>Moneda de la unitat de recursos</td>
</tr>
<tr>
<td>Vendes interorganitzatives</td>
<td>Moneda de la unitat de contractació</td>
</tr>
<tr>
<td>Valor real de les vendes no facturades - Imputable per a la nova quantitat</td>
<td>Moneda del contracte del projecte</td>
</tr>
<tr>
<td>Valor real de les vendes no facturades - No imputable per la diferència</td>
<td>Moneda del contracte del projecte</td>
</tr>
<tr>
<td rowspan="2">Es confirma una factura, i no es produeix cap canvi o augment de les hores facturables.</td>
<td>Reversió de vendes no facturades</td>
<td>Moneda del contracte del projecte</td>
<td rowspan="2">Vendes facturades per fita</td>
<td rowspan="2">Moneda del contracte del projecte</td>
<td rowspan="2">No aplicable</td>
<td rowspan="2">No aplicable</td>
</tr>
<tr>
<td>Vendes facturades</td>
<td>Moneda del contracte del projecte</td>
</tr>
<tr>
<td rowspan="3">Es confirma una factura, i es produeix una disminució de les hores facturables.</td>
<td>Reversió de vendes no facturades</td>
<td>Moneda del contracte del projecte</td>
<td rowspan="3">No aplicable</td>
<td rowspan="3">No aplicable</td>
<td rowspan="3">No aplicable</td>
<td rowspan="3">No aplicable</td>
</tr>
<tr>
<td>Vendes facturades - Imputable per a la nova quantitat</td>
<td>Moneda del contracte del projecte</td>
</tr>
<tr>
<td>Vendes facturades - No imputable per la diferència</td>
<td>Moneda del contracte del projecte</td>
</tr>
<tr>
<td rowspan="2">Una factura es corregeix per augmentar la quantitat imputable.</td>
<td>Vendes facturades - Reversió</td>
<td>Moneda del contracte del projecte</td>
<td rowspan="5">
<ul>
<li>Reversió de vendes facturades per fita</li>
<li>Canvi en l'estat de la fita de <strong>Facturada</strong> a <strong>Llesta per facturar</strong></li>
</ul>
</td>
<td rowspan="5">Moneda del contracte del projecte</td>
<td rowspan="5">No aplicable</td>
<td rowspan="5">No aplicable</td>
</tr>
<tr>
<td>Vendes facturades</td>
<td>Moneda del contracte del projecte</td>
</tr>
<tr>
<td rowspan="3">Una factura es corregeix per reduir la quantitat imputable.</td>
<td>Vendes facturades - Reversió</td>
<td>Moneda del contracte del projecte</td>
</tr>
<tr>
<td>Vendes facturades per a la nova quantitat</td>
<td>Moneda del contracte del projecte</td>
</tr>
<tr>
<td>Vendes no facturades - Imputable per la diferència</td>
<td>Moneda del contracte del projecte</td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]