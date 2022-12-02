---
title: 'Novetats del maig de 2021: Project Operations per a escenaris basats en recursos/no mantinguts en existències'
description: Aquest article proporciona informació sobre les actualitzacions de qualitat disponibles a la versió del maig de 2021 del Project Operations per a escenaris basats en recursos/no mantinguts en existències.
author: sigitac
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: cc5e8104702951fd787d02407d26671e46d44f0c
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029977"
---
# <a name="whats-new-may-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novetats del maig de 2021: Project Operations per a escenaris basats en recursos/no mantinguts en existències

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

Aquest article s'aplica als components i versions següents del Dynamics 365 Project Operations:

- Project Operations a l'entorn del Dynamics 365 Dataverse, versió 4.10.0.186
- Administració de projectes i comptabilitat en entorns d'aplicacions de finances i operacions versió 10.0.18

## <a name="features-included-in-this-release"></a>Característiques incloses en aquesta versió

En aquesta versió s'inclouen les característiques següents:

- [Modes de planificació](../project-management/scheduling-modes.md): els administradors de projectes poden definir si un projecte s'ha d'administrar amb el mode de planificació de duració fixa, treball fix o unitats fixes.
- [Configuració del quilometratge amb nivells de taxa de quilometratge](../expense/set-up-mileage.md): actualitzeu els nivells de taxa de quilometratge per als informes de despeses dels empleats.

## <a name="project-operations-dual-write-maps-updates"></a>Actualitzacions de les assignacions de doble ecriptura del Project Operations

A la llista següent es mostren les assignacions de doble escriptura que s'han modificat o afegit a la versió de maig de 2021 del Project Operations.

| Assignació d'entitats | Versió actualitzada | Comentaris |
| --- | --- | --- |
| Origen del fons del projecte (msdyn\_projectcontractsplitbillingrules) | 1.0.0.2 | Sincronització de les condicions de pagament dels clients del contracte del projecte. |
| Proposta de factura de projecte V2 (factures) | 1.0.0.3 | Sincronització de les condicions de pagament de factures proforma. |
| Entitat d'exportació de la línia de factura del proveïdor del projecte de la integració del Project Operations (msdyn\_projectvendorinvoicelines) | 1.0.0.1 | Actualitzacions de qualitat |
| Projectes V2 (msdyn\_projects) | 1.0.0.2 | Actualitzacions de qualitat |

Executeu sempre la versió més recent de l'assignació a l'entorn i habiliteu totes les assignacions de taules relacionades a mida que actualitzeu la versió de la solució del Project Operations al Dataverse i de les aplicacions de finances i operacions. És possible que algunes característiques i capacitats no funcionin correctament si la versió més recent del mapa no s'activa. Podeu veure la versió activa de l'assignació a la columna **Versió** de la pàgina **Escriptura doble**. Per activar una versió nova de l'assignació, seleccioneu **Versions de l'assignació de la taula**, seleccioneu la versió més recent i després deseu la versió seleccionada. Si heu personalitzat una assignació de taules llesta per al seu ús, torneu a aplicar els canvis. Per a més informació, vegeu [Administració del cicle de vida de les aplicacions](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Si teniu qualsevol problema relacionat amb l'inici de l'assignació, seguiu les instruccions de la secció [Problemes de columnes de la taula que falten](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) de la guia de detecció d'errors de doble escriptura.

## <a name="quality-updates"></a>Actualitzacions de qualitat

### <a name="project-operations-on-dataverse"></a>Project Operations a Dataverse

| **Àrea de característiques** | **Número de referència** | **Actualització de qualitat** |
| --- | --- | --- |
| Facturació i preus | 2227635 | Els valors dels camps **Grup d'unitats** i **Unitat** per defecte són el producte de la quadrícula **Estimacions de materials**. |
| Facturació i preus | 2234127 | El camp **ID de la tasca** ara s'integra correctament amb els valors reals del projecte del Dataverse quan es comptabilitza una factura del proveïdor. |
| Facturació i preus | 2235564 | Si deseu la línia del llibre diari, s'assegura que la moneda mostrada a l'entrada de la línia de la línia del llibre diari coincideix amb la moneda per defecte a la línia després de desar-la. |
| Facturació i preus | 2246671 | Fer una transacció no imputable durant la facturació inverteix el registre de vendes no facturat original i crea un nou registre de vendes no facturades com a no imputable. |
| Facturació i preus | 2264042 | No s'ha de bloquejar la correcció de la factura vàlida si hi ha un detall de correcció de la factura que no és vàlid a l'entorn. |
| Facturació i preus | 2146367 | L'assignació de doble escriptura de la capçalera de la factura del projecte s'amplia per incloure termes de pagament. |
|   Administració d'oportunitats | 2086888 | No afegiu funcions i categories desactivades abans de copiar una oferta a funcions i categories imputables d'una oferta nova copiada. |
|   Administració d'oportunitats | 2234376 | Els camps només de lectura apareixen de color gris a la quadrícula **Estimacions de materials**. |
|   Administració d'oportunitats | 2238337 | Una oferta basada en un contacte es pot desar encara que no estigui associada a una llista de preus del projecte. |
|   Administració d'oportunitats | 2239810 | El tancament d'una oferta com a perduda també tanca el projecte associat i cancel·la les reserves. |
| Planificació i seguiment de projectes | 2099559 | S'han afegit validacions addicionals per a l'estat del sistema abans que s'obri la quadrícula **Tasques del projecte**. |
| Planificació i seguiment de projectes | 2178987 | S'ha corregit un error transitori que es produeix en seleccionar **Fase següent** a la pàgina **Projecte**. |
| Administració de recursos | 2224817 | La funcionalitat per ampliar les reserves canvia per defecte a l'estat de reserva correcte. |
| Entrada de temps | 2202476 | La pàgina **Entrada de temps** utilitza ara el control de quadrícula reactiva i corregeix problemes com ara la mala alineació de la quadrícula. |
| Entrada de temps | 2223377 | L'entrada de temps s'amaga de la secció **Relacionat** a la pàgina **Recurs reservable** per evitar la confusió amb la usabilitat. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Administració de projectes i comptabilitat al Dynamics 365 Finance

| Àrea de característiques | Número de referència | Actualització de qualitat |
| --- | --- | --- |
| Administració i comptabilitat de projectes | [545878](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545878) | Project Operations per a escenaris basats en recursos: a causa d'un error d'integració, no podeu convertir una oferta en guanyada. |
| Administració i comptabilitat de projectes | [546604](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546604) | Project Operations: es produeix un error quan intenteu associar una línia de contracte a un identificador de projecte a causa de la comprovació de línies de contracte i tipus de transaccions superposats. |
| Administració i comptabilitat de projectes | [547440](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547440) | **ProjCDSProjectContractEntity** defineix l'adreça de factura de la font de finançament d'un client diferent. |
| Viatge i despesa | [480451](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480451) | Es pot produir un error de publicació relacionat amb la configuració del quilometratge. |
| Viatge i despesa | [522084](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522084) | La funcionalitat **Divisó en personal** no funciona per a les transaccions de despeses de moneda estrangera. |
| Viatge i despesa | [523938](https://fix.lcs.dynamics.com/Issue/Details/?bugId=523938) | Els valors del desplegable de categoria de despeses mostren categories incorrectes per als delegats independentment de si es configuren com a recurs. |
| Viatge i despesa | [539266](https://fix.lcs.dynamics.com/Issue/Details/?bugId=539266) | No podeu desar un informe de despesa entre empresa a causa d'un error de **validació de recurs o categoria**. |
| Viatge i despesa | [532610](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532610) | El càlcul de la taxa de quilometratge incorrecte a la publicació de l'informe de despeses té línies dividides. |
| Viatge i despesa | [537404](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537404) | No podeu publicar un informe de despeses entre empreses quan l'impost de vendes està inclòs i el tipus de compte de desplaçament del mètode de pagament és **Treballador**. |
| Viatge i despesa | [542927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=542927) | L'entitat de dades **TrvRequisitionLine** de reversió i l'índex únic estan associats. |
| Viatge i despesa | [543239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543239) | L'informe de despeses admet la creació i l'actualització de la línia de documents d'origen. |
| Viatge i despesa | [544323](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544323) | Es mostra un llibre diari de llibre major auxiliar incorrecte en un escenari entre empreses si l'impost de vendes es comptabilitza a l'entitat legal de destinació. |
| Viatge i despesa | [546877](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546877) | Project Operations: l'estimació de despeses no se suprimeix de Finance quan se suprimeix del Dataverse. |
| Viatge i despesa | [550575](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550575) | Quan la categoria de despesa és una categoria que no és de projecte, les condicions financeres seleccionades a la pàgina **Despeses** no es copien a l'informe de despeses. |
