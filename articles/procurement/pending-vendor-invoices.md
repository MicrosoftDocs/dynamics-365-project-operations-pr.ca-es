---
title: Compra materials no emmagatzemats o categories d'adquisició mitjançant una factura de proveïdor pendent
description: En aquest tema s'explica com es registren les factures pendents del proveïdor.
author: sigitac
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: e81f7a54e304ae6fc9a9f2637124579b6e7b54e9
ms.sourcegitcommit: 9916f536a71b6a0078297402564ac79308ec6890
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/18/2022
ms.locfileid: "8612645"
---
# <a name="purchase-non-stocked-materials-or-procurement-categories-using-a-pending-vendor-invoice"></a>Compra materials no emmagatzemats o categories d'adquisició mitjançant una factura de proveïdor pendent

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

Com que una empresa adquireix materials no emmagatzemats o categories d'adquisició per a un projecte, els costos es poden registrar immediatament contra el projecte. 

Per exemple, Contoso Robotics US està realitzant un projecte de renovació d'equipament i necessita llicències de programari. Aquestes llicències provenen d'un proveïdor de tercers.  Utilitzant Dynamics 365 Finance, l'empleat que es paga als comptes registra un document de factura de proveïdor pendent i atribueix els costos de la llicència directament contra el projecte de renovació d'equips. 

> [!IMPORTANT]
> Abans d'utilitzar la funcionalitat descrita en aquest tema, reviseu i apliqueu les configuracions necessàries. Per obtenir més informació, vegeu [Habilitar materials no emmagatzemats i factures pendents de proveïdor i](configure-materials-nonstocked.md) Utilitzar categories de contractació amb ordres [de compra de projectes i factures pendents del proveïdor](configure-procurement-categories.md)

## <a name="post-a-project-related-pending-vendor-invoice"></a>Publicar una factura pendent del proveïdor relacionada amb el projecte 

Les factures pendents del proveïdor es poden registrar a la pàgina **Factures pendents del proveïdor** (**Compte a pagar** > **Factures** > **Factures pendents del proveïdor**). Seguiu els passos següents per publicar una factura pendent del proveïdor relacionada amb el projecte:

1. Aneu a **Comptes que** > **paguen factures** i seleccioneu **Crea**. 
1. **Al camp Compte** factura, seleccioneu un proveïdor i, al **camp Número**, introduïu la identificació de la factura del proveïdor.
1. Afegiu una línia a la factura del proveïdor i, a continuació, al **camp Número** d'element, seleccioneu l'element no proveït que s'ha comprat al proveïdor. Alternativament, al **camp Categoria** Contractació, seleccioneu la categoria de contractació que s'ha comprat al proveïdor.   
1. Afegiu-hi la quantitat que s'ha comprat. El sistema omple el preu unitari, basat en la configuració del preu de l'article no emmagatzemat. 
1. Verifiqueu l'import total i altres detalls necessaris a la línia.
1. Als detalls de la línia, a la **pestanya Projecte**, seleccioneu l'identificador del projecte al què es registrarà aquest element.
1. Opcional: seleccioneu el número d'activitat i actualitzeu la propietat de la categoria i la línia del projecte.
1. Publica la factura pendent del proveïdor. Quan es publica la factura, el sistema registra la informació següent:
    
    - Import del balanç del proveïdor.
    - Import de l’impost sobre les vendes.
    - El cost en relació amb el projecte es registra al compte d'integració del proveïment.
    - Transacció de cost real del projecte al Dataverse.  Aquesta transacció es processa addicionalment per mitjà del [Llibre diari d'integració del Project Operations](../project-accounting/project-operations-integration-journal.md). El fet de publicar aquest llibre diari desplaça l'import del compte d'integració de proveïment al compte de cost del projecte. 
    - Compres facturades al client del projecte mitjançant el mètode de facturació de temps i materials. A més, les transaccions de vendes no facturades es creen per a les compres al Dataverse. La llista de preus del producte al Dataverse s'utilitza per als preus de vendes i els imports per a la transacció de vendes no utilitzada.
