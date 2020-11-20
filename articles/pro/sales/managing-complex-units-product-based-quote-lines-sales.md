---
title: Administració d'unitats complexes, com ara per usuari o per mes, de les línies d'oferta basades en productes (bàsic)
description: En aquest tema s'ofereix informació sobre l'administració d'unitats complexes per a línies d'oferta basades en projectes.
author: rumant
manager: Annbe
ms.date: 10/06/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2ee46da2f663ef4f5f8fc7f9f89b6fcfd09a1798
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/30/2020
ms.locfileid: "4175564"
---
# <a name="managing-complex-units-such-as-per-user-per-month-for-product-based-quote-lines---lite"></a>Administració d'unitats complexes, com ara per usuari o per mes, de les línies d'oferta basades en productes (bàsic)

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_

El Dynamics 365 Project Operations utilitza factors de quantitat per admetre la venda de productes basats en subscripcions. Per als productes basats en subscripcions, la quantitat de l'oferta o la línia de contracte del projecte s'expressa com el nombre de mesos d'usuari.

Normalment, el preu del programari de subscripció s'emmagatzema al catàleg com el preu per usuari i per mes. Durant el procés de vendes, el preu de la línia d'oferta sol ser el preu per usuari per mes que ha estat negociat i descomptat per l'agent de vendes de TI. Cada operació té un nombre diferent d'usuaris i un nombre diferent de mesos de subscripció. La quantitat que s'utilitza per calcular la línia d'oferta és un producte del nombre d'usuaris i el nombre de mesos de subscripció.

Per admetre aquest tipus de venda, el Project Operations ha introduït el concepte de factors de quantitat. Els factors de quantitat depenen dels atributs de producte al Dynamics 365. Quan configureu propietats específiques per a un producte, el Project Operations us permet marcar un subconjunt o totes les propietats, com a factors de quantitat.

El Project Operations valida que només les propietats numèriques o les propietats dels productes que tenen un tipus de dades numèric es marquen com a factors de quantitat. Quan afegiu un producte amb factors de quantitat a una línia d'oferta, el camp **Quantitat** es converteix en només de lectura. Després d'introduir els valors per a les propietats dels productes que són factors de quantitat, el Project Operations calcula la quantitat de la línia d'oferta.

Per exemple, el Dynamics 365 Sales pot tenir les propietats següents:

- **Nombre d'usuaris**: el nombre d'usuaris
- **Nombre de mesos**: el nombre de mesos de subscripció
- **SKU de producte**

Podeu marcar les propietats **Nombre d'usuaris** i **Nombre de mesos** com a factors de quantitat per editar les propietats de la línia de productes.

Per crear factors de quantitat a partir de les propietats dels productes, seguiu aquests passos:

1. A la subfinestra de navegació esquerra del Project Operations, aneu a **Vendes** > **Productes**.
2. Obriu el producte per al qual heu de configurar els factors de quantitat. Assegureu-vos que el producte tingui propietats ja configurades.
3. A la pàgina **Informació del projecte** del producte, seleccioneu la pestanya **Factors de quantitat**.
4. A la subquadrícula, seleccioneu **+ Càlcul de camp nou**.
5. Introduïu el nom del factor de quantitat i seleccioneu el valor de propietat que s'assigna al càlcul del camp.
6. Desa i tanca el formulari. Repetiu aquests passos per a totes les propietats que s'utilitzaran per calcular la quantitat de la línia d'oferta basada en productes.

Quan creeu una línia d'oferta basada en productes per a un producte, la quantitat de la línia d'oferta estarà bloquejada. La quantitat es calcularà com a producte dels valors de propietat que hàgiu introduït per a la línia d'oferta.
