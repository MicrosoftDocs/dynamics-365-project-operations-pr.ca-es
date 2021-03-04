---
title: Resolució dels preus de venda per a les estimacions i els valors reals (bàsic)
description: Aquest tema proporciona informació sobre la resolució dels preus de venda en estimacions i valors reals.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 92cebbe851c3cface86d0580e7e060134295e8c2
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176734"
---
# <a name="resolve-sales-prices-for-estimates-and-actuals---lite"></a>Resolució dels preus de venda per a les estimacions i els valors reals (bàsic)

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_

Quan els preus de venda en les estimacions i els valors reals es resolen al Dynamics 365 Project Operations, el sistema primer utilitza la data i la moneda de l'oferta del projecte o contracte relacionat per resoldre la llista de preus de vendes. Després de resoldre la llista de preus de vendes, el sistema resol la tarifa de vendes o de facturació.

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-time"></a>Resolució de tarifes de vendes en línies de valors reals i estimacions per al temps

Al Project Operations, les línies d'estimació per al temps s'utilitzen per denotar la línia d'oferta i els detalls de la línia de contracte per a les assignacions de temps i recursos en el projecte.

Després de resoldre una llista de preus per a les vendes, el sistema completa els següents passos per obtenir la tarifa de facturació per defecte.

1. El sistema utilitza els camps **Funció** i **Unitat de recursos** en la línia d'estimació de temps per a la coincidència amb les línies de preu per funció en la llista de preus resolts. Aquesta assignació assumeix que esteu utilitzant dimensions de preus de fàbrica per a les tarifes de facturació. Si heu configurat el preu en funció de qualsevol altre camp en comptes de, o a més de **Funció** i **Unitat de recursos**, llavors aquesta és la combinació que s'utilitzarà per recuperar una línia de preu per funció coincident.
2. Si el sistema troba una línia de preu per funció que té una tarifa de facturació per la combinació de camps **Funció** i **Unitat de recursos**, llavors la tarifa de facturació és el valor per defecte.
3. Si el sistema no és capaç de fer coincidir els valors dels camps **Funció** i **Unitat de recursos**, llavors recupera línies de preu per funció amb una funció coincident però valors nuls per a **Unitat de recursos**. Després que el sistema trobi un registre de preu per funció coincident, la tarifa de facturació per defecte és la d'aquest registre. Aquesta assignació assumeix una configuració de fàbrica per a la prioritat relativa de **Funció** i **Unitat de recursos** com a dimensió de preus de vendes.

> [!NOTE]
> Si configureu una priorització diferent de **Funció** i **Unitat de recursos**, o si teniu altres dimensions que tenen una prioritat més alta, aquest comportament canviarà en conseqüència. El sistema recupera els registres de preus per funció amb valors coincidents amb cadascun dels valors de la dimensió de preus en ordre de prioritat amb les files que tenen valors nuls per a aquestes dimensions al final.

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-expense"></a>Resolució de tarifes de vendes en línies de valors reals i estimacions per a les despeses

Al Project Operations, les línies d'estimació per a les despeses s'utilitzen per denotar la línia d'oferta i els detalls de la línia de contracte per a les despeses i línies d'estimació de despeses en el projecte.

Després de resoldre una llista de preus per a les vendes, el sistema completa els següents passos per obtenir el preu de venda per unitat per defecte.

1. El sistema utilitza la combinació dels camps **Categoria** i **Unitat** a la línia de despesa estimada per assignar-los a les línies de preu de categoria en la llista de preus resolta.
2. Si el sistema troba una línia de preu per categoria que té una tarifa de venda per a la combinació de camps **Categoria** i **Unitat**, aquesta és la tarifa de venda per defecte.
3. Si el sistema troba una línia de preu per categoria coincident, el mètode de preus es pot utilitzar per determinar el preu de venda per defecte. La següent taula mostra el comportament per determinar el preu per defecte de les despeses al Project Operations.

    | Context | Mètode de càlcul de preus | Preu per defecte |
    | --- | --- | --- |
    | Aproximat | Preu per unitat | Basat en la línia de preus per categoria |
    | &nbsp; | A partir del cost | 0.00 |
    | &nbsp; | Marge comercial sobre el cost | 0.00 |
    | Real | Preu per unitat | Basat en la línia de preus per categoria |
    | &nbsp; | A partir del cost | Basat en el valor real de cost relacionat |
    | &nbsp; | Marge comercial sobre el cost | Aplicar un marge comercial tal com defineix la línia de preus de categoria a la tarifa de cost unitari del valor real de cost relacionat |

4. Si el sistema no pot fer coincidir els valors dels camps **Categoria** i **Unitat**, la tarifa de vendes per defecte és zero (0).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]