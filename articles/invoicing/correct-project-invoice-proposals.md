---
title: Corregir la comptabilitat a l'esborrany de propostes de factures del projecte
description: En aquest article s'explica com ajustar la informació relacionada amb la comptabilitat d'un esborrany de proposta de factura.
author: sigitac
ms.date: 01/05/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 32f566a798d07b698693392f3aa1823f91fe5408
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921198"
---
# <a name="correct-the-accounting-on-draft-project-invoice-proposals"></a>Corregir la comptabilitat a l'esborrany de propostes de factures del projecte

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

L'administrador del projecte conserva els *Detalls de l'operació* de les factures del projecte en una factura proforma. Aquests detalls inclouen la decisió sobre les hores, les despeses, els materials o les fites que s'han de facturar, les tarifes i l'aplicació d'imports anticipats i de bestreta. Després de confirmar la factura proforma original, podeu ajustar els detalls operatius creant i confirmant una [factura proforma correctiva](../proforma-invoicing/corrective-invoices.md).

Els *Detalls de comptabilitat* de les factures del projecte es mantenen en un document de factura del client. Aquestes dades inclouen el càlcul de l'impost de vendes i les mesures financeres que s'apliquen a la factura. En aquest article s'ofereixen detalls sobre com es poden ajustar aquestes dades comptables en una proposta de factura del projecte.

## <a name="adjust-sales-tax"></a>Ajustar l’impost sobre les vendes

Els grups d'impostos sobre les vendes i els grups d'impostos sobre les vendes d'articles de la facturació per defecte es poden ajustar directament al document de proposta de factura. Per ajustar aquests grups, seleccioneu **Edita** i, a continuació, a cada línia de proposta de factura de projecte, introduïu un valor nou al camp **Grup d'impostos sobre les vendes** o **Grup d'impostos sobre les vendes d'articles**.

## <a name="adjust-financial-dimensions"></a>Ajustar les mesures financeres

### <a name="header-dimensions"></a>Dimensions de la capçalera

Per defecte, les dimensions financeres de la factura es deriven dels registres de transaccions del projecte no facturats. Tanmateix, la configuració del sistema us permet utilitzar dimensions financeres a la capçalera de les propostes de factures del projecte per publicar saldos de clients. Per habilitar aquesta funcionalitat, seleccioneu **Permet les actualitzacions de les dimensions del projecte per als comptes a cobrar** a la **pestanya Finances** de la **pàgina Gestió de projectes i paràmetres comptables**.

Les dimensions financeres de les capçaleres de les factures es poden editar abans de publicar una factura. A la **pàgina Proposta de factura** del projecte, canvieu a la **visualització capçalera** i editeu els valors a la **pestanya Dimensions financeres**.

La **visualització capçalera** només està disponible després que l'administrador del sistema hagibiliti la proposta de factura Del projecte d'ús **i els formularis de diari de factures amb la característica Visualització** capçalera i línies a l'àrea de treball d'administració **de** funcions. Aquesta característica requereix l'actualització financera 10.0.25 o posterior.

### <a name="line-dimensions"></a>Dimensions de la línia

Les mesures financeres no es poden editar directament en una línia de proposta de factura de projecte. Com a alternativa, seguiu aquests passos per ajustar les mesures financeres en una proposta de factura de projecte.

1. A la proposta de factura de projecte, seleccioneu **Suprimeix-ho tot** per suprimir les línies de proposta de factura de projecte.

    El botó **Suprimeix-ho tot** només està disponible quan l'administrador del sistema habilita la característica **Suprimeix les línies de proposta de factura en utilitzar el Project Operations per a escenaris basats en recursos/no mantinguts en existències** a l'àrea de treball **Administració de característiques**.

2. Ajustar les mesures financeres:

    - **Transaccions al compte (fites de facturació):** aneu a **Tots els projectes** \> **Administra** \> **Transaccions al compte** i seleccioneu la fita que requereix ajustament. A continuació, a la pestanya **Mesures financeres**, actualitzeu els valors segons calgui.
    - **Transaccions de temps, despeses i materials:** a la pàgina **Transaccions del projecte publicat**, seleccioneu **Ajusta la comptabilitat** per actualitzar les mesures financeres.

3. Un cop ajustats els valors de les mesures financeres, aneu a **Comptabilitat i l'administració de projectes** \> **Periòdic** \> **Integració del Project Operations** i seleccioneu **Importa des de la taula de còpia intermèdia** per executar el procés periòdic. Aquest procés utilitza els valors de mesures financeres actualitzats per tornar a crear les línies de proposta de factura de projecte. Els valors actualitzats s'utilitzen al subllibre i el llibre major del projecte quan es publica la factura del projecte.
