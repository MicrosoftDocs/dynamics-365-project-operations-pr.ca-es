---
title: Impacte real durant la fase de pre-vendes d'una interacció
description: En aquest article es proporciona informació sobre l'impacte en la taula Valors reals en diverses incidències mentre un compromís està en fase de prevendes al Microsoft Dynamics 365 Project Operations.
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
ms.openlocfilehash: d03d6ac2154806189d0d9d0b232bb317f51071ba
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922348"
---
# <a name="actuals-impact-during-the-pre-sales-stage-of-an-engagement"></a>Impacte real durant la fase de pre-vendes d'una interacció

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

A la taula següent s'enumeren els valors reals de diferents tipus de transaccions que es creen en diverses incidències durant la fase de prevendes d'un compromís de projecte intern.

| Esdeveniment | Valor real de cost | Exemple |
|---|---|---|
| Es crea el temps. | No aplicable | <p>Bob Kozack, de la unitat organitzativa Fabrikam US, que té un percentatge de cost de 100 dòlars EUA (100 USD) per hora, està treballant en un projecte que s'anomena "Instal·lació de braç a Adatum". Aquest projecte s'assigna a un mètode de facturació de preu fix a la línia de contracte. A continuació us mostrem una entrada de temps de mostra de Bob Kozak:</p><p>Bob Kozack - 8 hores</p> |
| S'envia el temps. | No aplicable | Es crea una línia del llibre diari de cost per a l'entrada de temps. El percentatge de cost per defecte s'introdueix a l'entrada del llibre diari. |
| Es recupera l'entrada de temps abans que s'aprovi. | No aplicable | |
| El temps s'aprova. | Es crea un valor real de cost. | <p>Valor real nou que es crea:</p><ul><li>**Valor real de cost**: Bob Kozack, 8 h, 800 USD</li></ul> |
| L'aprovació del temps es cancel·la. | <p>L'estat d'ajustament del valor real de cost original s'actualitza a **Ajustat**.</p><p>Es crea un valor real de cost de la reversió que té un estat d'ajustament de **No ajustable**.</p> | <p>Valor real existent que s'actualitza:</p><ul><li>**Valor real de cost**: Bob Kozack, 8 h, 800 USD, *Ajustat*</li></ul><p>Nou valor real que es crea per revertir l'impacte financer anterior:</p><ul><li>**Valor real de cost**: Bob Kozack (8 h), (800 USD), *No ajustable*</li></ul> |
| Es recupera l'entrada de temps després que s'aprovi. | <p>L'estat d'ajustament del valor real de cost original s'actualitza a **Ajustat**.</p><p>Es crea un valor real de cost de la reversió que té un estat d'ajustament de **No ajustable**.</p> | <p>Valor real existent que s'actualitza:</p><ul><li>**Valor real de cost**: Bob Kozack, 8 h, 800 USD, *Ajustat*</li></ul><p>Nou valor real que es crea per revertir l'impacte financer anterior:</p><ul><li>**Valor real de cost**: Bob Kozack (8 h), (800 USD), *No ajustable*</li></ul> |
| L'oferta es guanya i es crea un contracte. | <p>L'estat d'ajustament dels valors reals de cost originals s'actualitza a **Ajustat**.</p><p>Es creen valors reals de cost de la reversió que tenen un estat d'ajustament de **No ajustable**.</p><p>Els valors reals de cost nous es creen després de tornar a avaluar les regles contractuals.</p> | <p>Valor real existent que s'actualitza:</p><ul><li>**Valor real de cost**: Bob Kozack, 8 h, 800 USD, *Ajustat*</li></ul><p>Nou valor real que es crea per revertir l'impacte financer anterior:</p><ul><li>**Valor real de cost**: Bob Kozack (8 h), (800 USD), *No ajustable*</li></ul><p>Valors reals nous que es creen per a l'impacte financer reavaluat quan es guanya l'oferta i es crea el contracte:</p><ul><li>**Valor real de cost**: Bob Kozack, 8 h, 800 USD</li><li>**Valor real de vendes no facturades**: Bob Kozack, 8 h, 1.600 USD</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
