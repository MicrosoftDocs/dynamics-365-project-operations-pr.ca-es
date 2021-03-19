---
title: Assignar recursos que es poden reservar genèrics a una tasca i equip de projecte
description: En aquest tema es proporciona informació sobre la reserva de recursos genèrics a tasques i equips de projecte.
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
ms.openlocfilehash: 5b4c47513b96310745fd2cdb296988a57df0e966
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291382"
---
# <a name="assign-generic-bookable-resources-to-a-task-and-generate-resource-requirements"></a><span data-ttu-id="d333a-103">Assignar recursos que es poden reservar genèrics i generar requisits de recursos</span><span class="sxs-lookup"><span data-stu-id="d333a-103">Assign generic bookable resources to a task and generate resource requirements</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="d333a-104">A més de reservar i assignar recursos reals al vostre projecte, podeu assignar recursos genèrics a tasques de projecte.</span><span class="sxs-lookup"><span data-stu-id="d333a-104">In addition to booking and assigning named or real resources to your project, you can assign generic resources to project tasks.</span></span> <span data-ttu-id="d333a-105">Aquests recursos poden servir com a contenidors per als recursos amb nom fins que estigueu a punt per assignar personal al vostre projecte amb recursos amb nom.</span><span class="sxs-lookup"><span data-stu-id="d333a-105">These resources can serve as placeholders for named resources until you are ready to staff your project with named resources.</span></span> 

1. <span data-ttu-id="d333a-106">Al Project Service Automation (PSA), obriu la pàgina **Projecte** i a la pestanya **Planificació**, introduïu el nom del càrrec del recurs genèric a la cel·la **Recurs** de la planificació.</span><span class="sxs-lookup"><span data-stu-id="d333a-106">In Project Service Automation (PSA), open the **Project** page and on the **Schedule** tab, enter the position name of the generic resource in the **Resource** cell of the schedule.</span></span> <span data-ttu-id="d333a-107">O bé, feu clic a la icona **Recurs** a la cel·la per obrir el selector de recursos i escriviu el nom del recurs genèric que voleu crear.</span><span class="sxs-lookup"><span data-stu-id="d333a-107">Or, click the **Resource** icon in the cell to open the resource picker and then enter the name of the generic resource that you want to create.</span></span>

![Creació i assignació d'un membre genèric de l'equip](media/RM-how-to-9.png)

<span data-ttu-id="d333a-109">S'obrirà la subfinestra **Creació ràpida: membre de l'equip del projecte**.</span><span class="sxs-lookup"><span data-stu-id="d333a-109">This will open the **Quick Create: Project Team Member** panel.</span></span> 

2. <span data-ttu-id="d333a-110">Introduïu la funció i unitat d'organització del membre de l'equip de recursos genèric i, a continuació, feu clic a **Desa**.</span><span class="sxs-lookup"><span data-stu-id="d333a-110">Enter the role and organization unit of the generic resource team member and then click **Save**.</span></span>

![Creació ràpida de membres de l'equip genèrics](media/RM-how-to-10.png)

3. <span data-ttu-id="d333a-112">Després d'haver creat el nou membre de l'equip de recursos genèric, s'assigna a la tasca.</span><span class="sxs-lookup"><span data-stu-id="d333a-112">After you have created the new generic resource team member, it is assigned to the task.</span></span> <span data-ttu-id="d333a-113">Podeu continuar assignant aquest recurs genèric a altres tasques de la planificació de la tasca.</span><span class="sxs-lookup"><span data-stu-id="d333a-113">You can continue to assign that generic resource to other tasks in the task schedule.</span></span>

![Assignar membres de l'equip genèrics existents a tasques](media/RM-how-to-11.png)

4. <span data-ttu-id="d333a-115">Després d'assignar el recurs genèric, podeu generar un requisit de recurs i complir-lo reservant-lo directament o presentant una sol·licitud de recursos a un administrador de recursos.</span><span class="sxs-lookup"><span data-stu-id="d333a-115">After you have assigned the generic resource, you can generate a resource requirement and fulfill it by directly booking or submitting a resource request to a resource manager.</span></span>

![Generar un requisit per a un membre genèric de l'equip](media/RM-how-to-12.png)

<span data-ttu-id="d333a-117">A la quadrícula de membres de l'equip, a més de poder utilitzar el selector de recursos com s'ha esmentat anteriorment, podeu afegir recursos genèrics directament.</span><span class="sxs-lookup"><span data-stu-id="d333a-117">On the team member grid, in addition to being able to use the resource picker as mentioned above, you can add generic resources directly.</span></span> <span data-ttu-id="d333a-118">Els recursos s'afegeixen amb un requisit de recurs que es basa en les dates d'inici/finalització i el mètode d'assignació especificat a la subfinestra **Creació ràpida: membre de l'equip del projecte**.</span><span class="sxs-lookup"><span data-stu-id="d333a-118">The resources are added with a resource requirement that is based on the start/end dates and allocation method specified in the **Quick Create: Project Team Member** panel.</span></span>

<span data-ttu-id="d333a-119">Podeu veure una diferència si afegiu directament el membre de l'equip genèric i, a continuació, assigneu més tasques al recurs genèric que les hores necessàries per cobrir.</span><span class="sxs-lookup"><span data-stu-id="d333a-119">You can see a difference if you add the generic team member directly and then assign more tasks to the generic resource than they have required hours to cover.</span></span> <span data-ttu-id="d333a-120">Feu clic a **Genera un requisit** per tornar a generar el requisit per equilibrar les hores necessàries contra assignacions.</span><span class="sxs-lookup"><span data-stu-id="d333a-120">Click **Generate Requirement** to regenerate the requirement to balance the required hours against assignments.</span></span>

<span data-ttu-id="d333a-121">També podeu fer clic a l'enllaç **Requisit de recursos** a la quadrícula de l'equip per obrir el requisit i afegir aptituds, recursos preferents, etc.</span><span class="sxs-lookup"><span data-stu-id="d333a-121">You can also click the **Resource requirement** link in the team grid to open the requirement and add skills, preferred resources, etc.</span></span>

![Requisit de recursos](media/RM-how-to-13.png)



[!INCLUDE[footer-include](../includes/footer-banner.md)]