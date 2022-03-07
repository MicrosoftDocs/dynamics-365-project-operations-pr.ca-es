---
title: Despeses entre empreses
description: En aquest tema es proporciona informació sobre com utilitzar les despeses entre empreses per assignar les despeses d'un treballador a l'entitat legal per a la qual es va dur a terme la feina.
author: ShylaThompson
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d2cdba8d5368a8b26bf4d98226bda76a58261cf0
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005059"
---
# <a name="intercompany-expenses"></a>Despeses entre empreses

Un treballador que estigui contractat per una entitat jurídica en una organització pot treballar per a una altra entitat jurídica de la mateixa organització. Podeu utilitzar les despeses entre empreses per assignar les despeses del treballador a l'entitat legal per a la qual es va dur a terme la feina. L'entitat jurídica que dona feina al treballador s'anomena entitat jurídica prestadora. L'entitat jurídica per a la qual el treballador incorre despeses s'anomena entitat jurídica prestatària. 

Perquè un treballador pugui crear i enviar despeses entre empreses, abans heu d'habilitar les línies de despeses entre empreses. A l'entitat legal que fa el préstec, a la pàgina **Paràmetres d'administració de despeses**, seleccioneu **Permet les línies de despeses entre empreses**. 

## <a name="tax-posting-for-intercompany-expenses"></a>Comptabilització d'impostos per a despeses entre empreses

[!include [banner](../includes/banner.md)]

Per poder utilitzar els grups d'impostos associats a l'entitat legal que fa el préstec (origen) en comptes de l'entitat legal que rep el préstec (destinació) de l'informe de despeses, heu d'habilitar la funcionalitat a la configuració de l'impost de vendes del llibre general. Quan el paràmetre **entitat legal per a la publicació d'impostos entre empreses** es defineix com a **Origen** i **Aplica les regles de fiscalitat per a les vendes** es defineix com a **No**, s'utilitza la combinació d'impostos de l'entitat legal que fa el préstec. Quan s'estableix el mateix paràmetre a **Destinació**, s'utilitzarà la combinació d'impostos per a l'entitat jurídica prestatària. Per a les entitats jurídiques dels Estats Units, quan el paràmetre s'estableix a **Origen**, el camp **Es pot rebre l'impost de vendes** també s'ha de configurar a la nova pàgina **Grups de comptabilització del llibre major**. El motor de comptabilitat utilitzarà la informació d'aquest camp per a l'entrada de la comptabilitat relacionada amb els impostos.   
El comportament és coherent per a les línies de despesa publicades amb o sense un projecte.  


[!INCLUDE[footer-include](../includes/footer-banner.md)]