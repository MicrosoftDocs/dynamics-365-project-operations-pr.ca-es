---
title: Revisió dels recursos proposats
description: En aquest tema es proporciona informació sobre la manera de proposar recursos de projecte.
author: ruhercul
manager: AnnBe
ms.date: 11/05/2020
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
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: fa0515b9d6a0023c05c37d2bcfa6a403f48927cb
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279261"
---
# <a name="review-proposed-resources"></a>Revisió dels recursos proposats

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

Els administradors de recursos poden proposar un recurs a l'administrador del projecte mitjançant una sol·licitud de recursos.

1. A la graella de sol·licitud o a la sol·licitud en si mateixa, seleccioneu **Cerca recursos**.
2. A la pàgina **Auxiliar de planificació,** seleccioneu el recurs i, a continuació, a la subfinestra **Crea una reserva de recursos**, al camp **Estat de la reserva**, seleccioneu **Reserva**.

Es produeixen les següents actualitzacions d'estat:

- A la pàgina **Auxiliar de planificació**, els indicadors d'estat s'actualitzen per indicar que es proposa la reserva, no que es reserva de manera fixa.
- A la sol·licitud de recursos, l'estat canvia a **Necessita revisió**.
- A la pestanya **Equip** del projecte, el valor **Estat de la sol·licitud** de l'equip genèric es canvia a **Necessita revisió**.

L'administrador de projectes pot acceptar o rebutjar la proposta.

Quan els administradors de recursos processen les sol·licituds de recursos, poden utilitzar qualsevol dels enfocaments següents:

- Proposar diversos recursos per satisfer la demanda si no hi ha cap recurs disponible per complir les hores requerides. Les hores proposades es divideixen a continuació entre diversos recursos que poden satisfer les hores requerides. En aquest escenari, les hores no es poden superposar.
- Proposar menys recursos dels que calguin. En aquest escenari, la capacitat proposada del recurs és inferior a les hores requerides que especifica el sol·licitant. Per tant, quan el sol·licitant accepta els recursos proposats, es crea un requisit de recurs no complert per capturar la resta de la demanda.
- Reservar diversos recursos per satisfer la demanda si no hi ha cap recurs disponible per completar el treball.
- Reservar menys recursos dels que calguin. En aquest escenari, les hores reservades són menys que les hores requerides. El sistema us guia per proposar recursos en comptes de reserves, de manera que el sol·licitant pugui comprovar i fer un seguiment de la demanda restant.

## <a name="resource-availability"></a>Disponibilitat de recursos

És important que els administradors de recursos puguin visualitzar la disponibilitat dels recursos i actualitzar les reserves. En alguns casos, no hi ha cap demanda formal (sol·licitud de recurs), però un administrador de recursos ha de respondre a una demanda no planificada que entri per canals com ara el correu electrònic, una trucada telefònica o un missatge instantani. Els administradors de recursos utilitzen el tauler de planificació per actualitzar els recursos i les reserves.

Les hores de treball del recurs s'utilitzen com a base per calcular la disponibilitat d'un recurs. Les reserves de recursos consumeixen la capacitat dels recursos.

El tauler de planificació utilitza colors i ombrejat per mostrar les reserves, la disponibilitat i l'excés de reserves, i també l'estat de les reserves. Un paràmetre de la configuració del tauler de planificació us permet mostrar una llegenda.

Si una fletxa que apunta a la dreta apareix al costat d'un recurs individual que es pot reservar al tauler de planificació, el recurs es podrà expandir per mostrar els detalls del treball en què està reservat el recurs.

Com que el Dynamics 365 Project Operations utilitza el motor del Universal Resource Scheduling, si també teniu instal·lat el Dynamics 365 Field Service, podeu visualitzar els detalls de les reserves de recursos per a projectes, ordres de treball i altres entitats a les quals hàgiu ampliat la planificació.

Per visualitzar més detalls d'un recurs individual, feu-hi clic amb el botó dret per obrir la targeta de recursos.



[!INCLUDE[footer-include](../includes/footer-banner.md)]