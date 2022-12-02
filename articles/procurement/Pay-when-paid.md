---
title: Pagaments de proveïdors després del cobrament
description: En aquest tema s'explica com s'utilitza l'escenari de pagament després del cobrament (PWP).
author: mukumarm
ms.date: 08/18/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: mukumarm
ms.openlocfilehash: d1fe8d92663b31b22dc405fc1f3e06d976e6c5dc
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 09/16/2022
ms.locfileid: "9525379"
---
# <a name="pay-when-paid-vendor-payments"></a>Pagaments de proveïdors després del cobrament

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

En aquest tema s'explica com s'utilitza l'escenari de pagament després del cobrament (PWP).

## <a name="create-a-purchase-order-that-has-pwp-terms"></a>Crear una comanda de compra que té condicions de PWP

Quan comptabilitzeu una factura d'un proveïdor, si el proveïdor està subjecte a condicions de PWP, aquestes condicions es mostren en les línies de la comanda de compra (PO). Per crear una comanda de compra que tingui termes de PWP, seguiu aquests passos.

1. Seguiu un d'aquests passos al Microsoft Dynamics 365 Finance:

    - Aneu a **Contractació i proveïment** \> **Comandes de compra** \> **Totes les comandes de compra**. A la subfinestra d'acció, seleccioneu **Nou**. Al quadre de diàleg **Crea una comanda de compra**, seleccioneu el proveïdor per al qual s'han configurat condicions de PWP al projecte, introduïu altres informacions necessàries i, a continuació, seleccioneu **D'acord**.
    - Aneu a **Administració de projectes i comptabilitat** \> **Projectes** \> **Tots els projectes**. A la subfinestra Acció, a la pestanya **Administra**, seleccioneu **Tasca d'element**. Seleccioneu la comanda de compra. Seleccioneu el proveïdor per al qual es configuren les condicions de PWP al projecte i, a continuació, seleccioneu **D'acord**.

2. A la pàgina **Comanda de compra**, a la pestanya **Línies de la comanda de compra**, seleccioneu **Afegeix una línia** per crear una línia de comanda de compra.
3. Seleccioneu el número d'element o la categoria de proveïment i introduïu els altres detalls necessaris. Reviseu els detalls de la línia de PO del proveïdor.

    L'opció **Pagament després del cobrament** se selecciona automàticament i el valor en el camp **Percentatge de llindar de PWP** es copia automàticament del camp **Percentatge de llindar de PWP** de la pàgina **Projectes**.

4. Si no voleu aplicar termes de PWP al proveïdor per a una línia de comanda de compra, desactiveu l'opció **Pagament després del cobrament**. En aquest cas, el camp **Percentatge de llindar de PWP** de la línia de la comanda de compra es restablirà a **0** (zero).
5. A la pàgina **Comanda de compra**, a la subfinestra Acció, a la pestanya **Compra**, seleccioneu **Confirma** per confirmar la comanda de compra.
6. A la subfinestra Acció, a la pestanya **Factura**, seleccioneu **Factura** per generar la factura per a la comanda de compra.

## <a name="create-a-project-invoice-proposal"></a>Crear una proposta de factura de projecte

Les propostes de factura de projecte s'utilitzen per crear factures de projecte per al client. A l'escenari de PWP, els pagaments a proveïdors depenen dels pagaments dels clients segons la configuració de PWP. Tanmateix, hi ha opcions que us permeten alliberar els pagaments sense pagaments dels clients, si us calen. Per crear una factura de projecte per al client, seguiu aquests passos.

1. A les aplicacions del Customer Engagement, aneu a **Projecte** \> **Projectes** i seleccioneu el projecte.
2. A la pestanya **Valors reals**, seleccioneu la línia de valor real generada per la PO que té el tipus de transacció **Vendes no facturades**. A continuació, seleccioneu **Llesta per facturar**.
3. Aneu a **Vendes** \> **Vendes** \> **Contracte del projecte** i seleccioneu el contracte del projecte.
4. A la subfinestra Acció, seleccioneu **Factura** per generar la factura de client.
5. Al Finance, aneu a **Administració i comptabilitat del projecte** \> **Periòdic** \> **Importa de la taula intermèdia** i seleccioneu **D'acord** per generar el llibre diari d'integració del Project Operations.
6. Aneu a **Administració de projectes i comptabilitat** \> **Factures** \> **Proposta de factura del projecte** i seleccioneu **Comptabilitza** per comptabilitzar la proposta de factura generada per al projecte.

## <a name="update-a-customer-payment-and-pay-the-vendor"></a>Actualitzar un pagament de client i pagar al proveïdor

Quan un proveïdor completa el seu treball en un projecte i us envia una factura, heu de revisar l'estat del projecte i les factures del client per determinar si les condicions de PWP s'han complert per al projecte. Si es compleixen els termes de PWP per al proveïdor, podeu determinar quines línies de la factura de proveïdor pagareu, en funció dels pagaments al client del projecte. Si decidiu pagar al proveïdor tot i que els termes de PWP no es van complir, podeu substituir els termes de PWP en la pàgina **Factura de proveïdor amb pagament després del cobrament**.

1. Al Finance, aneu a **Administració de projectes i comptabilitat** \> **Projectes** \> **Tots els projectes** i seleccioneu el projecte.
2. A la subfinestra Acció , seleccioneu **Control** i, a continuació, seleccioneu **Factures de proveïdor** per mostrar totes les factures de proveïdor que s'han generat per al projecte.
3. A la pàgina **Factures de proveïdor amb pagament després del cobrament**, en el camp de cerca, introduïu valors per trobar la factura de proveïdor que voleu revisar i seleccioneu **Cerca**.
4. Seleccioneu l'opció **Pagament després del cobrament** per visualitzar només les factures PWP.
5. A la pestanya ràpida **Línies de factura de proveïdor**, seleccioneu les línies que alliberar per al pagament.
6. Seleccioneu **Allibera el pagament del proveïdor**. L'opció **Pagament després del cobrament** s'esborra i el valor del camp **A punt per al pagament** canvia a **Sí**.
