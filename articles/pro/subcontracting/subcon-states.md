---
title: Transicions d'Estat en una subcontracta
description: Aquest tema explica les transicions d'estat en una subcontracta a Microsoft Dynamics 365 Project Operations a mesura que la subcontractació es crea, s'executa i es tanca.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: d67f4a3cd834c25462304c2d75c824427fcbd034
ms.sourcegitcommit: 04dc8d952e6da3ab3eb2a20131c6f7cee6040876
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 12/10/2021
ms.locfileid: "7903624"
---
# <a name="state-transitions-on-a-subcontract"></a>Transicions d'Estat en una subcontracta 

[!include [banner](../../includes/dataverse-preview.md)]

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_

Aquest tema explica les transicions d'estat en una subcontracta a Microsoft Dynamics 365 Project Operations. Cada estat es representa com a esborrany, confirmat, tancat o cancel·lat. La següent imatge representa les transicions d'estat.

![Model d'estat de subcontractació](../media/SubconStates.png)  

La taula següent proporciona una descripció del que representa cada estat en el cicle de vida d'una subcontracta en operacions de projecte.

| Estat o província | Descripció | Transicions permeses |
| --- | --- | --- |
| Esborrany | Això representa l'estat inicial d'una subcontracta. Les negociacions amb el venedor estan en curs. Les línies i els preus estan subjectes a modificacions. Una subcontracta en aquest estat es pot utilitzar per estimar i el personal dels requisits del projecte de recursos i materials. També es pot fer referència a temps, despesa i ús de material en un projecte. Una subcontracta en aquest estat es pot editar i suprimir. | Confirmat |
| Confirmat | Això representa l'etapa d'una subcontracta després que s'hagin completat les negociacions amb el proveïdor sobre preus i articles de línia que es compren. No obstant això, el lliurament real de materials i/o treballs per part de recursos subcontractats continua. Una subcontracta en aquest estat es pot utilitzar per estimar i el personal dels requisits del projecte de recursos i materials. També es pot fer referència a temps, despesa i ús de material en un projecte. Una subcontracta d'aquest estat no es pot editar ni suprimir. El **botó** Cancel·la permet cancel·lar una subcontracta confirmada. El **botó Torna a obrir us permet tornar a obrir la** subcontracta per tornar-la a **l**'estat d'esborrany. Utilitzeu el **botó Tanca per tancar una** subcontracta confirmada. | Tancada <br> Cancel·lada <br> Esborrany |
| Tancada | Això representa l'etapa d'una subcontracta quan es completa el lliurament real de materials i / o treballs per recursos subcontractats. Una subcontracta en aquest estat ja no es pot utilitzar per estimar i el personal dels requisits del projecte de recursos i materials. A més, ja no es pot fer referència a temps, despesa i ús de material en un projecte. Una subcontracta d'aquest estat no es pot editar ni suprimir. | cap |
| Cancel·lada | Això representa l'etapa d'una subcontracta quan el lliurament real de materials i / o treballs per recursos subcontractats ja no és necessari. Una subcontracta en aquest estat no es pot utilitzar per estimar i el personal dels requisits del projecte per als recursos i materials ni, es pot fer referència a temps, despesa i ús de material en un projecte. Una subcontracta d'aquest estat no es pot editar ni suprimir. | cap |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
