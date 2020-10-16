---
title: Comprensió de l'estat del projecte
description: En aquest tema es proporciona informació sobre l'estat assignat els projectes al Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 336e479ad39653af14cca7930fe63e906b7de489
ms.sourcegitcommit: fd8ea1779db2bb39a428f459ae3293c4fd785572
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/06/2020
ms.locfileid: "3965664"
---
# <a name="understand-project-status"></a><span data-ttu-id="67b30-103">Comprensió de l'estat del projecte</span><span class="sxs-lookup"><span data-stu-id="67b30-103">Understand project status</span></span>

<span data-ttu-id="67b30-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_</span><span class="sxs-lookup"><span data-stu-id="67b30-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="67b30-105">La secció **Estat** de la pàgina **Entitat del projecte** proporciona un resum de l'estat d'un projecte en funció del cost i l'esforç.</span><span class="sxs-lookup"><span data-stu-id="67b30-105">The **Status** section on the **Project Entity** page provides a summary of a project's health based upon cost and effort.</span></span>


## <a name="status-summary-fields"></a><span data-ttu-id="67b30-106">Camps de resum d'estat</span><span class="sxs-lookup"><span data-stu-id="67b30-106">Status summary fields</span></span>

- <span data-ttu-id="67b30-107">El camp **Estat global del projecte** és un camp editable que mostra l'estat general del projecte.</span><span class="sxs-lookup"><span data-stu-id="67b30-107">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="67b30-108">Aquest camp utilitza una codificació de color, com ara verd, groc i vermell, per indicar un risc cada vegada major.</span><span class="sxs-lookup"><span data-stu-id="67b30-108">This field uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> 
- <span data-ttu-id="67b30-109">El camp **Comentaris** permet a l'administrador del projecte introduir comentaris específics sobre l'estat.</span><span class="sxs-lookup"><span data-stu-id="67b30-109">The **Comments** field lets the project manager enter specific comments about the status.</span></span> 
- <span data-ttu-id="67b30-110">El camp **Data d'actualització de l'estat** no es pot editar.</span><span class="sxs-lookup"><span data-stu-id="67b30-110">The **Status updated on** field isn't editable.</span></span> <span data-ttu-id="67b30-111">El valor d'aquest camp és una marca de temps que indica quan s'ha actualitzat l'estat per última vegada.</span><span class="sxs-lookup"><span data-stu-id="67b30-111">The value in this field is a timestamp that indicates when the status was last updated.</span></span>
- <span data-ttu-id="67b30-112">Els camps **Rendiment de la programació** i **Rendiment del cost** es defineixen a partir de la quadrícula de seguiment.</span><span class="sxs-lookup"><span data-stu-id="67b30-112">The **Schedule performance** and **Cost performance** fields are set from the tracking grid.</span></span> <span data-ttu-id="67b30-113">Quan la variació de planificació i costos per al node arrel de la visualització **Seguiment de l'esforç** és positiva, aquests camps s'actualitzen a **Per davant**.</span><span class="sxs-lookup"><span data-stu-id="67b30-113">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, these fields are updated to **Ahead**.</span></span> <span data-ttu-id="67b30-114">Quan la variació de planificació i costos per al node arrel és negativa, aquests camps es defineixen a **Per darrere**.</span><span class="sxs-lookup"><span data-stu-id="67b30-114">When the schedule and cost variance for the root node are negative, these fields are set to **Behind**.</span></span>
