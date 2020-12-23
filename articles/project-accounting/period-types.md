---
title: Tipus de períodes
description: En aquest tema es proporciona informació sobre com configurar els tipus de períodes per a l'estimació dels ingressos.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6bcd988fbd074c66d64f7e327b4329d3de27e950
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531365"
---
# <a name="period-types"></a><span data-ttu-id="16f38-103">Tipus de períodes</span><span class="sxs-lookup"><span data-stu-id="16f38-103">Period types</span></span>

<span data-ttu-id="16f38-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_</span><span class="sxs-lookup"><span data-stu-id="16f38-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="16f38-105">Un tipus de període defineix la freqüència amb què es calculen els ingressos d'un projecte.</span><span class="sxs-lookup"><span data-stu-id="16f38-105">A period type defines how frequently revenue on a project is estimated.</span></span> <span data-ttu-id="16f38-106">En aquest tema es proporciona informació sobre com configurar els tipus de períodes per a l'estimació dels ingressos.</span><span class="sxs-lookup"><span data-stu-id="16f38-106">This topic provides information about how to set up period types for revenue estimation.</span></span> 

## <a name="create-and-work-with-period-types"></a><span data-ttu-id="16f38-107">Crear i treballar amb tipus de períodes</span><span class="sxs-lookup"><span data-stu-id="16f38-107">Create and work with period types</span></span>
<span data-ttu-id="16f38-108">Per crear i treballar amb tipus de períodes, seguiu aquests passos:</span><span class="sxs-lookup"><span data-stu-id="16f38-108">To create and work with period types, complete the following steps:</span></span>

1. <span data-ttu-id="16f38-109">A l'entorn del Dynamics 365 Finance, aneu a **Gestió de projectes i comptabilitat** > **Configuració** > **Estimacions** > **Tipus de períodes**.</span><span class="sxs-lookup"><span data-stu-id="16f38-109">In your Dynamics 365 Finance environment, go to **Project management and accounting** > **Setup** > **Estimates** > **Period types**.</span></span>
2. <span data-ttu-id="16f38-110">Seleccioneu **Crea** per crear un tipus de període nou.</span><span class="sxs-lookup"><span data-stu-id="16f38-110">Select **New** to create new period type.</span></span> <span data-ttu-id="16f38-111">Introduïu un nom i una descripció.</span><span class="sxs-lookup"><span data-stu-id="16f38-111">Enter a name and description.</span></span>
3. <span data-ttu-id="16f38-112">Al camp **Freqüència**, seleccioneu un valor:</span><span class="sxs-lookup"><span data-stu-id="16f38-112">In the **Frequency** field, select a value:</span></span>

    - <span data-ttu-id="16f38-113">Si seleccioneu **Setmana**, **Quinzena**, **Semimensual**, **Mes**, **Dia**, **Trimestre** o **Any**, el calendari s'utilitzarà per generar els períodes.</span><span class="sxs-lookup"><span data-stu-id="16f38-113">If you select **Week**, **Bi-weekly**, **Semi-monthly**, **Month**, **Day**, **Quarter**, or **Year**, the calendar will be used to generate the periods.</span></span> 
    - <span data-ttu-id="16f38-114">Si seleccioneu **Període comptable**, els períodes comptables de la configuració del llibre general s'utilitzaran per generar períodes.</span><span class="sxs-lookup"><span data-stu-id="16f38-114">If you select **Ledger period**, ledger periods from the General ledger configuration will be used to generate periods.</span></span>
    - <span data-ttu-id="16f38-115">Si seleccioneu **Il·limitat**, podeu especificar períodes personalitzats.</span><span class="sxs-lookup"><span data-stu-id="16f38-115">If you select **Unlimited**, you can specify custom periods.</span></span>
4. <span data-ttu-id="16f38-116">Seleccioneu el registre del tipus de període i, a continuació, seleccioneu **Genera períodes** per crear períodes per al tipus de període.</span><span class="sxs-lookup"><span data-stu-id="16f38-116">Select the period type record and then select **Generate periods** to create periods for the period type.</span></span> <span data-ttu-id="16f38-117">Segons la freqüència del període que hàgiu seleccionat, pot ser que tingueu l'opció d'especificar una data d'inici o el nombre de períodes que cal generar.</span><span class="sxs-lookup"><span data-stu-id="16f38-117">Based on the period frequency that you selected, you might have the option to specify a start date or the number of periods to generate.</span></span>
5. <span data-ttu-id="16f38-118">Seleccioneu **Períodes** per revisar els períodes generats.</span><span class="sxs-lookup"><span data-stu-id="16f38-118">Select **Periods** to review generated periods.</span></span>

