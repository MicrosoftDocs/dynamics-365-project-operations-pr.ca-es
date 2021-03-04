---
title: Configurar les tarifes de cost laboral
description: Aquest tema proporciona informació sobre com configurar les tarifes per al cost laboral al Project Operations
author: rumant
manager: Annbe
ms.date: 10/12/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 697129b65f53359615ea537fe135d657748dd909
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/31/2020
ms.locfileid: "4180585"
---
# <a name="set-up-labor-cost-rates"></a>Configurar les tarifes de cost laboral

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_


Cada llista de preus té un conjunt de tarifes laborals (preus per funció) que s'alineen amb el contingut i la data d'efectivitat de la llista de preus.

1. Creeu una llista de preus i a la pestanya **Preu per funció**, a la subquadrícula, selecciona **Funció nova**.
2. A la pàgina **Creació ràpida**, seleccioneu la funció i la unitat d'organització.
3. Introduïu qualsevol altra informació de camp obligatòria.

La taula següent inclou alguns dels camps que són importants quan es creen tarifes laborals en una llista de preus de cost.

| Camp | Location | Descripció | Impacte descendent |
| --- | --- | --- | --- |
| Funció | Pestanya **General** i pàgines **Creació ràpida** | Seleccioneu la funció a la qual s'aplica la tarifa de cost. | La funció de l'estimació o el valor real d'entrada es farà coincidir amb aquesta línia per obtenir el cost per defecte de la funció. |
| Empresa de dotació de recursos | Pestanya **General** i pàgines **Creació ràpida** | Seleccioneu l'entitat jurídica a la qual s'assigna la funció. Per exemple, un desenvolupador de Fabrikam India o un desenvolupador de Fabrikam USA. | L'empresa de recursos de l'estimació o el valor real d'entrada es farà coincidir amb aquesta línia per obtenir la tarifa de cost per defecte de la funció. |
| Unitat de recursos | Pestanya **General** i pàgines **Creació ràpida** | Seleccioneu la unitat organitzativa o la divisió de l'empresa des d'on s'utilitzarà aquesta funció. Per exemple, un desenvolupador de la divisió de robòtica de Fabrikam India o un desenvolupador de la divisió de programari de Fabrikam USA. | L'unitat de recursos de l'estimació o el valor real d'entrada es farà coincidir amb aquesta línia per obtenir el cost per defecte de la funció. |
| Preu | Pestanya **General** i pàgines **Creació ràpida** | Establiu la tarifa de cost per a la combinació de funció, empresa de recursos i unitat de recursos. Per exemple, un desenvolupador de Fabrikam India costa 1000 INR o un desenvolupador de Fabrikam USA costa 150 USD. | El preu és la tarifa de cost per defecte del cost per unitat de la línia d'estimació o valor real d'entrada per a la classe de transacció **Temps**. |
| Moneda | Pestanya **General** i pàgines **Creació ràpida** | Per defecte, el valor de la moneda prové de la capçalera de la llista de preus de cost però es pot substituir. Per exemple, un desenvolupador de Fabrikam India costa 1000 INR. Un desenvolupador de Fabrikam USA costa 150 USD. | Aquesta moneda és per defecte el cost per unitat de la línia de cost de valor real d'entrada per a la classe de transacció **Temps**. En una estimació del projecte, el valor de moneda es converteix en la moneda del projecte i es mostra a la visualització per temps de l'estimació. |
| Planificació d'unitat | Pestanya **General** i pàgines **Creació ràpida** | La planificació de la unitat per defecte és el temps i no es pot canviar a l'entitat Preu per funció perquè s'utilitza per expressar les tarifes per unitats de temps. | No hi ha cap impacte descendent. |
| Unit | Pestanya **General** i pàgines **Creació ràpida** | Per defecte, el valor de la moneda prové del camp **Unitat de temps** de la capçalera de la llista de preus de cost. El valor es pot substituir. Per exemple, un desenvolupador de Fabrikam India costa 1000 INR per **Dia de l'Índia**. Un desenvolupador de Fabrikam USA costa 150 dòlars per **Dia dels EUA**. | El sistema utilitza el sistema d'unitats i conversió en unitats base per calcular un cost per unitat per calcular el preu per unitat per defecte en una línia d'estimació o valor real d'entrada. Per exemple, una estimació és de 10 **Dies de l'Índia** de treball per a un desenvolupador de l'Índia, i la unitat, **Dia de l'Índia** es defineix com a 10 hores. Quan es calcula la línia d'estimació, l'aplicació calcula el cost unitari de l'estimació com a: 1000 INR/10 hores = 100 INR per hora que es converteix en USD i es mostra com a cost unitari a la pàgina **Estimacions del projecte**. |

## <a name="transfer-pricing-and-costs-for-resources-outside-of-your-division-or-legal-entity"></a>Transferència de preus i costos per als recursos fora de la vostra divisió o entitat jurídica

En empreses basades en projectes, és habitual utilitzar empleats de diferents entitats jurídiques o divisions en projectes. Un projecte pot ser executat per una entitat jurídica, però els empleats o consultors que treballen en el projecte poden provenir de la mateixa entitat jurídica o d'una altra, o pot haver-hi una combinació de tots dos. Al Dynamics 365 Project Operations, l'entitat jurídica que és propietària del lliurament del projecte és l'**Empresa propietària** i la divisió que és propietària del lliurament és la **Unitat de contractació**. Altres entitats jurídiques que proporcionen recursos són **Empreses de recursos** i les divisions que proporcionen recursos són **Unitats de recursos**. En la majoria dels països, les empreses estan obligades a garantir que l'entitat jurídica o la divisió de recursos cobra a l'empresa propietària i a la unitat contractant per l'ús dels recursos.

Per exemple, la corporació Fabrikam ha de garantir que Fabrikam India-robòtica tingui una targeta de tarifa de cost negociada amb Fabrikam US-robòtica o Fabrikam UK-robòtica.

Un desenvolupador de Fabrikam India-robòtica cobra 100 USD quan es presta a Fabrikam US-robòtica i 150 USD quan es presta a Fabrikam UK-robòtica.

### <a name="set-up-costs-for-outside-resources"></a>Configurar els costos dels recursos externs

1. Creeu una llista de preus de cost anomenada *Tarifes de cost de Fabrikam US-robòtica* i establiu un interval de dates efectives.
2. A la llista de preus de cost, configureu les tarifes utilitzant la informació de la taula següent. 

| Funció | Empresa de dotació de recursos | Unitat de recursos | Taxa de cost |
| --- | --- | --- | --- |
| Desenvolupador | Fabrikam India | Fabrikam India-robòtica | 100 |
| Desenvolupador | Fabrikam Philippines | Fabrikam Philippines-robòtica | 90 USD |
| Desenvolupador | Fabrikam US | Fabrikam US-robòtica | 150 USD |

3. Adjunteu aquesta llista de preus de cost a la unitat d'organització Fabrikam US-robòtica.

### <a name="set-up-transfer-pricing-for-a-resource-in-the-appropriate-currency"></a>Configurar el preu de transferència d'un recurs en la moneda apropiada 

Al Project Operations, el preu dels recursos es pot establir en qualsevol moneda. La moneda per defecte és la que hi ha a la capçalera de la llista de preus, però es pot canviar.

Utilitzant l'exemple del preu de transferència establert, la informació podria canviar a:

La corporació Fabrikam ha de garantir que Fabrikam India-robòtica tingui una tarifa de cost negociada amb Fabrikam US-robòtica o Fabrikam UK-robòtica.

Un desenvolupador de Fabrikam India-robòtica costa 5000 INR quan es presta a Fabrikam US-robòtica i 5500 INR quan es presta a Fabrikam UK-robòtica.

En la llista de preus de cost per a Fabrikam US-robòtica, les tarifes de cost es poden expressar com:

| Funció | Empresa de dotació de recursos | Cost |
| --- | --- | --- |
| Desenvolupador | Fabrikam India | 5000 INR |
| Desenvolupador | Fabrikam US | 115 USD |

En la llista de preus de cost per a Fabrikam UK-robòtica, les tarifes de cost es poden expressar de la manera següent:

| Funció | Empresa de dotació de recursos | Cost |
| --- | --- | --- |
| Desenvolupador | Fabrikam India | 5500 INR |
| Desenvolupador | Fabrikam UK | 115 GBP |

La llista de preus de cost pot proporcionar les tarifes de treball en diverses monedes. Quan es generi una estimació de cost en el projecte, el Project Operations convertirà aquestes tarifes de cost en la moneda de projecte i les mostrarà a l'usuari. Quan s'aprova una entrada de temps i es crea un valor real de cost, el valor real de cost té el preu en la moneda d'aquesta línia de preu per funció coincident a la llista de preus de cost. Els valors reals de cost per temps en un sol projecte es poden registrar en diverses monedes. No obstant això, en consolidar o resumir els costos reals del treball a nivell de projecte, el Project Operations convertirà tots els imports de cost laboral en la moneda del projecte, que l'usuari pot veure.


[!INCLUDE[footer-include](../includes/footer-banner.md)]