---
title: Assignar recursos que es poden reservar genèrics a una tasca i equip de projecte
description: En aquest tema es proporciona informació sobre la reserva de recursos genèrics a tasques i equips de projecte.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
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
ms.openlocfilehash: 684167f0a68872ef871fbaa06c5161e78045c9a5
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145391"
---
# <a name="assign-generic-bookable-resources-to-a-task-and-generate-resource-requirements"></a>Assignar recursos que es poden reservar genèrics i generar requisits de recursos 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

A més de reservar i assignar recursos reals al vostre projecte, podeu assignar recursos genèrics a tasques de projecte. Aquests recursos poden servir com a contenidors per als recursos amb nom fins que estigueu a punt per assignar personal al vostre projecte amb recursos amb nom. 

1. Al Project Service Automation (PSA), obriu la pàgina **Projecte** i a la pestanya **Planificació**, introduïu el nom del càrrec del recurs genèric a la cel·la **Recurs** de la planificació. O bé, feu clic a la icona **Recurs** a la cel·la per obrir el selector de recursos i escriviu el nom del recurs genèric que voleu crear.

![Creació i assignació d'un membre genèric de l'equip](media/RM-how-to-9.png)

S'obrirà la subfinestra **Creació ràpida: membre de l'equip del projecte**. 

2. Introduïu la funció i unitat d'organització del membre de l'equip de recursos genèric i, a continuació, feu clic a **Desa**.

![Creació ràpida de membres de l'equip genèrics](media/RM-how-to-10.png)

3. Després d'haver creat el nou membre de l'equip de recursos genèric, s'assigna a la tasca. Podeu continuar assignant aquest recurs genèric a altres tasques de la planificació de la tasca.

![Assignar membres de l'equip genèrics existents a tasques](media/RM-how-to-11.png)

4. Després d'assignar el recurs genèric, podeu generar un requisit de recurs i complir-lo reservant-lo directament o presentant una sol·licitud de recursos a un administrador de recursos.

![Generar un requisit per a un membre genèric de l'equip](media/RM-how-to-12.png)

A la quadrícula de membres de l'equip, a més de poder utilitzar el selector de recursos com s'ha esmentat anteriorment, podeu afegir recursos genèrics directament. Els recursos s'afegeixen amb un requisit de recurs que es basa en les dates d'inici/finalització i el mètode d'assignació especificat a la subfinestra **Creació ràpida: membre de l'equip del projecte**.

Podeu veure una diferència si afegiu directament el membre de l'equip genèric i, a continuació, assigneu més tasques al recurs genèric que les hores necessàries per cobrir. Feu clic a **Genera un requisit** per tornar a generar el requisit per equilibrar les hores necessàries contra assignacions.

També podeu fer clic a l'enllaç **Requisit de recursos** a la quadrícula de l'equip per obrir el requisit i afegir aptituds, recursos preferents, etc.

![Requisit de recursos](media/RM-how-to-13.png)

