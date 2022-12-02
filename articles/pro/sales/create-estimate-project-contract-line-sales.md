---
title: Estimació d'una línia de contracte basada en projectes (bàsic)
description: Aquest article proporciona informació sobre l'estimació d'una línia de contracte basada en projectes.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 8b4379cc5822d08b55623f0f3d4d49791af90927
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914390"
---
# <a name="estimate-a-projectbased-contract-line---lite"></a>Estimació d'una línia de contracte basada en projectes (bàsic)

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_

Al Dynamics 365 Project Operations, una línia de contracte basada en projectes té detalls que ajuden a estimar el cost i els ingressos potencials del treball dedicat a realitzar la línia de contracte.

Per estimar una línia de contracte basada en projectes, aneu a la pestanya **Detall de línia contracte** de la **línia de contracte** basada en projectes.  Hi ha dues maneres de crear una estimació en una línia de contracte basada en projectes:

   - Crear una estimació directament a la línia de contracte afegint manualment els detalls de la línia de contracte.
   - Crear un projecte i un pla de projecte i després associar el projecte i les tasques a la línia de contracte del projecte. Això permet el procés pel qual podeu importar l'estimació del pla de projecte a la línia de contracte segons els components inclosos en la línia de contracte.

## <a name="create-an-estimation-directly-on-a-projectbased-contract-line"></a>Crear una estimació directament en una línia de contracte basada en projectes

Per crear una estimació directament en una línia de contracte basada en projecte, seguiu aquests passos:

1. Aneu a la línia de contracte i seleccioneu la pestanya **Detall de la línia contracte**. Les línies que creeu en aquesta pestanya es resumeixen i es mostren com el **valor contractat** per a aquesta **línia contracte**. 
2. A la subquadrícula **Detalls de la línia de contracte**, seleccioneu **Nou detall de línia contracte**. S'obre un control lliscant de creació ràpida. Els camps següents estan disponibles a la pàgina **Detalls de la línia de contracte**.

| Camp | Location | Descripció | Impacte descendent |
| --- | --- | --- | --- |
| **Descripció** | **Creació ràpida** | Descripció de l'estimació específica. | Aquest valor per defecte és el detall de la línia de contracte relacionada per al cost que es crea automàticament. |
| **Classe de la transacció** | **Creació ràpida** | Es tracta d'una llista de classes de transaccions incloses a la pestanya **General** de la línia de contracte basada en projectes. | Aquest valor per defecte és el detall de la línia de contracte relacionada per al cost que es crea automàticament. |
| **Seleccioneu el producte** | **Creació ràpida** | S'aplica quan la classe de transacció és **Material**. Podeu especificar si aquesta línia de previsió és per a un producte **Existent** (catàleg) o un producte **Fora de catàleg**. | Aquest valor per defecte és el detall de la línia de contracte relacionada per al cost que es crea automàticament. |
| **Producte** | **Creació ràpida** | L'identificador del producte del catàleg de productes. Aquest camp només està habilitat quan seleccioneu **Producte existent** al camp **Seleccioneu un producte**. L'ID s'utilitza per recuperar el preu de venda de la llista de preus del projecte al contracte. | Aquest valor per defecte és el detall de la línia de contracte relacionada per al cost que es crea automàticament. |
| **Producte fora de catàleg** | **Creació ràpida** | Camp de text on cal introduir el nom del producte. Aquest camp només està habilitat quan seleccioneu **Fora de catàleg** al camp **Seleccioneu un producte**.| Aquest valor per defecte és el detall de la línia de contracte relacionada per al cost que es crea automàticament. |
| **Funció** | **Creació ràpida** | Funció de la persona que està realitzant aquest treball o incorrent en aquesta despesa. | Aquest valor per defecte és el detall de la línia de contracte relacionada per al cost que es crea automàticament.|
| **Categoria** | **Creació ràpida** | Categoria del treball o despesa. |Aquest valor per defecte és el detall de la línia de contracte relacionada per al cost que es crea automàticament.|
| **Data d’inici** | **Creació ràpida** | Data d'inici del treball. | Aquest valor per defecte és el detall de la línia de contracte relacionada per al cost que es crea automàticament. |
| **Data d'acabament** | **Creació ràpida** | Data de finalització del treball. | Aquest valor per defecte és el detall de la línia de contracte relacionada per al cost que es crea automàticament. |
| **Unitat de recursos** | **Creació ràpida** | Unitat de proveïment que incorre en aquest cost i proporciona el recurs per treballar-hi. |Aquest valor per defecte és el detall de la línia de contracte relacionada per al cost que es crea automàticament i s'utilitza en la recuperació del preu de cost. |
| **Planificació d'unitat** | **Creació ràpida** | Grup d'unitats del treball, el producte o la despesa. Les unitats pertanyen a una planificació d'unitat o a un grup d'unitats. Per exemple, les *milles* i els *quilòmetres (km)* són unitats que pertanyen a un grup d'unitats que descriuen la distància. | Aquest valor per defecte és el detall de la línia de contracte relacionada per al cost que es crea automàticament. |
| **Unitat** | **Creació ràpida** | La unitat de treball, producte o despesa. | Aquest valor per defecte és el detall de la línia de contracte relacionada per al cost que es crea automàticament. |
| **Quantitat** | **Creació ràpida** | La quantitat de treball, producte o despesa. | Aquest valor per defecte és el detall de la línia de contracte relacionada per al cost que es crea automàticament. |
| **Preu per unitat** | **Creació ràpida** | Percentatge de facturació de la funció que està realitzant la feina, el preu unitari del producte o el preu de venda de la categoria de producte o despesa. Aquest valor és per defecte el **Temps** a partir de la combinació dels valors de dimensió de preus de la línia de preu de la funció de la llista de preus del projecte que sigui efectiva per a la data d'inici. Per a les **Despeses**, el valor per defecte d'aquest camp és de la configuració de preus per a la categoria de transacció a la llista de preus del projecte que és efectiva per a la data d'inici. Si el mètode de càlcul de preus de la categoria transacció no és de **preu per unitat**, no hi ha cap valor per defecte i aquest camp es deixa en blanc. Per als productes, el valor per defecte d'aquest camp es basa en la línia **Element de la llista de preus** de la llista de preus del projecte efectiva per a la data d'inici.| Percentatge de cost de la funció que està realitzant la feina, o el cost unitari de la categoria de despeses o cost unitari del producte. El valor per defecte d'aquest camp és **Temps** a partir de la combinació dels valors de dimensió de preus de la línia de preu de la funció de la llista de preus de cost adjuntada a la unitat de contractació que sigui efectiva per a la data d'inici. Per a les despeses, el valor per defecte d'aquest camp es basada en la línia de preus per categoria de la llista de preus de cost adjunta a la unitat contractant que és efectiva per a la data d'inici. Si el mètode de càlcul de preus de la categoria transacció no és de preu per unitat, no hi ha cap valor per defecte i aquest camp es deixa en blanc. Per als productes, el valor per defecte d'aquest camp es basa en la línia **Element de la llista de preus** de la llista de preus de cost adjuntada a la unitat de contractació efectiva per a la data d'inici.|
| **Impost estimat** | **Creació ràpida** | Impost previst per a aquesta feina o despesa. | Impost previst per a aquesta feina o despesa. |
| **Import** | **Creació ràpida** | Podeu afegir el valor d'aquest camp si els camps **Quantitat** i **Preu** es deixen en blanc. Si **Quantitat** i **Preu** s'emplenen, el camp **Import** és de només lectura i es calcula com a **(Quantitat \* Preu per unitat) + Impostos**. | &nbsp; |

## <a name="update-prices-on-contract-line-details"></a>Actualitzar els preus en els detalls de la línia de contracte

Si canvieu els preus de la llista de preus del projecte que s'adjunta al contracte o la llista de preus de cost de la unitat contractant, podeu actualitzar els preus dels detalls de la línia de contracte individual per reflectir el canvi. A la pàgina **Contracte**, seleccioneu **Torna a calcular**. Apareix un advertiment per informar-vos que es restabliran els preus de totes les línies de contracte d'aquest contracte. Seleccioneu **Sí** per actualitzar els preus tant per als detalls de la línia de vendes com de cost.

## <a name="access-contract-line-details-for-cost"></a>Accedir als detalls de la línia de contracte per al cost

A la pestanya **Detalls de la línia de contracte**, seleccioneu una fila a la quadrícula per mostrar les accions a la barra d'eines de la subquadrícula. La primera acció a la barra d'eines de la subquadrícula és **Obre el detall de cost**. Per veure la tarifa de cost i l'import relacionats per aquest detall de línia de contracte, seleccioneu **Obre el detall de cost**. 

> [!NOTE]
> Canviar els valors d'empresa de recursos, unitat de recursos, quantitat, dates, funció o categoria en el detall de la línia de contracte per al **cost** també canvia els valors corresponents en el detall de la línia de contracte de **vendes**.

## <a name="currency-on-contract-line-details-for-cost-and-sales"></a>Moneda als detalls de la línia de contracte per al cost i les vendes

El detall de la línia de contracte per a les **vendes** estableix la moneda per defecte a partir de la llista de preus del projecte que és efectiva per a la data d'inici del detall de la línia de contracte.

El detall de la línia de contracte per al **cost** estableix la moneda per defecte a partir de la llista de preus de la unitat contractant del contracte que és efectiva per a la data d'inici del detall de la línia de contracte per al **cost**.

Els càlculs de rendibilitat converteixen els imports per als detalls de la línia de contracte per al **cost** i les **vendes** en la moneda base de l'entorn per informar dels marges reals i estimats generals del contracte.

> [!NOTE]
> Podrien ocórrer errors d'arrodoniment de moneda i canvis de marges a causa de la manca de tipus de canvi amb data d'efectivitat. Utilitzeu aquests càlculs només als contractes de projecte, ja que són aproximacions i no són per a l'ús reglamentari real ni per a altres informes que requereixin una major precisió d'arrodoniment i coneixement de la data de vigència dels tipus de canvi.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
