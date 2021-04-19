---
title: Desactivació de llistes de preus
description: En aquest tema s'explica com desactivar o suprimir llistes de preus no usades o antigues.
author: rumant
manager: AnnBe
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Professional Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 3fa902e93815002be7d6915880cd7759dbbde5ef
ms.sourcegitcommit: 386921f44f1e9a8a828b140206d52945de07aee7
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "5701910"
---
# <a name="deactivate-price-lists"></a><span data-ttu-id="6e99d-103">Desactivació de llistes de preus</span><span class="sxs-lookup"><span data-stu-id="6e99d-103">Deactivate price lists</span></span> 

<span data-ttu-id="6e99d-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_</span><span class="sxs-lookup"><span data-stu-id="6e99d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="6e99d-105">Per suprimir llistes de preus antigues o no utilitzades del Dynamics 365 Project Operations, heu de completar dos passos.</span><span class="sxs-lookup"><span data-stu-id="6e99d-105">To remove old or unused price lists from Dynamics 365 Project Operations, there are two steps you must complete.</span></span> 

1. <span data-ttu-id="6e99d-106">Elimineu o suprimiu la llista de preus de pàgines específiques.</span><span class="sxs-lookup"><span data-stu-id="6e99d-106">Remove or delete the price list from specific pages.</span></span>
2. <span data-ttu-id="6e99d-107">Desactiveu o suprimiu la llista de preus de les llistes de preus actives de la pàgina **Llistes de preus**.</span><span class="sxs-lookup"><span data-stu-id="6e99d-107">Deactivate or delete the price list from the Active price lists on the **Price Lists** page.</span></span>

>[!IMPORTANT]
> <span data-ttu-id="6e99d-108">Heu de completar els dos passos per suprimir completament una llista de preus.</span><span class="sxs-lookup"><span data-stu-id="6e99d-108">You must complete both steps to fully remove a price list.</span></span> <span data-ttu-id="6e99d-109">No n'hi ha prou amb realitzar només el pas 2, que és suprimir o desactivar directament la llista de preus de la visualització Llistes de preus actives.</span><span class="sxs-lookup"><span data-stu-id="6e99d-109">Only performing step 2, which is to directly delete or deactivate the price list from the Active Price Lists view, is not sufficient.</span></span> <span data-ttu-id="6e99d-110">També heu de suprimir l'associació d'aquesta llista de preus de tots els llocs esmentats al pas 1.</span><span class="sxs-lookup"><span data-stu-id="6e99d-110">You must also delete the association of this price list from all the places mentioned in step 1.</span></span>

## <a name="delete-the-price-list-from-specific-pages"></a><span data-ttu-id="6e99d-111">Suprimir la llista de preus de pàgines específiques.</span><span class="sxs-lookup"><span data-stu-id="6e99d-111">Delete the price list from specific pages</span></span>
1. <span data-ttu-id="6e99d-112">Per suprimir una llista de preus del Project Operations, aneu a les pàgines següents:</span><span class="sxs-lookup"><span data-stu-id="6e99d-112">To delete a price list from Project Operations, go to the following pages:</span></span>  

      - <span data-ttu-id="6e99d-113">Pàgina **Paràmetres de projecte** > pestanya **Llistes de preus**</span><span class="sxs-lookup"><span data-stu-id="6e99d-113">**Project parameters** page > **Price Lists** tab</span></span>
      - <span data-ttu-id="6e99d-114">Pàgina **Unitat organitzativa** > quadrícula **Llistes de preus**</span><span class="sxs-lookup"><span data-stu-id="6e99d-114">**Organizational Unit** page > **Price Lists** grid</span></span>
      - <span data-ttu-id="6e99d-115">Pàgina **Compte** > quadrícula **Llistes de preus del projecte**</span><span class="sxs-lookup"><span data-stu-id="6e99d-115">**Account** page > **Project Price Lists** grid</span></span>
      - <span data-ttu-id="6e99d-116">Pàgina **Ofertes del projecte** > quadrícula **Llistes de preus del projecte**: s'aplica a totes les ofertes actives del projecte.</span><span class="sxs-lookup"><span data-stu-id="6e99d-116">**Project Quotes** page > **Project Price Lists** grid: This applies to all active project quotes.</span></span>
      - <span data-ttu-id="6e99d-117">Pàgina **Contractes del projecte** > quadrícula **Llistes de preus del projecte**: s'aplica a tots els contractes actius del projecte.</span><span class="sxs-lookup"><span data-stu-id="6e99d-117">**Project Contracts** page > **Project Price Lists** grid: This applies to all active project contracts.</span></span>

 2. <span data-ttu-id="6e99d-118">Per a cada pàgina, heu de seleccionar la llista de preus que voleu suprimir i, a continuació, seleccionar **Suprimeix**.</span><span class="sxs-lookup"><span data-stu-id="6e99d-118">For each page, you need to select the price list that you want to delete, and then select **Delete**.</span></span> 
 
## <a name="delete-or-deactivate-the-price-list-from-the-price-lists-page"></a><span data-ttu-id="6e99d-119">Suprimiu o desactiveu la llista de preus de la pàgina Llistes de preus</span><span class="sxs-lookup"><span data-stu-id="6e99d-119">Delete or deactivate the price list from the Price Lists page</span></span>
 
1. <span data-ttu-id="6e99d-120">Per suprimir una llista de preus de les llistes de preus actives, aneu a **Vendes** > **Clients** > **Llistes de preus**.</span><span class="sxs-lookup"><span data-stu-id="6e99d-120">To delete a price list from the active price lists, go to **Sales** > **Customers** > **Price Lists**.</span></span> 
2. <span data-ttu-id="6e99d-121">Seleccioneu la llista de preus que voleu suprimir i, a continuació, seleccioneu **Suprimeix**.</span><span class="sxs-lookup"><span data-stu-id="6e99d-121">Select the price list that you want to delete and then select **Delete**.</span></span> <span data-ttu-id="6e99d-122">Si es fa referència a la llista de preus en qualsevol transacció existent, no la podreu suprimir.</span><span class="sxs-lookup"><span data-stu-id="6e99d-122">If the price list is referenced on any existing transactions, you won't be able to delete it.</span></span> <span data-ttu-id="6e99d-123">Si això passa, podeu desactivar la llista de preus perquè no aparegui en cap visualització.</span><span class="sxs-lookup"><span data-stu-id="6e99d-123">If this happens, you can deactivate the price list so that it doesn't appear in any views.</span></span> 
3. <span data-ttu-id="6e99d-124">Per desactivar la llista de preus, torneu a seleccionar-la i, a continuació, seleccioneu **Desactiva**.</span><span class="sxs-lookup"><span data-stu-id="6e99d-124">To deactivate the price list, select the price list again, and then select **Deactivate**.</span></span>   
