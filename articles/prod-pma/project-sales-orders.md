---
title: Comandes de vendes de projectes per a projectes de temps i materials
description: En aquest tema s'explica com crear comandes de vendes basades en projectes per a projectes de temps i materials.
author: Yowelle
manager: AnnBe
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 74a90ea0bdb8f760273c0f6b1c61bffcb70b6c8d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289042"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a>Comandes de vendes de projectes per a projectes de temps i materials

[!include[banner](../includes/banner.md)]

En aquest tema es descriu com crear una comanda de vendes per a un projecte. Les comandes de vendes només es poden crear per a projectes del tipus de **temps i materials**.

Si un projecte de temps i material té diverses fonts de finançament al contracte del projecte, heu d'habilitar el paràmetre **Permet les comandes de vendes per a projectes amb diverses fonts de finançament** a la pàgina **Paràmetres de l'administració de projectes i la comptabilitat**. 

> [!NOTE]
> - El suport per a les comandes de vendes de projectes amb diverses fonts de finançament està disponible a partir de la versió de l'aplicació 10.0.2 i versions posteriors.
> - El paràmetre per habilitar el suport per a les comandes de vendes de projectes amb diverses fonts de finançament se suprimirà a la fase de llançament d'abril de 2020, després de la qual la funcionalitat estarà sempre activada.

Podeu crear comandes de vendes basades en projectes de dues maneres diferents:

- Aneu al projecte en si mateix. A la subfinestra acció, seleccioneu **Administra > Tasques d'article > Comanda de vendes**. La informació del projecte es definirà per defecte a la comanda de vendes del projecte. Si el contracte del projecte té més d'una font de finançament, haureu de seleccionar la font de finançament per definir el client per a la comanda de vendes. Si només hi ha una font de finançament per al projecte, el client es definirà automàticament.
- Aneu a la pàgina de llista **Totes les comandes de vendes** i creeu una comanda de vendes nova. Haureu de seleccionar el projecte per a la comanda de vendes. Després de seleccionar el projecte, el client es definirà des de la font del finançament o haureu de seleccionar la font del finançament si el contracte del projecte té diverses fonts de finançament.



[!INCLUDE[footer-include](../includes/footer-banner.md)]