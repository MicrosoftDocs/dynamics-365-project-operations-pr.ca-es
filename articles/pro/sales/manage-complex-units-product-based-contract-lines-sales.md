---
title: Administració d'unitats complexes per a línies de contracte basades en productes (bàsic)
description: Aquest tema proporciona informació sobre com admetre la venda de productes basats en subscripcions.
author: rumant
ms.date: 10/28/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 214593c5b3fbfc5194031af3d3bef59d01750099
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8593968"
---
# <a name="manage-complex-units-for-product-based-contract-lines---lite"></a>Administració d'unitats complexes per a línies de contracte basades en productes (bàsic)

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_

El Dynamics 365 Project Operations utilitza factors de quantitat per admetre la venda de productes basats en subscripcions. Per als productes basats en subscripcions, la quantitat del contracte o la línia de contracte del projecte s'expressa com el nombre de mesos d'usuari.

El preu del programari de subscripció s'emmagatzema al catàleg com el preu per usuari i per mes. Durant el procés de vendes, el preu de la línia de contracte sol ser el preu per usuari per mes que ha estat negociat i descomptat per l'agent de vendes. Cada operació té un nombre diferent d'usuaris i un nombre diferent de mesos de subscripció. La quantitat que s'utilitza per calcular la quantitat de la línia de contracte és un producte del nombre d'usuaris i el nombre de mesos de subscripció.

Per admetre aquest tipus de venda, el Project Operations admet el concepte de *factors de quantitat*. Els factors de quantitat depenen dels atributs del producte. Quan configureu propietats específiques per a un producte, podeu marcar un subconjunt d'aquestes propietats, o bé totes les propietats, com a factors de quantitat.

El Project Operations valida que només les propietats numèriques o les propietats dels productes que tenen un tipus de dades numèric es marquen com a factors de quantitat. Quan un producte amb factors de quantitat configurats s'afegeix a una línia de contracte, el camp **Quantitat** es converteix en només de lectura. Després d'introduir els valors per a les propietats dels productes que són factors de quantitat, el Project Operations calcula la quantitat de la línia de contracte.

Per exemple, el Dynamics 365 Sales pot tenir les propietats següents:

- **Nombre d'usuaris**: el nombre d'usuaris.
- **Nombre de mesos**: el nombre de mesos de subscripció.
- **SKU de producte**: la unitat de manteniment d'estoc (SKU) per al producte.

Les propietats **Nombre d'usuaris** i **Nombre de mesos** es poden marcar com a factors de quantitat per editar les propietats de la línia de productes.

Per crear factors de quantitat a partir de propietats de producte, completeu els passos següents.

1. Al **Project Operations**, seleccioneu **Vendes-productes**.
2. Obriu el producte per al qual heu de configurar factors de quantitat. Assegureu-vos que el producte ja tingui propietats configurades.
3. A la pàgina **Informació del projecte**, seleccioneu la pestanya **Factors de quantitat**.
4. A la subquadrícula, seleccioneu **+ Càlcul de camp nou**.
5. Introduïu el nom del **Factor de quantitat** i seleccioneu el valor de propietat que s'assigna al càlcul del camp.
6. Desa i tanca el formulari.
7. Repetiu els passos 2-6 per a totes les propietats que constitueixen la quantitat de la línia de contracte basada en productes.

Amb els factors de quantitat configurats, quan l'usuari crea una línia de contracte per a aquest producte, la quantitat de la línia de contracte està bloquejada. A continuació, la quantitat es calcula com un producte dels valors de propietat d'aquesta línia de contracte.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]