---
title: Configurar fluxos de treball per a l'administració de despeses
description: Podeu configurar un procés de flux de treball que s'utilitzi per revisar i aprovar els documents de viatges i de despeses.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: e54fca67427e8f3d0e7050563a751b5be354356c
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276021"
---
# <a name="set-up-workflows-for-expense-management"></a><span data-ttu-id="4fc59-103">Configurar fluxos de treball per a l'administració de despeses</span><span class="sxs-lookup"><span data-stu-id="4fc59-103">Set up workflows for Expense management</span></span>

<span data-ttu-id="4fc59-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_</span><span class="sxs-lookup"><span data-stu-id="4fc59-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="4fc59-105">Podeu configurar un procés de flux de treball per revisar i aprovar els documents de viatges i de despeses.</span><span class="sxs-lookup"><span data-stu-id="4fc59-105">You can set up a workflow process to review and approve travel and expense documents.</span></span> <span data-ttu-id="4fc59-106">Podeu definir fluxos de treball per a informes de despeses, requisicions de viatge i sol·licituds d'avançament en efectiu.</span><span class="sxs-lookup"><span data-stu-id="4fc59-106">You can define workflows for expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="4fc59-107">Un flux de treball representa un procés de negoci i defineix com un document flueix pel sistema.</span><span class="sxs-lookup"><span data-stu-id="4fc59-107">A workflow represents a business process and defines how a document flows through the system.</span></span> <span data-ttu-id="4fc59-108">El flux de treball també indica qui ha de completar una tasca o aprovar un document.</span><span class="sxs-lookup"><span data-stu-id="4fc59-108">The workflow also indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="4fc59-109">Hi ha diversos avantatges d'utilitzar el sistema de flux de treball a l'organització:</span><span class="sxs-lookup"><span data-stu-id="4fc59-109">There are several benefits of using the workflow system in your organization:</span></span>

- <span data-ttu-id="4fc59-110">**Processos coherents**: podeu definir el procés d'aprovació per a documents específics, com ara les requisicions de compra i els informes de despeses.</span><span class="sxs-lookup"><span data-stu-id="4fc59-110">**Consistent processes**: You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="4fc59-111">L'ús del sistema de flux de treball ajuda a garantir que els documents es processen i s'aproven de manera coherent i eficient.</span><span class="sxs-lookup"><span data-stu-id="4fc59-111">Using the workflow system helps ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
- <span data-ttu-id="4fc59-112">**Visibilitat de procés**: podeu fer el seguiment de l'estat, de l'historial i de les mètriques de rendiment d'una instància de flux de treball concreta.</span><span class="sxs-lookup"><span data-stu-id="4fc59-112">**Process visibility**: You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="4fc59-113">Això us ajudarà a determinar si s'han de fer canvis al flux de treball per millorar l'eficiència.</span><span class="sxs-lookup"><span data-stu-id="4fc59-113">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
- <span data-ttu-id="4fc59-114">**Llista de treball centralitzada**: els usuaris poden visualitzar una llista de treball centralitzada per visualitzar les tasques del flux de treball i les aprovacions assignades.</span><span class="sxs-lookup"><span data-stu-id="4fc59-114">**Centralized work list**: Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

## <a name="workflow-types"></a><span data-ttu-id="4fc59-115">Tipus de flux de treball</span><span class="sxs-lookup"><span data-stu-id="4fc59-115">Workflow types</span></span>

<span data-ttu-id="4fc59-116">A la taula següent s'enumeren els tipus de fluxos de treball que es poden crear a **Administració de despeses**.</span><span class="sxs-lookup"><span data-stu-id="4fc59-116">The following table lists the types of workflows that you can create in **Expense Management**.</span></span>


|              <span data-ttu-id="4fc59-117"><strong>Tipus</strong></span><span class="sxs-lookup"><span data-stu-id="4fc59-117"><strong>Type</strong></span></span>              |                   <span data-ttu-id="4fc59-118"><strong>Utilitzeu aquest tipus per</strong></span><span class="sxs-lookup"><span data-stu-id="4fc59-118"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|   <span data-ttu-id="4fc59-119"><strong>Aprovació automàtica d'informes de despeses</strong></span><span class="sxs-lookup"><span data-stu-id="4fc59-119"><strong>Expense report auto approval</strong></span></span> |            <span data-ttu-id="4fc59-120">Crear fluxos de treball d'aprovació per a informes de despeses.</span><span class="sxs-lookup"><span data-stu-id="4fc59-120">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="4fc59-121"><strong>Publicació automàtica d'informes de despeses</strong></span><span class="sxs-lookup"><span data-stu-id="4fc59-121"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="4fc59-122">Crear fluxos de treball de publicació automàtica per a informes de despeses.</span><span class="sxs-lookup"><span data-stu-id="4fc59-122">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="4fc59-123"><strong>Element de línia de despesa</strong></span><span class="sxs-lookup"><span data-stu-id="4fc59-123"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="4fc59-124">Crear fluxos de treball d'aprovació per a elements de línia d'informes de despeses.</span><span class="sxs-lookup"><span data-stu-id="4fc59-124">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="4fc59-125"><strong>Publicació automàtica d'elements de línies de despesa</strong></span><span class="sxs-lookup"><span data-stu-id="4fc59-125"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="4fc59-126">Crear fluxos de treball de publicació automàtica per a elements de línia d'informes de despeses.</span><span class="sxs-lookup"><span data-stu-id="4fc59-126">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="4fc59-127"><strong>Petició de viatge</strong></span><span class="sxs-lookup"><span data-stu-id="4fc59-127"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="4fc59-128">Crear fluxos de treball d'aprovació per a requisicions de viatge.</span><span class="sxs-lookup"><span data-stu-id="4fc59-128">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="4fc59-129"><strong>Sol·licitud d'avançament d'efectiu</strong></span><span class="sxs-lookup"><span data-stu-id="4fc59-129"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="4fc59-130">Crear fluxos de treball d'aprovació per a sol·licituds d'avançament d'efectiu.</span><span class="sxs-lookup"><span data-stu-id="4fc59-130">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="4fc59-131"><strong>Recuperació de l'IVA</strong></span><span class="sxs-lookup"><span data-stu-id="4fc59-131"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="4fc59-132">Crear fluxos de treball d'aprovació per a la recuperació de l'impost sobre el valor afegit (IVA).</span><span class="sxs-lookup"><span data-stu-id="4fc59-132">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |


[!INCLUDE[footer-include](../includes/footer-banner.md)]