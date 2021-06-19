---
title: Conjunts d'aprovacions
description: En aquest tema es proporciona informació sobre els conjunts d'aprovació, les sol·licituds i els subconjunts d'aquestes operacions.
author: stsporen
manager: tfehr
ms.date: 05/28/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: ac73313420029ece740d0bdb9c21c7abaa9defc6
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116859"
---
# <a name="approval-sets"></a><span data-ttu-id="ff023-103">Conjunts d'aprovacions</span><span class="sxs-lookup"><span data-stu-id="ff023-103">Approval sets</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="ff023-104">Els conjunts d'aprovació agrupen les sol·licituds d'aprovació en subconjunts d'operacions més petits.</span><span class="sxs-lookup"><span data-stu-id="ff023-104">Approval sets group approval requests together into smaller subsets of operations.</span></span> <span data-ttu-id="ff023-105">Aquest agrupament permet processar les aprovacions per ordre al projecte i permet tornar a provar i seqüenciar.</span><span class="sxs-lookup"><span data-stu-id="ff023-105">This grouping allows approvals to be processed in order by Project and allows for retrying and sequencing.</span></span> <span data-ttu-id="ff023-106">L'agrupació millora la fiabilitat i la traçabilitat del processament d'aprovacions per a grans volums d'aprovacions.</span><span class="sxs-lookup"><span data-stu-id="ff023-106">Grouping improves the reliability and traceability of approval processing for large volumes of approvals.</span></span>

<span data-ttu-id="ff023-107">Els conjunts d'aprovació indiquen l'estat de processament global dels registres relacionats.</span><span class="sxs-lookup"><span data-stu-id="ff023-107">Approval sets indicate the overall processing state of their related records.</span></span> <span data-ttu-id="ff023-108">Quan es processa un registre d'aprovació amb un conjunt d'aprovació, el registre passarà de l'estat **Enviat** a **Aprovat** i es desenllaçarà del conjunt d'aprovació.</span><span class="sxs-lookup"><span data-stu-id="ff023-108">When an approval record is processed using an approval set, the record moves from **Submitted** to **Approved**, and is unlinked from the approval set.</span></span> <span data-ttu-id="ff023-109">Si es produeix un error en un registre en enviar-lo per a l'aprovació, el registre es queda en estat **Enviat** i el conjunt d'aprovació es marca com a erroni.</span><span class="sxs-lookup"><span data-stu-id="ff023-109">If a record fails when it is submitted for approval, the record remains in a status of **Submitted** and the approval set is marked as failed.</span></span> <span data-ttu-id="ff023-110">El conjunt d'aprovació registra el missatge d'error de l'error.</span><span class="sxs-lookup"><span data-stu-id="ff023-110">The approval set logs the error message of the failure.</span></span>

## <a name="processing-approvals-and-approval-sets"></a><span data-ttu-id="ff023-111">Processament d'aprovacions i conjunts d'aprovació</span><span class="sxs-lookup"><span data-stu-id="ff023-111">Processing approvals and approval sets</span></span>
<span data-ttu-id="ff023-112">Les aprovacions que estan a la cua per al processament són visibles a la visualització **Aprovacions de processament**.</span><span class="sxs-lookup"><span data-stu-id="ff023-112">Approvals that are queued for processing are visible in the **Processing Approvals** view.</span></span> <span data-ttu-id="ff023-113">El sistema intenta processar totes les entrades de manera asíncrona diverses vegades, incloent-hi tornar a intentar una aprovació si s'ha produït un error en els intents anteriors.</span><span class="sxs-lookup"><span data-stu-id="ff023-113">The system tries to process all the entries multiple times asynchronously, including retrying an approval if previous attempts failed.</span></span>

<span data-ttu-id="ff023-114">El camp **Vida del conjunt d'aprovació** registra el nombre d'intents restants per processar el conjunt abans que es marqui com a error.</span><span class="sxs-lookup"><span data-stu-id="ff023-114">The **Approval Set Lifetime** field records the number of attempts left to process the set before it's marked as failed.</span></span>

## <a name="failed-approvals-and-approval-sets"></a><span data-ttu-id="ff023-115">Aprovacions i conjunts d'aprovació amb errors</span><span class="sxs-lookup"><span data-stu-id="ff023-115">Failed approvals and approval sets</span></span>
<span data-ttu-id="ff023-116">A la visualització **Aprovacions amb errors** s'enumeren totes les aprovacions que requereixen la intervenció de l'usuari.</span><span class="sxs-lookup"><span data-stu-id="ff023-116">The **Failed Approvals** view lists all approvals that require user intervention.</span></span> <span data-ttu-id="ff023-117">Obriu els registres del conjunt d'aprovació associats per identificar la causa de l'error.</span><span class="sxs-lookup"><span data-stu-id="ff023-117">Open the associated approval set logs to identify the cause of the failure.</span></span>
<span data-ttu-id="ff023-118">Si seleccioneu **Torna-ho a provar**, el recompte de vida del conjunt d'aprovacions augmenta, el conjunt d'aprovacions torna a tenir l'estat **En processament** i s'intenta processar els registres restants.</span><span class="sxs-lookup"><span data-stu-id="ff023-118">Selecting **Retry** adds to the approval set lifetime count, moves the approval set back to a status of **Processing**, and attempts to process the remaining records.</span></span>

## <a name="configure-approval-sets"></a><span data-ttu-id="ff023-119">Configurar conjunts d'aprovacions</span><span class="sxs-lookup"><span data-stu-id="ff023-119">Configure approval sets</span></span>

###  <a name="enable-the-approval-sets-feature"></a><span data-ttu-id="ff023-120">Habilitar la característica Conjunts d'aprovació</span><span class="sxs-lookup"><span data-stu-id="ff023-120">Enable the Approval sets feature</span></span>
<span data-ttu-id="ff023-121">Abans d'habilitar la característica Conjunts d'aprovació, comproveu que no s'estiguin processant aprovacions actualment.</span><span class="sxs-lookup"><span data-stu-id="ff023-121">Before you enable the Approval sets feature, verify that there are no approvals currently being processed.</span></span>

- <span data-ttu-id="ff023-122">Aneu a la pàgina **Paràmetres del projecte** i seleccioneu **Control de característiques** > **Habilita les aprovacions modernes**.</span><span class="sxs-lookup"><span data-stu-id="ff023-122">Go to the **Project parameters** page and select **Feature Control** > **Enable Modern Approvals**.</span></span>

### <a name="turn-off-the-approval-sets-feature"></a><span data-ttu-id="ff023-123">Desactivar la característica Conjunts d'aprovació</span><span class="sxs-lookup"><span data-stu-id="ff023-123">Turn off the Approval sets feature</span></span>
<span data-ttu-id="ff023-124">Abans de desactivar la característica Conjunts d'aprovació, comproveu que no s'estiguin processant aprovacions actualment.</span><span class="sxs-lookup"><span data-stu-id="ff023-124">Before you turn off the Approval sets feature, verify that there are no approvals currently being processed.</span></span>

- <span data-ttu-id="ff023-125">Aneu a la pàgina **Paràmetres del projecte** i seleccioneu **Control de característiques** > **Inhabilita les aprovacions modernes**.</span><span class="sxs-lookup"><span data-stu-id="ff023-125">Go to the **Project Parameters** page and select **Feature Control** > **Disable Modern Approvals**.</span></span>

### <a name="configuring-the-asynchronous-threshold"></a><span data-ttu-id="ff023-126">Configurar el llindar asíncron</span><span class="sxs-lookup"><span data-stu-id="ff023-126">Configuring the asynchronous threshold</span></span> 
<span data-ttu-id="ff023-127">Quan es creen conjunts d'aprovació, el processament es desplaça a segon terme quan el nombre de registres seleccionat per a la seva aprovació supera el llindar indicat.</span><span class="sxs-lookup"><span data-stu-id="ff023-127">When approval sets are created, processing moves to the background when the selected number of records for approval exceeds the indicated threshold.</span></span> <span data-ttu-id="ff023-128">Utilitzeu el camp **Llindar asíncron** per configurar quan el processament d'aprovació s'ha d'executar de manera síncrona o asíncrona.</span><span class="sxs-lookup"><span data-stu-id="ff023-128">Use the **Asynchronous Threshold** field to configure when approval processing should be run synchronously or asynchronously.</span></span>
<span data-ttu-id="ff023-129">Els valors vàlids són:</span><span class="sxs-lookup"><span data-stu-id="ff023-129">Valid values are:</span></span>

  - <span data-ttu-id="ff023-130">Zero: totes les sol·licituds s'han de processar de manera asíncrona.</span><span class="sxs-lookup"><span data-stu-id="ff023-130">Zero: All requests should be processed asynchronously.</span></span> 
  - <span data-ttu-id="ff023-131">Nombres majors que zero: les aprovacions es processen de manera asíncrona només quan el nombre d'aprovacions enviades supera aquest valor.</span><span class="sxs-lookup"><span data-stu-id="ff023-131">Numbers greater than zero: Approvals are processed asynchronously only when the submitted number of approvals exceeds this value.</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]