---
title: Informació general del Project Service Automation
description: Aquest tema proporciona informació sobre la solució d'integració Dynamics 365 Project Service Automation a Dynamics 365 Finance.
author: ruhercul
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: ruhercul
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1b8588e664f140ca1b0dd740d27fe6a5137da595
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/04/2022
ms.locfileid: "8685504"
---
# <a name="project-service-automation-overview"></a>Informació general del Project Service Automation

[!include[banner](../includes/banner.md)]


La solució d'integració project Service Automation to Finance utilitza la funció d'integració de dades per sincronitzar dades entre instàncies de Dynamics 365 Finance i Dynamics 365 Project Service Automation via Common Data Service. Les plantilles d'integració que estan disponible amb la característica d'integració de dades permeten el flux de projectes, contractes de projecte, línies de contracte de projecte, fites de les línies de contracte del projecte, tasques del projecte, categories de transacció de despeses, estimacions d'hores i estimacions de despeses del Project Service Automation al Finance.

> [!NOTE]
> - Si utilitzeu la versió 7.3.0, heu d'instal·lar el KB 4074835. Podreu integrar projectes de preu fix.
> - Si utilitzeu la versió 7.3.0 i incorporeu transaccions de taxes del Project Service Automation, heu d'instal·lar el KB 4345320 per tal d'incloure aquestes taxes a la factura del projecte.
> - Si utilitzeu la versió 8.0, podreu utilitzar la integració de tasques de projecte, les categories de transaccions de despeses, les estimacions d'hores, les estimacions de despeses i el bloqueig de funcionalitats.
> - Si esteu utilitzant la versió 8.0.1 o posterior, podreu sincronitzar els valors reals.

Per poder integrar el Project Service Automation i el Finance, heu de configurar els paràmetres d'integració del Project Service Automation. Per a més informació, vegeu [Paràmetres d'integració del Project Service Automation](PSA-parameters.md).

Aquesta solució d'integració permet la sincronització directa en els següents escenaris:

- Mantenir els contractes de projecte al Project Service Automation i sincronitzar-los directament del Project Service Automation al Finance.
- Crear projectes al Project Service Automation i sincronitzar-los directament del Project Service Automation al Finance.
- Mantenir línies de contracte del projecte al Project Service Automation i sincronitzar-les directament del Project Service Automation al Finance.
- Mantenir fites de línies de contracte del projecte al Project Service Automation i sincronitzar-les directament del Project Service Automation al Finance.
- Mantenir tasques del projecte al Project Service Automation i sincronitzar-les directament del Project Service Automation al Finance.
- Mantenir categories de transacció de despeses al Finance i sincronitzar-les directament del Finance al Project Service Automation.
- Crear estimacions d'hores del projecte al Project Service Automation i sincronitzar-les directament del Project Service Automation al Finance.
- Crear estimacions de despeses del projecte al Project Service Automation i sincronitzar-les directament del Project Service Automation al Finance.
- Crear valors reals de temps, despeses i taxes al Project Service Automation i crear transaccions de projecte al diari d'integració del Project Service Automation per tal que es puguin comptabilitzar al Finance.

## <a name="data-synchronization"></a>Sincronització de les dades

A la il·lustració següent es mostren les dades que se sincronitzen com a part de la integració entre el Project Service Automation i el Finance.

> [!NOTE]
> No totes les plantilles estan disponibles actualment. Les plantilles es publicaran a mesura que es completin.

[![Integració del Project Service Automation amb el Finance.](./media/PSA-integration.png)](./media/PSA-integration.png)

## <a name="system-requirements-for-finance"></a>Requisits del sistema per al Finance

Per utilitzar la solució d'integració del Project Service Automation al Finance, heu d'instal·lar l'Enterprise Edition 7.3 amb l'actualització de la plataforma 12 o posterior.

## <a name="system-requirements-for-project-service-automation"></a>Requisits del sistema per al Project Service Automation

Per utilitzar la solució d'integració del Project Service Automation al Finance, heu d'instal·lar els components següents:

- Dynamics 365 Project Service Automation versió 9.0.0.0 o posterior
- Solució Donant potencial a ingressos per al Dynamics 365 Sales, versió 1.14.0.0 (v14) o posterior
- Solució Project Service Automation a Finance per al Dynamics 365 Project Service Automation, versió 1.0.0.0 o posterior

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a>Instal·lar la solució d'integració del Project Service Automation al Finance a la instància del Project Service Automation

Baixeu la solució d'integració del Project Service Automation al Finance des del [Centre de baixades de Microsoft](https://www.microsoft.com/download/details.aspx?id=57016) i seguiu les instruccions que s'inclouen amb la solució.


[!INCLUDE[footer-include](../includes/footer-banner.md)]