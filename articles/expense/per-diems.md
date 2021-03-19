---
title: Dietes
description: En aquest tema es proporciona informació sobre les regles de dietes que s'utilitzen a l'administració de despeses.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 70e26a5e0f9a06730a2166318006429195335d4d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276291"
---
# <a name="per-diems"></a><span data-ttu-id="96c50-103">Dietes</span><span class="sxs-lookup"><span data-stu-id="96c50-103">Per diems</span></span>

<span data-ttu-id="96c50-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_</span><span class="sxs-lookup"><span data-stu-id="96c50-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="96c50-105">Una dieta és una assignació que es paga a un treballador que viatja per feina.</span><span class="sxs-lookup"><span data-stu-id="96c50-105">A per diem is an allowance that is paid to a worker who is traveling for work.</span></span> <span data-ttu-id="96c50-106">A l'administració de despeses, podeu crear regles de dietes per a diverses situacions de viatge.</span><span class="sxs-lookup"><span data-stu-id="96c50-106">In Expense management, you can create per diem rules for  various travel situations.</span></span> <span data-ttu-id="96c50-107">Els percentatges de les dietes es poden basar en l'època de l'any, en la ubicació del viatge o tots dos.</span><span class="sxs-lookup"><span data-stu-id="96c50-107">Per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="96c50-108">Quan creeu una regla de dieta, podeu especificar que un percentatge de la tarifa de la dieta es retindrà si un treballador rep àpats o serveis gratuïts.</span><span class="sxs-lookup"><span data-stu-id="96c50-108">When you create a per diem  rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="96c50-109">També podeu definir un nombre mínim i màxim d'hores en què el percentatge de dieta es pot aplicar als viatges d'un treballador.</span><span class="sxs-lookup"><span data-stu-id="96c50-109">You can also set a minimum and maximum number of hours that the per diem rate can apply to a worker's travel.</span></span>

## <a name="configuration"></a><span data-ttu-id="96c50-110">Configuració</span><span class="sxs-lookup"><span data-stu-id="96c50-110">Configuration</span></span> 

1. <span data-ttu-id="96c50-111">Per afegir ubicacions de dietes, aneu a **Configura** > **Càlculs i codis** > **Ubicacions de dietes**.</span><span class="sxs-lookup"><span data-stu-id="96c50-111">To add per diem locations, go to **Set up** > **Calculations and codes** > **Per diem locations**.</span></span>
2. <span data-ttu-id="96c50-112">Per a cadascuna de les ubicacions afegides anteriorment, seleccioneu una tarifa de dieta i la moneda que sigui vàlida entre una data d'inici i d'acabament específica per a hotels, àpats i altres despeses.</span><span class="sxs-lookup"><span data-stu-id="96c50-112">For each of the locations added above, select a per diem rate and currency that is valid between a specific start and end date for hotel, meals, and other expenses.</span></span> <span data-ttu-id="96c50-113">Les tarifes de dietes i les monedes es configuren a **Configura** > **Càlculs i codis** > **Dietes**.</span><span class="sxs-lookup"><span data-stu-id="96c50-113">Per diem rates and currencies are configured under **Set up** > **Calculations and codes** > **Per diems**.</span></span>
3. <span data-ttu-id="96c50-114">A la pàgina **Ubicacions de dietes**, configureu els nivells de tarifes de dietes.</span><span class="sxs-lookup"><span data-stu-id="96c50-114">On the **Per diem locations** page, configure per diem rate tiers.</span></span> <span data-ttu-id="96c50-115">Els nivells de tarifes de dietes us permeten definir el percentatge dividit d'un proveïment diari per a hotels, àpats i altres despeses.</span><span class="sxs-lookup"><span data-stu-id="96c50-115">Per diem rate tiers allow you to define the percentage split of a daily allowance for hotel, meal, and other expenses.</span></span> 
4. <span data-ttu-id="96c50-116">Per especificar la reducció dels percentatges d'àpats per a l'esmorzar, el dinar o el sopar, actualitzeu els camps de la pàgina **Paràmetres d'administració de despeses** a la pestanya **Dietes**.</span><span class="sxs-lookup"><span data-stu-id="96c50-116">To specify the meal percentage reduction for breakfast, lunch, or dinner, update the fields on the **Expense management parameters** page on the **Per diem** tab.</span></span> 
    
## <a name="submit-expenses-using-per-diem"></a><span data-ttu-id="96c50-117">Enviar despeses mitjançant una dieta</span><span class="sxs-lookup"><span data-stu-id="96c50-117">Submit expenses using per diem</span></span>
<span data-ttu-id="96c50-118">Per enviar les despeses que utilitzen les dietes, utilitzeu la categoria de despesa **Dieta** quan creeu un informe de despeses.</span><span class="sxs-lookup"><span data-stu-id="96c50-118">To submit expenses utilizing per diems, use the **Per diem** expense category when you create an expense report.</span></span> <span data-ttu-id="96c50-119">Introduïu la **Data d'inici de la dieta**, **Data de finalització de la dieta** i **Ubicació de la dieta**.</span><span class="sxs-lookup"><span data-stu-id="96c50-119">Enter the **Per diem from date**, **Per diem to date**,  and the **Per diem location**.</span></span> <span data-ttu-id="96c50-120">L'import es calcularà en funció de les tarifes de dieta per a la ubicació seleccionada i es calcularà la reducció dels àpats en funció dels nivells de tarifes de dietes.</span><span class="sxs-lookup"><span data-stu-id="96c50-120">The amount will be calculated based on the per diem rates for the selected location and meal reduction will be calculated based on the per diem rate tiers.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]