---
title: Utilitzar un camp existent al Project Service com a dimensió de preus
description: En aquest tema es proporciona informació sobre l'ús de camps del Project Service existents com a dimensions de preus.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 415e346f88e60cb064f3327bfb35e21bd1c89014
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072290"
---
# <a name="use-an-existing-field-in-project-service-as-a-pricing-dimension"></a><span data-ttu-id="8bfd4-103">Utilitzar un camp existent al Project Service com a dimensió de preus</span><span class="sxs-lookup"><span data-stu-id="8bfd4-103">Use an existing field in Project Service as a pricing dimension</span></span>

<span data-ttu-id="8bfd4-104">El Project Service Automation (PSA) té diversos camps a l'entitat **Valors reals** que es poden utilitzar com a dimensions de preus per als preus basats en recursos a les organitzacions del projecte.</span><span class="sxs-lookup"><span data-stu-id="8bfd4-104">Project Service Automation (PSA) has many fields on the **Actuals** entity that can be used as pricing dimensions for resource-based pricing in project organizations.</span></span> <span data-ttu-id="8bfd4-105">Per exemple, un camp comú és un **Recurs que es pot reservar**.</span><span class="sxs-lookup"><span data-stu-id="8bfd4-105">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="8bfd4-106">Les empreses més petites que tenen menys de 20-30 recursos facturables poden trobar que tenir taxes de factura i cost específiques per a cada recurs és una aproximació més simple.</span><span class="sxs-lookup"><span data-stu-id="8bfd4-106">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="8bfd4-107">No obstant això, a mesura que la força de treball creix, això podria esdevenir poc realista de mantenir a mesura que el cost de recursos i les taxes de facturació comencen a variar a mesura que els recursos ascendeixen, tenen més experiència o adquireixen un conjunt d'habilitats diferents.</span><span class="sxs-lookup"><span data-stu-id="8bfd4-107">However, as the billable workforce grows, this could become unrealistic to maintain as resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different skill sets.</span></span> <span data-ttu-id="8bfd4-108">Com que aquest enfocament encara funciona per a empreses d'una determinada mida, vegeu el tema [Utilitzar un recurs que es pot reservar com a dimensió de preu](bookable-resource-pricing-dimension.md) per entendre com es podria utilitzar un camp del Project Service existent com a dimensió de preus.</span><span class="sxs-lookup"><span data-stu-id="8bfd4-108">Because this approach still works for companies of a certain size, see the topic, [Use a bookable resource as a pricing dimension](bookable-resource-pricing-dimension.md) to understand how an existing Project Service field can be used as a pricing dimension.</span></span>

<span data-ttu-id="8bfd4-109">Un altre exemple és el de la categoria de transacció.</span><span class="sxs-lookup"><span data-stu-id="8bfd4-109">Another example is that of transaction category.</span></span> <span data-ttu-id="8bfd4-110">Els clients i els executors han utilitzat la categoria de transacció al PSA per classificar el treball i utilitzen el camp per posar el preu i el cost basat en la categoria de treball.</span><span class="sxs-lookup"><span data-stu-id="8bfd4-110">Customers and Implementers have used the transaction category in PSA to classify work and use the field to price and cost based on the category of work.</span></span> <span data-ttu-id="8bfd4-111">Per obtenir més informació, vegeu [Utilitzar la categoria de transacció coma dimensió de preus](transaction-category-pricing-dimension.md).</span><span class="sxs-lookup"><span data-stu-id="8bfd4-111">For more information, see [Use transaction category as a pricing dimension](transaction-category-pricing-dimension.md).</span></span>
