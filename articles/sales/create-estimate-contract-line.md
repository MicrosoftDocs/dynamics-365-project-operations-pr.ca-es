---
title: Estimació d'una línia de contracte basada en projectes
description: Aquest tema proporciona informació sobre les estimacions en una línia de contracte basada en projectes.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cdc8984e080d995e3a0b667fe662291b499235b2
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278496"
---
# <a name="estimate-a-projectbased-contract-line"></a>Estimació d'una línia de contracte basada en projectes

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_ 

Al Dynamics 365 Project Operations, una línia de contracte basada en projectes té detalls que ajuden a estimar el cost i els ingressos potencials del treball dedicat a realitzar la línia de contracte.

Per estimar una línia de contracte basada en projectes, aneu a la pestanya **Detall de línia contracte** de la **línia de contracte** basada en projectes.  Hi ha dues maneres de crear una estimació en una línia de contracte basada en projectes:

   - Crear una estimació directament a la línia de contracte afegint manualment els detalls de la línia de contracte.
   - Crear un projecte i un pla de projecte i després associar el projecte i les tasques a la línia de contracte del projecte. Això permet el procés pel qual podeu importar l'estimació del pla de projecte a la línia de contracte segons els components inclosos en la línia de contracte.

## <a name="create-an-estimate-directly-on-a-projectbased-contract-line"></a>Crear una estimació directament en una línia de contracte basada en projectes

1. Aneu a la línia de contracte i seleccioneu la pestanya **Detall de la línia contracte**. Les línies que creeu en aquesta pestanya es resumeixen i es mostren com el **valor contractat** per a aquesta **línia contracte**. 
2. A la subquadrícula **Detalls de la línia de contracte**, seleccioneu **+ Nou detall de línia contracte**. S'obre un control lliscant de creació ràpida. Els següents camps estan disponibles en el formulari **Detalls de la línia de contracte**:

| Camp | Location | Descripció | Impacte descendent |
| --- | --- | --- | --- |
| **Descripció** | **Creació ràpida** | Descripció de l'estimació específica. | Aquest camp per defecte és el detall de la línia de contracte relacionada per als costos que es creen automàticament. |
| **Classe de la transacció** | **Creació ràpida** | Aquesta llista desplegable és una llista de classes de transaccions incloses a la pestanya **General** de la línia de contracte basada en projectes. | Aquest camp per defecte és el detall de la línia de contracte relacionada per als costos que es creen automàticament. |
| **Funció** | **Creació ràpida** | Funció de la persona que està realitzant aquest treball o incorrent en aquesta despesa. | Aquest camp per defecte és el detall de la línia de contracte relacionada per als costos que es creen automàticament. |
| **Categoria** | **Creació ràpida** | Categoria del treball o despesa. | Aquest camp per defecte és el detall de la línia de contracte relacionada per als costos que es creen automàticament. |
| **Data d'inici** | **Creació ràpida** | Data d'inici del treball. | Aquest camp per defecte és el detall de la línia de contracte relacionada per als costos que es creen automàticament. |
| **Data d'acabament** | **Creació ràpida** | Data de finalització del treball. | Aquest camp per defecte és el detall de la línia de contracte relacionada per al cost que es crea automàticament. |
| **Empresa de dotació de recursos** | **Creació ràpida** | Empresa de recursos o entitat jurídica que està incorrent en aquest cost i que proporciona el recurs per treballar-hi. | Aquest camp per defecte és el detall de la línia de contracte relacionada per als costos que es creen automàticament. Aquest camp també s'utilitza a la recuperació de preus de cost. |
| **Unitat de recursos** | **Creació ràpida** | Unitat de recursos que incorre en aquest cost i proporciona el recurs per treballar-hi. | Aquest camp per defecte és el detall de la línia de contracte relacionada per als costos que es creen automàticament. Aquest camp també s'utilitza a la recuperació de preus de cost. |
| **Planificació d'unitat** | **Creació ràpida** | Grup d'unitats del treball o despesa. Les unitats pertanyen a una planificació d'unitat o a un grup d'unitats. Per exemple, les *milles* i els *quilòmetres* són unitats que pertanyen a un grup d'unitats que descriuen la distància. | Aquest camp per defecte és el detall de la línia de contracte relacionada per als costos que es creen automàticament. |
| **Unit** | **Creació ràpida** | Unitat de treball o despesa. | Aquest camp per defecte és el detall de la línia de contracte relacionada per als costos que es creen automàticament. |
| **Quantitat** | **Creació ràpida** | Quantitat de treball o despesa. | Aquest camp per defecte és el detall de la línia de contracte relacionada per als costos que es creen automàticament. |
| **Preu per unitat** | **Creació ràpida** | Tarifa de facturació de la funció que està realitzant el treball o preu de venda de la categoria de despeses. Aquest camp per defecte és **Temps** segons la combinació de funció i unitat de recursos a la llista de preus del projecte aplicable a la data d'inici. Per a les despeses, el valor per defecte d'aquest camp és de la configuració de preus per a la categoria de transacció a la llista de preus del projecte que és efectiva per a la data d'inici. Si el mètode de càlcul de preus de la categoria transacció no és de **preu per unitat**, no hi ha cap valor per defecte i aquest camp es deixa en blanc. | Tarifa de cost de la funció que està realitzant el treball o cost per unitat de la categoria de despeses. Aquest camp per defecte és **Temps** en funció de la combinació de funció i unitat de recursos a la línia de preu per funció de la llista de preus de cost adjunta a la unitat de contractació efectiva per a la data d'inici. Per a les despeses, el valor per defecte d'aquest camp es basada en la línia de preus per categoria de la llista de preus de cost adjunta a la unitat contractant que és efectiva per a la data d'inici. Si el mètode de càlcul de preus de la categoria transacció no és de preu per unitat, no hi ha cap valor per defecte i aquest camp es deixa en blanc. |
| **Impost estimat** | **Creació ràpida** | Impost estimat per aquest treball o despesa com a entrada per l'usuari. | Impost estimat per aquest treball o despesa com a entrada per l'usuari. |
| **Import** | **Creació ràpida** | Aquest valor en aquest camp pot afegir-lo l'usuari si els camps **Quantitat** i **Preu** es deixen en blanc. Si **Quantitat** i **Preu** s'emplenen, el camp **Import** és de només lectura i es calcula com a **(Quantitat \* Preu per unitat) + Impostos**. | &nbsp; |

## <a name="update-prices-on-contract-line-details"></a>Actualitzar els preus en els detalls de la línia de contracte

Si canvieu els preus de la llista de preus del projecte que s'adjunta al contracte o la llista de preus de cost de la unitat contractant, podeu actualitzar els preus dels detalls de la línia de contracte individual per reflectir el canvi. A la pàgina **Contracte**, seleccioneu **Torna a calcular**. S'obre un avís per informar-los que es restableixen els preus de totes les línies de contracte en aquest contracte. Seleccioneu **Sí** per actualitzar els preus tant per als detalls de la línia de vendes com de cost.

## <a name="access-contract-line-details-for-cost"></a>Accedir als detalls de la línia de contracte per al cost

A la pestanya **Detalls de la línia de contracte**, seleccioneu una fila a la quadrícula per mostrar les accions a la barra d'eines de la subquadrícula. La primera acció a la barra d'eines de la subquadrícula és **Obre el detall de cost**. Per veure la tarifa de cost i l'import relacionats per aquest detall de línia de contracte, seleccioneu **Obre el detall de cost**. 

> [!NOTE]
> Canviar els valors d'empresa de recursos, unitat de recursos, quantitat, dates, funció o categoria en el detall de la línia de contracte per al **cost** també canvia els valors corresponents en el detall de la línia de contracte de **vendes**.

## <a name="currency-on-contract-line-details-for-cost-and-sales"></a>Moneda als detalls de la línia de contracte per al cost i les vendes

El detall de la línia de contracte per a les **vendes** estableix la moneda per defecte a partir de la llista de preus del projecte que és efectiva per a la data d'inici del detall de la línia de contracte.

El detall de la línia de contracte per al **cost** estableix la moneda per defecte a partir de la llista de preus de la unitat contractant del contracte que és efectiva per a la data d'inici del detall de la línia de contracte per al **cost**.

Els càlculs de rendibilitat converteixen els imports per als detalls de la línia de contracte per al **cost** i les **vendes** en la moneda base de l'entorn per informar dels marges reals i estimats generals del contracte.

> [!NOTE]
> Podrien ocórrer errors d'arrodoniment de moneda i canvis de marges a causa de la manca de tipus de canvi amb data d'efectivitat. Utilitzeu aquests càlculs en els contractes de projectes només com a aproximacions i no per a la presentació legal real o d'altres informes que requereixin una major precisió d'arrodoniment i reconeixement de la data d'efectivitat per als tipus de canvi.


[!INCLUDE[footer-include](../includes/footer-banner.md)]