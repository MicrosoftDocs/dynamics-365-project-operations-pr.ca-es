---
title: Llistes de preus de productes
description: En aquest tema es proporciona informació sobre les llistes de preus en els preus dels catàlegs utilitzats per a ofertes de projectes i contractes.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: c0f30bec159254c078024549b7b0dd0c048ef65d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275346"
---
# <a name="product-price-lists"></a>Llistes de preus de productes

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

Les entitats de llistes de preus i element de la llista de preus admeten els preus del catàleg de productes. Generalment, aquesta funcionalitat s'utilitza per a les línies basades en catàleg sobre ofertes de projectes i contractes de projecte.

Per a les línies basades en el projecte, un contracte representa el tracte després de guanyar-lo. Com que el procés de negociació sol precedir la victòria, el preu adjunt a l'oferta sempre es copia com està a una llista de preus nova i s'adjunta al contracte. Aquesta llista de preus nova no es pot canviar fora de l'àmbit del contracte. Aquesta limitació ajuda a protegir la targeta de tarifes que es va negociar de qualsevol canvi de preu que es produeix a la llista de preus mestres.

Els productes s'han de configurar per tal que tinguin un cost i una llista de preus per defecte al catàleg de productes. Utilitzeu el preu d'una llista, el cost estàndard i el cost corrent per configurar els preus dels costos i les llistes per defecte. Els preus per defecte de llista s'utilitzen a una línia d'oferta o a una línia de contracte de projecte només quan el sistema no pot trobar una línia de llista de preu per a aquest producte a la llista de preus de producte per al contracte d'oferta o de projecte.

El preu de cost de les línies del catàleg de productes es pot canviar entre ofertes. Aquesta opció és important, perquè si no feu un seguiment precís dels costos, no podeu determinar els guanys operatius dels compromisos del projecte. Per defecte, el cost estàndard del producte s'utilitza com a preu de cost. No obstant, el preu de cost per defecte es pot actualitzar a la línia d'oferta si hi ha un preu de cost diferent per a aquesta oferta.

## <a name="price-list-items"></a>Elements de la llista de preus

Podeu afegir productes d'un catàleg de productes a diverses llistes de preus. Les línies de llista de preus dels productes sempre fan referència a una unitat específica. Els preus d'un producte en els elements de la llista de preus es poden configurar com a quantitat de moneda. Alternativament, pot configurar-se com una funció del preu de la llista, el cost corrent o el cost estàndard.

El PSA admet diverses opcions d'arrodoniment quan els preus es configuren com a funció del preu de llista, cost estàndard o cost corrent. A banda de treure profit de diversos mètodes de preus i d'arrodoniment, podeu associar llistes de descomptes amb elements de la llista de preus. 

Quan creeu una llista de preus personalitzada nova per a una oferta seleccionant **Crea un preu personalitzat** a la pàgina **Oferta del projecte**, es fa una còpia de la llista de preus i el camp **Entitat** a la capçalera de la llista de preus nova es defineix com a **Entitat de vendes**. Al nom de la llista de preus nova s'hi afegeix el nom de l'oferta i d'una marca horària. També podeu utilitzar el nom de la llista de preus nova i el nom de l'oferta als fluxos de treball personalitzats per activar la revisió i les aprovacions addicionals de les ofertes que utilitzin preus personalitzats.

 
## <a name="default-product-price-list"></a>Llista de preus per defecte
Cada registre de client té un camp **Llista de preus per defecte**, on es pot especificar una llista de preus que coincideixi amb la moneda del client. No s'introdueix automàticament un valor per defecte en aquest camp. Si hi ha un acord de preus personalitzat amb un client específic, podeu utilitzar aquest camp per associar una llista de preus amb el client.

Les entitats Oportunitat, Oferta i Contracte de projecte utilitzen el següent ordre per introduir llistes de preus de productes per defecte. El mateix ordre s'utilitza per a les llistes de preus del projecte.

1.  Oferta
2.  Oportunitat
3.  Client
4.  Configuració global 

Per defecte, el camp **Producte** de la línia d'oferta enumera tots els productes actius de la llista de preus de producte de l'oferta. Si un producte s'ha inhabilitat o si es tracta d'un esborrany, no s'hi mostra, fins i tot si està inclòs a la llista de preus. 

Les línies del catàleg de productes s'afegeixen com a línies de factura a la primera factura que es crea per a un contracte de projecte. En un esborrany de factura, les línies de factura es poden suprimir. En aquest cas, les línies apareixeran en una factura posterior fins que es facturin o fins que s'enviï la factura al client. No podeu facturar cap quantitat parcial d'una línia de factura de producte. Quan es facturen les línies de producte del contracte de projecte, es creen valors reals. No obstant, aquests valors reals no estan enllaçats a l'entitat del projecte relacionat. En altres paraules, les línies de contracte de projecte basades en productes són independents de qualsevol ús basat en projectes. No es fa el seguiment dels consums materials dels projectes.


[!INCLUDE[footer-include](../includes/footer-banner.md)]