---
title: Valors per defecte de la dimensió financera
description: Aquest tema proporciona informació sobre com configurar els valors predeterminats de les dimensions financeres.
author: sigitac
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 03b9a9028c1610b191db9c1bfb0163adc88bdf3e
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642351"
---
# <a name="financial-dimension-defaults"></a>Valors per defecte de la dimensió financera

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

El Dynamics 365 Project Operations utilitza el marc de [dimensions financeres](https://docs.microsoft.com/dynamics365/finance/general-ledger/financial-dimensions) del Dynamics 365 Finance per proporcionar informació addicional sobre les transaccions del subdiari del projecte i el diari general.

Les dimensions financeres predeterminades es poden establir en un client, font de finançament de projectes, fita, línia de contracte de projecte o projecte.

## <a name="define-default-financial-dimensions-for-a-customer"></a>Definir dimensions financeres per defecte per a un client

Els valors per defecte de la dimensió del client s'especifiquen al Finance. Completeu els passos següents per definir valors per defecte de dimensió.

1. Aneu a **Comptes a cobrar** > **Clients** > **Tots els clients**.
2. A la pàgina **Clients**, a la pestanya **Dimensions financeres**, definiu els valors de la dimensió financera per a un client concret.

## <a name="define-default-financial-dimensions-for-project-contracts"></a>Definir dimensions financeres per defecte per a contractes de projecte

Els contractes de projecte es creen i es mantenen al Common Data Service (CDS). Els atributs de comptabilitat dels contractes de projecte es fixen en el mòdul **Administració de projectes i comptabilitat** del Finance.

### <a name="set-financial-dimensions-for-a-project-funding-source"></a>Definir dimensions financeres per a una font de finançament del projecte

1. Aneu a **Administració de projectes i comptabilitat** > **Projectes** > **Contractes de projecte**.
2. Seleccioneu el registre que voleu actualitzar i, a la pestanya **Contracte del projecte**, seleccioneu **Mostra la comptabilitat per defecte**.
3. Expandiu **Informació relacionada** i seleccioneu la pestanya **Fonts de finançament**.
4. Definiu els valors per defecte de la dimensió financera. Tingueu en compte que les dimensions financeres provenen per defecte del compte de client.

### <a name="set-financial-dimensions-for-a-project-contract-line"></a>Definir dimensions financeres per a una línia de contracte del projecte

1. Aneu a **Administració de projectes i comptabilitat** > **Projectes** > **Contractes de projecte**.
2. Seleccioneu el registre que voleu actualitzar i, a la pestanya **Contracte del projecte**, seleccioneu **Mostra la comptabilitat per defecte**.
3. Expandiu **Informació relacionada** i seleccioneu la pestanya **Línies de contracte**.
4. Definiu els valors per defecte de la dimensió financera. Els valors per defecte de la dimensió financera són aplicables i només es poden utilitzar amb línies de contracte de preu fix (fita).

Aquests valors per defecte s'utilitzen en les transaccions i línies de factura relacionades amb el projecte.

## <a name="define-default-financial-dimensions-for-projects"></a>Definir dimensions financeres per defecte per a projectes

Els projectes es creen i es mantenen al CDS. Els atributs de comptabilitat dels projectes es fixen en el mòdul **Administració de projectes i comptabilitat** del Finance.

1. Aneu a **Administració de projectes i comptabilitat** > **Projectes** > **Tots els projectes**.
2. Seleccioneu el registre que voleu actualitzar i, a la pestanya **Projecte**, seleccioneu **Mostra la comptabilitat per defecte**.
3. Expandiu **Informació relacionada** i seleccioneu la pestanya **Configuració**.
4. Definiu els valors per defecte de la dimensió financera. Tingueu en compte que les dimensions financeres provenen per defecte del compte de client. Si el projecte està associat a una línia de contracte amb diversos clients del contracte del projecte, el client principal s'utilitza per obtenir les dimensions financeres per defecte.

Les dimensions financeres per defecte del projecte s'utilitzen per definir els valors per defecte de la línia de diari per a les transaccions de temps, despeses i càrrecs al **Diari d'integració del Project Operations** i a les línies de factura del projecte relacionades.


[!INCLUDE[footer-include](../includes/footer-banner.md)]