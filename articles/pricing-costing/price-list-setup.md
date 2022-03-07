---
title: Configuració de llistes de preus
description: Aquest tema proporciona informació sobre com configurar llistes de preus de cost i venda.
author: rumant
ms.date: 10/20/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 227e9a6f0ce6fd3fa1c2b0bd9afa014a3ec4f9758ead0dfb408156535692575c
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "7009474"
---
# <a name="set-up-price-lists"></a>Configuració de llistes de preus

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

Les llistes de preus del Dynamics 365 Project Operations representen un catàleg de tarifes. Les tarifes expressen les tarifes de cost, vendes i facturació. Segons si la llista de preus expressa tarifes de cost o tarifes de facturació, el context de la llista de preus és **Vendes** o **Cost**.

Les següents extensions són específiques del Project Operations i s'apliquen a les llistes de preus del Dynamics 365 Sales.

- **Context**: aquest camp té els valors admesos, **Cost** i **Vendes**. El valor **Compra** no és compatible. Definiu el context a **Cost** per crear una llista de preus de cost o definiu el context a **Vendes** per a una llista de preus de venda. Les llistes de preus de cost resolen el preu del tipus de cost en els registres d'estimacions i valors reals. Les llistes de preus de venda resolen el preu en els registres d'estimacions i valors reals dels tipus de vendes no facturats i facturats.
- **Unitat de temps**: aquesta és la unitat de temps per defecte per la qual el preu es configura en la taula relacionada **preu per funció** per a aquesta llista de preus.
- **Entitat de la llista de preus**: aquest camp ocult és perquè el Project Operations diferenciï les llistes de preus que són específiques d'ofertes o contractes de les que són estàndard i aplicables globalment.

## <a name="price-list-header"></a>Capçalera de la llista de preus

La taula següent inclou els camps de la pestanya **General** d'una llista de preus que són únics al Project Operations o que tenen canvis significatius en el comportament de les llistes de preus al Sales.

| Camp | Location | Descripció | Impacte descendent |
| --- | --- | --- | --- |
| Nom | Pestanya **General** i formularis **Creació ràpida** | Identitat de la llista de preus. | La llista de preus es mostra amb aquest valor en totes les pàgines de la llista i opcions desplegables.|
| Context | Pestanya **General** i formularis **Creació ràpida** | Aquest camp es pot establir a **Cost** o **Vendes**. | Una llista de preus establerta a **Cost** s'utilitza per consultar el preu de les estimacions de cost i els valors reals de cost. Una llista de preus establerta a **Vendes** s'utilitza per consultar el preu de les estimacions de vendes i els valors reals de vendes. Només les llistes de preus que tenen el context establert a **Vendes** es poden adjuntar a les llistes de preus de projecte per a clients, ofertes de projecte o contractes de projecte. |
| Data d’inici | Pestanya **General** i formularis **Creació ràpida** | Data d'inici del període en què la llista de preus és efectiva. | Amb el camp **Data de finalització**, aquest camp s'utilitza per determinar quina llista de preus és aplicable per a una determinada línia d'estimació o valors reals. |
| Data d’acabament | Pestanya **General** i formularis **Creació ràpida** | Data de finalització del període en què la llista de preus és efectiva. | Amb el camp **Data d'inici**, aquest camp s'utilitza per determinar quina llista de preus és aplicable per a una determinada línia d'estimació o valors reals. |
| Moneda | Pestanya **General** i formularis **Creació ràpida** | Aquest camp s'utilitza per prendre el valor per defecte de la moneda en cada línia de funció, categoria o element de la llista de preus relacionada amb aquesta llista de preus. | A les llistes de preus de **Vendes**, no es poden crear línies de funcions, categories o elements de la llista de preus en cap altra moneda que no sigui aquesta moneda. En llistes de preus de **Cost**, podeu crear una línia de preu per funció en qualsevol moneda. La moneda definida aquí s'utilitza com a valor per defecte. La configuració de l'usuari que està relacionada amb els preus per funció pot substituir aquest valor per habilitar la configuració de la tarifa de cost del treball en qualsevol moneda. Les tarifes de cost per categoria i els costos de la llista de preus només es poden establir en la moneda definida aquí. |
| Unitat de temps | Pestanya **General** i formularis **Creació ràpida** | Aquest camp s'utilitza per prendre el valor per defecte de la unitat de temps en cada línia de funció relacionada amb aquesta llista de preus. | Aquest valor de camp només s'utilitza en la configuració de preus per funció relacionada. En llistes de preus de **Cost** i **Vendes**, podeu crear una línia de preu per funció en qualsevol unitat de temps. La unitat de temps definida aquí s'utilitza per defecte. La configuració de l'usuari que està relacionada amb els preus per funció pot substituir aquest valor per habilitar la configuració de la tarifa de cost del treball i tarifa de facturació en qualsevol unitat de temps. |
| Descripció | Pestanya **General** i formularis **Creació ràpida** | Aquest camp de text us permet proporcionar una descripció de diverses línies de la llista de preus. | Aquest camp es mostra a les visualitzacions **Associat** sobre la llista de preus en diverses entitats que tenen llistes de preus relacionades. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]