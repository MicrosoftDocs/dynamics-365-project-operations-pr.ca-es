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
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a><span data-ttu-id="f009c-103">Per què el preu es defineix per defecte com a zero a les xifres reals dels costos de despeses</span><span class="sxs-lookup"><span data-stu-id="f009c-103">Why is the price defaulting to zero on expense cost actuals</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="f009c-104">Aquesta pregunta freqüent s'aplica als valors reals de despeses on la classe de transacció s'estableix en Despeses i el tipus de transacció és Cost.</span><span class="sxs-lookup"><span data-stu-id="f009c-104">This FAQ applies to expense actuals where the transaction class is set to Expense and transaction type is Cost.</span></span>

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a><span data-ttu-id="f009c-105">Resolució de problemes de costos en els costos reals de les despeses.</span><span class="sxs-lookup"><span data-stu-id="f009c-105">Troubleshooting cost rates on expense cost actuals</span></span>

<span data-ttu-id="f009c-106">Aneu a l'entrada de despeses relacionada i assegureu-vos que hi ha una quantitat al camp d'entrada de despeses.</span><span class="sxs-lookup"><span data-stu-id="f009c-106">Go to the related expense entry and make sure that there’s an amount in the expense entry field.</span></span> <span data-ttu-id="f009c-107">Si l'entrada de despeses d'origen no té el camp de quantitat ple, haureu aïllat el problema.</span><span class="sxs-lookup"><span data-stu-id="f009c-107">If the originating expense entry didn’t have the amount field filled, then you have isolated the problem.</span></span>
 
<span data-ttu-id="f009c-108">Per solucionar aquest problema, torneu a crear l'entrada de despesa amb una quantitat vàlida i aproveu-la.</span><span class="sxs-lookup"><span data-stu-id="f009c-108">To solve this problem, recreate the expense entry with a valid amount and approve it.</span></span>
