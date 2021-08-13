---
title: Reservar recursos amb nom a partir de requisits de recursos
description: Aquest tema proporciona informació sobre la reserva de recursos amb nom per a un requisit de recurs genèric.
author: JohnPBurrows
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
ms.openlocfilehash: e929a5fb4c307d3b64d0f7f70203fe20bc6dd4f99e89e039fae0ce8276c69c52
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "7000474"
---
# <a name="book-named-resources-from-resource-requirements"></a>Reservar recursos amb nom a partir de requisits de recursos

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Podeu reservar un recurs amb nom per reemplaçar un recurs genèric que tingui un requisit de recurs.

1. Al Project Service Automation (PSA), a la pàgina **Projectes**, feu clic a la pestanya **Equip**.
2. Seleccioneu el recurs genèric que té un requisit de recurs de la llista i, a continuació, feu clic a **Reserva**. O bé, obriu el requisit del recurs i, a continuació, feu clic a **Reserva**.


![Reservar un membre genèric de l'equip.](media/RM-how-to-14.png)


3. A la pàgina **Auxiliar de planificació**, seleccioneu un recurs amb nom per fer la reserva a l'equip del projecte i, a continuació, feu clic a **Reserva**.

![Reservar un membre genèric de l'equip mitjançant l'auxiliar de planificació.](media/RM-how-to-15.png)

Quan la reserva s'hagi completat i complert per un recurs amb nom, el recurs genèric se substitueix pel recurs amb nom.

![Membre de l'equip amb nom que substitueix un membre genèric de l'equip.](media/RM-how-to-16.png)

Les assignacions de la planificació s'actualitzen també amb el recurs amb nom.

![Membre de l'equip amb nom assignat a tasques de projecte.](media/RM-how-to-17.png)

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a>Complir un recurs genèric amb diversos recursos amb nom
El compliment d'un requisit per a un recurs genèric amb diversos recursos amb nom és similar a l'assignació d'un recurs amb nom. Per exemple, hi ha una tasca amb una durada de cinc dies i 120 hores d'esforç. No es pot completar aquesta tasca amb un recurs que treballi un dia típic de vuit hores al llarg d'una setmana de cinc dies. 

![Tasca que necessita 120 hores d'esforç durant cinc dies.](media/RM-how-to-21.png)

El requisit és de 120 hores d'enginyeria de robòtica al llarg de cinc dies, que és de 24 hores per dia.

![Requisit per dia.](media/RM-how-to-22.png)

Aquest és un exemple de quan es necessiten diversos recursos amb nom per complir una sol·licitud de recurs genèrica. Haureu de reservar diversos recursos per complir el requisit.

![Reservar diversos recursos per complir el requisit.](media/RM-how-to-23.png)

La diferència principal en aquest escenari és que el recurs genèric es manté a l'equip assignat a la tasca i els membres de l'equip de recursos amb nom no s'assignen com a part del càrrec. L'administrador del projecte pot assignar la feina segons calgui als recursos amb nom. La visualització **Conciliació** pot ajudar a l'administrador del projecte a dividir les reserves entre diversos recursos a assignacions de tasques. Això no es fa de manera automàtica perquè en qualsevol escenari més complicat que l'anterior, com ara un on teniu un paquet de tasques que constitueixen el requisit, el sistema ha de suposar la intenció de com vol assignar-ho l'administrador del projecte. Com que el sistema no pot entendre la intenció, és probable que les hipòtesis siguin diferents del previst i que es produeixi un resultat incorrecte o impredictible. El resultat predictible és que el recurs genèric es manté assignat fins que l'administrador del projecte crea deliberadament les assignacions amb l'ajuda de la visualització **Conciliació**.




[!INCLUDE[footer-include](../includes/footer-banner.md)]