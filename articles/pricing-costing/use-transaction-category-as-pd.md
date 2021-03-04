---
title: Utilització d'una categoria de transacció com a dimensió de preus
description: En aquest tema es proporciona informació sobre l'ús del camp Categoria de transacció com a dimensió de preu.
author: rumant
manager: tfehr
ms.date: 11/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: bace11455d34fdda95e08be1a7cc37850a0cf589
ms.sourcegitcommit: 869bde007805ef255f61b03937e4a44aeef61df9
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 11/12/2020
ms.locfileid: "4513962"
---
# <a name="use-transaction-category-as-a-pricing-dimension"></a>Utilització d'una categoria de transacció com a dimensió de preus


_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_


En aquest tema s'explica com utilitzar el camp **Categoria de transacció** com a dimensió de preu. 

## <a name="prerequisites"></a>Requisits previs
Abans de completar els procediments d'aquest tema, heu de tenir una solució de dimensió de preus nova per a la vostra organització. Si encara no l'heu creat, vegeu [Crear camps i entitats personalitzats com a dimensions de preus](create-custom-fields-entities-pricing-dimensions.md).

## <a name="add-the-transaction-category-field-to-forms-and-views"></a>Afegir el camp Categoria de transacció a formularis i visualitzacions
Per fer que el camp **Categoria de transacció** sigui visible a la solució de la dimensió de preus, heu d'afegir el camp a tots els formularis i les visualitzacions com a entitat.

A la taula següent s'enumeren tots els formularis i visualitzacions subministrats de sèrie, per entitat. També heu d'afegir el camp nou als formularis o visualitzacions addicionals de les entitats personalitzades.

|  Entity        | Formularis     |Visualitzacions        |
| ------------------------------|---------------------------------|----------------------------------|
|  Preu per funció| Informació |- Preus de categories de recursos actius<br> - Associat a preus de categories de recursos |
|  Marge comercial de preu de funció| Informació|- Marge comercial de preu de funcions actives<br>- Associat al marge comercial de preus de la funció |
|  Detall de la línia d’oferta|- Informació del projecte<br>- Creació ràpida de projectes| - Detall de la línia d'oferta activa<br>- Detalls de la línia d’oferta combinada<br>- Associat al detall de la línia d'oferta |
|  Detall de la línia de contracte del projecte|- Informació del projecte<br>- Creació ràpida de projectes|- Detalls de la línia de contracte combinada<br>- Detalls de la línia de contracte activa<br>- Associat als detalls de la línia de contracte |
|  Tasca del projecte|- Informació<br>- Formulari nou| &nbsp; |
|  Membre de l'equip del projecte|- Informació<br>- Formulari nou|- Membres de l’equip del projecte actius<br>- Membres de l'equip del projecte<br>- Associat als membres de l’equip del projecte |
|  Entrada de temps|- Informació<br>- Crear entrada de temps|- Les meves entrades de temps per data<br>- Les meves entrades de temps per a aquesta setmana<br>- Entrades de temps per a aprovació|
|  Línia del llibre diari|- Informació<br>- Creació ràpida|- Línies del llibre diari actives<br>- Associat a les línies del llibre diari|
|  Detall de la línia de factura|- Informació<br>- Creació ràpida|- Detalls de la línia de factura activa<br>- Transaccions de factura no imputables<br>- Transaccions de factura gratuïtes<br>- Associat al detall de la línia de factura <br>- Transaccions de factura no imputables|
|  Real|- Informació<br>- Valors reals actius| Associada a valors reals |

## <a name="set-up-the-transaction-category-field-as-a-pricing-dimension"></a>Configurar el camp Categoria de transacció com a dimensió de preus

1. Aneu a **Configuració** > **Paràmetres**. 
2. A la pàgina **Paràmetres**, a la pestanya **Dimensions de preus basades en l'import**, verifiqueu que a la quadrícula es mostrin els registres de l'entitat **Dimensions de preus**.
3. Afegiu **Categoria de la transacció** a aquesta llista i definiu els camps **Aplicable al cost** i **Aplicable a la venda** com a **Sí**.
4. Al camp **Tipus de dimensió**, seleccioneu **Basada en la quantitat** i, a continuació, seleccioneu la prioritat per a la **Categoria de transacció** relacionada amb el cost i les vendes.


[!INCLUDE[footer-include](../includes/footer-banner.md)]