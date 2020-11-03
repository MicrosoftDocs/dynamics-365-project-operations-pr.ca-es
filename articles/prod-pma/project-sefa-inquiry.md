---
title: Consulta de la Planificació de despeses per a concessions federals
description: Aquest tema proporciona informació sobre la consulta de la Planificació de despeses per a concessions federals.
author: velofog
manager: Ann Beebe
ms.date: 04/2/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PSNProjSEFAinquiry
audience: Application User
ms.devlang: ''
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.tgt_pltfrm: ''
ms.custom: ''
ms.search.region: Global
ms.search.industry: public sector
ms.author: andchoi
ms.search.validFrom: 2020-4-01
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: eaf523ab147cbe974fed6e7eab21967404583fe6
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072196"
---
# <a name="schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="b0c2b-103">Consulta de la Planificació de despeses per a concessions federals</span><span class="sxs-lookup"><span data-stu-id="b0c2b-103">Schedule of Expenditures of Federal Awards inquiry</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b0c2b-104">Segons la circular A-133 de l'Oficina d'administració i pressupost, les agències que reben fons federals estan subjectes a requisits d'auditoria, que també es coneixen com a auditories individuals.</span><span class="sxs-lookup"><span data-stu-id="b0c2b-104">According to Office of Management and Budget Circular A-133, agencies that receive federal funds are subject to audit requirements, which are also known as single audits.</span></span> <span data-ttu-id="b0c2b-105">El procés d'auditoria s'utilitza per a informar sobre els ingressos i despeses de les subvencions federals de manera recurrent.</span><span class="sxs-lookup"><span data-stu-id="b0c2b-105">The audit process is used to report on the revenues and expenditures of federal grants on a recurring basis.</span></span> <span data-ttu-id="b0c2b-106">Part de l'informe d'auditoria individual inclou la Planificació de despeses de concessions federals (SEFA).</span><span class="sxs-lookup"><span data-stu-id="b0c2b-106">Part of the single audit report includes the Schedule of Expenditures of Federal Awards (SEFA).</span></span>

<span data-ttu-id="b0c2b-107">La consulta de Planificació de despeses de concessions federals inclou el títol i número del Catàleg d'assistència nacional federal (CFDA), el número de subvenció, l'any de la subvenció, el nom de l'agència federal que proporciona els fons i el nom de l'entitat de traspàs.</span><span class="sxs-lookup"><span data-stu-id="b0c2b-107">The Schedule of Expenditures of Federal Awards inquiry includes the Catalog of Federal Domestic Assistance (CFDA) title and number, the grant number, the year of the grant, the name of the federal agency that provides the funds, and the name of the pass-through entity.</span></span> <span data-ttu-id="b0c2b-108">La consulta és per a un període concret.</span><span class="sxs-lookup"><span data-stu-id="b0c2b-108">The inquiry is for a specific period.</span></span> <span data-ttu-id="b0c2b-109">En general, aquest període és el mateix que el període de declaració financera, que és un any fiscal.</span><span class="sxs-lookup"><span data-stu-id="b0c2b-109">Typically, that period is the same as the financial statement period, which is a fiscal year.</span></span>

<span data-ttu-id="b0c2b-110">La investigació inclou subvencions que tenen dates de projecció a l'interval de dates seleccionat.</span><span class="sxs-lookup"><span data-stu-id="b0c2b-110">The inquiry includes grants that have projection dates in the selected date range.</span></span> <span data-ttu-id="b0c2b-111">La columna **Agència que rep la subvenció** de la consulta mostra el client de la subvenció o, per a una subvenció de traspàs, l'agència que rep la subvenció.</span><span class="sxs-lookup"><span data-stu-id="b0c2b-111">The **Grantor agency** column of the inquiry shows the grant customer or, for a pass-through grant, the grantor agency.</span></span> <span data-ttu-id="b0c2b-112">Per a una subvenció de traspàs, la columna **Agència de traspàs** mostra el client de subvenció.</span><span class="sxs-lookup"><span data-stu-id="b0c2b-112">For a pass-through grant, the **Pass-through agency** column shows the grant customer.</span></span> <span data-ttu-id="b0c2b-113">Si la subvenció no és una subvenció de traspàs, la columna **Agència de traspàs** està en blanc.</span><span class="sxs-lookup"><span data-stu-id="b0c2b-113">If the grant isn't a pass-through grant, the **Pass-through agency** column is blank.</span></span>

## <a name="set-up-the-cfda-clusters"></a><span data-ttu-id="b0c2b-114">Configurar els grups de CFDA</span><span class="sxs-lookup"><span data-stu-id="b0c2b-114">Set up the CFDA clusters</span></span>

<span data-ttu-id="b0c2b-115">Heu d'establir els grups de CFDA que es poden associar amb els números de CFDA a la consulta de la Planificació de despeses de concessions federals.</span><span class="sxs-lookup"><span data-stu-id="b0c2b-115">You must set up the CFDA clusters that can be associated with CFDA numbers in the Schedule of Expenditures of Federal Awards inquiry.</span></span>

1. <span data-ttu-id="b0c2b-116">Aneu a **Administració de projectes i comptabilitat \> Configuració \> Subvencions \> Grups del Catàleg d'assistència nacional federal**.</span><span class="sxs-lookup"><span data-stu-id="b0c2b-116">Go to **Project management and accounting \> Setup \> Grants \> Catalog of Federal Domestic Assistance clusters**.</span></span>
2. <span data-ttu-id="b0c2b-117">Seleccioneu **Nou** per crear un grup de CFDA.</span><span class="sxs-lookup"><span data-stu-id="b0c2b-117">Select **New** to create a CFDA cluster.</span></span>
3. <span data-ttu-id="b0c2b-118">Introduïu el nom del grup.</span><span class="sxs-lookup"><span data-stu-id="b0c2b-118">Enter the cluster name.</span></span>
4. <span data-ttu-id="b0c2b-119">Seleccioneu **Desa**  per desar els canvis.</span><span class="sxs-lookup"><span data-stu-id="b0c2b-119">Select **Save** to save your changes.</span></span>

## <a name="set-up-cfda-numbers"></a><span data-ttu-id="b0c2b-120">Configurar els números de CFDA</span><span class="sxs-lookup"><span data-stu-id="b0c2b-120">Set up CFDA numbers</span></span>

<span data-ttu-id="b0c2b-121">Heu de configurar els números de CFDA que es poden afegir a les subvencions i incloure a la consulta de la Planificació de despeses de concessions federals.</span><span class="sxs-lookup"><span data-stu-id="b0c2b-121">You must set up CFDA numbers that can be added to grants and included in the Schedule of Expenditures of Federal Awards inquiry.</span></span>

1. <span data-ttu-id="b0c2b-122">Aneu a **Administració de projectes i comptabilitat \> Configuració \> Subvencions \> Números del Catàleg d'assistència nacional federal**.</span><span class="sxs-lookup"><span data-stu-id="b0c2b-122">Go to **Project management and accounting \> Setup \> Grants \> Catalog of Federal Domestic Assistance numbers**.</span></span>
2. <span data-ttu-id="b0c2b-123">Seleccioneu **Nou** per crear un número de CFDA.</span><span class="sxs-lookup"><span data-stu-id="b0c2b-123">Select **New** to create a CFDA number.</span></span>
3. <span data-ttu-id="b0c2b-124">A la columna **Número** , introduïu el número de CFDA.</span><span class="sxs-lookup"><span data-stu-id="b0c2b-124">In the **Number** column, enter the CFDA number.</span></span>
4. <span data-ttu-id="b0c2b-125">Premeu la tecla **Tab**.</span><span class="sxs-lookup"><span data-stu-id="b0c2b-125">Press the **Tab** key.</span></span>
5. <span data-ttu-id="b0c2b-126">A la columna **Descripció** , introduïu el títol de CFDA.</span><span class="sxs-lookup"><span data-stu-id="b0c2b-126">In the **Description** column, enter the CFDA title.</span></span>
6. <span data-ttu-id="b0c2b-127">Premeu la tecla **Tab**.</span><span class="sxs-lookup"><span data-stu-id="b0c2b-127">Press the **Tab** key.</span></span>
7. <span data-ttu-id="b0c2b-128">Opcional: en el camp **Grup del programa** , afegiu el grup de CFDA corresponent.</span><span class="sxs-lookup"><span data-stu-id="b0c2b-128">Optional: In the **Program cluster** field, add the appropriate CFDA cluster.</span></span>
8. <span data-ttu-id="b0c2b-129">Seleccioneu **Desa**  per desar els canvis.</span><span class="sxs-lookup"><span data-stu-id="b0c2b-129">Select **Save** to save your changes.</span></span>

## <a name="set-up-grants-to-report-for-the-schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="b0c2b-130">Configurar subvencions per informar-ne a la consulta de la Planificació de despeses de concessions federals</span><span class="sxs-lookup"><span data-stu-id="b0c2b-130">Set up grants to report for the Schedule of Expenditures of Federal Awards inquiry</span></span>

1. <span data-ttu-id="b0c2b-131">Aneu a **Administració de projectes i comptabilitat \> Subvencions \> Subvencions** i seleccioneu una subvenció existent.</span><span class="sxs-lookup"><span data-stu-id="b0c2b-131">Go to **Project management and accounting \> Grants \> Grants** , and select an existing grant.</span></span>
2. <span data-ttu-id="b0c2b-132">Al FastTab **Configuració** , en el camp **Catàleg d'assistència nacional federal** , assigneu el número de CFDA.</span><span class="sxs-lookup"><span data-stu-id="b0c2b-132">On the **Setup** FastTab, in the  **Catalog of Federal Domestic Assistance** field, assign the CFDA number.</span></span> <span data-ttu-id="b0c2b-133">El número de CFDA a la subvenció determina el grup de CFDA per als informes.</span><span class="sxs-lookup"><span data-stu-id="b0c2b-133">The CFDA number on the grant determines the CFDA cluster for reporting.</span></span>
3. <span data-ttu-id="b0c2b-134">Al FastTab **Informació del contacte** , introduïu la informació de qui rebrà la subvenció seguint aquests passos:</span><span class="sxs-lookup"><span data-stu-id="b0c2b-134">On **Contact information** FastTab, enter the grantor information by following these steps:</span></span>

    1. <span data-ttu-id="b0c2b-135">En el camp **Client de la subvenció** , introduïu el client responsable de la subvenció.</span><span class="sxs-lookup"><span data-stu-id="b0c2b-135">In the **Grant customer** field, enter the customer who is responsible for the grant.</span></span> <span data-ttu-id="b0c2b-136">Per a una subvenció existent, aquesta informació ja podria estar introduïda.</span><span class="sxs-lookup"><span data-stu-id="b0c2b-136">For an existing grant, this information might already be entered.</span></span>
    2. <span data-ttu-id="b0c2b-137">Indiqueu si el client de la subvenció és el finançador.</span><span class="sxs-lookup"><span data-stu-id="b0c2b-137">Indicate whether the grant customer is the funder.</span></span> <span data-ttu-id="b0c2b-138">Si el client de la subvenció és el finançador, deixeu la casella de selecció **Traspàs** sense marcar.</span><span class="sxs-lookup"><span data-stu-id="b0c2b-138">If the grant customer is the funder, leave the **Pass-through** check box cleared.</span></span> <span data-ttu-id="b0c2b-139">Si un altre client és el finançador i el client de la subvenció és responsable de gastar i fer el seguiment dels diners, marqueu la casella de selecció **Traspàs**.</span><span class="sxs-lookup"><span data-stu-id="b0c2b-139">If another customer is the funder, and the grant customer is responsible for spending and tracking the money, select the **Pass-through** check box.</span></span>

4. <span data-ttu-id="b0c2b-140">Si marqueu la casella de selecció **Traspàs** en el pas anterior, en el camp **Agència que proporciona la subvenció** , introduïu el client que va proporcionar la subvenció.</span><span class="sxs-lookup"><span data-stu-id="b0c2b-140">If you selected the **Pass-through** check box in the previous step, in the **Grantor agency** field, enter the customer who provided the grant.</span></span> <span data-ttu-id="b0c2b-141">L'agència que proporciona la subvenció i el client de la subvenció no poden ser el mateix client.</span><span class="sxs-lookup"><span data-stu-id="b0c2b-141">The grantor agency and the grant customer can't be the same customer.</span></span>

<span data-ttu-id="b0c2b-142">Aquí teniu un exemple de subvenció de traspàs:</span><span class="sxs-lookup"><span data-stu-id="b0c2b-142">Here is an example of a pass-through grant:</span></span>

<span data-ttu-id="b0c2b-143">El govern federal va finançar un projecte d'infraestructura per a un estat.</span><span class="sxs-lookup"><span data-stu-id="b0c2b-143">The federal government funded an infrastructure project for a state.</span></span> <span data-ttu-id="b0c2b-144">El govern federal va donar els diners a l'estat perquè els gastés.</span><span class="sxs-lookup"><span data-stu-id="b0c2b-144">The federal government gave the money to the state to spend.</span></span> <span data-ttu-id="b0c2b-145">En aquest cas, el govern federal és l'agència que proporciona la subvenció i l'estat és el client de la subvenció.</span><span class="sxs-lookup"><span data-stu-id="b0c2b-145">In this case, the federal government is the grantor agency, and the state is the grant customer.</span></span>

> [!NOTE] 
> <span data-ttu-id="b0c2b-146">Quan inicieu per primera vegada la funció, els números inicials de CFDA s'introduiran utilitzant els números existents en les subvencions.</span><span class="sxs-lookup"><span data-stu-id="b0c2b-146">When you first turn on the feature, initial CFDA numbers will be entered by using the existing numbers on grants.</span></span>

## <a name="exclude-grants-from-sefa-reporting-based-on-the-grant-type"></a><span data-ttu-id="b0c2b-147">Excloure subvencions de l'informe de SEFA en funció del tipus de subvenció</span><span class="sxs-lookup"><span data-stu-id="b0c2b-147">Exclude grants from SEFA reporting based on the grant type</span></span>

1. <span data-ttu-id="b0c2b-148">Aneu a **Administració de projectes i comptabilitat \> Configuració \> Subvencions \> Tipus de subvenció**.</span><span class="sxs-lookup"><span data-stu-id="b0c2b-148">Go to **Project management and accounting \> Setup \> Grants \> Grant types**.</span></span>
2. <span data-ttu-id="b0c2b-149">Al FastTab **Informació per defecte** , marqueu la casella de selecció **Exclou de la Planificació de despeses de concessions federals**.</span><span class="sxs-lookup"><span data-stu-id="b0c2b-149">On the **Default information** FastTab, select the **Exclude from Schedule of Expenditures of Federal Awards** check box.</span></span>
3. <span data-ttu-id="b0c2b-150">Seleccioneu **Desa**  per desar els canvis.</span><span class="sxs-lookup"><span data-stu-id="b0c2b-150">Select **Save** to save your changes.</span></span>

## <a name="run-the-schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="b0c2b-151">Executar la consulta de la Planificació de despeses per a concessions federals</span><span class="sxs-lookup"><span data-stu-id="b0c2b-151">Run the Schedule of Expenditures of Federal Awards inquiry</span></span>

1. <span data-ttu-id="b0c2b-152">Aneu a **Administració de projectes i comptabilitat \> Consultes i informes \> Consulta de subvenció \> Planificació de despeses de concessions federals**.</span><span class="sxs-lookup"><span data-stu-id="b0c2b-152">Go to **Project management and accounting \> Inquiries and reports \> Grant inquiry \> Schedule of Expenditures of Federal Awards**.</span></span>
2. <span data-ttu-id="b0c2b-153">A la secció **Paràmetres** , seguiu aquests passos:</span><span class="sxs-lookup"><span data-stu-id="b0c2b-153">In the **Parameters** section, follow these steps:</span></span>

    1. <span data-ttu-id="b0c2b-154">En el camp **Interval de dates** , seleccioneu el codi per a l'interval de dates.</span><span class="sxs-lookup"><span data-stu-id="b0c2b-154">In the **Date interval** field, select the code for the date interval.</span></span> <span data-ttu-id="b0c2b-155">Alternativament, en els camps **Data d'inici** i **Data de finalització** , definiu l'interval de dates.</span><span class="sxs-lookup"><span data-stu-id="b0c2b-155">Alternatively, in the **From date** and **To date** fields, define the date interval.</span></span>
    2. <span data-ttu-id="b0c2b-156">Opcional: per incloure només les transaccions facturades com a ingressos en la consulta, establiu l'opció **Inclou només els ingressos facturats** a **Sí**.</span><span class="sxs-lookup"><span data-stu-id="b0c2b-156">Optional: To include only billed transactions as revenue in the inquiry, set the **Include only billed revenues** option to **Yes**.</span></span>

## <a name="columns"></a><span data-ttu-id="b0c2b-157">Columnes</span><span class="sxs-lookup"><span data-stu-id="b0c2b-157">Columns</span></span>

<span data-ttu-id="b0c2b-158">La consulta de la Planificació de despeses de concessions federals inclou les següents columnes:</span><span class="sxs-lookup"><span data-stu-id="b0c2b-158">The Schedule of Expenditures of Federal Awards inquiry includes the following columns:</span></span>

- <span data-ttu-id="b0c2b-159">Nom del grup del Catàleg d'assistència nacional federal</span><span class="sxs-lookup"><span data-stu-id="b0c2b-159">Catalog of Federal Domestic Assistance cluster name</span></span>
- <span data-ttu-id="b0c2b-160">Agència que proporciona la subvenció</span><span class="sxs-lookup"><span data-stu-id="b0c2b-160">Grantor agency</span></span>
- <span data-ttu-id="b0c2b-161">Agència de traspàs</span><span class="sxs-lookup"><span data-stu-id="b0c2b-161">Pass-through agency</span></span>
- <span data-ttu-id="b0c2b-162">Nom de la subvenció</span><span class="sxs-lookup"><span data-stu-id="b0c2b-162">Grant name</span></span>
- <span data-ttu-id="b0c2b-163">ID de subvenció</span><span class="sxs-lookup"><span data-stu-id="b0c2b-163">Grant ID</span></span>
- <span data-ttu-id="b0c2b-164">ID de sol·licitud de la subvenció</span><span class="sxs-lookup"><span data-stu-id="b0c2b-164">Grant application ID</span></span>
- <span data-ttu-id="b0c2b-165">Catàleg d'assistència nacional federal</span><span class="sxs-lookup"><span data-stu-id="b0c2b-165">Catalog of Federal Domestic Assistance</span></span>
- <span data-ttu-id="b0c2b-166">Rebuts</span><span class="sxs-lookup"><span data-stu-id="b0c2b-166">Receipts</span></span>
- <span data-ttu-id="b0c2b-167">Despeses</span><span class="sxs-lookup"><span data-stu-id="b0c2b-167">Expenditures</span></span>
