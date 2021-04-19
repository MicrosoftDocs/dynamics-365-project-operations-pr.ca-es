---
title: Resolució dels preus de cost per a les estimacions i els valors reals de projecte
description: En aquest tema es proporciona informació sobre com es resolen els preus de cost de les estimacions i els valors reals del projecte.
author: rumant
manager: Annbe
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9f20631f41c560f1a4047aaaa624fa4e8651c687
ms.sourcegitcommit: ac90be6106592f883a0de39a75836fb40255d65a
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/09/2021
ms.locfileid: "5877253"
---
# <a name="resolve-cost-prices-on-project-estimates-and-actuals"></a>Resolució dels preus de cost per a les estimacions i els valors reals de projecte 

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_

Per resoldre els preus de cost i la llista de preus de cost per a les estimacions i els valors reals, el sistema utilitza la informació en els camps **Data**, **Moneda** i **Unitat contractant** del projecte relacionat. Després de resoldre la llista de preus de cost, l'aplicació resol la tarifa de cost.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Resolució de tarifes de cost en línies de valors reals i estimacions per al temps

Les línies estimades per a temps fan referència a l'oferta i els detalls de la línia de contracte per a les assignacions de temps i recursos en un projecte.

Després de resoldre una llista de preus de cost, els camps **Funció** i **Unitat de recursos** de la línia de previsió per a Temps es relacionen amb les línies de preu de la funció de la llista de preus. Aquesta coincidència suposa que utilitzeu les mètriques de preus estàndard per al cost laboral. Si heu configurat el sistema perquè coincideixi amb els camps en lloc de, o a més de **Funció** i **Unitat de recursos**, llavors s'utilitzarà una combinació diferent per recuperar una línia de preu per funció coincident. Si l'aplicació troba una línia de preu per funció que té una tarifa de cost per a la combinació **Funció** i **Unitat de recursos**, aquesta és la tarifa de cost per defecte. Si l'aplicació no pot fer coincidir els valors **Funció** i **Unitat de recursos**, llavors recupera les línies de preu per funció amb una funció coincident, però valors nuls de la **Unitat de recursos**. Després que tingui un registre de preu per funció coincident, la tarifa de cost pren el valor per defecte d'aquest registre. 

> [!NOTE]
> Si configureu una priorització diferent de **Funció** i **Unitat de recursos**, o si teniu altres dimensions que tenen una prioritat més alta, aquest comportament canviarà en conseqüència. El sistema recupera els registres de preus per funció amb valors que coincideixen amb cadascun dels valors de la dimensió de preus en ordre de prioritat amb les files que tenen valors nuls per a aquestes dimensions al final.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Resolució de tarifes de cost en línies de valors reals i estimacions per a les despeses

Les línies estimades per a despeses fan referència a l'oferta i els detalls de la línia de contracte per a les despeses i línies d'estimació de despeses en un projecte.

Després de resoldre una llista de preus de cost, el sistema utilitza una combinació dels camps **Categoria** i **Unitat** de la línia de previsió de despeses per tal que coincideixi amb les línies de **Preu de categoria** de la llista de preus resolta. Si el sistema troba una línia de preu per categoria que té una tarifa de cost per a la combinació de camps **Categoria** i **Unitat**, aquesta és la tarifa de cost per defecte. Si el sistema no pot fer coincidir els valors **Categoria** i **Unitat**, o si és possible trobar una línia de preu de categoria que coincideixi, però el mètode de preus no és **Preu per unitat**, el valor per defecte del percentatge de cost és zero(0).

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-material"></a>Resolució de percentatges de cost de les línies de valor real i de previsió de materials

Les línies d'estimació per a materials fan referència als detalls de les ofertes i de les línies de contracte per als materials i les línies de previsió de materials d'un projecte.

Després de resoldre una llista de preus de cost, el sistema utilitza una combinació dels camps **Producte** i **Unitat** de la línia de previsió per tal que una estimació de material coincideixi amb les línies **Elements de la llista de preus** de la llista de preus resolta. Si el sistema troba una línia de preu de producte que té una tarifa de cost per a la combinació dels camps **Producte** i **Unitat**, la tarifa de cost s'utilitza per defecte. Si el sistema no pot fer coincidir els valors **Producte** i **Unitat**, o si és possible trobar una línia d'element de la llista de preus coincident, però el mètode de càlcul de preus es basa en el Cost estàndard o el Cost actual i tampoc es defineix al producte, el cost per defecte de la unitat tindrà per defecte el valor zero.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
