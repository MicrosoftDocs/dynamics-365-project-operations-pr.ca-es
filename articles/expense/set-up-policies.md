---
title: Definir normes de despesa
description: Podeu definir normes de despesa que els treballadors han de seguir en introduir i enviar informes de despeses i requisicions de viatge.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 30b3a0e1547ca7043b1433da2b4ebf02f2b473a1
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072282"
---
# <a name="define-expense-policies"></a><span data-ttu-id="3c954-103">Definir normes de despesa</span><span class="sxs-lookup"><span data-stu-id="3c954-103">Define expense policies</span></span>

<span data-ttu-id="3c954-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_</span><span class="sxs-lookup"><span data-stu-id="3c954-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="3c954-105">Podeu definir normes que els treballadors han de seguir en introduir i enviar informes de despeses i requisicions de viatge.</span><span class="sxs-lookup"><span data-stu-id="3c954-105">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="3c954-106">Implementar normes de despesa us pot ajudar a administrar les despeses de manera eficaç.</span><span class="sxs-lookup"><span data-stu-id="3c954-106">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="3c954-107">Per exemple, podeu definir una norma per a les despeses d'hotels a Nova York que indiqui que la despesa per nit no pot superar els 250 USD.</span><span class="sxs-lookup"><span data-stu-id="3c954-107">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="3c954-108">Si un treballador envia un informe de despeses o una requisició de viatges en què el preu de l'habitació excedeixi aquesta quantitat, el sistema notificarà al</span><span class="sxs-lookup"><span data-stu-id="3c954-108">If a worker submits an expense report or travel requisition where the room rate exceeds this amount, the system will notify the</span></span>         
<span data-ttu-id="3c954-109">treballador que l'import de la norma per a la despesa s'ha excedit.</span><span class="sxs-lookup"><span data-stu-id="3c954-109">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="3c954-110">Podeu configurar el missatge que rebrà el treballador en el moment de</span><span class="sxs-lookup"><span data-stu-id="3c954-110">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="3c954-111">definir la norma.</span><span class="sxs-lookup"><span data-stu-id="3c954-111">define the policy.</span></span>      
        
<span data-ttu-id="3c954-112">Podeu definir tres tipus de normes:</span><span class="sxs-lookup"><span data-stu-id="3c954-112">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="3c954-113">**Advertiment** : permet al treballador presentar un informe de despeses o una requisició de viatge però la despesa es marcarà per a tots els aprovadors i</span><span class="sxs-lookup"><span data-stu-id="3c954-113">**Warning** : Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>         
  <span data-ttu-id="3c954-114">per a informes posteriors.</span><span class="sxs-lookup"><span data-stu-id="3c954-114">for later reporting.</span></span>        

- <span data-ttu-id="3c954-115">**Error** : requereix que el treballador revisi la despesa per tal de complir la norma abans d'enviar l'informe de despeses o la requisició de viatges.</span><span class="sxs-lookup"><span data-stu-id="3c954-115">**Error** : Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>        
 
 - <span data-ttu-id="3c954-116">**Justificació** : requereix que el treballador o un cap introdueixin una justificació per superar la quantitat de la norma abans d'enviar l'informe de despeses o la requisició de viatges.</span><span class="sxs-lookup"><span data-stu-id="3c954-116">**Justification** : Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

## <a name="policy-tips"></a><span data-ttu-id="3c954-117">Consells per a les normes</span><span class="sxs-lookup"><span data-stu-id="3c954-117">Policy tips</span></span>
<span data-ttu-id="3c954-118">A continuació, trobareu alguns suggeriments que us poden ajudar a crear normes noves per a l'administració de despeses:</span><span class="sxs-lookup"><span data-stu-id="3c954-118">Here are a few suggestions that can assist you when creating new policies for expense management:</span></span> 

- <span data-ttu-id="3c954-119">Les normes tenen una data efectiva, la qual cosa significa que una norma no té efecte si es crea amb una data després de la data en què s'ha produït la despesa.</span><span class="sxs-lookup"><span data-stu-id="3c954-119">Policies are date effective which means a policy won't take effect if it's created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="3c954-120">Per exemple, es crea avui una norma nova per fer complir una despesa màxima d'àpats de 50 USD.</span><span class="sxs-lookup"><span data-stu-id="3c954-120">For example, you create a new policy today to enforce a maximum meal expense of $50.</span></span> <span data-ttu-id="3c954-121">Les despeses existents que no s'hagin introduït des d'ahir no es comprovaran amb aquesta norma.</span><span class="sxs-lookup"><span data-stu-id="3c954-121">Any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
- <span data-ttu-id="3c954-122">Quan es crea una norma per a una categoria de despesa que es pot desglossar, cal afegir una condició per al tipus de línia de despeses.</span><span class="sxs-lookup"><span data-stu-id="3c954-122">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="3c954-123">Algunes de les normes, com ara requerir un rebut, pot ser que no tinguin sentit per a les línies desglossades.</span><span class="sxs-lookup"><span data-stu-id="3c954-123">Some policies, such as requiring a receipt, may not make sense for itemized lines.</span></span> <span data-ttu-id="3c954-124">En aquesta situació, la norma només s'aplica a la línia de capçalera o en una línia no desglossada.</span><span class="sxs-lookup"><span data-stu-id="3c954-124">In this situation, the policy only is applied to the header line or a non-itemized line.</span></span> 
- <span data-ttu-id="3c954-125">Les normes d'administració de despeses s'avaluen amb l'entitat d'origen per defecte.</span><span class="sxs-lookup"><span data-stu-id="3c954-125">Expense management policies are evaluated against the source entity by default.</span></span> <span data-ttu-id="3c954-126">Per als escenaris entre empreses, podeu definir la norma que s'avalua a l'entitat de destinació (entitat prestatària) en el seu lloc.</span><span class="sxs-lookup"><span data-stu-id="3c954-126">For intercompany scenarios, you can set the policy to be evaluated against the destination entity (borrowing entity) instead.</span></span> <span data-ttu-id="3c954-127">Per executar les normes a l'entitat de destinació, activeu la funció **Avalua la norma de despesa a l'entitat jurídica prestatària** a l'àrea de treball **Administració de característiques**.</span><span class="sxs-lookup"><span data-stu-id="3c954-127">To run the policies against the destination entity, turn on the **Evaluate Expense policy against borrowing legal entity** feature in the **Feature Management** workspace.</span></span>

## <a name="when-to-evaluate-policies"></a><span data-ttu-id="3c954-128">Quan avaluar les normes</span><span class="sxs-lookup"><span data-stu-id="3c954-128">When to evaluate policies</span></span>

<span data-ttu-id="3c954-129">A paràmetres d'administració de despeses, podeu seleccionar avaluar les normes d'avaluació de despeses quan es desa una línia o quan s'envia un informe de despeses.</span><span class="sxs-lookup"><span data-stu-id="3c954-129">In expense management parameters, you can select to evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="3c954-130">Si trieu avaluar-les quan es desa una línia, els usuaris tindran una visibilitat prèvia del que han de fer per completar el seu informe de despeses d'una vegada.</span><span class="sxs-lookup"><span data-stu-id="3c954-130">If you choose to evaluate when a line is saved, users will have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="3c954-131">Si no és així, podeu endarrerir l'avaluació de la norma i estalviar temps validant-la al final durant l'enviament al flux de treball.</span><span class="sxs-lookup"><span data-stu-id="3c954-131">Otherwise, you can delay policy evaluation and save time by validating at the end, during the submission to workflow.</span></span>
