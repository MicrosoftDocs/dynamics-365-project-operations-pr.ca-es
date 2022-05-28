---
title: Crear i actualitzar un projecte
description: En aquest tema es proporciona informació sobre l'actualització de projectes al Project Operations.
author: ruhercul
ms.date: 10/20/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 07f96973a1341e65e648f126a931d72454334e9c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8592496"
---
# <a name="create-and-update-a-project"></a>Crear i actualitzar un projecte

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

El següent és un resum dels camps que es poden actualitzar en un projecte un cop s'ha creat. Això també inclou les implicacions aplicables a partir d'aquestes actualitzacions.

## <a name="project-detail-fields"></a>Camps de detalls del projecte

- **Nom**: títol del projecte.
- **Descripció**: informació general del projecte.
- **Client**: empresa a la qual es lliurarà el projecte.
- **Plantilla de calendari**: hores de treball del projecte. Quan el camp canvia, es torna a calcular la planificació sencera.
- **Moneda**: moneda per al projecte. El valor per defecte d'aquest camp es basa en la moneda que s'ha definit a la unitat de contracte. Quan la unitat de contractació s'actualitza, el camp també s'actualitza.
- **Unitat de contractació**: unitat organitzativa que representa el grup d'empreses o la divisió que s'encarrega principalment de guanyar la venda i administrar el lliurament de treballs i serveis al client.  Quan la unitat organitzativa del gestor de projectes no està definida, aquest camp per defecte té el valor definit als paràmetres del projecte.
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
