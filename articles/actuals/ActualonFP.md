---
title: Impacte real en una interacció amb els preus fixos
description: En aquest article es proporciona informació sobre l'impacte en la taula Valors reals en diverses incidències durant el cicle de vida d'un compromís de preu fix al Microsoft Dynamics 365 Project Operations.
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
ms.openlocfilehash: 50819d77d56935bfe5438d7d9dae99562bcc0b49
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918116"
---
# <a name="actuals-impact-in-a-fixed-price-engagement"></a>Impacte real en una interacció amb els preus fixos

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

A la taula següent s'enumeren els valors reals de diferents tipus de transaccions que es creen en diverses incidències d'un compromís de preu fix.

| Esdeveniment | Valor real de cost | Valor real de vendes no facturades | Valor real de vendes facturades | Exemple |
|---|---|---|---|---|
| Es crea el temps. | No aplicable | No aplicable | No aplicable | <p>Bob Kozack, de la unitat organitzativa Fabrikam US, que té un percentatge de cost de 100 dòlars EUA (100 USD) per hora, està treballant en un projecte que s'anomena "Instal·lació de braç a Adatum". Aquest projecte s'assigna a un mètode de facturació de preu fix a la línia de contracte. A continuació us mostrem una entrada de temps de mostra de Bob Kozak:</p><p>Bob Kozack - 8 hores</p> |
| S'envia el temps. | No aplicable | No aplicable | No aplicable | Es crea una línia del llibre diari de cost per a l'entrada de temps. El percentatge de cost per defecte s'introdueix a l'entrada del llibre diari. |
| Es recupera l'entrada de temps abans que s'aprovi. | No aplicable | No aplicable | No aplicable | |
| El temps s'aprova. | Es crea un valor real de cost. | No aplicable | No aplicable | <p>Valor real nou que es crea:</p><ul><li>**Valor real de cost**: Bob Kozack, 8 h, 800 USD</li></ul> |
| L'aprovació del temps es cancel·la. | <p>L'estat d'ajustament del valor real de cost original s'actualitza a **Ajustat**.</p><p>Es crea un valor real de cost de la reversió que té un estat d'ajustament de **No ajustable**.</p> | No aplicable | No aplicable | <p>Valor real existent que s'actualitza:</p><ul><li>**Valor real de cost**: Bob Kozack, 8 h, 800 USD, *Ajustat*</li></ul><p>Nou valor real que es crea per revertir l'impacte financer anterior:</p><ul><li>**Valor real de cost**: Bob Kozack (8 h), (800 USD), *No ajustable*</li></ul> |
| Es recupera l'entrada de temps després que s'aprovi. | <p>L'estat d'ajustament del valor real de cost original s'actualitza a **Ajustat**.</p><p>Es crea un valor real de cost de la reversió que té un estat d'ajustament de **No ajustable**.</p> | No aplicable | No aplicable | <p>Valor real existent que s'actualitza:</p><ul><li>**Valor real de cost**: Bob Kozack, 8 h, 800 USD, *Ajustat*</li></ul><p>Nou valor real que es crea per revertir l'impacte financer anterior:</p><ul><li>**Valor real de cost**: Bob Kozack (8 h), (800 USD), *No ajustable*</li></ul> |
| El contracte es confirma. | <p>L'estat d'ajustament dels valors reals de cost originals s'actualitza a **Ajustat**.</p><p>Es creen valors reals de cost de la reversió que tenen un estat d'ajustament de **No ajustable**.</p><p>Els valors reals de cost nous es creen després de tornar a avaluar les regles contractuals.</p> | No aplicable | No aplicable | <p>Valor real existent que s'actualitza:</p><ul><li>**Valor real de cost**: Bob Kozack, 8 h, 800 USD, *Ajustat*</li></ul><p>Nou valor real que es crea per revertir l'impacte financer anterior:</p><ul><li>**Valor real de cost**: Bob Kozack (8 h), (800 USD), *No ajustable*</li></ul><p>Nou valor real que es crea per a l'impacte financer reavaluat:</p><ul><li>**Valor real de cost**: Bob Kozack, 8 h, 800 USD</li></ul> |
| Es crea una factura. | No aplicable | No aplicable | No aplicable | |
| La factura es confirma amb una fita. | No aplicable | No aplicable | Es creen nous valors reals de vendes facturades basades en fites. | <p>Valor real existent que roman sense canvis:</p><ul><li>**Valor real de cost**: Bob Kozack, 8 h, 800 USD</li></ul><p>Valor real nou que es crea per registrar els valors de vendes facturades:</p><ul><li>**Valor real de vendes facturades**: fita, 5.000 USD</li></ul> |
| La factura es corregeix per abonar la fita. | No aplicable | No aplicable | Es creen valors reals de vendes facturades de reversió. | <p>Valor real existent que roman sense canvis:</p><ul><li>**Valor real de cost**: Bob Kozack, 8 h, 800 USD</li></ul><p>Valor real existent que s'actualitza:</p><ul><li>**Valor real de vendes facturades**: fita, 5.000 USD, *Ajustat*</li></ul><p>Valor real nou que es crea per revertir els valors de vendes facturades anteriors:</p><ul><li>**Valor real de vendes facturades**: fita, (5.000 USD), *No es pot ajustar*</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
