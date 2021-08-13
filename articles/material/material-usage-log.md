---
title: Registre de l'ús de materials en projectes i tasques de projectes
description: Aquest tema proporciona informació sobre com registrar l'ús de materials als projectes i a les tasques de projectes.
author: rumant
ms.date: 03/31/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4d8757049953fab0ad8bf6ee1a1d695fcb6df75b1be52641ad4af3b3137d7a0a
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6999259"
---
# <a name="record-material-usage-on-projects-and-project-tasks"></a>Registre de l'ús de materials en projectes i tasques de projectes

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

A mesura que un equip de projecte treballa en les tasques d'un projecte, consumeix o utilitza materials. Un registre d'ús de materials proporciona una manera de registrar aquest ús per tal que l'administrador del projecte pugui aprovar-lo i, finalment, facturar-lo al client. 

Per registrar l'ús de materials del catàleg o fora del catàleg i enviar-los a l'aprovador, seguiu aquests passos: 

1. A la subfinestra de navegació, seleccioneu **Ús de materials** i, a continuació, seleccioneu **Crea**.
2. A la pàgina **Ús de materials nou**, introduïu la informació d'ús de materials necessària i, a continuació, seleccioneu **Desa**.

La taula següent proporciona informació sobre els camps de la pàgina **Registre d'ús de materials**. 

| **Camp** | **Descripció** | **Impacte descendent** |
| --- | --- | --- |
| Descripció | Descripció de l'ús específic de materials. | No hi ha cap impacte descendent d'aquest camp. |
| Date | La data en què està previst que s'utilitzi el material. | No hi ha cap impacte descendent d'aquest camp. |
| Project | Llista dels projectes que estan actius. | La selecció d'un projecte per a un registre d'ús de materials afecta el camp **Tasca** per mostrar només les tasques que es troben al projecte. |
| Tasca | Llista de tasques per al projecte que inclou tasques de resum i de nodes fulla. | La selecció d'una tasca per a un registre d'ús de materials afecta el cost del material real i les vendes de materials reals per a una tasca. Si aquest camp està buit, es fa el seguiment del cost d'ús del material i de les vendes i es resumeixen només en el nivell del projecte. |
| Seleccioneu el producte | Especifiqueu si aquest ús de materials és per a un producte **Existent** (catàleg) o un producte **Fora de catàleg**. | Aquest camp determina el tipus de producte. |
| Producte | Identificador del producte del catàleg de productes. Quan seleccioneu un identificador de producte, el camp **Seleccioneu el producte** s'actualitza automàticament a **Producte existent**. L'ID s'utilitza per recuperar els preus de cost i de vendes de la llista de preus. | No hi ha cap impacte descendent d'aquest camp. |
| Descripció de producte fora de catàleg | Camp de text on cal escriure el nom del producte. Aquest camp està disponible quan seleccioneu un producte **Fora de catàleg** al camp **Seleccioneu el producte**.| No hi ha cap impacte descendent d'aquest camp. |
| Recurs que es pot reservar| Recurs que ha utilitzat aquest material en el projecte. El valor per defecte d'aquest camp és el recurs que es pot reservar de l'usuari que ha iniciat la sessió, però es pot canviar per registrar l'ús en nom d'altres membres de l'equip del projecte. | No hi ha cap impacte descendent d'aquest camp. |
| Grup d'unitats | El valor per defecte d'aquest camp prové del grup d'unitats configurat com a valor per defecte al producte del catàleg. Podeu actualitzar aquest camp per seleccionar un altre grup d'unitats. | No hi ha cap impacte descendent d'aquest camp. |
| Unitat | El valor per defecte d'aquest camp és la unitat per defecte del producte seleccionat. Podeu actualitzar aquest camp per seleccionar una altra unitat. | Canviar la unitat fa que canviï el preu unitari i el cost per defecte. |
| Quantitat | Quantitat del producte que s'ha utilitzat en el projecte o la tasca de projecte. | No hi ha cap impacte descendent d'aquest camp. |
| Cost de la unitat | Cost unitari de la combinació de producte i unitat seleccionada com a configurada a la llista de preus de cost aplicable. | El cost unitari sempre es mostra en la moneda de cost del projecte. Si no hi ha cap cost unitari per a la combinació de producte i unitat a la llista de preus, el cost per unitat per defecte és 0,00. |
| Cost total | Import del cost que es calcula com a quantitat \* cost unitari.| L'import del cost sempre es mostra en la moneda de cost del projecte. |


## <a name="submit-material-usage-for-review-and-approval"></a>Enviament de l'ús de materials per a la revisió i aprovació 
Un cop hagueu registrat tot l'ús de materials i estigueu a punt per aprovar-lo, heu d'enviar la informació d'ús per a la revisió.

1. Aneu a **Registre d'ús de materials** i seleccioneu una o diverses entrades. O bé seleccioneu tots els registres d'ús de materials mitjançant la casella de selecció de la capçalera.
2. Seleccioneu **Envia**. El sistema processa les entrades seleccionades i crea sol·licituds d'aprovació d'ús de materials.

## <a name="recall-a-material-usage-log"></a>Recuperació d'un registre d'ús de materials

Quan calgui, podeu recuperar un ús de materials enviat. El temps necessari per recuperar una entrada d'ús de materials depèn de la fase d'aprovació.  Si l'aprovador encara no ha aprovat l'entrada, pot ser que la recuperació es produeixi immediatament. No obstant, si l'entrada ja ha estat aprovada, es demana a l'aprovador que aprovi la recuperació i reverteixi les transaccions.

1. Aneu a **Ús de materials** i, a la llista de registres d'ús de materials, seleccioneu l'ús de materials per recuperar-lo.
2. Seleccioneu **Recupera**. Si l'entrada d'ús de materials encara no s'ha aprovat, el sistema la recupera immediatament. Si l'entrada de materials ja s'ha aprovat, es crea una sol·licitud de recuperació per notificar a l'aprovador que voleu recuperar l'ús de materials. A continuació, l'aprovador confirmarà que la reversió es pot fer i es recuperarà l'entrada.

## <a name="delete-a-material-usage-log"></a>Supressió d'un registre d'ús de materials

Podeu suprimir registres d'ús de materials que no s'han enviat. Per suprimir un registre d'ús de materials que ja s'ha enviat, primer l'heu de recuperar.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
