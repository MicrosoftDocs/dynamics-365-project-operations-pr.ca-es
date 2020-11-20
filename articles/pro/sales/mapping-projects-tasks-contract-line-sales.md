---
title: Assignació de projectes i tasques a una línia de contracte basada en projectes (bàsic)
description: Aquest tema proporciona informació sobre l'addició i eliminació de projectes i tasques a una línia de contracte.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 30a74f683a032d5bd6caed347f4d0a948376d267
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177634"
---
# <a name="map-projects-and-tasks-to-a-project-based-contract-line---lite"></a>Assignació de projectes i tasques a una línia de contracte basada en projectes (bàsic)

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_

A les línies de contracte basades en projectes, podeu assignar tasques específiques en un projecte a la línia de contracte.

Quan assigneu tasques específiques a una línia de contracte, el mètode de facturació, les opcions d'imputabilitat, els límits que no s'han de superar i els clients definits a la línia de contracte només seran aplicables a aquestes tasques específiques.

Si teniu un escenari on una fase d'un projecte, per exemple la fase Prototip, és de preu fix i totes les altres fases són de temps i material, podreu associar la fase Prototip i totes les tasques secundàries associades a la línia de contracte per a aquesta fase amb un mètode de facturació de preu fix.

Totes les altres fases de l'estructura del desglossament del treball del projecte (WBS) es poden associar a la línia de contracte basada en temps i material.

## <a name="associate-tasks-to-project-based-contract-lines"></a>Associar tasques a línies de contracte basades en projectes

Les tasques es poden associar a les línies de contracte des de la pestanya **Tasques imputables** de la pàgina **Línia de contracte** o des de la pestanya **Facturació de tasques** de la pàgina **Projecte**.

### <a name="from-the-contract-line-page"></a>Des de la pàgina Línia de contracte

Completeu els passos següents per associar les tasques del projecte a la línia de contracte des de la pestanya **Tasques imputables** de la pàgina **Línia de contracte**.

1. A la pestanya **General** d'una línia de contracte basada en projectes, verifiqueu que el camp **Projecte** estigui emplenat.
2. Al camp **Tasques incloses**, seleccioneu **Només tasques seleccionades**.
3. Desa els canvis. El formulari s'actualitzarà i la pestanya **Tasques imputables** serà visible.
4. Seleccioneu la pestanya **Tasques imputables** i, a la subquadrícula, seleccioneu **Afegeix una tasca de línia de contracte**.
5. A la pàgina **Tasques de línia de contracte**, al menú desplegable **Tasques**, seleccioneu la tasca. 
6. Introduïu informació al camp **Tipus de facturació** i, a continuació, seleccioneu **Desa i tanca**. La tasca seleccionada s'associa a la línia de contracte.

> [!NOTE]
> Aquesta no és l'experiència més òptima per associar les tasques del projecte a les línies de contracte. Cada projecte s'haurà d'associar manualment en aquesta experiència. La manera preferida és des de la pestanya **Facturació de tasques** de la pàgina **Projecte**.

### <a name="from-the-project-page"></a>Des de la pàgina Projecte

Aquest és el mètode òptim per associar tasques a línies de contracte. Podeu seleccionar diverses tasques i associar-les totes i les seves tasques secundàries a la línia de contracte seleccionada. Completeu els passos següents per associar tasques a la línia de contracte des de la pàgina **Projecte**.

1. A la pestanya **General** d'una línia de contracte basada en projectes, verifiqueu que el camp **Projecte** estigui emplenat.
2. Al camp **Tasques incloses**, seleccioneu **Només tasques seleccionades**.
3. Deseu la línia de contracte basada en projectes. El formulari s'actualitzarà i la pestanya **Tasques imputables** serà visible. Això és només amb finalitats de verificació.
4. A la pestanya **General** de la línia de contracte basada en projectes, al camp **Projecte**, seleccioneu l'enllaç del projecte.
5. A la pàgina **Projecte**, seleccioneu la pestanya **Configuració de la facturació de la tasca**.
6. Hi ha dues quadrícules. Una quadrícula és per a les línies de contracte que s'apliquen a tot el projecte. La segona quadrícula s'aplica a la configuració de facturació específica de la tasca. A la segona quadrícula, seleccioneu una o diverses tasques i, a continuació, seleccioneu **Associa les línies de contracte**.
7. A la pàgina de diàleg que s'obre, seleccioneu una línia de contracte al menú desplegable.
8. Utilitzeu el desplegable **Tipus de facturació** per marcar les tasques com a imputables o no imputables.
9. Marqueu la casella de selecció per indicar si l'associació també hauria d'incloure les tasques secundàries de les tasques seleccionades. Si marqueu la casella també s'associaran les tasques secundàries de les tasques seleccionades a la línia de contracte.
10. Trieu **D'acord** per tancar el quadre de diàleg.

## <a name="unassociate-tasks-from-project-based-contract-lines"></a>Desassociar tasques de línies de contracte basades en projectes

### <a name="from-the-contract-line-page"></a>Des de la pàgina Línia de contracte

Completeu els passos següents per desassociar les tasques del projecte de la línia de contracte a la pestanya **Tasques imputables** de la pàgina **Línia de contracte**.

1. A la pestanya **Tasques imputables**, seleccioneu **Suprimeix una tasca de línia de contracte**.
2. Un missatge d'advertiment indica que l'eliminació d'aquesta associació podria donar lloc a la reversió dels valors reals registrats prèviament a la tasca. Seleccioneu **D'acord** al diàleg per suprimir l'associació entre la tasca i la línia de contracte basada en projectes. 

> [!NOTE]
> Això no suprimeix la tasca del projecte. En lloc d'això, suprimeix l'associació de tasques de la línia de contracte basada en projectes.

### <a name="from-the-project-page"></a>Des de la pàgina Projecte

Aquesta és l'experiència més òptima per desassociar tasques de les línies de contracte. Podeu seleccionar diverses tasques i desassociar-les totes i les seves tasques secundàries de la línia de contracte seleccionada. Completeu els passos següents per desassociar tasques de la línia de contracte.

1. A la pestanya **General** de la línia de contracte basada en projectes, al camp **Projecte**, feu clic a l'enllaç del projecte.
2. A la pàgina **Projecte**, seleccioneu la pestanya **Configuració de la facturació de la tasca**.
3. Hi ha dues quadrícules a la pàgina. Una quadrícula és per a les línies de contracte que s'apliquen a tot el projecte i la segona s'aplica a la configuració de facturació específica de la tasca. A la segona quadrícula, seleccioneu una o diverses tasques i, a continuació, seleccioneu **Desassocia les línies de contracte**.
4. A la pàgina de diàleg que s'obre, seleccioneu una línia de contracte al menú desplegable.
5. Marqueu la casella de selecció per indicar si l'associació també s'hauria de suprimir de les tasques secundàries de les tasques seleccionades. Si marqueu la casella també es desassociaran les tasques secundàries de les tasques seleccionades de la línia de contracte.
6. Seleccioneu **D'acord**. Un missatge d'advertiment indica que l'eliminació d'aquesta associació podria donar lloc a la reversió dels valors reals registrats prèviament a la tasca. Seleccioneu **D'acord** al diàleg d'advertiment per suprimir l'associació entre la tasca i la línia de contracte basada en projectes.
