---
title: Determinar els preus de venda per a les estimacions i els valors reals basats en el projecte
description: En aquest article es proporciona informació sobre com es determinen els preus de venda de les estimacions i els valors reals basats en el projecte.
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
#  <a name="determine-sales-prices-for-project-based-estimates-and-actuals"></a>Determinar els preus de venda per a les estimacions i els valors reals basats en el projecte

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

Per determinar els preus de venda de les estimacions i els valors reals al Microsoft Dynamics 365 Project Operations, el sistema utilitza primer la data i la moneda de l'estimació entrant o del context real per determinar la llista de preus de venda. En el context real específicament, el sistema utilitza el camp **Data de transacció** per determinar quina llista de preus és aplicable. El valor de **Data de transacció** de l'estimació entrant o real es compara amb els valors d'**Inici efectiu (zona horària independent)** i **Final efectiu (independent de la zona horària)** de la llista de preus. Després de determinar la llista de preus de vendes, el sistema determina la tarifa de vendes o de facturació.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-time"></a>Determinació de tarifes de vendes en línies de valors reals i estimacions per al temps

El context d'estimació per a **Temps** fa referència a:

- Detalls de la línia d'oferta per a **Temps**.
- Detalls de la línia de contracte per a **Temps**.
- Assignacions de recursos a un projecte.

El context real per a **Temps** fa referència a:

- Línies del llibre diari d'entrada i de correcció per a **Temps**.
- Línies del llibre diari que es creen en enviar una entrada de temps.
- Detalls de la línia de factura per a **Temps**. 

Després de determinar una llista de preus per a les vendes, el sistema completa els següents passos per introduir la tarifa de facturació per defecte.

1. El sistema compara la combinació dels camps **Funció**, **Empresa de recursos** i **Unitat de recursos** en el context d'estimació o de valor real per al **Temps** amb les línies de preu per funció de la llista de preus. Aquesta assignació assumeix que esteu utilitzant dimensions de preus estàndard per a les tarifes de facturació. Si heu configurat els preus de manera que es basi en camps diferents o addicionals a **Funció**, **Empresa de recursos** i **Unitat de recursos**, aquesta és la combinació que s'utilitzarà per recuperar una línia de preu per funció coincident.
1. Si el sistema troba una línia de preu per funció que té una tarifa de facturació per la combinació de **Funció**, **Empresa de recursos** i **Unitat de recursos**, aquest percentatge de facturació s'utilitzarà com a percentatge de facturació per defecte.

> [!NOTE]
> Si configureu una priorització diferent dels camps **Funció**, **Empresa de recursos** i **Unitat de recursos**, o si teniu altres dimensions que tenen una prioritat més alta, el comportament anterior canviarà en conseqüència. El sistema recupera registres de preu per funció que tenen valors que coincideixen amb cada valor de dimensió de preus per ordre de prioritat. Les files que tenen valors nuls per a aquestes dimensions són les darreres.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-expense"></a>Determinació de tarifes de vendes en línies de valors reals i estimacions per a despeses

El context d'estimació per a **Despesa** fa referència a:

- Detalls de la línia d'oferta per a **Despesa**.
- Detalls de la línia de contracte per a **Despesa**.
- Línies d'estimació de despesa en un projecte.

El context real per a **Despesa** fa referència a:

- Línies del llibre diari d'entrada i de correcció per a **Despesa**.
- Línies del llibre diari que es creen en enviar una entrada de despesa.
- Detalls de la línia de factura per a **Despesa**. 

Després de determinar una llista de preus per a les vendes, el sistema completa els següents passos per introduir el preu de venda per unitat per defecte.

1. El sistema fa coincidir la combinació dels camps **Categoria** i **Unitat** a la línia d'estimació de **Despesa** amb les línies de preu de categoria de la llista de preus.
1. Si el sistema troba una línia de preu per categoria que té una tarifa de venda per a la combinació de **Categoria** i **Unitat**, aquesta tarifa de venda s'utilitza per defecte.
1. Si el sistema troba una línia de preu per categoria coincident, el mètode de preus es podria utilitzar per introduir el preu de venda per defecte. La següent taula mostra el comportament per defecte per als preus de les despeses al Project Operations.

    | Context | Mètode de càlcul de preus | Preu per defecte |
    | --- | --- | --- |
    | Aproximat | Preu per unitat | Basat en la línia de preus per categoria. |
    |        | A partir del cost | 0.00 |
    |        | Marge comercial sobre el cost | 0.00 |
    | Real | Preu per unitat | Basat en la línia de preus per categoria. |
    |        | A partir del cost | Basat en el valor real de cost relacionat. |
    |        | Marge comercial sobre el cost | S'aplica un marge comercial tal com defineix la línia de preus de categoria a la tarifa de cost unitari del valor real de cost relacionat. |

1. Si el sistema no pot fer coincidir els valors de **Categoria** i **Unitat**, la tarifa de venda es defineix com a **0** (zero) per defecte.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-material"></a>Determinació de percentatges de vendes de les línies de valor real i de previsió de materials

El context d'estimació per a **Material** fa referència a:

- Detalls de la línia d'oferta per a **Material**.
- Detalls de la línia de contracte per a **Material**.
- Línies d'estimació de materials en un projecte.

El context real per a **Material** fa referència a:

- Línies del llibre diari d'entrada i de correcció per a **Material**.
- Línies del llibre diari que es creen en enviar un registre d'ús de material.
- Detalls de la línia de factura per a **Material**. 

Després de determinar una llista de preus per a les vendes, el sistema completa els següents passos per introduir el preu de venda per unitat per defecte.

1. El sistema fa coincidir la combinació de camps **Producte** i **Unitat** de la línia d'estimació per a **Material** amb les línies d'element de la llista de preus de la llista de preus.
1. Si el sistema troba una línia d'element de la llista de preus que té un percentatge de vendes per a la combinació **Producte** i **Unitat** i el mètode de càlcul de preus és **Quantitat de moneda**, s'utilitza el preu de venda que s'especifica a la línia de la llista de preus. 
1. Si els valors dels camps **Producte** i **Unitat** no coincideixen, o si el mètode de preus és una cosa diferent de **Import monetari**, el percentatge de vendes es defineix com a **0** (zero) per defecte. Aquest comportament es produeix perquè el Project Operations només admet el mètode de preus **Import monetari** per als materials que s'utilitzen en un projecte.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
