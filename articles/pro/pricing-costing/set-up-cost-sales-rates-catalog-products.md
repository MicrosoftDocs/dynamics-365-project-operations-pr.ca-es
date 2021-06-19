---
title: Configuració de les tarifes de cost i de vendes per als productes del catàleg (bàsic)
description: Aquest tema proporciona informació sobre com configurar els costos i les tarifes de venda dels articles en un catàleg de productes.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4995859696c844e99593139f63dffbf86a52f2f0
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004299"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a>Configuració de les tarifes de cost i de vendes per als productes del catàleg (bàsic)

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_


La configuració de preus dels elements del catàleg de productes del Dynamics 365 Project Operations és la mateixa que al Dynamics 365 Sales.

Al Project Operations, els productes no es poden calcular ni utilitzar en els projectes, de manera que els preus del catàleg de productes no s'han de definir a les llistes de preus del projecte per a les ofertes i els contractes.

Utilitzeu el camp **Preu del producte** d'una oferta, un contracte o un compte per configurar els preus del catàleg de productes. No configureu els preus del catàleg de productes a les llistes de preus del projecte. Les llistes de preus del projecte són exclusives del Project Operations. La lògica empresarial específica de l'aplicació copia les llistes de preus d'una oferta a un contracte. El resultat és una llista de preus de projecte específica per al contracte. L'operació de còpia pot retardar el procés de guanyar l'oferta si la llista de preus del projecte de l'oferta es fa massa gran. Les llistes de preus del producte no es copien per crear llistes de preus personalitzades en els contractes. Com que no hi ha cap còpia involucrada, el rendiment del procés d'oferta no està afectat.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]