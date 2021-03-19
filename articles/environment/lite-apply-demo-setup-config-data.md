---
title: Aplicació de la configuració de la demostració i les dades de configuració (bàsic)
description: En aquest tema es proporciona informació sobre com aplicar la configuració de la demostració i les dades de configuració per al Project Operations.
author: sigitac
manager: Annbe
ms.date: 01/27/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 694dbc74591de74895095a9da6e590069711fc83
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290122"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a><span data-ttu-id="10bd6-103">Aplicació de la configuració de la demostració i les dades de configuració per al Project Operations (bàsic)</span><span class="sxs-lookup"><span data-stu-id="10bd6-103">Apply demo setup and configuration data for Project Operations - lite</span></span> 

<span data-ttu-id="10bd6-104">_\*\*Implementació bàsica: acord a facturació proforma_</span><span class="sxs-lookup"><span data-stu-id="10bd6-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="10bd6-105">Requisits previs</span><span class="sxs-lookup"><span data-stu-id="10bd6-105">Prerequisites</span></span>

<span data-ttu-id="10bd6-106">Abans de començar la configuració, heu de tenir un entorn del Common Data Service (CDS) proveït per al Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="10bd6-106">Before you begin the configuration, you must have a Common Data Service (CDS) environment provisioned for Dynamics 365 Project Operations.</span></span>


## <a name="instructions"></a><span data-ttu-id="10bd6-107">Instruccions</span><span class="sxs-lookup"><span data-stu-id="10bd6-107">Instructions</span></span>

1. <span data-ttu-id="10bd6-108">Baixeu el [paquet de dades mestres](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span><span class="sxs-lookup"><span data-stu-id="10bd6-108">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span></span> 
2. <span data-ttu-id="10bd6-109">Aneu a la carpeta *ProjOpsDemoDataSetupAndMaster - Integrated CMT* i executeu el fitxer executable, *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="10bd6-109">Navigate to the folder *ProjOpsDemoDataSetupAndMaster - Integrated CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="10bd6-110">A la pàgina 1 de l'auxiliar de configuració de la migració del Common Data Service (CMT), seleccioneu **Importa les dades** i, a continuació, seleccioneu **Continua**.</span><span class="sxs-lookup"><span data-stu-id="10bd6-110">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

    ![Migració de la configuració](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="10bd6-112">A la pàgina 2 de l'auxiliar CMT, seleccioneu **Microsoft 365** com a **Tipus d'implementació**.</span><span class="sxs-lookup"><span data-stu-id="10bd6-112">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="10bd6-113">Marqueu les caselles **Mostra una llista d'organitzacions disponibles** i **Mostra les opcions avançades**.</span><span class="sxs-lookup"><span data-stu-id="10bd6-113">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="10bd6-114">Seleccioneu la regió del vostre inquilí, introduïu les credencials i, a continuació, seleccioneu **Inicia la sessió**.</span><span class="sxs-lookup"><span data-stu-id="10bd6-114">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

   ![Inici de sessió de configuració](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="10bd6-116">A la pàgina 3, a la llista d'organitzacions de l'inquilí, seleccioneu l'organització a la qual voleu importar les dades de demostració i, a continuació, feu clic a **Inicia la sessió**.</span><span class="sxs-lookup"><span data-stu-id="10bd6-116">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="10bd6-117">A la pàgina 4, seleccioneu el fitxer zip *MasterAndSetupData* de la carpeta desempaquetada, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span><span class="sxs-lookup"><span data-stu-id="10bd6-117">On page 4, select the zip file, *MasterAndSetupData* from the unpacked folder, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span></span>

   ![Fitxer zip](./media/3ZipFile.png)

   ![Permet seleccionar un fitxer.](./media/4SelectAFile.png)

9. <span data-ttu-id="10bd6-120">Després de seleccionar el fitxer zip, seleccioneu **Importa les dades**.</span><span class="sxs-lookup"><span data-stu-id="10bd6-120">After the zip file is selected, select **Import Data**.</span></span>

   ![Importa dades](./media/5ImportData.png)

10. <span data-ttu-id="10bd6-122">La importació s'executarà durant aproximadament dos-deu minuts en funció de la velocitat de la xarxa.</span><span class="sxs-lookup"><span data-stu-id="10bd6-122">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="10bd6-123">Després de completar-se, sortiu de l'auxiliar de CMT.</span><span class="sxs-lookup"><span data-stu-id="10bd6-123">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="10bd6-124">Consulteu a la vostra organització les dades de les següents 20 entitats:</span><span class="sxs-lookup"><span data-stu-id="10bd6-124">Check your organization for data in the following 20 entities:</span></span>

    -   <span data-ttu-id="10bd6-125">Moneda</span><span class="sxs-lookup"><span data-stu-id="10bd6-125">Currency</span></span>
    -   <span data-ttu-id="10bd6-126">Compte</span><span class="sxs-lookup"><span data-stu-id="10bd6-126">Account</span></span>
    -   <span data-ttu-id="10bd6-127">Unitat organitzativa</span><span class="sxs-lookup"><span data-stu-id="10bd6-127">Organizational Unit</span></span>
    -   <span data-ttu-id="10bd6-128">Contacte</span><span class="sxs-lookup"><span data-stu-id="10bd6-128">Contact</span></span>
    -   <span data-ttu-id="10bd6-129">Unitat</span><span class="sxs-lookup"><span data-stu-id="10bd6-129">Unit</span></span>
    -   <span data-ttu-id="10bd6-130">Grup d’unitats</span><span class="sxs-lookup"><span data-stu-id="10bd6-130">Unit Group</span></span>
    -   <span data-ttu-id="10bd6-131">Llista de preus</span><span class="sxs-lookup"><span data-stu-id="10bd6-131">Price List</span></span>
    -   <span data-ttu-id="10bd6-132">Llista de preus del paràmetre de projecte</span><span class="sxs-lookup"><span data-stu-id="10bd6-132">Project Parameter Price List</span></span> 
    -   <span data-ttu-id="10bd6-133">Freqüència de facturació</span><span class="sxs-lookup"><span data-stu-id="10bd6-133">Invoice Frequency</span></span>
    -   <span data-ttu-id="10bd6-134">Categoria de recursos que es poden reservar</span><span class="sxs-lookup"><span data-stu-id="10bd6-134">Bookable Resource Category</span></span>
    -   <span data-ttu-id="10bd6-135">Categoria de transacció</span><span class="sxs-lookup"><span data-stu-id="10bd6-135">Transaction Category</span></span>
    -   <span data-ttu-id="10bd6-136">Categoria de despesa</span><span class="sxs-lookup"><span data-stu-id="10bd6-136">Expense Category</span></span>
    -   <span data-ttu-id="10bd6-137">Preu per funció</span><span class="sxs-lookup"><span data-stu-id="10bd6-137">Role Price</span></span>
    -   <span data-ttu-id="10bd6-138">Preu de categoria de transacció</span><span class="sxs-lookup"><span data-stu-id="10bd6-138">Transaction Category Price</span></span>
    -   <span data-ttu-id="10bd6-139">Característica</span><span class="sxs-lookup"><span data-stu-id="10bd6-139">Characteristic</span></span>
    -   <span data-ttu-id="10bd6-140">Recurs que es pot reservar</span><span class="sxs-lookup"><span data-stu-id="10bd6-140">Bookable Resource</span></span>
    -   <span data-ttu-id="10bd6-141">Associació de categoria de recursos que es poden reservar</span><span class="sxs-lookup"><span data-stu-id="10bd6-141">Bookable resource category Assn</span></span>
    -   <span data-ttu-id="10bd6-142">Característica dels recursos que es poden reservar</span><span class="sxs-lookup"><span data-stu-id="10bd6-142">Bookable Resource Characteristic</span></span>

    ![Importació completada](./media/6CompleteImport.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]