---
title: Determinar els preus de venda de les estimacions i els reals basats en projectes
description: Aquest article proporciona informació sobre com es determinen els preus de venda de les estimacions i els reals basats en projectes.
author: rumant
ms.date: 09/12/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f0b95c651983230cbf340f2c06089a287b2c8a10
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475357"
---
#  <a name="determine-sales-prices-for-project-based-estimates-and-actuals"></a>Determinar els preus de venda de les estimacions i els reals basats en projectes

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

Per determinar els preus de venda sobre estimacions i reals a Microsoft Dynamics 365 Project Operations, el sistema utilitza primer la data i la moneda en l'estimació entrant o context real per determinar la llista de preus de venda. En el context actual específicament, el sistema utilitza el camp Data **de la** transacció per determinar quina llista de preus és aplicable. El **valor de la data** de transacció de l'estimació entrant o real es compara amb els **valors Inici efectiu (zona horària independent)** i **Final efectiu (zona horària independent)** de la llista de preus. Un cop determinada la llista de preus de venda, el sistema determina la taxa de vendes o factura.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-time"></a>Determinació de les taxes de vendes en línies reals i d'estimació del temps

El context d'estimació **del temps** es refereix a:

- Detalls de la línia de pressupost per a **Time**.
- Dades de la línia de contracte per a **Time**.
- Assignacions de recursos sobre un projecte.

El context real del **temps** es refereix a:

- Línies de diari d'entrada i correcció del **temps**.
- Línies de diari que es creen quan s'envia una entrada de temps.
- Detalls de la línia de factura per a **Time**. 

Després de determinar una llista de preus per a les vendes, el sistema completa els passos següents per introduir la tarifa de factura predeterminada.

1. El sistema coincideix amb la combinació dels **camps Role**, **Resourcing Company** i **Resourcing Unit** en l'estimació o context real de **Time** amb les línies de preus de rol de la llista de preus. Aquesta coincidència suposa que utilitzeu les dimensions de preus estàndard per a les tarifes de les factures. Si heu configurat els preus de manera que es basin en camps que no siguin o a **més de Funció**, **Empresa de recursos i** Unitat **de** recursos, aquesta combinació de camps s'utilitza per recuperar una línia de preus de rol coincident.
1. Si el sistema troba una línia de preus de funció que té una tarifa de factura per a la **combinació Funció**, **Empresa** de recursos i **Unitat** de recursos, aquesta tarifa de factura s'utilitza com a tarifa de factura predeterminada.

> [!NOTE]
> Si configureu una priorització diferent dels camps Rol **,** Empresa **de** recursos i **Unitat** de recursos, o si teniu altres dimensions que tenen més prioritat, el comportament anterior canviarà en conseqüència. El sistema recupera registres de preus de funció que tenen valors que coincideixen amb cada valor de dimensió de preus per ordre de prioritat. Les files que tenen valors nuls per a aquestes dimensions són les últimes.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-expense"></a>Determinació de les taxes de vendes en línies reals i d'estimació de despeses

El context d'estimació **de la despesa** es refereix a:

- Detalls de la línia de pressupostos per a **despeses**.
- Dades de la línia de contractació de **despesa**.
- Línies d'estimació de despeses d'un projecte.

El context real de **la despesa** es refereix a:

- Registre i correcció de línies de registre de **despeses**.
- Línies de diari que es creen quan s'envia una entrada de despeses.
- Dades de la línia de factura per a **la despesa**. 

Després de determinar una llista de preus per a les vendes, el sistema completa els passos següents per introduir el preu de venda unitari predeterminat.

1. El sistema coincideix amb la combinació dels **camps Categoria** i **Unitat** de la línia d'estimació de **Despesa** amb les línies de preus de categoria de la llista de preus.
1. Si el sistema troba una línia de preus de categoria que té una taxa de vendes per a la **combinació categoria** i **unitat**, aquesta taxa de vendes s'utilitza com a taxa de venda predeterminada.
1. Si el sistema troba una línia de preus de categoria coincident, el mètode de preus es pot utilitzar per introduir el preu de venda predeterminat. La taula següent mostra el comportament per defecte dels preus de despesa a Project Operations.

    | Context | Mètode de càlcul de preus | Preu predeterminat |
    | --- | --- | --- |
    | Aproximat | Preu per unitat | Segons la línia de preus de la categoria. |
    |        | A partir del cost | 0.00 |
    |        | Marge comercial sobre el cost | 0.00 |
    | Real | Preu per unitat | Segons la línia de preus de la categoria. |
    |        | A partir del cost | En funció del cost real relacionat. |
    |        | Marge comercial sobre el cost | S'aplica un marcatge, tal com es defineix per la línia de preus de categoria, a la taxa de cost unitari del cost real relacionat. |

1. Si el sistema no pot coincidir amb els **valors categoria** i **unitat**, la taxa de vendes s'estableix en **0** (zero) per defecte.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-material"></a>Determinació de les taxes de vendes en línies reals i d'estimació de Material

El context d'estimació **del material** es refereix a:

- Detalls de la línia de pressupostos per a **Material**.
- Dades de la línia de contracte de **Material**.
- Línies d'estimació de materials d'un projecte.

El context **real del material** es refereix a:

- Línies de diari d'entrada i correcció de **material**.
- Línies de diari que es creen quan s'envia un registre d'ús de materials.
- Dades de la línia de factura de **Material**. 

Després de determinar una llista de preus per a les vendes, el sistema completa els passos següents per introduir el preu de venda unitari predeterminat.

1. El sistema coincideix amb la combinació dels camps Producte **i** Unitat **de la** línia d'estimació de **Material** amb les línies d'articles de la llista de preus de la llista de preus.
1. Si el sistema troba una línia d'articles de llista de preus que té una taxa de venda per a la **combinació Producte** i **Unitat**, i si el mètode de fixació de preus és **Import** de moneda, s'utilitza el preu de venda especificat a la línia de llista de preus. 
1. Si els valors del **camp Producte** i **Unitat** no coincideixen o si el mètode de preus no és una altra cosa que **l'import** de la moneda, la taxa de vendes s'estableix en **0** (zero) de manera predeterminada. Aquest comportament es produeix perquè Project Operations només admet el mètode de preus de l'import **de la** moneda per als materials que s'utilitzen en un projecte.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
