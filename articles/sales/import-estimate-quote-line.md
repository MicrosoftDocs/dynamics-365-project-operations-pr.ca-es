---
title: Importar les estimacions d'un projecte a una línia d'oferta basada en projectes
description: En aquest tema es proporciona informació sobre la importació d'estimacions d'un projecte a una línia d'oferta.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: fda8fee6dcf55126077fb6b8c502ee9dada9b44c
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4125571"
---
# <a name="import-estimates-for-a-project-to-a-project-based-quote-line"></a>Importar les estimacions d'un projecte a una línia d'oferta basada en projectes

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_


Si es crea un projecte durant la fase de prevendes, podeu seleccionar importar l'estimació financera del projecte a la línia d'oferta basada en projectes.

1. Assegureu-vos que la línia d'oferta basada en projectes tingui la informació del projecte al camp **Projecte**.
2. A la pestanya **Detalls de la línia d'oferta**, seleccioneu **Importa des de l'estimació del projecte**.
3. A la pàgina de diàleg que s'obre, seleccioneu una de les opcions de resum següents:

  - **Classe de la transacció**
  - **Categoria**
  - **Funció** 
  - **Tasca del projecte**

En funció de la vostra selecció, es copia la estimació del projecte per a totes les classes de transaccions incloses en aquesta línia d'oferta. Per comprovar les classes de transacció que s'inclouen, seleccioneu la pestanya **General** de la línia d'oferta basada en el projecte i comproveu els valors de **Inclou el temps**, **Inclou les despeses** i **Incloeu els impostos**.

Quan importeu estimacions, el sistema triarà per defecte els preus segons les llistes de preus del projecte enllaçades a l'oferta i el tipus de facturació que s'hagi definit a la línia d'oferta basada en el projecte. Si una funció o categoria es configura a la línia d'oferta basada en el projecte com a no imputable, la línia d'estimació importada es definirà com a no imputable i no es afegirà al valor de l'oferta de la línia d'oferta.

Quan una línia d'oferta té detalls de línia, els camps **Valor de l'oferta** i **Impostos estimats** de la línia d'oferta es resumeixen i no es poden editar.

Quan se seleccionen diverses opcions de resum, el sistema intenta resumir totes les opcions seleccionades. El resultat és que la sortida de les línies d'oferta importades serà major que si només heu seleccionat una opció de resum.

Per exemple, si el projecte té les línies d'estimació següents per a les despeses.

| Tasca | Categoria | Date | Quantitat | Preu per unitat | Import |
| --- | --- | --- | --- | --- | --- |
| Tasca A | Bitllets d'avió | 10/1/2020 | 4 | 400 | 1600 |
| Tasca B | Hotels | 10/1/2020 | 4 | 200 | 800 |
| Tasca C | Hotels | 11/1/2020 | 2 | 200 | 400 |

Quan l'usuari selecciona resumir per classe de transacció, la informació següent s'importarà.

| Tasca | Categoria | Date | Quantitat | Preu per unitat | Import |
| --- | --- | --- | --- | --- | --- |
| | | 10/1/2020 | 3.34 | 840 | 2800 |

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
