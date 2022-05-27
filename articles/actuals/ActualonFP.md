---
title: Impacte real en un compromís de preu fix
description: Aquest tema proporciona informació sobre l'impacte a la taula De reals en diversos esdeveniments durant el cicle de vida d'una interacció de preus fixos a Microsoft Dynamics 365 Project Operations.
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
ms.openlocfilehash: 222e7c5eefd7c619e4d7389cdaff2f96176ff275
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579216"
---
# <a name="actuals-impact-in-a-fixed-price-engagement"></a>Impacte real en un compromís de preu fix

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

La taula següent llista els reals dels diferents tipus de transaccions que es creen en diversos esdeveniments en una interacció de preu fix.

| Esdeveniment | Valor real de cost | Valor real de vendes no facturades | Vendes facturades reals | Exemple |
|---|---|---|---|---|
| Es crea el temps. | No aplicable | No aplicable | No aplicable | <p>Bob Kozack, de la unitat organitzativa nord-americana Fabrikam que té una taxa de cost de 100 dòlars eua (100 dòlars) per hora, està treballant en un projecte que es diu "Instal·lació d'braços a Adatum". Aquest projecte s'assigna a un mètode de facturació de preu fix a la línia de contracte. Aquí teniu una entrada de temps de mostra de Bob Kozak:</p><p>Bob Kozack - 8 hores</p> |
| S'ha enviat el temps. | No aplicable | No aplicable | No aplicable | Es crea una línia de diari de cost per a l'entrada de temps. La taxa de cost per defecte s'introdueix a l'entrada del diari. |
| L'entrada de l'hora es recorda abans que s'aprovi. | No aplicable | No aplicable | No aplicable | |
| El temps està aprovat. | Es crea un cost real. | No aplicable | No aplicable | <p>Nou real que es crea:</p><ul><li>**Cost real:** Bob Kozack, 8 h, USD 800</li></ul> |
| S'ha cancel·lat l'aprovació horària. | <p>L'estat d'ajust del cost original real s'actualitza a **Ajustat**.</p><p>Es crea un cost de reversió real que té un estat d'ajust d'Undjustable **·**.</p> | No aplicable | No aplicable | <p>Existents reals que s'actualitzen:</p><ul><li>**Cost real:** Bob Kozack, 8 h, USD 800, *Ajustat*</li></ul><p>Nou real que es crea per revertir l'impacte financer anterior:</p><ul><li>**Cost real:** Bob Kozack, (8 h), (USD 800), *Inajustable*</li></ul> |
| L'entrada de l'hora es recorda després d'haver estat aprovada. | <p>L'estat d'ajust del cost original real s'actualitza a **Ajustat**.</p><p>Es crea un cost de reversió real que té un estat d'ajust d'Undjustable **·**.</p> | No aplicable | No aplicable | <p>Existents reals que s'actualitzen:</p><ul><li>**Cost real:** Bob Kozack, 8 h, USD 800, *Ajustat*</li></ul><p>Nou real que es crea per revertir l'impacte financer anterior:</p><ul><li>**Cost real:** Bob Kozack, (8 h), (USD 800), *Inajustable*</li></ul> |
| El contracte està confirmat. | <p>L'estat d'ajust dels actuals de cost antics s'actualitza a **Ajustat**.</p><p>Es creen reals de costos de reversió que tenen un estat d'ajust d'Undjustable **·**.</p><p>Es creen nous costos reals després de la reavaluació de les regles contractuals.</p> | No aplicable | No aplicable | <p>Existents reals que s'actualitzen:</p><ul><li>**Cost real:** Bob Kozack, 8 h, USD 800, *Ajustat*</li></ul><p>Nou real que es crea per revertir l'impacte financer anterior:</p><ul><li>**Cost real:** Bob Kozack, (8 h), (USD 800), *Inajustable*</li></ul><p>Nou real que es crea per a l'impacte financer reavaluat:</p><ul><li>**Cost real:** Bob Kozack, 8 h, USD 800</li></ul> |
| S'ha creat una factura. | No aplicable | No aplicable | No aplicable | |
| La factura es confirma amb una fita. | No aplicable | No aplicable | Es creen nous reals de vendes facturades basades en fites. | <p>Existents que es mantenen inalterables:</p><ul><li>**Cost real:** Bob Kozack, 8 h, USD 800</li></ul><p>Nou real que es crea per registrar els valors de vendes facturats:</p><ul><li>**Vendes facturades reals:** Milestone, USD 5,000</li></ul> |
| La factura es corregeix per acreditar la fita. | No aplicable | No aplicable | Es creen els reals de vendes facturats. | <p>Existents que es mantenen inalterables:</p><ul><li>**Cost real:** Bob Kozack, 8 h, 800 USD</li></ul><p>Existents reals que s'actualitzen:</p><ul><li>**Vendes facturades reals:** Fita, USD 5,000, *Ajustada*</li></ul><p>Nou real que es crea per invertir els valors de vendes facturats anteriors:</p><ul><li>**Vendes facturades reals:** Milestone, (USD 5,000), *Undjustable*</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
