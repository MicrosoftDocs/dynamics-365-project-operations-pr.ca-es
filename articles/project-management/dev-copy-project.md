---
title: Desenvolupament de plantilles de projecte amb la característica Copia el projecte
description: En aquest tema es proporciona informació sobre com crear plantilles de projecte mitjançant l'acció personalitzada Copia el projecte.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 22976730ef3c8c22ea028b27a6eb5f14fb88993e
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642396"
---
# <a name="develop-project-templates-with-copy-project"></a><span data-ttu-id="67cc5-103">Desenvolupament de plantilles de projecte amb la característica Copia el projecte</span><span class="sxs-lookup"><span data-stu-id="67cc5-103">Develop project templates with Copy Project</span></span>

<span data-ttu-id="67cc5-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_</span><span class="sxs-lookup"><span data-stu-id="67cc5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="67cc5-105">Dynamics 365 Project Operations és compatible amb la capacitat de copiar un projecte i revertir les assignacions als recursos genèrics que representen la funció.</span><span class="sxs-lookup"><span data-stu-id="67cc5-105">Dynamics 365 Project Operations supports the ability to copy a project and revert any assignments back to the generic resources that represent the role.</span></span> <span data-ttu-id="67cc5-106">Els clients poden utilitzar aquesta funcionalitat per crear plantilles de projecte bàsiques.</span><span class="sxs-lookup"><span data-stu-id="67cc5-106">Customers can use this functionality to build basic project templates.</span></span>

<span data-ttu-id="67cc5-107">Quan seleccioneu **Copia el projecte**, l'estat del projecte de destinació s'actualitza.</span><span class="sxs-lookup"><span data-stu-id="67cc5-107">When you select **Copy Project**, the status of the target project is updated.</span></span> <span data-ttu-id="67cc5-108">Utilitzeu **Raó per a l'estat** per determinar quan ha finalitzat l'acció de còpia.</span><span class="sxs-lookup"><span data-stu-id="67cc5-108">Use **Status Reason** to determine when the copy action is complete.</span></span> <span data-ttu-id="67cc5-109">En seleccionar **Copia el projecte** també s'actualitza la data d'inici del projecte a la data d'inici actual si no es detecta cap data de la destinació a l'entitat del projecte de destinació.</span><span class="sxs-lookup"><span data-stu-id="67cc5-109">Selecting **Copy Project** also updates the start date of the project to the current start date if no target date is detected in the target project entity.</span></span>

## <a name="copy-project-custom-action"></a><span data-ttu-id="67cc5-110">Acció personalitzada Copia el projecte</span><span class="sxs-lookup"><span data-stu-id="67cc5-110">Copy Project custom action</span></span> 

### <a name="name"></a><span data-ttu-id="67cc5-111">Nom</span><span class="sxs-lookup"><span data-stu-id="67cc5-111">Name</span></span> 

<span data-ttu-id="67cc5-112">**msdyn_CopyProjectV2**</span><span class="sxs-lookup"><span data-stu-id="67cc5-112">**msdyn_CopyProjectV2**</span></span>

### <a name="input-parameters"></a><span data-ttu-id="67cc5-113">Paràmetres d’entrada</span><span class="sxs-lookup"><span data-stu-id="67cc5-113">Input parameters</span></span>
<span data-ttu-id="67cc5-114">Hi ha tres paràmetres d'entrada:</span><span class="sxs-lookup"><span data-stu-id="67cc5-114">There are three input parameters:</span></span>

| <span data-ttu-id="67cc5-115">Paràmetre</span><span class="sxs-lookup"><span data-stu-id="67cc5-115">Parameter</span></span>          | <span data-ttu-id="67cc5-116">Type</span><span class="sxs-lookup"><span data-stu-id="67cc5-116">Type</span></span>   | <span data-ttu-id="67cc5-117">Valors</span><span class="sxs-lookup"><span data-stu-id="67cc5-117">Values</span></span>                                                   | 
|--------------------|--------|----------------------------------------------------------|
| <span data-ttu-id="67cc5-118">ProjectCopyOption</span><span class="sxs-lookup"><span data-stu-id="67cc5-118">ProjectCopyOption</span></span>  | <span data-ttu-id="67cc5-119">String</span><span class="sxs-lookup"><span data-stu-id="67cc5-119">String</span></span> | <span data-ttu-id="67cc5-120">**{"removeNamedResources":true}** o **{"clearTeamsAndAssignments":true}**</span><span class="sxs-lookup"><span data-stu-id="67cc5-120">**{"removeNamedResources":true}** or **{"clearTeamsAndAssignments":true}**</span></span> |
| <span data-ttu-id="67cc5-121">SourceProject</span><span class="sxs-lookup"><span data-stu-id="67cc5-121">SourceProject</span></span>      | <span data-ttu-id="67cc5-122">Referència d’entitat</span><span class="sxs-lookup"><span data-stu-id="67cc5-122">Entity Reference</span></span> | <span data-ttu-id="67cc5-123">Projecte d'origen</span><span class="sxs-lookup"><span data-stu-id="67cc5-123">Source Project</span></span> |
| <span data-ttu-id="67cc5-124">Objectiu</span><span class="sxs-lookup"><span data-stu-id="67cc5-124">Target</span></span>             | <span data-ttu-id="67cc5-125">Referència d’entitat</span><span class="sxs-lookup"><span data-stu-id="67cc5-125">Entity Reference</span></span> | <span data-ttu-id="67cc5-126">Projecte de destinació</span><span class="sxs-lookup"><span data-stu-id="67cc5-126">Target Project</span></span> |


- <span data-ttu-id="67cc5-127">**{"clearTeamsAndAssignments":true}** : comportament per defecte d'un projecte per al web, i suprimirà totes les assignacions i membres de l'equip.</span><span class="sxs-lookup"><span data-stu-id="67cc5-127">**{"clearTeamsAndAssignments":true}**: Thee default behavior for Project for the Web, and will remove all assignments and team members.</span></span>
- <span data-ttu-id="67cc5-128">**{"removeNamedResources":true}** comportament per defecte del Project Operations, i revertirà les assignacions a recursos genèrics.</span><span class="sxs-lookup"><span data-stu-id="67cc5-128">**{"removeNamedResources":true}** The default behavior for Project Operations, and will revert assignments to generic resources.</span></span>

<span data-ttu-id="67cc5-129">Per veure més valors per defecte en accions, vegeu [Utilitzar les accions de l'API web](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span><span class="sxs-lookup"><span data-stu-id="67cc5-129">For more defaults on actions, see [Use Web API actions](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span></span>

## <a name="specify-fields-to-copy"></a><span data-ttu-id="67cc5-130">Especificar els camps que es copiaran</span><span class="sxs-lookup"><span data-stu-id="67cc5-130">Specify fields to copy</span></span> 
<span data-ttu-id="67cc5-131">Quan es crida l'acció, **Copia el projecte** consultarà la visualització del projecte **Copia les columnes del projecte** per determinar quins camps s'han de copiar quan es copia el projecte.</span><span class="sxs-lookup"><span data-stu-id="67cc5-131">When the action is called, **Copy Project** will look at the project view **Copy Project Columns** to determine which fields to copy when the project is copied.</span></span>
