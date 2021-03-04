---
title: Sincronitzar categories de despeses del projecte entre el Finance and Operations i el Project Service Automation
description: Aquest tema descriu les plantilles i tasques subjacents que s'utilitzen per sincronitzar categories de despesa entre el Microsoft Dynamics 365 Finance i el Dynamics 365 Project Service Automation.
author: Yowelle
manager: AnnBe
ms.date: 07/20/2018
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
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: ed7ca3c85d3f99b7eefe10f4ddec822b9aeb1684
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072351"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a>Sincronitzar categories de despeses del projecte entre el Finance and Operations i el Project Service Automation

[!include[banner](../includes/banner.md)]

Aquest tema descriu les plantilles i tasques subjacents que s'utilitzen per sincronitzar categories de despesa entre el Dynamics 365 Finance i el Dynamics 365 Project Service Automation.

> [!NOTE]
> - La integració de tasques de projecte, les categories de transaccions de despeses, les estimacions d'hores, les estimacions de despeses i el bloqueig de funcionalitats estan disponibles a la versió 8.0.
> - La integració dels valors reals del projecte està disponible a la versió 8.0.1 i posteriors.
> - Si utilitzeu l'Enterprise Edition 7.3.0 després d'instal·lar el KB 4132657 i el KB 4132660, podreu utilitzar les plantilles per integrar tasques de projecte, categories de transaccions de despeses, estimacions d'hores, estimacions de despeses i valors reals i configurar el bloqueig de funcionalitats. Si heu de reiniciar la distribució comptable, us recomanem que també instal·leu el KB 4131710.

## <a name="data-flow-for-project-service-automation-and-finance"></a>Flux de dades per al Project Service Automation i el Finance

La solució d'integració del Project Service Automation i el Finance utilitza la característica d'integració de dades per sincronitzar dades entre les instàncies del Project Service Automation i el Finance. Les plantilles d'integració que estan disponibles amb la característica d'integració de dades permeten el flux de dades sobre les categories de transaccions de despeses de projecte entre el Project Service Automation i el Finance.

Si les categories de despeses del projecte es basen en el Finance, el flux d'integració és primer del Finance al Project Service Automation. Els identificadors d'integració de les categories de despesa del projecte s'actualitzen a través de la sincronització del Project Service Automation al Finance.

Si les categories de despeses del projecte es basen en el Project Service Automation, el flux d'integració és primer del Project Service Automation al Finance. Les categories del projecte s'han de configurar al Finance abans de la sincronització des del Project Service Automation. A continuació, sincronitzeu del Finance al Project Service Automation i després del Project Service Automation al Finance una altra vegada. D'aquesta manera, ajudareu a garantir que les categories estan enllaçades i que no es creen duplicats.

> [!NOTE]
> Normalment, les categories de despeses del projecte s'agrupen al Finance. No obstant, si no ho estan o si ja s'han creat categories de despeses al Project Service Automation, heu de sincronitzar-les abans mitjançant amb la plantilla Categories de transaccions de despeses del projecte (PSA a Fin and Ops). A continuació, sincronitzeu-les mitjançant la plantilla Categories de transacció de despeses del projecte (Fin and Ops a PSA). A continuació, hauríeu d'executar la sincronització del Project Service Automation al Finance una vegada més.
>
> Si sincronitzeu en primer lloc des del Project Service Automation, els requisits següents s'han de complir al Finance abans d'executar la sincronització:
>
> - La categoria compartida que coincideix amb la categoria de projecte que s'instal·la al Project Service Automation ha d'existir i s'ha d'habilitar per al **Projecte** i per a la **Despesa**.
> - Per a cada entitat jurídica del Finance que s'ha d'integrar, han d'existir les següents categories de projectes:
>
>     - **Categoria de projecte** existeix. 
>     - **Ús a la despesa** està habilitat.
>     - **Actiu al diari** està habilitat.
>     - **Tipus de transacció** està definit com a **Despesa**.

A la il·lustració següent es mostren les dades que se sincronitzen entre el Project Service Automation i el Finance.

[![Flux de dades per a la integració de Project Service Automation amb el Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a>Sincronització de categories de despeses del projecte del Finance al Project Service Automation

### <a name="template-and-task"></a>Plantilla i tasca

Per accedir a la plantilla, al centre d'administració del Microsoft Power Apps, seleccioneu **Projectes** i, a continuació, a la cantonada superior dreta, seleccioneu **Nou projecte** per seleccionar les plantilles públiques.

La plantilla i la tasca subjacent següents s'utilitzen per sincronitzar les categories de despesa del projecte del Finance al Project Service Automation:

- **Nom de la plantilla en la integració de dades** : categories de transaccions de despesa del projecte (Fin and Ops a PSA)
- **Nom de la tasca del projecte:** sincronització de categories al PSA

### <a name="entity-set"></a>Conjunt d'entitats

| Finance                           | Project Service Automation |
|-----------------------------------|----------------------------|
| Entitat d'integració per a les categories | Categories de transacció     |

### <a name="entity-flow"></a>Flux d'entitat

Les categories de despesa del projecte estan administrades al Finance i se sincronitzen amb el Project Service Automation com a categories de transacció.

### <a name="power-query"></a>Power Query

Quan estigueu sincronitzant al Project Service Automation, heu d'utilitzar el Microsoft Power Query per a l'Excel per definir el tipus de facturació a la categoria de la transacció. La plantilla Categories de transaccions de despesa del projecte (Fin and Ops a PSA) proporciona una columna i una assignació per defecte. Si creeu una plantilla pròpia, heu d'afegir una columna condicional al Power Query. Seguiu aquests passos.

1. Feu clic a la fletxa per obrir l'assignació de la tasca de categories de despesa del projecte a la plantilla Categories de transaccions de despesa del projecte (Fin and Ops a PSA).
2. Feu clic a l'enllaç **Consulta i filtratge avançats** per obrir el Power Query.
2. Seleccioneu **Afegeix una columna condicional**.
3. Introduïu un nom per a la columna nova, com ara **BillingType**.
4. Introduïu la condició següent: **if CATEGORYID not equal to null then 19235001, Otherwise null**.
5. A la columna , feu clic a **D'acord**.
6. Assegureu-vos d'assignar aquesta columna nova a la pàgina assignació.

A la il·lustració següent es mostra un exemple de l'assignació de tasques de plantilla a la integració de dades. L'assignació mostra la informació de camp que se sincronitzarà del Finance al Project Service Automation.

[![Assignació de plantilla de categoria de despesa al Project Service Automation](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a>Sincronització de categories de despeses del projecte del Project Service Automation al Finance

### <a name="template-and-task"></a>Plantilla i tasca

La plantilla i la tasca subjacent següents s'utilitzen per sincronitzar les categories de despesa del projecte del Project Service Automation al Finance:

- **Nom de la plantilla en la integració de dades** : categories de transaccions de despesa del projecte (PSA a Fin and Ops)
- **Nom de la tasca del projecte:** sincronització de categories al Fin Ops

### <a name="entity-set"></a>Conjunt d'entitats

| Project Service Automation | Finance                           |
|----------------------------|-----------------------------------|
| Categories de transacció     | Entitat d'integració per a les categories |

### <a name="entity-flow"></a>Flux d'entitat

Les categories de despesa del projecte estan administrades al Finance i se sincronitzen amb el Project Service Automation com a categories de transacció. L'actualització al Finance actualitza la categoria del projecte al Finance amb l'identificador d'integració del Project Service Automation.

### <a name="template-mapping-in-data-integration"></a>Assignació de plantilles a la integració de dades

A la il·lustració següent es mostra un exemple de l'assignació de tasques de plantilla a la integració de dades.

> [!NOTE]
> L'assignació mostra la informació de camp que se sincronitzarà del Project Service Automation al Finance.

[![Assignació de plantilla del Project Service Automation al Finance](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]