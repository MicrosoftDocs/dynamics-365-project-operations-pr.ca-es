---
title: Sincronitza els valors reals del projecte directament des del Project Service Automation al diari d'integració del projecte per enviar missatges a les finances i operacions
description: Aquest article descriu les plantilles i tasques subjacents que s'utilitzen per sincronitzar els valors reals del projecte directament des del Microsoft Dynamics 365 Project Service Automation a les finances i operacions.
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
ms.openlocfilehash: 34a0a0f7277777895077d221cd95e8d962d2a902
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028966"
---
# <a name="synchronize-project-actuals-directly-from-project-service-automation-to-the-project-integration-journal-for-posting-in-finance-and-operations"></a>Sincronitza els valors reals del projecte directament des del Project Service Automation al diari d'integració del projecte per enviar missatges a les finances i operacions

[!include[banner](../includes/banner.md)]

Aquest article descriu les plantilles i les tasques subjacents que s'utilitzen per sincronitzar els valors reals del projecte directament des del Dynamics 365 Project Service Automation al Dynamics 365 Finance.

La plantilla sincronitza les transaccions del Project Service Automation en una taula intermèdia al Finance. Un cop completada la sincronització, **haureu** d'importar les dades de la taula intermèdia al diari d'integració.

> [!NOTE]
> - La integració dels valors reals del projecte està disponible a partir de la versió 8.0.1.
> - Si utilitzeu l'Enterprise Edition 7.3.0 després d'instal·lar el KB 4132657 i el KB 4132660, podreu utilitzar les plantilles per integrar tasques de projecte, categories de transaccions de despeses, estimacions d'hores, estimacions de despeses i valors reals i configurar el bloqueig de funcionalitats. Si heu de reiniciar la distribució comptable, us recomanem que també instal·leu el KB 4131710.
> - Si utilitzeu la versió 7.3.0 i incorporeu transaccions de taxes del Project Service Automation, heu d'instal·lar el KB 4345320 per tal d'incloure aquestes taxes a la factura del projecte.
> - Si introduïu imports de l'impost sobre les vendes a transaccions de temps o de despesa al Project Service Automation, heu d'instal·lar l'actualització 7 del Project Service Automation. En cas contrari, els valors reals d'impostos no estaran enllaçats als valors reals d'hores o despeses associats i no se sincronitzaran al Finance. Poseu-vos en contacte amb el Servei tècnic per obtenir més informació.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Flux de dades del Project Service Automation al Finance

La solució d'integració del Project Service Automation al Finance utilitza la característica d'integració de dades per sincronitzar dades entre les instàncies del Project Service Automation i el Finance. Les plantilles d'integració que estan disponibles amb la característica d'integració de dades permeten el flux de dades sobre els valors reals del projecte del Project Service Automation al Finance.

A la il·lustració següent es mostren les dades que se sincronitzen entre el Project Service Automation i el Finance.

[![Flux de dades per a la integració del Project Service Automation amb les finances i operacions.](./media/ProjectActualsFlow.jpg)](./media/ProjectActualsFlow.jpg)

## <a name="project-actuals-from-project-service-automation"></a>Valors reals del Project Service Automation

### <a name="template-and-tasks"></a>Plantilla i tasques

Per accedir a les plantilles disponibles, al centre d'administració del Microsoft Power Apps, seleccioneu **Projectes** i, a continuació, a la cantonada superior dreta, seleccioneu **Nou projecte** per seleccionar les plantilles públiques.

La plantilla i les tasques subjacents següents s'utilitzen per sincronitzar els valors reals del projecte del Project Service Automation al Finance:

- **Nom de la plantilla en la integració de dades**: valors reals del projecte (PSA a Fin and Ops)
- **Nom de les tasques del projecte:**

    - Valors reals
    - TransactionConnections

### <a name="entity-set"></a>Conjunt d'entitats

| Project Service Automation | Finance                                   |
|----------------------------|----------------------------------------------------------|
| Valors reals                    | Entitat d'integració per a valors reals del projecte                   |
| Connexions de transacció    | Entitat d'integració per a les relacions de transaccions del projecte |

### <a name="entity-flow"></a>Flux d'entitat

Els valors reals del projecte estan administrats al Project Service Automation i se sincronitzen amb el diari d'integració del projecte al Finance. La comptabilitat s'aplicarà en funció de les dimensions financeres per defecte i la configuració de comptabilització.

### <a name="prerequisites"></a>Requisits previs

Abans que es puguin produir la sincronització de valors reals, heu de configurar els paràmetres d'integració del Project Service Automation i sincronitzar els projectes, les tasques de projecte i les categories de transaccions de despeses del projecte.

### <a name="power-query"></a>Power Query

A la plantilla de valors reals del projecte, heu d'utilitzar el Microsoft Power Query per a l'Excel per completar aquestes tasques:

- Transformar el tipus d'operació al Project Service Automation al tipus de transacció correcte al Finance. Aquesta transformació ja està definida a la plantilla Valors reals del projecte (PSA a Fin and Ops).
- Transformar el tipus de facturació al Project Service Automation al tipus de facturació correcte al Finance. Aquesta transformació ja està definida a la plantilla Valors reals del projecte (PSA a Fin and Ops). El tipus de facturació s'assigna a la propietat de línia, en funció de la configuració de la pàgina **Paràmetres d'integració del Project Service Automation**.
- Filtrar a unitats organitzatives de recursos específics que s'han de sincronitzar amb aquesta plantilla.
- Si el valors reals de temps entre empreses o despesa entre empreses se sincronitzaran al Finance, heu de transformar la unitat organitzativa del contracte a l'entitat jurídica correcta al Finance. A la plantilla Valors reals del projecte (PSA a Fin and Ops), una columna condicional es defineix a partir de les dades de demostració. Heu d'actualitzar l'última columna condicional inserida a les entitats jurídiques correctes. Altrament, pot ser que es produeixi un error d'integració o que s'importin transaccions reals incorrectes al Finance.
- Si el valors reals de temps entre empreses o despesa entre empreses no se sincronitzaran amb el Finance, heu de suprimir la darrera columna condicional inserida de la plantilla. Altrament, pot ser que es produeixi un error d'integració o que s'importin transaccions reals incorrectes al Finance.

#### <a name="contract-organizational-unit"></a>Unitat organitzativa del contracte
Per actualitzar la columna condicional inserida a la plantilla, feu clic a la fletxa **Assignació** per obrir l'assignació. Seleccioneu l'enllaç **Consulta i filtratge avançats** per obrir el Power Query.

- Si utilitzeu la plantilla Valors reals del projecte (PSA a Fin and Ops) per defecte, al Power Query, seleccioneu l'última **Condició inserida** de la secció **Passos aplicats**. A l'entrada **Funció**, substituïu **USSI** pel nom de l'entitat jurídica que s'ha d'utilitzar amb la integració. Afegiu condicions addicionals a l'entrada **Funció** que necessiteu i actualitzeu la condició **else** d'**USMF** a l'entitat jurídica correcta.
- Si esteu creant una plantilla nova, heu d'afegir la columna per admetre les despeses i els temps entre empreses. Seleccioneu **Afegeix una columna condicional** i introduïu un nom per a la columna, com ara **LegalEntity**. Introduïu la condició per a la columna, on, if **msdyn\_contractorganizationalunitid.msdyn\_name** is \<organizational unit\>, then \<enter the legal entity\>; else null.

### <a name="template-mapping-in-data-integration"></a>Assignació de plantilles a la integració de dades

A les il·lustracions següents es mostra un exemple de l'assignació de tasques de plantilla a la integració de dades. L'assignació mostra la informació de camp que se sincronitzarà del Project Service Automation al Finance.

[![Assignació de plantilla: valors reals.](./media/ActualsMapping.jpg)](./media/ActualsMapping.jpg)

[![Assignació de plantilla: connexions de transacció.](./media/TransactionConnections.jpg)](./media/TransactionConnections.jpg)

## <a name="import-from-staging-table-after-integration-from-project-service-automation"></a>Importar des de la taula intermèdia després de la integració del Project Service Automation

S'ha d'executar el procés periòdic Importa des de la taula intermèdia després de la sincronització dels valors reals del Project Service Automation al Finance. Aquest procés importarà les transaccions del projecte de la taula intermèdia al diari d'integració del Project Service Automation, on s'aplica la comptabilitat i les transaccions importades es poden comptabilitzar. Us recomanem que executeu aquest procés en mode per lots; opcionalment es pot configurar per executar-se com un lot periòdic.

## <a name="update-actuals-from-finance"></a>Actualitzar els valors reals del Finance

### <a name="template-and-tasks"></a>Plantilla i tasques

La plantilla següent i les tasques subjacents s'utilitzen per sincronitzar el número del val i els impostos de vendes de les transaccions de projecte publicades del Finance al Project Service Automation:

- **Nom de la plantilla en la integració de dades**: actualització dels valors reals del projecte (Fin and Ops a PSA)
- **Nom de les tasques del projecte:**

    - Valors reals 
    - TransactionConnections

### <a name="entity-set"></a>Conjunt d'entitats

| Finance                                                  | Project Service Automation |
|----------------------------------------------------------|----------------------------|
| Entitat d'integració per a valors reals del projecte                   | Valors reals                    |
| Entitat d'integració per a les relacions de transaccions del projecte | Connexions de transacció    |

### <a name="entity-flow"></a>Flux d'entitat

Els valors reals del projecte estan administrats al Project Service Automation i se sincronitzen amb el diari d'integració del projecte al Finance. Després d'enviar els valors reals al Finance, s'actualitzen al Project Service Automation amb el número de val del Finance. Si s'han afegit impostos de vendes al Finance, els valors reals d'impostos nous es creen a Project Service Automation.

### <a name="power-query"></a>Power Query

A la plantilla d'actualització de valors reals del projecte, heu d'utilitzar el Power Query per completar aquestes tasques:

- Transformar el tipus d'operació al Finance al tipus de transacció correcte al Project Service Automation. Aquesta transformació ja està definida a la plantilla Actualització dels valors reals del projecte (Fin and Ops a PSA).
- Transformar el tipus de facturació al Finance al tipus de facturació correcte al Project Service Automation. Aquesta transformació ja està definida a la plantilla Actualització dels valors reals del projecte (Fin and Ops a PSA).

### <a name="template-mapping-in-data-integration"></a>Assignació de plantilles a la integració de dades

A les il·lustracions següents es mostren exemples de l'assignació de tasques de plantilla a la integració de dades. L'assignació mostra la informació de camp que se sincronitzarà del Finance al Project Service Automation.

[![Assignació de plantilla: actualització de valors reals.](./media/ActualsUpdateMapping.jpg)](./media/ActualsUpdateMapping.jpg)

[![Assignació de plantilla: actualització de transacció.](./media/TransactionConnectionsUpdate.jpg)](./media/TransactionConnectionsUpdate.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]