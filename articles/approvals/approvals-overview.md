---
title: Informació general de les aprovacions
description: En aquest tema es proporciona informació sobre treballar amb aprovacions al Project Operations.
author: stsporen
ms.date: 03/31/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 5e30b8a386805faee869f77e695d5ee492d78cdb
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996689"
---
# <a name="approvals-overview"></a><span data-ttu-id="e0f53-103">Informació general de les aprovacions</span><span class="sxs-lookup"><span data-stu-id="e0f53-103">Approvals overview</span></span>

<span data-ttu-id="e0f53-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_</span><span class="sxs-lookup"><span data-stu-id="e0f53-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e0f53-105">Les entrades de temps, despeses i ús de materials es desplacen a través d'un flux de treball d'aprovació.</span><span class="sxs-lookup"><span data-stu-id="e0f53-105">Time, expense, and material usage submissions move through an approval workflow.</span></span> <span data-ttu-id="e0f53-106">Un cop aprovades les entrades, les transaccions es registren en els valors reals o el temps es reserva a la planificació.</span><span class="sxs-lookup"><span data-stu-id="e0f53-106">After the entries are approved, transactions are recorded in actuals or time is booked in the schedule.</span></span>

## <a name="approvals-workflow"></a><span data-ttu-id="e0f53-107">Flux de treball d'aprovacions</span><span class="sxs-lookup"><span data-stu-id="e0f53-107">Approvals workflow</span></span>
<span data-ttu-id="e0f53-108">Quan creeu i envieu una entrada de temps, despesa o ús de materials, es crea un registre d'aprovació.</span><span class="sxs-lookup"><span data-stu-id="e0f53-108">When you create and submit a time, expense, or material usage entry, an approval record is created.</span></span> <span data-ttu-id="e0f53-109">L'aprovador o l'administrador del projecte revisa i aprova l'entrada.</span><span class="sxs-lookup"><span data-stu-id="e0f53-109">The project approver or manager reviews and approves the entry.</span></span> <span data-ttu-id="e0f53-110">Si l'entrada està relacionada amb un projecte, els valors reals es crearan quan s'aprovi.</span><span class="sxs-lookup"><span data-stu-id="e0f53-110">If the entry is related to a project, the actuals will be created when it's approved.</span></span> <span data-ttu-id="e0f53-111">Això permet fer un seguiment del cost i de la facturació.</span><span class="sxs-lookup"><span data-stu-id="e0f53-111">This allows the cost and billing to be tracked.</span></span>

## <a name="approve-an-entry"></a><span data-ttu-id="e0f53-112">Aprovar una entrada</span><span class="sxs-lookup"><span data-stu-id="e0f53-112">Approve an entry</span></span>
<span data-ttu-id="e0f53-113">La pàgina **Aprovacions** us permet canviar entre diferents visualitzacions per tal de visualitzar els diferents tipus d'aprovacions.</span><span class="sxs-lookup"><span data-stu-id="e0f53-113">The **Approvals** page allows you to switch between different views so that you can view the different types of approvals.</span></span>
  
1. <span data-ttu-id="e0f53-114">Aneu a la pàgina **Aprovacions** i seleccioneu **Despeses**, **Temps**, **Ús de materials** o **Recuperacions**.</span><span class="sxs-lookup"><span data-stu-id="e0f53-114">Go to the **Approvals** page and select **Expenses**, **Time**, **Material Usage**, or **Recalls**.</span></span>
2. <span data-ttu-id="e0f53-115">Reviseu cada aprovació i seleccioneu les que voleu aprovar.</span><span class="sxs-lookup"><span data-stu-id="e0f53-115">Review each approval, and select the ones you want to approve.</span></span>
3. <span data-ttu-id="e0f53-116">Seleccioneu **Aprova** per aprovar les entrades seleccionades.</span><span class="sxs-lookup"><span data-stu-id="e0f53-116">Select **Approve** to approve the selected entries.</span></span>
<span data-ttu-id="e0f53-117">El sistema processa aquestes entrades i crea valors reals.</span><span class="sxs-lookup"><span data-stu-id="e0f53-117">The system processes these entries and create actuals.</span></span>

## <a name="reject-an-entry"></a><span data-ttu-id="e0f53-118">Rebutjar una entrada</span><span class="sxs-lookup"><span data-stu-id="e0f53-118">Reject an entry</span></span>
<span data-ttu-id="e0f53-119">Com a aprovador de projectes, potser haureu de retornar una entrada a un usuari per corregir-la.</span><span class="sxs-lookup"><span data-stu-id="e0f53-119">As the Project approver, you may have to send an entry back to a user for correction.</span></span>
  
1. <span data-ttu-id="e0f53-120">Aneu a la pàgina **Aprovacions** i seleccioneu l'entrada per rebutjar.</span><span class="sxs-lookup"><span data-stu-id="e0f53-120">Go to the **Approvals** page and select the entry to reject.</span></span> 
2. <span data-ttu-id="e0f53-121">Seleccioneu **Rebutja**.</span><span class="sxs-lookup"><span data-stu-id="e0f53-121">Select **Reject**.</span></span>
3. <span data-ttu-id="e0f53-122">Opcionalment, afegiu un comentari al quadre de diàleg **Comentaris de rebuig** per informar l'usuari sobre la raó per la qual es rebutja l'entrada.</span><span class="sxs-lookup"><span data-stu-id="e0f53-122">Optional, add a comment in the **Rejection Comments** dialog box to inform the user why the entry is being rejected.</span></span>
4. <span data-ttu-id="e0f53-123">Seleccioneu **D'acord**.</span><span class="sxs-lookup"><span data-stu-id="e0f53-123">Select **OK**.</span></span> <span data-ttu-id="e0f53-124">L'entrada es retornarà a l'usuari.</span><span class="sxs-lookup"><span data-stu-id="e0f53-124">The entry will be returned to the user.</span></span>
  
## <a name="cancel-approval"></a><span data-ttu-id="e0f53-125">Cancel·la l'aprovació</span><span class="sxs-lookup"><span data-stu-id="e0f53-125">Cancel approval</span></span>
<span data-ttu-id="e0f53-126">En alguns casos, pot ser que hàgiu de cancel·lar una entrada prèviament aprovada.</span><span class="sxs-lookup"><span data-stu-id="e0f53-126">In some cases, you might need to cancel a previously approved entry.</span></span> <span data-ttu-id="e0f53-127">La cancel·lació d'una entrada prèviament aprovada tindrà un impacte financer.</span><span class="sxs-lookup"><span data-stu-id="e0f53-127">Canceling a previously approved entry will have a financial impact.</span></span> 

## <a name="approving-recall-requests"></a><span data-ttu-id="e0f53-128">Aprovació de sol·licituds de recuperació</span><span class="sxs-lookup"><span data-stu-id="e0f53-128">Approving recall requests</span></span>
<span data-ttu-id="e0f53-129">En alguns casos, un consultor pot haver de recuperar una entrada prèviament aprovada.</span><span class="sxs-lookup"><span data-stu-id="e0f53-129">In some cases, a consultant may need to recall a previously approved entry.</span></span> <span data-ttu-id="e0f53-130">La cancel·lació d'una entrada prèviament aprovada tindrà un impacte financer.</span><span class="sxs-lookup"><span data-stu-id="e0f53-130">Canceling a previously approved entry will have a financial impact.</span></span> <span data-ttu-id="e0f53-131">Cal l'aprovador del projecte per aprovar la recuperació per invertir la transacció a Valors reals.</span><span class="sxs-lookup"><span data-stu-id="e0f53-131">The project approver is required to approve the recall to reverse the transaction in Actuals.</span></span>

## <a name="specify-project-approvers"></a><span data-ttu-id="e0f53-132">Especificar els aprovadors del projecte</span><span class="sxs-lookup"><span data-stu-id="e0f53-132">Specify Project approvers</span></span>
<span data-ttu-id="e0f53-133">Cada projecte té un nombre de membres de l'equip del projecte.</span><span class="sxs-lookup"><span data-stu-id="e0f53-133">Each project has a number of project team members.</span></span> <span data-ttu-id="e0f53-134">Podeu especificar quins membres de l'equip són també aprovadors del projecte.</span><span class="sxs-lookup"><span data-stu-id="e0f53-134">You can specify which team members are also Project approvers.</span></span>

1. <span data-ttu-id="e0f53-135">Aneu a la pàgina **Projectes** i obriu el projecte de la llista.</span><span class="sxs-lookup"><span data-stu-id="e0f53-135">Go to the **Projects** page and open the project from the list.</span></span>
2. <span data-ttu-id="e0f53-136">A la pestanya **Equip**, seleccioneu el membre de l'equip que serà un aprovador del projecte i, a continuació, seleccioneu **Edita**.</span><span class="sxs-lookup"><span data-stu-id="e0f53-136">On the **Team** tab, select the team member who will be a Project approver and then select **Edit**.</span></span>
3. <span data-ttu-id="e0f53-137">Definiu el camp **Aprovador del projecte** a **Sí**.</span><span class="sxs-lookup"><span data-stu-id="e0f53-137">Set the **Project Approver** field to **Yes**.</span></span>
4. <span data-ttu-id="e0f53-138">Seleccioneu **Desa**.</span><span class="sxs-lookup"><span data-stu-id="e0f53-138">Select **Save**.</span></span>
5. <span data-ttu-id="e0f53-139">Repetiu els passos 2 i 4 per afegir aprovadors del projecte addicionals.</span><span class="sxs-lookup"><span data-stu-id="e0f53-139">Repeat steps 2-4 to add additional Project approvers.</span></span>

## <a name="configure-the-users-manager"></a><span data-ttu-id="e0f53-140">Configurar l'administrador de l'usuari</span><span class="sxs-lookup"><span data-stu-id="e0f53-140">Configure the user's manager</span></span>

1. <span data-ttu-id="e0f53-141">Aneu a **Configuració** > **Seguretat** > **Usuaris**.</span><span class="sxs-lookup"><span data-stu-id="e0f53-141">Go to **Settings** > **Security** > **Users**.</span></span>
2. <span data-ttu-id="e0f53-142">Seleccioneu l'usuari a qui esteu assignant un administrador i a l'àrea **Informació de l'organització**, seleccioneu l'administrador de la llista.</span><span class="sxs-lookup"><span data-stu-id="e0f53-142">Select the user to whom you are assigning a manager and in the **Organization Information** area, select the manager from the list.</span></span> 
3. <span data-ttu-id="e0f53-143">Seleccioneu **Desa**.</span><span class="sxs-lookup"><span data-stu-id="e0f53-143">Select **Save**.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]
