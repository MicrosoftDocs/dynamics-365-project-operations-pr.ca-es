---
title: Integració del Microsoft Project Client
description: La planificació i el manteniment d'una planificació de projecte poden ser complexos, de manera que els administradors de projectes han d'utilitzar eines que els ajudin a administrar aquesta tasca. La integració amb el Microsoft Project Client proporciona suport per obrir i administrar una estructura de desglossament del treball del projecte.
author: Yowelle
ms.date: 06/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 8ef34bc984510f23ab77cc1710c06abbcf80f721703685d696fea28eeaddd732
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6988009"
---
# <a name="microsoft-project-client-integration"></a>Integració del Microsoft Project Client

[!include [banner](../includes/banner.md)]

La planificació i el manteniment d'una planificació de projecte poden ser complexos, de manera que els administradors de projectes han d'utilitzar eines que els ajudin a administrar aquesta tasca. La integració amb el Microsoft Project Client proporciona suport per obrir i administrar una estructura de desglossament del treball del projecte. L'administrador del projecte pot publicar qualsevol canvi a l'estructura del desglossament del treball del projecte del Dynamics 365 Finance.

> [!NOTE]
> Si utilitzeu l'actualització de juliol (versió 10.0.4), heu d'instal·lar els KB 4054797 i el 4055884.

## <a name="configure-the-microsoft-project-client-add-in"></a>Configurar el complement del Microsoft Project Client
Per habilitar la integració amb el Microsoft Project Client, cal que s'instal·li un complement del Microsoft Dynamics 365 a l'aplicació client del Microsoft Project de l'usuari. Això es fa obrint l'**àrea de treball Administració de projectes**.

• Feu clic a **Configura el complement de client del Project** des de la secció **Enllaços** > **Configuració** de l'àrea de treball.

• Feu clic a **Obre** i, a continuació, feu clic a **Executa** quan se us demani.

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a>Obrir i editar una estructura de desglossament del treball existent d'esborrany al Microsoft Project Client
Si un projecte del Dynamics 365 Finance ja té una estructura de desglossament del treball creada, l'estructura del desglossament del treball es pot obrir a l'aplicació Microsoft Project Client si l'estructura del desglossament del treball està en un estat d'esborrany. Per obrir-la des de la pàgina **Projecte**, feu clic a l'enllaç **Obre al Microsoft Project** des de la pestanya **Pla**. Aquesta pàgina també es pot obrir des de l'aplicació Microsoft Project Client fent clic a **Obre** la pestanya **Microsoft Dynamics 365**. Seleccioneu una **Entitat jurídica** i **Projecte** de la llista.

> [!NOTE]
> Si utilitzeu l'Internet Explorer com a navegador, haureu de fer clic a **Desa** per obrir manualment la ubicació a la qual es descarrega el fitxer. O bé, feu clic a **Desa i obre** per obrir el fitxer Microsoft Project Client. No canvieu el nom del fitxer en desar-lo.

Abans de fer cap modificació al fitxer amb el Microsoft Project Client, heu de desprotegir-lo. Feu clic **Desprotegeix** a la pestanya **Microsoft Dynamics 365**. Això evitarà que altres usuaris editin l'estructura del desglossament del treball des del Finance al mateix temps. Per publicar l'estructura del desglossament de la feina després d'haver completat les edicions, feu clic **Protegeix** a la pestanya **Microsoft Dynamics 365**.

Si un equip del projecte ja s'ha afegit al projecte al Finance, la llista de recursos s'emplenarà amb els membres de l'equip. Si encara no s'ha afegit un equip del projecte al projecte, podeu seleccionar recursos i crear l'equip al Microsoft Project Client fent clic al botó **Recursos** de la pestanya **Microsoft Dynamics 365**. 

Les dades següents se sincronitzen de nou al Finance com a part del procés de desprotecció:

• Nom de la tasca

• Data d'inici

• Data de finalització

• Predecessors

• Noms dels recursos

• Categoria

• Categoria del recurs

• Hores de treball

• Notes

• Prioritat

> [!NOTE]
> Si afegiu altres columnes al fitxer del Microsoft Project Client, no es desaran al fitxer i no es mostraran quan el fitxer torni a obrir-se.

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>Crear l'estructura del desglossament del treball per a un projecte existent amb Microsoft Project Client
Per crear una nova estructura del desglossament del treball amb el Microsoft Project Client, seguiu aquests passos:


1.  Obriu el Microsoft Project Client.

2.  A la pestanya **Microsoft Dynamics 365**, feu clic a **Obre**.

3.  Seleccioneu l'**Entitat jurídica** per al projecte.

4.  Seleccioneu el **Projecte**.

5.  Feu clic a **Desprotegeix** a la pestanya **Microsoft Dynamics 365**.

6.  Quan estigueu a punt per publicar-ho al Finance, feu clic a **Protegeix** a la pestanya **Microsoft Dynamics 365**.

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>Substituir l'estructura del desglossament del treball existent per a un projecte existent amb Microsoft Project Client
Per crear una nova estructura del desglossament del treball amb el Microsoft Project Client i substituir una estructura del desglossament del treball existent per a un projecte existent, seguiu aquests passos:

1.  Obriu el Microsoft Project Client.

2.  Creeu una planificació al Microsoft Project Client.

3.  A la pestanya **Microsoft Dynamics 365**, feu clic a **Desa els canvis** > **Substitueix un projecte existent**.

4.  Seleccioneu l'**Entitat jurídica** per al projecte.

5.  Seleccioneu el **Projecte**.

6.  Feu clic a **D'acord**.

## <a name="create-a-new-project-from-within-microsoft-project-client"></a>Crear un projecte nou des del Microsoft Project Client


1.  Obriu el Microsoft Project Client.

2.  Creeu una planificació al Microsoft Project Client.

3.  A la pestanya **Microsoft Dynamics 365**, feu clic a **Desa els canvis** > **Desa en un projecte nou**.

4.  Seleccioneu l'**Entitat jurídica** per al projecte.

5.  Introduïu l'**Identificador del projecte**, si cal.

6.  Introduïu el **Nom del projecte**.

7.  Seleccioneu el **Tipus de projecte**, el **Grup de projectes** i l'**Identificador del contracte del projecte**. O bé, podeu crear un contracte de projecte nou fent clic a **Nou**.

8.  Seleccioneu el **calendari** que s'utilitzarà per als recursos.

11. Feu clic a **D'acord**.

> [!NOTE]
> El complement Client del projecte no admet els caràcters següents per al format d'ID del projecte:
> 
>   - Subratllat
>   - Període
>   - Espai
>   - Barra

[!INCLUDE[footer-include](../includes/footer-banner.md)]
