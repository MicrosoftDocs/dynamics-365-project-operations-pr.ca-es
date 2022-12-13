---
title: Configurar la conversió de moneda per calcular els preus de venda a partir de les taxes de cost
description: En aquest article s'explica com configurar el comportament de conversió de moneda que s'utilitzarà a Microsoft Dynamics 365 Project Operations quan es generin transaccions de vendes a partir de transaccions de cost.
author: rumant
ms.date: 11/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3fa8077deb18f1a54e7f0f5e6dc4491a830df45b
ms.sourcegitcommit: 95e52fcf012a51229f3f6ae7dbf7b0fa56072a85
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 12/01/2022
ms.locfileid: "9816686"
---
# <a name="set-up-currency-conversion-to-calculate-sales-prices-from-cost-rates"></a>Configurar la conversió de moneda per calcular els preus de venda a partir de les taxes de cost

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

A Microsoft Dynamics 365 Project Operations, els preus de venda de les categories de despeses es poden configurar com a valors numèrics o bé es poden configurar de manera que es calculin en funció del cost en què s'hagi incorregut.

Quan estan configurats per calcular-los en funció del cost incorregut, hi ha disponibles les opcions següents:

- A partir del cost
- Marqueu el percentatge sobre el cost

En els escenaris en què el cost de la despesa s'incorre en una moneda diferent de la moneda de venda del contracte del projecte, es requereix la conversió de moneda per calcular el preu de venda en funció del cost.

## <a name="currency-conversion-behavior-that-uses-native-dataverse-exchange-rates"></a>Comportament de conversió de moneda que utilitza tipus de canvi natius Dataverse 

Per defecte, Project Operations utilitza els tipus de canvi de moneda que s'emmagatzemen a la taula Moneda Dataverse. Per configurar Project Operations perquè utilitzi tipus de canvi natius per calcular els preus de venda a partir del cost, seguiu aquests passos.

1. Aneu a **Paràmetres de configuració \> de les operacions \> del projecte**.
1. Obriu la pàgina de detalls del **paràmetre de** projecte.
1. Definiu el **camp Lògica** de conversió de moneda en un valor en blanc.

## <a name="currency-conversion-behavior-that-uses-exchange-rates-from-finance-and-operations-apps"></a>Comportament de conversió de moneda que utilitza tipus de canvi d'aplicacions de finances i operacions

Els tipus de canvi de la taula Moneda que hi ha disponibles Dataverse de forma nativa no tenen data d'efecte. Per tant, és possible que no sempre s'ajustin als requisits que teniu per al càlcul dels preus de venda a partir de les tarifes de cost.

Podeu utilitzar els tipus de canvi de l'entorn financer i d'operacions per calcular el preu de venda en la moneda de venda a partir d'una taxa de cost a la moneda de cost. Per configurar aquest comportament de conversió de moneda, seguiu aquests passos.

1. A la **pàgina Paràmetres** del projecte, afegiu el **camp Lògica de conversió de** moneda. A continuació, deseu i publiqueu la personalització.
1. Aneu a **Paràmetres de configuració \> de les operacions \> del projecte**.
1. Obriu la pàgina de detalls del **paràmetre de** projecte. 
1. Definiu el **camp Comportament** de conversió de moneda a **Ampliat amb reserva alternativa al valor predeterminat**.
1. Doneu permís de lectura a l'usuari **·**  de doble escriptura funció de seguretat **Global a** les taules següents:

    - Moneda msdynexchangerates\_
    - msdyn\_ currencyexchangeratepairs
    - msdyn\_ exchangeratetypes

1. Al vostre entorn de finances i operacions, executeu els següents mapes de doble escriptura amb sincronització inicial:

    - Tipus de canvi (tipus de canvi msdyn\_)
    - Parell de divises de tipus de canvi (msdyn\_ currencyexchangeratepairs)
    - Tipus de canvi CDS (msdyn\_ currencyexchangerates)

Un cop completats aquests canvis, la doble escriptura farà que els tipus de canvi de l'entorn financer i d'operacions estiguin disponibles. Dataverse A continuació, Project Operations utilitzarà aquests tipus de canvi per convertir els tipus de cost en la moneda de venda del contracte.

> [!NOTE]
> Aquest comportament de conversió de moneda només s'aplica al càlcul dels preus de venda a partir de les taxes de cost. No s'utilitzarà per calcular genèricament els valors de la moneda base. Els valors de la moneda base sempre utilitzaran tipus de canvi natius Dataverse , independentment de si completeu aquest procediment.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
