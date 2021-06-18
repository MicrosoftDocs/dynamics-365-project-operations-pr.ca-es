---
title: Configuració i aplicació de les dades de configuració al Common Data Service
description: En aquest tema es proporciona informació sobre com configurar i aplicar les dades de configuració al Project Operations.
author: sigitac
ms.date: 05/10/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 2ea00df6112fb69b61f1889463424fdfee79aec9
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001279"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service"></a><span data-ttu-id="9a24a-103">Configuració i aplicació de les dades de configuració al Common Data Service</span><span class="sxs-lookup"><span data-stu-id="9a24a-103">Set up and apply configuration data in the Common Data Service</span></span> 

<span data-ttu-id="9a24a-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_</span><span class="sxs-lookup"><span data-stu-id="9a24a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="9a24a-105">Requisits previs</span><span class="sxs-lookup"><span data-stu-id="9a24a-105">Prerequisites</span></span>

<span data-ttu-id="9a24a-106">Abans de començar a configurar les dades al Common Data Service (CDS), cal complir els requisits previs següents:</span><span class="sxs-lookup"><span data-stu-id="9a24a-106">Before you begin to configure data in the Common Data Service (CDS), the following prerequisites must be met:</span></span>

1.  <span data-ttu-id="9a24a-107">Proveir un entorn del CDS i un entorn del Dynamics 365 Finance per al Project Operations.</span><span class="sxs-lookup"><span data-stu-id="9a24a-107">Provision a CDS environment and a Dynamics 365 Finance environment for Project Operations.</span></span>
2.  <span data-ttu-id="9a24a-108">La informació de les entitats jurídiques del Dynamics 365 Finance es comparteix a l'entorn del CDS.</span><span class="sxs-lookup"><span data-stu-id="9a24a-108">Legal entity information from Dynamics 365 Finance is shared to the CDS environment.</span></span> <span data-ttu-id="9a24a-109">Això significa que l'entitat **Empresa** al CDS té els següents registres d'empresa:</span><span class="sxs-lookup"><span data-stu-id="9a24a-109">This means that the **Company** entity in CDS has the following company records:</span></span>
  - <span data-ttu-id="9a24a-110">THPM</span><span class="sxs-lookup"><span data-stu-id="9a24a-110">THPM</span></span>
  - <span data-ttu-id="9a24a-111">USPM</span><span class="sxs-lookup"><span data-stu-id="9a24a-111">USPM</span></span>
  - <span data-ttu-id="9a24a-112">GBPM</span><span class="sxs-lookup"><span data-stu-id="9a24a-112">GBPM</span></span>

## <a name="install-setup-and-configuration-data"></a><span data-ttu-id="9a24a-113">Configuració de la instal·lació i dades de configuració</span><span class="sxs-lookup"><span data-stu-id="9a24a-113">Install setup and configuration data</span></span>

1. <span data-ttu-id="9a24a-114">Baixeu, desbloquegeu i descomprimiu el [paquet de dades d'instal·lació i configuració](https://download.microsoft.com/download/e/2/d/e2da6c98-d5dd-450c-aabe-fd6bf2ba374b/ProjOpsSampleSetupData-%20Integrated%20Latest.zip).</span><span class="sxs-lookup"><span data-stu-id="9a24a-114">Download, unblock, and unzip the [Setup and Configuration Data Package](https://download.microsoft.com/download/e/2/d/e2da6c98-d5dd-450c-aabe-fd6bf2ba374b/ProjOpsSampleSetupData-%20Integrated%20Latest.zip).</span></span>
2. <span data-ttu-id="9a24a-115">Aneu a la carpeta descomprimida i executeu el fitxer executable, *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="9a24a-115">Navigate to the unzipped folder and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="9a24a-116">A la pàgina 1 de l'auxiliar de configuració de la migració del Common Data Service (CMT), seleccioneu **Importa les dades** i, a continuació, seleccioneu **Continua**.</span><span class="sxs-lookup"><span data-stu-id="9a24a-116">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Migració de la configuració](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="9a24a-118">A la pàgina 2 de l'auxiliar CMT, seleccioneu **Microsoft 365** com a **Tipus d'implementació**.</span><span class="sxs-lookup"><span data-stu-id="9a24a-118">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="9a24a-119">Marqueu les caselles **Mostra una llista d'organitzacions disponibles** i **Mostra les opcions avançades**.</span><span class="sxs-lookup"><span data-stu-id="9a24a-119">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="9a24a-120">Seleccioneu la regió del vostre inquilí, introduïu les credencials i seleccioneu **Inicia la sessió**.</span><span class="sxs-lookup"><span data-stu-id="9a24a-120">Select the region of your tenant, enter your credentials, and select **Login**.</span></span>

![Inici de sessió de configuració](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="9a24a-122">A la pàgina 3, a la llista d'organitzacions de l'inquilí, seleccioneu l'organització a la qual voleu importar les dades de demostració i feu clic a **Inicia la sessió**.</span><span class="sxs-lookup"><span data-stu-id="9a24a-122">On page 3, from the list of organizations on the tenant, select the organization you want to import the demo data into and select **Login**.</span></span>
8. <span data-ttu-id="9a24a-123">A la pàgina 4, seleccioneu el fitxer zip *MasterAndSetupData* de la carpeta desempaquetada.</span><span class="sxs-lookup"><span data-stu-id="9a24a-123">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder.</span></span>

![Selecció del fitxer ZIP](./media/3ZipFile.png)

![Permet seleccionar un fitxer.](./media/4SelectAFile.png)

9. <span data-ttu-id="9a24a-126">Després de seleccionar el fitxer zip, seleccioneu **Importa les dades**.</span><span class="sxs-lookup"><span data-stu-id="9a24a-126">After the zip file is selected, select **Import Data**.</span></span>

![Importa les dades](./media/5ImportData.png)

10. <span data-ttu-id="9a24a-128">La importació s'executarà durant aproximadament dos-deu minuts en funció de la velocitat de la xarxa.</span><span class="sxs-lookup"><span data-stu-id="9a24a-128">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="9a24a-129">Després de completar-se la importació, sortiu de l'auxiliar de CMT.</span><span class="sxs-lookup"><span data-stu-id="9a24a-129">After import completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="9a24a-130">Consulteu a la vostra organització les dades de les següents 26 entitats:</span><span class="sxs-lookup"><span data-stu-id="9a24a-130">Check your organization for data in the following 26 entities:</span></span>

  - <span data-ttu-id="9a24a-131">Moneda</span><span class="sxs-lookup"><span data-stu-id="9a24a-131">Currency</span></span>
  - <span data-ttu-id="9a24a-132">Taula de comptes</span><span class="sxs-lookup"><span data-stu-id="9a24a-132">Chart of Accounts</span></span>
  - <span data-ttu-id="9a24a-133">Calendari fiscal</span><span class="sxs-lookup"><span data-stu-id="9a24a-133">Fiscal Calendar</span></span>
  - <span data-ttu-id="9a24a-134">Classificació de tipus de canvi de moneda</span><span class="sxs-lookup"><span data-stu-id="9a24a-134">Currency Exchange Rate Types</span></span>
  - <span data-ttu-id="9a24a-135">Dia de pagament</span><span class="sxs-lookup"><span data-stu-id="9a24a-135">Payment Day</span></span>
  - <span data-ttu-id="9a24a-136">Planificació de pagament</span><span class="sxs-lookup"><span data-stu-id="9a24a-136">Payment Schedule</span></span>
  - <span data-ttu-id="9a24a-137">Condició de pagament</span><span class="sxs-lookup"><span data-stu-id="9a24a-137">Payment Term</span></span>
  - <span data-ttu-id="9a24a-138">Unitat organitzativa</span><span class="sxs-lookup"><span data-stu-id="9a24a-138">Organizational Unit</span></span>
  - <span data-ttu-id="9a24a-139">Contacte</span><span class="sxs-lookup"><span data-stu-id="9a24a-139">Contact</span></span>
  - <span data-ttu-id="9a24a-140">Grup d'impostos</span><span class="sxs-lookup"><span data-stu-id="9a24a-140">Tax Group</span></span>
  - <span data-ttu-id="9a24a-141">Grup de clients</span><span class="sxs-lookup"><span data-stu-id="9a24a-141">Customer Group</span></span>
  - <span data-ttu-id="9a24a-142">Grup de proveïdors</span><span class="sxs-lookup"><span data-stu-id="9a24a-142">Vendor Group</span></span>
  - <span data-ttu-id="9a24a-143">Unitat</span><span class="sxs-lookup"><span data-stu-id="9a24a-143">Unit</span></span>
  - <span data-ttu-id="9a24a-144">Grup d’unitats</span><span class="sxs-lookup"><span data-stu-id="9a24a-144">Unit Group</span></span>
  - <span data-ttu-id="9a24a-145">Llista de preus</span><span class="sxs-lookup"><span data-stu-id="9a24a-145">Price List</span></span>
  - <span data-ttu-id="9a24a-146">Llista de preus del paràmetre de projecte</span><span class="sxs-lookup"><span data-stu-id="9a24a-146">Project Parameter Price List</span></span>
  - <span data-ttu-id="9a24a-147">Freqüència de facturació</span><span class="sxs-lookup"><span data-stu-id="9a24a-147">Invoice Frequency</span></span>
  - <span data-ttu-id="9a24a-148">Categoria de recursos que es poden reservar</span><span class="sxs-lookup"><span data-stu-id="9a24a-148">Bookable Resource Category</span></span>
  - <span data-ttu-id="9a24a-149">Categoria de transacció</span><span class="sxs-lookup"><span data-stu-id="9a24a-149">Transaction Category</span></span>
  - <span data-ttu-id="9a24a-150">Categoria de despesa</span><span class="sxs-lookup"><span data-stu-id="9a24a-150">Expense Category</span></span>
  - <span data-ttu-id="9a24a-151">Preu per funció</span><span class="sxs-lookup"><span data-stu-id="9a24a-151">Role Price</span></span>
  - <span data-ttu-id="9a24a-152">Preu de categoria de transacció</span><span class="sxs-lookup"><span data-stu-id="9a24a-152">Transaction Category Price</span></span>
  - <span data-ttu-id="9a24a-153">Característica</span><span class="sxs-lookup"><span data-stu-id="9a24a-153">Characteristic</span></span>
  - <span data-ttu-id="9a24a-154">Recurs que es pot reservar</span><span class="sxs-lookup"><span data-stu-id="9a24a-154">Bookable Resource</span></span>
  - <span data-ttu-id="9a24a-155">Associació de categoria de recursos que es poden reservar</span><span class="sxs-lookup"><span data-stu-id="9a24a-155">Bookable resource category Assn</span></span>
  - <span data-ttu-id="9a24a-156">Característica dels recursos que es poden reservar</span><span class="sxs-lookup"><span data-stu-id="9a24a-156">Bookable Resource Characteristic</span></span>

![Importació completada](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a><span data-ttu-id="9a24a-158">Actualitzar les configuracions del Project Operations</span><span class="sxs-lookup"><span data-stu-id="9a24a-158">Update Project Operations configurations</span></span>

1. <span data-ttu-id="9a24a-159">Navegueu a l'entorn del CE.</span><span class="sxs-lookup"><span data-stu-id="9a24a-159">Navigate to the CE environment.</span></span> <span data-ttu-id="9a24a-160">Podeu trobar-la obrint el [centre d'administració del Power Platform](https://admin.powerplatform.microsoft.com/environments), seleccionant l'entorn i, a continuació, seleccionant **Obre l'entorn**.</span><span class="sxs-lookup"><span data-stu-id="9a24a-160">You can find it by opening the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), selecting the environment, and then selecting **Open Environment**.</span></span> 

![Obrir l'entorn](./media/7OpenEnvironment.png)

2. <span data-ttu-id="9a24a-162">Aneu a **Projectes** > **Recursos** i, a continuació, seleccioneu **Nou** per crear un recurs reservable per a l'usuari.</span><span class="sxs-lookup"><span data-stu-id="9a24a-162">Go to **Projects** > **Resources** and then select **New** to create a bookable resource for your user.</span></span>

![Recursos que es poden reservar](./media/8BookableResources.png)

3. <span data-ttu-id="9a24a-164">A la pestanya **General**, seleccioneu el vostre usuari d'administració.</span><span class="sxs-lookup"><span data-stu-id="9a24a-164">On the **General** tab, select your admin user.</span></span> <span data-ttu-id="9a24a-165">Verifiqueu que el fus horari coincideixi amb el fus en què us trobeu.</span><span class="sxs-lookup"><span data-stu-id="9a24a-165">Verify that the time zone matches the one you are in.</span></span> 

![Nou recurs que es pot reservar](./media/9NewBookableResource.png)

4. <span data-ttu-id="9a24a-167">A la pestanya **Planificació**, al camp **Empresa**, trieu l'empresa **USPM** i, a continuació, seleccioneu **Desa**.</span><span class="sxs-lookup"><span data-stu-id="9a24a-167">On the **Scheduling** tab, in the **Company** field, pick the **USPM** company, and then select **Save**.</span></span> 

![Pestanya Planificació](./media/10SchedulingTab.png)

5. <span data-ttu-id="9a24a-169">Seleccioneu la pestanya **Hores de treball**.</span><span class="sxs-lookup"><span data-stu-id="9a24a-169">Select the **Work hours** tab.</span></span>  

![Hores de feina](./media/11WorkHours.png)

6. <span data-ttu-id="9a24a-171">Feu doble clic a qualsevol valor del calendari i seleccioneu **Edita** > **Tots els esdeveniments de la sèrie**.</span><span class="sxs-lookup"><span data-stu-id="9a24a-171">Double-click on any value in the calendar and select **Edit** > **All events in the series**.</span></span> 

![Calendari de treball](./media/12WorkCalendar.png)

7. <span data-ttu-id="9a24a-173">Canvieu les hores de treball a una jornada de treball de vuit (8) hores, marqueu els caps de setmana com a dies inhàbils i assegureu-vos que el fus horari coincideixi amb el vostre.</span><span class="sxs-lookup"><span data-stu-id="9a24a-173">Change work hours to an eight (8) hour work day, mark weekends as non-work days, and make sure time zone matches yours.</span></span> 
8. <span data-ttu-id="9a24a-174">Seleccioneu **Desa i tanca**.</span><span class="sxs-lookup"><span data-stu-id="9a24a-174">Select **Save and close**.</span></span>

![Actualitzar el calendari](./media/13UpdateCalendar.png)

9. <span data-ttu-id="9a24a-176">Aneu a **Configuració** > **Plantilles de calendari** i seleccioneu **Nova**.</span><span class="sxs-lookup"><span data-stu-id="9a24a-176">Go to **Settings** > **Calendar templates** and select **New**.</span></span>
 
 ![Plantilles de calendari](./media/14CalendarTemplates.png)
 
 10. <span data-ttu-id="9a24a-178">Introduïu un nom, seleccioneu el recurs de la plantilla que heu creat i, a continuació, seleccioneu **Desa**.</span><span class="sxs-lookup"><span data-stu-id="9a24a-178">Enter a name, select the template resource you created, and then select **Save**.</span></span> 
 
 ![Desar la plantilla de calendari](./media/15SaveCalendarTemplate.png)
 
 11. <span data-ttu-id="9a24a-180">Aneu a **Paràmetres** i feu doble clic al registre.</span><span class="sxs-lookup"><span data-stu-id="9a24a-180">Go to **Parameters** and double-click the record.</span></span> 
 
 ![Paràmetres del projecte](./media/16ProjectParameters.png)
 
12. <span data-ttu-id="9a24a-182">Actualitzeu els camps següents:</span><span class="sxs-lookup"><span data-stu-id="9a24a-182">Update the following fields:</span></span>

 - <span data-ttu-id="9a24a-183">**Empresa per defecte**: USPM</span><span class="sxs-lookup"><span data-stu-id="9a24a-183">**Default company**: USPM</span></span>
 - <span data-ttu-id="9a24a-184">**Unitat organitzativa per defecte**: Contoso Robotics Global</span><span class="sxs-lookup"><span data-stu-id="9a24a-184">**Default Organizational Unit**: Contoso Robotics Global</span></span>
 - <span data-ttu-id="9a24a-185">**Freqüència de factura**: setè i últim dia</span><span class="sxs-lookup"><span data-stu-id="9a24a-185">**Invoice Frequency**: Seventh and Last day</span></span>
 - <span data-ttu-id="9a24a-186">**Plantilla d'hores de treball**: canvieu-ho a la plantilla que heu creat.</span><span class="sxs-lookup"><span data-stu-id="9a24a-186">**Work hour template**: Change to the template you created.</span></span>

13. <span data-ttu-id="9a24a-187">Seleccioneu **Desa**.</span><span class="sxs-lookup"><span data-stu-id="9a24a-187">Select **Save**.</span></span> 

![Paràmetres del projecte actualitzats](./media/17UpdatedProjectParameters.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
