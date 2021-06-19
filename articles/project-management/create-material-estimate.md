---
title: Estimacions financeres per a materials en projectes
description: Aquest tema proporciona informació sobre la definició o l'estimació de materials basats en projectes.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 768da6adb83b4593a227f60182179b3036f4c040
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6002674"
---
# <a name="financial-estimates-for-materials-on-projects"></a>Estimacions financeres per a materials en projectes

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

El Dynamics 365 Project Operations permet als administradors de projectes definir els costos de materials basats en projectes per a cada projecte o tasca. Cada estimació de materials es pot associar a una tasca de projecte específica. Les despeses es classifiquen en diferents categories de despeses, que es defineixen en el nivell organitzatiu. El càlcul de preus i costos de cada categoria de despesa es defineix a la llista de preus. 

Completeu els passos següents per visualitzar, afegir o suprimir una estimació de materials de projecte.

1. Aneu a **Projectes** i seleccioneu el projecte que voleu actualitzar.
2. A la pestanya **Estimacions de materials**, vegeu la llista d'estimacions de materials del projecte.
3. Seleccioneu **Nova estimació de materials** per crear una nova estimació de materials. O bé seleccioneu una estimació de materials que vulgueu suprimir i, a continuació, seleccioneu **Suprimeix l'estimació de materials**.

La taula següent proporciona informació sobre els camps de la pàgina **Línia d'estimació de materials** d'un projecte. 

| **Camp** | **Descripció** | **Impacte descendent** |
| --- | --- | --- |
| Tasca | Llista de les tasques del projecte. Això inclou les tasques de resum i de nodes fulla. | Quan seleccioneu una tasca per a una línia d'estimació de materials, el cost de materials previst i les vendes de materials previstes per a una tasca es veuen afectades. Si aquest camp està buit, es fa el seguiment de l'estimació de materials i es resumeix només en el nivell del projecte. |
| Seleccioneu el producte |  Podeu especificar si la línia de previsió és per a un producte existent (catàleg) o fora de catàleg. | Aquest camp determina si seleccioneu un producte del catàleg o un producte fora de catàleg. |
| Producte | L'identificador del producte del catàleg de productes. Quan seleccioneu un identificador de producte, el valor del camp **Seleccioneu el producte** s'actualitza automàticament a **Producte existent**. L'ID s'utilitza per recuperar els preus de cost i de vendes de la llista de preus. | No hi ha cap impacte descendent d'aquest camp. |
| Descripció de producte fora de catàleg | Camp de text on cal escriure el nom del producte. Aquest camp s'ha d'utilitzar quan se selecciona **Fora de catàleg** al camp **Seleccioneu el producte**.| No hi ha cap impacte descendent d'aquest camp. |
| Data d’inici | La data en què està previst que s'utilitzi el material. | No hi ha cap impacte descendent d'aquest camp. |
| Grup d'unitats | El valor per defecte d'aquest camp prové del grup d'unitats per defecte al producte del catàleg. Podeu actualitzar aquest camp per seleccionar un altre grup d'unitats. | No hi ha cap impacte descendent d'aquest camp. |
| Unitat | El valor d'aquest camp ve de la unitat per defecte del producte seleccionat. Podeu actualitzar aquest camp per seleccionar una altra unitat. | Canviar la unitat fa que canviï el preu unitari i el cost per defecte. |
| Quantitat | Quantitat prevista del producte que s'utilitzarà en el projecte. | No hi ha cap impacte descendent d'aquest camp. |
| Cost de la unitat | Cost unitari de la combinació de producte i unitat seleccionada com a configurada a la llista de preus de cost aplicable. | El cost unitari sempre es mostra en la moneda de cost del projecte. Si no hi ha cap cost unitari configurat per a la combinació de producte i unitat a la llista de preus, el cost per unitat per defecte és 0,00. |
| Preu per unitat | Preu de la combinació de producte i unitat seleccionada com a configurada a la llista de preus de venda aplicable. | El preu unitari sempre es mostra en la moneda de vendes del projecte. Si no hi ha cap preu unitari configurat per a la combinació de producte i unitat a la llista de preus, el preu unitari per defecte és 0,00.|
| Cost total | Import del cost que es calcula com a quantitat \* cost unitari.| L'import del cost sempre es mostra en la moneda de cost del projecte. |
| Total vendes | Import de vendes que es calcula com a quantitat \* preu unitari. | L'import de vendes sempre es mostra en la moneda de vendes del projecte. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
