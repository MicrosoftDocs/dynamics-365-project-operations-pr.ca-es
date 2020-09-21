---
title: Novetats a la versió d'actualització 13 del Project Service Automation, V3
description: En aquest tema es proporciona informació sobre les novetats a la versió d'actualització 13 del Project Service Automation, V3.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: c6f6a5b6-b5bb-467c-b7c7-7fb962504c6d
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 5f1b6b3879c94a77ab62082aad1e470a3ba66552
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749494"
---
# <a name="project-service-automation-v3-update-release-13"></a><span data-ttu-id="0b819-103">Project Service Automation V3, versió d'actualització 13</span><span class="sxs-lookup"><span data-stu-id="0b819-103">Project Service Automation V3, Update Release 13</span></span>
<span data-ttu-id="0b819-104">Ens complau anunciar la darrera actualització de l'aplicació Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="0b819-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="0b819-105">Aquesta versió inclou algunes millores importants per a la qualitat, el rendiment i la usabilitat.</span><span class="sxs-lookup"><span data-stu-id="0b819-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="0b819-106">Aquest llançament és compatible amb el Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="0b819-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="0b819-107">Per actualitzar a aquesta versió, visiteu el Centre d'administració del Dynamics 365 en línia i aneu a la pàgina de solucions per instal·lar l'actualització.</span><span class="sxs-lookup"><span data-stu-id="0b819-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="0b819-108">Per obtenir més informació, vegeu [Instal·lar, actualitzar o eliminar una solució preferida](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="0b819-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="0b819-109">En aquest tema es mostren les característiques i correccions que són noves o s'han canviat per al Project Service Automation V3, versió d'actualització 13.</span><span class="sxs-lookup"><span data-stu-id="0b819-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 13.</span></span> <span data-ttu-id="0b819-110">Aquesta versió té el número de compilació V3.10.3.18 i està disponible segons la planificació següent:</span><span class="sxs-lookup"><span data-stu-id="0b819-110">This version has a build number of V3.10.3.18 and is available on the following schedule:</span></span>

- <span data-ttu-id="0b819-111">**Disponibilitat general (actualització automàtica):** novembre de 2019</span><span class="sxs-lookup"><span data-stu-id="0b819-111">**General availability (self-update):** November 2019</span></span>
- <span data-ttu-id="0b819-112">**Actualització automàtica:** desembre de 2019</span><span class="sxs-lookup"><span data-stu-id="0b819-112">**Auto-update:** December 2019</span></span>


## <a name="update-release-13"></a><span data-ttu-id="0b819-113">Versió d'actualització 13</span><span class="sxs-lookup"><span data-stu-id="0b819-113">Update Release 13</span></span> 

### <a name="bug-fixes"></a><span data-ttu-id="0b819-114">Correccions d'errors</span><span class="sxs-lookup"><span data-stu-id="0b819-114">Bug fixes</span></span>

- <span data-ttu-id="0b819-115">Temps i despesa</span><span class="sxs-lookup"><span data-stu-id="0b819-115">Time and Expense</span></span>

     - <span data-ttu-id="0b819-116">Correcció: la funcionalitat de cerca de la pàgina **Aprovació de despeses** no funciona en fer una cerca per finalitat de la despesa.</span><span class="sxs-lookup"><span data-stu-id="0b819-116">Fixed: Search functionality on the **Expense approval** page does not work when searching by expense purpose.</span></span>

- <span data-ttu-id="0b819-117">Administració de recursos</span><span class="sxs-lookup"><span data-stu-id="0b819-117">Resource Management</span></span>

     - <span data-ttu-id="0b819-118">Correcció: els números de la conciliació s'ha actualitzat per tal que es justifiquin a la dreta.</span><span class="sxs-lookup"><span data-stu-id="0b819-118">Fixed: Numbers in the reconciliation have been updated to be right justified.</span></span>
     - <span data-ttu-id="0b819-119">Correcció: els recursos amb nom no es poden assignar a tasques a través de la pestanya **Planificació**.</span><span class="sxs-lookup"><span data-stu-id="0b819-119">Fixed: Named Resources can't be assigned to tasks through the **Schedule** tab.</span></span>

- <span data-ttu-id="0b819-120">Administració de projectes</span><span class="sxs-lookup"><span data-stu-id="0b819-120">Project Management</span></span>

     - <span data-ttu-id="0b819-121">Correcció: excepció de referència nul·la en assignar un membre d'un equip quan falta la informació de configuració de **TransactionType** per a **Unitat** i **DefaultGroup**.</span><span class="sxs-lookup"><span data-stu-id="0b819-121">Fixed: Null reference exception when assigning team member when the **TransactionType** is missing setup information for **Unit** and **DefaultGroup**.</span></span>

- <span data-ttu-id="0b819-122">Sales</span><span class="sxs-lookup"><span data-stu-id="0b819-122">Sales</span></span>

     - <span data-ttu-id="0b819-123">Correcció: els registres de tipus de transacció duplicats retornen un error quan es creen registres de preu de funció.</span><span class="sxs-lookup"><span data-stu-id="0b819-123">Fixed: Duplicate transaction type records return an error when role price records are created.</span></span>
     - <span data-ttu-id="0b819-124">Correcció: els botons addicionals per a **Nova oportunitat**, **Oferta**, **Línia de comanda** i **Afegeix un producte** són visibles a les ordres per a Oportunitats, Ofertes, Productes de la comanda i la subquadrícula Línies basada en el projecte.</span><span class="sxs-lookup"><span data-stu-id="0b819-124">Fixed: Extra buttons for **New Opportunity**, **Quote**, **Order Line**, and **Add Product** are visible in commands for Opportunities, Quotes, Order Products, and the project-based Lines sub-grid.</span></span>


