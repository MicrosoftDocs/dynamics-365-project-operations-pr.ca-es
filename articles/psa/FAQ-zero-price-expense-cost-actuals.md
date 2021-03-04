---
title: Per què el preu predeterminat és zero al cost de despeses reals?
description: Solució de problemes amb el preu predeterminat a 0 en el cost de despeses real.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/22/2018
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
ms.openlocfilehash: f6ea664f9f38621ce5d1b0dd033d7df491f845ff
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146336"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a>Per què el preu es defineix per defecte com a zero a les xifres reals dels costos de despeses

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Aquesta pregunta freqüent s'aplica als valors reals de despeses on la classe de transacció s'estableix en Despeses i el tipus de transacció és Cost.

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a>Resolució de problemes de costos en els costos reals de les despeses.

Aneu a l'entrada de despeses relacionada i assegureu-vos que hi ha una quantitat al camp d'entrada de despeses. Si l'entrada de despeses d'origen no té el camp de quantitat ple, haureu aïllat el problema.
 
Per solucionar aquest problema, torneu a crear l'entrada de despesa amb una quantitat vàlida i aproveu-la.
