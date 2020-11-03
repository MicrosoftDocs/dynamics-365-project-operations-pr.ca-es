---
title: Creació de models de predicció per als pressupostos del projecte
description: Aquest tema descriu com crear un model de previsió per als pressupostos restants.
author: Yowelle
manager: AnnBe
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 32a436d240f5535ff15f8bc3b8ba9be2d1d4da17
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072348"
---
# <a name="create-forecast-models-for-project-budgets"></a><span data-ttu-id="8330d-103">Creació de models de predicció per als pressupostos del projecte</span><span class="sxs-lookup"><span data-stu-id="8330d-103">Create forecast models for project budgets</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8330d-104">Aquest tema descriu com crear un model de previsió per als pressupostos restants.</span><span class="sxs-lookup"><span data-stu-id="8330d-104">This topic describes how to create a forecast model for remaining budgets.</span></span> <span data-ttu-id="8330d-105">Un projecte que està subjecte al control pressupostari utilitza dos tipus de pressupostos: original i restant.</span><span class="sxs-lookup"><span data-stu-id="8330d-105">A project that is subject to budget control uses two types of budgets: original and remaining.</span></span> <span data-ttu-id="8330d-106">Quan creeu un pressupost de projecte, heu d'especificar els models de previsió del pressupost original i restant que es van crear en la pàgina **Models de previsió**.</span><span class="sxs-lookup"><span data-stu-id="8330d-106">When you create a project budget, you must specify the original and remaining budget forecast models that were created in the **Forecast models** page.</span></span> <span data-ttu-id="8330d-107">Els pressupostos del projecte basats en els models especificats es creen quan publiqueu el pressupost del projecte.</span><span class="sxs-lookup"><span data-stu-id="8330d-107">Project budgets based on the specified models are created when you commit the project budget.</span></span>

> [!NOTE]
> <span data-ttu-id="8330d-108">Un model de previsió que s'utilitza per al control pressupostari no pot tenir un submodel o utilitzar-se com a submodel.</span><span class="sxs-lookup"><span data-stu-id="8330d-108">A forecast model that is used for budget control can’t have a submodel or be used as a submodel.</span></span>

1. <span data-ttu-id="8330d-109">Seleccioneu **Administració de projectes i comptabilitat** > **Configuració** > **Previsions**  > **Models de previsió**.</span><span class="sxs-lookup"><span data-stu-id="8330d-109">Select **Project management and accounting** > **Setup** > **Forecasts**  > **Forecast models**.</span></span>
2. <span data-ttu-id="8330d-110">Seleccioneu **Nou** per crear un nou model de previsió i introduïu un número ID de model i un nom per al nou model.</span><span class="sxs-lookup"><span data-stu-id="8330d-110">Select **New** to create a new forecast model, and then enter a model ID number and name for the new model.</span></span> 
3. <span data-ttu-id="8330d-111">Definiu l'opció **Aturat** a **Sí** per evitar qualsevol canvi a les línies de previsió per al model de previsió.</span><span class="sxs-lookup"><span data-stu-id="8330d-111">Set the **Stopped** option to **Yes** to prevent any changes to the forecast lines for the forecast model.</span></span> 
4. <span data-ttu-id="8330d-112">Si les línies de previsió amb les quals està associat el model haurien de generar previsions de flux de caixa en el llibre major general, definiu **Inclou en les previsions de flux de caixa** a **Sí.**</span><span class="sxs-lookup"><span data-stu-id="8330d-112">If the forecast lines that the model is associated with should generate cash flow forecasts in the general ledger, set **Include in Cash flow forecasts** to **Yes.**</span></span> 
5. <span data-ttu-id="8330d-113">Per utilitzar la data del projecte com a data de la factura, definiu **Preveu la data de la factura** a **Sí**.</span><span class="sxs-lookup"><span data-stu-id="8330d-113">To use the project date as the invoice date, set **Forecast Invoice date** to **Yes**.</span></span> 
6. <span data-ttu-id="8330d-114">En el camp **Tipus de pressupost** , seleccioneu un dels següents tipus de model:</span><span class="sxs-lookup"><span data-stu-id="8330d-114">In the **Budget type** field, select one of the following model types:</span></span>

   - <span data-ttu-id="8330d-115">**Pressupost original** : utilitza els imports pressupostaris originals que s'han publicat quan es crea i aprova el pressupost inicial.</span><span class="sxs-lookup"><span data-stu-id="8330d-115">**Original budget** : Use the original budget amounts that are committed when the initial budget is created and approved.</span></span>
   - <span data-ttu-id="8330d-116">**Pressupost restant** : utilitza els imports pressupostaris restants durant la vida del projecte.</span><span class="sxs-lookup"><span data-stu-id="8330d-116">**Remaining budget** : Use the remaining budget amounts during the life of the project.</span></span> <span data-ttu-id="8330d-117">Els saldos d'aquest model de previsió es redueixen per transaccions reals i augmenten o disminueixen per revisions pressupostàries.</span><span class="sxs-lookup"><span data-stu-id="8330d-117">The balances in this forecast model are reduced by actual transactions and increased or decreased by budget revisions.</span></span>
   - <span data-ttu-id="8330d-118">**Transfereix** : utilitza els imports de transferència del pressupost per al projecte.</span><span class="sxs-lookup"><span data-stu-id="8330d-118">**Carry-forward** : Use the carry-forward budget amounts for the project.</span></span> <span data-ttu-id="8330d-119">La transferència és un procés opcional que pot executar-se per a transferir imports no utilitzats del pressupost d'un any fiscal a un altre.</span><span class="sxs-lookup"><span data-stu-id="8330d-119">Carry-forward is an optional process that can be run to transfer unused budget amounts from one fiscal year to another.</span></span>

7. <span data-ttu-id="8330d-120">Definiu les opcions següents segons sigui necessari:</span><span class="sxs-lookup"><span data-stu-id="8330d-120">Set the following options as required:</span></span>

   - <span data-ttu-id="8330d-121">Habiliteu **Preveu la data de la factura** per utilitzar la data del projecte com a data de la factura.</span><span class="sxs-lookup"><span data-stu-id="8330d-121">Enable **Forecast invoice date** to use the project date as the invoice date.</span></span>
   - <span data-ttu-id="8330d-122">Habiliteu **Previsió amb WIP** per fer la previsió segons el treball en curs (WIP) i seleccioneu el tipus de WIP.</span><span class="sxs-lookup"><span data-stu-id="8330d-122">Enable **Forecast with WIP** to forecast based on work in progress (WIP), and then select the type of WIP.</span></span> 
   - <span data-ttu-id="8330d-123">Podeu mantenir el **Tipus de pressupost** per defecte com a **Cap** o introduir un nou tipus.</span><span class="sxs-lookup"><span data-stu-id="8330d-123">You can keep the default **Budget type** as **None** or enter a new type.</span></span> <span data-ttu-id="8330d-124">El tipus de pressupost no es pot canviar després de canviar un registre.</span><span class="sxs-lookup"><span data-stu-id="8330d-124">The budget type can't be changed after you change a record.</span></span>     
    > [!NOTE]
    > <span data-ttu-id="8330d-125">Si canvieu el tipus de pressupost per defecte, totes les altres opcions no estaran disponibles per a les actualitzacions i no podeu reutilitzar aquest model de previsió.</span><span class="sxs-lookup"><span data-stu-id="8330d-125">If you change the default budget type, all other options will become unavailable for updates, and you can't reuse this forecast model.</span></span> 
   


 

