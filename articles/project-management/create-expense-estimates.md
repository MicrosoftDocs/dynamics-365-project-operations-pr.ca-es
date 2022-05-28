---
title: Estimacions financeres per a despeses en projectes
description: En aquest tema s'ofereix informació sobre la definició o estimació de les despeses basades en el projecte.
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c14dc31d666d0e0d026cf9cddfa1e78dee40f717
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8589460"
---
# <a name="financial-estimates-for-expenses-on-projects"></a>Estimacions financeres per a despeses en projectes
_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

El Dynamics 365 Project Operations permet als administradors de projectes definir les despeses basades en projectes per a un projecte o tasca. Cada element de despesa es pot associar a una tasca de projecte específica. Les despeses es classifiquen en diferents categories de despeses, que es defineixen en el nivell organitzatiu. El càlcul de preus i costos de cada categoria de despesa es defineix a la llista de preus. 

Completeu els passos següents per visualitzar, afegir o suprimir una despesa del projecte.

1. Aneu a **Projectes** i seleccioneu el projecte en el qual voleu treballar.
2. Seleccioneu la pestanya **Estimacions del projecte** i visualitzeu la llista de despeses del projecte.
3. Seleccioneu **Despesa nova** per afegir una despesa. O bé, seleccioneu la despesa que voleu suprimir i, a continuació, seleccioneu **Suprimeix la despesa**.

La taula següent proporciona informació sobre els camps de la pàgina **Línia d'estimació de despesa** d'un projecte. 

| **Camp** | **Descripció** | **Impacte descendent** |
| --- | --- | --- |
| Tasca | Llista de les tasques del projecte. Això inclou les tasques de resum i de nodes fulla. | Seleccionar una tasca per a una línia de previsió de despesa afectarà el cost de la despesa prevista i les vendes de despeses previstes per a una tasca. Si aquest camp es deixa buit, es fa el seguiment de l'estimació de despesa i es resumeix només en el nivell del projecte. |
| Categoria | Llista de categories de transaccions que tenen categories de despesa enllaçades a l'aplicació. | La selecció d'una categoria dona lloc al càlcul dels preus i costos a la línia de previsió de despeses. |
| Data d’inici | La data prevista en què es produirà la despesa. | No hi ha cap impacte descendent d'aquest camp. |
| Grup d'unitats | El valor per defecte d'aquest camp prové del grup d'unitats configurat com a valor per defecte a la categoria seleccionada. Podeu actualitzar aquest camp per seleccionar un altre grup d'unitats. | No hi ha cap impacte descendent d'aquest camp. |
| Unitat | El valor per defecte d'aquest camp és la unitat per defecte de la categoria seleccionada. Podeu actualitzar aquest camp per seleccionar una altra unitat. | Canviar la unitat fa que canviï el preu unitari i el cost per defecte. |
| Quantitat | La quantitat de la despesa prevista en què s'incorrerà. | No hi ha cap impacte descendent d'aquest camp. |
| Cost de la unitat | Cost de la combinació de categoria i unitat seleccionada com a configurada a la llista de preus de cost aplicable | El cost unitari sempre es mostra en la moneda de cost del projecte. |
| Preu per unitat | Preu de la combinació de categoria i unitat seleccionada com a configurada a la llista de preus de venda aplicable. | El preu unitari sempre es mostra en la moneda de vendes del projecte. |
| Cost total | Import del cost que es calcula com a quantitat \* cost unitari.| L'import del cost sempre es mostra en la moneda de cost del projecte. |
| Total vendes | Import de vendes que es calcula com a quantitat \* preu unitari. | L'import de vendes sempre es mostra en la moneda de vendes del projecte. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
