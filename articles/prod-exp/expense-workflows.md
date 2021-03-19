---
title: Configurar els fluxos de treball d'administració de despeses
description: Podeu configurar un procés de flux de treball per revisar i aprovar els documents de viatges i de despeses.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 36ab1edc4769013684fa9248e6c5eac025637bbd
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271611"
---
# <a name="set-up-expense-management-workflows"></a><span data-ttu-id="6a2b3-103">Configurar els fluxos de treball d'administració de despeses</span><span class="sxs-lookup"><span data-stu-id="6a2b3-103">Set up Expense management workflows</span></span>

<span data-ttu-id="6a2b3-104">Podeu configurar un procés de flux de treball que s'utilitzi per revisar i aprovar els documents de viatges i de despeses.</span><span class="sxs-lookup"><span data-stu-id="6a2b3-104">You can set up a workflow process that is used to review and approve travel and expense documents.</span></span> <span data-ttu-id="6a2b3-105">Els documents per als quals es poden definir fluxos de treball inclouen informes de despeses, peticions de viatges i sol·licituds d'avançament d'efectiu.</span><span class="sxs-lookup"><span data-stu-id="6a2b3-105">The documents for which workflows can be defined include expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="6a2b3-106">Un flux de treball representa un procés de negoci.</span><span class="sxs-lookup"><span data-stu-id="6a2b3-106">A workflow represents a business process.</span></span> <span data-ttu-id="6a2b3-107">Defineix com passa un document pel sistema i indica qui ha de completar una tasca o aprovar un document.</span><span class="sxs-lookup"><span data-stu-id="6a2b3-107">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="6a2b3-108">Hi ha diversos avantatges d'utilitzar el sistema de flux de treball a l'organització:</span><span class="sxs-lookup"><span data-stu-id="6a2b3-108">There are several benefits of using the workflow system in your organization:</span></span>

-   <span data-ttu-id="6a2b3-109">**Processos coherents**: podeu definir el procés d'aprovació per a documents específics, com ara les requisicions de compra i els informes de despeses.</span><span class="sxs-lookup"><span data-stu-id="6a2b3-109">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="6a2b3-110">L'ús del sistema de flux de treball ajuda a garantir que els documents es processen i s'aproven de manera coherent i eficient.</span><span class="sxs-lookup"><span data-stu-id="6a2b3-110">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>

-   <span data-ttu-id="6a2b3-111">Visibilitat de procés: podeu fer el seguiment de l'estat, de l'historial i de les mètriques de rendiment d'una instància de flux de treball concreta.</span><span class="sxs-lookup"><span data-stu-id="6a2b3-111">Process visibility — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="6a2b3-112">Això us ajudarà a determinar si s'han de fer canvis al flux de treball per millorar l'eficiència.</span><span class="sxs-lookup"><span data-stu-id="6a2b3-112">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>

-   <span data-ttu-id="6a2b3-113">Llista de treball centralitzada: els usuaris poden visualitzar una llista de treball centralitzada per visualitzar les tasques del flux de treball i les aprovacions assignades.</span><span class="sxs-lookup"><span data-stu-id="6a2b3-113">Centralized work list — Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

<span data-ttu-id="6a2b3-114">**Tipus de fluxos de treball que podeu crear**</span><span class="sxs-lookup"><span data-stu-id="6a2b3-114">**The types of workflows you can create**</span></span>

<span data-ttu-id="6a2b3-115">A la taula següent s'enumeren els tipus de fluxos de treball que es poden crear a **Despesa**.</span><span class="sxs-lookup"><span data-stu-id="6a2b3-115">The following table lists the types of workflows that you can create in **Expense**.</span></span>


|              <span data-ttu-id="6a2b3-116"><strong>Tipus</strong></span><span class="sxs-lookup"><span data-stu-id="6a2b3-116"><strong>Type</strong></span></span>              |                   <span data-ttu-id="6a2b3-117"><strong>Utilitzeu aquest tipus per</strong></span><span class="sxs-lookup"><span data-stu-id="6a2b3-117"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|         <span data-ttu-id="6a2b3-118"><strong>Informe de despeses</strong></span><span class="sxs-lookup"><span data-stu-id="6a2b3-118"><strong>Expense report</strong></span></span>         |            <span data-ttu-id="6a2b3-119">Crear fluxos de treball d'aprovació per a informes de despeses.</span><span class="sxs-lookup"><span data-stu-id="6a2b3-119">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="6a2b3-120"><strong>Publicació automàtica d'informes de despeses</strong></span><span class="sxs-lookup"><span data-stu-id="6a2b3-120"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="6a2b3-121">Crear fluxos de treball de publicació automàtica per a informes de despeses.</span><span class="sxs-lookup"><span data-stu-id="6a2b3-121">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="6a2b3-122"><strong>Element de línia de despesa</strong></span><span class="sxs-lookup"><span data-stu-id="6a2b3-122"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="6a2b3-123">Crear fluxos de treball d'aprovació per a elements de línia d'informes de despeses.</span><span class="sxs-lookup"><span data-stu-id="6a2b3-123">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="6a2b3-124"><strong>Publicació automàtica d'elements de línies de despesa</strong></span><span class="sxs-lookup"><span data-stu-id="6a2b3-124"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="6a2b3-125">Crear fluxos de treball de publicació automàtica per a elements de línia d'informes de despeses.</span><span class="sxs-lookup"><span data-stu-id="6a2b3-125">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="6a2b3-126"><strong>Petició de viatge</strong></span><span class="sxs-lookup"><span data-stu-id="6a2b3-126"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="6a2b3-127">Crear fluxos de treball d'aprovació per a requisicions de viatge.</span><span class="sxs-lookup"><span data-stu-id="6a2b3-127">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="6a2b3-128"><strong>Sol·licitud d'avançament d'efectiu</strong></span><span class="sxs-lookup"><span data-stu-id="6a2b3-128"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="6a2b3-129">Crear fluxos de treball d'aprovació per a sol·licituds d'avançament d'efectiu.</span><span class="sxs-lookup"><span data-stu-id="6a2b3-129">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="6a2b3-130"><strong>Recuperació de l'IVA</strong></span><span class="sxs-lookup"><span data-stu-id="6a2b3-130"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="6a2b3-131">Crear fluxos de treball d'aprovació per a la recuperació de l'impost sobre el valor afegit (IVA).</span><span class="sxs-lookup"><span data-stu-id="6a2b3-131">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |



[!INCLUDE[footer-include](../includes/footer-banner.md)]