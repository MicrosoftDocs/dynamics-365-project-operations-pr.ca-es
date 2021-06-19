---
title: Creació d'una solució per a les dimensions de preus personalitzades
description: En aquest tema s'ofereix informació sobre com crear solucions per a dimensions de preus personalitzades.
author: Rumant
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 86f4cd2c26ebfca621d1b226b571d220d3b2441e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010324"
---
# <a name="create-a-solution-for-custom-pricing-dimensions"></a>Creació d'una solució per a les dimensions de preus personalitzades

 _**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_ 

>[!IMPORTANT]
>Tots els canvis de dimensions de preus personalitzades han d'estar en una solució separada. Aquestes importants pràctiques recomanades ofereixen la flexibilitat d'actualitzar o suprimir canvis segons calgui, ajuden a reutilitzar la feina i faciliten la portabilitat dels canvis a altres instàncies. Després d'haver fet tots els canvis necessaris, exporteu la solució com a solució **Administrada** i importeu-la a altres instàncies per tornar a utilitzar-la.

## <a name="create-a-solution-for-custom-pricing-dimensions"></a>Creació d'una solució per a les dimensions de preus personalitzades

1.  Seleccioneu **Configuració** > **Solucions** i, a continuació, **Nova**.
2.  Anomeneu la solució, *<your organization name>: dimensions de preus*.
3. Introduïu la informació requerida restant i seleccioneu **Desa**.

  ![Creació d'una solució de dimensió de preus personalitzada](./media/Creation-of-custom-pricing-dimension-solution.png)
 
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>Afegir totes les entitats necessàries i els components relacionats a la solució de la dimensió de preus

Afegiu les entitats del Project Service següents a la solució de preus per fer canvis d'esquema importants a la solució de preus. Un cop completat aquest procediment, les entitats reconeixeran les noves dimensions de preus.

1.  Seleccioneu **Configuració** > **Solucions** i, a continuació, feu doble clic a **Dimensions de preus de <*nom de l'organització*>**.
2.  A l'Explorador de solucions, a la subfinestra de navegació esquerra, seleccioneu **Afegeix existent** > **Entitats**.
3.  Al quadre de diàleg **Components de la solució**, seleccioneu una de les entitats següents:
 
   - **Real**
   - **Recurs que es pot reservar**
   - **Línia d'estimació**
   - **Tasca del projecte**
   - **Detall de la línia de factura**
   - **Línia del llibre diari**
   - **Detall de la línia de contracte del projecte**
   - **Membre de l'equip del projecte**
   - **Detall de la línia d'oferta**
   - **Marge comercial de preu de funció**
   - **Preu per funció**
   - **Entrada de temps**
 
   ![Afegir entitats existents a la solució de dimensió de preus personalitzada](./media/Existing-entities-to-PD-solution.png)
 
 4. Per a cada entitat, reviseu els components que s'afegeixen i la llista final de recursos d'entitat per a cada entitat. 

   >[!NOTE]
   > Incloeu-hi tots els formularis i visualitzacions de cadascuna de les entitats seleccionades.

  ![Entitats afegides](./media/solution-component-selection.png)


5.  Quan se us demani que incloeu entitats dependents per a les entitats seleccionades, seleccioneu **No, no incloguis els components necessaris**.

    ![Incloure entitats dependents](./media/Do-not-include-required.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]