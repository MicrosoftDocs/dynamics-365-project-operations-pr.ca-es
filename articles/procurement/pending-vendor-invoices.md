---
title: Comrpa de materials sense existències mitjançant una factura pendent del proveïdor
description: En aquest tema s'explica com es registren les factures pendents del proveïdor.
author: sigitac
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e95f7dabe597968707fdd2dead40bfb93d7f1f95
ms.sourcegitcommit: 74a7e1c9c338fb8a4b0ad57c5560a88b6e02d0b2
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 09/23/2021
ms.locfileid: "7547277"
---
# <a name="purchase-non-stocked-materials-using-a-pending-vendor-invoice"></a>Comrpa de materials sense existències mitjançant una factura pendent del proveïdor

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

Com que una empresa processa materials sense existències per a un projecte, els costos es poden registrar immediatament en el projecte. 

Per exemple, Contoso Robotics US està realitzant un projecte de renovació d'equipament i necessita llicències de programari. Aquestes llicències provenen d'un proveïdor de tercers.  Mitjançant el Dynamics 365 Finance, l'encarregat del compte a pagar registra un document de factura pendent del proveïdor i atribueix els costos de llicència directament al projecte de renovació d'equipament. 

> [!IMPORTANT]
> Abans d'utilitzar la funcionalitat descrita en aquest tema, reviseu i apliqueu les configuracions necessàries. Per obtenir més informació, vegeu [Habilitar materials sense existències i factures pendents del proveïdor](configure-materials-nonstocked.md). 

## <a name="post-a-project-related-pending-vendor-invoice"></a>Publicar una factura pendent del proveïdor relacionada amb el projecte 

Les factures pendents del proveïdor es poden registrar a la pàgina **Factures pendents del proveïdor** (**Compte a pagar** > **Factures** > **Factures pendents del proveïdor**). Seguiu els passos següents per publicar una factura pendent del proveïdor relacionada amb el projecte:

1. Aneu a **Compte a pagar** > **Factures** i seleccioneu **Crea**. 
2. Al camp **Compte de factura**, seleccioneu un proveïdor i, al camp **Número**, introduïu l'identificador de factura del proveïdor.
3. Afegiu una línia a la factura del proveïdor i, al camp **Número d'element**, seleccioneu l'article sense existències adquirit del proveïdor. 

    > [!NOTE]
    > Les línies de factura del proveïdor basades en una categoria de proveïment no es poden registrar en el projecte. 
    
5. Afegiu la quantitat comprada. El sistema emplenarà el preu per unitat segons la configuració del preu de l'article sense existències. 
6. Verifiqueu l'import total i altres detalls necessaris a la línia.
7. Als detalls de línia, a la pestanya **Projecte**, seleccioneu l'identificador del projecte al qual es registrarà aquest element.
8. O bé seleccioneu el número d'activitat i actualitzeu la categoria del projecte i la propietat de la línia.
9. Publiqueu la factura pendent del proveïdor. Quan la factura es publica,el sistema registra:
    
    - Import del balanç del proveïdor.
    - Import de l’impost sobre les vendes.
    - El cost en relació amb el projecte es registra al compte d'integració del proveïment.
    - Transacció de cost real del projecte al Dataverse.  Aquesta transacció es processa addicionalment per mitjà del [Llibre diari d'integració del Project Operations](../project-accounting/project-operations-integration-journal.md). El fet de publicar aquest llibre diari desplaça l'import del compte d'integració de proveïment al compte de cost del projecte. 
    - Compres facturades al client del projecte mitjançant el mètode de facturació de temps i materials. A més, les transaccions de vendes no facturades es creen per a les compres al Dataverse. La llista de preus del producte al Dataverse s'utilitza per als preus de vendes i els imports per a la transacció de vendes no utilitzada.
