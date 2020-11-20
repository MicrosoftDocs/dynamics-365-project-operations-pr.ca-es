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
ms.openlocfilehash: 306f169ee25d42ac3c9e63fa70956b9c50315829
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122106"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a><span data-ttu-id="dfa5d-103">Per què el preu predeterminat és zero al cost de despeses reals?</span><span class="sxs-lookup"><span data-stu-id="dfa5d-103">Why is the price defaulting to zero on expense cost actuals?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="dfa5d-104">Aquesta pregunta freqüent s'aplica als valors reals de despeses on la classe de transacció s'estableix en Despeses i el tipus de transacció és Cost.</span><span class="sxs-lookup"><span data-stu-id="dfa5d-104">This FAQ applies to expense actuals where the transaction class is set to Expense and transaction type is Cost.</span></span>

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a><span data-ttu-id="dfa5d-105">Resolució de problemes de costos en els costos reals de les despeses.</span><span class="sxs-lookup"><span data-stu-id="dfa5d-105">Troubleshooting cost rates on expense cost actuals</span></span>

<span data-ttu-id="dfa5d-106">Aneu a l'entrada de despeses relacionada i assegureu-vos que hi ha una quantitat al camp d'entrada de despeses.</span><span class="sxs-lookup"><span data-stu-id="dfa5d-106">Go to the related expense entry and make sure that there’s an amount in the expense entry field.</span></span> <span data-ttu-id="dfa5d-107">Si l'entrada de despeses d'origen no té el camp de quantitat ple, haureu aïllat el problema.</span><span class="sxs-lookup"><span data-stu-id="dfa5d-107">If the originating expense entry didn’t have the amount field filled, then you have isolated the problem.</span></span>
 
<span data-ttu-id="dfa5d-108">Per solucionar aquest problema, torneu a crear l'entrada de despesa amb una quantitat vàlida i aproveu-la.</span><span class="sxs-lookup"><span data-stu-id="dfa5d-108">To solve this problem, recreate the expense entry with a valid amount and approve it.</span></span>
