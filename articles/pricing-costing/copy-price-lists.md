---
title: Còpia de les llistes de preus
description: Aquest tema proporciona informació sobre com copiar les llistes de preus al Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: e49a95a04e9506e983d920c49d4c504d9f944c88
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275706"
---
# <a name="copy-price-lists"></a>Còpia de les llistes de preus

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

Podeu crear còpies de llistes de preus al Dynamics 365 Project Operations. Per exemple, podeu crear llistes de preus per a l'any vinent utilitzant una llista de preus de l'any actual.  O bé podríeu copiar una llista de preus per a les tarifes de facturació i els preus de venda de les llistes de preus per al cost. 

Per fer una còpia de la llista de preus, completeu els següents passos.

1. Obriu la llista de preus de la qual voleu fer una còpia i seleccioneu **Copia**.
2. Introduïu la informació necessària per copiar la llista de preus. La taula següent mostra les consideracions que cal tenir en compte quan s'introdueix informació.

| Camp | Descripció | Impacte descendent |
| --- | --- | --- |
| Nom | Nom de la llista de preus d'origen amb el sufix **-còpia**. | La llista de preus inclou aquest valor en totes les pàgines de la llista i opcions desplegables. |
| Context | Introduïu el context que voleu per a la llista de preus de destinació. | Una llista de preus que té el context establert a **Cost** s'utilitza per consultar el preu de les estimacions de cost i els valors reals de cost. Una llista de preus que té el context establert a **Vendes** s'utilitza per consultar el preu de les estimacions de vendes i els valors reals de vendes. Només les llistes de preus que tenen el context establert a **Vendes** es poden adjuntar a una llista de preus de projecte per a un client, ofertes o contracte. |
| Data d’inici | Data d'inici del període en què la llista de preus és efectiva. | Juntament amb **Data de finalització**, aquest camp s'utilitza per determinar quina llista de preus és aplicable per a una determinada línia d'estimació o valors reals. |
| Data d’acabament | Data de finalització del període en què la llista de preus és efectiva. | Juntament amb **Data d'inici**, aquest camp s'utilitza per determinar quina llista de preus és aplicable per a una determinada línia d'estimació o valors reals. |
| Moneda | Moneda de la llista de preus d'origen. Això es pot canviar. | Quan això es canvia, totes les línies de preus resultants per al treball, la despesa i els articles del catàleg de productes es converteixen a la moneda de la llista de preus de destinació durant la còpia. |
| Unitat de temps | Moneda de la llista de preus d'origen. Això es pot canviar. | Quan això es canvia, totes les línies de preu resultants per als elements de treball es converteixen a la unitat de llista de preus de destinació durant la còpia. S'utilitza la conversió de la configuració de la unitat per a la unitat de temps de la llista de preus d'origen i la unitat de temps de la llista de preus de destinació. |
| Descripció | Descripció de la llista de preus d'origen amb el sufix **-còpia**. És un camp de text i us permet afegir una descripció de diverses línies de la llista de preus. | Aquest camp es mostra a les visualitzacions **Associat** sobre la llista de preus en diverses entitats que tenen llistes de preus relacionades. |

3. Deseu la llista de preus. 

## <a name="update-a-price-list-by-applying-a-mark-up-to-all-the-prices"></a>Actualitzar una llista de preus aplicant un marge comercial a tots els preus

1. A les pestanyes **Funció**, **Categoria** i **Element de la llista de preus** d'una llista de preus, podeu seleccionar **Actualitza els preus** per aplicar un marge comercial per a tots els preus de la subquadrícula. 
2. A la pàgina de diàleg que s'obre, introduïu un marge comercial. També podeu introduir un percentatge de marge comercial negatiu per reduir els preus en un determinat percentatge. 
3. Seleccioneu **D'acord** a la pàgina de diàleg i després verifiqueu que els preus de la subquadrícula reflecteixin els canvis que heu fet.


[!INCLUDE[footer-include](../includes/footer-banner.md)]