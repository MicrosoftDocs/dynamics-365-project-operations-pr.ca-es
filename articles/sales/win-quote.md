---
title: Tancar una oferta
description: En aquest tema es proporciona informació sobre el tancament d'ofertes al Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a2c752ba6395ed4bf025092219350dc245f7428f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5277236"
---
# <a name="close-a-quote"></a><span data-ttu-id="3c90b-103">Tancar una oferta</span><span class="sxs-lookup"><span data-stu-id="3c90b-103">Close a quote</span></span>

<span data-ttu-id="3c90b-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_</span><span class="sxs-lookup"><span data-stu-id="3c90b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="3c90b-105">Una oportunitat de projecte es pot tancar com a guanyada o perduda.</span><span class="sxs-lookup"><span data-stu-id="3c90b-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="3c90b-106">Com que les funcions Activa i Revisa a les ofertes no estàn admeses al Microsoft Dynamics 365 Project Operations, podeu tancar un esborrany d'oferta.</span><span class="sxs-lookup"><span data-stu-id="3c90b-106">Because the functions Activate and Revise are not supported on quotes in Microsoft Dynamics 365 Project Operations, you can close a draft quote.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="3c90b-107">Tancament d'una oferta com a guanyada</span><span class="sxs-lookup"><span data-stu-id="3c90b-107">Close a quote as Won</span></span>

<span data-ttu-id="3c90b-108">El tancament d'una oferta de projecte com a guanyada definirà l'estat de l'oferta a **Tancada** i la raó per a l'estat a **Guanyada**.</span><span class="sxs-lookup"><span data-stu-id="3c90b-108">Closing a project quote as Won will set the status of the quote to **Closed** and status reason to **Won**.</span></span> <span data-ttu-id="3c90b-109">Quan tanqueu una oferta, passa a ser de només de lectura i es crea un esborrany de contracte del projecte amb tota la informació de l'oferta.</span><span class="sxs-lookup"><span data-stu-id="3c90b-109">Closing the quotes makes it read-only and creates a draft project contract with all the quote information.</span></span> <span data-ttu-id="3c90b-110">Com que no es pot tornar a obrir una oferta tancada, abans de tancar una oferta, un quadre de diàleg de confirmació confirmarà els canvis.</span><span class="sxs-lookup"><span data-stu-id="3c90b-110">Because a closed quote can't be reopened, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="3c90b-111">El contracte de projecte creat a partir d'una oferta de projecte també es posa a la vostra disposició al mòdul d'administració de projectes i comptabilitat del Project Operations.</span><span class="sxs-lookup"><span data-stu-id="3c90b-111">The project contract created from a project quote is also made available in the Project management and accounting module of Project Operations.</span></span> <span data-ttu-id="3c90b-112">Si un contracte de projecte no s'assigna a un projecte a cap de les línies, aquest contracte de projecte es posa a la vostra disposició com a contracte de projecte inactiu i s'activa tan bon punt s'assigna un projecte com a mínim a una de les seves línies de contracte.</span><span class="sxs-lookup"><span data-stu-id="3c90b-112">If a project contract is not mapped to a project on any of its lines, this project contract is made available as an inactive project contract and becomes active as soon as a project is mapped to at least one of its contract lines.</span></span>

<span data-ttu-id="3c90b-113">Si l'oferta està unida a una oportunitat, la resta d'ofertes de projectes a l'oportunitat es tancaran automàticament com a perdudes.</span><span class="sxs-lookup"><span data-stu-id="3c90b-113">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="3c90b-114">Impacte financer del tancament d'una oferta com a guanyada</span><span class="sxs-lookup"><span data-stu-id="3c90b-114">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="3c90b-115">Si no s'ha registrat cap valor real per al temps enregistrat en un projecte mentre encara està vinculat a un esborrany d'oferta, només es registra el cost del temps o de la despesa.</span><span class="sxs-lookup"><span data-stu-id="3c90b-115">If there have been any actuals for time recorded on a project while it is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="3c90b-116">Després de tancar una oferta com a guanyada, l'aplicació refactoritzarà els costos revertint els valors reals del cost més antics i tornant a crear valors reals de cost nous.</span><span class="sxs-lookup"><span data-stu-id="3c90b-116">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="3c90b-117">L'aplicació processarà els valors reals d'aquests costos en funció del mètode de facturació de la línia de contracte del projecte associat.</span><span class="sxs-lookup"><span data-stu-id="3c90b-117">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="3c90b-118">Si els valors reals de costos fan referència a una línia de contracte de temps i material, el sistema crearà automàticament valors reals de vendes sense facturar per a quan es tanqui l'oferta i es creï el contracte del projecte.</span><span class="sxs-lookup"><span data-stu-id="3c90b-118">If the cost actuals reference a time and material contract line, the system will automatically create corresponding unbilled sales actuals for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="3c90b-119">Si els valors reals de cost fan referència a una línia de contracte de preu fix, l'aplicació deixarà de tornar a processar els valors reals de cost en funció de les regles de divisió de la facturació per als clients del contracte del projecte.</span><span class="sxs-lookup"><span data-stu-id="3c90b-119">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals based on the split billing rules for the project contract customers.</span></span>

<span data-ttu-id="3c90b-120">Tots els valors reals tornats a processar estan disponibles al mòdul d'administració de projectes i comptabilitat perquè el comptable del projecte els revisi, actualitzi i comptabilitzi al registre general.</span><span class="sxs-lookup"><span data-stu-id="3c90b-120">All reprocessed actuals are available in the Project management and accounting module for the Project accountant to review, update, and post to the General ledger.</span></span> 

## <a name="close-a-quote-as-lost"></a><span data-ttu-id="3c90b-121">Tancament d'una oferta com a perduda</span><span class="sxs-lookup"><span data-stu-id="3c90b-121">Close a quote as Lost</span></span>

<span data-ttu-id="3c90b-122">Si tanqueu una oferta de projecte com a Perduda, es definirà l'estat com a **Tancada** i la raó per a l'estat a **Perduda**.</span><span class="sxs-lookup"><span data-stu-id="3c90b-122">Closing a project quote as Lost will set the status to **Closed** and status reason to **Lost**.</span></span> <span data-ttu-id="3c90b-123">El tancament de l'oferta fa que sigui només de lectura.</span><span class="sxs-lookup"><span data-stu-id="3c90b-123">Closing the quote makes it read-only.</span></span> <span data-ttu-id="3c90b-124">Com que no es pot tornar a obrir una oferta tancada, abans de tancar una oferta, un quadre de diàleg de confirmació confirmarà els canvis.</span><span class="sxs-lookup"><span data-stu-id="3c90b-124">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="3c90b-125">Si l'oferta del projecte que es tanca com a perduda té un projecte al qual es fa referència en qualsevol de les seves línies, aquest projecte també es marca com a tancat i totes les reserves de recursos a partir d'aquell dia es cancel·len.</span><span class="sxs-lookup"><span data-stu-id="3c90b-125">If the project quote that is closed as Lost has a project referenced on any of its lines, that project is also marked as Closed and any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="3c90b-126">Al Project Operations, si tanqueu una oferta com a guanyada o perduda, l'estat de l'oportunitat no es veurà afectat i romandrà oberta fins que es tanqui manualment.</span><span class="sxs-lookup"><span data-stu-id="3c90b-126">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]