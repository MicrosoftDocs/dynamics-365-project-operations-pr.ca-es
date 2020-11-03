---
title: Comandes de compra per a un projecte
description: En aquest article es descriuen els diversos mètodes que podeu utilitzar per crear comandes de compra per a un projecte. El mètode que utilitzeu depèn de la finalitat de la comanda de compra i quan es consumeixen i carregaran els articles adquirits en un projecte.
author: Yowelle
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bd891aec5bcab66c5801a5d9ca8abbbf632d662d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072200"
---
# <a name="purchase-orders-for-a-project"></a>Comandes de compra per a un projecte

[!include [banner](../includes/banner.md)]

En aquest article es descriuen els diversos mètodes que podeu utilitzar per crear comandes de compra per a un projecte. El mètode que utilitzeu depèn de la finalitat de la comanda de compra i quan es consumeixen i carregaran els articles adquirits en un projecte.

### <a name="methods-for-creating-a-purchase-order"></a>Mètodes per crear una comanda de compra

Podeu utilitzar un dels mètodes següents per crear una comanda de compra a Administració de projectes i comptabilitat. La finalitat de la comanda de compra determina quan es consumeix la comanda de compra i, per tant, quan es consumeixen i carregaran els articles en un projecte.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Mètode</th>
<th>Finalitat</th>
<th>Consum d'articles</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Creeu una comanda de compra directament des d'un projecte.</td>
<td>Utilitzeu aquest mètode per comprar articles d'un proveïdor extern per al consum en un projecte. Podeu crear la comanda de compra de dues maneres:
<ul>
<li>Des del projecte en si mateix. En aquest cas, el projecte ja s'ha definit per a la comanda de compra.</li>
<li>Navegant a la comanda de compra del projecte. Heu de seleccionar el proveïdor i el projecte per als quals crear la comanda de compra.</li>
</ul></td>
<td>Els articles es consumeixen en actualitzar la factura del proveïdor.</td>
</tr>
<tr class="even">
<td>Creeu una comanda de compra d'una comanda de vendes.</td>
<td>Utilitzeu aquest mètode per comprar articles quan creeu una comanda de vendes d'un projecte.</td>
<td>Els articles es consumeixen quan la comanda de vendes s'ha facturat al client.</td>
</tr>
<tr class="odd">
<td>Creeu una comanda de compra a partir d'un requisit d'articles.</td>
<td>Utilitzeu aquest mètode per comprar articles quan creeu un requisit d'articles d'un projecte.</td>
<td>Els articles es consumeixen quan s'actualitza l'albarà de requisits d'articles.</td>
</tr>
</tbody>
</table>

> [!NOTE] 
> En actualitzar la factura o l'albarà del venedor, se us demanarà que actualitzeu l'albarà del requisit d'articles.

Per obtenir més informació, vegeu [Rebre articles en una comanda de compra per a un requisit d'articles](tasks/receive-items-purchase-order-item-requirement.md).

