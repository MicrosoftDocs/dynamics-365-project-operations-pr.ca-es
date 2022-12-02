---
title: Desglossament de les despeses
description: En aquest article s'explica com es desglossen les despeses mitjançant la nova àrea de treball Despeses.
author: suvaidya
ms.date: 12/16/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 71bfbe83259804fc0b0355c81d430805da23dd45
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920922"
---
# <a name="expense-itemization"></a>Desglossament de les despeses

[!include [banner](../includes/banner.md)]

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

Les organitzacions requereixen sovint que els empleats proporcionin un desglossament detallat de les despeses en que incorren durant els desplaçaments. Per exemple, un compte de client de l'hotel pot contenir diverses línies desglossades per al preu d'habitació, els impostos, l'aparcament i altres despeses ocasionades cada dia durant l'estada. O una despesa d'àpats pot requerir que indiqueu un desglossament més granular per a l'esmorzar, el dinar o el sopar. Independentment de les necessitats de l'organització, cada categoria de despesa es pot configurar per reflectir les subcategories o els elements de línia que componen una despesa. Mentre que l'ús del desglossament sempre s'ha admès a **Administració de despeses**, la **nova àrea de treball de Despeses** permet un desglossament més eficient quan la característica **Capacitat de desglossar les despeses periòdiques ràpidament** està habilitada.  

## <a name="enable-quick-itemization"></a>Habilitar el desglossament ràpid 

Podeu utilitzar la **Capacitat de desglossar les despeses periòdiques ràpidament** per desglossar les despeses periòdiques ràpidament i evitar la necessitat d'introduir les despeses diàries cada vegada durant tota l'estada. Completeu els passos següents per habilitar el desglossament ràpid.

1. Aneu a l'àrea de treball **Administració de característiques** i, a la llista de característiques, localitzeu i seleccioneu **Nous informes de despeses**. 
2. Seleccioneu **Habilita ara**. 
3. A la llista de característiques, localitzeu i seleccioneu **Capacitat de desglossar ràpidament les despeses periòdiques**.
4. Seleccioneu **Habilita ara**. 

## <a name="itemization-grid"></a>Quadrícula de desglossament 

Si una categoria de despesa té subcategories o components diferents que componen aquesta despesa, també la podreu desglossar. Per desglossar una despesa, seleccioneu la línia de despesa a l'informe de despeses i, a la subfinestra **Detalls de la despesa**, seleccioneu **Accions** > **Desglossa**. El control lliscant **Desglossament** mostra una quadrícula amb camps. A la taula següent es mostra un exemple de cada camp de la quadrícula i de quina manera es representa el camp a l'informe de despeses. 

|     Camp          |     Descripció                                                                                  |     Exemple              |
|--------------------|--------------------------------------------------------------------------------------------------|--------------------------|
|     Subcategoria    |     Llista de subcategories configurades segons el tipus de categoria de despesa, **Hotel**.             |     Tarifa diària d'habitació      |
|     Data d’inici     |     La data en què es va incórrer per primer cop l'article de la despesa.                                           |     09/13/2021           |
|     Tarifa diària     |     L'import incorregut per l'article de la despesa.                                                    |     200                  |
|     Quantitat       |     Nombre de vegades que el càrrec es repeteix en un període continu.                       |     3                    |

![Desglosseu la despesa.](media/Itemization%20screen%201.png)

Quan deseu un desglossament, veureu una línia desglossada individual per a la quantitat especificada a la quadrícula Desglossament. Cada línia s'inicia a la data que s'especifica a la quadrícula.

![Informe desglossat.](media/Itemization%20screen%202.png)

