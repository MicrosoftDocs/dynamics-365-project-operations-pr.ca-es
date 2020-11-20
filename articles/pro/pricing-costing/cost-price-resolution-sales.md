---
title: Resolució dels preus de cost per a les estimacions i els valors reals (bàsic)
description: Aquest tema proporciona informació sobre com es resolen els preus de cost en les estimacions i els valors reals.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3fedf7b577e2372fb10ea85ea1e3caa9bf2f5ad0
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176779"
---
# <a name="resolve-cost-prices-on-estimates-and-actuals---lite"></a>Resolució dels preus de cost per a les estimacions i els valors reals (bàsic)

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_

Per resoldre els preus de cost i la llista de preus de cost per a les estimacions i els valors reals, el sistema utilitza la informació en els camps **Data**, **Moneda** i **Unitat contractant** del projecte relacionat. Després de resoldre la llista de preus de cost, l'aplicació resol la tarifa de cost.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Resolució de tarifes de cost en línies de valors reals i estimacions per al temps

Les línies estimades per a temps fan referència a l'oferta i els detalls de la línia de contracte per a les assignacions de temps i recursos en un projecte.

Després de resoldre una llista de preus, el sistema utilitza els camps **Funció** i **Unitat de recursos** en la línia d'estimació de temps per a la coincidència amb les línies de preu per funció en la llista de preus. Aquesta assignació assumeix que esteu utilitzant dimensions de preus de fàbrica per al cost del treball. Si heu configurat el sistema perquè coincideixi amb els camps en lloc de, o a més de **Funció** i **Unitat de recursos**, llavors s'utilitzarà una combinació diferent per recuperar una línia de preu per funció coincident. Si l'aplicació troba una línia de preu per funció que té una tarifa de cost per a la combinació **Funció** i **Unitat de recursos**, aquesta és la tarifa de cost per defecte. Si l'aplicació no pot fer coincidir els valors **Funció** i **Unitat de recursos**, llavors recupera les línies de preu per funció amb una funció coincident, però valors nuls de la **Unitat de recursos**. Després que tingui un registre de preu per funció coincident, la tarifa de cost pren el valor per defecte d'aquest registre. 

> [!NOTE]
> Si configureu una priorització diferent de **Funció** i **Unitat de recursos**, o si teniu altres dimensions que tenen una prioritat més alta, aquest comportament canviarà en conseqüència. El sistema recupera els registres de preus per funció amb valors que coincideixen amb cadascun dels valors de la dimensió de preus en ordre de prioritat amb les files que tenen valors nuls per a aquestes dimensions al final.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Resolució de tarifes de cost en línies de valors reals i estimacions per a les despeses

Les línies estimades per a despeses fan referència a l'oferta i els detalls de la línia de contracte per a les despeses i línies d'estimació de despeses en un projecte.

Després de resoldre una llista de preus, el sistema utilitza una combinació dels camps **Categoria** i **Unitat** en la línia d'estimació per a una despesa per a la coincidència amb les línies **Preu per categoria** en la llista de preus resolta. Si el sistema troba una línia de preu per categoria que té una tarifa de cost per a la combinació de camps **Categoria** i **Unitat**, aquesta és la tarifa de cost per defecte. Si el sistema no pot fer coincidir els valors **Categoria** i **Unitat**, o si pot trobar una línia de preu de categoria coincident però el mètode de preu no és **Preu per unitat**, la tarifa de cost per defecte és zero (0).
