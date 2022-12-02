---
title: Comprar materials sense existències o categories de proveïment mitjançant una factura pendent del proveïdor
description: En aquest article s'explica com es registren les factures pendents del proveïdor.
author: sigitac
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b1c05755f6759e90e031a11261f15a2c4b6b716e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921980"
---
# <a name="purchase-non-stocked-materials-or-procurement-categories-using-a-pending-vendor-invoice"></a>Comprar materials sense existències o categories de proveïment mitjançant una factura pendent del proveïdor

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

Quan una empresa processa materials sense existències o categories de proveïment per a un projecte, els costos es poden registrar immediatament en el projecte. 

Per exemple, Contoso Robotics US està realitzant un projecte de renovació d'equipament i necessita llicències de programari. Aquestes llicències provenen d'un proveïdor de tercers.  Mitjançant el Dynamics 365 Finance, l'encarregat del compte a pagar registra un document de factura pendent del proveïdor i atribueix els costos de llicència directament al projecte de renovació d'equipament. 

> [!IMPORTANT]
> Abans d'utilitzar la funcionalitat descrita en aquest article, reviseu i apliqueu les configuracions necessàries. Per obtenir més informació, vegeu [Habilitar materials no mantinguts en existències i factures pendents del proveïdor](configure-materials-nonstocked.md) i [Utilitzar categories de proveïment amb comandes de compra de projectes i factures pendents del proveïdor](configure-procurement-categories.md)

## <a name="post-a-project-related-pending-vendor-invoice"></a>Publicar una factura pendent del proveïdor relacionada amb el projecte 

Les factures pendents del proveïdor es poden registrar a la pàgina **Factures pendents del proveïdor** (**Compte a pagar** > **Factures** > **Factures pendents del proveïdor**). Seguiu els passos següents per publicar una factura pendent del proveïdor relacionada amb el projecte:

1. Aneu a **Compte a pagar** > **Factures** i seleccioneu **Crea**. 
1. Al camp **Compte de factura**, seleccioneu un proveïdor i, al camp **Número**, introduïu l'identificador de factura del proveïdor.
1. Afegiu una línia a la factura del proveïdor i, al camp **Número d'element**, seleccioneu l'article sense existències adquirit del proveïdor. O bé, al camp **Categoria de proveïment**, seleccioneu la categoria de proveïment que s'ha adquirit al proveïdor.   
1. Afegiu la quantitat comprada. El sistema emplena el preu per unitat segons la configuració del preu de l'article sense existències. 
1. Verifiqueu l'import total i altres detalls necessaris a la línia.
1. Als detalls de línia, a la pestanya **Projecte**, seleccioneu l'identificador del projecte al qual es registrarà aquest element.
1. Opcional: seleccioneu el número d'activitat i actualitzeu la categoria del projecte i la propietat de la línia.
1. Publiqueu la factura pendent del proveïdor. Quan es comptabilitza la factura, el sistema registra la informació següent:
    
    - Import del balanç del proveïdor.
    - Import de l’impost sobre les vendes.
    - El cost en relació amb el projecte es registra al compte d'integració del proveïment.
    - Transacció de cost real del projecte al Dataverse.  Aquesta transacció es processa addicionalment per mitjà del [Llibre diari d'integració del Project Operations](../project-accounting/project-operations-integration-journal.md). El fet de publicar aquest llibre diari desplaça l'import del compte d'integració de proveïment al compte de cost del projecte. 
    - Compres facturades al client del projecte mitjançant el mètode de facturació de temps i materials. A més, les transaccions de vendes no facturades es creen per a les compres al Dataverse. La llista de preus del producte al Dataverse s'utilitza per als preus de vendes i els imports per a la transacció de vendes no utilitzada.
