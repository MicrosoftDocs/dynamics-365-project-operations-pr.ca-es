---
title: Seguiment de l'estat d'un projecte
description: Com fer un seguiment de l'estat d'un projecte al Project Service
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: d57f33cdf240db4cae1f33fe962173790fe0fe7f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5281916"
---
# <a name="track-a-projects-status-project-service"></a><span data-ttu-id="6e606-103">Seguiment de l'estat d'un projecte (Project Service)</span><span class="sxs-lookup"><span data-stu-id="6e606-103">Track a project’s status (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="6e606-104">Utilitzeu l'[!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] per fer el seguiment del progrés del projecte d'un client.</span><span class="sxs-lookup"><span data-stu-id="6e606-104">Use the [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] to track the progress of a client’s project.</span></span>  

<span data-ttu-id="6e606-105">A mesura que la participació avança, les fases del projecte s'actualitzen per reflectir la fase de la participació:</span><span class="sxs-lookup"><span data-stu-id="6e606-105">As the engagement progresses, the project stages update to reflect the stage of the engagement:</span></span>  


|              |                                                                                                                                                                                                                                                                                                  |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   <span data-ttu-id="6e606-106">**Crea**</span><span class="sxs-lookup"><span data-stu-id="6e606-106">**New**</span></span>    | <span data-ttu-id="6e606-107">Quan creeu un projecte, la fase es defineix a **Nou**.</span><span class="sxs-lookup"><span data-stu-id="6e606-107">When you create a project, the stage is set to **New**.</span></span> <span data-ttu-id="6e606-108">Si heu creat el projecte des d'una plantilla, en aquesta fase el projecte pot tenir una planificació, estimacions i dades d'equip.</span><span class="sxs-lookup"><span data-stu-id="6e606-108">If you created the project from a template, at this stage the project may have a schedule, estimates, and team data.</span></span> <span data-ttu-id="6e606-109">En cas contrari, serà l'esquema del projecte i haureu d'introduir manualment la resta de components del projecte.</span><span class="sxs-lookup"><span data-stu-id="6e606-109">Otherwise, it will be the outline of the project and you need to manually enter the rest of the project components.</span></span> |
|  <span data-ttu-id="6e606-110">**Oferta**</span><span class="sxs-lookup"><span data-stu-id="6e606-110">**Quote**</span></span>   |      <span data-ttu-id="6e606-111">Quan associeu un projecte a una oferta o el creeu a partir d'una oferta, la fase de projecte es defineix com a **Oferta** i les dates d'inici i finalització previstes també s'actualitzen.</span><span class="sxs-lookup"><span data-stu-id="6e606-111">When you associate a project to a quote or create it from a quote, the project stage is set to **Quote**, and the estimated start and end datesare updated as well.</span></span> <span data-ttu-id="6e606-112">Quan el projecte està en la fase d'oferta, els detalls de l'oferta es visualitzen a la pestanya **Vendes** de la pàgina **Projecte**.</span><span class="sxs-lookup"><span data-stu-id="6e606-112">When the project is in the quote stage, details on the quote display on the **Sales** tab on the **Project** page.</span></span>      |
|   <span data-ttu-id="6e606-113">**Pla**</span><span class="sxs-lookup"><span data-stu-id="6e606-113">**Plan**</span></span>   |                                     <span data-ttu-id="6e606-114">Quan guanyeu una oferta associada amb un projecte, i quan la participació avança a la fase de contracte, la fase de projecte s'actualitza a **Pla**.</span><span class="sxs-lookup"><span data-stu-id="6e606-114">When you win a quote associated with a project, and when the engagement progresses to the contract stage, the project stage updates to **Plan**.</span></span> <span data-ttu-id="6e606-115">Els detalls del contracte es visualitzen a la pestanya **Vendes** de la pàgina **Projecte**.</span><span class="sxs-lookup"><span data-stu-id="6e606-115">Contract details display on the **Sales** tab on the **Project** page.</span></span>                                      |
| <span data-ttu-id="6e606-116">**Complet**</span><span class="sxs-lookup"><span data-stu-id="6e606-116">**Complete**</span></span> |                    <span data-ttu-id="6e606-117">Quan la feina del projecte finalitza, podeu canviar la fase a **Completat**.</span><span class="sxs-lookup"><span data-stu-id="6e606-117">When the project work is complete, you can flip the stage to **Complete**.</span></span> <span data-ttu-id="6e606-118">Quan la fase del projecte es defineix com a completada, se suposa que el treball està 100 % completat, però el projecte es manté obert per a qualsevol entrada de temps o despesa pendent que calgui registrar.</span><span class="sxs-lookup"><span data-stu-id="6e606-118">When the project stage is set to complete, it’s understood that the work is 100% complete but the project is kept open for any pending time or expense entries to be recorded.</span></span>                     |
|  <span data-ttu-id="6e606-119">**Tanca**</span><span class="sxs-lookup"><span data-stu-id="6e606-119">**Close**</span></span>   |           <span data-ttu-id="6e606-120">Quan totes les transaccions s'han registrat en el projecte i no teniu previst que se'n registri cap més, podeu definir manualment la fase com a **Tancament**.</span><span class="sxs-lookup"><span data-stu-id="6e606-120">When all transactions have been recorded on the project and you don't expect any more to be logged, you can manually set the stage to **Close**.</span></span> <span data-ttu-id="6e606-121">Quan el projecte es defineix com a **Tancament**, no podreu registrar cap transacció més al projecte i el projecte passarà a ser de només de lectura.</span><span class="sxs-lookup"><span data-stu-id="6e606-121">When the project is set to **Close**, you can’t log any more transactions on the project and the project will be read only.</span></span>           |

## <a name="to-track-a-projects-status"></a><span data-ttu-id="6e606-122">Per fer el seguiment de l'estat d'un projecte</span><span class="sxs-lookup"><span data-stu-id="6e606-122">To track a project’s status</span></span>  

1.  <span data-ttu-id="6e606-123">Aneu a **Project Service > Projectes**.</span><span class="sxs-lookup"><span data-stu-id="6e606-123">Go to **Project Service > Projects**.</span></span>  

2.  <span data-ttu-id="6e606-124">Feu clic al projecte en el qual voleu treballant.</span><span class="sxs-lookup"><span data-stu-id="6e606-124">Click the project you want to work on.</span></span>  

3.  <span data-ttu-id="6e606-125">A la barra que hi ha a la part superior de la pantalla, seleccioneu la fletxa avall al costat del nom de projecte i, a continuació, feu clic a **Seguiment del projecte**.</span><span class="sxs-lookup"><span data-stu-id="6e606-125">In the bar across the top of the screen, select the down arrow next to the project name, and then click **Project Tracking**.</span></span>  

4.  <span data-ttu-id="6e606-126">Seleccioneu **Seguiment de l'esforç** o **Seguiment del cost** a la llista desplegable situada a la part superior de la llista de tasques.</span><span class="sxs-lookup"><span data-stu-id="6e606-126">Select **Effort Tracking** or **Cost Tracking** in the drop-down list above the task list.</span></span>  

5.  <span data-ttu-id="6e606-127">Feu doble clic a qualsevol tasca per editar-la.</span><span class="sxs-lookup"><span data-stu-id="6e606-127">Double-click any task to edit it.</span></span> <span data-ttu-id="6e606-128">També podeu moure o canviar de mida de les barres del gràfic de Gantt per canviar el temps i el progrés d'una tasca.</span><span class="sxs-lookup"><span data-stu-id="6e606-128">You can also move or resize the bars in the Gantt chart to change the time and progress for a task.</span></span>  

### <a name="see-also"></a><span data-ttu-id="6e606-129">Vegeu també</span><span class="sxs-lookup"><span data-stu-id="6e606-129">See Also</span></span>  
 [<span data-ttu-id="6e606-130">Guia d'administrador de projectes</span><span class="sxs-lookup"><span data-stu-id="6e606-130">Project Manager Guide</span></span>](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]