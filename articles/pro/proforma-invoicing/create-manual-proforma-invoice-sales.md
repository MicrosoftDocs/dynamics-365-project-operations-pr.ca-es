---
title: Creació d'una factura proforma manual (bàsic)
description: Aquest tema proporciona informació sobre la creació d'una factura proforma manual al Project Operations.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 87ef090454b2a7ab997e7c21d8d10badc31c8235
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176374"
---
# <a name="create-a-manual-proforma-invoice---lite"></a><span data-ttu-id="4913b-103">Creació d'una factura proforma manual (bàsic)</span><span class="sxs-lookup"><span data-stu-id="4913b-103">Create a manual proforma invoice - lite</span></span>

<span data-ttu-id="4913b-104">_**S'aplica a:** implementació bàsica: tracte de facturació proforma_</span><span class="sxs-lookup"><span data-stu-id="4913b-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="4913b-105">Al Dynamics 365 Project Operations, les factures proforma es poden crear manualment segons sigui necessari.</span><span class="sxs-lookup"><span data-stu-id="4913b-105">In Dynamics 365 Project Operations, proforma invoices can be created manually as needed.</span></span> <span data-ttu-id="4913b-106">Podeu crear manualment una factura proforma des de la pàgina de llista **Contractes del projecte** o la pàgina de detalls **Contracte del projecte**.</span><span class="sxs-lookup"><span data-stu-id="4913b-106">You can manually create a proforma invoice from the **Project Contracts** list page or from the **Project Contract** details page.</span></span>

##  <a name="project-contracts-list-page"></a><span data-ttu-id="4913b-107">Pàgina de llista Contractes del projecte</span><span class="sxs-lookup"><span data-stu-id="4913b-107">Project Contracts list page</span></span>

<span data-ttu-id="4913b-108">Des de la pàgina de llista **Contractes del projecte**, seleccioneu un o més contractes de projecte i creeu factures per a tots els registres seleccionats.</span><span class="sxs-lookup"><span data-stu-id="4913b-108">From **Project Contracts** list page, select one or more project contracts, and create invoices for all of the selected records.</span></span>

<span data-ttu-id="4913b-109">El sistema comprova quin dels contractes de projecte seleccionats té un registre **A punt per facturar** amb data abans d'avui.</span><span class="sxs-lookup"><span data-stu-id="4913b-109">The system checks to see which of the selected project contracts has a **Ready to Invoice** backlog  dated before today's date.</span></span> <span data-ttu-id="4913b-110">A partir d'aquests contractes, el sistema crea esborranys de factures proforma.</span><span class="sxs-lookup"><span data-stu-id="4913b-110">From those contracts, the system creates draft proforma invoices.</span></span> <span data-ttu-id="4913b-111">Si un contracte de projecte té diversos clients, pot haver-hi una factura creada per client i diverses factures per contracte de projecte.</span><span class="sxs-lookup"><span data-stu-id="4913b-111">If a project contract has multiple customers, there may be one invoice created per customer, and multiple invoices per project contract.</span></span>

<span data-ttu-id="4913b-112">Totes les factures de projecte creades estan disponibles a la pàgina **Factura** a la secció **Facturació** de l'àrea **Vendes**.</span><span class="sxs-lookup"><span data-stu-id="4913b-112">All of the created project invoices are available on the **Invoice** page in the **Billing** section of the **Sales** area.</span></span>

## <a name="project-contract-details-page"></a><span data-ttu-id="4913b-113">Pàgina de detalls Contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="4913b-113">Project Contract details page</span></span>

<span data-ttu-id="4913b-114">També es pot crear una factura proforma des de la pàgina de detalls **Contracte del projecte**, que crea la factura d'aquest contracte de projecte específic.</span><span class="sxs-lookup"><span data-stu-id="4913b-114">A proforma invoice can also be created from the **Project Contract** details page, which creates the invoice for that specific project contract.</span></span> <span data-ttu-id="4913b-115">El sistema verifica que el contracte del projecte té un registre **A punt per facturar** amb data abans d'avui.</span><span class="sxs-lookup"><span data-stu-id="4913b-115">The system verifies that the project contract has a **Ready to Invoice** backlog that is dated before today's date.</span></span> <span data-ttu-id="4913b-116">A partir d'aquests contractes, el sistema crea esborranys de factures proforma en funció del nombre de clients en cada línia de contracte.</span><span class="sxs-lookup"><span data-stu-id="4913b-116">From these contracts, the system creates draft proforma invoices based on the number of customers on each contract line.</span></span>

<span data-ttu-id="4913b-117">Quan es crea una única factura proforma, s'obre la pàgina **Factura**.</span><span class="sxs-lookup"><span data-stu-id="4913b-117">When there's a single proforma invoice created, the **Invoice** page opens.</span></span> <span data-ttu-id="4913b-118">Si hi ha diverses factures creades per aquest contracte de projecte, llavors la pàgina de llista **Factures** s'obre per mostrar totes les factures creades.</span><span class="sxs-lookup"><span data-stu-id="4913b-118">If there are multiple invoices created for that project contract, then the **Invoices** list page opens to show all of the created invoices.</span></span>
