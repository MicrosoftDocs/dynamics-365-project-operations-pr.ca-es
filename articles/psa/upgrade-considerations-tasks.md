---
title: Consideracions d'actualització per a l'estructura del desglossament del treball
description: En aquest tema es proporciona informació sobre l'actualització de l'estructura del desglossament del treball del Project Service Automation 2.x al 3.x.
ms.custom:
- dyn365-projectservice
ms.date: 10/18/2019
ms.topic: article
author: ruhercul
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 13ad93d5be3c0ab07c81db28d3e13561e9d40017
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8599718"
---
# <a name="upgrade-considerations-for-the-work-breakdown-structure"></a>Consideracions d'actualització per a l'estructura del desglossament del treball

[!include [banner](../includes/psa-now-project-operations.md)]

En aquest tema es proporciona informació sobre l'actualització de l'estructura del desglossament del treball del Project Service Automation 2.x al 3.x. Aquest tema defineix l'estat saludable d'un projecte del Project Service Automation (PSA) necessari per a una actualització correcta. També hi ha informació sobre les condicions de bloqueig habituals que faran que falli l'actualització. Per obtenir més informació sobre la definició de tasques de projecte i les seves funcions dins d'una planificació del projecte, vegeu [Planificacions de projecte](project-creating.md).

## <a name="key-entities"></a>Entitats clau
Per a una estructura de desglossament del treball exacta que ja està carregada de recursos, són necessàries les entitats següents:

- [Projecte](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project)
- [Equip del projecte](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam)
- [Tasca del projecte](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask)
- [Assignacions de recursos](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment)
- [Dependència de les tasques del projecte](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency)
- [Recursos que es poden reservar](/dynamics365/customerengagement/on-premises/developer/entities/bookableresource)

Per definir una estructura del desglossament del treball carregada de recursos, heu de completar els passos següents:

1. Crear un projecte nou. Per obtenir més informació sobre com crear un projecte nou, vegeu [msdyn_project](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project).
2. Crear una o diverses tasques. Per obtenir més informació sobre com crear una tasca, vegeu [msdyn_projecttask](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask).
3. Definir les dependències de la tasca. Per obtenir més informació, vegeu [Dependència de la tasca del projecte](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency).
4. Assignar membres de l'equip del projecte al projecte. Per obtenir més informació, vegeu [msdyn_projectteam](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam).
5. Assignar membres de l'equip del projecte a les tasques. Per obtenir més informació, vegeu [msdyn_resourceassignment](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment).

## <a name="project-team-relationships"></a>Relacions de l'equip del projecte

Per garantir l'actualització correcta, les relacions següents s'han de mantenir correctament:
- Tots els membres de l'equip del projecte han d'estar associats amb un recurs que es pugui reservar.
- Tots els membres de l'equip del projecte han d'estar associats amb un recurs del mateix projecte. 

## <a name="project-task-relationships"></a>Relacions de les tasques del projecte
Per garantir l'actualització correcta, les relacions següents s'han de mantenir correctament:

- Les tasques relacionades s'han d'associar amb el mateix projecte.
- Cada tasca de línia ha de tenir una tasca principal.
- Cada tasca de línia ha de tenir un projecte principal.

### <a name="valid-conditions"></a>Condicions vàlides

- Totes les duracions de tasques han de ser superiors o iguals a (> =) una hora i menys de 1.800.000 minuts (1.250 dies).*
- Totes les tasques han de tenir una data d'inici no anterior al 01/01/2000.*
- Totes les tasques han de tenir una data d'inici que no sigui més enllà de 17 anys des del dia d'avui.*
- Totes les tasques han de tenir una data d'inici abans o igual a la seva data d'acabament.
- Tots els tipus de transaccions de les classificacions (despeses, materials, impostos i temps) han de tenir valors per a **Unitat per defecte** i **Grup d'unitats**.
- S'han d'evitar els formats de data amb lletres.

### <a name="potential-mitigation-steps"></a>Possibles passos per a la mitigació
- Utilitzeu la cerca avançada per identificar tasques del projecte que no contenen cap identificador de projecte.
- Utilitzeu la cerca avançada per identificar tasques del projecte en què la duració programada és superior a > 1.800.000.
- Abans de fer canvis de les dades, heu d'investigar qualsevol personalització associada amb l'entitat que potser hagi fet que les dades estiguin en mal estat. Aquestes personalitzacions s'han d'abordar abans de continuar amb qualsevol actualització relacionada amb les dades.
- Per a les tasques identificades que han quedat òrfenes, considereu la possibilitat de suprimir aquestes tasques si no es necessiten o si han d'estar associades amb el projecte principal correcte.
- Per a qualsevol tasca en què la duració sigui superior a 1.250 dies, considereu afegir diverses tasques per representar la duració total, si és factible.

> [!NOTE]
> Els elements que s'han assenyalat amb un asterisc (\*) tenen límits que es deuen al fet que l'administració de relacions entre proveïdors i associats (CRM) només admet 7.320 expansions de periodicitat. Heu d'estar per sota d'aquest límit.

## <a name="resource-assignment-relationships"></a>Relacions de l'assignació de recursos
Per garantir l'actualització correcta, les relacions següents s'han de mantenir correctament:

- Totes les assignacions de recursos d'una estructura del desglossament del treball han d'estar relacionades amb el mateix projecte.
- Totes les assignacions de recursos d'una estructura del desglossament del treball han d'estar associades als membres de l'equip del projecte del mateix projecte.

### <a name="potential-mitigation-steps"></a>Possibles passos per a la mitigació
- Identifiqueu totes les tasques que es troben fora de les condicions descrites anteriorment.  
- Qualsevol assignació de recursos que ja no sigui vàlida hauria de suprimir-se.

## <a name="project-task-dependency-relationships"></a>Relacions de dependència de les tasques del projecte
Per garantir l'actualització correcta, les relacions següents s'han de mantenir correctament:

- Totes les dependències de les tasques del projecte han d'estar relacionades amb el mateix projecte.
- Una tasca no pot tenir la mateixa dependència a la qual es fa referència més d'una vegada.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
