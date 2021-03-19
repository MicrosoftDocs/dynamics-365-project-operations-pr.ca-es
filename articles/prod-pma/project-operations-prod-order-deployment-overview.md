---
title: Informació general de la implementació del Project Operations per a escenaris basats en producció/mantinguts en existències
description: En aquest tema es proporciona informació sobre el tipus d'implementació del Project Operations per a escenaris basats en producció/mantinguts en existències.
author: rumant
manager: Annbe
ms.date: 11/02/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 8ffbcb326e5cd86c49b3b3b27ce7d68404a6842b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289222"
---
# <a name="project-operations-for-stockedproduction-based-scenarios-deployment-overview"></a><span data-ttu-id="6c63c-103">Informació general de la implementació del Project Operations per a escenaris basats en producció/mantinguts en existències</span><span class="sxs-lookup"><span data-stu-id="6c63c-103">Project Operations for stocked/production-based scenarios deployment overview</span></span>

<span data-ttu-id="6c63c-104">_**S'aplica a:** Project Operations per a escenaris basats en producció/mantinguts en existències_</span><span class="sxs-lookup"><span data-stu-id="6c63c-104">_**Applies To:** Project Operations for stocked/production-based scenarios_</span></span>


<span data-ttu-id="6c63c-105">Aquest tipus d'implementació té les següents funcionalitats per a les empreses basades en projectes:</span><span class="sxs-lookup"><span data-stu-id="6c63c-105">This deployment type has the following capabilities for project-based companies:</span></span>

- <span data-ttu-id="6c63c-106">Planificació de projectes mitjançant [estructures del desglossament del treball](work-breakdown-structures.md)</span><span class="sxs-lookup"><span data-stu-id="6c63c-106">Project planning using the [Work breakdown structures](work-breakdown-structures.md)</span></span>
- <span data-ttu-id="6c63c-107">Compra i consum d'inventaris d'estoc per a projectes</span><span class="sxs-lookup"><span data-stu-id="6c63c-107">Procure and consume stocked inventory for projects</span></span>
- <span data-ttu-id="6c63c-108">Administració de vendes basades en projectes amb el mòdul **Vendes i màrqueting** a les aplicacions del Dynamics 365 Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="6c63c-108">Managing project-based sales using the **Sales and marketing** module in Dynamics 365 Finance and Operations apps</span></span>
- <span data-ttu-id="6c63c-109">Preus i costos de projectes mitjançant configuracions de tarifes de cost i facturació en aplicacions del Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="6c63c-109">Project pricing and costing using the cost rate and bill rate configurations in Finance and Operations apps</span></span>
- <span data-ttu-id="6c63c-110">Administració de recursos per a projectes a les aplicacions del Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="6c63c-110">Resource management for projects in Finance and Operations apps</span></span>
- <span data-ttu-id="6c63c-111">Seguiment del progrés i el temps del projecte a les aplicacions del Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="6c63c-111">Project progress and time tracking in Finance and Operations apps</span></span>
- <span data-ttu-id="6c63c-112">Experiències d'administració de despeses per a despeses del projecte i que no són del projecte amb captura de rebuts mitjançant característiques d'OCR</span><span class="sxs-lookup"><span data-stu-id="6c63c-112">Expense management experiences for project and non-project expenses with receipt capture using OCR capabilities</span></span>
- <span data-ttu-id="6c63c-113">Facturació mitjançant un sistema d'impost de vendes de classe empresarial i de tipus de canvi amb data d'efectivitat</span><span class="sxs-lookup"><span data-stu-id="6c63c-113">Invoicing using an enterprise-class sales tax and date-effective exchange rates system</span></span>
- <span data-ttu-id="6c63c-114">Grups de projectes configurables per a comptabilitat de treball en curs i les acumulacions</span><span class="sxs-lookup"><span data-stu-id="6c63c-114">Configurable project groups for WIP accounting and accruals</span></span>
- <span data-ttu-id="6c63c-115">Reconeixement d'ingressos del projecte</span><span class="sxs-lookup"><span data-stu-id="6c63c-115">Project revenue recognition</span></span>

<span data-ttu-id="6c63c-116">Aquest tipus de implementació també proporciona una extensió de la funcionalitat proporcionada per les aplicacions Dynamics 365 Finance i Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="6c63c-116">This deployment type also provides an extension to the functionality provided by the Dynamics 365 Finance and Dynamics 365 Supply Chain Management applications.</span></span>

<span data-ttu-id="6c63c-117">Seleccioneu aquest tipus d'implementació per utilitzar el Dynamics 365 Project Operations per al cicle de vida complet del projecte, incloent-hi els requisits clau següents:</span><span class="sxs-lookup"><span data-stu-id="6c63c-117">Select this deployment type to use Dynamics 365 Project Operations for the full project lifecycle, including the following key requirements:</span></span>

- <span data-ttu-id="6c63c-118">Ampli sistema d'administració de projectes que administra els elements d'inventari i costos de comanda de treball i producció per als projectes interns i facturables per a planificacions i finances.</span><span class="sxs-lookup"><span data-stu-id="6c63c-118">An extensive Project management system that manages inventoried items and job/production order costing for internal and billable projects for schedules and financials.</span></span>
- <span data-ttu-id="6c63c-119">L'organització ja té les aplicacions Dynamics 365 Finance o Dynamics 365 Supply Chain and Manufacturing i la integració de transaccions basades en projectes simplificarà les necessitats d'accés a les dades i informes.</span><span class="sxs-lookup"><span data-stu-id="6c63c-119">The organization already has Dynamics 365 Finance or Dynamics 365 Supply Chain and Manufacturing apps and integrating project-based transactions will simplify data access and reporting needs.</span></span>
- <span data-ttu-id="6c63c-120">Sistema d'administració de despeses completament funcional que inclou aplicacions de normes i reemborsaments per al seguiment de les despeses del projecte i les que no són del projecte.</span><span class="sxs-lookup"><span data-stu-id="6c63c-120">A fully functional Expense management system that includes policy enforcements and reimbursements for tracking project and non-project expenses.</span></span>
- <span data-ttu-id="6c63c-121">Motor d'impostos de vendes de classe empresarial ric i de tipus de canvi per generar factures de projectes per als clients.</span><span class="sxs-lookup"><span data-stu-id="6c63c-121">An enterprise-class sales tax and exchange rate engine to generate customer-facing invoices for projects.</span></span>
- <span data-ttu-id="6c63c-122">Sistema de comptabilitat del projecte i reconeixement d'ingressos que compleix amb els estàndards d'informes financers internacionals (IRFS).</span><span class="sxs-lookup"><span data-stu-id="6c63c-122">An International Financial Reporting Standards(IFRS)-compliant project accounting and revenue recognition system.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]