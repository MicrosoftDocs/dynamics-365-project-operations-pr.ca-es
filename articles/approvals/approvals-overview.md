---
title: Informació general de les aprovacions
description: En aquest tema es proporciona informació sobre treballar amb aprovacions al Project Operations.
author: stsporen
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 37994422e9146765076fdbb77f5c763b4f1d0802
ms.sourcegitcommit: 2cf93d8bf0be5b61a739195a41334c34d910e9ba
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961154"
---
# <a name="approvals-overview"></a><span data-ttu-id="1a9d5-103">Informació general de les aprovacions</span><span class="sxs-lookup"><span data-stu-id="1a9d5-103">Approvals overview</span></span>

<span data-ttu-id="1a9d5-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_</span><span class="sxs-lookup"><span data-stu-id="1a9d5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="1a9d5-105">Els enviaments de temps i de despeses passen per un flux de treball d'aprovació.</span><span class="sxs-lookup"><span data-stu-id="1a9d5-105">Time and Expense submissions move through an approval workflow.</span></span> <span data-ttu-id="1a9d5-106">Un cop aprovades les entrades, les transaccions es registren en els valors reals o el temps es reserva a la planificació.</span><span class="sxs-lookup"><span data-stu-id="1a9d5-106">After the entries are approved, transactions are recorded in actuals or time is booked in the schedule.</span></span>

## <a name="approvals-workflow"></a><span data-ttu-id="1a9d5-107">Flux de treball d'aprovacions</span><span class="sxs-lookup"><span data-stu-id="1a9d5-107">Approvals workflow</span></span>
<span data-ttu-id="1a9d5-108">Quan creeu i envieu una entrada de temps o de despesa, es crea una entrada d'aprovació.</span><span class="sxs-lookup"><span data-stu-id="1a9d5-108">When you create and submit a time or expense entry, an approval entry is created.</span></span> <span data-ttu-id="1a9d5-109">L'aprovador de projectes o l'administrador revisa i aprova l'entrada.</span><span class="sxs-lookup"><span data-stu-id="1a9d5-109">The Project approver or your manager reviews and approves your entry.</span></span> <span data-ttu-id="1a9d5-110">Si l'entrada està relacionada amb un projecte, quan s'hagi aprovat, es crearan els valors reals.</span><span class="sxs-lookup"><span data-stu-id="1a9d5-110">If the entry is related to a project, when it's approved, the actuals will be created.</span></span> <span data-ttu-id="1a9d5-111">Això permet fer un seguiment del cost i de la facturació.</span><span class="sxs-lookup"><span data-stu-id="1a9d5-111">This allows the cost and billing to be tracked.</span></span> 

## <a name="approve-an-entry"></a><span data-ttu-id="1a9d5-112">Aprovar una entrada</span><span class="sxs-lookup"><span data-stu-id="1a9d5-112">Approve an entry</span></span>
<span data-ttu-id="1a9d5-113">El formulari **Aprovacions** us permet canviar entre diferents visualitzacions per tal que pugueu visualitzar els diferents tipus d'aprovacions.</span><span class="sxs-lookup"><span data-stu-id="1a9d5-113">The **Approvals** form allows you to switch between different views so that you can view the different types of approvals.</span></span>
  
1. <span data-ttu-id="1a9d5-114">Aneu al formulari **Aprovacions** i seleccioneu **Despeses**, **Temps** o **Recuperacions**.</span><span class="sxs-lookup"><span data-stu-id="1a9d5-114">Go to the **Approvals** form and select **Expenses**, **Time**, or **Recalls**.</span></span>
2. <span data-ttu-id="1a9d5-115">Reviseu cada aprovació i seleccioneu les que voleu aprovar.</span><span class="sxs-lookup"><span data-stu-id="1a9d5-115">Review each approval, and select the ones you want to approve.</span></span>
3. <span data-ttu-id="1a9d5-116">Seleccioneu **Aprova** per aprovar les entrades seleccionades.</span><span class="sxs-lookup"><span data-stu-id="1a9d5-116">Select **Approve** to approve the selected entries.</span></span>
<span data-ttu-id="1a9d5-117">El sistema processarà aquestes entrades i crearà valors reals o una reserva.</span><span class="sxs-lookup"><span data-stu-id="1a9d5-117">The system will process these entries and create actuals or a booking.</span></span>

## <a name="reject-an-entry"></a><span data-ttu-id="1a9d5-118">Rebutjar una entrada</span><span class="sxs-lookup"><span data-stu-id="1a9d5-118">Reject an entry</span></span>
<span data-ttu-id="1a9d5-119">Com a aprovador de projectes, potser haureu de retornar una entrada a un usuari per corregir-la.</span><span class="sxs-lookup"><span data-stu-id="1a9d5-119">As the Project approver, you may have to send an entry back to a user for correction.</span></span>
  
1. <span data-ttu-id="1a9d5-120">Aneu al formulari **Aprovacions** i seleccioneu l'entrada per rebutjar.</span><span class="sxs-lookup"><span data-stu-id="1a9d5-120">Go to the **Approvals** form and select the entry to reject.</span></span> 
2. <span data-ttu-id="1a9d5-121">Seleccioneu **Rebutja**.</span><span class="sxs-lookup"><span data-stu-id="1a9d5-121">Select **Reject**.</span></span>
3. <span data-ttu-id="1a9d5-122">Opcional: afegiu un comentari al diàleg **Comentaris de rebuig** per informar l'usuari per què es rebutja l'entrada.</span><span class="sxs-lookup"><span data-stu-id="1a9d5-122">Optional - Add a comment in the **Rejection Comments** dialog to inform the user why the entry is being rejected.</span></span>
4. <span data-ttu-id="1a9d5-123">Seleccioneu **D'acord**.</span><span class="sxs-lookup"><span data-stu-id="1a9d5-123">Select **OK**.</span></span> <span data-ttu-id="1a9d5-124">L'entrada es retornarà a l'usuari.</span><span class="sxs-lookup"><span data-stu-id="1a9d5-124">The entry will be returned to the user.</span></span>
  
## <a name="recall-entries"></a><span data-ttu-id="1a9d5-125">Recuperar entrades</span><span class="sxs-lookup"><span data-stu-id="1a9d5-125">Recall entries</span></span>
<span data-ttu-id="1a9d5-126">En algun moment, pot ser que hàgiu de recuperar una entrada enviada.</span><span class="sxs-lookup"><span data-stu-id="1a9d5-126">At some point, you might need to recall a submitted entry.</span></span> <span data-ttu-id="1a9d5-127">Si l'entrada no ha estat aprovada, es retornarà immediatament.</span><span class="sxs-lookup"><span data-stu-id="1a9d5-127">If the entry has not been approved, it will be returned immediately.</span></span> <span data-ttu-id="1a9d5-128">Això no obstant, una entrada aprovada pot tenir un impacte material.</span><span class="sxs-lookup"><span data-stu-id="1a9d5-128">An approved entry however, may have a material impact.</span></span> <span data-ttu-id="1a9d5-129">L'aprovador de projectes es necessita per aprovar la recuperar per tal de revertir la transacció en valors reals.</span><span class="sxs-lookup"><span data-stu-id="1a9d5-129">The Project approver is required to approve the recall in order to reverse the transaction in Actuals.</span></span>

## <a name="specify-project-approvers"></a><span data-ttu-id="1a9d5-130">Especificar els aprovadors del projecte</span><span class="sxs-lookup"><span data-stu-id="1a9d5-130">Specify Project approvers</span></span>
<span data-ttu-id="1a9d5-131">Cada projecte té un nombre de membres de l'equip del projecte.</span><span class="sxs-lookup"><span data-stu-id="1a9d5-131">Each project has a number of project team members.</span></span> <span data-ttu-id="1a9d5-132">Podeu especificar quins membres de l'equip són també aprovadors del projecte.</span><span class="sxs-lookup"><span data-stu-id="1a9d5-132">You can specify which team members are also Project approvers.</span></span>

1. <span data-ttu-id="1a9d5-133">Aneu al formulari **Projectes** i obriu el projecte des de la llista.</span><span class="sxs-lookup"><span data-stu-id="1a9d5-133">Go to the **Projects** form and open the project from the list.</span></span>
2. <span data-ttu-id="1a9d5-134">A la pestanya **Equip**, seleccioneu el membre de l'equip que serà un aprovador del projecte i, a continuació, seleccioneu **Edita**.</span><span class="sxs-lookup"><span data-stu-id="1a9d5-134">On the **Team** tab, select the team member who will be a Project approver and then select **Edit**.</span></span>
3. <span data-ttu-id="1a9d5-135">Definiu el camp **Aprovador del projecte** a **Sí**.</span><span class="sxs-lookup"><span data-stu-id="1a9d5-135">Set the **Project Approver** field to **Yes**.</span></span>
4. <span data-ttu-id="1a9d5-136">Seleccioneu **Desa**.</span><span class="sxs-lookup"><span data-stu-id="1a9d5-136">Select **Save**.</span></span>
5. <span data-ttu-id="1a9d5-137">Repetiu els passos 2 i 4 per afegir aprovadors del projecte addicionals.</span><span class="sxs-lookup"><span data-stu-id="1a9d5-137">Repeat steps 2-4 to add additional Project approvers.</span></span>

## <a name="configure-the-users-manager"></a><span data-ttu-id="1a9d5-138">Configurar l'administrador de l'usuari</span><span class="sxs-lookup"><span data-stu-id="1a9d5-138">Configure the user's manager</span></span>

1. <span data-ttu-id="1a9d5-139">Aneu a **Configuració** > **Seguretat** > **Usuaris**.</span><span class="sxs-lookup"><span data-stu-id="1a9d5-139">Go to **Settings** > **Security** > **Users**.</span></span>
2. <span data-ttu-id="1a9d5-140">Seleccioneu l'usuari a qui esteu assignant un administrador i a l'àrea **Informació de l'organització**, seleccioneu l'administrador de la llista.</span><span class="sxs-lookup"><span data-stu-id="1a9d5-140">Select the user to whom you are assigning a manager and in the **Organization Information** area, select the manager from the list.</span></span> 
3. <span data-ttu-id="1a9d5-141">Seleccioneu **Desa**.</span><span class="sxs-lookup"><span data-stu-id="1a9d5-141">Select **Save**.</span></span>


