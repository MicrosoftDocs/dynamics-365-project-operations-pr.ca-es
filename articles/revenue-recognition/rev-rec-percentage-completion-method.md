---
title: Projectes d'estimació d'ingressos de preu fix
description: En aquest tema es proporciona informació sobre els ingressos de preu fix en projectes.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 80fe1d4171d80ca39e8b7ebb1eefaa524a4f2b07
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531366"
---
# <a name="fixed-price-revenue-estimate-projects"></a><span data-ttu-id="fa602-103">Projectes d'estimació d'ingressos de preu fix</span><span class="sxs-lookup"><span data-stu-id="fa602-103">Fixed price revenue estimate projects</span></span> 

<span data-ttu-id="fa602-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_</span><span class="sxs-lookup"><span data-stu-id="fa602-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="fa602-105">Quan creeu una línia de contracte de projecte amb els atributs següents al Dynamics 365 Project Operations al Microsoft Dataverse, el sistema crea automàticament un projecte d'estimació d'ingressos de preu fix.</span><span class="sxs-lookup"><span data-stu-id="fa602-105">When you create a project contract line with the following attributes in Dynamics 365 Project Operations on Microsoft Dataverse, the system automatically creates a fixed price revenue estimate project.</span></span> <span data-ttu-id="fa602-106">La informació d'aquest projecte es basa en el següent:</span><span class="sxs-lookup"><span data-stu-id="fa602-106">The information in this project is based on the following:</span></span>

  - <span data-ttu-id="fa602-107">Un mètode de facturació de preu fix.</span><span class="sxs-lookup"><span data-stu-id="fa602-107">A fixed price billing method.</span></span>
  - <span data-ttu-id="fa602-108">Un projecte associat.</span><span class="sxs-lookup"><span data-stu-id="fa602-108">An associated project.</span></span>
  - <span data-ttu-id="fa602-109">Com a mínim una fita definida a la pestanya **Planificació de la factura** de la pàgina **Línia de contracte del projecte**.</span><span class="sxs-lookup"><span data-stu-id="fa602-109">At least one milestone defined on the **Invoice schedule** tab on the **Project contract line** page.</span></span>

## <a name="review-fixed-price-revenue-estimates-projects"></a><span data-ttu-id="fa602-110">Revisió de projectes d'estimació d'ingressos de preu fix</span><span class="sxs-lookup"><span data-stu-id="fa602-110">Review fixed price revenue estimates projects</span></span>
<span data-ttu-id="fa602-111">Per revisar els projectes d'estimació d'ingressos de preu fix, seguiu aquests passos:</span><span class="sxs-lookup"><span data-stu-id="fa602-111">To review fixed price revenue estimates projects, complete the following steps:</span></span>

1. <span data-ttu-id="fa602-112">A l'entorn del Dynamics 365 Finance, aneu a **Gestió de projectes i comptabilitat** > **Projectes** > **Projectes d'estimació d'ingressos de preu fix**.</span><span class="sxs-lookup"><span data-stu-id="fa602-112">In the Dynamics 365 Finance environment, go to **Projects management and accounting** > **Projects** > **Fixed price revenue estimate projects**.</span></span>
2. <span data-ttu-id="fa602-113">Seleccioneu el projecte que voleu visualitzar i feu doble clic a **Identificador del projecte d'estimació** per obrir el registre i revisar els detalls del projecte.</span><span class="sxs-lookup"><span data-stu-id="fa602-113">Select the project that you want to view and double-click the **Estimate project ID** to open the record and review the details of the project.</span></span>
3. <span data-ttu-id="fa602-114">Expandiu la pestanya **Projecte**. Veureu un projecte a la quadrícula **Projectes seleccionats**.</span><span class="sxs-lookup"><span data-stu-id="fa602-114">Expand the **Project** tab. You will see one project in the **Selected projects** grid.</span></span> <span data-ttu-id="fa602-115">El sistema l'utilitza com a projecte per defecte perquè és el projecte associat a la línia de contracte del projecte.</span><span class="sxs-lookup"><span data-stu-id="fa602-115">The system uses this as default project because it is the project associated to the project contract line.</span></span> 
4. <span data-ttu-id="fa602-116">Per canviar l'associació, seleccioneu projectes addicionals i afegiu-los a la quadrícula **Projectes seleccionats**.</span><span class="sxs-lookup"><span data-stu-id="fa602-116">To change the association, select additional projects and add them to the **Selected projects** grid.</span></span> <span data-ttu-id="fa602-117">Si se seleccionen diversos projectes en aquesta quadrícula, el percentatge completat del projecte i les estimacions d'ingressos es calculen junts per a tots els projectes seleccionats.</span><span class="sxs-lookup"><span data-stu-id="fa602-117">If multiple projects are selected in this grid, the project percentage completion and revenue estimates are calculated together for of the all selected projects.</span></span>

  <span data-ttu-id="fa602-118">El cost del projecte, el perfil d'ingressos, la plantilla de costos i el codi del període es poden definir manualment.</span><span class="sxs-lookup"><span data-stu-id="fa602-118">Project cost, revenue profile, cost template, and the period code can be set manually.</span></span> <span data-ttu-id="fa602-119">Si no es defineixen manualment, els valors per defecte durant el càlcul de la primera estimació del projecte fan servir les regles configurades per als perfils de costos i ingressos del projecte.</span><span class="sxs-lookup"><span data-stu-id="fa602-119">If they aren't set manually, the values default during the first estimate calculation for the project using the rules configured for project cost and revenue profiles.</span></span>

