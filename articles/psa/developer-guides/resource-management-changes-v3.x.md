---
title: Canvis a l'administració de recursos (Project Service Automation 3.x)
description: En aquest article s'ofereix informació sobre els canvis a l'àrea d'administració de recursos.
author: makk
ms.custom:
- dyn365-projectservice
ms.date: 03/18/2019
ms.topic: article
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: cac11606811632bdc48f462eb3a09a163ba1620d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916000"
---
# <a name="resource-management-changes-project-service-automation-3x"></a>Canvis a l'administració de recursos (Project Service Automation 3.x)

[!include [banner](../../includes/psa-now-project-operations.md)]

Les seccions d'aquest article proporcionen informació sobre els canvis que s'han fet a l'àrea d'administració de recursos de la Dynamics 365 Project Service Automation versió 3.x.

## <a name="project-estimates"></a>Estimacions del projecte

En lloc de basar-se en l'entitat **msdyn\_projecttask** (**Tasca del projecte**), les estimacions de projecte es basen en l'entitat **msdyn\_resourceassignment** (**Assignació de recursos**). Les assignacions de recursos s'ha convertit en l'"origen de la veritat" per a la planificació de tasques i els preus.

## <a name="line-tasks"></a>Tasques de línia

Al PSA 3.x, les tasques de línia són obsoletes. Ara, les assignacions apunten a la tasca sencera en comptes de les tasques de línia.

A l'exemple següent es mostra com s'assigna una tasca que s'anomena "Tasca de prova" als membres de l'equip A i B a les versions anteriors del PSA i al PSA 3.x.

- **Abans del PSA 3.x:**

    - Tasca de prova

        - Tasca de prova: tasca de línia 1

            - Assignació a A

        - Tasca de prova: tasca de línia 2

            - Assignació a B

- **PSA 3.x:**

    - Tasca de prova

        - Assignació a A
        - Assignació a B

## <a name="unassigned-assignment"></a>Assignació no assignada

Al PSA 3.x, una assignació no assignada és una assignació assignada a un membre de l'equip **NUL** i a un recurs **NUL**. Les assignacions no assignades poden produir-se en alguns escenaris:

- Si s'ha creat una tasca, però encara no s'ha assignat a cap membre de l'equip, sempre es crea una assignació no assignada. 
- Si se suprimeixen tots els assignats d'una tasca, una assignació no assignada es torna a crear per a aquesta tasca.

## <a name="scheduling-fields-on-the-project-task-entity"></a>Planificar camps a l'entitat Tasca del projecte

Els camps de l'entitat **msdyn\_projecttask** s'han deixat d'utilitzar o s'han mogut a l'entitat **msdyn\_resourceassignment**, o ara s'hi fa referència des de l'entitat **msdyn\_projectteam** (**Membre de l'equip del projecte**).

| Camp obsolet a msdyn\_projecttask (Tasca del projecte) | Camp nou a msdyn\_resourceassignment (Assignació de recursos) | Comentari |
|---|---|---|
| msdyn\_assignedresources | cap | |
| msdyn\_assignedteammembers | cap | |
| msdyn\_numberofresources | cap | |
| msdyn\_scheduledhours | cap | |
| msdyn\_effortcontour | msdyn\_plannedwork | El format de l'estructura de dades JavaScript Object Notation (JSON) que s'emmagatzema al camp ha canviat. |

## <a name="schedule-contour"></a>Contorn de planificació

El contorn de la planificació s'emmagatzema al camp **Treball planificat** (**msdyn\_plannedwork**) de cada entitat **Assignació de recursos** (**msdyn\_resourceassignment**).

### <a name="structure"></a>Estructura

La nova estructura del contorn de la planificació consta de porcions de temps flexibles que es defineixen per a cada dia de la planificació. Cada porció de temps té les següents propietats:

- **Inici**: l'inici de les hores de treball per al dia, segons el calendari del projecte.
- **Acabament**: l'acabament de les hores de treball per al dia, segons el calendari del projecte.
- **Hores**: el nombre d'hores que s'assignen al dia.

**Exemple**

Aquest exemple utilitza un calendari de projecte on la jornada laboral és de 9 a 5 hores a la zona horària UTC-8.

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

### <a name="auto-scheduling-and-manual-scheduling"></a>Planificació automàtica i programació manual

Si una tasca es planifica automàticament, les hores es carreguen de forma frontal i la duració de la tasca es pot reduir.

**Exemple**

La tasca següent es planifica automàticament per a 18 hores durant tres dies (del 3 de desembre de 2018 al 5 de desembre de 2018).

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

Si es planifica manualment una tasca, les hores es distribueixen de manera uniforme a totes les dates.

**Exemple**

La tasca següent es planifica manualment per a 18 hores durant tres dies (del 3 de desembre de 2018 al 5 de desembre de 2018).

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":6},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":6},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":6}]
```

### <a name="assignment-unit"></a>Unitat d'assignació

La unitat d'assignació ha quedat obsoleta al PSA 3.x. Les hores d'esforç de tasca ara es divideixen equitativament, per dia, entre tots els recursos assignats.

**Exemple**

En aquest exemple, la tasca s'assigna a dos recursos i es planifica automàticament per a 36 hores al llarg de tres dies (del 3 de desembre, 2018 al 5 de desembre de 2018).

- Assignació 1:

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

- Assignació 2:

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

## <a name="pricing-dimensions"></a>Dimensions de preus

Al PSA 3.x, els camps de dimensió de preus específics de recursos (com ara **Funció** i **Unitat organitzativa**) s'han suprimit de l'entitat **msdyn\_projecttask**. Ara, aquests camps es poden recuperar del membre de l'equip corresponent (**msdyn\_projectteam**) de l'assignació de recursos (**msdyn\_resourceassignment**) en el moment de generar estimacions del projecte. S'ha afegit un nou camp, **msdyn\_organizationalunit** a l'entitat **msdyn\_projectteam**.

| Camp obsolet a msdyn\_projecttask (Tasca del projecte) | Camp de msdyn\_projectteam (Membre de l'equip del projecte) que s'utilitza en comptes d'això |
|---|---|
| msdyn\_resourcecategory | msdyn\_resourcecategory |
| msdyn\_organizationalunit | msdyn\_organizationalunit |

## <a name="contours"></a>Contorns

Els camps de preus i estimació de contorn s'ha deixat d'utilitzar a l'entitat **msdyn\_projecttask**. S'han desplaçat a l'entitat **msdyn\_resourceassignment**.

| Camp obsolet a msdyn\_projecttask (Tasca del projecte) | Camp nou a msdyn\_resourceassignment (Assignació de recursos) |
|---|---|
| msdyn\_costestimatecontour | msdyn\_plannedcostcontour |
| msdyn\_salesestimatecontour | msdyn\_plannedsalescontour |

Els camps següents s'han desplaçat a l'entitat **msdyn\_resourceassignment**:

* msdyn\_plannedcost
* msdyn\_plannedsales

Els camps següents per al cost i les vendes previstos, reals i restants no es modifiquen a l'entitat **msdyn\_projecttask**:

* msdyn\_plannedcost
* msdyn\_plannedsales
* msdyn\_actualcost
* msdyn\_actualsales
* msdyn\_remainingcost
* msdyn\_remainingsales


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
