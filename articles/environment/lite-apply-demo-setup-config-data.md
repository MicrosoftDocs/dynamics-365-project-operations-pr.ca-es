---
title: Aplicació de la configuració de la demostració i les dades de configuració
description: En aquest tema es proporciona informació sobre com aplicar la configuració de la demostració i les dades de configuració per al Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 42e02f393e89d20b2a462645f519a3792bee8f2f
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948757"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations-lite-deployment---deal-to-proforma-invoicing"></a><span data-ttu-id="a2b59-103">Aplicar la configuració de demostració i les dades de configuració per a la implementació bàsica del Project Operations: acord a la facturació proforma</span><span class="sxs-lookup"><span data-stu-id="a2b59-103">Apply demo setup and configuration data for Project Operations lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="a2b59-104">_\*\*Implementació bàsica: acord a facturació proforma_</span><span class="sxs-lookup"><span data-stu-id="a2b59-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

1. <span data-ttu-id="a2b59-105">Baixeu el [paquet de dades mestres](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span><span class="sxs-lookup"><span data-stu-id="a2b59-105">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span></span> 
2. <span data-ttu-id="a2b59-106">Aneu a la carpeta *ProjOpsDemoDataSetupAndMaster - Integrated CMT* i executeu el fitxer executable, *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="a2b59-106">Navigate to the folder *ProjOpsDemoDataSetupAndMaster - Integrated CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="a2b59-107">A la pàgina 1 de l'auxiliar de configuració de la migració del Common Data Service (CMT), seleccioneu **Importa les dades** i, a continuació, seleccioneu **Continua**.</span><span class="sxs-lookup"><span data-stu-id="a2b59-107">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Migració de la configuració](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="a2b59-109">A la pàgina 2 de l'auxiliar CMT, seleccioneu **Office 365** com a **Tipus d'implementació**.</span><span class="sxs-lookup"><span data-stu-id="a2b59-109">On Page 2 of the CMT Wizard, select **Office 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="a2b59-110">Marqueu les caselles **Mostra una llista d'organitzacions disponibles** i **Mostra les opcions avançades**.</span><span class="sxs-lookup"><span data-stu-id="a2b59-110">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="a2b59-111">Seleccioneu la regió del vostre inquilí, introduïu les credencials i, a continuació, seleccioneu **Inicia la sessió**.</span><span class="sxs-lookup"><span data-stu-id="a2b59-111">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

![Inici de sessió de configuració](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="a2b59-113">A la pàgina 3, a la llista d'organitzacions de l'inquilí, seleccioneu l'organització a la qual voleu importar les dades de demostració i, a continuació, feu clic a **Inicia la sessió**.</span><span class="sxs-lookup"><span data-stu-id="a2b59-113">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="a2b59-114">A la pàgina 4, seleccioneu el fitxer zip *MasterAndSetupData* de la carpeta desempaquetada, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span><span class="sxs-lookup"><span data-stu-id="a2b59-114">On page 4, select the zip file, *MasterAndSetupData* from the unpacked folder, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span></span>

![Fitxer zip](./media/3ZipFile.png)

![Permet seleccionar un fitxer.](./media/4SelectAFile.png)

9. <span data-ttu-id="a2b59-117">Després de seleccionar el fitxer zip, seleccioneu **Importa les dades**.</span><span class="sxs-lookup"><span data-stu-id="a2b59-117">After the zip file is selected, select **Import Data**.</span></span>

![Importa dades](./media/5ImportData.png)

10. <span data-ttu-id="a2b59-119">La importació s'executarà durant aproximadament dos-deu minuts en funció de la velocitat de la xarxa.</span><span class="sxs-lookup"><span data-stu-id="a2b59-119">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="a2b59-120">Després de completar-se, sortiu de l'auxiliar de CMT.</span><span class="sxs-lookup"><span data-stu-id="a2b59-120">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="a2b59-121">Consulteu a la vostra organització les dades de les següents 20 entitats:</span><span class="sxs-lookup"><span data-stu-id="a2b59-121">Check your organization for data in the following 20 entities:</span></span>

- <span data-ttu-id="a2b59-122">Moneda</span><span class="sxs-lookup"><span data-stu-id="a2b59-122">Currency</span></span>
- <span data-ttu-id="a2b59-123">Unitat organitzativa</span><span class="sxs-lookup"><span data-stu-id="a2b59-123">Organizational Unit</span></span>
- <span data-ttu-id="a2b59-124">Contacte</span><span class="sxs-lookup"><span data-stu-id="a2b59-124">Contact</span></span>
- <span data-ttu-id="a2b59-125">Grup d'impostos</span><span class="sxs-lookup"><span data-stu-id="a2b59-125">Tax Group</span></span>
- <span data-ttu-id="a2b59-126">Grup de clients</span><span class="sxs-lookup"><span data-stu-id="a2b59-126">Customer Group</span></span>
- <span data-ttu-id="a2b59-127">Unit</span><span class="sxs-lookup"><span data-stu-id="a2b59-127">Unit</span></span>
- <span data-ttu-id="a2b59-128">Grup d’unitats</span><span class="sxs-lookup"><span data-stu-id="a2b59-128">Unit Group</span></span>
- <span data-ttu-id="a2b59-129">Llista de preus</span><span class="sxs-lookup"><span data-stu-id="a2b59-129">Price List</span></span>
- <span data-ttu-id="a2b59-130">Llista de preus del paràmetre de projecte</span><span class="sxs-lookup"><span data-stu-id="a2b59-130">Project Parameter Price List</span></span>
- <span data-ttu-id="a2b59-131">Freqüència de facturació</span><span class="sxs-lookup"><span data-stu-id="a2b59-131">Invoice Frequency</span></span>
- <span data-ttu-id="a2b59-132">Detall de la freqüència de facturació</span><span class="sxs-lookup"><span data-stu-id="a2b59-132">Invoice Frequency Detail</span></span>
- <span data-ttu-id="a2b59-133">Categoria de recursos que es poden reservar</span><span class="sxs-lookup"><span data-stu-id="a2b59-133">Bookable Resource Category</span></span>
- <span data-ttu-id="a2b59-134">Categoria de transacció</span><span class="sxs-lookup"><span data-stu-id="a2b59-134">Transaction Category</span></span>
- <span data-ttu-id="a2b59-135">Categoria de despesa</span><span class="sxs-lookup"><span data-stu-id="a2b59-135">Expense Category</span></span>
- <span data-ttu-id="a2b59-136">Preu per funció</span><span class="sxs-lookup"><span data-stu-id="a2b59-136">Role Price</span></span>
- <span data-ttu-id="a2b59-137">Preu de categoria de transacció</span><span class="sxs-lookup"><span data-stu-id="a2b59-137">Transaction Category Price</span></span>
- <span data-ttu-id="a2b59-138">Característica</span><span class="sxs-lookup"><span data-stu-id="a2b59-138">Characteristic</span></span>
- <span data-ttu-id="a2b59-139">Recurs que es pot reservar</span><span class="sxs-lookup"><span data-stu-id="a2b59-139">Bookable Resource</span></span>
- <span data-ttu-id="a2b59-140">Associació de categoria de recursos que es poden reservar</span><span class="sxs-lookup"><span data-stu-id="a2b59-140">Bookable resource category Assn</span></span>
- <span data-ttu-id="a2b59-141">Característica dels recursos que es poden reservar</span><span class="sxs-lookup"><span data-stu-id="a2b59-141">Bookable Resource Characteristic</span></span>

![Importació completada](./media/6CompleteImport.png)
