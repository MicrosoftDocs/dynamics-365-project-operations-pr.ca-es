---
title: Proposar recursos de projecte
description: Aquest tema proporciona informació sobre la proposta de recursos del projecte.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.reviewer: johnmichalak
ms.openlocfilehash: fc18c5cbd1a564e186f533a3c0f972e60229a6d9
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8587436"
---
# <a name="propose-project-resources"></a>Proposar recursos de projecte

[!include [banner](../includes/psa-now-project-operations.md)]

Els administradors de recursos poden proposar un recurs a l'administrador del projecte mitjançant una sol·licitud de recursos.

1. A la graella de sol·licitud o a la sol·licitud en si mateixa, seleccioneu **Cerca recursos**.
2. A la pàgina **Auxiliar de planificació,** seleccioneu el recurs i, a continuació, a la subfinestra **Crea una reserva de recursos**, al camp **Estat de la reserva**, seleccioneu **Reserva**.

    ![Recurs proposat seleccionat.](media/Resource-Management-image62.png)

Es produeixen les següents actualitzacions d'estat:

- A la pàgina **Auxiliar de planificació**, els indicadors d'estat s'actualitzen per indicar que es proposa la reserva, no que es reserva de manera fixa.

    ![Indicadors d'estat per a la reserva de proposta a la pàgina Auxiliar de planificació.](media/Resource-Management-image63.png)

- A la sol·licitud de recursos, l'estat canvia a **Necessita revisió**.

    ![Estat de sol·licitud de recursos canviat a Necessita revisió.](media/Resource-Management-image64.png)

- A la pestanya **Equip** del projecte, el valor **Estat de la sol·licitud** de l'equip genèric es canvia a **Necessita revisió**.

    ![Estat de la sol·licitud de l'equip genèric canviat a Necessita revisió a la pestanya Equip.](media/Resource-Management-image48.png)

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

![Visualització de l'ús de recursos.](media/Resource-Management-image65.png)

Cada cel·la de la quadrícula representa el percentatge d'ús facturable del recurs en un període, com ara un dia, una setmana o un mes. Les següents fórmules s'utilitzen per acolorir les cel·les:

- **Verd:** Ús facturable \>= Objectiu d'ús de recursos
- **Groc:** Objectiu d'ús - 20 \<= Ús facturable \< Objectiu d'ús
- **Vermell:** Ús facturable \< Objectiu d'ús - 20

Com que la visualització **Ús de recursos** està basada en el tauler de planificació, podeu utilitzar les capacitats de filtratge del tauler de planificació per filtrar els resultats.

La quadrícula requereix que definiu un objectiu d'ús en la funció o en el recurs individual. Per configurar-ho, aneu a **Recursos** \> **Funcions de recurs**.

A més, cal assignar una funció per defecte a cadascun dels recursos que es pot reservar. Aneu a **Recursos** \> **Recursos**. A la pestanya **Project Service**, comproveu que es defineix una funció de recurs i que el camp **Per defecte** està definit com a **Sí**. Podeu afegir funcions addicionals on **Per defecte = No**. La funció on **Per defecte = Sí** s'utilitza per avaluar l'ús del recurs en relació amb l'objectiu per a aquesta funció.

![Conjunt de funcions per defecte.](media/Resource-Management-image67.png)

A la pestanya **Project Service** també podeu definir un objectiu d'ús individual per al recurs. A continuació, el càlcul d'ús utilitza l'objectiu d'ús per avaluar l'objectiu del recurs en comptes de l'objectiu de la funció per defecte del recurs.

L'ús es mostra per a un recurs només si aquest recurs té temps aprovat imputable durant el període que es mostra a la quadrícula.

## <a name="resource-availability"></a>Disponibilitat de recursos

És important que els administradors de recursos puguin visualitzar la disponibilitat dels recursos i actualitzar les reserves. En alguns casos, no hi ha cap demanda formal (sol·licitud de recurs), però un administrador de recursos ha de respondre a una demanda no planificada que entri per canals com ara el correu electrònic, una trucada telefònica o un missatge instantani. Els administradors de recursos utilitzen el tauler de planificació per actualitzar els recursos i les reserves.

Les hores de treball del recurs s'utilitzen com a base per calcular la disponibilitat d'un recurs. Les reserves de recursos consumeixen la capacitat dels recursos.

![Tauler de planificació.](media/Resource-Management-image68.png)

El tauler de planificació utilitza colors i ombrejat per mostrar les reserves, la disponibilitat i l'excés de reserves, i també l'estat de les reserves. Un paràmetre de la configuració del tauler de planificació us permet mostrar una llegenda.

Si una fletxa que apunta a la dreta apareix al costat d'un recurs individual que es pot reservar al tauler de planificació, el recurs es podrà expandir per mostrar els detalls del treball en què està reservat el recurs.

![Recurs que es pot reservar expandit al tauler de planificació.](media/Resource-Management-image69.png)

Com que el Dynamics 365 Project Service Automation utilitza el motor del Universal Resource Scheduling, si també teniu instal·lat el Dynamics 365 Field Service, podeu visualitzar els detalls de les reserves de recursos per a projectes, ordres de treball i altres entitats a les quals hàgiu ampliat la planificació.

![Detalls de les reserves de recursos per a projectes i ordres de treball.](media/Resource-Management-image70.png)

Per visualitzar més detalls d'un recurs individual, feu-hi clic amb el botó dret per obrir la targeta de recursos.

![Targeta de recursos.](media/Resource-Management-image71.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
