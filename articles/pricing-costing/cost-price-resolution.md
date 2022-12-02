---
title: Determinar els percentatges de cost de les estimacions i els valors reals basats en el projecte
description: En aquest article es proporciona informació sobre com es determinen els percentatges de cost de les estimacions basades en el projecte i els valors reals.
author: rumant
ms.date: 9/12/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 822a7bd8ae87d4fd4044d8b46347bfe1b4ca13ca
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475261"
---
# <a name="determine-cost-rates-for-project-based-estimates-and-actuals"></a>Determinar els percentatges de cost de les estimacions i els valors reals basats en el projecte

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

Per determinar els preus de cost de les estimacions i els valors reals al Microsoft Dynamics 365 Project Operations, el sistema utilitza primer la data i la moneda de l'estimació entrant o del context real per determinar la llista de preus de venda. En el context real específicament, el sistema utilitza el camp **Data de transacció** per determinar quina llista de preus és aplicable. El valor de **Data de transacció** de l'estimació entrant o real es compara amb els valors d'**Inici efectiu (zona horària independent)** i **Final efectiu (independent de la zona horària)** de la llista de preus. Després de determinar la llista de preus de cost, el sistema determina el percentatge de cost.

## <a name="determining-cost-rates-in-estimate-and-actual-contexts-for-time"></a>Determinar els percentatges de cost en contextos de valors reals i estimacions per al temps

El context d'estimació per a **Temps** fa referència a:

- Detalls de la línia d'oferta per a **Temps**.
- Detalls de la línia de contracte per a **Temps**.
- Assignacions de recursos a un projecte.

El context real per a **Temps** fa referència a:

- Línies del llibre diari d'entrada i de correcció per a **Temps**.
- Línies del llibre diari que es creen en enviar una entrada de temps.

Després de determinar una llista de preus de cost, el sistema completa els següents passos per introduir el percentatge de cost per defecte.

1. El sistema compara la combinació dels camps **Funció**, **Empresa de recursos** i **Unitat de recursos** en el context d'estimació o de valor real per al **Temps** amb les línies de preu per funció de la llista de preus. Aquesta comparació suposa que utilitzeu les mètriques de preus estàndard per al cost laboral. Si heu configurat el sistema perquè coincideixi amb camps diferents o addicionals a més de **Funció**, **Empresa de recursos** i **Unitat de recursos**, s'utilitzarà una combinació diferent per recuperar una línia de preu per funció coincident.
1. Si el sistema troba una línia de preu per funció que té un percentatge de cost per a la combinació **Funció**, **Empresa de recursos** i **Unitat de recursos**, aquest serà el percentatge de cost utilitzat per defecte.
1. Si el sistema no pot fer coincidir els valors **Funció**, **Empresa de recursos** i **Unitat de recursos**, abandona la dimensió que té la prioritat més baixa, cerca línies de preus per funció que tenen coincidències amb els altres dos valors de la dimensió, i continua abandonant progressivament dimensions fins que troba una fila de preus per funció coincident. El percentatge de cost d'aquest registre s'utilitzarà com a percentatge de cost per defecte. Si el sistema no troba cap fila de preu per funció que coincideixi, el preu es definirà com a **0** (zero) per defecte.

> [!NOTE]
> Si configureu una priorització diferent dels camps **Funció** i **Unitat de recursos**, o si teniu altres dimensions que tenen una prioritat més alta, aquest comportament canviarà en conseqüència. El sistema recupera registres de preu per funció que tenen valors que coincideixen amb cada valor de dimensió de preus per ordre de prioritat. Les files que tenen valors nuls per a aquestes dimensions són les darreres.

## <a name="determining-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Determinació de percentatges de cost en línies de valors reals i estimacions per a les despeses

El context d'estimació per a **Despesa** fa referència a:

- Detalls de la línia d'oferta per a **Despesa**.
- Detalls de la línia de contracte per a **Despesa**.
- Estimacions de despesa en un projecte.

El context real per a **Despesa** fa referència a:

- Línies del llibre diari d'entrada i de correcció per a **Despesa**.
- Línies del llibre diari que es creen en enviar una entrada de despesa.

Després de determinar una llista de preus de cost, el sistema completa els següents passos per introduir el percentatge de cost per defecte.

1. El sistema fa coincidir la combinació dels camps **Categoria** i **Unitat** del context d'estimació o de valor real per a **Despesa** amb les línies de preu de categoria de la llista de preus.
1. Si el sistema troba una línia de preu per categoria que té un percentatge de cost per a la combinació de camps **Categoria** i **Unitat**, aquest percentatge de cost s'utilitza per defecte.
1. Si el sistema no pot fer coincidir els valors de **Categoria** i **Unitat**, el preu es defineix com a **0** (zero) per defecte.
1. En el context d'estimació, si el sistema no pot trobar una línia de preu de categoria que coincideixi, però el mètode de preus no és **Preu per unitat**, el percentatge de cost s'estableix en **0** (zero) per defecte.

## <a name="determining-cost-rates-on-actual-and-estimate-lines-for-material"></a>Determinació de percentatges de cost de les línies de valor real i de previsió de materials

El context d'estimació per a **Material** fa referència a:

- Detalls de la línia d'oferta per a **Material**.
- Detalls de la línia de contracte per a **Material**.
- Estimacions de materials en un projecte.

El context real per a **Material** fa referència a:

- Línies del llibre diari d'entrada i de correcció per a **Material**.
- Línies del llibre diari que es creen en enviar un registre d'ús de material.

Després de determinar una llista de preus de cost, el sistema completa els següents passos per introduir el percentatge de cost per defecte.

1. El sistema utilitza la combinació dels camps **Producte** i **Unitat** del context d'estimació o de valor real per a **Material** amb les línies d'element de la llista de preus de la llista de preus.
1. Si el sistema troba un element de la llista de preus que té un percentatge de cost per a la combinació de camps **Producte** i **Unitat**, aquest percentatge de cost s'utilitza per defecte.
1. Si el sistema no pot fer coincidir els valors de **Producte** i **Unitat**, el cost unitari s'estableix en **0** (zero) per defecte.
1. En el context d'estimació o valors reals, si el sistema no pot trobar una línia d'element de la llista de preus que coincideixi, però el mètode de preus no és **Quantitat de moneda**, el percentatge de cost s'estableix en **0** (zero) per defecte. Aquest comportament es produeix perquè el Project Operations només admet el mètode de preus **Import monetari** per als materials que s'utilitzen en un projecte.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
