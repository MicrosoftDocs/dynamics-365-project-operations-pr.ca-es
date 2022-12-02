---
title: Informació general de les línies de contracte basades en productes (bàsic)
description: En aquest article es proporciona informació sobre les línies de contracte basades en productes.
author: rumant
ms.date: 10/07/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 4ad1fe6d5d56468d887535ddf107eefed3cbd28d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919864"
---
# <a name="product-based-contract-lines-overview---lite"></a>Informació general de les línies de contracte basades en productes (bàsic)

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_

Podeu crear línies de contracte basades en productes al Dynamics 365 Project Operations. Les línies de contracte basades en productes es poden crear manualment o poden ser articles del catàleg de productes.

## <a name="product-catalog"></a>Catàleg de productes

Els productes del catàleg de productes tenen una unitat i un grup d'unitats per defecte. Si diversos productes comparteixen el mateix conjunt d'atributs, podeu crear una família de productes que també tingui aquests atributs. Tots els productes d'una família de productes hereten el mateix conjunt d'atributs.

Per exemple, una empresa ven llicències de subscripció per a diversos tipus de programes. Tots els programes de subscripció tenen els dos atributs següents:

- Nombre d'usuaris
- Duració de la subscripció (en mesos)

Per mantenir aquest tipus de catàleg, creeu una família de productes que s'anomeni **Programari de subscripció**. Afegiu els atributs **Nombre d'usuaris** i **Duració de la subscripció** a la família de productes. A continuació, afegiu productes individuals a la família de productes **Programari de subscripció**.

## <a name="add-product-catalog-items-to-a-project-contract"></a>Afegir elements del catàleg de productes a un contracte de projecte

Els contractes de projectes tenen seccions per a dos tipus de línies, basades en projectes i basades en productes. Les línies basades en productes inclouen tots els productes i unitats de la llista de preus de producte del contracte. Es poden afegir productes que no formen part de la llista de preus de productes del contracte.

Podeu seleccionar productes d'altres llistes de preus o directament del catàleg de productes. En seleccionar productes directament des d'un catàleg de productes, la llista de preus per defecte d'aquest producte s'utilitza per obtenir el preu de venda del producte. Si no es defineix una llista de preus per defecte, el preu es defineix com a 0 (zero).

Si una línia de contracte es basa en un catàleg de productes, podeu substituir el preu de venda directament a la línia de contracte. Una línia de contracte té el camp **Preu** amb els dos valors:

- **Substitueix el preu**
- **Utilitza el valor per defecte**

Si establiu el camp **Preu** a **Substitueix el preu**, el preu per defecte no està establert. Introduïu un preu per al producte en la línia de contracte. Si establiu el camp a **Utilitza el valor per defecte**, el preu de venda per defecte s'utilitza i el camp no es pot editar.

Després d'instal·lar el Project Operations, els preus de vendes per defecte s'introdueixen a les línies basades en productes en un contracte. El camp **Preu** es defineix com a **Substitueix el preu** per tal que pugueu editar el preu per defecte a les línies de contracte. Aquesta és una substitució específica del Project Operations per al comportament de línies basades en productes al Dynamics 365 Sales.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]