---
title: Factures corregides
description: Aquest tema proporciona informació sobre les factures corregides.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: b31e702cc15bbb3937e8c4b305064212f63ce919
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072380"
---
# <a name="corrected-invoices"></a>Factures corregides

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

Es poden editar les factures confirmades. Quan editeu una factura confirmada, es crea un esborrany de la factura corregida. Com que s'assumeix que voleu revertir totes les transaccions i quantitats de la factura original, la factura corregida inclou totes les transaccions de la factura original i totes les quantitats que hi ha són zero.

Quan alguna transacció no requereix correcció, podeu eliminar-la de l'esborrany de factura correctiva. Per revertir o retornar només una quantitat parcial, podeu editar el camp Quantitat al detall de la línia. Si obriu el detall de la línia de factura, podeu veure la quantitat original de la factura. A continuació, podeu editar la quantitat de la factura actual de manera que sigui inferior o superior a la quantitat original de la factura.

Quan es confirma una factura correctiva, es reverteix el valor real de vendes facturades original i es crea un nou valor real de vendes facturades. Si la quantitat s'ha reduït, la diferència provocarà que també s'hagi creat un nou valor real de venda no facturada. Per exemple, si les vendes facturades originals eren de vuit hores, i el detall de la línia de factura corregida té una quantitat menor de sis hores, es reverteix la línia de vendes facturades originals i es creen dos nous valors reals:

- Un valor de vendes facturades durant sis hores.
- Un valor de vendes no facturades per a les dues hores restants. Aquesta transacció es pot facturar més tard o marcar com a no imputable, en funció de les negociacions amb el client.
