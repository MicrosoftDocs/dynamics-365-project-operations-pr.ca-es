---
title: Conjunts d'aprovacions
description: En aquest tema s'explica com es treballa amb els conjunts d'aprovació, les sol·licituds i els subconjunts d'aquestes operacions.
author: stsporen
manager: tfehr
ms.date: 08/10/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 1d9333033eb2b03966c6531d0fd6ad5b878acd93
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323224"
---
# <a name="approval-sets"></a>Conjunts d'aprovacions

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

Els conjunts d'aprovació agrupen les sol·licituds d'aprovació en subconjunts d'operacions més petits. Aquest agrupament permet processar les aprovacions per projecte en un ordre específic i tornar a provar i seqüenciar. L'agrupació de les sol·licituds d'aprovació millora la fiabilitat i la traçabilitat del processament d'aprovacions per a grans volums d'aprovacions.

Els conjunts d'aprovació indiquen l'estat de processament global dels registres relacionats. Quan es processa un registre d'aprovació amb un conjunt d'aprovacions, el registre passarà d'**Enviat** a **Aprovat** i ja no s'enllaçarà amb el conjunt d'aprovació. Si es produeix un error en un registre en enviar-lo per a l'aprovació, el registre es queda en estat **Enviat** i el conjunt d'aprovació es marca com a erroni. El conjunt d'aprovació registra el missatge d'error de l'error.

## <a name="processing-approvals-and-approval-sets"></a>Processament d'aprovacions i conjunts d'aprovació
Les aprovacions que estan a la cua per al processament són visibles a la visualització **Aprovacions de processament**. El sistema processa totes les entrades de manera asíncrona diverses vegades, incloent-hi tornar a provar una aprovació si s'ha produït un error en els intents anteriors.

El camp **Vida del conjunt d'aprovació** registra el nombre d'intents restants per processar el conjunt abans que es marqui com a error.

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
