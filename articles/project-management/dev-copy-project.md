---
title: Desenvolupament de plantilles de projecte amb la característica Copia el projecte
description: En aquest tema es proporciona informació sobre com crear plantilles de projecte mitjançant l'acció personalitzada Copia el projecte.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 22976730ef3c8c22ea028b27a6eb5f14fb88993e
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642396"
---
# <a name="develop-project-templates-with-copy-project"></a>Desenvolupament de plantilles de projecte amb la característica Copia el projecte

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dynamics 365 Project Operations és compatible amb la capacitat de copiar un projecte i revertir les assignacions als recursos genèrics que representen la funció. Els clients poden utilitzar aquesta funcionalitat per crear plantilles de projecte bàsiques.

Quan seleccioneu **Copia el projecte**, l'estat del projecte de destinació s'actualitza. Utilitzeu **Raó per a l'estat** per determinar quan ha finalitzat l'acció de còpia. En seleccionar **Copia el projecte** també s'actualitza la data d'inici del projecte a la data d'inici actual si no es detecta cap data de la destinació a l'entitat del projecte de destinació.

## <a name="copy-project-custom-action"></a>Acció personalitzada Copia el projecte 

### <a name="name"></a>Nom 

**msdyn_CopyProjectV2**

### <a name="input-parameters"></a>Paràmetres d’entrada
Hi ha tres paràmetres d'entrada:

| Paràmetre          | Type   | Valors                                                   | 
|--------------------|--------|----------------------------------------------------------|
| ProjectCopyOption  | String | **{"removeNamedResources":true}** o **{"clearTeamsAndAssignments":true}** |
| SourceProject      | Referència d’entitat | Projecte d'origen |
| Objectiu             | Referència d’entitat | Projecte de destinació |


- **{"clearTeamsAndAssignments":true}** : comportament per defecte d'un projecte per al web, i suprimirà totes les assignacions i membres de l'equip.
- **{"removeNamedResources":true}** comportament per defecte del Project Operations, i revertirà les assignacions a recursos genèrics.

Per veure més valors per defecte en accions, vegeu [Utilitzar les accions de l'API web](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)

## <a name="specify-fields-to-copy"></a>Especificar els camps que es copiaran 
Quan es crida l'acció, **Copia el projecte** consultarà la visualització del projecte **Copia les columnes del projecte** per determinar quins camps s'han de copiar quan es copia el projecte.
