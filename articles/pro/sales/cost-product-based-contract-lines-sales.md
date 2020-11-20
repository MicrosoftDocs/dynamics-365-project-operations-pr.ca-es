---
title: Càlcul de costos de línies de contracte basades en productes (bàsic)
description: Aquest tema proporciona informació sobre la creació
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0e961bcf32a5dd662b7cd27a23eb5f664c45c292
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177229"
---
# <a name="cost-product-based-contract-lines---lite"></a>Càlcul de costos de línies de contracte basades en productes (bàsic)

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_


Les línies de contracte basades en el producte al Dynamics 365 Project Operations inclouen el camp **Preu de cost**, que emmagatzema el preu de cost del producte per als càlculs de rendibilitat posteriors.

Quan es crea una línia de contracte basada en productes per a un producte del catàleg, el cost de la línia de contracte basada en productes és per defecte el del camp **Cost estàndard** del catàleg de productes. El camp **Cost estàndard** del catàleg de productes està configurat a la moneda base de l'organització. Quan el cost unitari per defecte és el de la línia de contracte, es converteix a la moneda de venda del contracte.

## <a name="unit-cost-on-a-product-based-contract-line"></a>Cost per unitat en una línia de contracte basada en productes

Tenir un cost unitari en una línia de contracte basada en el producte permet diferents costos de producte per a cada venda d'una unitat. Encara que no sempre és necessari, hi ha algunes situacions en les quals el proveïdor pot descomptar el cost del producte per al client. Tingueu en compte aquesta hipotètica situació:

Fabrikam Robotics està instal·lant braços robòtics a les línies de muntatge d'Adatum Corporation. Fabrikam ofereix serveis d'instal·lació però els braços robotitzats els fabrica Trey Research. Si la instal·lació de braços robòtics a Adatum Corporation obre un nou sector industrial per a Trey Research, podria oferir un descompte especial per aquest contracte a Fabrikam. En aquest cas, Fabrikam crea una línia de contracte basada en el producte per a braços robòtics i introdueix un cost per unitat per a aquest contracte que és diferent del cost estàndard dels braços robòtics de Trey Research.
