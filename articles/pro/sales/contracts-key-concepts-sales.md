---
title: 'Contractes de projecte: conceptes clau (bàsic)'
description: Aquest tema proporciona informació sobre els conceptes clau dels contractes de projectes.
author: rumant
ms.date: 10/07/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 09252e449c11d6602dccba83f26413f380698814
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580582"
---
# <a name="concepts-unique-to-project-contracts"></a>Conceptes únics per a contractes de projecte

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_



En aquest tema es proporcionen els conceptes clau que cal tenir en compte abans de començar a utilitzar els contractes de Project a Dynamics 365 Project Operations:

## <a name="contracting-unit"></a>Unitat de contractació

La unitat de contractació representa la divisió o el departament propietari del lliurament del projecte. Podeu configurar els costos de recursos per a cada unitat de contractació. Quan especifiqueu el cost del recurs per a un recurs, també podreu establir diferents tarifes de cost per als recursos. Aquesta unitat de contractació pren aquests recursos d'una altra divisió o departament dins de l'empresa. Les tarifes de cost per als recursos s'anomenen preus de transferència, préstec de recursos o preus d'intercanvi. Quan configureu les tarifes de cost per prestar recursos d'altres divisions, utilitzeu la moneda de la divisió prestadora.

## <a name="cost-currency"></a>Moneda de cost

La moneda de cost és la moneda en la qual s'informa dels costos a la pantalla. Aquesta moneda es deriva de la moneda enllaçada al camp **Unitat de contractació** del contracte i el projecte. Els costos es poden registrar en qualsevol moneda en un projecte. Tanmateix, hi ha una conversió de moneda dels costos de moneda de registre a la moneda de cost del projecte quan es mostren a la pantalla.

Com que els tipus de canvi a la plataforma Common Data Service CDS no poden tenir data d'efectivitat, els totals en pantalla per al cost poden canviar amb el temps si actualitzeu els tipus de canvi. Tanmateix, els costos registrats a la base de dades no es modifiquen perquè els imports s'emmagatzemaran en la moneda en què s'hagin incorregut.

## <a name="sales-currency"></a>Moneda de venda

La moneda de vendes al Project Operations és la moneda en la qual es registren i es mostren els imports de vendes estimats i reals. La moneda de vendes també és la moneda en què es factura al client per l'acord. En un contracte de projecte, la moneda de vendes és per defecte la del registre de client o de compte i es pot canviar quan es crea el contracte. Quan es crea un contracte tancant una oferta com a guanyada, la moneda del contracte no s'aplica a la moneda de l'oferta.

Quan creeu un contracte de projecte des de zero, el camp **Moneda de vendes** no es pot editar. Llistes de preus de productes i projectes per defecte basades en aquesta moneda en el contracte.

A diferència dels costos, els valors de vendes només es poden registrar en la moneda de vendes.

## <a name="billing-method"></a>Mètode de facturació

Normalment hi ha dos tipus de models de contractació per als projectes, tarifa fixa i basat en el consum. Aquests models estan representats al Project Operations com a mètodes de facturació amb dos valors possibles:

- Temps i material: model de contracte basat en el consum on cada cost incorregut té uns ingressos corresponents. A mesura que estimeu o suporteu més costos, les vendes estimades i reals corresponents també augmentaran. Especifiqueu límits que no voleu superar per a les línies de contracte que tenen aquest mètode de facturació que limitin els ingressos reals. Els ingressos estimats no es veuen afectats pels límits que no s'han de superar.
- Preu fix: model de contracte fix que indica que els valors de venda seran independents dels costos incorreguts. El valor de venda és fix i no canvia a mesura que s'estimen o incorren més costos.

## <a name="project-price-lists"></a>Llistes de preus del projecte

Les llistes de preus de projecte s'utilitzen per obtenir els preus per defecte, no les tarifes de costos, el temps, les despeses i altres components relacionats amb el projecte. Poden haver-hi diverses llistes de preus. Cada llista de preus té la seva pròpia data d'efectivitat per a cada contracte de projecte. El Project Operations no admet la superposició de la data d'efectivitat de les llistes de preus del projecte.

Quan es crea un contracte de projecte guanyant una oferta de projecte, les llistes de preus del projecte es copien amb el nom i la data del contracte inclòs. La còpia d'aquesta informació constitueix un preu personalitzat per als components del projecte en aquest contracte.

## <a name="product-price-lists"></a>Llistes de preus de productes

Les llistes de preus de producte s'utilitzen per obtenir els preus per defecte, no les tarifes de cost, per a les línies basades en productes en un contracte. Només hi ha una llista de preus de producte per contracte.

## <a name="transaction-classes"></a>Classes de transacció

El Project Operations admet quatre tipus de classes de transaccions:

- Temps
- Despesa
- Material
- Tarifa

Els valors de costos i de vendes es poden estimar i incórrer en classes de transaccions de temps, despeses i materials. Els impostos són una classe de transacció només d'ingressos.

## <a name="work-entities-and-billing-entities"></a>Entitats de treball i entitats de facturació

Les entitats que representen el treball són els projectes i tasques. Les entitats que representen els aspectes de facturació són les línies de contracte. Podeu enllaçar diferents entitats de treball amb opcions de facturació associant-les amb línies de contracte.

## <a name="multi-customer-deals"></a>Ofertes de diversos clients

Les ofertes de diversos clients tenen més d'un client per facturar en una oferta. Alguns exemples habituals inclouen:

- Empreses OEM i els seus associats: els associats i distribuïdors venen un producte amb alguns serveis de valor afegit, típicament amb un acord particular amb un client. L'OEM ofereix finançar una part del projecte. 

- Projectes del sector públic: diversos departaments d'un govern local acorden finançar un projecte i s'han de facturar segons una divisió convinguda prèviament. Per exemple, un districte escolar i el govern local acorden finançar la construcció d'una piscina.

## <a name="invoice-schedules"></a>Planificacions de facturació

Les planificacions de facturació són específiques de cada línia de contracte i són necessàries perquè funcioni la facturació automàtica. Les planificacions de factura es creen a partir de determinades dates d'inici i d'acabament i la freqüència de factura. Les planificacions s'utilitzen a la fase de contracte quan el procés de creació de factura automàtica està configurat. Quan es crea un contracte de projecte a partir d'una oferta, la planificació de facturació es copia al contracte del projecte a partir de l'oferta.

## <a name="changes-from-the-dynamics-365-sales-contract"></a>Canvis del contracte del Dynamics 365 Sales

Els contractes del Project Operations es basen en els contractes del Dynamics 365 Sales. No obstant, hi ha algunes desviacions i diferències importants en la funcionalitat que heu de tenir en compte:

- Els contractes del Project Operations tenen dos tipus diferents de línies, una per a projectes i una per a productes.
- Els contractes del Project Operations tenen el seu propi formulari i elements de la interfície d'usuari, regles de negoci, lògica empresarial en complements i scripts de client que els fan únics dels contractes del Sales.

Per aquestes raons, no s'hauria d'utilitzar un contracte del Sales i del Project indistintament.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
