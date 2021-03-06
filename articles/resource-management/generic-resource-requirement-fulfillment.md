---
title: Compliment dels requisits de recursos genèrics
description: Aquest tema proporciona informació sobre la reserva de recursos amb nom per a un requisit de recurs genèric.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 76dd47fa2451b5cb61298ff332d77bae646a288a
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897574"
---
# <a name="generic-resource-requirement-fulfillment"></a>Compliment dels requisits de recursos genèrics

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

Podeu reservar un recurs amb nom per reemplaçar un recurs genèric que tingui un requisit de recurs.

1. A la pàgina **Projectes**, seleccioneu la pestanya **Equip**.
2. Seleccioneu el recurs genèric que té un requisit de recurs de la llista i, a continuació, seleccioneu **Reserva**. O bé, obriu el requisit del recurs i, a continuació, seleccioneu **Reserva**.
3. A la pàgina **Auxiliar de planificació**, seleccioneu un recurs amb nom per fer la reserva a l'equip del projecte i, a continuació, seleccioneu **Reserva**.

Quan la reserva s'hagi completat i complert per un recurs amb nom, el recurs genèric se substitueix pel recurs amb nom.

Les assignacions de la planificació s'actualitzen també amb el recurs amb nom.

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a>Complir un recurs genèric amb diversos recursos amb nom
El compliment d'un requisit per a un recurs genèric amb diversos recursos amb nom és similar a l'assignació d'un recurs amb nom. Per exemple, hi ha una tasca amb una durada de cinc dies i 120 hores d'esforç. No es pot completar aquesta tasca amb un recurs que treballi un dia típic de vuit hores al llarg d'una setmana de cinc dies. 

El requisit és de 120 hores d'enginyeria de robòtica al llarg de cinc dies, que és de 24 hores per dia.

Aquest és un exemple de quan es necessiten diversos recursos amb nom per complir una sol·licitud de recurs genèrica. Haureu de reservar diversos recursos per complir el requisit.

La diferència principal en aquest escenari és que el recurs genèric es manté a l'equip assignat a la tasca i els membres de l'equip de recursos amb nom no s'assignen com a part del càrrec. L'administrador del projecte pot assignar la feina segons calgui als recursos amb nom. La visualització **Conciliació** pot ajudar a l'administrador del projecte a dividir les reserves entre diversos recursos a assignacions de tasques. Això no es fa de manera automàtica perquè en qualsevol escenari més complicat que l'anterior, com ara un on teniu un paquet de tasques que constitueixen el requisit, el sistema ha de suposar la intenció de com vol assignar-ho l'administrador del projecte. Com que el sistema no pot entendre la intenció, és probable que les hipòtesis siguin diferents del previst i que es produeixi un resultat incorrecte o imprevisible. El resultat predictible és que el recurs genèric es manté assignat fins que l'administrador del projecte crea deliberadament les assignacions amb l'ajuda de la visualització **Conciliació**.


