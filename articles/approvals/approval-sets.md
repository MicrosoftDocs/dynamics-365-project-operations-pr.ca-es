---
title: Conjunts d'aprovacions
description: En aquest tema s'explica com es treballa amb els conjunts d'aprovació, les sol·licituds i els subconjunts d'aquestes operacions.
author: stsporen
ms.date: 02/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 6809e01d8c3c93841125d0100d898dc208577019
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8576212"
---
# <a name="approval-sets"></a>Conjunts d'aprovacions

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

Els conjunts d'aprovació agrupen les sol·licituds d'aprovació en subconjunts d'operacions més petits. Aquest agrupament permet processar les aprovacions per projecte en un ordre específic i tornar a provar i seqüenciar. L'agrupació de les sol·licituds d'aprovació millora la fiabilitat i la traçabilitat del processament d'aprovacions per a grans volums d'aprovacions.

Els conjunts d'aprovació indiquen l'estat de processament global dels registres relacionats. Quan es processa un registre d'aprovació amb un conjunt d'aprovacions, el registre passarà d'**Enviat** a **Aprovat** i ja no s'enllaçarà amb el conjunt d'aprovació. Si es produeix un error en un registre en enviar-lo per a l'aprovació, el registre es queda en estat **Enviat** i el conjunt d'aprovació es marca com a erroni. El conjunt d'aprovació registra el missatge d'error de l'error.

## <a name="processing-approvals-and-approval-sets"></a>Processament d'aprovacions i conjunts d'aprovació
Les aprovacions que estan a la cua per al processament són visibles a la visualització **Aprovacions de processament**. El sistema processa totes les entrades de manera asíncrona diverses vegades, incloent-hi tornar a provar una aprovació si s'ha produït un error en els intents anteriors.

El camp **Vida del conjunt d'aprovació** registra el nombre d'intents restants per processar el conjunt abans que es marqui com a error.

Els conjunts d'aprovació es processen mitjançant l'activació periòdica basada en un **Servei de projecte anomenat** Cloud Flow **- Recurrently Schedule Project Approval Sets**. Això es troba a la **solució** anomenada **Operacions del projecte**. 

Assegureu-vos que el flux s'activi completant els passos següents.

1. Com a administrador, inicieu la sessió a [flow.microsoft.com](https://powerautomate.microsoft.com).
2. A l'extrem superior dret, canvieu a l'entorn que utilitzeu per a Dynamics 365 Project Operations.
3. Seleccioneu **Solucions** per llistar les solucions instal·lades a l'entorn.
4. A la llista de solucions, seleccioneu **Operacions** del projecte.
5. Canvia el filtre de **Tots** a fluxos **al** núvol.
6. Verifiqueu que el flux del **project Service - Planifica recurrentment el flux dels conjunts d'aprovació del** projecte està definit com a **Encitat**. Si no és així, seleccioneu el flux i, a continuació, seleccioneu **Activa**.
7. Verifiqueu que el processament es produeixi cada cinc minuts revisant la **llista Feines** **del sistema a l'àrea Configuració de l'entorn** Operacions Dataverse del projecte.

## <a name="failed-approvals-and-approval-sets"></a>Aprovacions i conjunts d'aprovació amb errors
A la visualització **Aprovacions amb error** s'enumeren totes les aprovacions que requereixen la intervenció de l'usuari. Obriu els registres del conjunt d'aprovació associats per identificar la causa de l'error.
Si seleccioneu **Torna-ho a provar**, el recompte de vida del conjunt d'aprovacions augmenta, el conjunt d'aprovacions torna a tenir l'estat **En processament** i s'intenta processar els registres restants.

## <a name="configure-approval-sets"></a>Configurar conjunts d'aprovacions

### <a name="enable-the-approval-sets-feature"></a>Habilitar la característica Conjunts d'aprovació
Abans d'habilitar la característica Conjunts d'aprovació, comproveu que no s'estiguin processant aprovacions actualment.

- Aneu a la pàgina **Paràmetres del projecte** i seleccioneu **Control de característiques** > **Habilita les aprovacions modernes**.

### <a name="turn-off-the-approval-sets-feature"></a>Desactivar la característica Conjunts d'aprovació
Abans de desactivar la característica Conjunts d'aprovació, comproveu que no s'estiguin processant aprovacions actualment.

- Aneu a la pàgina **Paràmetres del projecte** i seleccioneu **Control de característiques** > **Inhabilita les aprovacions modernes**.

### <a name="configuring-the-asynchronous-threshold"></a>Configurar el llindar asíncron 
Quan es creen conjunts d'aprovació, el processament es desplaça a segon terme quan el nombre de registres seleccionat per a la seva aprovació supera el llindar indicat. Utilitzeu el camp **Llindar asíncron** per configurar quan el processament d'aprovació s'ha d'executar de manera síncrona o asíncrona. Seleccioneu un dels valors següents:

  - Zero: totes les sol·licituds s'han de processar de manera asíncrona. 
  - Nombres majors que zero: les aprovacions es processen de manera asíncrona només quan el nombre d'aprovacions enviades supera aquest valor.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
