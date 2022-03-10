---
title: Informes de despeses redissenyats
description: En aquest tema es proporciona informació sobre l'experiència redissenyada i reinventada per a l'entrada d'informes de despeses.
author: ryansandness
ms.date: 06/14/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2019-6-30
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: fa111917ffd3107413846dae67c56fd2495cfc1e1bc7362152138efd7bf3b869
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986074"
---
# <a name="redesigned-expense-reports"></a>Informes de despeses redissenyats

L'entrada d'informes de despesa s'ha redissenyat per simplificar el procés de completar els informes de despeses i reduir el temps necessari. Aquests són els principals components de l'experiència de despesa nova:

- Nou espai de treball d'administració de despeses que us permet accedir a les despeses del vostre delegat.
- Una experiència nova que coincidència de rebuts per mostrar millor els rebuts de capçalera i simplificar el procés d'adjuntar rebuts a les línies de despeses.
- Nova quadrícula de només de lectura que us permet visualitzar moltes més línies de despeses i columnes addicionals de dades. Ara podeu veure totes les línies desglossades i dividides, juntament amb les seves despeses principals.
- Subfinestra simplificada per editar despeses.
- Missatges d'error, advertiment i de les normes redissenyats per ajudar a garantir que teniu el context correcte per entendre quin és el problema i com resoldre'l. Microsoft ha eliminat molts missatges que apareixien abans que els usuaris tinguessin l'oportunitat de completar les seves tasques i abordar els problemes, com ara el missatge de desglossament incomplet.
- Una pàgina nova per especificar quins camps requereix la vostra organització, quins camps són opcionals i quins camps no s'han de capturar. Aquesta pàgina ajudarà a reduir el nombre de camps que els usuaris han de definir.
- Nova aparença per als informes de despeses, perquè els informes ja no semblin com si fossin dissenyats per a la comptabilitat de persones.

Per activar la nova experiència, utilitzeu l'àrea de treball **Administració de característiques** per activar la característica **Informes de despeses reinventats**. Quan activeu aquesta característica es produeixen les següents accions:

- L'àrea de treball de despeses existent se substitueix per la nova àrea de treball.
- S'afegirà un element de menú nou per a la visibilitat del camp de despeses.
- No hi ha elements de menú existents per a informes de despeses (pàgina existent) o camps d'informe de despeses eliminats.
- Els fluxos de treball i les aprovacions encara us porten a la pàgina d'informes de despeses existent.

## <a name="new-features"></a>Noves característiques

| Nova característica | Descripció |
|---|----|
| Visibilitat del camp de despesa | Una pàgina de configuració nova us permet especificar quins camps s'han d'inhabilitar per a una organització, quins camps han de ser obligatoris i quins camps es recomanen. |
| Camps obligatoris | La configuració senzilla nova us permet fer alguns camps obligatoris sense haver d'utilitzar el marc de polítiques. |
| Camps opcionals | S'afegeix una segona pàgina per a camps opcionals. D'aquesta manera, els empleats no se sentiran com si s'han de definir els camps, però els camps encara són accessibles fàcilment. |
| Afegir rebuts sense adjuntar | La capacitat d'afegir rebuts sense adjuntar a l'informe de despeses és més visible des de l'àrea de treball i l'informe de despeses. |
| Missatgeria millorada | Hi ha una major visibilitat en les línies de despesa que tenen advertiments o errors. |
| Reducció dels missatges a la barra de missatges| El nombre de missatges d'informació i registra s'ha reduït i s'ha fet un esforç per evitar que apareguin missatges duplicats en molts casos. |
| S'han agrupat accions habituals | La interfície s'ha netejat amb l'addició d'un botó d'accions noves per a la majoria de les accions de nivell de la línia comuna i l'addició d'un botó de punts suspensius (...) per a la capçalera i altres accions menys freqüents. |
| Nova àrea de treball per augmentar la visibilitat | Una àrea de treball nova unifica les característiques i els enllaços que permeten als usuaris desplaçar-se a diferents àrees. |
| Afegiu despeses i rebuts existents durant la creació de despeses | Quan creeu informes de despeses, podeu afegir totes les despeses o rebuts seleccionats. |
| Calculadora de tipus de canvi | S'ha afegit una calculadora de tipus de canvi que permet calcular el tipus de canvi per a operacions multidivisa. |
| Deseu i afegiu línies de despeses noves | Els botons **Desa** i **Nou** estan disponibles quan s'introdueixen les despeses noves per ajudar-vos a introduir ràpidament les línies de despesa. |
| Visibilitat millorada a les línies dividides i desglossades | Les línies desglossades i dividides s'afegeixen directament a la llista de despeses per augmentar la visibilitat i ajudar-vos a determinar fàcilment si hi ha cap error de norma o un altre tipus d'error. |
| Mostra els rebuts durant el desglossament | Els rebuts poden mostrar-se durant el desglossament. |

La versió inicial se centra en escenaris d'entrada de despesa. Qualsevol escenari de revisió o aprovació de l'informe de despeses continuarà utilitzant la pàgina d'entrada de despeses existent.

Les característiques següents estan presents a la pàgina existent, però encara no estan presents a la pàgina nova. Aquestes característiques es tornaran a introduir en les següents versions:

- Aprovacions
- Aprovació dels comptes a pagar i capacitat d'editar la comptabilitat
- Diversos punts d'entrada
- Integració de les peticions de viatge
- Entitat de dades per a la visibilitat del camp de despeses
- Entrada de despeses de dietes
- Flux de treball de nivell de línia
- Compatibilitat amb aprovadors intermedis
- Desglossament avançat


[!INCLUDE[footer-include](../includes/footer-banner.md)]