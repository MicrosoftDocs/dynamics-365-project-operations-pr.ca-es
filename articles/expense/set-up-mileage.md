---
title: Configuració del quilometratge amb els nivells de la taxa de quilometratge
description: Aquest article proporciona informació sobre les taxes de quilometratge i els nivells de taxa de quilometratge.
author: suvaidya
ms.date: 05/20/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 9689bbaf4c4f88ad9f746c3f98676f97e634ab6c
ms.sourcegitcommit: 5e1f549a2e55a87351b2979e3aff402ed35487e1
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/29/2022
ms.locfileid: "9064266"
---
# <a name="set-up-mileage-using-mileage-rate-tiers"></a>Configuració del quilometratge amb els nivells de la taxa de quilometratge

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

Quan es notifica una despesa i la categoria de despesa seleccionada és **Quilometratge**, l'import d'aquesta línia de despesa es calcula segons l'import de *taxa per quilometratge*. Aquest import es determina mitjançant nivells de quilometratge definits o, si no es configuren nivells de taxa de quilometratge, seguint una taxa estàndard de quilometratge. 

Per configurar els nivells de taxa de quilometratge, aneu a **Administració de despeses** > **Configuració** > **General** > **Categories de despesa** > **Quilometratge** > **Configuració de les categories**.

Després d'actualitzar a la versió 10.0.18, si la vostra organització utilitza la categoria de despesa de quilometratge, considereu habilitar la característica de quilometratge després de revisar els canvis de disseny següents. 

El nou disseny dels nivells de taxa de quilometratge afecta la manera com es processa el valor del camp **Quantitat**. Abans de la versió 10.0.18, el valor del camp **Quantitat** es considerava el límit inferior. Quan l'acumulació superava aquest valor, s'utilitzava el tipus corresponent.  A partir de la versió 10.0.18, el valor del camp **Quantitat** es considera el límit superior. La taxa corresponent s'utilitza quan l'acumulació de quilometratge és inferior al valor del camp **Quantitat**.  El nou model de nivells de quilometratge ajuda amb la coherència entre els nivells de quilometratge i un millor ús.   

Tots els informes de despesa aprovats es tornaran a calcular durant la comptabilització segons el nou disseny.

## <a name="example"></a>Exemple
 
### <a name="before-version-10018"></a>Abans de la versió 10.0.18
Amb dos nivells de taxa de quilometratge, el camp **Quantitat** de cada nivell representa el límit de quilometratge inferior. Actualment, el nivell u té un valor de zero (0) i una taxa de 0,45, i el nivell dos té un valor de 1000 i una taxa de 0,25. Si les milles o quilòmetres acumulats superen el valor del camp, s'utilitza la taxa relacionada. Si no hi ha cap línia amb la quantitat zero, el sistema utilitza la taxa de quilometratge que es defineix a l'administració de despeses. 
 
Si un empleat envia un informe de despesa amb 1.500 milles, les dues línies de quilometratge de l'informe de despesa comptabilitzat serien: 1000 (taxa de 0,45) + 500 (taxa de 0,25) = 575,00.

### <a name="after-version-10018"></a>Després de la versió 10.0.18
A la versió 10.0.18, el camp **Quantitat** de cada nivell representa el límit superior del nivell. Actualment, el nivell u té un valor de 999 i una taxa de 0,45, i el nivell dos té un valor de 999.999.999,00 i una taxa de 0,25. Si les milles o quilòmetres acumulats superen el valor del camp **Quantitat**, s'utilitza la taxa relacionada. Si se superen tots els límits superiors, el sistema utilitza la taxa de quilometratge que es defineix a l'administració de despeses. 
 
Per calcular correctament el mateix escenari, cal canviar el nivell configurat. El camp **Quantitat** del nivell u té un valor de 999,00 i un valor de 999.999.999,00 al nivell dos. Si un empleat supera la quantitat total de milles o quilòmetres al nivell 1, el sistema utilitza la taxa de quilometratge que es defineix a l'administració de despeses. 
  
Si un empleat envia un informe de despesa amb 1.500 milles, les dues línies de quilometratge de l'informe de despesa comptabilitzat serien: 1000 (taxa de 0,45) + 500 (taxa de 0,25) = 575.

## <a name="enable-the-mileage-amount-calculation-for-multiple-mileage-tiers-with-same-rate-feature"></a>Habilitar la característica Càlcul d'imports de quilometratge per a diversos nivells de quilometratge amb la mateixa taxa

La característica **Càlcul d'imports de quilometratge per a diversos nivells de quilometratge amb la mateixa taxa** millora el càlcul de la taxa de quilometratge. Completeu els passos següents per habilitar aquesta característica.

1. Aneu a **Àrees de treball** > **Administració de característiques**. 
2. A la llista, localitzeu i seleccioneu **Càlcul d'imports de quilometratge per a diversos nivells de quilometratge amb la mateixa taxa** i, a continuació, seleccioneu **Habilita ara**.

Després d'habilitar la característica, restabliu els nivells de quilometratge per reflectir correctament el valor del camp **Quantitat**. 

## <a name="enable-the-mileage-totals-calculation-by-fiscal-year-feature"></a>Habiliteu la característica Càlcul de totals de quilometratge per exercici fiscal

La característica **Càlcul de totals de quilometratge per exercici fiscal** permet una nova configuració dels paràmetres d'administració de despeses que duu a terme els càlculs dels totals de quilometratge per exercici fiscal en comptes de per any natural. Completeu els passos següents per habilitar aquesta característica.

1. Aneu a **Àrees de treball** > **Administració de característiques**.
1. A la llista, localitzeu i seleccioneu **Càlcul del totals de quilometratge per exercici fiscal** i, a continuació, seleccioneu **Habilita ara**.
1. Aneu a **Administració de despeses** > **Configuració** > **General** > **Paràmetres d'administració de despeses**.
1. A la pàgina **Paràmetres d'administració de despeses**, localitzeu i habiliteu **Utilitza l'exercici fiscal per als totals de quilometratge**.

Després d'habilitar **Utilitza l'exercici fiscal per als totals de quilometratge**, els totals de quilometratge es calculen per exercici fiscal.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
