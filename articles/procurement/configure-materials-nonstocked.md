---
title: Configuració de materials sense existències i de factures pendents del proveïdor
description: En aquest tema s'explica com s'han d'habilitar els materials sense existències i les factures pendents del proveïdor.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 24418f3aad8356bd209eef7487a47a3870bce10f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993899"
---
# <a name="configure-non-stocked-materials-and-pending-vendor-invoices"></a><span data-ttu-id="b2190-103">Configuració de materials sense existències i de factures pendents del proveïdor</span><span class="sxs-lookup"><span data-stu-id="b2190-103">Configure non-stocked materials and pending vendor invoices</span></span>

<span data-ttu-id="b2190-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_</span><span class="sxs-lookup"><span data-stu-id="b2190-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

## <a name="minimum-version-requirement"></a><span data-ttu-id="b2190-105">Requisit mínim de la versió</span><span class="sxs-lookup"><span data-stu-id="b2190-105">Minimum version requirement</span></span>

<span data-ttu-id="b2190-106">Per utilitzar materials sense existències i factures pendents del proveïdor per a escenaris basats en recursos o sense existències per al Dynamics 365 Project Operations requereix aquestes versions:</span><span class="sxs-lookup"><span data-stu-id="b2190-106">Using non-stocked materials and pending vendor invoices for Dynamics 365 Project Operations non-stocked/resource based scenarios requires the following versions:</span></span>

<span data-ttu-id="b2190-107">Solucions del Dynamics 365 Dataverse:</span><span class="sxs-lookup"><span data-stu-id="b2190-107">Dynamics 365 Dataverse solutions:</span></span>

- <span data-ttu-id="b2190-108">Project Operations 4.9.0.221 o una versió posterior</span><span class="sxs-lookup"><span data-stu-id="b2190-108">Project Operations – 4.9.0.221 or higher</span></span>
- <span data-ttu-id="b2190-109">Solució d'orquestració d'aplicacions de doble escriptura 2.2.2.23 o una versió posterior</span><span class="sxs-lookup"><span data-stu-id="b2190-109">Dual-write application orchestration solution - 2.2.2.23 or higher</span></span>

<span data-ttu-id="b2190-110">Dynamics 365 Finance:</span><span class="sxs-lookup"><span data-stu-id="b2190-110">Dynamics 365 Finance:</span></span>
- <span data-ttu-id="b2190-111">10.0.18 (10.0.793.52) o una versió posterior.</span><span class="sxs-lookup"><span data-stu-id="b2190-111">10.0.18 (10.0.793.52) or higher.</span></span> <span data-ttu-id="b2190-112">Assegureu-vos que l'entorn de Finances estigui actualitzat i que totes les actualitzacions de qualitat s'apliquin segons els requisits mínims de versió.</span><span class="sxs-lookup"><span data-stu-id="b2190-112">Make sure that your Finance environment is current and all quality updates are applied to meet the minimum version requirements.</span></span>

## <a name="run-dual-write-maps-for-non-stocked-materials-and-vendor-invoice-integration"></a><span data-ttu-id="b2190-113">Executar assignacions de doble escriptura per a la integració de materials sense existències i de factures del proveïdor</span><span class="sxs-lookup"><span data-stu-id="b2190-113">Run Dual-write maps for non-stocked materials and vendor invoice integration</span></span>

<span data-ttu-id="b2190-114">Aquesta secció proporciona informació sobre les assignacions específiques necessàries per als materials sense existències i les factures de proveïdors.</span><span class="sxs-lookup"><span data-stu-id="b2190-114">This section provides information about specific the maps required for non-stocked materials and vendor invoices.</span></span> <span data-ttu-id="b2190-115">Verifiqueu que les assignacions de requisits previs que s'enumeren al tema [Proveïment d'un entorn nou](../environment/resource-provision-new-environment.md#run-project-operations-dual-write-maps) s'estiguin executant al vostre entorn.</span><span class="sxs-lookup"><span data-stu-id="b2190-115">Verify that the prerequisite maps listed in the [Provision a new environment](../environment/resource-provision-new-environment.md#run-project-operations-dual-write-maps) topic are running on your environment.</span></span>

1. <span data-ttu-id="b2190-116">Aneu a Lifecycle Services (LCS), aneu al projecte LCS i aneu a la pàgina **Detalls de l'entorn**.</span><span class="sxs-lookup"><span data-stu-id="b2190-116">Go to Lifecycle Services (LCS), navigate to your LCS project, and go to the **Environment details** page.</span></span>
2. <span data-ttu-id="b2190-117">A la secció **Informació de l'entorn Common Data Service**, seleccioneu **Enllaça amb CDS per a aplicacions**.</span><span class="sxs-lookup"><span data-stu-id="b2190-117">In the **Common Data Service Environment Information** section, select **Link to CDS for Apps**.</span></span> <span data-ttu-id="b2190-118">Després de seleccionar l'enllaç, se us redirigirà a la llista d'entitats de les assignacions.</span><span class="sxs-lookup"><span data-stu-id="b2190-118">After you select the link, you will be redirected to the list of entities in the mappings.</span></span>
3. <span data-ttu-id="b2190-119">Assegureu-vos que s'estiguin executant les assignacions següents.</span><span class="sxs-lookup"><span data-stu-id="b2190-119">Make sure the following maps are running.</span></span> <span data-ttu-id="b2190-120">Si no s'estan executant, inicieu-les i assegureu-vos d'incloure totes les assignacions de taules relacionades.</span><span class="sxs-lookup"><span data-stu-id="b2190-120">If they aren't running, start them and make sure to include all related table maps.</span></span>

    - <span data-ttu-id="b2190-121">Diferents productes publicats amb CDS (productes)</span><span class="sxs-lookup"><span data-stu-id="b2190-121">CDS released distinct products (products)</span></span>
    - <span data-ttu-id="b2190-122">Proveïdors v2 (msdyn_vendors)</span><span class="sxs-lookup"><span data-stu-id="b2190-122">Vendors v2 (msdyn_vendors)</span></span>
    - <span data-ttu-id="b2190-123">Taula del Project Operations per a estimacions de materials (msdyn_estimatelines)</span><span class="sxs-lookup"><span data-stu-id="b2190-123">Project Operations table for material estimates (msdyn_estimatelines)</span></span>
    - <span data-ttu-id="b2190-124">Entitat d'exportació de factura del proveïdor del projecte de la integració del Project Operations (msdyn_projectvendorinvoices)</span><span class="sxs-lookup"><span data-stu-id="b2190-124">Project Operations integration project vendor invoice export entity (msdyn_projectvendorinvoices)</span></span>
    - <span data-ttu-id="b2190-125">Entitat d'exportació de la línia de factura del proveïdor del projecte de la integració del Project Operations (msdyn_projectvendorinvoicelines)</span><span class="sxs-lookup"><span data-stu-id="b2190-125">Project Operations integration project vendor invoice line export entity (msdyn_projectvendorinvoicelines)</span></span>
    - <span data-ttu-id="b2190-126">Valors reals d'integració del Project Operations (msdyn_actuals).</span><span class="sxs-lookup"><span data-stu-id="b2190-126">Project Operations integration actuals (msdyn_actuals).</span></span> <span data-ttu-id="b2190-127">Assegureu-vos que esteu executant la versió d'assignació 1.0.0.14 o una de posterior.</span><span class="sxs-lookup"><span data-stu-id="b2190-127">Make sure you are running map version 1.0.0.14 or higher.</span></span> <span data-ttu-id="b2190-128">Podeu veure la versió activa de l'assignació a la columna **Versió** de la pàgina **Escriptura doble**.</span><span class="sxs-lookup"><span data-stu-id="b2190-128">You can see the active version of the map in the **Version** column on the **Dual Write** page.</span></span> <span data-ttu-id="b2190-129">Per activar una versió nova de l'assignació, seleccioneu **Versió de l'assignació de la taula** i després deseu la versió seleccionada.</span><span class="sxs-lookup"><span data-stu-id="b2190-129">You can activate a new version of the map by selecting **Table map version** and then saving the selected version.</span></span>

<span data-ttu-id="b2190-130">Si utilitzeu dades de demostració estàndard, pot ser que també hàgiu d'aturar i reiniciar les assignacions d'entitat següents amb la sincronització inicial:</span><span class="sxs-lookup"><span data-stu-id="b2190-130">If you are using standard demo data, you might also need to stop and restart the following entity maps with initial sync:</span></span>
  - <span data-ttu-id="b2190-131">Dies de pagament en CDS V2 (msdyn_paymentdays)</span><span class="sxs-lookup"><span data-stu-id="b2190-131">Payment days CDS V2 (msdyn_paymentdays)</span></span>
  - <span data-ttu-id="b2190-132">Planificació de pagaments (msdyn_paymentschedules)</span><span class="sxs-lookup"><span data-stu-id="b2190-132">Payment schedule (msdyn_paymentschedules)</span></span>
  - <span data-ttu-id="b2190-133">Condicions de pagament (msdyn_paymentterms)</span><span class="sxs-lookup"><span data-stu-id="b2190-133">Terms of payment (msdyn_paymentterms)</span></span>
  - <span data-ttu-id="b2190-134">Grups de proveïdors (msdyn_vendorgroups)</span><span class="sxs-lookup"><span data-stu-id="b2190-134">Vendor groups (msdyn_vendorgroups)</span></span>
  - <span data-ttu-id="b2190-135">Unitats (uom)</span><span class="sxs-lookup"><span data-stu-id="b2190-135">Units (uom)</span></span>

> [!NOTE]
> <span data-ttu-id="b2190-136">La sincronització inicial per a grups de proveïdors i unitats pot fallar en alguns registres del conjunt de dades de demostració existent.</span><span class="sxs-lookup"><span data-stu-id="b2190-136">The initial sync for vendor groups and units might fail for a few records in the existing demo data set.</span></span> <span data-ttu-id="b2190-137">Podeu ignorar els errors perquè no us privaran d'utilitzar dades de demostració amb el Project Operations.</span><span class="sxs-lookup"><span data-stu-id="b2190-137">You can ignore the failures as they won't prevent you from using demo data with Project Operations.</span></span>

## <a name="configure-prerequisites-in-dataverse"></a><span data-ttu-id="b2190-138">Configuració dels requisits previs al Dataverse</span><span class="sxs-lookup"><span data-stu-id="b2190-138">Configure prerequisites in Dataverse</span></span>

### <a name="activate-workflow-to-create-accounts-based-on-vendor-entity"></a><span data-ttu-id="b2190-139">Activació del flux de treball per crear comptes basats en una entitat de proveïdor</span><span class="sxs-lookup"><span data-stu-id="b2190-139">Activate workflow to create accounts based on vendor entity</span></span>

<span data-ttu-id="b2190-140">La solució Dual Write Orchestration proporciona [Integracó del patró de proveïdors](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/vendor-mapping.md)Proveïdors.</span><span class="sxs-lookup"><span data-stu-id="b2190-140">The Dual Write Orchestration solution provides [Vendors master integration](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/vendor-mapping.md).</span></span> <span data-ttu-id="b2190-141">Com a requisit previ per a aquesta característica, les dades del proveïdor s'han de crear a l'entitat **Comptes**.</span><span class="sxs-lookup"><span data-stu-id="b2190-141">As a prerequisite for this feature, vendor data must be created in the **Accounts** entity.</span></span> <span data-ttu-id="b2190-142">Activació d'un procés de flux de treball de plantilla per crear proveïdors a la taula **Comptes**, segons s'explica a [Canvia entre els dissenys del proveïdor](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/vendor-switch.md#use-the-extended-vendor-design-for-vendors-of-the-organization-type).</span><span class="sxs-lookup"><span data-stu-id="b2190-142">Activate a template workflow process to create vendors in the **Accounts** table as described in [Switch between vendor designs](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/vendor-switch.md#use-the-extended-vendor-design-for-vendors-of-the-organization-type).</span></span>

### <a name="set-products-to-be-created-as-active"></a><span data-ttu-id="b2190-143">Definiu que els productes es creïn com a actius</span><span class="sxs-lookup"><span data-stu-id="b2190-143">Set products to be created as active</span></span>

<span data-ttu-id="b2190-144">Els materials sense existències s'han de configurar com a **Productes publicats** a Finances.</span><span class="sxs-lookup"><span data-stu-id="b2190-144">Non-stocked materials must be configured as **Released products** in Finance.</span></span> <span data-ttu-id="b2190-145">La solució Dual Write Orchestration proporciona una [Integració de productes publicats a punt per a utilitzar al catàleg de productes del Dataverse](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/product-mapping.md).</span><span class="sxs-lookup"><span data-stu-id="b2190-145">The Dual Write Orchestration solution provides an out-of-the-box [Released products integration to Dataverse Product catalog](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/product-mapping.md).</span></span> <span data-ttu-id="b2190-146">Per defecte, els productes de Finances se sincronitzen amb el Dataverse en estat d'esborrany.</span><span class="sxs-lookup"><span data-stu-id="b2190-146">By default, products from Finance are synchronized to Dataverse in a draft state.</span></span> <span data-ttu-id="b2190-147">Per sincronitzar el producte amb un estat actiu per tal que es pugui utilitzar directament en documents d'ús de materials o en factures de proveïdor pendents, aneu a **Sistema** > **Administració** > **Administració del sistmea** > **Configuració del sistema** i, a la pestanya **Vendes**, definiu **Creació de productes en estat actiu** en **Sí**.</span><span class="sxs-lookup"><span data-stu-id="b2190-147">To synchronize the product to an active state so that it can be directly used in material usage documents or pending vendor invoices, go to **System** > **Administration** > **System administration** > **System settings**, and on the **Sales** tab, set **Create products in active state** to **Yes**.</span></span>

## <a name="configure-prerequisites-in-finance"></a><span data-ttu-id="b2190-148">Configuració dels requisits previs a Finances</span><span class="sxs-lookup"><span data-stu-id="b2190-148">Configure prerequisites in Finance</span></span>

### <a name="enable-the-feature-key-for-pending-vendor-invoices"></a><span data-ttu-id="b2190-149">Habilitació de la clau de característica per a les factures del proveïdor pendents</span><span class="sxs-lookup"><span data-stu-id="b2190-149">Enable the feature key for pending vendor invoices</span></span>

<span data-ttu-id="b2190-150">Completeu els passos següents per habilitar la funcionalitat per afegir detalls del projecte a les línies de factura del proveïdor pendents.</span><span class="sxs-lookup"><span data-stu-id="b2190-150">Complete the following steps to enable functionality to add project details on pending vendor invoice lines.</span></span>

1. <span data-ttu-id="b2190-151">A Finances, aneu a l'espai de treball **Administració de característiques**.</span><span class="sxs-lookup"><span data-stu-id="b2190-151">In Finance, go to the **Feature Management** workspace.</span></span>
2. <span data-ttu-id="b2190-152">A la llista de característiques, cerqueu la característica **Habilita les factures del proveïdor pendents al Project Operations per a escenaris basats en recursos o sense existències** i seleccioneu **Habilita**.</span><span class="sxs-lookup"><span data-stu-id="b2190-152">In the feature list, find **Enable pending vendor invoices on Project Operations for resource based/non-stocked scenarios** feature and select **Enable**.</span></span>

### <a name="define-category-groups-and-project-categories-for-items"></a><span data-ttu-id="b2190-153">Definició de grups de categories i categories de projecte per als elements</span><span class="sxs-lookup"><span data-stu-id="b2190-153">Define category groups and project categories for items</span></span>

<span data-ttu-id="b2190-154">Configureu com a mínim un grup de categories per al tipus de transacció **Element**, i com a mínim una categoria de projecte utilitzant aquest grup.</span><span class="sxs-lookup"><span data-stu-id="b2190-154">Configure at least one category group for the **Item** transaction type , and at least one project category using this group.</span></span> <span data-ttu-id="b2190-155">Per obtenir més informació, vegeu [Configuració de categories de projecte](../project-accounting/configure-project-categories.md#category-groups).</span><span class="sxs-lookup"><span data-stu-id="b2190-155">For more information, see [Configure project categories](../project-accounting/configure-project-categories.md#category-groups).</span></span>

<span data-ttu-id="b2190-156">Reviseu els perfils de cost i ingressos del projecte i configureu la configuració de publicació de missatges per a les transaccions d'articles.</span><span class="sxs-lookup"><span data-stu-id="b2190-156">Review the project cost and revenue profiles, and configure ledger posting setup for item transactions.</span></span> <span data-ttu-id="b2190-157">Per obtenir més informació, vegeu [Configuració de la comptabilitat per a projectes facturables](../project-accounting/configure-accounting-billable-projects.md).</span><span class="sxs-lookup"><span data-stu-id="b2190-157">For more information, see [Configure accounting for billable projects](../project-accounting/configure-accounting-billable-projects.md).</span></span>

### <a name="set-up-a-write-in-product"></a><span data-ttu-id="b2190-158">Configuració d'un producte fora de catàleg</span><span class="sxs-lookup"><span data-stu-id="b2190-158">Set up a write-in product</span></span>

<span data-ttu-id="b2190-159">Al Project Operations, podeu registrar les estimacions i l'ús de materials dels productes del catàleg que es configuren al catàleg de productes publicats i als productes fora de catàleg.</span><span class="sxs-lookup"><span data-stu-id="b2190-159">In Project Operations, you can record material estimates and usage for catalog products that are configured in the released product catalog and for write-in products.</span></span> <span data-ttu-id="b2190-160">Per utilitzar productes fora de catàleg cal un únic producte publicat que s'ha configurat a Finances amb aquesta finalitat.</span><span class="sxs-lookup"><span data-stu-id="b2190-160">Using write-in products requires a single released product that's configured in Finance for this purpose.</span></span> <span data-ttu-id="b2190-161">Completeu els passos següents per configurar un producte fora de catàleg.</span><span class="sxs-lookup"><span data-stu-id="b2190-161">Complete the following steps to configure a write-in product.</span></span> <span data-ttu-id="b2190-162">Repetiu aquests passos a cada entitat legal que utilitzi el Project Operations per a escenaris de recursos o sense existències.</span><span class="sxs-lookup"><span data-stu-id="b2190-162">Repeat these steps in each legal entity that is using Project Operations for resource/non-stocked scenarios.</span></span>

1. <span data-ttu-id="b2190-163">A Finances, aneu a **Administració de la informació dels productes** > **Productes** > **Productes publicats**, i seleccioneu **Crea**.</span><span class="sxs-lookup"><span data-stu-id="b2190-163">In Finance, go to **Product Information Management** > **Products** > **Released products**, and select **New**.</span></span>
2. <span data-ttu-id="b2190-164">Al camp **Tipus de producte**, seleccioneu **Element** i al camp **Subtipus de producte** seleccioneu **Producte**.</span><span class="sxs-lookup"><span data-stu-id="b2190-164">In the **Product type** field, select **Item** and in the **Product subtype** field, select **Product**.</span></span>
3. <span data-ttu-id="b2190-165">Introduïu el número del producte (WRITEIN) i el nom del producte (Producte fora de catàleg).</span><span class="sxs-lookup"><span data-stu-id="b2190-165">Enter the product number (WRITEIN) and the product name (Write-in Product).</span></span>
4. <span data-ttu-id="b2190-166">Seleccioneu el grup del model d'elements.</span><span class="sxs-lookup"><span data-stu-id="b2190-166">Select  the item model group.</span></span> <span data-ttu-id="b2190-167">Assegureu-vos que el grup del model d'elements que seleccioneu té el camp **Producte en existències de la política d'inventari** en **Fals**.</span><span class="sxs-lookup"><span data-stu-id="b2190-167">Make sure that the item model group you select has the **Inventory policy Stocked product** field set to **False**.</span></span>
5. <span data-ttu-id="b2190-168">Seleccioneu valors als camps **Grup d'elements**, **Grup de mesures d'emmagatzematge** i **Grup de mesures de seguiment**.</span><span class="sxs-lookup"><span data-stu-id="b2190-168">Select values in the **Item group**, **Storage dimension group**, and **Tracking dimension group** fields.</span></span> <span data-ttu-id="b2190-169">Utilitzeu la **Mesura d'emmagatzematge** només per a **Lloc**, i no definiu mesures de seguiment.</span><span class="sxs-lookup"><span data-stu-id="b2190-169">Use the **Storage dimension** for **Site** only, and do not set any tracking dimensions.</span></span>
6. <span data-ttu-id="b2190-170">Seleccioneu valors al camp **Unitat d'inventari**, **Unitat de compra** i **Unitat de vendes** i, a continuació, deseu els canvis.</span><span class="sxs-lookup"><span data-stu-id="b2190-170">Select values in the **Inventory unit**, **Purchase unit**, and **Sales unit** field, and then save your changes.</span></span>
7. <span data-ttu-id="b2190-171">A la pestanya **Pla**, definiu la configuració de comanda per defecte i, a la pestanya **Inventari**, definiu el lloc per defecte i el magatzem.</span><span class="sxs-lookup"><span data-stu-id="b2190-171">In the **Plan** tab, set the default order settings, and on the **Inventory** tab, set the default site and warehouse.</span></span>
8. <span data-ttu-id="b2190-172">Aneu a **Administració i comptabilitat del projecte** > **Configuració** > **Paràmetres d'administració i comptabilitat del projecte** i obriu **Project Operations al Dynamics 365 Dataverse**.</span><span class="sxs-lookup"><span data-stu-id="b2190-172">Go to **Project management and accounting** > **Setup** > **Project management and accounting parameters** and open **Project Operations on Dynamics 365 Dataverse**.</span></span> 
9. <span data-ttu-id="b2190-173">A la pestanya **Materials**, al camp **Producte fora de catàleg**, seleccioneu el producte que heu creat.</span><span class="sxs-lookup"><span data-stu-id="b2190-173">On the **Materials** tab, in the **Write-in product** field, select the product you created.</span></span>
10. <span data-ttu-id="b2190-174">Al vostre entorn del Dataverse, al mapa del lloc, obriu l'entitat **Productes** i cerqueu el registre de producte fora de catàleg.</span><span class="sxs-lookup"><span data-stu-id="b2190-174">In your Dataverse environment, in the site map, open the **Products** entity and find the write-in product record.</span></span> 
11. <span data-ttu-id="b2190-175">Obriu els detalls del registre i definiu l'estat de producte com a **Retirat**.</span><span class="sxs-lookup"><span data-stu-id="b2190-175">Open the record details and set product state to **Retired**.</span></span> <span data-ttu-id="b2190-176">Aquest estat del producte impedeix que algú pugui utilitzar accidentalment aquest registre directament en les estimacions de materials i en els documents d'ús.</span><span class="sxs-lookup"><span data-stu-id="b2190-176">This product state prevents anyone from accidentally using this record directly in material estimates and usage documents.</span></span>

### <a name="set-up-a-procurement-integration-account"></a><span data-ttu-id="b2190-177">Configuració d'un compte d'integració de proveïment</span><span class="sxs-lookup"><span data-stu-id="b2190-177">Set up a procurement integration account</span></span>

<span data-ttu-id="b2190-178">El compte d'integració de proveïment s'utilitza com a compte de neteja quan es publica una factura del proveïdor pendent amb línies atribuïdes a un projecte.</span><span class="sxs-lookup"><span data-stu-id="b2190-178">The procurement integration account is used as a clearing account when posting a pending vendor invoice with lines attributed to a project.</span></span>

<span data-ttu-id="b2190-179">Quan el sistema publica una factura de proveïdor pendent, aquest compte s'utilitza per a l'import de cost del projecte.</span><span class="sxs-lookup"><span data-stu-id="b2190-179">When the system posts a pending vendor invoice, this account is used for the project cost amount.</span></span> <span data-ttu-id="b2190-180">Els detalls de la factura del proveïdor es processen al Dataverse i es crea un valor real del projecte corresponent.</span><span class="sxs-lookup"><span data-stu-id="b2190-180">The vendor invoice details are processed in Dataverse, and a corresponding project actual is created.</span></span> <span data-ttu-id="b2190-181">La informació del valor real del projecte s'afegeix al llibre diari d'integració del Project Operations.</span><span class="sxs-lookup"><span data-stu-id="b2190-181">The information from the project actual is added to the Project Operations Integration journal.</span></span> <span data-ttu-id="b2190-182">Quan publiqueu el llibre diari d'integració, la quantitat s'esborra del compte d'integració del proveïment i es registra al cost del projecte.</span><span class="sxs-lookup"><span data-stu-id="b2190-182">When you post the integration journal, the amount is cleared from the procurement integration account and recorded to the project cost.</span></span>

1. <span data-ttu-id="b2190-183">Per configurar un compte d'integració del proveïment, aneu a **Administració i comptabilitat del projecte** > **Configuració** > **Paràmetres d'administració i comptabilitat del projecte** i obriu **Project Operations al Dynamics 365 Dataverse**.</span><span class="sxs-lookup"><span data-stu-id="b2190-183">To set up the procurement integration account, go to **Project management and accounting** > **Setup** > **Project management and accounting parameters**, and open **Project Operations on Dynamics 365 Dataverse**.</span></span> 
2. <span data-ttu-id="b2190-184">Seleccioneu la pestanya **Materials** i seleccioneu un valor al camp **Compte d'integració del proveïment**.</span><span class="sxs-lookup"><span data-stu-id="b2190-184">Select the **Materials** tab, and select a value in the **Procurement integration account** field.</span></span>

#### <a name="set-up-project-category-defaults-for-an-item"></a><span data-ttu-id="b2190-185">Configuració per defecte de les categories de projecte per a un element</span><span class="sxs-lookup"><span data-stu-id="b2190-185">Set up project category defaults for an item</span></span>

1. <span data-ttu-id="b2190-186">A Finances, aneu a **Administració i comptabilitat del projecte** > **Configuració** > **Paràmetres d'administració i comptabilitat del projecte**, i obriu **Project Operations al Dynamics 365 Dataverse**.</span><span class="sxs-lookup"><span data-stu-id="b2190-186">In Finance, go to **Project management and accounting** > **Setup** > **Project management and accounting parameters**, and open **Project Operations on Dynamics 365 Dataverse**.</span></span> 
2. <span data-ttu-id="b2190-187">A la pestanya **Valors per defecte de la categoria del projecte**, al camp **Element**, seleccioneu un valor.</span><span class="sxs-lookup"><span data-stu-id="b2190-187">On the **Project category defaults** tab, in the **Item** field, select a value.</span></span> <span data-ttu-id="b2190-188">Aquesta categoria de projecte s'utilitza per a transaccions materials si la categoria de projecte no s'ha definit al registre de valors reals del projecte.</span><span class="sxs-lookup"><span data-stu-id="b2190-188">This project category is used for material transactions if the project category wasn't set on the project actuals record.</span></span>