---
title: Administració de contractes de projectes
description: Aquest tema proporciona informació sobre la visualització de contractes basats en projectes.
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5a4357d5cf184a3c6ada3ae33631694c31bb5b00
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273186"
---
# <a name="manage-project-contracts"></a><span data-ttu-id="83942-103">Administració de contractes de projectes</span><span class="sxs-lookup"><span data-stu-id="83942-103">Manage project contracts</span></span>

<span data-ttu-id="83942-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_</span><span class="sxs-lookup"><span data-stu-id="83942-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="83942-105">Els contractes de projecte al Dynamics 365 Project Operations capturen i administren els compromisos acordats contractualment i els detalls de facturació d'un projecte.</span><span class="sxs-lookup"><span data-stu-id="83942-105">Project contracts in Dynamics 365 Project Operations capture and manage the contractually agreed on commitments and billing details of a project.</span></span> <span data-ttu-id="83942-106">L'estructura d'un contracte de projecte al Project Operations s'adapta al treball basat en projectes amb els components següents:</span><span class="sxs-lookup"><span data-stu-id="83942-106">The structure of a project contract in Project Operations is tailored to project-based work with the following components:</span></span>

- <span data-ttu-id="83942-107">Línies de contracte que identifiquen els components discrets del treball que es presentaran com a components d'alt nivell en una factura de projecte.</span><span class="sxs-lookup"><span data-stu-id="83942-107">Contract lines that identify the discrete components of work that will be presented as high-level components on a project invoice.</span></span>
- <span data-ttu-id="83942-108">Detalls de la línia de contracte que identifiquen i estimen la feina de cada component d'alt nivell o línia de contracte.</span><span class="sxs-lookup"><span data-stu-id="83942-108">Contract line details that identify and estimate the work for each high-level component or contract line.</span></span> <span data-ttu-id="83942-109">L'estimació inclou la planificació i els aspectes financers per al treball vinculat a la línia de contracte.</span><span class="sxs-lookup"><span data-stu-id="83942-109">The estimate includes the schedule and the financial aspects for the work tied to the contract line.</span></span>
- <span data-ttu-id="83942-110">Es configuren els models de contractació i els components imputables per a cada línia de contracte que contingui l'acord de facturació per a cada línia de contracte i el contracte global.</span><span class="sxs-lookup"><span data-stu-id="83942-110">Contracting models and chargeable components are set up for each contract line that holds the billing arrangement for each contract line and the overall contract.</span></span>

## <a name="view-all-project-based-contracts"></a><span data-ttu-id="83942-111">Visualitzar tots els contractes basats en projectes</span><span class="sxs-lookup"><span data-stu-id="83942-111">View all project-based contracts</span></span>

<span data-ttu-id="83942-112">Es pot veure una llista de tots els contractes del projecte a la pàgina de llista **Contractes**.</span><span class="sxs-lookup"><span data-stu-id="83942-112">A list of all project contracts can be seen on the **Contracts** list page.</span></span> 

1. <span data-ttu-id="83942-113">Aneu a **Vendes** > **Contactes**.</span><span class="sxs-lookup"><span data-stu-id="83942-113">Go to **Sales** > **Contracts**.</span></span> <span data-ttu-id="83942-114">Es mostra una llista de tots els contractes de projecte al sistema.</span><span class="sxs-lookup"><span data-stu-id="83942-114">A list of all your project Contracts in the system are shown.</span></span> 
2. <span data-ttu-id="83942-115">Seleccioneu el **Commutador de visualització** (la fletxa desplegable que hi ha al costat del nom de la visualització) per seleccionar altres visualitzacions filtrades.</span><span class="sxs-lookup"><span data-stu-id="83942-115">Select the **View switcher** (the drop-down arrow next to the name of the view) to select other filtered views.</span></span> <span data-ttu-id="83942-116">Podeu crear visualitzacions pròpies amb criteris de filtratge personalitzats.</span><span class="sxs-lookup"><span data-stu-id="83942-116">You can create your own views with custom filter criteria.</span></span>

<span data-ttu-id="83942-117">Es poden crear o suprimir contractes des d'aquesta pàgina de llista o des de les pàgines de detalls.</span><span class="sxs-lookup"><span data-stu-id="83942-117">Contracts can be created or deleted from this list page or detail pages.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]