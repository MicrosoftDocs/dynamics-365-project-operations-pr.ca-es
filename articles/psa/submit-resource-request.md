---
title: Enviar una sol·licitud de recurs
description: En aquest tema s'ofereix informació sobre la presentació d'una sol·licitud d'un recurs del projecte.
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/1/2018
ms.topic: article
author: JohnPBurrows
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
ms.openlocfilehash: bcea3d640d7e9ee2b071c55bff9ade3268edb319
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072305"
---
# <a name="submitting-a-resource-request"></a><span data-ttu-id="e7f43-103">Enviar una sol·licitud de recurs</span><span class="sxs-lookup"><span data-stu-id="e7f43-103">Submitting a resource request</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="e7f43-104">Podeu enviar una sol·licitud de recurs generat com a sol·licitud de recurs.</span><span class="sxs-lookup"><span data-stu-id="e7f43-104">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="e7f43-105">A continuació, la sol·licitud s'envia a un administrador de recursos perquè la compleixi.</span><span class="sxs-lookup"><span data-stu-id="e7f43-105">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="e7f43-106">Al Project Service Automation (PSA), a la pàgina **Projectes** , feu clic a la pestanya **Equip** per visualitzar una llista de recursos que es poden reservar.</span><span class="sxs-lookup"><span data-stu-id="e7f43-106">In Project Service Automation (PSA), on the **Projects** page, click the **Team** tab to view a list bookable resources.</span></span> 
2. <span data-ttu-id="e7f43-107">Seleccioneu el recurs genèric que té un requisit de recurs de la llista i, a continuació, feu clic a **Envia la sol·licitud**.</span><span class="sxs-lookup"><span data-stu-id="e7f43-107">Select the generic resource that has a resource requirement from the list and then click **Submit Request**.</span></span>

![Enviar una sol·licitud de recurs](media/RM-how-to-18.png)

<span data-ttu-id="e7f43-109">L'estat de sol·licitud del membre de l'equip genèric canviarà a **Enviada**.</span><span class="sxs-lookup"><span data-stu-id="e7f43-109">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="e7f43-110">Després que l'administrador de recursos hagi complert la sol·licitud, el recurs genèric se substituirà per un recurs anomenat si l'administrador de recursos compleix la sol·licitud amb la reserva d'un recurs amb nom.</span><span class="sxs-lookup"><span data-stu-id="e7f43-110">After the request is fulfilled by the resource manager, the generic resource will be replaced by a named resource if the resource manager fulfills the request with the booking of a named resource.</span></span> <span data-ttu-id="e7f43-111">Altrament, el recurs genèric romandrà a l'equip i l'estat de sol·licitud canviarà a **Necessita revisió** , si l'administrador de recursos ha proposat un recurs amb nom.</span><span class="sxs-lookup"><span data-stu-id="e7f43-111">Otherwise, the generic resource will remain on the team and the request status will change to **Needs Review** , if the resource manager has proposed a named resource.</span></span>
