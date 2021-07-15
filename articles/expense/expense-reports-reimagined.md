---
title: Informes de despeses nous
description: En aquest tema s'explica l'experiència redissenyada i nova per a l'entrada d'informes de despeses.
author: suvaidya
ms.date: 06/14/2021
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: f8c44f86ff7c00e2d5b927bbe6878be7ab6d7758
ms.sourcegitcommit: e93f436afbb92a312fc71b6371866f01927e49d5
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/14/2021
ms.locfileid: "6250992"
---
# <a name="expense-reports-reimagined"></a>Informes de despeses nous

L'entrada d'informes de despesa s'ha redissenyat per simplificar el procés i reduir el temps necessari per completar un informe. Aquests són els principals components de l'experiència de despesa nova:

- Nou espai de treball d'administració de despeses que us permet accedir a les despeses del vostre delegat.
- Una experiència nova que coincidència de rebuts per mostrar millor els rebuts de capçalera i simplificar el procés d'adjuntar rebuts a les línies de despeses.
- Quadrícula nova només de lectura que us permet visualitzar moltes més línies de despeses i altres columnes de dades. Ara podeu veure totes les línies desglossades i dividides, juntament amb les seves despeses principals.
- Subfinestra simplificada per editar despeses.
- Missatges d'error, advertiment i de les polítiques redissenyats per proporcionar el context correcte i informació del problema i com resoldre'l. Hem suprimit diversos dels missatges que apareixien abans que els usuaris poguessin completar les seves tasques i adreçar els problemes.
- Pàgina nova per especificar els camps obligatoris, els camps opcionals i els camps que no s'han d'incloure. Aquesta pàgina us ajuda a reduir el nombre de camps que s'han de definir.
- Nova aparença per als informes de despeses, perquè els informes ja no semblin com si fossin dissenyats per a la comptabilitat de persones.

Per activar la nova experiència, utilitzeu l'àrea de treball **Administració de característiques** per activar la característica **Àrea de treball d'informes de despeses nous**. Quan activeu aquesta característica es produeixen les següents accions:

- L'àrea de treball de despeses existent se substitueix per la nova àrea de treball.
- S'afegirà un element de menú nou per a la visibilitat del camp de despeses.
- No hi ha elements de menú existents per a informes de despeses (pàgina existent) o camps d'informe de despeses eliminats.
- Els fluxos de treball i les aprovacions encara us porten a la pàgina d'informes de despeses existent.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4IQFM]

## <a name="new-features"></a>Noves característiques

| Nova característica | Descripció |
|---|----|
| Visibilitat del camp de despesa | Una pàgina de configuració nova us permet especificar quins camps s'han d'inhabilitar per a una organització. També podeu especificar quins camps han de ser obligatoris i quins camps són recomanacions. |
| Camps obligatoris | La configuració senzilla nova us permet fer alguns camps obligatoris sense haver d'utilitzar el marc de polítiques. |
| Camps opcionals | S'afegeix una segona pàgina per a camps opcionals. D'aquesta manera, els empleats no se sentiran com si s'han de definir els camps, però els camps encara són accessibles fàcilment. |
| Afegir rebuts sense adjuntar | La capacitat d'afegir rebuts sense adjuntar a l'informe de despeses és més visible des de l'àrea de treball i l'informe de despeses. |
| Missatgeria millorada | Hi ha una major visibilitat en les línies de despesa que tenen advertiments o errors. |
| Reducció dels missatges a la barra de missatges| El nombre de missatges d'informació i registra s'ha reduït i s'ha fet un esforç per evitar que apareguin missatges duplicats en molts casos. |
| S'han agrupat accions habituals | La interfície s'ha netejat amb l'addició d'un botó d'accions noves per a la majoria de les accions de nivell de la línia comuna i l'addició d'un botó de punts suspensius (...) per a la capçalera i altres accions menys freqüents. |
| Nova àrea de treball per augmentar la visibilitat | Una àrea de treball nova unifica les característiques i els enllaços que permeten als usuaris desplaçar-se a diferents àrees. |
| Afegiu despeses i rebuts existents durant la creació de despeses | Quan creeu informes de despeses, podeu afegir totes les despeses o seleccionar despeses no adjuntades. Les despeses no adjuntades són les despeses importades des del canal de continguts de targeta de crèdit empresarial o les despeses que l'usuari ha creat manualment però que no s'han adjuntat a un informe de despeses.|
| Calculadora de tipus de canvi | S'ha afegit una calculadora de tipus de canvi que permet calcular el tipus de canvi per a operacions multidivisa. |
| Deseu i afegiu línies de despeses noves | Els botons **Desa** i **Nou** estan disponibles quan s'introdueixen les despeses noves per ajudar-vos a introduir ràpidament les línies de despesa. |
| Visibilitat millorada a les línies dividides i desglossades | Les línies desglossades i dividides s'afegeixen directament a la llista de despeses per augmentar la visibilitat i ajudar-vos a determinar fàcilment si hi ha cap error. |
| Visualitzar els detalls de la subcategoria en línies desglossades | Les línies desglossades d'una despesa principal mostren les etiquetes de subcategoria a l'informe de despeses, la qual cosa us ajuda a revisar d'un cop d'ull els detalls granulars.|
| Mostra els rebuts durant el desglossament | Els rebuts poden mostrar-se durant el desglossament. |
| Selecció de bestreta en efectiu | Seleccioneu una o diverses bestretes en efectiu per realitzar una transacció de despesa única. |
| Balanç de bestreta en efectiu | Reviseu el balanç de bestreta en efectiu en temps real quan creeu una entrada de despesa per a bestretes en efectiu aprovades i pagades. |

La versió inicial se centra en escenaris d'entrada de despesa. Qualsevol escenari de revisió o aprovació de l'informe de despeses continuarà utilitzant la pàgina d'entrada de despeses existent.

Les característiques següents no s'admeten a l'Àrea de treball d'informes de despeses nous, però estan previstes per a versions futures: 

- Integració de les peticions de viatge
- Entrada de despesa per dia
- Compatibilitat amb aprovadors intermedis
- Capacitat de visualitzar l'historial del flux de treball


[!INCLUDE[footer-include](../includes/footer-banner.md)]
