---
title: Compliment dels requisits de recursos genèrics
description: Aquest tema proporciona informació sobre com reservar recursos amb nom per a un requisit de recurs genèric.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 6bb7c185656ff87bb3ca24209594c07d25862d70
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072157"
---
# <a name="generic-resource-requirement-fulfillment"></a><span data-ttu-id="bd310-103">Compliment dels requisits de recursos genèrics</span><span class="sxs-lookup"><span data-stu-id="bd310-103">Generic resource requirement fulfillment</span></span>

<span data-ttu-id="bd310-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_</span><span class="sxs-lookup"><span data-stu-id="bd310-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="bd310-105">Podeu reservar un recurs amb nom per reemplaçar un recurs genèric que tingui un requisit de recurs.</span><span class="sxs-lookup"><span data-stu-id="bd310-105">You can book a named resource to replace generic resource that has a resource requirement.</span></span>

1. <span data-ttu-id="bd310-106">A la pàgina **Projectes** , seleccioneu la pestanya **Equip**.</span><span class="sxs-lookup"><span data-stu-id="bd310-106">On the **Projects** page, select the **Team** tab.</span></span>
2. <span data-ttu-id="bd310-107">Seleccioneu el recurs genèric que té un requisit de recurs de la llista i, a continuació, seleccioneu **Reserva**.</span><span class="sxs-lookup"><span data-stu-id="bd310-107">Select the generic resource that has a resource requirement from the list, and then select **Book**.</span></span> <span data-ttu-id="bd310-108">O bé, obriu el requisit del recurs i, a continuació, seleccioneu **Reserva**.</span><span class="sxs-lookup"><span data-stu-id="bd310-108">Or, open the resource requirement and then select **Book**.</span></span>
3. <span data-ttu-id="bd310-109">A la pàgina **Auxiliar de planificació** , seleccioneu un recurs amb nom per fer la reserva a l'equip del projecte i, a continuació, seleccioneu **Reserva**.</span><span class="sxs-lookup"><span data-stu-id="bd310-109">On the **Schedule Assistant** page, select a named resource to book onto your project team and then select **Book**.</span></span>

<span data-ttu-id="bd310-110">Quan la reserva s'hagi completat i complert per un recurs amb nom, el recurs genèric se substitueix pel recurs amb nom.</span><span class="sxs-lookup"><span data-stu-id="bd310-110">When the booking is complete and fulfilled by a named resource, the generic resource is replaced with the named resource.</span></span>

<span data-ttu-id="bd310-111">Les assignacions de la planificació s'actualitzen també amb el recurs amb nom.</span><span class="sxs-lookup"><span data-stu-id="bd310-111">The assignments on the schedule are updated with the named resource as well.</span></span>

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a><span data-ttu-id="bd310-112">Complir un recurs genèric amb diversos recursos amb nom</span><span class="sxs-lookup"><span data-stu-id="bd310-112">Fulfill a generic resource with multiple named resources</span></span>
<span data-ttu-id="bd310-113">El compliment d'un requisit per a un recurs genèric amb diversos recursos amb nom és similar a l'assignació d'un recurs amb nom.</span><span class="sxs-lookup"><span data-stu-id="bd310-113">Fulfilling a requirement for a generic resource with multiple named resources is similar to assigning a single named resource.</span></span> <span data-ttu-id="bd310-114">Per exemple, hi ha una tasca amb una durada de cinc dies i 120 hores d'esforç.</span><span class="sxs-lookup"><span data-stu-id="bd310-114">For example, there is a task with a duration of five days and 120 hours of effort.</span></span> <span data-ttu-id="bd310-115">No es pot completar aquesta tasca amb un recurs que treballi un dia típic de vuit hores al llarg d'una setmana de cinc dies.</span><span class="sxs-lookup"><span data-stu-id="bd310-115">This task can't be completed by one resource that works a typical eight-hour day over a five-day week.</span></span> 

<span data-ttu-id="bd310-116">El requisit és de 120 hores d'enginyeria de robòtica al llarg de cinc dies, que és de 24 hores per dia.</span><span class="sxs-lookup"><span data-stu-id="bd310-116">The requirement is for 120 hours of robotics engineering over five days, which is 24 hours per day.</span></span>

<span data-ttu-id="bd310-117">Aquest és un exemple de quan es necessiten diversos recursos amb nom per complir una sol·licitud de recurs genèrica.</span><span class="sxs-lookup"><span data-stu-id="bd310-117">This is an example of when multiple named resources are needed to fulfill a generic resource request.</span></span> <span data-ttu-id="bd310-118">Haureu de reservar diversos recursos per complir el requisit.</span><span class="sxs-lookup"><span data-stu-id="bd310-118">You will need to book multiple resources to fulfill the requirement.</span></span>

<span data-ttu-id="bd310-119">La diferència principal en aquest escenari és que el recurs genèric es manté a l'equip assignat a la tasca i els membres de l'equip de recursos amb nom no s'assignen com a part del càrrec.</span><span class="sxs-lookup"><span data-stu-id="bd310-119">The main difference in this scenario is that the generic resource remains on the team assigned to the task, and the booked named resource team members are not assigned as part of the position.</span></span> <span data-ttu-id="bd310-120">L'administrador del projecte pot assignar la feina segons calgui als recursos amb nom.</span><span class="sxs-lookup"><span data-stu-id="bd310-120">The project manager can assign the work as appropriate to the named resources.</span></span> <span data-ttu-id="bd310-121">La visualització **Conciliació** pot ajudar a l'administrador del projecte a dividir les reserves entre diversos recursos a assignacions de tasques.</span><span class="sxs-lookup"><span data-stu-id="bd310-121">The **Reconciliation** view can assist a project manager in breaking up the bookings across multiple resources to task assignments.</span></span> <span data-ttu-id="bd310-122">Això no es fa de manera automàtica perquè en qualsevol escenari més complicat que l'anterior, com ara un on teniu un paquet de tasques que constitueixen el requisit, el sistema ha de suposar la intenció de com vol assignar-ho l'administrador del projecte.</span><span class="sxs-lookup"><span data-stu-id="bd310-122">This is not done automatically because in any scenario more complicated than the simple example above, such as where you have a bundle of tasks making up the requirement or the intent of how the project manager wants to assign, needs to be assumed by the system.</span></span> <span data-ttu-id="bd310-123">Com que el sistema no pot entendre la intenció, és probable que les hipòtesis siguin diferents del previst i que es produeixi un resultat incorrecte o imprevisible.</span><span class="sxs-lookup"><span data-stu-id="bd310-123">Because the system can't understand intent, it's likely that the assumptions will be different than intended and an incorrect or unpredictable result will occur.</span></span> <span data-ttu-id="bd310-124">El resultat predictible és que el recurs genèric es manté assignat fins que l'administrador del projecte crea deliberadament les assignacions amb l'ajuda de la visualització **Conciliació**.</span><span class="sxs-lookup"><span data-stu-id="bd310-124">The predictable outcome is that the generic resource remains assigned until the project manager deliberately creates assignments, with the assistance of the **Reconciliation** view.</span></span>


