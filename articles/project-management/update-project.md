---
title: Actualització d'un projecte
description: En aquest tema es proporciona informació sobre l'actualització de projectes al Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 8bcbc6c5a62d252398d541649647fbad49006a0c
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131421"
---
# <a name="update-a-project"></a>Actualització d'un projecte

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

A continuació, es mostra un resum dels camps que es poden actualitzar en un projecte després d'haver-lo creat i altres implicacions aplicables a les actualitzacions.

## <a name="project-detail-fields"></a>Camps de detalls del projecte

- **Nom**: títol del projecte.
- **Descripció**: informació general del projecte.
- **Client**: empresa a la qual es lliurarà el projecte.
- **Plantilla de calendari**: hores de treball del projecte. Quan el camp canvia, es torna a calcular la planificació sencera.
- **Moneda**: moneda per al projecte. Aquest camp té com a valor per defecte la moneda definida a la unitat de contractació. Quan la unitat de contractació s'actualitza, el camp també s'actualitza.
- **Unitat de contractació**: unitat organitzativa que representa el grup d'empreses o la divisió que s'encarrega principalment de guanyar la venda i administrar el lliurament de treballs i serveis al client. 
- **Administrador del projecte**: membre de l'equip del projecte que té l'autoritat de revisar i aprovar les entrades de temps i les despeses.

## <a name="estimate-fields"></a>Camps d'estimació

- **Data d'inici estimada**: la data en què començarà el projecte. Quan s'actualitzi aquest camp, qualsevol tasca del projecte es desplaçarà proporcionalment a la nova data d'inici.
- **Data de finalització**: data en què es preveu finalitzar el projecte.
- **Esforç**: esforç estimat del projecte. Quan s'afegeixen tasques al projecte, aquest camp ja no es pot editar.
- **Cost de treball estimat**: cost del treball previst del projecte. Quan s'afegeixen costos de treball al projecte, aquest camp ja no es pot editar.
- **Despeses estimades**: despeses estimades del projecte. Quan s'afegeixen despeses al projecte, aquest camp ja no es pot editar.

## <a name="project-actual-fields"></a>Camps reals del projecte
- **Inici real**: data en què es va iniciar el projecte.
- **Finalització real**: s'actualitzarà quan es completi un projecte.

## <a name="project-status-fields"></a>Camps d'estat del projecte

- **Estat global del projecte**: estat global del projecte proporcionat per l'administrador del projecte.
- **Comentaris**: text sobre l'estat actual del projecte que proporciona l'administrador del projecte.



[!INCLUDE[footer-include](../includes/footer-banner.md)]