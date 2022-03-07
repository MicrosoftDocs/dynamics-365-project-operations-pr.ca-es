---
title: Escenaris multidivisa (versió 3.x)
description: Aquest tema proporciona informació sobre els escenaris multidivisa.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 12/26/2018
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
ms.openlocfilehash: 89a91cf3dbbcf81dbb089ee88c8c177c73afb694914ca7d95eae96776d38abed
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "7005109"
---
# <a name="multiple-currency-scenarios"></a>Escenaris multidivisa

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

El Microsoft Dynamics 365 té dos conceptes de moneda:

- **Moneda de transacció**: la moneda en què es produeix una transacció. 
- **Moneda base**: la moneda de la instància del Dynamics 365. Aquesta moneda es configura quan es proveeix una instància del Dynamics 365. No es pot canviar.

Per exemple, Contoso US va vendre 100 samarretes a un client del Regne Unit per 15 lliures esterlines (GBP) cadascuna. A la taula següent es mostra com s'enregistra aquesta transacció a l'entitat Producte de la comanda.

| Producte | Quantitat | Preu per unitat | Moneda | Import | Tipus de canvi | Preu per unitat (base)| Import (base)|
|---------|----------|----------------|----------|--------|---------------|----------------------|--------------|
| Samarreta | 100      | 15             | GBP      | 1500   | 0.94          | 17,25 USD               | 1.725 USD       |

A la columna **Moneda** es mostra la moneda de la transacció, la qual és la moneda en què es produeix la venda. La columna **Tipus de canvi** és el tipus de canvi entre la moneda de la transacció i la moneda base. La moneda base són els dòlars dels EUA (USD). Aquesta moneda base va es configurar en proveir la instància del Dynamics 365.
A mesura que es mostra la taula, cada transacció es registra tant en la moneda de la transacció com en la moneda base. El Dynamics 365 utilitza el tipus de canvi de moneda per calcular els imports de moneda base.

## <a name="project-service-automation-extensions"></a>Extensions del Project Service Automation

El Dynamics 365 Project Service Automation influeix en la moneda de la transacció, perquè les transaccions empresarials solen tenir dos aspectes: cost i vendes.

Les entitats següents es consideren transaccions empresarials:

- Detall de la línia d'oferta
- Detall de la línia de contracte del projecte
- Línia d'estimació
- Línia del llibre diari
- Detall de la línia de factura
- Real

A cadascuna d'aquestes entitats, hi ha un registre que representa l'import del cost o l'import de les vendes. Pel que fa a qualsevol entitat del Dynamics 365 que tingui un camp **Import**, cada registre inclou imports tant en la moneda de la transacció com en la moneda base. 

El PSA amplia el concepte de moneda de transacció per al cost i les vendes de les maneres següents:

- La moneda de transacció de costos per a transaccions de temps sempre prové de la moneda de la unitat organitzativa propietària o administradora del projecte. Aquesta unitat organitzativa es coneix com a unitat de contractació.
- La moneda de transacció de vendes d'operacions de temps i de despesa sempre prové de la moneda del contracte del projecte.
- La moneda de transacció de costos per a les despeses prové de la moneda en què es va crear l'entrada de la despesa.

## <a name="multiple-currency-scenario"></a>Escenari multidivisa

En aquesta secció es descriu un exemple d'un projecte que Contoso UK lliura a un client que s'anomena Fabrikam, Japó. Així és com s'ha configurat l'escenari:

1. GBP i el ien japonès (JPY) es configuren a **Configuració** \> **Administració empresarial** \> **Monedes**. 
2. Un compte de client que es diu **Fabrikam - Japó** està configurat i el JPY se selecciona com a moneda del compte.
3. Es configura una unitat organitzativa anomenada **Contoso UK** i GBP se selecciona com a moneda.
4. Es crea un contracte de projecte, on **Contoso UK** s'especifica com a unitat de contractació i **Fabrikam – Japó** s'especifica com a client.
5. Es creen línies de contracte de projecte, basades en els arranjaments de facturació de les diferents classes de transaccions en el projecte, com ara la facturació per temps versus la facturació per despeses.
6. Es crea un projecte on s'especifica **Contoso UK** com a unitat de contractació. Aquest projecte es crea i s'assigna a les línies de contracte del projecte.


Durant l'estimació que utilitza el detall de la línia d'oferta, el detall de la línia de contracte del projecte o la línia d'estimació de la planificació, dos registres es creen sempre a l'entitat. Un registre és per al cost i l'altre registre és per a les vendes.

- Per defecte, la moneda de transacció del registre de cost es defineix en la moneda de la unitat de contractació del projecte. En aquest exemple, la moneda és GBP.
- Per defecte, la moneda de transacció del registre de vendes es defineix en la moneda del contracte del projecte. En aquest exemple, la moneda és JPY.

Quan es creen valors reals de temps mitjançant una entrada de temps o la línia del llibre diari, es produeix el comportament següent:

- Per defecte, la moneda de transacció del registre de cost es defineix en la moneda de la unitat de contractació del projecte.
- Per defecte, la moneda de transacció del registre de vendes es defineix en la moneda del contracte del projecte.

Quan es creen valors reals de despeses mitjançant una entrada de despeses o línia del llibre diari, es produeix el comportament següent:

- Podeu registrar l'import de la despesa en qualsevol moneda. Seleccioneu la moneda mitjançant el selector de moneda de la pàgina **Entrada de despeses** o la pàgina **Línia del llibre diari**. Per defecte, la moneda de transacció del registre de costos es defineix en la moneda de l'entrada de despeses. 
- Per defecte, la moneda de transacció del registre de vendes és la moneda del contracte del projecte. Per definir aquesta moneda, el sistema converteix primer l'import de la transacció en la moneda que l'usuari ha introduït a la moneda base. A continuació, converteix l'import a la moneda del contracte del projecte. 

### <a name="computing-roll-ups-when-project-actuals-are-recorded-in-multiple-transaction-currencies"></a>Calcular valors consolidats quan es registren valors reals en diverses monedes de transacció

El Dynamics 365 gestiona automàticament els valors consolidats d'imports en diferents monedes. Aquest és un exemple.

| Classe de la transacció | Tipus de transacció| Date   | Recurs | Categoria de la transacció | Quantitat | Preu per unitat | Import      | Tipus de canvi | Import en base |
|-------------------|------------------|--------|----------|----------------------|----------|--------------|-------------|---------------|----------------|
| Time              | Vendes no facturades   | 14 de juny | Eudald  |                      | 8 h    | 20.000 JPY    | 160.000 JPY | 123           | 1.300,81 USD    |
| Time              | Vendes no facturades   | 15 de juny | Eudald  |                      | 8 h    | 20.000 JPY    | 160.000 JPY | 123           | 1.300,81 USD    |
| Despesa           | Vendes no facturades   | 16 de juny | Eudald  | Hotels                | 1 EA     | 250 EUR      | 250 EUR     | 0.94          | 265,95 USD     |
| Despesa           | Vendes no facturades   | 17 de juny | Eudald  | Lloguer de cotxes           | 1 EA     | 150 EUR      | 150 EUR     | 0.94          | 159,57 USD     |

Per calcular el valor total de les vendes no facturades al projecte, podeu crear un camp de valor consolidat per al camp **Import** a tots els valors reals de vendes no facturades. El camp de valor consolidat és una construcció del Dynamics 365 que permet fórmules ràpides als registres relacionats.


[!INCLUDE[footer-include](../includes/footer-banner.md)]