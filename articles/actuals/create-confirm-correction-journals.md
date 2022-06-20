---
title: Creació i confirmació de diaris de correcció
description: Aquest article proporciona informació sobre com crear i confirmar una revista de correcció.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 70886aa5a3060fa58461ce215e4de3b7286093e3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928052"
---
# <a name="create-and-confirm-correction-journals"></a>Creació i confirmació de diaris de correcció

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

De tant en tant, es pot introduir incorrectament una entrada de temps o de despeses. Per exemple, un consultor pot seleccionar la data incorrecta quan crea una entrada d'hora o pot seleccionar un projecte equivocat quan introdueixi una despesa. Si un consultor no pot actualitzar les entrades enviades, un administrador de back-end pot corregir directament els reals d'un projecte.

## <a name="correct-approved-time-entries"></a>Correcció de les entrades de temps aprovades     

Completeu els passos següents per corregir una o diverses entrades de temps d'un projecte.

1. A l'àrea **Vendes'**, seleccioneu **Transaccions** i, a continuació, seleccioneu **Temps aprovat**. 

2. A la llista **Temps aprovat**, localitzeu i seleccioneu una o diverses entrades de temps aprovades per corregir. Podeu utilitzar el filtre per cercar entrades relacionades. Per exemple, podeu aplicar el filtre segons un ID de projecte i seleccionar totes les entrades de temps aprovades amb l'identificador del projecte.

3. Seleccioneu **Entrades correctes**. Es crearà automàticament un diari de correcció nou amb el tipus assignat **Correcció de temps**. Les entrades que heu seleccionat s'afegiran al diari. 

4. A la pàgina **Diari nou**, introduïu una **descripció** per al diari de correcció i, a continuació, seleccioneu la pestanya **Correccions d'entrades de temps**.  

5. A la secció **Valors nous per a les entrades de temps**, actualitzeu els camps amb la informació correcta segons calgui. Per exemple, podeu canviar el projecte assignat o el recurs que es pot reservar.

6. Seleccioneu **Visualització prèvia**. Al quadre de diàleg, seleccioneu **Accepta**. A la pestanya **Línies del llibre diari**, podeu visualitzar una llista dels valors reals originals relacionats amb les entrades de temps seleccionades que s'han invertit i les línies corresponents corregides que s'han creat. Si s'han de fer correccions addicionals, repetiu els passos 5 i 6. 

    > [!NOTE]
    > Tots els valors reals corregits tindran els mateixos valors que heu seleccionat a la secció **Valors nous per a les entrades de temps**.

7. Si les correccions es mostren segons el previst, seleccioneu **Confirma**. Al quadre de diàleg, seleccioneu **Accepta**.

8. Torneu a l'àrea **Vendes**, seleccioneu **Projectes** i, a continuació, obriu el projecte per al qual acabeu d'actualitzar les entrades de temps. 

9. A la pàgina **Projectes**, de la pestanya **Valors reals**, visualitzeu els canvis que heu fet. 

    > [!NOTE]
    > Si la pestanya **Valors reals** no està visible, seleccioneu **Relacionat** > **Valors reals**.  

10. A la llista **Visualització associada de valors reals**, podeu veure que les entrades de temps originals que s'han invertit encara es mostren, així com les entrades de temps corregides corresponents. 

 
## <a name="correct-approved-expense-entries"></a>Correcció de les entrades de despeses aprovades

Seguiu aquests passos per corregir una o diverses entrades de despeses. 

1. A l'àrea **Vendes**, a la subfinestra de navegació esquerra, a **Transaccions**, seleccioneu **Despeses aprovades**.

2. A la llista **Despeses aprovades**, seleccioneu el projecte que voleu corregir i, a continuació, seleccioneu **Entrades correctes**. Es crearà automàticament un diari de correcció nou amb el tipus assignat **Correcció de despesa**. 

3. A la pàgina **Diari nou**, introduïu una **descripció** per a la correcció i, a la pestanya **Correcció de despeses**, a la secció **Valors nous per a les despeses**, seleccioneu els camps de dades que voleu corregir a les línies de despesa seleccionades. Per exemple, podeu assignar la despesa a un altre **Projecte**, o bé corregir les opcions **Categoria de despesa**, **Data de la despesa** o **Recurs que es pot reservar**.

4. Seleccioneu **Visualització prèvia**. Al quadre de diàleg, seleccioneu **Accepta**. 

5. Verifiqueu les correccions a la pestanya **Línies del llibre diari**. Podeu visualitzar una llista dels valors reals originals relacionats amb les entrades de despeses seleccionades que s'han invertit i les línies corresponents corregides que s'han creat.

6. Si els valors corregits es mostren segons el previst, seleccioneu **Confirma**. Al quadre de diàleg, seleccioneu **Accepta**. Si els valors no es mostren com s'esperava, seleccioneu **Cancel·la** per tornar a la llista **Despeses aprovades**. Repetiu els passos del 2 al 5. 

7. Després de confirmar el diari de correcció, torneu al projecte o als projectes que heu actualitzat per veure els canvis.

8. A la pàgina del projecte, a la **pestanya Fets reals**, reviseu la **llista Visualització** associada real. Les entrades originals i les corregides es mostren a la llista.


## <a name="correct-approved-material-usage-logs"></a>Corregir els registres d'ús de material aprovats

Completeu els passos següents per corregir una o més entrades de registre d'ús de material.

1. A l'àrea **Vendes**, a la subfinestra de navegació de l'esquerra, a **Transaccions**, seleccioneu **Actuals**.

2. A la **llista Actuals**, utilitzeu filtres de columna per seleccionar la **classe de transacció Material**, de manera que només es mostrin els reals dels materials. Utilitzeu altres filtres de columna per limitar encara més els reals que es mostren. Després de trobar el conjunt de reals desitjat, seleccioneu els reals i, a **continuació, seleccioneu** Entrades correctes. Es crea automàticament una nova revista de correcció i s'assigna el **tipus de correcció** material.

3. A la **pàgina Nou diari**, al **camp Descripció**, introduïu una descripció per a la correcció. A continuació, a la **pestanya Correcció** de materials, a la **secció Valors nous per a materials**, seleccioneu els camps de dades que cal corregir per a les línies de material seleccionades. Per exemple, podeu assignar el material a un altre projecte o corregir el producte, la data del material o la subcontractació.

4. Seleccioneu **Visualització prèvia**. A continuació, al quadre de diàleg, seleccioneu **D'acord**.

5. A la **pestanya Línies** del diari, verifiqueu les correccions. Podeu veure una llista dels reals originals que estan relacionats amb les entrades de material seleccionades que s'han invertit i les línies corresponents corregides que s'han creat.

6. Si els valors corregits es mostren segons el previst, seleccioneu **Confirma**. A continuació, al quadre de diàleg, seleccioneu **D'acord**. Si els valors no són els esperats, seleccioneu **Cancel·la** per tornar a la **llista De reals.** Repetiu els passos del 2 al 5.

7. Després de confirmar el diari de correcció, torneu al projecte o als projectes que heu actualitzat per veure els canvis.

8. A la pàgina del projecte, a la **pestanya Fets reals**, reviseu la **llista Visualització** associada real. Les entrades originals i les corregides es mostren a la llista.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
