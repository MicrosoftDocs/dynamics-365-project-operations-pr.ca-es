---
title: Configuració de la retenció de proveïdors
description: En aquest tema s'explica com es configura la retenció de proveïdors.
author: sigitac
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: e0cd7669c7d6b916261e2c85cce0f24ff241a075
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8583692"
---
# <a name="set-up-vendor-retention"></a>Configuració de la retenció de proveïdors

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

Aquest tema proporciona informació sobre com es configura la retenció de proveïdors.

## <a name="set-up-a-vendor-retention-account-in-general-ledger"></a>Configurar un compte de retenció del proveïdor al llibre general

1. A Dynamics 365 Finance, aneu a **Comptes de configuració de publicació** > **del llibre** > **major general per a transaccions automàtiques**.
2. Afegiu una línia nova.
3. Al camp **Tipus de comptabilització**, seleccioneu **Retenció de proveïdor**.
4. Seleccioneu el compte principal per a la comptabilització de la retenció de proveïdor.

## <a name="create-vendor-retention-terms"></a>Crear termes de retenció de proveïdors

Utilitzeu la pàgina **Termes de retenció de proveïdor** per configurar i mantenir els termes de retenció per als pagaments de proveïdors. Escriviu el percentatge del pagament al proveïdor que voleu retenir i el percentatge dels imports retinguts anteriorment que s'han d'alliberar. Els imports es retenen automàticament en factures de proveïdors fins que el contracte arribi a l'estat de finalització especificat. Després de configurar les condicions de retenció per a un proveïdor, podeu aplicar-los a qualsevol projecte en què treballi el proveïdor.

1. A Finances, aneu a **Administració de projectes i comptabilitat** > **Configuració** > **Retenció** > **Condicions de retenció de pagaments de proveïdors**.
2. Seleccioneu **Nou** per afegir un nou terme de retenció de proveïdor. El valor del camp **ID de regla** del terme nou s'introdueix automàticament. 
3. Al camp **Descripció**, introduïu un nom descriptiu per al terme nou.
4. A la pestanya **Condicions**, seleccioneu **Afegeix línia** per introduir un terme de retenció del proveïdor.
5. Al camp **Percentatge d'unitats lliurades**, introduïu un percentatge de compliment de la regla. Els imports es retenen automàticament a les factures del proveïdor fins que la fase de finalització del projecte sigui igual al percentatge que introduïu. Per exemple, si introduïu 50,00, els imports es retenen fins que el projecte estigui completat al 50%.
6. Al camp **Percentatge que es retindrà**, introduïu el percentatge de l'import de la factura del proveïdor que voleu retenir. Per exemple, si introduïu 10,00 en aquest camp, el 10 per cent de l'import de les factures de proveïdor es reté fins que el projecte assoleix el percentatge de finalització que seleccioneu al camp **Percentatge d'unitats lliurades**.
7. Al camp **Percentatge que s'alliberarà**, introduïu el percentatge dels imports retinguts prèviament que s'han d'alliberar al nivell seleccionat de finalització del projecte.

> [!NOTE]
> Si teniu més d'una fita per a diferents nivells de finalització del projecte, introduïu una línia de període de condició de retenció de proveïdor diferent per a cada regla de retenció. Cada línia pot especificar un percentatge diferent que es retindrà i un percentatge diferent per alliberar per a cada nivell designat de finalització del projecte.

## <a name="set-up-a-vendor-agreement-for-the-project"></a>Configurar un acord de proveïdor per al projecte

Configureu els termes de retenció del proveïdor que s'aplicaran al projecte. Els termes de retenció del proveïdor també es mostren a les comandes de compra que creeu per al proveïdor.

1. A Finances, aneu a **Administració de projectes i comptabilitat** > **Projectes** > **Tots els projectes**. 
2. Seleccioneu un projecte i, a la subfinestra Acció, seleccioneu **Grup de projectes** > **Acords de proveïdor**.
3. A la pàgina **Acords de proveïdor**, afegiu una línia nova.
4. En el camp **Codi del compte**, seleccioneu una de les següents opcions:
   - **Taula**: els termes de retenció del proveïdor s'apliquen a un sol proveïdor.
   - **Grup**: els termes de retenció del proveïdor s'apliquen a tots els proveïdors d'un grup de proveïdors.
   - **Tots**: els termes de retenció del proveïdor s'apliquen a tots els proveïdors.
5. En el camp **Proveïdor/Grup de proveïdors**, seleccioneu el proveïdor o grup de proveïdors al qual s'apliquen els termes de retenció del proveïdor. Si seleccioneu **Tots** en el pas anterior, aquest camp no està disponible.
6. Al camp **Termes de retenció del proveïdor**, seleccioneu l'ID de regla per a les condicions de retenció que s'aplicaran a aquest proveïdor.

