---
title: Resolució dels preus de cost per a les estimacions i els valors reals
description: Aquest tema proporciona informació sobre com es resolen els preus de cost en les estimacions i els valors reals.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c2fe2a15d38ab5a1f2a93c6db4ed6b7eb9bbd33d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275661"
---
# <a name="resolving-cost-prices-for-estimates-and-actuals"></a>Resolució dels preus de cost per a les estimacions i els valors reals

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

Per resoldre els preus de cost i la llista de preus de cost per a les estimacions i els valors reals, el sistema utilitza la informació en els camps **Data**, **Moneda** i **Unitat contractant** del projecte relacionat. Després de resoldre la llista de preus de cost, l'aplicació resol la tarifa de cost.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Resolució de tarifes de cost en línies de valors reals i estimacions per al temps

Les línies estimades per a temps fan referència a l'oferta i els detalls de la línia de contracte per a les assignacions de temps i recursos en un projecte.

Després de resoldre una llista de preus, el sistema utilitza els camps **Funció**, **Empresa de recursos** i **Unitat de recursos** en la línia d'estimació de temps per a la coincidència amb les línies de preu per funció en la llista de preus. Aquesta assignació assumeix que esteu utilitzant dimensions de preus de fàbrica per al cost del treball. Si heu configurat el sistema perquè coincideixi amb els camps en lloc de, o a més de **Funció**, **Empresa de recursos** i **Unitat de recursos**, llavors s'utilitzarà una combinació diferent per recuperar una línia de preu per funció coincident. Si l'aplicació troba una línia de preu per funció que té una tarifa de cost per a la combinació **Funció**, **Empresa de recursos** i **Unitat de recursos**, aquesta és la tarifa de cost per defecte. Si l'aplicació no pot fer coincidir els valors **Funció**, **Empresa de recursos** i **Unitat de recursos**, llavors recupera les línies de preu per funció amb una funció coincident, però valors nuls de la **Unitat de recursos**. Després que tingui un registre de preu per funció coincident, la tarifa de cost pren el valor per defecte d'aquest registre. 

> [!NOTE]
> Si configureu una priorització diferent de **Funció**, **Empresa de recursos** i **Unitat de recursos**, o si teniu altres dimensions que tenen una prioritat més alta, aquest comportament canviarà en conseqüència. El sistema recupera els registres de preus per funció amb valors que coincideixen amb cadascun dels valors de la dimensió de preus en ordre de prioritat amb les files que tenen valors nuls per a aquestes dimensions al final.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Resolució de tarifes de cost en línies de valors reals i estimacions per a les despeses

Les línies estimades per a despeses fan referència a l'oferta i els detalls de la línia de contracte per a les despeses i línies d'estimació de despeses en un projecte.

Després de resoldre una llista de preus, el sistema utilitza una combinació dels camps **Categoria** i **Unitat** en la línia d'estimació per a una despesa per a la coincidència amb les línies **Preu per categoria** en la llista de preus resolta. Si el sistema troba una línia de preu per categoria que té una tarifa de cost per a la combinació de camps **Categoria** i **Unitat**, aquesta és la tarifa de cost per defecte. Si el sistema no pot fer coincidir els valors **Categoria** i **Unitat**, o si pot trobar una línia de preu de categoria coincident però el mètode de preu no és **Preu per unitat**, la tarifa de cost per defecte és zero (0).


[!INCLUDE[footer-include](../includes/footer-banner.md)]