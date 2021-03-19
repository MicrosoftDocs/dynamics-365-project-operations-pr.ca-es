---
title: Sincronitzar la capacitat dels recursos
description: Aquest tema proporciona informació sobre com sincronitzar la capacitat d'un recurs entre calendaris i projectes.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e6b63ccb5b0f04dedb8a942e22d6e1993204dc20
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288547"
---
# <a name="synchronize-resource-capacity"></a>Sincronitzar la capacitat dels recursos

[!include [banner](../includes/banner.md)]

Els processos per a la sincronització de recursos ajuden a garantir que la informació del calendari i el calendari base es transfereix en la planificació de recursos del projecte. Si el calendari canvia, els processos fan les actualitzacions necessàries a la planificació de recursos del projecte. Els processos també ajuden a millorar el rendiment, ja que la informació de recursos del calendari se sincronitza amb antelació. Per tant, les actualitzacions de la informació de planificació de recursos ocorren amb més rapidesa. Us recomanem que planifiqueu els processos com un lot en comptes d'un en un cada vegada. Altrament, hi ha un risc que algú oblidi les dates inclusives quan la informació s'ha sincronitzat per última vegada. Si no es fan servir dates inclusives, poden produir-se llacunes durant la sincronització de les dates.

![Sincronització del calendari](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a>Sincronització de la consolidació de capacitat de recursos

El procés de sincronització està dissenyat per sincronitzar tota la informació del calendari de recursos. Aquesta informació inclou informació del calendari base sobre qualsevol canvi que hi hagi a la taula de capacitat de calendari de recursos del projecte. Si s'afegeixen recursos nous al projecte, la sincronització ajuda a garantir que la informació actualitzada del calendari estigui disponible. Aquesta sincronització es pot fer en qualsevol moment.

Es recomana utilitzar un lot. Hi ha disponibles les opcions durant la sincronització de les reserves de capacitat.

1. Seleccioneu **Administració de projectes i comptabilitat** &gt; **Periòdic** &gt; **Sincronització de capacitat** &gt; **Sincronitza les consolidacions de capacitat de recursos**.
2. Definiu les opcions a la taula següent.

    | Opció      | Descripció |
    |-------------|-------------|
    | Codi de període | Opcionalment, seleccioneu el codi d'interval de dates del llibre major general per definir les dates d'inici i d'acabament per al procés de sincronització per a les consolidacions de capacitat de recursos. |
    | Data d'inici  | Introduïu la data d'inici del procés de sincronització per a la consolidació de capacitat de recursos. |
    | Data de finalització    | Introduïu la data de finalització del procés de sincronització per a la consolidació de capacitat de recursos. |

[![Procés de sincronització](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]