---
title: Enviament d'una sol·licitud de recurs
description: Podeu enviar una sol·licitud de recurs generat com a sol·licitud de recurs. A continuació, la sol·licitud s'envia a un administrador de recursos perquè la compleixi.
author: ruhercul
ms.date: 10/04/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 6ac0044a27d1e506c9c62c477014017fd0ca06cb
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014014"
---
# <a name="submit-a-resource-request"></a><span data-ttu-id="ea1b3-104">Enviament d'una sol·licitud de recurs</span><span class="sxs-lookup"><span data-stu-id="ea1b3-104">Submit a resource request</span></span>

<span data-ttu-id="ea1b3-105">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_</span><span class="sxs-lookup"><span data-stu-id="ea1b3-105">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ea1b3-106">Podeu enviar una sol·licitud de recurs generat com a sol·licitud de recurs.</span><span class="sxs-lookup"><span data-stu-id="ea1b3-106">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="ea1b3-107">A continuació, la sol·licitud s'envia a un administrador de recursos perquè la compleixi.</span><span class="sxs-lookup"><span data-stu-id="ea1b3-107">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="ea1b3-108">Al Dynamics 365 Project Operations, a la pàgina **Projectes**, seleccioneu la pestanya **Equip** per visualitzar una llista de recursos que es poden reservar.</span><span class="sxs-lookup"><span data-stu-id="ea1b3-108">In Dynamics 365 Project Operations, on the **Projects** page, select the **Team** tab to view a list of bookable resources.</span></span> 
2. <span data-ttu-id="ea1b3-109">Seleccioneu el recurs genèric que té un requisit de recurs de la llista i, a continuació, feu clic a **Envia la sol·licitud**.</span><span class="sxs-lookup"><span data-stu-id="ea1b3-109">Select the generic resource that has a resource requirement from the list, and then click **Submit Request**.</span></span>

<span data-ttu-id="ea1b3-110">L'estat de sol·licitud del membre de l'equip genèric canviarà a **Enviada**.</span><span class="sxs-lookup"><span data-stu-id="ea1b3-110">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="ea1b3-111">Quan s'hagi complert la sol·licitud, el recurs genèric se substituirà per un recurs anomenat si l'administrador de recursos compleix la sol·licitud amb la reserva d'un recurs amb nom.</span><span class="sxs-lookup"><span data-stu-id="ea1b3-111">After the request is fulfilled, the generic resource is replaced by a named resource if the resource manager fulfills the request by booking a named resource.</span></span> <span data-ttu-id="ea1b3-112">Altrament, el recurs genèric romandrà a l'equip i l'estat de sol·licitud canviarà a **Necessita revisió**, si l'administrador de recursos ha proposat un recurs amb nom.</span><span class="sxs-lookup"><span data-stu-id="ea1b3-112">Otherwise, if the resource manager proposes a named resource, the generic resource remains on the team and the request status will change to **Needs Review**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]