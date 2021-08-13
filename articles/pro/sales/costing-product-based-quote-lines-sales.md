---
title: Càlcul de costos de les línies d'oferta basades en productes
description: En aquest tema es proporciona informació sobre l'aplicació d'un preu de cost a una línia d'oferta basada en productes.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: d9c03fa1a8f43cc110565efbafd7f5aba69f65f96bec7f15f2bd492123f639c7
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "7001869"
---
# <a name="costing-product-based-quote-lines"></a>Càlcul de costos de les línies d'oferta basades en productes

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_


Les línies d'oferta basades en productes al Dynamics 365 Project Operations també tenen un camp de **Preu de cost**. Aquest camp s'utilitza per fer el seguiment del preu de cost del producte a la línia d'oferta i per als càlculs de rendibilitat descendents.

Quan es crea una línia d'oferta basada en productes per a un producte del catàleg, el cost de la línia d'oferta basada en productes és per defecte el del camp **Cost estàndard** del catàleg de productes. El camp de cost estàndard del catàleg de productes està configurat a la moneda base de l'organització. El cost per unitat per defecte de la línia d'oferta basada en productes es converteix a la moneda de vendes de l'oferta.

## <a name="unit-cost-on-a-product-based-quote-line"></a>Cost per unitat en una línia d'oferta basada en productes

El propòsit de tenir un cost unitari en una línia d'oferta basada en productes és el de permetre diferents costos d'un producte per a cada venda. Aquest no és un escenari tipic, però de vegades el cost del producte pot ser descomptat pel proveïdor en funció del client de la venda definitiva.

Per exemple:

Fabrikam Robotics està instal·lant braços robòtics a les línies de muntatge d'A Datum Corporation. Fabrikam ofereix serveis d'instal·lació però els braços robotitzats els fabrica Trey Robotics. Si la instal·lació de braços robòtics a A Datum Corporation obre un nou sector industrial per als braços robòtics de Trey, Trey podria oferir un descompte especial per aquest contracte a Fabrikam.

En aquest cas, Fabrikam crearà una línia d'oferta basada en productes per a braços robòtics i un cost especial per unitat per a aquesta oferta. Aquest cost és diferent del cost estàndard de braços robòtics de Trey.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]