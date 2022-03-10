---
title: Línies d'oferta basades en productes
description: En aquest tema es proporciona informació sobre les línies d'oferta basades en productes.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 3cc2e8788ea699b57ef75903ec3771f2e66fe867a9b8b6328a55b484eb13ede4
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "7008574"
---
# <a name="product-based-quote-lines"></a>Línies d'oferta basades en productes

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


Podeu crear línies d'oferta basades en productes al Dynamics 365 Project Service Automation. Les línies d'oferta basades en productes poden ser línies fora del catàleg o poden ser elements del catàleg de productes.

## <a name="product-catalog"></a>Catàleg de productes

Els productes d'un catàleg de productes del Dynamics 365 tenen una unitat i un grup d'unitats per defecte. Si diversos productes comparteixen el mateix conjunt d'atributs, podeu crear una família de productes que també tingui aquests atributs. Tots els productes d'una família de productes hereten el mateix conjunt d'atributs.

Per exemple, una empresa ven llicències de subscripció per a diversos programes. Tots els programes de subscripció tenen els dos atributs següents:

- Nombre d'usuaris 
- Duració de la subscripció (en mesos)

Una bona manera de mantenir aquest tipus de catàleg és crear una família de productes que s'anomeni **Programari de subscripció** i que tingui **Nombre d'usuaris** i **Duració de la subscripció** com a atributs. A continuació, podeu afegir productes individuals, com ara el **Dynamics 365 Sales** o el **Dynamics 365 Field Service** a la família de productes **Programari de subscripció**.

## <a name="adding-product-catalog-items-to-a-project-quote"></a>Afegir elements del catàleg de productes a una oferta de projecte

Les pàgines dels contractes d'oferta i de contractes de projecte tenen seccions per a dos tipus de línies: línies basades en el projecte i línies basades en productes. Per a les línies basades en productes, el Dynamics 365 s'utilitza per afegir elements d'un catàleg de productes a una oferta. La llista desplegable de la línia d'oferta o de la línia de contracte de projecte inclou tots els productes i les unitats de la llista de preus de productes adjunta al contracte de l'oferta o del projecte. També podeu afegir productes que no siguin part de la llista de preus de productes de l'oferta.

A més, podeu seleccionar productes d'altres llistes de preus o bé podeu seleccionar productes directament des del catàleg de productes. En seleccionar productes directament des d'un catàleg de productes, la llista de preus per defecte d'aquest producte s'utilitza per obtenir el preu de venda del producte. Si no es defineix una llista de preus per defecte, el preu es defineix com a 0 (zero).

Si una línia d'oferta es basa en un catàleg de productes, podeu substituir el preu de venda directament a la línia d'oferta. Heu de tenir en compte que una línia d'oferta del Dynamics 365 té un camp **Preu**. Hi ha dos valors disponibles:

- Substitueix el preu  
- Utilitza el valor per defecte

Si definiu aquest camp com a **Substitueix el preu**, el Dynamics 365 no configura cap preu per defecte. Heu d'introduir un preu per al producte a la línia d'oferta. Si definiu aquest camp com a **Utilitza els valors per defecte**, el Dynamics 365 utilitza el preu de vendes per defecte i bloca el camp per evitar l'edició.

Després d'instal·lar el PSA, els preus de vendes per defecte s'introdueixen a les línies basades en productes en una oferta. El camp **Preu** es defineix com a **Substitueix el preu** per tal que pugueu editar el preu per defecte a les línies d'oferta.

> ![Definir la substitució del preu.](media/basic-guide-10.png)
 
## <a name="quantity-factors-for-products"></a>Factors de quantitat per a productes

El PSA utilitza factors de quantitat per admetre la venda de productes basats en subscripcions. Per als productes basats en subscripcions, la quantitat de l'oferta o la línia de contracte del projecte s'expressa com el nombre de mesos d'usuari.

Normalment, el preu del programari de subscripció s'emmagatzema al catàleg com el preu per usuari i per mes. Tanmateix, podeu utilitzar altres descripcions de temps en el seu lloc. Durant el procés de vendes, el preu de la línia d'oferta sol ser el preu per usuari per mes que ha estat negociat i descomptat per l'agent de vendes de TI. Cada operació té un nombre diferent d'usuaris i un nombre diferent de mesos de subscripció. La quantitat que s'utilitza per calcular la quantitat de la línia d'oferta és un producte del nombre d'usuaris i el nombre de mesos de subscripció.

Per admetre aquest tipus de venda, el PSA ha introduït el concepte de factors de quantitat. Els factors de quantitat depenen dels atributs de producte al Dynamics 365. Quan configureu propietats específiques per a un producte, el PSA us permet marcar un subconjunt d'aquestes propietats, o bé totes les propietats, com a factors de quantitat.

El PSA valida que només les propietats numèriques o les propietats dels productes que tenen un tipus de dades numèric es marquen com a factors de quantitat. Quan un producte amb factors de quantitat configurats s'afegeix a una línia d'oferta, el camp **Quantitat** de la línia d'oferta es converteix en un camp de només de lectura. Després d'introduir els valors per a les propietats dels productes que són factors de quantitat, el PSA calcula la quantitat de la línia d'oferta.

Per exemple, el Dynamics 365 pot tenir les propietats següents: 

- **Nombre d'usuaris**: el nombre d'usuaris 
- **Nombre de mesos**: el nombre de mesos de subscripció
- **SKU de producte** 

Les propietats **Nombre d'usuaris** i **Nombre de mesos** es poden marcar com a factors de quantitat per editar les propietats de la línia de productes. 

> ![Marcar Nombre d'usuaris i Nombre de mesos com a factors de qualitat.](media/basic-guide-11.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]