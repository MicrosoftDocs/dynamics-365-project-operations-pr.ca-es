---
title: 'Novetats de novembre de 2021: Project Operations per a escenaris basats en recursos/no mantinguts en existències'
description: Aquest tema proporciona informació sobre les actualitzacions de qualitat que estan disponibles a la versió de novembre de 2021 de Project Operations per a escenaris basats en recursos / no emmagatzemats.
author: sigitac
ms.date: 11/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: fb9dad5b04ef2933ed8a8d8211f888f13df5ba40
ms.sourcegitcommit: 9d20e7738cce195d344f5925a115741a1ce3ca36
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 12/21/2021
ms.locfileid: "7942873"
---
# <a name="whats-new-november-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novetats de novembre de 2021: Project Operations per a escenaris basats en recursos/no mantinguts en existències

*S'aplica a: Project Operations per a escenaris basats en recursos/sense cotització*

Aquest tema s'aplica als components i versions següents de Dynamics 365 Project Operations Microsoft:

- 4.26.0.145, 4.26.0.148, 4.26.0.150, 4.26.0.155 d'Operacions del projecte en una Dataverse versió d'entorn
- Gestió de projectes i comptabilitat en un Dynamics 365 Finance entorn versió 10.0.22

## <a name="features-included-in-this-release"></a>Característiques incloses en aquesta versió

En aquesta versió s'inclouen les característiques següents:

- Les interfícies de programació d'aplicacions de planificació de projectes (API) ara admeten la possibilitat de crear i eliminar cubs del projecte.

## <a name="project-operations-dual-write-maps-updates"></a>Actualitzacions de les assignacions de doble ecriptura del Project Operations

En aquesta versió no hi ha actualitzacions per a les assignacions d'escriptura doble del Project Operations. Per a una llista actual i versions de les assignacions d'escriptura doble del Project Operations, consulteu [Versions de les assignacions d'escriptura doble del Project Operations](/dynamics365/project-operations/environment/resource-dual-write-maps).

Executeu sempre la versió més recent del mapa al vostre entorn i habiliteu tots els mapes de taula relacionats a mesura que actualitzeu la solució d'operacions de projecte Dataverse i la versió de la solució de finançament. És possible que algunes funcions i capacitats no funcionin correctament si l'última versió del mapa no està activada. Podeu visualitzar la versió activa de l'assignació a la columna **Versió** de la pàgina **Escriptura doble**. Per activar una versió nova de l'assignació, seleccioneu **Versions de l'assignació de la taula**, seleccioneu la versió més recent i després deseu la versió seleccionada. Si has personalitzat un mapa de taula fora de caixa, torna a aplicar els canvis. Per a més informació, vegeu [Administració del cicle de vida de les aplicacions](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Si trobeu un problema quan inicieu el mapa, seguiu les instruccions del problema de columnes de [la taula que falten a la secció](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) mapes de la guia de resolució de problemes de doble escriptura.

## <a name="quality-updates"></a>Actualitzacions de qualitat

### <a name="project-operations-in-dataverse"></a>Operacions del projecte a Dataverse

| Àrea de característiques | Número de referència | Actualització de qualitat |
| --- | --- | --- |
| Facturació i preus | 2240080 | El **camp Condicions de pagament** no s'ha de duplicar a la factura proforma. |
| Facturació i preus | 2358236 | La correcció de factures ha de permetre correccions que tinguin línies de preu zero. |
| Administració de recursos | 2410072 | Permet la configuració d'un recurs assignat a la tasca com a administrador de projectes. |
| Facturació i preus | 2430234 | Solucionar un problema de càlcul del rendiment dels costos. |
| Temps i despesa | 2436978 | Permet que el temps s'introdueixi en format hh:mm. |
| Facturació i preus | 2448623 | Permet que les llistes de preus s'actualitzin després d'associar-se amb una unitat organitzativa. |
| Temps i despesa | 2460396 | Permet que se suprimeixi una entrada de temps esborrant la cel·la. |
| Facturació i preus | 2467386 | Permet que se suprimeixi un projecte que té una tasca, fins i tot quan la tasca està associada amb una oferta guanyada. |
| Temps i despesa | 2461744 | La **visualització d'aprovació El meu error** només conté aprovacions de projectes a la fase **Enviada**. |
| Temps i despesa | 2464082 | Suprimiu l'enllaç de les aprovacions del projecte al conjunt d'aprovació quan coincideixi un estat de destinació. |
| Temps i despesa | 2468108 | La feina De planificació no ha de definir un **estat de processament per al conjunt** d'aprovació. |
| Temps i despesa | 2471503 | Suprimeix els conjunts d'aprovació que falten set dies. |
| Facturació i preus | 2480687 | La referència de la línia d'oferta no s'ha de suprimir quan es crea una fita de línia d'oferta. |

### <a name="project-management-and-accounting-in-finance"></a>Gestió de projectes i comptabilitat en Finances

| Àrea de característiques | Número de referència | Actualització de qualitat |
| --- | --- | --- |
| Administració i comptabilitat de projectes | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | Els imports retinguts del proveïdor a les transaccions de despeses del projecte no es mostren a la llista de transaccions. |
| Administració i comptabilitat de projectes | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | La factura del proveïdor d'interempresa es trenca quan s'activa la integració de factures del proveïdor. |
| Administració i comptabilitat de projectes | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | Les condicions de pagament de les factures del projecte no funcionen com s'esperava. |
| Administració i comptabilitat de projectes | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | Quan es publica la retenció del proveïdor, la publicació del val té línies addicionals que són incorrectes. |
| Administració i comptabilitat de projectes | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | Quan es publica el diari d'integració d'operacions del projecte, falla a causa de les dimensions que falten per a un compte al que no s'està publicant. |
| Administració i comptabilitat de projectes | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | La **pestanya** Projecte no es pot editar en una factura pendent del proveïdor quan la categoria d'adquisició s'assigna a l'element. |
| Administració i comptabilitat de projectes | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Falta la subfinestra de navegació si no heu iniciat la sessió a Operacions del projecte Dataverse. |
| Administració i comptabilitat de projectes | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Quan publiqueu els ingressos d'una factura de projecte en un cas de retenció aplicat, es produeix un problema perquè les transaccions del val no es equilibren. |
| Administració i comptabilitat de projectes | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | La creació d'una estimació després de publicar una proposta de factura bloqueja les línies de correcció de la importació. |
| Administració i comptabilitat de projectes | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | No hauria de ser possible la modificació d'un registre de fita totalment facturat. |
| Viatge i despesa | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Tots els informes de despeses són visibles quan cerqueu una categoria a l'aplicació Mòbil Despeses. |
| Viatge i despesa | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | Els imports incorrectes en les transaccions del proveïdor i les transaccions d'impostos sobre les vendes es publiquen a partir d'una despesa que es crea a partir d'una transacció amb targeta de crèdit. |
| Viatge i despesa | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Es produeix un advertiment irrellevant quan actualitzeu la **pàgina De l'informe de** despeses. |
| Viatge i despesa | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | L'aprovador provisional incorrecte s'utilitza quan suprimiu un aprovador provisional i torneu a enviar un informe de despeses a través del flux de treball. |
| Viatge i despesa | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Es produeix un error de publicació relacionat amb la configuració del quilometratge. |
