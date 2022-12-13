---
title: Informació general de les línies d'oferta basades en productes
description: Aquest article proporciona informació sobre com treballar amb línies d'oferta basades en productes.
author: rumant
ms.date: 10/30/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: a260c0f51cc2d958281dbc6f0f711347cab85a9a
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 12/05/2022
ms.locfileid: "9826210"
---
# <a name="product-based-quote-lines-overview"></a>Informació general de les línies d'oferta basades en productes

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_

Podeu crear línies d'oferta basades en productes al Dynamics 365 Project Operations. Les línies d'oferta basades en productes poden afegir-se manualment o poden ser elements del catàleg de productes.

## <a name="product-catalog"></a>Catàleg de productes

Cada producte del catàleg de productes té una unitat i un grup d'unitats per defecte. Si diversos productes comparteixen el mateix conjunt d'atributs, podeu crear una família de productes que comparteixi aquests atributs. 

Per exemple, una empresa ven llicències de subscripció per a diversos tipus de programes. Tots els programes de subscripció tenen els dos atributs següents:

- Nombre d'usuaris
- Duració de la subscripció mesurada en mesos

Per mantenir aquest tipus de catàleg, creeu una família de productes que s'anomeni **Programari de subscripció** i afegiu el nombre d'usuaris i la duració de la subscripció com a atributs. A continuació, podeu afegir productes individuals a la família de productes **Programari de subscripció**.

## <a name="add-product-catalog-items-to-a-project-quote"></a>Afegir elements del catàleg de productes a una oferta de projecte

Les pàgines **Oferta del projecte** i **Contracte del projecte** tenen seccions per a línies basades en el projecte i línies basades en productes. Per a les línies basades en productes, la llista desplegable de la línia d'oferta o de la línia de contracte de projecte inclou tots els productes i les unitats de la llista de preus de productes. També podeu afegir productes que no siguin part de la llista de preus de productes.

A més, podeu seleccionar productes d'altres llistes de preus o directament des del catàleg de productes. En seleccionar productes directament des d'un catàleg de productes, la llista de preus per defecte d'aquest producte s'utilitza per obtenir el preu de venda del producte. Si no es defineix una llista de preus per defecte, el preu es defineix com a zero (0).

Si una línia d'oferta es basa en un catàleg de productes, podeu substituir el preu de venda directament a la línia d'oferta. Una línia d'oferta al camp **Preus** amb dos valors disponibles:

- **Substitueix el preu**
- **Opcions per defecte**

Si seleccioneu **Substitueix el preu**, el preu per defecte no està definit. En comptes d'això, heu d'introduir un preu per al producte a la línia d'oferta. Si seleccioneu **Utilitza el valor per defecte**, s'utilitzarà el preu de venda per defecte i el camp no es podrà editar.

Els preus de vendes per defecte s'introdueixen a les línies basades en productes en una oferta. El camp **Preu** es defineix com a **Substitueix el preu** per tal que pugueu editar el preu per defecte a les línies d'oferta. Es tracta d'una substitució específica del Project Operations per al comportament de les línies basades en productes al Dynamics 365 Sales.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
