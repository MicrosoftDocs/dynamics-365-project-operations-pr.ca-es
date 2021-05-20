---
title: Integració d'escriptura doble del Project Operations
description: En aquest tema es proporciona una descripció general de la integració d'escriptura doble del Project Operations.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d9d6a7c367872219b4aca32aecb15d6837ebe296
ms.sourcegitcommit: 02f00960198cc78a5e96955a9e4390c2c6393bbf
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "5955646"
---
# <a name="project-operations-dual-write-integration-overview"></a><span data-ttu-id="406a7-103">Descripció general de la integració d'escriptura doble del Project Operations</span><span class="sxs-lookup"><span data-stu-id="406a7-103">Project Operations dual-write integration overview</span></span>

<span data-ttu-id="406a7-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_</span><span class="sxs-lookup"><span data-stu-id="406a7-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="406a7-105">El Project Operations utilitza [capacitats de doble escriptura](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) per sincronitzar dades a través del Microsoft Dataverse i del Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="406a7-105">Project Operations uses [dual-write capabilities](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) to synchronize data across Microsoft Dataverse and Dynamics 365 Finance.</span></span>

<span data-ttu-id="406a7-106">A la il·lustració següent es mostra la manera que se sincronitzen les dades com a part d'aquesta integració entre el Dataverse i Finances.</span><span class="sxs-lookup"><span data-stu-id="406a7-106">The following illustration shows how data is synchronized as part of this integration between Dataverse and Finance.</span></span>

![Descripció general sobre els fluxos de dades del Project Operations](./media/ProjectOperationsFlows.jpg)

<span data-ttu-id="406a7-108">El Project Operations al Dataverse proporciona una interfície d'usuari (IU) moderna i extensibilitat senzilla sense codi o de baix codi mitjançant capacitats del Power Platform.</span><span class="sxs-lookup"><span data-stu-id="406a7-108">Project Operations on Dataverse provides a modern user interface (UI) and easy no-code/low-code extensibility using Power Platform capabilities.</span></span> <span data-ttu-id="406a7-109">Els administradors de projectes, els administradors de recursos, els membres de l'equip del projecte i altres persones d'atenció al públic duen a terme les seves activitats al Project Operations del Dataverse.</span><span class="sxs-lookup"><span data-stu-id="406a7-109">Project managers, Resource managers, Project team members, and other front-office personas, perform their activities in Project Operations on Dataverse.</span></span>

<span data-ttu-id="406a7-110">El Project Operations a Finances proporciona suport de comptabilitat del projecte i de reconeixement d'ingressos.</span><span class="sxs-lookup"><span data-stu-id="406a7-110">Project Operations in Finance provides project accounting and revenue recognition support.</span></span> <span data-ttu-id="406a7-111">El Project Operations es connecta al marc financer de Finances per al càlcul de l'impost de vendes, els tipus de canvi de moneda, els informes de condicions financeres, etc.</span><span class="sxs-lookup"><span data-stu-id="406a7-111">Project Operations plugs in to the financial framework in Finance for sales tax calculation, currency exchange rates, financial dimension reporting, and more.</span></span> <span data-ttu-id="406a7-112">Les experiències del comptable del projecte són principalment en Finances.</span><span class="sxs-lookup"><span data-stu-id="406a7-112">The Project accountant experiences are mostly based in Finance.</span></span>

<span data-ttu-id="406a7-113">La integració del Project Operations consisteix en la integració de components següent:</span><span class="sxs-lookup"><span data-stu-id="406a7-113">Project Operations integration consists of the following component integration:</span></span>


- [<span data-ttu-id="406a7-114">Configuració del Project Operations i integració de les dades de configuració</span><span class="sxs-lookup"><span data-stu-id="406a7-114">Project Operations setup and configuration data integration</span></span>](resource-dual-write-setup-integration.md) 
- [<span data-ttu-id="406a7-115">Valors reals i estimacions del projecte</span><span class="sxs-lookup"><span data-stu-id="406a7-115">Project estimates and actuals</span></span>](resource-dual-write-estimates-actuals.md)
- [<span data-ttu-id="406a7-116">Factures del projecte</span><span class="sxs-lookup"><span data-stu-id="406a7-116">Project invoices</span></span>](resource-dual-write-project-invoice.md)
- [<span data-ttu-id="406a7-117">Administració de despeses</span><span class="sxs-lookup"><span data-stu-id="406a7-117">Expense management</span></span>](resource-dual-write-expense.md)
- [<span data-ttu-id="406a7-118">Factura del proveïdor</span><span class="sxs-lookup"><span data-stu-id="406a7-118">Vendor invoice</span></span>](resource-dual-write-vendor-invoice.md)
