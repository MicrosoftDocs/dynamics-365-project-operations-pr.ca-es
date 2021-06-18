---
title: Aplicació de les dades de demostració en un entorn allotjat al núvol del Finance
description: En aquest tema s'explica com aplicar les dades de demostració del Project Operations en un entorn del Dynamics 365 Finance allotjat al núvol.
author: sigitac
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7d8a198b3bfd71ae08bc338d17896519b5ffd6b8
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000138"
---
# <a name="apply-demo-data-to-a-finance-cloud-hosted-environment"></a><span data-ttu-id="81b9c-103">Aplicació de les dades de demostració en un entorn allotjat al núvol del Finance</span><span class="sxs-lookup"><span data-stu-id="81b9c-103">Apply demo data to a Finance Cloud-hosted environment</span></span>

<span data-ttu-id="81b9c-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_</span><span class="sxs-lookup"><span data-stu-id="81b9c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="81b9c-105">Aquest tema només és aplicable només a la versió 10.0.13 del Microsoft Dynamics 365 Finance i només es pot fer en un entorn allotjat al núvol.</span><span class="sxs-lookup"><span data-stu-id="81b9c-105">This topic is only applicable only Microsoft Dynamics 365 Finance version 10.0.13 and can be performed only on a Cloud-hosted environment.</span></span> <span data-ttu-id="81b9c-106">Completeu els passos d'aquest tema **ABANS** d'aplicar les actualitzacions de qualitat a l'entorn.</span><span class="sxs-lookup"><span data-stu-id="81b9c-106">Complete the steps in this topic **BEFORE** you apply quality updates to the environment.</span></span>

1. <span data-ttu-id="81b9c-107">Al projecte del LCS, obriu la pàgina **Detalls de l'entorn**.</span><span class="sxs-lookup"><span data-stu-id="81b9c-107">In your LCS project, open the **Environment details** page.</span></span> <span data-ttu-id="81b9c-108">Observeu que inclou els detalls necessaris per connectar-se a l'entorn mitjançant el protocol d'escriptori remot (RDP).</span><span class="sxs-lookup"><span data-stu-id="81b9c-108">Notice that it includes the details needed to connect to the environment by using Remote Desktop Protocol (RDP).</span></span>

![Detalls de l'entorn del ](./media/1EnvironmentDetails.png)

<span data-ttu-id="81b9c-110">El primer conjunt de credencials ressaltades són les credencials del compte local i contenen un enllaç a la connexió d'escriptori remot.</span><span class="sxs-lookup"><span data-stu-id="81b9c-110">The first set of highlighted credentials are the local account credentials and contain a hyperlink to the remote desktop connection.</span></span> <span data-ttu-id="81b9c-111">Les credencials inclouen el nom d'usuari i la contrasenya d'administrador de l'entorn.</span><span class="sxs-lookup"><span data-stu-id="81b9c-111">The credentials include the environment admin username and password.</span></span> <span data-ttu-id="81b9c-112">El segon conjunt de credencials s'utilitza per iniciar la sessió a l'SQL Server en aquest entorn.</span><span class="sxs-lookup"><span data-stu-id="81b9c-112">The second set of credentials are used to log in to SQL Server in this environment.</span></span>

2. <span data-ttu-id="81b9c-113">Connecteu-vos a l'entorn amb l'enllaç a **Comptes locals** i utilitzeu les **Credencials del compte local** per autenticar-vos.</span><span class="sxs-lookup"><span data-stu-id="81b9c-113">Remote to the environment by the hyperlink in **Local Accounts**, and use the **Local Account credentials** to authenticate.</span></span>
3. <span data-ttu-id="81b9c-114">Aneu **Serveis d'informació d'Internet** > **Grups d'aplicacions** > **AOSService** i atureu el servei.</span><span class="sxs-lookup"><span data-stu-id="81b9c-114">Go to **Internet Information Services** > **Application Pools** > **AOSService** and stop the service.</span></span> <span data-ttu-id="81b9c-115">Atureu el servei en aquest punt perquè pugueu continuar reemplaçant la base de dades de l'SQL.</span><span class="sxs-lookup"><span data-stu-id="81b9c-115">You are stopping the service at this point so that you can continue to replace the SQL database.</span></span>

![Aturar l'AOS](./media/2StopAOS.png)

4. <span data-ttu-id="81b9c-117">Aneu a **Serveis** i atureu els dos elements següents:</span><span class="sxs-lookup"><span data-stu-id="81b9c-117">Go to **Services** and stop the following two items:</span></span>

- <span data-ttu-id="81b9c-118">Microsoft Dynamics 365 Unified Operations: servei d'administració de lots</span><span class="sxs-lookup"><span data-stu-id="81b9c-118">Microsoft Dynamics 365 Unified Operations: Batch Management Service</span></span>
- <span data-ttu-id="81b9c-119">Microsoft Dynamics 365 Unified Operations: marc d'importació i exportació de dades</span><span class="sxs-lookup"><span data-stu-id="81b9c-119">Microsoft Dynamics 365 Unified Operations: Data Import Export Framework</span></span>

![Aturar els serveis](./media/3StopServices.png)

5. <span data-ttu-id="81b9c-121">Obriu Microsoft SQL Server Management Studio.</span><span class="sxs-lookup"><span data-stu-id="81b9c-121">Open Microsoft SQL Server Management Studio.</span></span> <span data-ttu-id="81b9c-122">Inicieu sessió amb les credencials de l'SQL Server i utilitzeu l'usuari axdbadmin i la contrasenya de la pàgina **Detalls de l'entorn** del LCS.</span><span class="sxs-lookup"><span data-stu-id="81b9c-122">Log in with SQL server credentials and use the axdbadmin user and password from the LCS **Environments details** page.</span></span>

![SQL Server Management Studio](./media/4SSMS.png)

6. <span data-ttu-id="81b9c-124">A l'Explorador d'objectes, **Bases de dades** i localitzeu **AXDB**.</span><span class="sxs-lookup"><span data-stu-id="81b9c-124">In Object Explorer, **Databases** and locate **AXDB**.</span></span> <span data-ttu-id="81b9c-125">Substituireu la base de dades per una base de dades nova que es troba al [Centre de baixades](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip).</span><span class="sxs-lookup"><span data-stu-id="81b9c-125">You will replace database with a new database that is located in the [Download Center](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip).</span></span> 
7. <span data-ttu-id="81b9c-126">Copieu el fitxer zip a la VM a la que heu accedit remotament i extraieu el contingut del fitxer zip.</span><span class="sxs-lookup"><span data-stu-id="81b9c-126">Copy the zip file to the VM you are remoted into and extract zip contents.</span></span>
8. <span data-ttu-id="81b9c-127">A l'SQL Server Management Studio, feu clic amb el botó dret a **AXDB** i, a continuació, seleccioneu **Tasques** > **Restaura** > **Base de dades**.</span><span class="sxs-lookup"><span data-stu-id="81b9c-127">In SQL Server Management Studio, right-click **AxDB**, and then select **Tasks** > **Restore** > **Database**.</span></span>

![Restaurar la base de dades](./media/5RestoreDatabase.png)

9. <span data-ttu-id="81b9c-129">Seleccioneu **Dispositiu d'origen** i navegueu al fitxer extret del zip que heu copiat.</span><span class="sxs-lookup"><span data-stu-id="81b9c-129">Select **Source Device** and navigate to the file extracted from zip you copied.</span></span>

![Dispositius d'origen](./media/6SourceDevice.png)

10. <span data-ttu-id="81b9c-131">Seleccioneu **Opcions** i, a continuació, **Substitueix la base de dades existent** i **Tanca les connexions existents a la base de dades de destinació**.</span><span class="sxs-lookup"><span data-stu-id="81b9c-131">Select **Options**, and then select **Overwrite the existing database** and **Close existing connections to destination database**.</span></span> 
11. <span data-ttu-id="81b9c-132">Seleccioneu **D'acord**.</span><span class="sxs-lookup"><span data-stu-id="81b9c-132">Select **OK**.</span></span>

![Restaurar la configuració](./media/7RestoreSetting.png)

<span data-ttu-id="81b9c-134">Rebreu la confirmació que la restauració de l'AXDB s'ha realitzat correctament.</span><span class="sxs-lookup"><span data-stu-id="81b9c-134">You will receive confirmation that the AXDB restore was successful.</span></span> <span data-ttu-id="81b9c-135">Després de rebre aquesta confirmació, podeu tancar l'SQL Services Management Studio.</span><span class="sxs-lookup"><span data-stu-id="81b9c-135">After you receive this confirmation, you can close SQL Services Management Studio.</span></span>

12. <span data-ttu-id="81b9c-136">Torneu a **Serveis d'informació d'Internet** > **Grups d'aplicacions** > **AOSService** i inicieu el servei AOSService.</span><span class="sxs-lookup"><span data-stu-id="81b9c-136">Go back to **Internet Information Services** > **Application Pools** > **AOSService** and start the AOSService.</span></span>
13. <span data-ttu-id="81b9c-137">Aneu a **Serveis** i inicieu els dos serveis que heu aturat abans.</span><span class="sxs-lookup"><span data-stu-id="81b9c-137">Go to **Services** and start the two services you stopped earlier.</span></span>

14. <span data-ttu-id="81b9c-138">Localitzeu l'eina AdminUserProvisioning en aquesta VM.</span><span class="sxs-lookup"><span data-stu-id="81b9c-138">Locate the AdminUserProvisioning tool on this VM.</span></span> <span data-ttu-id="81b9c-139">Cerqueu a K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.</span><span class="sxs-lookup"><span data-stu-id="81b9c-139">Look under, K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.</span></span>
15. <span data-ttu-id="81b9c-140">Executeu el fitxer .ext amb l'adreça de l'usuari al camp **Adreça electrònica**.</span><span class="sxs-lookup"><span data-stu-id="81b9c-140">Run the .ext file using your user address in the **Email Address** field.</span></span> 
16. <span data-ttu-id="81b9c-141">Seleccioneu **Envia**.</span><span class="sxs-lookup"><span data-stu-id="81b9c-141">Select **Submit**.</span></span>

![Proveïment de l'usuari administrador](./media/8AdminUserProvisioning.png)

<span data-ttu-id="81b9c-143">Això tarda parell de minuts a completar-se.</span><span class="sxs-lookup"><span data-stu-id="81b9c-143">This takes a couple of minutes to complete.</span></span> <span data-ttu-id="81b9c-144">Rebreu un missatge de confirmació indicant que s'ha actualitzat l'usuari d'administració correctament.</span><span class="sxs-lookup"><span data-stu-id="81b9c-144">You should receive a confirmation message that the Admin user was successfully updated.</span></span>

17. <span data-ttu-id="81b9c-145">Finalment, executeu l'indicador d'ordres com a administrador i realitzeu iisreset</span><span class="sxs-lookup"><span data-stu-id="81b9c-145">Lastly, run Command Prompt as Administrator and perform iisreset</span></span>

![IIS Reset](./media/9IISReset.png)

18. <span data-ttu-id="81b9c-147">Tanqueu la sessió d'escriptori remot i utilitzeu la pàgina **Detalls de l'entorn** del LCS per iniciar la sessió a l'entorn per confirmar que està funcionant de la manera esperada.</span><span class="sxs-lookup"><span data-stu-id="81b9c-147">Close the remote desktop session and use the LCS **Environment details** page to log in to the environment to confirm it is working as expected.</span></span>

![Finance and Operations](./media/10FinanceAndOperations.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]