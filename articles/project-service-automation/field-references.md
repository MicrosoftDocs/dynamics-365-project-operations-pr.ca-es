---
title: Afegir camps personalitzats a la configuració de preus i a entitats transaccionals
description: En aquest tema es proporciona informació sobre com afegir camps personalitzats a la configuració de preus i a entitats transaccionals.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/26/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 1d6e996b-dcf2-473f-b642-edd33d8d6d4e
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 95cea2c5d499335c24d31b725ed68901808ee084
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749424"
---
# <a name="add-custom-fields-to-price-setup-and-transactional-entities"></a><span data-ttu-id="9a4fe-103">Afegir camps personalitzats a la configuració de preus i a entitats transaccionals</span><span class="sxs-lookup"><span data-stu-id="9a4fe-103">Add custom fields to price setup and transactional entities</span></span> 
<span data-ttu-id="9a4fe-104">En aquest tema s'assumeix que heu completat els procediments en el tema [Crear camps i entitats personalitzats](create-custom-fields-entities.md).</span><span class="sxs-lookup"><span data-stu-id="9a4fe-104">This topic assumes that you have completed the procedures in the topic, [Create custom fields and entities](create-custom-fields-entities.md).</span></span> <span data-ttu-id="9a4fe-105">Si no heu completat aquests procediments, aneu enrere per completar-los torneu a aquest tema.</span><span class="sxs-lookup"><span data-stu-id="9a4fe-105">If you haven't completed those procedures, go back and complete them and then return to this topic.</span></span> 

<span data-ttu-id="9a4fe-106">En aquest tema, els procediments us mostraran com afegir les referències de camp personalitzades necessàries a les entitats i als elements de la interfície d'usuari (IU), com ara formularis i visualitzacions.</span><span class="sxs-lookup"><span data-stu-id="9a4fe-106">In this topic, the procedures will show you how to add the required custom field references to entities and to the user interface (UI) elements such as forms and views.</span></span>

## <a name="add-custom-pricing-dimension-fields"></a><span data-ttu-id="9a4fe-107">Afegeix camps de dimensió de preus personalitzats</span><span class="sxs-lookup"><span data-stu-id="9a4fe-107">Add custom pricing dimension fields</span></span> 
<span data-ttu-id="9a4fe-108">Quan s'han creat camps i entitats personalitzats, el pas següent és fer que les entitats de configuració de preus i transaccionals reconeguin qualsevol entitat o conjunt d'opcions personalitzades creant camps de referència.</span><span class="sxs-lookup"><span data-stu-id="9a4fe-108">After custom fields and entities have been created, the next step is to make price setup and transactional entities aware of any custom entities or option sets by creating reference fields.</span></span> <span data-ttu-id="9a4fe-109">En funció de si la llista de dimensions de preus de preus inclou dimensions o dimensions de l'entitat de conjunt d'opcions o ambdues, seguiu només els passos a **Dimensions de preus personalitzades basades en el conjunt d'opcions** o **Dimensions de preus personalitzades basades en l'entitat**, o ambdues, respectivament.</span><span class="sxs-lookup"><span data-stu-id="9a4fe-109">Depending on whether your pricing dimensions list includes option set dimensions or entity dimensions or both, follow only the steps in **Option set-based custom pricing dimensions** or **Entity-based custom pricing dimensions**, or both, respectively.</span></span>

### <a name="option-set-based-custom-pricing-dimensions"></a><span data-ttu-id="9a4fe-110">Dimensions de preus personalitzades basades en conjunts d'opcions</span><span class="sxs-lookup"><span data-stu-id="9a4fe-110">Option set-based custom pricing dimensions</span></span>
<span data-ttu-id="9a4fe-111">Quan una dimensió de preus personalitzada està basada en un conjunt d'opcions, afegiu-la com a camp a entitats clau del Project Service.</span><span class="sxs-lookup"><span data-stu-id="9a4fe-111">When a custom pricing dimension is option set-based, add it as a field to key Project Service entities.</span></span> <span data-ttu-id="9a4fe-112">En el procediment següent, s'utilitzen **Ubicació de treball del recurs** i **Hores de treball del recurs** com a dimensions de preu basades en un conjunt d'opcions.</span><span class="sxs-lookup"><span data-stu-id="9a4fe-112">In the following procedure, **Resource Work Location** and **Resource Work Hours** are used as the option set-based pricing dimensions.</span></span> <span data-ttu-id="9a4fe-113">Primer s'han d'afegir com a camps a les entitats de preus, **Preu per funció** i **Marge comercial del preu per funció**.</span><span class="sxs-lookup"><span data-stu-id="9a4fe-113">These must first be added as fields to the pricing entities, **Role Price** and **Role Price Markup**.</span></span>

1. <span data-ttu-id="9a4fe-114">Al Project Service Automation (PSA), feu clic a **Configuració** > **Solucions** i, a continuació, feu doble clic a **Dimensions de preus de \<nom de l'organització>**.</span><span class="sxs-lookup"><span data-stu-id="9a4fe-114">In Project Service Automation (PSA), click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="9a4fe-115">A l'Explorador de solucions, a la subfinestra de navegació esquerra, seleccioneu **Entitats > Preu per funció**.</span><span class="sxs-lookup"><span data-stu-id="9a4fe-115">In Solution Explorer, on the left navigation pane, select **Entities > Role Price**.</span></span>
3. <span data-ttu-id="9a4fe-116">Expandiu l'entitat **Preu per funció** i seleccioneu **Camps**.</span><span class="sxs-lookup"><span data-stu-id="9a4fe-116">Expand the entity **Role Price** and select **Fields**.</span></span>
4. <span data-ttu-id="9a4fe-117">Feu clic a **Nou** per crear un camp nou anomenat **Ubicació de treball del recurs** i seleccioneu **Conjunt d'opcions** com a tipus de camp.</span><span class="sxs-lookup"><span data-stu-id="9a4fe-117">Click **New** to create a new field called **Resource Work Location** and select **Option set** as the field type.</span></span> 
5. <span data-ttu-id="9a4fe-118">Seleccioneu **Utilitza una conjunt d'opcions existent**, seleccioneu el conjunt d'opcions **Ubicació de treball del recurs** i, a continuació, feu clic a **Desa**.</span><span class="sxs-lookup"><span data-stu-id="9a4fe-118">Select **Use an existing Option set**, select the **Resource Work Location** option set, and then click **Save**.</span></span>
6. <span data-ttu-id="9a4fe-119">Repetiu els passos 1-5 per afegir aquest camp a l'entitat **Marge comercial del preu per funció**.</span><span class="sxs-lookup"><span data-stu-id="9a4fe-119">Repeat steps 1 - 5 to add this field to the **Role Price Markup** entity.</span></span> 
7. <span data-ttu-id="9a4fe-120">Repetiu els passos 1-5 per al conjunt d'opcions **Hores de treball del recurs**.</span><span class="sxs-lookup"><span data-stu-id="9a4fe-120">Repeat steps 1 - 5 for the **Resource Work Hours** option set.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9a4fe-121">Quan afegiu un camp a més d'una entitat, utilitzeu el mateix nom de camp a totes les entitats.</span><span class="sxs-lookup"><span data-stu-id="9a4fe-121">When you add a field to more than one entity, use the same field name across all of the entities.</span></span> 

> ![Afegir Ubicació de treball del recurs al preu per funció](media/RWL-Field.png)

<span data-ttu-id="9a4fe-123">En les fases de vendes i estimació d'un projecte, les estimacions de l'esforç de treball necessari per completar treball **Local** i **In situ** a **Hores normals** i **Hores extres** s'utilitzen per calcular el valor de l'oferta o el projecte.</span><span class="sxs-lookup"><span data-stu-id="9a4fe-123">In the sales and estimation phases for a project, estimates of the work effort that is required to complete **Local** and **Onsite** work, in **Regular hours** and **Overtime hours**  are used to estimate the value of the Quote/Project.</span></span> <span data-ttu-id="9a4fe-124">S'afegiran els camps **Ubicació de treball del recurs** i **Hores de treball del recurs** a les entitats d'estimació, **Detall de la línia d'oferta**, **Detall de la línia de contracte**, **Membre de l'equip del projecte** i **Línia d'estimació**.</span><span class="sxs-lookup"><span data-stu-id="9a4fe-124">The fields **Resource Work Location** and **Resource Work Hours** will be added to the estimation entities, **Quote Line Detail**, **Contract Line detail**, **Project Team Member**, and **Estimate Line**.</span></span>

1. <span data-ttu-id="9a4fe-125">Al PSA, feu clic a **Configuració** > **Solucions** i, a continuació, feu doble clic a **Dimensions de preus de \<nom de l'organització>**.</span><span class="sxs-lookup"><span data-stu-id="9a4fe-125">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="9a4fe-126">A l'Explorador de solucions, a la subfinestra de navegació esquerra, seleccioneu **Entitats > Detall de la línia d'oferta**.</span><span class="sxs-lookup"><span data-stu-id="9a4fe-126">In Solution Explorer, on the left navigation pane, select **Entities > Quote Line Detail**.</span></span>
3. <span data-ttu-id="9a4fe-127">Expandiu l'entitat **Detall de la línia d'oferta** i seleccioneu **Camps**.</span><span class="sxs-lookup"><span data-stu-id="9a4fe-127">Expand the **Quote Line Detail** entity, and select **Fields**.</span></span>
4. <span data-ttu-id="9a4fe-128">Feu clic a **Nou** per crear un camp nou anomenat **Ubicació de treball del recurs** i seleccioneu el tipus de camp **Conjunt d'opcions**.</span><span class="sxs-lookup"><span data-stu-id="9a4fe-128">Click **New** to create a new field called **Resource Work Location** and select the field type, **Option set**.</span></span> 
5. <span data-ttu-id="9a4fe-129">Seleccioneu **Utilitza una conjunt d'opcions existent** i **Ubicació de treball del recurs** i, a continuació, feu clic a **Desa**.</span><span class="sxs-lookup"><span data-stu-id="9a4fe-129">Select **Use an existing Option set** and **Resource Work Location**, and then click **Save**.</span></span>
6. <span data-ttu-id="9a4fe-130">Repetiu els passos 1-5 per afegir aquest camp a les entitats **Detall de la línia de contracte del projecte**, **Membre de l'equip del projecte** i **Línia d'estimació**.</span><span class="sxs-lookup"><span data-stu-id="9a4fe-130">Repeat steps 1 - 5 to add this field to the **Project Contract line detail**, **Project Team Member**, and **Estimate Line** entities.</span></span>
7. <span data-ttu-id="9a4fe-131">Repetiu els passos 1-6 per al conjunt d'opcions **Hores de treball del recurs**.</span><span class="sxs-lookup"><span data-stu-id="9a4fe-131">Repeat steps 1 - 6 for the **Resource Work Hours** option set.</span></span> 

> ![Afegir Ubicació de treball del recurs a Línia d'estimació](media/RWL-Default-Value.png)


<span data-ttu-id="9a4fe-133">Per al lliurament i la facturació, el treball completat ha de tenir un preu precís per seleccionar si s'ha realitzat **Local** o **In situ**, i si es va completar durant **Hores normals** o **Hores extres** a Valors reals del projecte.</span><span class="sxs-lookup"><span data-stu-id="9a4fe-133">For delivery and invoicing, completed work needs to be accurately priced to select whether it was performed **Local** or **Onsite**, and whether it was completed during **Regular hours** or **Overtime** on the Project Actuals.</span></span> <span data-ttu-id="9a4fe-134">S'han d'afegir els camps **Ubicació de treball del recurs** i **Hores de treball del recurs** a les entitats **Entrada de temps**, **Valor real**, **Detall de la línia de factura** i **Línia del llibre diari**.</span><span class="sxs-lookup"><span data-stu-id="9a4fe-134">The **Resource Work Location** and **Resource Work hours** fields should be added to the **Time Entry**, **Actual**, **Invoice Line Detail**, and **Journal Line** entities.</span></span>

1. <span data-ttu-id="9a4fe-135">Al PSA, feu clic a **Configuració** > **Solucions** i, a continuació, feu doble clic a **Dimensions de preus de \<nom de l'organització>**.</span><span class="sxs-lookup"><span data-stu-id="9a4fe-135">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="9a4fe-136">A l'Explorador de solucions, a la subfinestra de navegació esquerra, seleccioneu **Entitats > Entrada de temps**.</span><span class="sxs-lookup"><span data-stu-id="9a4fe-136">In Solution Explorer, on the left navigation pane, select  **Entities > Time Entry**.</span></span>
3. <span data-ttu-id="9a4fe-137">Expandiu l'entitat **Detall de la línia d'oferta** i, a continuació, seleccioneu **Camps**.</span><span class="sxs-lookup"><span data-stu-id="9a4fe-137">Expand the **Quote Line Detail** entity, and then select **Fields**.</span></span>
4. <span data-ttu-id="9a4fe-138">Feu clic a **Nou** per crear un camp nou anomenat **Ubicació de treball del recurs** i seleccioneu **Conjunt d'opcions** com a tipus de camp.</span><span class="sxs-lookup"><span data-stu-id="9a4fe-138">Click **New** to create a new field called **Resource Work Location** and select **Option set** as the field type.</span></span> 
5. <span data-ttu-id="9a4fe-139">Seleccioneu **Utilitza una conjunt d'opcions existent**, seleccioneu el conjunt d'opcions **Ubicació de treball del recurs** i, a continuació, feu clic a **Desa**.</span><span class="sxs-lookup"><span data-stu-id="9a4fe-139">Select **Use an existing Option set**, select the **Resource Work Location** option set, and then click **Save**.</span></span>
6. <span data-ttu-id="9a4fe-140">Repetiu els passos 1-5 per afegir aquest camp a les entitats **Valor real**, **Detall de la línia de factura** i **Línia del llibre diari**.</span><span class="sxs-lookup"><span data-stu-id="9a4fe-140">Repeat steps 1 - 5 to add this field to the **Actual**, **Invoice Line Detail**, and **Journal Line** entities.</span></span>
7. <span data-ttu-id="9a4fe-141">Repetiu els passos 1-6 per al conjunt d'opcions **Hores de treball del recurs**.</span><span class="sxs-lookup"><span data-stu-id="9a4fe-141">Repeat steps 1 - 6 for the **Resource Work Hours** option set.</span></span> 

> ![Afegir Ubicació de treball del recurs a una entrada de temps](media/RWL-time-entry.png)

<span data-ttu-id="9a4fe-143">Això completa els canvis d'esquema necessaris per a les dimensions personalitzades basades en conjunts d'opcions.</span><span class="sxs-lookup"><span data-stu-id="9a4fe-143">This completes the schema changes required for option set-based custom dimensions.</span></span>

## <a name="entity-based-custom-pricing-dimensions"></a><span data-ttu-id="9a4fe-144">Dimensions de preus personalitzades basades en entitats</span><span class="sxs-lookup"><span data-stu-id="9a4fe-144">Entity-based custom pricing dimensions</span></span>

<span data-ttu-id="9a4fe-145">Quan la dimensió de preus personalitzada és una entitat, hi afegireu relacions 1:N entre l'entitat de la dimensió i les entitats clau del Project Service.</span><span class="sxs-lookup"><span data-stu-id="9a4fe-145">When the custom pricing dimension is an entity, you will add 1:N relationships between the dimension entity and key Project Service entities.</span></span> <span data-ttu-id="9a4fe-146">Utilitzant de l'exemple de càrrec estàndard anterior, és raonable esperar que cada empleat tingui assignat un càrrec estàndard.</span><span class="sxs-lookup"><span data-stu-id="9a4fe-146">Using the Standard Title example from above, it is reasonable to expect that each employee is assigned a standard title.</span></span> <span data-ttu-id="9a4fe-147">Per tant, necessitareu una relació 1:N de Càrrec estàndard a Recurs que es pot reservar o una relació N:1 si s'ha creat des de Recurs que es pot reservar a Càrrec estàndard.</span><span class="sxs-lookup"><span data-stu-id="9a4fe-147">SAs a result, you will need a 1:N relationship from Standard Title to Bookable Resource, or a N:1 relationship if it were created from Bookable Resource to Standard Title.</span></span>

1. <span data-ttu-id="9a4fe-148">Al PSA, feu clic a **Configuració** > **Solucions** i, a continuació, feu doble clic a **Dimensions de preus de \<nom de l'organització>**.</span><span class="sxs-lookup"><span data-stu-id="9a4fe-148">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="9a4fe-149">A l'Explorador de solucions, a la subfinestra de navegació esquerra, seleccioneu **Entitats > Càrrec estàndard**.</span><span class="sxs-lookup"><span data-stu-id="9a4fe-149">In Solution Explorer, on the left navigation pane, select **Entities > Standard Title**.</span></span>
3. <span data-ttu-id="9a4fe-150">Expandiu l'entitat **Càrrec estàndard** i seleccioneu **Relacions 1:N**.</span><span class="sxs-lookup"><span data-stu-id="9a4fe-150">Expand the **Standard Title** entity and select **1:N Relationships**.</span></span>
4. <span data-ttu-id="9a4fe-151">Feu clic a **Nou** per crear una relació 1:N nova anomenada **Càrrec estàndard a Recurs que es pot reservar**.</span><span class="sxs-lookup"><span data-stu-id="9a4fe-151">Click **New** to create a new 1:N relationship called **Standard Title to Bookable Resource**.</span></span> <span data-ttu-id="9a4fe-152">Introduïu la informació requerida i feu clic a **Desa**.</span><span class="sxs-lookup"><span data-stu-id="9a4fe-152">Enter the required information, and then click **Save**.</span></span>

> ![Afegir Càrrec estàndard com a camp de referència a Recurs que es pot reservar](media/ST-BR.png)

<span data-ttu-id="9a4fe-154">El Càrrec estàndard també s'haurà d'afegir a les entitats de preus del Project Service, **Preu per funció** i **Marge comercial del preu per funció**.</span><span class="sxs-lookup"><span data-stu-id="9a4fe-154">The Standard Title will also need to be added to Project Service Pricing entities, **Role Price** and **Role Price Markup**.</span></span> <span data-ttu-id="9a4fe-155">Això també es completa utilitzant relacions 1:N entre les entitats **Càrrec estàndard** i **Preu per funció** i les entitats **Càrrec estàndard** i **Preu per funció**.</span><span class="sxs-lookup"><span data-stu-id="9a4fe-155">This is also completed using 1:N relationships between the **Standard Title** and **Role Price** entities and **Standard Title** and **Role Price Markup** entities.</span></span>

1. <span data-ttu-id="9a4fe-156">A l'Explorador de solucions, a la subfinestra de navegació esquerra, seleccioneu **Entitats > Càrrec estàndard**.</span><span class="sxs-lookup"><span data-stu-id="9a4fe-156">In Solution Explorer, on the left navigation pane, select **Entities > Standard Title**.</span></span>
2. <span data-ttu-id="9a4fe-157">Expandiu l'entitat **Càrrec estàndard** i seleccioneu **Relacions 1:N**.</span><span class="sxs-lookup"><span data-stu-id="9a4fe-157">Expand the **Standard Title** entity and select **1:N Relationships**.</span></span>
3. <span data-ttu-id="9a4fe-158">Feu clic a **Nou** per crear una relació 1:N nova anomenada **Càrrec estàndard a Preu per funció**.</span><span class="sxs-lookup"><span data-stu-id="9a4fe-158">Click **New** to create a new 1:N relationship called **Standard Title to Role Price**.</span></span> <span data-ttu-id="9a4fe-159">Introduïu la informació requerida i feu clic a **Desa**.</span><span class="sxs-lookup"><span data-stu-id="9a4fe-159">Enter the required information, and then click **Save**.</span></span>
4. <span data-ttu-id="9a4fe-160">Repetiu els passos 1-4 per crear relacions 1:N entre les entitats **Càrrec estàndard** i **Marge comercial del preu per funció**.</span><span class="sxs-lookup"><span data-stu-id="9a4fe-160">Repeat steps 1 - 4 to create 1:N relationships between the **Standard Title** and **Role Price Markup** entities,</span></span>

<span data-ttu-id="9a4fe-161">En les fases de vendes i estimació per al projecte, per posar un preu a l'oferta/projecte, les estimacions de l'esforç de treball són necessàries per a cada càrrec estàndard.</span><span class="sxs-lookup"><span data-stu-id="9a4fe-161">In the sales and estimation phases for the project, to price the Quote/Project, estimates of the work effort are required for each standard title.</span></span> <span data-ttu-id="9a4fe-162">Això significa que les relacions 1:N des de Càrrec estàndard a cadascuna d'aquestes entitats d'estimació del Project Service són necessàries:</span><span class="sxs-lookup"><span data-stu-id="9a4fe-162">This means that 1:N relationships from Standard Title to each of these estimation entities in Project Service are needed:</span></span> 

- <span data-ttu-id="9a4fe-163">**Detall de la línia d'oferta**</span><span class="sxs-lookup"><span data-stu-id="9a4fe-163">**Quote line Detail**</span></span>
- <span data-ttu-id="9a4fe-164">**Detall de la línia de contracte del projecte**</span><span class="sxs-lookup"><span data-stu-id="9a4fe-164">**Project Contract Line Detail**</span></span>
- <span data-ttu-id="9a4fe-165">**Membre de l'equip del projecte**</span><span class="sxs-lookup"><span data-stu-id="9a4fe-165">**Project Team Member**</span></span>
- <span data-ttu-id="9a4fe-166">**Línia d'estimació**</span><span class="sxs-lookup"><span data-stu-id="9a4fe-166">**Estimate Line**</span></span>

5. <span data-ttu-id="9a4fe-167">Repetiu els passos 1-5 per crear relacions 1:N des de **Càrrec estàndard** a **Detall de la línia d'oferta**, **Detall de la línia de contracte del projecte**, **Membre de l'equip del projecte** i **Línia d'estimació**.</span><span class="sxs-lookup"><span data-stu-id="9a4fe-167">Repeat steps 1 - 5 to create 1:N relationships from **Standard Title** to **Quote line Detail**, **Project Contract Line Detail**, **Project Team Member**, and **Estimate Line**.</span></span>

> ![Afegir Càrrec estàndard com a camp de referència a Línia d'estimació](media/ST-Estimate-Line.png)

<span data-ttu-id="9a4fe-169">En les fases de lliurament i de facturació, els treballs completats per cada càrrec estàndard han de tenir un preu precís a Valors reals del projecte.</span><span class="sxs-lookup"><span data-stu-id="9a4fe-169">In the Delivery and Invoicing phases, the work completed by each standard title must be accurately priced on the Project Actuals.</span></span> <span data-ttu-id="9a4fe-170">Això vol dir que hi ha d'haver relacions 1:N des de **Càrrec estàndard** a les entitats **Entrada de temps**, **Valor real**, **Detall de la línia de factura** i **Línia del llibre diari**.</span><span class="sxs-lookup"><span data-stu-id="9a4fe-170">This means that there needs to be 1:N relationships from **Standard Title** to **Time Entry**, **Actual**, **Invoice Line Detail**, and **Journal Line entities**.</span></span>

6. <span data-ttu-id="9a4fe-171">Repetiu els passos 1-6 per crear relacions 1:N des de **Càrrec estàndard** a les entitats **Entrada de temps**, **Valor real**, **Detall de la línia de factura** i **Línia del llibre diari**.</span><span class="sxs-lookup"><span data-stu-id="9a4fe-171">Repeat steps 1 - 6 to create 1:N relationships from **Standard Title** to **Time Entry**, **Actual**, **Invoice Line Detail**, and **Journal Line entities**.</span></span>

> ![Afegir Càrrec estàndard com a camp de referència a Entrada de temps](media/ST-Mapping.png)

### <a name="set-up-dimension-value-defaulting-using-the-mappings-features-of-the-platform"></a><span data-ttu-id="9a4fe-173">Configurar el valor de la dimensió per defecte amb les característiques d'assignacions de la plataforma</span><span class="sxs-lookup"><span data-stu-id="9a4fe-173">Set up Dimension value defaulting using the mappings features of the platform</span></span>
<span data-ttu-id="9a4fe-174">Per a l'entrada de temps, seria útil tenir el valor per defecte del sistema a l'entrada de temps del recurs disponible que està registrant l'entrada de temps.</span><span class="sxs-lookup"><span data-stu-id="9a4fe-174">For Time Entry, it would be helpful to have the system default the standard title on the Time Entry from the Bookable Resource that is recording the time entry.</span></span> <span data-ttu-id="9a4fe-175">Seguiu aquests passos per afegir assignacions de camp a la relació 1:N des de **Recurs que es pot reservar** a **Entrada de temps**.</span><span class="sxs-lookup"><span data-stu-id="9a4fe-175">Use the following steps to add field mappings on the 1:N relationship from **Bookable Resource** to **Time Entry**.</span></span>

1. <span data-ttu-id="9a4fe-176">A l'Explorador de solucions, a la subfinestra de navegació esquerra, seleccioneu **Entitats > Càrrec estàndard**.</span><span class="sxs-lookup"><span data-stu-id="9a4fe-176">In Solution Explorer, on the left navigation pane, select **Entities > Standard Title**.</span></span>
2. <span data-ttu-id="9a4fe-177">Expandiu l'entitat **Càrrec estàndard** i seleccioneu **Relacions 1:N**.</span><span class="sxs-lookup"><span data-stu-id="9a4fe-177">Expand the **Standard Title** entity and select **1:N Relationships**.</span></span>
3. <span data-ttu-id="9a4fe-178">Feu doble clic a **Recurs que es pot reservar a Entrada de temps**.</span><span class="sxs-lookup"><span data-stu-id="9a4fe-178">Double-click **Bookable Resource to Time Entry**.</span></span> <span data-ttu-id="9a4fe-179">A la pàgina **Relació**, feu clic a **Utilitza assignacions de camps**.</span><span class="sxs-lookup"><span data-stu-id="9a4fe-179">On the **Relationship** page, click **Use Field mappings**.</span></span> 
4. <span data-ttu-id="9a4fe-180">Feu clic a **Nou** per crear una assignació de camp nova entre el camp **Càrrec estàndard** a l'entitat **Recurs que es pot reservar** al camp de referència **Càrrec estàndard** a l'entitat **Entrada de temps**.</span><span class="sxs-lookup"><span data-stu-id="9a4fe-180">Click **New** to create a new field mapping between the **Standard Title** field on the **Bookable Resource** entity to the **Standard Title** reference field on **Time Entry** entity.</span></span> 

> ![Configurar les assignacions de camps per permetre l'assignació per defecte de Càrrec estàndard de Recurs disponible a Entrada de temps](media/ST-Mapping2.png)


<span data-ttu-id="9a4fe-182">Això completa els canvis d'esquema necessaris per a les dimensions personalitzades basades en entitats.</span><span class="sxs-lookup"><span data-stu-id="9a4fe-182">This completes the schema changes required for entity-based custom dimensions.</span></span>

##  <a name="add-custom-fields-to-forms-views-and-business-rules"></a><span data-ttu-id="9a4fe-183">Afegir camps personalitzats a formularis, visualitzacions i regles de negocis.</span><span class="sxs-lookup"><span data-stu-id="9a4fe-183">Add custom fields to forms, views, and business rules</span></span>

<span data-ttu-id="9a4fe-184">Després d'haver fet tots els canvis d'esquema necessaris, el pas següent és fer que els camps siguin visibles a la interfície d'usuari afegint els camps als formularis i a les visualitzacions.</span><span class="sxs-lookup"><span data-stu-id="9a4fe-184">After you have made all of the required schema changes, the next step is to make the fields visible in the UI by adding the fields to the forms and views.</span></span>

1. <span data-ttu-id="9a4fe-185">Obriu el formulari o la visualització.</span><span class="sxs-lookup"><span data-stu-id="9a4fe-185">Open the form or the view.</span></span> <span data-ttu-id="9a4fe-186">A la subfinestra de navegació dreta, seleccioneu el camp i arrossegueu-lo al llenç del formulari.</span><span class="sxs-lookup"><span data-stu-id="9a4fe-186">On the right navigation pane, select the field and drag it on to the form canvas.</span></span> 
2. <span data-ttu-id="9a4fe-187">Si esteu editant una visualització, utilitzeu la subfinestra de navegació dreta, feu clic a **Afegeix camps** i, al quadre de diàleg **Llista de camps**, seleccioneu els camps que necessiteu i feu clic a **D'acord**.</span><span class="sxs-lookup"><span data-stu-id="9a4fe-187">If you are editing a view, use the right navigation pane, click **Add fields**, and in the **Field listing** dialog box, select the fields that you need and click **Ok**.</span></span>

<span data-ttu-id="9a4fe-188">La taula següent proporciona una llista exhaustiva dels formularis i les visualitzacions de fàbrica, llistats per entitat, que s'han d'actualitzar amb els nous camps.</span><span class="sxs-lookup"><span data-stu-id="9a4fe-188">The following table provides a comprehensive list of out-of-the-box forms and views, by entity, that will need to be updated with the new fields.</span></span> <span data-ttu-id="9a4fe-189">Si teniu visualitzacions o formularis addicionals a les personalitzacions d'aquestes entitats, afegiu també els camps nous.</span><span class="sxs-lookup"><span data-stu-id="9a4fe-189">If you have any additional views or forms in your customizations on these entities, add the new fields to those as well.</span></span>

| <span data-ttu-id="9a4fe-190">Entitat del Project Service</span><span class="sxs-lookup"><span data-stu-id="9a4fe-190">Project Service Entity</span></span>        | <span data-ttu-id="9a4fe-191">Formularis que necessiten el nou camp</span><span class="sxs-lookup"><span data-stu-id="9a4fe-191">Forms that need the new field</span></span>   |<span data-ttu-id="9a4fe-192">Visualitzacions que necessiten el nou camp</span><span class="sxs-lookup"><span data-stu-id="9a4fe-192">Views that need the new field</span></span>      |
| ------------------------------|---------------------------------|----------------------------------|
|  <span data-ttu-id="9a4fe-193">Preu per funció</span><span class="sxs-lookup"><span data-stu-id="9a4fe-193">Role Price</span></span>|<span data-ttu-id="9a4fe-194">• Informació</span><span class="sxs-lookup"><span data-stu-id="9a4fe-194">• Information</span></span> |<span data-ttu-id="9a4fe-195">• Preus de categories de recursos actius</span><span class="sxs-lookup"><span data-stu-id="9a4fe-195">• Active Resource Category Prices</span></span><br> <span data-ttu-id="9a4fe-196">• Visualització associada de preus de categories de recursos</span><span class="sxs-lookup"><span data-stu-id="9a4fe-196">• Resource Category Price Associated View</span></span>|
|  <span data-ttu-id="9a4fe-197">Marge comercial de preu de funció</span><span class="sxs-lookup"><span data-stu-id="9a4fe-197">Role Price Markup</span></span>|<span data-ttu-id="9a4fe-198">• Informació</span><span class="sxs-lookup"><span data-stu-id="9a4fe-198">• Information</span></span>|<span data-ttu-id="9a4fe-199">• Marge comercial de preu de funcions actives</span><span class="sxs-lookup"><span data-stu-id="9a4fe-199">• Active Role Price Markup</span></span><br><span data-ttu-id="9a4fe-200">• Visualització associada de marge comercial de preus de la funció</span><span class="sxs-lookup"><span data-stu-id="9a4fe-200">• Role Price Markup Associated View</span></span>|
|  <span data-ttu-id="9a4fe-201">Detall de la línia d'oferta</span><span class="sxs-lookup"><span data-stu-id="9a4fe-201">Quote line detail</span></span>|<span data-ttu-id="9a4fe-202">• Informació del projecte</span><span class="sxs-lookup"><span data-stu-id="9a4fe-202">• Project Information</span></span><br><span data-ttu-id="9a4fe-203">• Creació ràpida de projectes</span><span class="sxs-lookup"><span data-stu-id="9a4fe-203">• Project Quick Create</span></span>|<span data-ttu-id="9a4fe-204">• Detall de la línia d'oferta activa</span><span class="sxs-lookup"><span data-stu-id="9a4fe-204">• Active Quote Line Detail</span></span><br><span data-ttu-id="9a4fe-205">• Detalls de la línia d'oferta combinada</span><span class="sxs-lookup"><span data-stu-id="9a4fe-205">• Combined Quote Line Details</span></span><br><span data-ttu-id="9a4fe-206">• Visualització associada de detall de la línia d'oferta</span><span class="sxs-lookup"><span data-stu-id="9a4fe-206">• Quote Line Detail associated view</span></span>|
|  <span data-ttu-id="9a4fe-207">Detall de la línia de contracte del projecte</span><span class="sxs-lookup"><span data-stu-id="9a4fe-207">Project Contract line detail</span></span>|<span data-ttu-id="9a4fe-208">• Informació del projecte</span><span class="sxs-lookup"><span data-stu-id="9a4fe-208">• Project Information</span></span><br><span data-ttu-id="9a4fe-209">• Creació ràpida de projectes</span><span class="sxs-lookup"><span data-stu-id="9a4fe-209">• Project Quick Create</span></span>|<span data-ttu-id="9a4fe-210">• Detalls de la línia de contracte combinada</span><span class="sxs-lookup"><span data-stu-id="9a4fe-210">• Combined Contract Line Details</span></span><br><span data-ttu-id="9a4fe-211">• Detalls de la línia de contracte activa</span><span class="sxs-lookup"><span data-stu-id="9a4fe-211">• Active Contract Line Details</span></span><br><span data-ttu-id="9a4fe-212">• Visualització associada de detalls de la línia de contracte</span><span class="sxs-lookup"><span data-stu-id="9a4fe-212">• Contract Line Details Associated View</span></span>|
|  <span data-ttu-id="9a4fe-213">Membre de l'equip del projecte</span><span class="sxs-lookup"><span data-stu-id="9a4fe-213">Project Team Member</span></span>|<span data-ttu-id="9a4fe-214">• Informació</span><span class="sxs-lookup"><span data-stu-id="9a4fe-214">• Information</span></span><br><span data-ttu-id="9a4fe-215">• Formulari nou</span><span class="sxs-lookup"><span data-stu-id="9a4fe-215">• New Form</span></span>|<span data-ttu-id="9a4fe-216">• Membres de l'equip del projecte actius</span><span class="sxs-lookup"><span data-stu-id="9a4fe-216">• Active Project Team Members</span></span><br><span data-ttu-id="9a4fe-217">• Membres de l'equip del projecte</span><span class="sxs-lookup"><span data-stu-id="9a4fe-217">• Project Team Members</span></span><br><span data-ttu-id="9a4fe-218">• Visualització associada de membres de l'equip del projecte</span><span class="sxs-lookup"><span data-stu-id="9a4fe-218">• Project Team members associated View</span></span>|
|  <span data-ttu-id="9a4fe-219">Entrada de temps</span><span class="sxs-lookup"><span data-stu-id="9a4fe-219">Time Entry</span></span>|<span data-ttu-id="9a4fe-220">• Informació</span><span class="sxs-lookup"><span data-stu-id="9a4fe-220">• Information</span></span><br><span data-ttu-id="9a4fe-221">• Crear entrada de temps</span><span class="sxs-lookup"><span data-stu-id="9a4fe-221">• Create Time Entry</span></span>|<span data-ttu-id="9a4fe-222">• Les meves entrades de temps per data</span><span class="sxs-lookup"><span data-stu-id="9a4fe-222">• My Time Entries By Date</span></span><br><span data-ttu-id="9a4fe-223">• Les meves entrades de temps aquesta setmana</span><span class="sxs-lookup"><span data-stu-id="9a4fe-223">• My time Entries for this week</span></span><br><span data-ttu-id="9a4fe-224">• Entrades de temps pendents d'aprovació</span><span class="sxs-lookup"><span data-stu-id="9a4fe-224">• Time entries for approval</span></span>|
|  <span data-ttu-id="9a4fe-225">Línia del llibre diari</span><span class="sxs-lookup"><span data-stu-id="9a4fe-225">Journal Line</span></span>|<span data-ttu-id="9a4fe-226">• Informació</span><span class="sxs-lookup"><span data-stu-id="9a4fe-226">• Information</span></span><br><span data-ttu-id="9a4fe-227">• Creació ràpida:</span><span class="sxs-lookup"><span data-stu-id="9a4fe-227">• Quick create</span></span>|<span data-ttu-id="9a4fe-228">• Línies del llibre diari actives</span><span class="sxs-lookup"><span data-stu-id="9a4fe-228">• Active journal lines</span></span><br><span data-ttu-id="9a4fe-229">• Visualització associada de les línies del llibre diari</span><span class="sxs-lookup"><span data-stu-id="9a4fe-229">• Journal Line associated view</span></span>|
|  <span data-ttu-id="9a4fe-230">Detall de la línia de factura</span><span class="sxs-lookup"><span data-stu-id="9a4fe-230">Invoice Line Detail</span></span>|<span data-ttu-id="9a4fe-231">• Informació</span><span class="sxs-lookup"><span data-stu-id="9a4fe-231">• Information</span></span><br><span data-ttu-id="9a4fe-232">• Creació ràpida:</span><span class="sxs-lookup"><span data-stu-id="9a4fe-232">• Quick create</span></span>|<span data-ttu-id="9a4fe-233">• Detalls de la línia de factura activa</span><span class="sxs-lookup"><span data-stu-id="9a4fe-233">• Active Invoice Line Details</span></span><br><span data-ttu-id="9a4fe-234">• Transaccions de factura imputables</span><span class="sxs-lookup"><span data-stu-id="9a4fe-234">• Chargeable Invoice Transactions</span></span><br><span data-ttu-id="9a4fe-235">• Transaccions de factura gratuïtes</span><span class="sxs-lookup"><span data-stu-id="9a4fe-235">• Complimentary Invoice Transactions</span></span><br><span data-ttu-id="9a4fe-236">• Visualització associada de detall de la línia de factura</span><span class="sxs-lookup"><span data-stu-id="9a4fe-236">• Invoice Line Detail associated view</span></span><br><span data-ttu-id="9a4fe-237">• Transaccions de factura no imputables</span><span class="sxs-lookup"><span data-stu-id="9a4fe-237">• Non-Chargeable Invoice Transactions</span></span>|
|  <span data-ttu-id="9a4fe-238">Real</span><span class="sxs-lookup"><span data-stu-id="9a4fe-238">Actual</span></span>|<span data-ttu-id="9a4fe-239">• Informació</span><span class="sxs-lookup"><span data-stu-id="9a4fe-239">• Information</span></span><br><span data-ttu-id="9a4fe-240">• Valors reals actius</span><span class="sxs-lookup"><span data-stu-id="9a4fe-240">• Active Actuals</span></span>|<span data-ttu-id="9a4fe-241">• Visualització associada de valors reals</span><span class="sxs-lookup"><span data-stu-id="9a4fe-241">• Actual Associated view</span></span>|

<span data-ttu-id="9a4fe-242">Els camps personalitzats també s'han d'afegir a les regles de negocis en funció del que hàgiu definit.</span><span class="sxs-lookup"><span data-stu-id="9a4fe-242">Custom fields may also need to be added on business rules depending on what you have defined.</span></span> <span data-ttu-id="9a4fe-243">Un exemple de fàbrica és per a la regla de negocis **Capacitat d'edició de l'entrada de temps basada en l'estat**.</span><span class="sxs-lookup"><span data-stu-id="9a4fe-243">One out-of-the-box example is for the business rule **Editability of Time Entry based on status**.</span></span> <span data-ttu-id="9a4fe-244">Aquesta regla defineix quins camps s'han de blocar quan l'entrada de temps es troba en un estat no editable com ara **Aprovada**.</span><span class="sxs-lookup"><span data-stu-id="9a4fe-244">This rule defines which fields need to be locked when the Time Entry is in a non-editable status such as **Approved**.</span></span> <span data-ttu-id="9a4fe-245">Afegiu camps a aquesta regla de negocis per tal que els camps estiguin blocats per editar-se quan l'entrada de temps es trobi en un estat que no sigui **Esborrany** o **Retornada**.</span><span class="sxs-lookup"><span data-stu-id="9a4fe-245">Add fields to this business rule so that the fields are locked for editing when the Time Entry is in a status other than **Draft** or **Returned**.</span></span>