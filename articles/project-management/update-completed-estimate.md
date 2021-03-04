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
ms.openlocfilehash: 59d04869839cebd6e197f94f2ada8ab12c495c3b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127191"
---
# <a name="update-estimate-at-completion"></a>Actualització de l'estimació en finalitzar

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

És habitual que un administrador de projecte revisi les estimacions originals d'una tasca. Les reprojeccions de projectes són la percepció de les estimacions d'un administrador de projecte, donat l'estat actual del projecte. No obstant, no recomanem que els administradors de projectes canviïn els números de la línia de base, ja que la línia de base del projecte representa la font de veritat establerta de l'estimació de la planificació i el cost del projecte, i totes les parts interessades del projecte l'han acordat.

Hi ha dues maneres de fer que un administrador del projecte pugui tornar a projectar l'esforç de les tasques:

- Substituir l'estimació per finalitzar (ETC) per defecte amb una nova estimació de l'esforç real restant de la tasca. 
- Substituir el percentatge de progrés per defecte amb una nova estimació del progrés real de la tasca.

Cadascuna d'aquestes aproximacions provoca un nou càlcul de l'ETC de la tasca, l'estimació en finalitzar (EAC) i el percentatge de progrés, i la variació de l'esforç projectat d'una tasca. Es torna a calcular l'EAC, l'ETC i el percentatge de progrés de les tasques de resum, i produeixen una nova projecció de la variació d'esforç.


[!INCLUDE[footer-include](../includes/footer-banner.md)]