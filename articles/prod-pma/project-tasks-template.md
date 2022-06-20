---
title: Sincronitza les tasques del projecte directament des del Project Service Automation fins a les finances i operacions
description: En aquest article es descriu la plantilla i la tasca subjacent que s'utilitzen per sincronitzar les tasques del projecte directament des de Microsoft Dynamics 365 Project Service Automation Dynamics 365 Finance.
author: Yowelle
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 7b8ba77bbb08052952a8a557bb71300652dca3b2
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931134"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a>Sincronitza les tasques del projecte directament des del Project Service Automation fins a les finances i operacions

[!include[banner](../includes/banner.md)]

En aquest article es descriu la plantilla i la tasca subjacent que s'utilitzen per sincronitzar les tasques del projecte directament des de Dynamics 365 Project Service Automation Dynamics 365 Finance.

> [!NOTE]
> - La integració de tasques de projecte, les categories de transaccions de despeses, les estimacions d'hores, les estimacions de despeses i el bloqueig de funcionalitats estan disponibles a la versió 8.0.
> - Si utilitzeu l'Enterprise Edition 7.3.0 després d'instal·lar el KB 4132657 i el KB 4132660, podreu utilitzar les plantilles per integrar tasques de projecte, categories de transaccions de despeses, estimacions d'hores, estimacions de despeses i valors reals i configurar el bloqueig de funcionalitats. Si heu de reiniciar la distribució comptable, us recomanem que també instal·leu el KB 4131710.
> - La integració dels valors reals del projecte està disponible a la versió 8.0.1 i posteriors.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Flux de dades del Project Service Automation al Finance

La solució d'integració del Project Service Automation al Finance utilitza la característica d'integració de dades per sincronitzar dades entre les instàncies del Project Service Automation i el Finance. La plantilla d'integració que està disponible amb la característica d'integració de dades permet el flux de dades sobre tasques del projecte del Project Service Automation al Finance.

A la il·lustració següent es mostren les dades que se sincronitzen entre el Project Service Automation i el Finance.

[![Flux de dades per a la integració de Project Service Automation amb el Finance.](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)

## <a name="template-and-task"></a>Plantilla i tasca

Per accedir a la plantilla, al centre d'administració del Microsoft Power Apps, seleccioneu **Projectes** i, a continuació, a la cantonada superior dreta, seleccioneu **Nou projecte** per seleccionar les plantilles públiques.

La plantilla i la tasca subjacents següents s'utilitzen per sincronitzar les plantilles del projecte del Project Service Automation al Finance:

- **Nom de la plantilla en la integració de dades**: tasques del projecte (PSA a Fin and Ops)
- **Nom de la tasca del projecte:** tasques del projecte

Abans que es produeixi la sincronització de tasques del projecte, cal sincronitzar els contractes del projecte i els projectes.

## <a name="entity-set"></a>Conjunt d'entitats

| Project Service Automation | Finance                             |
|----------------------------|-------------------------------------|
| Tasques del projecte              | Entitat d'integració per a la tasca del projecte |

## <a name="entity-flow"></a>Flux d'entitat

Les tasques del projecte estan administrades al Project Service Automation i se sincronitzen amb el Finance com a activitats del projecte.

## <a name="prerequisites-and-mapping-setup"></a>Requisits previs i configuració de l'assignació

Abans que es produeixi la sincronització de tasques del projecte, cal sincronitzar els contractes del projecte i els projectes.

## <a name="power-query"></a>Power Query

Heu d'utilitzar Microsoft Power Query per a l'Excel per filtrar dades si es compleix aquesta condició:

- Teniu registres específics de recurs en una tasca del projecte.

Si heu d'utilitzar Power Query, seguiu aquesta guia:

- La plantilla Tasques del projecte (PSA a Fin and Ops) té un filtre per defecte que exclou els registres específics d'un recurs d'una tasca del projecte establint el filtre a **IsLineTask** com a **False**. Si creeu una plantilla pròpia, heu d'afegir aquest filtre.

## <a name="template-mapping-in-data-integration"></a>Assignació de plantilles a la integració de dades

A la il·lustració següent es mostra un exemple de les assignacions de tasques de plantilla a la integració de dades. L'assignació mostra la informació de camp que se sincronitzarà del Project Service Automation al Finance.

[![Assignació de plantilla.](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]