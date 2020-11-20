---
title: Configuració de les tarifes de cost i de vendes per als productes del catàleg (bàsic)
description: Aquest tema proporciona informació sobre com configurar els costos i les tarifes de venda dels articles en un catàleg de productes.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 135b182af73bdab7a3520589431332ad059ec497
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176689"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a>Configuració de les tarifes de cost i de vendes per als productes del catàleg (bàsic)

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_


La configuració de preus per als articles del catàleg de productes al Dynamics 365 Project Operations és la mateixa que al Dynamics 365 Sales.

Com que els productes no es poden estimar o utilitzar en projectes del Project Operations no hi ha necessitat d'establir preus de catàleg de producte en llistes de preus de projecte per a les ofertes i els contractes.

Els preus del catàleg de productes s'han d'establir en el camp **Preu de producte** d'una oferta, contracte o compte. No configureu els preus del catàleg de productes a les llistes de preus del projecte per a aquestes entitats. Les llistes de preus del projecte són exclusives del Project Operations. Hi ha una lògica empresarial específica de l'aplicació que copia les llistes de preus d'una oferta a un contracte. El resultat és una llista de preus de projecte específica per al contracte. L'operació de còpia pot retardar el procés de guanyar l'oferta si la llista de preus del projecte de l'oferta es fa massa gran. Les llistes de preus del producte no es copien per crear llistes de preus personalitzades en els contractes. Això vol dir que les llistes de preus del producte no afecten el rendiment del procés de guanyar les ofertes.
