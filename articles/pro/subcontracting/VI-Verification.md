---
title: Verificació de factures del proveïdor amb valors reals aprovats
description: En aquest article s'explica com Microsoft Dynamics 365 Project Operations permet als administradors de projectes verificar les factures dels proveïdors amb els reals que es van aprovar a mesura que els contractistes realitzaven treballs i temps registrat, i les despeses i materials que utilitzaven els membres de l'equip del projecte.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: ab9f69e36aa58bfe3a2f8e3455db66b6bceea968
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261734"
---
# <a name="verification-of-vendor-invoices-with-approved-actuals"></a>Verificació de factures del proveïdor amb valors reals aprovats

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_

Els administradors de projectes de Microsoft Dynamics 365 Project Operations verifiquen les línies de factures dels proveïdors de les maneres següents:

- Utilitzeu el **camp Estat de verificació** de les línies de factura de proveïdor.
- Si les línies de factures del venedor fan referència a una línia de subcontractació, vinculen els costos reals de l'activitat del subcontractista a les línies de factures dels proveïdors. L'enllaç es crea fent coincidir els reals de costos amb les línies de factures del proveïdor.

    > [!NOTE]
    > Tot i que es pot fer un seguiment de l'estat de verificació de les línies de factures dels proveïdors que no fan referència a un subcontractista, els costos reals no es poden enllaçar amb aquestes línies de factures de proveïdors.

## <a name="verification-status"></a>Estat de verificació

El **camp Estat de verificació d'una** línia de factura del proveïdor indica l'estat de la verificació. S'admeten els següents estats:

1. No s'ha iniciat
2. En curs
3. Complet

Es poden editar línies de factures de proveïdor que tinguin un estat de verificació de **No iniciat**.

Les línies de factures de proveïdor que tinguin l'estat de verificació d'En **curs** ja no es poden editar. Per a una línia de factura del proveïdor que fa referència a un subcontractista, l'estat de verificació s'estableix automàticament a **En curs** tan bon punt el primer cost real coincideix amb la línia de factura del proveïdor.

Les línies de factures de proveïdor que tinguin l'estat de verificació de **Complete** ja no es poden editar. Quan totes les línies d'una factura de proveïdor tenen aquest estat de verificació, es pot confirmar la factura del proveïdor.

## <a name="match-cost-actuals-to-vendor-invoice-lines"></a>Coincidència de costos reals amb línies de factures de proveïdors

La coincidència dels reals de costos ajuda amb el procés de verificació en una línia de factures del proveïdor. Per fer coincidir els costos reals amb una línia de factures de proveïdor, seguiu aquests passos.

1. Obriu la línia de factures del proveïdor i seleccioneu la **pestanya Costos reals inigualables** . Una quadrícula mostra una llista de costos reals que fan referència a la mateixa línia de subcontractació que la línia de factures del proveïdor.
2. Seleccioneu un o més dels reals de cost i, a continuació, seleccioneu Coincidència **a** la barra d'eines que hi ha a sobre de la quadrícula. El sistema valida que els reals de cost seleccionats es puguin igualar. Un cop passada la validació, els reals de costos s'enllacen amb la línia de factura del proveïdor.

### <a name="validation-criteria-that-are-used-to-link-cost-actuals-to-vendor-invoice-lines"></a>Criteris de validació que s'utilitzen per vincular els reals de costos a les línies de factures dels proveïdors

Durant el procés de coincidència, només es pot establir un vincle entre un cost real i una línia de factura del proveïdor si es compleixen les dues condicions següents:

- El **camp Estat d'ajust** per a cada cost real seleccionat ha d'estar en blanc. Dit d'una altra manera, els costos reals no han d'haver estat substituïts per altres reals de costos durant un procés de retirada, cancel·lació d'aprovació o correcció.
- Els valors dels camps següents coincideixen entre la línia de factura del proveïdor i el cost real seleccionat. Si no s'estableix cap camp a la línia de factures del proveïdor, no es considera que coincideixi.

    - Contracte de projecte
    - Línia de contracte del projecte
    - Classe de la transacció
    - Project
    - Tasca
    - Categoria de recurs
    - Categoria de la transacció
    - Producte
    - Línia de subcontractació
    - Recurs que es pot reservar

## <a name="unmatch-cost-actuals-from-a-vendor-invoice-line"></a>Costos reals inigualables d'una línia de factures del proveïdor

La minimització dels reals de costos també pot ajudar amb el procés de verificació d'una factura de proveïdor, ja que permet eliminar els enllaços establerts prèviament. Els costos reals només es poden igualar des de les línies de factures de proveïdors que tenen un estat de verificació d'En **curs**. Per desencallar els costos reals d'una línia de factures del proveïdor, seguiu aquests passos.

1. Obriu la línia de factures del proveïdor i seleccioneu la **pestanya Realitats de cost coincidents** . Una quadrícula mostra una llista de costos reals que fan referència a la línia de factures del proveïdor.
2. Seleccioneu un o més dels reals de cost i, a continuació, seleccioneu **Inigualable** a la barra d'eines que hi ha a sobre de la quadrícula.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
