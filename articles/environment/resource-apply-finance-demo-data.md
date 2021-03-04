---
title: Aplicació de les dades de demostració en un entorn allotjat al núvol del Finance
description: En aquest tema s'explica com aplicar les dades de demostració del Project Operations en un entorn del Dynamics 365 Finance allotjat al núvol.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a7cdbd2847ce45972aadd0d1a2d4f26270727ad9
ms.sourcegitcommit: d33ef0ae39f90fe3b0f6b4524f483e8052057361
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 11/03/2020
ms.locfileid: "4365226"
---
# <a name="apply-demo-data-to-a-finance-cloud-hosted-environment"></a>Aplicació de les dades de demostració en un entorn allotjat al núvol del Finance

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

> [!IMPORTANT]
> Aquest tema només és aplicable només a la versió 10.0.13 del Microsoft Dynamics 365 Finance i només es pot fer en un entorn allotjat al núvol. Completeu els passos d'aquest tema **ABANS** d'aplicar les actualitzacions de qualitat a l'entorn.

1. Al projecte del LCS, obriu la pàgina **Detalls de l'entorn**. Observeu que inclou els detalls necessaris per connectar-se a l'entorn mitjançant el protocol d'escriptori remot (RDP).

![Detalls de l'entorn del ](./media/1EnvironmentDetails.png)

El primer conjunt de credencials ressaltades són les credencials del compte local i contenen un enllaç a la connexió d'escriptori remot. Les credencials inclouen el nom d'usuari i la contrasenya d'administrador de l'entorn. El segon conjunt de credencials s'utilitza per iniciar la sessió a l'SQL Server en aquest entorn.

2. Connecteu-vos a l'entorn amb l'enllaç a **Comptes locals** i utilitzeu les **Credencials del compte local** per autenticar-vos.
3. Aneu **Serveis d'informació d'Internet** > **Grups d'aplicacions** > **AOSService** i atureu el servei. Atureu el servei en aquest punt perquè pugueu continuar reemplaçant la base de dades de l'SQL.

![Aturar l'AOS](./media/2StopAOS.png)

4. Aneu a **Serveis** i atureu els dos elements següents:

- Microsoft Dynamics 365 Unified Operations: servei d'administració de lots
- Microsoft Dynamics 365 Unified Operations: marc d'importació i exportació de dades

![Aturar els serveis](./media/3StopServices.png)

5. Obriu Microsoft SQL Server Management Studio. Inicieu sessió amb les credencials de l'SQL Server i utilitzeu l'usuari axdbadmin i la contrasenya de la pàgina **Detalls de l'entorn** del LCS.

![SQL Server Management Studio](./media/4SSMS.png)

6. A l'Explorador d'objectes, **Bases de dades** i localitzeu **AXDB**. Substituireu la base de dades per una base de dades nova que es troba al [Centre de baixades](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip). 
7. Copieu el fitxer zip a la VM a la que heu accedit remotament i extraieu el contingut del fitxer zip.
8. A l'SQL Server Management Studio, feu clic amb el botó dret a **AXDB** i, a continuació, seleccioneu **Tasques** > **Restaura** > **Base de dades**.

![Restaurar la base de dades](./media/5RestoreDatabase.png)

9. Seleccioneu **Dispositiu d'origen** i navegueu al fitxer extret del zip que heu copiat.

![Dispositius d'origen](./media/6SourceDevice.png)

10. Seleccioneu **Opcions** i, a continuació, **Substitueix la base de dades existent** i **Tanca les connexions existents a la base de dades de destinació**. 
11. Seleccioneu **D'acord**.

![Restaurar la configuració](./media/7RestoreSetting.png)

Rebreu la confirmació que la restauració de l'AXDB s'ha realitzat correctament. Després de rebre aquesta confirmació, podeu tancar l'SQL Services Management Studio.

12. Torneu a **Serveis d'informació d'Internet** > **Grups d'aplicacions** > **AOSService** i inicieu el servei AOSService.
13. Aneu a **Serveis** i inicieu els dos serveis que heu aturat abans.

14. Localitzeu l'eina AdminUserProvisioning en aquesta VM. Cerqueu a K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.
15. Executeu el fitxer .ext amb l'adreça de l'usuari al camp **Adreça electrònica**. 
16. Seleccioneu **Envia**.

![Proveïment de l'usuari administrador](./media/8AdminUserProvisioning.png)

Això tarda parell de minuts a completar-se. Rebreu un missatge de confirmació indicant que s'ha actualitzat l'usuari d'administració correctament.

17. Finalment, executeu l'indicador d'ordres com a administrador i realitzeu iisreset

![IIS Reset](./media/9IISReset.png)

18. Tanqueu la sessió d'escriptori remot i utilitzeu la pàgina **Detalls de l'entorn** del LCS per iniciar la sessió a l'entorn per confirmar que està funcionant de la manera esperada.

![Finance and Operations](./media/10FinanceAndOperations.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]