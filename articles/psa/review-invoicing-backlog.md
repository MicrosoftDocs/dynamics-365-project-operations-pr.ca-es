---
title: Revisar el registre de facturació dels projectes i dels contractes del projecte
description: En aquest tema s'ofereix informació sobre com es poden revisar els registres de temps, despeses i productes, i com marcar-los com a preparats per a la facturació.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: ''
ms.author: rumant
ms.date: 03/11/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: eb6d942d61bf8b5d20afb75c88716132a596bcbd
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072421"
---
# <a name="review-the-invoicing-backlog-on-projects-and-project-contracts"></a><span data-ttu-id="5337e-103">Revisar el registre de facturació dels projectes i dels contractes del projecte</span><span class="sxs-lookup"><span data-stu-id="5337e-103">Review the invoicing backlog on projects and project contracts</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="5337e-104">Quan una transacció està preparada per tenir una factura creada i processada, la transacció s'ha de marcar com a **Llesta per facturar**.</span><span class="sxs-lookup"><span data-stu-id="5337e-104">When a transaction is ready to have an invoice created and processed, the transaction should be marked **Ready to invoice**.</span></span> <span data-ttu-id="5337e-105">Aquest tema descriu els tipus de transaccions que es poden crear.</span><span class="sxs-lookup"><span data-stu-id="5337e-105">This topic describes the types of transactions that can be created.</span></span>

## <a name="review-the-time-and-material-billing-backlog"></a><span data-ttu-id="5337e-106">Revisar el registre de facturació de temps i material</span><span class="sxs-lookup"><span data-stu-id="5337e-106">Review the time and material billing backlog</span></span>

<span data-ttu-id="5337e-107">Quan s'envia una entrada de temps o de la despesa i s'aprova per a un projecte, el PSA crea un valor real de projecte.</span><span class="sxs-lookup"><span data-stu-id="5337e-107">When a time or expense entry is submitted and approved for a project, PSA creates a project actual.</span></span> <span data-ttu-id="5337e-108">Si la combinació de la classe de projecte i transacció s'assignen a una línia de contracte per a un projecte de temps i materials, dos valors reals es creen quan s'aprova l'entrada:</span><span class="sxs-lookup"><span data-stu-id="5337e-108">If the combination of the project and the transaction class are mapped to a contract line for a time-and-materials project, two actuals are created when the entry is approved:</span></span>

- <span data-ttu-id="5337e-109">Valor real de cost</span><span class="sxs-lookup"><span data-stu-id="5337e-109">Cost actual</span></span> 
- <span data-ttu-id="5337e-110">Valor real de vendes no facturades</span><span class="sxs-lookup"><span data-stu-id="5337e-110">Unbilled sales actual</span></span>

<span data-ttu-id="5337e-111">Els valors reals de vendes no facturades representen el registre de facturació i l'estat de facturació s'ha de definir com a **Llest per facturar**.</span><span class="sxs-lookup"><span data-stu-id="5337e-111">Unbilled sales actuals represent the billing backlog, and their billing status must be set to **Ready to Invoice**.</span></span> <span data-ttu-id="5337e-112">Quan es crea una factura de projecte, els valors reals de vendes que no s'han facturat que s'han marcat com a **Llest per facturar** es copien com a detalls de la línia de factura.</span><span class="sxs-lookup"><span data-stu-id="5337e-112">When a project invoice is created, unbilled sales actuals that are marked **Ready to Invoice** are copied over as invoice line details.</span></span>

<span data-ttu-id="5337e-113">Per revisar el registre de facturació per temps i materials, aneu a **Vendes** \> **Facturació** \> **Registre de facturació de temps i material**.</span><span class="sxs-lookup"><span data-stu-id="5337e-113">To review the billing backlog for time and materials, go to **Sales** \> **Billing** \> **Time and Material Billing Backlog**.</span></span> <span data-ttu-id="5337e-114">Seleccioneu tots els valors reals de vendes no facturades que estiguin preparats per a facturar i, a continuació, seleccioneu **Llest per facturar**.</span><span class="sxs-lookup"><span data-stu-id="5337e-114">Select all the unbilled sales actuals that are ready to be invoiced, and then select **Ready to Invoice**.</span></span> <span data-ttu-id="5337e-115">L'estat de facturació d'aquests valors reals canvia a **Llest per facturar**.</span><span class="sxs-lookup"><span data-stu-id="5337e-115">The billing status of these actuals is changed to **Ready to Invoice**.</span></span>

![Registre de facturació de temps i material](media/TMBacklog.png)

## <a name="review-the-product-billing-backlog"></a><span data-ttu-id="5337e-117">Revisar el registre de facturació de producte</span><span class="sxs-lookup"><span data-stu-id="5337e-117">Review the product billing backlog</span></span>

<span data-ttu-id="5337e-118">Al PSA, quan un contracte de projecte té línies de contracte basades en productes, aquestes línies es tenen en compte per a la facturació cada vegada que es crea una factura per al contracte del projecte.</span><span class="sxs-lookup"><span data-stu-id="5337e-118">In PSA, when a project contract has product-based contract lines, those lines are considered for invoicing whenever an invoice is created for the project contract.</span></span> <span data-ttu-id="5337e-119">Qualsevol producte que tingui línies de contracte marcades com a **Llest per facturar** es copia a la factura de projecte com a línies de factura de projecte.</span><span class="sxs-lookup"><span data-stu-id="5337e-119">Any product that has contract lines that are marked **Ready to Invoice** is copied over to the project invoice as project invoice lines.</span></span>

<span data-ttu-id="5337e-120">Per revisar el registre d'entrada de facturació dels productes, aneu a **Vendes** \> **Facturació** \> **Registre de facturació de productes**.</span><span class="sxs-lookup"><span data-stu-id="5337e-120">To review the billing backlog for products, go to **Sales** \> **Billing** \> **Product Billing Backlog**.</span></span> <span data-ttu-id="5337e-121">Seleccioneu totes les línies de vendes basades en productes que estiguin preparades per a facturar i, a continuació, seleccioneu **Llest per facturar**.</span><span class="sxs-lookup"><span data-stu-id="5337e-121">Select all the product-based contract lines that are ready to be invoiced, and then select **Ready to Invoice**.</span></span> <span data-ttu-id="5337e-122">L'estat de facturació d'aquestes línies canvia a **Llest per facturar**.</span><span class="sxs-lookup"><span data-stu-id="5337e-122">The billing status of these lines is changed to **Ready to Invoice**.</span></span>

![Registre de facturació de producte](media/ProductBacklog.png)

## <a name="review-billing-milestones-on-fixed-price-contracts"></a><span data-ttu-id="5337e-124">Revisar les fites de facturació dels contractes de preu fix</span><span class="sxs-lookup"><span data-stu-id="5337e-124">Review billing milestones on fixed-price contracts</span></span>

<span data-ttu-id="5337e-125">Cada línia de contracte de projecte que té un mètode de facturació de preu fix ha de definir fites del contracte.</span><span class="sxs-lookup"><span data-stu-id="5337e-125">Each project contract line that has a fixed-price billing method must define contract milestones.</span></span> <span data-ttu-id="5337e-126">Aquestes fites dels contractes només es poden facturar si es marquen com a **Llest per facturar**.</span><span class="sxs-lookup"><span data-stu-id="5337e-126">These contract milestones can be invoiced only if they are marked **Ready to Invoice**.</span></span> 

<span data-ttu-id="5337e-127">Per revisar les fites de facturació, aneu a **Vendes** \> **Facturació** \> **Fites de preu fix**.</span><span class="sxs-lookup"><span data-stu-id="5337e-127">To review billing milestones, go to **Sales** \> **Billing** \> **Fixed Price Milestones**.</span></span> <span data-ttu-id="5337e-128">Seleccioneu totes les fites que estiguin preparades per a facturar i, a continuació, seleccioneu **Llest per facturar**.</span><span class="sxs-lookup"><span data-stu-id="5337e-128">Select the milestones that are ready to be invoiced, and then select **Ready to invoice**.</span></span> <span data-ttu-id="5337e-129">L'estat de facturació d'aquestes fites canvia a **Llest per facturar**.</span><span class="sxs-lookup"><span data-stu-id="5337e-129">The billing status of these milestones is changed to **Ready to Invoice**.</span></span>

![Fites de preu fix](media/FPBacklog.png)
