---
title: Reserves de recursos i com es relacionen amb les assignacions de tasques
description: En aquest tema es proporciona informació sobre la manera d'administrar els recursos amb nom, les reserves de recursos i les assignacions de tasques i la seva relació entre ells.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 9/27/2019
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
ms.openlocfilehash: 953d7ca1995eae823fd29d0a9e85ff6a2a2eb59b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8575467"
---
# <a name="resource-bookings-and-how-they-relate-to-task-assignments"></a>Reserves de recursos i com es relacionen amb les assignacions de tasques

[!include [banner](../includes/psa-now-project-operations.md)]

Hi ha dues maneres que els recursos amb nom es poden reservar en tasques d'un equip de projecte i d'un projecte assignat:

- El recurs es pot reservar directament en un projecte, i posteriorment assignar-lo a les tasques del projecte.
- Les tasques es poden assignar a un recurs genèric, que després s'utilitzen per trobar i reemplaçar el genèric per un recurs amb nom. 

En tots dos casos, l'acte de reservar el recurs reserva la capacitat del recurs.

L'administrador del projecte que és l'encarregat de planificar-lo posseeix el pla i la planificació del projecte. Mitjançant l'ús del recurs genèric per a l'assignació i quan es genera una sol·licitud de recursos, l'administrador del projecte pot reservar recursos al projecte amb els contorns especificats en el pla del projecte. Pot reservar recursos a un projecte i assignar-los a tasques, però és impossible alinear els contorns de la reserva amb els contorns de les tasques. Les reserves no afecten la planificació del projecte.

Imagineu un projecte complex amb múltiples tasques superposades, on diversos recursos del mateix tipus necessiten treballar simultàniament. Si a un recurs se li dóna un contorn diferent a l'agregat de les seves assignacions, és difícil modificar les tasques per adaptar-les al contorn de les reserves a les seves tasques discretes i els seus contorns originals.

En el següent exemple, l'esforç total requerit pel mateix recurs d'un conjunt de quatre tasques és de 62 hores durant un període de dues setmanes i hi ha un contorn específic. Si el recurs Bob es reserva durant 62 hores durant les mateixes dues setmanes però amb un contorn diferent, el requisit i les reserves estan alineats.

| **Contorns de tasca**    | **Hores totals** | Dl. 04/06 | Dm. 05/06 | Dc. 06/06 | Dj. 07/06 | Dv. 08/06 | Ds. 09/06 | Dg. 10/06 | Dl. 11/06 | Dm. 12/06 | Dc. 13/06 | Dj. 14/06 | Dv. 15/06 |
|----------------------|-----------------|--------|--------|--------|--------|--------|--------|---------|---------|---------|---------|---------|---------|
| Tasca 1               | 24              | 8      | 8      | 4      |        |        |        |         |         |         | 4       |         |         |
| Tasca 2               | 16              |        |        | 4      | 4      |        |        |         | 8       |         |         |         |         |
| Tasca 3               | 10              |        |        |        |        | 4      |        |         |         | 4       |         | 2       |         |
| Tasca 4               | 12              |        |        |        |        |        |        |         |         |         | 4       |         | 8       |
|                      |                 |        |        |        |        |        |        |         |         |         |         |         |         |
| **Totals**           | 62              | 8      | 8      | 8      | 4      | 4      |        |         | 8       | 4       | 8       | 2       | 8       |
|                      |                 |        |        |        |        |        |        |         |         |         |         |

### <a name="bobs-availability"></a>Disponibilitat de Bob
| **Reserva de recurs** | **Hores totals** | Dl. 04/06 | Dm. 05/06 | Dc. 06/06 | Dj. 07/06 | Dv. 08/06 | Ds. 09/06 | Dg. 10/06 | Dl. 11/06 | Dm. 12/06 | Dc. 13/06 | Dj. 14/06 | Dv. 15/06 |
|------------------------|-----------------|--------|--------|--------|--------|--------|--------|---------|---------|---------|---------|---------|---------|
| Bob                    | 62              | 4      | 4      | 8      | 8      | 8      |        |         | 4       | 4       | 8       | 8       | 6       |

No obstant això, no hi ha una forma sistemàtica d'assignar el contorn d'hores reservades a les tasques per dia. Si l'administrador de projecte està disposat a canviar la planificació del projecte per complir amb la disponibilitat del recurs, llavors haurà d'eliminar l'assignació i revisar totes les tasques perquè coincideixin amb els contorns de la reserva.

En cas que una organització hagi assignat la tasca de planificació de projectes a un administrador de projecte i a un administrador de recursos, l'administrador de projecte establirà la planificació, que inclou el resseguiment del treball requerit. L'administrador de recursos no podrà modificar la planificació sense que l'administrador del projecte ho sàpiga si canvia els contorns d'esforç mentre reserva recursos reals. Si l'administrador de recursos fa alguna cosa diferent a la que va sol·licitar l'administrador del projecte, hauran d'arribar a un acord sobre els canvis necessaris en la planificació.

Com que les reserves i assignacions no estan estretament vinculades, és possible reservar contorns que siguin diferents als contorns de la tasca o canviar les assignacions per donar com a resultat circumstàncies en què les reserves i assignacions no estan alineades.

La **Vista de conciliació** permet a l'administrador del projecte veure les reserves i assignacions per a cada membre de l'equip del projecte. La vista fa servir colors i ombrejats per mostrar on hi ha una manca de coincidència entre les reserves i les assignacions dels membres de l'equip. En funció d'aquesta informació, l'administrador del projecte pot prendre mesures correctives per ampliar les reserves de recursos per a casos en què hi ha assignacions i no hi ha reserves o cancel·lar reserves on es reserven recursos però no tenen assignacions.

> [!NOTE]
> Si es mou una tasca que heu contornejat, aquests contorns no es mantindran. Els contorns es regeneren d'acord amb el calendari del projecte per poder justificar canvis en les hores de treball i dies festius. Això és per temes de disseny, perquè el sistema no coneix la intenció del contorn original i no pot determinar si té sentit retenir aquest contorn en un nou període de temps. Com que les reserves i assignacions estan desconnectades, les reserves conserven els contorns de reserva originals. En aquest cas, haureu de cancel·lar i tornar a reservar el nou contorn d'assignació.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
