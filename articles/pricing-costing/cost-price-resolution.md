---
title: Resolució dels preus de cost per a les estimacions i els valors reals
description: Aquest tema proporciona informació sobre com es resolen els preus de cost en les estimacions i els valors reals.
author: rumant
ms.date: 04/09/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f9a6c3236c1d523a967155d3f1fdbe05aa00001bcc36b38afd86270c4cd1d7cc
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "7003669"
---
# <a name="resolving-cost-prices-for-estimates-and-actuals"></a>Resolució dels preus de cost per a les estimacions i els valors reals

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

Per resoldre els preus de cost i la llista de preus de cost per a les estimacions i els valors reals, el sistema utilitza la informació en els camps **Data**, **Moneda** i **Unitat contractant** del projecte relacionat. Després de resoldre la llista de preus de cost, l'aplicació resol la tarifa de cost.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Resolució de tarifes de cost en línies de valors reals i estimacions per al temps

Les línies estimades per a temps fan referència a l'oferta i els detalls de la línia de contracte per a les assignacions de temps i recursos en un projecte.

Després de resoldre una llista de preus, el sistema utilitza els camps **Funció**, **Empresa de recursos** i **Unitat de recursos** en la línia d'estimació de temps per a la coincidència amb les línies de preu per funció en la llista de preus. Aquesta assignació assumeix que esteu utilitzant dimensions de preus de fàbrica per al cost del treball. Si heu configurat el sistema perquè coincideixi amb els camps en lloc de, o a més de **Funció**, **Empresa de recursos** i **Unitat de recursos**, llavors s'utilitzarà una combinació diferent per recuperar una línia de preu per funció coincident. Si l'aplicació troba una línia de preu per funció que té una tarifa de cost per a la combinació **Funció**, **Empresa de recursos** i **Unitat de recursos**, aquesta és la tarifa de cost per defecte. Si l'aplicació no pot coincidir exactament amb la combinació dels valors **Funció**, **Empresa de dotació de recursos** i **Unitat de dotació de recursos**, recuperarà les línies de preu de les funcions amb un valor de funció coincident, però tindrà valors nuls per a la **Unitat de dotació de recursos** i l'**Empresa de dotació de recursos**. Després de trobar un registre de preu de funció coincident amb el valor de preu de la funció, s'utilitza per defecte el valor del preu de cost d'aquest registre. 

> [!NOTE]
> Si configureu una priorització diferent de **Funció**, **Empresa de recursos** i **Unitat de recursos**, o si teniu altres dimensions que tenen una prioritat més alta, aquest comportament canviarà en conseqüència. El sistema recupera registres de preu de funció amb valors que coincideixen amb cadascun dels valors de dimensió de preus per ordre de prioritat amb files que tenen valors nuls per a aquelles dimensions que són als últims llocs en l'ordre de prioritat.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Resolució de tarifes de cost en línies de valors reals i estimacions per a les despeses

Les línies estimades per a despeses fan referència a l'oferta i els detalls de la línia de contracte per a les despeses i línies d'estimació de despeses en un projecte.

Després de resoldre una llista de preus, el sistema utilitza una combinació dels camps **Categoria** i **Unitat** en la línia d'estimació per a una despesa per a la coincidència amb les línies **Preu per categoria** en la llista de preus resolta. Si el sistema troba una línia de preu per categoria que té una tarifa de cost per a la combinació de camps **Categoria** i **Unitat**, aquesta és la tarifa de cost per defecte. Si el sistema no pot fer coincidir els valors **Categoria** i **Unitat**, o si pot trobar una línia de preu de categoria coincident però el mètode de preu no és **Preu per unitat**, la tarifa de cost per defecte és zero (0).

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-material"></a>Resolució de percentatges de cost de les línies de valor real i de previsió de materials

Les línies d'estimació per a materials fan referència als detalls de les ofertes i de les línies de contracte per als materials i les línies de previsió de materials d'un projecte.

Després de resoldre una llista de preus de cost, el sistema utilitza una combinació dels camps **Producte** i **Unitat** de la línia de previsió per tal que una estimació de material coincideixi amb les línies **Elements de la llista de preus** de la llista de preus resolta. Si el sistema troba una línia de preu de producte que té una tarifa de cost per a la combinació dels camps **Producte** i **Unitat**, la tarifa de cost s'utilitza per defecte. Si el sistema no pot fer coincidir els valors de **Producte** i **Unitat**, s'utilitza el cost unitari zero per defecte. Aquest valor per defecte també succeeix si hi ha una línia d'element de la llista de preus coincident, però el mètode de càlcul de preus es basa en un cost estàndard o un cost corrent que no està definit al producte.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
