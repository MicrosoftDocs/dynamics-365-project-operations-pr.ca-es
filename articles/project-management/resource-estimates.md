---
title: Estimacions financeres per a temps de recursos en projectes
description: Aquest tema proporciona informació sobre com es calculen les estimacions financeres per a temps.
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: e4be4c8087005ae66a54d40ac88017df591c56eca64f04b00cf34b0e5a8a09ce
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6998674"
---
# <a name="financial-estimates-for-resource-time-on-projects"></a>Estimacions financeres per a temps de recursos en projectes

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

Les estimacions financeres per a temps es calculen a partir de tres factors: 

- El tipus de membre genèric o d'equip assignat a cada tasca de node fulla en el pla del projecte. 
- El tipus o la complexitat del treball.
- La difusió de l'esforç per a l'assignació del recurs a la tasca. 

Els dos primers factors influeixen en el cost unitari o la taxa de facturació de l'assignació d'un recurs. El cost unitari o la taxa de facturació d'una assignació de recursos venen determinats pels atributs del recurs assignat. Aquests atributs inclouen la unitat organitzativa a la qual pertany el recurs i la funció estàndard del recurs. També podeu afegir atributs personalitzats rellevants per a la vostra empresa per al recurs, com ara el títol estàndard o el nivell d'experiència, i fer que influeixin en el cost unitari o la taxa de facturació de l'assignació.
A més dels atributs del recurs, els atributs del treball, com ara la tasca, també poden influir en la taxa de facturació unitària o la taxa de cost de l'assignació. Per exemple, quan determinades tasques són més complexes, l'assignació del recurs a aquestes tasques específiques té com a resultat un cost unitari o una taxa de facturació més alts que les tasques menys complexes.   

El tercer factor proporciona la quantitat d'hores a aquesta taxa. En els casos en què una tasca cobreixi dos períodes de preus, és probable que la primera part de l'assignació de recursos per a aquesta tasca tingui un cost i un preu diferents dels de la segona part de la tasca. L'estimació de l'esforç en cada assignació de recursos és un valor complex emmagatzemat amb la distribució diària de l'esforç per dia.

Per obtenir instruccions detallades sobre com configurar atributs i recursos personalitzats com a dimensions de preus i costos, vegeu [Informació general sobre les dimensions dels preus](../pricing-costing/pricing-dimensions-overview.md).

L'estimació financera de cada assignació de recursos es calcula com a **taxa/h per a l'assignació multiplicada pel nombre d'hores.**  De manera similar a l'estimació de l'esforç, l'estimació financera del cost i dels ingressos per cada assignació de recursos és un valor complex emmagatzemat amb la distribució diària de l'import monetari per dia. 

## <a name="summarizing-financial-estimates-for-time"></a>Resum d'estimacions financeres per temps
Una estimació financera per a temps en una tasca de node fulla és la suma de les estimacions financeres de totes les assignacions de recursos per a aquesta tasca.

Una estimació financera per a temps en una tasca de resum o principal és la suma de les estimacions financeres de totes les seves tasques secundàries. Aquest és el cost laboral estimat del projecte. 

![Estimacions de recursos.](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a>Preu de cost i moneda de cost per defecte

El preu de cost per defecte prové de les llistes de preus adjuntades a la unitat de contractació del projecte. La moneda de cost d'un projecte és sempre la moneda de la unitat de contractació del projecte. En una assignació de recursos, l'estimació financera del cost s'emmagatzema en la moneda de cost del projecte. De vegades, la moneda en què la taxa de cost està configurada a la llista de preus és diferent de la moneda de cost del projecte. En aquests casos, l'aplicació converteix la moneda en què està configurat el preu de cost per la moneda del projecte. A la quadrícula **Estimacions**, totes les estimacions de costos es mostren i es resumeixen en la moneda de cost del projecte. 

## <a name="default-bill-rate-and-sales-currency"></a>Tarifa de facturació i moneda de vendes per defecte

El preu de venda per defecte prové de les llistes de preus del projecte adjuntades al contracte de projecte relacionat si s'ha guanyat el contracto o de l'oferta de projecte relacionada si l'acord encara es troba en fase de prevendes. La moneda de vendes del projecte és sempre la moneda de l'oferta de projecte o del contracte del projecte. En una assignació de recursos, l'estimació financera de les vendes s'emmagatzema en la moneda de vendes del projecte. A diferència del cost, el preu de venda que es configura a la llista de preus mai pot ser diferent de la moneda de vendes del projecte. No hi ha cap escenari on es necessiti la conversió de divises. A la quadrícula **Estimacions**, totes les estimacions de vendes es mostren i es resumeixen en la moneda de vendes del projecte. 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
