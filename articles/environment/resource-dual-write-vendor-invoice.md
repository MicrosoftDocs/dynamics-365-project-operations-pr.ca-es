---
title: Integració de factures del proveïdor
description: Aquest tema proporciona informació sobre la integració de factures del proveïdor al Project Operations.
author: sigitac
ms.date: 04/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 538a2694591f1d0d368ee0ffeed9bdf12cb47420c3d0571f75185fe433f23436
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986479"
---
# <a name="vendor-invoice-integration"></a>Integració de factures del proveïdor

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

La compra relacionada amb el projecte al Dynamics 365 Project Operations es pot registrar anant a **Compte a pagar** > **Factures** > **Factures pendents del proveïdor** i utilitzant un document de factura pendent del proveïdor. Per obtenir més informació, vegeu [Compra de materials sense existències mitjançant una factura pendent del proveïdor](../procurement/pending-vendor-invoices.md).

> [!IMPORTANT]
> Abans d'utilitzar la funcionalitat descrita en aquest tema, reviseu i apliqueu les configuracions necessàries. Per obtenir més informació, vegeu [Habilitar materials sense existències i factures pendents del proveïdor](../procurement/configure-materials-nonstocked.md).

Al Project Operations, les factures del proveïdor relacionades amb el projecte es publiquen mitjançant regles de publicació especials:

- El cost relacionat amb el projecte (incloent-hi els impostos que no es poden recuperar) no es publica immediatament al compte de cost del projecte al registre general. En lloc d'això, el cost es publica al **Compte d'integració de la compra**. Aquest compte es configura a **Administració i comptabilitat del projecte** > **Configuració** > **Paràmetres d'administració i comptabilitat del projecte** i a la pestanya de **Project Operations al Dynamics 365 Customer Engagement**.
- L'escriptura doble sincronitza els detalls de la factura del proveïdor amb el Microsoft Dataverse utilitzant les assignacions de taula següents:

     - **Entitat d'exportació de factura del proveïdor del projecte d'integració del Project Operations (msdyn_projectvendorinvoices)**: aquesta assignació de taules sincronitza la informació de la capçalera de la factura del proveïdor. Només les factures del proveïdor amb com a mínim una línia que contingui un identificador de projecte se sincronitzen amb el Dataverse.
     - **Entitat d'exportació de línia de factura del proveïdor del projecte d'integració del Project Operations (msdyn_projectvendorinvoicelines)**: aquesta assignació de taules sincronitza la informació de la línia de la factura del proveïdor. Amb el Dataverse només se sincronitzen les línies que contenen un identificador del projecte.

     > [!NOTE]
     > Els detalls de la factura del proveïdor del Dataverse no es poden editar.

El subllibre de comptabilitat d'impostos, el subllibre de comptabilitat de proveïdors i les altres publicacions financeres es registren segons calgui al Dynamics 365 Finance en el moment de publicar la factura del proveïdor.

![Integració de factures del proveïdor.](media/DW7VendorInvoice.png)

Quan s'escriuen registres en una entitat de **Factura del proveïdor** al Dataverse, s'inicia un procés d'aprovació automatitzada dels registres. Si cal, l'estat del procés d'aprovació automatitzada es pot revisar al Dataverse anant a **Configuració avançada** > **Sistema** > **Feines del sistema**. Un cop completada l'aprovació, el sistema crea registres de classe de transacció de materials a l'entitat **Valors reals**.

A continuació, els valors reals relacionats amb els materials es processen amb l'assignació de taules de doble escriptura **Valors reals d'integració del Project Operations (msdyn_actuals)**. Per obtenir més informació, vegeu [Estimacions i valors reals del projecte](resource-dual-write-estimates-actuals.md).

El procés periòdic **Importació des de la còpia intermèdia** crea línies del llibre diari d'integració del Project Operations relacionades amb la factura del proveïdor. El compte de desplaçament es defineix per defecte al compte d'integració de proveïment. Quan el llibre diari d'integració es publica, s'esborra el balanç del compte de la transacció de factura del proveïdor i es desplaça l'import de la línia al compte de cost del projecte. Les transaccions del subllibre de comptabilitat del projecte també es creen amb finalitats de facturació descendent i de reconeixement d'ingressos.
