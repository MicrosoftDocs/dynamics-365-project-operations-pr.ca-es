---
title: Configuració i aplicació de les dades de configuració al Common Data Service
description: En aquest tema es proporciona informació sobre com configurar i aplicar les dades de configuració al Project Operations.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 1651d3b3b85d3dc581bf61976fada249bafd6b7b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289807"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service"></a><span data-ttu-id="7a605-103">Configuració i aplicació de les dades de configuració al Common Data Service</span><span class="sxs-lookup"><span data-stu-id="7a605-103">Set up and apply configuration data in the Common Data Service</span></span> 

<span data-ttu-id="7a605-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_</span><span class="sxs-lookup"><span data-stu-id="7a605-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="7a605-105">Requisits previs</span><span class="sxs-lookup"><span data-stu-id="7a605-105">Prerequisites</span></span>

<span data-ttu-id="7a605-106">Abans de començar a configurar les dades al Common Data Service (CDS), s'han de complir els següents requisits previs:</span><span class="sxs-lookup"><span data-stu-id="7a605-106">Before you beging to configure data in the Common Data Service (CDS), the following prerequisites must be met:</span></span>

1.  <span data-ttu-id="7a605-107">Proveir un entorn del CDS i un entorn del Dynamics 365 Finance per al Project Operations.</span><span class="sxs-lookup"><span data-stu-id="7a605-107">Provision a CDS environment and a Dynamics 365 Finance environment for Project Operations.</span></span>
2.  <span data-ttu-id="7a605-108">La informació de les entitats jurídiques del Dynamics 365 Finance es comparteix a l'entorn del CDS.</span><span class="sxs-lookup"><span data-stu-id="7a605-108">Legal entity information from Dynamics 365 Finance is shared to the CDS environment.</span></span> <span data-ttu-id="7a605-109">Això significa que l'entitat **Empresa** al CDS té els següents registres d'empresa:</span><span class="sxs-lookup"><span data-stu-id="7a605-109">This means that the **Company** entity in CDS has the following company records:</span></span>
  - <span data-ttu-id="7a605-110">THPM</span><span class="sxs-lookup"><span data-stu-id="7a605-110">THPM</span></span>
  - <span data-ttu-id="7a605-111">USPM</span><span class="sxs-lookup"><span data-stu-id="7a605-111">USPM</span></span>
  - <span data-ttu-id="7a605-112">GBPM</span><span class="sxs-lookup"><span data-stu-id="7a605-112">GBPM</span></span>

## <a name="install-setup-and-configuration-data"></a><span data-ttu-id="7a605-113">Configuració de la instal·lació i dades de configuració</span><span class="sxs-lookup"><span data-stu-id="7a605-113">Install setup and configuration data</span></span>

1. <span data-ttu-id="7a605-114">Baixeu, desbloquegeu i descomprimiu el [paquet de dades d'instal·lació i configuració](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span><span class="sxs-lookup"><span data-stu-id="7a605-114">Download, unblock, and unzip the [Setup and Configuration Data Package](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span></span>
2. <span data-ttu-id="7a605-115">Aneu a la carpeta descomprimida i executeu el fitxer executable, *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="7a605-115">Navigate to the unzipped folder and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="7a605-116">A la pàgina 1 de l'auxiliar de configuració de la migració del Common Data Service (CMT), seleccioneu **Importa les dades** i, a continuació, seleccioneu **Continua**.</span><span class="sxs-lookup"><span data-stu-id="7a605-116">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Migració de la configuració](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="7a605-118">A la pàgina 2 de l'auxiliar CMT, seleccioneu **Microsoft 365** com a **Tipus d'implementació**.</span><span class="sxs-lookup"><span data-stu-id="7a605-118">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="7a605-119">Marqueu les caselles **Mostra una llista d'organitzacions disponibles** i **Mostra les opcions avançades**.</span><span class="sxs-lookup"><span data-stu-id="7a605-119">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="7a605-120">Seleccioneu la regió del vostre inquilí, introduïu les credencials i seleccioneu **Inicia la sessió**.</span><span class="sxs-lookup"><span data-stu-id="7a605-120">Select the region of your tenant, enter your credentials, and select **Login**.</span></span>

![Inici de sessió de configuració](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="7a605-122">A la pàgina 3, a la llista d'organitzacions de l'inquilí, seleccioneu l'organització a la qual voleu importar les dades de demostració i feu clic a **Inicia la sessió**.</span><span class="sxs-lookup"><span data-stu-id="7a605-122">On page 3, from the list of organizations on the tenant, select the organization you want to import the demo data into and select **Login**.</span></span>
8. <span data-ttu-id="7a605-123">A la pàgina 4, seleccioneu el fitxer zip *MasterAndSetupData* de la carpeta desempaquetada.</span><span class="sxs-lookup"><span data-stu-id="7a605-123">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder.</span></span>

![Selecció del fitxer ZIP](./media/3ZipFile.png)

![Permet seleccionar un fitxer.](./media/4SelectAFile.png)

9. <span data-ttu-id="7a605-126">Després de seleccionar el fitxer zip, seleccioneu **Importa les dades**.</span><span class="sxs-lookup"><span data-stu-id="7a605-126">After the zip file is selected, select **Import Data**.</span></span>

![Importa les dades](./media/5ImportData.png)

10. <span data-ttu-id="7a605-128">La importació s'executarà durant aproximadament dos-deu minuts en funció de la velocitat de la xarxa.</span><span class="sxs-lookup"><span data-stu-id="7a605-128">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="7a605-129">Després de completar-se la importació, sortiu de l'auxiliar de CMT.</span><span class="sxs-lookup"><span data-stu-id="7a605-129">After import completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="7a605-130">Consulteu a la vostra organització les dades de les següents 19 entitats:</span><span class="sxs-lookup"><span data-stu-id="7a605-130">Check your organization for data in the following 19 entities:</span></span>

  - <span data-ttu-id="7a605-131">Moneda</span><span class="sxs-lookup"><span data-stu-id="7a605-131">Currency</span></span>
  - <span data-ttu-id="7a605-132">Unitat organitzativa</span><span class="sxs-lookup"><span data-stu-id="7a605-132">Organizational Unit</span></span>
  - <span data-ttu-id="7a605-133">Contacte</span><span class="sxs-lookup"><span data-stu-id="7a605-133">Contact</span></span>
  - <span data-ttu-id="7a605-134">Grup d'impostos</span><span class="sxs-lookup"><span data-stu-id="7a605-134">Tax Group</span></span>
  - <span data-ttu-id="7a605-135">Grup de clients</span><span class="sxs-lookup"><span data-stu-id="7a605-135">Customer Group</span></span>
  - <span data-ttu-id="7a605-136">Unit</span><span class="sxs-lookup"><span data-stu-id="7a605-136">Unit</span></span>
  - <span data-ttu-id="7a605-137">Grup d’unitats</span><span class="sxs-lookup"><span data-stu-id="7a605-137">Unit Group</span></span>
  - <span data-ttu-id="7a605-138">Llista de preus</span><span class="sxs-lookup"><span data-stu-id="7a605-138">Price List</span></span>
  - <span data-ttu-id="7a605-139">Llista de preus del paràmetre de projecte</span><span class="sxs-lookup"><span data-stu-id="7a605-139">Project Parameter Price List</span></span>
  - <span data-ttu-id="7a605-140">Freqüència de facturació</span><span class="sxs-lookup"><span data-stu-id="7a605-140">Invoice Frequency</span></span>
  - <span data-ttu-id="7a605-141">Categoria de recursos que es poden reservar</span><span class="sxs-lookup"><span data-stu-id="7a605-141">Bookable Resource Category</span></span>
  - <span data-ttu-id="7a605-142">Categoria de transacció</span><span class="sxs-lookup"><span data-stu-id="7a605-142">Transaction Category</span></span>
  - <span data-ttu-id="7a605-143">Categoria de despesa</span><span class="sxs-lookup"><span data-stu-id="7a605-143">Expense Category</span></span>
  - <span data-ttu-id="7a605-144">Preu per funció</span><span class="sxs-lookup"><span data-stu-id="7a605-144">Role Price</span></span>
  - <span data-ttu-id="7a605-145">Preu de categoria de transacció</span><span class="sxs-lookup"><span data-stu-id="7a605-145">Transaction Category Price</span></span>
  - <span data-ttu-id="7a605-146">Característica</span><span class="sxs-lookup"><span data-stu-id="7a605-146">Characteristic</span></span>
  - <span data-ttu-id="7a605-147">Recurs que es pot reservar</span><span class="sxs-lookup"><span data-stu-id="7a605-147">Bookable Resource</span></span>
  - <span data-ttu-id="7a605-148">Associació de categoria de recursos que es poden reservar</span><span class="sxs-lookup"><span data-stu-id="7a605-148">Bookable resource category Assn</span></span>
  - <span data-ttu-id="7a605-149">Característica dels recursos que es poden reservar</span><span class="sxs-lookup"><span data-stu-id="7a605-149">Bookable Resource Characteristic</span></span>

![Importació completada](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a><span data-ttu-id="7a605-151">Actualitzar les configuracions del Project Operations</span><span class="sxs-lookup"><span data-stu-id="7a605-151">Update Project Operations configurations</span></span>

1. <span data-ttu-id="7a605-152">Navegueu a l'entorn del CE.</span><span class="sxs-lookup"><span data-stu-id="7a605-152">Navigate to the CE environment.</span></span> <span data-ttu-id="7a605-153">Podeu trobar-la obrint el [centre d'administració del Power Platform](https://admin.powerplatform.microsoft.com/environments), seleccionant l'entorn i, a continuació, seleccionant **Obre l'entorn**.</span><span class="sxs-lookup"><span data-stu-id="7a605-153">You can find it by opening the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), selecting the environment, and then selecting **Open Environment**.</span></span> 

![Obrir l'entorn](./media/7OpenEnvironment.png)

2. <span data-ttu-id="7a605-155">Aneu a **Projectes** > **Recursos** i, a continuació, seleccioneu **Nou** per crear un recurs reservable per a l'usuari.</span><span class="sxs-lookup"><span data-stu-id="7a605-155">Go to **Projects** > **Resources** and then select **New** to create a bookable resource for your user.</span></span>

![Recursos que es poden reservar](./media/8BookableResources.png)

3. <span data-ttu-id="7a605-157">A la pestanya **General**, seleccioneu el vostre usuari d'administració.</span><span class="sxs-lookup"><span data-stu-id="7a605-157">On the **General** tab, select your admin user.</span></span> <span data-ttu-id="7a605-158">Verifiqueu que el fus horari coincideixi amb el fus en què us trobeu.</span><span class="sxs-lookup"><span data-stu-id="7a605-158">Verify that the time zone matches the one you are in.</span></span> 

![Nou recurs que es pot reservar](./media/9NewBookableResource.png)

4. <span data-ttu-id="7a605-160">A la pestanya **Planificació**, al camp **Empresa**, trieu l'empresa **USPM** i, a continuació, seleccioneu **Desa**.</span><span class="sxs-lookup"><span data-stu-id="7a605-160">On the **Scheduling** tab, in the **Company** field, pick the **USPM** company, and then select **Save**.</span></span> 

![Pestanya Planificació](./media/10SchedulingTab.png)

5. <span data-ttu-id="7a605-162">Seleccioneu la pestanya **Hores de treball**.</span><span class="sxs-lookup"><span data-stu-id="7a605-162">Select the **Work hours** tab.</span></span>  

![Hores de feina](./media/11WorkHours.png)

6. <span data-ttu-id="7a605-164">Feu doble clic a qualsevol valor del calendari i seleccioneu **Edita** > **Tots els esdeveniments de la sèrie**.</span><span class="sxs-lookup"><span data-stu-id="7a605-164">Double-click on any value in the calendar and select **Edit** > **All events in the series**.</span></span> 

![Calendari de treball](./media/12WorkCalendar.png)

7. <span data-ttu-id="7a605-166">Canvieu les hores de treball a una jornada de treball de vuit (8) hores, marqueu els caps de setmana com a dies inhàbils i assegureu-vos que el fus horari coincideixi amb el vostre.</span><span class="sxs-lookup"><span data-stu-id="7a605-166">Change work hours to an eight (8) hour work day, mark weekends as non-work days, and make sure time zone matches yours.</span></span> 
8. <span data-ttu-id="7a605-167">Seleccioneu **Desa i tanca**.</span><span class="sxs-lookup"><span data-stu-id="7a605-167">Select **Save and close**.</span></span>

![Actualitzar el calendari](./media/13UpdateCalendar.png)

9. <span data-ttu-id="7a605-169">Aneu a **Configuració** > **Plantilles de calendari** i seleccioneu **Nova**.</span><span class="sxs-lookup"><span data-stu-id="7a605-169">Go to **Settings** > **Calendar templates** and select **New**.</span></span>
 
 ![Plantilles de calendari](./media/14CalendarTemplates.png)
 
 10. <span data-ttu-id="7a605-171">Introduïu un nom, seleccioneu el recurs de la plantilla que heu creat i, a continuació, seleccioneu **Desa**.</span><span class="sxs-lookup"><span data-stu-id="7a605-171">Enter a name, select the template resource you created, and then select **Save**.</span></span> 
 
 ![Desar la plantilla de calendari](./media/15SaveCalendarTemplate.png)
 
 11. <span data-ttu-id="7a605-173">Aneu a **Paràmetres** i feu doble clic al registre.</span><span class="sxs-lookup"><span data-stu-id="7a605-173">Go to **Parameters** and double-click the record.</span></span> 
 
 ![Paràmetres del projecte](./media/16ProjectParameters.png)
 
12. <span data-ttu-id="7a605-175">Actualitzeu els camps següents:</span><span class="sxs-lookup"><span data-stu-id="7a605-175">Update the following fields:</span></span>

 - <span data-ttu-id="7a605-176">**Empresa per defecte**: USPM</span><span class="sxs-lookup"><span data-stu-id="7a605-176">**Default company**: USPM</span></span>
 - <span data-ttu-id="7a605-177">**Unitat organitzativa per defecte**: Contoso Robotics Global</span><span class="sxs-lookup"><span data-stu-id="7a605-177">**Default Organizational Unit**: Contoso Robotics Global</span></span>
 - <span data-ttu-id="7a605-178">**Freqüència de factura**: setè i últim dia</span><span class="sxs-lookup"><span data-stu-id="7a605-178">**Invoice Frequency**: Seventh and Last day</span></span>
 - <span data-ttu-id="7a605-179">**Plantilla d'hores de treball**: canvieu-ho a la plantilla que heu creat.</span><span class="sxs-lookup"><span data-stu-id="7a605-179">**Work hour template**: Change to the template you created.</span></span>

13. <span data-ttu-id="7a605-180">Seleccioneu **Desa**.</span><span class="sxs-lookup"><span data-stu-id="7a605-180">Select **Save**.</span></span> 

![Paràmetres del projecte actualitzats](./media/17UpdatedProjectParameters.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]