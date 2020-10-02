---
title: Creació de camps i entitats personalitzats com a dimensions de preus
description: En aquest tema es proporciona informació sobre com crear conjunts d'opcions o entitats personalitzades.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: 2000f7e710267560fe2bd52b0e33024617d108ea
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898249"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a>Creació de camps i entitats personalitzats com a dimensions de preus

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

Completeu els passos següents en qualsevol moment que vulgueu crear un conjunt d'opcions o una entitat personalitzada.

> [!IMPORTANT]
> Us recomanem que realitzeu tots els canvis de dimensió de preus personalitzats en una solució separada. Aquestes pràctiques recomanades importants proporcionen una flexibilitat futura per actualitzar o suprimir els canvis segons calgui, us ajudaran a reutilitzar el vostre treball i facilita la portabilitat d'aquests canvis en una altra instància. Després d'haver fet tots els canvis necessaris, exporteu aquesta solució com a **Solució administrada** i importeu-la a altres instàncies per tornar a utilitzar la configuració dels preus.


## <a name="create-a-custom-solution-for-pricing-dimensions"></a>Crear una solució personalitzada per a les dimensions de preus
1. Aneu a **Configuració** > **Solucions** i, a continuació, seleccioneu **Crea** per crear una solució nova. 
2. Anomeneu la solució **Dimensions de preus de \<your organization name>**, introduïu la informació necessària restant i, a continuació, seleccioneu **Desa**.
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Crear camps personalitzats i conjunts d'opcions a la solució de preus de la dimensió

Una dimensió de preus pot ser una conjunt d'opcions o una entitat. Tots dos s'han de crear a la solució de preus. Els passos d'aquest procediment expliquen com crear dimensions basades en una entitat i dimensions basades en un conjunt d'opcions.

### <a name="entity-based-dimensions"></a>Dimensions basades en una entitat

1. Aneu a **Configuració** > **Solucions** i feu doble clic a **Dimensions de preus de \<your organization name>**.
2. A l'Explorador de solucions, a la subfinestra de navegació esquerra, seleccioneu **Entitats**.
3. Seleccioneu **Nou** per crear una entitat nova anomenada **Càrrec estàndard**. 
4. Introduïu la informació requerida restant i seleccioneu **Desa**.


### <a name="option-set-based-dimensions"></a>Dimensions basades en un conjunt d'opcions 
Podeu crear dues dimensions basades en un conjunt d'opcions. Utilitzeu **Ubicació de treball del recurs** per fer el seguiment del treball de la ubicació **Casa** i **In situ** i utilitzeu **Hores de treball del recurs** amb els valors **Normals** i **Extres** per aplicar un marge comercial quan s'hagi completat la feina.


1. Aneu a **Configuració** > **Solucions** i feu doble clic a **Dimensions de preus de \<your organization name>**. 
2. A l'Explorador de solucions, a la subfinestra de navegació esquerra, seleccioneu **Conjunts d'opcions**. 
3. Seleccioneu **Nou** per crear un conjunt d'opcions nou, introduïu la informació necessària restant i, a continuació, seleccioneu **Desa**.

## <a name="create-data-for-entity-based-dimensions"></a>Crear dades per a les dimensions basades en l'entitat

Podeu crear dades per a les dimensions basades en l'entitat manualment o mitjançant una importació del Microsoft Excel o trucades de servei. Utilitzeu els passos d'aquest procediment per crear dos càrrecs estàndard, **Enginyer de sistemes** i **Enginyer de sistemes sènior** per la dimensió basada en l'entitat **Càrrec estàndard**. Si les dades que voleu crear són petites, com a l'exemple següent, podeu utilitzar un formulari estàndard.

1. Seleccioneu **Cerca avançada**, seleccioneu l'entitat **Càrrec estàndard** i, a continuació, seleccioneu **Resultats**. Es mostraran totes les files de l'entitat **Càrrec estàndard**.
2. Seleccioneu **Nou** i al camp **Nom**, introduïu "Enginyer de sistemes" i, a continuació, seleccioneu **Desa**.
3. Tanca el formulari. 
4. Repetiu els passos 1-3 per crear un altre càrrec estàndard per a "Enginyer de sistemes sènior".

## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>Afegiu totes les entitats necessàries i els components relacionats a la solució de la dimensió de preus
Haureu d'afegir les següents entitats a la solució de preus. Utilitzeu els passos d'aquest procediment per fer canvis importants d'esquema a la solució de preus de manera que les entitats coneguin les noves dimensions de preus.

1. Seleccioneu **Configuració** > **Solucions** i feu doble clic a **Dimensions de preus de \<your organization name>**. 
2. A l'Explorador de solucions, a la subfinestra de navegació esquerra, seleccioneu **Afegeix existent** > **Entitats**.
3. Al quadre de diàleg **Components de la solució**, seleccioneu una de les entitats següents:

  - Real
  - Recurs que es pot reservar
  - Línia d'estimació
  - Detall de la línia de factura
  - Línia del llibre diari
  - Detall de la línia de contracte del projecte
  - Membre de l'equip del projecte
  - Detall de la línia d’oferta
  - Marge comercial de preu de funció
  - Preu per funció 
  - Entrada de temps 


> [!NOTE]
> Assegureu-vos d'incloure tots els formularis i les visualitzacions de cadascuna de les entitats seleccionades.

4. Quan se us demani que inclogueu entitats dependents de les entitats seleccionades anteriorment, seleccioneu **No**.

