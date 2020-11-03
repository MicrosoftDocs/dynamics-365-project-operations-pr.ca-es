---
title: Estimació d'una línia d'oferta basada en projectes
description: En aquest tema es proporciona informació sobre com crear una estimació en una línia d'oferta basada en projectes.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 65aee7238781ac90f603e57c6d9b0b92cabd6644
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072116"
---
# <a name="estimating-a-project-based-quote-line"></a>Estimació d'una línia d'oferta basada en projectes

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

Una línia d'oferta basada en projectes conté detalls que ajuden a estimar el cost i els possibles ingressos del treball implicat per lliurar la línia d'oferta.

Per estimar una línia d'oferta basada en projectes, a la línia d'oferta basada en projectes, seleccioneu la pestanya **Detalls de la línia d'oferta**. Hi ha dues maneres de crear una estimació en una línia d'oferta basada en projectes:

- Crear manualment l'estimació directament a la línia d'oferta mitjançant els detalls de la línia d'oferta 
- Crear un projecte i un pla de projecte i, a continuació, associar el projecte i les tasques del projecte a la línia d'oferta. El procés per importar les estimacions del pla del projecte a la línia d'oferta segons la informació que heu facilitat s'habilitarà.

## <a name="create-estimates-directly-on-a-project-based-quote-line"></a>Creació d'estimacions directament en una línia d'oferta basada en projectes

Per crear una estimació en una línia d'oferta basada en projectes, seleccioneu la pestanya **Detalls de la línia d'oferta**. L'element de línia que creeu en aquesta pestanya resumirà el valor ofert per a aquesta línia d'oferta. 

Per crear detalls de la línia d'oferta, seleccioneu **+ Detall nou de la línia d'oferta** a la subquadrícula **Detalls de la línia d'oferta**. S'obrirà un control lliscant de creació ràpida. Els camps següents del formulari **Línia d'oferta** :

| **Camp** | **Ubicació** | **Rellevància, propòsit i orientació** | **Impacte descendent** |
| --- | --- | --- | --- |
| Descripció | Creació ràpida | Descripció de l'estimació específica. | Aquest camp canvia per defecte al detall de la línia d'oferta relacionada per al cost que es crea automàticament. |
| Classe de la transacció | Creació ràpida | Aquesta llista desplegable proporciona les classes de transacció que s'inclouen a la pestanya **General** de la línia d'oferta basada en projectes.  | Aquest camp canvia per defecte al detall de la línia d'oferta relacionada per al cost que es crea automàticament. |
| Funció | Creació ràpida | Persona que realitzarà aquesta feina o incorrerà aquesta despesa. | Aquest camp canvia per defecte al detall de la línia d'oferta relacionada per al cost que es crea automàticament. |
| Categoria | Creació ràpida | Categoria del treball o despesa. | Aquest camp canvia per defecte al detall de la línia d'oferta relacionada per al cost que es crea automàticament. |
| Data d’inici | Creació ràpida | Data d'inici del treball. | Aquest camp canvia per defecte al detall de la línia d'oferta relacionada per al cost que es crea automàticament. |
| Data d’acabament | Creació ràpida | Data de finalització del treball. | Aquest camp canvia per defecte al detall de la línia d'oferta relacionada per al cost que es crea automàticament. |
| Unitat de recursos | Creació ràpida | Unitat de recursos que incorrerà en aquest cost i proporcionarà el recurs per treballar-hi. | Aquest camp canvia per defecte al detall de la línia d'oferta relacionada per al cost que es crea automàticament. Aquest camp també s'utilitza a la recuperació de preus de cost. |
| Planificació d'unitat | Creació ràpida | Grup d'unitats del treball o de la despesa. Les unitats pertanyen a una planificació d'unitat o a un grup d'unitats. Per exemple, les milles i quilòmetres són unitats que pertanyen a un grup d'unitats que descriu la distància. | Aquest camp canvia per defecte al detall de la línia d'oferta relacionada per al cost que es crea automàticament. |
| Unit | Creació ràpida | Unitat del treball o de la despesa. | Aquest camp canvia per defecte al detall de la línia d'oferta relacionada per al cost que es crea automàticament. |
| Quantitat | Creació ràpida | Quantitat del treball o de la despesa | Aquest camp canvia per defecte al detall de la línia d'oferta relacionada per al cost que es crea automàticament. |
| Preu per unitat | Creació ràpida | Tarifa de facturació de la funció que duu a terme el treball o el preu de venda de la categoria de despeses. Aquest camp per defecte es basa en el temps en la combinació de funció i unitat de recursos a la llista de preus del projecte aplicable a la data d'inici. Per a les despeses, aquest camp és per defecte la configuració de preus de la categoria de la transacció a la llista de preus del projecte aplicable a la data d'inici. Si el mètode de càlcul de preus de la categoria transacció no és de preu per unitat, no hi ha cap valor per defecte i aquest camp es deixa en blanc. | Tarifa de cost de la funció que duu a terme el treball o el cost per unitat de la categoria de despeses. Aquest camp per defecte es basa en el temps en la combinació de funció i unitat de recursos al preu de la unitat contractant de la llista de preus d'oferta aplicable a la data d'inici. Per a les despeses, aquest camp és per defecte la configuració de preus de la categoria de la transacció a la llista de preus de cost de la unitat contractant aplicable a la data d'inici. Si el mètode de càlcul de preus de la categoria transacció no és de preu per unitat, no hi ha cap valor per defecte i aquest camp es deixa en blanc. |
| Impost estimat | Creació ràpida | Podeu introduir manualment l'impost previst per a aquesta feina o despesa. | No hi ha cap impacte descendent d'aquest camp. |
| Import | Creació ràpida | Podeu introduir informació manualment en aquest camp si els camps **Quantitat** i **Preu** es deixen en blanc. Si aquests camps no estan en blanc, aquest camp és només de lectura i es calcula com a (Quantitat \* Preu per unitat) + Impost. | No hi ha cap impacte descendent d'aquest camp. |

## <a name="update-prices-on-quote-line-details"></a>Actualitzar els preus dels detalls de la línia d'oferta

Si heu canviat els preus de la llista de preus del projecte vinculada a l'oferta o a la llista de preu de cost de la unitat de contractant, podeu seleccionar **Torna a calcular** a la pàgina **Oferta** per actualitzar els preus dels detalls de la línia d'oferta individual per reflectir aquest canvi. Quan se selecciona **Torna a calcular** , es produeix un advertiment que us informa que els preus dels detalls de la línia d'oferta de totes les línies d'oferta d'aquesta oferta es restabliran. Seleccioneu **Sí** per actualitzar els preus dels detalls de la línia de vendes i d'oferta de costos.

## <a name="access-quote-line-details-for-cost"></a>Accedir als detalls de la línia d'oferta per al cost

A la pestanya **Detalls de la línia d'oferta** , seleccioneu una fila a la quadrícula per habilitar algunes accions a la barra d'eines de la subquadrícula. La primera acció de la barra d'eines de la subquadrícula quan se selecciona un detall de la línia d'oferta és **Obre els detalls del cost**. Seleccioneu **Obre els detalls del cost** per veure la tarifa de costos i la quantitat relacionada d'aquesta línia d'oferta.

> [!NOTE]
> Si canvieu la unitat, la quantitat, les dates, la funció o els valors de categoria del detall de la línia d'oferta per al cost, canviaran els valors corresponents als detalls de la línia d'oferta.
## <a name="currency-on-quote-line-details-for-cost-and-sales"></a>Moneda als detalls de la línia d'oferta per al cost i les vendes

La moneda del detall de la línia d'oferta per a les vendes es pren per defecte de la llista de preus del projecte aplicable a la data d'inici del detall de la línia d'oferta.

La moneda del detall de la línia d'oferta per al cost es pren per defecte de la llista de preus de la unitat contractant de l'oferta aplicable a la data d'inici del detall de la línia d'oferta.

Els càlculs de rendibilitat converteixen l'import en els detalls de la línia d'oferta per al cost i les vendes a la moneda base de l'entorn per informar del marge previst global de l'oferta.

Això podria comportar els errors d'arrodoniment de moneda i marges canviants per la manca de la data de tipus de canvi efectiu. Utilitzeu aquests càlculs a les ofertes de projecte només com a aproximacions i no valors legals reals o altres informes que requereixin una major precisió d'arrodoniment i presa de consciència de la data d'efectivitat dels tipus de canvi.
