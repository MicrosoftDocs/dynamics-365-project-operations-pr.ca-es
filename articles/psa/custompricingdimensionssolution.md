---
title: Crear solucions personalitzades per a les dimensions de preus
description: Aquest tema explica com crear una solució personalitzada en crear dimensions de preus personalitzades.
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
ms.openlocfilehash: 3e437fce5b9f1fb330a713788e24100a4fe02948
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072221"
---
# <a name="create-custom-solutions-for-pricing-dimensions"></a>Crear solucions personalitzades per a les dimensions de preus

> [!IMPORTANT]
> Tots els canvis de dimensions de preus personalitzades han d'estar en una solució separada. Aquestes pràctiques recomanades importants proporcionen una flexibilitat futura per actualitzar o suprimir els canvis segons calgui, us ajudaran a reutilitzar el vostre treball i facilita la portabilitat d'aquests canvis en una altra instància. Després de fer els canvis necessaris, exporteu aquesta solució com a **Solució administrada** i importeu-la a altres instàncies per tornar a utilitzar la configuració dels preus.

1. Seleccioneu **Configuració** > **Solucions** i, a continuació, **Nova**. 
2. Anomeneu la solució **Dimensions de preus de \<your organization name>** , introduïu la informació necessària restant i, a continuació, seleccioneu **Desa**.

> ![Crear una solució personalitzada per a les dimensions de preus](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>Afegir totes les entitats necessàries i els components relacionats a la solució de la dimensió de preus
Haureu d'afegir les següents entitats del Project Service a la solució de preus. Completeu els passos d'aquest procediment per fer canvis importants d'esquema a la solució de preus de manera que les entitats coneguin les noves dimensions de preus.

1. Seleccioneu **Configuració** > **Solucions** i feu doble clic a **Dimensions de preus de \<your organization name>**. 
2. A l'Explorador de solucions, a la subfinestra de navegació esquerra, seleccioneu **Afegeix existent** > **Entitats**.
3. Al quadre de diàleg **Components de la solució** , seleccioneu una de les entitats següents:

- Real
- Recurs que es pot reservar
- Línia d'estimació
- Tasca del projecte
- Detall de la línia de factura
- Línia del llibre diari
- Detall de la línia de contracte del projecte
- Membre de l'equip del projecte
- Detall de la línia d'oferta
- Marge comercial de preu de funció
- Preu per funció 
- Entrada de temps 

> ![Afegir entitats existents a la solució de dimensions de preus](media/Existing-entities-to-PD-solution.png)

> ![Selecció de components de la solució](media/Dimension-Components.png)

> [!NOTE]
> Assegureu-vos d'incloure tots els formularis i les visualitzacions de cadascuna de les entitats seleccionades.

4. Quan se us demani que inclogueu entitats dependents de les entitats seleccionades, seleccioneu **No**.

> ![No incloguis tots els components relacionats](media/Do-not-include-required.png)

