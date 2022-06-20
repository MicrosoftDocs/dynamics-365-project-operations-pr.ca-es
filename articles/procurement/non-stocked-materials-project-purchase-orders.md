---
title: Comanda de materials no mantinguts en existències per a un projecte amb comandes de compra del projecte
description: En aquest article s'explica com podeu demanar materials no emmagatzemats per a un projecte mitjançant ordres de compra de projectes.
author: sigitac
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: fe24faa143869af2396f3b0f28aae31417cadda7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929800"
---
# <a name="order-procurement-categories-or-non-stocked-materials-for-a-project-using-project-purchase-orders"></a>Categories de contractació de comandes o materials no emmagatzemats per a un projecte mitjançant ordres de compra de projectes

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

El departament de compres de l'organització podria utilitzar les [comandes de compra](/dynamics365/supply-chain/procurement/purchase-order-overview) per fer el seguiment de les comandes de béns i serveis. Les comandes de compra per a categories d'adquisició o materials no estoc es poden atribuir a un projecte. La facturació d'aquestes comandes de compra registra el cost al projecte.

## <a name="prerequisites"></a>Requisits previs
Completeu els passos següents per habilitar la funcionalitat de les comandes de compra del projecte.

1. Al Dynamics 365 Finance, aneu a l'àrea **de treball Gestió de** funcions.
2. A la llista de característiques, cerqueu i seleccioneu la característica **Habilita les comandes de compra de projecte al Project Operations per a escenaris basats en recursos/no mantinguts en existències**.
3. Seleccioneu **Habilita**.
4. Configureu els materials no mantinguts en existències i les factures de proveïdor pendents tal com s'explica a [Configurar materials no mantinguts en existències i les factures de proveïdor pendents](configure-materials-nonstocked.md).
5. Configureu les categories d'adquisició tal com es descriu a [Utilitza les categories d'adquisició amb ordres de compra de projectes i factures pendents de proveïdor](configure-procurement-categories.md).

## <a name="create-a-project-purchase-order-from-the-project-purchase-order-list"></a>Crear una comanda de compra de projecte des de la llista de comandes de compra del projecte

1. A Finances, aneu a **Administració de projectes i comptabilitat** > **Projectes** > **Tots els projectes** i seleccioneu un projecte.
2. A la subfinestra Acció, a la pestanya **Administra**, al grup **Nou**, seleccioneu **Tasta d'element** > **Comanda de compra**.
3. A la pàgina **Crea la comanda de compra**, seleccioneu el proveïdor amb el qual voleu fer la comanda de compra, introduïu la informació que calgui i, a continuació, seleccioneu **D'acord**.
4. A la pàgina **Comanda de compra**, a la quadrícula **Adquireix línies de comanda**, seleccioneu **Afegeix línia**.
5. Introduïu un número d'article o una categoria d'adquisició, quantitat, unitat, preu unitari i altra informació segons convingui.

    > [!NOTE]
    > Només es poden utilitzar categories d'adquisició, articles no proveïts i serveis amb ordres de compra de projectes. Els elements emmagatzemats no són compatibles.

6. Continueu afegint articles o categories de contractació segons calgui i confirmeu l'ordre de compra.

    Els rebuts de béns i serveis es poden registrar creant i comptabilitzant un rebut de producte.

    > [!NOTE]
    > Els rebuts de producte no es registren als valors reals del projecte al Microsoft Dataverse i no afecten el subllibre major del projecte.

    Quan un proveïdor envia la factura dels elements i serveis de la comanda de compra, el departament de compres pot generar una factura per a la comanda de compra anant a **Factura** > **Genera** > **Factura** a la subfinestra Accions. Per obtenir més informació sobre les factures de proveïdor pendents, vegeu [Adquirir materials no mantinguts en existències mitjançant una factura de proveïdor pendent](pending-vendor-invoices.md).
