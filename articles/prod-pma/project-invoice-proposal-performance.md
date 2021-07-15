---
title: Rendiment de propostes de factura de projecte
description: Aquest tema proporciona informació sobre millores de rendiment a les propostes de factures de projectes.
author: Yowelle
ms.date: 06/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 20121-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 5a14acf51d277b16896d64c4b12ee00bfb326910
ms.sourcegitcommit: 3a4b181be08ef0428104d72b54a3e61ac2782f14
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/17/2021
ms.locfileid: "6269778"
---
# <a name="project-invoice-proposal-performance"></a><span data-ttu-id="6eb11-103">Rendiment de propostes de factura de projecte</span><span class="sxs-lookup"><span data-stu-id="6eb11-103">Project invoice proposal performance</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6eb11-104">Quan creeu una proposta de factura nova, és possible que trobeu problemes de rendiment a mesura que augmenti el nombre de projectes i subprojectes.</span><span class="sxs-lookup"><span data-stu-id="6eb11-104">When you create a new invoice proposal you might encounter performance issues as the number of projects and subprojects increase.</span></span> <span data-ttu-id="6eb11-105">Per millorar el rendiment, hi ha disponible una característica que redueix el temps necessari per crear una nova proposta de factura per a les transaccions de projectes comptabilitzades.</span><span class="sxs-lookup"><span data-stu-id="6eb11-105">To improve performance, a feature is available that reduces the time needed to create a new invoice proposal for posted project transactions.</span></span>

## <a name="enable-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="6eb11-106">Habilitar la millora del rendiment de la proposta de factura del projecte</span><span class="sxs-lookup"><span data-stu-id="6eb11-106">Enable project invoice proposal performance enhancement</span></span>
<span data-ttu-id="6eb11-107">Per habilitar la característica de millora del rendiment de la proposta de factura del projecte, seguiu els passos següents.</span><span class="sxs-lookup"><span data-stu-id="6eb11-107">To enable the project invoice proposal performance enhancement feature, complete the following steps.</span></span>

1.  <span data-ttu-id="6eb11-108">Aneu a **Administració de característiques** > **Totes**.</span><span class="sxs-lookup"><span data-stu-id="6eb11-108">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="6eb11-109">A la llista de característiques, localitzeu **Millora del rendiment de la proposta de factura del projecte**.</span><span class="sxs-lookup"><span data-stu-id="6eb11-109">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="6eb11-110">Seleccioneu **Habilita ara**.</span><span class="sxs-lookup"><span data-stu-id="6eb11-110">Select **Enable now**.</span></span>
3.  <span data-ttu-id="6eb11-111">Actualitzeu el navegador i, a continuació, creeu una proposta de factura nova.</span><span class="sxs-lookup"><span data-stu-id="6eb11-111">Refresh your browser, and then create a new invoice proposal.</span></span>

## <a name="turn-off-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="6eb11-112">Desactiveu la millora del rendiment de la proposta de factura del projecte</span><span class="sxs-lookup"><span data-stu-id="6eb11-112">Turn off project invoice proposal performance enhancement</span></span>
<span data-ttu-id="6eb11-113">Completeu els passos a continuació per desactivar la millora del rendiment de la proposta de factura del projecte.</span><span class="sxs-lookup"><span data-stu-id="6eb11-113">Complete the following steps to turn off the project invoice proposal performance enhancement.</span></span>

1.  <span data-ttu-id="6eb11-114">Aneu a **Administració de característiques** > **Totes**.</span><span class="sxs-lookup"><span data-stu-id="6eb11-114">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="6eb11-115">A la llista de característiques, localitzeu **Millora del rendiment de la proposta de factura del projecte**.</span><span class="sxs-lookup"><span data-stu-id="6eb11-115">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="6eb11-116">Seleccioneu **Inhabilita**.</span><span class="sxs-lookup"><span data-stu-id="6eb11-116">Select **Disable**.</span></span>
3.  <span data-ttu-id="6eb11-117">Actualitzeu el navegador.</span><span class="sxs-lookup"><span data-stu-id="6eb11-117">Refresh your browser.</span></span>

> [!NOTE]
> <span data-ttu-id="6eb11-118">Quan s'han habilitat les regles de facturació, el rendiment de proposta de factura no es pot aplicar.</span><span class="sxs-lookup"><span data-stu-id="6eb11-118">Invoice proposal performance can't be applied when billing rules are enabled.</span></span>
> 
> <span data-ttu-id="6eb11-119">Durant el procés per lots per crear propostes de factures, el nombre de subtasques dividirà les tasques en un nombre màxim segons el nombre de contractes amb transaccions facturables, independentment de què s'hagi introduït.</span><span class="sxs-lookup"><span data-stu-id="6eb11-119">During the batch process to create invoice proposals, the number of subtasks will split the tasks to a maximum number based on the number of contracts with invoiceable transactions, regardless of what you have entered.</span></span> <span data-ttu-id="6eb11-120">Per exemple, si introduïu **3** com a nombre de subtasques per a la creació de propostes de factures en un lot i només hi ha dos contractes amb transaccions facturables, només es creen dues subtasques.</span><span class="sxs-lookup"><span data-stu-id="6eb11-120">For example, if you enter **3** for the number of subtasks for invoice proposal creation in batch, and there are only two contracts with invoiceable transactions, only two subtasks are created.</span></span>
