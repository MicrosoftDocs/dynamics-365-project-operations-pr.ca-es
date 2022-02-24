---
title: Configuració de plantilles de costos
description: Aquest tema proporciona informació sobre com crear i utilitzar plantilles de costos a Project Operations.
author: sigitac
manager: tfehr
ms.date: 11/18/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 786b2b9b140f82d406044c2ed05761d7f46ee9e0
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642711"
---
# <a name="set-up-cost-templates"></a>Configuració de plantilles de costos

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_


Aquest tema proporciona informació sobre com crear i utilitzar plantilles de costos a Project Operations. Una plantilla de costos determina:

- Les categories de projectes per a la predicció i les transaccions reals que s'inclouran en un percentatge del càlcul de compleció del projecte. El valor de percentatge complet s'utilitza després per calcular la quantitat d'ingressos que es reconeixerà.
- Si el percentatge de compleció es pot modificar si s'ha calculat automàticament.
- Si el percentatge completat es calcula a partir de quantitats o unitats.

## <a name="cost-template-example"></a>Exemple de plantilla de costos

Esteu treballant en un projecte de disseny de pàgines web per a un client en el qual cobreu una tarifa plana de 10.000 USD. Preveieu que trigareu 100 hores (5.000 USD) a completar el projecte. També preveieu dos bitllets d'avió i quatre nits en un hotel per als viatges a la seu del client (1.800 USD). Això resulta en un cost total de la previsió de 6.800 USD.

Quan executeu el procés de reconeixement d'ingressos de preu fix per crear una estimació a final de mes, trobeu que heu treballat 35 hores en el projecte. Això encara no inclou els vols ni els costos de l'Hotel. També vau tenir un assistent que va dur a terme cinc hores d'investigació per al projecte a un cost de 100 USD, que no havíeu planificat.

Quan calculeu el valor de percentatge completat d'aquest projecte, teniu les opcions següents:

- Voleu incloure tots els costos (hores i despeses) o només les hores?
- Voleu incloure totes les hores o només les hores planificades?
- Voleu calcular el percentatge completat en funció del cost en dòlars de les hores planificades (5.000 USD) o només el nombre d'hores (100)?

Les respostes a aquestes preguntes determinen les opcions que definiu a la plantilla de costos i les categories que seleccioneu a les línies de la plantilla de costos.

A la taula següent s'il·lustren els resultats de diferents mètodes per calcular el valor de percentatge completat per a aquest escenari.

| Compleció basada en | Cost en dòlars o unitats | Percentatge completat | Càlcul |
| --- | --- | --- | --- |
| Totes les hores, sense despeses | Cost en dòlars | 37% 35 x 50 USD + 100 USD = 1.850 USD 1.850 USD/5.000 USD |
| Totes les hores, sense despeses | Unitats | 40% | 40 hores/100 hores (incloent-hi cinc hores no planificades) |
| Hores planificades, sense despeses | Cost en dòlars o unitat | 35% | 35/100 hores o 35 x 50/5.000 USD |
| Totes les hores i despeses | Cost en dòlars | 27.2% | 1.850 USD/6.800 USD |

Decidir quin enfocament utilitzar per crear una plantilla de costos pot dependre de diverses consideracions:

- Si incloeu hores no planificades a la plantilla de costos, us arrisqueu a assolir el 100 per cent d'abans que el projecte hagi finalitzat. Això es deu a que les hores reals seran majors que les hores planificades. Si utilitzeu qualsevol dels dos primers mètodes que s'enumeren a la taula, hauríeu de canviar el pla (unitats previstes) quan us adoneu de les desviacions. En aquest cas, afegireu o restareu hores basant-vos en els vostres coneixements sobre el que cal per acabar el projecte. Si el projecte requereix que s'hi destinin 65 hores més, haureu d'afegir cinc hores al pla per a un total de 105. Si sabeu que el vostre assistent farà cinc hores més de recerca, el total serà de 110 hores.
- Si utilitzeu el tercer mètode indicat a la taula, només s'actualitzaran les hores planificades per al vostre propi temps per mantenir la precisió del càlcul del percentatge completat. La vostra rendibilitat canviarà quan es registrin les hores no planificades, però es mantindrà en una trajectòria coneguda per un percentatge completat.
- Si utilitzeu el quart mètode indicat a la taula, el perill és que les despeses es produeixin en moments irregulars i que no es reflecteixin en el vostre progrés de compleció. Per tant, si s'inclouen les despeses, poden provocar que el percentatge completat fluctuï més del que és desitjable. Per exemple, com que encara no heu fet cap vol, el percentatge completat és del 27 per cent en comptes del 35 per cent o el 37 per cent si baseu el càlcul només en el temps. Si haguéssiu fet un viatge de dues nits i haguéssiu previst el vol i els costos de l'Hotel amb precisió, el percentatge completat seria del 40,4 per cent (1.850 USD per al treball i 900 USD per a les despeses = 2.750 USD/6.800 USD = 40,4 per cent). Per tant, en incórrer en les despeses d'un sol viatge en avió canviarà el percentatge completat del 27 per cent al 40 per cent.

## <a name="create-cost-templates"></a>Crear plantilles de costos
Per crear plantilles de costos, seguiu aquests passos:

1. Per accedir a les plantilles de costos, a l'entorn del Dynamics 365 Finance, aneu a **Administració de projectes i comptabilitat** > **Configuració** > **Estimacions** > **Plantilla de costos**.
2. Seleccioneu **Crea** per crear una plantilla de costos nova. Introduïu un nom i una descripció.
3. Proporcioneu l'identificador de la línia de cost per a cada tipus de transacció.
4. Seleccioneu un mètode de compleció per defecte:

  - **Automàtic** : el percentatge completat es calcula automàticament en un projecte. El valor resultant no es pot canviar.
  - **Manual** : el percentatge completat es calcula automàticament en un projecte. El valor resultant es pot canviar.

  > [!NOTE]
  > Per als càlculs manuals, el percentatge completat es manté a **Càlcul manual** a la pestanya **General** de la pàgina **Estimació**.

5. A **Compleció basada en**, seleccioneu un dels valors següents:

  - **Import**: l'import de la moneda comptable calcula el percentatge completat.
  - **Unitat**: la quantitat calcula el percentatge completat.
  - **Línia recta**: el sistema calcula el percentatge completat de manera proporcional utilitzant les dates d'inici i d'acabament del projecte per determinar la durada del projecte.

6. Seleccioneu **Línies de cost** per revisar les línies de cost de la plantilla de costos. Cal com a mínim una línia de cost per a cada tipus de transacció. No obstant, podeu crear diverses línies de cost per als mateixos tipus de transaccions i definir els atributs desitjats per a aquestes línies.
7. A la pestanya **Categories**, seleccioneu les categories del projecte que voleu incloure a la línia de la plantilla de costos.
8. A la pestanya **General**, seleccioneu si aquesta línia s'inclourà en el càlcul del percentatge completat.
9. Seleccioneu el mètode de cost per completar que s'ha d'utilitzar per calcular el percentatge completat.
