---
title: Utilitzar un recurs que es pot reservar com a dimensió de preus
description: En aquest tema es proporciona informació sobre l'ús d'un recurs disponible com a dimensió de preu.
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
ms.openlocfilehash: d9b25a768f892d83c09d37ce76291d6c8e75b1be
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144986"
---
# <a name="use-bookable-resource-as-a-pricing-dimension"></a>Utilitzar un recurs que es pot reservar com a dimensió de preus

[!include [banner](../includes/psa-now-project-operations.md)]

En aquest tema es proporciona informació sobre l'ús d'un recurs disponible com a dimensió de preu. Abans de començar, si encara no heu creat una solució de la dimensió de preus, haureu de crear-ne una de nova. Si ja teniu una solució de dimensió de preus, podeu fer els canvis en aquesta solució. Si no heu creat una solució nova per a la dimensió de preus de l'organització, completeu els procediments del tema [Crear camps i entitats personalitzats](create-custom-fields-entities.md).

## <a name="add-bookable-resource-to-forms-and-views"></a>Afegir un recurs que es pot reservar als formularis i a les visualitzacions
Per fer que els camps siguin visibles a la interfície d'usuari a la solució de la dimensió de preus, haureu de recórrer tots els formularis i les visualitzacions de les entitats clau del Project Service i afegir aquests camps als formularis i visualitzacions d'aquestes entitats.
A la taula següent es mostra una llista exhaustiva dels formularis i les visualitzacions de fàbrica, llistats per entitat, que s'han d'actualitzar. Si hi ha visualitzacions o formularis addicionals a les personalitzacions d'aquestes entitats, afegiu també els camps nous.
Obriu l'Explorador de solucions de la solució de dimensió de preus i, a continuació, feu clic a **Publica totes les personalitzacions**.


|   Entitat        | Formularis   |Visualitzacions        |
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

## <a name="set-up-bookable-resource-as-a-pricing-dimension"></a>Configurar un recurs que es pot reservar com a dimensió de preus

1. A la interfície web, aneu a **Project Service** > **Configuració** > **Paràmetres**. A la pàgina **Paràmetre**, a la pestanya **Dimensions de preus basades en el preu**, observeu que la quadrícula de la pestanya mostra els registres de l'entitat de dimensions de preus. 
2. Afegiu **Recurs que es pot reservar** a aquesta llista de dimensions de preus com a **msdyn_bookableresource**. 
3. Indiqueu el context en què el recurs disponible funciona com una dimensió de preus i definiu els valors **Aplicable al cost** i **Aplicable a les vendes**.
4. Al camp **Tipus de dimensió**, seleccioneu **Basada en la quantitat**. 
5. Seleccioneu la prioritat de costos i vendes per al recurs disponible. Normalment, quan s'inclou com a dimensió de preus, un recurs disponible té la prioritat més alta, de manera que definir-ho com a **1** (o **0** en funció de com compteu la prioritat) garantiria aquest comportament.

## <a name="set-up-pricing-dimension-field-names"></a>Configurar noms de camps de dimensions de preus

Quan el nom del camp d'una dimensió de preus a la taula **Preu de funció** és diferent del seu nom de camp a qualsevol de les altres entitats en què ha de treballar el preu per defecte, el registre de la dimensió de preus ha de ser conscient dels diferents noms.    
Per a un recurs que es pot reservar, l'entitat **Membres de l'equip del projecte** té un nom de camp lleugerament diferent (**msdyn_bookableresourceid**) de com s'anomena a l'entitat **Preu de la funció** (**msdyn_ bookableresource**). El registre de la dimensió de preus de **msydn_bookableresource** s'ha de fer conscient d'això. 
1. Per fer-ho, feu doble clic a la fila de la quadrícula **Dimensions de preus** per obrir la pàgina de dimensió de **msdyn_bookableresource**.
2. A la pàgina dimensió, a la pestanya **Relacionat**, feu clic a **Noms de camp de dimensions de preus**.

 ![Pestanya Noms de camps de dimensions de preu](media/PD-fieldname.png)

4. A la visualització associada que s'obre , feu clic a **Afegeix un nou nom del camp de la dimensió de preus**.

 ![Afegeix nous noms de camps de dimensions de preus](media/Add-NewPD-fieldname.png)


S'obre la pàgina **Nou nom de camp de dimensions de preus** per a **msdyn_bookableresource**. 

5. Afegiu **msdyn_projectteam** al camp **Nom lògic de l'entitat** i **msdyn_bookableresourceid** al camp **Nom del camp**. Desar el registre.

 ![Formulari Afegeix nous noms de camps de dimensions de preus](media/PD-fieldname-Added.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]