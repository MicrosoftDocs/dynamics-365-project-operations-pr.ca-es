---
title: Registre per obtenir una subscripció de versió preliminar (bàsica)
description: "En aquest article s'ofereix informació sobre com subscriure i implementar la implementació de lite d'operacions del projecte: tracteu la facturació proforma."
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 6953956c0b3401a6c64ee597f966ba4a4c0d07b5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921244"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a>Registre per obtenir una subscripció de versió preliminar (bàsica) 

En aquest article s'explica com subscriure's a l'oferta de prova i implementar Dynamics 365 Project Operations el desplegament lite: tracteu la facturació proforma.

> [!NOTE]
> Aquest procés canviarà en pròximes versions del Project Operations.

## <a name="prerequisites"></a>Requisits previs
- L'usuari que implementa la versió preliminar ha de tenir drets d'administrador global a l'inquilí de l'Azure. Podeu crear un inquilí en bescanviar la primera oferta.

> [!IMPORTANT]
> Només cal que una persona de l'organització, l'administrador d'inquilins, realitzi aquesta tasca. Si no sou el subscriptor en aquesta versió, espereu fins que l'organització s'hagi registrat i hàgiu rebut les vostres credencials d'usuari.
> 
> Les proves són d'un sol ús a l'inquilí. Una versió de prova només es pot executar una vegada. Us recomanem que creeu un inquilí nou per a la versió de prova.

### <a name="dynamics-365-project-operations-trial"></a>Prova del Dynamics 365 Project Operations 

Abans de començar, assegureu-vos que hàgiu iniciat la sessió en un navegador amb el compte laboral de l'usuari a l'inquilí on voleu la versió preliminar del Project Operations.

1. Aneu a [Prova del Project Operations](https://aka.ms/try-po) per bescanviar el primer codi de l'oferta, **Dynamics 365 Project Operations**.
2. Confirmeu la comanda.

  Veureu que l'oferta de confirmació s'ha bescanviat correctament.

## <a name="assign-licenses"></a>Assignar llicències

> [!IMPORTANT]
> Necessitareu accés d'administrador al portal de l'Microsoft 365 de l'organització per completar els passos següents.


1. Aneu al [Microsoft 365 centre](https://portal.office.com/) d'administració per assignar les llicències als usuaris.
2. A la pàgina **Usuaris actius**, seleccioneu els usuaris als quals voleu assignar una llicència.
3. Verifiqueu que la llicència del **Dynamics 365 Project Operations** estigui seleccionada. 
4. Seleccioneu **Desa els canvis**.

## <a name="create-a-new-dataverse-environment"></a>Crear un entorn nou del Dataverse

1. Proporcioneu un entorn de desplegament d'operacions Dataverse de projecte nou seguint les instruccions de l'article, [Dataverse model de desplegament](lite-deployment.md). Quan seleccioneu el tipus d'entorn, assegureu-vos d'utilitzar **Prova (basada en subscripció)**.

  ![Entorn nou.](./media/19CreateEnvironment.png)

2. Seleccioneu l'opció **Habilita les aplicacions del Dynamics 365** i deixeu **Implementa aquestes aplicacions automàticament** en blanc.  
3. Seleccioneu **Desa** per crear l'entorn.

  ![Afegeix base de dades.](./media/20CreateEnvironment1.png)

4. Un cop creat l'entorn, instal·leu la solució **Microsoft Dynamics 365 Project Operations**. 

![Instal·lar la solució.](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a>Instal·lar una configuració del CDS i configurar les dades de demostració

Instal·leu la configuració del CDS i configureu les dades de demostració seguint les instruccions de l'article, [Aplica les dades de configuració i configuració de la demostració](lite-apply-demo-setup-config-data.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
