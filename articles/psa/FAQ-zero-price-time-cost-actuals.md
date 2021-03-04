---
title: Per què el preu predeterminat és zero en el cost de temps real?
description: Solució de problemes amb el preu predeterminat a 0 en el cost de temps real.
author: rumant
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 635fe6dfb547e8b9f96ca1786912309a770e24c2
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146246"
---
# <a name="why-is-the-price-defaulting-to-zero-on-time-cost-actuals"></a>Per què el preu predeterminat és zero en el cost de temps real?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Aquesta pregunta freqüent s'aplica als valors reals on la classe de transacció s'estableix en Temps i el tipus de transacció és Cost. Els tres controls següents us ajudaran a solucionar per què el preu està predeterminat a 0 en el cost de temps real.
 
## <a name="check-1-identify-the-cost-price-list-for-the-project"></a>Comprovació 1: identificar la llista de preus de cost per al projecte

Busqueu el projecte des del camp del projecte real i aneu a la pàgina del projecte. Feu clic a l'enllaç de la unitat de contractació al camp. A la pàgina Unitat de contractació, verifiqueu si la unitat té una llista de preus en la quadrícula de Llistes de preus de cost.

Si hi ha més d'una llista de preus, haureu aïllat el problema. El Project Service només admet una llista de preus per unitat organitzativa. Elimineu totes les llistes de preus d'aquesta entitat fins que només hi hagi una llista de preus adjunta a la quadrícula Llistes de preus de cost de la Unitat organitzativa.

Si no hi ha llistes de preus adjuntes a la Unitat organitzativa, anoteu la moneda de la Unitat organitzativa. Aneu al Project Service i després a Paràmetres i obriu la pestanya Llistes de preus. Comproveu si hi ha llistes de preus amb context establert a Cost i moneda que coincideixi amb la moneda de la Unitat organitzativa.
 
Si no hi ha llistes de preus que coincideixin amb els criteris, haureu aïllat el problema. Assegureu-vos de tenir almenys una llista de preus amb el context configurat a Cost i amb la moneda de la Unitat organitzativa.

Si hi ha més d'una llista de preus que coincideixi amb aquest criteri, continueu llegint aquest document per fer més comprovacions.

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-cost-actual"></a>Comprovació 2: Alguna de les llistes de preus identificades anteriorment és vàlida per a la data específica del cost de temps real?

Perquè el Project Service tingui en compte una llista de preus utilitzada per establir el preu per defecte, s'ha de poder aplicar per a la data del cost de temps real. Comproveu les opcions següents per veure si les llistes de preus identificades anteriorment són aplicables:

- Comproveu si les dates d'inici i finalització de la pestanya general de les llistes de preus adjuntes i mireu que no estiguin buides. Si les dates d'inici i finalització estan buides, haureu aïllat el problema. 
- Anoteu el camp de data d'inici en el cost de temps real i verifiqueu si alguna de les llistes de preus identificades és aplicable per a aquesta data. Per exemple, la data del cost de temps real ha d'estar dins de la data d'inici i la de finalització en la llista de preus. 
    - Si no hi ha cap llista de preus que cobreixi aquesta data al cost de temps real, haureu aïllat el problema. Modifiqueu les dates d'inici i finalització de la llista de preus per assegurar-vos que la llista de preus cobreix la data del cost de temps real. 
    - Si hi ha més d'una llista de preus que cobreix la data del cost de temps real, haureu aïllat el problema. Pot solucionar aquests conflictes si editeu les dates d'inici i finalització de la llista de preus perquè només hi hagi una llista de preus que cobreixi la data del cost de temps real. 
    - Si només hi ha una llista de preus que cobreixi aquesta data del cost de temps real, passeu al següent control al document.
Un cop hagueu finalitzat amb les correccions necessàries, torneu a crear una entrada de temps, aproveu-la i verifiqueu que els cost de temps real mostri un preu vàlid.

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-cost-actual"></a>Comprovació 3: Hi ha un preu a la llista de preus per a les dimensions de fixació de preus en el cost de temps real?

Si heu completat amb èxit les comprovacions 1 i 2, ara hauríeu de tenir només una llista de preus aplicable per a la data del temps de cost real. Obriu aquesta Llista de preus i aneu a la pestanya Preus de funció. Assegureu-vos que hi hagi una fila a la quadrícula per a les dimensions de fixació de preus al cost de temps real.

Si no hi ha cap fila, haureu aïllat el problema. Creeu una fila a la quadrícula de preus de funció per a les dimensions de fixació de preus al cost de temps real. Un cop fet, torneu a crear una entrada de temps, aproveu-la i verifiqueu que el cost de temps real mostri un preu vàlid.
 
Si encara no veieu un preu vàlid al cost de temps real després de realitzar les tres comprovacions anteriors, registreu una sol·licitud d'assistència tècnica.



