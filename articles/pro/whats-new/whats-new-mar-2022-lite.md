---
title: Novetats del març del 2022 - Implementació bàsica del Project Operations
description: Aquest article proporciona informació sobre les actualitzacions de qualitat que estan disponibles a la versió de març de 2022 de la implementació del lite Project Operations.
author: sigitac
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 321d59568bfd33bb00a1500afe514fbecf9a0250
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8934216"
---
# <a name="whats-new-march-2022---project-operations-lite-deployment"></a>Novetats del març del 2022 - Implementació bàsica del Project Operations

_S'aplica a: implementació bàsica: tracte de facturació proforma_

Aquest article s'aplica als components i versions següents de Microsoft Dynamics 365 Project Operations:

- 4.30.0.99 d'operacions del projecte en una Dataverse versió d'entorn

## <a name="features-included-in-this-release"></a>Característiques incloses en aquesta versió

- Subcontractació: experiències de creació i coincidència de factures de proveïdors

## <a name="quality-updates"></a>Actualitzacions de qualitat

| Àrea de característiques | Número de referència | Actualització de qualitat |
| --- | --- | --- |
| Temps i despeses | 2388011 | Mostra els comentaris de rebuig als remitents d'entrades de temps durant l'aprovació massiva. |
| Planificació i seguiment de projectes | 2495294 | Els detalls del projecte no s'han d'editar a la pàgina Detalls **de la** tasca. |
| Facturació i preus | 2499605 | Les fites del contracte que es creen a partir de fites de cotització es marquen incorrectament com a només de lectura. |
| Planificació i seguiment de projectes | 2506050 | El conjunt d'operacions romandrà pendent durant una hora si no hi ha cap canvi per desar. El conjunt es marca falsament com a **Fallit**, mentre que s'ha de completar immediatament. |
| Facturació i preus | 2507401 | Les unitats de contractació per defecte no s'han introduït correctament en projectes a causa d'una memòria cau incorrecta. |
| Facturació i preus | 2541660 | **La validació de creació** de comandes de vendes en doble escriptura ha de ser només per a comandes basades en projectes. |
| Facturació i preus | 2552745 | Els impostos no es divideixen entre els clients que han configurat regles de facturació dividides. |
| Facturació i preus | 2558859 | S'han millorat els missatges d'error quan es configuren les dimensions de preus. |
| Facturació i preus | 2558933 | **La importació des de les estimacions** del projecte falla quan **s'afegeix el projecte\_ msdyn** com a dimensió de preus. |
| Facturació i preus | 2559101 | La supressió del paràmetre del projecte no està bloquejada i causa problemes. |
|   Administració d'oportunitats | 2570390 | El connector de doble escriptura força el tipus de compte a les cotitzacions, comandes i oportunitats de ser **client**, fins i tot quan aquest tipus de compte no és correcte. |
| Facturació i preus | 2586097 | Els reals de cost facturat dividits no s'inverteixen quan un projecte s'elimina d'una línia de contracte del projecte. |
| Facturació i preus | 2589619 | L'impost sobre el material d'escriptura es propaga a les vendes reals no facturades i a la factura. |
|   Administració d'oportunitats | 2594015 | Un pressupost no es pot tancar com a guanyat per als clients que tinguin condicions **de pagament Net60**. |
| Planificació i seguiment de projectes | 2595841 | Al Projecte per al web, els usuaris reben un missatge d'error sobre un inici **real de l'msdyn\_ que falta** quan creen una sol·licitud de recurs nova. |
| Temps i despesa | 2602511 | El **camp Rebutjat per** a les entrades de temps mostra **Sistema** en lloc d'un usuari amb nom com a rebutjador. |
| Temps i despesa | 2602528 | Un aprovador de projectes pot aprovar temps en projectes en què no es mostreja com a aprovador. |
| Facturació i preus | 2608550 | Es pot confirmar una factura de correcció encara que no hi hagi canvis en l'original. |

## <a name="removed-and-deprecated-features"></a>Característiques eliminades i obsoletes

Les [característiques eliminades o obsoletes de l'article Operacions del](../../whats-new/removed-depreciated-features-project.md) projecte descriuen les característiques que s'han suprimit o obsolet per a Dynamics 365 Project Operations.

- Les característiques suprimides deixen d'estar disponibles al producte.
- Una característica obsoleta no està en desenvolupament actiu i es pot suprimir en una actualització futura.

Apareixerà un anunci d'obsolet a les funcions eliminades o obsoletes de l'article [d'operacions](../../whats-new/removed-depreciated-features-project.md) del projecte 12 mesos abans que s'elimini cap característica del producte.
