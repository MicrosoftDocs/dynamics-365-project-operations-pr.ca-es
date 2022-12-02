---
title: Administració de contractes de projectes
description: Aquest article proporciona informació sobre la visualització de contractes basats en projectes.
author: rumant
ms.date: 10/26/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: acf1331068ccd1cbbf6a63f85c1bc424889f67e5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8917242"
---
# <a name="manage-project-contracts"></a>Administració de contractes de projectes

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

Els contractes de projecte al Dynamics 365 Project Operations capturen i administren els compromisos acordats contractualment i els detalls de facturació d'un projecte. L'estructura d'un contracte de projecte al Project Operations s'adapta al treball basat en projectes amb els components següents:

- Línies de contracte que identifiquen els components discrets del treball que es presentaran com a components d'alt nivell en una factura de projecte.
- Detalls de la línia de contracte que identifiquen i estimen la feina de cada component d'alt nivell o línia de contracte. L'estimació inclou la planificació i els aspectes financers per al treball vinculat a la línia de contracte.
- Es configuren els models de contractació i els components imputables per a cada línia de contracte que contingui l'acord de facturació per a cada línia de contracte i el contracte global.

## <a name="view-all-project-based-contracts"></a>Visualitzar tots els contractes basats en projectes

Es pot veure una llista de tots els contractes del projecte a la pàgina de llista **Contractes**. 

1. Aneu a **Vendes** > **Contactes**. Es mostra una llista de tots els contractes de projecte al sistema. 
2. Seleccioneu el **Commutador de visualització** (la fletxa desplegable que hi ha al costat del nom de la visualització) per seleccionar altres visualitzacions filtrades. Podeu crear visualitzacions pròpies amb criteris de filtratge personalitzats.

Es poden crear o suprimir contractes des d'aquesta pàgina de llista o des de les pàgines de detalls.

> [!NOTE]
> Els contractes que tenen projectes, tasques, estimacions, diaris i/o valors reals associats no es poden suprimir. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
