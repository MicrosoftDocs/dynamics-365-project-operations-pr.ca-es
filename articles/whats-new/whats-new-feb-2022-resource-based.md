---
title: 'Novetats de febrer de 2022: Project Operations per a escenaris basats en recursos/no mantinguts en existències'
description: Aquest tema proporciona informació sobre les actualitzacions de qualitat que estan disponibles a la versió de febrer de 2022 de Project Operations per a escenaris basats en recursos / no emmagatzemats.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 76ae00517c857415c89d7a03f421686dad28da93
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8600822"
---
# <a name="whats-new-february-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novetats de febrer de 2022: Project Operations per a escenaris basats en recursos/no mantinguts en existències

*S'aplica a: Project Operations per a escenaris basats en recursos/sense cotització*

Aquest tema s'aplica als components i versions següents de Microsoft Dynamics 365 Project Operations:

- 4.28.0.120 d'operacions del projecte en una Dataverse versió d'entorn
- Gestió de projectes i comptabilitat en un entorn Dynamics 365 Finance versió 10.0.24

## <a name="features-included-in-this-release"></a>Característiques incloses en aquesta versió

- A partir d'aquest llançament, podeu afegir fins a 300 membres de l'equip a un sol projecte. Anteriorment, el límit en el nombre de membres de l'equip era de 150. Per obtenir més informació, vegeu [Límits del projecte](../project-management/create-wbs.md#project-limitations).

## <a name="project-operations-dual-write-map-updates"></a>Actualitzacions del mapa de doble escriptura d'operacions del projecte

La llista següent mostra els mapes de doble escriptura que s'han modificat o afegit a la versió de Project Operations de febrer de 2022.

| Assignació d'entitats | Versió actualitzada | Comentaris |
| --- | --- | --- |
| Entitat exportadora de despeses del projecte d'integració d'operacions del projecte (despeses de msdyn\_) | 1.0.0.3 | Ampliat per a la sincronització de l'activitat del projecte a Dataverse. |

Per veure la llista actual i les versions dels mapes de doble escriptura de Project Operations, vegeu [Les versions del mapa de doble escriptura del Project Operations](../environment/resource-dual-write-maps.md).

Executeu sempre la versió més recent del mapa al vostre entorn i habiliteu tots els mapes de taula relacionats a mesura que actualitzeu la solució d'operacions Dataverse de projecte i la versió de la solució de finançament. És possible que algunes funcions i capacitats no funcionin correctament si l'última versió del mapa no està activada. Podeu visualitzar la versió activa de l'assignació a la columna **Versió** de la pàgina **Escriptura doble**. Per activar una versió nova de l'assignació, seleccioneu **Versions de l'assignació de la taula**, seleccioneu la versió més recent i després deseu la versió seleccionada. Si has personalitzat un mapa de taula fora de caixa, torna a aplicar els canvis. Per a més informació, vegeu [Administració del cicle de vida de les aplicacions](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Si trobeu un problema quan inicieu el mapa, seguiu les instruccions del problema De les columnes de la [taula que falten a la secció mapes](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) de la guia de resolució de problemes d'escriptura dual.

## <a name="quality-updates"></a>Actualitzacions de qualitat

### <a name="project-operations-on-dataverse"></a>Project Operations a Dataverse

| Àrea de característiques | Número de referència | Actualització de qualitat |
| --- | --- | --- |
| Facturació i preus | 2415109 | El valor per defecte del camp Condicions **de** pagament d'operacions ha de ser el registre de client del contracte del projecte i el registre de factura proforma. |
| Facturació i preus | 2497369 | La correcció de material ha de seguir el valor de data en els **paràmetres de correcció**. |
| Facturació i preus | 2498697 | S'ha millorat la configuració de seguretat per a **la recuperació** de l'entrada de temps. |
| Facturació i preus | 2513824 | Per als escenaris basats en recursos, l'identificador de categoria de transacció no pot superar els 28 caràcters a Operacions del projecte. |
| Facturació i preus | 2517455 | No s'ha **de permetre que l'acció Actualitza les transaccions** de línia de factura s'activi diverses vegades simultànies per a la mateixa factura. |
| Facturació i preus | 2517465 | L'acció **Desactiva els detalls de** la línia de factura està bloquejada perquè no és compatible. |
| Facturació i preus | 2556660 | S'ha corregit la comprovació d'eficàcia de la data que es fa a la llista de preus que s'adjunta a un registre de paràmetres del projecte. |
|   Administració d'oportunitats | 2369202 | S'ha corregit la lògica empresarial que verifica que les llistes de preus que tenen dates d'eficàcia superposades es poden adjuntar al mateix contracte de projecte. |
|   Administració d'oportunitats | 2385965 | S'ha corregit el comportament de la **pestanya Clients** de la **pàgina Contracte del projecte** quan seleccioneu **Desa i tanca**. |
| Temps i despeses | 2538503 | Una tasca del projecte ha d'estar disponible a l'entitat **Reals** del projecte després de publicar un informe de despeses. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Gestió de projectes i comptabilitat sobre Dynamics 365 Finance

| Àrea de característiques | Número de referència | Actualització de qualitat |
| --- | --- | --- |
| Administració i comptabilitat de projectes | [615496](https://fix.lcs.dynamics.com/Issue/Details/?bugId=615496) | Durant la importació de notes de crèdit del proveïdor, es produeix un error. El missatge d'error diu: "L'import de retenció no pot ser superior a l'import net restant". |
| Administració i comptabilitat de projectes | [619391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=619391) | Si una proposta de factura inclou les transaccions de comissió en import zero que no siguin reals de vendes no facturades, la facturació no es pot produir. |
| Administració i comptabilitat de projectes | [624423](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624423) | El cost publicat no és correcte després d'actualitzar el preu de compra i **activar la gestió del** canvi.|
| Administració i comptabilitat de projectes | [628386](https://fix.lcs.dynamics.com/Issue/Details/?bugId=628386) | L'estimació de publicació d'un projecte de preu fix utilitza la moneda i l'import incorrectes del val d'estimació, fins i tot quan la funció Habilita la moneda del contracte del **projecte per al càlcul** d'estimacions està habilitada. |
| Administració i comptabilitat de projectes | [629239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=629239) | **ProjDMFDataPopulation\_ Extension** no hauria de fer una crida per habilitar el seguiment de canvis sense detectar excepcions per a les entitats que tenen claus de configuració que no estan habilitades. |
| Administració i comptabilitat de projectes | [623818](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623818) | El treball per lots es fixa quan es publiquen diverses revistes avançades i es produeix un error. |
| Viatge i despesa | [616805](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616805) | A causa d'una qüestió de liquidació relacionada amb les bestretes d'efectiu en els informes de despeses, l'import de l'impost no es cobreix com a part de l'avançament d'efectiu. |
| Viatge i despesa | [616959](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616959) | La informació de l'impost sobre les vendes no s'inclou a l'informe **Despeses - Transaccions** publicades. |
| Viatge i despesa | [618943](https://fix.lcs.dynamics.com/Issue/Details/?bugId=618943) | La **infracció de la política de despeses requerida** per rebuts mostra incorrectament un advertiment sobre els informes de despeses. |
| Viatge i despesa | [633470](https://fix.lcs.dynamics.com/Issue/Details/?bugId=633470) | Una transacció del projecte no inclou l'impost sobre les vendes no recuperable en l'import total de les vendes quan la transacció és el resultat d'una despesa de quilometratge. |
| Viatge i despesa | [642979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642979) | Quan una línia desglossada té impostos, no podeu canviar la data de la línia d'elementització i es produeix un error d'estat del document d'origen. |

## <a name="removed-and-deprecated-features"></a>Característiques eliminades i obsoletes

Les [característiques eliminades o obsoletes del tema Operacions](removed-depreciated-features-project.md) del projecte descriuen les característiques que s'han suprimit o obsolet per a Dynamics 365 Project Operations.

- Les característiques suprimides deixen d'estar disponibles al producte.
- Una característica obsoleta no està en desenvolupament actiu i es pot suprimir en una actualització futura.

Apareixerà un anunci de despreocupat a les funcions Eliminades o obsoletes del [tema Operacions](removed-depreciated-features-project.md) del projecte 12 mesos abans que s'elimini cap característica del producte.

Per trencar els canvis que només afecten el temps de compilació, però són binaris compatibles amb sandbox i entorns de producció, el temps d'espera serà inferior a 12 mesos. Normalment, aquests canvis són actualitzacions funcionals que s'han de fer al compilador.
