---
title: Resolució dels preus de venda per a les estimacions i els valors reals del projecte
description: En aquest tema es proporciona informació sobre com es resolen els preus de venda de les estimacions i els valors reals del projecte.
author: rumant
manager: Annbe
ms.date: 04/07/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3bf4686b414300370e6b364834b33edad98b7f39
ms.sourcegitcommit: ac90be6106592f883a0de39a75836fb40255d65a
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/09/2021
ms.locfileid: "5877344"
---
# <a name="resolve-sales-prices-for-project-estimates-and-actuals"></a>Resolució dels preus de venda per a les estimacions i els valors reals del projecte

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_

Quan els preus de venda de les estimacions i els valors reals es resolen al Dynamics 365 Project Operations, el sistema utilitza primer la data i la moneda de l'oferta o el contracte de projecte relacionats per resoldre la llista de preus de venda. Després de resoldre la llista de preus de vendes, el sistema resol la tarifa de vendes o de facturació.

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

## <a name="resolving-sales-rates-on-actual-and-estimate-lines-for-material"></a>Resolució de percentatges de vendes de les línies de valor real i de previsió de materials

A Project Operations, les línies d'estimació per a materials s'utilitzen per indicar els detalls de línia d'oferta i de línia de contracte per als materials i les línies de previsió de materials d'un projecte.

Després de resoldre una llista de preus per a les vendes, el sistema completa els següents passos per obtenir el preu de venda per unitat per defecte.

1. El sistema utilitza la combinació de camp **Producte** i **Unitat** de la línia de previsió perquè el material coincideixi amb les línies d'element de la llista de preus de la llista de preus resolta.
2. Si el sistema troba una línia d'element de la llista de preus que té un percentatge de vendes per a la combinació de camps **Producte** i **Unitat** i el mètode de càlcul de preus és **Quantitat de moneda**, s'utilitza el preu de venda que s'especifica a la línia de la llista de preus.
3. Si els valors dels camps **Producte** i **Unitat** no coincideixen, s'utilitza el percentatge de vendes zero per defecte.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
