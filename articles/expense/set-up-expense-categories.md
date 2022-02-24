---
title: Configuració de les categories de despesa
description: En aquest tema es proporciona informació sobre la configuració de les categories de despesa i categories compartides per als informes de despeses.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 13e72e4b852fd0edac5ad35d5162e74b016bce33
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123771"
---
# <a name="set-up-expense-categories"></a>Configuració de les categories de despesa

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

Quan els empleats creen informes de despeses, cada despesa que registren s'ha d'associar amb una categoria de despesa. Les categories de despeses es deriven de les categories compartides que es poden compartir amb els organismes jurídics de l'organització. Segons la definició de l'organització, aquestes categories de despesa també es poden compartir en altres àrees. Segons la definició de l'organització i de l'orientació de l'equip d'implementació, cal que determineu si les categories que s'utilitzen a l'administració de despeses només s'utilitzaran a l'administració de despeses o s'han de compartir en altres àrees.

> [!NOTE]
> Aquestes categories es poden compartir entre l'administració de projectes i la comptabilitat i l'administració de despeses, o entre l'administració de projectes i la comptabilitat i la producció. No obstant, no es poden compartir entre l'administració de despeses i la producció.

Per poder començar el procés de configuració, cal que prendre les següents decisions per a cada categoria de despesa:

- Quina és la categoria de despesa? Alguns exemples són categories per a vols, hotels o quilometratge.
- La categoria de despesa també pot utilitzar-se en l'administració de projectes i la comptabilitat? Si és així, també heu de prendre les següents decisions:

    - Quins comptes de cost s'utilitzaran per a les despeses següents?

        - Cost
        - Assignació de nòmines
        - En curs: valor de cost
        - Cost: article
        - En curs: valor de cost: article
        - Pèrdua acumulada
        - En curs: pèrdua acumulada

    - Quins comptes d'ingressos s'utilitzaran per a les següents fonts d'ingressos?

        - Ingressos facturats
        - Ingressos acumulats: valor de vendes
        - En curs: valor de vendes
        - Ingressos acumulats: producció
        - En curs: producció
        - Ingressos acumulats: beneficis
        - En curs: beneficis
        - Ingressos acumulats: subscripció
        - En curs: subscripció

- Quin és el tipus de despesa?
- Què és el mètode de pagament per defecte per a la categoria de despesa?
- Les despeses de la categoria de despesa s'hauran de desglossar?
- Què és el compte per defecte principal per a la categoria de despesa?
- Què és el grup d'impostos de vendes de l'element per a la categoria de despeses?
- Es permeten mètodes de pagament addicionals per a la categoria de despeses? Si és així, quins són?
- Hi ha subcategories en aquesta categoria de despeses? Si hi ha subcategories, també heu de prendre les següents decisions:

    - S'exclou cap subcategoria de la recuperació d'impostos?
    - Quin és el grup d'impostos de vendes de l'element de les subcategories?
