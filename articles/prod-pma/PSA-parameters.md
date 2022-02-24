---
title: Paràmetres d'integració del Project Service Automation
description: Aquest tema explica com configurar com s'introdueixen les dades per defecte quan integreu el Microsoft Dynamics 365 for Project Service Automation amb el Microsoft Dynamics 365 Finance.
author: ruhercul
manager: AnnBe
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: ruhercul
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: b8faba1d799e360e58d47a02dc8b46e09fa0d393
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5270891"
---
# <a name="project-service-automation-integration-parameters"></a>Paràmetres d'integració del Project Service Automation

[!include[banner](../includes/banner.md)]

A la pàgina **Paràmetres d'integració del Project Service Automation** podeu configurar com s'introdueixen les dades per defecte quan integreu el Dynamics 365 Project Service Automation amb el Dynamics 365 Finance. Per tal que els projectes se sincronitzin correctament del Project Service Automation al Finance, heu de configurar els camps següents.

Per obrir la pàgina **Paràmetres d'integració del Project Service Automation**, aneu a **Administració de projectes i comptabilitat** \> **Configuració** \> **Paràmetres d'integració del Dynamics 365 for Project Service Automation**. 

> [!NOTE]
> - La integració de tasques de projecte, les categories de transaccions de despeses, les estimacions d'hores, les estimacions de despeses i el bloqueig de funcionalitats estan disponibles a la versió 8.0.
> - La integració dels valors reals del projecte està disponible a la versió 8.0.1 i posteriors.


| Tabulació                    | Camp                | Descripció |
|------------------------|----------------------|-------------|
| General                | Tipus de projecte per defecte | Seleccioneu el tipus de projecte per defecte. Quan se sincronitzen els projectes del Project Service Automation, aquest valor s'utilitza si no heu proporcionat cap valor per defecte a la plantilla d'integració. Durant la sincronització, el camp **Tipus de projecte** dels projectes nous es defineix en aquest valor. No obstant, el valor podria actualitzar-se quan les línies del contracte del projecte se sincronitzen amb el Project Service Automation. |
|                        | Categoria de temps        | Seleccioneu la categoria de temps per defecte. Aquest valor s'utilitza quan les estimacions d'hores se sincronitzen des del Project Service Automation. Quan les estimacions i els valors reals d'hores se sincronitzen des del Project Service Automation, el camp **Categoria** de les noves previsions d'hores de projecte al Finance es defineix en aquest valor. |
|                        | Categoria de taxa         | Seleccioneu la categoria de taxa per defecte. Aquest valor s'utilitza quan els valors reals de taxes se sincronitzen des del Project Service Automation. Quan els valors reals de taxes se sincronitzen des del Project Service Automation, el camp **Categoria** de les noves transaccions de taxes al Finance es defineix en aquest valor. |
| Valors per defecte del grup de projectes | Tipus de projecte         | Feu clic a **Nou** per afegir una fila en la qual pugueu seleccionar el tipus de projecte per definir el grup de projectes per defecte. Un tipus de projecte específic es pot seleccionar només una vegada a la configuració. |
|                        | Grup de projectes        | Seleccioneu el grup de projectes per defecte per al tipus de projecte seleccionat. Quan se sincronitzen nous projectes des del Project Service Automation, el camp **Grup de projectes** es defineix al valor per defecte per al tipus de projecte si no proporcioneu cap valor per defecte a la plantilla d'integració. |
| Valors per defecte del tipus de facturació  | Tipus de facturació         | Feu clic a **Nou** per afegir una fila en la qual pugueu seleccionar el tipus de facturació per definir la propietat de línia per defecte. Un tipus de facturació específic es pot seleccionar només una vegada a la configuració. |
|                        | Propietat de línia        | Seleccioneu la propietat de línia per defecte per al tipus de facturació seleccionat. Quan se sincronitzen noves estimacions d'hores, estimacions de despesa o valors reals des del Project Service Automation, el camp **Propietat de línia** es defineix al valor per defecte del tipus de facturació. |
| Bloqueig de funcionalitat  | No aplicable       | Seleccioneu la funcionalitat per inhabilitar al Finance per a projectes i contractes que tinguin l'origen al Project Service Automation. Per exemple, podeu desactivar la possibilitat d'editar contractes i projectes, crear estructures del desglossament del treball i introduir fulls d'hores al Finance. Els camps relacionats amb la comptabilitat continuaran habilitats, fins i tot si no estan disponibles segons la configuració. Per defecte, tota la funcionalitat està habilitada. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]