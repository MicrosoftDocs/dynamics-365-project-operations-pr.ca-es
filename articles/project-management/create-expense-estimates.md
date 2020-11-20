---
title: Estimacions de despeses
description: En aquest tema s'ofereix informació sobre la definició o estimació de les despeses basades en el projecte.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 10872366453985561bda0c07e50cff7f5f6d333e
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131691"
---
# <a name="expense-estimates"></a><span data-ttu-id="7e786-103">Estimacions de despeses</span><span class="sxs-lookup"><span data-stu-id="7e786-103">Expense estimates</span></span>
<span data-ttu-id="7e786-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_</span><span class="sxs-lookup"><span data-stu-id="7e786-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="7e786-105">Juntament amb la definició d'estimacions basades en recursos, el Dynamics 365 Project Operations permet als administradors de projectes definir les despeses basades en projectes per a cada projecte.</span><span class="sxs-lookup"><span data-stu-id="7e786-105">Along with defining resource-based estimates, Dynamics 365 Project Operations allows Project managers to define project-based expenses for each project.</span></span> <span data-ttu-id="7e786-106">Cada element de despesa es pot associar amb una tasca del projecte o categoria de despesa concreta.</span><span class="sxs-lookup"><span data-stu-id="7e786-106">Each expense item can be associated with a specific project task or expense category.</span></span> <span data-ttu-id="7e786-107">Les categories de despesa es defineixen típicament a nivell organitzatiu.</span><span class="sxs-lookup"><span data-stu-id="7e786-107">Expense categories are typically defined at the organizational level.</span></span> <span data-ttu-id="7e786-108">Els preus de cada categoria de despesa es defineixen típicament segons la jerarquia següent:</span><span class="sxs-lookup"><span data-stu-id="7e786-108">Pricing for each expense category is typically defined in the following hierarchy:</span></span>

- <span data-ttu-id="7e786-109">Organització</span><span class="sxs-lookup"><span data-stu-id="7e786-109">Organization</span></span>
- <span data-ttu-id="7e786-110">Client</span><span class="sxs-lookup"><span data-stu-id="7e786-110">Customer</span></span>
- <span data-ttu-id="7e786-111">Oferta/contracte</span><span class="sxs-lookup"><span data-stu-id="7e786-111">Quote/contract</span></span>

<span data-ttu-id="7e786-112">Completeu els passos següents per visualitzar, afegir o suprimir una despesa del projecte.</span><span class="sxs-lookup"><span data-stu-id="7e786-112">Complete the following steps to view, add, or delete a project expense.</span></span>

1. <span data-ttu-id="7e786-113">Aneu a **Projectes** i seleccioneu el projecte en el qual voleu treballar.</span><span class="sxs-lookup"><span data-stu-id="7e786-113">Go to **Projects**, and select the project you want to work on.</span></span>
2. <span data-ttu-id="7e786-114">Seleccioneu la pestanya **Estimacions del projecte** i visualitzeu la llista de despeses del projecte.</span><span class="sxs-lookup"><span data-stu-id="7e786-114">Select the **Project Estimates** tab and view the list of project expenses.</span></span>
3. <span data-ttu-id="7e786-115">Seleccioneu **Despesa nova** per afegir una despesa.</span><span class="sxs-lookup"><span data-stu-id="7e786-115">Select **New Expense** to add an expense.</span></span> <span data-ttu-id="7e786-116">O bé, seleccioneu la despesa que voleu suprimir i, a continuació, seleccioneu **Suprimeix la despesa**.</span><span class="sxs-lookup"><span data-stu-id="7e786-116">Or, select an expense to delete, and then select **Delete Expense**.</span></span>

<span data-ttu-id="7e786-117">Els atributs següents es defineixen per a cada element de la línia de despesa:</span><span class="sxs-lookup"><span data-stu-id="7e786-117">The following attributes are defined for each expense line item:</span></span>

- <span data-ttu-id="7e786-118">**Categoria**: agrupaments comuns utilitzats per descriure totes les despeses ocasionades en un projecte.</span><span class="sxs-lookup"><span data-stu-id="7e786-118">**Category**: The common groupings used to describe all expenses incurred on a project.</span></span>
- <span data-ttu-id="7e786-119">**Data d'inici**: data prevista en que s'incorrerà la despesa.</span><span class="sxs-lookup"><span data-stu-id="7e786-119">**Start Date**: The date when the expense is forecasted to be incurred.</span></span>
- <span data-ttu-id="7e786-120">**Quantitat**: nombre estimat d'elements de despesa per a una categoria concreta.</span><span class="sxs-lookup"><span data-stu-id="7e786-120">**Quantity**: The estimated number of expense items for a specific category.</span></span>
- <span data-ttu-id="7e786-121">**Preu de cost per unitat**: preu per unitat utilitzat per calcular el cost de la despesa.</span><span class="sxs-lookup"><span data-stu-id="7e786-121">**Unit Cost Price**: The unit price used to calculate to cost of the expense.</span></span>
- <span data-ttu-id="7e786-122">**Preu de venda per unitat**: preu per unitat utilitzat per calcular el preu de venda de la despesa.</span><span class="sxs-lookup"><span data-stu-id="7e786-122">**Unit Sales Price**: The unit price used to calculate the sale prices of the expense.</span></span>

