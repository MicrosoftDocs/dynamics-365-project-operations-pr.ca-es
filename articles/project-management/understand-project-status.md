---
title: Comprensió de l'estat del projecte
description: En aquest tema es proporciona informació sobre l'estat assignat als projectes al Dynamics 365 Project Operations.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: ad8c012b93bc65595dca33df1770562916c557e0
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993404"
---
# <a name="understand-project-status"></a><span data-ttu-id="31749-103">Comprensió de l'estat del projecte</span><span class="sxs-lookup"><span data-stu-id="31749-103">Understand project status</span></span>

<span data-ttu-id="31749-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_</span><span class="sxs-lookup"><span data-stu-id="31749-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="31749-105">La secció **Estat** de la pàgina **Entitat del projecte** proporciona un resum de l'estat d'un projecte segons el cost i l'esforç.</span><span class="sxs-lookup"><span data-stu-id="31749-105">The **Status** section on the **Project Entity** page provides a summary of a project's health based upon cost and effort.</span></span>


## <a name="status-summary-fields"></a><span data-ttu-id="31749-106">Camps de resum d'estat</span><span class="sxs-lookup"><span data-stu-id="31749-106">Status summary fields</span></span>

- <span data-ttu-id="31749-107">El camp **Estat global del projecte** és un camp editable que mostra l'estat general del projecte.</span><span class="sxs-lookup"><span data-stu-id="31749-107">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="31749-108">Aquest camp utilitza una codificació de color, com ara verd, groc i vermell, per indicar un risc cada vegada major.</span><span class="sxs-lookup"><span data-stu-id="31749-108">This field uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> 
- <span data-ttu-id="31749-109">El camp **Comentaris** permet a l'administrador del projecte introduir comentaris específics sobre l'estat.</span><span class="sxs-lookup"><span data-stu-id="31749-109">The **Comments** field lets the project manager enter specific comments about the status.</span></span> 
- <span data-ttu-id="31749-110">El camp **Data d'actualització de l'estat** no és editable.</span><span class="sxs-lookup"><span data-stu-id="31749-110">The **Status updated on** field isn't editable.</span></span> <span data-ttu-id="31749-111">El valor d'aquest camp és una marca de temps que indica quan s'ha actualitzat l'estat per última vegada.</span><span class="sxs-lookup"><span data-stu-id="31749-111">The value in this field is a timestamp that indicates when the status was last updated.</span></span>
- <span data-ttu-id="31749-112">Els camps **Rendiment de la planificació** i **Rendiment del cost** s'estableixen a partir de la quadrícula de seguiment.</span><span class="sxs-lookup"><span data-stu-id="31749-112">The **Schedule performance** and **Cost performance** fields are set from the tracking grid.</span></span> <span data-ttu-id="31749-113">Quan la variació de planificació i costos per al node arrel de la visualització **Seguiment de l'esforç** és positiva, aquests camps s'actualitzen a **Per davant**.</span><span class="sxs-lookup"><span data-stu-id="31749-113">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, these fields are updated to **Ahead**.</span></span> <span data-ttu-id="31749-114">Quan la variació de planificació i costos per al node arrel és negativa, aquests camps es defineixen a **Per darrere**.</span><span class="sxs-lookup"><span data-stu-id="31749-114">When the schedule and cost variance for the root node are negative, these fields are set to **Behind**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]