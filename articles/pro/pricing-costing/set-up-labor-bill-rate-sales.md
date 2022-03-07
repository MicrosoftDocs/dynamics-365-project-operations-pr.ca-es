---
title: Configuració de les tarifes de la factura de treball (bàsic)
description: Aquest tema proporciona informació sobre la configuració de tarifes de facturació de treball al Project Operations.
author: rumant
ms.date: 10/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9b8c4a19260156480e40f2cc26afa83df3ec9fe9de53edc0ad0ca8c7b78bf352
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007584"
---
# <a name="set-up-labor-bill-rates---lite"></a>Configuració de les tarifes de la factura de treball (bàsic)

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_

Cada llista de preus té un conjunt de preus per funció o tarifes de treball que són efectives per al context i la data d'efectivitat inclosos a la capçalera de la llista de preus. Les tarifes de facturació per al temps al Dynamics 365 Project Operations es poden configurar només en una moneda, que és la moneda de la capçalera de la llista de preus.

1. Per establir les tarifes de facturació del treball per a una llista de preus de venda, creeu una llista de preus basada en la capçalera de la llista de preus. 
2. A la pestanya **Preus per funció**, a la subquadrícula, seleccioneu **+ Preu per funció nou**. 
3. A la subfinestra **Creació ràpida**, introduïu la funció rol i la combinació d'unitats de l'organització per a la qual heu d'establir la tarifa de facturació.

  La taula següent inclou els camps de la pestanya **General** i la subfinestra **Creació ràpida** d'una línia de preu per funció que heu de tenir en compte quan creeu els preus per funció en una llista de preus de vendes:

  | Camp | Location | Descripció | Impacte descendent |
  | --- | --- | --- | --- |
  | Funció | Pestanya **General** i subfinestra **Creació ràpida** | Seleccioneu la funció per a la qual definiu la tarifa de facturació. | La funció de l'estimació o el valor real d'entrada es farà coincidir amb aquesta línia per obtenir la tarifa de facturació per defecte de la funció. |
  | Unitat de recursos | Pestanya **General** i subfinestra **Creació ràpida** | Seleccioneu la unitat organitzativa o la divisió de l'empresa de la qual és la funció. Per exemple, un desenvolupador de la divisió de robòtica de Fabrikam India o un desenvolupador de la divisió de programari de Fabrikam USA. | La unitat de recursos de l'estimació o el valor real d'entrada es farà coincidir amb aquesta línia per obtenir la tarifa de facturació per defecte de la funció. |
  | Preu | Pestanya **General** i subfinestra **Creació ràpida** | Establiu la tarifa de facturació per a la combinació de funció, empresa de recursos i unitat de recursos. Per exemple, un desenvolupador de Fabrikam India té una tarifa de facturació de 100 USD o un desenvolupador de Fabrikam USA té una tarifa de facturació de 150 USD. | Aquest preu és la tarifa de facturació per defecte en el preu per unitat de la línia d'estimació o valor real d'entrada per a la classe de transacció de temps. |
  | Moneda | Pestanya **General** i subfinestra **Creació ràpida**| Per defecte, el valor de la moneda prové de la capçalera de la llista de preus de vendes. En una llista de preus de venda, la moneda no es pot substituir. | Aquesta moneda és la moneda de facturació per defecte en el preu per unitat de la línia de venda de valor real d'entrada per a la classe de transacció de temps. |
  | Planificació d'unitat | Pestanya **General** i subfinestra **Creació ràpida** | Aquesta planificació de la unitat per defecte és el temps i no es pot canviar a l'entitat Preu per funció perquè s'utilitza per expressar les tarifes per unitats de temps. | No hi ha cap impacte descendent d'aquest camp. |
  | Unit | Pestanya **General** i subfinestra **Creació ràpida** | El valor de la unitat prové del camp **Unitat de temps** de la capçalera de la llista de preus de vendes. Tanmateix, el valor es pot substituir. Per exemple, un desenvolupador de Fabrikam India té una tarifa de facturació 1000 USD per **Dia de l'Índia**. Un desenvolupador de Fabrikam USA té una tarifa de facturació de 1500 USD per **Dia dels EUA**. | Quan el preu per unitat per defecte és una línia d'estimació o valor real d'entrada, el sistema utilitza el sistema d'unitats i la conversió en unitats base per calcular un preu per unitat. Per exemple, una estimació és de 10 **Dies de l'Índia** de treball per a un desenvolupador de l'Índia, i la unitat, Dia de l'Índia es defineix com a 10 hores. Quan es calcula el preu de la línia d'estimació, l'aplicació calcula el preu per unitat en l'estimació com a 1.000 USD/10 hores = 100 USD per hora. |


## <a name="transfer-pricing-or-set-up-bill-rates-for-resources-from-other-organizational-units-or-divisions"></a>Transferència de preus o configuració de tarifes de facturació de recursos d'altres unitats o divisions de l'organització 

En empreses basades en projectes, s'utilitzen empleats de diferents divisions de l'empresa per treballar en projectes. Els projectes es poden executar des d'una divisió, mentre que els empleats o assessors provenen de la mateixa divisió de l'empresa o una de diferent. El projecte també podria estar format per una combinació de persones de diferents divisions. Al Project Operations, l'empresa que és propietària del lliurament del projecte s'anomena **Unitat de contractació**. La resta de divisions que proporcionen recursos s'anomenen **Unitats de recursos**. A causa de les diferències en els costos laborals entre les diverses zones geogràfiques i els mercats laborals de tot el món, les taxes de facturació del treball també s'estableixen de manera diferent per a les diferents zones geogràfiques.

Per exemple, un desenvolupador de Fabrikam India que treballa en un projecte dels EUA es factura a una tarifa de 100 USD per hora. Un desenvolupador de Fabrikam US que treballa en un projecte dels EUA es factura a 150 USD per hora.

### <a name="example-set-up-a-bill-rate"></a>Exemple: configurar una tarifa de facturació

1. Creeu una llista de preus de vendes anomenada *Tarifes de facturació de Fabrikam US* i definiu la data d'efectivitat.
2. A la llista de preus de venda, introduïu la següent informació de tarifes:

    | Funció | Unitat organitzativa | Tarifa de facturació |
    | --- | --- | --- |
    | Desenvolupador | Fabrikam India | 100 |
    | Desenvolupador | Fabrikam Philippines | 90 USD |
    | Desenvolupador | Fabrikam US | 150 USD |

3. Adjunteu la llista de preus de venda, **Tarifes de facturació de Fabrikam US** a la llista de preus del projecte del contracte o a un compte determinat.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]