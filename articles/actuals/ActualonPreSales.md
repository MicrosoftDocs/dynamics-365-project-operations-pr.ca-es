---
title: Impacte real durant la fase de prevenda d'un compromís
description: Aquest tema proporciona informació sobre l'impacte a la taula Des de fets en diversos esdeveniments, mentre que un engagment es troba en la fase de prevenda a Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 02/22/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: ad62639b345d5519b103d4bde3fbb033b9a7a519
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8577224"
---
# <a name="actuals-impact-during-the-pre-sales-stage-of-an-engagement"></a>Impacte real durant la fase de prevenda d'un compromís

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

La taula següent llista els reals de diferents tipus de transaccions que es creen en diversos esdeveniments durant la fase de prevenda d'un engagement del projecte.

| Esdeveniment | Valor real de cost | Exemple |
|---|---|---|
| Es crea el temps. | No aplicable | <p>Bob Kozack, de la unitat organitzativa nord-americana Fabrikam que té una taxa de cost de 100 dòlars eua (100 dòlars) per hora, està treballant en un projecte que es diu "Instal·lació d'braços a Adatum". Aquest projecte s'assigna a un mètode de facturació de preu fix a la línia de contracte. Aquí teniu una entrada de temps de mostra de Bob Kozak:</p><p>Bob Kozack - 8 hores</p> |
| S'ha enviat el temps. | No aplicable | Es crea una línia de diari de cost per a l'entrada de temps. La taxa de cost per defecte s'introdueix a l'entrada del diari. |
| L'entrada de l'hora es recorda abans que s'aprovi. | No aplicable | |
| El temps està aprovat. | Es crea un cost real. | <p>Nou real que es crea:</p><ul><li>**Cost real:** Bob Kozack, 8 h, USD 800</li></ul> |
| S'ha cancel·lat l'aprovació horària. | <p>L'estat d'ajust del cost original real s'actualitza a **Ajustat**.</p><p>Es crea un cost de reversió real que té un estat d'ajust d'Undjustable **·**.</p> | <p>Existents reals que s'actualitzen:</p><ul><li>**Cost real:** Bob Kozack, 8 h, USD 800, *Ajustat*</li></ul><p>Nou real que es crea per revertir l'impacte financer anterior:</p><ul><li>**Cost real:** Bob Kozack, (8 h), (USD 800), *Inajustable*</li></ul> |
| L'entrada de l'hora es recorda després d'haver estat aprovada. | <p>L'estat d'ajust del cost original real s'actualitza a **Ajustat**.</p><p>Es crea un cost de reversió real que té un estat d'ajust d'Undjustable **·**.</p> | <p>Existents reals que s'actualitzen:</p><ul><li>**Cost real:** Bob Kozack, 8 h, USD 800, *Ajustat*</li></ul><p>Nou real que es crea per revertir l'impacte financer anterior:</p><ul><li>**Cost real:** Bob Kozack, (8 h), (USD 800), *Inajustable*</li></ul> |
| L'oferta es guanya i es crea un contracte. | <p>L'estat d'ajust dels actuals de cost antics s'actualitza a **Ajustat**.</p><p>Es creen reals de costos de reversió que tenen un estat d'ajust d'Undjustable **·**.</p><p>Es creen nous costos reals després de la reavaluació de les regles contractuals.</p> | <p>Existents reals que s'actualitzen:</p><ul><li>**Cost real:** Bob Kozack, 8 h, USD 800, *Ajustat*</li></ul><p>Nou real que es crea per revertir l'impacte financer anterior:</p><ul><li>**Cost real:** Bob Kozack, (8 h), (USD 800), *Inajustable*</li></ul><p>Nous reals que es creen per a l'impacte financer reavaluat quan es guanya l'oferta i es crea el contracte:</p><ul><li>**Cost real:** Bob Kozack, 8 h, USD 800</li><li>**Vendes nobil·lades reals:** Bob Kozack, 8 h, USD 1,600</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
