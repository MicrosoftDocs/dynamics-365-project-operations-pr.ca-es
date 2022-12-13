---
title: Còpia de les ofertes de projectes
description: Aquest article proporciona informació sobre com copiar les cotitzacions del projecte a Project Operations.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 4f865a4c8a541d6a9c92c5f58a4ed2ed32891eb0
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 12/05/2022
ms.locfileid: "9825265"
---
# <a name="copy-project-quotes"></a>Còpia de les ofertes de projectes

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

Podeu crear fàcilment una nova oferta de projecte copiant-ne una d'existent. 

- Per copiar una oferta de projecte, a la pàgina de llista **Ofertes de projecte** o a la pàgina de detalls **Oferta del projecte**, seleccioneu l'oferta de projecte que voleu copiar i, a continuació, seleccioneu **Copia**.

S'obrirà una pàgina de diàleg on podeu introduir els paràmetres de la còpia. A la taula següent s'enumeren els camps inclosos a la pàgina de diàleg. En funció dels valors que seleccioneu, pot ser que el procés de còpia canviï.

| **Camp** | **Descripció** | **Impacte descendent** |
| --- | --- | --- |
| Tema | Introduïu el tema o el nom pertinents de l'oferta de destinació. Quan s'obre el quadre de diàleg, el sistema el definirà al tema de l'oferta d'origen amb el sufix **-còpia**. | |
| Client potencial | Referència al registre d'empresa o compte del client. Quan s'obre el quadre de diàleg, el sistema el definirà al compte de l'oferta d'origen. | Aquest camp és el client principal a l'oferta. |
| Unitat de contractació | La unitat de l'organització responsable del lliurament dels projectes associats amb aquest acord.
Quan s'obre el quadre de diàleg, el sistema el definirà a la unitat contractant de l'oferta d'origen. | La unitat de contractació és la divisió de l'empresa que executarà els projectes després d'haver tancat l'acord. Cada unitat de contractació té una moneda. La moneda s'utilitza per informar de les despeses estimades i reals incorregudes durant l'execució del projecte. |
| Moneda | Aquesta és la moneda en la qual es realitza la transacció de l'acord. Quan s'obre el quadre de diàleg, el sistema el definirà a la moneda de l'oferta d'origen. Això es pot modificar i si es canvia el camp **Copia el preu** sempre està definit com a **No**. Això es deu a que les llistes de preus de l'oferta d'origen ja no són rellevants. | La moneda s'utilitza per triar per defecte una llista de preus, per crear una estimació financera a l'oferta i, finalment, per facturar el client quan es guanya l'acord. |
| Data de lliurament sol·licitada | Aquesta és la data del lliurament sol·licitada pel client. | S'utilitza com a data d'acabament en crear dates de facturació amb una freqüència concreta. |
| Copia els preus | Un valor Sí/No indica si els preus de l'oferta s'han de copiar de l'oferta d'origen. | Si se selecciona **Sí**, la llista de preus del projecte i les referències de la llista de preus del producte es copien de l'oferta d'origen a l'oferta de destinació. Si se selecciona **No**, les llistes de preus canvien per defecte a les darreres llistes de preus que s'han configurat en els paràmetres del compte o projecte. |

Quan seleccioneu **D'acord** a la pàgina de diàleg, el sistema crea una còpia de l'oferta del projecte segons els paràmetres seleccionats en el diàleg. S'obre l'oferta del projecte nova. 

> [!NOTE]
> La informació següent no es copia de l'oferta d'origen a la de destinació:
>
> - Planificacions de facturació
> - Clients d'oferta i línia d’oferta
> - Referència del projecte a les línies d'oferta basades en el projecte: informació pressupostària del client
>
>Com que aquesta informació és molt específica per a cada oferta, aquests camps i registres no es copien. Les línies d'oferta per als projectes i els productes, les estimacions sobre els detalls de la línia d'oferta i els valors que no voleu superar en el nivell d'oferta es copien. Els valors de preus i les tarifes depenen de l'opció **Copia els preus** seleccionada a la pàgina de diàleg **Paràmetres de la còpia**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
