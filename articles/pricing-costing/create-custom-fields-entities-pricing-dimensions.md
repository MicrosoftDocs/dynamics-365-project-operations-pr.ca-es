---
title: Creació de camps i entitats personalitzats com a dimensions de preus
description: En aquest tema es proporciona informació sobre com crear conjunts d'opcions o entitats personalitzades.
author: rumant
manager: AnnBe
ms.date: 11/18/2020
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
ms.openlocfilehash: fc5917856b8f28d36dc55593a68eba7823a00b36
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642801"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a>Creació de camps i entitats personalitzats com a dimensions de preus

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

Completeu els passos següents quan vulgueu crear un conjunt d'opcions o una entitat personalitzats per utilitzar-los com a dimensió de preus. Per obtenir més informació, vegeu [Informació general sobre les dimensions de preus](pricing-dimensions-overview.md).  

> [!IMPORTANT]
> Us recomanem que realitzeu tots els canvis de dimensió de preus personalitzats en una solució separada. Aquesta pràctica important proporciona flexibilitat en el futur per actualitzar o suprimir els canvis segons calgui. D'aquesta manera, també us ajudarà a reutilitzar la feina feta i facilitarà el trasllat d'aquests canvis a una altra instància Quan hagueu fet tots els canvis necessaris, exporteu aquesta solució com a **Solució administrada** i importeu-la en altres instàncies per reutilitzar la configuració de preus.

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Crear camps personalitzats i conjunts d'opcions a la solució de preus de la dimensió

Una dimensió de preus pot ser una conjunt d'opcions o una entitat. Tots dos s'han de crear a la solució de preus. Els passos d'aquest procediment expliquen com crear dimensions basades en una entitat i dimensions basades en un conjunt d'opcions.

### <a name="entity-based-dimensions"></a>Dimensions basades en una entitat
Per crear dimensions basades en entitat, seguiu aquests passos:

1. Aneu a **Configuració** > **Solucions** i feu doble clic a **Dimensions de preus de \<your organization name>**.
2. A l'Explorador de solucions, a la subfinestra de navegació esquerra, seleccioneu **Entitats**.
3. Seleccioneu **Nou** per crear una entitat nova anomenada **Càrrec estàndard**. 
4. Introduïu la informació requerida restant i seleccioneu **Desa**.

> ![Definició de l'entitat de càrrec estàndard](media/Standard-Title-entity-definition.png)

### <a name="option-set-based-dimensions"></a>Dimensions basades en un conjunt d'opcions 
Podeu crear dues dimensions basades en un conjunt d'opcions. 

- Utilitzeu **Ubicació del treball dels recursos** per fer el seguiment del preu de la feina a la ubicació **Casa** i de la feina **In situ**. 
- Utilitzeu **Hores de feina de recursos** amb valors **Normals** i **Hores extres** per aplicar un marge comercial quan s'hagi completat l'obra.

El gràfic següent proporciona una visualització de la dimensió **Ubicació del treball del recurs**. 

> ![Dimensió de preus basada en conjunt d'opcions anomenada Ubicació de treball del recurs](media/Option-set-PD-called-Resource-Work-Location.png)

El gràfic següent proporciona una visualització de la dimensió **Hores de treball del recurs**. 

> ![Dimensió de preus basada en conjunt d'opcions anomenada Hores de treball del recurs](media/Option-set-PD-called-Resource-Work-Hours.png)

1. Aneu a **Configuració** > **Solucions** i feu doble clic a **Dimensions de preus de \<your organization name>**. 
2. A l'Explorador de solucions, a la subfinestra de navegació esquerra, seleccioneu **Conjunts d'opcions**. 
3. Seleccioneu **Nou** per crear un conjunt d'opcions nou, introduïu la informació necessària restant i, a continuació, seleccioneu **Desa**.

## <a name="create-data-for-entity-based-dimensions"></a>Crear dades per a les dimensions basades en l'entitat

Podeu crear dades per a les dimensions basades en l'entitat manualment o mitjançant una importació del Microsoft Excel o trucades de servei. Utilitzeu els passos d'aquest procediment per crear dos càrrecs estàndard, **Enginyer de sistemes** i **Enginyer de sistemes sènior** per la dimensió basada en l'entitat **Càrrec estàndard**. Si les dades que voleu crear són petites, com a l'exemple següent, podeu utilitzar un formulari estàndard.

1. Seleccioneu **Cerca avançada**.
2. Seleccioneu l'entitat **Càrrec estàndard** i, a continuació, seleccioneu **Resultats**. Es mostraran totes les files de l'entitat **Càrrec estàndard**.
3. Seleccioneu **Nou** i al camp **Nom**, introduïu "Enginyer de sistemes" i, a continuació, seleccioneu **Desa**.
4. Tanqueu la pàgina. 
5. Repetiu els passos 1-3 per crear un altre càrrec estàndard per a "Enginyer de sistemes sènior".

> ![Dades d'exemple per a l'entitat Càrrec estàndard](media/ST-data.png)
