---
title: Despeses entre empreses
description: En aquest tema es proporciona informació sobre com utilitzar les despeses entre empreses per assignar les despeses d'un treballador a l'entitat legal per a la qual es va dur a terme la feina.
author: Surya Vaidyanathan
ms.date: 07/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 80ef42bf5274ff9a5c50e6dcb93995cfbbda40a66d7471f29ebf056086320640
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "7001194"
---
# <a name="intercompany-expenses"></a>Despeses entre empreses

Un treballador que estigui contractat per una entitat jurídica en una organització pot treballar per a una altra entitat jurídica de la mateixa organització. Podeu utilitzar les despeses entre empreses per assignar les despeses del treballador a l'entitat legal per a la qual es va dur a terme la feina. L'entitat jurídica que dona feina al treballador s'anomena entitat jurídica prestadora. L'entitat jurídica per a la qual el treballador incorre despeses s'anomena entitat jurídica prestatària. 

Perquè un treballador pugui crear i enviar despeses entre empreses, abans heu d'habilitar les línies de despeses entre empreses. A l'entitat legal que fa el préstec, a la pàgina **Paràmetres d'administració de despeses**, seleccioneu **Permet les línies de despeses entre empreses**. 

## <a name="tax-posting-for-intercompany-expenses"></a>Comptabilització d'impostos per a despeses entre empreses

[!include [banner](../includes/banner.md)]

Per poder utilitzar els grups d'impostos associats a l'entitat legal que fa el préstec (origen) en comptes de l'entitat legal que rep el préstec (destinació) de l'informe de despeses, heu d'habilitar la funcionalitat a la configuració de l'impost de vendes del llibre general. Quan el paràmetre **entitat legal per a la publicació d'impostos entre empreses** es defineix com a **Origen** i **Aplica les regles de fiscalitat per a les vendes** es defineix com a **No**, s'utilitza la combinació d'impostos de l'entitat legal que fa el préstec. Quan s'estableix el mateix paràmetre a **Destinació**, s'utilitzarà la combinació d'impostos per a l'entitat jurídica prestatària. Per a les entitats jurídiques dels Estats Units, quan el paràmetre s'estableix a **Origen**, el camp **Es pot rebre l'impost de vendes** també s'ha de configurar a la nova pàgina **Grups de comptabilització del llibre major**. El motor de comptabilitat utilitzarà la informació d'aquest camp per a l'entrada de la comptabilitat relacionada amb els impostos.   
El comportament és coherent per a les línies de despesa publicades amb o sense un projecte.  

## <a name="new-expense-expression-builder"></a>Nou generdor d'expressions de despeses

El nou generdor d'expressions de despeses aborda els casos de despeses entre empreses que utilitzen els projectes. Aquesta característica garanteix que, quan creeu una despesa entre empreses, la política de despeses es valida correctament amb el projecte seleccionat a la línia de despeses i també que l'informe de despeses s'envïi correctament.

Per tal que la característica del generdor d'expressions de despeses funcioni, ha d'estar activada. A més, s'ha de configurar la política de despeses que té un ID del projecte.

Si ja heu configurat polítiques que validen l'ID del projecte a la línia de despeses, aquestes polítiques s'han de retirar. Més endavant podeu activar la característica i tornar a configurar les normes.

Per activar la característica, seguiu aquests passos.

1. Aneu a **Àrees de treball** \> **Administració de característiques**.
2. A la llista, seleccioneu **Nou generdor d'expressions de despeses per abordar els casos de despeses entre empreses que utilitzen els projectes**. A continuació, seleccioneu **Habilita ara**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
