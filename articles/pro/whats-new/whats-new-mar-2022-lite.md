---
title: Novetats del març del 2022 - Implementació bàsica del Project Operations
description: Aquest article proporciona informació sobre les actualitzacions de qualitat que estan disponibles en el llançament de març de 2022 de la implementació bàsica del Project Operations.
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

Aquest article s'aplica als components i les versions següents del Microsoft Dynamics 365 Project Operations:

- Project Operations en un entorn del Dataverse, versió 4.30.0.99

## <a name="features-included-in-this-release"></a>Característiques incloses en aquesta versió

- Subcontractació: creació de la factura del proveïdor i experiències coincidents

## <a name="quality-updates"></a>Actualitzacions de qualitat

| Àrea de característiques | Número de referència | Actualització de qualitat |
| --- | --- | --- |
| Temps i despeses | 2388011 | Mostra els comentaris de rebuig a les persones que envien les entrades de temps durant l'aprovació massiva. |
| Planificació i seguiment de projectes | 2495294 | Els detalls del projecte no s'han de poder editar a la pàgina de **Detalls de la tasca**. |
| Facturació i preus | 2499605 | Les fites de contracte creades a partir de les fites d'oferta estan marcades incorrectament com a només de lectura. |
| Planificació i seguiment de projectes | 2506050 | El conjunt d'operacions continua pendent durant una hora si no hi ha cap canvi per desar. El conjunt s'ha marcat erròniament com a **Error**, però s'hauria d'haver completat immediatament. |
| Facturació i preus | 2507401 | Les unitats de contracte per defecte s'introdueixen incorrectament en projectes a causa de l'emmagatzematge incorrecte a la memòria cau. |
| Facturació i preus | 2541660 | La **Validació de creació de comanda de venda** en mode de doble escriptura ha de ser només per a comandes basades en projectes. |
| Facturació i preus | 2552745 | Els impostos no es divideixen entre els clients que han configurat regles de facturació amb divisió. |
| Facturació i preus | 2558859 | S'han millorat els missatges d'error en la configuració de les dimensions de preus. |
| Facturació i preus | 2558933 | **Importa des d'estimacions del projecte** falla quan s'afegeix **msdyn\_project** com a dimensió de preus. |
| Facturació i preus | 2559101 | La supressió de paràmetres de projecte no està bloquejada i provoca problemes. |
|   Administració d'oportunitats | 2570390 | El complement de doble escriptura aplica el tipus de compte **Client** a les ofertes, comandes i oportunitats, encara que aquest tipus de compte no sigui correcte. |
| Facturació i preus | 2586097 | Els valors reals de cost facturats fraccionats no es reverteixen quan s'elimina un projecte d'una línia de contracte del projecte. |
| Facturació i preus | 2589619 | L'impost sobre el material fora de catàleg es propaga als valors reals de vendes no facturades i a la factura. |
|   Administració d'oportunitats | 2594015 | L'oferta no es pot tancar com a guanyada per als clients que tenen condicions de pagament **Net60**. |
| Planificació i seguiment de projectes | 2595841 | A Project for the Web, els usuaris reben un missatge d'error sobre un fitxer **msdyn\_actualstart** que falta quan creen una sol·licitud de recurs nova. |
| Temps i despesa | 2602511 | El camp **Rebutjat per** a les entrades de temps mostra **Sistema** en comptes d'un usuari amb nom com a persona que les rebutja. |
| Temps i despesa | 2602528 | Un aprovador del projecte pot aprovar el temps dels projectes en què no apareix com a aprovador. |
| Facturació i preus | 2608550 | Es pot confirmar una factura de correcció encara que no hi hagi canvis en l'original. |

## <a name="removed-and-deprecated-features"></a>Característiques suprimides i obsoletes

L'article [Característiques eliminades o obsoletes del Project Operations](../../whats-new/removed-depreciated-features-project.md) descriu les característiques que s'han eliminat o que són obsoletes per al Dynamics 365 Project Operations.

- Les característiques suprimides deixen d'estar disponibles al producte.
- Les característiques obsoletes no estan en desenvolupament actiu i podrien suprimir-se en una actualització futura.

Un anunci d'obsolescència apareixerà a l'article [Característiques eliminades o obsoletes del Project Operations](../../whats-new/removed-depreciated-features-project.md) 12 mesos abans que se suprimeixi qualsevol característica del producte.
