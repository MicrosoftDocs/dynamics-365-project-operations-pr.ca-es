---
title: Creació i aplicació de les condicions de retenció de pagaments de proveïdors
description: Aquest tema proporciona informació sobre com establir i mantenir els termes de retenció de pagaments de proveïdors.
author: Yowelle
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 1970a24a5073de6af43db1f1c068332c9ba9c8fe
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072349"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a>Creació i aplicació de les condicions de retenció de pagaments de proveïdors

[!include [banner](../includes/banner.md)] 

La configuració de termes de retenció de pagaments de proveïdors per a un projecte és útil quan la vostra organització vol retenir part dels pagaments realitzats a un proveïdor. Per exemple, quan voleu retenir el pagament al proveïdor fins que els productes lliurats compleixin les vostres expectatives. Els termes de retenció de pagaments del proveïdor es poden especificar quan negocieu un contracte de proveïdor.

## <a name="create-vendor-payment-retention-terms"></a>Crear termes de retenció de pagaments de proveïdors

Podeu introduir el percentatge de pagament del proveïdor per a la retenció i el percentatge dels imports retinguts prèviament que s'alliberaran. Els imports es retenen automàticament en factures de proveïdors fins que el contracte arribi a l'estat de finalització especificat. Després d'establir els termes de retenció, els podeu aplicar a qualsevol projecte per a aquest proveïdor.

Utilitzeu els passos següents per establir i mantenir els termes de retenció per als pagaments de proveïdors. 

1. Aneu a **Administració de projectes i comptabilitat** > **Retenció** > **Termes de retenció de pagaments de proveïdors**.
2. Seleccioneu **Nou** per afegir un nou terme de retenció de proveïdor. El valor **ID de regla** per al nou terme s'introdueix automàticament. 
3. Introduïu una breu descripció en el camp **Descripció** i, en el FastTab **Termes** , seleccioneu **Afegeix una línia** per introduir valors de termes per al següent:

   - **Percentatge d'unitats lliurades** : introduïu un percentatge de finalització per al terme. Els imports es retenen automàticament en factures de proveïdors fins que la fase de finalització del projecte és igual al percentatge especificat. Per exemple, si introduïu 50,00, els imports es retenen fins que el projecte estigui completat al 50%.
   - **Percentatge de retenció** : introduïu un percentatge de l'import de la factura del proveïdor que es retindrà. Per exemple, si introduïu 10,00, llavors el 10 per cent de l'import d'una factura de proveïdor es reté fins que el projecte arriba al percentatge de finalització establert en el camp **Percentatge d'unitats lliurades**.
   - **Percentatge per a l'alliberament** : seleccioneu **Afegeix una línia** per introduir un percentatge dels imports retinguts prèviament que s'han d'alliberar per al nivell seleccionat de finalització del projecte.

> [!NOTE]
> Si teniu més d'una fita per a diferents nivells de finalització del projecte, introduïu una línia separada de terme de retenció de proveïdors per a cada regla de retenció. Cada línia pot especificar un percentatge de retenció diferent i un percentatge de llançament diferent per a cada nivell designat de finalització del projecte.

Després de crear els termes de retenció de proveïdors per a un proveïdor, podeu aplicar els termes a un projecte.

## <a name="apply-vendor-retention-terms-to-a-project"></a>Aplicar els termes de retenció del proveïdor a un projecte

1. Aneu a **Administració de projectes i comptabilitat** > **Projectes** > **Tots els projectes** i obriu un projecte de la pàgina de llista de projectes.
2. Al FastTab **Acords de proveïdors** , seleccioneu **Afegeix una línia**.
3. En el camp **Codi del compte** , seleccioneu una de les següents opcions: 

   - **Taula** : els termes de retenció del proveïdor s'apliquen a un sol proveïdor.
   - **Grup** : els termes de retenció del proveïdor s'apliquen a tots els proveïdors d'un grup de proveïdors.
   - **Tots** : els termes de retenció del proveïdor s'apliquen a tots els proveïdors.

4. En el camp **Proveïdor/Grup de proveïdors** , seleccioneu el proveïdor o grup de proveïdors al qual s'apliquen els termes de retenció del proveïdor. Si seleccioneu **Tots** en el pas anterior, aquest camp no està disponible.
5. En el camp **Termes de retenció del proveïdor** , seleccioneu els termes de retenció que heu creat en el procediment anterior.
6. Si el projecte també té termes de pagament després del cobrament (PWP) establerts per al proveïdor, introduïu el percentatge de llindar per al projecte en el camp **Percentatge de llindar de PWP**.

Els termes de retenció del proveïdor també es mostren a les comandes de compra que creeu per al proveïdor.
