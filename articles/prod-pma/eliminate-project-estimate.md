---
title: Supressió d'una estimació de projecte
description: Aquest tema proporciona informació sobre la supressió d'una estimació del projecte després que s'hagi completat.
author: Yowelle
manager: AnnBe
ms.date: 05/26/2020
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
ms.openlocfilehash: 000eabdac41f30a6e7dd37e34b8fd91d7c51f6c4
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5270666"
---
# <a name="eliminate-a-project-estimate"></a><span data-ttu-id="2d9a9-103">Supressió d'una estimació de projecte</span><span class="sxs-lookup"><span data-stu-id="2d9a9-103">Eliminate a project estimate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2d9a9-104">Les estimacions de projecte proporcionen informació visual financera del treball que està previst i planificat per a un projecte.</span><span class="sxs-lookup"><span data-stu-id="2d9a9-104">Project estimates provide the financial view for work that is estimated and scheduled for a project.</span></span> <span data-ttu-id="2d9a9-105">Per treballar amb les estimacions d'un projecte, heu d'adjuntar el projecte a un projecte estimat.</span><span class="sxs-lookup"><span data-stu-id="2d9a9-105">To work with estimates for a project, you must attach the project to an estimate project.</span></span> <span data-ttu-id="2d9a9-106">Un projecte estimat es basa sempre en un projecte existent, però diversos projectes poden fer referència a un únic projecte estimat.</span><span class="sxs-lookup"><span data-stu-id="2d9a9-106">An estimate project is always based on an existing project, however multiple projects can refer to a single estimate project.</span></span> <span data-ttu-id="2d9a9-107">Només es poden adjuntar projectes de preu fix i d'inversió a projectes estimats i aquests projectes han de pertànyer al mateix grup de projectes que el projecte estimat.</span><span class="sxs-lookup"><span data-stu-id="2d9a9-107">Only fixed-price and investment projects can be attached to estimate projects, and those projects must belong to the same project group as the estimate project.</span></span>

<span data-ttu-id="2d9a9-108">Per suprimir un projecte estimat, s'ha de completar.</span><span class="sxs-lookup"><span data-stu-id="2d9a9-108">To eliminate an estimate project, it must be complete.</span></span> <span data-ttu-id="2d9a9-109">Els passos següents expliquen com suprimir una estimació.</span><span class="sxs-lookup"><span data-stu-id="2d9a9-109">The following steps explain how to eliminate an estimate.</span></span>

1. <span data-ttu-id="2d9a9-110">Aneu a **Administració de projectes i comptabilitat** > **Tots els projectes** i obriu el projecte.</span><span class="sxs-lookup"><span data-stu-id="2d9a9-110">Go to **Project management and accounting** > **All Projects** and open the project.</span></span> 
2. <span data-ttu-id="2d9a9-111">A la pestanya **Administra**, seleccioneu **Estimacions** i, a la pàgina **Estimació**, seleccioneu **Elimina**.</span><span class="sxs-lookup"><span data-stu-id="2d9a9-111">On the **Manage** tab, select **Estimates**, and on the **Estimate** page select **Eliminate**.</span></span>
3. <span data-ttu-id="2d9a9-112">A la pestanya **Elimina l'estimació** a la pestanya **General**, definiu les següents opcions:</span><span class="sxs-lookup"><span data-stu-id="2d9a9-112">On the **Eliminate estimate** page on the **General** tab, set the following options:</span></span>

   - <span data-ttu-id="2d9a9-113">**Codi de període**: seleccioneu el codi del període per triar els projectes estimats pertinents.</span><span class="sxs-lookup"><span data-stu-id="2d9a9-113">**Period code**: Select the period code to choose the appropriate estimate projects.</span></span> 
   - <span data-ttu-id="2d9a9-114">**Data estimada**: seleccioneu la data estimada apropiada per a l'eliminació.</span><span class="sxs-lookup"><span data-stu-id="2d9a9-114">**Estimate date**: Select the appropriate estimate date for elimination.</span></span>
   - <span data-ttu-id="2d9a9-115">**Avisos d'eliminació amb WIP**: habiliteu aquesta opció per proporcionar una notificació quan s'elimini una estimació associada amb un treball en curs (WIP).</span><span class="sxs-lookup"><span data-stu-id="2d9a9-115">**Eliminate with WIP warnings**: Enable this option to provide notification when an estimate that is associated with a work in progress (WIP) will be eliminated.</span></span> <span data-ttu-id="2d9a9-116">Quan aquesta opció no està habilitada, l'eliminació no pot continuar si existeixen transaccions no estimades.</span><span class="sxs-lookup"><span data-stu-id="2d9a9-116">When this option is not enabled, elimination can’t continue if any non-estimated transactions exist.</span></span> 
   > [!NOTE]
   > <span data-ttu-id="2d9a9-117">Aquesta opció només està disponible quan s'aplica l'eliminació a un projecte estimat.</span><span class="sxs-lookup"><span data-stu-id="2d9a9-117">This option is available only when elimination is applied to an estimate project.</span></span> <span data-ttu-id="2d9a9-118">No està disponible si utilitzeu comptabilitzacions periòdiques.</span><span class="sxs-lookup"><span data-stu-id="2d9a9-118">It is not available if you are using periodic postings.</span></span> <span data-ttu-id="2d9a9-119">Aquest paràmetre funciona amb els paràmetres de la pestanya **Estimació** a la pestanya **Paràmetres del projecte**, al grup de camps **Permet l'eliminació quan hi ha transaccions no estimades**.</span><span class="sxs-lookup"><span data-stu-id="2d9a9-119">This setting works with the settings on the **Estimate** tab on the **Project parameters** page, in the **Allow elimination when non-estimated transactions exist** field group.</span></span>
   - <span data-ttu-id="2d9a9-120">**Defineix la fase a Finalitzat**: habiliteu aquesta opció per establir la fase del projecte estimat a **Finalitzat** després d'executar l'eliminació.</span><span class="sxs-lookup"><span data-stu-id="2d9a9-120">**Set stage to Finished**: Enable this option to set the estimate project’s stage to **Finished** after you run the elimination.</span></span>
   - <span data-ttu-id="2d9a9-121">**Imprimeix la llista d'estimació**: seleccioneu la informació que s'inclourà quan s'imprimeixi la llista d'estimació.</span><span class="sxs-lookup"><span data-stu-id="2d9a9-121">**Print estimate list**: Select the information to be included when the estimate list is printed.</span></span>
   - <span data-ttu-id="2d9a9-122">**Mostra el registre d'informació**: habiliteu aquesta opció per mostrar el registre d'informació.</span><span class="sxs-lookup"><span data-stu-id="2d9a9-122">**Show Infolog**: Enable this option to display the Infolog.</span></span>
   - <span data-ttu-id="2d9a9-123">**Data de comptabilització**: trieu la data de comptabilització al llibre major de l'estimació.</span><span class="sxs-lookup"><span data-stu-id="2d9a9-123">**Posting date**: Choose the ledger posting date of the estimate.</span></span>

4.  <span data-ttu-id="2d9a9-124">Seleccioneu **D'acord**.</span><span class="sxs-lookup"><span data-stu-id="2d9a9-124">Select **OK**.</span></span>
5. <span data-ttu-id="2d9a9-125">Després de completar el procés d'eliminació, el projecte estimat eliminat es mostra amb un valor negatiu.</span><span class="sxs-lookup"><span data-stu-id="2d9a9-125">After the elimination process is complete, the eliminated estimate project is displayed with a negative value.</span></span> 

<span data-ttu-id="2d9a9-126">Si no teniu la intenció d'eliminar una estimació, podeu seleccionar l'estimació eliminada i seleccionar **Desfés l'eliminació**.</span><span class="sxs-lookup"><span data-stu-id="2d9a9-126">If you did not intend to eliminate an estimate, you can select the eliminated estimate and select **Reverse elimination**.</span></span>   


[!INCLUDE[footer-include](../includes/footer-banner.md)]