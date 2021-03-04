---
title: Creació d'una factura proforma manual (bàsic)
description: Aquest tema proporciona informació sobre la creació d'una factura proforma manual al Project Operations.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5a924de6efc377e28a20e038e7deac04616b95aa
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764491"
---
# <a name="create-a-manual-proforma-invoice---lite"></a><span data-ttu-id="6e290-103">Creació d'una factura proforma manual (bàsic)</span><span class="sxs-lookup"><span data-stu-id="6e290-103">Create a manual proforma invoice - lite</span></span>

<span data-ttu-id="6e290-104">_**S'aplica a:** implementació bàsica: tracte de facturació proforma_</span><span class="sxs-lookup"><span data-stu-id="6e290-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="6e290-105">Al Dynamics 365 Project Operations, les factures de proforma es poden crear manualment segons calgui.</span><span class="sxs-lookup"><span data-stu-id="6e290-105">In Dynamics 365 Project Operations, proforma invoices can be created manually as needed.</span></span> <span data-ttu-id="6e290-106">Podeu crear manualment una factura proforma des de la pàgina de llista **Contractes del projecte** o la pàgina de detalls **Contracte del projecte**.</span><span class="sxs-lookup"><span data-stu-id="6e290-106">You can manually create a proforma invoice from the **Project Contracts** list page or from the **Project Contract** details page.</span></span>

##  <a name="project-contracts-list-page"></a><span data-ttu-id="6e290-107">Pàgina de llista Contractes del projecte</span><span class="sxs-lookup"><span data-stu-id="6e290-107">Project Contracts list page</span></span>

<span data-ttu-id="6e290-108">Des de la pàgina de llista **Contractes del projecte**, seleccioneu un o més contractes de projecte i creeu factures per a tots els registres seleccionats.</span><span class="sxs-lookup"><span data-stu-id="6e290-108">From **Project Contracts** list page, select one or more project contracts, and create invoices for all of the selected records.</span></span>

<span data-ttu-id="6e290-109">El sistema comprova quin dels contractes de projecte seleccionats té un registre **A punt per facturar** amb data abans d'avui.</span><span class="sxs-lookup"><span data-stu-id="6e290-109">The system checks to see which of the selected project contracts has a **Ready to Invoice** backlog dated before today's date.</span></span> <span data-ttu-id="6e290-110">A partir d'aquests contractes, el sistema crea esborranys de factures proforma.</span><span class="sxs-lookup"><span data-stu-id="6e290-110">From those contracts, the system creates draft proforma invoices.</span></span> <span data-ttu-id="6e290-111">Si un contracte de projecte té diversos clients, pot haver-hi una factura creada per client i diverses factures per contracte de projecte.</span><span class="sxs-lookup"><span data-stu-id="6e290-111">If a project contract has multiple customers, there may be one invoice created per customer, and multiple invoices per project contract.</span></span>

<span data-ttu-id="6e290-112">Totes les factures de projecte creades estan disponibles a la pàgina **Factura** a la secció **Facturació** de l'àrea **Vendes**.</span><span class="sxs-lookup"><span data-stu-id="6e290-112">All of the created project invoices are available on the **Invoice** page in the **Billing** section of the **Sales** area.</span></span>

## <a name="project-contract-details-page"></a><span data-ttu-id="6e290-113">Pàgina de detalls Contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="6e290-113">Project Contract details page</span></span>

<span data-ttu-id="6e290-114">També es pot crear una factura de proforma des de la pàgina de detalls **Contracte del projecte**.</span><span class="sxs-lookup"><span data-stu-id="6e290-114">A proforma invoice can also be created from the **Project Contract** details page.</span></span> <span data-ttu-id="6e290-115">El sistema verifica que el contracte de projecte té un registre **A punt per facturar** amb data abans d'avui.</span><span class="sxs-lookup"><span data-stu-id="6e290-115">The system verifies the project contract has a **Ready to Invoice** backlog dated before today's date.</span></span> <span data-ttu-id="6e290-116">A partir d'aquests contractes, el sistema crea esborranys de factures proforma en funció del nombre de clients en cada línia de contracte.</span><span class="sxs-lookup"><span data-stu-id="6e290-116">From these contracts, the system creates draft proforma invoices based on the number of customers on each contract line.</span></span>

<span data-ttu-id="6e290-117">Quan es crea una única factura proforma, s'obre la pàgina **Factura**.</span><span class="sxs-lookup"><span data-stu-id="6e290-117">When there's a single proforma invoice created, the **Invoice** page opens.</span></span> <span data-ttu-id="6e290-118">Si es creen diverses factures per al contracte del projecte, s'obrirà la pàgina de llistes **Factures** per mostrar totes les factures creades.</span><span class="sxs-lookup"><span data-stu-id="6e290-118">If multiple invoices are created for that project contract, the **Invoices** list page opens to show all of the created invoices.</span></span>
