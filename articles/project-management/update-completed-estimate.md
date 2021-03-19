---
title: Actualització de l'estimació en finalitzar
description: En aquest tema es proporciona informació sobre l'actualització de la projecció de l'esforç en un projecte.
author: ruhercul
manager: AnnBe
ms.date: 09/20/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 0e63bdb815a6f758c57d055c8c03d92e04700445
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286416"
---
# <a name="update-estimate-at-completion"></a>Actualització de l'estimació en finalitzar

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

És habitual que un administrador de projecte revisi les estimacions originals d'una tasca. Les reprojeccions de projectes són la percepció de les estimacions d'un administrador de projecte, donat l'estat actual del projecte. No obstant, no recomanem que els administradors de projectes canviïn els números de la línia de base, ja que la línia de base del projecte representa la font de veritat establerta de l'estimació de la planificació i el cost del projecte, i totes les parts interessades del projecte l'han acordat.

Hi ha dues maneres de fer que un administrador del projecte pugui tornar a projectar l'esforç de les tasques:

- Substituir l'estimació per finalitzar (ETC) per defecte amb una nova estimació de l'esforç real restant de la tasca. 
- Substituir el percentatge de progrés per defecte amb una nova estimació del progrés real de la tasca.

Cadascuna d'aquestes aproximacions provoca un nou càlcul de l'ETC de la tasca, l'estimació en finalitzar (EAC) i el percentatge de progrés, i la variació de l'esforç projectat d'una tasca. Es torna a calcular l'EAC, l'ETC i el percentatge de progrés de les tasques de resum, i produeixen una nova projecció de la variació d'esforç.


[!INCLUDE[footer-include](../includes/footer-banner.md)]