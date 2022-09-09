---
title: Llistes de preus per defecte
description: Aquest article proporciona informació sobre les vendes predeterminades i les llistes de preus de cost a Project Operations.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 50dbf74e31b9eb8d63c378e5fd718dc17c9691f4
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410250"
---
# <a name="default-price-lists"></a>Llistes de preus per defecte

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

## <a name="sales-price-lists"></a>Llistes de preus de venda

Cada oferta i contracte de projecte del Dynamics 365 Project Operations conté una llista de preus de venda per defecte. 

### <a name="price-list-default-on-project-quotes"></a>Llista de preus per defecte en ofertes del projecte
El sistema completa el següent procés per determinar quina és la llista de preus per defecte en una oferta de projecte:

1. El sistema consulta les llistes de preus que s'adjunten a les llistes de preus del projecte del compte. 
1. Si no hi ha llistes de preus del projecte adjuntes al registre del compte, el sistema examina les llistes de preus de venda adjuntes als paràmetres del projecte que coincideixen amb la moneda de l'oferta del projecte.
1. A continuació, el sistema comprova la data d'efectivitat de les llistes de preus que coincideixen amb l'interval de dates de l'oferta del projecte. Concretament, la data en què es va crear l'oferta.
1. Si hi ha diverses llistes de preus que són efectives per a la data de l'oferta del projecte, s'utilitzen per defecte totes les llistes de preus a l'oferta del projecte.
1. Si no hi ha llistes de preus en vigor per a la data de l'oferta del projecte, no hi ha cap llista de preus del projecte per defecte a l'oferta del projecte. Hi haurà un missatge d'avís a l'oferta del projecte. El missatge indica que els valors reals i les estimacions del projecte no tindran preus perquè no hi ha llistes de preus del projecte adjuntes.

### <a name="price-list-default-on-project-contracts"></a>Llista de preus per defecte en contractes del projecte 
El sistema completa el següent procés per determinar quina és la llista de preus per defecte en un contracte de projecte:

1. Si el contracte es crea a partir d'una oferta, les llistes de preus del projecte de l'oferta es copien per separat i s'adjunten al contracte del projecte.
1. Si el contracte es crea des de zero, el sistema consulta les llistes de preus que s'adjunten a les llistes de preus del projecte del compte. Si hi ha llistes de preus del projecte adjuntes al registre del compte, el sistema consulta les llistes de preus de venda adjuntes als paràmetres del projecte que coincideixen amb la moneda del contracte del projecte.
1. A continuació, el sistema comprova la data d'efectivitat de les llistes de preus que coincideixen amb l'interval de dates del contracte del projecte. Concretament, la data en què es va crear el contracte.
1. Si hi ha diverses llistes de preus que són efectives per a la data del contracte, s'utilitzen per defecte totes les llistes de preus al contracte.
1. Si no hi ha llistes de preus en vigor per a la data del contracte, no hi ha cap llista de preus per defecte al contracte. Hi haurà un missatge d'avís al contracte del projecte. El missatge indica que els valors reals i les estimacions del projecte no tindran preus perquè no hi ha llistes de preus del projecte adjuntes.

## <a name="cost-price-lists"></a>Llistes de preus de cost

Les llistes de preus de cost no tenen per defecte cap entitat al Project Operations. La determinació de la llista de preus de cost que s'utilitzarà per als costos del projecte sempre es fa per transacció. El sistema completa el següent procés per determinar quina és la llista de preus que s'utilitzarà per als costos del projecte:

1. El sistema analitza les llistes de preus que s'adjunten a la unitat d'organització contractant del projecte.
1. A continuació, el sistema analitza l'efectivitat de la data de les llistes de preus que coincideixen amb la data del context d'estimació entrant o el context real.

    - *El context* d'estimació es refereix a qualsevol dels tres contextos d'estimació en les operacions del projecte:

        - Línia d'estimació del projecte
        - Detall de la línia d’oferta
        - Detall de línia de contracte

    - *El context* real es refereix a qualsevol de les tres fonts reals en operacions de projecte:

       - Línies de diari d'entrada creades manualment, o línies de diari de correcció que es creen en un diari de correcció
       - Línies de diari que es creen durant l'enviament de registres de temps, despeses o ús de materials
       - Detall de la línia de factura

    Quan el Project Operations coincideix amb l'efectivitat de la data de la línia de diari entrant o el detall de la línia de factura en el *context* real, utilitza el camp Data **de transacció**.

    - Si diverses llistes de preus són efectives per a la data del context d'estimació entrant o del context real, se selecciona la llista de preus creada més recentment.
    - Si no s'adjunten llistes de preus a la unitat d'organització contractant del projecte, el sistema analitza les llistes de preus de cost que s'adjunten als paràmetres del projecte que coincideixen amb la moneda del projecte.

## <a name="enable-multi-currency-cost-price-list"></a>Habilita la llista de preus de cost en diverses monedes

Aquesta configuració es pot trobar a **Paràmetres** de configuració \>**·**. **No** es el valor per defecte.

Quan aquesta configuració està habilitada (és a dir, el valor està definit com a **Sí**), el sistema es comporta de la manera següent:

- Permet associar llistes de preus de cost en qualsevol moneda a la unitat organitzativa. Per exemple, una llista de preus de cost de la moneda EUR es pot adjuntar a una unitat organitzativa de la moneda usd. El sistema continuarà validant que les llistes de preus de cost que s'adjunten a una unitat organitzativa no tinguin efectivitat de data superposada.
- Valida que les llistes de preus de cost que s'adjunten als paràmetres del projecte no tenen efectivitat de data superposada, encara que tinguin monedes diferents. Aquest comportament difereix del comportament per defecte (és a dir, del comportament quan el valor s'estableix com a **No**). En el comportament per defecte, només es validen les llistes de preus de cost que tenen la **mateixa** moneda per a l'efectivitat de la data no superposada.
- Per a un context de transacció entrant, determina la llista de preus de cost només en funció de l'efectivitat de la data. Aquest comportament difereix del comportament per defecte, on el sistema selecciona la llista de preus de cost que coincideix tant amb la moneda del projecte com amb l'efectivitat de la data.

A causa d'aquests canvis en el comportament, els clients de Project Operations podran mantenir una llista global de preus de cost que serà rellevant per a tota l'empresa. No hauran de tenir llistes de preus en cada moneda d'operacions. La llista de preus global tindrà efectivitat de la data i permetrà establir tarifes de cost en qualsevol moneda per a una combinació específica de valors de dimensió de preus. La moneda de la llista de preus de cost només s'utilitza per introduir valors predeterminats quan **es creen els preus de funció,** els **preus** de la categoria i **els registres d'elements de la llista** de preus. No s'utilitzarà per determinar la llista de preus.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
