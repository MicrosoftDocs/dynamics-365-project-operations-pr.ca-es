---
title: Confirmació d'un contracte de projecte
description: Aquest tema proporciona informació sobre com confirmar un contracte al Project Operations.
author: rumant
ms.date: 10/13/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b5eabcad028a8282f552f3571b170d9b933a7b88
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003664"
---
# <a name="confirm-a-project-contract"></a><span data-ttu-id="782dc-103">Confirmació d'un contracte de projecte</span><span class="sxs-lookup"><span data-stu-id="782dc-103">Confirm a project contract</span></span>

<span data-ttu-id="782dc-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_</span><span class="sxs-lookup"><span data-stu-id="782dc-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="782dc-105">Un contracte de projecte al Dynamics 365 Project Operations pot estar actiu amb un motiu de **Confirmat** o tancat amb un motiu de **Perdut**.</span><span class="sxs-lookup"><span data-stu-id="782dc-105">A project contract in Dynamics 365 Project Operations can be active with a reason of **Confirmed**, or closed with a reason of **Lost**.</span></span> <span data-ttu-id="782dc-106">Quan es confirma un contracte de projecte, l'estat s'actualitza d'**Esborrany** a **Actiu** i la raó per a l'estat és **Confirmat**.</span><span class="sxs-lookup"><span data-stu-id="782dc-106">When you confirm a project contract, the status updates from **Draft** to **Active** and the status reason is **Confirmed**.</span></span> <span data-ttu-id="782dc-107">Un contracte actiu o tancat no es pot editar o reobrir.</span><span class="sxs-lookup"><span data-stu-id="782dc-107">An active or closed contract can't be edited or reopened.</span></span> 

### <a name="financial-impact-of-confirming-a-project-contract"></a><span data-ttu-id="782dc-108">Impacte financer de confirmar un contracte de projecte</span><span class="sxs-lookup"><span data-stu-id="782dc-108">Financial impact of confirming a project contract</span></span>

<span data-ttu-id="782dc-109">Després que es confirmi un contracte de projecte, l'aplicació recalcula els costos invertint els valors reals de cost més antics i creant nous valors reals de cost.</span><span class="sxs-lookup"><span data-stu-id="782dc-109">After a project contract is confirmed, the application recalculates the costs by reversing the older cost actuals and creating new cost actuals.</span></span> <span data-ttu-id="782dc-110">Els nous valors reals de cost llavors es processen segons el mètode de facturació de la línia de contracte del projecte associat.</span><span class="sxs-lookup"><span data-stu-id="782dc-110">The new cost actuals are then processed based on the billing method of the associated project contract line.</span></span> <span data-ttu-id="782dc-111">Si els valors reals de cost fan referència a una línia de contracte de temps i material, l'aplicació torna a crear automàticament els valors reals de vendes no facturades corresponents.</span><span class="sxs-lookup"><span data-stu-id="782dc-111">If the cost actuals reference a Time and Material contract line, the application automatically re-creates corresponding unbilled sales actuals.</span></span> <span data-ttu-id="782dc-112">Si els valors reals de cost fan referència a una línia de contracte de preu fix, l'aplicació deixa de processar els valors reals de cost.</span><span class="sxs-lookup"><span data-stu-id="782dc-112">If the cost actuals reference a Fixed Price contract line, the application stops reprocessing the cost actuals.</span></span>

<span data-ttu-id="782dc-113">Els límits que no s'han de superar, la configuració d'imputabilitat i els preus i el cost dels valors reals s'avaluen i s'actualitzen com a part del procés de confirmació.</span><span class="sxs-lookup"><span data-stu-id="782dc-113">Not-to-exceed limits, chargeability setup, and pricing and costing on the actuals is evaluated and then updated as part of the confirmations process.</span></span>

## <a name="close-a-project-contract-as-lost"></a><span data-ttu-id="782dc-114">Tancar un contracte de projecte com a perdut</span><span class="sxs-lookup"><span data-stu-id="782dc-114">Close a project contract as lost</span></span>

<span data-ttu-id="782dc-115">Quan es tanca un contracte de projecte com a perdut, l'estat del contracte s'actualitza a **Tancat** i la raó per a l'estat és **Perdut**.</span><span class="sxs-lookup"><span data-stu-id="782dc-115">When you close a project contract as lost, the contract status is updated to **Closed** and the status reason is **Lost**.</span></span> <span data-ttu-id="782dc-116">El contracte del projecte es converteix en només de lectura.</span><span class="sxs-lookup"><span data-stu-id="782dc-116">The project contract becomes read-only.</span></span> <span data-ttu-id="782dc-117">Es proporciona un diàleg de confirmació abans que els canvis es completin perquè no podeu reobrir un contracte de projecte tancat.</span><span class="sxs-lookup"><span data-stu-id="782dc-117">A confirmation dialog is provided before the changes are complete because you can't reopen a closed project contract.</span></span>

<span data-ttu-id="782dc-118">Si el contracte de projecte que es tanca com a perdut fa referència a un projecte en les seves línies, aquest projecte també es marca com a tancat.</span><span class="sxs-lookup"><span data-stu-id="782dc-118">If the project contract that is closed as lost references a project on its lines, that project is also marked as closed.</span></span> <span data-ttu-id="782dc-119">Qualsevol reserva de recursos a partir d'aquell dia es cancel·la.</span><span class="sxs-lookup"><span data-stu-id="782dc-119">Any resource bookings from that day forward are canceled.</span></span> <span data-ttu-id="782dc-120">Es revertirà qualsevol valor real de venda sense facturar al contracte del projecte que no estigui en una factura.</span><span class="sxs-lookup"><span data-stu-id="782dc-120">Any unbilled sales actuals on the project contract that aren't already on an invoice, will be reversed.</span></span>

> [!NOTE]
> <span data-ttu-id="782dc-121">Al Dynamics 365 Project Operations, el tancament d'un contracte de projecte com a perdut no afectarà aquest estat de l'oportunitat associada.</span><span class="sxs-lookup"><span data-stu-id="782dc-121">In Dynamics 365 Project Operations, closing a project contract as lost will not impact that status of the associated opportunity.</span></span> <span data-ttu-id="782dc-122">L'oportunitat romandrà oberta i ha de tancar-se manualment.</span><span class="sxs-lookup"><span data-stu-id="782dc-122">The opportunity will remain open and must be manually closed.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]