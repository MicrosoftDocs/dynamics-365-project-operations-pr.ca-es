---
title: Revisió dels recursos proposats
description: Aquest article proporciona informació sobre com proposar recursos del projecte.
author: ruhercul
ms.date: 08/18/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 2a5b5159ceb8aa5b29dffad59517bc11fbf16871
ms.sourcegitcommit: 66e376675e6df8efc86fa84ec24e9aad6a980304
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 07/21/2022
ms.locfileid: "9183962"
---
# <a name="review-proposed-resources"></a>Revisió dels recursos proposats

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

Els administradors de recursos poden proposar un recurs a l'administrador del projecte mitjançant una sol·licitud de recursos.

Per revisar els recursos proposats, seguiu aquests passos:

1. A la graella **Sol·licitud** o a la sol·licitud mateixa, seleccioneu **Cerca recursos**.
2. A la pàgina **Auxiliar de planificació**, seleccioneu el recurs i confirmeu que totes les hores proposades s'incloguin a la reserva proposada.
3. A la subfinestra **Crea una reserva de recurs**, definiu el camp **Estat de reserva** com a **Proposat** i, a continuació, seleccioneu **Reserva**.

    > [!NOTE]
    > La definició de l'**Estat de reserva** com a **Proposat** no reserva el recurs i no substitueix el recurs genèric pel membre de l'equip nomenat.

    Es produeixen les següents actualitzacions d'estat:

    - A la pàgina **Auxiliar de planificació**, els indicadors d'estat s'actualitzen per indicar que es proposa la reserva, no que es reserva de manera fixa.
    - A la sol·licitud de recurs, el revisor de la sol·licitud hauria de canviar l'estat a **Revisió de necessitats**.
    - A la **pestanya Equip** del projecte, el valor Estat **de sol·licitud del membre de l'equip genèric es** canvia automàticament a **Revisió de necessitats**.

L'administrador de projectes pot acceptar o rebutjar la proposta.

Quan els administradors de recursos processen les sol·licituds de recursos, poden utilitzar qualsevol dels enfocaments següents:

- Proposar diversos recursos per satisfer la demanda si no hi ha cap recurs disponible per complir les hores requerides. Les hores proposades es divideixen a continuació entre diversos recursos que poden satisfer les hores requerides. En aquest escenari, les hores no es poden superposar.
- Proposar menys recursos dels que calguin. En aquest escenari, la capacitat proposada del recurs és inferior a les hores requerides que especifica el sol·licitant. Quan el sol·licitant accepta els recursos proposats, es crea un requisit de recurs no complert per capturar la resta de la demanda.
- Reservar diversos recursos per satisfer la demanda si no hi ha cap recurs disponible per completar el treball.
- Reserveu menys recursos dels que calguin. En aquest escenari, les hores reservades són menys que les hores requerides. El sistema us guia per proposar recursos en comptes de reserves, de manera que el sol·licitant pugui comprovar i fer un seguiment de la demanda restant.

## <a name="resource-availability"></a>Disponibilitat de recursos

Els administradors de recursos han de poder visualitzar la disponibilitat dels recursos i actualitzar les reserves. En alguns casos, no hi ha cap demanda formal (sol·licitud de recurs). Tanmateix, un administrador de recursos ha de respondre a una demanda no planificada que arriba a través d'altres canals, com ara correus electrònics, trucades telefòniques o missatges instantanis. Els administradors de recursos utilitzen el **Tauler de planificació** per actualitzar els recursos i les reserves.

Les hores de treball del recurs s'utilitzen com a base per calcular la disponibilitat d'un recurs. Les reserves de recursos consumeixen la capacitat dels recursos.

El **Tauler de planificació** utilitza colors i ombrejat per mostrar les reserves, la disponibilitat i l'excés de reserves, i també l'estat de les reserves. Una configuració del **Tauler de planificació** us permet visualitzar una llegenda.

Si una fletxa que apunta a la dreta apareix al costat d'un recurs individual que es pot reservar al **Tauler de planificació**, el recurs es podrà expandir per mostrar els detalls del treball en què està reservat el recurs.

Com que el Dynamics 365 Project Operations utilitza el motor del Universal Resource Scheduling, si també teniu instal·lat el Dynamics 365 Field Service, podeu visualitzar els detalls de les reserves de recursos per a projectes, ordres de treball i altres entitats a les quals hàgiu ampliat la planificació.

Per visualitzar detalls addicionals d'un recurs individual, feu-hi clic amb el botó dret per obrir la targeta de recursos.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
