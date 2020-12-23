---
title: Configuració de les normes de despesa
description: Podeu configurar les normes de despeses que els vostres treballadors han de seguir en introduir i enviar informes de despeses i peticions de viatge al Microsoft Dynamics 365 Finance.
author: suvaidya
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6240a7be175800ce6f3b066de9e935ab370629ef
ms.sourcegitcommit: 13a4e58eddbb0f81aca07c1ff452c420dbd8a68f
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 11/30/2020
ms.locfileid: "4650082"
---
# <a name="set-up-expense-policies"></a><span data-ttu-id="1afde-103">Configuració de les normes de despesa</span><span class="sxs-lookup"><span data-stu-id="1afde-103">Set up expense policies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1afde-104">Podeu definir normes que els treballadors han de seguir en introduir i enviar informes de despeses i requisicions de viatge.</span><span class="sxs-lookup"><span data-stu-id="1afde-104">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="1afde-105">Implementar normes de despesa us pot ajudar a administrar les despeses de manera eficaç.</span><span class="sxs-lookup"><span data-stu-id="1afde-105">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="1afde-106">Per exemple, podeu definir una norma per a les despeses d'hotels a Nova York que indiqui que la despesa per nit no pot superar els 250 USD.</span><span class="sxs-lookup"><span data-stu-id="1afde-106">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="1afde-107">Si un treballador envia un informe de despeses o una petició de viatge en què el preu de l'habitació excedeixi aquesta quantitat, el sistema notificarà al</span><span class="sxs-lookup"><span data-stu-id="1afde-107">If a worker submits an expense report or a travel requisition in which the room rate exceeds this amount, the system will notify the</span></span>        
<span data-ttu-id="1afde-108">treballador que l'import de la norma per a la despesa s'ha excedit.</span><span class="sxs-lookup"><span data-stu-id="1afde-108">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="1afde-109">Podeu configurar el missatge que rebrà el treballador en el moment de</span><span class="sxs-lookup"><span data-stu-id="1afde-109">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="1afde-110">definir la norma.</span><span class="sxs-lookup"><span data-stu-id="1afde-110">define the policy.</span></span>      
        
<span data-ttu-id="1afde-111">Podeu definir tres tipus de normes:</span><span class="sxs-lookup"><span data-stu-id="1afde-111">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="1afde-112">Advertiment: permet al treballador presentar un informe de despeses o una requisició de viatge però la despesa es marcarà per a tots els aprovadors i</span><span class="sxs-lookup"><span data-stu-id="1afde-112">Warning – Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>        
  <span data-ttu-id="1afde-113">per a informes posteriors.</span><span class="sxs-lookup"><span data-stu-id="1afde-113">for later reporting.</span></span>        

- <span data-ttu-id="1afde-114">Error: requereix que el treballador revisi la despesa per tal de complir la norma abans d'enviar l'informe de despeses o la requisició de viatges.</span><span class="sxs-lookup"><span data-stu-id="1afde-114">Error – Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>       
 
 - <span data-ttu-id="1afde-115">Justificació: requereix que el treballador o un cap introdueixin una justificació per superar la quantitat de la norma abans d'enviar l'informe de despeses o la requisició de viatges.</span><span class="sxs-lookup"><span data-stu-id="1afde-115">Justification – Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

## <a name="policy-tips"></a><span data-ttu-id="1afde-116">Consells per a les normes</span><span class="sxs-lookup"><span data-stu-id="1afde-116">Policy tips</span></span>
<span data-ttu-id="1afde-117">A continuació, trobareu alguns suggeriments que us poden ajudar a crear normes noves per a l'administració de despeses.</span><span class="sxs-lookup"><span data-stu-id="1afde-117">Here are a few suggestions that can assist you when creating new policies for expense management.</span></span> 
* <span data-ttu-id="1afde-118">Les normes tenen una data efectiva i no tenen efecte si es crea la norma amb una data després de la data en què s'ha produït la despesa.</span><span class="sxs-lookup"><span data-stu-id="1afde-118">Policies are date effective and won't take effect if the policy is created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="1afde-119">Per exemple, si avui creeu una nova norma per aplicar una despesa màxima per àpat de 50 USD, qualsevol despesa existent introduïda fins ahir no es comprovarà amb aquesta norma.</span><span class="sxs-lookup"><span data-stu-id="1afde-119">For example, if you are creating a new policy today to enforce a maximum meal expense of $50, then any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
* <span data-ttu-id="1afde-120">Quan es crea una norma per a una categoria de despesa que es pot desglossar, cal afegir una condició per al tipus de línia de despeses.</span><span class="sxs-lookup"><span data-stu-id="1afde-120">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="1afde-121">Algunes normes, com ara exigir un rebut, poden no tenir sentit per a les línies i només s'han d'aplicar a la línia de capçalera o a una línia no desglossada.</span><span class="sxs-lookup"><span data-stu-id="1afde-121">Some policies such as requiring a receipt may not make sense for itemized lines and should only be applied to the header line or a non-itemized line.</span></span> 
* <span data-ttu-id="1afde-122">Les normes d'administració de despeses s'avaluen amb l'entitat d'origen per defecte.</span><span class="sxs-lookup"><span data-stu-id="1afde-122">Expense management policies are evaluated against the source entity by default.</span></span> <span data-ttu-id="1afde-123">Per als escenaris entre empreses, podeu definir la norma que s'avalua a l'entitat de destinació (entitat prestatària) en el seu lloc.</span><span class="sxs-lookup"><span data-stu-id="1afde-123">For intercompany scenarios, you can set the policy to be evaluated against the destination entity (borrowing entity) instead.</span></span> <span data-ttu-id="1afde-124">Per executar les normes a l'entitat de destinació, activeu la funció "Avalua la norma de despesa a l'entitat jurídica prestatària" a l'àrea de treball **Administració de característiques**.</span><span class="sxs-lookup"><span data-stu-id="1afde-124">To run the policies against the destination entity, turn on the "Evaluate Expense policy against borrowing legal entity" feature in the **Feature Management** workspace.</span></span>

## <a name="when-to-evaluate-policies"></a><span data-ttu-id="1afde-125">Quan avaluar les normes</span><span class="sxs-lookup"><span data-stu-id="1afde-125">When to evaluate policies</span></span>

<span data-ttu-id="1afde-126">Als paràmetres d'administració de despeses, hi ha una opció per avaluar les normes d'avaluació de despeses quan es desa una línia o quan s'envia un informe de despeses.</span><span class="sxs-lookup"><span data-stu-id="1afde-126">In expense management parameters, there is an option to either evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="1afde-127">Si trieu avaluar-les quan es desa una línia, això assegura que els usuaris tindran una visibilitat prèvia del que han de fer per completar el seu informe de despeses d'una vegada.</span><span class="sxs-lookup"><span data-stu-id="1afde-127">If you choose to evaluate when a line is saved this ensures that users have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="1afde-128">Si no és així, podeu endarrerir l'avaluació de la norma i estalviar temps si feu que l'avaluació sigui al final, durant l'enviament al flux de treball.</span><span class="sxs-lookup"><span data-stu-id="1afde-128">Otherwise, you can delay policy evaluation and save time if you have validation occur at the end, during submission to workflow.</span></span>
