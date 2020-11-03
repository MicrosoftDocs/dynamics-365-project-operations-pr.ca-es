---
title: Despeses entre empreses
description: Un treballador que estigui contractat per una entitat jurídica en una organització pot treballar per a una altra entitat jurídica de la mateixa organització. En aquesta situació, es pot utilitzar la funció de despesa entre empreses per assignar les despeses del treballador a l'entitat jurídica per a la qual es va realitzar el treball.
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072363"
---
# <a name="intercompany-expenses"></a><span data-ttu-id="63e19-104">Despeses entre empreses</span><span class="sxs-lookup"><span data-stu-id="63e19-104">Intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="63e19-105">Un treballador que estigui contractat per una entitat jurídica en una organització pot treballar per a una altra entitat jurídica de la mateixa organització.</span><span class="sxs-lookup"><span data-stu-id="63e19-105">A worker who is employed by one legal entity in an organization might perform work for another legal entity in the same organization.</span></span> <span data-ttu-id="63e19-106">En aquesta situació, es pot utilitzar la funció de despesa entre empreses per assignar les despeses del treballador a l'entitat jurídica per a la qual es va realitzar el treball.</span><span class="sxs-lookup"><span data-stu-id="63e19-106">In this situation, you can use the intercompany expense feature to assign the worker’s expenses to the legal entity for which the work was performed.</span></span> <span data-ttu-id="63e19-107">L'entitat jurídica que dona feina al treballador s'anomena entitat jurídica prestadora.</span><span class="sxs-lookup"><span data-stu-id="63e19-107">The legal entity that employs the worker is called the loaning legal entity.</span></span> <span data-ttu-id="63e19-108">L'entitat jurídica per a la qual el treballador incorre despeses s'anomena entitat jurídica prestatària.</span><span class="sxs-lookup"><span data-stu-id="63e19-108">The legal entity for which the worker incurs expenses is called the borrowing legal entity.</span></span> 

<span data-ttu-id="63e19-109">Abans que un treballador pugui crear i presentar despeses per al treball que es realitza per a una entitat jurídica diferent, a l'entitat jurídica prestadora, a l'opció **Paràmetres d'administració de despeses** , seleccioneu l'opció **Permet les línies de despesa entre empreses**.</span><span class="sxs-lookup"><span data-stu-id="63e19-109">Before a worker can create and submit expenses for work that is performed for a different legal entity, in the loaning legal entity, on the **Expense management parameters** page, select the **Allow intercompany expense lines** option.</span></span> 

## <a name="tax-posting-for-intercompany-expenses"></a><span data-ttu-id="63e19-110">Comptabilització d'impostos per a despeses entre empreses</span><span class="sxs-lookup"><span data-stu-id="63e19-110">Tax posting for intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="63e19-111">Si voleu utilitzar grups d'impostos que estan associats amb l'entitat jurídica prestadora (origen) en lloc de l'entitat jurídica prestatària (destinació) en el vostre informe de despeses, haureu de configurar-ho a la configuració d'impostos de vendes del llibre major general.</span><span class="sxs-lookup"><span data-stu-id="63e19-111">If you want to use tax groups that are associated with the loaning (source) legal entity instead of the borrowing (destination) legal entity in your expense report, you will need to configure this in the General ledger sales tax set up.</span></span> <span data-ttu-id="63e19-112">Quan el paràmetre del llibre major general **Entitat jurídica per a la comptabilització d'impostos entre empreses** s'estableix a **Origen** i **Aplica les regles d'impostos de vendes** s'estableix a **No** , s'utilitzarà la combinació d'impostos per a l'entitat jurídica prestadora.</span><span class="sxs-lookup"><span data-stu-id="63e19-112">When the General ledger parameter, **Legal entity for intercompany tax posting** is set to **Source** and **Apply sales tax taxation rules** is set to **No** , the tax combination for the loaning legal entity will be used.</span></span> <span data-ttu-id="63e19-113">Quan s'estableix el mateix paràmetre a **Destinació** , s'utilitzarà la combinació d'impostos per a l'entitat jurídica prestatària.</span><span class="sxs-lookup"><span data-stu-id="63e19-113">When the same parameter is set to **Destination** , the tax combination for borrowing legal entity will be used.</span></span> <span data-ttu-id="63e19-114">Per a les entitats jurídiques dels Estats Units, quan el paràmetre s'estableix a **Origen** , el camp **Es pot rebre l'impost de vendes** també s'ha de configurar a la nova pàgina **Grups de comptabilització del llibre major**.</span><span class="sxs-lookup"><span data-stu-id="63e19-114">For legal entities in the United States, when the parameter is set to **Source** , the **Sales tax receivable** field must also be configured on the new **Ledger posting groups** page.</span></span> <span data-ttu-id="63e19-115">El motor de comptabilitat utilitzarà la informació d'aquest camp per a l'entrada de la comptabilitat relacionada amb els impostos.</span><span class="sxs-lookup"><span data-stu-id="63e19-115">The accounting engine will use the information from this field for tax related accounting entry.</span></span>   
<span data-ttu-id="63e19-116">El comportament és coherent per a les línies de despesa publicades amb o sense un projecte.</span><span class="sxs-lookup"><span data-stu-id="63e19-116">The behavior is consistent for expense lines posted with or without a project.</span></span>  
