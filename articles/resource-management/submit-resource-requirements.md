---
title: Enviament d'una sol·licitud de recurs
description: Podeu enviar una sol·licitud de recurs generat com a sol·licitud de recurs. A continuació, la sol·licitud s'envia a un administrador de recursos perquè la compleixi.
author: ruhercul
manager: Annbe
ms.date: 10/04/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 94cf0f0d88e9be2522936b45122ed0037434d4f3
ms.sourcegitcommit: 2cf93d8bf0be5b61a739195a41334c34d910e9ba
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961684"
---
# <a name="submit-a-resource-request"></a>Enviament d'una sol·licitud de recurs

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

Podeu enviar una sol·licitud de recurs generat com a sol·licitud de recurs. A continuació, la sol·licitud s'envia a un administrador de recursos perquè la compleixi.

1. Al Dynamics 365 Project Operations, a la pàgina **Projectes**, seleccioneu la pestanya **Equip** per visualitzar una llista de recursos que es poden reservar. 
2. Seleccioneu el recurs genèric que té un requisit de recurs de la llista i, a continuació, feu clic a **Envia la sol·licitud**.

L'estat de sol·licitud del membre de l'equip genèric canviarà a **Enviada**.

Quan s'hagi complert la sol·licitud, el recurs genèric se substituirà per un recurs anomenat si l'administrador de recursos compleix la sol·licitud amb la reserva d'un recurs amb nom. Altrament, el recurs genèric romandrà a l'equip i l'estat de sol·licitud canviarà a **Necessita revisió**, si l'administrador de recursos ha proposat un recurs amb nom.
