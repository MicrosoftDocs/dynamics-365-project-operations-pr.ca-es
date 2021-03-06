---
title: Revisió dels recursos proposats
description: En aquest tema es proporciona informació sobre la manera de proposar recursos de projecte.
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
ms.openlocfilehash: 212b80a7fde8368eedd7572dd5f9278cc53fae98
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897349"
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

## <a name="billable-utilization"></a>Ús facturable

Els recursos poden tenir un objectiu d'ús facturable. Aquest objectiu d'ús es defineix com un atribut de la funció per defecte d'un recurs o es defineix al registre del recurs individual que es pot reservar. Els càlculs d'ús es basen en les hores reals que els recursos han informat mitjançant les entrades de temps aprovades.

Les següents fórmules s'utilitzen per calcular l'ús:

- Ús facturable = Hores reals imputables ÷ Capacitat de recursos
- Ús no facturable = Temps real amb ID de tipus de facturació = No imputable, Gratuït o No disponible ÷ Capacitat de recursos
- Intern = Temps real sense contracte de vendes ÷ Capacitat de recursos
- Capacitat de recursos = Hores de treball - Fora de l'oficina - Dies no hàbils

Podeu cercar la visualització **Ús de recursos** a la subfinestra **Recursos**.

Cada cel·la de la quadrícula representa el percentatge d'ús facturable del recurs en un període, com ara un dia, una setmana o un mes. Les següents fórmules s'utilitzen per acolorir les cel·les:

- **Verd:** Ús facturable \>= Objectiu d'ús de recursos
- **Groc:** Objectiu d'ús - 20 \<= Ús facturable \< Objectiu d'ús
- **Vermell:** Ús facturable \< Objectiu d'ús - 20

Com que la visualització **Ús de recursos** està basada en el tauler de planificació, podeu utilitzar les capacitats de filtratge del tauler de planificació per filtrar els resultats.

La quadrícula requereix que definiu un objectiu d'ús en la funció o en el recurs individual. Per configurar-ho, aneu a **Recursos** \> **Funcions de recurs**.

A més, cal assignar una funció per defecte a cadascun dels recursos que es pot reservar. Aneu a **Recursos** \> **Recursos**. A la pestanya **Project Service**, comproveu que es defineix una funció de recurs i que el camp **Per defecte** està definit com a **Sí**. Podeu afegir funcions addicionals on **Per defecte = No**. La funció on **Per defecte = Sí** s'utilitza per avaluar l'ús del recurs en relació amb l'objectiu per a aquesta funció.

A la pestanya **Project Service** també podeu definir un objectiu d'ús individual per al recurs. A continuació, el càlcul d'ús utilitza l'objectiu d'ús per avaluar l'objectiu del recurs en comptes de l'objectiu de la funció per defecte del recurs.

L'ús es mostra per a un recurs només si aquest recurs té temps aprovat imputable durant el període que es mostra a la quadrícula.

## <a name="resource-availability"></a>Disponibilitat de recursos

És important que els administradors de recursos puguin visualitzar la disponibilitat dels recursos i actualitzar les reserves. En alguns casos, no hi ha cap demanda formal (sol·licitud de recurs), però un administrador de recursos ha de respondre a una demanda no planificada que entri per canals com ara el correu electrònic, una trucada telefònica o un missatge instantani. Els administradors de recursos utilitzen el tauler de planificació per actualitzar els recursos i les reserves.

Les hores de treball del recurs s'utilitzen com a base per calcular la disponibilitat d'un recurs. Les reserves de recursos consumeixen la capacitat dels recursos.

El tauler de planificació utilitza colors i ombrejat per mostrar les reserves, la disponibilitat i l'excés de reserves, i també l'estat de les reserves. Un paràmetre de la configuració del tauler de planificació us permet mostrar una llegenda.

Si una fletxa que apunta a la dreta apareix al costat d'un recurs individual que es pot reservar al tauler de planificació, el recurs es podrà expandir per mostrar els detalls del treball en què està reservat el recurs.

Com que el Dynamics 365 Project Operations utilitza el motor del Universal Resource Scheduling, si també teniu instal·lat el Dynamics 365 Field Service, podeu visualitzar els detalls de les reserves de recursos per a projectes, ordres de treball i altres entitats a les quals hàgiu ampliat la planificació.

Per visualitzar més detalls d'un recurs individual, feu-hi clic amb el botó dret per obrir la targeta de recursos.

