---
title: Configuració de les tarifes de cost i de vendes per a les despeses
description: Aquest article proporciona informació sobre com configurar les tarifes de cost i de venda per a les categories de transaccions i despeses.
author: rumant
ms.date: 04/07/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c503230348750af246f6ee7a4af1176d7bf22ba4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911860"
---
# <a name="set-up-cost-and-sales-rates-for-expenses"></a>Configuració de les tarifes de cost i de vendes per a les despeses

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

Podeu configurar els preus de cost i de venda per a categories de transaccions al Dynamics 365 Project Operations. Atès que els preus de cost i venda estan dissenyats per a les despeses, cada categoria de transacció que els inclou també ha d'establir-se com a categoria de despeses. Aquesta configuració assegura la precisió de la funcionalitat descendent. Els preus de cost i venda per a les categories de transaccions només es poden indicar en una moneda, que ha de ser la moneda de la capçalera de la llista de preus.

Per configurar les tarifes de cost i venda per a les categories de transacció, completeu els passos següents. 

1. Aneu a **Vendes** > **Clients** > **Llistes de preus**.
2. Seleccioneu **Crea** per crear una llista de preus nova. 
3. Als **Preus per categoria**, en el menú de la subquadrícula, seleccioneu **Preu per categoria nou**. 
4. A la pàgina **Creació ràpida**, introduïu la categoria de transacció i la unitat per la qual esteu creant el nou preu.

La taula següent indica els camps de la pestanya **General** i la pàgina **Creació ràpida** d'una línia de preu de categoria que haureu de tenir en compte quan creeu preus de categoria en una llista de preus de vendes o de cost.

| Camp | Location | Descripció | Impacte descendent |
| --- | --- | --- | --- |
| Categoria de transacció | Pestanya **General** i pàgines **Creació ràpida** | Seleccioneu la categoria de transacció per a la qual esteu creant un preu de venda o cost. | La categoria de transacció de l'estimació o el valor real d'entrada coincidirà amb aquesta línia per defecte per obtenir la tarifa de cost o de venda per defecte de la categoria de transacció. |
| Planificació d'unitat | Pestanya **General** i pàgines **Creació ràpida** | La planificació de la unitat per defecte és la planificació de la categoria de la transacció. | No hi ha cap impacte descendent d'aquest camp. |
| Unit | Pestanya **General** i pàgines **Creació ràpida** | Seleccioneu la unitat per a la qual s'estan configurant les tarifes. | La unitat de l'estimació o valor real d'entrada es fa coincidir amb la unitat d'aquesta línia per prendre per defecte la tarifa de l'estimació o valor real de la despesa. |
| Mètode de càlcul de preus | Pestanya **General** i pàgines **Creació ràpida** | Els valors possibles del camp **Mètode de preus** són **Preu per unitat**, **per cost** i **Marge comercial sobre el cost**. | Durant la configuració del preu, seleccionar **Preu per unitat** bloqueja el camp **Percentatge** a la línia de preus de la categoria. Si se selecciona **Per cost**, els camps **Preu** i **Percentatge** estan bloquejats a la llista de preus de venda. Seleccionar **Marge comercial sobre el cost** bloqueja el camp **Preu** a la llista de preus de venda. En una línia de valor real d'entrada per a despeses, el mètode de preus **Per cost** o **Marge comercial sobre el cost** dona com a resultat que a la línia de vendes no facturada corresponent se li assigna un preu que és igual al preu en el valor real de cost o es calcula com a marge comercial sobre el preu. |
| Preu | Pestanya **General** i pàgines **Creació ràpida** | Configureu una tarifa per unitat per a la categoria de transacció i la combinació d'unitats. Per exemple, la tarifa de quilometratge és de 10 dòlars per milla i 8 USD per quilòmetre. | La tarifa de quilometratge serà la tarifa per defecte en el preu per unitat o el cost de la línia d'estimació o valor real per a una classe de transacció de despesa.|
| Percentatge | Pestanya **General** i pàgines **Creació ràpida** | Configureu un percentatge sobre el cost per a la combinació de categoria de transacció i unitat. Per exemple, la tarifa de venda de les tarifes aeroportuàries hauria d'estar un 10% per sobre del cost de les despeses de tarifes aeroportuàries incorregudes. | Aquest percentatge sobre el cost només és aplicable en una llista de preus de venda quan el mètode de preus seleccionat és **Marge comercial sobre el cost**. |
| Moneda | Pestanya **General** i pàgines **Creació ràpida** | Per defecte, aquest valor prové de la moneda de la capçalera de la llista de preus. Per als preus de la categoria de transaccions, la moneda no es pot substituir. | Aquesta moneda per defecte és el preu per unitat de la línia real entrant per a la classe de transacció de despesa per a cost i vendes. |

## <a name="pricing-methods-for-expenses"></a>Mètodes de preus per a despeses

Quan configureu preus per categoria que només són rellevants en el context dels preus de despesa, podeu utilitzar un dels següents tres mètodes de preus:

- **Preu per unitat**
- **A partir del cost**
- **Marge comercial sobre el cost**

### <a name="price-per-unit"></a>Preu per unitat
Quan se selecciona aquest mètode de preus en una línia de preu per categoria que està vinculada a una llista de preus de venda, el preu per defecte és el de la combinació de categoria i unitat tant en l'estimació com en el valor real. Estimació fa referència a les línies d'estimació del projecte per a les despeses, el detall de la línia d'oferta i el detall de la línia de contracte per a les despeses.

### <a name="at-cost"></a>A partir del cost
Quan se selecciona aquest mètode de preus en la línia de preus de categoria que està vinculada a una llista de preus de venda, el preu per defecte és el de la combinació de categoria i unitat només per al valor real de despesa. Per exemple, els valors reals de vendes no facturades per a la classe de transacció de despeses. El preu unitari està establert en el valor real de vendes no facturades a partir del preu unitari en el valor real de cost per a aquesta despesa. Els preus per defecte basats en el cost no es produeixen en les estimacions del projecte de despeses o en els detalls de la línia d'oferta i la línia de contracte per a les despeses.

### <a name="markup-over-cost"></a>Marge comercial sobre el cost
Quan se selecciona aquest mètode de preus en la línia de preus de categoria que està vinculada a una llista de preus de venda, el preu per defecte és el de la combinació de categoria i unitat només per a un valor real de despesa. Per exemple, els valors reals de vendes no facturades per a la classe de transacció de despeses. Aquest preu unitari s'estableix en el valor real de vendes no facturades a un valor calculat a partir del preu unitari en el valor real de cost per a aquesta despesa després d'aplicar-hi el percentatge de marge comercial definit. Els preus per defecte basats en el cost no es produeixen en les estimacions del projecte de despeses o en els detalls de la línia d'oferta i la línia de contracte per a les despeses.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
