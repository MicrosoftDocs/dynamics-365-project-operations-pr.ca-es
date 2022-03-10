---
title: Configuració de camps personalitzats com a dimensions de preus
description: En aquest tema, podreu obtenir informació sobre la configuració de dimensions de preus personalitzades.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 11/20/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 9503b6528f91f86cc1ebe1c7ed6111171e74c4a3cbf83b3f68810c3ee5efdd28
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "7002319"
---
# <a name="setting-up-custom-fields-as-pricing-dimensions"></a>Configuració de camps personalitzats com a dimensions de preus 

[!include [banner](../includes/psa-now-project-operations.md)]

Abans de començar, aquest tema assumeix que heu completat els procediments dels temes [Crear camps i entitats personalitzats](create-custom-fields-entities.md) i [Afegir camps personalitzats a la configuració de preus i les entitats transaccionals](field-references.md). Si no heu completat aquests procediments, aneu enrere per completar-los torneu a aquest tema. 

En aquest tema, podreu obtenir informació sobre la configuració de dimensions de preus personalitzades. A la interfície web del Project Service, a la pàgina **Paràmetres**, la pestanya **Dimensions de preus basades en el preu** mostra els registres de l'entitat de dimensions de preus. Per defecte, la instal·lació del Project Service crea 2 files a la quadrícula en aquesta pestanya:

- **msdyn_resourcecategory** (Funció)
- **msdyn_OrganizationalUnit** (Unitat organitzativa)

> [!IMPORTANT]
> No suprimiu aquestes files. No obstant, si no les necessiteu, podeu fer que no s'apliquin en un context específic establint **Aplicable al cost**, **Aplicable a les vendes** i **Aplicable a les compres** com a **No**. La configuració d'aquests valors d'atribut com a **No** té el mateix efecte de no tenir el camp com a dimensió de preus.

Per tal que un camp es converteixi en una dimensió de preus, ha de ser:

- Creat com a camp a les entitats **Preu per funció** i **Marge comercial del preu per funció**. Per obtenir més informació sobre com fer-ho, vegeu [Afegir camps personalitzats a la configuració de preus i a entitats transaccionals](field-references.md).
- Creat com una fila a la taula **Dimensió de preus**. Per exemple, afegiu files de dimensió de preus com es mostra a la gràfica següent. 

![Files de dimensions de preus basades en els imports.](media/Amt-based-PD.png)

Observeu que Hores de treball del recurs (**msdyn_resourceworkhours**) s'ha afegit com una dimensió basada en el marge comercial i s'ha afegit a la quadrícula a la pestanya **Dimensió de preus basada en el marge comercial**.

![Files de dimensions de preus basades en el marge comercial.](media/Markup-based-PD.png)

> [!IMPORTANT]
> Qualsevol canvi de les dades de dimensió de preus d'aquesta taula, existents o noves, es propaga a la lògica empresarial de preus del Project Service només després de l'actualització de la memòria cau. El temps d'actualització de la memòria cau pot tardar fins a 10 minuts. Permeteu aquesta duració de temps per veure els canvis en la lògica de preus per defecte que han de derivar dels canvis en les dades de la dimensió de preus.


## <a name="attributes-of-the-pricing-dimensions-table"></a>Atributs de la taula Dimensions de preus
A les seccions següents es proporciona informació sobre els diferents atributs a la taula **Dimensions de preus**.

### <a name="pricing-dimension-name"></a>Nom de la dimensió de preus
Aquest valor hauria de ser el mateix que el nom de l'esquema del camp que s'afegeix a la taula **Preu per funció** per a les dimensions de preus personalitzades. Per obtenir més informació sobre l'addició de camps a la taula **Preu per funció**, vegeu [Afegir camps personalitzats a la configuració de preus i a les entitats transaccionals](field-references.md).

### <a name="type-of-dimension"></a>Tipus de dimensió
Hi ha dos tipus de dimensions de preus:
  
  - **Dimensions basades en l'import**: els valors de les dimensions del context d'entrada es corresponen als valors de dimensió en la línia **Preu per funció** i el preu i el cost s'obtindran directament per defecte dels valors de la taula **Preu per funció**.
  - **Dimensions basades en el marge comercial**: són les dimensions en què el Project Service adoptarà el procés de 3 passos següent per obtenir el preu i el cost
 
    1. El Project Service fa coincidir els valors de dimensió basats en el marge comercial des del context d'entrada a la línia Preu per funció per obtenir la tarifa base.
    2. El Project Service fa coincidir tots els valors de dimensió basats en el marge comercial des del context d'entrada a la línia **Marge comercial del preu per funció** per obtenir el percentatge de marge comercial.
    3. El Project Service aplica el percentatge de marge comercial del segon pas a la tarifa base **obtinguda a** partir de la taula Preu per funció en el primer pas per arribar al preu/cost definitiu.
   
   La taula següent il·lustra el càlcul dels marges comercials de preus.
  
| Funció        | Unitat organitzativa    |Ubicació del treball      |Càrrec estàndard      |Hores de treball del recurs      |  Marge comercial|
| ------------|-------------|-------------------|--------------------|-------------------------|--------:|
|             | Contoso India|In situ            |                    |Hores extra                 |15     |
|             | Contoso India|Local             |                    |Hores extra                 |10     |
|             | Contoso US   |Local             |                    |Hores extra                 |20     |


Si un recurs de Contoso India la tarifa base del qual és 100 USD treballa in situ, i registra 8 hores de temps normal i 2 hores de temps extra a l'entrada de temps, el motor de preus del Project Service utilitzarà la tarifa base de 100 per a les 8 hores per registrar 800 USD. Per a les 2 hores extres, s'aplicarà un marge comercial del 15% a la tarifa base de 100 per obtenir un preu d'unitat de 115 USD i registrarà un cost total de 230 USD.

### <a name="applicable-to-cost"></a>Aplicable al cost 
Si està definit com a **Sí**, indica que el valor de la dimensió del context d'entrada s'ha d'utilitzar per coincidir amb **Preu per funció** i **Marge comercial del preu per funció** quan es recuperen les tarifes de costos i marge comercial.

### <a name="applicable-to-sales"></a>Aplicable a les vendes
Si està definit com a **Sí**, indica que el valor de la dimensió del context d'entrada s'ha d'utilitzar per coincidir amb **Preu per funció** i **Marge comercial del preu per funció** quan es recuperen les tarifes de facturació i marge comercial.

### <a name="applicable-to-purchase"></a>Aplicable a les compres
Si està definit com a **Sí**, indica que el valor de la dimensió del context d'entrada s'ha d'utilitzar per coincidir amb **Preu per funció** i **Marge comercial del preu per funció** quan es recupera el preu de compra. El Project Service actualment no és compatible amb escenaris de subcontractació, de manera que aquest camp no s'utilitza. 

### <a name="priority"></a>Prioritat
Definir la prioritat de dimensions ajuda que el Project Service produeixi un preu encara que no trobi una coincidència exacta entre els valors de la dimensió d'entrada i els valors de les taules **Preu per funció** o **Marge comercial del preu per funció**. En aquest escenari, el Project Service utilitzarà valors nuls per als valors d'una dimensió no coincidents pesant les dimensions segons la seva prioritat.

- **Prioritat de costos**: el valor d'una prioritat de costos d'una dimensió indicarà el pes d'aquesta dimensió el fer-la coincidir amb la configuració dels preus de cost. El valor de **Prioritat de cost** ha de ser únic en totes les dimensions **Aplicable al cost**.
- **Prioritat de vendes**: el valor d'una prioritat de vendes d'una dimensió indicarà el pes d'aquesta dimensió el fer-la coincidir amb la configuració dels preus de vendes o tarifes de facturació. El valor de **Prioritat de vendes** ha de ser únic en totes les dimensions **Aplicable a les vendes**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]