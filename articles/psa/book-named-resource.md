---
title: Reservar recursos amb nom a partir de requisits de recursos
description: Aquest tema proporciona informació sobre la reserva de recursos amb nom per a un requisit de recurs genèric.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 50858d4fc55285b2e91117c6cbfb2419931b4197
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291022"
---
# <a name="book-named-resources-from-resource-requirements"></a><span data-ttu-id="a62ac-103">Reservar recursos amb nom a partir de requisits de recursos</span><span class="sxs-lookup"><span data-stu-id="a62ac-103">Book named resources from resource requirements</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="a62ac-104">Podeu reservar un recurs amb nom per reemplaçar un recurs genèric que tingui un requisit de recurs.</span><span class="sxs-lookup"><span data-stu-id="a62ac-104">You can book a named resource to replace generic resource that has a resource requirement.</span></span>

1. <span data-ttu-id="a62ac-105">Al Project Service Automation (PSA), a la pàgina **Projectes**, feu clic a la pestanya **Equip**.</span><span class="sxs-lookup"><span data-stu-id="a62ac-105">In Project Service Automation (PSA), on the **Projects** page, click the **Team** tab.</span></span>
2. <span data-ttu-id="a62ac-106">Seleccioneu el recurs genèric que té un requisit de recurs de la llista i, a continuació, feu clic a **Reserva**.</span><span class="sxs-lookup"><span data-stu-id="a62ac-106">Select the generic resource that has a resource requirement from the list and then click **Book**.</span></span> <span data-ttu-id="a62ac-107">O bé, obriu el requisit del recurs i, a continuació, feu clic a **Reserva**.</span><span class="sxs-lookup"><span data-stu-id="a62ac-107">Or, open the resource requirement and then click **Book**.</span></span>


![Reservar un membre genèric de l'equip](media/RM-how-to-14.png)


3. <span data-ttu-id="a62ac-109">A la pàgina **Auxiliar de planificació**, seleccioneu un recurs amb nom per fer la reserva a l'equip del projecte i, a continuació, feu clic a **Reserva**.</span><span class="sxs-lookup"><span data-stu-id="a62ac-109">On the **Schedule Assistant** page, select a named resource to book onto your project team and then click **Book**.</span></span>

![Reservar un membre genèric de l'equip mitjançant l'auxiliar de planificació](media/RM-how-to-15.png)

<span data-ttu-id="a62ac-111">Quan la reserva s'hagi completat i complert per un recurs amb nom, el recurs genèric se substitueix pel recurs amb nom.</span><span class="sxs-lookup"><span data-stu-id="a62ac-111">When the booking is complete and fulfilled by a named resource, the generic resource is replaced with the named resource.</span></span>

![Membre de l'equip amb nom que substitueix un membre genèric de l'equip](media/RM-how-to-16.png)

<span data-ttu-id="a62ac-113">Les assignacions de la planificació s'actualitzen també amb el recurs amb nom.</span><span class="sxs-lookup"><span data-stu-id="a62ac-113">The assignments on the schedule are updated with the named resource as well.</span></span>

![Membre de l'equip amb nom assignat a tasques de projecte](media/RM-how-to-17.png)

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a><span data-ttu-id="a62ac-115">Complir un recurs genèric amb diversos recursos amb nom</span><span class="sxs-lookup"><span data-stu-id="a62ac-115">Fulfill a generic resource with multiple named resources</span></span>
<span data-ttu-id="a62ac-116">El compliment d'un requisit per a un recurs genèric amb diversos recursos amb nom és similar a l'assignació d'un recurs amb nom.</span><span class="sxs-lookup"><span data-stu-id="a62ac-116">Fulfilling a requirement for a generic resource with multiple named resources is similar to assigning a single named resource.</span></span> <span data-ttu-id="a62ac-117">Per exemple, hi ha una tasca amb una durada de cinc dies i 120 hores d'esforç.</span><span class="sxs-lookup"><span data-stu-id="a62ac-117">For example, there is a task with a duration of five days and 120 hours of effort.</span></span> <span data-ttu-id="a62ac-118">No es pot completar aquesta tasca amb un recurs que treballi un dia típic de vuit hores al llarg d'una setmana de cinc dies.</span><span class="sxs-lookup"><span data-stu-id="a62ac-118">This task can't be completed by one resource that works a typical eight-hour day over a five day week.</span></span> 

![Tasca que necessita 120 hores d'esforç durant cinc dies](media/RM-how-to-21.png)

<span data-ttu-id="a62ac-120">El requisit és de 120 hores d'enginyeria de robòtica al llarg de cinc dies, que és de 24 hores per dia.</span><span class="sxs-lookup"><span data-stu-id="a62ac-120">The requirement is for 120 hours of robotics engineering over five days, which is 24 hours per day.</span></span>

![Requisit per dia](media/RM-how-to-22.png)

<span data-ttu-id="a62ac-122">Aquest és un exemple de quan es necessiten diversos recursos amb nom per complir una sol·licitud de recurs genèrica.</span><span class="sxs-lookup"><span data-stu-id="a62ac-122">This is an example of when multiple named resources are needed to fulfill a generic resource request.</span></span> <span data-ttu-id="a62ac-123">Haureu de reservar diversos recursos per complir el requisit.</span><span class="sxs-lookup"><span data-stu-id="a62ac-123">You will need to book multiple resources to fulfill the requirement.</span></span>

![Reservar diversos recursos per complir el requisit](media/RM-how-to-23.png)

<span data-ttu-id="a62ac-125">La diferència principal en aquest escenari és que el recurs genèric es manté a l'equip assignat a la tasca i els membres de l'equip de recursos amb nom no s'assignen com a part del càrrec.</span><span class="sxs-lookup"><span data-stu-id="a62ac-125">The main difference in this scenario is that the generic resource remains on the team assigned to the task, and the booked named resource team members are not assigned as part of the position.</span></span> <span data-ttu-id="a62ac-126">L'administrador del projecte pot assignar la feina segons calgui als recursos amb nom.</span><span class="sxs-lookup"><span data-stu-id="a62ac-126">The project manager can assign the work as appropriate to the named resources.</span></span> <span data-ttu-id="a62ac-127">La visualització **Conciliació** pot ajudar a l'administrador del projecte a dividir les reserves entre diversos recursos a assignacions de tasques.</span><span class="sxs-lookup"><span data-stu-id="a62ac-127">The **Reconciliation** view can assist a project manager in breaking up the bookings across multiple resources to task assignments.</span></span> <span data-ttu-id="a62ac-128">Això no es fa de manera automàtica perquè en qualsevol escenari més complicat que l'anterior, com ara un on teniu un paquet de tasques que constitueixen el requisit, el sistema ha de suposar la intenció de com vol assignar-ho l'administrador del projecte.</span><span class="sxs-lookup"><span data-stu-id="a62ac-128">This is not done automatically because in any scenario more complicated than the simple example above, such as where you have a bundle of tasks making up the requirement, the intent of how the project manager wants to assign, needs to be assumed by the system.</span></span> <span data-ttu-id="a62ac-129">Com que el sistema no pot entendre la intenció, és probable que les hipòtesis siguin diferents del previst i que es produeixi un resultat incorrecte o impredictible.</span><span class="sxs-lookup"><span data-stu-id="a62ac-129">Because the system can't understand intent, chances are that the assumptions will be different than intended and an incorrect or unpredictable result will happen.</span></span> <span data-ttu-id="a62ac-130">El resultat predictible és que el recurs genèric es manté assignat fins que l'administrador del projecte crea deliberadament les assignacions amb l'ajuda de la visualització **Conciliació**.</span><span class="sxs-lookup"><span data-stu-id="a62ac-130">The predictable outcome is that the generic resource remains assigned until the project manager deliberately creates assignments, with the assistance of the **Reconciliation** view.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]