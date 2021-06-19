---
title: Anàlisi de les ofertes del projecte
description: En aquest tema es proporciona informació sobre l'anàlisi de les ofertes del projecte.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
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
ms.openlocfilehash: acb3f1a2020cfd59f60f828e9092bd7ccde00077
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012439"
---
# <a name="analysis-of-project-quotes"></a><span data-ttu-id="573b3-103">Anàlisi de les ofertes del projecte</span><span class="sxs-lookup"><span data-stu-id="573b3-103">Analysis of project quotes</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="573b3-104">El Dynamics 365 Project Service Automation analitza les ofertes de projectes per estimar la rendibilitat.</span><span class="sxs-lookup"><span data-stu-id="573b3-104">Dynamics 365 Project Service Automation analyzes project quotes to estimate profitability.</span></span> <span data-ttu-id="573b3-105">També analitza la manera com s'alinea l'oferta amb les expectatives del client sobre la data d'entrega o de finalització i sobre el pressupost.</span><span class="sxs-lookup"><span data-stu-id="573b3-105">It also analyzes how well the quote is aligned with customer expectations about the delivery date or completion date, and about the budget.tions.</span></span>

## <a name="profitability-analysis"></a><span data-ttu-id="573b3-106">Anàlisi de rendibilitat</span><span class="sxs-lookup"><span data-stu-id="573b3-106">Profitability analysis</span></span>

<span data-ttu-id="573b3-107">El Project Service Automation analitza la rendibilitat mitjançant el marge brut i el marge brut ajustat.</span><span class="sxs-lookup"><span data-stu-id="573b3-107">Project Service Automation analyzes profitability by using the gross margin and the adjusted gross margin.</span></span>

- <span data-ttu-id="573b3-108">Els marges bruts es calculen mitjançant la fórmula següent:</span><span class="sxs-lookup"><span data-stu-id="573b3-108">Gross margins are calculated by using the following formula:</span></span>

  `
    (Sum of estimated chargeable sales value – Sum of estimated chargeable costs) x 100
  `
- <span data-ttu-id="573b3-109">El marge brut ajustat es calcula mitjançant la fórmula següent:</span><span class="sxs-lookup"><span data-stu-id="573b3-109">The adjusted gross margin is calculated by using the following formula:</span></span>

  `
    (Sum of estimated chargeable sales value – Sum of all estimated costs) x 100
  `

<span data-ttu-id="573b3-110">Si els valors del marge brut i el marge brut ajustat difereixen per un marge ampli, gran part del treball de l'oferta es classifica com a de no-pagament.</span><span class="sxs-lookup"><span data-stu-id="573b3-110">If the values for gross margin and adjusted gross margin differ by a wide margin, much of the work in the quote is classified as non-chargeable.</span></span>

## <a name="analysis-of-customer-expectations"></a><span data-ttu-id="573b3-111">Anàlisi de les expectatives del client</span><span class="sxs-lookup"><span data-stu-id="573b3-111">Analysis of customer expectations</span></span>

<span data-ttu-id="573b3-112">Podeu analitzar ofertes i generar gràfics per a les expectatives de client sobre la planificació i el pressupost si introduïu valors per als camps següents:</span><span class="sxs-lookup"><span data-stu-id="573b3-112">You can analyze quotes and generate charts for customer expectations about the schedule and budget if you enter values for the following fields:</span></span>

- <span data-ttu-id="573b3-113">Camp **Data de lliurament sol·licitada** a la capçalera de l'oferta.</span><span class="sxs-lookup"><span data-stu-id="573b3-113">The **Requested delivery date** field on the quote header.</span></span>
- <span data-ttu-id="573b3-114">Camp **Pressupost de client** per a cada línia d'oferta (per a les línies basades en el projecte i les línies basades en productes).</span><span class="sxs-lookup"><span data-stu-id="573b3-114">The **Customer budget** field for each quote line (for project-based lines and product-based lines).</span></span>

<span data-ttu-id="573b3-115">L'anàlisi de les expectatives dels clients sobre la planificació es fa comparant l'última data d'acabament del detall de la línia d'oferta amb la data de lliurament sol·licitada a totes les línies d'oferta de l'oferta.</span><span class="sxs-lookup"><span data-stu-id="573b3-115">Analysis of customer expectations about the schedule is done by comparing the latest end date of the quote line detail with the requested delivery date across all quote lines in the quote.</span></span>

<span data-ttu-id="573b3-116">L'anàlisi de les expectatives dels clients sobre el pressupost es fa comparant la suma del pressupost total de clients amb l'import de la cotització a totes les línies d'oferta.</span><span class="sxs-lookup"><span data-stu-id="573b3-116">Analysis of customer expectations about the budget is done by comparing the sum of the total customer budget with the quoted amount across all quote lines.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]