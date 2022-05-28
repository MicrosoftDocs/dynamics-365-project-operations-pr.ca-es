---
title: Conjunts d'aprovacions al Project Service Automation
description: En aquest tema es proporciona informació sobre els conjunts d'aprovació, les sol·licituds i els subconjunts d'aquestes operacions.
author: stsporen
manager: tfehr
ms.date: 05/28/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 0783441d3bf7ed80192a3890a2e297fea05fe425
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8583296"
---
# <a name="approval-sets-in-project-service-automation"></a>Conjunts d'aprovacions al Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Els conjunts d'aprovació agrupen les sol·licituds d'aprovació en subconjunts d'operacions més petits. Aquest agrupament permet processar les aprovacions per ordre al projecte i permet tornar a provar i seqüenciar. L'agrupació millora la fiabilitat i la traçabilitat del processament d'aprovacions per a grans volums d'aprovacions.

Els conjunts d'aprovació indiquen l'estat de processament global dels registres relacionats. Quan es processa un registre d'aprovació amb un conjunt d'aprovació, el registre passarà de l'estat **Enviat** a **Aprovat** i es desenllaçarà del conjunt d'aprovació. Si es produeix un error en un registre en enviar-lo per a l'aprovació, el registre es queda en estat **Enviat** i el conjunt d'aprovació es marca com a erroni. El conjunt d'aprovació registra el missatge d'error de l'error.

## <a name="processing-approvals-and-approval-sets"></a>Processament d'aprovacions i conjunts d'aprovació
Les aprovacions que estan a la cua per al processament són visibles a la visualització **Aprovacions de processament**. El sistema intenta processar totes les entrades de manera asíncrona diverses vegades, incloent-hi tornar a intentar una aprovació si s'ha produït un error en els intents anteriors.

El camp **Vida del conjunt d'aprovació** registra el nombre d'intents restants per processar el conjunt abans que es marqui com a error.

## <a name="failed-approvals-and-approval-sets"></a>Aprovacions i conjunts d'aprovació amb errors
A la visualització **Aprovacions amb errors** s'enumeren totes les aprovacions que requereixen la intervenció de l'usuari. Obriu els registres del conjunt d'aprovació associats per identificar la causa de l'error.
Si seleccioneu **Torna-ho a provar**, el recompte de vida del conjunt d'aprovacions augmenta, el conjunt d'aprovacions torna a tenir l'estat **En processament** i s'intenta processar els registres restants.

## <a name="configure-approval-sets"></a>Configurar conjunts d'aprovacions

###  <a name="enable-the-approval-sets-feature"></a>Habilitar la característica Conjunts d'aprovació
Abans d'habilitar la característica Conjunts d'aprovació, comproveu que no s'estiguin processant aprovacions actualment.

- Aneu a la pàgina **Paràmetres del projecte** i seleccioneu **Control de característiques** > **Habilita les aprovacions modernes**.

### <a name="turn-off-the-approval-sets-feature"></a>Desactivar la característica Conjunts d'aprovació
Abans de desactivar la característica Conjunts d'aprovació, comproveu que no s'estiguin processant aprovacions actualment.

- Aneu a la pàgina **Paràmetres del projecte** i seleccioneu **Control de característiques** > **Inhabilita les aprovacions modernes**.

### <a name="configuring-the-asynchronous-threshold"></a>Configurar el llindar asíncron 
Quan es creen conjunts d'aprovació, el processament es desplaça a segon terme quan el nombre de registres seleccionat per a la seva aprovació supera el llindar indicat. Utilitzeu el camp **Llindar asíncron** per configurar quan el processament d'aprovació s'ha d'executar de manera síncrona o asíncrona.
Els valors vàlids són:

  - Zero: totes les sol·licituds s'han de processar de manera asíncrona. 
  - Nombres majors que zero: les aprovacions es processen de manera asíncrona només quan el nombre d'aprovacions enviades supera aquest valor.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
