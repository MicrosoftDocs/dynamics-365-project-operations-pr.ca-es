---
title: Camps del Project Operations com a dimensions de preus
description: En aquest tema es proporciona informació sobre l'ús de camps com a dimensions de preus al Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 56ff45169058d96d7ef81a710de309eec698a75f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072275"
---
# <a name="project-operations-fields-as-pricing-dimensions"></a><span data-ttu-id="27e81-103">Camps del Project Operations com a dimensions de preus</span><span class="sxs-lookup"><span data-stu-id="27e81-103">Project Operations fields as pricing dimensions</span></span>

<span data-ttu-id="27e81-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_</span><span class="sxs-lookup"><span data-stu-id="27e81-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="27e81-105">L'entitat **Valors reals** té diversos camps que es poden utilitzar com a dimensions de preus per a la fixació de preus basats en recursos.</span><span class="sxs-lookup"><span data-stu-id="27e81-105">The **Actuals** entity has many fields that can be used as pricing dimensions for resource-based pricing.</span></span> <span data-ttu-id="27e81-106">Per exemple, un camp comú és un **Recurs que es pot reservar**.</span><span class="sxs-lookup"><span data-stu-id="27e81-106">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="27e81-107">Les empreses més petites que tenen menys de 20-30 recursos facturables poden trobar que tenir taxes de factura i cost específiques per a cada recurs és una aproximació més simple.</span><span class="sxs-lookup"><span data-stu-id="27e81-107">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="27e81-108">No obstant això, a mesura que la força de treball creix, podria ser poc realista mantenir tarifes específiques per recurs.</span><span class="sxs-lookup"><span data-stu-id="27e81-108">However, as the billable workforce grows, resource-secific rates could become unrealistic to maintain.</span></span> <span data-ttu-id="27e81-109">El cost dels recursos i les tarifes de facturació comencen a variar a mesura que els recursos reben ascensos, guanyen més experiència o adquireixen un conjunt d'habilitats diferent.</span><span class="sxs-lookup"><span data-stu-id="27e81-109">Resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different set of skills.</span></span> 

<span data-ttu-id="27e81-110">Un altre exemple és el de la categoria de transacció.</span><span class="sxs-lookup"><span data-stu-id="27e81-110">Another example is that of transaction category.</span></span> <span data-ttu-id="27e81-111">Els clients i els executors han utilitzat la categoria de transacció per classificar el treball i utilitzen el camp per posar el preu i el cost basat en la categoria de treball.</span><span class="sxs-lookup"><span data-stu-id="27e81-111">Customers and Implementers have used the transaction category to classify work and use the field to price and cost based on the category of work.</span></span>
