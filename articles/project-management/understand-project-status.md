---
title: Comprensió de l'estat del projecte
description: En aquest article s'ofereix informació sobre l'estat assignat als projectes de Dynamics 365 Project Operations.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 86cb60b634b62af23f39720c0452dca82ff3ad26
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923590"
---
# <a name="understand-project-status"></a>Comprensió de l'estat del projecte

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_


La secció **Estat** de la pàgina **Entitat del projecte** proporciona un resum de l'estat d'un projecte segons el cost i l'esforç.


## <a name="status-summary-fields"></a>Camps de resum d'estat

- El camp **Estat global del projecte** és un camp editable que mostra l'estat general del projecte. Aquest camp utilitza una codificació de color, com ara verd, groc i vermell, per indicar un risc cada vegada major. 
- El camp **Comentaris** permet a l'administrador del projecte introduir comentaris específics sobre l'estat. 
- El camp **Data d'actualització de l'estat** no és editable. El valor d'aquest camp és una marca de temps que indica quan s'ha actualitzat l'estat per última vegada.
- Els camps **Rendiment de la planificació** i **Rendiment del cost** s'estableixen a partir de la quadrícula de seguiment. Quan la variació de planificació i costos per al node arrel de la visualització **Seguiment de l'esforç** és positiva, aquests camps s'actualitzen a **Per davant**. Quan la variació de planificació i costos per al node arrel és negativa, aquests camps es defineixen a **Per darrere**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]