---
title: Informació general de la retenció de proveïdors
description: En aquest tema es proporciona informació general de les capacitats de retenció de proveïdors.
author: sigitac
ms.date: 10/01/2021
ms.topic: overview
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: f9e4a1e63e47524bb622771f645c04e61c279496
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8588448"
---
# <a name="vendor-retention-overview"></a>Informació general de la retenció de proveïdors

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

La vostra organització podria voler conservar una part dels pagaments als proveïdors que treballen en projectes de l'organització. Per exemple, abans de pagar el proveïdor, us pot interessar assegurar-vos que els articles i els serveis que han proporcionat compleixin les vostres expectatives.

Quan negocieu les compres per a projectes amb proveïdors, podeu especificar les condicions de retenció del proveïdor que inclouen el percentatge o l'import que voleu retenir. A mida que el proveïdor proporciona articles i serveis, es dedueix el percentatge de retenció o l'import especificat del pagament al proveïdor. Quan el projecte està complet o arriba a una fase preliminar segons s'especifica al contracte del proveïdor, s'allibera l'import retingut i es crea un pagament al proveïdor.

## <a name="vendor-retention-example"></a>Exemple de retenció de proveïdor

A l'exemple següent es mostra com es retén un percentatge d'un import de factura del proveïdor en funció del percentatge que s'ha completat per a un projecte.

Contoso Robotics USA ha fet un contracte amb el proveïdor Fabrikam per lliurar 100 hores de formació per al projecte de renovació d'equipament. El valor total del contracte es de 30.000 USD amb un preu de compra acordat de 300 USD per hora.

La formació es farà en tres fases amb la planificació següent:

- Fase 1: 50 hores o 50 per cent del projecte
- Fase 2: 30 hores o 80 per cent del projecte en total
- Fase 3: 20 hores o 100 per cent del projecte

A la taula següent s'enumeren les condicions de la retenció.

| **Percentatge d'unitats lliurades** | **Percentatge que es retindrà** | **Percentatge que s'alliberarà** |
| --- | --- | --- |
| 50 % | 20% | 0% |
| 80% | 10% | 10% |
| 100 % | 0% | 100 % |

Les transaccions donen els imports següents:

- Fase 1:
  - L'import per pagar és de 50 x 300, o 15.000.
  - El 20 per cent de la quantitat, o 3.000, es reté i s'alliberarà en una fase posterior.
  - L'import que es paga al proveïdor és de 12.000.
- Fase 2:
  - L'import per pagar és de 30 x 300, o 9.000.
  - Es reté el 10 per cent de la quantitat, 900.
  - S'allibera el 10 per cent dels 3.000 que es van retenir a la fase 1, 300.
  - L'import que es paga al proveïdor és de 8.400. Aquesta quantitat és 9.000 menys la retenció de 900 més els 300 que es van alliberar de la retenció de la fase 1.
- Fase 3:
  - L'import per pagar és de 20 x 300, o 6.000.
  - No es reté cap quantitat.
  - L'import que s'allibera és de 3.600. Aquesta quantitat consisteix en els 3.000 que es van retenir en la fase 1, menys els 300 de la fase 1 que es van alliberar a la fase 2, més els 900 que es van retenir a la fase 2.
  - L'import que es paga al proveïdor és de 9.600. Aquesta quantitat consisteix en l'import retingut de 3.600 més els 6.000 per la finalització de la fase 3.

L'import total que es paga al proveïdor després de completar les tres fases és de 30.000, que és l'import total de la comanda de compra (15.000 + 9.000 + 6.000).
