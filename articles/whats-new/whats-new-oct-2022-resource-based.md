---
title: "Novetats d'octubre de 2022: Project Operations per a escenaris basats en recursos/no mantinguts en existències"
description: Aquest article proporciona informació sobre les actualitzacions de qualitat disponibles a la versió d'octubre de 2022 de Microsoft Dynamics 365 Project Operations per a escenaris basats en recursos o no emmagatzemats.
author: ramagadu
ms.date: 11/17/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 392a12d6954c2390e5bad8e8e36cf58b7a1d0749
ms.sourcegitcommit: 1f162707ac342343fb5390fb9ae335e4cea4f3f2
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 11/29/2022
ms.locfileid: "9806718"
---
# <a name="whats-new-october-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novetats d'octubre de 2022: Project Operations per a escenaris basats en recursos/no mantinguts en existències

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

Aquest article s'aplica als components i les versions següents del Microsoft Dynamics 365 Project Operations:

- Project Operations en un entorn del Dataverse, versió 4.57.0.176
- Administració de projectes i comptabilitat en un entorn del Dynamics 365 Finance, versió 10.0.30

## <a name="features-included-in-this-release"></a>Característiques incloses en aquesta versió

| Àrea de característiques | Nom de la característica | Més informació |
| --- | --- | --- |
| Planificació i seguiment de projectes | **Planificació externa d'operacions del projecte**<br>El mode de planificació externa permet als clients crear, actualitzar i suprimir de forma nativa entitats relacionades amb les estructures del desglossament del treball (WBS) mitjançant l'ús de les API natives Dataverse , sense els límits actuals que el Project for the Web aplica. | [Programació externa](/dynamics365/project-operations/project-management/external-scheduling) |
| Implementació i configuració | <p>**Permetre als clients triar el tipus d'implementació**<br>Les actualitzacions basades en el producte (PDU) de Project Operations s'utilitzen per instal·lar automàticament la solució de doble escriptura del Project Operations quan s'instal·len solucions de nucli i orquestració de doble escriptura a l'entorn.</p><p>Aquesta característica introdueix un paràmetre de comportament **d'actualització de la solució nou** als paràmetres del projecte. Quan aquest paràmetre només **s'estableix com a** Lite, els PUD ja no instal·laran automàticament la solució Project Operations Dual-write, fins i tot si les solucions de nucli i orquestració de doble escriptura estan instal·lades a l'entorn. Aquest comportament beneficiarà els clients que tinguin previst utilitzar solucions d'escriptura dual per integrar comandes de vendes a les aplicacions de finances i operacions, però vulguin utilitzar Project Operations en mode Lite (és a dir, sense integració a les aplicacions de finances i operacions).</p> | |
| Facturació i preus | <p>**Conversió de divises per a operacions de venda sense cost en entorns integrats**<br>Per als clients que utilitzen Project Operations integrats amb aplicacions financeres i operatives (és a dir, en el tipus de distribució de recursos o no estocades), els tipus de canvi solen dominar-se en aplicacions de finances i operacions. Tanmateix, si una categoria de despesa s'ha de valorar mitjançant el mètode de càlcul de preus "a cost" o "marcatge sobre el cost" quan es factura al client, el tipus de canvi que s'utilitza per calcular l'import de les vendes utilitza els tipus de canvi, no els tipus Dataverse de canvi de les aplicacions de finances i operacions.</p><p>Aquesta característica introdueix un paràmetre nou **de comportament** de conversió de moneda als paràmetres del projecte. Quan aquest paràmetre s'estableix com a **Ampliat amb retrocés**, els imports de vendes no reduïts de les transaccions de despeses es calculen mitjançant l'ús dels tipus de canvi de les aplicacions de finances i operacions.</p> | |

## <a name="project-operations-dual-write-maps-updates"></a>Actualitzacions de les assignacions de doble ecriptura del Project Operations

En aquesta versió no hi ha actualitzacions per a les assignacions d'escriptura doble del Project Operations. Per a una llista actual i versions de les assignacions d'escriptura doble del Project Operations, consulteu [Versions de les assignacions d'escriptura doble del Project Operations](../environment/resource-dual-write-maps.md).

Executeu sempre la versió més recent de l'assignació a l'entorn i habiliteu totes les assignacions de taules relacionades a mida que actualitzeu la versió de la solució del Finance i del Dataverse del Project Operations. És possible que algunes característiques i capacitats no funcionin correctament si la versió més recent del mapa no s'activa. Podeu visualitzar la versió activa de l'assignació a la columna **Versió** de la pàgina **Escriptura doble**. Per activar una versió nova de l'assignació, seleccioneu **Versions de l'assignació de la taula**, seleccioneu la versió més recent i després deseu la versió seleccionada. Si heu personalitzat una assignació de taules llesta per al seu ús, torneu a aplicar els canvis. Per a més informació, vegeu [Administració del cicle de vida de les aplicacions](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Si teniu qualsevol problema quan inicieu l'assignació, seguiu les instruccions de la secció [Problemes de columnes de la taula que falten](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) de la guia de detecció d'errors de doble escriptura.

## <a name="quality-updates"></a>Actualitzacions de qualitat

### <a name="project-operations-on-dataverse"></a>Project Operations a Dataverse

| Àrea de característiques | Número de referència | Actualització de qualitat |
| --- | --- | --- |
| Facturació i preus | 2316317 | El sistema permet crear factures que no tinguin transaccions repercutibles. |
| Facturació i preus | 2737300 | Valideu la **disponibilitat dels camps Client** abans d'accedir al formulari. |
| Facturació i preus | 2744948 | Afegiu una comprovació nul·la per al mètode de facturació. |
| Facturació i preus | 2763515 | Gestió d'errors de referència nul·la quan falti el contracte de compravenda de la factura. |
| Facturació i preus | 2844301 | La creació de factures per lots falla a causa d'un error. |
| Facturació i preus | 2845869 | Emmagatzematge incorrecte del Servei de l'Organització. |
| Facturació i preus | 2853729 | Els detalls de la funció i del preu s'actualitzen quan es modifica el tipus de facturació. |
| Facturació i preus | 2940350 | Quan els reals tenen un preu, només s'han d'introduir automàticament les llistes de preus actives. |
| Implementació i configuració | 3001206 | L'entitat msdyn\_ replaylogheader està impedint les actualitzacions de les organitzacions de clients. |
| Administració d'oportunitats | 2755582 | Les excepcions de referència nul·les es gestionen a l'ajudant de la regla de facturació dividida. |
| Administració d'oportunitats | 2761477 | Quan s'utilitza la facturació dividida, la supressió d'una fita (capçalera) deixa fites òrfenes. |
| Administració d'oportunitats | 2767595 | Quan s'obre un registre d'ús de material al formulari principal, el recurs que es pot reservar per al registre es canvia a l'usuari que ha iniciat la sessió. |
| Planificació i seguiment de projectes | 2790384 | El temps d'espera pendent d'OperacióSet és massa curt. |
| Planificació i seguiment de projectes | 2957840 | Les tasques no es poden desar i les columnes no es poden afegir a la pàgina Tasques **de l'Operacions** integrades del projecte. |
| Administració de recursos | 2751560 | Unitats d'organització preferides inconsistents en requisit de recursos. |
| Subcontractació | 2853245 | La coincidència amb els reals de Vendor Invoice Line no actualitza l'estat de verificació si una línia de contracte ja està vinculada a la línia de factures del proveïdor. |
| Subcontractació | 2907231 | La fase de procés de les factures dels proveïdors no es pot avançar. |
| Temps i despesa | 2867363 | Els registres no queden fora de la visualització Absències / Vacances per a l'aprovació quan estan a la cua per a la seva aprovació. |
| Temps i despesa | 2894405 | TESA: El directori POC no utilitzat està causant problemes de compliment. |

### <a name="project-management-and-accounting-in-finance"></a>Administració de projectes i comptabilitat al Finance

Per obtenir informació sobre les correccions d'errors incloses en aquesta actualització, inicieu la sessió al Microsoft Dynamics Lifecycle Services i vegeu l'[article de la KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468).
