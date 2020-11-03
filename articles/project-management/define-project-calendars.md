---
title: Definició dels calendaris del projecte
description: En aquest tema es proporciona informació sobre l'ús d'un calendari de projecte per fer el seguiment de la planificació del projecte.
author: ruhercul
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 774399f2c02d8434c9c042c3a9f995792893bfce
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072386"
---
# <a name="define-project-calendars"></a><span data-ttu-id="ff2b2-103">Definició dels calendaris del projecte</span><span class="sxs-lookup"><span data-stu-id="ff2b2-103">Define project calendars</span></span>

<span data-ttu-id="ff2b2-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_</span><span class="sxs-lookup"><span data-stu-id="ff2b2-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ff2b2-105">Per crear una planificació de projecte, creeu uns plantilla de calendari de projecte que defineixi el nombre d'hores de treball al dia i qualsevol tancament de negoci.</span><span class="sxs-lookup"><span data-stu-id="ff2b2-105">To create a project schedule, you create a project calendar template that defines the number of working hours per day and any business closures.</span></span> <span data-ttu-id="ff2b2-106">Per crear una plantilla de calendari de projecte, associeu una plantilla de treball amb el camp **Plantilla de calendari** per al projecte.</span><span class="sxs-lookup"><span data-stu-id="ff2b2-106">To create a project calendar template, you associate a work template with the **Calendar template** field for the project.</span></span> <span data-ttu-id="ff2b2-107">Seguiu els passos que es descriuen a continuació per crear una plantilla de treball.</span><span class="sxs-lookup"><span data-stu-id="ff2b2-107">Follow these steps to create a work template.</span></span>

1. <span data-ttu-id="ff2b2-108">A la subfinestra de navegació esquerra, seleccioneu **Recursos**.</span><span class="sxs-lookup"><span data-stu-id="ff2b2-108">In the left navigation pane, select **Resources**.</span></span> 
2. <span data-ttu-id="ff2b2-109">A la pàgina de la llista **Recursos** , obriu un registre d'usuari i després seleccioneu **Mostra les hores de treball**.</span><span class="sxs-lookup"><span data-stu-id="ff2b2-109">On the **Resources** list page, open a user record, and then select **Show Work Hours**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="ff2b2-110">Assegureu-vos que permeteu les finestres emergents a la pàgina del navegador.</span><span class="sxs-lookup"><span data-stu-id="ff2b2-110">Make sure that you allow pop-ups on the browser page.</span></span> <span data-ttu-id="ff2b2-111">Això us permet veure les hores de feina definides per al recurs.</span><span class="sxs-lookup"><span data-stu-id="ff2b2-111">This lets you see the work hours set for the resource.</span></span>
  
3. <span data-ttu-id="ff2b2-112">A la pestanya **Visualització mensual** , seleccioneu **Configura**.</span><span class="sxs-lookup"><span data-stu-id="ff2b2-112">On the **Monthly View** tab, select **Set Up**.</span></span> <span data-ttu-id="ff2b2-113">Es mostra una llista de tres opcions:</span><span class="sxs-lookup"><span data-stu-id="ff2b2-113">A list of three options appears:</span></span> 

  - <span data-ttu-id="ff2b2-114">Planificació setmanal nova</span><span class="sxs-lookup"><span data-stu-id="ff2b2-114">New Weekly Schedule</span></span>
  - <span data-ttu-id="ff2b2-115">Planificació de treball per a un dia</span><span class="sxs-lookup"><span data-stu-id="ff2b2-115">Work Schedule for One Day</span></span>
  - <span data-ttu-id="ff2b2-116">Temps lliure</span><span class="sxs-lookup"><span data-stu-id="ff2b2-116">Time Off</span></span>

4. <span data-ttu-id="ff2b2-117">Seleccioneu **Planificació setmanal nova** i, a continuació, definiu les opcions d'aquesta planificació de recursos.</span><span class="sxs-lookup"><span data-stu-id="ff2b2-117">Select **New Weekly Schedule** , and then set the options for this resource schedule.</span></span> <span data-ttu-id="ff2b2-118">Podeu definir una planificació setmanal periòdica, paràmetres d'hores diàries, tancaments d'empresa, etc.</span><span class="sxs-lookup"><span data-stu-id="ff2b2-118">You can set a recurring weekly schedule, daily hour parameters, business closures, and more.</span></span>
5. <span data-ttu-id="ff2b2-119">Definiu l'interval de dates ,seleccioneu **Desa** i, a continuació, seleccioneu **Tanca**.</span><span class="sxs-lookup"><span data-stu-id="ff2b2-119">Set the date range, select **Save** , and then select **Close**.</span></span> 
6. <span data-ttu-id="ff2b2-120">Torneu a la pàgina de la llista **Recursos** i seleccioneu el recurs per al qual definiu les hores de feina.</span><span class="sxs-lookup"><span data-stu-id="ff2b2-120">Go back to the **Resources** list page, and select the resource that you set the work hours for.</span></span> 
7. <span data-ttu-id="ff2b2-121">Seleccioneu **Defineix el calendari com a** per definir la plantilla de treball.</span><span class="sxs-lookup"><span data-stu-id="ff2b2-121">Select **Set Calendar As** to set the work template.</span></span> 
8. <span data-ttu-id="ff2b2-122">Al quadre de diàleg **Plantilla de treball** introduïu el nom de la plantilla de treball i després seleccioneu **Aplica**.</span><span class="sxs-lookup"><span data-stu-id="ff2b2-122">In the **Work Template** dialog box, enter a name for the work template, and then select **Apply**.</span></span> 

<span data-ttu-id="ff2b2-123">Ara podeu associar la plantilla de treball amb una plantilla de calendari de projectes.</span><span class="sxs-lookup"><span data-stu-id="ff2b2-123">You can now associate the work template with a project calendar template.</span></span>
