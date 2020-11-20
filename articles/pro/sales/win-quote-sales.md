---
title: Tancament d'una oferta (bàsic)
description: En aquest tema es proporciona informació sobre el tancament d'una oferta al Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5ad206232d616cdbdc83e2a17b9177cfb98ffda9
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/30/2020
ms.locfileid: "4175699"
---
# <a name="close-a-quote---lite"></a><span data-ttu-id="ddc23-103">Tancament d'una oferta (bàsic)</span><span class="sxs-lookup"><span data-stu-id="ddc23-103">Close a quote - lite</span></span>

<span data-ttu-id="ddc23-104">_**S'aplica a:** implementació bàsica: tracte de facturació proforma_</span><span class="sxs-lookup"><span data-stu-id="ddc23-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ddc23-105">Una oportunitat de projecte es pot tancar com a guanyada o perduda.</span><span class="sxs-lookup"><span data-stu-id="ddc23-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="ddc23-106">les operacions d'activació i revisió en les ofertes no s'admeten al Microsoft Dynamics 365 Project Operations; per tant, es pot tancar un esborrany d'oferta.</span><span class="sxs-lookup"><span data-stu-id="ddc23-106">The Activate and Revise operations on quotes is not supported in Microsoft Dynamics 365 Project Operations, so a draft quote can be closed.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="ddc23-107">Tancament d'una oferta com a guanyada</span><span class="sxs-lookup"><span data-stu-id="ddc23-107">Close a quote as Won</span></span>

<span data-ttu-id="ddc23-108">El tancament d'una oferta de projecte com a guanyada tancarà l'oferta amb l'estat definit com a Tancada i la raó per a l'estat definida com a Guanyada.</span><span class="sxs-lookup"><span data-stu-id="ddc23-108">Closing a project quote as Won will close the quote with the status set to Closed and the status reason set to Won.</span></span> <span data-ttu-id="ddc23-109">Quan tanqueu l'oferta, l'oferta del projecte és de només de lectura i crea un esborrany de contracte del projecte que conté la informació de l'oferta.</span><span class="sxs-lookup"><span data-stu-id="ddc23-109">Closing the quote makes the project quote read-only and creates a draft project contract that contains the quote information.</span></span> <span data-ttu-id="ddc23-110">Com que no es pot tornar a obrir una oferta tancada, hi ha un quadre de diàleg de confirmació abans que es facin els canvis, ja que una oferta tancada no es pot tornar a obrir i els canvis són irreversibles.</span><span class="sxs-lookup"><span data-stu-id="ddc23-110">Because a closed quote can't be reopened, a confirmation dialog There is a confirmation dialog before the changes are done since a closed quote cannot be re-opened and the changes are irreversible.</span></span>

<span data-ttu-id="ddc23-111">Si l'oferta està unida a una oportunitat, la resta d'ofertes de projectes a l'oportunitat es tancaran automàticament com a perdudes.</span><span class="sxs-lookup"><span data-stu-id="ddc23-111">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="ddc23-112">Impacte financer del tancament d'una oferta com a guanyada</span><span class="sxs-lookup"><span data-stu-id="ddc23-112">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="ddc23-113">Si no s'ha registrat cap valor real per al temps enregistrat en un projecte mentre encara està vinculat a un esborrany d'oferta, només es registra el cost del temps o de la despesa.</span><span class="sxs-lookup"><span data-stu-id="ddc23-113">If there have been any actuals for time recorded on a project while it is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="ddc23-114">Després de tancar una oferta com a guanyada, l'aplicació refactoritzarà els costos revertint els valors reals del cost més antics i tornant a crear valors reals de cost nous.</span><span class="sxs-lookup"><span data-stu-id="ddc23-114">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="ddc23-115">L'aplicació processarà els valors reals d'aquests costos en funció del mètode de facturació de la línia de contracte del projecte associat.</span><span class="sxs-lookup"><span data-stu-id="ddc23-115">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="ddc23-116">Si els valors reals de costos fan referència a una línia de contracte de temps i material, el sistema crearà automàticament valors reals de vendes sense facturar per a quan es tanqui l'oferta i es creï el contracte del projecte.</span><span class="sxs-lookup"><span data-stu-id="ddc23-116">If the cost actuals reference a time and material contract line, the system will automatically create corresponding unbilled sales actuals for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="ddc23-117">Si els valors reals de cost fan referència a una línia de contracte de preu fix, l'aplicació deixarà de tornar a processar els valors reals de cost en funció de les regles de divisió de la facturació per als clients del contracte del projecte.</span><span class="sxs-lookup"><span data-stu-id="ddc23-117">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals based on the split billing rules for the project contract customers.</span></span>

## <a name="closing-a-quote-as-lost"></a><span data-ttu-id="ddc23-118">Tancament d'una oferta com a perduda:</span><span class="sxs-lookup"><span data-stu-id="ddc23-118">Closing a quote as lost:</span></span>

<span data-ttu-id="ddc23-119">Si tanqueu una oferta de projecte com a Perduda, es definirà l'estat com a Tancada i la raó per a l'estat a Perduda.</span><span class="sxs-lookup"><span data-stu-id="ddc23-119">Closing a project quote as Lost will set the status to Closed and status reason to Lost.</span></span> <span data-ttu-id="ddc23-120">En tancar l'oferta, l'oferta del projecte passa a ser només de lectura.</span><span class="sxs-lookup"><span data-stu-id="ddc23-120">Closing the quote makes the project quote read-only.</span></span> <span data-ttu-id="ddc23-121">Com que no es pot tornar a obrir una oferta tancada, abans de tancar una oferta, un quadre de diàleg de confirmació confirmarà els canvis.</span><span class="sxs-lookup"><span data-stu-id="ddc23-121">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="ddc23-122">Si l'oferta del projecte que es tanca com a perduda té un projecte al qual es fa referència en qualsevol de les seves línies, aquest projecte també es marca com a tancat i totes les reserves de recursos a partir d'aquell dia es cancel·len.</span><span class="sxs-lookup"><span data-stu-id="ddc23-122">If the project quote that is closed as Lost has a project referenced on any of its lines, that project is also marked as Closed and any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="ddc23-123">Al Project Operations, si tanqueu una oferta com a guanyada o perduda, l'estat de l'oportunitat no es veurà afectat i romandrà oberta fins que es tanqui manualment.</span><span class="sxs-lookup"><span data-stu-id="ddc23-123">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>
