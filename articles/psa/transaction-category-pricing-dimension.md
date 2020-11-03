---
title: Utilitzar una categoria de transacció com a dimensió de preus
description: En aquest tema es proporciona informació sobre l'ús d'una categoria de transacció com a dimensió de preu.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 0019571a1d37d3b6a503e7221db3c3b51365c236
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072296"
---
# <a name="use-transaction-category-as-a-pricing-dimension"></a>Utilitzar una categoria de transacció com a dimensió de preus
En aquest tema es mostra com utilitzar una categoria de transacció com a dimensió de preu. Abans de començar, si encara no heu creat una solució de la dimensió de preus, haureu de crear-ne una de nova. Si ja teniu una solució de dimensió de preus, podeu fer els canvis en aquesta solució. Si no heu creat una solució nova per a la dimensió de preus de l'organització, completeu els procediments del tema [Crear camps i entitats personalitzats](create-custom-fields-entities.md).

## <a name="add-transaction-category-to-forms-and-views"></a>Afegir una categoria de transacció als formularis i a les visualitzacions
Per fer que la categoria de transacció sigui visible a la interfície d'usuari a la solució de la dimensió de preus, haureu de recórrer tots els formularis i les visualitzacions de les entitats clau i afegir aquests camps als formularis i visualitzacions d'aquestes entitats.
La taula següent és una llista exhaustiva dels formularis i les visualitzacions de fàbrica, llistats per entitat, que s'han d'actualitzar amb els nous camps. Si hi ha visualitzacions o formularis addicionals a les personalitzacions d'aquestes entitats, afegiu-hi també els camps nous.

|  Entitat        | Formularis     |Visualitzacions        |
| ------------------------------|---------------------------------|----------------------------------|
|  Preu per funció|• Informació |• Preus de categories de recursos actius<br> • Visualització associada de preus de categories de recursos|
|  Marge comercial de preu de funció|• Informació|• Marge comercial de preu de funcions actives<br>• Visualització associada de marge comercial de preus de la funció|
|  Detall de la línia d'oferta|• Informació del projecte<br>• Creació ràpida de projectes|• Detall de la línia d'oferta activa<br>• Detalls de la línia d'oferta combinada<br>• Visualització associada de detall de la línia d'oferta|
|  Detall de la línia de contracte del projecte|• Informació del projecte<br>• Creació ràpida de projectes|• Detalls de la línia de contracte combinada<br>• Detalls de la línia de contracte activa<br>• Visualització associada de detalls de la línia de contracte|
|  Tasca del projecte|• Informació<br>• Formulari nou||
|  Membre de l'equip del projecte|• Informació<br>• Formulari nou|• Membres de l'equip del projecte actius<br>• Membres de l'equip del projecte<br>• Visualització associada de membres de l'equip del projecte|
|  Entrada de temps|• Informació<br>• Crear entrada de temps|• Les meves entrades de temps per data<br>• Les meves entrades de temps aquesta setmana<br>• Entrades de temps pendents d'aprovació|
|  Línia del llibre diari|• Informació<br>• Creació ràpida:|• Línies del llibre diari actives<br>• Visualització associada de les línies del llibre diari|
|  Detall de la línia de factura|• Informació<br>• Creació ràpida:|• Detalls de la línia de factura activa<br>• Transaccions de factura imputables<br>• Transaccions de factura gratuïtes<br>• Visualització associada de detall de la línia de factura<br>• Transaccions de factura no imputables|
|  Real|• Informació<br>• Valors reals actius|• Visualització associada de valors reals|

## <a name="set-up-transaction-category-as-a-pricing-dimension"></a>Configurar una categoria de transacció com a dimensió de preus

1. A la interfície web, aneu a **Project Service** > **Configuració** > **Paràmetres**. 
2. A la pàgina **Paràmetres** , a la pestanya **Dimensions de preus basades en l'import** , observeu que la quadrícula de la pestanya mostra els registres de l'entitat **Dimensions de preus**.
3. Afegiu **Categoria de la transacció** a aquesta llista i definiu els camps **Aplicable al cost** i **Aplicable a la venda** com a **Sí**.
4. Al camp **Tipus de dimensió** , seleccioneu **Basada en la quantitat** i, a continuació, seleccioneu la prioritat per a la **Categoria de transacció** relacionada amb el cost i les vendes.