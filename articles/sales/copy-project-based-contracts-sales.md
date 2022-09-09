---
title: Còpia de contractes basats en projectes
description: Aquest article proporciona informació sobre la còpia dels contractes de projectes a Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 21994ef6d8f6e6cdf321599d107cc80368c96ecc
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410361"
---
# <a name="copy-project-based-contracts"></a>Còpia de contractes basats en projectes

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

Podeu crear fàcilment nous contractes de projecte copiant els contractes existents d'una d'aquestes dues maneres:

- A la **pàgina de la llista Contractes** de projecte, seleccioneu un contracte de projecte i, a continuació, seleccioneu **Copia**.
- A la pàgina de detalls **Contracte del projecte**, seleccioneu **Copia**.

En ambdós casos, apareix un quadre de diàleg on podeu establir els paràmetres del contracte copiat. El quadre de diàleg inclou els camps següents. En funció dels valors que seleccioneu, és possible que el procés de còpia canviï.

| Camp | Descripció | Impacte descendent |
| --- | --- | --- |
| Tema | Introduïu el tema del contracte de destinació. Quan s'obre el quadre de diàleg, el sistema estableix el camp al nom del contracte d'origen, però s'hi afegeix la paraula "còpia". | No hi ha cap impacte descendent d'aquest camp. |
| Client | Referència al registre d'empresa o compte del client. Quan s'obre el quadre de diàleg, el sistema estableix el camp al compte del contracte d'origen. | Aquest camp és el client principal del contracte. |
| Empresa propietària | L'empresa que s'encarrega del lliurament dels projectes que s'associen a aquest acord. Quan s'obre el quadre de diàleg, el sistema estableix el camp a l'empresa propietària del contracte d'origen. | L'empresa propietària és la persona jurídica que executarà el projecte un cop tancat l'acord. La moneda de l'empresa propietària ha de coincidir amb la moneda de la unitat contractant. |
| Unitat de contractació | La unitat d'organització que s'encarrega del lliurament dels projectes que s'associen a aquest acord. Quan s'obre el quadre de diàleg, el sistema estableix el camp a la unitat de contractació del contracte d'origen. | Unitat de contractació és la divisió de l'empresa que executarà els projectes després d'haver tancat l'acord. Cada unitat de contractació té una moneda. Aquesta moneda s'utilitza per informar dels costos estimats i reals incorreguts durant el projecte. |
| Moneda | Moneda en la qual es realitza la transacció de l'acord. Quan s'obre el quadre de diàleg, el sistema estableix el camp a la moneda del contracte d'origen. La moneda es pot canviar. Si és així, el camp Copia el **preu** sempre s'estableix com a **No**, perquè les llistes de preus del contracte d'origen ja no són rellevants. | Aquesta moneda s'utilitza per a llistes de preus per defecte, per generar estimacions financeres al contracte i per facturar al client quan es guanya l'oferta. |
| Data de lliurament sol·licitada | La data de lliurament que li sigui sol·licitada pel client. | Aquesta data s'utilitza com a data de finalització quan creeu dates de facturació amb una freqüència específica. |
| Copia els preus | Un valor que indica si el preu del contracte s'ha de copiar del contracte d'origen. | Si el camp està definit com a **Sí**, les referències de la llista de preus del projecte i del producte es copien del contracte d'origen al contracte de destinació. Si està definit com a **No**, s'utilitzen llistes de preus per defecte, basades en les llistes de preus més recents dels paràmetres del compte o del projecte. |

Quan seleccioneu **D'acord** al quadre de diàleg, el sistema crea una còpia del contracte, en funció dels valors del paràmetre que hàgiu definit. Després s'obre el nou contracte.

La informació següent no **es** copia del contracte d'origen al contracte de destinació, perquè és específica per a cada contracte:

- Planificacions de facturació
- Clients de línia contracte i contracte
- Referència del projecte a les línies de contracte basades en el projecte
- Informació del pressupost del client

Es copien línies contractuals per a projectes i productes, estimacions en detalls de línies de contracte i valors no superiors a nivell de contracte. L'entrada de preus predeterminats i tarifes de cost depèn de la selecció al camp Copia els **preus** del quadre de diàleg Copia els **paràmetres**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
