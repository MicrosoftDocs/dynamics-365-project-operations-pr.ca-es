---
title: Desglossament de les despeses
description: En aquest tema s'explica com detallar les despeses mitjançant l'espai de treball de despeses reimaginat.
author: suvaidya
ms.date: 12/16/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 34b11c6bd8be729957973a60fccccc2dd32c2669
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8574510"
---
# <a name="expense-itemization"></a>Desglossament de les despeses

[!include [banner](../includes/banner.md)]

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

Les organitzacions sovint requereixen que els empleats proporcionin un desglossament detallat de les despeses incorregudes durant el viatge. Per exemple, un foli d'hotel pot contenir diverses línies detallades per al preu de l'habitació, els impostos, l'aparcament i altres despeses diverses incorregudes cada dia durant la durada de l'estada. O una despesa de menjar pot requerir que proporcioneu una avaria més granular per esmorzar, dinar o sopar. Siguin quines siguin les necessitats de l'organització, cada categoria de despeses es pot configurar per reflectir les subcategories o les partides de línia que conformen una despesa. Tot i que la desglossació sempre s'ha compatible amb **la gestió** de despeses, l'àrea **de treball de despeses** reimaginada permet una detallització més eficient quan la funció, **La possibilitat de detallar les despeses recurrents ràpidament** està habilitada.  

## <a name="enable-quick-itemization"></a>Habilita l'elementació ràpida 

Podeu utilitzar la **funció Capacitat per detallar les despeses recurrents ràpidament** per detallar les despeses recurrents ràpidament, evitant la necessitat d'introduir les despeses diàries cada vegada durant la durada de l'estada. Completeu els passos següents per habilitar l'elementització ràpida.

1. Aneu a l'àrea **de treball Gestió** de funcions i, a la llista de funcions, localitzeu i seleccioneu, **Informes de despeses Reimaginats**. 
2. Seleccioneu **Habilita ara**. 
3. A la llista de funcions, localitzeu i seleccioneu, **Possibilitat de detallar ràpidament** les despeses recurrents.
4. Seleccioneu **Habilita ara**. 

## <a name="itemization-grid"></a>Quadrícula d'elements 

Si una categoria de despeses té subcategories o components diferents que componen aquesta despesa, es pot detallar. Per detallar una despesa, seleccioneu la línia de despeses de l'informe de despeses i, a la **subfinestra Dades de despeses**, seleccioneu **Accions** > **elementa**. El **control lliscant Itemization** revela una quadrícula amb camps. La taula següent proporciona un exemple de cada camp de la quadrícula i com es representa el camp a l'informe de despeses. 

|     Camp          |     Descripció                                                                                  |     Exemple              |
|--------------------|--------------------------------------------------------------------------------------------------|--------------------------|
|     Subcategoria    |     La llista de subcategories configurades sota el tipus de categoria de despeses, **Hotel**.             |     Tarifa d'habitació diària      |
|     Data d’inici     |     La data en què es va incórrer per primera vegada en l'article de despeses.                                           |     09/13/2021           |
|     Tarifa diària     |     L'import incorregut per l'import de la partida de despeses.                                                    |     200                  |
|     Quantitat       |     Nombre de vegades que la càrrega es repeteix al llarg d'un període continu.                       |     3                    |

![Desglossa la despesa.](media/Itemization%20screen%201.png)

Quan deseu una elementització, veureu una línia desglossada individual per a la quantitat especificada a la quadrícula d'element. Cada línia comença en la data especificada a la quadrícula.

![Informe desglossat.](media/Itemization%20screen%202.png)

