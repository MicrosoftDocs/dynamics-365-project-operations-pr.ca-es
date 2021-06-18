---
title: Informació general de la implementació del Project Operations per a escenaris basats en recursos/no mantinguts en existències
description: En aquest tema es proporciona informació sobre el tipus d'implementació del Project Operations per a escenaris basats en recursos/no mantinguts en existències.
author: rumant
ms.date: 11/02/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ca8c0894dff1a74b532f8262278fb20400f097c5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001234"
---
# <a name="project-operations-for-resourcenon-stocked-based-scenarios-deployment-overview"></a><span data-ttu-id="3aa51-103">Informació general de la implementació del Project Operations per a escenaris basats en recursos/no mantinguts en existències</span><span class="sxs-lookup"><span data-stu-id="3aa51-103">Project Operations for resource/non-stocked based scenarios deployment overview</span></span>

<span data-ttu-id="3aa51-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_</span><span class="sxs-lookup"><span data-stu-id="3aa51-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="3aa51-105">El tipus d'implementació, Dynamics 365 Project Operations per a escenaris basats en recursos/no mantinguts en existències té les capacitats següents per a les empreses basades en projectes:</span><span class="sxs-lookup"><span data-stu-id="3aa51-105">The deployment type, Dynamics 365 Project Operations for resource/non-stocked based scenarios has the following capabilities for project-based companies:</span></span>

- <span data-ttu-id="3aa51-106">Planificació de projectes mitjançant el Microsoft Project per al web</span><span class="sxs-lookup"><span data-stu-id="3aa51-106">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="3aa51-107">Preus i costos multidimensionals per a recursos de treball</span><span class="sxs-lookup"><span data-stu-id="3aa51-107">Multi-dimensional pricing and costing for labor resources</span></span>
- <span data-ttu-id="3aa51-108">Preus basats en categories per a categories de despesa</span><span class="sxs-lookup"><span data-stu-id="3aa51-108">Category-based pricing for expense categories</span></span>
- <span data-ttu-id="3aa51-109">Administració de vendes basada en projectes mitjançant les característiques del Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="3aa51-109">Project-based sales management using Dynamics 365 Sales capabilities</span></span>
- <span data-ttu-id="3aa51-110">Universal Resource Scheduling, que s'integra amb altres aplicacions, com ara el Dynamics 365 Field Service i el Dynamics 365 Customer Service</span><span class="sxs-lookup"><span data-stu-id="3aa51-110">Universal resource scheduling that integrates with other applications such as Dynamics 365 Field Service and Dynamics 365 Customer Service</span></span>
- <span data-ttu-id="3aa51-111">Seguiment del progrés i el temps del projecte</span><span class="sxs-lookup"><span data-stu-id="3aa51-111">Project progress and Time Tracking</span></span>
- <span data-ttu-id="3aa51-112">Experiències d'administració de despeses bàsiques i completes per a despeses del projecte i que no són del projecte, incloent-hi la captura de rebuts mitjançant característiques d'OCR</span><span class="sxs-lookup"><span data-stu-id="3aa51-112">Basic and full Expense management experiences for project and non-project expenses including receipt capture using OCR capabilities</span></span>
- <span data-ttu-id="3aa51-113">Facturació que s'estén des de la proforma a la orientada al client i que es basa en un sistema d'impost de vendes de classe empresarial i tipus de canvi amb data d'efectivitat.</span><span class="sxs-lookup"><span data-stu-id="3aa51-113">Invoicing that extends from proforma to customer-facing and is backed by an enterprise-class sales tax and date-effective exchange rate system.</span></span>
- <span data-ttu-id="3aa51-114">Costos del projecte, perfils d'ingressos i les regles configurables per a la comptabilitat del treball en curs i les acumulacions</span><span class="sxs-lookup"><span data-stu-id="3aa51-114">Configurable project cost, revenue profiles, and rules for work in progress (WIP) accounting and accruals</span></span>
- <span data-ttu-id="3aa51-115">Reconeixement d'ingressos del projecte</span><span class="sxs-lookup"><span data-stu-id="3aa51-115">Project revenue recognition</span></span>
- <span data-ttu-id="3aa51-116">Extensibilitat a través del Power Platform</span><span class="sxs-lookup"><span data-stu-id="3aa51-116">Extensibility through the Power Platform</span></span>

<span data-ttu-id="3aa51-117">Aquest tipus de implementació proporciona una extensió de la funcionalitat proporcionada per les aplicacions Dynamics 365 Finance i Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="3aa51-117">This deployment type provides an extension to the functionality provided by Dynamics 365 Finance and Dynamics 365 Supply Chain Management applications.</span></span>

<span data-ttu-id="3aa51-118">Utilitzeu aquest tipus d'implementació si l'expectativa del Project Operations és utilitzar el cicle de vida complet del projecte amb els següents requisits:</span><span class="sxs-lookup"><span data-stu-id="3aa51-118">This deployment should be chosen the expectation of Project Operations is to use the full project lifecycle that includes the following requirements:</span></span>

- <span data-ttu-id="3aa51-119">Possibilitat d'administrar vendes basades en projectes amb altres tipus de vendes mitjançant les funcionalitats de l'aplicació Sales.</span><span class="sxs-lookup"><span data-stu-id="3aa51-119">Ability to manage project-based sales with other types of sales using the capabilities in the Sales application.</span></span>
- <span data-ttu-id="3aa51-120">Sistema d'administració de projectes integrat que permet administrar els projectes interns i facturables per a planificacions i finances des de les vendes de projectes fins a la comptabilitat.</span><span class="sxs-lookup"><span data-stu-id="3aa51-120">An integrated project management system that manages internal and billable projects for schedules and financials from project sales to accounting.</span></span>
- <span data-ttu-id="3aa51-121">Sistema d'administració de despeses que inclou aplicacions de normes i reemborsaments per al seguiment de les despeses del projecte i les que no són del projecte.</span><span class="sxs-lookup"><span data-stu-id="3aa51-121">An expense management system that includes policy enforcements and reimbursements for tracking project and non-project expenses.</span></span>
- <span data-ttu-id="3aa51-122">Necessiteu un motor d'impostos de vendes de classe empresarial ric i de tipus de canvi per generar factures de projectes per als clients.</span><span class="sxs-lookup"><span data-stu-id="3aa51-122">Require a rich, enterprise-class sales tax and exchange rate engine to generate customer-facing invoices for projects.</span></span>
- <span data-ttu-id="3aa51-123">Sistema de comptabilitat del projecte i reconeixement d'ingressos que compleix amb els estàndards d'informes financers internacionals (IRFS).</span><span class="sxs-lookup"><span data-stu-id="3aa51-123">An International Financial Reporting Standards(IFRS)-compliant project accounting and revenue recognition system.</span></span>
- <span data-ttu-id="3aa51-124">Aplicacions de finances o administració de cadenes de subministrament i integració de transaccions basades en projectes.</span><span class="sxs-lookup"><span data-stu-id="3aa51-124">Finance or Supply Chain Management applications and integration of project-based transactions.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]