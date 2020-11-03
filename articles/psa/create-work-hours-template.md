---
title: Crear una plantilla d'hores de treball
description: Com crear una plantilla d'hores de treball al Project Service
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: c34634817fc8e4c993261024a8b19d45052bf5e5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072222"
---
# <a name="create-a-work-hours-template-project-service"></a><span data-ttu-id="b3c5e-103">Crear una plantilla d'hores de treball (Project Service)</span><span class="sxs-lookup"><span data-stu-id="b3c5e-103">Create a work hours template (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="b3c5e-104">Abans de crear planificacions de projecte, heu de configurar un calendari de projecte que defineixi el nombre d'hores de treball que es poden assignar al dia a la planificació i qualsevol tancament de negoci.</span><span class="sxs-lookup"><span data-stu-id="b3c5e-104">Before you can create project schedules, you need to set up a project calendar that defines the number of working hours to accommodate per day in the schedule and any business closures.</span></span> <span data-ttu-id="b3c5e-105">Per fer-ho heu d'utilitzar una plantilla de hores de treball, que conté detalls sobre les hores diàries de feina, els dies de festa i qualsevol dia de tancament de l'empresa.</span><span class="sxs-lookup"><span data-stu-id="b3c5e-105">You do this with a work hours template, which contains details about work hours per day, days off, and any other business closures.</span></span>  
  
 <span data-ttu-id="b3c5e-106">Quan creeu un projecte, heu d'associar una plantilla de treball al calendari del projecte per aplicar la planificació per al projecte.</span><span class="sxs-lookup"><span data-stu-id="b3c5e-106">When you’re creating a project, you associate a work template to the project calendar to apply the schedule for the project.</span></span>  
  
 <span data-ttu-id="b3c5e-107">Hi ha dues maneres de crear una plantilla d'hores de treball:</span><span class="sxs-lookup"><span data-stu-id="b3c5e-107">There are two ways you can create a work hours template:</span></span>  
  
-   <span data-ttu-id="b3c5e-108">Crear una plantilla d'hores de treball basada en un calendari de recurs.</span><span class="sxs-lookup"><span data-stu-id="b3c5e-108">Create a work hours template based on a resource’s calendar.</span></span>  
  
-   <span data-ttu-id="b3c5e-109">Crear una nova plantilla d'hores de treball.</span><span class="sxs-lookup"><span data-stu-id="b3c5e-109">Create a new work hours template.</span></span>  
  
#### <a name="to-create-a-work-hours-template-based-on-a-resources-calendar"></a><span data-ttu-id="b3c5e-110">Per crear una plantilla d'hores de treball basada en un calendari de recurs</span><span class="sxs-lookup"><span data-stu-id="b3c5e-110">To create a work hours template based on a resource’s calendar</span></span>  
  
1.  <span data-ttu-id="b3c5e-111">Aneu a **Project Service > Recursos**.</span><span class="sxs-lookup"><span data-stu-id="b3c5e-111">Go to **Project Service > Resources**.</span></span>  
  
2.  <span data-ttu-id="b3c5e-112">Seleccioneu el recurs en el qual voleu basar el vostre horari de treball.</span><span class="sxs-lookup"><span data-stu-id="b3c5e-112">Select the resource you want to base your work hours on.</span></span>  
  
3.  <span data-ttu-id="b3c5e-113">Feu clic a **Anomena i desa calendari** , introduïu un nom per a la plantilla d'hores de treball i feu clic a **Desa**.</span><span class="sxs-lookup"><span data-stu-id="b3c5e-113">Click **Save Calendar As** , enter a name for the work hours template, and then click **Save**.</span></span>  
  
4.  <span data-ttu-id="b3c5e-114">Quan acabeu de canviar les opcions, feu clic a **Desa i tanca**.</span><span class="sxs-lookup"><span data-stu-id="b3c5e-114">When you’re done changing options, click **Save and Close**.</span></span>  
  
5.  <span data-ttu-id="b3c5e-115">Feu clic al botó **Desa** a la cantonada inferior dreta de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="b3c5e-115">Click the **Save** button at the bottom right corner of the screen.</span></span>  
  
#### <a name="to-create-a-new-work-hours-template"></a><span data-ttu-id="b3c5e-116">Per crear una nova plantilla d'hores de treball</span><span class="sxs-lookup"><span data-stu-id="b3c5e-116">To create a new work hours template</span></span>  
  
1.  <span data-ttu-id="b3c5e-117">Aneu a **Project Service > Plantilles d'hores de treball**.</span><span class="sxs-lookup"><span data-stu-id="b3c5e-117">Go to **Project Service > Work Hours Templates**.</span></span>  
  
2.  <span data-ttu-id="b3c5e-118">Feu clic a **Nou**.</span><span class="sxs-lookup"><span data-stu-id="b3c5e-118">Click **New**.</span></span>  
  
3.  <span data-ttu-id="b3c5e-119">Introduïu un nom per a la plantilla d'hores de treball.</span><span class="sxs-lookup"><span data-stu-id="b3c5e-119">Enter a name for the work hours template.</span></span>  
  
4.  <span data-ttu-id="b3c5e-120">Seleccioneu un recurs en el qual es basaran les hores de treball i, a continuació, feu clic a **Desa**.</span><span class="sxs-lookup"><span data-stu-id="b3c5e-120">Select a resource to base the work hours on, and then click **Save**.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="b3c5e-121">Vegeu també</span><span class="sxs-lookup"><span data-stu-id="b3c5e-121">See Also</span></span>  
 [<span data-ttu-id="b3c5e-122">Definir recursos</span><span class="sxs-lookup"><span data-stu-id="b3c5e-122">Set up resources</span></span>](../psa/set-up-resources.md)
