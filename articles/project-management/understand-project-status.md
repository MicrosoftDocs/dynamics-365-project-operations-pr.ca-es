---
title: Comprensió de l'estat del projecte
description: En aquest tema es proporciona informació sobre l'estat assignat els projectes al Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 336e479ad39653af14cca7930fe63e906b7de489
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072084"
---
# <a name="understand-project-status"></a>Comprensió de l'estat del projecte

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_


La secció **Estat** de la pàgina **Entitat del projecte** proporciona un resum de l'estat d'un projecte en funció del cost i l'esforç.


## <a name="status-summary-fields"></a>Camps de resum d'estat

- El camp **Estat global del projecte** és un camp editable que mostra l'estat general del projecte. Aquest camp utilitza una codificació de color, com ara verd, groc i vermell, per indicar un risc cada vegada major. 
- El camp **Comentaris** permet a l'administrador del projecte introduir comentaris específics sobre l'estat. 
- El camp **Data d'actualització de l'estat** no es pot editar. El valor d'aquest camp és una marca de temps que indica quan s'ha actualitzat l'estat per última vegada.
- Els camps **Rendiment de la programació** i **Rendiment del cost** es defineixen a partir de la quadrícula de seguiment. Quan la variació de planificació i costos per al node arrel de la visualització **Seguiment de l'esforç** és positiva, aquests camps s'actualitzen a **Per davant**. Quan la variació de planificació i costos per al node arrel és negativa, aquests camps es defineixen a **Per darrere**.
