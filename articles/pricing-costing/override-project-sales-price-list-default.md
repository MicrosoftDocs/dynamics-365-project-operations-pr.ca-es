---
title: Substitució de les llistes de preus de vendes de projectes
description: Aquest tema proporciona informació sobre la creació de llistes de preus de vendes personalitzades.
author: rumant
ms.date: 10/22/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b26947822eb8e87b3b36fcde9c99c6ee69375aa942a5641112b9b1109dcaa26c
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "7009564"
---
# <a name="override-project-sales-price-lists"></a>Substitució de les llistes de preus de vendes de projectes

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

## <a name="customer-specific-project-price-lists"></a>Llistes de preus de projecte específiques del client

Es poden configurar acords de preus específics de client com a llistes de preus del projecte en un registre de compte al Dynamics 365 Project Operations.

Per configurar una llista de preus de projecte específica del client, a l'àrea **Vendes**, aneu al registre del compte.

1. Obriu la pàgina de llista **Comptes**.
2. Localitzeu i feu doble clic en un registre de client per obrir la pàgina **Detalls del compte**.
3. A la pestanya **Llistes de preus del projecte**, seleccioneu **+ Nova llista de preus del projecte**.
4. A la pàgina **Nova llista de preus del projecte**, seleccioneu una llista de preus al menú desplegable. Només s'inclouen les llistes de preus que tenen el context definit com a **Vendes** i la moneda de les quals coincideixi amb la moneda del compte.
5. Anomeneu l'associació i seleccioneu **Desa**. Es crea una llista de preus de projecte específica del client. Aquesta llista de preus s'utilitzarà per defecte en els preus del projecte en les ofertes o contractes de projecte creats per a aquest client en què la data de creació de l'oferta o contracte de projecte estigui dins de la data d'efectivitat de la llista de preus.

## <a name="custom-pricing-on-project-quotes"></a>Preus personalitzats en ofertes del projecte

A les ofertes del projecte, podeu tenir preus de projecte que comencin amb una llista de preus estàndard per defecte que es basi per defecte en els paràmetres del client o del projecte.

Quan necessiteu preus personalitzats per al treball relacionat amb el projecte en una oferta concreta, podeu obtenir-ho de l'entitat associada de les llistes de preus del projecte.

Completeu els passos següents per configurar els preus del projecte específics de l'oferta.

1. Obriu l'oferta del projecte i seleccioneu la pestanya **Llistes de preus del projecte**.
2. A la subquadrícula, seleccioneu **Crea preus personalitzats**.

Totes les llistes de preus del projecte que s'adjunten a l'oferta es copien a les llistes de preus noves. Els noms de les noves llistes de preus reflecteixen el nom de l'oferta amb una marca de temps de la data de creació d'aquestes llistes de preus.

Podeu utilitzar cadascuna d'aquestes llistes de preus i fer actualitzacions dels preus laborals (preu per funció) i de despeses (preu per categoria). Aquests preus només seran aplicables a aquesta oferta de projecte.

## <a name="price-lists-on-a-project-contract"></a>Llistes de preus en un contracte de projecte

En un contracte de projecte, els preus del projecte sempre són per defecte una llista de preus personalitzada amb el nom del contracte i la marca de temps de creació afegida al nom. Això és cert si el contracte es va crear quan es va guanyar l'oferta o si el contracte es va crear des de zero. Si cal, podeu suprimir aquesta associació a la llista de preus personalitzada i associar una llista de preus estàndard al contracte del projecte.

Quan associeu una llista de preus estàndard a les llistes de preus del projecte en una oferta o contracte, els canvis realitzats als preus de la llista de preus afectaran totes les ofertes i contractes que utilitzin la llista de preus.


[!INCLUDE[footer-include](../includes/footer-banner.md)]