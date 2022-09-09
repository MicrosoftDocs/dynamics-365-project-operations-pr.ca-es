---
title: Determineu les taxes de costos per a les estimacions i els reals del projecte
description: Aquest article proporciona informació sobre com es determinen les taxes de costos per a les estimacions i els reals del projecte.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c7dd264ebbd1da9b2f42d2284fb38988a09aa03f
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410088"
---
# <a name="determine-cost-rates-for-project-estimates-and-actuals"></a>Determineu les taxes de costos per a les estimacions i els reals del projecte

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_

Per determinar la llista de preus de cost i les taxes de cost en l'estimació i els contextos reals, el sistema utilitza la informació dels **camps Data**, **Moneda** i **Unitat** de contractació del projecte relacionat.

## <a name="determining-cost-rates-in-estimate-and-actual-contexts-for-time"></a>Determinació de taxes de costos en l'estimació i contextos reals de Time

El context d'estimació **del temps** es refereix a:

- Detalls de la línia de pressupost per a **Time**.
- Dades de la línia de contracte per a **Time**.
- Assignacions de recursos sobre un projecte.

El context real del **temps** es refereix a:

- Línies de diari d'entrada i correcció del **temps**.
- Línies de diari que es creen quan s'envia una entrada de temps.

Després de determinar una llista de preus de cost, el sistema completa els passos següents per introduir la taxa de cost predeterminada.

1. El sistema coincideix amb la combinació dels **camps Role** i **Resourcing Unit** en l'estimació o context real de **Time** amb les línies de preus de rol de la llista de preus. Aquesta coincidència suposa que utilitzeu les dimensions de preus estàndard per al cost laboral. Si heu configurat el sistema perquè coincideixi amb camps que no siguin o a **més de La funció** i **la unitat** de recursos, s'utilitza una combinació diferent per recuperar una línia de preus de rol coincident.
1. Si el sistema troba una línia de preus de rol que té una taxa de cost per a la combinació d'unitats **de** funció **i** recurs, aquesta taxa de cost s'utilitza com a taxa de cost per defecte.
1. Si el sistema no pot coincidir amb els valors de la **unitat** de funció **i** recurs, recupera les línies de preus de la funció que tenen valors coincidents per al **camp Funció**, però valors nuls per al **camp Unitat** de recursos. Després que el sistema tingui un registre de preus de funció coincident, la taxa de cost d'aquest registre s'utilitzarà com a taxa de cost predeterminada.

> [!NOTE]
> Si configureu una priorització diferent dels camps Funció **i** Unitat **de** recursos, o si teniu altres dimensions que tenen més prioritat, el comportament anterior canviarà en conseqüència. El sistema recupera registres de preus de funció que tenen valors que coincideixen amb cada valor de dimensió de preus per ordre de prioritat. Les files que tenen valors nuls per a aquestes dimensions són les últimes.

## <a name="determining-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Determinació de les taxes de cost en línies reals i d'estimació de despeses

El context d'estimació **de la despesa** es refereix a:

- Detalls de la línia de pressupostos per a **despeses**.
- Dades de la línia de contractació de **despesa**.
- Estimacions de despeses d'un projecte.

El context real de **la despesa** es refereix a:

- Registre i correcció de línies de registre de **despeses**.
- Línies de diari que es creen quan s'envia una entrada de despeses.

Després de determinar una llista de preus de cost, el sistema completa els passos següents per introduir la taxa de cost predeterminada.

1. El sistema coincideix amb la combinació dels **camps Categoria** i **Unitat** en l'estimació o context real de **Despesa** amb les línies de preus de categoria de la llista de preus.
1. Si el sistema troba una línia de preus de categoria que té una taxa de cost per a la **combinació de categoria** i **unitat**, aquesta taxa de cost s'utilitza com a taxa de cost predeterminada.
1. Si el sistema no pot coincidir amb els **valors Categoria** i **Unitat**, el preu s'estableix en **0** (zero) per defecte.
1. En el context de l'estimació, si el sistema pot trobar una línia de preus de categoria coincident, però el mètode de preus és una altra cosa que **el preu per unitat**, la taxa de cost s'estableix en **0** (zero) per defecte.

## <a name="determining-cost-rates-on-actual-and-estimate-lines-for-material"></a>Determinació de taxes de costos en línies reals i d'estimació de Material

El context d'estimació **del material** es refereix a:

- Detalls de la línia de pressupostos per a **Material**.
- Dades de la línia de contracte de **Material**.
- Estimacions de materials sobre un projecte.

El context **real del material** es refereix a:

- Línies de diari d'entrada i correcció de **material**.
- Línies de diari que es creen quan s'envia un registre d'ús de materials.

Després de determinar una llista de preus de cost, el sistema completa els passos següents per introduir la taxa de cost predeterminada.

1. El sistema utilitza la combinació dels **camps Producte** i **Unitat** en el context estimatiu o real de **Material** contra les línies d'articles de la llista de preus de la llista de preus.
1. Si el sistema troba una línia d'articles de llista de preus que té una taxa de cost per a la **combinació Producte** i **Unitat**, aquesta taxa de cost s'utilitza com a taxa de cost predeterminada.
1. Si el sistema no pot coincidir amb els **valors Producte** i **Unitat**, el cost unitari es defineix com a **0** (zero) per defecte.
1. En l'estimació o en el context real, si el sistema pot trobar una línia d'articles de llista de preus coincidents, però el mètode de preus és una altra cosa que **l'import** de la moneda, el cost unitari s'estableix en **0** per defecte. Aquest comportament es produeix perquè Project Operations només admet el mètode de preus de l'import **de la** moneda per als materials que s'utilitzen en un projecte.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
