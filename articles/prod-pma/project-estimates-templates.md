---
title: Sincronitza les estimacions del projecte directament des de Project Service Automation fins a Finances i Operacions
description: Aquest tema descriu les plantilles i les tasques subjacents que s'utilitzen per sincronitzar les estimacions de l'hora del projecte i les estimacions de despeses del projecte directament des de Microsoft Dynamics 365 Project Service Automation Dynamics 365 Finance.
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
ms.openlocfilehash: 47de3556034227e072d14dc93908edec42cec93c
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/04/2022
ms.locfileid: "8684584"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a>Sincronitza les estimacions del projecte directament des de Project Service Automation fins a Finances i Operacions

[!include[banner](../includes/banner.md)]

Aquest tema descriu les plantilles i les tasques subjacents que s'utilitzen per sincronitzar les estimacions de l'hora del projecte i les estimacions de despeses del projecte directament des de Dynamics 365 Project Service Automation Dynamics 365 Finance.

> [!NOTE]
> - La integració de tasques de projecte, les categories de transaccions de despeses, les estimacions d'hores, les estimacions de despeses i el bloqueig de funcionalitats estan disponibles a la versió 8.0.
> - La integració dels valors reals del projecte està disponible a la versió 8.0.1 i posteriors.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Flux de dades del Project Service Automation al Finance

La solució d'integració del Project Service Automation al Finance utilitza la característica d'integració de dades per sincronitzar dades entre les instàncies del Project Service Automation i el Finance. Les plantilles d'integració que estan disponibles amb la característica d'integració de dades permeten el flux de dades sobre les estimacions d'hores de projecte i estimacions de despeses de projecte del Project Service Automation al Finance.

A la il·lustració següent es mostren les dades que se sincronitzen entre el Project Service Automation i el Finance.

[![Flux de dades per a la integració de Project Service Automation amb el Finance.](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)

## <a name="project-hour-estimates"></a>Estimacions d'hores del projecte

### <a name="template-and-tasks"></a>Plantilla i tasques

Per accedir a les plantilles disponibles, al centre d'administració del Microsoft Power Apps, seleccioneu **Projectes** i, a continuació, a la cantonada superior dreta, seleccioneu **Nou projecte** per seleccionar les plantilles públiques.

La plantilla i les tasques subjacents següents s'utilitzen per sincronitzar les estimacions d'hores del projecte del Project Service Automation al Finance:

- **Nom de la plantilla en la integració de dades**: estimacions d'hores del projecte (PSA a Fin and Ops)
- **Nom de les tasques del projecte:**

    - Relacions de transacció
    - Estimacions de despeses

### <a name="entity-set"></a>Conjunt d'entitats

| Project Service Automation | Finance                                       |
|----------------------------|-----------------------------------------------|
| Tasques del projecte              | Entitat d'integració per a estimacions d'hores del projecte |

### <a name="entity-flow"></a>Flux d'entitat

Les estimacions d'hores del projecte estan administrades al Project Service Automation i se sincronitzen amb el Finance com a previsions d'hores del projecte.

### <a name="prerequisites"></a>Requisits previs

Abans de la sincronització de les estimacions d'hores del projecte, cal sincronitzar els projectes, les tasques del projecte i les categories de transaccions de despeses del projecte.

### <a name="power-query"></a>Power Query

A la plantilla d'estimacions de l'hora del projecte, heu d'utilitzar Microsoft Power Query per a l'Excel per completar aquestes tasques:

- Definiu l'identificador del model de previsió per defecte que s'utilitzarà quan la integració creï previsions d'hores noves.
- Filtreu tots els registres específics del recurs a la tasca que no es podran integrar en previsions d'hores.
- Filtreu totes les files de categoria de transaccions buides. Si no completeu aquesta tasca, pot ser que es facin prediccions d'hores incorrectes.

#### <a name="set-the-default-forecast-model-id"></a>Definir l'identificador del model de previsió per defecte

Per actualitzar l'identificador del model de previsió per defecte a la plantilla, feu clic a la fletxa **Assignació** per obrir l'assignació. A continuació, seleccioneu l'enllaç **Consulta i filtratge avançats**.

- Si utilitzeu la plantilla Estimacions d'hores del projecte (PSA a Fin and Ops) per defecte, seleccioneu la **Condició inserida** a la llista de **Passos aplicats**. A l'entrada de **Funció**, substituïu **O\_previsió** pel nom de l'identificador del model de previsió que s'ha d'utilitzar amb la integració. La plantilla per defecte té un ID de model de previsió a partir de les dades de demostració.
- Si esteu creant una plantilla nova, heu d'afegir aquesta columna. A Power Query, seleccioneu **Afegeix una columna** condicional i introduïu un nom per a la columna nova, com **ara ModelID**. Introduïu la condició per a la columna, on, if Project task is not null, then \<enter the forecast model ID\>; else null.

#### <a name="filter-out-resource-specific-records"></a>Filtrar els registres específics de recurs

La plantilla Estimacions d'hores del projecte (PSA a Fin and Ops) té un filtre per defecte que elimina els registres específics d'un recurs. Si creeu una plantilla pròpia, heu d'afegir aquest filtre. Seleccioneu l'enllaç **Consulta i filtratge avançats** per filtrar a la columna **msdyn\_islinetask** per incloure només els registres amb **False**.

#### <a name="filter-out-empty-transaction-category-rows"></a>Filtrar les files de categoria de transaccions buides

Heu d'afegir un filtre per suprimir qualsevol fila que tingui categories de transaccions buides. Aquesta tasca és necessària, independentment de si utilitzeu la plantilla per defecte o creeu la vostra pròpia plantilla. Aquest filtre suprimeix les files de resum de Project Service Automation que podrien fer que la previsió d'hores al Finance fos incorrecta. Seleccioneu l'enllaç **Consulta i filtratge avançats** per filtrar els registres nuls a la columna **msdyn\_transactioncategory\_value**.

### <a name="template-mapping-in-data-integration"></a>Assignació de plantilles a la integració de dades

A la il·lustració següent es mostra un exemple de l'assignació de tasques de plantilla a la integració de dades. L'assignació mostra la informació de camp que se sincronitzarà del Project Service Automation al Finance.

[![Assignació de tasques de plantilla a la integració de dades.](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)

## <a name="project-expense-estimates"></a>Estimacions de despesa del projecte

### <a name="template-and-tasks"></a>Plantilla i tasques

La plantilla i les tasques subjacents següents s'utilitzen per sincronitzar les estimacions de despesa del projecte del Project Service Automation al Finance:

- **Nom de la plantilla en la integració de dades**: estimacions de despesa del projecte (PSA a Fin and Ops)
- **Nom de les tasques del projecte:**

    - Relacions de transacció 
    - Estimacions de despeses

### <a name="entity-set"></a>Conjunt d'entitats

| Project Service Automation | Finance                                                  |
|----------------------------|----------------------------------------------------------|
| Connexions de transacció    | Entitat d'integració per a les relacions de transaccions del projecte |
| Línies d'estimació             | Entitat d'integració per a estimacions de despesa del projecte         |

### <a name="entity-flow"></a>Flux d'entitat

Les estimacions de despesa del projecte estan administrades al Project Service Automation i se sincronitzen amb el Finance com a previsions de despesa del projecte.

### <a name="prerequisites"></a>Requisits previs

Abans de la sincronització de les estimacions de despesa del projecte, cal sincronitzar els projectes, les tasques del projecte i les categories de transaccions de despeses del projecte.

### <a name="power-query"></a>Power Query

A la plantilla d'estimacions de despeses del projecte, heu d'utilitzar Power Query per completar les tasques següents:

- Filtrar per incloure només els registres de la línia d'estimació de despesa.
- Definiu l'identificador del model de previsió per defecte que s'utilitzarà quan la integració creï previsions d'hores noves.
- Transformar els tipus de facturació.
- Transformar els tipus de transacció.

#### <a name="filter-to-include-only-expense-estimate-lines"></a>Filtrar per incloure només les línies d'estimació de despesa

La plantilla Estimacions de despesa de projecte (PSA a Fin and Ops) té un filtre per defecte que inclou només les línies de despesa a la integració. Si creeu una plantilla pròpia, heu d'afegir aquest filtre. Seleccioneu la tasca **Relacions de transacció** i, a continuació, feu clic a la fletxa **Assignació** per obrir l'assignació. Seleccioneu l'enllaç **Consulta i filtratge avançats**. Filtreu la columna **msdyn\_transactiontype1** per tal que inclogui només **msdyn\_estimateline**.

#### <a name="set-the-default-forecast-model-id"></a>Definir l'identificador del model de previsió per defecte

Per actualitzar l'identificador del model de previsió per defecte a la plantilla, seleccioneu la tasca **Estimacions de despesa** i feu clic a la fletxa **Assignació** per obrir l'assignació. Seleccioneu l'enllaç **Consulta i filtratge avançats**.

- Si utilitzeu la plantilla predeterminada d'estimacions de despeses del projecte (PSA a Fin i Ops), a Power Query, seleccioneu la primera **condició** inserida de la **secció Passos aplicats**. A l'entrada de **Funció**, substituïu **O\_previsió** pel nom de l'identificador del model de previsió que s'ha d'utilitzar amb la integració. La plantilla per defecte té un ID de model de previsió a partir de les dades de demostració.
- Si esteu creant una plantilla nova, heu d'afegir aquesta columna. A Power Query, seleccioneu **Afegeix una columna** condicional i introduïu un nom per a la columna nova, com **ara ModelID**. Introduïu la condició per a la columna, on, if Estimate line ID is not null, then \<enter the forecast model ID\>; else null.

#### <a name="transform-the-billing-types"></a>Transformar els tipus de facturació

La plantilla Estimacions de despesa del projecte (PSA a Fin and Ops) inclou una columna condicional que s'utilitza per transformar els tipus de facturació que es reben del Project Service Automation durant la integració. Si creeu una plantilla pròpia, heu d'afegir aquesta columna condicional. Seleccioneu l'enllaç **Consulta i filtratge avançats** i, a continuació, seleccioneu **Afegeix una columna condicional**. Introduïu un nom per a la columna nova, com ara **BillingType**. Introduïu la condició següent:

If **msdyn\_billingtype** = 192350000, then **NonChargeable**  
else if **msdyn\_billingtype** = 192350001, then **Chargeable**  
else if **msdyn\_billingtype** = 192350002, then **Complimentary**  
else **NotAvailable**

#### <a name="transform-the-transaction-types"></a>Transformar els tipus de transacció

La plantilla Estimacions de despesa del projecte (PSA a Fin and Ops) inclou una columna condicional que s'utilitza per transformar els tipus de transacció que es reben del Project Service Automation durant la integració. Si creeu una plantilla pròpia, heu d'afegir aquesta columna condicional. Seleccioneu l'enllaç **Consulta i filtratge avançats** i, a continuació, seleccioneu **Afegeix una columna condicional**. Introduïu un nom per a la columna nova, com ara **TransactionType**. Introduïu la condició següent:

If **msdyn\_transactiontypecode** = 192350000, then **Cost**  
else if **msdyn\_transactiontypecode** = 192350005, then **Sales**  
else **null**

### <a name="template-mapping-in-data-integration"></a>Assignació de plantilles a la integració de dades

A les il·lustracions següents es mostren exemples de l'assignació de tasques de plantilla a la integració de dades. L'assignació mostra la informació de camp que se sincronitzarà del Project Service Automation al Finance.

[![Assignació de plantilles de transaccions d'estimació de despeses.](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)

[![Assignació de plantilles d'estimacions de despeses.](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]