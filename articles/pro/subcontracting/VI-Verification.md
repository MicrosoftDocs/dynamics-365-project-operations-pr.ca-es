---
title: Verificació de factures de proveïdors amb reals aprovats
description: Aquest tema explica com Microsoft Dynamics 365 Project Operations let's project managers verifica les factures del proveïdor amb els reals que es van aprovar com a contractistes van realitzar treballs i temps registrat, i les despeses i materials que van ser utilitzats pels membres de l'equip del projecte.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3350a51bde2872036b79a789fae23ea6790fb21a
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8585458"
---
# <a name="verification-of-vendor-invoices-with-approved-actuals"></a>Verificació de factures de proveïdors amb reals aprovats

[!include [banner](../../includes/dataverse-preview.md)]

_ **Aplica a: Desplegament de Lite:** acord a la facturació proforma

Microsoft Dynamics 365 Project Operations permet als gestors de projectes verificar les línies de factures del proveïdor de les maneres següents:

- Utilitzeu el **camp Estat** de verificació de les línies de factura del proveïdor.
- Si les línies de factura del proveïdor fan referència a una línia de subcontractació, enllaceu els reals de cost de l'activitat del subcontractista a aquestes línies de factura del proveïdor. L'enllaç es crea fent coincidir els reals de costos amb les línies de factura del proveïdor.

    > [!NOTE]
    > Tot i que es pot fer un seguiment de l'estat de verificació de les línies de factura del proveïdor que no fan referència a una subcontracta, els reals de cost no es poden enllaçar a aquestes línies de factura del proveïdor.

## <a name="verification-status"></a>Estat de verificació

El **camp Estat** de verificació d'una línia de factura del proveïdor indica l'estat de la verificació. S'admeten els estats següents:

1. No s'ha iniciat
2. En curs
3. Complet

Es poden editar les línies de factura del proveïdor que tenen un estat de verificació de **No iniciat**.

Les línies de factura del proveïdor que tenen un estat de verificació de **En curs** ja no es poden editar. Per a una línia de factura del proveïdor que fa referència a una subcontracta, l'estat de verificació s'estableix automàticament en **curs** tan aviat com el primer cost real coincideixi amb la línia de factura del proveïdor.

Les línies de factura del proveïdor que tenen un estat de verificació de **Complete** ja no es poden editar. Quan totes les línies d'una factura de proveïdor tenen aquest estat de verificació, es pot confirmar la factura del proveïdor.

## <a name="match-cost-actuals-to-vendor-invoice-lines"></a>Coincideix amb els reals de cost amb les línies de factura del proveïdor

La coincidència de reals de costos ajuda amb el procés de verificació d'una línia de factura del proveïdor. Per fer coincidir els costos reals amb una línia de factura del proveïdor, seguiu aquests passos.

1. Obriu la línia de factura del proveïdor i seleccioneu la **pestanya Cost real no** coincident. Una quadrícula mostra una llista de reals de costos que fan referència a la mateixa línia de subcontractació que la línia de factura del proveïdor.
2. Seleccioneu un o més dels reals de cost i, a continuació, seleccioneu **Coincideix** a la barra d'eines que hi ha a sobre de la quadrícula. El sistema valida que els reals de cost seleccionats es poden igualar. Un cop superada la validació, els reals de cost s'envien a la línia de factura del proveïdor.

### <a name="validation-criteria-that-are-used-to-link-cost-actuals-to-vendor-invoice-lines"></a>Criteris de validació que s'utilitzen per enllaçar els reals de costos a les línies de factures del proveïdor

Durant el procés de coincidència, només es pot establir un enllaç entre una línia de factura de cost real i una línia de factura de proveïdor si es compleixen les dues condicions següents:

- El **camp Estat d'ajust** per a cada cost real seleccionat ha d'estar en blanc. En altres paraules, els reals de cost no han d'haver estat substituïts per altres reals de costos durant un procés de recuperació, cancel·lació d'aprovació o correcció de revistes.
- Els valors dels camps següents coincideixen entre la línia de factura del proveïdor i el cost real seleccionat. Si algun camp no està definit a la línia de factura del proveïdor, no es considera que coincideixi.

    - Contracte de projecte
    - Línia de contracte del projecte
    - Classe de la transacció
    - Project
    - Tasca
    - Categoria de recursos
    - Categoria de la transacció
    - Producte
    - Línia subcontractada
    - Recurs que es pot reservar

## <a name="unmatch-cost-actuals-from-a-vendor-invoice-line"></a>Cost real no coincident d'una línia de factura del proveïdor

L'inigualable dels reals de costos també pot ajudar amb el procés de verificació d'una factura de proveïdor, ja que permet eliminar enllaços establerts prèviament. Els reals de costos només es poden obtenir de les línies de factura del proveïdor que tenen un estat de verificació de **En curs**. Per obtenir un cost real inigualable des d'una línia de factura de proveïdor, seguiu aquests passos.

1. Obriu la línia de factura del proveïdor i seleccioneu la **pestanya Cost real** coincident. Una quadrícula mostra una llista dels reals de cost que fan referència a la línia de factura del proveïdor.
2. Seleccioneu un o més dels reals de cost i, a continuació, seleccioneu **Unigua** a la barra d'eines que hi ha a sobre de la quadrícula.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
