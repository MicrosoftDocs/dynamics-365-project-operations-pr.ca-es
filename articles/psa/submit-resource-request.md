---
title: Enviar una sol·licitud de recurs
description: En aquest tema s'ofereix informació sobre la presentació d'una sol·licitud d'un recurs del projecte.
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/1/2018
ms.topic: article
author: JohnPBurrows
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
ms.openlocfilehash: bcea3d640d7e9ee2b071c55bff9ade3268edb319
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072305"
---
# <a name="submitting-a-resource-request"></a>Enviar una sol·licitud de recurs

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Podeu enviar una sol·licitud de recurs generat com a sol·licitud de recurs. A continuació, la sol·licitud s'envia a un administrador de recursos perquè la compleixi.

1. Al Project Service Automation (PSA), a la pàgina **Projectes** , feu clic a la pestanya **Equip** per visualitzar una llista de recursos que es poden reservar. 
2. Seleccioneu el recurs genèric que té un requisit de recurs de la llista i, a continuació, feu clic a **Envia la sol·licitud**.

![Enviar una sol·licitud de recurs](media/RM-how-to-18.png)

L'estat de sol·licitud del membre de l'equip genèric canviarà a **Enviada**.

Després que l'administrador de recursos hagi complert la sol·licitud, el recurs genèric se substituirà per un recurs anomenat si l'administrador de recursos compleix la sol·licitud amb la reserva d'un recurs amb nom. Altrament, el recurs genèric romandrà a l'equip i l'estat de sol·licitud canviarà a **Necessita revisió** , si l'administrador de recursos ha proposat un recurs amb nom.