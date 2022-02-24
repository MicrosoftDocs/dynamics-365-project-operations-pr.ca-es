---
title: Estimació d'una línia d'oferta de projecte
description: Aquest tema proporciona informació sobre com crear una estimació en una línia d'oferta del projecte.
author: rumant
manager: Annbe
ms.date: 04/01/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b941511f842a81764ddd1c05a437578b9fd902ce
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858776"
---
# <a name="estimate-a-project-quote-line"></a>Estimació d'una línia d'oferta de projecte

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

Una línia d'oferta basada en projectes conté detalls que ajuden a estimar el cost i els possibles ingressos del treball implicat per lliurar la línia d'oferta.

Per calcular una línia d'oferta basada en projectes, a la línia d'oferta, seleccioneu la pestanya **Detall de la línia d'oferta**. Hi ha dues maneres de crear una estimació en una línia d'oferta basada en projectes:

   - Creeu manualment l'estimació directament a la línia d'oferta mitjançant els detalls de la línia d'oferta. 
   - Crear un projecte i un pla de projecte i, a continuació, associar el projecte i les tasques del projecte a la línia d'oferta. El procés per importar les estimacions del pla del projecte a la línia d'oferta segons la informació que heu facilitat s'habilitarà.

## <a name="create-estimates-directly-on-a-project-based-quote-line"></a>Creació d'estimacions directament en una línia d'oferta basada en projectes

Per crear estimacions directament en una línia d'oferta basada en projecte, seguiu aquests passos:

1. Per crear una estimació en una línia d'oferta basada en projectes, seleccioneu la pestanya **Detalls de la línia d'oferta**. L'element de línia que creeu en aquesta pestanya resumirà el valor ofert per a aquesta línia d'oferta. 
2. Per crear els detalls de la línia d'oferta, seleccioneu **Nou detall de la línia d'oferta** a la subquadrícula **Detalls de la línia d'oferta**. S'obrirà un control lliscant de creació ràpida. Els camps següents de la pàgina **Línia d'oferta**.

| **Camp** | **Location** | **Descripció** | **Impacte descendent** |
| --- | --- | --- | --- |
| Descripció | Creació ràpida | Descripció de l'estimació específica. | Aquest valor per defecte és el detall de la línia d'oferta relacionada per al cost que es crea automàticament. |
| Classe de la transacció | Creació ràpida | Aquesta llista desplegable proporciona les classes de transacció que s'inclouen a la pestanya **General** de la línia d'oferta basada en projectes.  | Aquest valor per defecte és el detall de la línia d'oferta relacionada per al cost que es crea automàticament. |
| Seleccioneu el producte | Creació ràpida | S'aplica quan la classe de transacció és **Material**. Podeu seleccionar d'especificar que aquesta línia de previsió és per a un producte **Existent** (catàleg) o un producte **Fora de catàleg**. | Aquest valor per defecte és el detall de la línia d'oferta relacionada per al cost que es crea automàticament. |
| Producte | Creació ràpida | L'identificador del producte del catàleg de productes. Aquest camp només està habilitat quan seleccioneu **Existent** al camp **Seleccioneu un producte**. L'ID s'utilitza per recuperar el preu de venda de la llista de preus del projecte a l'oferta. | Aquest valor per defecte és el detall de la línia d'oferta relacionada per al cost que es crea automàticament. |
| Producte fora de catàleg | Creació ràpida | Quadre de text on cal escriure el nom del producte. Aquest camp només està habilitat quan seleccioneu **Fora de catàleg** al camp **Seleccioneu un producte**.| Aquest valor per defecte és el detall de la línia d'oferta relacionada per al cost que es crea automàticament. |
| Funció | Creació ràpida | Funció de la persona que durà a terme aquesta feina o que incorri en aquesta despesa. | Aquest valor per defecte és el detall de la línia d'oferta relacionada per al cost que es crea automàticament. |
| Categoria | Creació ràpida | Categoria del treball o despesa. | Aquest valor per defecte és el detall de la línia d'oferta relacionada per al cost que es crea automàticament. |
| Data d’inici | Creació ràpida | Data d'inici del treball. | Aquest camp pren per defecte el valor del detall de la línia d'oferta relacionada per al cost que es crea automàticament. |
| Data d’acabament | Creació ràpida | Data de finalització del treball. | Aquest camp pren per defecte el valor del detall de la línia d'oferta relacionada per al cost que es crea automàticament. |
| Empresa de dotació de recursos | Creació ràpida | Empresa de proveïment o entitat legal que incorre en aquest cost i proporciona el recurs per treballar-hi. | El valor per defecte és el detall de la línia d'oferta relacionada per al cost que es crea automàticament i s'utilitza en la recuperació del preu de cost. |
| Unitat de recursos | Creació ràpida | Unitat de proveïment que incorre en aquest cost i proporciona el recurs per treballar-hi. | Aquest valor per defecte és el detall de la línia d'oferta relacionada per al cost que es crea automàticament i s'utilitza en la recuperació del preu de cost. |
| Planificació d'unitat | Creació ràpida | Grup d'unitats del treball, el producte o la despesa. Les unitats pertanyen a una planificació d'unitat o a un grup d'unitats. Per exemple, les milles i els kilòmetres són unitats que pertanyen a un grup d'unitats que descriuen la distància. | Aquest valor per defecte és el detall de la línia d'oferta relacionada per al cost que es crea automàticament. |
| Unitat | Creació ràpida | La unitat del treball, el producte o la despesa. | Aquest valor per defecte és el detall de la línia d'oferta relacionada per al cost que es crea automàticament. |
| Quantitat | Creació ràpida | La quantitat de treball, producte o despesa. | Aquest valor per defecte és el detall de la línia d'oferta relacionada per al cost que es crea automàticament. |
| Preu unitari | Creació ràpida |Percentatge de facturació de la funció que està realitzant la feina, el preu unitari del producte o el preu de venda de la categoria de producte o despesa. El valor per defecte de **Temps** es basa en la combinació dels valors de dimensió de preus de la línia de preu de la funció de la llista de preus del projecte que sigui efectiva per a la data d'inici. Per a les **Despeses**, el valor per defecte és la configuració de preus de la categoria de transaccions de la llista de preus del projecte efectiva per a la data d'inici. Si el mètode de càlcul de preus de la categoria transacció no és de preu per unitat, no hi ha cap valor per defecte i aquest camp es deixa en blanc. Per als productes, el valor per defecte d'aquest camp es basa en la línia **Element de la llista de preus** de la llista de preus del projecte efectiva per a la data d'inici.| Percentatge de cost de la funció que està realitzant la feina, el cost unitari de la categoria de despeses o el cost unitari del producte. El valor per defecte de **Temps** es basa en la combinació dels valors de dimensió de preus de la línia de preu de la funció de la llista de preus de cost adjuntada a la unitat de contractació que sigui efectiva per a la data d'inici. Per a les despeses, el valor per defecte es basa en la línia de preu de la categoria de la llista de preus de cost adjuntada a la unitat de contractació efectiva per a la data d'inici. Si el mètode de càlcul de preus de la categoria de transaccions no és el preu unitari, no hi ha cap valor per defecte i aquest camp es deixa en blanc. Per als productes, el valor per defecte d'aquest camp es basa en la línia **Element de la llista de preus** de la llista de preus de cost adjuntada a la unitat de contractació efectiva per a la data d'inici.|
| Impost estimat | Creació ràpida | Podeu introduir manualment l'impost previst per a aquesta feina o despesa. | No hi ha cap impacte descendent d'aquest camp. |
| Import | Creació ràpida | Podeu introduir informació manualment en aquest camp si els camps **Quantitat** i **Preu** es deixen en blanc. Si aquests camps no estan en blanc, aquest camp és només de lectura i es calcula com a (Quantitat \* Preu per unitat) + Impost. | No hi ha cap impacte descendent d'aquest camp. |

## <a name="update-prices-on-quote-line-details"></a>Actualitzar els preus dels detalls de la línia d'oferta

Si heu canviat els preus de la llista de preus del projecte vinculada a l'oferta o a la llista de preu de cost de la unitat de contractant, podeu seleccionar **Torna a calcular** a la pàgina **Oferta** per actualitzar els preus dels detalls de la línia d'oferta individual per reflectir aquest canvi. Quan seleccioneu **Torna a calcular**, apareix un advertiment que us informa que els preus dels detalls de la línia d'oferta per a totes les línies d'oferta d'aquesta oferta es restabliran. Seleccioneu **Sí** per actualitzar els preus dels detalls de la línia de vendes i d'oferta de costos.

## <a name="access-quote-line-details-for-cost"></a>Accedir als detalls de la línia d'oferta per al cost

Per accedir als detalls de la línia d'oferta per al cost, seguiu aquests passos:

1. A la pestanya **Detalls de la línia d'oferta**, seleccioneu una fila de la quadrícula per habilitar les accions a la barra d'eines de la subquadrícula. 
2. Seleccioneu **Obre els detalls del cost** per veure la tarifa de costos i la quantitat relacionada d'aquesta línia d'oferta.

> [!NOTE]
> Si canvieu la unitat, la quantitat, les dates, la funció o els valors de categoria del detall de la línia d'oferta per al cost, canviaran els valors corresponents als detalls de la línia d'oferta.

## <a name="currency-on-quote-line-details-for-cost-and-sales"></a>Moneda als detalls de la línia d'oferta per al cost i les vendes

Moneda al detall de la línia d'oferta per als valors per defecte de vendes de la llista de preus del projecte que és vigent per a la data d'inici del detall de la línia d'oferta.

Moneda al detall de la línia d'oferta per als valors per defecte de cost de la llista de preus de la unitat de contractació de l'oferta que és vigent per a la data d'inici del detall de la línia d'oferta per al cost.

> [!NOTE]
> Els càlculs de rendibilitat converteixen l'import en els detalls de la línia d'oferta per al cost i les vendes a la moneda base de l'entorn per informar del marge previst global de l'oferta. Podrien ocórrer errors d'arrodoniment de moneda i canvis de marges a causa de la manca de tipus de canvi amb data d'efectivitat. Utilitzeu aquests càlculs només a les ofertes de projecte, ja que són aproximacions i no són per a l'ús reglamentari real ni per a altres informes que requereixin una major precisió d'arrodoniment i coneixement de la data de vigència dels tipus de canvi.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
