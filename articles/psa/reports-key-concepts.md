---
title: Conceptes clau
description: En aquest tema s'enllaça a informació sobre els conceptes clau de l'administració de recursos al Project Service Automation.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
ms.topic: article
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
ms.openlocfilehash: 8e56523a9a2fbe8bc07e6d46062f4e1c20e6d2fa2244b32ff53e96d898b0086c
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6995074"
---
# <a name="key-concepts"></a>Conceptes clau

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

A la taula següent es defineixen els conceptes clau que s'utilitzen a l'aplicació del Dynamics 365 Project Service Automation.

| Concepte                    | Definició |
|----------------------------|------------|
| Membre de l'equip del projecte        | Com a part de l'equip del projecte, un membre d'un equip del projecte pot ser un recurs amb nom que tingui reserves, un recurs amb nom que no tingui reserves o un recurs genèric. Els recursos genèrics no tenen reserves, són locals per al projecte i no tenen restriccions de capacitat en els projectes. |
| Recurs genèric del projecte   | Un contenidor de recursos que us permet formar un equip i assignar personal a un pla de projecte sense haver de conèixer el recurs amb nom. El calendari del projecte s'utilitza com a calendari del recurs genèric. Es poden afegir recursos genèrics a un equip del projecte i assignar-los a tasques. |
| Hores reservades               | Les hores de recurs es reserven de manera fixa en un projecte per ajudar-vos a garantir que es completarà el treball del projecte. Les hores reservades es consumeixen des de la capacitat total del recurs. Les reserves només es fan de recursos amb nom, no de recursos genèrics. |
| Hores assignades             | Les hores de recurs s'assignen a tasques de la planificació del projecte. Les assignacions es poden fer de recursos amb nom o genèrics. Les assignacions poden ser independents de reserves. |
| Hores necessàries             | Capacitat que cal, però que encara no compleix un recurs amb nom. Les hores necessàries només són rellevants per als membres de l'equip genèric que han generat requisits de recurs. |
| Demanda                     | La càrrega de treball actual i entrant. Al Project Service Automation, la demanda es mostra com a requisits de recursos o sol·licituds de recursos. |
| Requisit de recursos       | Entitat que s'utilitza per capturar hores obligatòries, dates d'inici i d'acabament, habilitats, geografia i altres dimensions de preus per als recursos necessaris. Els requisits dels recursos es generen mitjançant els membres de l'equip del projecte o creats individualment. |
| Sol·licitud de recurs           | Entitat que s'utilitza com a "sobre" per dur a terme el requisit de recurs que ha de complir un administrador de recursos. |
| Funció de recurs per defecte      | La funció en què s'agrupa un recurs per al càlcul d'ús. El recurs se suposa que té les aptituds necessàries per a la funció i per satisfer l'objectiu d'ús per a aquesta funció. |
| Unitat d'organització de recurs | La unitat organitzativa a la qual s'assigna un recurs. |
| Perfil                    | Tasca, requisit o assignació d'hores a mesura que es descomponen en una distribució diària. Per exemple, una tasca de 5 dies i 40 hores es pot contar en vuit hores al dia durant cinc dies. |
| Visualització de conciliació        | Visualització que mostra les reserves i totes les assignacions de cada membre de l'equip del projecte. Aquesta visualització permet que l'administrador del projecte busqui qualsevol error de coincidència entre reserves i assignacions i prendre mesures correctives si es produeix una acció errònia. |
| Hores de feina                 | Entitat que s'utilitza per identificar la capacitat de recursos, i les hores hàbils i no hàbils. Aquesta entitat també s'anomena calendari de recursos. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]