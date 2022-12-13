---
title: Conceptes únics per a les ofertes basades en projectes
description: En aquest article es proporciona informació sobre les cotitzacions del projecte a Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/02/2022
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 89867cfbe92f47d58b16da40b62d3d9dd6a15b64
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824315"
---
# <a name="concepts-unique-to-project-based-quotes"></a>Conceptes únics per a les ofertes basades en projectes

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

Abans de començar a utilitzar pressupostos de projecte a Microsoft Dynamics 365 Project Operations, heu de tenir en compte els conceptes clau següents.

## <a name="owning-company"></a>Empresa propietària

L'empresa propietària representa la persona jurídica propietària del lliurament del projecte. El client del pressupost ha de ser un client vàlid en aquesta persona jurídica en aplicacions de finances i operacions. La moneda de l'empresa propietària i la moneda de la unitat de contractació seleccionada en un pressupost basat en projecte han de coincidir.

## <a name="contracting-unit"></a>Unitat de contractació

Una unitat de contractació representa la divisió o pràctica propietària del lliurament del projecte. Podeu configurar els costos de recursos per a cada unitat de contractació. Quan especifiqueu els costos de recursos d'un recurs d'una unitat de contractació, podeu configurar diferents taxes de cost per als recursos dels quals la unitat de contractació presta o per a altres divisions o pràctiques de l'empresa. Aquestes taxes de cost es denominen preus de transferència, préstecs de recursos o preus de canvi. Quan configureu el cost de demanar prestat recursos d'altres divisions, podeu establir les taxes de cost en la moneda de la divisió de préstecs.

## <a name="cost-currency"></a>Moneda de cost

La moneda de cost del Project Operations és la moneda en què s'informen els costos. Aquesta moneda deriva de la moneda que s'adjunta al **camp Unitat** de contractació de l'oferta, contracte i projecte. Els costos d'un projecte es poden registrar en qualsevol moneda. Tanmateix, hi ha una conversió de moneda de la moneda en què es van registrar els costos a la moneda de cost del projecte.

Com que els tipus de canvi de la Dataverse plataforma no poden ser efectius amb data, els totals de costos en pantalla poden canviar amb el pas del temps si actualitzeu els tipus de canvi de moneda. No obstant això, els costos que es registren a la base de dades es mantenen sense canvis, ja que els imports s'emmagatzemen en la moneda en què van incórrer.

## <a name="sales-currency"></a>Moneda de venda

La moneda de vendes del Project Operations és la moneda en què es registren i es mostren els imports de vendes estimats i reals. També és la moneda en què es factura el client per l'oferta. Per a una oferta de projecte, s'estableix una moneda de vendes predeterminada del registre de client o compte i es pot canviar quan es crea l'oferta. Tanmateix, la moneda de venda no es pot canviar després de desar l'oferta. Les llistes de preus predeterminats per a productes i projectes s'estableixen en funció de la moneda de venda de l'oferta.

A diferència dels costos, els valors de vendes només **es poden registrar** en la moneda de venda.

## <a name="billing-method"></a>Mètode de facturació

Els projectes solen tenir models de contractació basats en la quota fixa i en el consum. Al Project Operations, el model de contractació d'un projecte està representat pel mètode de facturació. El mètode de facturació té dos valors: temps i material i preu fix.

- **Temps i material** : Un model de contractació basat en el consum on cada cost en què s'incorre està avalat pels ingressos corresponents. A mesura que estimeu o suporteu més costos, les vendes estimades i reals corresponents també augmentaran. Podeu especificar els límits que no voleu superar en les línies d'oferta que tenen aquest mètode de facturació. D'aquesta manera, podeu limitar els ingressos reals. Els ingressos estimats no es veuen afectats per no superar els límits.
- **Preu**  fix: Model de contractació de quota fixa on els valors de venda són independents dels costos en què s'incorre. El valor de venda és fix i no canvia a mesura que s'estimen o incorren més costos.

## <a name="project-price-lists"></a>Llistes de preus del projecte

Les llistes de preus del projecte són llistes de preus que s'utilitzen per introduir preus predeterminats, no tarifes de cost, per temps, despeses i altres components relacionats amb el projecte. Hi poden haver diverses llistes de preus i cada llista pot tenir la seva pròpia data d'efectivitat per a cada oferta de projecte. Les operacions del projecte no admeten l'efectivitat de la data superposada per a les llistes de preus del projecte.

## <a name="product-price-lists"></a>Llistes de preus de productes

Les llistes de preus de productes són llistes de preus que s'utilitzen per introduir els preus predeterminats, no les tarifes de cost, per a les línies basades en productes d'un pressupost. Només hi ha una llista de preus de productes per pressupost.

## <a name="transaction-classes"></a>Classes de transaccions

El Project Operations admet quatre tipus de classes de transaccions:

- Temps
- Despesa
- Material
- Tarifa

Els valors de costos i vendes es poden estimar i incórrer en **classes de transaccions de temps** **, despeses** i **materials** . **La tarifa** és una classe de transacció només d'ingressos.

## <a name="work-entities-and-billing-entities"></a>Entitats de treball i entitats de facturació

Els Projectes i Tasques són entitats que representen el treball. Les línies de cotització i les línies de contracte són entitats que representen la facturació. Podeu enllaçar diferents entitats de treball a opcions de facturació associant-les a Línies de pressupost o Línies de contracte.

## <a name="multi-customer-deals"></a>Ofertes de diversos clients

Les ofertes multiclient es produeixen quan hi ha més d'un client per factura. Aquests són alguns exemples típics:

- **Les empreses fabricants d'equips originals (OEM) i els seus socis** : socis i revenedors venen un producte que inclou serveis de valor afegit. Durant un acord amb un client, l'OEM sol oferir finançar part del projecte.
- **Projectes del sector**  públic: diversos departaments d'un govern local acorden finançar un projecte i es facturen segons una divisió prèviament acordada. Per exemple, un districte escolar i la ciutat o el departament de govern local acorden finançar la construcció d'una piscina.

## <a name="invoice-schedules"></a>Planificacions de facturació

Els horaris de factures són específics per a cada línia de pressupost i són opcionals. Els calendaris de factures es creen en funció de les dates d'inici i finalització específiques i d'una freqüència de factura. S'utilitzen durant la fase de contracte, quan es configura el procés de creació automàtica de factures. Durant la fase de pressupost, els horaris de factures són opcionals. Si es creen durant la fase d'oferta, es copien al contracte de projecte que es crea quan es guanya una oferta de projecte.

## <a name="differences-from-dynamics-365-sales-quotes"></a>Diferències respecte a les cotitzacions del Dynamics 365 Sales

Les cotitzacions d'Operacions del Projecte es basen en les cotitzacions del Dynamics 365 Sales. No obstant, hi ha algunes diferències importants en la funcionalitat que heu de tenir en compte:

- Els pressupostos d'operacions de projecte tenen dos tipus diferents de línies: una per a projectes i una altra per a productes.
- Les ofertes del Project Operations tenen els seus propis elements de pàgina i interfície d'usuari (IU), regles de negoci, lògica empresarial en connectors i scripts del costat del client que els fan diferents de les ofertes de vendes.
- A Vendes, podeu adjuntar diverses comandes a un únic pressupost de vendes. Al Project Operations, només podeu adjuntar un contracte de projecte a un pressupost de projecte.
- Quan guanyeu un pressupost de vendes, l'oportunitat relacionada pot romandre oberta. Quan es guanya una oferta de projecte, l'oportunitat relacionada es tanca.
- Un pressupost de vendes no inclou alguns camps i conceptes que inclou un pressupost de projecte. Els camps inclouen **Unitat de contractació**, **Administrador de comptes** i **Nom del contacte de la factura**.
- Les ofertes de vendes i les ofertes de projecte s'identifiquen mitjançant el camp Tipus **basat en** conjunt d'opcions. Per a un pressupost de vendes, el valor d'aquest camp es basa **en** elements. Per a un pressupost de projecte, el valor es **basa en el** treball.

A causa d'aquestes diferències, no us recomanem que utilitzeu les cotitzacions de vendes i les cotitzacions d'operacions de projecte indistintament.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
