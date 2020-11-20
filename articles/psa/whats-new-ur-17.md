---
title: Novetats o canvis de la versió d'actualització 17 del Project Service Automation, V3
description: En aquest tema es mostren les característiques i correccions disponibles al Project Service Automation V3, versió d'actualització 17.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 03/06/2020
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
ms.openlocfilehash: bb93208217972639f91b39b7b6705d9897373ef7
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4126786"
---
# <a name="project-service-automation-update-release-17-v3"></a><span data-ttu-id="dc984-103">Project Service Automation, versió d'actualització 17, V3</span><span class="sxs-lookup"><span data-stu-id="dc984-103">Project Service Automation Update Release 17, V3</span></span>

<span data-ttu-id="dc984-104">Estem encantats d'anunciar-vos l'última actualització per a l'aplicació Project Service Automation per al Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="dc984-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="dc984-105">Aquesta versió inclou algunes millores importants per a la qualitat, el rendiment i la usabilitat.</span><span class="sxs-lookup"><span data-stu-id="dc984-105">This release includes some important improvements to quality, performance, and usability.</span></span>  <span data-ttu-id="dc984-106">Aquest llançament és compatible amb el Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="dc984-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="dc984-107">Per actualitzar a aquesta versió, visiteu el Centre d'administració del Dynamics 365 en línia i aneu a la pàgina de solucions per instal·lar l'actualització.</span><span class="sxs-lookup"><span data-stu-id="dc984-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="dc984-108">Per obtenir més informació, vegeu [Instal·lar, actualitzar o eliminar una solució preferida](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="dc984-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="dc984-109">En aquest tema es mostren les característiques i correccions que són noves o s'han canviat per al PSA V3, versió d'actualització 17.</span><span class="sxs-lookup"><span data-stu-id="dc984-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 17.</span></span> <span data-ttu-id="dc984-110">Aquesta versió té el número de compilació V3.10.6.34 i està disponible de forma general a través d'una actualització automàtica el març de 2020.</span><span class="sxs-lookup"><span data-stu-id="dc984-110">This version has a build number of V3.10.6.34 and is generally available through a self-update in March 2020.</span></span>


## <a name="update-release-17"></a><span data-ttu-id="dc984-111">Versió d'actualització 17</span><span class="sxs-lookup"><span data-stu-id="dc984-111">Update Release 17</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="dc984-112">Correccions d'errors</span><span class="sxs-lookup"><span data-stu-id="dc984-112">Bug fixes</span></span>

<span data-ttu-id="dc984-113">**General**</span><span class="sxs-lookup"><span data-stu-id="dc984-113">**General**</span></span>

- <span data-ttu-id="dc984-114">Correcció: actualitza el Project Service Automation per aplicar les llicències dels membres de l'equip (el centre de recursos de projecte inclourà les metadades 3.x del pla del servei membre d'equip)</span><span class="sxs-lookup"><span data-stu-id="dc984-114">Fixed: Update Project Service Automation to enforce Team Member licenses (Project Resource Hub will include Team Member Service plan metadata 3.x)</span></span>
 
<span data-ttu-id="dc984-115">**Temps i despesa**</span><span class="sxs-lookup"><span data-stu-id="dc984-115">**Time and Expense**</span></span>

- <span data-ttu-id="dc984-116">Correcció: no és possible canviar una estimació de despesa d’un preu diferent de zero a zero (0).</span><span class="sxs-lookup"><span data-stu-id="dc984-116">Fixed: It is not possible to change an expense estimate from a non-zero price to zero (0).</span></span> <span data-ttu-id="dc984-117">El canvi s’ignora.</span><span class="sxs-lookup"><span data-stu-id="dc984-117">The change is ignored.</span></span>

<span data-ttu-id="dc984-118">**Administració de projectes**</span><span class="sxs-lookup"><span data-stu-id="dc984-118">**Project Management**</span></span>

- <span data-ttu-id="dc984-119">Correcció: s’ha afegit una comprovació de valors nuls al nom de posició d’un membre de l’equip.</span><span class="sxs-lookup"><span data-stu-id="dc984-119">Fixed: A check for null values has been added on a team member's position name.</span></span>
- <span data-ttu-id="dc984-120">Correcció: el camp **msdyn_userresourceid** de l'entitat **msdyn_resourceassignment** ha quedat obsolet.</span><span class="sxs-lookup"><span data-stu-id="dc984-120">Fixed: **msdyn_userresourceid** field on the **msdyn_resourceassignment** entity has been deprecated.</span></span>
- <span data-ttu-id="dc984-121">Correcció: l’actualització de 2.x a 3.x ara controla els contorns d’esforç buits a les assignacions de tasques.</span><span class="sxs-lookup"><span data-stu-id="dc984-121">Fixed: Upgrade from 2.x to 3.x now handles empty effort contours on task assignments.</span></span>

<span data-ttu-id="dc984-122">**Sales**</span><span class="sxs-lookup"><span data-stu-id="dc984-122">**Sales**</span></span>

- <span data-ttu-id="dc984-123">Correcció: **Invoice.PreValidateInvoiceUpdate** ara gestiona l'escenari de reassignació dels propietaris de registres correctament.</span><span class="sxs-lookup"><span data-stu-id="dc984-123">Fixed: **Invoice.PreValidateInvoiceUpdate** now handles the scenario of reassigning record owners properly.</span></span>
- <span data-ttu-id="dc984-124">Correcció: quan la classe de transacció és **Time**, **UnitGroup** no es pot editar per a les entitats que inclouen **QuoteLineDetails**, **JournalLine**, **InvoiceLineDetail** i **ContractLineDetails**.</span><span class="sxs-lookup"><span data-stu-id="dc984-124">Fixed: When the transaction class is **Time**, **UnitGroup** is non-editable for all entities including, **QuoteLineDetails**, **JournalLine**, **InvoiceLineDetail**, and **ContractLineDetails**.</span></span> <span data-ttu-id="dc984-125">Això no obstant, **Unit** no es pot editar només per a **JournalLine** i **InvoiceLineDetails**.</span><span class="sxs-lookup"><span data-stu-id="dc984-125">However, **Unit** is non-editable only for **JournalLine** and **InvoiceLineDetails**.</span></span>


