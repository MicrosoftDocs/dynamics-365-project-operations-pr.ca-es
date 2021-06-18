---
title: Crear entrades de temps
description: En aquest tema es proporciona informació sobre com crear entrades de temps.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 05/20/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: bc8e52fef0aa02505e412c746343ce1410c40ac3
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999254"
---
# <a name="create-time-entries"></a><span data-ttu-id="e69f4-103">Crear entrades de temps</span><span class="sxs-lookup"><span data-stu-id="e69f4-103">Create time entries</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="e69f4-104">En versions anteriors del Dynamics 365 Project Service Automation, les entrades de temps s'introduïen de manera setmanal.</span><span class="sxs-lookup"><span data-stu-id="e69f4-104">In previous versions of Dynamics 365 Project Service Automation, time entries were entered on a weekly basis.</span></span> <span data-ttu-id="e69f4-105">A la versió 3 del Project Service Automation, les entrades de temps s'introdueixen diàriament.</span><span class="sxs-lookup"><span data-stu-id="e69f4-105">In version 3 of Project Service Automation, time entries are entered on a daily basis.</span></span> <span data-ttu-id="e69f4-106">No obstant això, després de crear algunes entrades de temps, podeu crear-ne més massivament o copiar-les.</span><span class="sxs-lookup"><span data-stu-id="e69f4-106">However, after a few time entries have been created, you can bulk create or copy them.</span></span>

## <a name="create-a-time-entry"></a><span data-ttu-id="e69f4-107">Crear una entrada de temps</span><span class="sxs-lookup"><span data-stu-id="e69f4-107">Create a time entry</span></span>

<span data-ttu-id="e69f4-108">Seguiu els passos que es descriuen a continuació per crear una entrada de temps.</span><span class="sxs-lookup"><span data-stu-id="e69f4-108">Follow these steps to create a time entry.</span></span>

1. <span data-ttu-id="e69f4-109">A la pàgina **Entrades de temps**, seleccioneu **Nova**.</span><span class="sxs-lookup"><span data-stu-id="e69f4-109">On the **Time Entries** page, select **New**.</span></span>
2. <span data-ttu-id="e69f4-110">Al quadre de diàleg **Creació ràpida: entrada de temps**, introduïu la duració de l'entrada de temps en minuts, hores o dies.</span><span class="sxs-lookup"><span data-stu-id="e69f4-110">In the **Quick Create: Time Entry** dialog box, enter the duration of the time entry in minutes, hours, or days.</span></span> <span data-ttu-id="e69f4-111">La duració s'ha d'escriure en el format següent: "*x* minuts", "*x* hores" o "*x* dies".</span><span class="sxs-lookup"><span data-stu-id="e69f4-111">The duration must be entered in the following format: *x* minutes, *x* hours, or *x* days.</span></span> <span data-ttu-id="e69f4-112">Les hores i els dies també es poden escriure amb decimals, per exemple, "*x,x* hores" o "*x,x* dies".</span><span class="sxs-lookup"><span data-stu-id="e69f4-112">Hours and days can also be entered as decimal values, such as *x.x* hours or *x.x* days.</span></span>
3. <span data-ttu-id="e69f4-113">Seleccioneu el tipus d'entrada de temps i el projecte per al qual introduïu l'entrada de temps.</span><span class="sxs-lookup"><span data-stu-id="e69f4-113">Select the type of time entry and the project that you're entering the time entry for.</span></span>
4. <span data-ttu-id="e69f4-114">Al camp **Tasca del projecte**, cerqueu la tasca per a l'entrada de temps.</span><span class="sxs-lookup"><span data-stu-id="e69f4-114">In the **Project Task** field, find the task for this time entry.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e69f4-115">Si esteu creant una entrada de temps per a una tasca que no està assignada a un usuari , al camp **Tasca del projecte**, seleccioneu el botó **Cerca**, seleccioneu **Canvia la visualització** i, a continuació, seleccioneu **Totes les tasques actives del projecte** per llistar totes les tasques.</span><span class="sxs-lookup"><span data-stu-id="e69f4-115">If you're creating a time entry for a task that isn't assigned to a user, in the **Project Task** field, select the **Search** button, select **Change View**, and then select **All Active Project Tasks** to list all tasks.</span></span>

5. <span data-ttu-id="e69f4-116">Introduïu una descripció, si cal una descripció i, a continuació, seleccioneu **Desa i tanca**.</span><span class="sxs-lookup"><span data-stu-id="e69f4-116">Enter a description, if a description is required, and then select **Save and Close**.</span></span>

<span data-ttu-id="e69f4-117">Després d'haver creat i desat l'entrada de temps, podeu editar-la a la quadrícula d'entrada de temps.</span><span class="sxs-lookup"><span data-stu-id="e69f4-117">After the time entry is created and saved, you can edit it in the time entry grid.</span></span> <span data-ttu-id="e69f4-118">La quadrícula d'entrada de temps admet dos formats:</span><span class="sxs-lookup"><span data-stu-id="e69f4-118">The time entry grid supports two formats:</span></span>

- <span data-ttu-id="e69f4-119">Podeu introduir entrades de temps en el format **hh:mm**.</span><span class="sxs-lookup"><span data-stu-id="e69f4-119">You can enter time entries in **hh:mm** format.</span></span> <span data-ttu-id="e69f4-120">Aquest format es converteix en hores i fraccions.</span><span class="sxs-lookup"><span data-stu-id="e69f4-120">This format is then converted to hours and fractions.</span></span>
- <span data-ttu-id="e69f4-121">Podeu introduir hores i fraccions directament.</span><span class="sxs-lookup"><span data-stu-id="e69f4-121">You can enter hours and fractions directly.</span></span>

<span data-ttu-id="e69f4-122">Heu de tenir en compte que les fraccions d'una hora no són minuts.</span><span class="sxs-lookup"><span data-stu-id="e69f4-122">Note that the fractions of an hour aren't minutes.</span></span> <span data-ttu-id="e69f4-123">Per tant, 1,5 hores representen 1 hora i 30 minuts.</span><span class="sxs-lookup"><span data-stu-id="e69f4-123">Therefore, 1.5 hours represents 1 hour and 30 minutes.</span></span> <span data-ttu-id="e69f4-124">La mateixa regla s'aplica a les fraccions d'un dia.</span><span class="sxs-lookup"><span data-stu-id="e69f4-124">The same rule applies to fractions of a day.</span></span> <span data-ttu-id="e69f4-125">Un dia és de 24 hores, i 0,5 dies representen 12 hores.</span><span class="sxs-lookup"><span data-stu-id="e69f4-125">One day is 24 hours, and 0.5 days represents 12 hours.</span></span>

## <a name="bulk-create-time-entries"></a><span data-ttu-id="e69f4-126">Crear entrades de temps massivament</span><span class="sxs-lookup"><span data-stu-id="e69f4-126">Bulk create time entries</span></span>

<span data-ttu-id="e69f4-127">Després de crear algunes d'entrades de temps, podeu copiar-les per crear entrades de temps addicionals massivament.</span><span class="sxs-lookup"><span data-stu-id="e69f4-127">After a few time entries have been created, you can copy them to create additional time entries in bulk.</span></span>

1. <span data-ttu-id="e69f4-128">A la pàgina **Entrades de temps**, seleccioneu **Copia la setmana**.</span><span class="sxs-lookup"><span data-stu-id="e69f4-128">On the **Time Entries** page, select **Copy Week**.</span></span>
2. <span data-ttu-id="e69f4-129">Al grup de camps **Del període**, utilitzeu els camps **Data d'inici** i **Data de finalització** per definir l'interval de dates des d'on copiar entrades de temps.</span><span class="sxs-lookup"><span data-stu-id="e69f4-129">In the **From Period** field group, in the **Start Date** and **End Date** fields, define the date range to copy time entries from.</span></span>
3. <span data-ttu-id="e69f4-130">Al grup de camps **Al període**, al camp **Data d'inici**, especifiqueu la data on crear les entrades de temps.</span><span class="sxs-lookup"><span data-stu-id="e69f4-130">In the **To Period** field group, in the **Start Date** field, specify the date to create time entries for.</span></span>
4. <span data-ttu-id="e69f4-131">Seleccioneu **Copia** per crear una còpia de les entrades de temps que corresponen al dia de la setmana que s'especifica al grup de camps **Al període**.</span><span class="sxs-lookup"><span data-stu-id="e69f4-131">Select **Copy** to create a copy of the time entries that correspond to the day of the week that is specified in the **To Period** field group.</span></span> <span data-ttu-id="e69f4-132">Per exemple, l'entrada de temps del dilluns de la setmana passada es copia al dilluns de la setmana especificada al grup de camps **Al període**.</span><span class="sxs-lookup"><span data-stu-id="e69f4-132">For example, the time entry for Monday of last week is copied to Monday of the week that is specified in the **To Period** field group.</span></span>

## <a name="import-data-for-time-entries"></a><span data-ttu-id="e69f4-133">Importar dades d'entrades de temps</span><span class="sxs-lookup"><span data-stu-id="e69f4-133">Import data for time entries</span></span>

<span data-ttu-id="e69f4-134">Podeu importar dades a partir de les reserves de projectes i assignacions.</span><span class="sxs-lookup"><span data-stu-id="e69f4-134">You can import data from project bookings and assignments.</span></span> <span data-ttu-id="e69f4-135">Quan importeu dades, podeu especificar l'interval de dates de les reserves que s'han d'importar i, a continuació, seleccionar explícitament les reserves que haurien de crear-se com a entrades de temps **Esborrany**.</span><span class="sxs-lookup"><span data-stu-id="e69f4-135">When you import data, you can specify the date range of the bookings to import and then explicitly select the bookings that should be created as **Draft** time entries.</span></span>

## <a name="group-by-sort-search-and-filter-capabilities"></a><span data-ttu-id="e69f4-136">Agrupar, ordenar, cercar i filtrar capacitats</span><span class="sxs-lookup"><span data-stu-id="e69f4-136">Group by, sort, search, and filter capabilities</span></span>

<span data-ttu-id="e69f4-137">Podeu agrupar i filtrar entrades de temps per les dimensions que s'especifiquen a les columnes.</span><span class="sxs-lookup"><span data-stu-id="e69f4-137">You can group and filter time entries by the dimensions that are specified in the columns.</span></span> <span data-ttu-id="e69f4-138">Al camp **Agrupa per**, seleccioneu la dimensió que s'utilitzarà per filtrar les entrades de temps.</span><span class="sxs-lookup"><span data-stu-id="e69f4-138">In the **Group by** field, select the dimension to use to filter time entries.</span></span> <span data-ttu-id="e69f4-139">També podeu ordenar els registres d'entrada de temps en ordre ascendent o descendent mitjançant la fletxa d'ordenació a les capçaleres de columna.</span><span class="sxs-lookup"><span data-stu-id="e69f4-139">You can also sort the time entry records in ascending or descending order by using the sort arrow on the column headings.</span></span> <span data-ttu-id="e69f4-140">A més, podeu mostrar o amagar les entrades seleccionant el botó **Filtra** a les capçaleres de columna i, a continuació, al quadre **Cerca**, introduint el text que s'hauria d'utilitzar per cercar entrades de temps pel nom del projecte, tasca de projecte, entrada de temps o recurs.</span><span class="sxs-lookup"><span data-stu-id="e69f4-140">Additionally, you can show or hide entries by selecting the **Filter** button on the column headings, and then, in the **Search** box, entering the text that should be used to search for time entries by project name, project task, time entry, or resource.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]