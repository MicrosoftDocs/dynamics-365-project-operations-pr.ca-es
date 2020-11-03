---
title: Despeses entre empreses
description: Un treballador que estigui contractat per una entitat jurídica en una organització pot treballar per a una altra entitat jurídica de la mateixa organització. En aquesta situació, es pot utilitzar la funció de despesa entre empreses per assignar les despeses del treballador a l'entitat jurídica per a la qual es va realitzar el treball.
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072363"
---
# <a name="intercompany-expenses"></a>Despeses entre empreses

[!include [banner](../includes/banner.md)]

Un treballador que estigui contractat per una entitat jurídica en una organització pot treballar per a una altra entitat jurídica de la mateixa organització. En aquesta situació, es pot utilitzar la funció de despesa entre empreses per assignar les despeses del treballador a l'entitat jurídica per a la qual es va realitzar el treball. L'entitat jurídica que dona feina al treballador s'anomena entitat jurídica prestadora. L'entitat jurídica per a la qual el treballador incorre despeses s'anomena entitat jurídica prestatària. 

Abans que un treballador pugui crear i presentar despeses per al treball que es realitza per a una entitat jurídica diferent, a l'entitat jurídica prestadora, a l'opció **Paràmetres d'administració de despeses** , seleccioneu l'opció **Permet les línies de despesa entre empreses**. 

## <a name="tax-posting-for-intercompany-expenses"></a>Comptabilització d'impostos per a despeses entre empreses

[!include [banner](../includes/banner.md)]

Si voleu utilitzar grups d'impostos que estan associats amb l'entitat jurídica prestadora (origen) en lloc de l'entitat jurídica prestatària (destinació) en el vostre informe de despeses, haureu de configurar-ho a la configuració d'impostos de vendes del llibre major general. Quan el paràmetre del llibre major general **Entitat jurídica per a la comptabilització d'impostos entre empreses** s'estableix a **Origen** i **Aplica les regles d'impostos de vendes** s'estableix a **No** , s'utilitzarà la combinació d'impostos per a l'entitat jurídica prestadora. Quan s'estableix el mateix paràmetre a **Destinació** , s'utilitzarà la combinació d'impostos per a l'entitat jurídica prestatària. Per a les entitats jurídiques dels Estats Units, quan el paràmetre s'estableix a **Origen** , el camp **Es pot rebre l'impost de vendes** també s'ha de configurar a la nova pàgina **Grups de comptabilització del llibre major**. El motor de comptabilitat utilitzarà la informació d'aquest camp per a l'entrada de la comptabilitat relacionada amb els impostos.   
El comportament és coherent per a les línies de despesa publicades amb o sense un projecte.  
