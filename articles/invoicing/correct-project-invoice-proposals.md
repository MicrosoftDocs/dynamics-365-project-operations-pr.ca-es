---
title: Corregir la comptabilitat a l'esborrany de propostes de factures del projecte
description: En aquest tema s'explica com s'ajusta la informació relacionada amb la comptabilitat en un esborrany de proposta de factura.
author: sigitac
ms.date: 06/07/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 387dc9a81db9c22f170b664152cbafeddf72d149
ms.sourcegitcommit: e93f436afbb92a312fc71b6371866f01927e49d5
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/14/2021
ms.locfileid: "6251180"
---
# <a name="correct-the-accounting-on-draft-project-invoice-proposals"></a>Corregir la comptabilitat a l'esborrany de propostes de factures del projecte

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

L'administrador del projecte conserva els *Detalls de l'operació* de les factures del projecte en una factura proforma. Aquests detalls inclouen la decisió sobre les hores, les despeses, els materials o les fites que s'han de facturar, les tarifes i l'aplicació d'imports anticipats i de bestreta. Després de confirmar la factura proforma original, podeu ajustar els detalls operatius creant i confirmant una [factura proforma correctiva](../proforma-invoicing/corrective-invoices.md).

Els *Detalls de comptabilitat* de les factures del projecte es mantenen en un document de factura del client. Aquestes dades inclouen el càlcul de l'impost de vendes i les mesures financeres que s'apliquen a la factura. En aquest tema es proporcionen detalls sobre com aquests detalls de comptabilitat es poden ajustar en un esborrany de proposta de factura de projecte.

## <a name="adjust-sales-tax"></a>Ajustar l’impost sobre les vendes

Els grups d'impostos sobre les vendes i els grups d'impostos sobre les vendes d'articles de la facturació per defecte es poden ajustar directament al document de proposta de factura. Per ajustar aquests grups, seleccioneu **Edita** i, a continuació, a cada línia de proposta de factura de projecte, introduïu un valor nou al camp **Grup d'impostos sobre les vendes** o **Grup d'impostos sobre les vendes d'articles**.

## <a name="adjust-financial-dimensions"></a>Ajustar les mesures financeres

Les mesures financeres no es poden editar directament en una línia de proposta de factura de projecte. Com a alternativa, seguiu aquests passos per ajustar les mesures financeres en una proposta de factura de projecte.

1. A la proposta de factura de projecte, seleccioneu **Suprimeix-ho tot** per suprimir les línies de proposta de factura de projecte.

    > [!NOTE]
    > El botó **Suprimeix-ho tot** només està disponible quan l'administrador del sistema habilita la característica **Suprimeix les línies de proposta de factura en utilitzar el Project Operations per a escenaris basats en recursos/no mantinguts en existències** a l'àrea de treball **Administració de característiques**.

2. Ajustar les mesures financeres:

    - **Transaccions al compte (fites de facturació):** aneu a **Tots els projectes** \> **Administra** \> **Transaccions al compte** i seleccioneu la fita que requereix ajustament. A continuació, a la pestanya **Mesures financeres**, actualitzeu els valors segons calgui.
    - **Transaccions de temps, despeses i materials:** a la pàgina **Transaccions del projecte publicat**, seleccioneu **Ajusta la comptabilitat** per actualitzar les mesures financeres.

3. Un cop ajustats els valors de les mesures financeres, aneu a **Comptabilitat i l'administració de projectes** \> **Periòdic** \> **Integració del Project Operations** i seleccioneu **Importa des de la taula de còpia intermèdia** per executar el procés periòdic. Aquest procés utilitza els valors de mesures financeres actualitzats per tornar a crear les línies de proposta de factura de projecte. Els valors actualitzats s'utilitzen al subllibre i el llibre major del projecte quan es publica la factura del projecte.
