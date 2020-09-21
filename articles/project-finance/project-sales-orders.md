---
title: Comandes de vendes de projectes per a projectes de temps i materials
description: En aquest tema s'explica com crear comandes de vendes basades en projectes per a projectes de temps i materials.
author: KimANelson
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
ms.assetid: 05ab0cf6-318c-42de-ba56-3e662283497e
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 446c73e9491b1892847caf7e843c802292107ef9
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749449"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a>Comandes de vendes de projectes per a projectes de temps i materials

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

En aquest tema es descriu com crear una comanda de vendes per a un projecte. Les comandes de vendes només es poden crear per a projectes del tipus de **temps i materials**.

Si un projecte de temps i material té diverses fonts de finançament al contracte del projecte, heu d'habilitar el paràmetre **Permet les comandes de vendes per a projectes amb diverses fonts de finançament** a la pàgina **Paràmetres de l'administració de projectes i la comptabilitat**. 

> [!NOTE]
> - El suport per a les comandes de vendes de projectes amb diverses fonts de finançament està disponible a partir de la versió de l'aplicació 10.0.2 i versions posteriors.
> - El paràmetre per habilitar el suport per a les comandes de vendes de projectes amb diverses fonts de finançament se suprimirà a la fase de llançament d'abril de 2020, després de la qual la funcionalitat estarà sempre activada.

Podeu crear comandes de vendes basades en projectes de dues maneres diferents:

- Aneu al projecte en si mateix. A la subfinestra acció, seleccioneu **Administra > Tasques d'article > Comanda de vendes**. La informació del projecte es definirà per defecte a la comanda de vendes del projecte. Si el contracte del projecte té més d'una font de finançament, haureu de seleccionar la font de finançament per definir el client per a la comanda de vendes. Si només hi ha una font de finançament per al projecte, el client es definirà automàticament.
- Aneu a la pàgina de llista **Totes les comandes de vendes** i creeu una comanda de vendes nova. Haureu de seleccionar el projecte per a la comanda de vendes. Després de seleccionar el projecte, el client es definirà des de la font del finançament o haureu de seleccionar la font del finançament si el contracte del projecte té diverses fonts de finançament.

