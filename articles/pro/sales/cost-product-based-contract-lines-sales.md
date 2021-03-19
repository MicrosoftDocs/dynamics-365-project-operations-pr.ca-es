---
title: Càlcul de costos de línies de contracte basades en productes (bàsic)
description: Aquest tema proporciona informació sobre la creació
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 001b0b54abcdd5fcd1eca7f3271cc78392f68860
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273681"
---
# <a name="cost-product-based-contract-lines---lite"></a>Càlcul de costos de línies de contracte basades en productes (bàsic)

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_


Les línies de contracte basades en productes al Dynamics 365 Project Operations inclouen el camp **Preu de cost**, que emmagatzema el preu de cost del producte per als càlculs de rendibilitat posteriors.

Quan es crea una línia de contracte basada en productes per a un producte del catàleg, el cost de la línia ve per defecte del camp **Cost estàndard** del catàleg de productes. El camp **Cost estàndard** del catàleg de productes està configurat a la moneda base de l'organització. Quan el cost unitari per defecte és el de la línia de contracte, es converteix a la moneda de venda del contracte.

## <a name="unit-cost-on-a-product-based-contract-line"></a>Cost per unitat en una línia de contracte basada en productes

Tenir un cost unitari en una línia de contracte basada en el producte permet diferents costos de producte per a cada venda d'una unitat. Encara que no sempre és necessari, hi ha algunes situacions en les quals el proveïdor pot descomptar el cost del producte per al client. Tingueu en compte aquesta hipotètica situació:

Fabrikam Robotics està instal·lant braços robòtics a les línies de muntatge d'Adatum Corporation. Fabrikam proporciona serveis d'instal·lació, però els braços robòtics són de Trey Research. Si la instal·lació de braços robòtics a Adatum Corporation obre un nou sector industrial per a Trey Research, podria oferir un descompte especial per aquest contracte a Fabrikam. En aquest cas, Fabrikam crea una línia de contracte basada en productes per a braços robòtics. S'introdueix un cost per unitat per a aquest contracte. El cost és diferent del cost dels braços robòtics de Trey Research.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]