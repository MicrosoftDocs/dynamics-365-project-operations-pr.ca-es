---
title: Per què el preu predeterminat és zero en les dades de vendes de despeses?
description: Els tres controls següents us ajudaran a solucionar per què el preu està predeterminat a 0 en vendes de despeses reals.
author: rumant
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.prod: Applies to all versions of Project Service
ms.technology: Applies to all versions of Project Service
ms.assetid: 85a177ec-ad61-450d-bfe6-cdea7a415566
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: ccbad4ac969ffe4f09744557e2a9be68aa93e8c2
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749558"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-sales-actuals"></a>Per què el preu predeterminat és zero en les dades de vendes de despeses?

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Aquesta pregunta freqüent s'aplica als valors reals de despeses on la classe de transacció s'estableix en Despeses i el tipus de transacció és Vendes no facturades. Els tres controls següents us ajudaran a solucionar per què el preu (tarifa de facturació) està predeterminat a 0 en vendes de despeses reals.

## <a name="check-1-identify-the-sales-price-list-for-project"></a>Comprovació 1: identificar la llista de preus de vendes per al projecte

Busqueu el projecte des del camp del projecte real i aneu a la pàgina del projecte. A continuació, aneu a la pestanya Vendes. A la quadrícula Línies de contracte de projecte, feu clic a l'enllaç en el camp Contracte de projecte. La pàgina del contracte del projecte s'obrirà. A la pàgina Contracte del projecte, aneu a la pestanya Llistes de preus del projecte. Comproveu si hi ha almenys una llista de preus adjunta.

Si no hi ha una llista de preus adjunta a la quadrícula de Llistes de preus del Contracte de projecte, feu el següent:

- Adjunteu una llista de preus a la quadrícula Llistes de preus del projecte. Les llistes de preus que es poden adjuntar han de tenir el camp de context establert en Vendes i el camp de moneda a la llista de preus ha de coincidir amb el camp de moneda al Contracte del projecte. Un cop hagueu realitzat les correccions necessàries, torneu a crear una entrada de despeses, aproveu-la i verifiqueu que les vendes no facturades reals mostrin un preu vàlid.
- Si teniu una o més llistes de preus adjuntes a la graella de Llistes de preus del projecte del Contracte del projecte, aneu a Comprovació 2.

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-expense-actual"></a>Comprovació 2: Alguna de les llistes de preus identificades anteriorment és vàlida per a la data específica de la despesa real?

Perquè el Project Service tingui en compte una llista de preus utilitzada per establir el preu per defecte, s'ha de poder aplicar per a la data de les vendes de despeses reals. Comproveu les opcions següents per veure si les llistes de preus identificades anteriorment són aplicables:

- Comenceu per les dates d'inici i finalització de la pestanya general de les llistes de preus adjuntes i mireu que no estiguin buides. Si les dates d'inici i finalització estan buides, haureu aïllat el problema. 
- Anoteu el camp de data d'inici en les vendes de despeses reals i verifiqueu si alguna de les llistes de preus identificades és aplicable per a aquesta data. Per exemple, la data de la despesa real ha d'estar dins de la data d'inici i la de finalització en la llista de preus. 
    - Si no hi ha cap llista de preus que cobreixi aquesta data en les vendes de despeses reals, haureu aïllat el problema. Modifiqueu les dates d'inici i finalització de la llista de preus per assegurar-vos que la llista de preus cobreix la data de la despesa real. 
    - Si hi ha més d'una llista de preus que cobreix la data de les vendes de despeses reals, haureu aïllat el problema. Pot solucionar aquests conflictes si editeu les dates d'inici i finalització de la llista de preus perquè només hi hagi una llista de preus que cobreixi la data de la despesa real. 
    - Si només hi ha una llista de preus que cobreixi aquesta data, passeu a la comprovació 3.
Un cop hagueu finalitzat amb les correccions necessàries, torneu a crear una entrada de despeses, aproveu-la i verifiqueu que les vendes no facturades reals mostrin un preu vàlid.

## <a name="check-3-is-there-a-valid-price-for-the-expense-category-in-the-applicable-project-price-list"></a>Comprovació 3: Hi ha un preu vàlid per a la categoria de despeses en la llista de preus del projecte aplicable? 

Si heu completat amb èxit les comprovacions 1 i 2, ara hauríeu de tenir només una llista de preus del projecte aplicable per a la data de les vendes de despeses reals. Obriu aquesta Llista de preus del projecte i aneu a la pestanya Preus de categoria. Assegureu-vos que hi hagi una fila a la quadrícula per a la categoria de despesa específica en la Despesa real.
 
- Si no hi ha cap fila, haureu aïllat el problema. Creeu una fila a la quadrícula Preus de categoria per a la categoria de la vostra despesa real. Un cop fet, torneu a crear una entrada de despeses, aproveu-la i verifiqueu que les vendes no facturades reals mostrin un preu vàlid. 
- Si hi ha una fila per a la categoria de despeses en la quadrícula de preus de la categoria, comproveu que tingui un preu vàlid.

Per entendre quin preu és vàlid, utilitzeu aquests mètodes:

- Si el camp Mètode de fixació de preus en la línia de Preu de categoria s'estableix a A partir del cost, la taxa unitària a les vendes de despeses reals s'establirà per defecte en el valor de l'entrada Despeses.
- Si el camp Mètode de fixació de preus en la línia de Preu de categoria s'estableix a Percentatge de marge comercial, verifiqueu si el camp Percentatge està establert en un valor vàlid. La taxa unitària en les vostres vendes de despeses està predeterminada perquè s'aplica aquest percentatge de marge comercial al preu a l'entrada de Despeses.
- Si el camp Mètode de fixació de preus en la línia de Preu de categoria s'estableix a Preu per unitat, verifiqueu si el camp Preu està establert en un valor vàlid. La taxa unitària en les vendes de despeses reals s'ha d'establir per defecte en la quantitat de moneda especificada en el camp Preu.

Si la configuració del preu per a la categoria de despeses no és vàlida, haureu aïllat el problema. La solució és editar la línia de preu de la categoria amb un preu vàlid per a la categoria de despesa d'acord amb les regles anteriors. Un cop fet això, torneu a crear una entrada de despeses, aproveu-la i comproveu que les vendes no facturades reals tinguin un preu vàlid.

Si encara no veieu un preu vàlid a les vendes de despeses reals després de fer les tres comprovacions anteriors, registreu una sol·licitud d'assistència tècnica.


