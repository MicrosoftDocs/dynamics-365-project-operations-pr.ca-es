---
title: Estimació d'una línia d'oferta basada en projectes
description: En aquest tema es proporciona informació sobre com crear una estimació en una línia d'oferta basada en projectes.
author: rumant
ms.date: 04/01/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: a29cf20fe95ee5bfb189defded4f06aadb75a841
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8598338"
---
# <a name="estimating-a-project-based-quote-line"></a>Estimació d'una línia d'oferta basada en projectes

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_

Una línia d'oferta basada en projectes conté detalls que ajuden a estimar el cost i els possibles ingressos del treball implicat per lliurar la línia d'oferta.

Per estimar una línia d'oferta basada en projectes, a la línia d'oferta basada en projectes, seleccioneu la pestanya **Detalls de la línia d'oferta**. Hi ha dues maneres de crear una estimació en una línia d'oferta basada en projectes:

- Creeu manualment l'estimació directament a la línia d'oferta mitjançant els detalls de la línia d'oferta. 
- Crear un projecte i un pla de projecte i, a continuació, associar el projecte i les tasques del projecte a la línia d'oferta. El procés per importar les estimacions del pla del projecte a la línia d'oferta segons la informació que heu facilitat s'habilitarà.

## <a name="create-estimates-directly-on-a-project-based-quote-line"></a>Creació d'estimacions directament en una línia d'oferta basada en projectes

Per crear una estimació en una línia d'oferta basada en projectes, seleccioneu la pestanya **Detalls de la línia d'oferta**. L'element de línia que creeu en aquesta pestanya resumirà el valor ofert per a aquesta línia d'oferta. 

Per crear els detalls de la línia d'oferta, seleccioneu **Nou detall de la línia d'oferta** a la subquadrícula **Detalls de la línia d'oferta**. S'obrirà un control lliscant de creació ràpida. A la taula següent es proporcionen detalls sobre els camps de la pàgina **Detall de la línia d'oferta** i sobre com els valors afecten la funcionalitat.

| **Camp** | **Location** | **Descripció** | **Impacte descendent** |
| --- | --- | --- | --- |
| Descripció | Creació ràpida | Descripció de l'estimació específica. | Aquest valor per defecte és el detall de la línia d'oferta relacionada per al cost que es crea automàticament. |
| Classe de la transacció | Creació ràpida | Aquesta llista desplegable proporciona les classes de transacció que s'inclouen a la pestanya **General** de la línia d'oferta basada en projectes.  | Aquest valor per defecte és el detall de la línia d'oferta relacionada per al cost que es crea automàticament. |
| Seleccioneu el producte | Creació ràpida | S'aplica quan la classe de transacció és **Material**. Podeu seleccionar d'especificar que aquesta línia de previsió és per a un producte **Existent** (catàleg) o un producte **Fora de catàleg**. | Aquest valor per defecte és el detall de la línia d'oferta relacionada per al cost que es crea automàticament. |
| Producte | Creació ràpida | L'identificador del producte del catàleg de productes. Aquest camp només està habilitat si seleccioneu **Existent** al camp **Seleccioneu un producte**. L'ID s'utilitza per recuperar el preu de venda de la llista de preus del projecte a l'oferta. | Aquest valor per defecte és el detall de la línia d'oferta relacionada per al cost que es crea automàticament. |
| Producte fora de catàleg | Creació ràpida | Quadre de text on cal escriure el nom del producte. Aquest camp només està habilitat si seleccioneu **Fora de catàleg** al camp **Seleccioneu un producte**.| Aquest valor per defecte és el detall de la línia d'oferta relacionada per al cost que es crea automàticament. |
| Funció | Creació ràpida | Funció de la persona que durà a terme aquesta feina o que incorri en aquesta despesa. | Aquest valor per defecte és el detall de la línia d'oferta relacionada per al cost que es crea automàticament. |
| Categoria | Creació ràpida | Categoria del treball o despesa. | Aquest valor per defecte és el detall de la línia d'oferta relacionada per al cost que es crea automàticament. |
| Data d’inici | Creació ràpida | Data d'inici del treball. | Aquest camp pren per defecte el valor del detall de la línia d'oferta relacionada per al cost que es crea automàticament. |
| Data d’acabament | Creació ràpida | Data de finalització del treball. | Aquest camp pren per defecte el valor del detall de la línia d'oferta relacionada per al cost que es crea automàticament. |
| Unitat de recursos | Creació ràpida | Unitat de proveïment que incorrerà en aquest cost i que proporciona el recurs per treballar-hi. | Aquest valor per defecte és el detall de la línia d'oferta relacionada per al cost que es crea automàticament i s'utilitza en la recuperació del preu de cost. |
| Planificació d'unitat | Creació ràpida | Grup d'unitats del treball, el producte o la despesa. Les unitats pertanyen a una planificació d'unitat o a un grup d'unitats. Per exemple, les milles i els kilòmetres són unitats que pertanyen a un grup d'unitats que descriuen la distància. | Aquest valor per defecte és el detall de la línia d'oferta relacionada per al cost que es crea automàticament. |
| Unitat | Creació ràpida | La unitat del treball, el producte o la despesa. | Aquest valor per defecte és el detall de la línia d'oferta relacionada per al cost que es crea automàticament. |
| Quantitat | Creació ràpida | La quantitat de treball, producte o despesa. | Aquest valor per defecte és el detall de la línia d'oferta relacionada per al cost que es crea automàticament. |
| Preu unitari | Creació ràpida |Percentatge de facturació de la funció que està realitzant la feina, el preu unitari del producte o el preu de venda de la categoria de producte o despesa. El valor per defecte d'aquest camp és **Temps** a partir de la combinació dels valors de dimensió de preus de la línia de preu de la funció de la llista de preus del projecte que sigui efectiva per a la data d'inici. Per a les **Despeses**, el valor per defecte és la configuració de preus de la categoria de transaccions de la llista de preus del projecte efectiva per a la data d'inici. Si el mètode de càlcul de preus de la categoria de transaccions no és el preu unitari, no hi ha cap valor per defecte i aquest camp es deixa en blanc. Per als productes, el valor per defecte es basa en la línia **Element de la llista de preus** de la llista de preus del projecte efectiva per a la data d'inici.| Percentatge de cost de la funció que està realitzant la feina, el cost unitari de la categoria de despeses o el cost unitari del producte. El valor per defecte d'aquest camp és **Temps** a partir de la combinació dels valors de dimensió de preus de la línia de preu de la funció de la llista de preus del projecte que sigui efectiva per a la data d'inici. Per a les **Despeses**, el valor per defecte és la configuració de preus de la categoria de transaccions de la llista de preus del projecte efectiva per a la data d'inici. Si el mètode de càlcul de preus de la categoria de transaccions no és el preu unitari, no hi ha cap valor per defecte i aquest camp es deixa en blanc. Per als productes, el valor per defecte es basa en la línia **Element de la llista de preus** de la llista de preus del projecte efectiva per a la data d'inici.|
| Impost estimat | Creació ràpida | Podeu introduir manualment l'impost previst per a aquesta feina o despesa. | No hi ha cap impacte descendent d'aquest camp. |
| Import | Creació ràpida | Podeu introduir informació manualment en aquest camp si els camps **Quantitat** i **Preu** es deixen en blanc. Si aquests camps no estan en blanc, aquest camp és només de lectura i es calcula com a (Quantitat \* Preu per unitat) + Impost. | No hi ha cap impacte descendent d'aquest camp. |


## <a name="update-prices-on-quote-line-details"></a>Actualitzar els preus dels detalls de la línia d'oferta

Si heu canviat els preus de la llista de preus del projecte adjuntada a l'oferta o a la llista de preus de cost de la unitat de contracte, podeu seleccionar **Torna a calcular** a la pàgina **Oferta** per actualitzar els preus dels detalls de la línia d'oferta individual per reflectir aquest canvi. Quan seleccioneu **Torna a calcular**, apareix un advertiment que us informa que els preus dels detalls de la línia d'oferta per a totes les línies d'oferta d'aquesta oferta es restabliran. Seleccioneu **Sí** per actualitzar els preus dels detalls de la línia de vendes i d'oferta de costos.

## <a name="access-quote-line-details-for-cost"></a>Accedir als detalls de la línia d'oferta per al cost

A la pestanya **Detalls de la línia d'oferta**, seleccioneu una fila a la quadrícula per habilitar algunes accions a la barra d'eines de la subquadrícula. La primera acció a la barra d'eines de la subquadrícula quan se selecciona un detall de línia d'oferta és **Obre el detall de cost**. Seleccioneu **Obre els detalls del cost** per veure la tarifa de costos i la quantitat relacionada d'aquesta línia d'oferta.

> [!NOTE]
> Si canvieu la unitat, la quantitat, les dates, la funció o els valors de categoria del detall de la línia d'oferta per al cost, canviaran els valors corresponents als detalls de la línia d'oferta.
## <a name="currency-on-quote-line-details-for-cost-and-sales"></a>Moneda als detalls de la línia d'oferta per al cost i les vendes

La moneda del detall de la línia d'oferta per a les vendes es pren per defecte de la llista de preus del projecte aplicable a la data d'inici del detall de la línia d'oferta.

La moneda del detall de la línia d'oferta per al cost es pren per defecte de la llista de preus de la unitat contractant de l'oferta aplicable a la data d'inici del detall de la línia d'oferta.

Els càlculs de rendibilitat converteixen l'import en els detalls de la línia d'oferta per al cost i les vendes a la moneda base de l'entorn per informar del marge previst global de l'oferta.

> [!NOTA
> > Podrien ocórrer errors d'arrodoniment de moneda i canvis de marges a causa de la manca de tipus de canvi amb data d'efectivitat. Utilitzeu aquests càlculs només als contractes de projecte, ja que són aproximacions i no són per a l'ús reglamentari real ni per a altres informes que requereixin una major precisió d'arrodoniment i coneixement de la data de vigència dels tipus de canvi.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
