---
title: Verificació de factures del proveïdor amb valors reals aprovats
description: En aquest article s'explica com el Microsoft Dynamics 365 Project Operations permet als gestors de projectes verificar les factures de proveïdor amb els valors reals aprovats quan els contractistes fan feina i registren el temps, i les despeses i els materials utilitzats pels membres de l'equip del projecte.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 67e0a0143fa354ca9a87bfac5fbbd6306a97811c
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522935"
---
# <a name="verification-of-vendor-invoices-with-approved-actuals"></a>Verificació de factures del proveïdor amb valors reals aprovats

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

El Microsoft Dynamics 365 Project Operations permet als administradors del projecte verificar les línies de factura del proveïdor d'aquestes maneres:

- Utilitzar el camp **Estat de verificació** a les línies de factura del proveïdor amb errors.
- Si les línies de factura del proveïdor fan referència a una línia de subcontracte, enllaçar els valors reals de cost de l'activitat del subcontractista amb aquestes línies de factura del proveïdor. L'enllaç es crea fent coincidir els valors reals de cost amb les línies de factura del proveïdor.

    > [!NOTE]
    > Tot i que es pot fer el seguiment de l'estat de la verificació per a les línies de factura del proveïdor que no fan referència a un subcontracte, els valors reals de cost no es poden enllaçar a aquestes línies de factura del proveïdor.

## <a name="verification-status"></a>Estat de verificació

El camp **Estat de verificació** d'una línia de factura del proveïdor indica l'estat de la verificació. S'admeten els estats següents:

1. No s'ha iniciat
2. En curs
3. Complet

Les línies de factura del proveïdor que tenen un estat de verificació de **No iniciada** es poden editar.

Les línies de factura del proveïdor que tenen un estat de verificació d'**En curs** ja no es poden editar. Per a una línia de factura del proveïdor que fa referència a un subcontracte, l'estat de verificació es defineix automàticament com a **En curs** tan bon punt es fa coincidir el primer cost real amb la línia de factura del proveïdor.

Les línies de factura del proveïdor que tenen un estat de verificació de **Completa** ja no es poden editar. Si totes les línies d'una factura de proveïdor tenen aquest estat de verificació, la factura de proveïdor no es pot confirmar.

## <a name="match-cost-actuals-to-vendor-invoice-lines"></a>Igualar els valors reals de cost amb les línies de factura del proveïdor

La coincidència dels valors reals de cost ajuda amb el procés de verificació en una línia de factura del proveïdor. Per aparellar els valors reals de cost amb una línia de factura del proveïdor, seguiu aquests passos.

1. Obriu la línia de factura del proveïdor i seleccioneu la pestanya **Valors reals de cost sense coincidència**. En una quadrícula es mostra una llista de valors reals de cost que fan referència a la mateixa línia de subcontracte que la línia de factura del proveïdor.
2. Seleccioneu un o diversos valors reals de cost i, a continuació, seleccioneu **Coincidències** a la barra d'eines que hi ha a sobre de la quadrícula. El sistema valida que es poden igualar els valors reals de cost seleccionats. Un cop passada la validació, els valors reals de cost s'enllacen amb la línia de factura del proveïdor.

### <a name="validation-criteria-that-are-used-to-link-cost-actuals-to-vendor-invoice-lines"></a>Criteris de validació que s'utilitzen per enllaçar els valors reals de cost amb les línies de factura del proveïdor

Durant el procés de coincidència, es pot establir un enllaç entre un cost real i una línia de factura del proveïdor només si es compleixen les condicions següents:

- El camp **Estat d'ajustament** de cada cost real seleccionat ha d'estar buit. En altres paraules, els valors reals de cost no han d'haver estat substituïts per altres valors reals de cost durant un procés de retirada, cancel·lació de l'aprovació o correcció de diari.
- Els valors dels camps següents s'igualen entre la línia de factura del proveïdor i el cost real seleccionat. Si no es defineix cap camp a la línia de factura del proveïdor, no es considera que coincideixi.

    - Contracte de projecte
    - Línia de contracte del projecte
    - Classe de la transacció
    - Project
    - Tasca
    - Categoria del recurs
    - Categoria de la transacció
    - Producte
    - Línia de subcontracte
    - Recurs que es pot reservar

## <a name="unmatch-cost-actuals-from-a-vendor-invoice-line"></a>Eliminar la coincidència dels valors reals de cost d'una línia de factura del proveïdor

Eliminar la coincidència dels valors reals de cost també pot ajudar amb el procés de verificació d'una factura del proveïdor habilitant els enllaços establerts anteriorment que s'han de suprimir. Només es pot eliminar la coincidència dels valors reals de cost des de línies de factura del proveïdor que tenen un estat de verificació d'**En curs**. Per eliminar la coincidència dels valors reals de cost d'una línia de factura del proveïdor, seguiu aquests passos.

1. Obriu la línia de factura del proveïdor i seleccioneu la pestanya **Valors reals de cost amb coincidència**. En una quadrícula es mostra una llista de valors reals de cost que fan referència a la línia de factura del proveïdor.
2. Seleccioneu un o diversos valors reals de cost i, a continuació, seleccioneu **Elimina la coincidència** a la barra d'eines que hi ha a sobre de la quadrícula.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
