---
title: 'Ofertes: conceptes clau (bàsic)'
description: En aquest tema es proporciona informació sobre l'ús d'ofertes de projectes al Project Operations.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 279e7dd47d3d61b02227b307a5833ca0bac66f4a774b5ff23cb69aac417e2f0e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "7009429"
---
# <a name="concepts-unique-to-project-quotes"></a>Conceptes únics per a ofertes de projecte

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_


Aquests són els conceptes clau que cal tenir en compte abans de començar a utilitzar les ofertes de projecte al Dynamics 365 Project Operations:

## <a name="contracting-unit"></a>Unitat de contractació

La unitat de contractació representa la divisió o el departament propietari del lliurament del projecte. Podeu configurar els costos de recursos per a cada unitat de contractació. Quan especifiqueu el cost dels recursos d'un recurs de la unitat contractant, també podreu configurar diferents tarifes de costos per als recursos que aquesta unitat de contractació prengui d'altres divisions o departaments de l'empresa. S'anomenen preus de transferència, préstec de recursos o preus d'intercanvi. Quan configureu el cost del préstec de recursos d'altres divisions, també podeu configurar aquestes tarifes de costos en la moneda de la divisió prestadora.

## <a name="cost-currency"></a>Moneda de cost

La moneda de cost al Project Operations és la moneda en què s'informen els costos. Aquesta moneda es deriva de la moneda enllaçada al camp **Unitat de contractació** a l'oferta, el contracte i el projecte. Els costos es poden registrar en qualsevol moneda en un projecte. Tanmateix, hi ha una conversió de moneda dels costos de moneda de registre a la moneda de cost del projecte.

Com que els tipus de canvi a la plataforma del CDS no poden tenir data d'efectivitat, els totals en pantalla per al cost poden canviar amb el temps si actualitzeu els tipus de canvi. Tanmateix, els costos registrats a la base de dades no es modifiquen perquè els imports s'emmagatzemaran en la moneda en què s'hagin incorregut.

## <a name="sales-currency"></a>Moneda de venda

La moneda de vendes al Project Operations és la moneda en la qual es registren i es mostren els imports de vendes estimats i reals. També és la moneda en què es factura al client per l'acord. En una oferta de projecte, la moneda de vendes és per defecte la del registre de client o de compte i es pot canviar quan es crea l'oferta. Després d'haver desat l'oferta, la moneda de vendes no es pot canviar. Llistes de preus de productes i projectes per defecte basades en la moneda de vendes de l'oferta.

A diferència dels costos, els valors de vendes només es poden registrar en la moneda de vendes.

## <a name="billing-method"></a>Mètode de facturació

Els projectes acostumen a tenir models de contractació fixos i basats en el consum. Això es representa al Project Operations com a **Mètode de facturació** i té dos valors, temps i material i preu fix.

- **Temps i material:** es tracta d'un model de contracte basat en el consum on cada despesa té uns ingressos corresponents. A mesura que estimeu o suporteu més costos, les vendes estimades i reals corresponents també augmentaran. Podeu especificar els límits que no voleu superar en les línies d'oferta que tenen aquest mètode de facturació. Això limitarà els ingressos reals. Els ingressos estimats no es veuen afectats pels límits que no s'han de superar.
- **Preu fix:** es tracta d'un model de contracte fix que indica que els valors de venda seran independents dels costos incorreguts. El valor de venda és fix i no canvia a mesura que s'estimen o incorren més costos.

## <a name="project-price-lists"></a>Llistes de preus del projecte

Les llistes de preus de projecte són llistes de preus que s'utilitzen per obtenir els preus per defecte, no les tarifes de costos, el temps, les despeses i altres components relacionats amb el projecte. Hi poden haver diverses llistes de preus i cada llista pot tenir la seva pròpia data d'efectivitat per a cada oferta de projecte. El Project Operations no admet la superposició de la data d'efectivitat de les llistes de preus del projecte.

## <a name="product-price-lists"></a>Llistes de preus de productes

Les llistes de preus de producte són llistes de costos que s'utilitzen per obtenir els preus per defecte, no les tarifes de cost, per a les línies basades en productes en una oferta. Només hi ha una llista de preus de producte per oferta.

## <a name="transaction-classes"></a>Classes de transaccions

El Project Operations admet quatre tipus de classes de transaccions:

- Temps
- Despesa
- Material
- Tarifa

Els valors de costos i de vendes es poden estimar i incórrer en classes de transaccions de temps, despeses i materials. Els impostos són una classe de transaccions només d'ingressos.

## <a name="work-entities-and-billing-entities"></a>Entitats de treball i entitats de facturació

Les entitats que representen el treball són els projectes i tasques. Les entitats que representen la facturació són les línies d'oferta i línies de contracte. Podeu enllaçar diferents entitats de treball amb opcions de facturació associant-les amb línies d'oferta o de contracte.

## <a name="multi-customer-deals"></a>Ofertes de diversos clients

Les ofertes de diversos clients es produeixen quan hi ha més d'un client per facturar. Entre els exemples més habituals s'inclouen:

- **Empreses OEM i els seus associats:** els associats i distribuïdors venen un producte amb els serveis de valor afegit. Normalment, aquest és un escenari en què durant un acord especial amb un client, l'OEM ofereix finançar una part del projecte. 

- **Projectes del sector públic:** diversos departaments d'un govern local acorden finançar un projecte i s'han de facturar segons una divisió convinguda prèviament. Per exemple, un districte escolar i la ciutat o el departament de govern local acorden finançar la construcció d'una piscina.

## <a name="invoice-schedules"></a>Planificacions de facturació

Les planificacions de factura són específiques de cada línia d'oferta i també són opcionals. Les planificacions de factura es creen a partir de determinades dates d'inici i d'acabament i la freqüència de factura. Les planificacions de la factura s'utilitzen a la fase de contracte quan el procés de creació de factura automàtica està configurat. A la fase d'oferta, les planificacions són opcionals. Quan es creen les planificacions de la factura a la fase **Oferta**, es copien al contracte del projecte que es crea quan es guanya una oferta de projecte.

## <a name="changes-from-dynamics-365-sales-quote"></a>Canvis de l'oferta del Dynamics 365 Sales:

Les ofertes del Project Operations es basen en les ofertes del Dynamics 365 Sales. No obstant, hi ha algunes diferències importants en la funcionalitat que heu de tenir en compte:

- No s'admeten les accions **Revisa** ni **Activa**.
- Les ofertes del Project Operations tenen dos tipus de línies diferents. Una és per als projectes i l'altra és per als productes.
- Les ofertes del Project Operations tenen el seu propi formulari i elements de la interfície d'usuari, regles de negoci, lògica empresarial en complements i scripts de client que les fan úniques de les ofertes del Sales.

Per aquests motius, no es recomana utilitzar una oferta del Sales i una oferta del Project Operations indistintament.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
