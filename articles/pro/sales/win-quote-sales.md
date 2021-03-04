---
title: Tancament d'una oferta (bàsic)
description: En aquest tema es proporciona informació sobre el tancament d'una oferta al Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 8d387816f51f63ecd95df6534c7c012b323e6ddc
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764852"
---
# <a name="close-a-quote---lite"></a><span data-ttu-id="1a73f-103">Tancament d'una oferta (bàsic)</span><span class="sxs-lookup"><span data-stu-id="1a73f-103">Close a quote - lite</span></span>

<span data-ttu-id="1a73f-104">_**S'aplica a:** implementació bàsica: tracte de facturació proforma_</span><span class="sxs-lookup"><span data-stu-id="1a73f-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="1a73f-105">Una oportunitat de projecte es pot tancar com a guanyada o perduda.</span><span class="sxs-lookup"><span data-stu-id="1a73f-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="1a73f-106">Una oferta en esborrany es pot tancar perquè les operacions Activa i Revisa a les ofertes no estàn admeses al Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="1a73f-106">A draft quote can be closed because the Activate and Revise operations on quotes isn't supported in Microsoft Dynamics 365 Project Operations.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="1a73f-107">Tancament d'una oferta com a guanyada</span><span class="sxs-lookup"><span data-stu-id="1a73f-107">Close a quote as Won</span></span>

<span data-ttu-id="1a73f-108">Quan tanqueu una oferta de projecte com a Guanyada, l'estat es defineix com a Tancat i la raó per a l'estat és Guanyat.</span><span class="sxs-lookup"><span data-stu-id="1a73f-108">When you close a project quote as Won, the status is set to Closed and the status reason is Won.</span></span> <span data-ttu-id="1a73f-109">Quan tanqueu l'oferta, l'oferta del projecte és de només de lectura i crea un esborrany de contracte del projecte que conté la informació de l'oferta.</span><span class="sxs-lookup"><span data-stu-id="1a73f-109">Closing the quote makes the project quote read-only and creates a draft project contract that contains the quote information.</span></span> <span data-ttu-id="1a73f-110">Com que una oferta tancada no es pot tornar a obrir, un diàleg de confirmació confirmarà els canvis.</span><span class="sxs-lookup"><span data-stu-id="1a73f-110">Because a closed quote can't be reopened, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="1a73f-111">Si l'oferta està unida a una oportunitat, la resta d'ofertes de projectes a l'oportunitat es tancaran automàticament com a perdudes.</span><span class="sxs-lookup"><span data-stu-id="1a73f-111">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="1a73f-112">Impacte financer del tancament d'una oferta com a guanyada</span><span class="sxs-lookup"><span data-stu-id="1a73f-112">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="1a73f-113">Si hi ha valors reals per al temps en un projecte mentre encara està adjunt a un esborrany d'oferta, només es registra el cost del temps o la despesa.</span><span class="sxs-lookup"><span data-stu-id="1a73f-113">If there are any actuals for time on a project while is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="1a73f-114">Després de tancar una oferta com a guanyada, l'aplicació refactoritzarà els costos revertint els valors reals del cost més antics i tornant a crear valors reals de cost nous.</span><span class="sxs-lookup"><span data-stu-id="1a73f-114">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="1a73f-115">L'aplicació processarà els valors reals d'aquests costos en funció del mètode de facturació de la línia de contracte del projecte associat.</span><span class="sxs-lookup"><span data-stu-id="1a73f-115">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="1a73f-116">Si el valors reals del cost fan referència a una línia de contracte de temps i materials, es creen els valors reals de vendes no facturats corresponents per al moment en què l'oferta es tanqui i es creï el contracte del projecte.</span><span class="sxs-lookup"><span data-stu-id="1a73f-116">If the cost actuals reference a time and material contract line, corresponding unbilled sales actuals are created for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="1a73f-117">Si els valors reals del cost fan referència a una línia de contracte de preu fix, l'aplicació deixarà de reprocessar els valors reals del cost que es basen en les regles de facturació fraccionades per als clients de contracte del projecte.</span><span class="sxs-lookup"><span data-stu-id="1a73f-117">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals that are based on the split billing rules for the project contract customers.</span></span>

## <a name="closing-a-quote-as-lost"></a><span data-ttu-id="1a73f-118">Tancament d'una oferta com a perduda:</span><span class="sxs-lookup"><span data-stu-id="1a73f-118">Closing a quote as lost:</span></span>

<span data-ttu-id="1a73f-119">Quan tanqueu una oferta de projecte com a Perduda, l'estat es defineix com a Tancat i la raó per a l'estat és Perdut.</span><span class="sxs-lookup"><span data-stu-id="1a73f-119">When you close a project quote as Lost, the status is set to Closed and status reason is Lost.</span></span> <span data-ttu-id="1a73f-120">En tancar l'oferta, l'oferta del projecte passa a ser només de lectura.</span><span class="sxs-lookup"><span data-stu-id="1a73f-120">Closing the quote makes the project quote read-only.</span></span> <span data-ttu-id="1a73f-121">Com que no es pot tornar a obrir una oferta tancada, abans de tancar una oferta, un quadre de diàleg de confirmació confirmarà els canvis.</span><span class="sxs-lookup"><span data-stu-id="1a73f-121">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="1a73f-122">Si l'oferta del projecte que es tanca com a Perduda fa referència a un projecte en qualsevol de les seves línies, aquest projecte també es marca com a Tancat.</span><span class="sxs-lookup"><span data-stu-id="1a73f-122">If the project quote that is closed as Lost references a project on any of its lines, that project is also marked as Closed.</span></span> <span data-ttu-id="1a73f-123">Qualsevol reserva de recursos a partir d'aquell dia es cancel·la.</span><span class="sxs-lookup"><span data-stu-id="1a73f-123">Any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="1a73f-124">Al Project Operations, si tanqueu una oferta com a guanyada o perduda, l'estat de l'oportunitat no es veurà afectat i romandrà oberta fins que es tanqui manualment.</span><span class="sxs-lookup"><span data-stu-id="1a73f-124">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>
