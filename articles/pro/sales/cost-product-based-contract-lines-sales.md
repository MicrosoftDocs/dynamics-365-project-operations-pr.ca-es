---
title: Càlcul de costos de línies de contracte basades en productes (bàsic)
description: Aquest article proporciona informació sobre la creació
author: rumant
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: a63ad12c081d19efde02303bf626184f8586d4a2
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922900"
---
# <a name="cost-product-based-contract-lines---lite"></a>Càlcul de costos de línies de contracte basades en productes (bàsic)

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_


Les línies de contracte basades en productes al Dynamics 365 Project Operations inclouen el camp **Preu de cost**, que emmagatzema el preu de cost del producte per als càlculs de rendibilitat posteriors.

Quan es crea una línia de contracte basada en productes per a un producte del catàleg, el cost de la línia ve per defecte del camp **Cost estàndard** del catàleg de productes. El camp **Cost estàndard** del catàleg de productes està configurat a la moneda base de l'organització. Quan el cost unitari per defecte és el de la línia de contracte, es converteix a la moneda de venda del contracte.

## <a name="unit-cost-on-a-product-based-contract-line"></a>Cost per unitat en una línia de contracte basada en productes

Tenir un cost unitari en una línia de contracte basada en el producte permet diferents costos de producte per a cada venda d'una unitat. Encara que no sempre és necessari, hi ha algunes situacions en les quals el proveïdor pot descomptar el cost del producte per al client. Tingueu en compte aquesta hipotètica situació:

Fabrikam Robotics està instal·lant braços robòtics a les línies de muntatge d'Adatum Corporation. Fabrikam proporciona serveis d'instal·lació, però els braços robòtics són de Trey Research. Si la instal·lació de braços robòtics a Adatum Corporation obre un nou sector industrial per a Trey Research, podria oferir un descompte especial per aquest contracte a Fabrikam. En aquest cas, Fabrikam crea una línia de contracte basada en productes per a braços robòtics. S'introdueix un cost per unitat per a aquest contracte. El cost és diferent del cost dels braços robòtics de Trey Research.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]