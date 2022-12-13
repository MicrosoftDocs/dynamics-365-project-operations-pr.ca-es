---
title: Importar estimacions d'un projecte a una línia de pressupostos de projecte
description: Aquest article proporciona informació sobre com importar estimacions d'un projecte a una línia de pressupostos de projecte.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 61c9660f18882d12a7da8965c23b65e408256219
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824474"
---
# <a name="import-estimates-from-a-project-to-a-project-quote-line"></a>Importar estimacions d'un projecte a una línia de pressupostos de projecte 

_**S'aplica a:** Implementació bàsica: tracte de facturació proforma, Project Operations per a escenaris basats en recursos/sense cotització_

Si es crea un projecte durant la fase de prevendes, podeu seleccionar importar l'estimació financera del projecte a la línia d'oferta basada en projectes.

1. Assegureu-vos que la línia d'oferta basada en projectes tingui la informació del projecte al camp **Projecte**.
2. A la pestanya **Detalls de la línia d'oferta**, seleccioneu **Importa des de l'estimació del projecte**.
3. A la pàgina de diàleg que s'obre, seleccioneu una de les opcions de resum següents.

  - **Classe de la transacció**
  - **Categoria**
  - **Funció** 
  - **Tasca del projecte**

En funció de la vostra selecció, es copia la estimació del projecte per a totes les classes de transaccions incloses en aquesta línia d'oferta. Per comprovar les classes de transacció que s'inclouen, seleccioneu la pestanya **General** a la línia d'oferta basada en projectes i comproveu els valors d'**Inclou el temps**, **Inclou les despeses**, **Inclou els materials** i **Inclou les tarifes**.  Per comprovar quines tasques s'inclouen, seleccioneu la pestanya **Tasques imputables** a la línia d'oferta.

Segons les tasques associades i les classes de transacció incloses, les estimacions d'aquestes combinacions de tasques i classes de transacció s'importen a la línia d'oferta.

Quan importeu estimacions, el sistema triarà per defecte els preus segons les llistes de preus del projecte enllaçades a l'oferta i el tipus de facturació que s'hagi definit a la línia d'oferta basada en el projecte. Si una tasca, funció o categoria es configura a la línia d'oferta basada en el projecte com a no imputable, la línia d'estimació importada es definirà com a no imputable i no s'afegirà al valor de l'oferta de la línia d'oferta.

Quan una línia d'oferta té detalls de línia, els camps **Valor de l'oferta** i **Impostos estimats** de la línia d'oferta es resumeixen i no es poden editar.

Quan se seleccionen diverses opcions de resum, el sistema intenta resumir totes les opcions seleccionades. El resultat és que la sortida de les línies d'oferta importades serà major que si només heu seleccionat una opció de resum.

Per exemple, si el projecte tenia les línies d'estimació següents per a les despeses.

| Tasca | Categoria | Date | Quantitat | Preu per unitat | Import |
| --- | --- | --- | --- | --- | --- |
| Tasca A | Bitllets d'avió | 10/1/2020 | 4 | 400 | 1600 |
| Tasca B | Hotels | 10/1/2020 | 4 | 200 | 800 |
| Tasca C | Hotels | 11/1/2020 | 2 | 200 | 400 |

Quan l'usuari selecciona resumir per classe de transacció, la informació següent s'importarà.

| Tasca | Categoria | Date | Quantitat | Preu per unitat | Import |
| --- | --- | --- | --- | --- | --- |
|||10/1/2020 | 3.34 | 840 | 2800 |

Quan l'usuari selecciona resumir per classe i categoria de transacció, la informació següent s'importarà.

| Tasca | Categoria | Date | Quantitat | Preu per unitat | Import |
| --- | --- | --- | --- | --- | --- |
| Tasca A | Bitllets d'avió | 10/1/2020 | 4 | 400 | 1600 |
| | Hotels | 10/1/2020 | 6 | 200 | 1200 |

Quan l'usuari selecciona resumir per classe de transacció, categoria i tasca de node fulla, la informació següent s'importarà. Observeu que aquest resultat és el mateix que el que hi ha al projecte.

| Tasca | Categoria | Date | Quantitat | Preu per unitat | Import |
| --- | --- | --- | --- | --- | --- |
| Tasca A | Bitllets d'avió | 10/1/2020 | 4 | 400 | 1600 |
| Tasca B | Hotels | 10/1/2020 | 4 | 200 | 800 |
| Tasca C | Hotels | 11/1/2020 | 2 | 200 | 400 |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
