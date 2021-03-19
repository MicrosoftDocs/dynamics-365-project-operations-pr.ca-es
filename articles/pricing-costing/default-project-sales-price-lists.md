---
title: Llistes de preus per defecte
description: Aquest tema proporciona informació sobre les llistes de preus de vendes i cost per defecte al Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 04c97429ab8ac769dd22b4127432d80de8fde937
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275571"
---
# <a name="default-price-lists"></a>Llistes de preus per defecte

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

## <a name="sales-price-lists"></a>Llistes de preus de venda

Cada oferta i contracte de projecte del Dynamics 365 Project Operations conté una llista de preus de venda per defecte. 

### <a name="price-list-default-on-project-quotes"></a>Llista de preus per defecte en ofertes del projecte
El sistema completa el següent procés per determinar quina és la llista de preus per defecte en una oferta de projecte:

1. El sistema consulta les llistes de preus que s'adjunten a les llistes de preus del projecte del compte. 
2. Si hi ha llistes de preus del projecte adjuntes al registre del compte, el sistema consulta les llistes de preus de venda adjuntes als paràmetres del projecte que coincideixen amb la moneda de l'oferta del projecte.
3. A continuació, el sistema comprova la data d'efectivitat de les llistes de preus que coincideixen amb l'interval de dates de l'oferta del projecte. Concretament, la data en què es va crear l'oferta.
4. Si hi ha diverses llistes de preus que són efectives per a la data de l'oferta del projecte, s'utilitzen per defecte totes les llistes de preus a l'oferta del projecte.
5. Si no hi ha llistes de preus en vigor per a la data de l'oferta del projecte, no hi ha cap llista de preus del projecte per defecte a l'oferta del projecte. Hi haurà un missatge d'avís a l'oferta del projecte. El missatge indica que els valors reals i les estimacions del projecte no tindran preus perquè no hi ha llistes de preus del projecte adjuntes.

### <a name="price-list-default-on-project-contracts"></a>Llista de preus per defecte en contractes del projecte 
El sistema completa el següent procés per determinar quina és la llista de preus per defecte en un contracte de projecte:

1. Si el contracte es crea a partir d'una oferta, les llistes de preus del projecte de l'oferta es copien per separat i s'adjunten al contracte del projecte.
2. Si el contracte es crea des de zero, el sistema consulta les llistes de preus que s'adjunten a les llistes de preus del projecte del compte. Si hi ha llistes de preus del projecte adjuntes al registre del compte, el sistema consulta les llistes de preus de venda adjuntes als paràmetres del projecte que coincideixen amb la moneda del contracte del projecte.
4. A continuació, el sistema comprova la data d'efectivitat de les llistes de preus que coincideixen amb l'interval de dates del contracte del projecte. Concretament, la data en què es va crear el contracte.
5. Si hi ha diverses llistes de preus que són efectives per a la data del contracte, s'utilitzen per defecte totes les llistes de preus al contracte.
6. Si no hi ha llistes de preus en vigor per a la data del contracte, no hi ha cap llista de preus per defecte al contracte. Hi haurà un missatge d'avís al contracte del projecte. El missatge indica que els valors reals i les estimacions del projecte no tindran preus perquè no hi ha llistes de preus del projecte adjuntes.

## <a name="cost-price-lists"></a>Llistes de preus de cost

Les llistes de preus de cost no tenen per defecte cap entitat al Project Operations. La determinació de la llista de preus de cost que s'utilitzarà per als costos del projecte sempre es fa al moment. El sistema completa el següent procés per determinar quina és la llista de preus que s'utilitzarà per als costos del projecte:

1. En primer lloc, el sistema consulta les llistes de preus que s'adjunten a la unitat d'organització contractant del projecte.
2. El sistema consulta la data d'efectivitat de les llistes de preus que coincideixen amb la data de la línia d'estimació o valor real d'entrada. En aquesta situació, *línia d'estimació* es refereix als tres contexts d'estimació al Project Operations:

    - Línia d'estimació del projecte
    - Detall de la línia d’oferta
    - Detall de línia de contracte
  
3. Si hi ha diverses llistes de preus que són efectives per a la data de l'estimació o els valors reals d'entrada, se selecciona la llista de preus creada més recentment.
4. Si no hi ha llistes de preus adjuntes a la unitat d'organització contractant del projecte, el sistema consulta les llistes de preus de cost adjuntes als paràmetres del projecte que coincideixen amb la moneda del projecte.
5. A continuació, el sistema consulta la data d'efectivitat de les llistes de preus que coincideixen amb la data de la línia d'estimació o valor real d'entrada. 
6. Si hi ha diverses llistes de preus que són efectives per a la data de l'estimació o els valors reals d'entrada, se selecciona la llista de preus creada més recentment.
7. Si no hi ha llistes de preus de cost adjuntes als paràmetres del projecte que coincideixin amb la moneda i la data d'efectivitat, el sistema estableix per defecte la tarifa de cost a zero (0) en la línia d'estimació o valor real d'entrada.


[!INCLUDE[footer-include](../includes/footer-banner.md)]