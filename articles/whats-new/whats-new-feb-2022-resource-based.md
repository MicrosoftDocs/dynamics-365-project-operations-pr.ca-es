---
title: 'Novetats de febrer de 2022: Project Operations per a escenaris basats en recursos/no mantinguts en existències'
description: Aquest article proporciona informació sobre les actualitzacions de qualitat que estan disponibles en el llançament de febrer de 2022 del Project Operations per a escenaris de recursos/sense existències.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b036c0a3c39c52cb15277293679ef88906cae2c4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932974"
---
# <a name="whats-new-february-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novetats de febrer de 2022: Project Operations per a escenaris basats en recursos/no mantinguts en existències

*S'aplica a: Project Operations per a escenaris basats en recursos/sense cotització*

Aquest article s'aplica als components i les versions següents del Microsoft Dynamics 365 Project Operations:

- Project Operations en un entorn del Dataverse, versió 4.28.0.120
- Administració de projectes i comptabilitat en un entorn del Dynamics 365 Finance, versió 10.0.24

## <a name="features-included-in-this-release"></a>Característiques incloses en aquesta versió

- A partir d'aquesta versió, podeu afegir fins a 300 membres de l'equip a un únic projecte. Anteriorment, el límit pel que fa al nombre de membres de l'equip era de 150. Per obtenir més informació, vegeu [Límits de projecte](../project-management/create-wbs.md#project-limitations).

## <a name="project-operations-dual-write-map-updates"></a>Actualitzacions de les assignacions de doble escriptura del Project Operations

A la llista següent es mostren les assignacions de doble escriptura que s'han modificat o afegit a la versió de febrer de 2022 del Project Operations.

| Assignació d'entitats | Versió actualitzada | Comentaris |
| --- | --- | --- |
| Entitat d'exportació de despeses del projecte d'integració del Project Operations (msdyn\_expenses) | 1.0.0.3 | Ampliat per a la sincronització d'activitats del projecte al Dataverse. |

Per veure la llista actual i les versions de les assignacions d'escriptura doble del Project Operations, consulteu [Versions de les assignacions d'escriptura doble del Project Operations](../environment/resource-dual-write-maps.md).

Executeu sempre la versió més recent de l'assignació a l'entorn i habiliteu totes les assignacions de taules relacionades a mida que actualitzeu la versió de la solució del Finance i del Dataverse del Project Operations. És possible que algunes característiques i capacitats no funcionin correctament si la versió més recent del mapa no s'activa. Podeu visualitzar la versió activa de l'assignació a la columna **Versió** de la pàgina **Escriptura doble**. Per activar una versió nova de l'assignació, seleccioneu **Versions de l'assignació de la taula**, seleccioneu la versió més recent i després deseu la versió seleccionada. Si heu personalitzat una assignació de taules llesta per al seu ús, torneu a aplicar els canvis. Per a més informació, vegeu [Administració del cicle de vida de les aplicacions](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Si teniu qualsevol problema quan inicieu l'assignació, seguiu les instruccions de la secció [Problemes de columnes de la taula que falten](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) de la guia de detecció d'errors de doble escriptura.

## <a name="quality-updates"></a>Actualitzacions de qualitat

### <a name="project-operations-on-dataverse"></a>Project Operations a Dataverse

| Àrea de característiques | Número de referència | Actualització de qualitat |
| --- | --- | --- |
| Facturació i preus | 2415109 | El valor per defecte del camp **Condicions de pagament d'operacions** ha de ser el registre de client del contracte del projecte i el registre de factura proforma. |
| Facturació i preus | 2497369 | La correcció de materials ha de seguir el valor de data dels paràmetres de **Correcció**. |
| Facturació i preus | 2498697 | S'ha millorat la configuració de seguretat de **Recuperació d'entrada de temps**. |
| Facturació i preus | 2513824 | Per als escenaris basats en recursos, l'identificador de la categoria de transacció no pot superar els 28 caràcters al Project Operations. |
| Facturació i preus | 2517455 | L'acció **Actualitza les transaccions de línia de factura** no s'ha de permetre que s'activi diverses vegades simultànies per a la mateixa factura. |
| Facturació i preus | 2517465 | L'acció **Desactiva els detalls de la línia de factura** està bloquejada perquè no està admesa. |
| Facturació i preus | 2556660 | S'ha corregit la comprovació d'efectivitat de la data que es fa a la llista de preus que s'adjunta a un registre de paràmetres de projecte. |
|   Administració d'oportunitats | 2369202 | S'ha corregit la lògica empresarial que verifica que es poden adjuntar llistes de preus que tenen dates d'efecte superposades al mateix contracte de projecte. |
|   Administració d'oportunitats | 2385965 | S'ha corregit el comportament de la pestanya **Clients** de la pàgina **Contracte del projecte** quan seleccioneu **Desa i tanca**. |
| Temps i despeses | 2538503 | Una tasca de projecte ha d'estar disponible a l'entitat **Valors reals del projecte** després de publicar un informe de despesa. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Administració de projectes i comptabilitat al Dynamics 365 Finance

| Àrea de característiques | Número de referència | Actualització de qualitat |
| --- | --- | --- |
| Administració i comptabilitat de projectes | [615496](https://fix.lcs.dynamics.com/Issue/Details/?bugId=615496) | Durant la importació de notes de crèdit del proveïdor, es produeix un error. El missatge d'error diu que "L'import de retenció no pot ser més que l'import net restant". |
| Administració i comptabilitat de projectes | [619391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=619391) | Si una proposta de factura inclou transaccions de tarifa amb import zero que són valors reals de vendes no facturades, la facturació no es pot produir. |
| Administració i comptabilitat de projectes | [624423](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624423) | El cost comptabilitzat no és correcte després d'actualitzar el preu de compra i s'habilita **Activa l'administració de canvis**.|
| Administració i comptabilitat de projectes | [628386](https://fix.lcs.dynamics.com/Issue/Details/?bugId=628386) | L'estimació de comptabilització d'un projecte de preu fix utilitza una moneda i un import incorrectes en el val de l'estimació, fins i tot quan s'habilita la característica **Habilita la moneda del contracte del projecte per al càlcul de l'estimació**. |
| Administració i comptabilitat de projectes | [629239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=629239) | **ProjDMFDataPopulation\_Extension** no ha de fer una crida per habilitar el seguiment de canvis sense capturar excepcions per a les entitats que tenen claus de configuració que no estan habilitades. |
| Administració i comptabilitat de projectes | [623818](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623818) | La feina per lots es corregeix quan es comptabilitzen diversos diaris avançats i es produeix un error. |
| Viatge i despesa | [616805](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616805) | A causa d'un problema de liquidació que està relacionat amb els avançaments en efectiu dels informes de despeses, l'import de l'impost no es cobreix com a part del bestreta en efectiu. |
| Viatge i despesa | [616959](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616959) | La informació sobre l'impost de vendes no s'inclou a l'informe **Despesa - Transaccions comptabilitzades**. |
| Viatge i despesa | [618943](https://fix.lcs.dynamics.com/Issue/Details/?bugId=618943) | La infracció de la norma de despesa **Rebuts necessaris** mostra incorrectament un advertiment als informes de despesa. |
| Viatge i despesa | [633470](https://fix.lcs.dynamics.com/Issue/Details/?bugId=633470) | Una transacció de projecte no inclou l'impost de vendes no recuperable en l'import total de les vendes quan la transacció és el resultat d'una despesa de quilometratge. |
| Viatge i despesa | [642979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642979) | Quan una línia desglossada té impostos, no podeu canviar la data de la línia desglossada i es produeix un error d'estat del document d'origen. |

## <a name="removed-and-deprecated-features"></a>Característiques suprimides i obsoletes

L'article [Característiques eliminades o obsoletes del Project Operations](removed-depreciated-features-project.md) descriu les característiques que s'han eliminat o que són obsoletes per al Dynamics 365 Project Operations.

- Les característiques suprimides deixen d'estar disponibles al producte.
- Les característiques obsoletes no estan en desenvolupament actiu i podrien suprimir-se en una actualització futura.

Un anunci d'obsolescència apareixerà a l'article [Característiques eliminades o obsoletes del Project Operations](removed-depreciated-features-project.md) 12 mesos abans que se suprimeixi qualsevol característica del producte.

Per als canvis que només afecten el temps de compilació, però que són compatibles binaris amb entorns aïllats i de producció, el temps d'obsolescència serà inferior a 12 mesos. Normalment, aquests canvis són actualitzacions funcionals que s'han de fer al compilador.
