---
title: Crear camps i entitats personalitzats
description: En aquest tema s'explica com crear conjunts d'opcions i entitats a la vostra pròpia solució a la plataforma Power Apps.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/26/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: fb160bfd-e037-4a21-a968-3ff2e6e16481
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 7ee30e3bb6b8034ef226e2e9181195685355011f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749560"
---
# <a name="create-custom-fields-and-entities"></a>Crear camps i entitats personalitzats 

Completeu els passos següents en qualsevol moment que vulgueu crear un conjunt d'opcions o una entitat personalitzada a la plataforma del Power Apps.  
Els procediments d'aquest tema s'han d'emplenar mitjançant la interfície web del Project Service Automation (PSA).

> [!IMPORTANT]
> Us recomanem que realitzeu tots els canvis de dimensió de preus personalitzats en una solució separada. Aquestes pràctiques recomanades importants proporcionen una flexibilitat futura per actualitzar o suprimir els canvis segons calgui, us ajudaran a reutilitzar el vostre treball i facilita la portabilitat d'aquests canvis en una altra instància. Després d'haver fet tots els canvis necessaris, exporteu aquesta solució com a **Solució administrada** i importeu-la a altres instàncies per tornar a utilitzar la configuració dels preus.


## <a name="create-a-custom-solution-for-pricing-dimensions"></a>Crear una solució personalitzada per a les dimensions de preus
1. Al PSA, feu clic a **Configuració** > **Solucions** i, a continuació, feu clic a **Crea** per crear una solució nova. 
2. Anomeneu la solució **Dimensions de preus de \<nom de l'organització>**, introduïu la informació necessària restant i, a continuació, feu clic a **Desa**.

> ![Crear una solució personalitzada per a les dimensions de preus](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Crear camps personalitzats i conjunts d'opcions a la solució de preus de la dimensió

Una dimensió de preus pot ser una conjunt d'opcions o una entitat. Tots dos s'han de crear a la solució de preus. Els passos d'aquest procediment expliquen com crear dimensions basades en una entitat i dimensions basades en un conjunt d'opcions.

### <a name="entity-based-dimensions"></a>Dimensions basades en una entitat

1. Al PSA, feu clic a **Configuració** > **Solucions** i, a continuació, feu doble clic a **Dimensions de preus de \<nom de l'organització>**.
2. A l'Explorador de solucions, a la subfinestra de navegació esquerra, seleccioneu **Entitats**.
3. Feu clic a **Nou** per crear una entitat nova anomenada **Càrrec estàndard**. Introduïu la informació requerida restant i feu clic a **Desa**.

> ![Definició de l'entitat de càrrec estàndard](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a>Dimensions basades en un conjunt d'opcions 
Podeu crear dues dimensions basades en un conjunt d'opcions. Utilitzeu **Ubicació de treball del recurs** per fer el seguiment del treball de la ubicació **Casa** i **In situ** i utilitzeu **Hores de treball del recurs** amb els valors **Normals** i **Extres** per aplicar un marge comercial quan s'hagi completat la feina.


1. Al PSA, feu clic a **Configuració** > **Solucions** i, a continuació, feu doble clic a **Dimensions de preus de \<nom de l'organització>**. 
2. A l'Explorador de solucions, a la subfinestra de navegació esquerra, seleccioneu **Conjunts d'opcions**. 
3. Feu clic a **Nou** per crear un conjunt d'opcions nou, introduïu la informació necessària restant i, a continuació, feu clic a **Desa**.

> ![Dimensió de preus basada en conjunt d'opcions anomenada Ubicació de treball del recurs ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![Dimensió de preus basada en conjunt d'opcions anomenada Hores de treball del recurs ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a>Crear dades per a les dimensions basades en l'entitat

Podeu crear dades per a les dimensions basades en l'entitat manualment o mitjançant una importació del Microsoft Excel o trucades de servei. Utilitzeu els passos d'aquest procediment per crear dos càrrecs estàndard, **Enginyer de sistemes** i **Enginyer de sistemes sènior** per la dimensió basada en l'entitat **Càrrec estàndard**. Si les dades que voleu crear són petites, com a l'exemple següent, podeu utilitzar un formulari estàndard.

1. Al PSA, feu clic a **Cerca avançada**. Seleccioneu l'entitat **Càrrec estàndard** i, a continuació, feu clic a **Resultats**. Es mostraran totes les files de l'entitat **Càrrec estàndard**.
2. Feu clic a **Nou**. Al camp **Nom**, introduïu "Enginyer de sistemes" i, a continuació, feu clic a **Desa**.
3. Tanqueu el formulari. 
4. Repetiu els passos 1-3 per crear un altre càrrec estàndard per a "Enginyer de sistemes sènior".

> ![Dades d'exemple per a l'entitat Càrrec estàndard ](media/ST-data.png)

## <a name="add-all-required-psa-entities-and-related-components-to-the-pricing-dimension-solution"></a>Afegiu totes les entitats del PSA necessàries i els components relacionats a la solució de la dimensió de preus
Haureu d'afegir les següents entitats del Project Service a la solució de preus. Utilitzeu els passos d'aquest procediment per fer canvis importants d'esquema a la solució de preus de manera que les entitats coneguin les noves dimensions de preus.

1. Al PSA, feu clic a **Configuració** > **Solucions** i, a continuació, feu doble clic a **Dimensions de preus de \<nom de l'organització>**. 
2. A l'Explorador de solucions, a la subfinestra de navegació esquerra, seleccioneu **Afegeix existent** > **Entitats**.
3. Al quadre de diàleg **Components de la solució**, seleccioneu una de les entitats següents:

- Real
- Recurs que es pot reservar
- Línia d'estimació
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

4. Quan se us demani que inclogueu entitats dependents de les entitats seleccionades anteriorment ,feu clic a **No**.

> ![No incloguis tots els components relacionats](media/Do-not-include-required.png)


