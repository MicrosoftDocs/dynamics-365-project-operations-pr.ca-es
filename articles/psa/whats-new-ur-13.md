---
title: Novetats o canvis de la versió d'actualització 13 del Project Service Automation, V3
description: En aquest tema es proporciona informació sobre les novetats a la versió d'actualització 13 del Project Service Automation, V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 435b70255dd0053a496362c9ced9e742cfcca843
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072172"
---
# <a name="project-service-automation-update-release-13-v3"></a><span data-ttu-id="11ba0-103">Project Service Automation, versió d'actualització 13, V3</span><span class="sxs-lookup"><span data-stu-id="11ba0-103">Project Service Automation Update Release 13, V3</span></span>
<span data-ttu-id="11ba0-104">Ens complau anunciar la darrera actualització de l'aplicació Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="11ba0-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="11ba0-105">Aquesta versió inclou algunes millores importants per a la qualitat, el rendiment i la usabilitat.</span><span class="sxs-lookup"><span data-stu-id="11ba0-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="11ba0-106">Aquest llançament és compatible amb el Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="11ba0-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="11ba0-107">Per actualitzar a aquesta versió, visiteu el Centre d'administració del Dynamics 365 en línia i aneu a la pàgina de solucions per instal·lar l'actualització.</span><span class="sxs-lookup"><span data-stu-id="11ba0-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="11ba0-108">Per obtenir més informació, vegeu [Instal·lar, actualitzar o eliminar una solució preferida](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="11ba0-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="11ba0-109">En aquest tema es mostren les característiques i correccions que són noves o s'han canviat per al Project Service Automation V3, versió d'actualització 13.</span><span class="sxs-lookup"><span data-stu-id="11ba0-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 13.</span></span> <span data-ttu-id="11ba0-110">Aquesta versió té el número de compilació V3.10.3.18 i està disponible segons la planificació següent:</span><span class="sxs-lookup"><span data-stu-id="11ba0-110">This version has a build number of V3.10.3.18 and is available on the following schedule:</span></span>

- <span data-ttu-id="11ba0-111">**Disponibilitat general (actualització automàtica):** novembre de 2019</span><span class="sxs-lookup"><span data-stu-id="11ba0-111">**General availability (self-update):** November 2019</span></span>
- <span data-ttu-id="11ba0-112">**Actualització automàtica:** desembre de 2019</span><span class="sxs-lookup"><span data-stu-id="11ba0-112">**Auto-update:** December 2019</span></span>


## <a name="update-release-13"></a><span data-ttu-id="11ba0-113">Versió d'actualització 13</span><span class="sxs-lookup"><span data-stu-id="11ba0-113">Update Release 13</span></span> 

### <a name="bug-fixes"></a><span data-ttu-id="11ba0-114">Correccions d'errors</span><span class="sxs-lookup"><span data-stu-id="11ba0-114">Bug fixes</span></span>

- <span data-ttu-id="11ba0-115">Temps i despesa</span><span class="sxs-lookup"><span data-stu-id="11ba0-115">Time and Expense</span></span>

     - <span data-ttu-id="11ba0-116">Correcció: la funcionalitat de cerca de la pàgina **Aprovació de despeses** no funciona en fer una cerca per finalitat de la despesa.</span><span class="sxs-lookup"><span data-stu-id="11ba0-116">Fixed: Search functionality on the **Expense approval** page does not work when searching by expense purpose.</span></span>

- <span data-ttu-id="11ba0-117">Administració de recursos</span><span class="sxs-lookup"><span data-stu-id="11ba0-117">Resource Management</span></span>

     - <span data-ttu-id="11ba0-118">Correcció: els números de la conciliació s'ha actualitzat per tal que es justifiquin a la dreta.</span><span class="sxs-lookup"><span data-stu-id="11ba0-118">Fixed: Numbers in the reconciliation have been updated to be right justified.</span></span>
     - <span data-ttu-id="11ba0-119">Correcció: els recursos amb nom no es poden assignar a tasques a través de la pestanya **Planificació**.</span><span class="sxs-lookup"><span data-stu-id="11ba0-119">Fixed: Named Resources can't be assigned to tasks through the **Schedule** tab.</span></span>

- <span data-ttu-id="11ba0-120">Administració de projectes</span><span class="sxs-lookup"><span data-stu-id="11ba0-120">Project Management</span></span>

     - <span data-ttu-id="11ba0-121">Correcció: excepció de referència nul·la en assignar un membre d'un equip quan falta la informació de configuració de **TransactionType** per a **Unitat** i **DefaultGroup**.</span><span class="sxs-lookup"><span data-stu-id="11ba0-121">Fixed: Null reference exception when assigning team member when the **TransactionType** is missing setup information for **Unit** and **DefaultGroup**.</span></span>

- <span data-ttu-id="11ba0-122">Sales</span><span class="sxs-lookup"><span data-stu-id="11ba0-122">Sales</span></span>

     - <span data-ttu-id="11ba0-123">Correcció: els registres de tipus de transacció duplicats retornen un error quan es creen registres de preu de funció.</span><span class="sxs-lookup"><span data-stu-id="11ba0-123">Fixed: Duplicate transaction type records return an error when role price records are created.</span></span>
     - <span data-ttu-id="11ba0-124">Correcció: els botons addicionals per a **Nova oportunitat** , **Oferta** , **Línia de comanda** i **Afegeix un producte** són visibles a les ordres per a Oportunitats, Ofertes, Productes de la comanda i la subquadrícula Línies basada en el projecte.</span><span class="sxs-lookup"><span data-stu-id="11ba0-124">Fixed: Extra buttons for **New Opportunity** , **Quote** , **Order Line** , and **Add Product** are visible in commands for Opportunities, Quotes, Order Products, and the project-based Lines sub-grid.</span></span>


