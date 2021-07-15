---
title: Informació general sobre l'ús de recursos
description: En aquest tema es proporciona informació sobre l'ús dels recursos al Project Operations.
author: ruhercul
ms.date: 11/05/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.custom: intro-internal
ms.openlocfilehash: c9464b1de87211f8317a39a1d749e619769309ae
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 07/07/2021
ms.locfileid: "6367924"
---
# <a name="resource-utilization-overview"></a><span data-ttu-id="433ee-103">Informació general sobre l'ús de recursos</span><span class="sxs-lookup"><span data-stu-id="433ee-103">Resource utilization overview</span></span>

<span data-ttu-id="433ee-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_</span><span class="sxs-lookup"><span data-stu-id="433ee-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="433ee-105">Els recursos poden tenir un objectiu d'ús facturable.</span><span class="sxs-lookup"><span data-stu-id="433ee-105">Resources can have a target billable utilization.</span></span> <span data-ttu-id="433ee-106">Aquest objectiu d'ús es defineix com un atribut de la funció per defecte d'un recurs o es defineix al registre del recurs individual que es pot reservar.</span><span class="sxs-lookup"><span data-stu-id="433ee-106">This target utilization is defined as an attribute on a resource's default role or set on the record of the individual bookable resource.</span></span> <span data-ttu-id="433ee-107">Els càlculs d'ús es basen en les hores reals que els recursos han informat mitjançant les entrades de temps aprovades.</span><span class="sxs-lookup"><span data-stu-id="433ee-107">Utilization calculations are based on the actual hours that resources have reported by using approved time entries.</span></span>

<span data-ttu-id="433ee-108">Les següents fórmules s'utilitzen per calcular l'ús:</span><span class="sxs-lookup"><span data-stu-id="433ee-108">The following formulas are used to calculate utilization:</span></span>

  - <span data-ttu-id="433ee-109">Ús facturable = Hores reals imputables ÷ Capacitat de recursos</span><span class="sxs-lookup"><span data-stu-id="433ee-109">Billable utilization = Chargeable actual hours ÷ Resource capacity</span></span>
  - <span data-ttu-id="433ee-110">Ús no facturable = Temps real amb ID de tipus de facturació = No imputable, Gratuït o No disponible ÷ Capacitat de recursos</span><span class="sxs-lookup"><span data-stu-id="433ee-110">Non-billable utilization = Actual time with billing type ID = Non-chargeable, Complementary, or Not available ÷ Resource capacity</span></span>
  - <span data-ttu-id="433ee-111">Intern = Temps real sense contracte de vendes ÷ Capacitat de recursos</span><span class="sxs-lookup"><span data-stu-id="433ee-111">Internal = Actual time with no sales contract ÷ Resource capacity</span></span>
  - <span data-ttu-id="433ee-112">Capacitat de recursos = Hores de treball - Fora de l'oficina - Dies no hàbils</span><span class="sxs-lookup"><span data-stu-id="433ee-112">Resource capacity = Resource work hours – Out-of-office – Non-working days</span></span>

<span data-ttu-id="433ee-113">Podeu cercar la visualització **Ús de recursos** a la subfinestra **Recursos**.</span><span class="sxs-lookup"><span data-stu-id="433ee-113">You can find the **Resource Utilization** view in the **Resources** pane.</span></span>

<span data-ttu-id="433ee-114">Cada cel·la de la quadrícula representa el percentatge d'ús facturable del recurs en un període, com ara un dia, una setmana o un mes.</span><span class="sxs-lookup"><span data-stu-id="433ee-114">Each cell in the grid represents the billable utilization percentage of the resource in a period, such as a day, week, or month.</span></span> <span data-ttu-id="433ee-115">Les següents fórmules s'utilitzen per acolorir les cel·les:</span><span class="sxs-lookup"><span data-stu-id="433ee-115">The following formulas are used to color the cells:</span></span>

  - <span data-ttu-id="433ee-116">**Verd**: ús facturable> = ús objectiu dels recursos</span><span class="sxs-lookup"><span data-stu-id="433ee-116">**Green**: Billable utilization >= Resource target utilization</span></span>
  - <span data-ttu-id="433ee-117">**Groc**: ús objectiu - 20 <= ús facturable < ús objectiu</span><span class="sxs-lookup"><span data-stu-id="433ee-117">**Yellow**: Target utilization – 20 <= Billable utilization < Target utilization</span></span>
  - <span data-ttu-id="433ee-118">**Vermell**: ús facturable < ús de l'objectiu - 20</span><span class="sxs-lookup"><span data-stu-id="433ee-118">**Red**: Billable utilization < Target utilization – 20</span></span>

<span data-ttu-id="433ee-119">Com que la visualització **Ús de recursos** està basada en el tauler de planificació, podeu utilitzar les capacitats de filtratge del tauler de planificació per filtrar els resultats.</span><span class="sxs-lookup"><span data-stu-id="433ee-119">Because the **Resource Utilization** view is based on the Schedule Board, you can use the filtering capabilities of the Schedule Board to filter your results.</span></span>

<span data-ttu-id="433ee-120">La quadrícula requereix que definiu un objectiu d'ús en la funció o en el recurs individual.</span><span class="sxs-lookup"><span data-stu-id="433ee-120">The grid requires that you set a target utilization on either the role or the individual resource.</span></span> <span data-ttu-id="433ee-121">Per configurar-ho, aneu a **Recursos** > **Funcions de recurs**.</span><span class="sxs-lookup"><span data-stu-id="433ee-121">To do this setup, go to **Resources** > **Resource roles**.</span></span>

<span data-ttu-id="433ee-122">A més, cal assignar una funció per defecte a cadascun dels recursos que es pot reservar.</span><span class="sxs-lookup"><span data-stu-id="433ee-122">Additionally, a default role must be assigned to each bookable resource.</span></span> <span data-ttu-id="433ee-123">Aneu a **Recursos** > **Recursos**.</span><span class="sxs-lookup"><span data-stu-id="433ee-123">Go to **Resources** > **Resources**.</span></span> <span data-ttu-id="433ee-124">A la pestanya **Project Service**, comproveu que es defineix una funció de recurs i que el camp **Per defecte** està definit com a **Sí**.</span><span class="sxs-lookup"><span data-stu-id="433ee-124">On the **Project Service** tab, verify that a resource role is defined, and that the **Is Default** field is set to **Yes**.</span></span> <span data-ttu-id="433ee-125">Podeu afegir funcions addicionals on **Per defecte** = **No**.</span><span class="sxs-lookup"><span data-stu-id="433ee-125">You can add additional roles where **Is Default** = **No**.</span></span> <span data-ttu-id="433ee-126">La funció on **Per defecte** = **Sí** s'utilitza per avaluar l'ús del recurs en relació amb l'objectiu per a aquesta funció.</span><span class="sxs-lookup"><span data-stu-id="433ee-126">The role where the **Is Default** = **Yes** is used to evaluate the resource's utilization against the target for that role.</span></span>

<span data-ttu-id="433ee-127">A la pestanya **Project Service** també podeu definir un objectiu d'ús individual per al recurs.</span><span class="sxs-lookup"><span data-stu-id="433ee-127">On the **Project Service** tab, you can also set an individual target utilization for the resource.</span></span> <span data-ttu-id="433ee-128">A continuació, el càlcul d'ús utilitza l'objectiu d'ús per avaluar l'objectiu del recurs en comptes de l'objectiu de la funció per defecte del recurs.</span><span class="sxs-lookup"><span data-stu-id="433ee-128">The utilization calculation then uses that target utilization to evaluate the resource's target instead of the target of the resource's default role.</span></span>

<span data-ttu-id="433ee-129">L'ús es mostra només per a un recurs si aquest recurs té temps aprovat imputable durant el període que es mostra a la quadrícula.</span><span class="sxs-lookup"><span data-stu-id="433ee-129">Utilization is only shown for a resource if that resource has approved, chargeable time during the period shown in the grid.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]