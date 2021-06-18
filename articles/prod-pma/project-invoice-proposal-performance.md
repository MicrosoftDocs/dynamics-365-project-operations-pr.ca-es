---
title: Rendiment de propostes de factura de projecte
description: Aquest tema proporciona informació sobre millores de rendiment a les propostes de factures de projectes.
author: Yowelle
ms.date: 04/20/2021
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
ms.openlocfilehash: 0e7a9eedc80a88e80b7788be4fe4b2f969be8ba1
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999479"
---
# <a name="project-invoice-proposal-performance"></a><span data-ttu-id="d2a7d-103">Rendiment de propostes de factura de projecte</span><span class="sxs-lookup"><span data-stu-id="d2a7d-103">Project invoice proposal performance</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d2a7d-104">Quan creeu una proposta de factura nova, és possible que trobeu problemes de rendiment a mesura que augmenti el nombre de projectes i subprojectes.</span><span class="sxs-lookup"><span data-stu-id="d2a7d-104">When you create a new invoice proposal you might encounter performance issues as the number of projects and subprojects increase.</span></span> <span data-ttu-id="d2a7d-105">Per millorar el rendiment, hi ha disponible una característica que redueix el temps necessari per crear una nova proposta de factura per a les transaccions de projectes comptabilitzades.</span><span class="sxs-lookup"><span data-stu-id="d2a7d-105">To improve performance, a feature is available that reduces the time needed to create a new invoice proposal for posted project transactions.</span></span>

## <a name="enable-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="d2a7d-106">Habilitar la millora del rendiment de la proposta de factura del projecte</span><span class="sxs-lookup"><span data-stu-id="d2a7d-106">Enable project invoice proposal performance enhancement</span></span>
<span data-ttu-id="d2a7d-107">Per habilitar la característica de millora del rendiment de la proposta de factura del projecte, seguiu els passos següents.</span><span class="sxs-lookup"><span data-stu-id="d2a7d-107">To enable the project invoice proposal performance enhancement feature, complete the following steps.</span></span>

1.  <span data-ttu-id="d2a7d-108">Aneu a **Administració de característiques** > **Totes**.</span><span class="sxs-lookup"><span data-stu-id="d2a7d-108">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="d2a7d-109">A la llista de característiques, localitzeu **Millora del rendiment de la proposta de factura del projecte**.</span><span class="sxs-lookup"><span data-stu-id="d2a7d-109">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="d2a7d-110">Seleccioneu **Habilita ara**.</span><span class="sxs-lookup"><span data-stu-id="d2a7d-110">Select **Enable now**.</span></span>
3.  <span data-ttu-id="d2a7d-111">Actualitzeu el navegador i, a continuació, creeu una proposta de factura nova.</span><span class="sxs-lookup"><span data-stu-id="d2a7d-111">Refresh your browser, and then create a new invoice proposal.</span></span>

## <a name="turn-off-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="d2a7d-112">Desactiveu la millora del rendiment de la proposta de factura del projecte</span><span class="sxs-lookup"><span data-stu-id="d2a7d-112">Turn off project invoice proposal performance enhancement</span></span>
<span data-ttu-id="d2a7d-113">Completeu els passos a continuació per desactivar la millora del rendiment de la proposta de factura del projecte.</span><span class="sxs-lookup"><span data-stu-id="d2a7d-113">Complete the following steps to turn off the project invoice proposal performance enhancement.</span></span>

1.  <span data-ttu-id="d2a7d-114">Aneu a **Administració de característiques** > **Totes**.</span><span class="sxs-lookup"><span data-stu-id="d2a7d-114">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="d2a7d-115">A la llista de característiques, localitzeu **Millora del rendiment de la proposta de factura del projecte**.</span><span class="sxs-lookup"><span data-stu-id="d2a7d-115">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="d2a7d-116">Seleccioneu **Inhabilita**.</span><span class="sxs-lookup"><span data-stu-id="d2a7d-116">Select **Disable**.</span></span>
3.  <span data-ttu-id="d2a7d-117">Actualitzeu el navegador.</span><span class="sxs-lookup"><span data-stu-id="d2a7d-117">Refresh your browser.</span></span>

> [!NOTE]
> <span data-ttu-id="d2a7d-118">El rendiment de la proposta de factura no es pot aplicar quan les regles de facturació estan habilitades o els processos per lots s'estan executant.</span><span class="sxs-lookup"><span data-stu-id="d2a7d-118">Invoice proposal performance can't be applied when billing rules are enabled or batch processes are running.</span></span>
