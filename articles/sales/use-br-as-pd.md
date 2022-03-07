---
title: Utilització d'un recurs que es pot reservar com a dimensió de preus
description: En aquest tema es proporciona informació sobre com utilitzar un recurs disponible com a dimensió de preu.
author: Rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1e8487d3d32acab294bb2de16fb0278f357f774e62b553eb0c1ebd5b6246e332
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6996244"
---
# <a name="use-a-bookable-resource-as-a-pricing-dimension"></a>Utilització d'un recurs que es pot reservar com a dimensió de preus

 _**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_ 

En aquest tema es proporciona informació sobre com utilitzar un recurs disponible com a dimensió de preu. Si la vostra estratègia de preus està configurada de manera que cada recurs disponible ha de tenir un preu o un percentatge de cost determinat, utilitzeu un recurs que es pot reservar com a dimensió de preus.

## <a name="prerequisites"></a>Requisits previs
Abans de completar els procediments d'aquest tema, heu de tenir una solució de dimensió de preus nova per a la vostra organització. Si encara no l'heu creat, vegeu [Crear camps i entitats personalitzats](../pricing-costing/create-custom-fields-entities-pricing-dimensions.md).

## <a name="add-the-bookable-resource-field-to-forms-and-views"></a>Afegir el camp Recurs que es pot reservar als formularis i a les visualitzacions
Per fer que el camp **Recurs que es pot reservar** sigui visible a la solució de la dimensió de preus, heu d'afegir el camp a tots els formularis i les visualitzacions com a entitat.

A la taula següent s'enumeren tots els formularis i visualitzacions subministrats de sèrie, per entitat. També heu d'afegir el camp nou als formularis o visualitzacions addicionals de les entitats personalitzades.

|   Entity        | Formularis   |Visualitzacions        |
| ------------------------------|---------------------------------|----------------------------------|
|  Preu per funció| Informació | - Preus de categories de recursos actius<br> - Associat a preus de categories de recursos |
|  Marge comercial de preu de funció| Informació| - Marge comercial de preu de funcions actives<br>- Associat al marge comercial de preus de la funció |
|  Detall de la línia d’oferta| - Informació del projecte<br>- Creació ràpida de projectes| - Detall de la línia d'oferta activa<br>- Detalls de la línia d’oferta combinada<br>- Associat al detall de la línia d'oferta |
|  Detall de la línia de contracte del projecte| - Informació del projecte<br>- Creació ràpida de projectes| - Detalls de la línia de contracte combinada<br>- Detalls de la línia de contracte activa<br>- Associat als detalls de la línia de contracte |
|  Tasca del projecte| - Informació<br>- Formulari nou| &nbsp; |
|  Membre de l'equip del projecte| - Informació<br>- Formulari nou| - Membres de l’equip del projecte actius<br>- Membres de l'equip del projecte<br>- Associada als membres de l’equip del projecte |
|  Entrada de temps| - Informació<br>- Crear entrada de temps| - Les meves entrades de temps per data<br>- Les meves entrades de temps per a aquesta setmana<br>- Entrades de temps per a aprovació|
|  Línia del llibre diari| - Informació<br>- Creació ràpida| - Línies del llibre diari actives<br>- Associat a les línies del llibre diari |
|  Detall de la línia de factura| - Informació<br>- Creació ràpida| - Detalls de la línia de factura activa<br>- Transaccions de factura no imputables<br>- Transaccions de factura gratuïtes<br>- Associat al detall de la línia de factura <br>- Transaccions de factura no imputables|
|  Real| - Informació<br>- Valors reals actius| Associada a valors reals |

## <a name="set-up-a-bookable-resource-as-a-pricing-dimension"></a>Configurar un recurs que es pot reservar com a dimensió de preus
Per configurar un recurs que es pot reservar com a dimensió de preus, seguiu aquests passos:

1. Aneu a **Configuració** > **Paràmetres**. 
2. A la pàgina **Paràmetre**, a la pestanya **Dimensions de preus basades en l'import**, verifiqueu que a la quadrícula es mostrin els registres de l'entitat **Dimensions de preus**. 
2. Afegiu **Recurs que es pot reservar** a aquesta llista de dimensions de preus com a **msdyn_bookableresource**. 
3. A **Aplicable al cost** i **Aplicable a les vendes**, seleccioneu un valor.
4. A **Tipus de dimensió**, seleccioneu **Basada en la quantitat**. 
5. Seleccioneu la prioritat de costos i vendes per al recurs disponible. Normalment, un recurs que es pot reservar té la prioritat més alta quan s'inclou com una dimensió de preu. Definiu la prioritat en **1** (o **0**, depenent de la manera com compteu la prioritat) per garantir aquest comportament.

## <a name="set-up-pricing-dimension-field-names"></a>Configurar noms de camps de dimensions de preus

Quan el nom del camp d'una dimensió de preus a la taula **Preu de funció** és diferent del nom del camp a qualsevol de les altres entitats en què s'utilitza el preu per defecte, s'ha d'informar el registre de la dimensió de preus sobre els noms diferents.  

Per a un recurs que es pot reservar, l'entitat **Membres de l'equip del projecte** té un nom de camp lleugerament diferent de com s'anomena a l'entitat **Preu de la funció**: 

 - Entitat **Membres de l'equip de projecte** = **msdyn_bookableresourceid**
 - Entitat **Preu de la funció** = **msdyn_bookableresource**

El registre de la dimensió de preus de **msydn_bookableresource** ha de ser informat sobre aquesta diferència.

1. Feu doble clic a la fila de la quadrícula **Dimensions de preus** per obrir la pàgina de dimensió de **msdyn_bookableresource**.
2. A la pàgina dimensió, a la pestanya **Relacionat**, seleccioneu **Noms de camp de dimensions de preus**.

  ![Pestanya Noms de camps de dimensions de preu.](media/PD-fieldname.png)

3. A la visualització associada que s'obre, seleccioneu **Afegeix un nou nom del camp de la dimensió de preus**.

  ![Afegeix nous noms de camps de dimensions de preus.](media/Add-NewPD-fieldname.png)

  S'obre la pàgina **Nou nom de camp de dimensions de preus** per a **msdyn_bookableresource**. 

4. A la pàgina **Nom del camp nou de dimensió de preus**, afegiu **msdyn_projectteam** a **Nom lògic de l'entitat**.
5. Afegiu **msdyn_bookableresourceid** al **Nom del camp**.

 ![Formulari Afegeix nous noms de camps de dimensions de preus.](media/PD-fieldname-Added.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]