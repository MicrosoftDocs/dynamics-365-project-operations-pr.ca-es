---
title: Novetats o canvis de la versió d'actualització 20 del Project Service Automation, V3
description: En aquest tema es mostren les característiques i correccions disponibles al Project Service Automation V3, versió d'actualització 20
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 06/12/2020
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
ms.openlocfilehash: 124dad5438f9489d1ddbc952cecaee977b6b7f01
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949082"
---
# <a name="project-service-automation-update-release-20-v3"></a><span data-ttu-id="66809-103">Project Service Automation, versió d'actualització 20, V3</span><span class="sxs-lookup"><span data-stu-id="66809-103">Project Service Automation Update Release 20, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="66809-104">Estem encantats d'anunciar-vos l'última actualització per a l'aplicació Project Service Automation per al Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="66809-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="66809-105">Aquesta versió inclou algunes millores importants per a la qualitat, el rendiment i la usabilitat.</span><span class="sxs-lookup"><span data-stu-id="66809-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="66809-106">Aquest llançament és compatible amb el Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="66809-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="66809-107">Per actualitzar a aquesta versió, visiteu el Centre d'administració del Dynamics 365 en línia i aneu a la pàgina de solucions per instal·lar l'actualització.</span><span class="sxs-lookup"><span data-stu-id="66809-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="66809-108">Per obtenir més informació, vegeu [Instal·lar, actualitzar o eliminar una solució preferida](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="66809-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="66809-109">En aquest tema es mostren les característiques i correccions que són noves o s'han canviat per al Project Service Automation V3, versió d'actualització 20.</span><span class="sxs-lookup"><span data-stu-id="66809-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 20.</span></span> <span data-ttu-id="66809-110">Aquesta versió té el número de compilació V 3.10.31.37 i està disponible de manera general a través d'una actualització automàtica el juny de 2020.</span><span class="sxs-lookup"><span data-stu-id="66809-110">This version has a build number of V 3.10.31.37 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-20"></a><span data-ttu-id="66809-111">Versió d'actualització 20</span><span class="sxs-lookup"><span data-stu-id="66809-111">Update Release 20</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="66809-112">Correccions d'errors</span><span class="sxs-lookup"><span data-stu-id="66809-112">Bug fixes</span></span>

<span data-ttu-id="66809-113">**Administració de projectes**</span><span class="sxs-lookup"><span data-stu-id="66809-113">**Project Management**</span></span>

<span data-ttu-id="66809-114">S'han corregit els problemes següents:</span><span class="sxs-lookup"><span data-stu-id="66809-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="66809-115">La importació dels membres de l'equip del projecte amb un mètode d'assignació que requereix hores resulta en un missatge d'error confús quan les hores especificades són zero.</span><span class="sxs-lookup"><span data-stu-id="66809-115">Importing project team members with an allocation method that requires hours results in an unclear error message when the specified hours are zero.</span></span>
- <span data-ttu-id="66809-116">Els usuaris reben un error incorrecte quan s'ha introduït el nombre màxim de caràcters en el camp **Descripció** d'una tasca de projecte.</span><span class="sxs-lookup"><span data-stu-id="66809-116">Users receive an incorrect error when the maximum number of characters have been entered into the **Description** field for a project task.</span></span>
- <span data-ttu-id="66809-117">La pàgina de baixada de complements del **Microsoft Dynamics 365 Project Service Automation** redirigeix a la pàgina de baixada en anglès quan la configuració de llengua de l'usuari es defineix com a Japonès.</span><span class="sxs-lookup"><span data-stu-id="66809-117">The **Microsoft Dynamics 365 Project Service Automation add-in download** page redirects to the English download page when the user’s language settings are set to Japanese.</span></span>
- <span data-ttu-id="66809-118">Quan es produeix un error del servidor, l'etiqueta de sincronització de la pestanya **Planificació** del formulari **Projectes** de vegades no desapareix.</span><span class="sxs-lookup"><span data-stu-id="66809-118">When a server error occurs, the synchronization label on the **Schedule** tab of the **Projects** form sometimes remains.</span></span>
- <span data-ttu-id="66809-119">S'envien actualitzacions de tasques redundants al servidor quan es modifica una tasca.</span><span class="sxs-lookup"><span data-stu-id="66809-119">Redundant task updates are being sent to the server when a task is modified.</span></span>

<span data-ttu-id="66809-120">**Sales**</span><span class="sxs-lookup"><span data-stu-id="66809-120">**Sales**</span></span>

<span data-ttu-id="66809-121">S'han corregit els problemes següents:</span><span class="sxs-lookup"><span data-stu-id="66809-121">The following issues have been fixed:</span></span>

- <span data-ttu-id="66809-122">Al formulari **Contracte**, fer doble clic a **Crea una factura** crea dues factures per a un únic registre de valors reals.</span><span class="sxs-lookup"><span data-stu-id="66809-122">On the **Contract** form, double-clicking **Create Invoice** creates two invoices for a single actuals record.</span></span>
- <span data-ttu-id="66809-123">A l'Internet Explorer 11, els usuaris no poden crear entrades de despeses.</span><span class="sxs-lookup"><span data-stu-id="66809-123">In Internet Explorer 11, users are unable to create expense entries.</span></span>
- <span data-ttu-id="66809-124">La revocació del cost i dels valors reals de vendes no facturades no s'enllaça.</span><span class="sxs-lookup"><span data-stu-id="66809-124">Reversal of Cost and reversal of Unbilled Sales Actuals are not linked.</span></span>
- <span data-ttu-id="66809-125">El botó **Actualitza els valors reals** del formulari **Projecte** no actualitza **Hores reals de la tasca**.</span><span class="sxs-lookup"><span data-stu-id="66809-125">The **Refresh Actuals** button on the **Project** form does not refresh **Task Actual Hours**.</span></span>
- <span data-ttu-id="66809-126">El complement **PreValidateProjectTeamMemberCreate** pot crear recursos reservables genèrics duplicats si l'atribut **msdyn_isgenericresourceprojectscoped** està definit com a **fals**.</span><span class="sxs-lookup"><span data-stu-id="66809-126">The **PreValidateProjectTeamMemberCreate** plug-in can create duplicate generic bookable resources when the attribute **msdyn_isgenericresourceprojectscoped** is set to **False**.</span></span>
- <span data-ttu-id="66809-127">**Torna a calcular** esborra els costos facturables de detalls de la línia d'oferta basada en productes i detalls de la línia de contracte.</span><span class="sxs-lookup"><span data-stu-id="66809-127">**Recalculate** clears chargeable costs of product-based quote line details and contract line details.</span></span>
- <span data-ttu-id="66809-128">En escenaris concrets, el complement **PostEstimateLineUpdate** mostra un error d'excepció de referència nul·la.</span><span class="sxs-lookup"><span data-stu-id="66809-128">In specific scenarios, the **PostEstimateLineUpdate** plug-in displays a null teference exception error.</span></span>
- <span data-ttu-id="66809-129">Duració de la fase de temps del **Gràfic d'anàlisi de rendibilitat** no coincideix amb la duració dels costos del detall de la línia d'oferta de preu fix de l'oferta.</span><span class="sxs-lookup"><span data-stu-id="66809-129">Time phase duration on the **Profitability Analysis Chart** does not match duration of the costs in the fixed-price quote line detail of the quote.</span></span>
- <span data-ttu-id="66809-130">Els valors d'unitat i grup d'unitats no canvien per defecte correctament per a les categories de despesa als formularis **Detalls de la línia de contracte** i **Detalls de la línia d'oferta**.</span><span class="sxs-lookup"><span data-stu-id="66809-130">Unit and unit group values do not default correctly for expense categories on the **Contract Line Details** and **Quote Line Details** forms.</span></span>
- <span data-ttu-id="66809-131">Les llistes **Preu de cost per unitat organitzativa** permeten solapaments en la data de l'efectivitat.</span><span class="sxs-lookup"><span data-stu-id="66809-131">**Org Unit Cost Price** lists permit overlaps in the date effectivity.</span></span>
- <span data-ttu-id="66809-132">Els usuaris no poden canviar la **Unitat organitzativa** quan el tipus de comanda no està basat en el treball, ja que produirà un error d'excepció de referència nul·la.</span><span class="sxs-lookup"><span data-stu-id="66809-132">Users are not permitted to change the **OrgUnit** when the order type is not work-based because it will lead to a null reference exception error.</span></span>
- <span data-ttu-id="66809-133">Quan intenteu navegar del formulari **Detalls de la línia d'oferta** a la pestanya **Oferta**, el formulari s'actualitza i es mostrarà la pestanya **Resum**.</span><span class="sxs-lookup"><span data-stu-id="66809-133">When attempting to navigate from the **Quote Line Details** form, back to the **Quote** tab, the form refreshes and displays the **Summary** tab.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]