---
title: Despeses entre empreses
description: En aquest tema es proporciona informació sobre com utilitzar les despeses entre empreses per assignar les despeses d'un treballador a l'entitat legal per a la qual es va dur a terme la feina.
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
ms.openlocfilehash: d908a1c062f5b7f01cf340dcd6f7f24714a992bf
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271521"
---
# <a name="intercompany-expenses"></a><span data-ttu-id="294db-103">Despeses entre empreses</span><span class="sxs-lookup"><span data-stu-id="294db-103">Intercompany expenses</span></span>

<span data-ttu-id="294db-104">Un treballador que estigui contractat per una entitat jurídica en una organització pot treballar per a una altra entitat jurídica de la mateixa organització.</span><span class="sxs-lookup"><span data-stu-id="294db-104">A worker who is employed by one legal entity in an organization might perform work for another legal entity in the same organization.</span></span> <span data-ttu-id="294db-105">Podeu utilitzar les despeses entre empreses per assignar les despeses del treballador a l'entitat legal per a la qual es va dur a terme la feina.</span><span class="sxs-lookup"><span data-stu-id="294db-105">You can use intercompany expenses to assign the worker’s expenses to the legal entity for which the  work was performed.</span></span> <span data-ttu-id="294db-106">L'entitat jurídica que dona feina al treballador s'anomena entitat jurídica prestadora.</span><span class="sxs-lookup"><span data-stu-id="294db-106">The legal entity that employs the worker is called the loaning legal entity.</span></span> <span data-ttu-id="294db-107">L'entitat jurídica per a la qual el treballador incorre despeses s'anomena entitat jurídica prestatària.</span><span class="sxs-lookup"><span data-stu-id="294db-107">The legal entity for which the worker incurs expenses is called the borrowing legal entity.</span></span> 

<span data-ttu-id="294db-108">Perquè un treballador pugui crear i enviar despeses entre empreses, abans heu d'habilitar les línies de despeses entre empreses.</span><span class="sxs-lookup"><span data-stu-id="294db-108">Before a worker can create and submit intercompany expenses, you must enable intercompany expense lines.</span></span> <span data-ttu-id="294db-109">A l'entitat legal que fa el préstec, a la pàgina **Paràmetres d'administració de despeses**, seleccioneu **Permet les línies de despeses entre empreses**.</span><span class="sxs-lookup"><span data-stu-id="294db-109">In the loaning legal entity, on the **Expense management parameters** page, select **Allow intercompany expense lines**.</span></span> 

## <a name="tax-posting-for-intercompany-expenses"></a><span data-ttu-id="294db-110">Comptabilització d'impostos per a despeses entre empreses</span><span class="sxs-lookup"><span data-stu-id="294db-110">Tax posting for intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="294db-111">Per poder utilitzar els grups d'impostos associats a l'entitat legal que fa el préstec (origen) en comptes de l'entitat legal que rep el préstec (destinació) de l'informe de despeses, heu d'habilitar la funcionalitat a la configuració de l'impost de vendes del llibre general.</span><span class="sxs-lookup"><span data-stu-id="294db-111">Before you can use tax groups that are associated with the loaning (source) legal entity instead of the borrowing (destination) legal entity in your expense report, you must enable the functionality in the General ledger sales tax setup.</span></span> <span data-ttu-id="294db-112">Quan el paràmetre **entitat legal per a la publicació d'impostos entre empreses** es defineix com a **Origen** i **Aplica les regles de fiscalitat per a les vendes** es defineix com a **No**, s'utilitza la combinació d'impostos de l'entitat legal que fa el préstec.</span><span class="sxs-lookup"><span data-stu-id="294db-112">When the **Legal entity for intercompany tax posting** parameter is set to **Source** and **Apply sales tax taxation rules** is set to **No**, the tax combination for the loaning legal entity is used.</span></span> <span data-ttu-id="294db-113">Quan s'estableix el mateix paràmetre a **Destinació**, s'utilitzarà la combinació d'impostos per a l'entitat jurídica prestatària.</span><span class="sxs-lookup"><span data-stu-id="294db-113">When the same parameter is set to **Destination**, the tax combination for borrowing legal entity will be used.</span></span> <span data-ttu-id="294db-114">Per a les entitats jurídiques dels Estats Units, quan el paràmetre s'estableix a **Origen**, el camp **Es pot rebre l'impost de vendes** també s'ha de configurar a la nova pàgina **Grups de comptabilització del llibre major**.</span><span class="sxs-lookup"><span data-stu-id="294db-114">For legal entities in the United States, when the parameter is set to **Source**, the **Sales tax receivable** field must also be configured on the new **Ledger posting groups** page.</span></span> <span data-ttu-id="294db-115">El motor de comptabilitat utilitzarà la informació d'aquest camp per a l'entrada de la comptabilitat relacionada amb els impostos.</span><span class="sxs-lookup"><span data-stu-id="294db-115">The accounting engine will use the information from this field for tax-related accounting entry.</span></span>   
<span data-ttu-id="294db-116">El comportament és coherent per a les línies de despesa publicades amb o sense un projecte.</span><span class="sxs-lookup"><span data-stu-id="294db-116">The behavior is consistent for expense lines posted with or without a project.</span></span>  


[!INCLUDE[footer-include](../includes/footer-banner.md)]