---
title: Còpia dels contractes del projecte (bàsic)
description: Aquest tema proporciona informació sobre la còpia dels contractes de projecte al Project Operations.
author: rumant
ms.date: 10/07/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d5c45c6f1631d9e20bd0416410c7fe24a11623da425c8e2a633b085fbfabdd79
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "7006009"
---
# <a name="copy-project-contracts---lite"></a>Còpia dels contractes del projecte (bàsic)

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_

Podeu crear fàcilment nous contractes de projecte fent còpies dels contractes existents d'una de dues maneres: 

  - A la pàgina de llista **Contractes del projecte**, seleccioneu un contracte de projecte i, a continuació, seleccioneu **Copia**.
  - A la pàgina de detalls **Contracte del projecte**, seleccioneu **Copia**.

S'obrirà una pàgina de diàleg on podreu seleccionar els paràmetres del contracte copiat. Els camps següents s'inclouen al diàleg. Segons els valors que seleccioneu en aquest diàleg, el procés de còpia pot canviar.

| **Camp** | **Descripció** | **Impacte descendent** |
| --- | --- | --- |
| Tema | Introduïu el tema del contracte de destinació. Quan s'obri la pàgina de diàleg, el sistema establirà aquest camp al nom del contracte d'origen amb **còpia** annexat. | No hi ha cap impacte descendent d'aquest camp. |
| Client | Referència al registre d'empresa o compte del client. Quan s'obri el diàleg, el sistema establirà aquest camp al compte en el contracte d'origen. | Aquest camp és el client principal del contracte. |
| Unitat de contractació | La unitat de l'organització responsable del lliurament dels projectes associats amb aquest acord. Quan s'obre el quadre de diàleg, el sistema el definirà a la unitat contractant del contracte d'origen. | Unitat de contractació és la divisió de l'empresa que executarà els projectes després d'haver tancat l'acord. Cada unitat de contractació té una moneda. La moneda s'utilitza per informar de les despeses estimades i reals incorregudes durant el projecte. |
| Moneda | Moneda en la qual es realitza la transacció de l'acord. Quan s'obri la pàgina de diàleg, el sistema establirà el camp a la moneda del contracte d'origen. La moneda es pot canviar. Si ho és, el camp **Copia els preus** sempre s'estableix a **No** perquè les llistes de preus del contracte d'origen ja no són rellevants. | La moneda s'utilitza per a les llistes de preus per defecte, per a la creació d'estimacions financeres en el contracte i per a la facturació del client quan es guanya l'acord. |
| Data de lliurament sol·licitada | Data de lliurament sol·licitada pel client. | Aquesta data s'utilitza com a data d'acabament quan creeu dates de facturació amb una freqüència concreta. |
| Copia els preus | Indica si els preus del contracte s'han de copiar del contracte d'origen. | Si el camp és **Sí**, les referències de la llista de preus del projecte i del producte es copien del contracte d'origen al contracte de destinació. Si se selecciona **No**, les llistes de preus són per defecte les darreres llistes de preus en els paràmetres del compte o projecte. |

Quan seleccioneu **D'acord** a la pàgina de diàleg, el sistema crea una còpia del contracte segons els paràmetres seleccionats. El nou contracte s'obrirà.

La informació següent no es copia del contracte d'**origen** al contracte de **destinació**:

  - Planificacions de facturació
  - Clients de línia contracte i contracte
  - Referència del projecte a les línies de contracte basades en el projecte
  - Informació del pressupost del client

Com que aquesta informació és específica de cada contracte, aquests camps i registres no es copien. Es copien les línies de contracte per a projectes i productes, les estimacions en els detalls de la línia de contracte i els valors que no s'han de superar en el nivell del contracte. Els valors per defecte de la tarifa de preu i cost depenen de la selecció en el camp **Copia els preus** en el camp **Copia els paràmetres**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]