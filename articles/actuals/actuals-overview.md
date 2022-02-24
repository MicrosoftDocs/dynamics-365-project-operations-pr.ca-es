---
title: Valors reals
description: En aquest tema es proporciona informació sobre com treballar amb valors reals al Microsoft Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 304c51a4e502ad6ecec1fd821e98d6604ddd59ba
ms.sourcegitcommit: b4a05c7d5512d60abdb0d05bedd390e288e8adc9
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/02/2021
ms.locfileid: "5852532"
---
# <a name="actuals"></a>Valors reals 

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

Els valors reals representen el progrés financer revisat i aprovat i la planificació en un projecte. Es creen com a resultat de l'aprovació del temps, la despesa, les entrades d'ús de materials i les entrades i factures al llibre diari.

## <a name="journal-lines-and-time-submission"></a>Línies del llibre diari i enviament de temps

Per obtenir més informació sobre l'entrada de temps, vegeu [Descripció general de les entrades de temps](../time/time-entry-overview.md).

### <a name="time-and-materials"></a>Temps i materials

Quan un registre de temps que s'envia està enllaçat a un projecte que s'assigna a una línia de contracte de temps i materials, el sistema crea dues línies del llibre diari, una per al cost i l'altra per a les vendes sense facturar.

### <a name="fixed-price"></a>Preu fix

Quan una entrada de temps que s'envia està enllaçada a un projecte assignat a una línia de contracte de preu fix, el sistema crea una línia del llibre diari per al cost.

### <a name="default-pricing"></a>Preus per defecte

La lògica per crear els preus per defecte resideix a la línia del llibre diari. Els valors de camp de l'entrada de temps es copien a la línia del llibre diari. Aquests valors inclouen la data de la transacció, la línia de contracte a la qual està assignada el projecte i el resultat de moneda a la llista de preus adequada.

Els camps que afecten els preus per defecte, com ara **Funció** i **Unitat de recursos** s'utilitzen per determinar un preu adient a la línia del llibre diari. Podeu afegir un camp personalitzat a l'entrada de temps. Si voleu que el valor de camp es propagui als valors reals, creeu el camp a les taules **Valors reals** i **Línia del llibre diari**. Utilitzeu el codi personalitzat per propagar el valor del camp seleccionat des d'Entrada de temps a Valors reals a través de la línia del llibre diari mitjançant orígens de transaccions. Per obtenir més informació sobre els orígens i les connexions de les transaccions, vegeu [Enllaçar valors reals amb registres originals](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).

## <a name="journal-lines-and-basic-expense-submission"></a>Línies del llibre diari i enviament bàsic de despeses

Per obtenir més informació sobre l'entrada de despesa, vegeu [Descripció general de les entrades de despesa](../expense/expense-overview.md).

### <a name="time-and-materials"></a>Temps i materials

Quan una entrada de despesa bàsica que s'envia està enllaçat a un projecte que s'assigna a una línia de contracte de temps i materials, el sistema crea dues línies del llibre diari, una per al cost i l'altra per a les vendes sense facturar.

### <a name="fixed-price"></a>Preu fix

Quan una entrada de despesa bàsica presentada està a enllaçada a un projecte assignat a una línia de contracte de preu fix, el sistema crea una línia del llibre diari per al cost.

### <a name="default-pricing"></a>Preus per defecte

La lògica per a la introducció dels preus per defecte de les despeses es basa en la categoria de despeses. La data de la transacció, la línia de contracte a la qual està assignada el projecte i la moneda s'utilitzen per determinar la llista de preus adequada. Els camps que afecten els preus per defecte, com ara **Categoria de transacció** i **Unitat** s'utilitzen per determinar un preu adient a la línia del llibre diari. Tanmateix, només funciona quan el mètode de preus de la llista de preus és **Preu per unitat**. Si el mètode de càlcul de preus és **A partir del cost** o **Marcador sobre el cost**, el preu que s'ha introduït en crear l'entrada de despesa s'utilitza per al cost i el preu de la línia al llibre diari segons el mètode de càlcul de preus. 

Podeu afegir un camp personalitzat a l'entrada de despesa. Si voleu que el valor de camp es propagui als valors reals, creeu el camp a les taules **Valors reals** i **Línia del llibre diari**. Utilitzeu el codi personalitzat per propagar el valor del camp seleccionat des d'Entrada de temps a Valors reals a través de la línia del llibre diari mitjançant orígens de transaccions. Per obtenir més informació sobre els orígens i les connexions de les transaccions, vegeu [Enllaçar valors reals amb registres originals](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).

## <a name="journal-lines-and-material-usage-log-submission"></a>Enviament de línies del llibre diari i de registre d'ús de materials

Per obtenir més informació sobre l'entrada de despeses, vegeu [Registre d'ús de materials](../material/material-usage-log.md).

### <a name="time-and-materials"></a>Temps i materials

Quan una entrada de registre d'ús de materials enviada s'enllaça amb un projecte que està assignat a una línia de contracte de temps i materials, el sistema crea dues línies del llibre diari, una per al cost i una altra per a les vendes no facturades.

### <a name="fixed-price"></a>Preu fix

Quan una entrada de registre d'ús de materials presentada està enllaçada a un projecte assignat a una línia de contracte de preu fix, el sistema crea una línia del llibre diari per al cost.

### <a name="default-pricing"></a>Preus per defecte

La lògica per introduir preus per defecte per al material es basa en la combinació de productes i unitats. La data de la transacció, la línia de contracte a la qual està assignada el projecte i la moneda s'utilitzen per determinar la llista de preus adequada. Els camps que afecten els preus per defecte, com ara **Identificador del producte** i **Unitat**, s'utilitzen per determinar un preu adient a la línia del llibre diari. Però això només funciona per als productes del catàleg. Per als productes fora de catàleg, el preu que introduït en crear l'entrada del registre d'ús de materials s'utilitza per al cost i el preu de venda a les línies del llibre diari, 

Podeu afegir un camp personalitzat a l'entrada **Registre d'ús de materials**. Si voleu que el valor de camp es propagui als valors reals, creeu el camp a les taules **Valors reals** i **Línia del llibre diari**. Utilitzeu el codi personalitzat per propagar el valor del camp seleccionat des d'Entrada de temps a Valors reals a través de la línia del llibre diari mitjançant orígens de transaccions. Per obtenir més informació sobre els orígens i les connexions de les transaccions, vegeu [Enllaçar valors reals amb registres originals](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).

## <a name="use-entry-journals-to-record-costs"></a>Utilitzar llibres diari per registrar costos de registre

Podeu utilitzar llibres diari per registrar els costos o ingressos en classes de material, quota, temps, despeses o transaccions tributàries. Els diaris es poden utilitzar amb l'objectiu següent:

- Avanceu els valors reals de la transacció des d'un altre sistema al Microsoft Dynamics 365 Project Operations.
- Registrar els costos que s'han produït en un altre sistema. Aquestes despeses poden incloure costos de contractació o subcontractació.

> [!IMPORTANT]
> L'aplicació no valida el tipus de línia del llibre diari ni el preu relacionat que introduïu a la línia del llibre diari. Per tant, només un usuari que tingui consciència de l'impacte comptable que tenen els valors reals en el projecte hauria d'utilitzar els llibres diari per crear valors reals. A causa de l'impacte d'aquest tipus de diari, heu de triar amb cura qui té accés per crear llibres diari.

## <a name="record-actuals-based-on-project-events"></a>Enregistrament de valors reals a partir d'esdeveniments de projecte

El Project Operations registra totes les transaccions financeres que es produeixen durant un projecte. Aquestes transaccions es registren com a valors reals. Les taules següents mostren els diferents tipus de valors reals que s'han creat, en funció de si el projecte és un projecte de temps i materials o de preu fix, si es troba a la fase de prevenda o si és un projecte intern.

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a>El recurs pertany a la mateixa unitat organitzativa que la unitat de contractació del projecte

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

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a>El recurs pertany a una unitat organitzativa diferent de la unitat de contractació del projecte

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
