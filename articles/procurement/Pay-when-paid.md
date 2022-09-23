---
title: Pagar quan es paguin pagaments al proveïdor
description: En aquest tema s'explica com utilitzar l'escenari de pagament quan es paga (PWP).
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
# <a name="pay-when-paid-vendor-payments"></a>Pagar quan es paguin pagaments al proveïdor

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

En aquest tema s'explica com utilitzar l'escenari de pagament quan es paga (PWP).

## <a name="create-a-purchase-order-that-has-pwp-terms"></a>Creeu una ordre de compra que tingui termes PWP

Quan publiqueu una factura d'un proveïdor, si el proveïdor està subjecte a termes PWP, aquests termes es mostren a les línies de l'ordre de compra (PO). Per crear una comanda de compra que tingui termes de PWP, seguiu aquests passos.

1. A Microsoft Dynamics 365 Finances, seguiu un d'aquests passos:

    - Aneu a **Contractació i proveïment** \> **Comandes de compra** \> **Totes les comandes de compra**. A la subfinestra d'acció, seleccioneu **Nou**. Al quadre de diàleg Crea una **ordre de** compra, seleccioneu el proveïdor per al qual es configuren els termes PWP al projecte, introduïu altra informació necessària i, a continuació, seleccioneu **D'acord**.
    - Aneu a **Administració de projectes i comptabilitat** \> **Projectes** \> **Tots els projectes**. A la subfinestra d'accions, a la **pestanya Administra**, seleccioneu **Tasca d'element**. Selecciona l'ordre de compra. Seleccioneu el proveïdor per al qual es configuren els termes PWP al projecte i, a continuació, seleccioneu **D'acord**.

2. A la **pàgina Comanda de** compra, a la **pestanya** Comanda de compra Ràpida, seleccioneu **Afegeix una línia** per crear una línia de comanda de compra.
3. Seleccioneu el número d'element o la categoria de contractació i introduïu els altres detalls necessaris. Reviseu els detalls de la línia de correu electrònic per al proveïdor.

    L'opció **Pagament després del cobrament** se selecciona automàticament i el valor en el camp **Percentatge de llindar de PWP** es copia automàticament del camp **Percentatge de llindar de PWP** de la pàgina **Projectes**.

4. Si no voleu aplicar termes de PWP al proveïdor per a una línia de comanda de compra, desactiveu l'opció **Pagament després del cobrament**. En aquest cas, el camp percentatge **llindar** PWP per a la línia PO es restablirà a **0** (zero).
5. A la pàgina Comanda de **compra**, a la subfinestra d'accions, a la **pestanya Compra**, seleccioneu **Confirma** per confirmar l'ordre de compra.
6. A la subfinestra d'accions, a la **pestanya Factura**, seleccioneu **Factura** per generar la factura de l'ordre de compra.

## <a name="create-a-project-invoice-proposal"></a>Crear una proposta de factura de projecte

Les propostes de factures de projecte s'utilitzen per crear factures de projecte per al client. En l'escenari PWP, els pagaments dels proveïdors depenen dels pagaments dels clients segons la configuració de PWP. Tot i això, hi ha opcions que us permeten alliberar els pagaments sense els pagaments dels clients segons necessiteu. Per crear una factura de projecte per al client, seguiu aquests passos.

1. A les aplicacions d'interacció amb el client, aneu a **Projectes** de projecte \>**i** seleccioneu el projecte.
2. A la **pestanya Actuals**, seleccioneu la línia real generada pel PO que té el **tipus de transacció de vendes** no contaminada. A continuació, seleccioneu **Preparats per a la factura**.
3. Accedeix al **contracte** del \>**·** \> **projecte** comercial i selecciona el contracte del projecte.
4. A la subfinestra d'accions, seleccioneu **Factura** per generar la factura del client.
5. A Finances, aneu a **Administració de projectes i comptabilitat** \> **Importació periòdica** \> **des de la taula** de posada en escena i seleccioneu **OK** per generar el diari d'integració d'operacions del projecte.
6. Aneu a **Gestió de projectes i comptabilitat** \> **Factures** \> **del projecte Proposta** de factura del projecte i seleccioneu **Publica** per publicar la proposta de factura que s'ha generat per al projecte.

## <a name="update-a-customer-payment-and-pay-the-vendor"></a>Actualitzar un pagament de client i pagar al proveïdor

Quan un proveïdor completa el seu treball en un projecte i us envia una factura, heu de revisar l'estat del projecte i les factures dels clients per determinar si s'han complert els termes PWP del projecte. Si es compleixen els termes de PWP per al proveïdor, podeu determinar quines línies de la factura de proveïdor pagareu, en funció dels pagaments al client del projecte. Si decidiu pagar al proveïdor tot i que els termes de PWP no es van complir, podeu substituir els termes de PWP en la pàgina **Factura de proveïdor amb pagament després del cobrament**.

1. A Finances, aneu a **Gestió de projectes i comptabilitat** \> **Tots** \> **els projectes** i seleccioneu el projecte.
2. A la subfinestra d'accions, seleccioneu **Control** i, a continuació, seleccioneu **Factures** de proveïdor per mostrar totes les factures de proveïdor que s'han generat per al projecte.
3. A la pàgina **Factures de proveïdor amb pagament després del cobrament**, en el camp de cerca, introduïu valors per trobar la factura de proveïdor que voleu revisar i seleccioneu **Cerca**.
4. Seleccioneu l'opció **Paga quan es paga** per veure només les factures PWP.
5. A la **pestanya Ràpid de línies de factures** de proveïdor, seleccioneu les línies que voleu publicar per al pagament.
6. Seleccioneu **Allibera el pagament** del proveïdor. L'opció **Pagament després del cobrament** s'esborra i el valor del camp **A punt per al pagament** canvia a **Sí**.
