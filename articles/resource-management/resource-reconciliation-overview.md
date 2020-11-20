---
title: Informació general sobre la conciliació de recursos
description: En aquest tema es proporciona informació sobre com assegurar-se que les reserves de recursos i les assignacions als projectes estiguin alineades.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 574afac3bf5d1f6e5e13d8c61aa1ace6188f4008
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4125706"
---
# <a name="resource-reconciliation-overview"></a>Informació general sobre la conciliació de recursos

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

Per als membres de l'equip, les reserves i assignacions estan lleugerament vinculades. En altres paraules, els recursos poden tenir assignacions però no reserves, o poden tenir reserves però no assignacions. Idealment, les reserves i assignacions s'han d'alinear perquè els recursos tinguin capacitat confirmada de dur a terme l'assignació de tasques. No obstant, les reserves poden basar-se en la disponibilitat i els temps de treball podrien canviar a mesura que el projecte continua. Per tant, la lleugera vinculació de les reserves i les assignacions proporciona flexibilitat.

La pestanya **Conciliació** del formulari **Projecte** permet als administradors projectar les reserves dels membres de l'equip i els seus treballs per a equips de projectes.

La pestanya **Conciliació** també mostra les reserves i les assignacions al nivell de l'assignació de tasques individuals per a cada membre de l'equip. Es mostren les hores a les cel·les que representen períodes de temps de mesos a dies.

La pestanya també mostra un total de la xarxa global per al projecte, juntament amb una columna **Total**.

Per a cada recurs, la pestanya calcula la diferència entre les reserves dels membres de l'equip i un valor consolidat de les assignacions de tasques del membre de l'equip. Idealment, aquesta diferència hauria de ser 0 (zero). En altres paraules, no hi hauria d'haver diferències entre les reserves i les assignacions. Les diferències es marquen amb color i un ombrejat per cridar l'atenció sobre dues condicions:

- **Manca de reserves**: una manca de reserves es produeix quan un recurs té més assignacions que reserves. Com que aquesta capacitat no s'ha reservat, un administrador de projecte pot voler corregir aquesta situació ampliant les reserves del recurs fins a cobrir el dèficit.
- **Excés de reserves**: un excés de reserves es produeix quan un recurs s'ha reservat al projecte però no s'ha assignat a tasques. Aquesta situació podria ser acceptable en els casos en què s'ha reservat el recurs al projecte abans d'haver produït una assignació de tasques. No obstant, en altres casos, el recurs no està planificat per assignar-se a tasques. En aquests casos, l'administrador del projecte hauria de considerar la cancel·lació de les reserves del recurs, de manera que la capacitat pugui utilitzar-se per a un altre projecte.

En alguns casos, quan visualitzeu temps en un nivell superior al nivell de dia (per exemple, al nivell de mes), pot ser que vegeu una diferència neta de zero per a un recurs (en altres paraules, reserves = assignacions). No obstant, si visualitzeu temps al nivell de la setmana, podeu veure que hi ha assignacions de zero hores i reserves de 40 hores a la primera setmana, però assignacions de 40 hores i reserves de zero hores a la segona setmana. En general, les reserves i assignacions es concilien, però difereixen d'una setmana a la següent.

Quan visualitzeu el temps en nivells superiors, les cel·les de la pestanya **Conciliació** tenen un indicador per informar-vos que hi ha diferències en nivells inferiors. En fer doble clic en una cel·la, podeu apropar el zoom per visualitzar la diferència. A continuació, podeu fer clic amb el botó dret per allunyar-vos. En seleccionar un recurs i utilitzar el control **Diferència següent** a la barra d'eines de la quadrícula, podeu anar a la diferència següent entre les reserves i les assignacions d'aquest recurs. A continuació, podeu utilitzar el control **Diferència anterior** per tornar enrere. També podeu desactivar l'indicador de diferències i el comportament de la navegació a **Configuració**.


Si teniu assignacions de tasca per a un recurs però no hi ha cap reserva, a la pàgina **Projectes**, a la pestanya **Conciliació**, seleccioneu la manca de reserves i, a continuació, seleccioneu **Amplia la reserva**. El quadre de diàleg **Amplia la reserva** apareix i mostra la reserva necessària per fer front a la manca del recurs. També mostra les reserves existents del recurs en tots els projectes o altres entitats planificables. Si seleccioneu **D'acord** per crear la reserva del recurs, independentment de la disponibilitat del recurs, pot ser que hi hagi un excés de reserves.

L'administrador de projectes o administrador de recursos poden utilitzar el Tauler de planificació per administrar les situacions en què el recurs té un excés de reserves més enllà de la seva capacitat.

