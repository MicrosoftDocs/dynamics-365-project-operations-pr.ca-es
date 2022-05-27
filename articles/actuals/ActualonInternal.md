---
title: Impacte real d'un projecte intern
description: Aquest tema proporciona informació sobre l'impacte a la taula Actuals en diversos esdeveniments per a un projecte intern a Microsoft Dynamics 365 Project Operations.
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
ms.openlocfilehash: 66a9ac4d2f56ae95313ed6731c3e51926105cff7
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579754"
---
# <a name="actuals-impact-for-an-internal-project"></a>Impacte real d'un projecte intern

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

La taula següent llista els reals de diferents tipus de transaccions que es creen en diversos esdeveniments en una interacció interna del projecte.

| Esdeveniment | Valor real de cost | Exemple |
|---|---|---|
| Es crea el temps. | No aplicable | <p>Bob Kozack, de la unitat organitzativa nord-americana Fabrikam que té una taxa de cost de 100 dòlars eua (100 dòlars) per hora, està treballant en un projecte que es diu "Instal·lació d'braços a Adatum". Aquest projecte s'assigna a un mètode de facturació de preu fix a la línia de contracte. Aquí teniu una entrada de temps de mostra de Bob Kozak:</p><p>Bob Kozack - 8 hores</p> |
| S'ha enviat el temps. | No aplicable | Es crea una línia de diari de cost per a l'entrada de temps. La taxa de cost per defecte s'introdueix a l'entrada del diari. |
| L'entrada de l'hora es recorda abans que s'aprovi. | No aplicable | |
| El temps està aprovat. | Es crea un cost real. | <p>Nou real que es crea:</p><ul><li>**Cost real:** Bob Kozack, 8 h, USD 800</li></ul> |
| S'ha cancel·lat l'aprovació de l'hora. | <p>L'estat d'ajust del cost original real s'actualitza a **Ajustat**.</p><p>Es crea un cost de reversió real que té un estat d'ajust d'Undjustable **·**.</p> | <p>Existents reals que s'actualitzen:</p><ul><li>**Cost real:** Bob Kozack, 8 h, USD 800, *Ajustat*</li></ul><p>Nou real que es crea per revertir l'impacte financer anterior:</p><ul><li>**Cost real:** Bob Kozack, (8 h), (USD 800), *Inajustable*</li></ul> |
| L'entrada de l'hora es recorda després d'haver estat aprovada. | <p>L'estat d'ajust del cost original real s'actualitza a **Ajustat**.</p><p>Es crea un cost de reversió real que té un estat d'ajust d'Undjustable **·**.</p> | <p>Existents reals que s'actualitzen:</p><ul><li>**Cost real:** Bob Kozack, 8 h, USD 800, *Ajustat*</li></ul><p>Nou real que es crea per revertir l'impacte financer anterior:</p><ul><li>**Cost real:** Bob Kozack, (8 h), (USD 800), *Inajustable*</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
