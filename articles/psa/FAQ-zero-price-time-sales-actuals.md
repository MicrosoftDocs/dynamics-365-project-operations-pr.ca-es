---
title: Per què el preu predeterminat és zero en les vendes de temps real?
description: Solució de problemes amb el preu predeterminat a 0 en les vendes de temps real.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: e32b4c8113afdc18d9b220b1a8daf5007be93ac8
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6011629"
---
# <a name="why-is-price-defaulting-to-zero-on-time-sales-actuals"></a>Per què el preu predeterminat és zero en les vendes de temps real?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Aquesta pregunta freqüent s'aplica als valors reals on la classe de transacció s'estableix en Temps i el tipus de transacció és Vendes no facturades. Els tres controls següents us ajudaran a solucionar per què el preu (tarifa de facturació) està predeterminat a 0 en vendes de temps reals.

## <a name="check-1-identify-the-sales-price-list-for-the-project"></a>Comprovació 1: identificar la llista de preus de vendes per al projecte

Busqueu el projecte des del camp del projecte real i aneu a la pàgina del projecte. A continuació, aneu a la pestanya Vendes i a la quadrícula Línies de contracte de projecte, feu clic a l'enllaç en el camp Contracte de projecte. La pàgina del contracte del projecte s'obrirà. A la pàgina Contracte del projecte, aneu a la pestanya Llistes de preus del projecte. Comproveu si hi ha almenys una llista de preus adjunta. Si no hi ha una llista de preus adjunta a la quadrícula de Llistes de preus del Contracte de projecte, haureu aïllat el problema. Adjunteu una llista de preus a la quadrícula Llistes de preus del projecte. Les llistes de preus que es poden adjuntar han de tenir el camp de context establert en Vendes i el camp de moneda a la llista de preus ha de coincidir amb el camp de moneda al Contracte del projecte. Un cop hagueu finalitzat amb les correccions necessàries, torneu a crear una entrada de temps, aproveu-la i verifiqueu que les vendes no facturades reals mostrin un preu vàlid. 

Si teniu una o més llistes de preus adjuntes a la graella de Llistes de preus del projecte del Contracte del projecte, aneu a la comprovació següent del document.

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-sales-actual"></a>Comprovació 2: Alguna de les llistes de preus identificades anteriorment és vàlida per a la data específica de les vendes de temps real?

Perquè el Project Service tingui en compte una llista de preus utilitzada per establir el preu per defecte, s'ha de poder aplicar per a la data de les vendes de temps real. Comproveu les opcions següents per veure si les llistes de preus identificades anteriorment són aplicables:
- Comproveu si les dates d'inici i finalització de la pestanya general de les llistes de preus adjuntes i mireu que no estiguin buides. Si les dates d'inici i finalització estan buides, haureu aïllat el problema. 
- Anoteu el camp de data d'inici en les vendes de temps real i verifiqueu si alguna de les llistes de preus identificades és aplicable per a aquesta data. Per exemple, la data de les vendes de temps real ha d'estar dins de la data d'inici i la de finalització en la llista de preus. 
    - Si no hi ha cap llista de preus que cobreixi aquesta data a les vendes de temps real, haureu aïllat el problema. Modifiqueu les dates d'inici i finalització de la llista de preus per assegurar-vos que la llista de preus cobreix la data de les vendes de temps real. 
    - Si hi ha més d'una llista de preus que cobreix la data de les vendes de temps real, haureu aïllat el problema. Pot solucionar aquests conflictes si editeu les dates d'inici i finalització de la llista de preus perquè només hi hagi una llista de preus que cobreixi la data de les vendes de temps real. 
    - Si només hi ha una llista de preus que cobreixi aquesta data, aneu a la comprovació 3.
Un cop hagueu finalitzat amb les correccions necessàries, torneu a crear una entrada de temps, aproveu-la i verifiqueu que les vendes de temps real mostrin un preu vàlid.

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-sales-actual"></a>Comprovació 3: Hi ha un preu a la llista de preus per a les dimensions de fixació de preus en les vendes de temps real?

Si heu completat amb èxit les comprovacions 1 i 2, ara hauríeu de tenir només una llista de preus aplicable per a la data de les vendes de temps real. Obriu aquesta Llista de preus i aneu a la pestanya Preus de funció. Assegureu-vos que hi hagi una fila a la quadrícula per a les dimensions de fixació de preus a les vendes de temps real.

Si no hi ha cap fila, haureu aïllat el problema. Creeu una fila a la quadrícula de preus de funció per a les dimensions de fixació de preus a les vendes de temps real. Un cop fet, torneu a crear una entrada de temps, aproveu-la i verifiqueu que les vendes de temps real mostrin un preu vàlid.

Si encara no veieu un preu vàlid a les vendes de temps reals després de seguir les tres comprovacions anteriors, registreu una sol·licitud d'assistència tècnica. 



[!INCLUDE[footer-include](../includes/footer-banner.md)]