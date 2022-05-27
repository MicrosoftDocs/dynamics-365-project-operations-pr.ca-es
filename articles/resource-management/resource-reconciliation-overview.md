---
title: Informació general sobre la conciliació de recursos
description: Aquest tema proporciona informació que us ajudarà a garantir que les reserves i assignacions de recursos per a projectes estan alineades.
author: ruhercul
ms.date: 01/08/2021
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 0574a0402bc6b34ab82bbc223aeb3a0ffcc9df9c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580030"
---
# <a name="resource-reconciliation-overview"></a>Informació general sobre la conciliació de recursos

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

Per als membres de l'equip, les reserves i assignacions estan lleugerament vinculades. En altres paraules, els recursos poden tenir assignacions i cap reserva, o poden tenir reserves i cap assignació. Idealment, les reserves i assignacions s'han d'alinear perquè els recursos tinguin capacitat confirmada de dur a terme l'assignació de tasques. No obstant, les reserves poden basar-se en la disponibilitat i els temps de treball podrien canviar a mesura que el projecte continua. Per tant, la lleugera vinculació de les reserves i les assignacions proporciona flexibilitat.

La pestanya **Conciliació** a la pàgina **Projecte** permet als administradors projectar les reserves dels membres de l'equip i els seus treballs per a equips de projectes.

La pestanya **Conciliació** mostra les reserves i les assignacions al nivell de l'assignació de tasques individuals per a cada membre de l'equip. Les hores es mostren a les cel·les que representen períodes de temps de mesos a dies. La pestanya també mostra un total de la xarxa global per al projecte, juntament amb una columna **Total**.

Per a cada recurs, la pestanya **Reconciliació** calcula la diferència entre les reserves dels membres de l'equip i un valor consolidat de les assignacions de tasques del membre d'aquell equip. Idealment, aquesta diferència hauria de ser 0 (zero). En altres paraules, no hi hauria d'haver diferències entre les reserves i les assignacions. Les diferències es marquen amb color i un ombrejat per cridar l'atenció sobre dues condicions:

- **Manca de reserves**: una manca de reserves es produeix quan un recurs té més assignacions que reserves. Com que la capacitat no s'ha reservat, l'administrador de projecte pot voler corregir aquesta situació ampliant les reserves del recurs fins a cobrir el dèficit.
- **Excés de reserves**: un excés de reserves es produeix quan un recurs s'ha reservat al projecte però no s'ha assignat a tasques. Aquesta situació podria ser acceptable en casos en què s'ha reservat el recurs al projecte abans d'haver produït una assignació de tasques. Tanmateix, en altres casos en què no hi ha cap pla per assignar el recurs a les tasques, l'administrador del projecte hauria de tenir en compte la possibilitat de cancel·lar les reserves del recurs. D'aquesta manera, la capacitat es pot utilitzar per a un altre projecte.

En alguns casos, quan visualitzeu temps en un nivell superior al nivell de dia (per exemple, al nivell de mes), pot ser que vegeu una diferència neta de zero per a un recurs (en altres paraules, reserves vol dir assignacions). No obstant, si visualitzeu temps al nivell de la setmana, podeu veure que hi ha assignacions de zero hores i reserves de 40 hores a la primera setmana, però assignacions de 40 hores i reserves de zero hores a la segona setmana. En general, les reserves i assignacions es concilien, però difereixen d'una setmana a la següent.

Quan visualitzeu el temps en nivells superiors, les cel·les de la pestanya **Conciliació** tenen un indicador per informar-vos que hi ha diferències en nivells inferiors. En tocar dos cops o fer doble clic en una cel·la, podeu apropar el zoom per visualitzar la diferència. A continuació, podeu seleccionar i mantenir premut (o fer clic amb el botó dret) per allunyar-vos. En seleccionar un recurs i utilitzar el control **Diferència següent** a la barra d'eines de la quadrícula, podeu anar a la diferència següent entre les reserves i les assignacions d'aquest recurs. A continuació, podeu utilitzar el control **Diferència anterior** per tornar enrere. També podeu desactivar l'indicador de diferències i el comportament de la navegació a **Configuració**.

Si teniu assignacions de tasca per a un recurs però no hi ha cap reserva, seleccioneu la manca de reserves a la pestanya **Conciliació** de la pàgina **Projectes** i, a continuació, seleccioneu **Amplia la reserva**. El quadre de diàleg **Amplia la reserva** que apareix mostra la reserva requerida per fer front a la manca del recurs. El quadre de diàleg també mostra les reserves existents del recurs en tots els projectes o altres entitats planificables. Si seleccioneu **D'acord** per crear la reserva del recurs, independentment de la disponibilitat del recurs, pot ser que hi hagi un excés de reserves.

Les reserves creades mitjançant l'acció **Amplia la reserva** s'associen amb el requisit del projecte principal. Quan s'inicia una ampliació, els requisits específics que s'han d'ampliar no es poden determinar perquè el recurs es pot associar amb més d'un requisit per al projecte.

L'administrador de projectes o administrador de recursos pot utilitzar el tauler de planificació per administrar les situacions en què el recurs té un excés de reserves més enllà de la seva capacitat.


[!INCLUDE[footer-include](../includes/footer-banner.md)]