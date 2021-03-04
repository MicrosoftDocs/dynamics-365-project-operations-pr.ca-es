---
title: Creació i confirmació de diaris de correcció
description: En aquest tema es proporciona informació sobre com crear i confirmar un diari de correcció.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 6cc22168cdfefc4ae7b833bea75f68ba37c1ee67
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127732"
---
# <a name="create-and-confirm-correction-journals"></a>Creació i confirmació de diaris de correcció

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

De vegades, pot ser que s'introdueixi una entrada de temps o de despesa incorrectament. Per exemple, un consultor podria seleccionar una data incorrecta en el moment de crear una entrada de temps o podria transposar els números en introduir una despesa. Si un consultor no pot fer les actualitzacions a les entrades enviades, un administrador pot corregir directament l'entrada d'un projecte.

Per completar els procediments d'aquest tema, necessitareu permisos d'administrador.

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

Per exemple, en el gràfic següent hi ha dos elements de línia amb una quantitat de 8,00 que tenen dèbits enumerats a la columna Import. A més, hi ha dos elements de línia amb una quantitat de -8,00 que mostren els imports dels crèdits a la columna Import. Aquestes correccions aporten la quantitat a zero.

 
## <a name="correct-approved-expense-entries"></a>Correcció de les entrades de despeses aprovades

Seguiu aquests passos per corregir una o diverses entrades de despeses. 

1. A l'àrea **Vendes**, a la subfinestra de navegació esquerra, a **Transaccions**, seleccioneu **Despeses aprovades**.

2. A la llista **Despeses aprovades**, seleccioneu el projecte que voleu corregir i, a continuació, seleccioneu **Entrades correctes**. Es crearà automàticament un diari de correcció nou amb el tipus assignat **Correcció de despesa**. 

3. A la pàgina **Diari nou**, introduïu una **descripció** per a la correcció i, a la pestanya **Correcció de despeses**, a la secció **Valors nous per a les despeses**, seleccioneu els camps de dades que voleu corregir a les línies de despesa seleccionades. Per exemple, podeu assignar la despesa a un altre **Projecte**, o bé corregir les opcions **Categoria de despesa**, **Data de la despesa** o **Recurs que es pot reservar**.

4. Seleccioneu **Visualització prèvia**. Al quadre de diàleg, seleccioneu **Accepta**. 

5. Verifiqueu les correccions a la pestanya **Línies del llibre diari**. Podeu visualitzar una llista dels valors reals originals relacionats amb les entrades de despeses seleccionades que s'han invertit i les línies corresponents corregides que s'han creat.

6. Si els valors corregits es mostren segons el previst, seleccioneu **Confirma**. Al quadre de diàleg, seleccioneu **Accepta**. Si els valors no es mostren com s'esperava, seleccioneu **Cancel·la** per tornar a la llista **Despeses aprovades**. Repetiu els passos del 2 al 5. 

> [!NOTE]
> Els valors reals corregits tindran els mateixos valors que heu seleccionat a la secció **Valors nous per a les despeses**.

7. Després de confirmar el diari de correcció, torneu al projecte o als projectes que heu actualitzat, per visualitzar els canvis.  

8. A la pàgina del projecte, a la pestanya **Valors reals**, reviseu **Visualització associada de valors reals**. Les entrades originals i les corregides es mostren a la llista. En el següent gràfic es mostren els imports d'entrada de despeses originals i les quantitats d'entrada de despeses corregides corresponents. 




[!INCLUDE[footer-include](../includes/footer-banner.md)]