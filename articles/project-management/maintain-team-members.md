---
title: Manteniment dels membres de l'equip
description: En aquest tema es proporciona informació sobre la reserva de recursos amb nom a equips de projecte i assignar-los a tasques.
author: ruhercul
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: f5b36628e90896c9fe6570de71c95eab83a44ebd
ms.sourcegitcommit: 396e0fea2f1598a5313cb0128eca4fe0bb5aade9
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961821"
---
# <a name="maintain-team-members"></a><span data-ttu-id="71fab-103">Manteniment dels membres de l'equip</span><span class="sxs-lookup"><span data-stu-id="71fab-103">Maintain team members</span></span>

<span data-ttu-id="71fab-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_</span><span class="sxs-lookup"><span data-stu-id="71fab-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="71fab-105">Podeu afegir un recurs amb nom a l'equip del projecte reservant-lo directament a l'equip.</span><span class="sxs-lookup"><span data-stu-id="71fab-105">You can add a named resource to your project team by booking them directly to the team.</span></span>

1. <span data-ttu-id="71fab-106">Al Dynamics 365 Project Operations, aneu a **Projectes**i, a continuació, seleccioneu el projecte obert al qual voleu reservar.</span><span class="sxs-lookup"><span data-stu-id="71fab-106">In Dynamics 365 Project Operations, go to **Projects**, and select the open the project that you're booking for.</span></span>
2. <span data-ttu-id="71fab-107">A la pàgina **Projecte**, a la pestanya **Equip**, seleccioneu **Nou**.</span><span class="sxs-lookup"><span data-stu-id="71fab-107">On the **Project** page, on the **Team** tab, select **New**.</span></span> 
3. <span data-ttu-id="71fab-108">Al quadre de diàleg **Creació ràpida de membre de l'equip**, seleccioneu el recurs que es pot reservar.</span><span class="sxs-lookup"><span data-stu-id="71fab-108">In the **Quick Create Project Team Member** dialog box, select the bookable resource.</span></span> <span data-ttu-id="71fab-109">El camp **Funció** s'emplenarà amb la funció per defecte del recurs si en té assignada una.</span><span class="sxs-lookup"><span data-stu-id="71fab-109">The **Role** field will populate with the resource's default role if they have one assigned.</span></span> <span data-ttu-id="71fab-110">Podeu canviar la funció.</span><span class="sxs-lookup"><span data-stu-id="71fab-110">You can change the role.</span></span> 
4. <span data-ttu-id="71fab-111">Seleccioneu les dates d'origen i finalització en què es necessitaran els recursos i seleccioneu el mètode d'assignació de la capacitat del recurs.</span><span class="sxs-lookup"><span data-stu-id="71fab-111">Select the from and to dates that the resource will be needed, and select the allocation method of the resource's capacity.</span></span> 
5. <span data-ttu-id="71fab-112">Si voleu que el membre de l'equip sigui un aprovador de projecte, seleccioneu **Sí** al camp **Aprovador de projectes**.</span><span class="sxs-lookup"><span data-stu-id="71fab-112">In the **Project Approver** field, select **Yes** if you want the team member to be a project approver.</span></span> <span data-ttu-id="71fab-113">El membre de l'equip pot aprovar les entrades de despesa i de despeses enviades per a aquest projecte.</span><span class="sxs-lookup"><span data-stu-id="71fab-113">The team member can approve submitted time and expense entries for this project.</span></span> 
6. <span data-ttu-id="71fab-114">Seleccioneu **Desa**.</span><span class="sxs-lookup"><span data-stu-id="71fab-114">Select **Save**.</span></span>

<span data-ttu-id="71fab-115">Ara podeu assignar el recurs reservat a les tasques del projecte.</span><span class="sxs-lookup"><span data-stu-id="71fab-115">You can now assign the booked resource to tasks on the project.</span></span> <span data-ttu-id="71fab-116">A la pàgina **Projecte**, a la pestanya **Planificació**, assigneu tasques al recurs nou.</span><span class="sxs-lookup"><span data-stu-id="71fab-116">On the **Project** page, on the **Schedule** tab, assign tasks to the new resource.</span></span> <span data-ttu-id="71fab-117">El selector de recursos que s'inicia des del camp **Recursos** de la quadrícula de tasques mostrarà els membres de l'equip que podeu seleccionar.</span><span class="sxs-lookup"><span data-stu-id="71fab-117">The resource picker that is launched from the **Resources** field in the task grid will show the team members that you can select.</span></span>


<span data-ttu-id="71fab-118">Al Project Operations, les reserves de recursos i assignacions de tasques no es vinculen estretament.</span><span class="sxs-lookup"><span data-stu-id="71fab-118">In Project Operations, resource bookings and task assignments aren't tightly coupled.</span></span> <span data-ttu-id="71fab-119">Quan utilitzeu el selector de recursos de la planificació, podeu assignar tasques als membres de l'equip durant més hores de les cobertes per les reserves en el projecte.</span><span class="sxs-lookup"><span data-stu-id="71fab-119">When you use the resource picker in the schedule, you can assign tasks to team members for more hours than their bookings cover on the project.</span></span>

<span data-ttu-id="71fab-120">Les diferències entre les reserves dels membres de l'equip i les assignacions es mostren a les pestanyes **Equip** i **Conciliació de recursos**.</span><span class="sxs-lookup"><span data-stu-id="71fab-120">The differences between team member bookings and assignments are shown on the **Team** and **Resource Reconciliation** tabs.</span></span> <span data-ttu-id="71fab-121">També podeu conciliar les diferències entre reserves i tasques per als recursos en un nivell més detallat.</span><span class="sxs-lookup"><span data-stu-id="71fab-121">You can also reconcile the differences between bookings and assignments for resources at a more detailed level.</span></span>

<span data-ttu-id="71fab-122">Utilitzeu el selector de recursos a la pestanya **Planificació** per cercar i seleccionar altres recursos que encara no formen part de l'equip del projecte.</span><span class="sxs-lookup"><span data-stu-id="71fab-122">Use the resource picker on the **Schedule** tab to search for and select bookable resources that are not already part of the project team.</span></span> <span data-ttu-id="71fab-123">Aquests recursos es mostren al selector de recursos com a **Altres recursos**.</span><span class="sxs-lookup"><span data-stu-id="71fab-123">These resources are shown in the resource picker as **Other Resources**.</span></span>

<span data-ttu-id="71fab-124">En fer una selecció, el recurs s'afegeix a l'equip del projecte i se l'assigna a la tasca, però no es genera cap reserva.</span><span class="sxs-lookup"><span data-stu-id="71fab-124">When you make a selection, the resource is added to the project team and assigned to the task, but no bookings are generated.</span></span>

<span data-ttu-id="71fab-125">Podeu utilitzar la capacitat d'ampliació de la reserva de la pestanya **Conciliació** o el **Tauler de planificació** per reservar la capacitat del recurs al projecte.</span><span class="sxs-lookup"><span data-stu-id="71fab-125">You can use the **Reconciliation** tab’s extend booking capability or the **Schedule Board** to book the resource’s capacity to the project.</span></span>

<span data-ttu-id="71fab-126">Després d'haver reservat un membre de l'equip al vostre projecte, podeu utilitzar **Mantén les reserves** o el **Tauler de planificació** directament per administrar les seves reserves.</span><span class="sxs-lookup"><span data-stu-id="71fab-126">After a team member is booked on your project, you can use **Maintain bookings** or the **Schedule Board** directly to manage their bookings.</span></span>
