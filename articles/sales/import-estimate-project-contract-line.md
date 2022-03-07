---
title: Importació d'una estimació a una línia de contracte basada en projecte
description: En aquest tema es proporciona informació sobre com importar estimacions d'un projecte a una línia de contracte.
author: rumant
ms.date: 10/19/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ea513ca8126eadbf563f3c6cb3e966f81703ae805d12881f865cdc1dd77e191d
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6990079"
---
# <a name="import-an-estimate-to-a-project-based-contract-line"></a>Importació d'una estimació a una línia de contracte basada en projecte

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

Al Dynamics 365 Project Operations, podeu importar les estimacions d'un projecte en una línia de contracte basada en projectes.

1. Verifiqueu que el camp **Projecte** en la línia de contracte basada en el projecte estigui emplenat.
2. A la pestanya **Detalls de la línia de contracte**, a la subquadrícula, seleccioneu **Importa de l'estimació del projecte**. S'obre una pàgina de diàleg amb les opcions de resum. Les opcions de resum disponibles són: **Classe de transacció**, **Categoria**, **Funció** i **Tasca del projecte**. En funció de les seleccions de resum, es copia la estimació del projecte per a totes les classes de transaccions incloses en aquesta línia de contracte. 
3. Per comprovar les classes de transacció que s'inclouen, seleccioneu la pestanya **General** de la línia de contracte i comproveu els valors dels camps **Inclou el temps**, **Inclou les despeses** i **Inclou els impostos**.

Quan importeu estimacions, l'aplicació triarà per defecte els preus segons les llistes de preus del projecte enllaçades al contracte i el tipus de facturació que s'hagi definit a la línia de contracte. Si una funció o categoria es configura a la línia de contracte com a no imputable, la línia d'estimació importada d'aquesta funció o categoria és no imputable i no s'afegirà al valor contractat de la línia d'oferta.

Quan una línia de contracte té detalls de línia, els camps **Valor del contracte** i **Impostos estimats** de la línia de contracte es resumeixen i no es poden editar.

Quan se seleccionen diverses opcions de resum, el sistema intenta resumir totes les opcions seleccionades. La sortida del resum dona com a resultat més línies de contracte importades que si seleccioneu només una opció de resum.

Per exemple, si el projecte tenia les línies d'estimació següents per a les despeses:

| Tasca | Categoria | Date | Quantitat | Preu per unitat | Import |
| --- | --- | --- | --- | --- | --- |
| Tasca A | Bitllets d'avió | 10/1/2020 | 4 | 400 | 1600 |
| Tasca B | Hotels | 10/1/2020 | 4 | 200 | 800 |
| Tasca C | Hotels | 11/1/2020 | 2 | 200 | 400 |

Quan l'usuari selecciona resumir per **Classe de transacció**, la informació següent s'importarà:

| Tasca | Categoria | Date | Quantitat | Preu per unitat | Import |
| --- | --- | --- | --- | --- | --- |
| &nbsp;  | &nbsp;  | 10/1/2020 | 3.34 | 840 | 2800 |

Quan l'usuari selecciona resumir per **Classe de transacció** i **Categoria**, la informació següent s'importarà:

| Tasca | Categoria | Date | Quantitat | Preu per unitat | Import |
| --- | --- | --- | --- | --- | --- |
| Tasca A | Bitllets d'avió | 10/1/2020 | 4 | 400 | 1600 |
| &nbsp;  | Hotels | 10/1/2020 | 6 | 200 | 1200 |

Quan l'usuari selecciona resumir per **Classe de transacció**, **Categoria** i **Tasca de node fulla**, s'importarà el següent. Observeu que aquest resultat és el mateix que el que hi havia al projecte:

| Tasca | Categoria | Date | Quantitat | Preu per unitat | Import |
| --- | --- | --- | --- | --- | --- |
| Tasca A | Bitllets d'avió | 10/1/2020 | 4 | 400 | 1600 |
| Tasca B | Hotels | 10/1/2020 | 4 | 200 | 800 |
| Tasca C | Hotels | 11/1/2020 | 2 | 200 | 400 |


[!INCLUDE[footer-include](../includes/footer-banner.md)]