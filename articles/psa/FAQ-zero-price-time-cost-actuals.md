---
title: Per què el preu predeterminat és zero en el cost de temps real?
description: Solució de problemes amb el preu predeterminat a 0 en el cost de temps real.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
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
ms.openlocfilehash: ffe915a48f088bde457121a323325ba490c24e45
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993044"
---
# <a name="why-is-the-price-defaulting-to-zero-on-time-cost-actuals"></a><span data-ttu-id="76aad-103">Per què el preu predeterminat és zero en el cost de temps real?</span><span class="sxs-lookup"><span data-stu-id="76aad-103">Why is the price defaulting to zero on time cost actuals?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="76aad-104">Aquesta pregunta freqüent s'aplica als valors reals on la classe de transacció s'estableix en Temps i el tipus de transacció és Cost.</span><span class="sxs-lookup"><span data-stu-id="76aad-104">This FAQ applies to actuals where the transaction class is set to Time and transaction type is Cost.</span></span> <span data-ttu-id="76aad-105">Els tres controls següents us ajudaran a solucionar per què el preu està predeterminat a 0 en el cost de temps real.</span><span class="sxs-lookup"><span data-stu-id="76aad-105">The following three checks will help you troubleshoot why the price is defaulting to 0 on time cost actuals.</span></span>
 
## <a name="check-1-identify-the-cost-price-list-for-the-project"></a><span data-ttu-id="76aad-106">Comprovació 1: identificar la llista de preus de cost per al projecte</span><span class="sxs-lookup"><span data-stu-id="76aad-106">Check 1: Identify the cost price list for the project</span></span>

<span data-ttu-id="76aad-107">Busqueu el projecte des del camp del projecte real i aneu a la pàgina del projecte.</span><span class="sxs-lookup"><span data-stu-id="76aad-107">Find the project from the project field of the actual and then go to the project page.</span></span> <span data-ttu-id="76aad-108">Feu clic a l'enllaç de la unitat de contractació al camp.</span><span class="sxs-lookup"><span data-stu-id="76aad-108">Click on the contracting unit link in the field.</span></span> <span data-ttu-id="76aad-109">A la pàgina Unitat de contractació, verifiqueu si la unitat té una llista de preus en la quadrícula de Llistes de preus de cost.</span><span class="sxs-lookup"><span data-stu-id="76aad-109">On the Contracting Unit page, check if the contracting unit has a price list in the Cost Price Lists grid.</span></span>

<span data-ttu-id="76aad-110">Si hi ha més d'una llista de preus, haureu aïllat el problema.</span><span class="sxs-lookup"><span data-stu-id="76aad-110">If there is more than one price list, you have isolated the problem.</span></span> <span data-ttu-id="76aad-111">El Project Service només admet una llista de preus per unitat organitzativa.</span><span class="sxs-lookup"><span data-stu-id="76aad-111">Project Service only supports one price list per organizational unit.</span></span> <span data-ttu-id="76aad-112">Elimineu totes les llistes de preus d'aquesta entitat fins que només hi hagi una llista de preus adjunta a la quadrícula Llistes de preus de cost de la Unitat organitzativa.</span><span class="sxs-lookup"><span data-stu-id="76aad-112">Remove all prices lists from this entity until there is only one price list attached in the Cost Price Lists grid of the Organizational Unit.</span></span>

<span data-ttu-id="76aad-113">Si no hi ha llistes de preus adjuntes a la Unitat organitzativa, anoteu la moneda de la Unitat organitzativa.</span><span class="sxs-lookup"><span data-stu-id="76aad-113">If there are no price lists attached to the Organizational Unit, make a note of the currency of the Organizational unit.</span></span> <span data-ttu-id="76aad-114">Aneu al Project Service i després a Paràmetres i obriu la pestanya Llistes de preus. Comproveu si hi ha llistes de preus amb context establert a Cost i moneda que coincideixi amb la moneda de la Unitat organitzativa.</span><span class="sxs-lookup"><span data-stu-id="76aad-114">Go to the Project Service and then Parameters and open the Price Lists tab. Check if there are any price lists with context set to Cost and currency that matches the currency of the Organizational Unit.</span></span>
 
<span data-ttu-id="76aad-115">Si no hi ha llistes de preus que coincideixin amb els criteris, haureu aïllat el problema.</span><span class="sxs-lookup"><span data-stu-id="76aad-115">If there are no price lists that match that criteria, you have isolated the problem.</span></span> <span data-ttu-id="76aad-116">Assegureu-vos de tenir almenys una llista de preus amb el context configurat a Cost i amb la moneda de la Unitat organitzativa.</span><span class="sxs-lookup"><span data-stu-id="76aad-116">Make sure to have at least one price list whose context is set to Cost and whose currency matches the currency of the Organizational Unit.</span></span>

<span data-ttu-id="76aad-117">Si hi ha més d'una llista de preus que coincideixi amb aquest criteri, continueu llegint aquest document per fer més comprovacions.</span><span class="sxs-lookup"><span data-stu-id="76aad-117">If there is more than one price list that match that criteria, continue reading this document to make more checks.</span></span>

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-cost-actual"></a><span data-ttu-id="76aad-118">Comprovació 2: Alguna de les llistes de preus identificades anteriorment és vàlida per a la data específica del cost de temps real?</span><span class="sxs-lookup"><span data-stu-id="76aad-118">Check 2: Are any of the price lists identified above valid for the specific date of the time cost actual?</span></span>

<span data-ttu-id="76aad-119">Perquè el Project Service tingui en compte una llista de preus utilitzada per establir el preu per defecte, s'ha de poder aplicar per a la data del cost de temps real.</span><span class="sxs-lookup"><span data-stu-id="76aad-119">For Project Service to consider a price list for defaulting price, that price list should be applicable for the date on the time cost actual.</span></span> <span data-ttu-id="76aad-120">Comproveu les opcions següents per veure si les llistes de preus identificades anteriorment són aplicables:</span><span class="sxs-lookup"><span data-stu-id="76aad-120">Check the following to see if the price list(s) identified above are applicable:</span></span>

- <span data-ttu-id="76aad-121">Comproveu si les dates d'inici i finalització de la pestanya general de les llistes de preus adjuntes i mireu que no estiguin buides.</span><span class="sxs-lookup"><span data-stu-id="76aad-121">Check if the start and end dates on the general tab for the price lists attached aren’t empty.</span></span> <span data-ttu-id="76aad-122">Si les dates d'inici i finalització estan buides, haureu aïllat el problema.</span><span class="sxs-lookup"><span data-stu-id="76aad-122">If the start and end dates on price lists identified above are empty, you have isolated the problem.</span></span> 
- <span data-ttu-id="76aad-123">Anoteu el camp de data d'inici en el cost de temps real i verifiqueu si alguna de les llistes de preus identificades és aplicable per a aquesta data.</span><span class="sxs-lookup"><span data-stu-id="76aad-123">Make a note of the start date field on your time cost actual and check if any of the price lists identified is applicable for that date.</span></span> <span data-ttu-id="76aad-124">Per exemple, la data del cost de temps real ha d'estar dins de la data d'inici i la de finalització en la llista de preus.</span><span class="sxs-lookup"><span data-stu-id="76aad-124">For example, the date of the time cost actual should fall within the start date and end date on the price list.</span></span> 
    - <span data-ttu-id="76aad-125">Si no hi ha cap llista de preus que cobreixi aquesta data al cost de temps real, haureu aïllat el problema.</span><span class="sxs-lookup"><span data-stu-id="76aad-125">If there is no price list that covers that date on the time cost actual, you have isolated the problem.</span></span> <span data-ttu-id="76aad-126">Modifiqueu les dates d'inici i finalització de la llista de preus per assegurar-vos que la llista de preus cobreix la data del cost de temps real.</span><span class="sxs-lookup"><span data-stu-id="76aad-126">Modify the start and end dates of the price list to ensure that the price list covers the date of the time cost actual.</span></span> 
    - <span data-ttu-id="76aad-127">Si hi ha més d'una llista de preus que cobreix la data del cost de temps real, haureu aïllat el problema.</span><span class="sxs-lookup"><span data-stu-id="76aad-127">If there is more than one price list that covers the date on the time cost actual, you have isolated the problem.</span></span> <span data-ttu-id="76aad-128">Pot solucionar aquests conflictes si editeu les dates d'inici i finalització de la llista de preus perquè només hi hagi una llista de preus que cobreixi la data del cost de temps real.</span><span class="sxs-lookup"><span data-stu-id="76aad-128">You can fix this by editing the start and end dates of the price list(s) so that there is only one price list that covers the date of the time cost actual.</span></span> 
    - <span data-ttu-id="76aad-129">Si només hi ha una llista de preus que cobreixi aquesta data del cost de temps real, passeu al següent control al document.</span><span class="sxs-lookup"><span data-stu-id="76aad-129">If there is only one price list that covers that date of the time cost actual, move to the next check in the document.</span></span>
<span data-ttu-id="76aad-130">Un cop hagueu finalitzat amb les correccions necessàries, torneu a crear una entrada de temps, aproveu-la i verifiqueu que els cost de temps real mostri un preu vàlid.</span><span class="sxs-lookup"><span data-stu-id="76aad-130">Once you’ve done made the required fixes, recreate a time entry, approve it, and verify that the time cost actual shows a valid price.</span></span>

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-cost-actual"></a><span data-ttu-id="76aad-131">Comprovació 3: Hi ha un preu a la llista de preus per a les dimensions de fixació de preus en el cost de temps real?</span><span class="sxs-lookup"><span data-stu-id="76aad-131">Check 3: Is there a price in the price list for the pricing dimensions on the time cost actual?</span></span>

<span data-ttu-id="76aad-132">Si heu completat amb èxit les comprovacions 1 i 2, ara hauríeu de tenir només una llista de preus aplicable per a la data del temps de cost real.</span><span class="sxs-lookup"><span data-stu-id="76aad-132">If you have successfully completed Check 1 and Check 2, you should now have only one price list that is applicable for the date of the time cost actual.</span></span> <span data-ttu-id="76aad-133">Obriu aquesta Llista de preus i aneu a la pestanya Preus de funció. Assegureu-vos que hi hagi una fila a la quadrícula per a les dimensions de fixació de preus al cost de temps real.</span><span class="sxs-lookup"><span data-stu-id="76aad-133">Open this Price List and go to the Role Prices tab. Make sure that there is a row in the grid for the pricing dimensions on the time cost actual.</span></span>

<span data-ttu-id="76aad-134">Si no hi ha cap fila, haureu aïllat el problema.</span><span class="sxs-lookup"><span data-stu-id="76aad-134">If there is no row in the role price grid for the pricing dimensions on the time cost actual, then you have isolated the problem.</span></span> <span data-ttu-id="76aad-135">Creeu una fila a la quadrícula de preus de funció per a les dimensions de fixació de preus al cost de temps real.</span><span class="sxs-lookup"><span data-stu-id="76aad-135">Create a row in the Role prices grid for the pricing dimensions on your time cost actual.</span></span> <span data-ttu-id="76aad-136">Un cop fet, torneu a crear una entrada de temps, aproveu-la i verifiqueu que el cost de temps real mostri un preu vàlid.</span><span class="sxs-lookup"><span data-stu-id="76aad-136">Once this is done, recreate time entry, approve it, and verify that the time cost actual shows a valid price.</span></span>
 
<span data-ttu-id="76aad-137">Si encara no veieu un preu vàlid al cost de temps real després de realitzar les tres comprovacions anteriors, registreu una sol·licitud d'assistència tècnica.</span><span class="sxs-lookup"><span data-stu-id="76aad-137">If you still don't see a valid price on your time cost actual after you’ve done the three checks above, please log a support ticket.</span></span>





[!INCLUDE[footer-include](../includes/footer-banner.md)]