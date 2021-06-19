---
title: Anàlisi de les ofertes del projecte
description: En aquest tema es proporciona informació sobre l'anàlisi de les ofertes del projecte.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: acb3f1a2020cfd59f60f828e9092bd7ccde00077
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012439"
---
# <a name="analysis-of-project-quotes"></a>Anàlisi de les ofertes del projecte

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

El Dynamics 365 Project Service Automation analitza les ofertes de projectes per estimar la rendibilitat. També analitza la manera com s'alinea l'oferta amb les expectatives del client sobre la data d'entrega o de finalització i sobre el pressupost.

## <a name="profitability-analysis"></a>Anàlisi de rendibilitat

El Project Service Automation analitza la rendibilitat mitjançant el marge brut i el marge brut ajustat.

- Els marges bruts es calculen mitjançant la fórmula següent:

  `
    (Sum of estimated chargeable sales value – Sum of estimated chargeable costs) x 100
  `
- El marge brut ajustat es calcula mitjançant la fórmula següent:

  `
    (Sum of estimated chargeable sales value – Sum of all estimated costs) x 100
  `

Si els valors del marge brut i el marge brut ajustat difereixen per un marge ampli, gran part del treball de l'oferta es classifica com a de no-pagament.

## <a name="analysis-of-customer-expectations"></a>Anàlisi de les expectatives del client

Podeu analitzar ofertes i generar gràfics per a les expectatives de client sobre la planificació i el pressupost si introduïu valors per als camps següents:

- Camp **Data de lliurament sol·licitada** a la capçalera de l'oferta.
- Camp **Pressupost de client** per a cada línia d'oferta (per a les línies basades en el projecte i les línies basades en productes).

L'anàlisi de les expectatives dels clients sobre la planificació es fa comparant l'última data d'acabament del detall de la línia d'oferta amb la data de lliurament sol·licitada a totes les línies d'oferta de l'oferta.

L'anàlisi de les expectatives dels clients sobre el pressupost es fa comparant la suma del pressupost total de clients amb l'import de la cotització a totes les línies d'oferta.


[!INCLUDE[footer-include](../includes/footer-banner.md)]