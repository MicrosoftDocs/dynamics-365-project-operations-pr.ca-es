---
title: Transicions d'estat en un subcontracte
description: En aquest article s'expliquen les transicions estatals sobre una subcontractació a Microsoft Dynamics 365 Project Operations a mesura que es crea, s'executa i es tanca la subcontractació.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 02553099a6728c19c219659dff431ff9a5cf10fc
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261170"
---
# <a name="state-transitions-on-a-subcontract"></a>Transicions d'estat en un subcontracte 

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_

En aquest article s'expliquen les transicions estatals sobre una subcontracta en Microsoft Dynamics 365 Project Operations. Cada estat es representa com a esborrany, confirmat, tancat o cancel·lat. La imatge següent representa les transicions d'estat.

![Model d'estat de subcontractació](../media/SubconStates.png)  

La taula següent proporciona una descripció del que representa cada estat en el cicle de vida d'una subcontracta en operacions de projecte.

| Estat o província | Descripció | Transicions permeses |
| --- | --- | --- |
| Esborrany | Això representa l'estat inicial d'una subcontractació. Les negociacions amb el proveïdor estan en curs. Les línies i els preus estan subjectes a modificacions. Una subcontracta en aquest estat es pot utilitzar per estimar i planificar els requisits del projecte de recursos i materials. També es pot fer referència sobre el temps, la despesa i l'ús de material en un projecte. Un subcontractat en aquest estat es pot editar i suprimir. | Confirmat |
| Confirmat | Això representa l'etapa d'una subcontractació després que s'hagin completat les negociacions amb el proveïdor sobre els preus i els articles de línia que s'estan comprant. No obstant això, el lliurament real de materials i/o treballs per part dels recursos subcontractats continua en curs. Una subcontracta en aquest estat es pot utilitzar per estimar i planificar els requisits del projecte de recursos i materials. També es pot fer referència sobre el temps, la despesa i l'ús de material en un projecte. Una subcontractació en aquest estat no es pot editar ni suprimir. El **botó Cancel·lar** permet cancel·lar una subcontracta confirmada. El **botó Torna a obrir** permet tornar a obrir la subcontracta per tornar-la **a l'estat Esborrany**. Utilitzeu el **botó Tanca** per tancar una subcontracta confirmada. | Tancada <br> Cancel·lada <br> Esborrany |
| Tancada | Això representa l'etapa d'una subcontractació quan es completa el lliurament real de materials i/o treballs per part dels recursos subcontractats. Una subcontracta en aquest estat ja no es pot utilitzar per estimar i planificar els requisits del projecte de recursos i materials. A més, ja no es pot fer referència a l'ús de temps, despeses i material en un projecte. Una subcontractació en aquest estat no es pot editar ni suprimir. | cap |
| Cancel·lada | Això representa l'etapa d'una subcontractació quan ja no es necessita el lliurament real de materials i/o treballs per part dels recursos subcontractats. Una subcontractació en aquest estat no es pot utilitzar per estimar i els requisits del projecte de personal per a recursos i materials ni tampoc es pot fer referència a temps, despeses i ús de material en un projecte. Una subcontractació en aquest estat no es pot editar ni suprimir. | cap |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
