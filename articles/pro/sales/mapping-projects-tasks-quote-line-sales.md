---
title: Assignació de projectes i tasques a una línia d'oferta basada en projectes
description: En aquest tema es proporciona informació sobre com assignar projectes i tasques a una línia de tasca basada en projectes.
author: rumant
ms.date: 10/05/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6ad46f3636d749740115b11584eb81977c73cb30b63ef1092c0c2aac97cbc647
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6988234"
---
# <a name="map-projects-and-tasks-to-a-project-based-quote-line"></a>Assignació de projectes i tasques a una línia d'oferta basada en projectes

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

A les línies d'ofertes basades en projectes, podeu assignar les tasques específiques d'un projecte que ja està associat a una línia d'oferta.

Quan assigneu tasques a una línia d'oferta, els elements següents que heu definit a la línia d'oferta només s'aplicaran a aquestes tasques:

- Mètode de facturació
- Opcions d'imputabilitat
- Límits que no s'han de superar
- Clients

Per exemple, pot ser que tingueu un projecte en què una fase sigui de preu fix i que la resta de fases siguin de temps i materials. En aquest cas, podeu associar la primera fase i totes les tasques secundàries a la línia d'oferta per a aquesta fase amb un mètode de facturació de preu fix. A continuació, podeu associar totes les altres fases a la línia d'oferta basada en temps i materials.

## <a name="associate-tasks-to-project-based-quote-lines"></a>Associar tasques a línies d’oferta basades en projectes

Podeu associar tasques amb línies d'oferta des de les ubicacions següents:

- Pàgina **Projecte** > pestanya **Facturació de tasques** (òptima)
- Pàgina **Línia d'oferta** > pestanya **Tasques imputables** 

### <a name="from-the-project-page"></a>Des de la pàgina Projecte

La pàgina **Projecte** proporciona l'experiència òptima per associar tasques a línies d'oferta. Podeu utilitzar aquesta pàgina per seleccionar diverses tasques i associar-les totes, a més de les tasques secundàries, a la línia d'oferta seleccionada.

1. A la pestanya **General** d'una línia d'oferta basada en projectes, verifiqueu que el camp **Projecte** s'hagi emplenat.
2. Al camp **Tasques incloses**, seleccioneu **Només les tasques seleccionades**.
3. Deseu la línia d'oferta basada en projectes. Quan el formulari s'actualitza, la pestanya **Tasques imputables** es mostra.
4. A la pestanya **General**, seleccioneu l'enllaç per al projecte des del camp **Projecte**.
5. A la pàgina **Projecte**, seleccioneu la pestanya **Facturació de tasques**.
6. A la segona quadrícula, que s'aplica a la configuració de facturació específica de la tasca, seleccioneu una o diverses tasques i, a continuació, seleccioneu **Associa les línies d'oferta**.
7. A la pàgina de diàleg que apareix, seleccioneu una línia d'oferta que mostri les línies d'oferta basades en projectes a l'oferta.
8. Al camp **Tipus de facturació**, indiqueu si aquestes tasques són imputables o no.
9. Marqueu la casella de selecció per indicar si l'associació ha d'incloure les tasques secundàries de les tasques seleccionades. Si marqueu la casella s'associaran les tasques secundàries de les tasques seleccionades a la línia d'oferta.
10. Trieu **D'acord** per tancar el quadre de diàleg.

### <a name="from-the-quote-line-page"></a>Des de la pàgina de la línia d'oferta

Podeu associar tasques de projecte a línies d'oferta des de la pestanya **Tasques imputables** a la pàgina **Línia d'oferta**.

>[!NOTE]
>El lloc òptim per associar tasques de projecte a línies d'oferta és la pestanya **Facturació de tasques** a la pàgina **Projecte**. Si associeu tasques de la pestanya **Tasques imputables** a la pàgina **Línia d'oferta**, heu d'associar cada projecte manualment.

1. A la pestanya **General** d'una línia d'oferta basada en projectes, verifiqueu que hi hagi un projecte seleccionat al camp **Projecte**.
2. Al camp **Tasques incloses**, seleccioneu **Només les tasques seleccionades**.
3. Deseu la línia d'oferta basada en projectes. Quan el formulari s'actualitza, la pestanya **Tasques imputables** es mostra.
4. A la pestanya **Tasques imputables**, seleccioneu **Afegeix una tasca de línia d'oferta**.
5. A la pàgina **Tasca de la línia d'oferta**, al camp **Tasques**, seleccioneu la tasca i, al camp **Tipus de facturació**, seleccioneu **Desa**. 
6. Tanqueu la pàgina. La tasca seleccionada s'associa ara a la línia d'oferta.

## <a name="disassociate-tasks-from-projectbased-quote-lines"></a>Desassociar tasques de línies d’oferta basades en projectes

### <a name="from-the-project-page"></a>Des de la pàgina Projecte

Aquest mètode proporciona l'experiència més òptima per desassociar tasques de línies d'oferta. Podeu utilitzar seleccionar diverses tasques i desassociar-les totes, a més de les tasques secundàries, de la línia d'oferta seleccionada.

1. A la pestanya **General** d'una línia d'oferta basada en projectes, al camp **Projecte**, seleccioneu l'enllaç del projecte.
2. A la pàgina **Projecte**, seleccioneu la pestanya **Facturació de tasques**.
3. A la segona quadrícula, que s'aplica a la configuració de facturació específica de la tasca, seleccioneu una o diverses tasques i, a continuació, seleccioneu **Desassocia les línies d'oferta**.
4. A la pàgina de diàleg que apareix, seleccioneu una línia d'oferta.
5. Marqueu la casella de selecció per indicar si l'associació també s'ha de suprimir de les tasques secundàries de les tasques seleccionades. Si marqueu la casella també es desassociaran les tasques secundàries de les tasques seleccionades a la línia d'oferta.
6. Seleccioneu **D'acord**. Un missatge d'advertiment us informa que, si suprimiu aquesta associació, els valors reals registrats prèviament a la tasca podrien revertir-se. 
7. Seleccioneu **D'acord** per continuar i suprimir l'associació entre la tasca i la línia d'oferta basada en projectes.

### <a name="from-the-quote-line-page"></a>Des de la pàgina de la línia d'oferta

També podeu desassociar tasques de projecte a línies d'oferta des de la pestanya **Tasques imputables** a la pàgina **Línia d'oferta**.

1. A la pestanya **Tasques imputables**, seleccioneu **Suprimeix una tasca de línia d'oferta**.
2. Seleccioneu **D'acord**. Un missatge d'advertiment us informa que, si suprimiu aquesta associació, els valors reals registrats prèviament a la tasca podrien revertir-se. 
3. Seleccioneu **D'acord** per continuar i suprimir l'associació entre la tasca i la línia d'oferta basada en projectes.

>[!NOTE]
> Aquest procediment no suprimeix la tasca del projecte. Només elimina l'associació de la tasca de la línia d'oferta basada en projectes.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]